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
# <a name="transport-agent-code-samples-for-exchange-2013"></a><span data-ttu-id="0096e-103">Ejemplos de código de agente para Exchange 2013 de transporte</span><span class="sxs-lookup"><span data-stu-id="0096e-103">Transport agent code samples for Exchange 2013</span></span>

<span data-ttu-id="0096e-104">Obtenga información acerca de los agentes de transporte de ejemplo que están disponibles para Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="0096e-104">Find information about the sample transport agents that are available for Exchange 2013.</span></span>
  
<span data-ttu-id="0096e-105">**Se aplica a:** Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="0096e-105">**Applies to:** Exchange Server 2013</span></span>
  
<span data-ttu-id="0096e-106">Puede usar las API que se incluyen en Exchange Server 2013 para desarrollar a los agentes que amplían la funcionalidad de transporte.</span><span class="sxs-lookup"><span data-stu-id="0096e-106">You can use the APIs that are included in Exchange Server 2013 to develop agents that extend transport functionality.</span></span> <span data-ttu-id="0096e-107">En este artículo se proporciona información acerca de los agentes de ejemplo que están disponibles para ayudarle a aprender a extender mediante programación el comportamiento de transporte.</span><span class="sxs-lookup"><span data-stu-id="0096e-107">This article provides information about the sample agents that are available to help you to learn how to extend transport behavior programmatically.</span></span> <span data-ttu-id="0096e-108">Los agentes de ejemplo incluyen el código fuente para cada componente.</span><span class="sxs-lookup"><span data-stu-id="0096e-108">The sample agents include the source code for each component.</span></span> 
  
<span data-ttu-id="0096e-109">En la siguiente tabla se enumera a los agentes de ejemplo para Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="0096e-109">The following table lists the sample agents for Exchange 2013.</span></span>
  
<span data-ttu-id="0096e-110">**La tabla 1. Ejemplos de agentes de transporte**</span><span class="sxs-lookup"><span data-stu-id="0096e-110">**Table 1. Transport agent samples**</span></span>

