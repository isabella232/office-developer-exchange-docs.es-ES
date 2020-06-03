---
title: CancelCalendarItem
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CancelCalendarItem
api_type:
- schema
ms.assetid: a2046402-a176-44d5-b4b3-adb696581935
description: El elemento CancelCalendarItem representa el objeto de respuesta que se usa para cancelar una reunión.
ms.openlocfilehash: 45ad76d19bd43e2081aa9b9eb63547e091014803
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462258"
---
# <a name="cancelcalendaritem"></a><span data-ttu-id="f84fc-103">CancelCalendarItem</span><span class="sxs-lookup"><span data-stu-id="f84fc-103">CancelCalendarItem</span></span>

<span data-ttu-id="f84fc-104">El elemento **CancelCalendarItem** representa el objeto de respuesta que se usa para cancelar una reunión.</span><span class="sxs-lookup"><span data-stu-id="f84fc-104">The **CancelCalendarItem** element represents the response object that is used to cancel a meeting.</span></span> 
  
```xml
<CancelCalendarItem>
   <Subject/>
   <Body/>
   <ToRecipients/>
   <CcRecipients/>
   <BccRecipients/>
   <IsReadReceiptRequested/>
   <IsDeliveryReceiptRequested/>
   <ReferenceItemId/>
   <NewBodyContent/>
   <ReceivedBy/>
   <ReceivedRepresenting/>
</CancelCalendarItem>
```

 <span data-ttu-id="f84fc-105">**CancelCalendarItemType**</span><span class="sxs-lookup"><span data-stu-id="f84fc-105">**CancelCalendarItemType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f84fc-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="f84fc-106">Attributes and elements</span></span>

<span data-ttu-id="f84fc-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="f84fc-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f84fc-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="f84fc-108">Attributes</span></span>

<span data-ttu-id="f84fc-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="f84fc-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f84fc-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="f84fc-110">Child elements</span></span>

