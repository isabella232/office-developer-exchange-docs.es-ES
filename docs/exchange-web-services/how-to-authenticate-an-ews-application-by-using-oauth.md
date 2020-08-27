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
# <a name="authenticate-an-ews-application-by-using-oauth"></a><span data-ttu-id="c9b54-103">Autenticar una aplicación EWS mediante OAuth</span><span class="sxs-lookup"><span data-stu-id="c9b54-103">Authenticate an EWS application by using OAuth</span></span>
<!-- markdownlint-enable MD025 -->

<span data-ttu-id="c9b54-104">Obtenga información sobre cómo usar la autenticación OAuth con las aplicaciones de la API administrada de EWS.</span><span class="sxs-lookup"><span data-stu-id="c9b54-104">Learn how to use OAuth authentication with your EWS Managed API applications.</span></span>

<span data-ttu-id="c9b54-105">Puede usar el servicio de autenticación OAuth proporcionado por Azure Active Directory para permitir que las aplicaciones de la API administrada de EWS obtengan acceso a Exchange Online en Office 365.</span><span class="sxs-lookup"><span data-stu-id="c9b54-105">You can use the OAuth authentication service provided by Azure Active Directory to enable your EWS Managed API applications to access Exchange Online in Office 365.</span></span> <span data-ttu-id="c9b54-106">Para usar OAuth con la aplicación tendrá que:</span><span class="sxs-lookup"><span data-stu-id="c9b54-106">To use OAuth with your application you will need to:</span></span>

