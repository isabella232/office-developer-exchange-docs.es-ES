---
title: Crear un agente de transporte de DeliveryAgent para Exchange 2013
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 4af904d7-b315-4849-92b1-66018f76ffdf
description: Descubra cómo crear un agente de transporte de DeliveryAgent personalizado para usarlo con Exchange 2013.
ms.openlocfilehash: b349f0b6d835ba3d6195b43e80d1dcd21750bf82
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44527575"
---
# <a name="create-a-deliveryagent-transport-agent-for-exchange-2013"></a><span data-ttu-id="c5d3c-103">Crear un agente de transporte de DeliveryAgent para Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="c5d3c-103">Create a DeliveryAgent transport agent for Exchange 2013</span></span>

<span data-ttu-id="c5d3c-104">Descubra cómo crear un agente de transporte de DeliveryAgent personalizado para usarlo con Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="c5d3c-104">Find out how to create a custom DeliveryAgent transport agent to use with Exchange 2013.</span></span>
  
<span data-ttu-id="c5d3c-105">**Se aplica a:** Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="c5d3c-105">**Applies to:** Exchange Server 2013</span></span>
  
<span data-ttu-id="c5d3c-106">Las [clases \<Manager\> DeliveryAgentFactory](https://msdn.microsoft.com/library/dd877550(v=exchg.150).aspx) y [DeliveryAgent](https://msdn.microsoft.com/library/microsoft.exchange.data.transport.delivery.deliveryagent(v=exchg.150).aspx) son las clases base para los agentes de transporte que están diseñadas para ejecutarse en el servicio de transporte en un servidor de buzones de correo de Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="c5d3c-106">The [DeliveryAgentFactory\<Manager\>](https://msdn.microsoft.com/library/dd877550(v=exchg.150).aspx) and [DeliveryAgent](https://msdn.microsoft.com/library/microsoft.exchange.data.transport.delivery.deliveryagent(v=exchg.150).aspx) classes are the base classes for transport agents that are designed to run on the Transport service on an Exchange Server 2013 Mailbox server.</span></span> <span data-ttu-id="c5d3c-107">Puede implementar controladores en el agente de transporte de DeliveryAgent para los eventos proporcionados por la clase [DeliveryAgent](https://msdn.microsoft.com/library/microsoft.exchange.data.transport.delivery.deliveryagent(v=exchg.150).aspx) que se enumeran en la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="c5d3c-107">You might implement handlers in your DeliveryAgent transport agent for the events provided by the [DeliveryAgent](https://msdn.microsoft.com/library/microsoft.exchange.data.transport.delivery.deliveryagent(v=exchg.150).aspx) class that are listed in the following table.</span></span> 
  
<span data-ttu-id="c5d3c-108">**Tabla 1. Eventos de la clase DeliveryAgent**</span><span class="sxs-lookup"><span data-stu-id="c5d3c-108">**Table 1. DeliveryAgent class events**</span></span>

|<span data-ttu-id="c5d3c-109">**Event**</span><span class="sxs-lookup"><span data-stu-id="c5d3c-109">**Event**</span></span>|<span data-ttu-id="c5d3c-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c5d3c-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c5d3c-111">[OnCloseConnection](https://msdn.microsoft.com/library/microsoft.exchange.data.transport.delivery.deliveryagent.oncloseconnection(v=exchg.150).aspx)</span><span class="sxs-lookup"><span data-stu-id="c5d3c-111">[OnCloseConnection](https://msdn.microsoft.com/library/microsoft.exchange.data.transport.delivery.deliveryagent.oncloseconnection(v=exchg.150).aspx)</span></span> <br/> |<span data-ttu-id="c5d3c-112">Se produce después de que se haya entregado el último elemento de correo y se haya cerrado la conexión.</span><span class="sxs-lookup"><span data-stu-id="c5d3c-112">Occurs after the last mail item has been delivered and the connection is closed.</span></span>  <br/> |
|<span data-ttu-id="c5d3c-113">[OnDeliverMailItem](https://msdn.microsoft.com/library/microsoft.exchange.data.transport.delivery.deliveryagent.ondelivermailitem(v=exchg.150).aspx)</span><span class="sxs-lookup"><span data-stu-id="c5d3c-113">[OnDeliverMailItem](https://msdn.microsoft.com/library/microsoft.exchange.data.transport.delivery.deliveryagent.ondelivermailitem(v=exchg.150).aspx)</span></span> <br/> |<span data-ttu-id="c5d3c-114">Se produce cuando un elemento de correo está listo para su entrega.</span><span class="sxs-lookup"><span data-stu-id="c5d3c-114">Occurs when a mail item is ready to be delivered.</span></span>  <br/> |
|<span data-ttu-id="c5d3c-115">[OnOpenConnection](https://msdn.microsoft.com/library/microsoft.exchange.data.transport.delivery.deliveryagent.onopenconnection(v=exchg.150).aspx)</span><span class="sxs-lookup"><span data-stu-id="c5d3c-115">[OnOpenConnection](https://msdn.microsoft.com/library/microsoft.exchange.data.transport.delivery.deliveryagent.onopenconnection(v=exchg.150).aspx)</span></span> <br/> |<span data-ttu-id="c5d3c-116">Se produce cuando el agente de entrega se abre para la entrega de correo.</span><span class="sxs-lookup"><span data-stu-id="c5d3c-116">Occurs when the delivery agent is opened for mail delivery.</span></span>  <br/> |
   
## <a name="creating-a-custom-deliveryagent-transport-agent"></a><span data-ttu-id="c5d3c-117">Creación de un agente de transporte de DeliveryAgent personalizado</span><span class="sxs-lookup"><span data-stu-id="c5d3c-117">Creating a custom DeliveryAgent transport agent</span></span>

<span data-ttu-id="c5d3c-118">El siguiente procedimiento describe cómo crear un agente de transporte de DeliveryAgent personalizado.</span><span class="sxs-lookup"><span data-stu-id="c5d3c-118">The following procedure describes how to create a custom DeliveryAgent transport agent.</span></span> 
  
### <a name="to-create-the-transport-agent"></a><span data-ttu-id="c5d3c-119">Para crear el agente de transporte</span><span class="sxs-lookup"><span data-stu-id="c5d3c-119">To create the transport agent</span></span>

1. <span data-ttu-id="c5d3c-120">Agregue referencias a los espacios de nombres.</span><span class="sxs-lookup"><span data-stu-id="c5d3c-120">Add references to the namespaces.</span></span>
    
   ```cs
        using Microsoft.Exchange.Data.Transport;
        using Microsoft.Exchange.Data.Transport.Delivery;
    
   ```

   <span data-ttu-id="c5d3c-121">Puede encontrar estos espacios de nombres en su servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="c5d3c-121">You can find these namespaces on your Exchange server.</span></span> <span data-ttu-id="c5d3c-122">Al agregar una referencia a estos espacios de nombres, tendrá acceso a los miembros de [DeliveryAgent](https://msdn.microsoft.com/library/microsoft.exchange.data.transport.delivery.deliveryagent(v=exchg.150).aspx) .</span><span class="sxs-lookup"><span data-stu-id="c5d3c-122">By adding a reference to these namespaces, you will have access to the [DeliveryAgent](https://msdn.microsoft.com/library/microsoft.exchange.data.transport.delivery.deliveryagent(v=exchg.150).aspx) members.</span></span> 
    
2. <span data-ttu-id="c5d3c-123">Implemente la clase derivada para la clase [DeliveryAgentFactory \<Manager\> ](https://msdn.microsoft.com/library/dd877550(v=exchg.150).aspx) .</span><span class="sxs-lookup"><span data-stu-id="c5d3c-123">Implement the derived class for the [DeliveryAgentFactory\<Manager\>](https://msdn.microsoft.com/library/dd877550(v=exchg.150).aspx) class.</span></span> 
    
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

   <span data-ttu-id="c5d3c-124">Este código creará una instancia de la clase derivada y reemplazará el método **CreateAgent** para crear una instancia del nuevo agente personalizado.</span><span class="sxs-lookup"><span data-stu-id="c5d3c-124">This code will instantiate the derived class and override the **CreateAgent** method to create an instance of your new custom agent.</span></span> <span data-ttu-id="c5d3c-125">Los métodos adicionales, como **Close**, también se pueden invalidar en esta clase para ejecutar código personalizado.</span><span class="sxs-lookup"><span data-stu-id="c5d3c-125">Additional methods, such as **Close**, can also be overridden in this class to execute custom code.</span></span> <span data-ttu-id="c5d3c-126">Se crea una clase [DeliveryAgentManager](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Delivery.DeliveryAgentManager.aspx) para invalidar la propiedad [SupportedDeliveryProtocol](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Delivery.DeliveryAgentManager.SupportedDeliveryProtocol.aspx) y establecer el protocolo que usará el agente.</span><span class="sxs-lookup"><span data-stu-id="c5d3c-126">A [DeliveryAgentManager](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Delivery.DeliveryAgentManager.aspx) class is created to override the [SupportedDeliveryProtocol](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Delivery.DeliveryAgentManager.SupportedDeliveryProtocol.aspx) property and set the protocol your agent will use.</span></span> 
    
3. <span data-ttu-id="c5d3c-127">Definir el agente.</span><span class="sxs-lookup"><span data-stu-id="c5d3c-127">Define your agent.</span></span>
    
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

   <span data-ttu-id="c5d3c-128">Después de definir la clase del agente, puede Agregar una funcionalidad personalizada.</span><span class="sxs-lookup"><span data-stu-id="c5d3c-128">After you define your agent class, you can add you custom functionality.</span></span> <span data-ttu-id="c5d3c-129">En este ejemplo, los tres eventos, [OnCloseConnection](https://msdn.microsoft.com/library/microsoft.exchange.data.transport.delivery.deliveryagent.oncloseconnection(v=exchg.150).aspx), [OnDeliverMailItem](https://msdn.microsoft.com/library/microsoft.exchange.data.transport.delivery.deliveryagent.ondelivermailitem(v=exchg.150).aspx)y [OnOpenConnection](https://msdn.microsoft.com/library/microsoft.exchange.data.transport.delivery.deliveryagent.onopenconnection(v=exchg.150).aspx), se redirigen a los controladores de eventos personalizados.</span><span class="sxs-lookup"><span data-stu-id="c5d3c-129">In this example, the three events, [OnCloseConnection](https://msdn.microsoft.com/library/microsoft.exchange.data.transport.delivery.deliveryagent.oncloseconnection(v=exchg.150).aspx), [OnDeliverMailItem](https://msdn.microsoft.com/library/microsoft.exchange.data.transport.delivery.deliveryagent.ondelivermailitem(v=exchg.150).aspx), and [OnOpenConnection](https://msdn.microsoft.com/library/microsoft.exchange.data.transport.delivery.deliveryagent.onopenconnection(v=exchg.150).aspx), are redirected to your custom event handlers.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="c5d3c-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="c5d3c-130">See also</span></span>

- [<span data-ttu-id="c5d3c-131">Conceptos del agente de transporte en Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="c5d3c-131">Transport agent concepts in Exchange 2013</span></span>](transport-agent-concepts-in-exchange-2013.md)
- [<span data-ttu-id="c5d3c-132">Referencia del agente de transporte para Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="c5d3c-132">Transport agent reference for Exchange 2013</span></span>](transport-agent-reference-for-exchange-2013.md)          

 