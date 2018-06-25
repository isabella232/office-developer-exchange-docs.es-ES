---
title: Crear a un agente de transporte DeliveryAgent para Exchange 2013
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 4af904d7-b315-4849-92b1-66018f76ffdf
description: Encuentre información acerca de cómo crear un agente de transporte DeliveryAgent personalizado para usar con Exchange 2013.
ms.openlocfilehash: 44ee5dc465f4435f0b835d264331cb719fe875c1
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763347"
---
# <a name="create-a-deliveryagent-transport-agent-for-exchange-2013"></a><span data-ttu-id="ba130-103">Crear a un agente de transporte DeliveryAgent para Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="ba130-103">Create a DeliveryAgent transport agent for Exchange 2013</span></span>

<span data-ttu-id="ba130-104">Encuentre información acerca de cómo crear un agente de transporte DeliveryAgent personalizado para usar con Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="ba130-104">Find out how to create a custom DeliveryAgent transport agent to use with Exchange 2013.</span></span>
  
<span data-ttu-id="ba130-105">**Se aplica a:** Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="ba130-105">**Applies to:** Exchange Server 2013</span></span>
  
<span data-ttu-id="ba130-106">La [DeliveryAgentFactory\<Manager\> ](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Delivery.DeliveryAgentFactory`1.aspx) y las clases de [DeliveryAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.DeliveryType.DeliveryAgent.aspx) son las clases base para los agentes de transporte que están diseñadas para ejecutarse en el servicio de transporte en un servidor de buzones de Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="ba130-106">The [DeliveryAgentFactory\<Manager\>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Delivery.DeliveryAgentFactory`1.aspx) and [DeliveryAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.DeliveryType.DeliveryAgent.aspx) classes are the base classes for transport agents that are designed to run on the Transport service on an Exchange Server 2013 Mailbox server.</span></span> <span data-ttu-id="ba130-107">Es posible que implemente los controladores en el agente de transporte DeliveryAgent para los eventos proporcionados por la clase [DeliveryAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.DeliveryType.DeliveryAgent.aspx) que se enumeran en la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="ba130-107">You might implement handlers in your DeliveryAgent transport agent for the events provided by the [DeliveryAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.DeliveryType.DeliveryAgent.aspx) class that are listed in the following table.</span></span> 
  
<span data-ttu-id="ba130-108">**La tabla 1. Eventos de clase DeliveryAgent**</span><span class="sxs-lookup"><span data-stu-id="ba130-108">**Table 1. DeliveryAgent class events**</span></span>

|<span data-ttu-id="ba130-109">**Evento**</span><span class="sxs-lookup"><span data-stu-id="ba130-109">**Event**</span></span>|<span data-ttu-id="ba130-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ba130-110">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ba130-111">OnCloseConnection</span><span class="sxs-lookup"><span data-stu-id="ba130-111">OnCloseConnection</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Delivery.DeliveryAgent.OnCloseConnection.aspx) <br/> |<span data-ttu-id="ba130-112">Se produce después de que se ha entregado el último elemento de correo y se cierra la conexión.</span><span class="sxs-lookup"><span data-stu-id="ba130-112">Occurs after the last mail item has been delivered and the connection is closed.</span></span>  <br/> |
|[<span data-ttu-id="ba130-113">OnDeliverMailItem</span><span class="sxs-lookup"><span data-stu-id="ba130-113">OnDeliverMailItem</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Delivery.DeliveryAgent.OnDeliverMailItem.aspx) <br/> |<span data-ttu-id="ba130-114">Se produce cuando un elemento de correo está listo para entregar.</span><span class="sxs-lookup"><span data-stu-id="ba130-114">Occurs when a mail item is ready to be delivered.</span></span>  <br/> |
|[<span data-ttu-id="ba130-115">OnOpenConnection</span><span class="sxs-lookup"><span data-stu-id="ba130-115">OnOpenConnection</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Delivery.DeliveryAgent.OnOpenConnection.aspx) <br/> |<span data-ttu-id="ba130-116">Se produce cuando se abre el agente de entrega para la entrega de correo.</span><span class="sxs-lookup"><span data-stu-id="ba130-116">Occurs when the delivery agent is opened for mail delivery.</span></span>  <br/> |
   
## <a name="creating-a-custom-deliveryagent-transport-agent"></a><span data-ttu-id="ba130-117">Creación de un agente de transporte DeliveryAgent personalizado</span><span class="sxs-lookup"><span data-stu-id="ba130-117">Creating a custom DeliveryAgent transport agent</span></span>

<span data-ttu-id="ba130-118">El siguiente procedimiento describe cómo crear a un agente de transporte DeliveryAgent personalizado.</span><span class="sxs-lookup"><span data-stu-id="ba130-118">The following procedure describes how to create a custom DeliveryAgent transport agent.</span></span> 
  
### <a name="to-create-the-transport-agent"></a><span data-ttu-id="ba130-119">Para crear al agente de transporte</span><span class="sxs-lookup"><span data-stu-id="ba130-119">To create the transport agent</span></span>

1. <span data-ttu-id="ba130-120">Agregue referencias a los espacios de nombres.</span><span class="sxs-lookup"><span data-stu-id="ba130-120">Add references to the namespaces.</span></span>
    
   ```cs
        using Microsoft.Exchange.Data.Transport;
        using Microsoft.Exchange.Data.Transport.Delivery;
    
   ```

   <span data-ttu-id="ba130-121">Puede encontrar estos espacios de nombres en el servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="ba130-121">You can find these namespaces on your Exchange server.</span></span> <span data-ttu-id="ba130-122">Mediante la adición de una referencia a estos espacios de nombres, tendrá acceso a los miembros de [DeliveryAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.DeliveryType.DeliveryAgent.aspx) .</span><span class="sxs-lookup"><span data-stu-id="ba130-122">By adding a reference to these namespaces, you will have access to the [DeliveryAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.DeliveryType.DeliveryAgent.aspx) members.</span></span> 
    
