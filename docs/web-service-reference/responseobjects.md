---
title: ResponseObjects
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ResponseObjects
api_type:
- schema
ms.assetid: ad29e064-3f3d-4b7b-aa4c-9ec27326381d
description: El elemento ResponseObjects contiene una colección de todos los objetos de respuesta que están asociados a un elemento en el almacén de Exchange.
ms.openlocfilehash: 675bfda4addb38535736efc0c790577ff4739108
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457441"
---
# <a name="responseobjects"></a><span data-ttu-id="ff44f-103">ResponseObjects</span><span class="sxs-lookup"><span data-stu-id="ff44f-103">ResponseObjects</span></span>

<span data-ttu-id="ff44f-104">El elemento **ResponseObjects** contiene una colección de todos los objetos de respuesta que están asociados a un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="ff44f-104">The **ResponseObjects** element contains a collection of all the response objects that are associated with an item in the Exchange store.</span></span> 
  
```XML
<ResponseObjects>
   <AcceptItem/>
   <TentativelyAcceptItem/>
   <DeclineItem/>
   <ReplyToItem/>
   <ForwardItem/>
   <ReplyAllToItem/>
   <CancelCalendarItem/>
   <RemoveItem/>
   <PostReplyItem/>
   <SuppressReadReceipt/>
   <AcceptSharingInvitation/>
</ResponseObjects>
```

 <span data-ttu-id="ff44f-105">**NonEmptyArrayOfResponseObjectsType**</span><span class="sxs-lookup"><span data-stu-id="ff44f-105">**NonEmptyArrayOfResponseObjectsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ff44f-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="ff44f-106">Attributes and elements</span></span>

<span data-ttu-id="ff44f-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="ff44f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ff44f-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="ff44f-108">Attributes</span></span>

<span data-ttu-id="ff44f-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="ff44f-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ff44f-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ff44f-110">Child elements</span></span>

|<span data-ttu-id="ff44f-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="ff44f-111">**Element**</span></span>|<span data-ttu-id="ff44f-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ff44f-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ff44f-113">AcceptItem</span><span class="sxs-lookup"><span data-stu-id="ff44f-113">AcceptItem</span></span>](acceptitem.md) <br/> |<span data-ttu-id="ff44f-114">Representa una respuesta de aceptación para una convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="ff44f-114">Represents an Accept reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="ff44f-115">TentativelyAcceptItem</span><span class="sxs-lookup"><span data-stu-id="ff44f-115">TentativelyAcceptItem</span></span>](tentativelyacceptitem.md) <br/> |<span data-ttu-id="ff44f-116">Representa una respuesta provisional a una convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="ff44f-116">Represents a Tentative reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="ff44f-117">DeclineItem</span><span class="sxs-lookup"><span data-stu-id="ff44f-117">DeclineItem</span></span>](declineitem.md) <br/> |<span data-ttu-id="ff44f-118">Representa una respuesta de rechazo a una convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="ff44f-118">Represents a Decline reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="ff44f-119">ReplyToItem</span><span class="sxs-lookup"><span data-stu-id="ff44f-119">ReplyToItem</span></span>](replytoitem.md) <br/> |<span data-ttu-id="ff44f-120">Contiene una respuesta al creador de un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="ff44f-120">Contains a reply to the creator of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="ff44f-121">ForwardItem</span><span class="sxs-lookup"><span data-stu-id="ff44f-121">ForwardItem</span></span>](forwarditem.md) <br/> |<span data-ttu-id="ff44f-122">Contiene un elemento de almacén de Exchange que se va a reenviar a los destinatarios.</span><span class="sxs-lookup"><span data-stu-id="ff44f-122">Contains an Exchange store item to forward to recipients.</span></span>  <br/> |
|[<span data-ttu-id="ff44f-123">ReplyAllToItem</span><span class="sxs-lookup"><span data-stu-id="ff44f-123">ReplyAllToItem</span></span>](replyalltoitem.md) <br/> |<span data-ttu-id="ff44f-124">Contiene una respuesta a todos los destinatarios identificados de un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="ff44f-124">Contains a reply to all identified recipients of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="ff44f-125">CancelCalendarItem</span><span class="sxs-lookup"><span data-stu-id="ff44f-125">CancelCalendarItem</span></span>](cancelcalendaritem.md) <br/> |<span data-ttu-id="ff44f-126">Representa el objeto de respuesta usado para cancelar una reunión.</span><span class="sxs-lookup"><span data-stu-id="ff44f-126">Represents the response object used to cancel a meeting.</span></span>  <br/> |
|[<span data-ttu-id="ff44f-127">RemoveItem</span><span class="sxs-lookup"><span data-stu-id="ff44f-127">RemoveItem</span></span>](removeitem.md) <br/> |<span data-ttu-id="ff44f-128">Quita un elemento del almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="ff44f-128">Removes an item from the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="ff44f-129">PostReplyItem</span><span class="sxs-lookup"><span data-stu-id="ff44f-129">PostReplyItem</span></span>](postreplyitem.md) <br/> |<span data-ttu-id="ff44f-130">Contiene una respuesta a un elemento post.</span><span class="sxs-lookup"><span data-stu-id="ff44f-130">Contains a reply to a post item.</span></span> <span data-ttu-id="ff44f-131">Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="ff44f-131">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span>  <br/> |
|[<span data-ttu-id="ff44f-132">SuppressReadReceipt</span><span class="sxs-lookup"><span data-stu-id="ff44f-132">SuppressReadReceipt</span></span>](suppressreadreceipt.md) <br/> |<span data-ttu-id="ff44f-133">Se usa para suprimir solicitudes de confirmación de lectura.</span><span class="sxs-lookup"><span data-stu-id="ff44f-133">Used to suppress read receipt requests.</span></span>  <br/> |
|[<span data-ttu-id="ff44f-134">AcceptSharingInvitation</span><span class="sxs-lookup"><span data-stu-id="ff44f-134">AcceptSharingInvitation</span></span>](acceptsharinginvitation.md) <br/> |<span data-ttu-id="ff44f-135">Se usa para aceptar una invitación que permite el acceso al calendario o los datos de contactos de otro usuario.</span><span class="sxs-lookup"><span data-stu-id="ff44f-135">Used to accept an invitation that allows access to another user's calendar or contacts data.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ff44f-136">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="ff44f-136">Parent elements</span></span>

