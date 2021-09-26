---
title: Ejemplos de código de agente de transporte Exchange 2013
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 626345ec-918f-4d91-932f-e6ce92553ccb
description: Busque información sobre los agentes de transporte de ejemplo que están disponibles para Exchange 2013.
ms.openlocfilehash: 56334f661947cffceaf18eb257feeb6504a71ecb
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59545722"
---
# <a name="transport-agent-code-samples-for-exchange-2013"></a>Ejemplos de código de agente de transporte Exchange 2013

Busque información sobre los agentes de transporte de ejemplo que están disponibles para Exchange 2013.
  
**Se aplica a:** Exchange Server 2013
  
Puede usar las API que se incluyen en Exchange Server 2013 para desarrollar agentes que amplíen la funcionalidad de transporte. En este artículo se proporciona información sobre los agentes de ejemplo que están disponibles para ayudarle a aprender a extender el comportamiento de transporte mediante programación. Los agentes de ejemplo incluyen el código fuente de cada componente. 
  
En la tabla siguiente se enumeran los agentes de ejemplo Exchange 2013.
  
**Tabla 1. Ejemplos de agentes de transporte**

|**Ejemplo de nombre**|**Descripción**|
|:-----|:-----|
|[Exchange 2013: crear un agente de transporte antivirus](https://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-an-6e544269) <br/> |Este agente responde a los eventos [OnEndOfData](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnEndOfData.aspx) y [OnSubmittedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnSubmittedMessage.aspx) y envía el mensaje entrante a un servidor fuera de proceso que examina de forma asincrónica el mensaje y devuelve una versión modificada.  <br/> |
|[Exchange 2013: crear un agente de transporte de registro de ancho de banda](https://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-a-d61a4aaa) <br/> |Este agente responde a los eventos [OnSubmittedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnSubmittedMessage.aspx) y [OnRoutedMessage,](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnRoutedMessage.aspx) captura el uso de ancho de banda para destinatarios especificados y registra la información de uso de ancho de banda en un archivo de texto.  <br/> |
|[Exchange 2013: crear un agente de transporte de conversión de cuerpo](https://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-a-body-ed36ecb0) <br/> |Este agente filtra los scripts de los mensajes de correo electrónico determinando el formato del mensaje entrante y decidiendo si debe producirse el filtrado. Si es necesario el filtrado, el contenido se convierte en HTML, se filtra y, a continuación, se convierte al formato de origen.  <br/> |
|[Exchange 2013: crear un agente de transporte de registro SMTP](https://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-an-fc23dc33) <br/> |Este agente responde al evento [OnEndOfData](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnEndOfData.aspx) y registra de forma asincrónica el mensaje en un archivo en el disco duro local.  <br/> |
|[Exchange 2013: crear un agente de transporte que bloquee los remitentes temporalmente](https://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-a-52a767d8) <br/> |Este agente responde a los eventos [OnEndOfHeaders](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnEndOfHeaders.aspx) y [OnRcptCommand](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnRcptCommand.aspx) y determina si el remitente del mensaje ha enviado mensajes previamente al servicio de transporte front-end. Si el remitente no ha enviado previamente un mensaje al servicio de transporte front-end, el remitente se agrega a una lista de remitentes y el mensaje se rechaza con una respuesta que indica al cliente que vuelva a intentarlo más adelante (también conocido como lista gris). Si el remitente está en la lista de remitentes anteriores, el agente no rechaza el mensaje.  <br/> |
|[Exchange 2013: crear un agente de transporte de registro de servidor de buzones](https://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-a-fc8632e5) <br/> |Este agente responde al evento de canalización de transporte [OnRoutedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnRoutedMessage.aspx) y registra sincrónicamente el mensaje en un archivo en el disco duro local.  <br/> |
|[Exchange 2013: crear un agente de transporte de encabezado X](https://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-an-32f62f5a) <br/> |Este agente responde al evento [OnEndOfHeaders](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnEndOfHeaders.aspx) y lee y modifica los encabezados X en los mensajes.  <br/> |
   
## <a name="see-also"></a>Consulte también

- [Conceptos de agente de transporte Exchange 2013](transport-agent-concepts-in-exchange-2013.md)    
- [Referencia de agente de transporte para Exchange 2013](transport-agent-reference-for-exchange-2013.md)    
- [Crear un agente de transporte RoutingAgent para Exchange 2013](how-to-create-a-routingagent-transport-agent-for-exchange-2013.md)   
- [Crear un agente de transporte SmtpReceiveAgent para Exchange 2013](how-to-create-an-smtpreceiveagent-transport-agent-for-exchange-2013.md)    
- [Crear un agente de transporte DeliveryAgent para Exchange 2013](how-to-create-a-deliveryagent-transport-agent-for-exchange-2013.md)
    

