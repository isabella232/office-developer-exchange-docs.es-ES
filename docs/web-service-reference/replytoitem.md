---
title: ReplyToItem
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ReplyToItem
api_type:
- schema
ms.assetid: 35ee751a-41c0-4216-ad8b-78f7ada43a2f
description: El elemento ReplyToItem contiene una respuesta al remitente de un elemento en el almacén de Exchange.
ms.openlocfilehash: 561ddc3b64ad6d2fe0ea3a3583c41faea36a4a5b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19837120"
---
# <a name="replytoitem"></a><span data-ttu-id="9cd45-103">ReplyToItem</span><span class="sxs-lookup"><span data-stu-id="9cd45-103">ReplyToItem</span></span>

<span data-ttu-id="9cd45-104">El elemento **ReplyToItem** contiene una respuesta al remitente de un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="9cd45-104">The **ReplyToItem** element contains a reply to the sender of an item in the Exchange store.</span></span> 
  
```xml
<ReplyToItem>
   <Subject/>
   <Body/>
   <ToRecipients/>
   <CcRecipients/>
   <BccRecipients/>
   <IsReadReceiptRequested/>
   <IsDeliveryReceiptRequested/>
   <From/>
   <ReferenceItemId/>
   <NewBodyContent/>
   <ReceivedBy/>
   <ReceivedRepresenting/>
</ReplyToItem>
```

<span data-ttu-id="9cd45-105">**ReplyToItemType**</span><span class="sxs-lookup"><span data-stu-id="9cd45-105">**ReplyToItemType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="9cd45-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="9cd45-106">Attributes and elements</span></span>

<span data-ttu-id="9cd45-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="9cd45-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9cd45-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="9cd45-108">Attributes</span></span>

<span data-ttu-id="9cd45-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="9cd45-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="9cd45-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="9cd45-110">Child elements</span></span>

