---
title: De
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- From
api_type:
- schema
ms.assetid: 5a52d644-3677-4049-874c-12bd5c3080dc
description: El elemento From representa la dirección desde la que se envió el mensaje.
ms.openlocfilehash: 39c8c8ef84ff445e8f44ebb9f2285ccfc42353a7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764728"
---
# <a name="from"></a><span data-ttu-id="dddab-103">De</span><span class="sxs-lookup"><span data-stu-id="dddab-103">From</span></span>

<span data-ttu-id="dddab-104">El elemento **de** representa la dirección desde la que se envió el mensaje.</span><span class="sxs-lookup"><span data-stu-id="dddab-104">The **From** element represents the address from which the message was sent.</span></span> 
  
```xml
<From>
   <Mailbox/>
</From>
```

 <span data-ttu-id="dddab-105">**SingleRecipientType**</span><span class="sxs-lookup"><span data-stu-id="dddab-105">**SingleRecipientType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="dddab-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="dddab-106">Attributes and elements</span></span>

<span data-ttu-id="dddab-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="dddab-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="dddab-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="dddab-108">Attributes</span></span>

<span data-ttu-id="dddab-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="dddab-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="dddab-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="dddab-110">Child elements</span></span>

|<span data-ttu-id="dddab-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="dddab-111">**Element**</span></span>|<span data-ttu-id="dddab-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="dddab-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="dddab-113">Buzón de correo</span><span class="sxs-lookup"><span data-stu-id="dddab-113">Mailbox</span></span>](mailbox.md) <br/> |<span data-ttu-id="dddab-114">Identifica un objeto de servicio de directorio de Active Directory habilitados para correo.</span><span class="sxs-lookup"><span data-stu-id="dddab-114">Identifies a mail-enabled Active Directory directory service object.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="dddab-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="dddab-115">Parent elements</span></span>

|<span data-ttu-id="dddab-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="dddab-116">**Element**</span></span>|<span data-ttu-id="dddab-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="dddab-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="dddab-118">RemoveItem</span><span class="sxs-lookup"><span data-stu-id="dddab-118">RemoveItem</span></span>](removeitem.md) <br/> |<span data-ttu-id="dddab-119">Quita un elemento desde el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="dddab-119">Removes an item from the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="dddab-120">Message</span><span class="sxs-lookup"><span data-stu-id="dddab-120">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="dddab-121">Representa un mensaje de correo electrónico de Exchange.</span><span class="sxs-lookup"><span data-stu-id="dddab-121">Represents an Exchange e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="dddab-122">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="dddab-122">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="dddab-123">Representa una reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="dddab-123">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="dddab-124">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="dddab-124">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="dddab-125">Representa una convocatoria de reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="dddab-125">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="dddab-126">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="dddab-126">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="dddab-127">Representa una respuesta a la reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="dddab-127">Represents a meeting response in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="dddab-128">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="dddab-128">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="dddab-129">Representa la cancelación de la reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="dddab-129">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="dddab-130">AcceptItem</span><span class="sxs-lookup"><span data-stu-id="dddab-130">AcceptItem</span></span>](acceptitem.md) <br/> |<span data-ttu-id="dddab-131">Representa una respuesta a Aceptar a una convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="dddab-131">Represents an Accept reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="dddab-132">TentativelyAcceptItem</span><span class="sxs-lookup"><span data-stu-id="dddab-132">TentativelyAcceptItem</span></span>](tentativelyacceptitem.md) <br/> |<span data-ttu-id="dddab-133">Representa un provisional responde a una convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="dddab-133">Represents a Tentative reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="dddab-134">DeclineItem</span><span class="sxs-lookup"><span data-stu-id="dddab-134">DeclineItem</span></span>](declineitem.md) <br/> |<span data-ttu-id="dddab-135">Representa una respuesta de rechazo a una convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="dddab-135">Represents a Decline reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="dddab-136">ReplyToItem</span><span class="sxs-lookup"><span data-stu-id="dddab-136">ReplyToItem</span></span>](replytoitem.md) <br/> |<span data-ttu-id="dddab-137">Contiene una respuesta para el creador de un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="dddab-137">Contains a reply to the creator of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="dddab-138">ReplyAllToItem</span><span class="sxs-lookup"><span data-stu-id="dddab-138">ReplyAllToItem</span></span>](replyalltoitem.md) <br/> |<span data-ttu-id="dddab-139">Contiene una respuesta para todos los destinatarios identificados de un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="dddab-139">Contains a reply to all identified recipients of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="dddab-140">ForwardItem</span><span class="sxs-lookup"><span data-stu-id="dddab-140">ForwardItem</span></span>](forwarditem.md) <br/> |<span data-ttu-id="dddab-141">Contiene un elemento del almacén de Exchange reenviar a los destinatarios.</span><span class="sxs-lookup"><span data-stu-id="dddab-141">Contains an Exchange store item to forward to recipients.</span></span>  <br/> |
|[<span data-ttu-id="dddab-142">CancelCalendarItem</span><span class="sxs-lookup"><span data-stu-id="dddab-142">CancelCalendarItem</span></span>](cancelcalendaritem.md) <br/> |<span data-ttu-id="dddab-143">Representa el objeto de respuesta que se usa para cancelar una reunión.</span><span class="sxs-lookup"><span data-stu-id="dddab-143">Represents the response object that is used to cancel a meeting.</span></span>  <br/> |
|[<span data-ttu-id="dddab-144">Objeto postItem</span><span class="sxs-lookup"><span data-stu-id="dddab-144">PostItem</span></span>](postitem.md) <br/> |<span data-ttu-id="dddab-145">Representa un elemento para exponer en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="dddab-145">Represents a post item in the Exchange store.</span></span> <span data-ttu-id="dddab-146">Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="dddab-146">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dddab-147">Comentarios</span><span class="sxs-lookup"><span data-stu-id="dddab-147">Remarks</span></span>

<span data-ttu-id="dddab-148">Este elemento se utiliza para mensajes de correo electrónico "enviar en nombre de".</span><span class="sxs-lookup"><span data-stu-id="dddab-148">This element is used for "send on behalf of" e-mails.</span></span>
  
<span data-ttu-id="dddab-149">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="dddab-149">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="dddab-150">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="dddab-150">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="dddab-151">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="dddab-151">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="dddab-152">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="dddab-152">Schema Name</span></span>  <br/> |<span data-ttu-id="dddab-153">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="dddab-153">Types schema</span></span>  <br/> |
|<span data-ttu-id="dddab-154">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="dddab-154">Validation File</span></span>  <br/> |<span data-ttu-id="dddab-155">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="dddab-155">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="dddab-156">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="dddab-156">Can be Empty</span></span>  <br/> |<span data-ttu-id="dddab-157">False</span><span class="sxs-lookup"><span data-stu-id="dddab-157">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="dddab-158">Vea también</span><span class="sxs-lookup"><span data-stu-id="dddab-158">See also</span></span>



- [<span data-ttu-id="dddab-159">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="dddab-159">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

