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
# <a name="authenticate-an-ews-application-by-using-oauth"></a><span data-ttu-id="2aa83-103">Autenticar una aplicación EWS mediante OAuth</span><span class="sxs-lookup"><span data-stu-id="2aa83-103">Authenticate an EWS application by using OAuth</span></span>
<!-- markdownlint-enable MD025 -->

<span data-ttu-id="2aa83-104">Obtenga información sobre cómo usar la autenticación OAuth con las aplicaciones de la API administrada de EWS.</span><span class="sxs-lookup"><span data-stu-id="2aa83-104">Learn how to use OAuth authentication with your EWS Managed API applications.</span></span>

<span data-ttu-id="2aa83-105">Puede usar el servicio de autenticación OAuth proporcionado por Azure Active Directory para permitir que las aplicaciones de la API administrada de EWS obtengan acceso a Exchange Online en Office 365.</span><span class="sxs-lookup"><span data-stu-id="2aa83-105">You can use the OAuth authentication service provided by Azure Active Directory to enable your EWS Managed API applications to access Exchange Online in Office 365.</span></span> <span data-ttu-id="2aa83-106">Para usar OAuth con la aplicación tendrá que:</span><span class="sxs-lookup"><span data-stu-id="2aa83-106">To use OAuth with your application you will need to:</span></span>