|<span data-ttu-id="9cd45-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="9cd45-111">**Element**</span></span>|<span data-ttu-id="9cd45-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9cd45-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9cd45-113">Subject</span><span class="sxs-lookup"><span data-stu-id="9cd45-113">Subject</span></span>](subject.md) <br/> |<span data-ttu-id="9cd45-114">Representa la propiedad de asunto de los elementos del almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="9cd45-114">Represents the subject property of Exchange store items.</span></span>  <br/> |
|[<span data-ttu-id="9cd45-115">Body</span><span class="sxs-lookup"><span data-stu-id="9cd45-115">Body</span></span>](body.md) <br/> |<span data-ttu-id="9cd45-116">Representa el contenido real del cuerpo de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="9cd45-116">Represents the actual body content of a message.</span></span>  <br/> |
|[<span data-ttu-id="9cd45-117">ToRecipients</span><span class="sxs-lookup"><span data-stu-id="9cd45-117">ToRecipients</span></span>](torecipients.md) <br/> |<span data-ttu-id="9cd45-118">Contiene una matriz de destinatarios de un elemento.</span><span class="sxs-lookup"><span data-stu-id="9cd45-118">Contains an array of recipients of an item.</span></span> <span data-ttu-id="9cd45-119">Estos son los destinatarios principales de un elemento.</span><span class="sxs-lookup"><span data-stu-id="9cd45-119">These are the primary recipients of an item.</span></span>  <br/> |
|[<span data-ttu-id="9cd45-120">CcRecipients</span><span class="sxs-lookup"><span data-stu-id="9cd45-120">CcRecipients</span></span>](ccrecipients.md) <br/> |<span data-ttu-id="9cd45-121">Representa una colección de los destinatarios que recibirán una copia del mensaje.</span><span class="sxs-lookup"><span data-stu-id="9cd45-121">Represents a collection of recipients that will receive a copy of the message.</span></span>  <br/> |
|[<span data-ttu-id="9cd45-122">BccRecipients</span><span class="sxs-lookup"><span data-stu-id="9cd45-122">BccRecipients</span></span>](bccrecipients.md) <br/> |<span data-ttu-id="9cd45-123">Representa una colección de destinatarios para recibir una copia oculta (CCO) del mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="9cd45-123">Represents a collection of recipients to receive a blind carbon copy (Bcc) of an e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="9cd45-124">IsReadReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="9cd45-124">IsReadReceiptRequested</span></span>](isreadreceiptrequested.md) <br/> |<span data-ttu-id="9cd45-125">Indica si el remitente de un elemento solicita una confirmación de lectura.</span><span class="sxs-lookup"><span data-stu-id="9cd45-125">Indicates whether the sender of an item requests a read receipt.</span></span>  <br/> |
|[<span data-ttu-id="9cd45-126">IsDeliveryReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="9cd45-126">IsDeliveryReceiptRequested</span></span>](isdeliveryreceiptrequested.md) <br/> |<span data-ttu-id="9cd45-127">Indica si el remitente de un elemento solicita una confirmación de entrega.</span><span class="sxs-lookup"><span data-stu-id="9cd45-127">Indicates whether the sender of an item requests a delivery receipt.</span></span>  <br/> |
|[<span data-ttu-id="9cd45-128">From</span><span class="sxs-lookup"><span data-stu-id="9cd45-128">From</span></span>](from.md) <br/> |<span data-ttu-id="9cd45-129">Representa la dirección desde la que se envió el mensaje.</span><span class="sxs-lookup"><span data-stu-id="9cd45-129">Represents the address from which the message was sent.</span></span>  <br/> |
|[<span data-ttu-id="9cd45-130">ReferenceItemId</span><span class="sxs-lookup"><span data-stu-id="9cd45-130">ReferenceItemId</span></span>](referenceitemid.md) <br/> |<span data-ttu-id="9cd45-131">Identifica el elemento al que hace referencia el objeto de respuesta.</span><span class="sxs-lookup"><span data-stu-id="9cd45-131">Identifies the item to which the response object refers.</span></span>  <br/> |
|[<span data-ttu-id="9cd45-132">NewBodyContent</span><span class="sxs-lookup"><span data-stu-id="9cd45-132">NewBodyContent</span></span>](newbodycontent.md) <br/> |<span data-ttu-id="9cd45-133">Representa el nuevo contenido del cuerpo de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="9cd45-133">Represents the new body content of a message.</span></span>  <br/> |
|[<span data-ttu-id="9cd45-134">ReceivedBy</span><span class="sxs-lookup"><span data-stu-id="9cd45-134">ReceivedBy</span></span>](receivedby.md) <br/> |<span data-ttu-id="9cd45-135">Identifica al delegado en un escenario de acceso delegado.</span><span class="sxs-lookup"><span data-stu-id="9cd45-135">Identifies the delegate in a delegate access scenario.</span></span> <span data-ttu-id="9cd45-136">Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="9cd45-136">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span>  <br/> |
|[<span data-ttu-id="9cd45-137">ReceivedRepresenting</span><span class="sxs-lookup"><span data-stu-id="9cd45-137">ReceivedRepresenting</span></span>](receivedrepresenting.md) <br/> |<span data-ttu-id="9cd45-138">Identifica la entidad de seguridad en un escenario de acceso delegado.</span><span class="sxs-lookup"><span data-stu-id="9cd45-138">Identifies the principal in a delegate access scenario.</span></span> <span data-ttu-id="9cd45-139">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="9cd45-139">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="9cd45-140">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="9cd45-140">Parent elements</span></span>

