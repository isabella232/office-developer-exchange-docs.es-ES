---
title: Obtener la configuración de dominio de un servidor de Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 2f9acb81-5135-4f72-94e8-65c235d725e6
description: Aprenda a obtener la configuración del dominio de un servidor Exchange mediante el servicio Detección automática.
ms.openlocfilehash: 0dd990cc82762936e7827115685ce0178eafb5ae
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763070"
---
# <a name="get-domain-settings-from-an-exchange-server"></a>Obtener la configuración de dominio de un servidor de Exchange

Aprenda a obtener la configuración del dominio de un servidor Exchange mediante el servicio Detección automática.
  
Puede recuperar información de configuración de un dominio de correo electrónico mediante el servicio Detección automática. El servicio Detección automática proporciona un proceso a la aplicación para conectarse al punto de conexión del servicio correcto de un dominio específico.
  
Puede usar una de las siguientes tecnologías de desarrollo para tener acceso al servicio Detección automática:
  
- La API administrada de servicios Web Exchange (EWS)
    
- EWS
    
    Si usa EWS, puede usar los métodos siguientes para recuperar la configuración de usuario:
    
  - El servicio Detección automática basado en SOAP
    
  - El servicio Detección automática XML (POX)
    
  - Un proxy generado automáticamente se ha generado del servicio Detección automática de XML o SOAP
    
    Para obtener más información acerca de estos métodos, vea [detección automática de Exchange](autodiscover-for-exchange.md).
    
La API administrada de EWS proporciona una interfaz basada en objetos para recuperar la configuración de usuario. Si su aplicación cliente usa un código administrado, le recomendamos que use la API administrada de EWS. La interfaz de la API administrada de EWS está mejor optimizada para un modelo de objetos simples que el típico proxy de servicio web generado automáticamente.  
  
Si está usando EWS, le sugerimos que use el servicio Detección automática de SOAP, ya que admite un conjunto superior de características que el servicio Detección automática de POX.
  
El servicio Detección automática solo devuelve las opciones de configuración solicitadas. En la siguiente tabla se enumeran las opciones de configuración del dominio que puede devolver el servicio Detección automática.
  
**La tabla 1: Opciones de configuración de dominio**

|**Opción de configuración**|**Descripción**|
|:-----|:-----|
|ExternalEwsUrl  <br/> |La dirección URL externa para EWS.  <br/> |
|ExternalEwsVersion  <br/> |La versión del servidor Exchange que hospeda la dirección URL de EWS.  <br/> |
   
## <a name="prerequisites-for-getting-domain-settings"></a>Requisitos previos para obtener la configuración del dominio
<a name="bk_Prereq"> </a>

Antes de crear una aplicación que se conecte al servicio Detección automática para obtener la configuración del dominio, asegúrese de que tiene acceso a lo siguiente:
  
- Exchange Online, Exchange Online como parte de Office 365 o un servidor que ejecuta una versión de Exchange a partir de Exchange 2007. Si está usando el servicio Detección automática basado en SOAP de EWS, un servidor que ejecuta una versión de Exchange a partir de Exchange 2010.
    
- Un servidor de Exchange que está configurado para aceptar conexiones desde la aplicación cliente. Para obtener información acerca de cómo configurar el servidor de Exchange, vea [controlar el acceso de la aplicación de cliente para EWS en Exchange](controlling-client-application-access-to-ews-in-exchange.md).
    
- Una cuenta que está autorizada para uso de EWS. Para obtener información acerca de cómo configurar una cuenta, vea [controlar el acceso de la aplicación de cliente para EWS en Exchange](controlling-client-application-access-to-ews-in-exchange.md).
    
> [!NOTE]
> Si está utilizando la API administrada de EWS, debe proporcionar una devolución de llamada de validación de certificado en algunas circunstancias. También es posible que deba una devolución de llamada de validación de certificado con algunas bibliotecas proxy generado, como las creadas por Visual Studio. Para obtener más información, vea [validar un certificado de servidor para la API administrada de EWS](how-to-validate-a-server-certificate-for-the-ews-managed-api.md). 
  