1. <span data-ttu-id="2aa83-107">[Registrar la aplicación](#register-your-application) con Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="2aa83-107">[Register your application](#register-your-application) with Azure Active Directory.</span></span>
1. <span data-ttu-id="2aa83-108">[Agregar código para obtener un token de autenticación](#add-code-to-get-an-authentication-token) para obtener un token de autenticación de un servidor de tokens.</span><span class="sxs-lookup"><span data-stu-id="2aa83-108">[Add code to get an authentication token](#add-code-to-get-an-authentication-token) to get an authentication token from a token server.</span></span>
1. <span data-ttu-id="2aa83-109">[Agregar un token de autenticación a las solicitudes de EWS](#add-an-authentication-token-to-ews-requests) que envíe.</span><span class="sxs-lookup"><span data-stu-id="2aa83-109">[Add an authentication token to EWS requests](#add-an-authentication-token-to-ews-requests) that you send.</span></span>

> [!NOTE]
> <span data-ttu-id="2aa83-110">La autenticación OAuth para EWS solo está disponible en Exchange como parte de Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="2aa83-110">OAuth authentication for EWS is only available in Exchange Online as part of Microsoft 365.</span></span> <span data-ttu-id="2aa83-111">Las aplicaciones de EWS que usan OAuth deben registrarse con Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="2aa83-111">EWS applications that use OAuth must be registered with Azure Active Directory.</span></span>

<span data-ttu-id="2aa83-112">Para usar el código de este artículo, tendrá que tener acceso a lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="2aa83-112">To use the code in this article, you will need to have access to the following:</span></span>

- <span data-ttu-id="2aa83-113">Una cuenta de Microsoft 365 con un buzón de Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="2aa83-113">A Microsoft 365 account with an Exchange Online mailbox.</span></span> <span data-ttu-id="2aa83-114">Si no tiene una cuenta de Microsoft 365, puede [registrarse en el Programa de desarrolladores de Microsoft 365](https://developer.microsoft.com/microsoft-365/dev-program) para obtener una suscripción gratuita.</span><span class="sxs-lookup"><span data-stu-id="2aa83-114">If you do not have a Microsoft 365 account, you can [sign up for the Microsoft 365 Developer Program](https://developer.microsoft.com/microsoft-365/dev-program) to get a free Microsoft 365 subscription.</span></span>
- <span data-ttu-id="2aa83-115">La [Biblioteca de autenticación de Microsoft para .NET](/dotnet/api/microsoft.identity.client).</span><span class="sxs-lookup"><span data-stu-id="2aa83-115">The [Microsoft Authentication Library for .NET](/dotnet/api/microsoft.identity.client).</span></span>
- <span data-ttu-id="2aa83-116">La [API administrada de EWS](https://github.com/officedev/ews-managed-api).</span><span class="sxs-lookup"><span data-stu-id="2aa83-116">The [EWS Managed API](https://github.com/officedev/ews-managed-api).</span></span>

<span data-ttu-id="2aa83-117">Hay dos tipos de permisos OAuth que se pueden usar para obtener acceso a las API de EWS en Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="2aa83-117">There are two types of OAuth permissions that can be used to access EWS APIs in Exchange Online.</span></span> <span data-ttu-id="2aa83-118">Antes de continuar con el tutorial, tendrá que seleccionar el tipo de permiso específico que desea usar.</span><span class="sxs-lookup"><span data-stu-id="2aa83-118">Before you proceed with the tutorial, you will need to choose the specific permission type to use.</span></span>

- <span data-ttu-id="2aa83-119">Los **permisos delegados** los usan las aplicaciones en las que un usuario debe haber iniciado sesión.</span><span class="sxs-lookup"><span data-stu-id="2aa83-119">**Delegated permissions** are used by apps that have a signed-in user present.</span></span> <span data-ttu-id="2aa83-120">En estas aplicaciones, el usuario o un administrador dan su consentimiento a los permisos que solicita la aplicación, y la aplicación puede actuar como un usuario que ha iniciado sesión cuando se hacen llamadas de API.</span><span class="sxs-lookup"><span data-stu-id="2aa83-120">For these apps, either the user or an administrator consents to the permissions that the app requests and the app can act as the signed-in user when making API calls.</span></span>
- <span data-ttu-id="2aa83-121">Los **permisos de aplicación** son los que usan las aplicaciones que se ejecutan sin que un usuario haya iniciado sesión, como las aplicaciones que se ejecutan como servicios en segundo plano o demonios y que pueden acceder a varios buzones.</span><span class="sxs-lookup"><span data-stu-id="2aa83-121">**Application permissions** are used by apps that run without a signed-in user present; for example, apps that run as background services or daemons and can access multiple mailboxes.</span></span>

## <a name="register-your-application"></a><span data-ttu-id="2aa83-122">Registrar su aplicación</span><span class="sxs-lookup"><span data-stu-id="2aa83-122">Register your application</span></span>

<span data-ttu-id="2aa83-123">Para usar OAuth, una aplicación debe tener un Id. de aplicación emitido por Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="2aa83-123">To use OAuth, an application must have an application ID issued by Azure Active Directory.</span></span> <span data-ttu-id="2aa83-124">En este tutorial, se presupone que la aplicación es una aplicación de consola, por lo que necesita registrar la aplicación como cliente público con Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="2aa83-124">In this tutorial, it is assumed that the application is a console application, so you need to register your application as a public client with Azure Active Directory.</span></span> <span data-ttu-id="2aa83-125">Puede registrar una aplicación en el Centro de administración de Azure Active Directory o a través de Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="2aa83-125">You can register an application in the Azure Active Directory admin center or by using Microsoft Graph.</span></span>

1. <span data-ttu-id="2aa83-126">Abra un explorador y vaya al [centro de administración de Azure Active Directory](https://aad.portal.azure.com) e inicie sesión con una **cuenta personal** (también conocida como: cuenta Microsoft) o una **cuenta profesional o educativa**.</span><span class="sxs-lookup"><span data-stu-id="2aa83-126">Open a browser and navigate to the [Azure Active Directory admin center](https://aad.portal.azure.com) and login using a **personal account** (aka: Microsoft Account) or **Work or School Account**.</span></span>

1. <span data-ttu-id="2aa83-127">Seleccione **Azure Active Directory** en el panel de navegación izquierdo y, a continuación, seleccione **Registros de aplicaciones** en **Administrar**.</span><span class="sxs-lookup"><span data-stu-id="2aa83-127">Select **Azure Active Directory** in the left-hand navigation, then select **App registrations** under **Manage**.</span></span>

1. <span data-ttu-id="2aa83-128">Seleccione **Nuevo registro**.</span><span class="sxs-lookup"><span data-stu-id="2aa83-128">Select **New registration**.</span></span> <span data-ttu-id="2aa83-129">En la página **Registrar una aplicación**, establezca los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="2aa83-129">On the **Register an application** page, set the values as follows.</span></span>

    - <span data-ttu-id="2aa83-130">Establezca **Nombre** como un nombre descriptivo para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2aa83-130">Set **Name** to a friendly name for your app.</span></span>
    - <span data-ttu-id="2aa83-131">Configure **Tipos de cuenta compatibles** de manera adecuada para su escenario.</span><span class="sxs-lookup"><span data-stu-id="2aa83-131">Set **Supported account types** to the choice that makes sense for your scenario.</span></span>
    - <span data-ttu-id="2aa83-132">Para **URI de redirección**, cambie la lista desplegable a **Cliente público (dispositivo móvil y escritorio)** y establezca el valor en `urn:ietf:wg:oauth:2.0:oob`.</span><span class="sxs-lookup"><span data-stu-id="2aa83-132">For **Redirect URI**, change the dropdown to **Public client (mobile & desktop)** and set the value to `urn:ietf:wg:oauth:2.0:oob`.</span></span>

1. <span data-ttu-id="2aa83-133">Elija **Registrar**.</span><span class="sxs-lookup"><span data-stu-id="2aa83-133">Choose **Register**.</span></span> <span data-ttu-id="2aa83-134">En la página siguiente, copie los valores del **Id. de la aplicación (cliente)** y del **Id. del directorio (cuenta empresarial)** y guárdelos; los necesitará más adelante.</span><span class="sxs-lookup"><span data-stu-id="2aa83-134">On the next page, copy the values of the **Application (client) ID** and **Directory (tenant) ID** and save them, you will need them later.</span></span>

### <a name="configure-for-delegated-authentication"></a><span data-ttu-id="2aa83-135">Configurar para la autenticación delegada</span><span class="sxs-lookup"><span data-stu-id="2aa83-135">Configure for delegated authentication</span></span>

<span data-ttu-id="2aa83-136">Si la aplicación usa una autenticación delegada, no es necesario realizar ninguna configuración adicional.</span><span class="sxs-lookup"><span data-stu-id="2aa83-136">If your application uses delegated authentication, no further configuration is required.</span></span> <span data-ttu-id="2aa83-137">La [Plataforma de identidad de Microsoft](/azure/active-directory/develop/v2-overview) permite que las aplicaciones soliciten permisos de forma dinámica, por lo que no es necesario que configure previamente los permisos en el registro de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2aa83-137">The [Microsoft identity platform](/azure/active-directory/develop/v2-overview) allows apps to request permissions dynamically, so you do not have to pre-configure permissions on the app registration.</span></span> <span data-ttu-id="2aa83-138">Sin embargo, en algunos casos (como en el del [flujo con derechos delegados](/azure/active-directory/develop/v2-oauth2-on-behalf-of-flow)) se necesitan permisos para la configuración previa.</span><span class="sxs-lookup"><span data-stu-id="2aa83-138">However, in some scenarios (like the [on-behalf-of flow](/azure/active-directory/develop/v2-oauth2-on-behalf-of-flow)) pre-configuring permissions is required.</span></span> <span data-ttu-id="2aa83-139">Siga los siguientes pasos para configurar previamente los permisos de EWS.</span><span class="sxs-lookup"><span data-stu-id="2aa83-139">Use the following steps to pre-configure EWS permissions.</span></span>

1. <span data-ttu-id="2aa83-140">Seleccione **Manifiesto** en el panel de navegación izquierdo, debajo de **Administrar**.</span><span class="sxs-lookup"><span data-stu-id="2aa83-140">Select **Manifest** in the left-hand navigation under **Manage**.</span></span>

1. <span data-ttu-id="2aa83-141">Localice la propiedad `requiredResourceAccess` en el manifiesto y agregue lo siguiente dentro de los corchetes (`[]`):</span><span class="sxs-lookup"><span data-stu-id="2aa83-141">Locate the `requiredResourceAccess` property in the manifest, and add the following inside the square brackets (`[]`):</span></span>

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

1. <span data-ttu-id="2aa83-142">Seleccione **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="2aa83-142">Select **Save**.</span></span>

1. <span data-ttu-id="2aa83-143">Seleccione **Permisos de las API** en **Administrar**.</span><span class="sxs-lookup"><span data-stu-id="2aa83-143">Select **API permissions** under **Manage**.</span></span> <span data-ttu-id="2aa83-144">Confirme que el permiso **EWS.AccessAsUser.All** aparezca en la lista.</span><span class="sxs-lookup"><span data-stu-id="2aa83-144">Confirm that the **EWS.AccessAsUser.All** permission is listed.</span></span>

### <a name="configure-for-app-only-authentication"></a><span data-ttu-id="2aa83-145">Configurar la autenticación solo para la aplicación</span><span class="sxs-lookup"><span data-stu-id="2aa83-145">Configure for app-only authentication</span></span>

<span data-ttu-id="2aa83-146">Para usar los permisos de la aplicación, siga estos pasos adicionales.</span><span class="sxs-lookup"><span data-stu-id="2aa83-146">To use application permissions, follow these additional steps.</span></span>

1. <span data-ttu-id="2aa83-147">Seleccione **Manifiesto** en el panel de navegación izquierdo, debajo de **Administrar**.</span><span class="sxs-lookup"><span data-stu-id="2aa83-147">Select **Manifest** in the left-hand navigation under **Manage**.</span></span>

1. <span data-ttu-id="2aa83-148">Localice la propiedad `requiredResourceAccess` en el manifiesto y agregue lo siguiente dentro de los corchetes (`[]`):</span><span class="sxs-lookup"><span data-stu-id="2aa83-148">Locate the `requiredResourceAccess` property in the manifest, and add the following inside the square brackets (`[]`):</span></span>

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

1. <span data-ttu-id="2aa83-149">Seleccione **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="2aa83-149">Select **Save**.</span></span>

1. <span data-ttu-id="2aa83-150">Seleccione **Permisos de las API** en **Administrar**.</span><span class="sxs-lookup"><span data-stu-id="2aa83-150">Select **API permissions** under **Manage**.</span></span> <span data-ttu-id="2aa83-151">Confirme que aparezca el permiso **full_access_as_app**.</span><span class="sxs-lookup"><span data-stu-id="2aa83-151">Confirm that the **full_access_as_app** permission is listed.</span></span>

1. <span data-ttu-id="2aa83-152">Seleccione **Conceder consentimiento de administrador para organización** y acepte el cuadro de diálogo de consentimiento.</span><span class="sxs-lookup"><span data-stu-id="2aa83-152">Select **Grant admin consent for org** and accept the consent dialog.</span></span>

1. <span data-ttu-id="2aa83-153">Seleccione **Certificados y secretos** en el panel de navegación de la parte izquierda, en **Administrar**.</span><span class="sxs-lookup"><span data-stu-id="2aa83-153">Select **Certificates & Secrets** in the left-hand navigation under **Manage**.</span></span>

1. <span data-ttu-id="2aa83-154">Seleccione **Nuevo secreto de cliente**, escriba una descripción breve y seleccione **Agregar**.</span><span class="sxs-lookup"><span data-stu-id="2aa83-154">Select **New client secret**, enter a short description and select **Add**.</span></span>

1. <span data-ttu-id="2aa83-155">Copie el **Valor** del secreto de cliente recién agregado y guárdelo, ya que lo necesitará más adelante.</span><span class="sxs-lookup"><span data-stu-id="2aa83-155">Copy the **Value** of the newly added client secret and save it, you will need it later.</span></span>

## <a name="add-code-to-get-an-authentication-token"></a><span data-ttu-id="2aa83-156">Agregar código para obtener un token de autenticación</span><span class="sxs-lookup"><span data-stu-id="2aa83-156">Add code to get an authentication token</span></span>

<span data-ttu-id="2aa83-157">Los siguientes fragmentos de código muestran cómo usar la Biblioteca de autenticación de Microsoft para obtener los tokens de autenticación de los permisos delegados y los permisos de aplicación.</span><span class="sxs-lookup"><span data-stu-id="2aa83-157">The following code snippets show how to use the Microsoft Authentication Library to get authentication tokens for delegated permissions and application permissions.</span></span> <span data-ttu-id="2aa83-158">En estos fragmentos se presupone que la información necesaria para realizar la solicitud de autenticación está almacenada en el archivo **App.config** de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2aa83-158">These snippets assume that the information required to make the authentication request is stored in the application's **App.config** file.</span></span> <span data-ttu-id="2aa83-159">Entre estos ejemplos no se incluyen la comprobación de errores. Consulte los [Ejemplos de código](#code-samples) para el código completo.</span><span class="sxs-lookup"><span data-stu-id="2aa83-159">These examples do not include error checking, see the [Code samples](#code-samples) for the complete code.</span></span>

### <a name="get-a-token-with-delegated-auth"></a><span data-ttu-id="2aa83-160">Obtener un token con la autenticación delegada</span><span class="sxs-lookup"><span data-stu-id="2aa83-160">Get a token with delegated auth</span></span>

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

### <a name="get-a-token-with-app-only-auth"></a><span data-ttu-id="2aa83-161">Obtener un token con autenticación solo para la aplicación</span><span class="sxs-lookup"><span data-stu-id="2aa83-161">Get a token with app-only auth</span></span>

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

## <a name="add-an-authentication-token-to-ews-requests"></a><span data-ttu-id="2aa83-162">Agregar un token de autenticación a las solicitudes de EWS</span><span class="sxs-lookup"><span data-stu-id="2aa83-162">Add an authentication token to EWS requests</span></span>

<span data-ttu-id="2aa83-163">Tras recibir el objeto **AuthenticationResult**, puede usar la propiedad **AccessToken** para obtener el token emitido por el servicio de token.</span><span class="sxs-lookup"><span data-stu-id="2aa83-163">After you've received the **AuthenticationResult** object you can use the **AccessToken** property to get the token issued by the token service.</span></span>

```cs
// Configure the ExchangeService with the access token
var ewsClient = new ExchangeService();
ewsClient.Url = new Uri("https://outlook.office365.com/EWS/Exchange.asmx");
ewsClient.Credentials = new OAuthCredentials(authResult.AccessToken);
```

<span data-ttu-id="2aa83-164">Para usar los permisos de la aplicación, también tendrá que suplantar de manera explícita al buzón al que le gustaría acceder.</span><span class="sxs-lookup"><span data-stu-id="2aa83-164">To use application permissions, you will also need to explicitly impersonate a mailbox that you would like to access.</span></span>

```cs
//Impersonate the mailbox you'd like to access.
ewsClient.ImpersonatedUserId = new ImpersonatedUserId(ConnectingIdType.SmtpAddress, "test@demotenant.onmicrosoft.com");
```

## <a name="code-samples"></a><span data-ttu-id="2aa83-165">Ejemplos de código</span><span class="sxs-lookup"><span data-stu-id="2aa83-165">Code samples</span></span>

### <a name="delegated-authentication"></a><span data-ttu-id="2aa83-166">Autenticación delegada</span><span class="sxs-lookup"><span data-stu-id="2aa83-166">Delegated authentication</span></span>

<span data-ttu-id="2aa83-167">El siguiente es un código de muestra completo que ejemplifica cómo realizar una solicitud EWS autenticada por OAuth usando los permisos delegados de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2aa83-167">The following is the complete code sample that demonstrates making an OAuth-authenticated EWS request using delegated authentication.</span></span>

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

### <a name="app-only-authentication"></a><span data-ttu-id="2aa83-168">Autenticación solo para la aplicación</span><span class="sxs-lookup"><span data-stu-id="2aa83-168">App-only authentication</span></span>

<span data-ttu-id="2aa83-169">El siguiente es un código de muestra completo que ejemplifica cómo realizar una solicitud EWS autenticada por OAuth usando la autenticación solo para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2aa83-169">The following is the complete code sample that demonstrates making an OAuth-authenticated EWS request using app-only authentication.</span></span>

> [!NOTE]
> <span data-ttu-id="2aa83-170">Cuando se usa la suplantación, debe usar siempre el encabezado de la solicitud X-AnchorMailbox, el cual debería estar establecido para la dirección SMTP del buzón suplantado.</span><span class="sxs-lookup"><span data-stu-id="2aa83-170">When using impersonation you must always use the X-AnchorMailbox request header, which should be set to the SMTP address of the impersonated mailbox.</span></span>

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

<span data-ttu-id="2aa83-171">En ambos casos, el ejemplo de código requiere un archivo **App.config** con las entradas siguientes:</span><span class="sxs-lookup"><span data-stu-id="2aa83-171">The sample code in both cases requires an **App.config** file with the following entries:</span></span>

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

## <a name="see-also"></a><span data-ttu-id="2aa83-172">Vea también</span><span class="sxs-lookup"><span data-stu-id="2aa83-172">See also</span></span>

- [<span data-ttu-id="2aa83-173">Autenticación y EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="2aa83-173">Authentication and EWS in Exchange</span></span>](authentication-and-ews-in-exchange.md)
