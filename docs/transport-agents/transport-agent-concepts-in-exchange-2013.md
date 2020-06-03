---
title: Conceptos del agente de transporte en Exchange 2013
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0c700af8-2792-4d3f-8571-8860e0550d8e
description: Obtenga información acerca de cómo la canalización de agentes de transporte y la arquitectura de roles de servidor en Exchange 2013 afectan al desarrollo de agentes de transporte y a las clases que puede usar para desarrollar agentes de transporte.
ms.openlocfilehash: b9552ea4398ac8135a11b48eb7e7bdf5ec81985e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44527561"
---
# <a name="transport-agent-concepts-in-exchange-2013"></a>Conceptos del agente de transporte en Exchange 2013

Obtenga información acerca de cómo la canalización de agentes de transporte y la arquitectura de roles de servidor en Exchange 2013 afectan al desarrollo de agentes de transporte y a las clases que puede usar para desarrollar agentes de transporte. 
  
**Se aplica a:** Exchange Server 2013 
  
Puede usar la biblioteca de clases que se proporciona en Exchange Server 2013 para implementar agentes de transporte que se registran para eventos y emprenden acciones en los mensajes a medida que pasan a través de la canalización de transporte. También puede usar agentes de transporte para modificar mensajes y convertir contenido. 
  
En este artículo se proporciona información acerca de los agentes de transporte y la arquitectura de canalización de transporte. Es importante comprender la arquitectura de la canalización de transporte para que pueda modificar el comportamiento de transporte para satisfacer las necesidades de su organización. En este artículo también se proporciona información acerca de los cambios en la arquitectura de Exchange 2013 que afectan a los agentes de transporte y a las clases que puede usar para desarrollar agentes de transporte. 
  
## <a name="transport-agents-in-the-transport-pipeline"></a>Agentes de transporte en la canalización de transporte
<a name="Pipeline"> </a>

Los agentes de transporte se derivan de una de las tres clases siguientes:
  
- [SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx)
- [RoutingAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.aspx)
- [DeliveryAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Delivery.DeliveryAgent.aspx)
    
La canalización de transporte hace referencia al flujo de datos de mensajes dentro de los límites de una organización de Exchange 2013. La canalización consta de los servicios que se enumeran en la tabla siguiente.
  
**Tabla 1. Servicios de canalización de transporte**

