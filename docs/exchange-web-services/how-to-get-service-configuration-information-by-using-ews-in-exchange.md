---
title: Obtener la información de configuración de servicio mediante el uso de EWS en Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9379740a-96e1-490d-a229-0f9937c548d2
description: Averigüe cómo obtener información de configuración de servicio de mensajería unificada, desplazar de directiva, las sugerencias de correo y las reglas de protección de EWS en Exchange.
ms.openlocfilehash: e84a563bb094a2fe03e08f8e1a81b2b054d45850
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763067"
---
# <a name="get-service-configuration-information-by-using-ews-in-exchange"></a>Obtener la información de configuración de servicio mediante el uso de EWS en Exchange

Averigüe cómo obtener información de configuración de servicio de mensajería unificada, desplazar de directiva, las sugerencias de correo y las reglas de protección de EWS en Exchange.
  
¿La aplicación EWS funciona con mensajería unificada (UM), desplazar de directiva, las sugerencias de correo o las reglas de protección? Si es así, la aplicación deberá llamar a la [operación de GetServiceConfiguration](http://msdn.microsoft.com/library/070cbfe5-325a-4955-8e4a-8230ea0459a7%28Office.15%29.aspx) para obtener la información de configuración de servicio que necesita. La operación **GetServiceConfiguration** devuelve información de configuración que es específica de cada una de estas características EWS. 
  
> [!NOTE]
> La API administrada de EWS no implementa esta funcionalidad. 
  
**La tabla 1. Información de configuración que devuelve la operación GetServiceConfiguration**

|Característica EWS|Devuelve la operación GetServiceConfiguration...|
|:-----|:-----|
|MENSAJERÍA UNIFICADA  <br/> | <ul><li>Un valor que indica si está habilitada la mensajería unificada.</li><li>Un valor que indica si está habilitada la reproducir en el teléfono.</li><li>Reproducir en la cadena de marcado de teléfono.</li></ul> |
|Desplazar de directiva  <br/> | <ul><li>Directiva se desplazará para mostrarla en el cliente.</li></ul> |
|Sugerencias de correo  <br/> | <ul><li>Un valor que indica si están habilitadas las sugerencias de correo.</li><li>El número máximo de destinatarios por solicitud.</li><li>El tamaño máximo de mensaje.</li><li>Umbral de la audiencia de gran tamaño.</li><li>Un valor que indica si se muestra el número de destinatarios externos.</li><li>Una lista de los dominios internos.</li><li>Un valor que indica si están habilitadas las sugerencias de directiva.</li><li>El umbral del límite audiencia grandes para que indica si el correo se considera que tiene un gran número de destinatarios.  </li></ul>|
|Reglas de protección  <br/> | <ul><li>Configuración de reglas de protección de su cliente.</li><li>Una lista de dominios que son internos a la organización.  </li></ul> |
   
## <a name="code-example-get-service-configuration-information-for-mail-tips-by-using-ews"></a>Ejemplo de código: obtener la información de configuración de servicio para las sugerencias de correo mediante el uso de EWS

En el ejemplo de código siguiente se usa la [operación de GetServiceConfiguration](http://msdn.microsoft.com/library/070cbfe5-325a-4955-8e4a-8230ea0459a7%28Office.15%29.aspx) para solicitar información de configuración de servicio para las sugerencias de correo. Puede solicitar información de configuración de servicios adicionales mediante la adición de más elementos [ConfigurationName](http://msdn.microsoft.com/library/3b524a2f-9c6b-4550-9f3d-f78d176b0f7b%28Office.15%29.aspx) con valores diferentes. 
  
```cs
private static void GetServiceConfiguration(ExchangeService service, NetworkCredential creds)
{ 
  // XML for the GetServiceConfiguration request SOAP envelope for mail tips configuration information.
  const string getServiceConfigurationRequest = 
    "<?xml version=\"1.0\" encoding=\"utf-8\"?>\n" +
    "<soap:Envelope xmlns:xsi=\"http://www.w3.org/2001/XMLSchema-instance\"\n" +
    "               xmlns:m=\"http://schemas.microsoft.com/exchange/services/2006/messages\"\n" +
    "               xmlns:t=\"http://schemas.microsoft.com/exchange/services/2006/types\" \n" +
    "               xmlns:soap=\"http://schemas.xmlsoap.org/soap/envelope/\"\n" +
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

Después de solicitar información de configuración de servicio, use la [clase XmlDocument](http://msdn.microsoft.com/en-us/library/system.xml.xmldocument.aspx) para cargar el XML de la respuesta de manera que se puede analizar. A continuación, dependiendo de su situación, puede hacer una de las siguientes: 
  
- Use la [operación de GetMailTips](http://msdn.microsoft.com/library/025483ec-a9f3-4735-8a95-d26e30ea7974%28Office.15%29.aspx) para obtener sugerencias de correo para las aplicaciones de cliente mostrar a los usuarios. 
    
- Si está habilitada la mensajería unificada, [Obtenga información sobre cómo reproducir los elementos del buzón](http://blogs.msdn.com/b/exchangedev/archive/2009/11/05/play-exchange-2010-mailbox-items-on-your-phone-by-using-the-ews-managed-api.aspx) a través de su teléfono. 
    
## <a name="see-also"></a>Ver también

- [Opciones de configuración para EWS en Exchange](configuration-options-for-ews-in-exchange.md)    
- [Configurar una aplicación de EWS](setting-up-your-ews-application.md)    
- [Desarrollo de clientes de servicios web de Exchange](develop-web-service-clients-for-exchange.md)
    

