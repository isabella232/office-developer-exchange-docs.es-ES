---
title: Autenticar una conexión IMAP, POP o SMTP mediante OAuth
description: Obtenga información sobre cómo usar la autenticación OAuth con las aplicaciones IMAP, POP y SMTP.
author: svpsiva
ms.date: 02/19/2020
ms.audience: Developer
ms.openlocfilehash: 4662aa904ed162edcced6c096eac8cf636180f6a
ms.sourcegitcommit: 37d4ecd4f469690ba1de87baad2f2f58c40c96ba
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/18/2020
ms.locfileid: "49348818"
---
# <a name="authenticate-an-imap-pop-or-smtp-connection-using-oauth"></a>Autenticar una conexión IMAP, POP o SMTP mediante OAuth

Obtenga información sobre cómo usar la autenticación de OAuth para conectarse con protocolos IMAP, POP o SMTP y obtener acceso a datos de correo electrónico para usuarios de Office 365.

> La compatibilidad de OAuth2 con los protocolos IMAP, POP y SMTP, como se describe a continuación, es compatible con Microsoft 365 (que incluye Office en la web) y los usuarios de Outlook.com.

Si no está familiarizado con el protocolo OAuth 2,0, empiece por leer el [Protocolo oauth 2,0 en la introducción a la plataforma de identidades de Microsoft](/azure/active-directory/develop/active-directory-v2-protocols). Para obtener más información acerca del Libariers de autenticación de Microsoft (MSAL), que implementan el protocolo OAuth 2,0 para autenticar a los usuarios y acceder a las API seguras, lea la [información general de MSAL](/azure/active-directory/develop/msal-overview).

Puede usar el servicio de autenticación OAuth proporcionado por Azure Active Directory para permitir que la aplicación se conecte con los protocolos IMAP, POP o SMTP para acceder a Exchange online en Office 365. Para usar OAuth con la aplicación, debe:

