---
title: Conceptos de agente de transporte Exchange 2013
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 0c700af8-2792-4d3f-8571-8860e0550d8e
description: Busque información sobre cómo la canalización del agente de transporte y la arquitectura de roles de servidor en Exchange 2013 afectan al desarrollo de agentes de transporte y las clases que puede usar para desarrollar agentes de transporte.
ms.openlocfilehash: 9116c9b7811958a2479421a642052df3cee24e34
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59537164"
---
# <a name="transport-agent-concepts-in-exchange-2013"></a>Conceptos de agente de transporte Exchange 2013

Busque información sobre cómo la canalización del agente de transporte y la arquitectura de roles de servidor en Exchange 2013 afectan al desarrollo de agentes de transporte y las clases que puede usar para desarrollar agentes de transporte. 
  
**Se aplica a:** Exchange Server 2013 
  
Puede usar la biblioteca de clases proporcionada en Exchange Server 2013 para implementar agentes de transporte que se registran para eventos y realizar acciones en los mensajes a medida que pasan por la canalización de transporte. También puede usar agentes de transporte para modificar mensajes y convertir contenido. 
  
En este artículo se proporciona información sobre los agentes de transporte y la arquitectura de canalización de transporte. Es importante comprender la arquitectura de la canalización de transporte para poder modificar el comportamiento del transporte para satisfacer las necesidades de su organización. En este artículo también se proporciona información sobre los cambios en la arquitectura Exchange 2013 que afectan a los agentes de transporte y a las clases que puede usar para desarrollar agentes de transporte. 
  
## <a name="transport-agents-in-the-transport-pipeline"></a>Agentes de transporte en la canalización de transporte
<a name="Pipeline"> </a>

Los agentes de transporte se derivan de una de las tres clases siguientes:
  
- [SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx)
- [RoutingAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.aspx)
- [DeliveryAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Delivery.DeliveryAgent.aspx)
    
La canalización de transporte hace referencia al flujo de datos de mensajes dentro de los límites de una Exchange 2013. La canalización consta de los servicios enumerados en la tabla siguiente.
  
**Tabla 1. Servicios de canalización de transporte**