### <a name="core-concepts-for-getting-domain-settings"></a>Conceptos básicos para obtener la configuración del dominio
<a name="bk_Core"> </a>

Antes de que use la Detección automática para obtener la configuración del dominio, debería familiarizarse con los conceptos que se enumeran en la siguiente tabla.
  
|**Concepto**|**Descripción**|
|:-----|:-----|
|[Detección automática de Exchange](autodiscover-for-exchange.md) <br/> |Proporciona información general del funcionamiento del servicio Detección automática.  <br/> |
|[Usar detección automática para buscar puntos de conexión](how-to-use-autodiscover-to-find-connection-points.md) <br/> |Describe el proceso que ha usado el servicio Detección automática para redirigir la aplicación cliente al punto de conexión de servicio correcto.  <br/> |
   
Si está utilizando la API administrada de EWS, use la clase [Microsoft.Exchange.WebServices.Data.ExchangeService](http://msdn.microsoft.com/en-us/library/exchange/dd635811%28v=exchg.80%29.aspx) en el espacio de nombres [Microsoft.Exchange.WebServices.Data](http://msdn.microsoft.com/en-us/library/exchange/dd633907%28v=exchg.80%29.aspx) para administrar la conexión a EWS. Los ejemplos de código en esta sección se suponen que hace referencia a los siguientes espacios de nombres en el código: 
  
- **System.Net**
    
- **Microsoft.Exchange.WebServices.Data.ExchangeService**
    
## <a name="get-domain-settings-by-using-the-ews-managed-api"></a>Obtener la configuración del dominio mediante la API administrada de EWS
<a name="bk_Managed"> </a>

Si está utilizando la API administrada de EWS, puede usar el método [Microsoft.Exchange.WebServices.Data.AutodiscoverSettings.GetUserSettings](http://msdn.microsoft.com/en-us/library/exchange/microsoft.exchange.webservices.autodiscover.autodiscoverservice.getusersettings%28v=exchg.80%29.aspx) del objeto [Microsoft.Exchange.WebServices.Data.AutodiscoverService](http://msdn.microsoft.com/en-us/library/exchange/dd634321%28v=exchg.80%29.aspx) para generar la solicitud que recupera información de configuración para un dominio, tal como se muestra en el siguiente ejemplo. En este ejemplo, solo algunas de las opciones de dominio posibles se solicitan y se devuelven sólo los valores solicitados desde el servidor. 
  
```cs
AutodiscoverService autodiscoverService = new AutodiscoverService("domain.contoso.com");
autodiscoverService.Credentials = new NetworkCredential("User1", "password", "domain.contoso.com");
// Submit a request and get the settings. The response contains only the
// settings that are requested, if they exist.
GetDomainSettingsResponse domainresponse = autodiscoverService.GetDomainSettings(
    "domain",
    ExchangeVersion.Exchang2013,
    DomainSettingName.ExternalEwsUrl,
    DomainSettingName.ExternalEwsVersion);
```

Puede analizar la colección que se ha devuelto para tener acceso a cada par clave-valor. En el siguiente ejemplo se muestra cómo analizar mediante cada elemento devuelto y mostrar el nombre y el valor de cada par clave-valor.
  
```cs
// Display each retrieved value. The settings are part of a key/value pair.
foreach (KeyValuePair<DomainSettingName, Object> domainsetting in domainresponse.Settings)
{
    Console.WriteLine(domainsetting.Key.ToString() + ": " + domainsetting.Value.ToString());
}
```

Como alternativa, puede obtener el valor de una configuración específica. En el siguiente ejemplo, el valor de **ExternalEwsUrl** es que se mostrará. 
  
```cs
// Display a specific setting, such as ExternalEwsUrl.
Console.WriteLine(domainresponse.Settings[DomainSettingName.ExternalEwsUrl]);
```

## <a name="get-user-settings-by-using-ews-soap-autodiscover"></a>Obtener la configuración de usuario mediante la Detección automática SOAP de EWS
<a name="bk_SOAP"> </a>

En el siguiente ejemplo se muestra una solicitud XML de SOAP para obtener la configuración de dominio del servicio Detección automática.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:a="http://schemas.microsoft.com/exchange/2010/Autodiscover" 
        xmlns:wsa="http://www.w3.org/2005/08/addressing" 
        xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
        xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <a:RequestedServerVersion>Exchange2013</a:RequestedServerVersion>
    <wsa:Action>http://schemas.microsoft.com/exchange/2010/Autodiscover/Autodiscover/GetDomainSettings</wsa:Action>
    <wsa:To>https://autodiscover.exchange.microsoft.com/autodiscover/autodiscover.svc</wsa:To>
  </soap:Header>
  <soap:Body>
    <a:GetDomainSettingsRequestMessage xmlns:a="http://schemas.microsoft.com/exchange/2010/Autodiscover">
      <a:Request>
        <a:Domains>
          <a:Domain>domain</a:Domain>
        </a:Domains>
        <a:RequestedSettings>
          <a:Setting>ExternalEwsUrl</a:Setting>
          <a:Setting>ExternalEwsVersion</a:Setting>
        </a:RequestedSettings>
        <a:RequestedVersion>Exchange2013</a:RequestedVersion>
      </a:Request>
    </a:GetDomainSettingsRequestMessage>
  </soap:Body>
</soap:Envelope>
```

En el siguiente ejemplo se muestra la respuesta XML que se ha devuelto del servidor después de que analice la solicitud del cliente.
  
```XML
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/" 
        xmlns:a="http://www.w3.org/2005/08/addressing">
  <s:Header>
    <a:Action s:mustUnderstand="1">http://schemas.microsoft.com/exchange/2010/
          Autodiscover/Autodiscover/GetDomainSettingsResponse</a:Action>
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
    <GetDomainSettingsResponseMessage xmlns="http://schemas.microsoft.com/exchange/2010/Autodiscover">
      <Response xmlns:i="http://www.w3.org/2001/XMLSchema-instance">
        <ErrorCode>NoError</ErrorCode>
        <ErrorMessage />
        <DomainResponses>
          <DomainResponse>
            <ErrorCode>NoError</ErrorCode>
            <ErrorMessage>No error.</ErrorMessage>
            <DomainSettingErrors />
            <DomainSettings>
              <DomainSetting i:type="DomainStringSetting">
                <Name>ExternalEwsUrl</Name>
                <Value>https://failover.exchange.microsoft.com/ews/exchange.asmx</Value>
              </DomainSetting>
              <DomainSetting i:type="DomainStringSetting">
                <Name>ExternalEwsVersion</Name>
                <Value>15.00.0085.000</Value>
              </DomainSetting>
            </DomainSettings>
            <RedirectTarget i:nil="true" />
          </DomainResponse>
        </DomainResponses>
      </Response>
    </GetDomainSettingsResponseMessage>
  </s:Body>
</s:Envelope>
```

## <a name="next-steps"></a>Siguientes pasos
<a name="bk_Next"> </a>

La configuración de dominio proporciona la información básica que su cliente necesita para conectarse a EWS. Puede usar esta información para conectarse a EWS, o puede recuperar las opciones de configuración adicionales de una cuenta de correo electrónico del servidor. Para obtener más información, vea el siguiente artículo:
  
- [Obtener la configuración de usuario de Exchange mediante el uso de detección automática](how-to-get-user-settings-from-exchange-by-using-autodiscover.md)
    
## <a name="see-also"></a>Vea también


- [Configurar una aplicación de EWS](setting-up-your-ews-application.md)
    
- [Referencia de servicio web de detección automática para Exchange](http://msdn.microsoft.com/library/a01124a8-a8cf-4b80-8625-d7ee05690bca%28Office.15%29.aspx)
    
- [Referencia EWS para Exchange](http://msdn.microsoft.com/library/2a873474-1bb2-4cb1-a556-40e8c4159f4a%28Office.15%29.aspx)
    

