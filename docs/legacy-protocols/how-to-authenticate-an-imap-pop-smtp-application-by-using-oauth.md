---
title: Autenticar una conexión IMAP, POP o SMTP con OAuth
description: Obtenga información sobre cómo usar la autenticación de OAuth con las aplicaciones IMAP, POP y SMTP.
author: svpsiva
ms.date: 07/08/2021
ms.audience: Developer
ms.openlocfilehash: cfc9de18a53ce4cfdd8535f26fe3b04aab9cde55
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59531326"
---
# <a name="authenticate-an-imap-pop-or-smtp-connection-using-oauth"></a>Autenticar una conexión IMAP, POP o SMTP con OAuth

Obtenga información sobre cómo usar la autenticación de OAuth para conectarse con los protocolos IMAP, POP o SMTP y obtener acceso a los datos de correo electrónico Office 365 usuarios.

> La compatibilidad de OAuth2 con los protocolos IMAP, POP y SMTP, como se describe a continuación, es compatible con los usuarios de Microsoft 365 (que incluye Office en la Web) y Outlook.com.

Si no está familiarizado con el protocolo OAuth 2.0, empiece por leer el protocolo [OAuth 2.0](/azure/active-directory/develop/active-directory-v2-protocols)en Plataforma de identidad de Microsoft información general. Para obtener más información sobre las bibliotecas de autenticación de Microsoft (MSAL), que implementan el protocolo OAuth 2.0 para autenticar usuarios y obtener acceso a API seguras, lea la introducción a [MSAL](/azure/active-directory/develop/msal-overview).

Puede usar el servicio de autenticación de OAuth proporcionado por Azure Active Directory para permitir que la aplicación se conecte con los protocolos IMAP, POP o SMTP para obtener acceso a Exchange Online en Office 365. Para usar OAuth con la aplicación, debe:

