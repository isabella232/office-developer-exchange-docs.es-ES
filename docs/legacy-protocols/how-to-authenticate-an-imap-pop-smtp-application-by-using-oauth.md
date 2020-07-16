---
title: Autenticar una conexión IMAP, POP o SMTP mediante OAuth
description: Obtenga información sobre cómo usar la autenticación OAuth con las aplicaciones IMAP, POP y SMTP.
author: svpsiva
ms.date: 02/19/2020
ms.audience: Developer
ms.openlocfilehash: f83a932790cde558e741ece1e87403103aff18fd
ms.sourcegitcommit: eeda51cb037aa25566adb293f25574674fdb2d9e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/01/2020
ms.locfileid: "45012562"
---
# <a name="authenticate-an-imap-pop-or-smtp-connection-using-oauth"></a><span data-ttu-id="cf1e3-103">Autenticar una conexión IMAP, POP o SMTP mediante OAuth</span><span class="sxs-lookup"><span data-stu-id="cf1e3-103">Authenticate an IMAP, POP or SMTP connection using OAuth</span></span>

<span data-ttu-id="cf1e3-104">Obtenga información sobre cómo usar la autenticación de OAuth para conectarse con protocolos IMAP, POP o SMTP y obtener acceso a datos de correo electrónico para usuarios de Office 365.</span><span class="sxs-lookup"><span data-stu-id="cf1e3-104">Learn how to use OAuth authentication to connect with IMAP, POP or SMTP protocols and access email data for Office 365 users.</span></span>

> <span data-ttu-id="cf1e3-105">La compatibilidad de OAuth2 con los protocolos IMAP, POP y SMTP, tal y como se describe a continuación, no es compatible con los usuarios de Outlook.com.</span><span class="sxs-lookup"><span data-stu-id="cf1e3-105">OAuth2 support for IMAP, POP, SMTP protocols as described below is not supported for Outlook.com users.</span></span>

<span data-ttu-id="cf1e3-106">Si no está familiarizado con OAuth 2,0, empiece por leer la [Introducción a la plataforma de identidad de Microsoft (v 2.0)](/azure/active-directory/develop/v2-overview).</span><span class="sxs-lookup"><span data-stu-id="cf1e3-106">If you're not familiar with OAuth 2.0, start by reading the [Microsoft identity platform (v2.0) overview](/azure/active-directory/develop/v2-overview).</span></span> <span data-ttu-id="cf1e3-107">Este documento presenta diferentes componentes de la plataforma de identidad de Microsoft, incluidos los SDK.</span><span class="sxs-lookup"><span data-stu-id="cf1e3-107">That document introduces you to different components of Microsoft identity platform, including SDKs.</span></span>

<span data-ttu-id="cf1e3-108">Puede usar el servicio de autenticación OAuth proporcionado por Azure Active Directory para permitir que la aplicación se conecte con los protocolos IMAP, POP o SMTP para acceder a Exchange online en Office 365.</span><span class="sxs-lookup"><span data-stu-id="cf1e3-108">You can use the OAuth authentication service provided by Azure Active Directory to enable your application to connect with IMAP, POP or SMTP protocols to access Exchange Online in Office 365.</span></span> <span data-ttu-id="cf1e3-109">Para usar OAuth con la aplicación, debe:</span><span class="sxs-lookup"><span data-stu-id="cf1e3-109">To use OAuth with your application you need to:</span></span>