2. <span data-ttu-id="ba130-123">Implementar la clase derivada de la [DeliveryAgentFactory\<Manager\> ](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Delivery.DeliveryAgentFactory`1.aspx) clase.</span><span class="sxs-lookup"><span data-stu-id="ba130-123">Implement the derived class for the [DeliveryAgentFactory\<Manager\>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Delivery.DeliveryAgentFactory`1.aspx) class.</span></span> 
    
   ```cs
      public class MyDeliveryAgentFactory : DeliveryAgentFactory<MyDeliveryAgentFactory.MyDeliveryAgentManager>
      {
          static MyDeliveryAgentFactory()
          {
          }
          public override DeliveryAgent CreateAgent(SmtpServer server)
          {
              return new MyDeliveryAgent(server);
          }
          public sealed class MyDeliveryAgentManager : DeliveryAgentManager
          {
              /// <summary>
              /// Gets the supported delivery protocol.
              /// </summary>
              public override string SupportedDeliveryProtocol
              {
                  get { return "MyProtocol"; }
              }
          }
      }
  
   ```

   <span data-ttu-id="ba130-124">Este código se cree una instancia de la clase derivada y reemplace el método **CreateAgent** para crear una instancia de su nuevo agente personalizado.</span><span class="sxs-lookup"><span data-stu-id="ba130-124">This code will instantiate the derived class and override the **CreateAgent** method to create an instance of your new custom agent.</span></span> <span data-ttu-id="ba130-125">Métodos adicionales, como **Close**, también pueden reemplazarse en esta clase para ejecutar código personalizado.</span><span class="sxs-lookup"><span data-stu-id="ba130-125">Additional methods, such as **Close**, can also be overridden in this class to execute custom code.</span></span> <span data-ttu-id="ba130-126">Se crea una clase [DeliveryAgentManager](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Delivery.DeliveryAgentManager.aspx) para invalidar la propiedad [SupportedDeliveryProtocol](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Delivery.DeliveryAgentManager.SupportedDeliveryProtocol.aspx) y establecer el protocolo que se va a usar el agente.</span><span class="sxs-lookup"><span data-stu-id="ba130-126">A [DeliveryAgentManager](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Delivery.DeliveryAgentManager.aspx) class is created to override the [SupportedDeliveryProtocol](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Delivery.DeliveryAgentManager.SupportedDeliveryProtocol.aspx) property and set the protocol your agent will use.</span></span> 
    
3. <span data-ttu-id="ba130-127">Definir al agente.</span><span class="sxs-lookup"><span data-stu-id="ba130-127">Define your agent.</span></span>
    
   ```cs
      public class MyDeliveryAgent : DeliveryAgent
      {
          public MyDeliveryAgent(SmtpServer server)
          {
              this.OnCloseConnection += CloseConnection;
              this.OnDeliverMailItem += DeliverMailItem;
              this.OnOpenConnection += OpenConnection;
          }
      }
  
   ```

   <span data-ttu-id="ba130-128">Después de definir la clase de agente, se puede agregar funcionalidad personalizada.</span><span class="sxs-lookup"><span data-stu-id="ba130-128">After you define your agent class, you can add you custom functionality.</span></span> <span data-ttu-id="ba130-129">En este ejemplo, los tres eventos, [OnCloseConnection](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Delivery.DeliveryAgent.OnCloseConnection.aspx) , [OnDeliverMailItem](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Delivery.DeliveryAgent.OnDeliverMailItem.aspx) y [OnOpenConnection](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Delivery.DeliveryAgent.OnOpenConnection.aspx) , se redirigen a sus controladores de eventos personalizados.</span><span class="sxs-lookup"><span data-stu-id="ba130-129">In this example, the three events, [OnCloseConnection](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Delivery.DeliveryAgent.OnCloseConnection.aspx) , [OnDeliverMailItem](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Delivery.DeliveryAgent.OnDeliverMailItem.aspx) and [OnOpenConnection](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Delivery.DeliveryAgent.OnOpenConnection.aspx) , are redirected to your custom event handlers.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="ba130-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="ba130-130">See also</span></span>

- [<span data-ttu-id="ba130-131">Conceptos de agente en Exchange 2013 de transporte</span><span class="sxs-lookup"><span data-stu-id="ba130-131">Transport agent concepts in Exchange 2013</span></span>](transport-agent-concepts-in-exchange-2013.md)
- [<span data-ttu-id="ba130-132">Referencia de agente de transporte de Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="ba130-132">Transport agent reference for Exchange 2013</span></span>](transport-agent-reference-for-exchange-2013.md)    
- [<span data-ttu-id="ba130-133">DeliveryAgentFactory\<Manager\></span><span class="sxs-lookup"><span data-stu-id="ba130-133">DeliveryAgentFactory\<Manager\></span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Delivery.DeliveryAgentFactory`1.aspx)   
- [<span data-ttu-id="ba130-134">DeliveryAgent</span><span class="sxs-lookup"><span data-stu-id="ba130-134">DeliveryAgent</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.DeliveryType.DeliveryAgent.aspx)    
- [<span data-ttu-id="ba130-135">DeliveryAgentManager</span><span class="sxs-lookup"><span data-stu-id="ba130-135">DeliveryAgentManager</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Delivery.DeliveryAgentManager.aspx)
    

