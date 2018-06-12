---
title: Seguimiento de las solicitudes y respuestas para solucionar problemas de aplicaciones de la API administrada de EWS
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 186c1d1d-b8dc-4914-b3cd-6fada7ecd877
description: Descubra cómo realizar un seguimiento de las solicitudes EWS y respuestas para solucionar problemas de errores en una aplicación de API administrada de EWS.
ms.openlocfilehash: 056a1f84c4172b0404975d6fc35f9ecd7395ecdb
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763173"
---
# <a name="trace-requests-and-responses-to-troubleshoot-ews-managed-api-apps"></a>Seguimiento de las solicitudes y respuestas para solucionar problemas de aplicaciones de la API administrada de EWS

Descubra cómo realizar un seguimiento de las solicitudes EWS y respuestas para solucionar problemas de errores en una aplicación de API administrada de EWS.
  
Depurar una aplicación de servicio web puede resultar difícil debido a que parte del procesamiento se realiza en un equipo remoto que no puede tener acceso a. Debido a que no se puede recorrer el código en el servidor, puede ser útil ver las solicitudes XML y las respuestas que se envían entre el cliente y el servidor para determinar qué parte de la aplicación está provocando un error. 
  
Si usa EWS, ya tiene acceso a la solicitud XML y la respuesta; puede colocar un punto de interrupción en el código para revisar la respuesta del servidor a la solicitud con el fin de solucionar un problema. Si se usa la API administrada de EWS, no tiene acceso directo a la solicitud EWS y la respuesta. Sin embargo, puede usar los métodos de seguimiento en el objeto [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) para capturar la solicitud XML y la respuesta y, a continuación, puede usar el código XML para determinar por qué no funciona el código. 

Por ejemplo, si no ha definido una propiedad correctamente, es posible que obtenga una respuesta inesperada, y puede utilizar los resultados de seguimiento para buscar en la solicitud XML y la respuesta para identificar el error. Los resultados del seguimiento de la API administrada de EWS también pueden ayudar a crear manualmente la solicitud XML para crear la aplicación de EWS. Si usa EWS, puede crear una aplicación pequeña mediante el uso de API administrada de EWS, seguimiento de él y, a continuación, use la información de la solicitud XML que le ayudarán a crear la solicitud EWS. 
  
## <a name="enabling-tracing-on-the-exchangeservice-object"></a>Al habilitar el seguimiento en el objeto ExchangeService
<a name="bk_EnableTracing"> </a>

Para habilitar el seguimiento, cree un objeto [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) para la aplicación y establecer las propiedades de seguimiento tal como se muestra en el siguiente ejemplo. 
  
```cs
ExchangeService service = new ExchangeService(ExchangeVersion.Exchange2010);
service.TraceListener = ITraceListenerInstance;
// Optional flags to indicate the requests and responses to trace.
service.TraceFlags = TraceFlags.EwsRequest | TraceFlags.EwsResponse
service.TraceEnabled = true;

```

Después de establecer la propiedad [TraceEnabled](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservicebase.traceenabled%28v=exchg.80%29.aspx) en **true**, se enviarán todas las solicitudes que coinciden con los marcadores de seguimiento en el agente de escucha de seguimiento especificado. Puede especificar una marca de seguimiento único, o puede especificar varios indicadores de traza mediante la combinación de ellas con un operador lógico **OR**. Puede usar la [enumeración TraceFlags](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.traceflags%28v=exchg.80%29.aspx) para especificar valores para EWS y para las respuestas y solicitudes de detección automática. 
  
## <a name="implementing-a-tracelistener-object"></a>Implementación de un objeto TraceListener
<a name="bk_traceListener"> </a>

Puede establecer la propiedad [TraceEnabled](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservicebase.traceenabled%28v=exchg.80%29.aspx) en **true** para las solicitudes XML y las respuestas a la aplicación, como una ventana de la consola de salida. Si desea controlar los resultados del seguimiento y guárdelo en un archivo, se recomienda que implemente un objeto [TraceListener (clase)](http://msdn.microsoft.com/en-us/library/system.diagnostics.tracelistener.aspx) . En el ejemplo de código siguiente se muestra un objeto simple que implementa la interfaz [ITraceListener](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.itracelistener%28v=exchg.80%29.aspx) y almacena el seguimiento de las solicitudes y respuestas en archivos XML o de texto. 
  
```cs
class TraceListener : ITraceListener
{
    #region ITraceListener Members
    public void Trace(string traceType, string traceMessage)
    {
      CreateXMLTextFile(traceType, traceMessage.ToString());
    }
    #endregion
    private void CreateXMLTextFile(string fileName, string traceContent)
    {
      // Create a new XML file for the trace information.
      try
      {
        // If the trace data is valid XML, create an XmlDocument object and save.
        XmlDocument xmlDoc = new XmlDocument();
        xmlDoc.Load(traceContent);
        xmlDoc.Save(fileName + ".xml");
      }
      catch
      {
        // If the trace data is not valid XML, save it as a text document.
        System.IO.File.WriteAllText(fileName + ".txt", traceContent);
      }
    }
}

```

## <a name="see-also"></a>Ver también

- [Empezar a utilizar servicios web de Exchange](start-using-web-services-in-exchange.md)
- [Administrar los mensajes de error de detección automática](handling-autodiscover-error-messages.md)    
- [Hacer referencia al ensamblado de la API administrada de EWS](how-to-reference-the-ews-managed-api-assembly.md)    
- [Comunicarse con EWS mediante el uso de la API administrada de EWS](how-to-communicate-with-ews-by-using-the-ews-managed-api.md)
    

