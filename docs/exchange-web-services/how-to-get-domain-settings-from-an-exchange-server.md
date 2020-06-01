---
title: Obtener la configuración de dominio de un servidor de Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: 2f9acb81-5135-4f72-94e8-65c235d725e6
description: Aprenda a obtener la configuración del dominio de un servidor Exchange mediante el servicio Detección automática.
localization_priority: Priority
ms.openlocfilehash: e77810089b77f614f6bca064b2e5cf6bde2bff7c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44455810"
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
    
    Para obtener más información sobre estos métodos, vea [Detección automática en Exchange](autodiscover-for-exchange.md).
    
La API administrada de EWS proporciona una interfaz basada en objetos para recuperar la configuración de usuario. Si su aplicación cliente usa un código administrado, le recomendamos que use la API administrada de EWS. La interfaz de la API administrada de EWS está mejor optimizada para un modelo de objetos simples que el típico proxy de servicio web generado automáticamente.  
  
Si está usando EWS, le sugerimos que use el servicio Detección automática de SOAP, ya que admite un conjunto superior de características que el servicio Detección automática de POX.
  
El servicio Detección automática solo devuelve las opciones de configuración solicitadas. En la siguiente tabla se enumeran las opciones de configuración de dominio que puede devolver el servicio Detección automática.
  
**Tabla 1: Opciones de configuración de dominio**

|**Opción de configuración**|**Descripción**|
|:-----|:-----|
|ExternalEwsUrl  <br/> |La dirección URL externa para EWS.  <br/> |
|ExternalEwsVersion  <br/> |La versión del servidor Exchange que hospeda la dirección URL de EWS.  <br/> |
   
## <a name="prerequisites-for-getting-domain-settings"></a>Requisitos previos para obtener la configuración del dominio
<a name="bk_Prereq"> </a>

Antes de crear una aplicación que se conecte al servicio Detección automática para obtener la configuración del dominio, asegúrese de que tiene acceso a lo siguiente:
  
- Exchange Online, Exchange Online como parte de Office 365 o un servidor que ejecuta una versión de Exchange a partir de Exchange 2007. Si está usando el servicio Detección automática basado en SOAP de EWS, un servidor que ejecuta una versión de Exchange a partir de Exchange 2010.
    
- Un servidor Exchange que está configurado para aceptar conexiones de su aplicación cliente. Para obtener información sobre cómo configurar su servidor de Exchange, vea [Controlar el acceso de la aplicación de cliente a EWS en Exchange](controlling-client-application-access-to-ews-in-exchange.md).
    
- Una cuenta que esté autorizada para usar EWS. Para obtener información sobre cómo configurar una cuenta, vea [Controlar el acceso de la aplicación de cliente a EWS en Exchange](controlling-client-application-access-to-ews-in-exchange.md).
    
> [!NOTE]
> Si está usando la API administrada de EWS, debe proporcionar una devolución de llamada de validación de certificado en algunas circunstancias. También puede necesitar una devolución de llamada de validación de certificado con algunas bibliotecas de proxy generadas, como las que se han creado mediante Visual Studio. Para obtener más información, vea [Validar un certificado de servidor de la API de administración de EWS](how-to-validate-a-server-certificate-for-the-ews-managed-api.md). 
  
### <a name="core-concepts-for-getting-domain-settings"></a>Conceptos básicos para obtener la configuración del dominio
<a name="bk_Core"> </a>

Antes de que use la Detección automática para obtener la configuración del dominio, debería familiarizarse con los conceptos que se enumeran en la siguiente tabla.
  
|**Concepto**|**Descripción**|
|:-----|:-----|
|[Detección automática en Exchange](autodiscover-for-exchange.md) <br/> |Proporciona información general del funcionamiento del servicio Detección automática.  <br/> |
|[Usar autodetección para buscar puntos de conexión](how-to-use-autodiscover-to-find-connection-points.md) <br/> |Describe el proceso que ha usado el servicio Detección automática para redirigir la aplicación cliente al punto de conexión de servicio correcto.  <br/> |
   
