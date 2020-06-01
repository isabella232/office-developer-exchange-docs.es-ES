---
title: ConversationIndex
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ConversationIndex
api_type:
- schema
ms.assetid: fdf47e22-8d93-4ae4-883b-0c9f07f48724
description: El elemento ConversationIndex contiene un identificador binario que representa el subproceso al que pertenece el mensaje.
ms.openlocfilehash: 03874c6462be6380e34c999bc2354c376a462882
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461439"
---
# <a name="conversationindex"></a><span data-ttu-id="44b3a-103">ConversationIndex</span><span class="sxs-lookup"><span data-stu-id="44b3a-103">ConversationIndex</span></span>

<span data-ttu-id="44b3a-104">El elemento **ConversationIndex** contiene un identificador binario que representa el subproceso al que pertenece el mensaje.</span><span class="sxs-lookup"><span data-stu-id="44b3a-104">The **ConversationIndex** element contains a binary ID that represents the thread to which this message belongs.</span></span> 
  
```xml
<ConversationIndex/>
```

 <span data-ttu-id="44b3a-105">**Base64Binary**</span><span class="sxs-lookup"><span data-stu-id="44b3a-105">**Base64Binary**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="44b3a-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="44b3a-106">Attributes and elements</span></span>

<span data-ttu-id="44b3a-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="44b3a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="44b3a-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="44b3a-108">Attributes</span></span>

<span data-ttu-id="44b3a-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="44b3a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="44b3a-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="44b3a-110">Child elements</span></span>

<span data-ttu-id="44b3a-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="44b3a-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="44b3a-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="44b3a-112">Parent elements</span></span>

|<span data-ttu-id="44b3a-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="44b3a-113">**Element**</span></span>|<span data-ttu-id="44b3a-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="44b3a-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="44b3a-115">RemoveItem</span><span class="sxs-lookup"><span data-stu-id="44b3a-115">RemoveItem</span></span>](removeitem.md) <br/> |<span data-ttu-id="44b3a-116">Quita un elemento del almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="44b3a-116">Removes an item from the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="44b3a-117">Mensaje</span><span class="sxs-lookup"><span data-stu-id="44b3a-117">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="44b3a-118">Representa un mensaje de correo electrónico de Exchange.</span><span class="sxs-lookup"><span data-stu-id="44b3a-118">Represents an Exchange e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="44b3a-119">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="44b3a-119">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="44b3a-120">Representa una reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="44b3a-120">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="44b3a-121">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="44b3a-121">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="44b3a-122">Representa una convocatoria de reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="44b3a-122">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="44b3a-123">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="44b3a-123">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="44b3a-124">Representa una respuesta a una reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="44b3a-124">Represents a meeting response in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="44b3a-125">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="44b3a-125">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="44b3a-126">Representa una cancelación de reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="44b3a-126">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="44b3a-127">AcceptItem</span><span class="sxs-lookup"><span data-stu-id="44b3a-127">AcceptItem</span></span>](acceptitem.md) <br/> |<span data-ttu-id="44b3a-128">Representa una respuesta de aceptación para una convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="44b3a-128">Represents an Accept reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="44b3a-129">TentativelyAcceptItem</span><span class="sxs-lookup"><span data-stu-id="44b3a-129">TentativelyAcceptItem</span></span>](tentativelyacceptitem.md) <br/> |<span data-ttu-id="44b3a-130">Representa una respuesta aceptada provisionalmente a una convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="44b3a-130">Represents a tentatively accepted reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="44b3a-131">DeclineItem</span><span class="sxs-lookup"><span data-stu-id="44b3a-131">DeclineItem</span></span>](declineitem.md) <br/> |<span data-ttu-id="44b3a-132">Representa una respuesta de rechazo a una convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="44b3a-132">Represents a Decline reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="44b3a-133">ReplyToItem</span><span class="sxs-lookup"><span data-stu-id="44b3a-133">ReplyToItem</span></span>](replytoitem.md) <br/> |<span data-ttu-id="44b3a-134">Contiene una respuesta al creador de un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="44b3a-134">Contains a reply to the creator of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="44b3a-135">ReplyAllToItem</span><span class="sxs-lookup"><span data-stu-id="44b3a-135">ReplyAllToItem</span></span>](replyalltoitem.md) <br/> |<span data-ttu-id="44b3a-136">Contiene una respuesta a todos los destinatarios identificados de un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="44b3a-136">Contains a reply to all identified recipients of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="44b3a-137">ForwardItem</span><span class="sxs-lookup"><span data-stu-id="44b3a-137">ForwardItem</span></span>](forwarditem.md) <br/> |<span data-ttu-id="44b3a-138">Contiene un elemento de almacén de Exchange que se va a reenviar a los destinatarios.</span><span class="sxs-lookup"><span data-stu-id="44b3a-138">Contains an Exchange store item to forward to recipients.</span></span>  <br/> |
|[<span data-ttu-id="44b3a-139">CancelCalendarItem</span><span class="sxs-lookup"><span data-stu-id="44b3a-139">CancelCalendarItem</span></span>](cancelcalendaritem.md) <br/> |<span data-ttu-id="44b3a-140">Representa el objeto de respuesta que se usa para cancelar una reunión.</span><span class="sxs-lookup"><span data-stu-id="44b3a-140">Represents the response object that is used to cancel a meeting.</span></span>  <br/> |
|[<span data-ttu-id="44b3a-141">PostItem</span><span class="sxs-lookup"><span data-stu-id="44b3a-141">PostItem</span></span>](postitem.md) <br/> |<span data-ttu-id="44b3a-142">Representa un elemento post en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="44b3a-142">Represents a post item in the Exchange store.</span></span> <span data-ttu-id="44b3a-143">Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="44b3a-143">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="44b3a-144">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="44b3a-144">Text value</span></span>

<span data-ttu-id="44b3a-145">El valor de texto representa un identificador binario en formato **Base64Binary** .</span><span class="sxs-lookup"><span data-stu-id="44b3a-145">The text value represents a binary identifier in **Base64Binary** format.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="44b3a-146">Comentarios</span><span class="sxs-lookup"><span data-stu-id="44b3a-146">Remarks</span></span>

<span data-ttu-id="44b3a-147">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del servidor de Exchange que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="44b3a-147">The schema that describes this element is located in the EWS virtual directory of the Exchange server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="44b3a-148">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="44b3a-148">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="44b3a-149">Namespace</span><span class="sxs-lookup"><span data-stu-id="44b3a-149">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="44b3a-150">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="44b3a-150">Schema Name</span></span>  <br/> |<span data-ttu-id="44b3a-151">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="44b3a-151">Types schema</span></span>  <br/> |
|<span data-ttu-id="44b3a-152">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="44b3a-152">Validation File</span></span>  <br/> |<span data-ttu-id="44b3a-153">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="44b3a-153">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="44b3a-154">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="44b3a-154">Can be Empty</span></span>  <br/> |<span data-ttu-id="44b3a-155">Falso</span><span class="sxs-lookup"><span data-stu-id="44b3a-155">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="44b3a-156">Vea también</span><span class="sxs-lookup"><span data-stu-id="44b3a-156">See also</span></span>



- [<span data-ttu-id="44b3a-157">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="44b3a-157">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

