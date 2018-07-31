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
ms.openlocfilehash: bc36c7b5e0fb8006c5927d423d7767dcc7382ce0
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/28/2018
ms.locfileid: "21353311"
---
# <a name="create-a-deliveryagent-transport-agent-for-exchange-2013"></a>Crear a un agente de transporte DeliveryAgent para Exchange 2013

Encuentre información acerca de cómo crear un agente de transporte DeliveryAgent personalizado para usar con Exchange 2013.
  
**Se aplica a:** Exchange Server 2013
  
La [DeliveryAgentFactory\<Manager\> ](https://msdn.microsoft.com/en-us/library/dd877550(v=exchg.150).aspx) y las clases de [DeliveryAgent](https://msdn.microsoft.com/en-us/library/microsoft.exchange.data.transport.delivery.deliveryagent(v=exchg.150).aspx) son las clases base para los agentes de transporte que están diseñadas para ejecutarse en el servicio de transporte en un servidor de buzones de Exchange Server 2013. Es posible que implemente los controladores en el agente de transporte DeliveryAgent para los eventos proporcionados por la clase [DeliveryAgent](https://msdn.microsoft.com/en-us/library/microsoft.exchange.data.transport.delivery.deliveryagent(v=exchg.150).aspx) que se enumeran en la siguiente tabla. 
  
**La tabla 1. Eventos de clase DeliveryAgent**

|**Evento**|**Descripción**|
|:-----|:-----|
|[OnCloseConnection](https://msdn.microsoft.com/en-us/library/microsoft.exchange.data.transport.delivery.deliveryagent.oncloseconnection(v=exchg.150).aspx) <br/> |Se produce después de que se ha entregado el último elemento de correo y se cierra la conexión.  <br/> |
|[OnDeliverMailItem](https://msdn.microsoft.com/en-us/library/microsoft.exchange.data.transport.delivery.deliveryagent.ondelivermailitem(v=exchg.150).aspx) <br/> |Se produce cuando un elemento de correo está listo para entregar.  <br/> |
|[OnOpenConnection](https://msdn.microsoft.com/en-us/library/microsoft.exchange.data.transport.delivery.deliveryagent.onopenconnection(v=exchg.150).aspx) <br/> |Se produce cuando se abre el agente de entrega para la entrega de correo.  <br/> |
   
## <a name="creating-a-custom-deliveryagent-transport-agent"></a>Creación de un agente de transporte DeliveryAgent personalizado

El siguiente procedimiento describe cómo crear a un agente de transporte DeliveryAgent personalizado. 
  
### <a name="to-create-the-transport-agent"></a>Para crear al agente de transporte

1. Agregue referencias a los espacios de nombres.
    
   ```cs
        using Microsoft.Exchange.Data.Transport;
        using Microsoft.Exchange.Data.Transport.Delivery;
    
   ```

   Puede encontrar estos espacios de nombres en el servidor de Exchange. Mediante la adición de una referencia a estos espacios de nombres, tendrá acceso a los miembros de [DeliveryAgent](https://msdn.microsoft.com/en-us/library/microsoft.exchange.data.transport.delivery.deliveryagent(v=exchg.150).aspx) . 
    
2. Implementar la clase derivada de la [DeliveryAgentFactory\<Manager\> ](https://msdn.microsoft.com/en-us/library/dd877550(v=exchg.150).aspx) clase. 
    
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

   Este código se cree una instancia de la clase derivada y reemplace el método **CreateAgent** para crear una instancia de su nuevo agente personalizado. Métodos adicionales, como **Close**, también pueden reemplazarse en esta clase para ejecutar código personalizado. Se crea una clase [DeliveryAgentManager](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Delivery.DeliveryAgentManager.aspx) para invalidar la propiedad [SupportedDeliveryProtocol](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Delivery.DeliveryAgentManager.SupportedDeliveryProtocol.aspx) y establecer el protocolo que se va a usar el agente. 
    
3. Definir al agente.
    
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

   Después de definir la clase de agente, se puede agregar funcionalidad personalizada. En este ejemplo, los tres eventos, [OnCloseConnection](https://msdn.microsoft.com/en-us/library/microsoft.exchange.data.transport.delivery.deliveryagent.oncloseconnection(v=exchg.150).aspx), [OnDeliverMailItem](https://msdn.microsoft.com/en-us/library/microsoft.exchange.data.transport.delivery.deliveryagent.ondelivermailitem(v=exchg.150).aspx)y [OnOpenConnection](https://msdn.microsoft.com/en-us/library/microsoft.exchange.data.transport.delivery.deliveryagent.onopenconnection(v=exchg.150).aspx), se redirigen a sus controladores de eventos personalizados. 
    
## <a name="see-also"></a>Vea también

- [Conceptos de agente en Exchange 2013 de transporte](transport-agent-concepts-in-exchange-2013.md)
- [Referencia de agente de transporte de Exchange 2013](transport-agent-reference-for-exchange-2013.md)          

 