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
# <a name="trace-requests-and-responses-to-troubleshoot-ews-managed-api-apps"></a><span data-ttu-id="10e4e-103">Seguimiento de solicitudes y respuestas para solucionar problemas de aplicaciones de la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="10e4e-103">Trace requests and responses to troubleshoot EWS Managed API apps</span></span>

<span data-ttu-id="10e4e-104">Descubra cómo realizar un seguimiento de las solicitudes y respuestas de EWS para solucionar errores en la aplicación de la API administrada de EWS.</span><span class="sxs-lookup"><span data-stu-id="10e4e-104">Find out how to trace EWS requests and responses to troubleshoot errors in your EWS Managed API application.</span></span>
  
<span data-ttu-id="10e4e-105">La depuración de una aplicación basada en el servicio web puede resultar difícil porque parte del procesamiento se realiza en un equipo remoto al que puede que no tenga acceso.</span><span class="sxs-lookup"><span data-stu-id="10e4e-105">Debugging a web service-based application can be difficult because part of the processing is performed on a remote computer that you might not have access to.</span></span> <span data-ttu-id="10e4e-106">Como no puede recorrer el código en el servidor, puede resultar útil ver las solicitudes y respuestas XML que se envían entre el cliente y el servidor para determinar qué parte de la aplicación está causando un error.</span><span class="sxs-lookup"><span data-stu-id="10e4e-106">Because you cannot step through the code on the server, it can be helpful to see the XML requests and responses that are sent between the client and the server to determine which part of the application is causing an error.</span></span> 
  
<span data-ttu-id="10e4e-107">Si está usando EWS, ya tiene acceso a la solicitud y respuesta XML; puede colocar un punto de interrupción en el código para revisar la respuesta del servidor a su solicitud a fin de solucionar un problema.</span><span class="sxs-lookup"><span data-stu-id="10e4e-107">If you are using EWS, you already have access to the XML request and response; you can put a break point in your code to review the server's response to your request in order to troubleshoot an issue.</span></span> <span data-ttu-id="10e4e-108">Si está usando la API administrada de EWS, no tiene acceso directo a la solicitud y respuesta de EWS.</span><span class="sxs-lookup"><span data-stu-id="10e4e-108">If you're using the EWS Managed API, you don't have direct access to the EWS request and response.</span></span> <span data-ttu-id="10e4e-109">Sin embargo, puede usar métodos de seguimiento en el objeto [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) para capturar la solicitud XML y la respuesta y, a continuación, puede usar el XML para determinar por qué el código no funciona.</span><span class="sxs-lookup"><span data-stu-id="10e4e-109">However, you can use tracing methods on the [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object to capture the XML request and response, and you can then use the XML to determine why your code is not working.</span></span> 

<span data-ttu-id="10e4e-110">Por ejemplo, si no estableció correctamente una propiedad, es posible que obtenga una respuesta inesperada y puede usar el resultado de seguimiento para ver la solicitud XML y la respuesta para identificar el error.</span><span class="sxs-lookup"><span data-stu-id="10e4e-110">For example, if you did not set a property correctly, you might get an unexpected response, and you can use the trace output to look at the XML request and response to identify the error.</span></span> <span data-ttu-id="10e4e-111">La salida de seguimiento de la API administrada de EWS también puede ayudarle a compilar manualmente la solicitud XML para crear la aplicación de EWS.</span><span class="sxs-lookup"><span data-stu-id="10e4e-111">The trace output from the EWS Managed API can also help you manually build the XML request to create your EWS application.</span></span> <span data-ttu-id="10e4e-112">Si usa EWS, puede crear una pequeña aplicación con la API administrada de EWS, realizar un seguimiento y, a continuación, usar la información de solicitud XML para ayudarle a compilar la solicitud de EWS.</span><span class="sxs-lookup"><span data-stu-id="10e4e-112">If you are using EWS, you can create a small application by using EWS Managed API, trace it, and then use the XML request information to help you build your EWS request.</span></span> 
  
## <a name="enabling-tracing-on-the-exchangeservice-object"></a><span data-ttu-id="10e4e-113">Habilitación del seguimiento en el objeto ExchangeService</span><span class="sxs-lookup"><span data-stu-id="10e4e-113">Enabling tracing on the ExchangeService object</span></span>
<span data-ttu-id="10e4e-114"><a name="bk_EnableTracing"> </a></span><span class="sxs-lookup"><span data-stu-id="10e4e-114"><a name="bk_EnableTracing"> </a></span></span>