1. <span data-ttu-id="c9b54-107">[Registrar la aplicación](#register-your-application) con Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c9b54-107">[Register your application](#register-your-application) with Azure Active Directory.</span></span>

2. <span data-ttu-id="c9b54-108">[Agregar código para obtener un token de autenticación](#add-code-to-get-an-authentication-token) para obtener un token de autenticación de un servidor de tokens.</span><span class="sxs-lookup"><span data-stu-id="c9b54-108">[Add code to get an authentication token](#add-code-to-get-an-authentication-token) to get an authentication token from a token server.</span></span>

3. <span data-ttu-id="c9b54-109">[Agregar un token de autenticación a las solicitudes de EWS](#add-an-authentication-token-to-ews-requests) que envíe.</span><span class="sxs-lookup"><span data-stu-id="c9b54-109">[Add an authentication token to EWS requests](#add-an-authentication-token-to-ews-requests) that you send.</span></span>

> [!NOTE]
> <span data-ttu-id="c9b54-110">La autenticación OAuth para EWS solo está disponible en Exchange como parte de Office 365.</span><span class="sxs-lookup"><span data-stu-id="c9b54-110">OAuth authentication for EWS is only available in Exchange as part of Office 365.</span></span> <span data-ttu-id="c9b54-111">Las aplicaciones de EWS que usan OAuth deben registrarse con Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c9b54-111">EWS applications that use OAuth must be registered with Azure Active Directory.</span></span>

<span data-ttu-id="c9b54-112">Para usar el código de este artículo, tendrá que tener acceso a lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="c9b54-112">To use the code in this article, you will need to have access to the following:</span></span>

- <span data-ttu-id="c9b54-113">Una cuenta de Office 365 con un buzón de Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="c9b54-113">An Office 365 account with an Exchange Online mailbox.</span></span> <span data-ttu-id="c9b54-114">Si no tiene una cuenta de Office 365, puede obtener una suscripción gratuita de Office 365 si [se registra en el Programa de desarrolladores de Office 365](https://developer.microsoft.com/office/dev-program).</span><span class="sxs-lookup"><span data-stu-id="c9b54-114">If you do not have an Office 365 account, you can [sign up for the Office 365 Developer Program](https://developer.microsoft.com/office/dev-program) to get a free Office 365 subscription.</span></span>

- <span data-ttu-id="c9b54-115">La [Biblioteca de autenticación de Microsoft para .NET](/dotnet/api/microsoft.identity.client?view=azure-dotnet).</span><span class="sxs-lookup"><span data-stu-id="c9b54-115">The [Microsoft Authentication Library for .NET](/dotnet/api/microsoft.identity.client?view=azure-dotnet).</span></span>

- <span data-ttu-id="c9b54-116">La [API administrada de EWS](https://github.com/officedev/ews-managed-api).</span><span class="sxs-lookup"><span data-stu-id="c9b54-116">The [EWS Managed API](https://github.com/officedev/ews-managed-api).</span></span>


<span data-ttu-id="c9b54-117">Hay dos tipos de permisos OAuth que se pueden usar para obtener acceso a las API de EWS en Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="c9b54-117">There are two types of OAuth permissions that can be used to access EWS APIs in Exchange Online.</span></span> <span data-ttu-id="c9b54-118">Antes de continuar con el tutorial, tendrá que seleccionar el tipo de permiso específico que desea usar.</span><span class="sxs-lookup"><span data-stu-id="c9b54-118">Before you proceed with the tutorial, you will need to choose the specific permission type to use.</span></span>

* <span data-ttu-id="c9b54-119">Los **permisos delegados** los usan las aplicaciones en las que un usuario debe haber iniciado sesión.</span><span class="sxs-lookup"><span data-stu-id="c9b54-119">**Delegated permissions** are used by apps that have a signed-in user present.</span></span> <span data-ttu-id="c9b54-120">En estas aplicaciones, el usuario o un administrador dan su consentimiento a los permisos que solicita la aplicación, y la aplicación puede actuar como un usuario que ha iniciado sesión cuando se hacen llamadas de API.</span><span class="sxs-lookup"><span data-stu-id="c9b54-120">For these apps, either the user or an administrator consents to the permissions that the app requests and the app can act as the signed-in user when making API calls.</span></span> 
* <span data-ttu-id="c9b54-121">Los **permisos de aplicación** son los que usan las aplicaciones que se ejecutan sin que un usuario haya iniciado sesión, como las aplicaciones que se ejecutan como servicios en segundo plano o demonios y que pueden acceder a varios buzones.</span><span class="sxs-lookup"><span data-stu-id="c9b54-121">**Application permissions** are used by apps that run without a signed-in user present; for example, apps that run as background services or daemons and can access multiple mailboxes.</span></span>

## <a name="register-your-application"></a><span data-ttu-id="c9b54-122">Registrar su aplicación</span><span class="sxs-lookup"><span data-stu-id="c9b54-122">Register your application</span></span>

<span data-ttu-id="c9b54-123">Para usar OAuth, una aplicación debe tener un Id. de aplicación emitido por Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c9b54-123">To use OAuth, an application must have an application ID issued by Azure Active Directory.</span></span> <span data-ttu-id="c9b54-124">En este tutorial, se presupone que la aplicación es una aplicación de consola, por lo que necesita registrar la aplicación como cliente público con Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c9b54-124">In this tutorial, it is assumed that the application is a console application, so you need to register your application as a public client with Azure Active Directory.</span></span>

1. <span data-ttu-id="c9b54-125">Abra un explorador y vaya al [centro de administración de Azure Active Directory](https://aad.portal.azure.com) e inicie sesión con una **cuenta personal** (también conocida como: cuenta Microsoft) o una **cuenta profesional o educativa**.</span><span class="sxs-lookup"><span data-stu-id="c9b54-125">Open a browser and navigate to the [Azure Active Directory admin center](https://aad.portal.azure.com) and login using a **personal account** (aka: Microsoft Account) or **Work or School Account**.</span></span>

1. <span data-ttu-id="c9b54-126">Seleccione **Azure Active Directory** en el panel de navegación izquierdo y, a continuación, seleccione **Registros de aplicaciones** en **Administrar**.</span><span class="sxs-lookup"><span data-stu-id="c9b54-126">Select **Azure Active Directory** in the left-hand navigation, then select **App registrations** under **Manage**.</span></span>

1. <span data-ttu-id="c9b54-127">Seleccione **Nuevo registro**.</span><span class="sxs-lookup"><span data-stu-id="c9b54-127">Select **New registration**.</span></span> <span data-ttu-id="c9b54-128">En la página **Registrar una aplicación**, establezca los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="c9b54-128">On the **Register an application** page, set the values as follows.</span></span>

    - <span data-ttu-id="c9b54-129">Establezca **Nombre** como un nombre descriptivo para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c9b54-129">Set **Name** to a friendly name for your app.</span></span>
    - <span data-ttu-id="c9b54-130">Configure **Tipos de cuenta compatibles** de manera adecuada para su escenario.</span><span class="sxs-lookup"><span data-stu-id="c9b54-130">Set **Supported account types** to the choice that makes sense for your scenario.</span></span>
    - <span data-ttu-id="c9b54-131">Para **URI de redirección**, cambie la lista desplegable a **Cliente público (dispositivo móvil y escritorio)** y establezca el valor en `urn:ietf:wg:oauth:2.0:oob`.</span><span class="sxs-lookup"><span data-stu-id="c9b54-131">For **Redirect URI**, change the dropdown to **Public client (mobile & desktop)** and set the value to `urn:ietf:wg:oauth:2.0:oob`.</span></span>

1. <span data-ttu-id="c9b54-132">Elija **Registrar**.</span><span class="sxs-lookup"><span data-stu-id="c9b54-132">Choose **Register**.</span></span> <span data-ttu-id="c9b54-133">En la página siguiente, copie el valor del **Id. de aplicación (cliente)** y guárdelo, ya que lo necesitará más adelante.</span><span class="sxs-lookup"><span data-stu-id="c9b54-133">On the next page, copy the value of the **Application (client) ID** and save it, you will need it later.</span></span>

1. <span data-ttu-id="c9b54-134">Seleccione **Permisos API** en el panel de navegación de la parte izquierda, en **Administrar**.</span><span class="sxs-lookup"><span data-stu-id="c9b54-134">Select **API permissions** in the left-hand navigation under **Manage**.</span></span> 

1. <span data-ttu-id="c9b54-135">Seleccione **Agregar un permiso**</span><span class="sxs-lookup"><span data-stu-id="c9b54-135">Select **Add a permission**.</span></span> <span data-ttu-id="c9b54-136">En la página **Solicitar permisos de la API**, seleccione **Exchange** en **API de herencia compatibles**.</span><span class="sxs-lookup"><span data-stu-id="c9b54-136">On the **Request API permissions** page, select **Exchange** under **Supported legacy APIs**.</span></span> 

1. <span data-ttu-id="c9b54-137">Para usar permisos delegados, seleccione **Permisos delegados** y, después, seleccione **EWS.AccessAsUser.All** en **EWS**.</span><span class="sxs-lookup"><span data-stu-id="c9b54-137">To use Delegated permissions, select **Delegated permissions** and then select **EWS.AccessAsUser.All** under **EWS**.</span></span> <span data-ttu-id="c9b54-138">Haga clic en **Agregar permisos**.</span><span class="sxs-lookup"><span data-stu-id="c9b54-138">Click on **Add permissions**.</span></span> 

<span data-ttu-id="c9b54-139">Para usar los permisos de aplicación, siga estos pasos adicionales.</span><span class="sxs-lookup"><span data-stu-id="c9b54-139">To use Application permissions, follow these additional steps.</span></span>

1. <span data-ttu-id="c9b54-140">Seleccione **Permisos de aplicación** y, a continuación, seleccione **full_access_as_app**.</span><span class="sxs-lookup"><span data-stu-id="c9b54-140">Select **Application permissions** and then select **full_access_as_app**.</span></span> <span data-ttu-id="c9b54-141">Haga clic en **Agregar permisos**.</span><span class="sxs-lookup"><span data-stu-id="c9b54-141">Click on **Add permissions**.</span></span>

1. <span data-ttu-id="c9b54-142">Seleccione **Conceder consentimiento de administrador para organización** y acepte el cuadro de diálogo de consentimiento.</span><span class="sxs-lookup"><span data-stu-id="c9b54-142">Select **Grant admin consent for org** and accept the consent dialog.</span></span> 

1. <span data-ttu-id="c9b54-143">Seleccione **Certificados y secretos** en el panel de navegación de la parte izquierda, en **Administrar**.</span><span class="sxs-lookup"><span data-stu-id="c9b54-143">Select **Certificates & Secrets** in the left-hand navigation under **Manage**.</span></span> 

1. <span data-ttu-id="c9b54-144">Seleccione **Nuevo secreto de cliente**, escriba una descripción breve y seleccione **Agregar**.</span><span class="sxs-lookup"><span data-stu-id="c9b54-144">Select **New client secret**, enter a short description and select **Add**.</span></span>

1. <span data-ttu-id="c9b54-145">Copie el **Valor** del secreto de cliente recién agregado y guárdelo, ya que lo necesitará más adelante.</span><span class="sxs-lookup"><span data-stu-id="c9b54-145">Copy the **Value** of the newly added client secret and save it, you will need it later.</span></span> 

## <a name="add-code-to-get-an-authentication-token"></a><span data-ttu-id="c9b54-146">Agregar código para obtener un token de autenticación</span><span class="sxs-lookup"><span data-stu-id="c9b54-146">Add code to get an authentication token</span></span>

<span data-ttu-id="c9b54-147">Los siguientes fragmentos de código muestran cómo usar la Biblioteca de autenticación de Microsoft para obtener los tokens de autenticación de los permisos delegados y los permisos de aplicación.</span><span class="sxs-lookup"><span data-stu-id="c9b54-147">The following code snippets show how to use the Microsoft Authentication Library to get authentication tokens for delegated permissions and application permissions.</span></span> <span data-ttu-id="c9b54-148">En estos fragmentos se presupone que la información necesaria para realizar la solicitud de autenticación está almacenada en el archivo **App.config** de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c9b54-148">These snippets assume that the information required to make the authentication request is stored in the application's **App.config** file.</span></span> <span data-ttu-id="c9b54-149">Entre estos ejemplos no se incluyen la comprobación de errores. Consulte los [Ejemplos de código](#code-samples) para el código completo.</span><span class="sxs-lookup"><span data-stu-id="c9b54-149">These examples do not include error checking, see the [Code samples](#code-samples) for the complete code.</span></span>

### <a name="delegated-permissions"></a><span data-ttu-id="c9b54-150">Permisos delegados</span><span class="sxs-lookup"><span data-stu-id="c9b54-150">Delegated permissions</span></span>

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

### <a name="application-permissions"></a><span data-ttu-id="c9b54-151">Permisos de aplicación</span><span class="sxs-lookup"><span data-stu-id="c9b54-151">Application permissions</span></span>

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

## <a name="add-an-authentication-token-to-ews-requests"></a><span data-ttu-id="c9b54-152">Agregar un token de autenticación a las solicitudes de EWS</span><span class="sxs-lookup"><span data-stu-id="c9b54-152">Add an authentication token to EWS requests</span></span>

<span data-ttu-id="c9b54-153">Tras recibir el objeto **AuthenticationResult**, puede usar la propiedad **AccessToken** para obtener el token emitido por el servicio de token.</span><span class="sxs-lookup"><span data-stu-id="c9b54-153">After you've received the **AuthenticationResult** object you can use the **AccessToken** property to get the token issued by the token service.</span></span>

```cs
// Configure the ExchangeService with the access token
var ewsClient = new ExchangeService();
ewsClient.Url = new Uri("https://outlook.office365.com/EWS/Exchange.asmx");
ewsClient.Credentials = new OAuthCredentials(authResult.AccessToken);
```

<span data-ttu-id="c9b54-154">Para usar permisos de aplicación, también tendrá que suplantar manera explícita un buzón al que le gustaría acceder.</span><span class="sxs-lookup"><span data-stu-id="c9b54-154">To use Application permissions, you will also need to explictly impersonate a mailbox that you would like to access.</span></span> 

```cs
//Impersonate the mailbox you'd like to access.
ewsClient.ImpersonatedUserId = new ImpersonatedUserId(ConnectingIdType.SmtpAddress, "test@demotenant.onmicrosoft.com");
```

## <a name="code-samples"></a><span data-ttu-id="c9b54-155">Muestras de código</span><span class="sxs-lookup"><span data-stu-id="c9b54-155">Code samples</span></span>

### <a name="delegated-permissions"></a><span data-ttu-id="c9b54-156">Permisos delegados</span><span class="sxs-lookup"><span data-stu-id="c9b54-156">Delegated permissions</span></span>

<span data-ttu-id="c9b54-157">A continuación, se muestra el ejemplo de código completo, en el que se muestra cómo realizar una solicitud EWS autenticada por OAuth mediante permisos delegados.</span><span class="sxs-lookup"><span data-stu-id="c9b54-157">The following is the complete code sample that demonstrates making an OAuth-authenticated EWS request using Delegated permissions.</span></span>

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

### <a name="application-permissions"></a><span data-ttu-id="c9b54-158">Permisos de aplicación</span><span class="sxs-lookup"><span data-stu-id="c9b54-158">Application permissions</span></span>

<span data-ttu-id="c9b54-159">A continuación, se ofrece un ejemplo de código completo que muestra cómo realizar una solicitud EWS autenticada por OAuth mediante permisos de aplicación.</span><span class="sxs-lookup"><span data-stu-id="c9b54-159">The following is the complete code sample that demonstrates making an OAuth-authenticated EWS request using Application permissions.</span></span>

> [!NOTE]
> <span data-ttu-id="c9b54-160">Cuando se usa la suplantación, debe usar siempre el encabezado de solicitud X-AnchorMailbox, que debe establecerse en el SMTP de la bandeja de entrada suplantada.</span><span class="sxs-lookup"><span data-stu-id="c9b54-160">When using impersonation you must always use the X-AnchorMailbox request header, which should be set to the SMTP of the impersonated mailbox.</span></span>

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

<span data-ttu-id="c9b54-161">En ambos casos, el ejemplo de código requiere un archivo **App.config** con las entradas siguientes:</span><span class="sxs-lookup"><span data-stu-id="c9b54-161">The sample code in both cases requires an **App.config** file with the following entries:</span></span>

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

## <a name="see-also"></a><span data-ttu-id="c9b54-162">Vea también</span><span class="sxs-lookup"><span data-stu-id="c9b54-162">See also</span></span>

- [<span data-ttu-id="c9b54-163">Autenticación y EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="c9b54-163">Authentication and EWS in Exchange</span></span>](authentication-and-ews-in-exchange.md)