|<span data-ttu-id="f84fc-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="f84fc-111">**Element**</span></span>|<span data-ttu-id="f84fc-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f84fc-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f84fc-113">Asunto</span><span class="sxs-lookup"><span data-stu-id="f84fc-113">Subject</span></span>](subject.md) <br/> |<span data-ttu-id="f84fc-114">Representa la propiedad Subject de los elementos del almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="f84fc-114">Represents the subject property of Exchange store items.</span></span>  <br/> |
|[<span data-ttu-id="f84fc-115">Body</span><span class="sxs-lookup"><span data-stu-id="f84fc-115">Body</span></span>](body.md) <br/> |<span data-ttu-id="f84fc-116">No se usa en **CancelCalendarItem**.</span><span class="sxs-lookup"><span data-stu-id="f84fc-116">Not used by **CancelCalendarItem**.</span></span> <span data-ttu-id="f84fc-117">Use la propiedad [NewBodyContent](newbodycontent.md) para establecer el contenido del cuerpo.</span><span class="sxs-lookup"><span data-stu-id="f84fc-117">Use the [NewBodyContent](newbodycontent.md) property to set the body content.</span></span>  <br/> |
|[<span data-ttu-id="f84fc-118">ToRecipients</span><span class="sxs-lookup"><span data-stu-id="f84fc-118">ToRecipients</span></span>](torecipients.md) <br/> |<span data-ttu-id="f84fc-119">Contiene un conjunto de destinatarios de un elemento.</span><span class="sxs-lookup"><span data-stu-id="f84fc-119">Contains a set of recipients of an item.</span></span> <span data-ttu-id="f84fc-120">Estos son los destinatarios principales de un elemento.</span><span class="sxs-lookup"><span data-stu-id="f84fc-120">These are the primary recipients of an item.</span></span>  <br/> |
|[<span data-ttu-id="f84fc-121">CcRecipients</span><span class="sxs-lookup"><span data-stu-id="f84fc-121">CcRecipients</span></span>](ccrecipients.md) <br/> |<span data-ttu-id="f84fc-122">Representa una colección de destinatarios que recibirán una copia del mensaje.</span><span class="sxs-lookup"><span data-stu-id="f84fc-122">Represents a collection of recipients that will receive a copy of the message.</span></span>  <br/> |
|[<span data-ttu-id="f84fc-123">BccRecipients</span><span class="sxs-lookup"><span data-stu-id="f84fc-123">BccRecipients</span></span>](bccrecipients.md) <br/> |<span data-ttu-id="f84fc-124">Representa una colección de destinatarios para recibir una copia oculta (CCO) de un correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="f84fc-124">Represents a collection of recipients to receive a blind carbon copy (Bcc) of an e-mail.</span></span>  <br/> |
|[<span data-ttu-id="f84fc-125">IsReadReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="f84fc-125">IsReadReceiptRequested</span></span>](isreadreceiptrequested.md) <br/> |<span data-ttu-id="f84fc-126">Indica si el remitente de un elemento solicita una confirmación de lectura.</span><span class="sxs-lookup"><span data-stu-id="f84fc-126">Indicates whether the sender of an item requests a read receipt.</span></span>  <br/> |
|[<span data-ttu-id="f84fc-127">IsDeliveryReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="f84fc-127">IsDeliveryReceiptRequested</span></span>](isdeliveryreceiptrequested.md) <br/> |<span data-ttu-id="f84fc-128">Indica si el remitente de un elemento solicita una confirmación de entrega.</span><span class="sxs-lookup"><span data-stu-id="f84fc-128">Indicates whether the sender of an item requests a delivery receipt.</span></span>  <br/> |
|[<span data-ttu-id="f84fc-129">ReferenceItemId</span><span class="sxs-lookup"><span data-stu-id="f84fc-129">ReferenceItemId</span></span>](referenceitemid.md) <br/> |<span data-ttu-id="f84fc-130">Identifica el elemento al que hace referencia el objeto de respuesta.</span><span class="sxs-lookup"><span data-stu-id="f84fc-130">Identifies the item to which the response object refers.</span></span>  <br/> |
|[<span data-ttu-id="f84fc-131">NewBodyContent</span><span class="sxs-lookup"><span data-stu-id="f84fc-131">NewBodyContent</span></span>](newbodycontent.md) <br/> |<span data-ttu-id="f84fc-132">Representa el nuevo contenido del cuerpo de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="f84fc-132">Represents the new body content of a message.</span></span>  <br/> |
|[<span data-ttu-id="f84fc-133">ReceivedBy</span><span class="sxs-lookup"><span data-stu-id="f84fc-133">ReceivedBy</span></span>](receivedby.md) <br/> |<span data-ttu-id="f84fc-134">Identifica el delegado en un escenario de acceso delegado.</span><span class="sxs-lookup"><span data-stu-id="f84fc-134">Identifies the delegate in a delegate access scenario.</span></span> <span data-ttu-id="f84fc-135">Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="f84fc-135">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span>  <br/> |
|[<span data-ttu-id="f84fc-136">ReceivedRepresenting</span><span class="sxs-lookup"><span data-stu-id="f84fc-136">ReceivedRepresenting</span></span>](receivedrepresenting.md) <br/> |<span data-ttu-id="f84fc-137">Identifica la entidad de identidad en un escenario de acceso delegado.</span><span class="sxs-lookup"><span data-stu-id="f84fc-137">Identifies the principal in a delegate access scenario.</span></span> <span data-ttu-id="f84fc-138">Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="f84fc-138">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="f84fc-139">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="f84fc-139">Parent elements</span></span>

