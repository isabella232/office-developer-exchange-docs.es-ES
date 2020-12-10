---
title: Autenticar una aplicación EWS mediante OAuth
manager: sethgros
ms.date: 11/25/2020
ms.audience: Developer
ms.assetid: 1d8d57f9-4df5-4f21-9bbb-a89e0e259052
description: Obtenga información sobre cómo usar la autenticación OAuth con las aplicaciones de la API administrada de EWS.
localization_priority: Priority
ms.openlocfilehash: a7b1d2a099cf5f3c95f8453605363de12ff33c54
ms.sourcegitcommit: 843a2e030a94b12aec70c553ca4e06e39ac02d82
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/09/2020
ms.locfileid: "49603830"
---
<!-- markdownlint-disable MD025 -->
# <a name="authenticate-an-ews-application-by-using-oauth"></a>Autenticar una aplicación EWS mediante OAuth
<!-- markdownlint-enable MD025 -->

Obtenga información sobre cómo usar la autenticación OAuth con las aplicaciones de la API administrada de EWS.

Puede usar el servicio de autenticación OAuth proporcionado por Azure Active Directory para permitir que las aplicaciones de la API administrada de EWS obtengan acceso a Exchange Online en Office 365. Para usar OAuth con la aplicación tendrá que:

1. [Registrar la aplicación](#register-your-application) con Azure Active Directory.
1. [Agregar código para obtener un token de autenticación](#add-code-to-get-an-authentication-token) para obtener un token de autenticación de un servidor de tokens.
1. [Agregar un token de autenticación a las solicitudes de EWS](#add-an-authentication-token-to-ews-requests) que envíe.

> [!NOTE]
> La autenticación OAuth para EWS solo está disponible en Exchange como parte de Microsoft 365. Las aplicaciones de EWS que usan OAuth deben registrarse con Azure Active Directory.

Para usar el código de este artículo, tendrá que tener acceso a lo siguiente:

- Una cuenta de Microsoft 365 con un buzón de Exchange Online. Si no tiene una cuenta de Microsoft 365, puede [registrarse en el Programa de desarrolladores de Microsoft 365](https://developer.microsoft.com/microsoft-365/dev-program) para obtener una suscripción gratuita.
- La [Biblioteca de autenticación de Microsoft para .NET](/dotnet/api/microsoft.identity.client).
- La [API administrada de EWS](https://github.com/officedev/ews-managed-api).

Hay dos tipos de permisos OAuth que se pueden usar para obtener acceso a las API de EWS en Exchange Online. Antes de continuar con el tutorial, tendrá que seleccionar el tipo de permiso específico que desea usar.

- Los **permisos delegados** los usan las aplicaciones en las que un usuario debe haber iniciado sesión. En estas aplicaciones, el usuario o un administrador dan su consentimiento a los permisos que solicita la aplicación, y la aplicación puede actuar como un usuario que ha iniciado sesión cuando se hacen llamadas de API.
- Los **permisos de aplicación** son los que usan las aplicaciones que se ejecutan sin que un usuario haya iniciado sesión, como las aplicaciones que se ejecutan como servicios en segundo plano o demonios y que pueden acceder a varios buzones.

## <a name="register-your-application"></a>Registrar su aplicación

Para usar OAuth, una aplicación debe tener un Id. de aplicación emitido por Azure Active Directory. En este tutorial, se presupone que la aplicación es una aplicación de consola, por lo que necesita registrar la aplicación como cliente público con Azure Active Directory. Puede registrar una aplicación en el Centro de administración de Azure Active Directory o a través de Microsoft Graph.

1. Abra un explorador y vaya al [centro de administración de Azure Active Directory](https://aad.portal.azure.com) e inicie sesión con una **cuenta personal** (también conocida como: cuenta Microsoft) o una **cuenta profesional o educativa**.

1. Seleccione **Azure Active Directory** en el panel de navegación izquierdo y, a continuación, seleccione **Registros de aplicaciones** en **Administrar**.

1. Seleccione **Nuevo registro**. En la página **Registrar una aplicación**, establezca los valores siguientes.

    - Establezca **Nombre** como un nombre descriptivo para la aplicación.
    - Configure **Tipos de cuenta compatibles** de manera adecuada para su escenario.
    - Para **URI de redirección**, cambie la lista desplegable a **Cliente público (dispositivo móvil y escritorio)** y establezca el valor en `urn:ietf:wg:oauth:2.0:oob`.

1. Elija **Registrar**. En la página siguiente, copie los valores del **Id. de la aplicación (cliente)** y del **Id. del directorio (cuenta empresarial)** y guárdelos; los necesitará más adelante.

### <a name="configure-for-delegated-authentication"></a>Configurar para la autenticación delegada

Si la aplicación usa una autenticación delegada, no es necesario realizar ninguna configuración adicional. La [Plataforma de identidad de Microsoft](/azure/active-directory/develop/v2-overview) permite que las aplicaciones soliciten permisos de forma dinámica, por lo que no es necesario que configure previamente los permisos en el registro de la aplicación. Sin embargo, en algunos casos (como en el del [flujo con derechos delegados](/azure/active-directory/develop/v2-oauth2-on-behalf-of-flow)) se necesitan permisos para la configuración previa. Siga los siguientes pasos para configurar previamente los permisos de EWS.

1. Seleccione **Manifiesto** en el panel de navegación izquierdo, debajo de **Administrar**.

1. Localice la propiedad `requiredResourceAccess` en el manifiesto y agregue lo siguiente dentro de los corchetes (`[]`):

    ```json
    {
        "resourceAppId": "00000002-0000-0ff1-ce00-000000000000",
        "resourceAccess": [
            {
                "id": "3b5f3d61-589b-4a3c-a359-5dd4b5ee5bd5",
                "type": "Scope"
            }
        ]
    }
    ```

1. Seleccione **Guardar**.

1. Seleccione **Permisos de las API** en **Administrar**. Confirme que el permiso **EWS.AccessAsUser.All** aparezca en la lista.

### <a name="configure-for-app-only-authentication"></a>Configurar la autenticación solo para la aplicación

Para usar los permisos de la aplicación, siga estos pasos adicionales.

1. Seleccione **Manifiesto** en el panel de navegación izquierdo, debajo de **Administrar**.

1. Localice la propiedad `requiredResourceAccess` en el manifiesto y agregue lo siguiente dentro de los corchetes (`[]`):

    ```json
    {
        "resourceAppId": "00000002-0000-0ff1-ce00-000000000000",
        "resourceAccess": [
            {
                "id": "dc890d15-9560-4a4c-9b7f-a736ec74ec40",
                "type": "Role"
            }
        ]
    }
    ```

1. Seleccione **Guardar**.

1. Seleccione **Permisos de las API** en **Administrar**. Confirme que aparezca el permiso **full_access_as_app**.

1. Seleccione **Conceder consentimiento de administrador para organización** y acepte el cuadro de diálogo de consentimiento.

1. Seleccione **Certificados y secretos** en el panel de navegación de la parte izquierda, en **Administrar**.

1. Seleccione **Nuevo secreto de cliente**, escriba una descripción breve y seleccione **Agregar**.

1. Copie el **Valor** del secreto de cliente recién agregado y guárdelo, ya que lo necesitará más adelante.

## <a name="add-code-to-get-an-authentication-token"></a>Agregar código para obtener un token de autenticación

Los siguientes fragmentos de código muestran cómo usar la Biblioteca de autenticación de Microsoft para obtener los tokens de autenticación de los permisos delegados y los permisos de aplicación. En estos fragmentos se presupone que la información necesaria para realizar la solicitud de autenticación está almacenada en el archivo **App.config** de la aplicación. Entre estos ejemplos no se incluyen la comprobación de errores. Consulte los [Ejemplos de código](#code-samples) para el código completo.

### <a name="get-a-token-with-delegated-auth"></a>Obtener un token con la autenticación delegada

```cs
// Using Microsoft.Identity.Client 4.22.0

// Configure the MSAL client to get tokens
var pcaOptions = new PublicClientApplicationOptions
{
    ClientId = ConfigurationManager.AppSettings["appId"],
    TenantId = ConfigurationManager.AppSettings["tenantId"]
};

var pca = PublicClientApplicationBuilder
    .CreateWithApplicationOptions(pcaOptions).Build();

// The permission scope required for EWS access
var ewsScopes = new string[] { "https://outlook.office365.com/EWS.AccessAsUser.All" };

// Make the interactive token request
var authResult = await pca.AcquireTokenInteractive(ewsScopes).ExecuteAsync();
```

### <a name="get-a-token-with-app-only-auth"></a>Obtener un token con autenticación solo para la aplicación

```cs
// Using Microsoft.Identity.Client 4.22.0
var cca = ConfidentialClientApplicationBuilder
    .Create(ConfigurationManager.AppSettings["appId"])
    .WithClientSecret(ConfigurationManager.AppSettings["clientSecret"])
    .WithTenantId(ConfigurationManager.AppSettings["tenantId"])
    .Build();

// The permission scope required for EWS access
var ewsScopes = new string[] { "https://outlook.office365.com/.default" };

//Make the token request
var authResult = await cca.AcquireTokenForClient(ewsScopes).ExecuteAsync();
```

## <a name="add-an-authentication-token-to-ews-requests"></a>Agregar un token de autenticación a las solicitudes de EWS

Tras recibir el objeto **AuthenticationResult**, puede usar la propiedad **AccessToken** para obtener el token emitido por el servicio de token.

```cs
// Configure the ExchangeService with the access token
var ewsClient = new ExchangeService();
ewsClient.Url = new Uri("https://outlook.office365.com/EWS/Exchange.asmx");
ewsClient.Credentials = new OAuthCredentials(authResult.AccessToken);
```

Para usar los permisos de la aplicación, también tendrá que suplantar de manera explícita al buzón al que le gustaría acceder.

```cs
//Impersonate the mailbox you'd like to access.
ewsClient.ImpersonatedUserId = new ImpersonatedUserId(ConnectingIdType.SmtpAddress, "test@demotenant.onmicrosoft.com");
```

## <a name="code-samples"></a>Ejemplos de código

### <a name="delegated-authentication"></a>Autenticación delegada

El siguiente es un código de muestra completo que ejemplifica cómo realizar una solicitud EWS autenticada por OAuth usando los permisos delegados de la aplicación.

```cs
using Microsoft.Exchange.WebServices.Data;
using Microsoft.Identity.Client;
using System;
using System.Configuration;

namespace EwsOAuth
{
    class Program
    {
        static async System.Threading.Tasks.Task Main(string[] args)
        {
            // Using Microsoft.Identity.Client 4.22.0

            // Configure the MSAL client to get tokens
            var pcaOptions = new PublicClientApplicationOptions
            {
                ClientId = ConfigurationManager.AppSettings["appId"],
                TenantId = ConfigurationManager.AppSettings["tenantId"]
            };

            var pca = PublicClientApplicationBuilder
                .CreateWithApplicationOptions(pcaOptions).Build();

            // The permission scope required for EWS access
            var ewsScopes = new string[] { "https://outlook.office365.com/EWS.AccessAsUser.All" };

            try
            {
                // Make the interactive token request
                var authResult = await pca.AcquireTokenInteractive(ewsScopes).ExecuteAsync();

                // Configure the ExchangeService with the access token
                var ewsClient = new ExchangeService();
                ewsClient.Url = new Uri("https://outlook.office365.com/EWS/Exchange.asmx");
                ewsClient.Credentials = new OAuthCredentials(authResult.AccessToken);

                // Make an EWS call
                var folders = ewsClient.FindFolders(WellKnownFolderName.MsgFolderRoot, new FolderView(10));
                foreach(var folder in folders)
                {
                    Console.WriteLine($"Folder: {folder.DisplayName}");
                }
            }
            catch (MsalException ex)
            {
                Console.WriteLine($"Error acquiring access token: {ex}");
            }
            catch (Exception ex)
            {
                Console.WriteLine($"Error: {ex}");
            }

            if (System.Diagnostics.Debugger.IsAttached)
            {
                Console.WriteLine("Hit any key to exit...");
                Console.ReadKey();
            }
        }
    }
}
```

### <a name="app-only-authentication"></a>Autenticación solo para la aplicación

El siguiente es un código de muestra completo que ejemplifica cómo realizar una solicitud EWS autenticada por OAuth usando la autenticación solo para la aplicación.

> [!NOTE]
> Cuando se usa la suplantación, debe usar siempre el encabezado de la solicitud X-AnchorMailbox, el cual debería estar establecido para la dirección SMTP del buzón suplantado.

```cs
using Microsoft.Exchange.WebServices.Data;
using Microsoft.Identity.Client;
using System;
using System.Configuration;

namespace EwsOAuth
{
    class Program
    {
        static async System.Threading.Tasks.Task Main(string[] args)
        {
            // Using Microsoft.Identity.Client 4.22.0
            var cca = ConfidentialClientApplicationBuilder
                .Create(ConfigurationManager.AppSettings["appId"])
                .WithClientSecret(ConfigurationManager.AppSettings["clientSecret"])
                .WithTenantId(ConfigurationManager.AppSettings["tenantId"])
                .Build();

            var ewsScopes = new string[] { "https://outlook.office365.com/.default" };

            try
            {
                var authResult = await cca.AcquireTokenForClient(ewsScopes)
                    .ExecuteAsync();

                // Configure the ExchangeService with the access token
                var ewsClient = new ExchangeService();
                ewsClient.Url = new Uri("https://outlook.office365.com/EWS/Exchange.asmx");
                ewsClient.Credentials = new OAuthCredentials(authResult.AccessToken);
                ewsClient.ImpersonatedUserId =
                    new ImpersonatedUserId(ConnectingIdType.SmtpAddress, "meganb@contoso.onmicrosoft.com");

                //Include x-anchormailbox header
                ewsClient.HttpHeaders.Add("X-AnchorMailbox", "meganb@contoso.onmicrosoft.com");

                // Make an EWS call
                var folders = ewsClient.FindFolders(WellKnownFolderName.MsgFolderRoot, new FolderView(10));
                foreach(var folder in folders)
                {
                    Console.WriteLine($"Folder: {folder.DisplayName}");
                }
            }
            catch (MsalException ex)
            {
                Console.WriteLine($"Error acquiring access token: {ex}");
            }
            catch (Exception ex)
            {
                Console.WriteLine($"Error: {ex}");
            }

            if (System.Diagnostics.Debugger.IsAttached)
            {
                Console.WriteLine("Hit any key to exit...");
                Console.ReadKey();
            }
        }
    }
}
```

En ambos casos, el ejemplo de código requiere un archivo **App.config** con las entradas siguientes:

```xml
<?xml version="1.0" encoding="utf-8" ?>
<configuration>
  <startup>
    <supportedRuntime version="v4.0" sku=".NETFramework,Version=v4.7.2" />
  </startup>
  <appSettings>
    <!-- The application ID from your app registration -->
    <add key="appId" value="YOUR_APP_ID_HERE" />
    <!-- The tenant ID copied from your app registration -->
    <add key="tenantId" value="YOUR_TENANT_ID_HERE"/>
    <!-- The application's client secret from your app registration. Needed for application permission access -->
    <add key="clientSecret" value="YOUR_CLIENT_SECRET_HERE"/>
  </appSettings>
</configuration>
```

## <a name="see-also"></a>Vea también

- [Autenticación y EWS en Exchange](authentication-and-ews-in-exchange.md)