|**Servicio**|**Descripción**|**Clases admitidas**|
|:-----|:-----|:-----|
|Transporte front-end  <br/> |Se ejecuta en todos los [servidores de acceso de cliente](https://technet.microsoft.com/library/dd298114%28v=exchg.150%29.aspx) y actúa como un proxy sin estado para todo el tráfico SMTP externo entrante y saliente para la organización Exchange 2013. El servicio de transporte front-end no inspecciona el contenido del mensaje ni pone en cola los mensajes de forma local. Se comunica con el servicio de transporte en un [servidor de buzones de correo](https://technet.microsoft.com/library/jj150491%28v=exchg.150%29.aspx).  <br/> |[SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx) <br/> |
|Transport  <br/> |Se ejecuta en todos los servidores de buzones de correo y es similar a la función de [servidor transporte de concentradores](https://technet.microsoft.com/library/bb123494%28v=exchg.141%29.aspx) en Exchange Server 2010. El servicio de transporte enruta los mensajes entre sí y los servicios de transporte de buzones y de transporte front-end. Este servicio no se comunica directamente con las bases de datos de buzones de correo.  <br/> |[SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx) <br/> [RoutingAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.aspx) <br/> [DeliveryAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Delivery.DeliveryAgent.aspx) <br/> |
|Transporte de buzones  <br/> |Se ejecuta en todos los servidores de buzones de correo y consta de dos servicios independientes: envío de transporte de buzones y entrega de transporte de buzones. La entrega de transporte de buzones de correo recibe mensajes SMTP del servicio de transporte y se conecta a la base de datos de buzones de correo mediante una llamada a procedimiento remoto (RPC) de Exchange para entregar el mensaje. El envío de transporte de buzones de correo se conecta a la base de datos de buzones de correo mediante RPC para recuperar mensajes y envía los mensajes a través de SMTP al servicio de transporte.  <br/> |Ninguna.  <br/> |
   
### <a name="transport-events"></a>Eventos de transporte
<a name="Events"> </a>

Los agentes de transporte se implementan en primer lugar al registrarse para un evento y, a continuación, realizar una acción cuando se desencadene el evento. Cada uno de los tres tipos de agentes se puede registrar para un conjunto de eventos diferente.
  
La siguiente figura muestra dónde pueden registrarse los agentes de transporte de las canalizaciones de transporte para los eventos.
  
**Figura 1. Eventos de transporte**

![Imagen que muestra el flujo de mensajes por la canalización de transporte y los eventos que cada agente puede registrar, comenzando por los eventos Smtp para SmtpReceivedAgent, después los eventos Categorizor para RoutingAgent y, por último, eventos Deliver para DeliveryAgent.](media/TAConceptsFig1.png)
  
Cuando un mensaje entra en la canalización de transporte, un agente de transporte derivado de la clase [SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx) puede actuar en el mensaje durante cualquiera de los eventos SMTP que el agente ha registrado. Un agente derivado de la clase [RoutingAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.aspx) puede actuar en cualquiera de los cuatro eventos de categorizador para los que se ha registrado. Un agente derivado de la clase [DeliveryAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Delivery.DeliveryAgent.aspx) puede actuar en un mensaje durante cualquier evento de entrega para el que se haya registrado. 
  
## <a name="transport-agents-and-server-roles"></a>Agentes de transporte y roles de servidor
<a name="ServerRoles"> </a>

Los cambios en la arquitectura de roles de servidor de Exchange 2013 afectan a los agentes de transporte y a lo que pueden hacer los agentes de transporte. Exchange 2013 incluye las siguientes funciones de servidor:
  
- Servidor de buzones de correo: incluye los protocolos de acceso de cliente, el servicio de transporte, las bases de datos de buzones y los componentes de mensajería unificada. El servidor de buzones se comunica directamente con los servicios de dominio de Active Directory (AD DS), los servidores de acceso de cliente y los clientes de correo, como Outlook.
    
- Servidor de acceso de cliente: proporciona autenticación, redirección limitada, servicios proxy y protocolos de acceso de cliente, como HTTP, POP, IMAP y SMTP.
    
- Servidor de transporte perimetral: enruta el correo electrónico dentro y fuera de una organización. Los servidores de transporte perimetral suelen sentarse en el perímetro de una topología de Exchange.
    
Esta estructura consolidada reduce el número de servidores que se deben implementar en un entorno de Exchange 2013. Los administradores ya no tienen que implementar servidores de transporte de concentradores y acceso de cliente en cada sitio de Active Directory que incluya un servidor de buzones de correo, y ya no necesitan actualizar todos los roles de servidor para aprovechar la nueva funcionalidad.
  
Estos cambios en la arquitectura del rol de servidor pueden afectar a la ubicación de la canalización que el agente puede responder a los eventos. Si ha creado agentes de transporte para versiones de Exchange anteriores a Exchange 2013, asegúrese de revisar los cambios en la arquitectura para determinar si necesita realizar cambios en los agentes.
  
La siguiente figura muestra cómo los cambios en la arquitectura de Exchange 2013 dan como resultado una canalización de transporte optimizada y consolidada. En esta figura, los servidores de acceso de cliente tienen la etiqueta CAS. Y los servidores de buzones de correo tienen la etiqueta MBX.
  
**Figura 2. Arquitectura de roles de servidor de Exchange 2013**

![Imagen que muestra el tráfico de cliente a través de un firewall externo, el Transporte perimetral a la izquierda que pasa el tráfico por un equilibrio de carga de nivel 4 a una matriz CAS consolidada y un conjunto de servidores de buzones en un grupo de accesibilidad a bases de datos a la derecha.](media/Transport_Agent_Concepts_Fig_3.png)
  
La siguiente figura muestra las interacciones entre los roles de servidor de Exchange 2013.
  
**Figura 3. Interacciones del servidor de acceso de cliente y buzón**

![Imagen que muestra las interacciones que se inician con flechas desde el tráfico de cliente que pasa por un equilibrio de carga de nivel 4 que tiene 4 destinos en la matriz CAS: proxy IIS/HTTP, POP/IMAP, SMTP y UM. Las flechas pasan a sus destinos complementarios en el almacén de buzones.](media/Transport_Agent_Concepts_Fig_4.png)
  
Para obtener más información acerca de los cambios en la arquitectura de roles de servidor de Exchange 2013, consulte [arquitectura de exchange 2013](https://technet.microsoft.com/library/jj150540%28v=exchg.150%29.aspx#BKMK_Arch) en [What's New in Exchange 2013](https://technet.microsoft.com/library/jj150540%28v=exchg.150%29.aspx). 
  
## <a name="transport-agent-classes"></a>Clases de agente de transporte
<a name="Create"> </a>

La clase de la que deriva el agente de transporte determina los eventos que el agente puede registrar. Normalmente, el agente contendrá una clase de agente, un generador de agentes, uno o más controladores de eventos y el código que realiza las acciones que desea que realice el agente.
  
En la siguiente tabla se enumeran las clases desde las que se va a derivar para cada tipo de agente.
  
**Tabla 2. Clases de agente**

||||
|:-----|:-----|:-----|
|Tipo de agente  <br/> |Clase base de fábrica  <br/> |Clase base de agente  <br/> |
|Recepción SMTP  <br/> |[SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx) <br/> |[SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx) <br/> |
|Distribuir  <br/> |[RoutingAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgentFactory.aspx) <br/> |[RoutingAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.aspx) <br/> |
|Delivery  <br/> |[DeliveryAgentFactory\<Manager\>](https://msdn.microsoft.com/library/dd877550(v=exchg.150).aspx) <br/> |[DeliveryAgent](https://msdn.microsoft.com/library/microsoft.exchange.data.transport.delivery.deliveryagent(v=exchg.150).aspx) <br/> |
   
Estas clases base de generador y agente proporcionan propiedades y métodos que puede usar para tener acceso a eventos y mensajes de transporte. Implementar clases en el agente que hereden de estas clases. En la clase derivada de Factory del agente, invalide el método **CreateAgent** para que devuelva una nueva instancia de la clase del agente. 
  
Los argumentos que se pasan a los eventos pueden contener una instancia de la clase [EmailMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Email.EmailMessage.aspx) , que se puede usar para cambiar las propiedades y el contenido del mensaje subyacente. No toda la información de mensajes está disponible en cada evento. Debe determinar qué agente y qué evento es el mejor para la tarea que desea realizar. 
  
Los espacios de nombres siguientes contienen tipos que puede usar para leer, escribir y modificar mensajes en la canalización de transporte:
  
- [Microsoft. Exchange. Data. MIME. codificadores](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.Encoders.aspx)
    
- [Microsoft. Exchange. Data. ContentTypes. iCalendar](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.iCalendar.aspx)
    
- [Microsoft. Exchange. Data. MIME](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.aspx)
    
- [Microsoft. Exchange. Data. ContentTypes. TNEF](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.Tnef.aspx)
    
- [Microsoft. Exchange. Data. ContentTypes. vCard](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.vCard.aspx)
    
Después de escribir el agente de transporte, [Instale y administre el agente](https://technet.microsoft.com/library/bb125175%28v=exchg.150%29.aspx) mediante el shell de administración de Exchange. Para obtener más información, vea [crear agentes de transporte para Exchange 2013](creating-transport-agents-for-exchange-2013.md). 
  
## <a name="see-also"></a>Vea también

- [Agentes de transporte en Exchange](transport-agents-in-exchange-2013.md)    
- [Referencia del agente de transporte para Exchange 2013](transport-agent-reference-for-exchange-2013.md)   
- [Leer y modificar mensajes en la canalización de transporte de Exchange 2013](reading-and-modifying-messages-in-the-exchange-2013-transport-pipeline.md)    
- [Novedades en Exchange 2013](https://technet.microsoft.com/library/jj150540%28v=exchg.150%29.aspx)   
- [Arquitectura de roles de servidor de Exchange 2013](https://blogs.technet.com/b/exchange/archive/2013/01/23/exchange-2013-server-role-architecture.aspx)    
- [Servidores de buzones de correo y acceso de cliente](https://technet.microsoft.com/library/jj150519%28v=exchg.150%29.aspx)   
- [Flujo de correo de Exchange Server 2013](https://technet.microsoft.com/library/aa996349.aspx)
- [Enrutamiento de correo de Exchange Server 2013](https://technet.microsoft.com/library/aa998825%28v=exchg.150%29.aspx)   
- [PowerShell de Exchange Server (Shell de administración de Exchange)](https://docs.microsoft.com/powershell/exchange/exchange-server/exchange-management-shell?view=exchange-ps)
    

