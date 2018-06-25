---
title: Datos adjuntos
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Attachments
api_type:
- schema
ms.assetid: b470e614-34bb-44f0-8790-7ddbdcbbd29d
description: El elemento de datos adjuntos contiene los elementos o archivos que se adjuntan a un elemento en el almacén de Exchange.
ms.openlocfilehash: 8aa5c0849122f5ca83485459fce5d0fea449c974
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763572"
---
# <a name="attachments"></a><span data-ttu-id="583c0-103">Datos adjuntos</span><span class="sxs-lookup"><span data-stu-id="583c0-103">Attachments</span></span>

<span data-ttu-id="583c0-104">El elemento de **datos adjuntos** contiene los elementos o archivos que se adjuntan a un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="583c0-104">The **Attachments** element contains the items or files that are attached to an item in the Exchange store.</span></span> 
  
```xml
<Attachments>
   <ItemAttachment/>
   <FileAttachment/>
</Attachments>
```

 <span data-ttu-id="583c0-105">**ArrayOfAttachmentsType** y **NonEmptyArrayOfAttachmentsType**</span><span class="sxs-lookup"><span data-stu-id="583c0-105">**ArrayOfAttachmentsType** and **NonEmptyArrayOfAttachmentsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="583c0-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="583c0-106">Attributes and elements</span></span>

<span data-ttu-id="583c0-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="583c0-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="583c0-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="583c0-108">Attributes</span></span>

<span data-ttu-id="583c0-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="583c0-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="583c0-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="583c0-110">Child elements</span></span>

|<span data-ttu-id="583c0-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="583c0-111">**Element**</span></span>|<span data-ttu-id="583c0-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="583c0-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="583c0-113">ItemAttachment</span><span class="sxs-lookup"><span data-stu-id="583c0-113">ItemAttachment</span></span>](itemattachment.md) <br/> |<span data-ttu-id="583c0-114">Representa un elemento de Exchange que está vinculado a otro elemento de Exchange.</span><span class="sxs-lookup"><span data-stu-id="583c0-114">Represents an Exchange item that is attached to another Exchange item.</span></span>  <br/> |
|[<span data-ttu-id="583c0-115">FileAttachment</span><span class="sxs-lookup"><span data-stu-id="583c0-115">FileAttachment</span></span>](fileattachment.md) <br/> |<span data-ttu-id="583c0-116">Representa un archivo que se adjunta a un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="583c0-116">Represents a file that is attached to an item in the Exchange store.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="583c0-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="583c0-117">Parent elements</span></span>

