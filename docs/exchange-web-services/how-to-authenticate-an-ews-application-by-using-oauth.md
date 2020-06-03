---
title: Autenticar una aplicación de EWS mediante OAuth
manager: sethgros
ms.date: 05/17/2019
ms.audience: Developer
ms.assetid: 1d8d57f9-4df5-4f21-9bbb-a89e0e259052
description: Obtenga información sobre cómo usar la autenticación OAuth con sus aplicaciones de API administrada de EWS.
localization_priority: Priority
ms.openlocfilehash: e2bcb339ddac51b888660b6f982a8377591b1a29
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44528254"
---
<!-- markdownlint-disable MD025 -->
# <a name="authenticate-an-ews-application-by-using-oauth"></a><span data-ttu-id="60ce7-103">Autenticar una aplicación de EWS mediante OAuth</span><span class="sxs-lookup"><span data-stu-id="60ce7-103">Authenticate an EWS application by using OAuth</span></span>
<!-- markdownlint-enable MD025 -->

<span data-ttu-id="60ce7-104">Obtenga información sobre cómo usar la autenticación OAuth con sus aplicaciones de API administrada de EWS.</span><span class="sxs-lookup"><span data-stu-id="60ce7-104">Learn how to use OAuth authentication with your EWS Managed API applications.</span></span>

<span data-ttu-id="60ce7-105">Puede usar el servicio de autenticación OAuth proporcionado por Azure Active Directory para permitir que las aplicaciones de la API administrada de EWS obtengan acceso a Exchange online en Office 365.</span><span class="sxs-lookup"><span data-stu-id="60ce7-105">You can use the OAuth authentication service provided by Azure Active Directory to enable your EWS Managed API applications to access Exchange Online in Office 365.</span></span> <span data-ttu-id="60ce7-106">Para usar OAuth con la aplicación, deberá:</span><span class="sxs-lookup"><span data-stu-id="60ce7-106">To use OAuth with your application you will need to:</span></span>