1. <span data-ttu-id="cf1e3-110">[Registre la aplicación](#register-your-application) con Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="cf1e3-110">[Register your application](#register-your-application) with Azure Active Directory.</span></span>
1. <span data-ttu-id="cf1e3-111">[Configure la aplicación](#configure-your-application) en Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="cf1e3-111">[Configure your application](#configure-your-application) in Azure Active Directory.</span></span>
1. <span data-ttu-id="cf1e3-112">[Obtener un token de acceso](#get-an-access-token) desde un servidor de tokens.</span><span class="sxs-lookup"><span data-stu-id="cf1e3-112">[Get an access token](#get-an-access-token) from a token server.</span></span>
1. <span data-ttu-id="cf1e3-113">[Autentique las solicitudes de conexión](#authenticate-connection-requests) con un token de acceso.</span><span class="sxs-lookup"><span data-stu-id="cf1e3-113">[Authenticate connection requests](#authenticate-connection-requests) with an access token.</span></span>

## <a name="register-your-application"></a><span data-ttu-id="cf1e3-114">Registrar la aplicación</span><span class="sxs-lookup"><span data-stu-id="cf1e3-114">Register your application</span></span>

<span data-ttu-id="cf1e3-115">Para usar OAuth, se debe registrar una aplicación con Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="cf1e3-115">To use OAuth, an application must be registered with Azure Active Directory.</span></span>

<span data-ttu-id="cf1e3-116">Siga las instrucciones que aparecen en [registrar una aplicación con la plataforma de identidad de Microsoft](/azure/active-directory/develop/quickstart-register-app) para crear una nueva aplicación.</span><span class="sxs-lookup"><span data-stu-id="cf1e3-116">Follow the instructions listed in [Register an application with the Microsoft identity platform](/azure/active-directory/develop/quickstart-register-app) to create a new application.</span></span>

## <a name="configure-your-application"></a><span data-ttu-id="cf1e3-117">Configurar la aplicación</span><span class="sxs-lookup"><span data-stu-id="cf1e3-117">Configure your application</span></span>

<span data-ttu-id="cf1e3-118">Siga las instrucciones que aparecen en [configurar una aplicación cliente para acceder a las API Web](/azure/active-directory/develop/quickstart-configure-app-access-web-apis)</span><span class="sxs-lookup"><span data-stu-id="cf1e3-118">Follow the instructions listed in [Configure a client application to access web APIs](/azure/active-directory/develop/quickstart-configure-app-access-web-apis)</span></span>

<span data-ttu-id="cf1e3-119">Asegúrese de agregar uno o más de los siguientes ámbitos de permisos que correspondan a los protocolos con los que desea integrar.</span><span class="sxs-lookup"><span data-stu-id="cf1e3-119">Make sure to add one or more of the following permission scopes that correspond to the protocols you would like to integrate with.</span></span> <span data-ttu-id="cf1e3-120">En el Asistente para **Agregar un permiso** , seleccione **Microsoft Graph** y, a continuación, **permisos delegados** para buscar los siguientes ámbitos de permiso enumerados.</span><span class="sxs-lookup"><span data-stu-id="cf1e3-120">In the **Add a permission** wizard, select **Microsoft Graph** and then **Delegated permissions** to find the following permission scopes listed.</span></span>

| <span data-ttu-id="cf1e3-121">Protocolo</span><span class="sxs-lookup"><span data-stu-id="cf1e3-121">Protocol</span></span>  | <span data-ttu-id="cf1e3-122">Ámbito de permisos</span><span class="sxs-lookup"><span data-stu-id="cf1e3-122">Permission scope</span></span>        |
|-----------|-------------------------|
| <span data-ttu-id="cf1e3-123">IMAP</span><span class="sxs-lookup"><span data-stu-id="cf1e3-123">IMAP</span></span>      | `IMAP.AccessAsUser.All` |
| <span data-ttu-id="cf1e3-124">POP</span><span class="sxs-lookup"><span data-stu-id="cf1e3-124">POP</span></span>       | `POP.AccessAsUser.All`  |
| <span data-ttu-id="cf1e3-125">AUTENTICACIÓN SMTP</span><span class="sxs-lookup"><span data-stu-id="cf1e3-125">SMTP AUTH</span></span> | `SMTP.Send`             |

## <a name="get-an-access-token"></a><span data-ttu-id="cf1e3-126">Obtener un token de acceso</span><span class="sxs-lookup"><span data-stu-id="cf1e3-126">Get an access token</span></span>

<span data-ttu-id="cf1e3-127">Puede usar una de las [bibliotecas de cliente de MSAL](/azure/active-directory/develop/msal-overview) para obtener un token de acceso desde la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="cf1e3-127">You can use one of our [MSAL client libraries](/azure/active-directory/develop/msal-overview) to fetch an access token from your client application.</span></span>

<span data-ttu-id="cf1e3-128">Como alternativa, puede seleccionar un flujo adecuado de la siguiente lista y seguir los pasos correspondientes para llamar a las API de REST de la plataforma de identidad subyacente y recuperar un token de acceso.</span><span class="sxs-lookup"><span data-stu-id="cf1e3-128">Alternatively, you can select an appropriate flow from the following list and follow the corresponding steps to call the underlying identity platform REST APIs and retrieve an access token.</span></span>

1. [<span data-ttu-id="cf1e3-129">Flujo de código de autorización de OAuth2</span><span class="sxs-lookup"><span data-stu-id="cf1e3-129">OAuth2 authorization code flow</span></span>](/azure/active-directory/develop/v2-oauth2-auth-code-flow)
1. [<span data-ttu-id="cf1e3-130">Flujo de concesión de autorización de dispositivo de OAuth2</span><span class="sxs-lookup"><span data-stu-id="cf1e3-130">OAuth2 Device authorization grant flow</span></span>](/azure/active-directory/develop/v2-oauth2-device-code)

<span data-ttu-id="cf1e3-131">Acceso de OAuth a protocolos IMAP, POP, SMTP AUTH mediante OAuth2 el flujo de concesión de credenciales de cliente no es compatible.</span><span class="sxs-lookup"><span data-stu-id="cf1e3-131">OAuth access to IMAP, POP, SMTP AUTH protocols via OAuth2 client credentials grant flow is not supported.</span></span> <span data-ttu-id="cf1e3-132">Si la aplicación necesita acceso persistente a todos los buzones de una organización de Microsoft 365, se recomienda usar las API de Microsoft Graph que permiten el acceso sin un usuario, habilitar permisos granulares y permitir a los administradores el acceso a un conjunto específico de buzones.</span><span class="sxs-lookup"><span data-stu-id="cf1e3-132">If your application needs persistent access to all mailboxes in a Microsoft 365 organization, we recommend that you use the Microsoft Graph APIs which allow access without a user, enable granular permissions and let administrators scope such access to a specific set of mailboxes.</span></span>

<span data-ttu-id="cf1e3-133">Asegúrese de especificar los ámbitos completos, incluidas las direcciones URL de recursos de Outlook, al autorizar la aplicación y solicitar un token de acceso.</span><span class="sxs-lookup"><span data-stu-id="cf1e3-133">Make sure to specify the full scopes, including Outlook resource URLs, when authorizing your application and requesting an access token.</span></span>

| <span data-ttu-id="cf1e3-134">Protocolo</span><span class="sxs-lookup"><span data-stu-id="cf1e3-134">Protocol</span></span>  | <span data-ttu-id="cf1e3-135">Cadena de ámbito de permiso</span><span class="sxs-lookup"><span data-stu-id="cf1e3-135">Permission scope string</span></span> |
|-----------|-------------------------|
| <span data-ttu-id="cf1e3-136">IMAP</span><span class="sxs-lookup"><span data-stu-id="cf1e3-136">IMAP</span></span>      | `https://outlook.office.com/IMAP.AccessAsUser.All` |
| <span data-ttu-id="cf1e3-137">POP</span><span class="sxs-lookup"><span data-stu-id="cf1e3-137">POP</span></span>       | `https://outlook.office.com/POP.AccessAsUser.All`  |
| <span data-ttu-id="cf1e3-138">AUTENTICACIÓN SMTP</span><span class="sxs-lookup"><span data-stu-id="cf1e3-138">SMTP AUTH</span></span> | `https://outlook.office.com/SMTP.Send`             |

<span data-ttu-id="cf1e3-139">Además, puede solicitar [offline_access](/azure/active-directory/develop/v2-permissions-and-consent#offline_access) ámbito.</span><span class="sxs-lookup"><span data-stu-id="cf1e3-139">In addition, you can request for [offline_access](/azure/active-directory/develop/v2-permissions-and-consent#offline_access) scope.</span></span> <span data-ttu-id="cf1e3-140">Cuando un usuario aprueba el ámbito de offline_access, la aplicación puede recibir tokens de actualización desde el punto de conexión del token de plataforma de identidad de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="cf1e3-140">When a user approves the offline_access scope, your app can receive refresh tokens from the Microsoft identity platform token endpoint.</span></span> <span data-ttu-id="cf1e3-141">Los tokens de actualización son de larga duración.</span><span class="sxs-lookup"><span data-stu-id="cf1e3-141">Refresh tokens are long-lived.</span></span> <span data-ttu-id="cf1e3-142">La aplicación puede obtener nuevos tokens de acceso a medida que expiren los más antiguos.</span><span class="sxs-lookup"><span data-stu-id="cf1e3-142">Your app can get new access tokens as older ones expire.</span></span>

## <a name="authenticate-connection-requests"></a><span data-ttu-id="cf1e3-143">Autenticar solicitudes de conexión</span><span class="sxs-lookup"><span data-stu-id="cf1e3-143">Authenticate connection requests</span></span>

<span data-ttu-id="cf1e3-144">Puede iniciar una conexión con los servidores de correo de Office 365 mediante la [configuración de correo electrónico IMAP y pop para office 365](https://support.office.com/article/pop-and-imap-email-settings-for-outlook-8361e398-8af4-4e97-b147-6c6c4ac95353).</span><span class="sxs-lookup"><span data-stu-id="cf1e3-144">You can initiate a connection to Office 365 mail servers using the [IMAP and POP email settings for Office 365](https://support.office.com/article/pop-and-imap-email-settings-for-outlook-8361e398-8af4-4e97-b147-6c6c4ac95353).</span></span>

### <a name="sasl-xoauth2"></a><span data-ttu-id="cf1e3-145">SASL XOAUTH2</span><span class="sxs-lookup"><span data-stu-id="cf1e3-145">SASL XOAUTH2</span></span>

<span data-ttu-id="cf1e3-146">La integración de OAuth con requiere que la aplicación use el formato SASL XOAUTH2 para codificar y transmitir el token de acceso.</span><span class="sxs-lookup"><span data-stu-id="cf1e3-146">OAuth integration with requires your application to use SASL XOAUTH2 format for encoding and transmitting the access token.</span></span> <span data-ttu-id="cf1e3-147">SASL XOAUTH2 codifica el nombre de usuario, el token de acceso junto con el siguiente formato:</span><span class="sxs-lookup"><span data-stu-id="cf1e3-147">SASL XOAUTH2 encodes the username, access token together in the following format:</span></span>

```text
base64("user=" + userName + "^Aauth=Bearer " + accessToken + "^A^A")
```

<span data-ttu-id="cf1e3-148">`^A`representa un **control**  +  **a** ( `%x01` ).</span><span class="sxs-lookup"><span data-stu-id="cf1e3-148">`^A` represents a **Control** + **A** (`%x01`).</span></span>

<span data-ttu-id="cf1e3-149">Por ejemplo, el formato XOAUTH2 de SASL para obtener acceso `test@contoso.onmicrosoft.com` con el token de acceso `EwBAAl3BAAUFFpUAo7J3Ve0bjLBWZWCclRC3EoAA` es:</span><span class="sxs-lookup"><span data-stu-id="cf1e3-149">For example, the SASL XOAUTH2 format to access `test@contoso.onmicrosoft.com` with access token `EwBAAl3BAAUFFpUAo7J3Ve0bjLBWZWCclRC3EoAA` is:</span></span>

```text
base64("user=test@contoso.onmicrosoft.com^Aauth=Bearer EwBAAl3BAAUFFpUAo7J3Ve0bjLBWZWCclRC3EoAA^A^A")
```

<span data-ttu-id="cf1e3-150">Después de la codificación Base64, esto se traduce en la siguiente cadena.</span><span class="sxs-lookup"><span data-stu-id="cf1e3-150">After base64 encoding, this translates to the following string.</span></span> <span data-ttu-id="cf1e3-151">Tenga en cuenta que los saltos de línea se insertan para facilitar la lectura.</span><span class="sxs-lookup"><span data-stu-id="cf1e3-151">Note that line breaks are inserted for readability.</span></span>

```text
dXNlcj10ZXN0QGNvbnRvc28ub25taWNyb3NvZnQuY29tAWF1dGg9QmVhcmVy
IEV3QkFBbDNCQUFVRkZwVUFvN0ozVmUwYmpMQldaV0NjbFJDM0VvQUEBAQ==
```

### <a name="sasl-xoauth2-authentication-for-shared-mailboxes-in-office-365"></a><span data-ttu-id="cf1e3-152">XOAUTH2 de la autenticación de SASL para buzones compartidos en Office 365</span><span class="sxs-lookup"><span data-stu-id="cf1e3-152">SASL XOAUTH2 authentication for shared mailboxes in Office 365</span></span>

<span data-ttu-id="cf1e3-153">En caso de acceso a buzones compartidos mediante OAuth, la aplicación necesita obtener el token de acceso en nombre de un usuario, pero reemplazar el campo userName en la cadena con codificación SASL XOAUTH2 con la dirección de correo electrónico del buzón compartido.</span><span class="sxs-lookup"><span data-stu-id="cf1e3-153">In case of shared mailbox access using OAuth, application needs to obtain the access token on behalf of a user but replace the userName field in the SASL XOAUTH2 encoded string with the email address of the shared mailbox.</span></span> 

### <a name="imap-protocol-exchange"></a><span data-ttu-id="cf1e3-154">Intercambio de protocolo IMAP</span><span class="sxs-lookup"><span data-stu-id="cf1e3-154">IMAP Protocol Exchange</span></span>

<span data-ttu-id="cf1e3-155">Para autenticar una conexión de servidor IMAP, el cliente tendrá que responder con un `AUTHENTICATE` comando con el siguiente formato:</span><span class="sxs-lookup"><span data-stu-id="cf1e3-155">To authenticate a IMAP server connection, the client will have to respond with an `AUTHENTICATE` command in the following format:</span></span>

```text
AUTHENTICATE XOAUTH2 <base64 string in XOAUTH2 format>
```

<span data-ttu-id="cf1e3-156">Intercambio de mensajes de cliente-servidor de ejemplo que da como resultado una autenticación correcta:</span><span class="sxs-lookup"><span data-stu-id="cf1e3-156">Sample client-server message exchange that results in an authentication success:</span></span>

```text
[connection begins]
C: C01 CAPABILITY
S: * CAPABILITY … AUTH=XOAUTH2
S: C01 OK Completed
C: A01 AUTHENTICATE XOAUTH2 dXNlcj1zb21ldXNlckBleGFtcGxlLmNvbQFhdXRoPUJlYXJlciB5YTI5LnZGOWRmdDRxbVRjMk52YjNSbGNrQmhkSFJoZG1semRHRXVZMjl0Q2cBAQ==
S: A01 OK AUTHENTICATE completed.
```

<span data-ttu-id="cf1e3-157">Ejemplo de intercambio de mensajes cliente-servidor que da como resultado un error de autenticación:</span><span class="sxs-lookup"><span data-stu-id="cf1e3-157">Sample client-server message exchange that results in an authentication failure:</span></span>

```text
[connection begins]
S: * CAPABILITY … AUTH=XOAUTH2
S: C01 OK Completed
C: A01 AUTHENTICATE XOAUTH2 dXNlcj1zb21ldXNlckBleGFtcGxlLmNvbQFhdXRoPUJlYXJlciB5YTI5LnZGOWRmdDRxbVRjMk52YjNSbGNrQmhkSFJoZG1semRHRXVZMjl0Q2cBAQ==
S: A01 NO AUTHENTICATE failed.
```

### <a name="pop-protocol-exchange"></a><span data-ttu-id="cf1e3-158">Intercambio de protocolo POP</span><span class="sxs-lookup"><span data-stu-id="cf1e3-158">POP Protocol Exchange</span></span>

<span data-ttu-id="cf1e3-159">Para autenticar una conexión de servidor POP, el cliente tendrá que responder con un `AUTH` comando dividido en dos líneas con el siguiente formato:</span><span class="sxs-lookup"><span data-stu-id="cf1e3-159">To authenticate a POP server connection, the client will have to respond with an `AUTH` command split into two lines in the following format:</span></span>    

```text 
AUTH XOAUTH2 
<base64 string in XOAUTH2 format>   
``` 

<span data-ttu-id="cf1e3-160">Intercambio de mensajes de cliente-servidor de ejemplo que da como resultado una autenticación correcta:</span><span class="sxs-lookup"><span data-stu-id="cf1e3-160">Sample client-server message exchange that results in an authentication success:</span></span>    

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

<span data-ttu-id="cf1e3-161">Ejemplo de intercambio de mensajes cliente-servidor que da como resultado un error de autenticación:</span><span class="sxs-lookup"><span data-stu-id="cf1e3-161">Sample client-server message exchange that results in an authentication failure:</span></span>    

```text 
[connection begins] 
C: AUTH XOAUTH2     
S: +    
C: dXNlcj1zb21ldXNlckBleGFtcGxlLmNvbQFhdXRoPUJlY    
XJlciB5YTI5LnZGOWRmdDRxbVRjMk52YjNSbGNrQmhkSFJoZG1semRHRXVZMj   
l0Q2cBAQ=   
S: -ERR Authentication failure: unknown user name or bad password.  
```

### <a name="smtp-protocol-exchange"></a><span data-ttu-id="cf1e3-162">Intercambio de protocolo SMTP</span><span class="sxs-lookup"><span data-stu-id="cf1e3-162">SMTP Protocol Exchange</span></span>

<span data-ttu-id="cf1e3-163">Para autenticar una conexión de servidor SMTP, el cliente tendrá que responder con un `AUTH` comando con el siguiente formato:</span><span class="sxs-lookup"><span data-stu-id="cf1e3-163">To authenticate a SMTP server connection, the client will have to respond with an `AUTH` command in the following format:</span></span>

```text
AUTH XOAUTH2 <base64 string in XOAUTH2 format>
```

<span data-ttu-id="cf1e3-164">Intercambio de mensajes de cliente-servidor de ejemplo que da como resultado una autenticación correcta:</span><span class="sxs-lookup"><span data-stu-id="cf1e3-164">Sample client-server message exchange that results in an authentication success:</span></span>

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

<span data-ttu-id="cf1e3-165">Ejemplo de intercambio de mensajes cliente-servidor que da como resultado un error de autenticación:</span><span class="sxs-lookup"><span data-stu-id="cf1e3-165">Sample client-server message exchange that results in an authentication failure:</span></span>

```text
[connection begins]
C: auth xoauth2
S: 334
C: dXNlcj1zb21ldXNlckBleGFtcGxlLmNvbQFhdXRoPUJlY
XJlciB5YTI5LnZGOWRmdDRxbVRjMk52YjNSbGNrQmhkSFJoZG1semRHRXVZMj
l0Q2cBAQ==
S: 535 5.7.3 Authentication unsuccessful [SN2PR00CA0018.namprd00.prod.outlook.com]
```

## <a name="see-also"></a><span data-ttu-id="cf1e3-166">Ver también</span><span class="sxs-lookup"><span data-stu-id="cf1e3-166">See also</span></span>

- [<span data-ttu-id="cf1e3-167">Autenticación y EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="cf1e3-167">Authentication and EWS in Exchange</span></span>](../exchange-web-services/authentication-and-ews-in-exchange.md)
- [<span data-ttu-id="cf1e3-168">Configuración de la conexión de POP IMAP</span><span class="sxs-lookup"><span data-stu-id="cf1e3-168">IMAP, POP Connection settings</span></span>](https://support.office.com/article/pop-and-imap-email-settings-for-outlook-8361e398-8af4-4e97-b147-6c6c4ac95353)
- [<span data-ttu-id="cf1e3-169">Protocolo de acceso a mensajes de Internet</span><span class="sxs-lookup"><span data-stu-id="cf1e3-169">Internet Message Access Protocol</span></span>](https://tools.ietf.org/html/rfc3501)
- [<span data-ttu-id="cf1e3-170">Protocolo de oficina de correos</span><span class="sxs-lookup"><span data-stu-id="cf1e3-170">Post Office Protocol</span></span>](https://tools.ietf.org/html/rfc1081)
- [<span data-ttu-id="cf1e3-171">Extensión de servicio SMTP para autenticación</span><span class="sxs-lookup"><span data-stu-id="cf1e3-171">SMTP Service extension for Authentication</span></span>](https://tools.ietf.org/html/rfc4954)