|<span data-ttu-id="f84fc-140">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="f84fc-140">**Element**</span></span>|<span data-ttu-id="f84fc-141">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f84fc-141">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f84fc-142">AdjacentMeetings</span><span class="sxs-lookup"><span data-stu-id="f84fc-142">AdjacentMeetings</span></span>](adjacentmeetings.md) <br/> | <span data-ttu-id="f84fc-143">Describe todos los elementos adyacentes a una hora de reunión.</span><span class="sxs-lookup"><span data-stu-id="f84fc-143">Describes all items that are adjacent to a meeting time.</span></span><br/><br/> <span data-ttu-id="f84fc-144">Las siguientes son algunas de las expresiones XPath de este elemento:</span><span class="sxs-lookup"><span data-stu-id="f84fc-144">The following are some of the XPath expressions to this element:</span></span><br/><br/>`/CalendarItem/AdjacentMeetings` <br/>  `/MeetingRequest/AdjacentMeetings` <br/>  `/SetItemField/CalendarItem/AdjacentMeetings` <br/>  `/AppendToItemField/CalendarItem/AdjacentMeetings` <br/>  `/AcceptItem/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/>  `/DeclineItem/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/>  `/TentativelyAcceptItem/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/>  `/UpdateItem/ItemChanges/ItemChange/Updates/SetItemField/CalendarItem/AdjacentMeetings` <br/>  `/UpdateItem/ItemChanges/ItemChange/Updates/AppendToItemField/CalendarItem/AdjacentMeetings` <br/>  `/CreateAttachmentResponseMessage/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/>  `/GetAttachmentResponseMessage/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/> |
|[<span data-ttu-id="f84fc-145">ConflictingMeetings</span><span class="sxs-lookup"><span data-stu-id="f84fc-145">ConflictingMeetings</span></span>](conflictingmeetings.md) <br/> | <span data-ttu-id="f84fc-146">Describe todos los elementos que entran en conflicto con una hora de reunión.</span><span class="sxs-lookup"><span data-stu-id="f84fc-146">Describes all items that conflict with a meeting time.</span></span><br/><br/><span data-ttu-id="f84fc-147">Las siguientes son algunas de las expresiones XPath de este elemento:</span><span class="sxs-lookup"><span data-stu-id="f84fc-147">The following are some of the XPath expressions to this element:</span></span><br/><br/>`/CalendarItem/ConflictingMeetings` <br/>  `/MeetingRequest/ConflictingMeetings` <br/>  `/SetItemField/CalendarItem/ConflictingMeetings` <br/>  `/AppendToItemField/CalendarItem/ConflictingMeetings` <br/>  `/AcceptItem/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/>  `/DeclineItem/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/>  `/TentativelyAcceptItem/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/>  `/UpdateItem/ItemChanges/ItemChange/Updates/SetItemField/CalendarItem/ConflictingMeetings` <br/>  `/UpdateItem/ItemChanges/ItemChange/Updates/AppendToItemField/CalendarItem/ConflictingMeetings` <br/>  `/CreateAttachmentResponseMessage/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/>  `/GetAttachmentResponseMessage/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/> |
|[<span data-ttu-id="f84fc-148">ResponseObjects</span><span class="sxs-lookup"><span data-stu-id="f84fc-148">ResponseObjects</span></span>](responseobjects.md) <br/> |<span data-ttu-id="f84fc-149">Contiene una colección de todos los objetos de respuesta que están asociados a un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="f84fc-149">Contains a collection of all the response objects that are associated with an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="f84fc-150">Elementos (NonEmptyArrayOfAllItemsType)</span><span class="sxs-lookup"><span data-stu-id="f84fc-150">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md) <br/> |<span data-ttu-id="f84fc-151">Contiene una matriz de elementos que se van a crear en la carpeta identificada por el elemento [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) .</span><span class="sxs-lookup"><span data-stu-id="f84fc-151">Contains an array of items to create in the folder identified by the [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) element.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f84fc-152">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f84fc-152">Remarks</span></span>

<span data-ttu-id="f84fc-153">El elemento **CancelCalendarItem** solo lo ve el organizador.</span><span class="sxs-lookup"><span data-stu-id="f84fc-153">The **CancelCalendarItem** element is only viewed by the organizer.</span></span> <span data-ttu-id="f84fc-154">Solo se aplica al elemento de calendario del organizador.</span><span class="sxs-lookup"><span data-stu-id="f84fc-154">It only applies to the organizer's calendar item.</span></span> 
  
<span data-ttu-id="f84fc-155">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="f84fc-155">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f84fc-156">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="f84fc-156">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f84fc-157">Namespace</span><span class="sxs-lookup"><span data-stu-id="f84fc-157">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f84fc-158">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="f84fc-158">Schema Name</span></span>  <br/> |<span data-ttu-id="f84fc-159">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="f84fc-159">Types schema</span></span>  <br/> |
|<span data-ttu-id="f84fc-160">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="f84fc-160">Validation File</span></span>  <br/> |<span data-ttu-id="f84fc-161">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="f84fc-161">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="f84fc-162">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="f84fc-162">Can be Empty</span></span>  <br/> |<span data-ttu-id="f84fc-163">Falso</span><span class="sxs-lookup"><span data-stu-id="f84fc-163">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f84fc-164">Vea también</span><span class="sxs-lookup"><span data-stu-id="f84fc-164">See also</span></span>

- [<span data-ttu-id="f84fc-165">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="f84fc-165">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

