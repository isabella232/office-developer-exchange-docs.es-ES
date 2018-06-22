---
title: Autenticar una aplicación EWS mediante OAuth
manager: sethgros
ms.date: 1/15/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 1d8d57f9-4df5-4f21-9bbb-a89e0e259052
description: Obtenga información sobre cómo usar la autenticación de OAuth con las aplicaciones de la API administrada de EWS.
ms.openlocfilehash: 66bbc0525ecf78407e853da0c8dcdec92791ca56
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763035"
---
# <a name="authenticate-an-ews-application-by-using-oauth"></a><span data-ttu-id="a6dcc-103">Autenticar una aplicación EWS mediante OAuth</span><span class="sxs-lookup"><span data-stu-id="a6dcc-103">Authenticate an EWS application by using OAuth</span></span>

<span data-ttu-id="a6dcc-104">Obtenga información sobre cómo usar la autenticación de OAuth con las aplicaciones de la API administrada de EWS.</span><span class="sxs-lookup"><span data-stu-id="a6dcc-104">Learn how to use OAuth authentication with your EWS Managed API applications.</span></span>
  
<span data-ttu-id="a6dcc-105">Puede usar el servicio de autenticación de OAuth proporcionado por Azure Active Directory para integrar las aplicaciones de la API administrada de EWS con el mismo modelo de autenticación usado por la API de REST de Office 365.</span><span class="sxs-lookup"><span data-stu-id="a6dcc-105">You can use the OAuth authentication service provided by Azure Active Directory to integrate your EWS Managed API applications with the same authentication model used by the Office 365 REST APIs.</span></span> <span data-ttu-id="a6dcc-106">Para usar OAuth con la aplicación, necesitará:</span><span class="sxs-lookup"><span data-stu-id="a6dcc-106">To use OAuth with your application you will need to:</span></span>
  
