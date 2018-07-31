---
title: Usar autodetección para buscar puntos de conexión
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 03896542-549b-4c45-973c-98f9025ea26c
description: Descubra cómo usar el servicio Detección automática para indicar a su aplicación de cliente al servidor de Exchange correcto.
ms.openlocfilehash: eb3fb3664e5789638c097a43cf48f757bb0713ae
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/28/2018
ms.locfileid: "21353983"
---
# <a name="use-autodiscover-to-find-connection-points"></a>Usar autodetección para buscar puntos de conexión

Descubra cómo usar el servicio Detección automática para indicar a su aplicación de cliente al servidor de Exchange correcto.
  
El servicio de detección automática de Exchange proporciona la aplicación de cliente con opciones de configuración para las cuentas de correo electrónico que se hospedan en Exchange Online, Exchange Online como parte de Office 365 o un servidor de Exchange que ejecuta una versión de Exchange a partir de Exchange 2013. El servicio Detección automática es un servicio web que proporciona opciones de configuración. El servicio Detección automática es un servicio web que proporciona información de configuración de Exchange server a la aplicación cliente. Las aplicaciones cliente usan la detección automática para determinar el extremo del servicio de detección automática para un buzón específico. En este artículo se explica cómo debe seguir las respuestas de un servidor de Exchange para buscar el extremo correcto. 
  
Para obtener información acerca de cómo obtener los valores de configuración de dirección de correo electrónico, vea [obtener la configuración de usuario de Exchange mediante el uso de detección automática](how-to-get-user-settings-from-exchange-by-using-autodiscover.md) y [obtendrá la configuración de dominio de un servidor de Exchange](how-to-get-domain-settings-from-an-exchange-server.md).
  
> [!NOTE]
> El proceso para buscar el extremo correcto es parte de la solicitud de configuración de usuario o dominio. El servicio Detección automática usa una serie de respuestas de redirección para enviar la aplicación cliente en el extremo correcto para una dirección de correo electrónico. 
  
Puede usar una de las siguientes tecnologías de desarrollo de Exchange para tener acceso al servicio de detección automática:

- La API administrada de servicios Web Exchange (EWS)
    
- EWS
    
Si usa EWS, puede usar los métodos siguientes para recuperar la configuración de usuario:
    
- El servicio Detección automática basado en SOAP
    
- El servicio Detección automática XML (POX)
    
- Un proxy generado automáticamente se ha generado del servicio Detección automática de XML o SOAP
    
Para obtener más información acerca de estos métodos, vea [detección automática de Exchange](autodiscover-for-exchange.md).

Para obtener más información acerca de estas tecnologías de desarrollo de Exchange, vea [Explorar la API administrada de EWS, EWS y web de servicios de Exchange](explore-the-ews-managed-api-ews-and-web-services-in-exchange.md). 

La API administrada de EWS proporciona una interfaz basada en objetos para recuperar la configuración de usuario. Si su aplicación cliente usa un código administrado, le recomendamos que use la API administrada de EWS. La interfaz de la API administrada de EWS está mejor optimizada para un modelo de objetos simples que el típico proxy de servicio web generado automáticamente.  
  
Si está usando EWS, le sugerimos que use el servicio Detección automática de SOAP, ya que admite un conjunto superior de características que el servicio Detección automática de POX.
  
## <a name="prerequisites-for-finding-an-endpoint"></a>Requisitos previos de la búsqueda de un extremo
<a name="bk_Prereq"> </a>

Antes de poder crear una aplicación cliente que usa el servicio de detección automática, necesita tener acceso a lo siguiente:
  
- Exchange Online o un servidor que está ejecutando una versión de Exchange a partir de Exchange 2007 SP1. Si está usando el servicio Detección automática basada en SOAP, Exchange Online o una versión de Exchange a partir de Exchange 2010.
    
- Un servidor de Exchange que está configurado para aceptar conexiones desde la aplicación cliente. Para obtener información acerca de cómo configurar el servidor de Exchange, vea [controlar el acceso de la aplicación de cliente para EWS en Exchange](controlling-client-application-access-to-ews-in-exchange.md).
    
