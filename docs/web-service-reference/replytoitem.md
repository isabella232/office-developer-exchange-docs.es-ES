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
ms.openlocfilehash: fc40335dc73327820c0b39cafa07168d1f27851d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529857"
---
# <a name="replytoitem"></a><span data-ttu-id="838ad-103">ReplyToItem</span><span class="sxs-lookup"><span data-stu-id="838ad-103">ReplyToItem</span></span>

<span data-ttu-id="838ad-104">El elemento **ReplyToItem** contiene una respuesta al remitente de un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="838ad-104">The **ReplyToItem** element contains a reply to the sender of an item in the Exchange store.</span></span> 
  
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

<span data-ttu-id="838ad-105">**ReplyToItemType**</span><span class="sxs-lookup"><span data-stu-id="838ad-105">**ReplyToItemType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="838ad-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="838ad-106">Attributes and elements</span></span>

<span data-ttu-id="838ad-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="838ad-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="838ad-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="838ad-108">Attributes</span></span>

<span data-ttu-id="838ad-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="838ad-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="838ad-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="838ad-110">Child elements</span></span>

|<span data-ttu-id="838ad-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="838ad-111">**Element**</span></span>|<span data-ttu-id="838ad-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="838ad-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="838ad-113">Asunto</span><span class="sxs-lookup"><span data-stu-id="838ad-113">Subject</span></span>](subject.md) <br/> |<span data-ttu-id="838ad-114">Representa la propiedad Subject de los elementos del almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="838ad-114">Represents the subject property of Exchange store items.</span></span>  <br/> |
|[<span data-ttu-id="838ad-115">Body</span><span class="sxs-lookup"><span data-stu-id="838ad-115">Body</span></span>](body.md) <br/> |<span data-ttu-id="838ad-116">Representa el contenido del cuerpo real de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="838ad-116">Represents the actual body content of a message.</span></span>  <br/> |
|[<span data-ttu-id="838ad-117">ToRecipients</span><span class="sxs-lookup"><span data-stu-id="838ad-117">ToRecipients</span></span>](torecipients.md) <br/> |<span data-ttu-id="838ad-118">Contiene una matriz de destinatarios de un elemento.</span><span class="sxs-lookup"><span data-stu-id="838ad-118">Contains an array of recipients of an item.</span></span> <span data-ttu-id="838ad-119">Estos son los destinatarios principales de un elemento.</span><span class="sxs-lookup"><span data-stu-id="838ad-119">These are the primary recipients of an item.</span></span>  <br/> |
|[<span data-ttu-id="838ad-120">CcRecipients</span><span class="sxs-lookup"><span data-stu-id="838ad-120">CcRecipients</span></span>](ccrecipients.md) <br/> |<span data-ttu-id="838ad-121">Representa una colección de destinatarios que recibirán una copia del mensaje.</span><span class="sxs-lookup"><span data-stu-id="838ad-121">Represents a collection of recipients that will receive a copy of the message.</span></span>  <br/> |
|[<span data-ttu-id="838ad-122">BccRecipients</span><span class="sxs-lookup"><span data-stu-id="838ad-122">BccRecipients</span></span>](bccrecipients.md) <br/> |<span data-ttu-id="838ad-123">Representa una colección de destinatarios para recibir una copia oculta (CCO) de un mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="838ad-123">Represents a collection of recipients to receive a blind carbon copy (Bcc) of an e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="838ad-124">IsReadReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="838ad-124">IsReadReceiptRequested</span></span>](isreadreceiptrequested.md) <br/> |<span data-ttu-id="838ad-125">Indica si el remitente de un elemento solicita una confirmación de lectura.</span><span class="sxs-lookup"><span data-stu-id="838ad-125">Indicates whether the sender of an item requests a read receipt.</span></span>  <br/> |
|[<span data-ttu-id="838ad-126">IsDeliveryReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="838ad-126">IsDeliveryReceiptRequested</span></span>](isdeliveryreceiptrequested.md) <br/> |<span data-ttu-id="838ad-127">Indica si el remitente de un elemento solicita una confirmación de entrega.</span><span class="sxs-lookup"><span data-stu-id="838ad-127">Indicates whether the sender of an item requests a delivery receipt.</span></span>  <br/> |
|[<span data-ttu-id="838ad-128">From</span><span class="sxs-lookup"><span data-stu-id="838ad-128">From</span></span>](from.md) <br/> |<span data-ttu-id="838ad-129">Representa la dirección desde la que se envió el mensaje.</span><span class="sxs-lookup"><span data-stu-id="838ad-129">Represents the address from which the message was sent.</span></span>  <br/> |
|[<span data-ttu-id="838ad-130">ReferenceItemId</span><span class="sxs-lookup"><span data-stu-id="838ad-130">ReferenceItemId</span></span>](referenceitemid.md) <br/> |<span data-ttu-id="838ad-131">Identifica el elemento al que hace referencia el objeto de respuesta.</span><span class="sxs-lookup"><span data-stu-id="838ad-131">Identifies the item to which the response object refers.</span></span>  <br/> |
|[<span data-ttu-id="838ad-132">NewBodyContent</span><span class="sxs-lookup"><span data-stu-id="838ad-132">NewBodyContent</span></span>](newbodycontent.md) <br/> |<span data-ttu-id="838ad-133">Representa el nuevo contenido del cuerpo de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="838ad-133">Represents the new body content of a message.</span></span>  <br/> |
|[<span data-ttu-id="838ad-134">ReceivedBy</span><span class="sxs-lookup"><span data-stu-id="838ad-134">ReceivedBy</span></span>](receivedby.md) <br/> |<span data-ttu-id="838ad-135">Identifica el delegado en un escenario de acceso delegado.</span><span class="sxs-lookup"><span data-stu-id="838ad-135">Identifies the delegate in a delegate access scenario.</span></span> <span data-ttu-id="838ad-136">Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="838ad-136">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span>  <br/> |
|[<span data-ttu-id="838ad-137">ReceivedRepresenting</span><span class="sxs-lookup"><span data-stu-id="838ad-137">ReceivedRepresenting</span></span>](receivedrepresenting.md) <br/> |<span data-ttu-id="838ad-138">Identifica la entidad de identidad en un escenario de acceso delegado.</span><span class="sxs-lookup"><span data-stu-id="838ad-138">Identifies the principal in a delegate access scenario.</span></span> <span data-ttu-id="838ad-139">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="838ad-139">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="838ad-140">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="838ad-140">Parent elements</span></span>

