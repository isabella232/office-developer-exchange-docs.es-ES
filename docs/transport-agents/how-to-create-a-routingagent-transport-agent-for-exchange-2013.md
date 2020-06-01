---
title: Crear un agente de transporte de RoutingAgent para Exchange 2013
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3f0e745f-9289-4f31-8877-926692a8c133
description: Descubra cómo crear un agente de transporte de RoutingAgent personalizado para usarlo con Exchange 2013.
ms.openlocfilehash: 9acf30be0dd795098f757effaa34b2e72183b000
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463702"
---
# <a name="create-a-routingagent-transport-agent-for-exchange-2013"></a><span data-ttu-id="69ff1-103">Crear un agente de transporte de RoutingAgent para Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="69ff1-103">Create a RoutingAgent transport agent for Exchange 2013</span></span>

<span data-ttu-id="69ff1-104">Descubra cómo crear un agente de transporte de RoutingAgent personalizado para usarlo con Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="69ff1-104">Find out how to create a custom RoutingAgent transport agent to use with Exchange 2013.</span></span>
  
<span data-ttu-id="69ff1-105">**Se aplica a:** Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="69ff1-105">**Applies to:** Exchange Server 2013</span></span>
  
<span data-ttu-id="69ff1-106">Fragmentos de código y aplicaciones de ejemplo relacionados:</span><span class="sxs-lookup"><span data-stu-id="69ff1-106">Related code snippets and sample apps:</span></span>

- [<span data-ttu-id="69ff1-107">Exchange 2013: crear un agente de transporte de registro de ancho de banda</span><span class="sxs-lookup"><span data-stu-id="69ff1-107">Exchange 2013: Build a bandwidth logging transport agent</span></span>](https://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-a-d61a4aaa)
  
<span data-ttu-id="69ff1-108">Las clases [RoutingAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgentFactory.aspx) y [RoutingAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.aspx) son las clases base para los agentes de transporte que están diseñadas para ejecutarse en el servicio de transporte en un servidor de buzones de correo de Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="69ff1-108">The [RoutingAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgentFactory.aspx) and [RoutingAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.aspx) classes are the base classes for transport agents that are designed to run on the transport service on an Exchange Server 2013 Mailbox server.</span></span> <span data-ttu-id="69ff1-109">La clase [RoutingAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.aspx) proporciona los eventos enumerados en la siguiente tabla para los que puede implementar controladores en el agente de transporte RoutingAgent.</span><span class="sxs-lookup"><span data-stu-id="69ff1-109">The [RoutingAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.aspx) class provides the events listed in the following table for which you might implement handlers in your RoutingAgent transport agent.</span></span> 
  
<span data-ttu-id="69ff1-110">**Tabla 1. Eventos de la clase RoutingAgent**</span><span class="sxs-lookup"><span data-stu-id="69ff1-110">**Table 1. RoutingAgent class events**</span></span>

|<span data-ttu-id="69ff1-111">**Event**</span><span class="sxs-lookup"><span data-stu-id="69ff1-111">**Event**</span></span>|<span data-ttu-id="69ff1-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="69ff1-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="69ff1-113">OnCategorizedMessage</span><span class="sxs-lookup"><span data-stu-id="69ff1-113">OnCategorizedMessage</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnCategorizedMessage.aspx) <br/> |<span data-ttu-id="69ff1-114">Se produce después de que el servidor realice la conversión de contenido, si es necesario.</span><span class="sxs-lookup"><span data-stu-id="69ff1-114">Occurs after the server performs content conversion, if it is required.</span></span>  <br/> |
|[<span data-ttu-id="69ff1-115">OnResolvedMessage</span><span class="sxs-lookup"><span data-stu-id="69ff1-115">OnResolvedMessage</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnResolvedMessage.aspx) <br/> |<span data-ttu-id="69ff1-116">Se produce después de que se hayan resuelto todos los destinatarios del mensaje y antes de que se determine el enrutamiento.</span><span class="sxs-lookup"><span data-stu-id="69ff1-116">Occurs after all the recipients of the message have been resolved and before routing is determined.</span></span>  <br/> |
|[<span data-ttu-id="69ff1-117">OnRoutedMessage</span><span class="sxs-lookup"><span data-stu-id="69ff1-117">OnRoutedMessage</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnRoutedMessage.aspx) <br/> |<span data-ttu-id="69ff1-118">Se produce después de que el servidor enruta el mensaje al siguiente salto y realiza la conversión de contenido, si es necesario.</span><span class="sxs-lookup"><span data-stu-id="69ff1-118">Occurs after the server routes the message to the next hop and performs content conversion, if required.</span></span> <span data-ttu-id="69ff1-119">Es posible que el servidor use más recursos para procesar cada mensaje en el evento [OnRoutedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnRoutedMessage.aspx) que el evento [OnSubmittedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnSubmittedMessage.aspx) , ya que el servidor realizará la conversión de contenido necesaria y determinará el siguiente salto en la ruta del mensaje antes de ejecutar el código en el controlador de eventos [OnRoutedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnRoutedMessage.aspx) .</span><span class="sxs-lookup"><span data-stu-id="69ff1-119">The server might use more resources to process each message in the [OnRoutedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnRoutedMessage.aspx) event than the [OnSubmittedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnSubmittedMessage.aspx) event because the server will perform any necessary content conversion and determine the next hop in the route for the message before it executes the code in the [OnRoutedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnRoutedMessage.aspx) event handler.</span></span>  <br/> |
|[<span data-ttu-id="69ff1-120">OnSubmittedMessage</span><span class="sxs-lookup"><span data-stu-id="69ff1-120">OnSubmittedMessage</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnSubmittedMessage.aspx) <br/> |<span data-ttu-id="69ff1-121">Se produce después de que el mensaje se sale de la cola de envío.</span><span class="sxs-lookup"><span data-stu-id="69ff1-121">Occurs after the message is taken off the submit queue.</span></span> <span data-ttu-id="69ff1-122">Use el evento [OnSubmittedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnSubmittedMessage.aspx) si el agente de transporte RoutingAgent no requiere la conversión de contenido, los destinatarios resueltos o los datos de enrutamiento.</span><span class="sxs-lookup"><span data-stu-id="69ff1-122">Use the [OnSubmittedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnSubmittedMessage.aspx) event if your RoutingAgent transport agent does not require content conversion, resolved recipients, or routing data.</span></span>  <br/> |
   
