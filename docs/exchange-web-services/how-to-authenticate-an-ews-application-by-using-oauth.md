---
title: Autenticar una aplicación EWS mediante OAuth
manager: sethgros
ms.date: 05/17/2019
ms.audience: Developer
ms.assetid: 1d8d57f9-4df5-4f21-9bbb-a89e0e259052
description: Obtenga información sobre cómo usar la autenticación OAuth con sus aplicaciones de API administrada de EWS.
localization_priority: Priority
ms.openlocfilehash: 0375095faac918859354da026118ea4ccfd6792b
ms.sourcegitcommit: eeda51cb037aa25566adb293f25574674fdb2d9e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/01/2020
ms.locfileid: "45012569"
---
<!-- markdownlint-disable MD025 -->
# <a name="authenticate-an-ews-application-by-using-oauth"></a>Autenticar una aplicación EWS mediante OAuth
<!-- markdownlint-enable MD025 -->

Obtenga información sobre cómo usar la autenticación OAuth con sus aplicaciones de API administrada de EWS.

Puede usar el servicio de autenticación OAuth proporcionado por Azure Active Directory para permitir que las aplicaciones de la API administrada de EWS obtengan acceso a Exchange online en Office 365. Para usar OAuth con la aplicación, deberá:

1. [Registre la aplicación](#register-your-application) con Azure Active Directory.

2. [Agregue código para obtener un token de autenticación](#add-code-to-get-an-authentication-token) para obtener un token de autenticación de un servidor de tokens.

3. [Agregue un token de autenticación a las solicitudes de EWS](#add-an-authentication-token-to-ews-requests) que envíe.

> [!NOTE]
> La autenticación OAuth para EWS solo está disponible en Exchange como parte de Office 365. Las aplicaciones de EWS que usan OAuth deben registrarse con Azure Active Directory.

Para usar el código de este artículo, tendrá que tener acceso a lo siguiente:

- Una cuenta de Office 365 con un buzón de correo de Exchange Online. Si no tiene una cuenta de Office 365, puede [registrarse para el programa de desarrolladores de office 365](https://developer.microsoft.com/office/dev-program) para obtener una suscripción gratuita a Office 365.

- La [biblioteca de autenticación de Microsoft para .net](/dotnet/api/microsoft.identity.client?view=azure-dotnet).

- La [API administrada EWS](https://github.com/officedev/ews-managed-api).


Hay dos tipos de permisos de OAuth que se pueden usar para acceder a las API de EWS en Exchange Online. Antes de continuar con el tutorial, deberá elegir el tipo de permiso específico que se va a usar.

* Los **permisos delegados** los usan las aplicaciones en las que un usuario debe haber iniciado sesión. Para estas aplicaciones, el usuario o un administrador confirman los permisos que la aplicación solicita y la aplicación puede actuar como el usuario que ha iniciado sesión al realizar llamadas a la API. 
* **Los permisos de aplicación** se usan en aplicaciones que se ejecutan sin la presencia de un usuario que ha iniciado sesión; por ejemplo, aplicaciones que se ejecutan como daemons o servicios en segundo plano y que pueden tener acceso a varios buzones.

## <a name="register-your-application"></a>Registrar la aplicación

Para usar OAuth, una aplicación debe tener un identificador de aplicación emitido por Azure Active Directory. En este tutorial, se da por supuesto que la aplicación es una aplicación de consola, por lo que debe registrar la aplicación como cliente público con Azure Active Directory.

1. Abra un explorador y vaya al [centro de administración de Azure Active Directory](https://aad.portal.azure.com) e inicie sesión con una **cuenta personal** (también conocida como: cuenta Microsoft) o una **cuenta profesional o educativa**.

1. Seleccione **Azure Active Directory** en el panel de navegación de la izquierda y, después, seleccione **registros de aplicaciones** en **administrar**.

1. Seleccione **Nuevo registro**. En la página **Registrar una aplicación**, establezca los valores siguientes.

    - Establezca **Name** en un nombre descriptivo para la aplicación.
    - Establezca los **tipos de cuenta admitidos** en la opción adecuada para su escenario.
    - Para el **URI de redireccionamiento**, cambie la lista desplegable a **cliente público (móvil & escritorio)** y establezca el valor en `urn:ietf:wg:oauth:2.0:oob` .

1. Elija **Registrar**. En la página siguiente, copie el valor del identificador de la **aplicación (cliente)** y guárdelo, lo necesitará más adelante.

1. Seleccione **permisos de API** en el panel de navegación izquierdo en **administrar**. 

1. Seleccione **Agregar un permiso**. En la página **solicitar permisos de API** , seleccione **Exchange** en **API heredadas admitidas**. 

1. Para usar permisos delegados, seleccione **permisos delegados** y, después, seleccione **EWS. AccessAsUser. All** en **EWS**. Haga clic en **Agregar permisos**. 

Para usar los permisos de la aplicación, siga estos pasos adicionales.

1. Seleccione **permisos** de la aplicación y, a continuación, seleccione **full_access_as_app**. Haga clic en **Agregar permisos**.

1. Seleccione **conceder consentimiento de administrador para org** y acepte el cuadro de diálogo de consentimiento. 

1. Seleccione **certificados & secretos** en el panel de navegación izquierdo en **administrar**. 

1. Seleccione **nuevo secreto de cliente**, escriba una descripción breve y seleccione **Agregar**.

1. Copie el **valor** del secreto de cliente recién agregado y guárdelo, lo necesitará más adelante. 

## <a name="add-code-to-get-an-authentication-token"></a>Agregar código para obtener un token de autenticación

Los fragmentos de código siguientes muestran cómo usar la biblioteca de autenticación de Microsoft para obtener tokens de autenticación para permisos delegados y permisos de aplicación. En estos fragmentos de código se presupone que la información necesaria para realizar la solicitud de autenticación se almacena en el archivo de **App.config** de la aplicación. Estos ejemplos no incluyen la comprobación de errores, vea los [ejemplos de código](#code-samples) para obtener el código completo.

### <a name="delegated-permissions"></a>Permisos delegados

```cs
// Configure the MSAL client to get tokens
var pcaOptions = new PublicClientApplicationOptions
{
    ClientId = ConfigurationManager.AppSettings["appId"],
    TenantId = ConfigurationManager.AppSettings["tenantId"]
};

var pca = PublicClientApplicationBuilder
    .CreateWithApplicationOptions(pcaOptions).Build();

// The permission scope required for EWS access
var ewsScopes = new string[] { "https://outlook.office.com/EWS.AccessAsUser.All" };

// Make the interactive token request
var authResult = await pca.AcquireTokenInteractive(ewsScopes).ExecuteAsync();
```

### <a name="application-permissions"></a>Permisos de la aplicación

```cs
// Configure the MSAL client to get tokens
var app = ConfidentialClientApplicationBuilder
    .Create(ConfigurationManager.AppSettings["appId"])
    .WithAuthority(AzureCloudInstance.AzurePublic, ConfigurationManager.AppSettings["tenantId"])
    .WithClientSecret(ConfigurationManager.AppSettings["clientSecret"]).Build();

// The permission scope required for EWS access
var ewsScopes = new string[] { "https://outlook.office.com/.default" };

//Make the token request
AuthenticationResult authResult = await app.AcquireTokenForClient(ewsScopes).ExecuteAsync();

```

## <a name="add-an-authentication-token-to-ews-requests"></a>Adición de un token de autenticación a las solicitudes de EWS

Una vez que haya recibido el objeto **AuthenticationResult** , puede usar la propiedad **AccessToken** para obtener el token emitido por el servicio de token.

```cs
// Configure the ExchangeService with the access token
var ewsClient = new ExchangeService();
ewsClient.Url = new Uri("https://outlook.office365.com/EWS/Exchange.asmx");
ewsClient.Credentials = new OAuthCredentials(authResult.AccessToken);
```

Para usar los permisos de la aplicación, también tendrá que suplantar explícitamente un buzón al que desee tener acceso. 

```cs
//Impersonate the mailbox you'd like to access.
ewsClient.ImpersonatedUserId = new ImpersonatedUserId(ConnectingIdType.SmtpAddress, "test@demotenant.onmicrosoft.com");
```

## <a name="code-samples"></a>Muestras de código

### <a name="delegated-permissions"></a>Permisos delegados

El siguiente es el ejemplo de código completo que muestra cómo realizar una solicitud EWS autenticada con OAuth mediante permisos delegados.

```cs
using Microsoft.Exchange.WebServices.Data;
using Microsoft.Identity.Client;
using System;
using System.Configuration;

namespace EwsOAuth
{
    class Program
    {
        static void Main(string[] args)
        {
            MainAsync(args).Wait();

            if (System.Diagnostics.Debugger.IsAttached)
            {
                Console.WriteLine("Hit any key to exit...");
                Console.ReadKey();
            }
        }

        static async System.Threading.Tasks.Task MainAsync(string[] args)
        {
            // Configure the MSAL client to get tokens
            var pcaOptions = new PublicClientApplicationOptions
            {
                ClientId = ConfigurationManager.AppSettings["appId"],
                TenantId = ConfigurationManager.AppSettings["tenantId"]
            };

            var pca = PublicClientApplicationBuilder
                .CreateWithApplicationOptions(pcaOptions).Build();

            var ewsScopes = new string[] { "https://outlook.office.com/EWS.AccessAsUser.All" };

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
                Console.WriteLine($"Error acquiring access token: {ex.ToString()}");
            }
            catch (Exception ex)
            {
                Console.WriteLine($"Error: {ex.ToString()}");
            }
        }
    }
}
```

### <a name="application-permissions"></a>Permisos de la aplicación

El siguiente es el ejemplo de código completo que muestra cómo realizar una solicitud EWS autenticada con OAuth mediante permisos de aplicación.

```cs
using System;
using System.Configuration;
using Microsoft.Exchange.WebServices.Data;
using Microsoft.Identity.Client;

namespace ews_oauth_samples
{
    class Program
    {
        static void Main(string[] args)
        {
            MainAsync(args).Wait();

            if (System.Diagnostics.Debugger.IsAttached)
            {
                Console.WriteLine("Hit any key to exit...");
                Console.ReadKey();
            }
        }
        
        static async System.Threading.Tasks.Task MainAsync(string[] args)
        {
            // Configure the MSAL client to get tokens
            var ewsScopes = new string[] { "https://outlook.office.com/.default" };

            var app = ConfidentialClientApplicationBuilder.Create(ConfigurationManager.AppSettings["appId"])
                .WithAuthority(AzureCloudInstance.AzurePublic, ConfigurationManager.AppSettings["tenantId"])
                .WithClientSecret(ConfigurationManager.AppSettings["clientSecret"])
                .Build();

            AuthenticationResult result = null;

            try
            {
                // Make the interactive token request
                result = await app.AcquireTokenForClient(ewsScopes)
                    .ExecuteAsync();

                // Configure the ExchangeService with the access token
                var ewsClient = new ExchangeService();
                ewsClient.Url = new Uri("https://outlook.office365.com/EWS/Exchange.asmx");
                ewsClient.Credentials = new OAuthCredentials(result.AccessToken);

                //Impersonate the mailbox you'd like to access.
                ewsClient.ImpersonatedUserId = new ImpersonatedUserId(ConnectingIdType.SmtpAddress, "test@demotenant.onmicrosoft.com");

                // Make an EWS call
                var folders = ewsClient.FindFolders(WellKnownFolderName.MsgFolderRoot, new FolderView(10));
                foreach (var folder in folders)
                {
                    Console.WriteLine($"Folder: {folder.DisplayName}");
                }
            }
            catch (MsalException ex)
            {
                Console.WriteLine($"Error acquiring access token: {ex.ToString()}");
            }
            catch (Exception ex)
            {
                Console.WriteLine($"Error: {ex.ToString()}");
            }
        }
    }
}
```

En ambos casos, el código de ejemplo requiere un archivo **App.config** con las siguientes entradas:

```xml
<?xml version="1.0" encoding="utf-8" ?>
<configuration>
  <startup>
    <supportedRuntime version="v4.0" sku=".NETFramework,Version=v4.7.2" />
  </startup>
  <appSettings>
    <!-- The application ID from your app registration -->
    <add key="appId" value="YOUR_APP_ID_HERE" />
    <!-- If you registered your app to support only users in your organization, change the value
           of this key to your tenant ID -->
    <add key="tenantId" value="common"/>
    <!-- The application's client secret from your app registration. Needed for application permission access -->
    <add key="clientSecret" value="YOUR_CLIENT_SECRET_HERE"/>
  </appSettings>
</configuration>
```

## <a name="see-also"></a>Vea también

- [Autenticación y EWS en Exchange](authentication-and-ews-in-exchange.md)