|<span data-ttu-id="0096e-111">**Nombre de ejemplo**</span><span class="sxs-lookup"><span data-stu-id="0096e-111">**Sample name**</span></span>|<span data-ttu-id="0096e-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0096e-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0096e-113">Exchange 2013: Crear a un agente de transporte antivirus</span><span class="sxs-lookup"><span data-stu-id="0096e-113">Exchange 2013: Build an antivirus transport agent</span></span>](http://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-an-6e544269) <br/> |<span data-ttu-id="0096e-114">Este agente responde a los eventos [OnEndOfData](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnEndOfData.aspx) y [OnSubmittedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnSubmittedMessage.aspx) y envía el mensaje entrante a un servidor fuera de proceso que examina el mensaje y devuelve una versión modificada de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="0096e-114">This agent responds to the [OnEndOfData](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnEndOfData.aspx) and [OnSubmittedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnSubmittedMessage.aspx) events and sends the incoming message to an out-of-process server that asynchronously examines the message and returns a modified version.</span></span>  <br/> |
|[<span data-ttu-id="0096e-115">Exchange 2013: Crear a un agente de transporte de registro de ancho de banda</span><span class="sxs-lookup"><span data-stu-id="0096e-115">Exchange 2013: Build a bandwidth logging transport agent</span></span>](http://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-a-d61a4aaa) <br/> |<span data-ttu-id="0096e-116">Este agente responde a los eventos [OnSubmittedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnSubmittedMessage.aspx) y [OnRoutedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnRoutedMessage.aspx) , captura el uso de ancho de banda para los destinatarios especificados y registra la información de uso de ancho de banda en un archivo de texto.</span><span class="sxs-lookup"><span data-stu-id="0096e-116">This agent responds to the [OnSubmittedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnSubmittedMessage.aspx) and [OnRoutedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnRoutedMessage.aspx) events, captures bandwidth usage for specified recipients, and logs the bandwidth usage information to a text file.</span></span>  <br/> |
|[<span data-ttu-id="0096e-117">Exchange 2013: Crear a un agente de transporte de conversión de cuerpo</span><span class="sxs-lookup"><span data-stu-id="0096e-117">Exchange 2013: Build a body conversion transport agent</span></span>](http://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-a-body-ed36ecb0) <br/> |<span data-ttu-id="0096e-118">Este agente filtra las secuencias de comandos fuera de los mensajes de correo electrónico por determinar el formato del mensaje entrante y decidir si debe producirse el filtrado.</span><span class="sxs-lookup"><span data-stu-id="0096e-118">This agent filters scripts out of email messages by determining the format of the incoming message and deciding if filtering must occur.</span></span> <span data-ttu-id="0096e-119">Si es necesario el filtrado, el contenido se va a convertir a HTML, filtrado y, a continuación, se convierten al formato de origen.</span><span class="sxs-lookup"><span data-stu-id="0096e-119">If filtering is needed, the content is converted to HTML, filtered, and then converted back to the source format.</span></span>  <br/> |
|[<span data-ttu-id="0096e-120">Exchange 2013: Crear a un agente de transporte de registro de SMTP</span><span class="sxs-lookup"><span data-stu-id="0096e-120">Exchange 2013: Build an SMTP logging transport agent</span></span>](http://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-an-fc23dc33) <br/> |<span data-ttu-id="0096e-121">Este agente responde al evento [OnEndOfData](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnEndOfData.aspx) y registros de forma asincrónica el mensaje a un archivo en el disco duro local.</span><span class="sxs-lookup"><span data-stu-id="0096e-121">This agent responds to the [OnEndOfData](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnEndOfData.aspx) event, and asynchronously logs the message to a file on the local hard disk.</span></span>  <br/> |
|[<span data-ttu-id="0096e-122">Exchange 2013: Crear a un agente de transporte que bloquea temporalmente los remitentes</span><span class="sxs-lookup"><span data-stu-id="0096e-122">Exchange 2013: Build a transport agent that blocks senders temporarily</span></span>](http://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-a-52a767d8) <br/> |<span data-ttu-id="0096e-123">Este agente responde a los eventos [OnEndOfHeaders](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnEndOfHeaders.aspx) y [OnRcptCommand](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnRcptCommand.aspx) y determina si el remitente del mensaje anteriormente ha enviado mensajes para el servicio de transporte Front-End.</span><span class="sxs-lookup"><span data-stu-id="0096e-123">This agent responds to the [OnEndOfHeaders](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnEndOfHeaders.aspx) and [OnRcptCommand](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnRcptCommand.aspx) events and determines whether the message sender has previously sent messages to the Front End Transport service.</span></span> <span data-ttu-id="0096e-124">Si el remitente no ha enviado anteriormente un mensaje para el servicio de transporte Front-End, el remitente se agrega a una lista de remitentes y se rechaza el mensaje con una respuesta que indica al cliente que intente de nuevo más tarde (también conocido como graylisting).</span><span class="sxs-lookup"><span data-stu-id="0096e-124">If the sender has not previously sent a message to the Front End Transport service, the sender is added to a list of senders, and the message is rejected with a response that tells the client to try again later (also known as graylisting).</span></span> <span data-ttu-id="0096e-125">Si el remitente está en la lista de remitentes anteriores, el agente no rechazar el mensaje.</span><span class="sxs-lookup"><span data-stu-id="0096e-125">If the sender is in the list of previous senders, the agent does not reject the message.</span></span>  <br/> |
|[<span data-ttu-id="0096e-126">Exchange 2013: Crear a un agente de transporte de registro del servidor de buzón de correo</span><span class="sxs-lookup"><span data-stu-id="0096e-126">Exchange 2013: Build a Mailbox server logging transport agent</span></span>](http://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-a-fc8632e5) <br/> |<span data-ttu-id="0096e-127">Este agente responde al evento de canalización de transporte [OnRoutedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnRoutedMessage.aspx) y registros de forma sincrónica el mensaje a un archivo en el disco duro local.</span><span class="sxs-lookup"><span data-stu-id="0096e-127">This agent responds to the [OnRoutedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnRoutedMessage.aspx) transport pipeline event and synchronously logs the message to a file on the local hard disk.</span></span>  <br/> |
|[<span data-ttu-id="0096e-128">Exchange 2013: Crear a un agente de transporte de encabezado X</span><span class="sxs-lookup"><span data-stu-id="0096e-128">Exchange 2013: Build an X-header transport agent</span></span>](http://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-an-32f62f5a) <br/> |<span data-ttu-id="0096e-129">Este agente responde al evento [OnEndOfHeaders](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnEndOfHeaders.aspx) y lee y modifica encabezados X en los mensajes.</span><span class="sxs-lookup"><span data-stu-id="0096e-129">This agent responds to the [OnEndOfHeaders](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnEndOfHeaders.aspx) event and read and modify X-headers in messages.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0096e-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="0096e-130">See also</span></span>

- [<span data-ttu-id="0096e-131">Conceptos de agente en Exchange 2013 de transporte</span><span class="sxs-lookup"><span data-stu-id="0096e-131">Transport agent concepts in Exchange 2013</span></span>](transport-agent-concepts-in-exchange-2013.md)    
- [<span data-ttu-id="0096e-132">Referencia de agente de transporte de Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="0096e-132">Transport agent reference for Exchange 2013</span></span>](transport-agent-reference-for-exchange-2013.md)    
- [<span data-ttu-id="0096e-133">Crear a un agente de transporte RoutingAgent para Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="0096e-133">Create a RoutingAgent transport agent for Exchange 2013</span></span>](how-to-create-a-routingagent-transport-agent-for-exchange-2013.md)   
- [<span data-ttu-id="0096e-134">Crear a un agente de transporte SmtpReceiveAgent para Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="0096e-134">Create an SmtpReceiveAgent transport agent for Exchange 2013</span></span>](how-to-create-an-smtpreceiveagent-transport-agent-for-exchange-2013.md)    
- [<span data-ttu-id="0096e-135">Crear a un agente de transporte DeliveryAgent para Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="0096e-135">Create a DeliveryAgent transport agent for Exchange 2013</span></span>](how-to-create-a-deliveryagent-transport-agent-for-exchange-2013.md)
    