|<span data-ttu-id="9cd45-141">**Element**</span><span class="sxs-lookup"><span data-stu-id="9cd45-141">**Element**</span></span>|<span data-ttu-id="9cd45-142">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9cd45-142">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9cd45-143">AdjacentMeetings</span><span class="sxs-lookup"><span data-stu-id="9cd45-143">AdjacentMeetings</span></span>](adjacentmeetings.md) <br/> | <span data-ttu-id="9cd45-144">Describe todos los elementos que están adyacentes a una hora de reunión.</span><span class="sxs-lookup"><span data-stu-id="9cd45-144">Describes all items that are adjacent to a meeting time.</span></span> <br/> <br/>  <span data-ttu-id="9cd45-145">Las siguientes son algunas de las expresiones de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="9cd45-145">The following are some of the XPath expressions to this element:</span></span> <br/> <br/>  `/CalendarItem/AdjacentMeetings` <br/>  `/MeetingRequest/AdjacentMeetings` <br/>  `/SetItemField/CalendarItem/AdjacentMeetings` <br/>  `/AppendToItemField/CalendarItem/AdjacentMeetings` <br/>  `/AcceptItem/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/>  `/DeclineItem/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/>  `/TentativelyAcceptItem/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/>  `/UpdateItem/ItemChanges/ItemChange/Updates/SetItemField/CalendarItem/AdjacentMeetings` <br/>  `/UpdateItem/ItemChanges/ItemChange/Updates/AppendToItemField/CalendarItem/AdjacentMeetings` <br/>  `/CreateAttachmentResponseMessage/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/>  `/GetAttachmentResponseMessage/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/> |
|[<span data-ttu-id="9cd45-146">ConflictingMeetings</span><span class="sxs-lookup"><span data-stu-id="9cd45-146">ConflictingMeetings</span></span>](conflictingmeetings.md) <br/> | <span data-ttu-id="9cd45-147">Describe todos los elementos que entran en conflicto con un tiempo de la reunión.</span><span class="sxs-lookup"><span data-stu-id="9cd45-147">Describes all items that conflict with a meeting time.</span></span> <br/> <br/>  <span data-ttu-id="9cd45-148">Las siguientes son algunas de las expresiones de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="9cd45-148">The following are some of the XPath expressions to this element:</span></span> <br/> <br/>  `/CalendarItem/ConflictingMeetings` <br/>  `/MeetingRequest/ConflictingMeetings` <br/>  `/SetItemField/CalendarItem/ConflictingMeetings` <br/>  `/AppendToItemField/CalendarItem/ConflictingMeetings` <br/>  `/AcceptItem/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/>  `/DeclineItem/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/>  `/TentativelyAcceptItem/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/>  `/UpdateItem/ItemChanges/ItemChange/Updates/SetItemField/CalendarItem/ConflictingMeetings` <br/>  `/UpdateItem/ItemChanges/ItemChange/Updates/AppendToItemField/CalendarItem/ConflictingMeetings` <br/>  `/CreateAttachmentResponseMessage/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/>  `/GetAttachmentResponseMessage/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/> |
|[<span data-ttu-id="9cd45-149">ResponseObjects</span><span class="sxs-lookup"><span data-stu-id="9cd45-149">ResponseObjects</span></span>](responseobjects.md) <br/> |<span data-ttu-id="9cd45-150">Contiene una colección de todos los objetos de respuesta que están asociados con un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="9cd45-150">Contains a collection of all the response objects that are associated with an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="9cd45-151">Elementos (NonEmptyArrayOfAllItemsType)</span><span class="sxs-lookup"><span data-stu-id="9cd45-151">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md) <br/> |<span data-ttu-id="9cd45-152">Contiene una matriz de elementos que desea crear en la carpeta que se identifica con el elemento [ID (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) .</span><span class="sxs-lookup"><span data-stu-id="9cd45-152">Contains an array of items to create in the folder that is identified by the [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) element.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9cd45-153">Notas</span><span class="sxs-lookup"><span data-stu-id="9cd45-153">Remarks</span></span>

<span data-ttu-id="9cd45-154">El elemento [de](from.md) debe establecerse en la dirección de correo electrónico de la entidad de seguridad si un elemento es una respuesta por un delegado.</span><span class="sxs-lookup"><span data-stu-id="9cd45-154">The [From](from.md) element should be set to the e-mail address of the principal if an item is a reply by a delegate.</span></span> <span data-ttu-id="9cd45-155">Si el delegado no establece la propiedad [From](from.md) , aparecerá el elemento al que se han enviado directamente desde el buzón del delegado.</span><span class="sxs-lookup"><span data-stu-id="9cd45-155">If the delegate does not set the [From](from.md) property, the item will appear to have been sent directly from the delegate's mailbox.</span></span> 
  
<span data-ttu-id="9cd45-156">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="9cd45-156">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9cd45-157">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="9cd45-157">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9cd45-158">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="9cd45-158">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="9cd45-159">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="9cd45-159">Schema Name</span></span>  <br/> |<span data-ttu-id="9cd45-160">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="9cd45-160">Types schema</span></span>  <br/> |
|<span data-ttu-id="9cd45-161">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="9cd45-161">Validation File</span></span>  <br/> |<span data-ttu-id="9cd45-162">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="9cd45-162">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="9cd45-163">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="9cd45-163">Can be Empty</span></span>  <br/> |<span data-ttu-id="9cd45-164">False</span><span class="sxs-lookup"><span data-stu-id="9cd45-164">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9cd45-165">Ver también</span><span class="sxs-lookup"><span data-stu-id="9cd45-165">See also</span></span>

- [<span data-ttu-id="9cd45-166">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="9cd45-166">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

