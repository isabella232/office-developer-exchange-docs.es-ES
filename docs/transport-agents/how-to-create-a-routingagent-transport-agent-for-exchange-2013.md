---
title: Crear a un agente de transporte RoutingAgent para Exchange 2013
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3f0e745f-9289-4f31-8877-926692a8c133
description: Encuentre información acerca de cómo crear un agente de transporte RoutingAgent personalizado para usar con Exchange 2013.
ms.openlocfilehash: d07f68494acd26940a4837bbbfc7a0505114bd20
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763357"
---
# <a name="create-a-routingagent-transport-agent-for-exchange-2013"></a>Crear a un agente de transporte RoutingAgent para Exchange 2013

Encuentre información acerca de cómo crear un agente de transporte RoutingAgent personalizado para usar con Exchange 2013.
  
**Se aplica a:** Exchange Server 2013
  
Aplicaciones de ejemplo y fragmentos de código relacionados:

- [Exchange 2013: Crear a un agente de transporte de registro de ancho de banda](http://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-a-d61a4aaa)
  
Las clases [RoutingAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgentFactory.aspx) y [RoutingAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.aspx) son las clases base para los agentes de transporte que están diseñadas para ejecutarse en el servicio de transporte en un servidor de buzones de Exchange Server 2013. La clase [RoutingAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.aspx) proporciona los eventos que aparecen en la siguiente tabla para la que podría implementar controladores en el agente de transporte RoutingAgent. 
  
**La tabla 1. Eventos de clase RoutingAgent**

|**Evento**|**Descripción**|
|:-----|:-----|
|[OnCategorizedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnCategorizedMessage.aspx) <br/> |Se produce después de que el servidor realiza la conversión de contenido, si es necesario.  <br/> |
|[OnResolvedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnResolvedMessage.aspx) <br/> |Se produce después de que se han resueltos todos los destinatarios del mensaje y antes de enrutamiento está determinado.  <br/> |
|[OnRoutedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnRoutedMessage.aspx) <br/> |Se produce después de que el servidor enruta el mensaje al siguiente salto y realiza la conversión de contenido, si es necesario. El servidor podría utilizar más recursos para procesar cada mensaje en el evento [OnRoutedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnRoutedMessage.aspx) que el evento [OnSubmittedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnSubmittedMessage.aspx) debido a que el servidor va a realizar cualquier conversión de contenido necesaria y determinar el próximo salto en la ruta para el mensaje antes de ejecutar el código en el controlador de eventos [OnRoutedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnRoutedMessage.aspx) .  <br/> |
|[OnSubmittedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnSubmittedMessage.aspx) <br/> |Se produce después de que el mensaje se desconecta de la cola de envío. Use el evento [OnSubmittedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnSubmittedMessage.aspx) si el agente de transporte RoutingAgent no requieren conversión del contenido, los destinatarios resueltos o datos de enrutamiento.  <br/> |
   
## <a name="creating-a-custom-routingagent-transport-agent"></a>Creación de un agente de transporte RoutingAgent personalizado

El siguiente procedimiento describe cómo crear a un agente de transporte RoutingAgent personalizado. 
  
### <a name="to-create-the-transport-agent"></a>Para crear al agente de transporte

1. Agregue referencias a los espacios de nombres.
    
   ```cs
      using Microsoft.Exchange.Data.Mime;
      using Microsoft.Exchange.Data.Transport;
      using Microsoft.Exchange.Data.Transport.Routing;
  
   ```

   Puede encontrar estos espacios de nombres en el servidor de Exchange. Mediante la adición de una referencia a estos espacios de nombres, tendrá acceso a los miembros de [RoutingAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.aspx) así como otras clases que se usan en el [Exchange 2013: crear un agente de transporte de registro de ancho de banda](http://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-a-d61a4aaa) ejemplo. 
    
2. Implementar la clase derivada de la clase [RoutingAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgentFactory.aspx) . 
    
   ```cs
      public class BandwidthLoggerFactory : RoutingAgentFactory
      {
          public override RoutingAgent CreateAgent(SmtpServer server)
          {
              return new BandwidthLogger(server);
          }
      }
  
   ```

   Este código se cree una instancia de la clase derivada y reemplace el método **CreateAgent** para crear una instancia de su nuevo agente personalizado. Métodos adicionales, como **Close**, también pueden reemplazarse en esta clase para ejecutar código personalizado. 
    
3. Definir al agente.
    
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

   Después de definir la clase de agente, se puede agregar funcionalidad personalizada. En este ejemplo, los dos eventos [OnSubmittedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnSubmittedMessage.aspx) y [OnRoutedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnRoutedMessage.aspx)se redirigen a sus controladores de eventos personalizados. 
    
## <a name="see-also"></a>Vea también

- [Conceptos de agente en Exchange 2013 de transporte](transport-agent-concepts-in-exchange-2013.md)    
- [Referencia de agente de transporte de Exchange 2013](transport-agent-reference-for-exchange-2013.md)    
- [RoutingAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgentFactory.aspx)    
- [RoutingAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.aspx)
    