|<span data-ttu-id="838ad-141">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="838ad-141">**Element**</span></span>|<span data-ttu-id="838ad-142">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="838ad-142">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="838ad-143">AdjacentMeetings</span><span class="sxs-lookup"><span data-stu-id="838ad-143">AdjacentMeetings</span></span>](adjacentmeetings.md) <br/> | <span data-ttu-id="838ad-144">Describe todos los elementos adyacentes a una hora de reunión.</span><span class="sxs-lookup"><span data-stu-id="838ad-144">Describes all items that are adjacent to a meeting time.</span></span> <br/> <br/>  <span data-ttu-id="838ad-145">Las siguientes son algunas de las expresiones XPath de este elemento:</span><span class="sxs-lookup"><span data-stu-id="838ad-145">The following are some of the XPath expressions to this element:</span></span> <br/> <br/>  `/CalendarItem/AdjacentMeetings` <br/>  `/MeetingRequest/AdjacentMeetings` <br/>  `/SetItemField/CalendarItem/AdjacentMeetings` <br/>  `/AppendToItemField/CalendarItem/AdjacentMeetings` <br/>  `/AcceptItem/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/>  `/DeclineItem/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/>  `/TentativelyAcceptItem/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/>  `/UpdateItem/ItemChanges/ItemChange/Updates/SetItemField/CalendarItem/AdjacentMeetings` <br/>  `/UpdateItem/ItemChanges/ItemChange/Updates/AppendToItemField/CalendarItem/AdjacentMeetings` <br/>  `/CreateAttachmentResponseMessage/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/>  `/GetAttachmentResponseMessage/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/> |
|[<span data-ttu-id="838ad-146">ConflictingMeetings</span><span class="sxs-lookup"><span data-stu-id="838ad-146">ConflictingMeetings</span></span>](conflictingmeetings.md) <br/> | <span data-ttu-id="838ad-147">Describe todos los elementos que entran en conflicto con una hora de reunión.</span><span class="sxs-lookup"><span data-stu-id="838ad-147">Describes all items that conflict with a meeting time.</span></span> <br/> <br/>  <span data-ttu-id="838ad-148">Las siguientes son algunas de las expresiones XPath de este elemento:</span><span class="sxs-lookup"><span data-stu-id="838ad-148">The following are some of the XPath expressions to this element:</span></span> <br/> <br/>  `/CalendarItem/ConflictingMeetings` <br/>  `/MeetingRequest/ConflictingMeetings` <br/>  `/SetItemField/CalendarItem/ConflictingMeetings` <br/>  `/AppendToItemField/CalendarItem/ConflictingMeetings` <br/>  `/AcceptItem/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/>  `/DeclineItem/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/>  `/TentativelyAcceptItem/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/>  `/UpdateItem/ItemChanges/ItemChange/Updates/SetItemField/CalendarItem/ConflictingMeetings` <br/>  `/UpdateItem/ItemChanges/ItemChange/Updates/AppendToItemField/CalendarItem/ConflictingMeetings` <br/>  `/CreateAttachmentResponseMessage/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/>  `/GetAttachmentResponseMessage/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/> |
|[<span data-ttu-id="838ad-149">ResponseObjects</span><span class="sxs-lookup"><span data-stu-id="838ad-149">ResponseObjects</span></span>](responseobjects.md) <br/> |<span data-ttu-id="838ad-150">Contiene una colección de todos los objetos de respuesta que están asociados a un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="838ad-150">Contains a collection of all the response objects that are associated with an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="838ad-151">Elementos (NonEmptyArrayOfAllItemsType)</span><span class="sxs-lookup"><span data-stu-id="838ad-151">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md) <br/> |<span data-ttu-id="838ad-152">Contiene una matriz de elementos que se van a crear en la carpeta identificada por el elemento [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) .</span><span class="sxs-lookup"><span data-stu-id="838ad-152">Contains an array of items to create in the folder that is identified by the [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) element.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="838ad-153">Comentarios</span><span class="sxs-lookup"><span data-stu-id="838ad-153">Remarks</span></span>

