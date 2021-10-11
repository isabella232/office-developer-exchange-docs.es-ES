---
title: Crear un agente de transporte RoutingAgent para Exchange 2013
manager: sethgros
ms.date: 09/21/2021
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 3f0e745f-9289-4f31-8877-926692a8c133
description: Descubra cómo crear un agente de transporte RoutingAgent personalizado para usarlo con Exchange 2013.
ms.openlocfilehash: 89c70e7d021b9b2cc46f65ee3bbff334430fecc7
ms.sourcegitcommit: f13a3a4a61fa23ca6414b7c96ddf087adbe3dc9e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/11/2021
ms.locfileid: "60262214"
---
# <a name="create-a-routingagent-transport-agent-for-exchange-2013"></a>Crear un agente de transporte RoutingAgent para Exchange 2013

Descubra cómo crear un agente de transporte RoutingAgent personalizado para usarlo con Exchange 2013.
  
**Se aplica a:** Exchange Server 2013
  
Fragmentos de código relacionados y aplicaciones de ejemplo:

- [Exchange 2013: crear un agente de transporte de registro de ancho de banda](/exchange/client-developer/transport-agents/transport-agent-code-samples-for-exchange-2013.md)
  
Las [clases RoutingAgentFactory](https://docs.microsoft.com/previous-versions/office/exchange-server-api/aa564164(v=exchg.150)) y [RoutingAgent](https://docs.microsoft.com/previous-versions/office/exchange-server-api/aa564421(v=exchg.150)) son las clases base para agentes de transporte diseñados para ejecutarse en el servicio de transporte en un servidor de buzones de correo Exchange Server 2013. La [clase RoutingAgent](https://docs.microsoft.com/previous-versions/office/exchange-server-api/aa564421(v=exchg.150)) proporciona los eventos enumerados en la tabla siguiente para los que puede implementar controladores en el agente de transporte RoutingAgent. 
  
**Tabla 1. Eventos de clase RoutingAgent**

|**Event**|**Descripción**|
|:-----|:-----|
|[OnCategorizedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnCategorizedMessage.aspx) <br/> |Se produce después de que el servidor realiza la conversión de contenido, si es necesario.  <br/> |
|[OnResolvedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnResolvedMessage.aspx) <br/> |Se produce después de que se hayan resuelto todos los destinatarios del mensaje y antes de determinar el enrutamiento.  <br/> |
|[OnRoutedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnRoutedMessage.aspx) <br/> |Se produce después de que el servidor enruta el mensaje al próximo salto y realiza la conversión de contenido, si es necesario. El servidor puede usar más recursos para procesar cada mensaje del evento [OnRoutedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnRoutedMessage.aspx) que el evento [OnSubmittedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnSubmittedMessage.aspx) porque el servidor realizará cualquier conversión de contenido necesaria y determinará el próximo salto en la ruta del mensaje antes de ejecutar el código en el controlador de eventos [OnRoutedMessage.](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnRoutedMessage.aspx)  <br/> |
|[OnSubmittedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnSubmittedMessage.aspx) <br/> |Se produce después de quitar el mensaje de la cola de envío. Use el [evento OnSubmittedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnSubmittedMessage.aspx) si el agente de transporte RoutingAgent no requiere conversión de contenido, destinatarios resueltos o datos de enrutamiento.  <br/> |
   
## <a name="creating-a-custom-routingagent-transport-agent"></a>Creación de un agente de transporte RoutingAgent personalizado

En el siguiente procedimiento se describe cómo crear un agente de transporte RoutingAgent personalizado. 
  
### <a name="to-create-the-transport-agent"></a>Para crear el agente de transporte

1. Agregue referencias a los espacios de nombres.
    
   ```cs
      using Microsoft.Exchange.Data.Mime;
      using Microsoft.Exchange.Data.Transport;
      using Microsoft.Exchange.Data.Transport.Routing;
  
   ```

   Puede encontrar estos espacios de nombres en su Exchange servidor. Al agregar una referencia a estos espacios de nombres, tendrá acceso a los miembros [de RoutingAgent,](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.aspx) así como a otras clases usadas en [Exchange 2013: Crear](https://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-a-d61a4aaa) un ejemplo de agente de transporte de registro de ancho de banda. 
    
2. Implemente la clase derivada para la [clase RoutingAgentFactory.](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgentFactory.aspx) 
    
   ```cs
      public class BandwidthLoggerFactory : RoutingAgentFactory
      {
          public override RoutingAgent CreateAgent(SmtpServer server)
          {
              return new BandwidthLogger(server);
          }
      }
  
   ```

   Este código creará una instancia de la clase derivada e invalidará el **método CreateAgent** para crear una instancia del nuevo agente personalizado. Los métodos adicionales, **como Close**, también se pueden invalidar en esta clase para ejecutar código personalizado. 
    
3. Defina el agente.
    
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

   Después de definir la clase de agente, puede agregar la funcionalidad personalizada. En este ejemplo, los dos eventos [OnSubmittedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnSubmittedMessage.aspx) y [OnRoutedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnRoutedMessage.aspx)se redirigen a los controladores de eventos personalizados. 
    
## <a name="see-also"></a>Vea también

- [Conceptos de agente de transporte Exchange 2013](transport-agent-concepts-in-exchange-2013.md)    
- [Referencia de agente de transporte para Exchange 2013](transport-agent-reference-for-exchange-2013.md)    
- [RoutingAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgentFactory.aspx)    
- [RoutingAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.aspx)
    