1. [Registrar la aplicación](#register-your-application) con Azure Active Directory.
1. [Configure la aplicación](#configure-your-application) en Azure Active Directory.
1. [Obtener un token de acceso](#get-an-access-token) desde un servidor de tokens.
1. [Autentique las solicitudes de conexión](#authenticate-connection-requests) con un token de acceso.

## <a name="register-your-application"></a>Registrar su aplicación

Para usar OAuth, se debe registrar una aplicación con Azure Active Directory.

Siga las instrucciones que aparecen en [registrar una aplicación con la plataforma de identidad de Microsoft](/azure/active-directory/develop/quickstart-register-app) para crear una nueva aplicación.

## <a name="configure-your-application"></a>Configurar la aplicación

Siga las instrucciones que aparecen en [configurar una aplicación cliente para acceder a las API Web](/azure/active-directory/develop/quickstart-configure-app-access-web-apis)

Asegúrese de agregar uno o más de los siguientes ámbitos de permisos que correspondan a los protocolos con los que desea integrar. En el Asistente para **Agregar un permiso** , seleccione **Microsoft Graph** y, a continuación, **permisos delegados** para buscar los siguientes ámbitos de permiso enumerados.

| Protocolo  | Ámbito de permisos        |
|-----------|-------------------------|
| IMAP      | `IMAP.AccessAsUser.All` |
| POP       | `POP.AccessAsUser.All`  |
| AUTENTICACIÓN SMTP | `SMTP.Send`             |

## <a name="get-an-access-token"></a>Obtener un token de acceso

Puede usar una de las [bibliotecas de cliente de MSAL](/azure/active-directory/develop/msal-overview) para obtener un token de acceso desde la aplicación cliente.

Como alternativa, puede seleccionar un flujo adecuado de la siguiente lista y seguir los pasos correspondientes para llamar a las API de REST de la plataforma de identidad subyacente y recuperar un token de acceso.

1. [Flujo de código de autorización de OAuth2](/azure/active-directory/develop/v2-oauth2-auth-code-flow)
1. [Flujo de concesión de autorización de dispositivo de OAuth2](/azure/active-directory/develop/v2-oauth2-device-code)

Acceso de OAuth a protocolos IMAP, POP, SMTP AUTH mediante OAuth2 el flujo de concesión de credenciales de cliente no es compatible. Si la aplicación necesita acceso persistente a todos los buzones de una organización de Microsoft 365, se recomienda usar las API de Microsoft Graph que permiten el acceso sin un usuario, habilitar permisos granulares y permitir a los administradores el acceso a un conjunto específico de buzones.

Asegúrese de especificar los ámbitos completos, incluidas las direcciones URL de recursos de Outlook, al autorizar la aplicación y solicitar un token de acceso.

| Protocolo  | Cadena de ámbito de permiso |
|-----------|-------------------------|
| IMAP      | `https://outlook.office.com/IMAP.AccessAsUser.All` |
| POP       | `https://outlook.office.com/POP.AccessAsUser.All`  |
| AUTENTICACIÓN SMTP | `https://outlook.office.com/SMTP.Send`             |

Además, puede solicitar [offline_access](/azure/active-directory/develop/v2-permissions-and-consent#offline_access) ámbito. Cuando un usuario aprueba el ámbito de offline_access, la aplicación puede recibir tokens de actualización desde el punto de conexión del token de plataforma de identidad de Microsoft. Los tokens de actualización son de larga duración. La aplicación puede obtener nuevos tokens de acceso a medida que expiren los más antiguos.

## <a name="authenticate-connection-requests"></a>Autenticar solicitudes de conexión

Puede iniciar una conexión con los servidores de correo de Office 365 mediante la [configuración de correo electrónico IMAP y pop para office 365](https://support.office.com/article/pop-and-imap-email-settings-for-outlook-8361e398-8af4-4e97-b147-6c6c4ac95353).

### <a name="sasl-xoauth2"></a>SASL XOAUTH2

La integración de OAuth con requiere que la aplicación use el formato SASL XOAUTH2 para codificar y transmitir el token de acceso. SASL XOAUTH2 codifica el nombre de usuario, el token de acceso junto con el siguiente formato:

```text
base64("user=" + userName + "^Aauth=Bearer " + accessToken + "^A^A")
```

`^A`representa un **control**  +  **a** ( `%x01` ).

Por ejemplo, el formato XOAUTH2 de SASL para obtener acceso `test@contoso.onmicrosoft.com` con el token de acceso `EwBAAl3BAAUFFpUAo7J3Ve0bjLBWZWCclRC3EoAA` es:

```text
base64("user=test@contoso.onmicrosoft.com^Aauth=Bearer EwBAAl3BAAUFFpUAo7J3Ve0bjLBWZWCclRC3EoAA^A^A")
```

Después de la codificación Base64, esto se traduce en la siguiente cadena. Tenga en cuenta que los saltos de línea se insertan para facilitar la lectura.

```text
dXNlcj10ZXN0QGNvbnRvc28ub25taWNyb3NvZnQuY29tAWF1dGg9QmVhcmVy
IEV3QkFBbDNCQUFVRkZwVUFvN0ozVmUwYmpMQldaV0NjbFJDM0VvQUEBAQ==
```

### <a name="sasl-xoauth2-authentication-for-shared-mailboxes-in-office-365"></a>XOAUTH2 de la autenticación de SASL para buzones compartidos en Office 365

En caso de acceso a buzones compartidos mediante OAuth, la aplicación necesita obtener el token de acceso en nombre de un usuario, pero reemplazar el campo userName en la cadena con codificación SASL XOAUTH2 con la dirección de correo electrónico del buzón compartido. 

### <a name="imap-protocol-exchange"></a>Intercambio de protocolo IMAP

Para autenticar una conexión de servidor IMAP, el cliente tendrá que responder con un `AUTHENTICATE` comando con el siguiente formato:

```text
AUTHENTICATE XOAUTH2 <base64 string in XOAUTH2 format>
```

Intercambio de mensajes de cliente-servidor de ejemplo que da como resultado una autenticación correcta:

```text
[connection begins]
C: C01 CAPABILITY
S: * CAPABILITY … AUTH=XOAUTH2
S: C01 OK Completed
C: A01 AUTHENTICATE XOAUTH2 dXNlcj1zb21ldXNlckBleGFtcGxlLmNvbQFhdXRoPUJlYXJlciB5YTI5LnZGOWRmdDRxbVRjMk52YjNSbGNrQmhkSFJoZG1semRHRXVZMjl0Q2cBAQ==
S: A01 OK AUTHENTICATE completed.
```

Ejemplo de intercambio de mensajes cliente-servidor que da como resultado un error de autenticación:

```text
[connection begins]
S: * CAPABILITY … AUTH=XOAUTH2
S: C01 OK Completed
C: A01 AUTHENTICATE XOAUTH2 dXNlcj1zb21ldXNlckBleGFtcGxlLmNvbQFhdXRoPUJlYXJlciB5YTI5LnZGOWRmdDRxbVRjMk52YjNSbGNrQmhkSFJoZG1semRHRXVZMjl0Q2cBAQ==
S: A01 NO AUTHENTICATE failed.
```

### <a name="pop-protocol-exchange"></a>Intercambio de protocolo POP

Para autenticar una conexión de servidor POP, el cliente tendrá que responder con un `AUTH` comando dividido en dos líneas con el siguiente formato:    

```text 
AUTH XOAUTH2 
<base64 string in XOAUTH2 format>   
``` 

Intercambio de mensajes de cliente-servidor de ejemplo que da como resultado una autenticación correcta:    

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

Ejemplo de intercambio de mensajes cliente-servidor que da como resultado un error de autenticación:    

```text 
[connection begins] 
C: AUTH XOAUTH2     
S: +    
C: dXNlcj1zb21ldXNlckBleGFtcGxlLmNvbQFhdXRoPUJlY    
XJlciB5YTI5LnZGOWRmdDRxbVRjMk52YjNSbGNrQmhkSFJoZG1semRHRXVZMj   
l0Q2cBAQ=   
S: -ERR Authentication failure: unknown user name or bad password.  
```

### <a name="smtp-protocol-exchange"></a>Intercambio de protocolo SMTP

Para autenticar una conexión de servidor SMTP, el cliente tendrá que responder con un `AUTH` comando con el siguiente formato:

```text
AUTH XOAUTH2 <base64 string in XOAUTH2 format>
```

Intercambio de mensajes de cliente-servidor de ejemplo que da como resultado una autenticación correcta:

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

Ejemplo de intercambio de mensajes cliente-servidor que da como resultado un error de autenticación:

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
- [Configuración de la conexión de POP IMAP](https://support.office.com/article/pop-and-imap-email-settings-for-outlook-8361e398-8af4-4e97-b147-6c6c4ac95353)
- [Protocolo de acceso a mensajes de Internet](https://tools.ietf.org/html/rfc3501)
- [Protocolo de oficina de correos](https://tools.ietf.org/html/rfc1081)
- [Extensión de servicio SMTP para autenticación](https://tools.ietf.org/html/rfc4954)