- Una cuenta que está autorizada para uso de EWS. Para obtener información acerca de cómo configurar una cuenta, vea [controlar el acceso de la aplicación de cliente para EWS en Exchange](controlling-client-application-access-to-ews-in-exchange.md).
    
> [!NOTE]
> Si está utilizando la API administrada de EWS, debe proporcionar una devolución de llamada de validación de certificado en algunas circunstancias. También es posible que deba una devolución de llamada de validación de certificado con algunas bibliotecas proxy generado, como las creadas por Visual Studio. Para obtener más información, vea [validar un certificado de servidor para la API administrada de EWS](how-to-validate-a-server-certificate-for-the-ews-managed-api.md). 
  
### <a name="core-concepts-for-finding-an-endpoint"></a>Conceptos básicos de la búsqueda de un extremo
<a name="bk_Core"> </a>

Antes de usar detección automática para encontrar un extremo, debe estar familiarizado con los conceptos que se muestran en la tabla siguiente.
  
|**Concepto**|**Descripción**|
|:-----|:-----|
|[Detección automática de Exchange](autodiscover-for-exchange.md) <br/> |Proporciona información general del funcionamiento del servicio Detección automática.  <br/> |
   
Si está utilizando la API administrada de EWS, use la clase [Microsoft.Exchange.WebServices.Data.ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) en el espacio de nombres [Microsoft.Exchange.WebServices.Data](http://msdn.microsoft.com/en-us/library/dd633907%28v=exchg.80%29.aspx) para administrar la conexión a EWS. Para usar los ejemplos de código de API administrada de EWS en este artículo, debe hacer referencia a los siguientes espacios de nombres en el código: 
  
- **System.Net**
    
- **Microsoft.Exchange.WebServices.Data.ExchangeService**
    
## <a name="find-the-correct-endpoint-by-using-the-ews-managed-api"></a>Buscar el extremo correcto mediante el uso de la API administrada de EWS
<a name="bk_Managed"> </a>

Si está utilizando la API administrada de EWS, llamadas al servicio de detección automática se controlan mediante la clase **ExchangeService** . Para determinar el extremo correcto para una cuenta de correo electrónico, llama al método **AutodiscoverUrl** en un objeto **[ExchangeService]** . En el ejemplo de código siguiente se muestra cómo establecer el extremo de servicio web EWS para una dirección de correo electrónico en el archivo Exchange.asmx en el servidor de acceso de cliente correcto mediante el uso de la API administrada de EWS. 
  
```cs
NetworkCredential credentials = new NetworkCredential(securelyStoredEmail, securelyStoredPassword);
ExchangeService service = new ExchangeService(ExchangeVersion.Exchange2013);
service.Credentials = credentials;
service.AutodiscoverUrl("User1@contoso.com");
```

## <a name="find-the-correct-endpoint-by-using-ews"></a>Buscar el extremo correcto mediante el uso de EWS
<a name="bk_SOAP"> </a>

El servicio de detección automática de SOAP puede utilizar una serie de solicitudes y respuestas para dirigir la aplicación para el extremo correcto para EWS. Para obtener información acerca del proceso para determinar el extremo correcto para una cuenta de correo electrónico, vea [detección automática de Exchange](autodiscover-for-exchange.md). Los siguientes ejemplos XML muestran la serie de solicitudes y respuestas que puede esperar cuando se realiza una solicitud de detección automática de SOAP para encontrar el extremo correcto.
  
### <a name="soap-autodiscover-endpoint-request"></a>Solicitud de extremo de detección automática SOAP

En el ejemplo siguiente se muestra una solicitud XML que se envía al servicio de detección automática para buscar el extremo correcto.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:a="http://schemas.microsoft.com/exchange/2010/Autodiscover" 
        xmlns:wsa="http://www.w3.org/2005/08/addressing" 
        xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
        xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <a:RequestedServerVersion>Exchange2013</a:RequestedServerVersion>
    <wsa:Action>http://schemas.microsoft.com/exchange/2010/Autodiscover/Autodiscover/GetUserSettings</wsa:Action>
    <wsa:To>https://mail.microsoft.com/autodiscover/autodiscover.svc</wsa:To>
  </soap:Header>
  <soap:Body>
    <a:GetUserSettingsRequestMessage xmlns:a="http://schemas.microsoft.com/exchange/2010/Autodiscover">
      <a:Request>
        <a:Users>
          <a:User>
            <a:Mailbox>User1@Contoso.com</a:Mailbox>
          </a:User>
        </a:Users>
        <a:RequestedSettings>
          <a:Setting>InternalEwsUrl</a:Setting>
          <a:Setting>ExternalEwsUrl</a:Setting>
        </a:RequestedSettings>
      </a:Request>
    </a:GetUserSettingsRequestMessage>
  </soap:Body>
</soap:Envelope>

```

### <a name="soap-autodiscover-redirection-response"></a>Respuesta de redirección de detección automática SOAP

El servicio Detección automática puede responder con una de las dos respuestas de redirección: una redirección HTTP 302 o una respuesta de redirección de SOAP. Si la respuesta del servidor de Exchange es un redireccionamiento 302 de HTTP, la aplicación cliente debe validar que la dirección de redireccionamiento es aceptable y, a continuación, siga la respuesta de redirección.
  
> [!IMPORTANT]
> Para los criterios de validación de una respuesta de redirección, vea [detección automática de Exchange](autodiscover-for-exchange.md). 
  
Si el servicio Detección automática devuelve una respuesta de redirección, indicada por el elemento [ErrorCode](http://msdn.microsoft.com/library/0bb00cee-c66b-4f34-b99d-355458f5e83b%28Office.15%29.aspx) del elemento **UserResponse** , la aplicación cliente debe usar el elemento **RedirectTarget** para crear una nueva solicitud de configuración que es se envían al servidor especificado en la respuesta de redirección. En el ejemplo siguiente se muestra una respuesta de redirección desde el servidor. 
  
```XML
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/" xmlns:a="http://www.w3.org/2005/08/addressing">
  <s:Header>
    <a:Action s:mustUnderstand="1">http://schemas.microsoft.com/exchange/2010/
        Autodiscover/Autodiscover/GetUserSettingsResponse</a:Action>
    <h:ServerVersionInfo xmlns:h="http://schemas.microsoft.com/exchange/2010/Autodiscover" 
        xmlns:i="http://www.w3.org/2001/XMLSchema-instance">
      <h:MajorVersion>15</h:MajorVersion>
      <h:MinorVersion>0</h:MinorVersion>
      <h:MajorBuildNumber>682</h:MajorBuildNumber>
      <h:MinorBuildNumber>1</h:MinorBuildNumber>
      <h:Version>Exchange2013</h:Version>
    </h:ServerVersionInfo>
  </s:Header>
  <s:Body>
    <GetUserSettingsResponseMessage xmlns="http://schemas.microsoft.com/exchange/2010/Autodiscover">
      <Response xmlns:i="http://www.w3.org/2001/XMLSchema-instance">
        <ErrorCode>NoError</ErrorCode>
        <ErrorMessage />
        <UserResponses>
          <UserResponse>
            <ErrorCode>RedirectAddress</ErrorCode>
            <ErrorMessage>Redirection address.</ErrorMessage>
            <RedirectTarget>User1@mail.Contoso.com</RedirectTarget>
            <UserSettingErrors />
            <UserSettings />
          </UserResponse>
        </UserResponses>
      </Response>
    </GetUserSettingsResponseMessage>
  </s:Body>
</s:Envelope>

```

Después de una redirección, el cliente utiliza la dirección URL de redirección para preparar otra solicitud. El código siguiente muestra un ejemplo de la solicitud que cree a partir de la respuesta de redirección.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:a="http://schemas.microsoft.com/exchange/2010/Autodiscover" 
        xmlns:wsa="http://www.w3.org/2005/08/addressing" 
        xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
        xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <a:RequestedServerVersion>Exchange2013</a:RequestedServerVersion>
    <wsa:Action>http://schemas.microsoft.com/exchange/2010/
        Autodiscover/Autodiscover/GetUserSettings</wsa:Action>
    <wsa:To>https://autodiscover.exchange.microsoft.com/autodiscover/autodiscover.svc</wsa:To>
  </soap:Header>
  <soap:Body>
    <a:GetUserSettingsRequestMessage xmlns:a="http://schemas.microsoft.com/exchange/2010/Autodiscover">
      <a:Request>
        <a:Users>
          <a:User>
            <a:Mailbox>User1@mail.Contoso.com</a:Mailbox>
          </a:User>
        </a:Users>
        <a:RequestedSettings>
          <a:Setting>InternalEwsUrl</a:Setting>
          <a:Setting>ExternalEwsUrl</a:Setting>
        </a:RequestedSettings>
      </a:Request>
    </a:GetUserSettingsRequestMessage>
  </soap:Body>
</soap:Envelope>

```

Cuando haya se ha indicado a la aplicación cliente para el extremo correcto para el servicio Detección automática, el servidor enviará una respuesta con el elemento [ErrorCode](http://msdn.microsoft.com/library/0bb00cee-c66b-4f34-b99d-355458f5e83b%28Office.15%29.aspx) del elemento **UserResponse** establecida en **NoError** y que contiene la información solicitada configuración del usuario. Sólo la configuración de usuario solicitado, **InternalEwsUrl** y **ExternalEwsUrl**, se devuelve. En el ejemplo siguiente se muestra la respuesta del servidor. 
  
```XML
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/" 
        xmlns:a="http://www.w3.org/2005/08/addressing">
  <s:Header>
    <a:Action s:mustUnderstand="1">http://schemas.microsoft.com/exchange/2010/
        Autodiscover/Autodiscover/GetUserSettingsResponse</a:Action>
    <h:ServerVersionInfo xmlns:h="http://schemas.microsoft.com/exchange/2010/Autodiscover" 
        xmlns:i="http://www.w3.org/2001/XMLSchema-instance">
      <h:MajorVersion>15</h:MajorVersion>
      <h:MinorVersion>0</h:MinorVersion>
      <h:MajorBuildNumber>160</h:MajorBuildNumber>
      <h:MinorBuildNumber>4</h:MinorBuildNumber>
      <h:Version>Exchange2013</h:Version>
    </h:ServerVersionInfo>
  </s:Header>
  <s:Body>
    <GetUserSettingsResponseMessage xmlns="http://schemas.microsoft.com/exchange/2010/Autodiscover">
      <Response xmlns:i="http://www.w3.org/2001/XMLSchema-instance">
        <ErrorCode>NoError</ErrorCode>
        <ErrorMessage />
        <UserResponses>
          <UserResponse>
            <ErrorCode>NoError</ErrorCode>
            <ErrorMessage>No error.</ErrorMessage>
            <RedirectTarget i:nil="true" />
            <UserSettingErrors />
            <UserSettings>
              <UserSetting i:type="StringSetting">
                <Name>InternalEwsUrl</Name>
                <Value>https://server.Contoso.com/ews/exchange.asmx</Value>
              </UserSetting>
              <UserSetting i:type="StringSetting">
                <Name>ExternalEwsUrl</Name>
                <Value>https://server.Contoso.com/ews/exchange.asmx</Value>
              </UserSetting>
            </UserSettings>
          </UserResponse>
        </UserResponses>
      </Response>
    </GetUserSettingsResponseMessage>
  </s:Body>
</s:Envelope>
```

## <a name="next-steps"></a>Pasos siguientes
<a name="bk_Next"> </a>

Buscar el extremo siguiendo el proceso de detección automática devuelve el dominio solicitado o la configuración del usuario. Para obtener información acerca de cómo realizar una solicitud para configuraciones específicas, vea los siguientes artículos:
  
- [Obtener la configuración de dominio de un servidor de Exchange](how-to-get-domain-settings-from-an-exchange-server.md)    
- [Obtener la configuración de usuario de Exchange mediante el uso de detección automática](how-to-get-user-settings-from-exchange-by-using-autodiscover.md)
    
## <a name="see-also"></a>Vea también

- [Configurar la aplicación EWS](setting-up-your-ews-application.md)   
- [Detección automática de Exchange](autodiscover-for-exchange.md)    
- [Referencia de servicio web de detección automática para Exchange](http://msdn.microsoft.com/library/a01124a8-a8cf-4b80-8625-d7ee05690bca%28Office.15%29.aspx)    
- [Referencia EWS para Exchange](http://msdn.microsoft.com/library/2a873474-1bb2-4cb1-a556-40e8c4159f4a%28Office.15%29.aspx)
    

