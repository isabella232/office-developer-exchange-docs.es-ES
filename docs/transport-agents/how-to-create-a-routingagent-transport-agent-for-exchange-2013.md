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
# <a name="create-a-routingagent-transport-agent-for-exchange-2013"></a>Crear un agente de transporte de RoutingAgent para Exchange 2013

Descubra cómo crear un agente de transporte de RoutingAgent personalizado para usarlo con Exchange 2013.
  
**Se aplica a:** Exchange Server 2013
  
Fragmentos de código y aplicaciones de ejemplo relacionados:

- [Exchange 2013: crear un agente de transporte de registro de ancho de banda](https://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-a-d61a4aaa)
  
Las clases [RoutingAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgentFactory.aspx) y [RoutingAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.aspx) son las clases base para los agentes de transporte que están diseñadas para ejecutarse en el servicio de transporte en un servidor de buzones de correo de Exchange Server 2013. La clase [RoutingAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.aspx) proporciona los eventos enumerados en la siguiente tabla para los que puede implementar controladores en el agente de transporte RoutingAgent. 
  
**Tabla 1. Eventos de la clase RoutingAgent**

|**Event**|**Descripción**|
|:-----|:-----|
|[OnCategorizedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnCategorizedMessage.aspx) <br/> |Se produce después de que el servidor realice la conversión de contenido, si es necesario.  <br/> |
|[OnResolvedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnResolvedMessage.aspx) <br/> |Se produce después de que se hayan resuelto todos los destinatarios del mensaje y antes de que se determine el enrutamiento.  <br/> |
|[OnRoutedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnRoutedMessage.aspx) <br/> |Se produce después de que el servidor enruta el mensaje al siguiente salto y realiza la conversión de contenido, si es necesario. Es posible que el servidor use más recursos para procesar cada mensaje en el evento [OnRoutedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnRoutedMessage.aspx) que el evento [OnSubmittedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnSubmittedMessage.aspx) , ya que el servidor realizará la conversión de contenido necesaria y determinará el siguiente salto en la ruta del mensaje antes de ejecutar el código en el controlador de eventos [OnRoutedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnRoutedMessage.aspx) .  <br/> |
|[OnSubmittedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnSubmittedMessage.aspx) <br/> |Se produce después de que el mensaje se sale de la cola de envío. Use el evento [OnSubmittedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnSubmittedMessage.aspx) si el agente de transporte RoutingAgent no requiere la conversión de contenido, los destinatarios resueltos o los datos de enrutamiento.  <br/> |
   
## <a name="creating-a-custom-routingagent-transport-agent"></a>Creación de un agente de transporte de RoutingAgent personalizado

El siguiente procedimiento describe cómo crear un agente de transporte de RoutingAgent personalizado. 
  
### <a name="to-create-the-transport-agent"></a>Para crear el agente de transporte

1. Agregue referencias a los espacios de nombres.
    
   ```cs
      using Microsoft.Exchange.Data.Mime;
      using Microsoft.Exchange.Data.Transport;
      using Microsoft.Exchange.Data.Transport.Routing;
  
   ```

   Puede encontrar estos espacios de nombres en su servidor de Exchange. Al agregar una referencia a estos espacios de nombres, tendrá acceso a los miembros de [RoutingAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.aspx) y a otras clases usadas en el ejemplo [Exchange 2013: Build a Bandwidth Logging Transport Agent](https://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-a-d61a4aaa) . 
    
2. Implemente la clase derivada para la clase [RoutingAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgentFactory.aspx) . 
    
   ```cs
      public class BandwidthLoggerFactory : RoutingAgentFactory
      {
          public override RoutingAgent CreateAgent(SmtpServer server)
          {
              return new BandwidthLogger(server);
          }
      }
  
   ```

   Este código creará una instancia de la clase derivada y reemplazará el método **CreateAgent** para crear una instancia del nuevo agente personalizado. Los métodos adicionales, como **Close**, también se pueden invalidar en esta clase para ejecutar código personalizado. 
    
3. Definir el agente.
    
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

   Después de definir la clase del agente, puede Agregar una funcionalidad personalizada. En este ejemplo, los dos eventos [OnSubmittedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnSubmittedMessage.aspx) y [OnRoutedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnRoutedMessage.aspx)se redirigen a los controladores de eventos personalizados. 
    
## <a name="see-also"></a>Vea también

- [Conceptos del agente de transporte en Exchange 2013](transport-agent-concepts-in-exchange-2013.md)    
- [Referencia del agente de transporte para Exchange 2013](transport-agent-reference-for-exchange-2013.md)    
- [RoutingAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgentFactory.aspx)    
- [RoutingAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.aspx)
    