1. <span data-ttu-id="a6dcc-107">[Registrar la aplicación](#bk_register) con Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="a6dcc-107">[Register your application](#bk_register) with Azure Active Directory.</span></span> 
    
2. <span data-ttu-id="a6dcc-108">[Agregar código para obtener un token de autenticación](#bk_getToken) para obtener una autenticación símbolo (token) de un servidor de token.</span><span class="sxs-lookup"><span data-stu-id="a6dcc-108">[Add code to get an authentication token](#bk_getToken) to get an authentication token from a token server.</span></span> 
    
3. <span data-ttu-id="a6dcc-109">[Agregar un token de autenticación para las solicitudes EWS](#bk_useToken) que envíe.</span><span class="sxs-lookup"><span data-stu-id="a6dcc-109">[Add an authentication token to EWS requests](#bk_useToken) that you send.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="a6dcc-110">Autenticación de OAuth para EWS sólo está disponible en Exchange como parte de Office 365.</span><span class="sxs-lookup"><span data-stu-id="a6dcc-110">OAuth authentication for EWS is only available in Exchange as part of Office 365.</span></span> <span data-ttu-id="a6dcc-111">Las aplicaciones de EWS requieren el permiso "Acceso total al buzón del usuario".</span><span class="sxs-lookup"><span data-stu-id="a6dcc-111">EWS applications require the "Full access to user's mailbox" permission.</span></span> 
  
<span data-ttu-id="a6dcc-112">Para usar el código de este artículo, necesita tener acceso a la siguiente:</span><span class="sxs-lookup"><span data-stu-id="a6dcc-112">To use the code in this article, you will need to have access to the following:</span></span>
  
- <span data-ttu-id="a6dcc-113">Una [cuenta de desarrollador de Office 365](http://office.microsoft.com/compare-office-365-for-business-plans-FX102918419.aspx.aspx).</span><span class="sxs-lookup"><span data-stu-id="a6dcc-113">An [Office 365 developer account](http://office.microsoft.com/compare-office-365-for-business-plans-FX102918419.aspx.aspx).</span></span> <span data-ttu-id="a6dcc-114">Puede usar una cuenta de prueba para probar la aplicación</span><span class="sxs-lookup"><span data-stu-id="a6dcc-114">You can use a trial account to test your application</span></span>
    
- <span data-ttu-id="a6dcc-115">La [biblioteca de autenticación de Azure AD para. NET](http://msdn.microsoft.com/en-us/library/office/jj573266.aspx.aspx).</span><span class="sxs-lookup"><span data-stu-id="a6dcc-115">The [Azure AD Authentication Library for .NET](http://msdn.microsoft.com/en-us/library/office/jj573266.aspx.aspx).</span></span>
    
- <span data-ttu-id="a6dcc-116">[API administrada de EWS](https://github.com/officedev/ews-managed-api.aspx).</span><span class="sxs-lookup"><span data-stu-id="a6dcc-116">[The EWS Managed API](https://github.com/officedev/ews-managed-api.aspx).</span></span>

<span data-ttu-id="a6dcc-117"><a name="bk_register"> </a></span><span class="sxs-lookup"><span data-stu-id="a6dcc-117"></span></span>

## <a name="register-your-application"></a><span data-ttu-id="a6dcc-118">Registrar la aplicación</span><span class="sxs-lookup"><span data-stu-id="a6dcc-118">Register your application</span></span>

<span data-ttu-id="a6dcc-119">Para usar OAuth, una aplicación debe tener un identificador de cliente y un URI que identifica la aplicación de aplicación.</span><span class="sxs-lookup"><span data-stu-id="a6dcc-119">To use OAuth, an application must have a client identifier and an application URI that identifies the application.</span></span> <span data-ttu-id="a6dcc-120">Si aún no ha registrado su aplicación con servicios de Azure Active Directory, debe agregar manualmente la aplicación siguiendo los pasos en el [registro de aplicación](http://msdn.microsoft.com/en-us/office/office365/howto/test-and-deploy-apps.aspx).</span><span class="sxs-lookup"><span data-stu-id="a6dcc-120">If you have not yet registered your application with Azure Active Directory Services, you'll need to manually add your application by following the steps under [Register you app](http://msdn.microsoft.com/en-us/office/office365/howto/test-and-deploy-apps.aspx).</span></span>

<span data-ttu-id="a6dcc-121"><a name="bk_getToken"> </a></span><span class="sxs-lookup"><span data-stu-id="a6dcc-121"></span></span>

## <a name="add-code-to-get-an-authentication-token"></a><span data-ttu-id="a6dcc-122">Agregar código para obtener un token de autenticación</span><span class="sxs-lookup"><span data-stu-id="a6dcc-122">Add code to get an authentication token</span></span>

<span data-ttu-id="a6dcc-123">La biblioteca de autenticación de AD Azure para .NET simplifica la obtención de un token de autenticación de Azure Active Directory para que se puede utilizar el token en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="a6dcc-123">The Azure AD Authentication Library for .NET simplifies getting an authentication token from Azure Active Directory so that you can use the token in your application.</span></span> <span data-ttu-id="a6dcc-124">Debe proporcionar cuatro fragmentos de información para obtener el token:</span><span class="sxs-lookup"><span data-stu-id="a6dcc-124">You need to provide four pieces of information to get the token:</span></span>
  
1. <span data-ttu-id="a6dcc-125">El URI del servidor de símbolo (token).</span><span class="sxs-lookup"><span data-stu-id="a6dcc-125">The URI of the token server.</span></span> <span data-ttu-id="a6dcc-126">El servidor de token es la **entidad de certificación** que autentica al usuario y devuelve un símbolo (token) que la aplicación puede utilizar para tener acceso a EWS.</span><span class="sxs-lookup"><span data-stu-id="a6dcc-126">The token server is the **authority** that authenticates the user and returns a token that your application can use to access EWS.</span></span> 
    
2. <span data-ttu-id="a6dcc-127">El identificador de cliente de aplicación que se crea al registrar la aplicación con Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="a6dcc-127">The application client ID created when you registered your application with Azure Active Directory.</span></span>
    
3. <span data-ttu-id="a6dcc-128">El cliente de aplicación de URI que se crean al registrar la aplicación con Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="a6dcc-128">The application client URI created when you registered your application with Azure Active Directory.</span></span>
    
4. <span data-ttu-id="a6dcc-129">El URI del servidor EWS y el URI del extremo de EWS.</span><span class="sxs-lookup"><span data-stu-id="a6dcc-129">The URI of the EWS server and the URI of the EWS endpoint.</span></span> <span data-ttu-id="a6dcc-130">Para Exchange como parte de Office 365, será `https://<server name>/ews/exchange.asmx`.</span><span class="sxs-lookup"><span data-stu-id="a6dcc-130">For Exchange as part of Office 365, this will be  `https://<server name>/ews/exchange.asmx`.</span></span>
    
<span data-ttu-id="a6dcc-131">El código siguiente muestra cómo usar la biblioteca de autenticación de AD Azure para obtener un token de autenticación.</span><span class="sxs-lookup"><span data-stu-id="a6dcc-131">The following code shows how to use the Azure AD Authentication Library to get an authentication token.</span></span> <span data-ttu-id="a6dcc-132">Se supone que la información necesaria para realizar la solicitud de autenticación se almacena en el archivo de App.config de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="a6dcc-132">It assumes that the information required to make the authentication request is stored in the application's App.config file.</span></span> <span data-ttu-id="a6dcc-133">En este ejemplo no incluyen comprobación de errores, vea el [ejemplo de código](#bk_codeSample) para el código completo.</span><span class="sxs-lookup"><span data-stu-id="a6dcc-133">This example does not include error checking, see the [Code sample](#bk_codeSample) for the complete code.</span></span> 
  
```cs
string authority = ConfigurationManager.AppSettings["authority"];
string clientID = ConfigurationManager.AppSettings["clientID"];
Uri clientAppUri = new Uri(ConfigurationManager.AppSettings["clientAppUri"];
string serverName = ConfigurationManager.AppSettings["serverName"];
AuthenticationContext authenticationContext = new AuthenticationContext(authority, false);
AuthenticationResult authenticationResult = authenticationContext.AcquireToken(serverName, clientId, clientAppUri);

```

<span data-ttu-id="a6dcc-134"><a name="bk_useToken"> </a></span><span class="sxs-lookup"><span data-stu-id="a6dcc-134"></span></span>

## <a name="add-an-authentication-token-to-ews-requests"></a><span data-ttu-id="a6dcc-135">Agregar un token de autenticación para las solicitudes EWS</span><span class="sxs-lookup"><span data-stu-id="a6dcc-135">Add an authentication token to EWS requests</span></span>

<span data-ttu-id="a6dcc-136">Una vez que ha recibido el objeto **AuthenticationResult** puede usar la propiedad **AccessToken** para obtener el token emitido por el servicio de token.</span><span class="sxs-lookup"><span data-stu-id="a6dcc-136">After you've received the **AuthenticationResult** object you can use the **AccessToken** property to get the token issued by the token service.</span></span> 
  
```cs
ExchangeService exchangeService = new ExchangeService(ExchangeVersion.Exchange2013);
exchangeService.Url = new Uri(ConfigurationManager.AppSettings["serverName"]+"ews/exchange.asmx");
exchangeService.TraceEnabled = true;
exchangeService.TraceFlags = TraceFlags.All;
exchangeService.Credentials = new OAuthCredentials(authenticationResult.AccessToken));
exchangeService.FindFolders(WellKnownFolderName.Root, new Folderview(10));
```

<span data-ttu-id="a6dcc-137"><a name="bk_codeSample"> </a></span><span class="sxs-lookup"><span data-stu-id="a6dcc-137"></span></span>

## <a name="code-sample"></a><span data-ttu-id="a6dcc-138">Ejemplo de código</span><span class="sxs-lookup"><span data-stu-id="a6dcc-138">Code sample</span></span>

<span data-ttu-id="a6dcc-139">El siguiente es el ejemplo de código completo que muestra cómo realizar una solicitud de autenticación de OAuth EWS.</span><span class="sxs-lookup"><span data-stu-id="a6dcc-139">The following is the complete code sample that demonstrates making an OAuth-authenticated EWS request.</span></span>
  
```cs
using System;
using System.Collections.Generic;
using System.Configuration;
using System.Globalization;
using System.Linq;
using System.Text;
using System.Threading;
using System.Threading.Tasks;
using System.Web.Script.Serialization;
using Microsoft.Exchange.WebServices.Autodiscover;
using Microsoft.Exchange.WebServices.Data;
using Microsoft.IdentityModel.Clients.ActiveDirectory;
namespace TestV1App
{
    class Program
    {
        static void Main(string[] args)
        {
            var t = new Thread(Run);
            t.SetApartmentState(ApartmentState.STA);
            t.Start();
            t.Join();
        }
        static void Run()
        {
           string authority = ConfigurationManager.AppSettings["authority"];
           string clientID = ConfigurationManager.AppSettings["clientID"];
           Uri clientAppUri = new Uri(ConfigurationManager.AppSettings["clientAppUri"];
           string serverName = ConfigurationManager.AppSettings["serverName"];
            AuthenticationResult authenticationResult = null;
            AuthenticationContext authenticationContext = new AuthenticationContext(authority, false);
            
            string errorMessage = null;
            try
            {
                Console.WriteLine("Trying to acquire token");
                authenticationResult = authenticationContext.AcquireToken(serverName, clientId, clientAppUri);
            }
                catch (AdalException ex)
            {
                errorMessage = ex.Message;
                if (ex.InnerException != null)
                {
                    errorMessage += "\nInnerException : " + ex.InnerException.Message;
                }
            }
            catch (ArgumentException ex)
            {
                errorMessage = ex.Message;
            }
            if (!string.IsNullOrEmpty(errorMessage))
            {
                Console.WriteLine("Failed: {0}" + errorMessage);
                return;
            }
            Console.WriteLine("\nMaking the protocol call\n");
            ExchangeService exchangeService = new ExchangeService(ExchangeVersion.Exchange2013);
            exchangeService.Url = new Uri(resource + "ews/exchange.asmx");
            exchangeService.TraceEnabled = true;
            exchangeService.TraceFlags = TraceFlags.All;
            exchangeService.Credentials = new OAuthCredentials(authenticationResult.AccessToken);
            exchangeService.FindFolders(WellKnownFolderName.Root, new FolderView(10));
        }
    }
}

```

<span data-ttu-id="a6dcc-140">El código de ejemplo requiere un archivo App.config con las siguientes entradas:</span><span class="sxs-lookup"><span data-stu-id="a6dcc-140">The sample code requires an App.config file with the following entries:</span></span>
  
```xml
<?xml version="1.0" encoding="utf-8" ?>
<configuration>
  <startup>
    <supportedRuntime version="v4.0" sku=".NETFramework,Version=v4.5" />
  </startup>
  <appSettings>
    <add key="authority" value="http://login.windows.net/<devAccountName>.onmicrosoft.com" />
    <add key="clientId" value="<ID generated by Azure Active Directory"/>
    <add key="clientAppUri" value="<URI registered with Azure Active Directory"/>
    <add key="serverName" value="outlook.office365.com" />
  </appSettings>
</configuration>
```

## <a name="see-also"></a><span data-ttu-id="a6dcc-141">Ver también</span><span class="sxs-lookup"><span data-stu-id="a6dcc-141">See also</span></span>

- [<span data-ttu-id="a6dcc-142">Autenticación y EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="a6dcc-142">Authentication and EWS in Exchange</span></span>](authentication-and-ews-in-exchange.md)    
- [<span data-ttu-id="a6dcc-143">Probar e implementar aplicaciones de Office 365</span><span class="sxs-lookup"><span data-stu-id="a6dcc-143">Test and deploy Office 365 apps</span></span>](http://msdn.microsoft.com/en-us/office/office365/howto/test-and-deploy-apps.aspx)
    

