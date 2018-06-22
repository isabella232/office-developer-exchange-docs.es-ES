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
# <a name="trace-requests-and-responses-to-troubleshoot-ews-managed-api-apps"></a><span data-ttu-id="3f6f9-103">Seguimiento de las solicitudes y respuestas para solucionar problemas de aplicaciones de la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="3f6f9-103">Trace requests and responses to troubleshoot EWS Managed API apps</span></span>

<span data-ttu-id="3f6f9-104">Descubra cómo realizar un seguimiento de las solicitudes EWS y respuestas para solucionar problemas de errores en una aplicación de API administrada de EWS.</span><span class="sxs-lookup"><span data-stu-id="3f6f9-104">Find out how to trace EWS requests and responses to troubleshoot errors in your EWS Managed API application.</span></span>
  
<span data-ttu-id="3f6f9-105">Depurar una aplicación de servicio web puede resultar difícil debido a que parte del procesamiento se realiza en un equipo remoto que no puede tener acceso a.</span><span class="sxs-lookup"><span data-stu-id="3f6f9-105">Debugging a web service-based application can be difficult because part of the processing is performed on a remote computer that you might not have access to.</span></span> <span data-ttu-id="3f6f9-106">Debido a que no se puede recorrer el código en el servidor, puede ser útil ver las solicitudes XML y las respuestas que se envían entre el cliente y el servidor para determinar qué parte de la aplicación está provocando un error.</span><span class="sxs-lookup"><span data-stu-id="3f6f9-106">Because you cannot step through the code on the server, it can be helpful to see the XML requests and responses that are sent between the client and the server to determine which part of the application is causing an error.</span></span> 
  
<span data-ttu-id="3f6f9-107">Si usa EWS, ya tiene acceso a la solicitud XML y la respuesta; puede colocar un punto de interrupción en el código para revisar la respuesta del servidor a la solicitud con el fin de solucionar un problema.</span><span class="sxs-lookup"><span data-stu-id="3f6f9-107">If you are using EWS, you already have access to the XML request and response; you can put a break point in your code to review the server's response to your request in order to troubleshoot an issue.</span></span> <span data-ttu-id="3f6f9-108">Si se usa la API administrada de EWS, no tiene acceso directo a la solicitud EWS y la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3f6f9-108">If you're using the EWS Managed API, you don't have direct access to the EWS request and response.</span></span> <span data-ttu-id="3f6f9-109">Sin embargo, puede usar los métodos de seguimiento en el objeto [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) para capturar la solicitud XML y la respuesta y, a continuación, puede usar el código XML para determinar por qué no funciona el código.</span><span class="sxs-lookup"><span data-stu-id="3f6f9-109">However, you can use tracing methods on the [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object to capture the XML request and response, and you can then use the XML to determine why your code is not working.</span></span> 

<span data-ttu-id="3f6f9-110">Por ejemplo, si no ha definido una propiedad correctamente, es posible que obtenga una respuesta inesperada, y puede utilizar los resultados de seguimiento para buscar en la solicitud XML y la respuesta para identificar el error.</span><span class="sxs-lookup"><span data-stu-id="3f6f9-110">For example, if you did not set a property correctly, you might get an unexpected response, and you can use the trace output to look at the XML request and response to identify the error.</span></span> <span data-ttu-id="3f6f9-111">Los resultados del seguimiento de la API administrada de EWS también pueden ayudar a crear manualmente la solicitud XML para crear la aplicación de EWS.</span><span class="sxs-lookup"><span data-stu-id="3f6f9-111">The trace output from the EWS Managed API can also help you manually build the XML request to create your EWS application.</span></span> <span data-ttu-id="3f6f9-112">Si usa EWS, puede crear una aplicación pequeña mediante el uso de API administrada de EWS, seguimiento de él y, a continuación, use la información de la solicitud XML que le ayudarán a crear la solicitud EWS.</span><span class="sxs-lookup"><span data-stu-id="3f6f9-112">If you are using EWS, you can create a small application by using EWS Managed API, trace it, and then use the XML request information to help you build your EWS request.</span></span> 
  
## <a name="enabling-tracing-on-the-exchangeservice-object"></a><span data-ttu-id="3f6f9-113">Al habilitar el seguimiento en el objeto ExchangeService</span><span class="sxs-lookup"><span data-stu-id="3f6f9-113">Enabling tracing on the ExchangeService object</span></span>
<span data-ttu-id="3f6f9-114"><a name="bk_EnableTracing"> </a></span><span class="sxs-lookup"><span data-stu-id="3f6f9-114"></span></span>

