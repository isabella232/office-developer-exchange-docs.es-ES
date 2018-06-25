---
title: Conceptos de agente en Exchange 2013 de transporte
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0c700af8-2792-4d3f-8571-8860e0550d8e
description: Obtenga información acerca de cómo la arquitectura de rol de canalización y servidor de agente de transporte en Exchange 2013 afectan al desarrollo de agentes de transporte y las clases que puede usar para desarrollar a los agentes de transporte.
ms.openlocfilehash: 9ddee0d68c9104357f84322b2cce7c5f2576d871
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763379"
---
# <a name="transport-agent-concepts-in-exchange-2013"></a>Conceptos de agente en Exchange 2013 de transporte

Obtenga información acerca de cómo la arquitectura de rol de canalización y servidor de agente de transporte en Exchange 2013 afectan al desarrollo de agentes de transporte y las clases que puede usar para desarrollar a los agentes de transporte. 
  
**Se aplica a:** Exchange Server 2013 
  
Puede usar la biblioteca de clases proporcionada en Exchange Server 2013 para implementar a los agentes de transporte que registrar los eventos y realizar acciones en los mensajes que pasan por la canalización de transporte. También puede utilizar a los agentes de transporte para modificar los mensajes y convertir el contenido. 
  
En este artículo se proporcionan información acerca de los agentes de transporte y la arquitectura de canalización de transporte. Es importante comprender la arquitectura de la canalización de transporte para que se puede modificar el comportamiento de transporte para satisfacer las necesidades de su organización. En este artículo también proporciona información acerca de los cambios en la arquitectura de Exchange 2013 que afectan a los agentes de transporte y las clases que puede usar para desarrollar a los agentes de transporte. 
  
## <a name="transport-agents-in-the-transport-pipeline"></a>Agentes de transporte en la canalización de transporte
<a name="Pipeline"> </a>

Los agentes de transporte se derivan de una de las tres clases siguientes:
  
- [SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx)
- [RoutingAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.aspx)
- [DeliveryAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Delivery.DeliveryAgent.aspx)
    
La canalización de transporte hace referencia para el flujo de datos de mensaje dentro de los límites de una organización de Exchange 2013. La canalización consta de los servicios enumerados en la siguiente tabla.
  
**La tabla 1. Servicios de la canalización de transporte**