|<span data-ttu-id="ff44f-137">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="ff44f-137">**Element**</span></span>|<span data-ttu-id="ff44f-138">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ff44f-138">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ff44f-139">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="ff44f-139">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="ff44f-140">Representa un elemento de calendario de Exchange.</span><span class="sxs-lookup"><span data-stu-id="ff44f-140">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="ff44f-141">Contacto</span><span class="sxs-lookup"><span data-stu-id="ff44f-141">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="ff44f-142">Representa un elemento de contacto de Exchange.</span><span class="sxs-lookup"><span data-stu-id="ff44f-142">Represents an Exchange contact item.</span></span>  <br/> |
|[<span data-ttu-id="ff44f-143">DistributionList</span><span class="sxs-lookup"><span data-stu-id="ff44f-143">DistributionList</span></span>](distributionlist.md) <br/> |<span data-ttu-id="ff44f-144">Representa una lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="ff44f-144">Represents a distribution list.</span></span>  <br/> |
|[<span data-ttu-id="ff44f-145">Elemento</span><span class="sxs-lookup"><span data-stu-id="ff44f-145">Item</span></span>](item.md) <br/> |<span data-ttu-id="ff44f-146">Representa un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="ff44f-146">Represents an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="ff44f-147">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="ff44f-147">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="ff44f-148">Representa una cancelación de reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="ff44f-148">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="ff44f-149">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="ff44f-149">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="ff44f-150">Representa una reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="ff44f-150">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="ff44f-151">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="ff44f-151">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="ff44f-152">Representa una convocatoria de reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="ff44f-152">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="ff44f-153">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="ff44f-153">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="ff44f-154">Representa una respuesta a una reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="ff44f-154">Represents a meeting response in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="ff44f-155">Mensaje</span><span class="sxs-lookup"><span data-stu-id="ff44f-155">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="ff44f-156">Representa un mensaje de correo electrónico de Exchange.</span><span class="sxs-lookup"><span data-stu-id="ff44f-156">Represents an Exchange e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="ff44f-157">RemoveItem</span><span class="sxs-lookup"><span data-stu-id="ff44f-157">RemoveItem</span></span>](removeitem.md) <br/> |<span data-ttu-id="ff44f-158">Quita un elemento del almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="ff44f-158">Removes an item from the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="ff44f-159">Tarea</span><span class="sxs-lookup"><span data-stu-id="ff44f-159">Task</span></span>](task.md) <br/> |<span data-ttu-id="ff44f-160">Representa una tarea del almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="ff44f-160">Represents a task in the Exchange store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ff44f-161">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ff44f-161">Remarks</span></span>

<span data-ttu-id="ff44f-162">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="ff44f-162">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ff44f-163">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="ff44f-163">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ff44f-164">Namespace</span><span class="sxs-lookup"><span data-stu-id="ff44f-164">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ff44f-165">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="ff44f-165">Schema Name</span></span>  <br/> |<span data-ttu-id="ff44f-166">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="ff44f-166">Types schema</span></span>  <br/> |
|<span data-ttu-id="ff44f-167">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="ff44f-167">Validation File</span></span>  <br/> |<span data-ttu-id="ff44f-168">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="ff44f-168">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="ff44f-169">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="ff44f-169">Can be Empty</span></span>  <br/> |<span data-ttu-id="ff44f-170">Falso</span><span class="sxs-lookup"><span data-stu-id="ff44f-170">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ff44f-171">Vea también</span><span class="sxs-lookup"><span data-stu-id="ff44f-171">See also</span></span>



- [<span data-ttu-id="ff44f-172">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="ff44f-172">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

