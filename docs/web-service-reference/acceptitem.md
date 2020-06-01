---
title: AcceptItem
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AcceptItem
api_type:
- schema
ms.assetid: 05a15431-77e1-411a-a16b-5481d364d3cc
description: El elemento AcceptItem representa una respuesta de aceptación para una convocatoria de reunión.
ms.openlocfilehash: 6f2197e9df8a095aec545e1a09a761f7e8e432d3
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461719"
---
# <a name="acceptitem"></a><span data-ttu-id="4e7c4-103">AcceptItem</span><span class="sxs-lookup"><span data-stu-id="4e7c4-103">AcceptItem</span></span>

<span data-ttu-id="4e7c4-104">El elemento **AcceptItem** representa una respuesta de aceptación para una convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="4e7c4-104">The **AcceptItem** element represents an Accept reply to a meeting request.</span></span> 
  
```xml
<AcceptItem>
   <ItemClass/>
   <Sensitivity/>
   <Body/>
   <Attachments/>
   <InternetMessageHeaders/>
   <Sender/>
   <ToRecipients/>
   <CcRecipients/>
   <BccRecipients/>
   <IsReadReceiptRequested/>
   <IsDeliveryReceiptRequested/>
   <ReferenceItemId/>
   <ReceivedBy/>
   <ReceivedRepresenting/>
   <ProposedStart/>
   <ProposedEnd/>
</AcceptItem>
```

 <span data-ttu-id="4e7c4-105">**AcceptItemType**</span><span class="sxs-lookup"><span data-stu-id="4e7c4-105">**AcceptItemType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4e7c4-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="4e7c4-106">Attributes and elements</span></span>

<span data-ttu-id="4e7c4-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="4e7c4-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4e7c4-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="4e7c4-108">Attributes</span></span>

<span data-ttu-id="4e7c4-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="4e7c4-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4e7c4-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="4e7c4-110">Child elements</span></span>