|<span data-ttu-id="583c0-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="583c0-118">**Element**</span></span>|<span data-ttu-id="583c0-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="583c0-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="583c0-120">CreateAttachment</span><span class="sxs-lookup"><span data-stu-id="583c0-120">CreateAttachment</span></span>](createattachment.md) <br/> |<span data-ttu-id="583c0-121">Define una solicitud para crear un archivo adjunto a un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="583c0-121">Defines a request to create an attachment to an item in the Exchange store.</span></span><br/><br/> <span data-ttu-id="583c0-122">La siguiente es la expresión de XPath para este elemento:`/CreateAttachment`</span><span class="sxs-lookup"><span data-stu-id="583c0-122">The following is the XPath expression to this element:  `/CreateAttachment`</span></span> <br/> |
|[<span data-ttu-id="583c0-123">AcceptItem</span><span class="sxs-lookup"><span data-stu-id="583c0-123">AcceptItem</span></span>](acceptitem.md) <br/> | <span data-ttu-id="583c0-124">Representa una respuesta a Aceptar a una convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="583c0-124">Represents an Accept reply to a meeting request.</span></span><br/><br/><span data-ttu-id="583c0-125">Las siguientes son algunas de las expresiones de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="583c0-125">The following are some of the XPath expressions to this element:</span></span><ul><li>`/CreateItem/Items`</li><li>`/MeetingRequest/ConflictingMeetings` </li><li>`/SetItemField/CalendarItem/ConflictingMeetings`</li><li>`/AppendToItemField/CalendarItem/ConflictingMeetings`</li><li>`/AcceptItem/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings`</li><li>`/DeclineItem/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings`</li><li>`/UpdateItem/ItemChanges/ItemChange/Updates/AppendToItemField/CalendarItem/AdjacentMeetings`</li><li>`/CreateAttachmentResponseMessage/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings`</li><li>`/GetAttachmentResponseMessage/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings`</li></ul> |
|[<span data-ttu-id="583c0-126">DeclineItem</span><span class="sxs-lookup"><span data-stu-id="583c0-126">DeclineItem</span></span>](declineitem.md) <br/> |<span data-ttu-id="583c0-127">Representa una respuesta de rechazo a una convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="583c0-127">Represents a Decline reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="583c0-128">TentativelyAcceptItem</span><span class="sxs-lookup"><span data-stu-id="583c0-128">TentativelyAcceptItem</span></span>](tentativelyacceptitem.md) <br/> |<span data-ttu-id="583c0-129">Representa un provisional responde a una convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="583c0-129">Represents a Tentative reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="583c0-130">RemoveItem</span><span class="sxs-lookup"><span data-stu-id="583c0-130">RemoveItem</span></span>](removeitem.md) <br/> |<span data-ttu-id="583c0-131">Quita un elemento desde el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="583c0-131">Removes an item from the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="583c0-132">Item</span><span class="sxs-lookup"><span data-stu-id="583c0-132">Item</span></span>](item.md) <br/> |<span data-ttu-id="583c0-133">Representa un elemento genérico de Exchange.</span><span class="sxs-lookup"><span data-stu-id="583c0-133">Represents a generic Exchange item.</span></span>  <br/> |
|[<span data-ttu-id="583c0-134">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="583c0-134">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="583c0-135">Representa una reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="583c0-135">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="583c0-136">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="583c0-136">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="583c0-137">Representa una convocatoria de reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="583c0-137">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="583c0-138">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="583c0-138">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="583c0-139">Representa una respuesta a la reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="583c0-139">Represents a meeting response in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="583c0-140">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="583c0-140">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="583c0-141">Representa la cancelación de la reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="583c0-141">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="583c0-142">Message</span><span class="sxs-lookup"><span data-stu-id="583c0-142">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="583c0-143">Representa un mensaje de correo electrónico de Exchange.</span><span class="sxs-lookup"><span data-stu-id="583c0-143">Represents an Exchange e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="583c0-144">Tarea</span><span class="sxs-lookup"><span data-stu-id="583c0-144">Task</span></span>](task.md) <br/> |<span data-ttu-id="583c0-145">Representa una tarea en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="583c0-145">Represents a task in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="583c0-146">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="583c0-146">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="583c0-147">Representa un elemento de calendario de Exchange.</span><span class="sxs-lookup"><span data-stu-id="583c0-147">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="583c0-148">Contact</span><span class="sxs-lookup"><span data-stu-id="583c0-148">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="583c0-149">Representa un elemento de contacto de Exchange.</span><span class="sxs-lookup"><span data-stu-id="583c0-149">Represents an Exchange contact item.</span></span>  <br/> |
|[<span data-ttu-id="583c0-150">DistributionList</span><span class="sxs-lookup"><span data-stu-id="583c0-150">DistributionList</span></span>](distributionlist.md) <br/> |<span data-ttu-id="583c0-151">Representa una lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="583c0-151">Represents a distribution list.</span></span>  <br/> |
|[<span data-ttu-id="583c0-152">CreateAttachmentResponseMessage</span><span class="sxs-lookup"><span data-stu-id="583c0-152">CreateAttachmentResponseMessage</span></span>](createattachmentresponsemessage.md) <br/> |<span data-ttu-id="583c0-153">Contiene el estado y el resultado de una única solicitud CreateAttachment.</span><span class="sxs-lookup"><span data-stu-id="583c0-153">Contains the status and result of a single CreateAttachment request.</span></span>  <br/> |
|[<span data-ttu-id="583c0-154">GetAttachmentResponseMessage</span><span class="sxs-lookup"><span data-stu-id="583c0-154">GetAttachmentResponseMessage</span></span>](getattachmentresponsemessage.md) <br/> |<span data-ttu-id="583c0-155">Contiene el estado y el resultado de una solicitud de GetAttachment.</span><span class="sxs-lookup"><span data-stu-id="583c0-155">Contains the status and result of a GetAttachment request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="583c0-156">Comentarios</span><span class="sxs-lookup"><span data-stu-id="583c0-156">Remarks</span></span>

<span data-ttu-id="583c0-157">Los elementos de **los datos adjuntos** tienen los mismos elementos secundarios pero se basan en los distintos tipos: **ArrayOfAttachmentsType** y **NonEmptyArrayOfAttachmentsType**.</span><span class="sxs-lookup"><span data-stu-id="583c0-157">The **Attachments** elements have the same child elements but are based on different types: **ArrayOfAttachmentsType** and **NonEmptyArrayOfAttachmentsType**.</span></span> <span data-ttu-id="583c0-158">Los tipos de definición si se requiere un elemento secundario.</span><span class="sxs-lookup"><span data-stu-id="583c0-158">The types define whether a child element is required.</span></span> <span data-ttu-id="583c0-159">El **ArrayOfAttachmentsType** solo se usa en el mensaje de respuesta.</span><span class="sxs-lookup"><span data-stu-id="583c0-159">The **ArrayOfAttachmentsType** is only used in the response message.</span></span> <span data-ttu-id="583c0-160">También es importante tener en cuenta que estos elementos se producen en los mensajes y tipos de espacios de nombres.</span><span class="sxs-lookup"><span data-stu-id="583c0-160">It is also important to note that these elements occur in both the messages and types namespaces.</span></span> 
  
<span data-ttu-id="583c0-161">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="583c0-161">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="583c0-162">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="583c0-162">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="583c0-163">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="583c0-163">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="583c0-164">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="583c0-164">Schema Name</span></span>  <br/> |<span data-ttu-id="583c0-165">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="583c0-165">Types schema</span></span>  <br/> |
|<span data-ttu-id="583c0-166">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="583c0-166">Validation File</span></span>  <br/> |<span data-ttu-id="583c0-167">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="583c0-167">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="583c0-168">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="583c0-168">Can be Empty</span></span>  <br/> |<span data-ttu-id="583c0-169">False</span><span class="sxs-lookup"><span data-stu-id="583c0-169">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="583c0-170">Vea también</span><span class="sxs-lookup"><span data-stu-id="583c0-170">See also</span></span>

- [<span data-ttu-id="583c0-171">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="583c0-171">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

