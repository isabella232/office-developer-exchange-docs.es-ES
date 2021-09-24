---
title: Crear un agente de transporte DeliveryAgent para Exchange 2013
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 4af904d7-b315-4849-92b1-66018f76ffdf
description: Descubra cómo crear un agente de transporte DeliveryAgent personalizado para usarlo con Exchange 2013.
ms.openlocfilehash: b465c3bbd4658bea700d5be9f4eb16ae81693717
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59526936"
---
# <a name="create-a-deliveryagent-transport-agent-for-exchange-2013"></a>Crear un agente de transporte DeliveryAgent para Exchange 2013

Descubra cómo crear un agente de transporte DeliveryAgent personalizado para usarlo con Exchange 2013.
  
**Se aplica a:** Exchange Server 2013
  
Las [clases \<Manager\> DeliveryAgentFactory](https://msdn.microsoft.com/library/dd877550(v=exchg.150).aspx) y [DeliveryAgent](https://msdn.microsoft.com/library/microsoft.exchange.data.transport.delivery.deliveryagent(v=exchg.150).aspx) son las clases base para agentes de transporte diseñados para ejecutarse en el servicio de transporte en un servidor de buzones de correo Exchange Server 2013. Puede implementar controladores en el agente de transporte DeliveryAgent para los eventos proporcionados por la [clase DeliveryAgent](https://msdn.microsoft.com/library/microsoft.exchange.data.transport.delivery.deliveryagent(v=exchg.150).aspx) que se enumeran en la tabla siguiente. 
  
**Tabla 1. Eventos de clase DeliveryAgent**

|**Event**|**Descripción**|
|:-----|:-----|
|[OnCloseConnection](https://msdn.microsoft.com/library/microsoft.exchange.data.transport.delivery.deliveryagent.oncloseconnection(v=exchg.150).aspx) <br/> |Se produce después de que se haya entregado el último elemento de correo y se cierre la conexión.  <br/> |
|[OnDeliverMailItem](https://msdn.microsoft.com/library/microsoft.exchange.data.transport.delivery.deliveryagent.ondelivermailitem(v=exchg.150).aspx) <br/> |Se produce cuando un elemento de correo está listo para entregarse.  <br/> |
|[OnOpenConnection](https://msdn.microsoft.com/library/microsoft.exchange.data.transport.delivery.deliveryagent.onopenconnection(v=exchg.150).aspx) <br/> |Se produce cuando se abre el agente de entrega para la entrega de correo.  <br/> |
   
## <a name="creating-a-custom-deliveryagent-transport-agent"></a>Creación de un agente de transporte DeliveryAgent personalizado

En el siguiente procedimiento se describe cómo crear un agente de transporte DeliveryAgent personalizado. 
  
### <a name="to-create-the-transport-agent"></a>Para crear el agente de transporte

1. Agregue referencias a los espacios de nombres.
    
   ```cs
        using Microsoft.Exchange.Data.Transport;
        using Microsoft.Exchange.Data.Transport.Delivery;
    
   ```

   Puede encontrar estos espacios de nombres en su Exchange servidor. Al agregar una referencia a estos espacios de nombres, tendrá acceso a los [miembros de DeliveryAgent.](https://msdn.microsoft.com/library/microsoft.exchange.data.transport.delivery.deliveryagent(v=exchg.150).aspx) 
    
2. Implemente la clase derivada para la [clase DeliveryAgentFactory. \<Manager\> ](https://msdn.microsoft.com/library/dd877550(v=exchg.150).aspx) 
    
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

   Este código creará una instancia de la clase derivada e invalidará el **método CreateAgent** para crear una instancia del nuevo agente personalizado. Los métodos adicionales, **como Close**, también se pueden invalidar en esta clase para ejecutar código personalizado. Se [crea una clase DeliveryAgentManager](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Delivery.DeliveryAgentManager.aspx) para invalidar la propiedad [SupportedDeliveryProtocol](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Delivery.DeliveryAgentManager.SupportedDeliveryProtocol.aspx) y establecer el protocolo que usará el agente. 
    
3. Defina el agente.
    
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

   Después de definir la clase de agente, puede agregar la funcionalidad personalizada. En este ejemplo, los tres eventos, [OnCloseConnection](https://msdn.microsoft.com/library/microsoft.exchange.data.transport.delivery.deliveryagent.oncloseconnection(v=exchg.150).aspx), [OnDeliverMailItem](https://msdn.microsoft.com/library/microsoft.exchange.data.transport.delivery.deliveryagent.ondelivermailitem(v=exchg.150).aspx)y [OnOpenConnection](https://msdn.microsoft.com/library/microsoft.exchange.data.transport.delivery.deliveryagent.onopenconnection(v=exchg.150).aspx), se redirigen a los controladores de eventos personalizados. 
    
## <a name="see-also"></a>Ver también

- [Conceptos de agente de transporte Exchange 2013](transport-agent-concepts-in-exchange-2013.md)
- [Referencia de agente de transporte para Exchange 2013](transport-agent-reference-for-exchange-2013.md)          

 