Si usa la API administrada de EWS, usa la clase [Microsoft.Exchange.WebServices.Data.ExchangeService](https://msdn.microsoft.com/library/exchange/dd635811%28v=exchg.80%29.aspx) del espacio de nombres [Microsoft.Exchange.WebServices.Data](https://msdn.microsoft.com/library/exchange/dd633907%28v=exchg.80%29.aspx) para administrar la conexión con EWS. En los ejemplos de código de esta sección se asume que hace referencia a los siguientes espacios de nombres en el código: 
  
- **System.Net**
    
- **Microsoft.Exchange.WebServices.Data.ExchangeService**
    
## <a name="get-domain-settings-by-using-the-ews-managed-api"></a>Obtener la configuración del dominio mediante la API administrada de EWS
<a name="bk_Managed"> </a>

Si usa la API administrada de EWS, puede usar el método [Microsoft.Exchange.WebServices.Data.AutodiscoverSettings.GetUserSettings](https://msdn.microsoft.com/library/exchange/microsoft.exchange.webservices.autodiscover.autodiscoverservice.getusersettings%28v=exchg.80%29.aspx) del objeto [Microsoft.Exchange.WebServices.Data.AutodiscoverService ](https://msdn.microsoft.com/library/exchange/dd634321%28v=exchg.80%29.aspx) para generar la solicitud que recupera información de configuración para un dominio, como se muestra en el ejemplo siguiente. En este ejemplo, solo se solicitan algunas de las posibles opciones de configuración del dominio, y solo las opciones de configuración solicitadas se devuelven del servidor. 
  
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

De manera alternativa, puede obtener el valor de una configuración específica. En el siguiente ejemplo, se va a mostrar la configuración **ExternalEwsUrl**. 
  
```cs
// Display a specific setting, such as ExternalEwsUrl.
Console.WriteLine(domainresponse.Settings[DomainSettingName.ExternalEwsUrl]);
```

## <a name="get-user-settings-by-using-ews-soap-autodiscover"></a>Obtener la configuración de usuario mediante la Detección automática SOAP de EWS
<a name="bk_SOAP"> </a>

En el siguiente ejemplo se muestra una solicitud XML de SOAP para obtener la configuración de dominio del servicio Detección automática.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:a="https://schemas.microsoft.com/exchange/2010/Autodiscover" 
        xmlns:wsa="http://www.w3.org/2005/08/addressing" 
        xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
        xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <a:RequestedServerVersion>Exchange2013</a:RequestedServerVersion>
    <wsa:Action>https://schemas.microsoft.com/exchange/2010/Autodiscover/Autodiscover/GetDomainSettings</wsa:Action>
    <wsa:To>https://autodiscover.exchange.microsoft.com/autodiscover/autodiscover.svc</wsa:To>
  </soap:Header>
  <soap:Body>
    <a:GetDomainSettingsRequestMessage xmlns:a="https://schemas.microsoft.com/exchange/2010/Autodiscover">
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
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/" 
        xmlns:a="http://www.w3.org/2005/08/addressing">
  <s:Header>
    <a:Action s:mustUnderstand="1">https://schemas.microsoft.com/exchange/2010/
          Autodiscover/Autodiscover/GetDomainSettingsResponse</a:Action>
    <h:ServerVersionInfo xmlns:h="https://schemas.microsoft.com/exchange/2010/Autodiscover" 
          xmlns:i="http://www.w3.org/2001/XMLSchema-instance">
      <h:MajorVersion>15</h:MajorVersion>
      <h:MinorVersion>0</h:MinorVersion>
      <h:MajorBuildNumber>160</h:MajorBuildNumber>
      <h:MinorBuildNumber>4</h:MinorBuildNumber>
      <h:Version>Exchange2013</h:Version>
    </h:ServerVersionInfo>
  </s:Header>
  <s:Body>
    <GetDomainSettingsResponseMessage xmlns="https://schemas.microsoft.com/exchange/2010/Autodiscover">
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


- [Configurar la aplicación EWS](setting-up-your-ews-application.md)
    
- [Referencia del servicio web de Detección automática para Exchange](https://msdn.microsoft.com/library/a01124a8-a8cf-4b80-8625-d7ee05690bca%28Office.15%29.aspx)
    
- [Referencia EWS para Exchange](https://msdn.microsoft.com/library/2a873474-1bb2-4cb1-a556-40e8c4159f4a%28Office.15%29.aspx)
    

