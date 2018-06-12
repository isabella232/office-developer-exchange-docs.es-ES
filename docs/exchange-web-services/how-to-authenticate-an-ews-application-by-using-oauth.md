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
# <a name="authenticate-an-ews-application-by-using-oauth"></a>Autenticar una aplicación EWS mediante OAuth

Obtenga información sobre cómo usar la autenticación de OAuth con las aplicaciones de la API administrada de EWS.
  
Puede usar el servicio de autenticación de OAuth proporcionado por Azure Active Directory para integrar las aplicaciones de la API administrada de EWS con el mismo modelo de autenticación usado por la API de REST de Office 365. Para usar OAuth con la aplicación, necesitará:
  
1. [Registrar la aplicación](#bk_register) con Azure Active Directory. 
    
2. [Agregar código para obtener un token de autenticación](#bk_getToken) para obtener una autenticación símbolo (token) de un servidor de token. 
    
3. [Agregar un token de autenticación para las solicitudes EWS](#bk_useToken) que envíe. 
    
> [!NOTE]
> Autenticación de OAuth para EWS sólo está disponible en Exchange como parte de Office 365. Las aplicaciones de EWS requieren el permiso "Acceso total al buzón del usuario". 
  
Para usar el código de este artículo, necesita tener acceso a la siguiente:
  
- Una [cuenta de desarrollador de Office 365](http://office.microsoft.com/compare-office-365-for-business-plans-FX102918419.aspx.aspx). Puede usar una cuenta de prueba para probar la aplicación
    
- La [biblioteca de autenticación de Azure AD para. NET](http://msdn.microsoft.com/en-us/library/office/jj573266.aspx.aspx).
    
- [API administrada de EWS](https://github.com/officedev/ews-managed-api.aspx).

<a name="bk_register"> </a>

## <a name="register-your-application"></a>Registrar la aplicación

Para usar OAuth, una aplicación debe tener un identificador de cliente y un URI que identifica la aplicación de aplicación. Si aún no ha registrado su aplicación con servicios de Azure Active Directory, debe agregar manualmente la aplicación siguiendo los pasos en el [registro de aplicación](http://msdn.microsoft.com/en-us/office/office365/howto/test-and-deploy-apps.aspx).

<a name="bk_getToken"> </a>

## <a name="add-code-to-get-an-authentication-token"></a>Agregar código para obtener un token de autenticación

La biblioteca de autenticación de AD Azure para .NET simplifica la obtención de un token de autenticación de Azure Active Directory para que se puede utilizar el token en la aplicación. Debe proporcionar cuatro fragmentos de información para obtener el token:
  
1. El URI del servidor de símbolo (token). El servidor de token es la **entidad de certificación** que autentica al usuario y devuelve un símbolo (token) que la aplicación puede utilizar para tener acceso a EWS. 
    
2. El identificador de cliente de aplicación que se crea al registrar la aplicación con Azure Active Directory.
    
3. El cliente de aplicación de URI que se crean al registrar la aplicación con Azure Active Directory.
    
4. El URI del servidor EWS y el URI del extremo de EWS. Para Exchange como parte de Office 365, será `https://<server name>/ews/exchange.asmx`.
    
El código siguiente muestra cómo usar la biblioteca de autenticación de AD Azure para obtener un token de autenticación. Se supone que la información necesaria para realizar la solicitud de autenticación se almacena en el archivo de App.config de la aplicación. En este ejemplo no incluyen comprobación de errores, vea el [ejemplo de código](#bk_codeSample) para el código completo. 
  
```cs
string authority = ConfigurationManager.AppSettings["authority"];
string clientID = ConfigurationManager.AppSettings["clientID"];
Uri clientAppUri = new Uri(ConfigurationManager.AppSettings["clientAppUri"];
string serverName = ConfigurationManager.AppSettings["serverName"];
AuthenticationContext authenticationContext = new AuthenticationContext(authority, false);
AuthenticationResult authenticationResult = authenticationContext.AcquireToken(serverName, clientId, clientAppUri);

```

<a name="bk_useToken"> </a>

## <a name="add-an-authentication-token-to-ews-requests"></a>Agregar un token de autenticación para las solicitudes EWS

Una vez que ha recibido el objeto **AuthenticationResult** puede usar la propiedad **AccessToken** para obtener el token emitido por el servicio de token. 
  
```cs
ExchangeService exchangeService = new ExchangeService(ExchangeVersion.Exchange2013);
exchangeService.Url = new Uri(ConfigurationManager.AppSettings["serverName"]+"ews/exchange.asmx");
exchangeService.TraceEnabled = true;
exchangeService.TraceFlags = TraceFlags.All;
exchangeService.Credentials = new OAuthCredentials(authenticationResult.AccessToken));
exchangeService.FindFolders(WellKnownFolderName.Root, new Folderview(10));
```

<a name="bk_codeSample"> </a>

## <a name="code-sample"></a>Ejemplo de código

El siguiente es el ejemplo de código completo que muestra cómo realizar una solicitud de autenticación de OAuth EWS.
  
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

El código de ejemplo requiere un archivo App.config con las siguientes entradas:
  
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

## <a name="see-also"></a>Ver también

- [Autenticación y EWS en Exchange](authentication-and-ews-in-exchange.md)    
- [Probar e implementar aplicaciones de Office 365](http://msdn.microsoft.com/en-us/office/office365/howto/test-and-deploy-apps.aspx)
    

