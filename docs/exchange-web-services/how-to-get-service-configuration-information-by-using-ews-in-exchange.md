---
title: Obtener información de configuración de servicio mediante EWS en Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9379740a-96e1-490d-a229-0f9937c548d2
description: Descubra cómo obtener información de configuración del servicio para mensajería unificada, zumbidos de la Directiva, sugerencias de correo y reglas de protección de EWS en Exchange.
ms.openlocfilehash: 7546d9524f1e004eda2bdc55687fb44beafa44af
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44528009"
---
# <a name="get-service-configuration-information-by-using-ews-in-exchange"></a>Obtener información de configuración de servicio mediante EWS en Exchange

Descubra cómo obtener información de configuración del servicio para mensajería unificada, zumbidos de la Directiva, sugerencias de correo y reglas de protección de EWS en Exchange.
  
¿Funciona la aplicación de EWS con la mensajería unificada, los zumbidos de la Directiva, las sugerencias de correo o las reglas de protección? Si es así, la aplicación tendrá que llamar a la [operación GetServiceConfiguration](https://msdn.microsoft.com/library/070cbfe5-325a-4955-8e4a-8230ea0459a7%28Office.15%29.aspx) para obtener la información de configuración del servicio que necesita. La operación **GetServiceConfiguration** devuelve información de configuración específica para cada una de estas características de EWS. 
  
> [!NOTE]
> La API administrada de EWS no implementa esta funcionalidad. 
  
**Tabla 1. Información de configuración que devuelve la operación GetServiceConfiguration**

|Característica EWS|La operación GetServiceConfiguration devuelve...|
|:-----|:-----|
|MU  <br/> | <ul><li>Un valor que indica si la mensajería unificada está habilitada.</li><li>Un valor que indica si está habilitada la función reproducir en teléfono.</li><li>La cadena de marcado de reproducir en teléfono.</li></ul> |
|Zumbidos de Directiva  <br/> | <ul><li>La Directiva zumbidos para mostrar en el cliente.</li></ul> |
|Sugerencias de correo electrónico  <br/> | <ul><li>Un valor que indica si las sugerencias de correo están habilitadas.</li><li>El número máximo de destinatarios por solicitud.</li><li>El tamaño máximo del mensaje.</li><li>El umbral de gran audiencia.</li><li>Un valor que indica si se muestra el número de destinatarios externos.</li><li>Una lista de dominios internos.</li><li>Un valor que indica si las sugerencias de directiva están habilitadas.</li><li>El umbral de la punta de la audiencia grande para indicar si el correo se considera que tiene un gran número de destinatarios.  </li></ul>|
|Reglas de protección  <br/> | <ul><li>Configuración de reglas de protección para el cliente.</li><li>Una lista de los dominios internos de la organización.  </li></ul> |
   
## <a name="code-example-get-service-configuration-information-for-mail-tips-by-using-ews"></a>Ejemplo de código: obtener información de configuración del servicio para sugerencias de correo mediante EWS

En el ejemplo de código siguiente se usa la [operación GetServiceConfiguration](https://msdn.microsoft.com/library/070cbfe5-325a-4955-8e4a-8230ea0459a7%28Office.15%29.aspx) para solicitar información de configuración del servicio para sugerencias de correo. Puede solicitar información de configuración del servicio adicional agregando más elementos [ConfigurationName](https://msdn.microsoft.com/library/3b524a2f-9c6b-4550-9f3d-f78d176b0f7b%28Office.15%29.aspx) con valores diferentes. 
  
```cs
private static void GetServiceConfiguration(ExchangeService service, NetworkCredential creds)
{ 
  // XML for the GetServiceConfiguration request SOAP envelope for mail tips configuration information.
  const string getServiceConfigurationRequest = 
    "<?xml version=\"1.0\" encoding=\"utf-8\"?>\n" +
    "<soap:Envelope xmlns:xsi=\"http://www.w3.org/2001/XMLSchema-instance\"\n" +
    "               xmlns:m=\"https://schemas.microsoft.com/exchange/services/2006/messages\"\n" +
    "               xmlns:t=\"https://schemas.microsoft.com/exchange/services/2006/types\" \n" +
    "               xmlns:soap=\"https://schemas.xmlsoap.org/soap/envelope/\"\n" +
    "               xmlns:xs=\"http://www.w3.org/2001/XMLSchema\">\n" +
    "  <soap:Header>\n" +
    "    <t:RequestServerVersion Version=\"Exchange2013\" />\n" +
    "  </soap:Header>\n" +
    "  <soap:Body>\n" +
    "    <m:GetServiceConfiguration>\n" +
    "      <m:ActingAs>\n" +
    "        <t:EmailAddress>user1@contoso.com</t:EmailAddress>\n" +
    "        <t:RoutingType>SMTP</t:RoutingType>\n" +
    "      </m:ActingAs>\n" +
    "      <m:RequestedConfiguration>\n" +
    "        <m:ConfigurationName>MailTips</m:ConfigurationName>\n" +
    "      </m:RequestedConfiguration>\n" +
    "    </m:GetServiceConfiguration>\n" +
    "  </soap:Body>\n" +
    "</soap:Envelope>";
  // Encoded GetServiceConfiguration operation request.
  byte[] payload = System.Text.Encoding.UTF8.GetBytes(getServiceConfigurationRequest);
  try
  {
    HttpWebRequest request = (HttpWebRequest)WebRequest.Create(service.Url);
    request.AllowAutoRedirect = false;
    request.Credentials = creds;
    request.Method = "POST";
    request.ContentType = "text/xml";
    Stream requestStream = request.GetRequestStream();
    requestStream.Write(payload, 0, payload.Length);
    requestStream.Close();
    HttpWebResponse response = (HttpWebResponse)request.GetResponse();
    if (response.StatusCode == HttpStatusCode.OK)
    {
      Stream responseStream = response.GetResponseStream();
      StreamReader reader = new StreamReader(responseStream);
      string responseFromServer = reader.ReadToEnd();
      Console.WriteLine("You will need to parse this response to get the configuration information:\n\n" + responseFromServer);
      reader.Close();
      responseStream.Close();
    }
    else
      throw new WebException(response.StatusDescription);
          
  }
  catch (WebException e)
  {
    Console.WriteLine(e.Message);
  }
}

```

## <a name="next-steps"></a>Siguientes pasos

Una vez solicitada la información de configuración del servicio, use la [clase XmlDocument](https://msdn.microsoft.com/library/system.xml.xmldocument.aspx) para cargar el XML de respuesta para que pueda analizarlo. A continuación, según el escenario, puede realizar una de las siguientes acciones: 
  
- Use la [operación GetMailTips](https://msdn.microsoft.com/library/025483ec-a9f3-4735-8a95-d26e30ea7974%28Office.15%29.aspx) para obtener sugerencias de correo para que las aplicaciones cliente se muestren a los usuarios. 
    
- Si la mensajería unificada está habilitada, [obtenga información sobre cómo reproducir elementos de buzón](https://blogs.msdn.com/b/exchangedev/archive/2009/11/05/play-exchange-2010-mailbox-items-on-your-phone-by-using-the-ews-managed-api.aspx) a través del teléfono. 
    
## <a name="see-also"></a>Vea también

- [Opciones de configuración de EWS en Exchange](configuration-options-for-ews-in-exchange.md)    
- [Configurar la aplicación EWS](setting-up-your-ews-application.md)    
- [Desarrollo de clientes de servicios web de Exchange](develop-web-service-clients-for-exchange.md)
    