|<span data-ttu-id="4e7c4-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="4e7c4-111">**Element**</span></span>|<span data-ttu-id="4e7c4-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4e7c4-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4e7c4-113">ItemClass</span><span class="sxs-lookup"><span data-stu-id="4e7c4-113">ItemClass</span></span>](itemclass.md) <br/> |<span data-ttu-id="4e7c4-114">Representa la clase de mensaje de un elemento.</span><span class="sxs-lookup"><span data-stu-id="4e7c4-114">Represents the message class of an item.</span></span>  <br/> |
|[<span data-ttu-id="4e7c4-115">Sensitivity</span><span class="sxs-lookup"><span data-stu-id="4e7c4-115">Sensitivity</span></span>](sensitivity.md) <br/> |<span data-ttu-id="4e7c4-116">Indica el nivel de confidencialidad de un elemento.</span><span class="sxs-lookup"><span data-stu-id="4e7c4-116">Indicates the sensitivity level of an item.</span></span>  <br/> |
|[<span data-ttu-id="4e7c4-117">Body</span><span class="sxs-lookup"><span data-stu-id="4e7c4-117">Body</span></span>](body.md) <br/> |<span data-ttu-id="4e7c4-118">Representa el contenido del cuerpo real de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="4e7c4-118">Represents the actual body content of a message.</span></span>  <br/> |
|[<span data-ttu-id="4e7c4-119">Datos adjuntos</span><span class="sxs-lookup"><span data-stu-id="4e7c4-119">Attachments</span></span>](attachments-ex15websvcsotherref.md) <br/> |<span data-ttu-id="4e7c4-120">Contiene el elemento o archivo que se adjunta a un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="4e7c4-120">Contains the item or file that is attached to an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="4e7c4-121">InternetMessageHeaders</span><span class="sxs-lookup"><span data-stu-id="4e7c4-121">InternetMessageHeaders</span></span>](internetmessageheaders.md) <br/> |<span data-ttu-id="4e7c4-122">Representa el nombre de encabezado de un mensaje de Internet para un encabezado determinado dentro de la colección de encabezados.</span><span class="sxs-lookup"><span data-stu-id="4e7c4-122">Represents the Internet message header name for a given header within the headers collection.</span></span>  <br/> |
|[<span data-ttu-id="4e7c4-123">Sender</span><span class="sxs-lookup"><span data-stu-id="4e7c4-123">Sender</span></span>](sender.md) <br/> |<span data-ttu-id="4e7c4-124">Identifica al remitente de un elemento.</span><span class="sxs-lookup"><span data-stu-id="4e7c4-124">Identifies the sender of an item.</span></span>  <br/> |
|[<span data-ttu-id="4e7c4-125">ToRecipients</span><span class="sxs-lookup"><span data-stu-id="4e7c4-125">ToRecipients</span></span>](torecipients.md) <br/> |<span data-ttu-id="4e7c4-126">Contiene un conjunto de destinatarios de un elemento.</span><span class="sxs-lookup"><span data-stu-id="4e7c4-126">Contains a set of recipients of an item.</span></span> <span data-ttu-id="4e7c4-127">Estos son los destinatarios principales de un elemento.</span><span class="sxs-lookup"><span data-stu-id="4e7c4-127">These are the primary recipients of an item.</span></span>  <br/> |
|[<span data-ttu-id="4e7c4-128">CcRecipients</span><span class="sxs-lookup"><span data-stu-id="4e7c4-128">CcRecipients</span></span>](ccrecipients.md) <br/> |<span data-ttu-id="4e7c4-129">Representa una colección de destinatarios que recibirán una copia del mensaje.</span><span class="sxs-lookup"><span data-stu-id="4e7c4-129">Represents a collection of recipients that will receive a copy of the message.</span></span>  <br/> |
|[<span data-ttu-id="4e7c4-130">BccRecipients</span><span class="sxs-lookup"><span data-stu-id="4e7c4-130">BccRecipients</span></span>](bccrecipients.md) <br/> |<span data-ttu-id="4e7c4-131">Representa una colección de destinatarios para recibir una copia oculta (CCO) de un correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="4e7c4-131">Represents a collection of recipients to receive a blind carbon copy (Bcc) of an e-mail.</span></span>  <br/> |
|[<span data-ttu-id="4e7c4-132">IsReadReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="4e7c4-132">IsReadReceiptRequested</span></span>](isreadreceiptrequested.md) <br/> |<span data-ttu-id="4e7c4-133">Indica si el remitente de un elemento solicita una confirmación de lectura.</span><span class="sxs-lookup"><span data-stu-id="4e7c4-133">Indicates whether the sender of an item requests a read receipt.</span></span>  <br/> |
|[<span data-ttu-id="4e7c4-134">IsDeliveryReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="4e7c4-134">IsDeliveryReceiptRequested</span></span>](isdeliveryreceiptrequested.md) <br/> |<span data-ttu-id="4e7c4-135">Indica si el remitente de un elemento solicita una confirmación de entrega.</span><span class="sxs-lookup"><span data-stu-id="4e7c4-135">Indicates whether the sender of an item requests a delivery receipt.</span></span>  <br/> |
|[<span data-ttu-id="4e7c4-136">ReferenceItemId</span><span class="sxs-lookup"><span data-stu-id="4e7c4-136">ReferenceItemId</span></span>](referenceitemid.md) <br/> |<span data-ttu-id="4e7c4-137">Identifica el elemento al que hace referencia el objeto de respuesta.</span><span class="sxs-lookup"><span data-stu-id="4e7c4-137">Identifies the item to which the response object refers.</span></span>  <br/> |
|[<span data-ttu-id="4e7c4-138">ReceivedBy</span><span class="sxs-lookup"><span data-stu-id="4e7c4-138">ReceivedBy</span></span>](receivedby.md) <br/> |<span data-ttu-id="4e7c4-139">Identifica el delegado en un escenario de acceso delegado.</span><span class="sxs-lookup"><span data-stu-id="4e7c4-139">Identifies the delegate in a delegate access scenario.</span></span> <span data-ttu-id="4e7c4-140">Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="4e7c4-140">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span>  <br/> |
|[<span data-ttu-id="4e7c4-141">ReceivedRepresenting</span><span class="sxs-lookup"><span data-stu-id="4e7c4-141">ReceivedRepresenting</span></span>](receivedrepresenting.md) <br/> |<span data-ttu-id="4e7c4-142">Identifica la entidad de identidad en un escenario de acceso delegado.</span><span class="sxs-lookup"><span data-stu-id="4e7c4-142">Identifies the principal in a delegate access scenario.</span></span> <span data-ttu-id="4e7c4-143">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="4e7c4-143">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="4e7c4-144">ProposedStart</span><span class="sxs-lookup"><span data-stu-id="4e7c4-144">ProposedStart</span></span>](proposedstart.md) <br/> |<span data-ttu-id="4e7c4-145">Especifica la hora de inicio propuesta de la reunión.</span><span class="sxs-lookup"><span data-stu-id="4e7c4-145">Specifies the proposed start time of the meeting.</span></span>  <br/> |
|[<span data-ttu-id="4e7c4-146">ProposedEnd</span><span class="sxs-lookup"><span data-stu-id="4e7c4-146">ProposedEnd</span></span>](proposedend.md) <br/> |<span data-ttu-id="4e7c4-147">Especifica la hora de finalización propuesta de la reunión.</span><span class="sxs-lookup"><span data-stu-id="4e7c4-147">Specifies the proposed end time of the meeting.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="4e7c4-148">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="4e7c4-148">Parent elements</span></span>