<span data-ttu-id="10e4e-115">Para habilitar el seguimiento, cree un objeto [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) para la aplicación y establezca las propiedades de seguimiento como se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="10e4e-115">To enable tracing, create an [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object for your application, and set the tracing properties as shown in the following example.</span></span> 
  
```cs
ExchangeService service = new ExchangeService(ExchangeVersion.Exchange2010);
service.TraceListener = ITraceListenerInstance;
// Optional flags to indicate the requests and responses to trace.
service.TraceFlags = TraceFlags.EwsRequest | TraceFlags.EwsResponse
service.TraceEnabled = true;

```

<span data-ttu-id="10e4e-116">Después de establecer la propiedad [TraceEnabled](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.traceenabled%28v=exchg.80%29.aspx) en **true**, todas las solicitudes que coinciden con las marcas de seguimiento se enviarán al agente de escucha de seguimiento especificado.</span><span class="sxs-lookup"><span data-stu-id="10e4e-116">After you set the [TraceEnabled](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.traceenabled%28v=exchg.80%29.aspx) property to **true**, all requests that match the trace flags will be sent to the specified trace listener.</span></span> <span data-ttu-id="10e4e-117">Puede especificar una sola marca de seguimiento o puede especificar varias marcas de seguimiento combinándolos con un operador lógico **or**.</span><span class="sxs-lookup"><span data-stu-id="10e4e-117">You can specify a single trace flag, or you can specify multiple trace flags by combining them with a logical **OR**.</span></span> <span data-ttu-id="10e4e-118">Puede usar la [enumeración TraceFlags](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.traceflags%28v=exchg.80%29.aspx) para especificar valores para EWS y para las respuestas y solicitudes de detección automática.</span><span class="sxs-lookup"><span data-stu-id="10e4e-118">You can use the [TraceFlags enumeration](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.traceflags%28v=exchg.80%29.aspx) to specify values for EWS and for Autodiscover requests and responses.</span></span> 
  
## <a name="implementing-a-tracelistener-object"></a><span data-ttu-id="10e4e-119">Implementar un objeto TraceListener</span><span class="sxs-lookup"><span data-stu-id="10e4e-119">Implementing a TraceListener object</span></span>
<span data-ttu-id="10e4e-120"><a name="bk_traceListener"> </a></span><span class="sxs-lookup"><span data-stu-id="10e4e-120"><a name="bk_traceListener"> </a></span></span>

<span data-ttu-id="10e4e-121">Puede establecer la propiedad [TraceEnabled](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.traceenabled%28v=exchg.80%29.aspx) en **true** para enviar las solicitudes y respuestas XML a la aplicación, como una ventana de consola.</span><span class="sxs-lookup"><span data-stu-id="10e4e-121">You can set the [TraceEnabled](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.traceenabled%28v=exchg.80%29.aspx) property to **true** to output the XML requests and responses to your application, such as a console window.</span></span> <span data-ttu-id="10e4e-122">Si desea controlar el resultado del seguimiento y guardarlo en un archivo, le recomendamos que implemente un objeto de [clase TraceListener](https://msdn.microsoft.com/library/system.diagnostics.tracelistener.aspx) .</span><span class="sxs-lookup"><span data-stu-id="10e4e-122">If you want to control the trace output and save it to a file, we recommend that you implement a [TraceListener class](https://msdn.microsoft.com/library/system.diagnostics.tracelistener.aspx) object.</span></span> <span data-ttu-id="10e4e-123">En el ejemplo de código siguiente se muestra un objeto simple que implementa la interfaz [ITraceListener](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.itracelistener%28v=exchg.80%29.aspx) y almacena las solicitudes y respuestas a las que se realiza un seguimiento en archivos XML o de texto.</span><span class="sxs-lookup"><span data-stu-id="10e4e-123">The following code example shows a simple object that implements the [ITraceListener](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.itracelistener%28v=exchg.80%29.aspx) interface and stores the traced requests and responses in XML or text files.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="10e4e-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="10e4e-124">See also</span></span>

- [<span data-ttu-id="10e4e-125">Empezar a usar los servicios web de Exchange</span><span class="sxs-lookup"><span data-stu-id="10e4e-125">Start using web services in Exchange</span></span>](start-using-web-services-in-exchange.md)
- [<span data-ttu-id="10e4e-126">Administrar los mensajes de error de detección automática</span><span class="sxs-lookup"><span data-stu-id="10e4e-126">Handling Autodiscover error messages</span></span>](handling-autodiscover-error-messages.md)    
- [<span data-ttu-id="10e4e-127">Hacer referencia al ensamblado de la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="10e4e-127">Reference the EWS Managed API assembly</span></span>](how-to-reference-the-ews-managed-api-assembly.md)    
- [<span data-ttu-id="10e4e-128">Comunicarse con EWS mediante la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="10e4e-128">Communicate with EWS by using the EWS Managed API</span></span>](how-to-communicate-with-ews-by-using-the-ews-managed-api.md)
    

