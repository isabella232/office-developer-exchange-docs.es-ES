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
# <a name="create-a-deliveryagent-transport-agent-for-exchange-2013"></a>Crear un agente de transporte de DeliveryAgent para Exchange 2013

Descubra cómo crear un agente de transporte de DeliveryAgent personalizado para usarlo con Exchange 2013.
  
**Se aplica a:** Exchange Server 2013
  
Las [clases \<Manager\> DeliveryAgentFactory](https://msdn.microsoft.com/library/dd877550(v=exchg.150).aspx) y [DeliveryAgent](https://msdn.microsoft.com/library/microsoft.exchange.data.transport.delivery.deliveryagent(v=exchg.150).aspx) son las clases base para los agentes de transporte que están diseñadas para ejecutarse en el servicio de transporte en un servidor de buzones de correo de Exchange Server 2013. Puede implementar controladores en el agente de transporte de DeliveryAgent para los eventos proporcionados por la clase [DeliveryAgent](https://msdn.microsoft.com/library/microsoft.exchange.data.transport.delivery.deliveryagent(v=exchg.150).aspx) que se enumeran en la siguiente tabla. 
  
**Tabla 1. Eventos de la clase DeliveryAgent**

|**Event**|**Descripción**|
|:-----|:-----|
|[OnCloseConnection](https://msdn.microsoft.com/library/microsoft.exchange.data.transport.delivery.deliveryagent.oncloseconnection(v=exchg.150).aspx) <br/> |Se produce después de que se haya entregado el último elemento de correo y se haya cerrado la conexión.  <br/> |
|[OnDeliverMailItem](https://msdn.microsoft.com/library/microsoft.exchange.data.transport.delivery.deliveryagent.ondelivermailitem(v=exchg.150).aspx) <br/> |Se produce cuando un elemento de correo está listo para su entrega.  <br/> |
|[OnOpenConnection](https://msdn.microsoft.com/library/microsoft.exchange.data.transport.delivery.deliveryagent.onopenconnection(v=exchg.150).aspx) <br/> |Se produce cuando el agente de entrega se abre para la entrega de correo.  <br/> |
   
## <a name="creating-a-custom-deliveryagent-transport-agent"></a>Creación de un agente de transporte de DeliveryAgent personalizado

El siguiente procedimiento describe cómo crear un agente de transporte de DeliveryAgent personalizado. 
  
### <a name="to-create-the-transport-agent"></a>Para crear el agente de transporte

1. Agregue referencias a los espacios de nombres.
    
   ```cs
        using Microsoft.Exchange.Data.Transport;
        using Microsoft.Exchange.Data.Transport.Delivery;
    
   ```

   Puede encontrar estos espacios de nombres en su servidor de Exchange. Al agregar una referencia a estos espacios de nombres, tendrá acceso a los miembros de [DeliveryAgent](https://msdn.microsoft.com/library/microsoft.exchange.data.transport.delivery.deliveryagent(v=exchg.150).aspx) . 
    
2. Implemente la clase derivada para la clase [DeliveryAgentFactory \<Manager\> ](https://msdn.microsoft.com/library/dd877550(v=exchg.150).aspx) . 
    
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

   Este código creará una instancia de la clase derivada y reemplazará el método **CreateAgent** para crear una instancia del nuevo agente personalizado. Los métodos adicionales, como **Close**, también se pueden invalidar en esta clase para ejecutar código personalizado. Se crea una clase [DeliveryAgentManager](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Delivery.DeliveryAgentManager.aspx) para invalidar la propiedad [SupportedDeliveryProtocol](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Delivery.DeliveryAgentManager.SupportedDeliveryProtocol.aspx) y establecer el protocolo que usará el agente. 
    
3. Definir el agente.
    
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

   Después de definir la clase del agente, puede Agregar una funcionalidad personalizada. En este ejemplo, los tres eventos, [OnCloseConnection](https://msdn.microsoft.com/library/microsoft.exchange.data.transport.delivery.deliveryagent.oncloseconnection(v=exchg.150).aspx), [OnDeliverMailItem](https://msdn.microsoft.com/library/microsoft.exchange.data.transport.delivery.deliveryagent.ondelivermailitem(v=exchg.150).aspx)y [OnOpenConnection](https://msdn.microsoft.com/library/microsoft.exchange.data.transport.delivery.deliveryagent.onopenconnection(v=exchg.150).aspx), se redirigen a los controladores de eventos personalizados. 
    
## <a name="see-also"></a>Vea también

- [Conceptos del agente de transporte en Exchange 2013](transport-agent-concepts-in-exchange-2013.md)
- [Referencia del agente de transporte para Exchange 2013](transport-agent-reference-for-exchange-2013.md)          

 