1. <span data-ttu-id="60ce7-107">[Registre la aplicación](#register-your-application) con Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="60ce7-107">[Register your application](#register-your-application) with Azure Active Directory.</span></span>

2. <span data-ttu-id="60ce7-108">[Agregue código para obtener un token de autenticación](#add-code-to-get-an-authentication-token) para obtener un token de autenticación de un servidor de tokens.</span><span class="sxs-lookup"><span data-stu-id="60ce7-108">[Add code to get an authentication token](#add-code-to-get-an-authentication-token) to get an authentication token from a token server.</span></span>

3. <span data-ttu-id="60ce7-109">[Agregue un token de autenticación a las solicitudes de EWS](#add-an-authentication-token-to-ews-requests) que envíe.</span><span class="sxs-lookup"><span data-stu-id="60ce7-109">[Add an authentication token to EWS requests](#add-an-authentication-token-to-ews-requests) that you send.</span></span>

> [!NOTE]
> <span data-ttu-id="60ce7-110">La autenticación OAuth para EWS solo está disponible en Exchange como parte de Office 365.</span><span class="sxs-lookup"><span data-stu-id="60ce7-110">OAuth authentication for EWS is only available in Exchange as part of Office 365.</span></span> <span data-ttu-id="60ce7-111">Las aplicaciones de EWS que usan OAuth deben registrarse con Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="60ce7-111">EWS applications that use OAuth must be registered with Azure Active Directory.</span></span>

<span data-ttu-id="60ce7-112">Para usar el código de este artículo, tendrá que tener acceso a lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="60ce7-112">To use the code in this article, you will need to have access to the following:</span></span>

- <span data-ttu-id="60ce7-113">Una cuenta de Office 365 con un buzón de correo de Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="60ce7-113">An Office 365 account with an Exchange Online mailbox.</span></span> <span data-ttu-id="60ce7-114">Si no tiene una cuenta de Office 365, puede [registrarse para el programa de desarrolladores de office 365](https://developer.microsoft.com/office/dev-program) para obtener una suscripción gratuita a Office 365.</span><span class="sxs-lookup"><span data-stu-id="60ce7-114">If you do not have an Office 365 account, you can [sign up for the Office 365 Developer Program](https://developer.microsoft.com/office/dev-program) to get a free Office 365 subscription.</span></span>

- <span data-ttu-id="60ce7-115">La [biblioteca de autenticación de Microsoft para .net](/dotnet/api/microsoft.identity.client?view=azure-dotnet).</span><span class="sxs-lookup"><span data-stu-id="60ce7-115">The [Microsoft Authentication Library for .NET](/dotnet/api/microsoft.identity.client?view=azure-dotnet).</span></span>

- <span data-ttu-id="60ce7-116">La [API administrada EWS](https://github.com/officedev/ews-managed-api).</span><span class="sxs-lookup"><span data-stu-id="60ce7-116">The [EWS Managed API](https://github.com/officedev/ews-managed-api).</span></span>


<span data-ttu-id="60ce7-117">Hay dos tipos de permisos de OAuth que se pueden usar para acceder a las API de EWS en Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="60ce7-117">There are two types of OAuth permissions that can be used to access EWS APIs in Exchange Online.</span></span> <span data-ttu-id="60ce7-118">Antes de continuar con el tutorial, deberá elegir el tipo de permiso específico que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="60ce7-118">Before you proceed with the tutorial, you will need to choose the specific permission type to use.</span></span>

* <span data-ttu-id="60ce7-119">Los **permisos delegados** los usan las aplicaciones en las que un usuario debe haber iniciado sesión.</span><span class="sxs-lookup"><span data-stu-id="60ce7-119">**Delegated permissions** are used by apps that have a signed-in user present.</span></span> <span data-ttu-id="60ce7-120">Para estas aplicaciones, el usuario o un administrador confirman los permisos que la aplicación solicita y la aplicación puede actuar como el usuario que ha iniciado sesión al realizar llamadas a la API.</span><span class="sxs-lookup"><span data-stu-id="60ce7-120">For these apps, either the user or an administrator consents to the permissions that the app requests and the app can act as the signed-in user when making API calls.</span></span> 
* <span data-ttu-id="60ce7-121">**Los permisos de aplicación** se usan en aplicaciones que se ejecutan sin la presencia de un usuario que ha iniciado sesión; por ejemplo, aplicaciones que se ejecutan como daemons o servicios en segundo plano y que pueden tener acceso a varios buzones.</span><span class="sxs-lookup"><span data-stu-id="60ce7-121">**Application permissions** are used by apps that run without a signed-in user present; for example, apps that run as background services or daemons and can access multiple mailboxes.</span></span>

## <a name="register-your-application"></a><span data-ttu-id="60ce7-122">Registrar la aplicación</span><span class="sxs-lookup"><span data-stu-id="60ce7-122">Register your application</span></span>

<span data-ttu-id="60ce7-123">Para usar OAuth, una aplicación debe tener un identificador de aplicación emitido por Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="60ce7-123">To use OAuth, an application must have an application ID issued by Azure Active Directory.</span></span> <span data-ttu-id="60ce7-124">En este tutorial, se da por supuesto que la aplicación es una aplicación de consola, por lo que debe registrar la aplicación como cliente público con Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="60ce7-124">In this tutorial, it is assumed that the application is a console application, so you need to register your application as a public client with Azure Active Directory.</span></span>

1. <span data-ttu-id="60ce7-125">Abra un explorador y vaya al [centro de administración de Azure Active Directory](https://aad.portal.azure.com) e inicie sesión con una **cuenta personal** (también conocida como: cuenta Microsoft) o una **cuenta profesional o educativa**.</span><span class="sxs-lookup"><span data-stu-id="60ce7-125">Open a browser and navigate to the [Azure Active Directory admin center](https://aad.portal.azure.com) and login using a **personal account** (aka: Microsoft Account) or **Work or School Account**.</span></span>

1. <span data-ttu-id="60ce7-126">Seleccione **Azure Active Directory** en el panel de navegación de la izquierda y, después, seleccione **registros de aplicaciones** en **administrar**.</span><span class="sxs-lookup"><span data-stu-id="60ce7-126">Select **Azure Active Directory** in the left-hand navigation, then select **App registrations** under **Manage**.</span></span>

1. <span data-ttu-id="60ce7-127">Seleccione **Nuevo registro**.</span><span class="sxs-lookup"><span data-stu-id="60ce7-127">Select **New registration**.</span></span> <span data-ttu-id="60ce7-128">En la página **Registrar una aplicación**, establezca los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="60ce7-128">On the **Register an application** page, set the values as follows.</span></span>

    - <span data-ttu-id="60ce7-129">Establezca **Name** en un nombre descriptivo para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="60ce7-129">Set **Name** to a friendly name for your app.</span></span>
    - <span data-ttu-id="60ce7-130">Establezca los **tipos de cuenta admitidos** en la opción adecuada para su escenario.</span><span class="sxs-lookup"><span data-stu-id="60ce7-130">Set **Supported account types** to the choice that makes sense for your scenario.</span></span>
    - <span data-ttu-id="60ce7-131">Para el **URI de redireccionamiento**, cambie la lista desplegable a **cliente público (móvil & escritorio)** y establezca el valor en `urn:ietf:wg:oauth:2.0:oob` .</span><span class="sxs-lookup"><span data-stu-id="60ce7-131">For **Redirect URI**, change the dropdown to **Public client (mobile & desktop)** and set the value to `urn:ietf:wg:oauth:2.0:oob`.</span></span>

1. <span data-ttu-id="60ce7-132">Elija **Registrar**.</span><span class="sxs-lookup"><span data-stu-id="60ce7-132">Choose **Register**.</span></span> <span data-ttu-id="60ce7-133">En la página siguiente, copie el valor del identificador de la **aplicación (cliente)** y guárdelo, lo necesitará más adelante.</span><span class="sxs-lookup"><span data-stu-id="60ce7-133">On the next page, copy the value of the **Application (client) ID** and save it, you will need it later.</span></span>

1. <span data-ttu-id="60ce7-134">Seleccione **permisos de API** en el panel de navegación izquierdo en **administrar**.</span><span class="sxs-lookup"><span data-stu-id="60ce7-134">Select **API permissions** in the left-hand navigation under **Manage**.</span></span> 

1. <span data-ttu-id="60ce7-135">Seleccione **Agregar un permiso**.</span><span class="sxs-lookup"><span data-stu-id="60ce7-135">Select **Add a permission**.</span></span> <span data-ttu-id="60ce7-136">En la página **solicitar permisos de API** , seleccione **Exchange** en **API heredadas admitidas**.</span><span class="sxs-lookup"><span data-stu-id="60ce7-136">On the **Request API permissions** page, select **Exchange** under **Supported legacy APIs**.</span></span> 

1. <span data-ttu-id="60ce7-137">Para usar permisos delegados, seleccione **permisos delegados** y, después, seleccione **EWS. AccessAsUser. All** en **EWS**.</span><span class="sxs-lookup"><span data-stu-id="60ce7-137">To use Delegated permissions, select **Delegated permissions** and then select **EWS.AccessAsUser.All** under **EWS**.</span></span> <span data-ttu-id="60ce7-138">Haga clic en **Agregar permisos**.</span><span class="sxs-lookup"><span data-stu-id="60ce7-138">Click on **Add permissions**.</span></span> 

<span data-ttu-id="60ce7-139">Para usar los permisos de la aplicación, siga estos pasos adicionales.</span><span class="sxs-lookup"><span data-stu-id="60ce7-139">To use Application permissions, follow these additional steps.</span></span>

1. <span data-ttu-id="60ce7-140">Seleccione **permisos** de la aplicación y, a continuación, seleccione **full_access_as_app**.</span><span class="sxs-lookup"><span data-stu-id="60ce7-140">Select **Application permissions** and then select **full_access_as_app**.</span></span> <span data-ttu-id="60ce7-141">Haga clic en **Agregar permisos**.</span><span class="sxs-lookup"><span data-stu-id="60ce7-141">Click on **Add permissions**.</span></span>

1. <span data-ttu-id="60ce7-142">Seleccione **conceder consentimiento de administrador para org** y acepte el cuadro de diálogo de consentimiento.</span><span class="sxs-lookup"><span data-stu-id="60ce7-142">Select **Grant admin consent for org** and accept the consent dialog.</span></span> 

1. <span data-ttu-id="60ce7-143">Seleccione **certificados & secretos** en el panel de navegación izquierdo en **administrar**.</span><span class="sxs-lookup"><span data-stu-id="60ce7-143">Select **Certificates & Secrets** in the left-hand navigation under **Manage**.</span></span> 

1. <span data-ttu-id="60ce7-144">Seleccione **nuevo secreto de cliente**, escriba una descripción breve y seleccione **Agregar**.</span><span class="sxs-lookup"><span data-stu-id="60ce7-144">Select **New client secret**, enter a short description and select **Add**.</span></span>

1. <span data-ttu-id="60ce7-145">Copie el **valor** del secreto de cliente recién agregado y guárdelo, lo necesitará más adelante.</span><span class="sxs-lookup"><span data-stu-id="60ce7-145">Copy the **Value** of the newly added client secret and save it, you will need it later.</span></span> 

## <a name="add-code-to-get-an-authentication-token"></a><span data-ttu-id="60ce7-146">Agregar código para obtener un token de autenticación</span><span class="sxs-lookup"><span data-stu-id="60ce7-146">Add code to get an authentication token</span></span>

<span data-ttu-id="60ce7-147">Los fragmentos de código siguientes muestran cómo usar la biblioteca de autenticación de Microsoft para obtener tokens de autenticación para permisos delegados y permisos de aplicación.</span><span class="sxs-lookup"><span data-stu-id="60ce7-147">The following code snippets show how to use the Microsoft Authentication Library to get authentication tokens for delegated permissions and application permissions.</span></span> <span data-ttu-id="60ce7-148">En estos fragmentos de código se presupone que la información necesaria para realizar la solicitud de autenticación se almacena en el archivo **app. config** de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="60ce7-148">These snippets assume that the information required to make the authentication request is stored in the application's **App.config** file.</span></span> <span data-ttu-id="60ce7-149">Estos ejemplos no incluyen la comprobación de errores, vea los [ejemplos de código](#code-samples) para obtener el código completo.</span><span class="sxs-lookup"><span data-stu-id="60ce7-149">These examples do not include error checking, see the [Code samples](#code-samples) for the complete code.</span></span>

### <a name="delegated-permissions"></a><span data-ttu-id="60ce7-150">Permisos delegados</span><span class="sxs-lookup"><span data-stu-id="60ce7-150">Delegated permissions</span></span>

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

### <a name="application-permissions"></a><span data-ttu-id="60ce7-151">Permisos de la aplicación</span><span class="sxs-lookup"><span data-stu-id="60ce7-151">Application permissions</span></span>

```cs
// Configure the MSAL client to get tokens
var app = ConfidentialClientApplicationBuilder
    .Create(ConfigurationManager.AppSettings["appId"])
    .WithAuthority(AzureCloudInstance.AzurePublic, ConfigurationManager.AppSettings["tenantId"])
    .WithClientSecret(ConfigurationManager.AppSettings["clientSecret"]).Build();

// The permission scope required for EWS access
var ewsScopes = new string[] { "https://outlook.office.com/.default" };

//Make the toekn request
AuthenticationResult authResult = await app.AcquireTokenForClient(ewsScopes).ExecuteAsync();

```

## <a name="add-an-authentication-token-to-ews-requests"></a><span data-ttu-id="60ce7-152">Adición de un token de autenticación a las solicitudes de EWS</span><span class="sxs-lookup"><span data-stu-id="60ce7-152">Add an authentication token to EWS requests</span></span>

<span data-ttu-id="60ce7-153">Una vez que haya recibido el objeto **AuthenticationResult** , puede usar la propiedad **AccessToken** para obtener el token emitido por el servicio de token.</span><span class="sxs-lookup"><span data-stu-id="60ce7-153">After you've received the **AuthenticationResult** object you can use the **AccessToken** property to get the token issued by the token service.</span></span>

```cs
// Configure the ExchangeService with the access token
var ewsClient = new ExchangeService();
ewsClient.Url = new Uri("https://outlook.office365.com/EWS/Exchange.asmx");
ewsClient.Credentials = new OAuthCredentials(authResult.AccessToken);
```

<span data-ttu-id="60ce7-154">Para usar los permisos de la aplicación, también tendrá que suplantar explícitamente un buzón al que desee tener acceso.</span><span class="sxs-lookup"><span data-stu-id="60ce7-154">To use Application permissions, you will also need to explictly impersonate a mailbox that you would like to access.</span></span> 

```cs
//Impersonate the mailbox you'd like to access.
ewsClient.ImpersonatedUserId = new ImpersonatedUserId(ConnectingIdType.SmtpAddress, "test@demotenant.onmicrosoft.com");
```

## <a name="code-samples"></a><span data-ttu-id="60ce7-155">Ejemplos de código</span><span class="sxs-lookup"><span data-stu-id="60ce7-155">Code samples</span></span>

### <a name="delegated-permissions"></a><span data-ttu-id="60ce7-156">Permisos delegados</span><span class="sxs-lookup"><span data-stu-id="60ce7-156">Delegated permissions</span></span>

<span data-ttu-id="60ce7-157">El siguiente es el ejemplo de código completo que muestra cómo realizar una solicitud EWS autenticada con OAuth mediante permisos delegados.</span><span class="sxs-lookup"><span data-stu-id="60ce7-157">The following is the complete code sample that demonstrates making an OAuth-authenticated EWS request using Delegated permissions.</span></span>

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

### <a name="application-permissions"></a><span data-ttu-id="60ce7-158">Permisos de la aplicación</span><span class="sxs-lookup"><span data-stu-id="60ce7-158">Application permissions</span></span>

<span data-ttu-id="60ce7-159">El siguiente es el ejemplo de código completo que muestra cómo realizar una solicitud EWS autenticada con OAuth mediante permisos de aplicación.</span><span class="sxs-lookup"><span data-stu-id="60ce7-159">The following is the complete code sample that demonstrates making an OAuth-authenticated EWS request using Application permissions.</span></span>

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

<span data-ttu-id="60ce7-160">En ambos casos, el código de ejemplo requiere un archivo **app. config** con las siguientes entradas:</span><span class="sxs-lookup"><span data-stu-id="60ce7-160">The sample code in both cases requires an **App.config** file with the following entries:</span></span>

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

## <a name="see-also"></a><span data-ttu-id="60ce7-161">Vea también</span><span class="sxs-lookup"><span data-stu-id="60ce7-161">See also</span></span>

- [<span data-ttu-id="60ce7-162">Autenticación y EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="60ce7-162">Authentication and EWS in Exchange</span></span>](authentication-and-ews-in-exchange.md)
