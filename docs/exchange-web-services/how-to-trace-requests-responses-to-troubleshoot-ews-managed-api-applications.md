---
title: Seguimiento de solicitudes y respuestas para solucionar problemas de aplicaciones de la API administrada de EWS
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: 186c1d1d-b8dc-4914-b3cd-6fada7ecd877
description: Descubra cómo realizar un seguimiento de las solicitudes y respuestas de EWS para solucionar errores en la aplicación de la API administrada de EWS.
localization_priority: Priority
ms.openlocfilehash: dd225030d62a2e8211b7063ee78a59fd1a070263
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44455859"
---
# <a name="trace-requests-and-responses-to-troubleshoot-ews-managed-api-apps"></a>Seguimiento de solicitudes y respuestas para solucionar problemas de aplicaciones de la API administrada de EWS

Descubra cómo realizar un seguimiento de las solicitudes y respuestas de EWS para solucionar errores en la aplicación de la API administrada de EWS.
  
La depuración de una aplicación basada en el servicio web puede resultar difícil porque parte del procesamiento se realiza en un equipo remoto al que puede que no tenga acceso. Como no puede recorrer el código en el servidor, puede resultar útil ver las solicitudes y respuestas XML que se envían entre el cliente y el servidor para determinar qué parte de la aplicación está causando un error. 
  
Si está usando EWS, ya tiene acceso a la solicitud y respuesta XML; puede colocar un punto de interrupción en el código para revisar la respuesta del servidor a su solicitud a fin de solucionar un problema. Si está usando la API administrada de EWS, no tiene acceso directo a la solicitud y respuesta de EWS. Sin embargo, puede usar métodos de seguimiento en el objeto [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) para capturar la solicitud XML y la respuesta y, a continuación, puede usar el XML para determinar por qué el código no funciona. 

Por ejemplo, si no estableció correctamente una propiedad, es posible que obtenga una respuesta inesperada y puede usar el resultado de seguimiento para ver la solicitud XML y la respuesta para identificar el error. La salida de seguimiento de la API administrada de EWS también puede ayudarle a compilar manualmente la solicitud XML para crear la aplicación de EWS. Si usa EWS, puede crear una pequeña aplicación con la API administrada de EWS, realizar un seguimiento y, a continuación, usar la información de solicitud XML para ayudarle a compilar la solicitud de EWS. 
  
## <a name="enabling-tracing-on-the-exchangeservice-object"></a>Habilitación del seguimiento en el objeto ExchangeService
<a name="bk_EnableTracing"> </a>

Para habilitar el seguimiento, cree un objeto [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) para la aplicación y establezca las propiedades de seguimiento como se muestra en el ejemplo siguiente. 
  
```cs
ExchangeService service = new ExchangeService(ExchangeVersion.Exchange2010);
service.TraceListener = ITraceListenerInstance;
// Optional flags to indicate the requests and responses to trace.
service.TraceFlags = TraceFlags.EwsRequest | TraceFlags.EwsResponse
service.TraceEnabled = true;

```

Después de establecer la propiedad [TraceEnabled](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.traceenabled%28v=exchg.80%29.aspx) en **true**, todas las solicitudes que coinciden con las marcas de seguimiento se enviarán al agente de escucha de seguimiento especificado. Puede especificar una sola marca de seguimiento o puede especificar varias marcas de seguimiento combinándolos con un operador lógico **or**. Puede usar la [enumeración TraceFlags](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.traceflags%28v=exchg.80%29.aspx) para especificar valores para EWS y para las respuestas y solicitudes de detección automática. 
  
## <a name="implementing-a-tracelistener-object"></a>Implementar un objeto TraceListener
<a name="bk_traceListener"> </a>

Puede establecer la propiedad [TraceEnabled](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.traceenabled%28v=exchg.80%29.aspx) en **true** para enviar las solicitudes y respuestas XML a la aplicación, como una ventana de consola. Si desea controlar el resultado del seguimiento y guardarlo en un archivo, le recomendamos que implemente un objeto de [clase TraceListener](https://msdn.microsoft.com/library/system.diagnostics.tracelistener.aspx) . En el ejemplo de código siguiente se muestra un objeto simple que implementa la interfaz [ITraceListener](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.itracelistener%28v=exchg.80%29.aspx) y almacena las solicitudes y respuestas a las que se realiza un seguimiento en archivos XML o de texto. 
  
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

## <a name="see-also"></a>Vea también

- [Empezar a usar los servicios web de Exchange](start-using-web-services-in-exchange.md)
- [Administrar los mensajes de error de detección automática](handling-autodiscover-error-messages.md)    
- [Hacer referencia al ensamblado de la API administrada de EWS](how-to-reference-the-ews-managed-api-assembly.md)    
- [Comunicarse con EWS mediante la API administrada de EWS](how-to-communicate-with-ews-by-using-the-ews-managed-api.md)
    