<span data-ttu-id="838ad-154">El elemento [from](from.md) debe establecerse en la dirección de correo electrónico de la entidad de identidad si un elemento es una respuesta de un delegado.</span><span class="sxs-lookup"><span data-stu-id="838ad-154">The [From](from.md) element should be set to the e-mail address of the principal if an item is a reply by a delegate.</span></span> <span data-ttu-id="838ad-155">Si el delegado no establece la propiedad [from](from.md) , parecerá que el elemento se ha enviado directamente desde el buzón de correo del delegado.</span><span class="sxs-lookup"><span data-stu-id="838ad-155">If the delegate does not set the [From](from.md) property, the item will appear to have been sent directly from the delegate's mailbox.</span></span> 
  
<span data-ttu-id="838ad-156">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="838ad-156">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="838ad-157">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="838ad-157">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="838ad-158">Namespace</span><span class="sxs-lookup"><span data-stu-id="838ad-158">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="838ad-159">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="838ad-159">Schema Name</span></span>  <br/> |<span data-ttu-id="838ad-160">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="838ad-160">Types schema</span></span>  <br/> |
|<span data-ttu-id="838ad-161">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="838ad-161">Validation File</span></span>  <br/> |<span data-ttu-id="838ad-162">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="838ad-162">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="838ad-163">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="838ad-163">Can be Empty</span></span>  <br/> |<span data-ttu-id="838ad-164">Falso</span><span class="sxs-lookup"><span data-stu-id="838ad-164">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="838ad-165">Vea también</span><span class="sxs-lookup"><span data-stu-id="838ad-165">See also</span></span>

- [<span data-ttu-id="838ad-166">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="838ad-166">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