|**Servicio**|**Descripción**|**Clases admitidas**|
|:-----|:-----|:-----|
|Transporte front-end  <br/> |Se ejecuta en todos los servidores [de](https://technet.microsoft.com/library/dd298114%28v=exchg.150%29.aspx) acceso de cliente y actúa como proxy sin estado para todo el tráfico SMTP externo entrante y saliente de la Exchange 2013. El servicio de transporte front-end no inspecciona el contenido de los mensajes ni pone en cola ningún mensaje localmente. Se comunica con el servicio de transporte en un servidor [de buzones de correo.](https://technet.microsoft.com/library/jj150491%28v=exchg.150%29.aspx)  <br/> |[SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx) <br/> |
|Transport  <br/> |Se ejecuta en todos los [](https://technet.microsoft.com/library/bb123494%28v=exchg.141%29.aspx) servidores de buzones de correo y es similar al rol de servidor Transporte de concentradores en Exchange Server 2010. El servicio de transporte enruta los mensajes entre sí y los servicios de transporte de buzones y de transporte front-end. Este servicio no se comunica directamente con bases de datos de buzones de correo.  <br/> |[SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx) <br/> [RoutingAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.aspx) <br/> [DeliveryAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Delivery.DeliveryAgent.aspx) <br/> |
|Transporte de buzones  <br/> |Se ejecuta en todos los servidores de buzones de correo y consta de dos servicios independientes: envío de transporte de buzones y entrega de transporte de buzones. La entrega de transporte de buzones recibe mensajes SMTP del servicio de transporte y se conecta Exchange la base de datos de buzones mediante una llamada Exchange procedimiento remoto (RPC) para entregar el mensaje. El envío de transporte de buzones se conecta a la base de datos de buzones de correo mediante RPC para recuperar mensajes y envía los mensajes a través de SMTP al servicio de transporte.  <br/> |Ninguno.  <br/> |
   
### <a name="transport-events"></a>Eventos de transporte
<a name="Events"> </a>

Primero se implementan agentes de transporte para registrar un evento y, a continuación, realizar una acción cuando se desen llamas. Cada uno de los tres tipos de agente puede registrarse para un conjunto diferente de eventos.
  
En la siguiente figura se muestra dónde pueden registrarse los eventos en la canalización de transporte.
  
**Figura 1. Eventos de transporte**

![Imagen que muestra el flujo de mensajes por la canalización de transporte y los eventos que cada agente puede registrar, comenzando por los eventos Smtp para SmtpReceivedAgent, después los eventos Categorizor para RoutingAgent y, por último, eventos Deliver para DeliveryAgent.](media/TAConceptsFig1.png)
  
Cuando un mensaje entra en la canalización de transporte, un agente de transporte derivado de la clase [SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx) puede actuar en el mensaje durante cualquiera de los eventos SMTP para los que se registró el agente. Un agente derivado de la [clase RoutingAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.aspx) puede actuar en cualquiera de los cuatro eventos categorizador para los que se ha registrado. Un agente derivado de la [clase DeliveryAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Delivery.DeliveryAgent.aspx) puede actuar en un mensaje durante cualquiera de los eventos de entrega para los que se ha registrado. 
  
## <a name="transport-agents-and-server-roles"></a>Agentes de transporte y roles de servidor
<a name="ServerRoles"> </a>

Los cambios en la arquitectura de roles de servidor Exchange 2013 afectan a los agentes de transporte y a lo que pueden hacer los agentes de transporte. Exchange 2013 incluye los siguientes roles de servidor:
  
- Servidor de buzones: incluye protocolos de acceso de cliente, el servicio de transporte, bases de datos de buzones de correo y componentes de mensajería unificada. El servidor de buzones de correo se comunica directamente con los Servicios de dominio de Active Directory (AD DS), los servidores de acceso de cliente y los clientes de correo, como Outlook.
    
- Servidor de acceso de cliente: proporciona autenticación, redirección limitada, servicios proxy y protocolos de acceso de cliente como HTTP, POP, IMAP y SMTP.
    
- Servidor de transporte perimetral: enruta el correo electrónico dentro y fuera de una organización. Los servidores de transporte perimetral normalmente se sientan en el perímetro de una Exchange topología.
    
Esta estructura consolidada reduce el número de servidores que deben implementarse en un entorno Exchange 2013. Los administradores ya no tienen que implementar servidores de transporte de concentradores y acceso de cliente en todos los sitios de Active Directory que incluyan un servidor de buzones de correo y ya no necesitan actualizar todos los roles de servidor para aprovechar las nuevas funciones.
  
Estos cambios en la arquitectura del rol de servidor pueden afectar a dónde puede responder el agente a los eventos. Si ha creado agentes de transporte para versiones de Exchange anteriores a Exchange 2013, asegúrese de revisar los cambios de arquitectura para determinar si necesita realizar cambios en los agentes.
  
En la siguiente figura se muestra cómo los cambios en la arquitectura Exchange 2013 resultan en una canalización de transporte simplificada y consolidada. En esta figura, los servidores de acceso de cliente tienen la etiqueta CAS. Y los servidores de buzones de correo tienen la etiqueta MBX.
  
**Figura 2. Exchange de roles de servidor de 2013**

![Imagen que muestra el tráfico de cliente a través de un firewall externo, el Transporte perimetral a la izquierda que pasa el tráfico por un equilibrio de carga de nivel 4 a una matriz CAS consolidada y un conjunto de servidores de buzones en un grupo de accesibilidad a bases de datos a la derecha.](media/Transport_Agent_Concepts_Fig_3.png)
  
En la siguiente figura se muestran las interacciones entre los Exchange de servidor de 2013.
  
**Figura 3. Interacciones del servidor de acceso de cliente y buzón**

![Imagen que muestra las interacciones que se inician con flechas desde el tráfico de cliente que pasa por un equilibrio de carga de nivel 4 que tiene 4 destinos en la matriz CAS: proxy IIS/HTTP, POP/IMAP, SMTP y UM. Las flechas pasan a sus destinos complementarios en el almacén de buzones.](media/Transport_Agent_Concepts_Fig_4.png)
  
Para obtener más información acerca de los cambios en la arquitectura de roles de servidor de Exchange 2013, vea [Exchange arquitectura de 2013](https://technet.microsoft.com/library/jj150540%28v=exchg.150%29.aspx#BKMK_Arch) en Novedades de [Exchange 2013](https://technet.microsoft.com/library/jj150540%28v=exchg.150%29.aspx). 
  
## <a name="transport-agent-classes"></a>Clases de agente de transporte
<a name="Create"> </a>

La clase de la que deriva el agente de transporte determina los eventos para los que el agente puede registrarse. El agente normalmente contendrá una clase de agente, una fábrica de agentes, uno o varios controladores de eventos y el código que realiza las acciones que desea que realice el agente.
  
En la tabla siguiente se enumeran las clases de las que se derivará para cada tipo de agente.
  
**Tabla 2. Clases de agente**

||||
|:-----|:-----|:-----|
|Tipo de agente  <br/> |Clase base de fábrica  <br/> |Clase base de agente  <br/> |
|Recepción SMTP  <br/> |[SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx) <br/> |[SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx) <br/> |
|Enrutamiento  <br/> |[RoutingAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgentFactory.aspx) <br/> |[RoutingAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.aspx) <br/> |
|Delivery  <br/> |[DeliveryAgentFactory\<Manager\>](https://msdn.microsoft.com/library/dd877550(v=exchg.150).aspx) <br/> |[DeliveryAgent](https://msdn.microsoft.com/library/microsoft.exchange.data.transport.delivery.deliveryagent(v=exchg.150).aspx) <br/> |
   
Estas clases base de agente y de fábrica proporcionan propiedades y métodos que puede usar para obtener acceso a los mensajes y eventos de transporte. Implemente clases en el agente que hereden de estas clases. En la clase derivada de fábrica de agentes, invalide el **método CreateAgent** para que devuelva una nueva instancia de la clase de agente. 
  
Los argumentos que se pasan a los eventos pueden contener una instancia de la clase [EmailMessage,](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Email.EmailMessage.aspx) que puede usar para cambiar las propiedades y el contenido del mensaje subyacente. No toda la información del mensaje está disponible en cada evento. Debe determinar qué agente y qué evento es el mejor para la tarea que desea realizar. 
  
Los siguientes espacios de nombres contienen tipos que puede usar para leer, escribir y modificar mensajes en la canalización de transporte:
  
- [Microsoft. Exchange. Data.Mime.Encoders](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.Encoders.aspx)
    
- [Microsoft. Exchange. Data.ContentTypes.iCalendar](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.iCalendar.aspx)
    
- [Microsoft. Exchange. Data.Mime](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.aspx)
    
- [Microsoft. Exchange. Data.ContentTypes.Tnef](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.Tnef.aspx)
    
- [Microsoft. Exchange. Data.ContentTypes.vCard](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.vCard.aspx)
    
Después de escribir el agente de transporte, instale [y administre el](https://technet.microsoft.com/library/bb125175%28v=exchg.150%29.aspx) agente mediante el Shell Exchange administración. Para obtener más información, vea [Creating transport agents for Exchange 2013](creating-transport-agents-for-exchange-2013.md). 
  
## <a name="see-also"></a>Ver también

- [Agentes de transporte en Exchange](transport-agents-in-exchange-2013.md)    
- [Referencia de agente de transporte para Exchange 2013](transport-agent-reference-for-exchange-2013.md)   
- [Lectura y modificación de mensajes en la canalización Exchange transporte de 2013](reading-and-modifying-messages-in-the-exchange-2013-transport-pipeline.md)    
- [Novedades de Exchange 2013](https://technet.microsoft.com/library/jj150540%28v=exchg.150%29.aspx)   
- [Exchange de roles de servidor de 2013](https://blogs.technet.com/b/exchange/archive/2013/01/23/exchange-2013-server-role-architecture.aspx)    
- [Servidores de acceso de cliente y buzón](https://technet.microsoft.com/library/jj150519%28v=exchg.150%29.aspx)   
- [Exchange Server 2013 Mail Flow](https://technet.microsoft.com/library/aa996349.aspx)
- [Exchange Server de correo de 2013](https://technet.microsoft.com/library/aa998825%28v=exchg.150%29.aspx)   
- [Exchange Server PowerShell (Exchange Shell de administración)](https://docs.microsoft.com/powershell/exchange/exchange-server/exchange-management-shell?view=exchange-ps)
    