|<span data-ttu-id="4e7c4-149">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="4e7c4-149">**Element**</span></span>|<span data-ttu-id="4e7c4-150">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4e7c4-150">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4e7c4-151">AdjacentMeetings</span><span class="sxs-lookup"><span data-stu-id="4e7c4-151">AdjacentMeetings</span></span>](adjacentmeetings.md) <br/> | <span data-ttu-id="4e7c4-152">Describe todos los elementos adyacentes a una hora de reunión.</span><span class="sxs-lookup"><span data-stu-id="4e7c4-152">Describes all items that are adjacent to a meeting time.</span></span><br/><br/>  <span data-ttu-id="4e7c4-153">Las siguientes son algunas de las expresiones XPath de este elemento:</span><span class="sxs-lookup"><span data-stu-id="4e7c4-153">The following are some of the XPath expressions to this element:</span></span><br/><br/>  `/CalendarItem/AdjacentMeetings` <br/>  `/MeetingRequest/AdjacentMeetings` <br/>  `/SetItemField/CalendarItem/AdjacentMeetings` <br/>  `/AppendToItemField/CalendarItem/AdjacentMeetings` <br/>  `/AcceptItem/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/>  `/DeclineItem/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/>  `/TentativelyAcceptItem/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/>  `/UpdateItem/ItemChanges/ItemChange/Updates/SetItemField/CalendarItem/AdjacentMeetings` <br/>  `/UpdateItem/ItemChanges/ItemChange/Updates/AppendToItemField/CalendarItem/AdjacentMeetings` <br/>  `/CreateAttachmentResponseMessage/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/>  `/GetAttachmentResponseMessage/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/> |
|[<span data-ttu-id="4e7c4-154">ConflictingMeetings</span><span class="sxs-lookup"><span data-stu-id="4e7c4-154">ConflictingMeetings</span></span>](conflictingmeetings.md) <br/> | <span data-ttu-id="4e7c4-155">Describe todos los elementos que entran en conflicto con una hora de reunión.</span><span class="sxs-lookup"><span data-stu-id="4e7c4-155">Describes all items that conflict with a meeting time.</span></span><br/><br/>  <span data-ttu-id="4e7c4-156">Las siguientes son algunas de las expresiones XPath de este elemento:</span><span class="sxs-lookup"><span data-stu-id="4e7c4-156">The following are some of the XPath expressions to this element:</span></span><br/><br/>  `/CalendarItem/ConflictingMeetings` <br/>  `/MeetingRequest/ConflictingMeetings` <br/>  `/SetItemField/CalendarItem/ConflictingMeetings` <br/>  `/AppendToItemField/CalendarItem/ConflictingMeetings` <br/>  `/AcceptItem/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/>  `/DeclineItem/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/>  `/TentativelyAcceptItem/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/>  `/UpdateItem/ItemChanges/ItemChange/Updates/SetItemField/CalendarItem/ConflictingMeetings` <br/>  `/UpdateItem/ItemChanges/ItemChange/Updates/AppendToItemField/CalendarItem/ConflictingMeetings` <br/>  `/CreateAttachmentResponseMessage/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/>  `/GetAttachmentResponseMessage/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/> |
|[<span data-ttu-id="4e7c4-157">ResponseObjects</span><span class="sxs-lookup"><span data-stu-id="4e7c4-157">ResponseObjects</span></span>](responseobjects.md) <br/> |<span data-ttu-id="4e7c4-158">Contiene una colección de todos los objetos de respuesta que están asociados a un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="4e7c4-158">Contains a collection of all the response objects that are associated with an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="4e7c4-159">Elementos (NonEmptyArrayOfAllItemsType)</span><span class="sxs-lookup"><span data-stu-id="4e7c4-159">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md) <br/> |<span data-ttu-id="4e7c4-160">Contiene una matriz de elementos que se van a crear en la carpeta identificada por el elemento [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) .</span><span class="sxs-lookup"><span data-stu-id="4e7c4-160">Contains an array of items to create in the folder identified by the [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) element.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4e7c4-161">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4e7c4-161">Remarks</span></span>

<span data-ttu-id="4e7c4-162">El esquema que describe este elemento se encuentra en el directorio EWS del servidor de Exchange que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="4e7c4-162">The schema that describes this element is located in the EWS directory of the Exchange server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4e7c4-163">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="4e7c4-163">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4e7c4-164">Namespace</span><span class="sxs-lookup"><span data-stu-id="4e7c4-164">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="4e7c4-165">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="4e7c4-165">Schema Name</span></span>  <br/> |<span data-ttu-id="4e7c4-166">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="4e7c4-166">Types schema</span></span>  <br/> |
|<span data-ttu-id="4e7c4-167">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="4e7c4-167">Validation File</span></span>  <br/> |<span data-ttu-id="4e7c4-168">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="4e7c4-168">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="4e7c4-169">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="4e7c4-169">Can be Empty</span></span>  <br/> |<span data-ttu-id="4e7c4-170">Falso</span><span class="sxs-lookup"><span data-stu-id="4e7c4-170">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4e7c4-171">Vea también</span><span class="sxs-lookup"><span data-stu-id="4e7c4-171">See also</span></span>

- [<span data-ttu-id="4e7c4-172">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="4e7c4-172">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

