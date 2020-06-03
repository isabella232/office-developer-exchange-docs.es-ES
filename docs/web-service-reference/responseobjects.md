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
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457441"
---
# <a name="responseobjects"></a><span data-ttu-id="6de92-103">ResponseObjects</span><span class="sxs-lookup"><span data-stu-id="6de92-103">ResponseObjects</span></span>

<span data-ttu-id="6de92-104">El elemento **ResponseObjects** contiene una colección de todos los objetos de respuesta que están asociados a un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="6de92-104">The **ResponseObjects** element contains a collection of all the response objects that are associated with an item in the Exchange store.</span></span> 
  
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

 <span data-ttu-id="6de92-105">**NonEmptyArrayOfResponseObjectsType**</span><span class="sxs-lookup"><span data-stu-id="6de92-105">**NonEmptyArrayOfResponseObjectsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6de92-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="6de92-106">Attributes and elements</span></span>

<span data-ttu-id="6de92-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="6de92-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6de92-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="6de92-108">Attributes</span></span>

<span data-ttu-id="6de92-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="6de92-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6de92-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="6de92-110">Child elements</span></span>

|<span data-ttu-id="6de92-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="6de92-111">**Element**</span></span>|<span data-ttu-id="6de92-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6de92-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6de92-113">AcceptItem</span><span class="sxs-lookup"><span data-stu-id="6de92-113">AcceptItem</span></span>](acceptitem.md) <br/> |<span data-ttu-id="6de92-114">Representa una respuesta de aceptación para una convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="6de92-114">Represents an Accept reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="6de92-115">TentativelyAcceptItem</span><span class="sxs-lookup"><span data-stu-id="6de92-115">TentativelyAcceptItem</span></span>](tentativelyacceptitem.md) <br/> |<span data-ttu-id="6de92-116">Representa una respuesta provisional a una convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="6de92-116">Represents a Tentative reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="6de92-117">DeclineItem</span><span class="sxs-lookup"><span data-stu-id="6de92-117">DeclineItem</span></span>](declineitem.md) <br/> |<span data-ttu-id="6de92-118">Representa una respuesta de rechazo a una convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="6de92-118">Represents a Decline reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="6de92-119">ReplyToItem</span><span class="sxs-lookup"><span data-stu-id="6de92-119">ReplyToItem</span></span>](replytoitem.md) <br/> |<span data-ttu-id="6de92-120">Contiene una respuesta al creador de un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="6de92-120">Contains a reply to the creator of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="6de92-121">ForwardItem</span><span class="sxs-lookup"><span data-stu-id="6de92-121">ForwardItem</span></span>](forwarditem.md) <br/> |<span data-ttu-id="6de92-122">Contiene un elemento de almacén de Exchange que se va a reenviar a los destinatarios.</span><span class="sxs-lookup"><span data-stu-id="6de92-122">Contains an Exchange store item to forward to recipients.</span></span>  <br/> |
|[<span data-ttu-id="6de92-123">ReplyAllToItem</span><span class="sxs-lookup"><span data-stu-id="6de92-123">ReplyAllToItem</span></span>](replyalltoitem.md) <br/> |<span data-ttu-id="6de92-124">Contiene una respuesta a todos los destinatarios identificados de un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="6de92-124">Contains a reply to all identified recipients of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="6de92-125">CancelCalendarItem</span><span class="sxs-lookup"><span data-stu-id="6de92-125">CancelCalendarItem</span></span>](cancelcalendaritem.md) <br/> |<span data-ttu-id="6de92-126">Representa el objeto de respuesta usado para cancelar una reunión.</span><span class="sxs-lookup"><span data-stu-id="6de92-126">Represents the response object used to cancel a meeting.</span></span>  <br/> |
|[<span data-ttu-id="6de92-127">RemoveItem</span><span class="sxs-lookup"><span data-stu-id="6de92-127">RemoveItem</span></span>](removeitem.md) <br/> |<span data-ttu-id="6de92-128">Quita un elemento del almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="6de92-128">Removes an item from the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="6de92-129">PostReplyItem</span><span class="sxs-lookup"><span data-stu-id="6de92-129">PostReplyItem</span></span>](postreplyitem.md) <br/> |<span data-ttu-id="6de92-130">Contiene una respuesta a un elemento post.</span><span class="sxs-lookup"><span data-stu-id="6de92-130">Contains a reply to a post item.</span></span> <span data-ttu-id="6de92-131">Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="6de92-131">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span>  <br/> |
|[<span data-ttu-id="6de92-132">SuppressReadReceipt</span><span class="sxs-lookup"><span data-stu-id="6de92-132">SuppressReadReceipt</span></span>](suppressreadreceipt.md) <br/> |<span data-ttu-id="6de92-133">Se usa para suprimir solicitudes de confirmación de lectura.</span><span class="sxs-lookup"><span data-stu-id="6de92-133">Used to suppress read receipt requests.</span></span>  <br/> |
|[<span data-ttu-id="6de92-134">AcceptSharingInvitation</span><span class="sxs-lookup"><span data-stu-id="6de92-134">AcceptSharingInvitation</span></span>](acceptsharinginvitation.md) <br/> |<span data-ttu-id="6de92-135">Se usa para aceptar una invitación que permite el acceso al calendario o los datos de contactos de otro usuario.</span><span class="sxs-lookup"><span data-stu-id="6de92-135">Used to accept an invitation that allows access to another user's calendar or contacts data.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="6de92-136">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="6de92-136">Parent elements</span></span>

