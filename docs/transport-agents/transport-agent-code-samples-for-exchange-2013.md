---
title: Ejemplos de código de agente para Exchange 2013 de transporte
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 626345ec-918f-4d91-932f-e6ce92553ccb
description: Obtenga información acerca de los agentes de transporte de ejemplo que están disponibles para Exchange 2013.
ms.openlocfilehash: 122a3351748fa6ffd823a51ce65ffb913332cb2c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763374"
---
# <a name="transport-agent-code-samples-for-exchange-2013"></a>Ejemplos de código de agente para Exchange 2013 de transporte

Obtenga información acerca de los agentes de transporte de ejemplo que están disponibles para Exchange 2013.
  
**Se aplica a:** Exchange Server 2013
  
Puede usar las API que se incluyen en Exchange Server 2013 para desarrollar a los agentes que amplían la funcionalidad de transporte. En este artículo se proporciona información acerca de los agentes de ejemplo que están disponibles para ayudarle a aprender a extender mediante programación el comportamiento de transporte. Los agentes de ejemplo incluyen el código fuente para cada componente. 
  
En la siguiente tabla se enumera a los agentes de ejemplo para Exchange 2013.
  
**La tabla 1. Ejemplos de agentes de transporte**

|**Nombre de ejemplo**|**Descripción**|
|:-----|:-----|
|[Exchange 2013: Crear a un agente de transporte antivirus](http://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-an-6e544269) <br/> |Este agente responde a los eventos [OnEndOfData](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnEndOfData.aspx) y [OnSubmittedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnSubmittedMessage.aspx) y envía el mensaje entrante a un servidor fuera de proceso que examina el mensaje y devuelve una versión modificada de forma asincrónica.  <br/> |
|[Exchange 2013: Crear a un agente de transporte de registro de ancho de banda](http://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-a-d61a4aaa) <br/> |Este agente responde a los eventos [OnSubmittedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnSubmittedMessage.aspx) y [OnRoutedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnRoutedMessage.aspx) , captura el uso de ancho de banda para los destinatarios especificados y registra la información de uso de ancho de banda en un archivo de texto.  <br/> |
|[Exchange 2013: Crear a un agente de transporte de conversión de cuerpo](http://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-a-body-ed36ecb0) <br/> |Este agente filtra las secuencias de comandos fuera de los mensajes de correo electrónico por determinar el formato del mensaje entrante y decidir si debe producirse el filtrado. Si es necesario el filtrado, el contenido se va a convertir a HTML, filtrado y, a continuación, se convierten al formato de origen.  <br/> |
|[Exchange 2013: Crear a un agente de transporte de registro de SMTP](http://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-an-fc23dc33) <br/> |Este agente responde al evento [OnEndOfData](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnEndOfData.aspx) y registros de forma asincrónica el mensaje a un archivo en el disco duro local.  <br/> |
|[Exchange 2013: Crear a un agente de transporte que bloquea temporalmente los remitentes](http://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-a-52a767d8) <br/> |Este agente responde a los eventos [OnEndOfHeaders](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnEndOfHeaders.aspx) y [OnRcptCommand](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnRcptCommand.aspx) y determina si el remitente del mensaje anteriormente ha enviado mensajes para el servicio de transporte Front-End. Si el remitente no ha enviado anteriormente un mensaje para el servicio de transporte Front-End, el remitente se agrega a una lista de remitentes y se rechaza el mensaje con una respuesta que indica al cliente que intente de nuevo más tarde (también conocido como graylisting). Si el remitente está en la lista de remitentes anteriores, el agente no rechazar el mensaje.  <br/> |
|[Exchange 2013: Crear a un agente de transporte de registro del servidor de buzón de correo](http://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-a-fc8632e5) <br/> |Este agente responde al evento de canalización de transporte [OnRoutedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnRoutedMessage.aspx) y registros de forma sincrónica el mensaje a un archivo en el disco duro local.  <br/> |
|[Exchange 2013: Crear a un agente de transporte de encabezado X](http://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-an-32f62f5a) <br/> |Este agente responde al evento [OnEndOfHeaders](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnEndOfHeaders.aspx) y lee y modifica encabezados X en los mensajes.  <br/> |
   
## <a name="see-also"></a>Vea también

- [Conceptos de agente en Exchange 2013 de transporte](transport-agent-concepts-in-exchange-2013.md)    
- [Referencia de agente de transporte de Exchange 2013](transport-agent-reference-for-exchange-2013.md)    
- [Crear a un agente de transporte RoutingAgent para Exchange 2013](how-to-create-a-routingagent-transport-agent-for-exchange-2013.md)   
- [Crear a un agente de transporte SmtpReceiveAgent para Exchange 2013](how-to-create-an-smtpreceiveagent-transport-agent-for-exchange-2013.md)    
- [Crear a un agente de transporte DeliveryAgent para Exchange 2013](how-to-create-a-deliveryagent-transport-agent-for-exchange-2013.md)
    