|**Servicio**|**Descripción**|**Clases admitidas**|
|:-----|:-----|:-----|
|Transporte de Front-End  <br/> |Se ejecuta en todos los [servidores acceso de cliente](http://technet.microsoft.com/en-us/library/dd298114%28v=exchg.150%29.aspx) y actúa como un proxy para todos los entrante y saliente SMTP el tráfico externo para la organización de Exchange 2013 sin estado. El servicio de transporte Front-End no inspeccionar el contenido del mensaje o cola todos los mensajes de forma local. Se comunica con el servicio de transporte en un [servidor de buzones](http://technet.microsoft.com/en-us/library/jj150491%28v=exchg.150%29.aspx).  <br/> |[SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx) <br/> |
|Transporte  <br/> |Se ejecuta en todos los servidores de buzones de correo y es similar a la función de [servidor transporte de concentradores](http://technet.microsoft.com/en-us/library/bb123494%28v=exchg.141%29.aspx) en Exchange Server 2010. El servicio de transporte enruta los mensajes entre sí y los servicios de transporte de buzón de correo y transporte de Front-End. Este servicio no se comunica directamente con las bases de datos de buzón de correo.  <br/> |[SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx) <br/> [RoutingAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.aspx) <br/> [DeliveryAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Delivery.DeliveryAgent.aspx) <br/> |
|Transporte de buzones  <br/> |Se ejecuta en todos los servidores de buzones de correo y se compone de dos servicios independientes: envío de transporte de buzón de correo y entrega de transporte de buzón de correo. Entrega de transporte de buzón de correo recibe los mensajes SMTP desde el servicio de transporte y se conecta a la base de datos de buzones de correo mediante una llamada a procedimiento remoto (RPC de) Exchange para entregar el mensaje. Envío de transporte de buzón de correo se conecta a la base de datos de buzones de correo mediante RPC para recuperar los mensajes y envía los mensajes a través de SMTP para el servicio de transporte.  <br/> |Ninguno.  <br/> |
   
### <a name="transport-events"></a>Eventos de transporte
<a name="Events"> </a>

Implementar a los agentes de transporte registrando en primer lugar para un evento, y luego llevar a cabo una acción cuando se desencadena el evento. Cada uno de los tipos de tres agente puede registrarse para obtener un conjunto diferente de eventos.
  
En la siguiente figura se muestra dónde en el transporte de canalización de transporte los agentes pueden registrar los eventos.
  
**En la figura 1. Eventos de transporte**

![Imagen que muestra el flujo de mensajes por la canalización de transporte y los eventos que cada agente puede registrar, comenzando por los eventos Smtp para SmtpReceivedAgent, después los eventos Categorizor para RoutingAgent y, por último, eventos Deliver para DeliveryAgent.](media/TAConceptsFig1.png)
  
Cuando un mensaje entra en la canalización de transporte, un agente de transporte derivado de la clase [SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx) puede actuar en el mensaje durante cualquiera de los eventos de SMTP que el agente registrado para. Un agente derivado de la clase [RoutingAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.aspx) puede actuar en cualquiera de los cuatro eventos de categorizador que se han registrado para. Un agente derivado de la clase [DeliveryAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Delivery.DeliveryAgent.aspx) puede actuar en un mensaje durante cualquiera de los eventos de entrega que se han registrado para. 
  
## <a name="transport-agents-and-server-roles"></a>Los agentes de transporte y funciones de servidor
<a name="ServerRoles"> </a>

Los cambios realizados en la arquitectura del rol de servidor en Exchange 2013 afecta a los agentes de transporte y lo que pueden hacer los agentes de transporte. Exchange 2013 incluye las siguientes funciones de servidor:
  
- Servidor de buzones: protocolos incluye acceso de cliente, el servicio de transporte, las bases de datos de buzones de correo y componentes de mensajería unificada. El servidor de buzón de correo se comunica directamente con los servicios de dominio de Active Directory (AD DS), los servidores de acceso de cliente y los clientes de correo, como Outlook.
    
- Servidor acceso de cliente: proporciona autenticación, redirección limitado, servicios de proxy y protocolos de acceso de cliente, como HTTP, POP, IMAP y SMTP.
    
- Servidor de transporte perimetral: rutas de correo electrónico dentro y fuera de una organización. Servidores de transporte perimetral se encuentran normalmente en el perímetro de una topología de Exchange.
    
Esta estructura consolidada reduce el número de servidores que deben implementarse en un entorno de Exchange 2013. Los administradores ya no tienen que implementar servidores de transporte de concentradores y acceso de cliente en cada sitio de Active Directory que incluye un servidor de buzón de correo y ya no es necesario actualizar todos los roles de servidor para poder aprovechar las ventajas de la nueva funcionalidad.
  
Estos cambios a la arquitectura del rol de servidor pueden afectar a donde en la canalización de los agentes pueden responder a eventos. Si ha creado a los agentes de transporte para las versiones de Exchange anteriores a Exchange 2013, asegúrese de revisar los cambios de arquitectura para determinar si necesita realizar cambios en los agentes.
  
La siguiente ilustración muestra cómo los cambios en la arquitectura de Exchange 2013 de resultados en una canalización de transporte simplificado y consolidado. En esta figura, los servidores de acceso de cliente están etiquetadas como entidades de certificación. Y los servidores de buzones se etiquetan los Buzones.
  
**La figura 2. Arquitectura del rol de servidor de Exchange 2013**

![Imagen que muestra el tráfico de cliente a través de un firewall externo, el Transporte perimetral a la izquierda que pasa el tráfico por un equilibrio de carga de nivel 4 a una matriz CAS consolidada y un conjunto de servidores de buzones en un grupo de accesibilidad a bases de datos a la derecha.](media/Transport_Agent_Concepts_Fig_3.png)
  
La siguiente ilustración muestra las interacciones entre las funciones de servidor Exchange 2013.
  
**La figura 3. Interacciones de servidor de buzón de correo y acceso de cliente**

![Imagen que muestra las interacciones que se inician con flechas desde el tráfico de cliente que pasa por un equilibrio de carga de nivel 4 que tiene 4 destinos en la matriz CAS: proxy IIS/HTTP, POP/IMAP, SMTP y UM. Las flechas pasan a sus destinos complementarios en el almacén de buzones.](media/Transport_Agent_Concepts_Fig_4.png)
  
Para obtener más información acerca de los cambios en la arquitectura del rol de servidor de Exchange 2013, vea [arquitectura de Exchange 2013](http://technet.microsoft.com/en-us/library/jj150540%28v=exchg.150%29.aspx#BKMK_Arch) en [Novedades en Exchange 2013](http://technet.microsoft.com/en-us/library/jj150540%28v=exchg.150%29.aspx). 
  
## <a name="transport-agent-classes"></a>Clases de agente de transporte
<a name="Create"> </a>

La clase que se deriva el agente de transporte determina los eventos para los que puede registrar su agente. El agente normalmente contendrá una clase de agente, un generador de agentes, uno o varios controladores de eventos y el código que realiza las acciones que desea que realice su agente.
  
En la siguiente tabla se enumera las clases desde la que se derivan para cada tipo de agente.
  
**Tabla 2. Clases de agente**

||||
|:-----|:-----|:-----|
|Tipo de agente  <br/> |Clase base de fábrica  <br/> |Clase base del agente  <br/> |
|De recepción SMTP  <br/> |[SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx) <br/> |[SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx) <br/> |
|Enrutamiento  <br/> |[RoutingAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgentFactory.aspx) <br/> |[RoutingAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.aspx) <br/> |
|Entrega  <br/> |[DeliveryAgentFactory\<Manager\>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Delivery.DeliveryAgentFactory`1.aspx) <br/> |[DeliveryAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Delivery.DeliveryAgent.aspx) <br/> |
   
Estas clases base de fábrica y agente proporcionan propiedades y métodos que puede usar para obtener acceso a los eventos de transporte y mensajes. Implementar las clases en el agente que heredan de estas clases. En la clase derivada de fábrica del agente, reemplace el método **CreateAgent** para que devuelva una nueva instancia de la clase de agente. 
  
Argumentos que se pasan a los eventos pueden contener una instancia de la clase [EmailMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Email.EmailMessage.aspx) , que puede usar para cambiar las propiedades y el contenido del mensaje subyacente. No toda la información de mensaje está disponible en cada evento. Debe determinar a qué agente y qué evento es adecuado para la tarea que desee realizar. 
  
Los siguientes espacios de nombres contienen tipos que puede usar para leer, escribir y modificar los mensajes en la canalización de transporte:
  
- [Microsoft.Exchange.Data.Mime.Encoders](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.Encoders.aspx)
    
- [Microsoft.Exchange.Data.ContentTypes.iCalendar](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.iCalendar.aspx)
    
- [Microsoft.Exchange.Data.Mime](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.aspx)
    
- [Microsoft.Exchange.Data.ContentTypes.Tnef](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.Tnef.aspx)
    
- [Microsoft.Exchange.Data.ContentTypes.vCard](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.vCard.aspx)
    
Tras escribir el agente de transporte, [instalar y administrar al agente](http://technet.microsoft.com/en-us/library/bb125175%28v=exchg.150%29.aspx) mediante el Shell de administración de Exchange. Para obtener más información, vea [crear agentes de transporte de Exchange 2013](creating-transport-agents-for-exchange-2013.md). 
  
## <a name="see-also"></a>Vea también

- [Los agentes de transporte en Exchange](transport-agents-in-exchange-2013.md)    
- [Referencia de agente de transporte de Exchange 2013](transport-agent-reference-for-exchange-2013.md)   
- [Leer y modificar los mensajes en la canalización de transporte de Exchange 2013](reading-and-modifying-messages-in-the-exchange-2013-transport-pipeline.md)    
- [What ' s New in Exchange 2013](http://technet.microsoft.com/en-us/library/jj150540%28v=exchg.150%29.aspx)   
- [Arquitectura del rol de servidor de Exchange 2013](http://blogs.technet.com/b/exchange/archive/2013/01/23/exchange-2013-server-role-architecture.aspx)    
- [Buzón de correo y servidores de acceso de cliente](http://technet.microsoft.com/en-us/library/jj150519%28v=exchg.150%29.aspx)   
- [Flujo de correo de Exchange Server 2013](http://technet.microsoft.com/en-us/library/aa996349.aspx)
- [Enrutamiento de Exchange Server 2013 correo](http://technet.microsoft.com/en-us/library/aa998825%28v=exchg.150%29.aspx)   
- [Exchange Server PowerShell (Shell de administración de Exchange)](https://docs.microsoft.com/en-us/powershell/exchange/exchange-server/exchange-management-shell?view=exchange-ps)
    