|<span data-ttu-id="6de92-137">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="6de92-137">**Element**</span></span>|<span data-ttu-id="6de92-138">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6de92-138">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6de92-139">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="6de92-139">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="6de92-140">Representa un elemento de calendario de Exchange.</span><span class="sxs-lookup"><span data-stu-id="6de92-140">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="6de92-141">Contacto</span><span class="sxs-lookup"><span data-stu-id="6de92-141">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="6de92-142">Representa un elemento de contacto de Exchange.</span><span class="sxs-lookup"><span data-stu-id="6de92-142">Represents an Exchange contact item.</span></span>  <br/> |
|[<span data-ttu-id="6de92-143">DistributionList</span><span class="sxs-lookup"><span data-stu-id="6de92-143">DistributionList</span></span>](distributionlist.md) <br/> |<span data-ttu-id="6de92-144">Representa una lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="6de92-144">Represents a distribution list.</span></span>  <br/> |
|[<span data-ttu-id="6de92-145">Elemento</span><span class="sxs-lookup"><span data-stu-id="6de92-145">Item</span></span>](item.md) <br/> |<span data-ttu-id="6de92-146">Representa un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="6de92-146">Represents an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="6de92-147">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="6de92-147">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="6de92-148">Representa una cancelación de reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="6de92-148">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="6de92-149">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="6de92-149">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="6de92-150">Representa una reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="6de92-150">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="6de92-151">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="6de92-151">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="6de92-152">Representa una convocatoria de reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="6de92-152">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="6de92-153">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="6de92-153">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="6de92-154">Representa una respuesta a una reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="6de92-154">Represents a meeting response in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="6de92-155">Message</span><span class="sxs-lookup"><span data-stu-id="6de92-155">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="6de92-156">Representa un mensaje de correo electrónico de Exchange.</span><span class="sxs-lookup"><span data-stu-id="6de92-156">Represents an Exchange e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="6de92-157">RemoveItem</span><span class="sxs-lookup"><span data-stu-id="6de92-157">RemoveItem</span></span>](removeitem.md) <br/> |<span data-ttu-id="6de92-158">Quita un elemento del almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="6de92-158">Removes an item from the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="6de92-159">Tarea</span><span class="sxs-lookup"><span data-stu-id="6de92-159">Task</span></span>](task.md) <br/> |<span data-ttu-id="6de92-160">Representa una tarea del almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="6de92-160">Represents a task in the Exchange store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6de92-161">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6de92-161">Remarks</span></span>

<span data-ttu-id="6de92-162">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="6de92-162">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6de92-163">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="6de92-163">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6de92-164">Namespace</span><span class="sxs-lookup"><span data-stu-id="6de92-164">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="6de92-165">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="6de92-165">Schema Name</span></span>  <br/> |<span data-ttu-id="6de92-166">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="6de92-166">Types schema</span></span>  <br/> |
|<span data-ttu-id="6de92-167">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="6de92-167">Validation File</span></span>  <br/> |<span data-ttu-id="6de92-168">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="6de92-168">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="6de92-169">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="6de92-169">Can be Empty</span></span>  <br/> |<span data-ttu-id="6de92-170">Falso</span><span class="sxs-lookup"><span data-stu-id="6de92-170">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6de92-171">Vea también</span><span class="sxs-lookup"><span data-stu-id="6de92-171">See also</span></span>



- [<span data-ttu-id="6de92-172">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="6de92-172">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