1. [Registrar la aplicación](#register-your-application) con Azure Active Directory.
1. [Configure la aplicación](#configure-your-application) en Azure Active Directory.
1. [Obtener un token de acceso](#get-an-access-token) desde un servidor de tokens.
1. [Autenticar solicitudes de conexión](#authenticate-connection-requests) con un token de acceso.

## <a name="register-your-application"></a>Registrar su aplicación

Para usar OAuth, una aplicación debe registrarse con Azure Active Directory.

Siga las instrucciones que se [enumeran en Registrar una aplicación con el Plataforma de identidad de Microsoft](/azure/active-directory/develop/quickstart-register-app) para crear una nueva aplicación.

## <a name="get-an-access-token"></a>Obtener un token de acceso

Puede usar una de nuestras bibliotecas de [cliente MSAL](/azure/active-directory/develop/msal-overview) para capturar un token de acceso de la aplicación cliente.

Como alternativa, puede seleccionar un flujo adecuado de la siguiente lista y seguir los pasos correspondientes para llamar a las API rest de la plataforma de identidad subyacente y recuperar un token de acceso.

1. [Flujo de código de autorización de OAuth2](/azure/active-directory/develop/v2-oauth2-auth-code-flow)
1. [Flujo de concesión de autorización de dispositivo de OAuth2](/azure/active-directory/develop/v2-oauth2-device-code)

No se admite el acceso de OAuth a los protocolos IMAP, POP, SMTP AUTH mediante el flujo de concesión de credenciales de cliente de OAuth2. Si la aplicación necesita acceso persistente a todos los buzones de una organización de Microsoft 365, se recomienda usar las API de Microsoft Graph que permiten el acceso sin un usuario, habilitar permisos pormenorizados y permitir a los administradores el ámbito de dicho acceso a un conjunto específico de buzones.

Asegúrese de especificar todos los ámbitos, incluidas Outlook de recursos, al autorizar la aplicación y solicitar un token de acceso.

| Protocolo  | Cadena de ámbito de permisos |
|-----------|-------------------------|
| IMAP      | `https://outlook.office.com/IMAP.AccessAsUser.All` |
| POP       | `https://outlook.office.com/POP.AccessAsUser.All`  |
| AUTENTICACIÓN SMTP | `https://outlook.office.com/SMTP.Send`             |

Además, puede solicitar el [ámbito offline_access](/azure/active-directory/develop/v2-permissions-and-consent#offline_access) usuario. Cuando un usuario aprueba el offline_access, la aplicación puede recibir tokens de actualización del punto de conexión Plataforma de identidad de Microsoft token. Los tokens de actualización son de larga duración. La aplicación puede obtener nuevos tokens de acceso a medida que expiran los antiguos.

## <a name="authenticate-connection-requests"></a>Autenticar solicitudes de conexión

Puede iniciar una conexión a los servidores Office 365 correo electrónico mediante la configuración de correo electrónico IMAP y [POP para Office 365](https://support.office.com/article/pop-and-imap-email-settings-for-outlook-8361e398-8af4-4e97-b147-6c6c4ac95353).

### <a name="sasl-xoauth2"></a>SASL XOAUTH2

La integración de OAuth con requiere que la aplicación use el formato XOAUTH2 sasl para codificar y transmitir el token de acceso. SASL XOAUTH2 codifica el nombre de usuario y el token de acceso en el siguiente formato:

```text
base64("user=" + userName + "^Aauth=Bearer " + accessToken + "^A^A")
```

`^A`representa un **control**  +  **A** ( `%x01` ).

Por ejemplo, el formato XOAUTH2 sasl para acceder `test@contoso.onmicrosoft.com` con token de acceso `EwBAAl3BAAUFFpUAo7J3Ve0bjLBWZWCclRC3EoAA` es:

```text
base64("user=test@contoso.onmicrosoft.com^Aauth=Bearer EwBAAl3BAAUFFpUAo7J3Ve0bjLBWZWCclRC3EoAA^A^A")
```

Después de la codificación base64, esto se traduce en la siguiente cadena. Tenga en cuenta que los saltos de línea se insertan para mejorar la legibilidad.

```text
dXNlcj10ZXN0QGNvbnRvc28ub25taWNyb3NvZnQuY29tAWF1dGg9QmVhcmVy
IEV3QkFBbDNCQUFVRkZwVUFvN0ozVmUwYmpMQldaV0NjbFJDM0VvQUEBAQ==
```

### <a name="sasl-xoauth2-authentication-for-shared-mailboxes-in-office-365"></a>Autenticación XOAUTH2 SASL para buzones compartidos en Office 365

En caso de acceso a buzones compartidos con OAuth, la aplicación debe obtener el token de acceso en nombre de un usuario, pero reemplazar el campo userName de la cadena codificada XOAUTH2 de SASL por la dirección de correo electrónico del buzón compartido. 

### <a name="imap-protocol-exchange"></a>Protocolo IMAP Exchange

Para autenticar una conexión de servidor IMAP, el cliente tendrá que responder con un `AUTHENTICATE` comando con el siguiente formato:

```text
AUTHENTICATE XOAUTH2 <base64 string in XOAUTH2 format>
```

Intercambio de mensajes cliente-servidor de ejemplo que da como resultado un éxito de autenticación:

```text
[connection begins]
C: C01 CAPABILITY
S: * CAPABILITY … AUTH=XOAUTH2
S: C01 OK Completed
C: A01 AUTHENTICATE XOAUTH2 dXNlcj1zb21ldXNlckBleGFtcGxlLmNvbQFhdXRoPUJlYXJlciB5YTI5LnZGOWRmdDRxbVRjMk52YjNSbGNrQmhkSFJoZG1semRHRXVZMjl0Q2cBAQ==
S: A01 OK AUTHENTICATE completed.
```

Intercambio de mensajes cliente-servidor de ejemplo que da como resultado un error de autenticación:

```text
[connection begins]
S: * CAPABILITY … AUTH=XOAUTH2
S: C01 OK Completed
C: A01 AUTHENTICATE XOAUTH2 dXNlcj1zb21ldXNlckBleGFtcGxlLmNvbQFhdXRoPUJlYXJlciB5YTI5LnZGOWRmdDRxbVRjMk52YjNSbGNrQmhkSFJoZG1semRHRXVZMjl0Q2cBAQ==
S: A01 NO AUTHENTICATE failed.
```

### <a name="pop-protocol-exchange"></a>Protocolo POP Exchange

Para autenticar una conexión de servidor POP, el cliente tendrá que responder con un comando dividido en `AUTH` dos líneas en el siguiente formato:    

```text 
AUTH XOAUTH2 
<base64 string in XOAUTH2 format>   
``` 

Intercambio de mensajes cliente-servidor de ejemplo que da como resultado un éxito de autenticación:    

```text 
[connection begins] 
C: AUTH XOAUTH2     
S: +    
C: dXNlcj1zb21ldXNlckBleGFtcGxlLmNvbQFhdXRoPUJlYX   
JlciB5YTI5LnZGOWRmdDRxbVRjMk52YjNSbGNrQmhkSFJoZG1semRHRXVZMjl0  
Q2cBAQ==    
S: +OK User successfully authenticated. 
[connection continues...]   
``` 

Intercambio de mensajes cliente-servidor de ejemplo que da como resultado un error de autenticación:    

```text 
[connection begins] 
C: AUTH XOAUTH2     
S: +    
C: dXNlcj1zb21ldXNlckBleGFtcGxlLmNvbQFhdXRoPUJlY    
XJlciB5YTI5LnZGOWRmdDRxbVRjMk52YjNSbGNrQmhkSFJoZG1semRHRXVZMj   
l0Q2cBAQ=   
S: -ERR Authentication failure: unknown user name or bad password.  
```

### <a name="smtp-protocol-exchange"></a>Protocolo SMTP Exchange

Para autenticar una conexión de servidor SMTP, el cliente tendrá que responder con un `AUTH` comando con el siguiente formato:

```text
AUTH XOAUTH2 <base64 string in XOAUTH2 format>
```

Intercambio de mensajes cliente-servidor de ejemplo que da como resultado un éxito de autenticación:

```text
[connection begins]
C: auth xoauth2
S: 334
C: dXNlcj1zb21ldXNlckBleGFtcGxlLmNvbQFhdXRoPUJlY
XJlciB5YTI5LnZGOWRmdDRxbVRjMk52YjNSbGNrQmhkSFJoZG1semRHRXVZMj
l0Q2cBAQ==
S: 235 2.7.0 Authentication successful
[connection continues...]
```

Intercambio de mensajes cliente-servidor de ejemplo que da como resultado un error de autenticación:

```text
[connection begins]
C: auth xoauth2
S: 334
C: dXNlcj1zb21ldXNlckBleGFtcGxlLmNvbQFhdXRoPUJlY
XJlciB5YTI5LnZGOWRmdDRxbVRjMk52YjNSbGNrQmhkSFJoZG1semRHRXVZMj
l0Q2cBAQ==
S: 535 5.7.3 Authentication unsuccessful [SN2PR00CA0018.namprd00.prod.outlook.com]
```

## <a name="see-also"></a>Vea también

- [Autenticación y EWS en Exchange](../exchange-web-services/authentication-and-ews-in-exchange.md)
- [Configuración de conexión IMAP, POP](https://support.office.com/article/pop-and-imap-email-settings-for-outlook-8361e398-8af4-4e97-b147-6c6c4ac95353)
- [Protocolo de acceso a mensajes de Internet](https://tools.ietf.org/html/rfc3501)
- [Protocolo Office post](https://tools.ietf.org/html/rfc1081)
- [Extensión de servicio SMTP para autenticación](https://tools.ietf.org/html/rfc4954)