## <a name="creating-a-custom-routingagent-transport-agent"></a><span data-ttu-id="69ff1-123">Creación de un agente de transporte de RoutingAgent personalizado</span><span class="sxs-lookup"><span data-stu-id="69ff1-123">Creating a custom RoutingAgent transport agent</span></span>

<span data-ttu-id="69ff1-124">El siguiente procedimiento describe cómo crear un agente de transporte de RoutingAgent personalizado.</span><span class="sxs-lookup"><span data-stu-id="69ff1-124">The following procedure describes how to create a custom RoutingAgent transport agent.</span></span> 
  
### <a name="to-create-the-transport-agent"></a><span data-ttu-id="69ff1-125">Para crear el agente de transporte</span><span class="sxs-lookup"><span data-stu-id="69ff1-125">To create the transport agent</span></span>

1. <span data-ttu-id="69ff1-126">Agregue referencias a los espacios de nombres.</span><span class="sxs-lookup"><span data-stu-id="69ff1-126">Add references to the namespaces.</span></span>
    
   ```cs
      using Microsoft.Exchange.Data.Mime;
      using Microsoft.Exchange.Data.Transport;
      using Microsoft.Exchange.Data.Transport.Routing;
  
   ```

   <span data-ttu-id="69ff1-127">Puede encontrar estos espacios de nombres en su servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="69ff1-127">You can find these namespaces on your Exchange server.</span></span> <span data-ttu-id="69ff1-128">Al agregar una referencia a estos espacios de nombres, tendrá acceso a los miembros de [RoutingAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.aspx) y a otras clases usadas en el ejemplo [Exchange 2013: Build a Bandwidth Logging Transport Agent](https://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-a-d61a4aaa) .</span><span class="sxs-lookup"><span data-stu-id="69ff1-128">By adding a reference to these namespaces, you will have access to the [RoutingAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.aspx) members as well as other classes used in the [Exchange 2013: Build a bandwidth logging transport agent](https://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-a-d61a4aaa) sample.</span></span> 
    
2. <span data-ttu-id="69ff1-129">Implemente la clase derivada para la clase [RoutingAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgentFactory.aspx) .</span><span class="sxs-lookup"><span data-stu-id="69ff1-129">Implement the derived class for the [RoutingAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgentFactory.aspx) class.</span></span> 
    
   ```cs
      public class BandwidthLoggerFactory : RoutingAgentFactory
      {
          public override RoutingAgent CreateAgent(SmtpServer server)
          {
              return new BandwidthLogger(server);
          }
      }
  
   ```

   <span data-ttu-id="69ff1-130">Este código creará una instancia de la clase derivada y reemplazará el método **CreateAgent** para crear una instancia del nuevo agente personalizado.</span><span class="sxs-lookup"><span data-stu-id="69ff1-130">This code will instantiate the derived class and override the **CreateAgent** method to create an instance of your new custom agent.</span></span> <span data-ttu-id="69ff1-131">Los métodos adicionales, como **Close**, también se pueden invalidar en esta clase para ejecutar código personalizado.</span><span class="sxs-lookup"><span data-stu-id="69ff1-131">Additional methods, such as **Close**, can also be overridden in this class to execute custom code.</span></span> 
    
3. <span data-ttu-id="69ff1-132">Definir el agente.</span><span class="sxs-lookup"><span data-stu-id="69ff1-132">Define your agent.</span></span>
    
   ```cs
      public class BandwidthLogger : RoutingAgent
      {
          // Your custom code goes here
          public BandwidthLogger(SmtpServer server)
          {
              Debug.WriteLine(logPrefix + "Agent constructor");
              this.server = server;
              this.OnSubmittedMessage += SubmittedMessage;
              this.OnRoutedMessage += RoutedMessage;
          }
      }
  
   ```

   <span data-ttu-id="69ff1-133">Después de definir la clase del agente, puede Agregar una funcionalidad personalizada.</span><span class="sxs-lookup"><span data-stu-id="69ff1-133">After you define your agent class, you can add you custom functionality.</span></span> <span data-ttu-id="69ff1-134">En este ejemplo, los dos eventos [OnSubmittedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnSubmittedMessage.aspx) y [OnRoutedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnRoutedMessage.aspx)se redirigen a los controladores de eventos personalizados.</span><span class="sxs-lookup"><span data-stu-id="69ff1-134">In this example, the two events [OnSubmittedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnSubmittedMessage.aspx) and [OnRoutedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnRoutedMessage.aspx)are redirected to your custom event handlers.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="69ff1-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="69ff1-135">See also</span></span>

- [<span data-ttu-id="69ff1-136">Conceptos del agente de transporte en Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="69ff1-136">Transport agent concepts in Exchange 2013</span></span>](transport-agent-concepts-in-exchange-2013.md)    
- [<span data-ttu-id="69ff1-137">Referencia del agente de transporte para Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="69ff1-137">Transport agent reference for Exchange 2013</span></span>](transport-agent-reference-for-exchange-2013.md)    
- [<span data-ttu-id="69ff1-138">RoutingAgentFactory</span><span class="sxs-lookup"><span data-stu-id="69ff1-138">RoutingAgentFactory</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgentFactory.aspx)    
- [<span data-ttu-id="69ff1-139">RoutingAgent</span><span class="sxs-lookup"><span data-stu-id="69ff1-139">RoutingAgent</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.aspx)
    

