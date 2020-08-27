---
title: Autenticar una aplicación EWS mediante OAuth
manager: sethgros
ms.date: 05/17/2019
ms.audience: Developer
ms.assetid: 1d8d57f9-4df5-4f21-9bbb-a89e0e259052
description: Obtenga información sobre cómo usar la autenticación OAuth con las aplicaciones de la API administrada de EWS.
localization_priority: Priority
ms.openlocfilehash: 795cbcc3dd1c895850086ebf0e23da905c1c99b7
ms.sourcegitcommit: 636c05a929279812c6ef87d75b01c166a4a05584
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2020
ms.locfileid: "47254968"
---
<!-- markdownlint-disable MD025 -->
# <a name="authenticate-an-ews-application-by-using-oauth"></a>Autenticar una aplicación EWS mediante OAuth
<!-- markdownlint-enable MD025 -->

Obtenga información sobre cómo usar la autenticación OAuth con las aplicaciones de la API administrada de EWS.

Puede usar el servicio de autenticación OAuth proporcionado por Azure Active Directory para permitir que las aplicaciones de la API administrada de EWS obtengan acceso a Exchange Online en Office 365. Para usar OAuth con la aplicación tendrá que:

1. [Registrar la aplicación](#register-your-application) con Azure Active Directory.

2. [Agregar código para obtener un token de autenticación](#add-code-to-get-an-authentication-token) para obtener un token de autenticación de un servidor de tokens.

3. [Agregar un token de autenticación a las solicitudes de EWS](#add-an-authentication-token-to-ews-requests) que envíe.

> [!NOTE]
> La autenticación OAuth para EWS solo está disponible en Exchange como parte de Office 365. Las aplicaciones de EWS que usan OAuth deben registrarse con Azure Active Directory.

Para usar el código de este artículo, tendrá que tener acceso a lo siguiente:

- Una cuenta de Office 365 con un buzón de Exchange Online. Si no tiene una cuenta de Office 365, puede obtener una suscripción gratuita de Office 365 si [se registra en el Programa de desarrolladores de Office 365](https://developer.microsoft.com/office/dev-program).

- La [Biblioteca de autenticación de Microsoft para .NET](/dotnet/api/microsoft.identity.client?view=azure-dotnet).

- La [API administrada de EWS](https://github.com/officedev/ews-managed-api).


Hay dos tipos de permisos OAuth que se pueden usar para obtener acceso a las API de EWS en Exchange Online. Antes de continuar con el tutorial, tendrá que seleccionar el tipo de permiso específico que desea usar.

* Los **permisos delegados** los usan las aplicaciones en las que un usuario debe haber iniciado sesión. En estas aplicaciones, el usuario o un administrador dan su consentimiento a los permisos que solicita la aplicación, y la aplicación puede actuar como un usuario que ha iniciado sesión cuando se hacen llamadas de API. 
* Los **permisos de aplicación** son los que usan las aplicaciones que se ejecutan sin que un usuario haya iniciado sesión, como las aplicaciones que se ejecutan como servicios en segundo plano o demonios y que pueden acceder a varios buzones.

## <a name="register-your-application"></a>Registrar su aplicación

Para usar OAuth, una aplicación debe tener un Id. de aplicación emitido por Azure Active Directory. En este tutorial, se presupone que la aplicación es una aplicación de consola, por lo que necesita registrar la aplicación como cliente público con Azure Active Directory.

1. Abra un explorador y vaya al [centro de administración de Azure Active Directory](https://aad.portal.azure.com) e inicie sesión con una **cuenta personal** (también conocida como: cuenta Microsoft) o una **cuenta profesional o educativa**.

1. Seleccione **Azure Active Directory** en el panel de navegación izquierdo y, a continuación, seleccione **Registros de aplicaciones** en **Administrar**.

1. Seleccione **Nuevo registro**. En la página **Registrar una aplicación**, establezca los valores siguientes.

    - Establezca **Nombre** como un nombre descriptivo para la aplicación.
    - Configure **Tipos de cuenta compatibles** de manera adecuada para su escenario.
    - Para **URI de redirección**, cambie la lista desplegable a **Cliente público (dispositivo móvil y escritorio)** y establezca el valor en `urn:ietf:wg:oauth:2.0:oob`.

1. Elija **Registrar**. En la página siguiente, copie el valor del **Id. de aplicación (cliente)** y guárdelo, ya que lo necesitará más adelante.

1. Seleccione **Permisos API** en el panel de navegación de la parte izquierda, en **Administrar**. 

1. Seleccione **Agregar un permiso** En la página **Solicitar permisos de la API**, seleccione **Exchange** en **API de herencia compatibles**. 

1. Para usar permisos delegados, seleccione **Permisos delegados** y, después, seleccione **EWS.AccessAsUser.All** en **EWS**. Haga clic en **Agregar permisos**. 

Para usar los permisos de aplicación, siga estos pasos adicionales.

1. Seleccione **Permisos de aplicación** y, a continuación, seleccione **full_access_as_app**. Haga clic en **Agregar permisos**.

1. Seleccione **Conceder consentimiento de administrador para organización** y acepte el cuadro de diálogo de consentimiento. 

1. Seleccione **Certificados y secretos** en el panel de navegación de la parte izquierda, en **Administrar**. 

1. Seleccione **Nuevo secreto de cliente**, escriba una descripción breve y seleccione **Agregar**.

1. Copie el **Valor** del secreto de cliente recién agregado y guárdelo, ya que lo necesitará más adelante. 

## <a name="add-code-to-get-an-authentication-token"></a>Agregar código para obtener un token de autenticación

Los siguientes fragmentos de código muestran cómo usar la Biblioteca de autenticación de Microsoft para obtener los tokens de autenticación de los permisos delegados y los permisos de aplicación. En estos fragmentos se presupone que la información necesaria para realizar la solicitud de autenticación está almacenada en el archivo **App.config** de la aplicación. Entre estos ejemplos no se incluyen la comprobación de errores. Consulte los [Ejemplos de código](#code-samples) para el código completo.

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

### <a name="application-permissions"></a>Permisos de aplicación

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

## <a name="add-an-authentication-token-to-ews-requests"></a>Agregar un token de autenticación a las solicitudes de EWS

Tras recibir el objeto **AuthenticationResult**, puede usar la propiedad **AccessToken** para obtener el token emitido por el servicio de token.

```cs
// Configure the ExchangeService with the access token
var ewsClient = new ExchangeService();
ewsClient.Url = new Uri("https://outlook.office365.com/EWS/Exchange.asmx");
ewsClient.Credentials = new OAuthCredentials(authResult.AccessToken);
```

Para usar permisos de aplicación, también tendrá que suplantar manera explícita un buzón al que le gustaría acceder. 

```cs
//Impersonate the mailbox you'd like to access.
ewsClient.ImpersonatedUserId = new ImpersonatedUserId(ConnectingIdType.SmtpAddress, "test@demotenant.onmicrosoft.com");
```

## <a name="code-samples"></a>Muestras de código

### <a name="delegated-permissions"></a>Permisos delegados

A continuación, se muestra el ejemplo de código completo, en el que se muestra cómo realizar una solicitud EWS autenticada por OAuth mediante permisos delegados.

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

### <a name="application-permissions"></a>Permisos de aplicación

A continuación, se ofrece un ejemplo de código completo que muestra cómo realizar una solicitud EWS autenticada por OAuth mediante permisos de aplicación.

> [!NOTE]
> Cuando se usa la suplantación, debe usar siempre el encabezado de solicitud X-AnchorMailbox, que debe establecerse en el SMTP de la bandeja de entrada suplantada.

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

                //Include x-anchormailbox header
                ewsClient.HttpHeaders.Add("X-AnchorMailbox", "test@demotenant.onmicrosoft.com");

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