<span data-ttu-id="3f6f9-115">Para habilitar el seguimiento, cree un objeto [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) para la aplicación y establecer las propiedades de seguimiento tal como se muestra en el siguiente ejemplo.</span><span class="sxs-lookup"><span data-stu-id="3f6f9-115">To enable tracing, create an [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object for your application, and set the tracing properties as shown in the following example.</span></span> 
  
```cs
ExchangeService service = new ExchangeService(ExchangeVersion.Exchange2010);
service.TraceListener = ITraceListenerInstance;
// Optional flags to indicate the requests and responses to trace.
service.TraceFlags = TraceFlags.EwsRequest | TraceFlags.EwsResponse
service.TraceEnabled = true;

```

<span data-ttu-id="3f6f9-116">Después de establecer la propiedad [TraceEnabled](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservicebase.traceenabled%28v=exchg.80%29.aspx) en **true**, se enviarán todas las solicitudes que coinciden con los marcadores de seguimiento en el agente de escucha de seguimiento especificado.</span><span class="sxs-lookup"><span data-stu-id="3f6f9-116">After you set the [TraceEnabled](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservicebase.traceenabled%28v=exchg.80%29.aspx) property to **true**, all requests that match the trace flags will be sent to the specified trace listener.</span></span> <span data-ttu-id="3f6f9-117">Puede especificar una marca de seguimiento único, o puede especificar varios indicadores de traza mediante la combinación de ellas con un operador lógico **OR**.</span><span class="sxs-lookup"><span data-stu-id="3f6f9-117">You can specify a single trace flag, or you can specify multiple trace flags by combining them with a logical **OR**.</span></span> <span data-ttu-id="3f6f9-118">Puede usar la [enumeración TraceFlags](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.traceflags%28v=exchg.80%29.aspx) para especificar valores para EWS y para las respuestas y solicitudes de detección automática.</span><span class="sxs-lookup"><span data-stu-id="3f6f9-118">You can use the [TraceFlags enumeration](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.traceflags%28v=exchg.80%29.aspx) to specify values for EWS and for Autodiscover requests and responses.</span></span> 
  
## <a name="implementing-a-tracelistener-object"></a><span data-ttu-id="3f6f9-119">Implementación de un objeto TraceListener</span><span class="sxs-lookup"><span data-stu-id="3f6f9-119">Implementing a TraceListener object</span></span>
<span data-ttu-id="3f6f9-120"><a name="bk_traceListener"> </a></span><span class="sxs-lookup"><span data-stu-id="3f6f9-120"></span></span>

<span data-ttu-id="3f6f9-121">Puede establecer la propiedad [TraceEnabled](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservicebase.traceenabled%28v=exchg.80%29.aspx) en **true** para las solicitudes XML y las respuestas a la aplicación, como una ventana de la consola de salida.</span><span class="sxs-lookup"><span data-stu-id="3f6f9-121">You can set the [TraceEnabled](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservicebase.traceenabled%28v=exchg.80%29.aspx) property to **true** to output the XML requests and responses to your application, such as a console window.</span></span> <span data-ttu-id="3f6f9-122">Si desea controlar los resultados del seguimiento y guárdelo en un archivo, se recomienda que implemente un objeto [TraceListener (clase)](http://msdn.microsoft.com/en-us/library/system.diagnostics.tracelistener.aspx) .</span><span class="sxs-lookup"><span data-stu-id="3f6f9-122">If you want to control the trace output and save it to a file, we recommend that you implement a [TraceListener class](http://msdn.microsoft.com/en-us/library/system.diagnostics.tracelistener.aspx) object.</span></span> <span data-ttu-id="3f6f9-123">En el ejemplo de código siguiente se muestra un objeto simple que implementa la interfaz [ITraceListener](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.itracelistener%28v=exchg.80%29.aspx) y almacena el seguimiento de las solicitudes y respuestas en archivos XML o de texto.</span><span class="sxs-lookup"><span data-stu-id="3f6f9-123">The following code example shows a simple object that implements the [ITraceListener](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.itracelistener%28v=exchg.80%29.aspx) interface and stores the traced requests and responses in XML or text files.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="3f6f9-124">Ver también</span><span class="sxs-lookup"><span data-stu-id="3f6f9-124">See also</span></span>

- [<span data-ttu-id="3f6f9-125">Empezar a utilizar servicios web de Exchange</span><span class="sxs-lookup"><span data-stu-id="3f6f9-125">Start using web services in Exchange</span></span>](start-using-web-services-in-exchange.md)
- [<span data-ttu-id="3f6f9-126">Administrar los mensajes de error de detección automática</span><span class="sxs-lookup"><span data-stu-id="3f6f9-126">Handling Autodiscover error messages</span></span>](handling-autodiscover-error-messages.md)    
- [<span data-ttu-id="3f6f9-127">Hacer referencia al ensamblado de la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="3f6f9-127">Reference the EWS Managed API assembly</span></span>](how-to-reference-the-ews-managed-api-assembly.md)    
- [<span data-ttu-id="3f6f9-128">Comunicarse con EWS mediante el uso de la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="3f6f9-128">Communicate with EWS by using the EWS Managed API</span></span>](how-to-communicate-with-ews-by-using-the-ews-managed-api.md)
    

