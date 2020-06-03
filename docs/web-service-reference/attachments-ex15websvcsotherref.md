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
description: El elemento Attachments contiene los elementos o archivos que están adjuntos a un elemento en el almacén de Exchange.
ms.openlocfilehash: a9f79cd79f19e6226703c99c53c91efed600f495
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461537"
---
# <a name="attachments"></a><span data-ttu-id="8c3a3-103">Datos adjuntos</span><span class="sxs-lookup"><span data-stu-id="8c3a3-103">Attachments</span></span>

<span data-ttu-id="8c3a3-104">El elemento **Attachments** contiene los elementos o archivos que están adjuntos a un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="8c3a3-104">The **Attachments** element contains the items or files that are attached to an item in the Exchange store.</span></span> 
  
```xml
<Attachments>
   <ItemAttachment/>
   <FileAttachment/>
</Attachments>
```

 <span data-ttu-id="8c3a3-105">**ArrayOfAttachmentsType** y **NonEmptyArrayOfAttachmentsType**</span><span class="sxs-lookup"><span data-stu-id="8c3a3-105">**ArrayOfAttachmentsType** and **NonEmptyArrayOfAttachmentsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="8c3a3-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="8c3a3-106">Attributes and elements</span></span>

<span data-ttu-id="8c3a3-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="8c3a3-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8c3a3-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="8c3a3-108">Attributes</span></span>

<span data-ttu-id="8c3a3-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="8c3a3-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="8c3a3-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="8c3a3-110">Child elements</span></span>

|<span data-ttu-id="8c3a3-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="8c3a3-111">**Element**</span></span>|<span data-ttu-id="8c3a3-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8c3a3-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8c3a3-113">ItemAttachment</span><span class="sxs-lookup"><span data-stu-id="8c3a3-113">ItemAttachment</span></span>](itemattachment.md) <br/> |<span data-ttu-id="8c3a3-114">Representa un elemento de Exchange que está adjunto a otro elemento de Exchange.</span><span class="sxs-lookup"><span data-stu-id="8c3a3-114">Represents an Exchange item that is attached to another Exchange item.</span></span>  <br/> |
|[<span data-ttu-id="8c3a3-115">FileAttachment</span><span class="sxs-lookup"><span data-stu-id="8c3a3-115">FileAttachment</span></span>](fileattachment.md) <br/> |<span data-ttu-id="8c3a3-116">Representa un archivo que está adjunto a un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="8c3a3-116">Represents a file that is attached to an item in the Exchange store.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="8c3a3-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="8c3a3-117">Parent elements</span></span>

|<span data-ttu-id="8c3a3-118">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="8c3a3-118">**Element**</span></span>|<span data-ttu-id="8c3a3-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8c3a3-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8c3a3-120">CreateAttachment</span><span class="sxs-lookup"><span data-stu-id="8c3a3-120">CreateAttachment</span></span>](createattachment.md) <br/> |<span data-ttu-id="8c3a3-121">Define una solicitud para crear datos adjuntos a un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="8c3a3-121">Defines a request to create an attachment to an item in the Exchange store.</span></span><br/><br/> <span data-ttu-id="8c3a3-122">La siguiente es la expresión XPath a este elemento:`/CreateAttachment`</span><span class="sxs-lookup"><span data-stu-id="8c3a3-122">The following is the XPath expression to this element:  `/CreateAttachment`</span></span> <br/> |
|[<span data-ttu-id="8c3a3-123">AcceptItem</span><span class="sxs-lookup"><span data-stu-id="8c3a3-123">AcceptItem</span></span>](acceptitem.md) <br/> | <span data-ttu-id="8c3a3-124">Representa una respuesta de aceptación para una convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="8c3a3-124">Represents an Accept reply to a meeting request.</span></span><br/><br/><span data-ttu-id="8c3a3-125">Las siguientes son algunas de las expresiones XPath de este elemento:</span><span class="sxs-lookup"><span data-stu-id="8c3a3-125">The following are some of the XPath expressions to this element:</span></span><ul><li>`/CreateItem/Items`</li><li>`/MeetingRequest/ConflictingMeetings` </li><li>`/SetItemField/CalendarItem/ConflictingMeetings`</li><li>`/AppendToItemField/CalendarItem/ConflictingMeetings`</li><li>`/AcceptItem/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings`</li><li>`/DeclineItem/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings`</li><li>`/UpdateItem/ItemChanges/ItemChange/Updates/AppendToItemField/CalendarItem/AdjacentMeetings`</li><li>`/CreateAttachmentResponseMessage/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings`</li><li>`/GetAttachmentResponseMessage/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings`</li></ul> |
|[<span data-ttu-id="8c3a3-126">DeclineItem</span><span class="sxs-lookup"><span data-stu-id="8c3a3-126">DeclineItem</span></span>](declineitem.md) <br/> |<span data-ttu-id="8c3a3-127">Representa una respuesta de rechazo a una convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="8c3a3-127">Represents a Decline reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="8c3a3-128">TentativelyAcceptItem</span><span class="sxs-lookup"><span data-stu-id="8c3a3-128">TentativelyAcceptItem</span></span>](tentativelyacceptitem.md) <br/> |<span data-ttu-id="8c3a3-129">Representa una respuesta provisional a una convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="8c3a3-129">Represents a Tentative reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="8c3a3-130">RemoveItem</span><span class="sxs-lookup"><span data-stu-id="8c3a3-130">RemoveItem</span></span>](removeitem.md) <br/> |<span data-ttu-id="8c3a3-131">Quita un elemento del almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="8c3a3-131">Removes an item from the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="8c3a3-132">Elemento</span><span class="sxs-lookup"><span data-stu-id="8c3a3-132">Item</span></span>](item.md) <br/> |<span data-ttu-id="8c3a3-133">Representa un elemento de Exchange genérico.</span><span class="sxs-lookup"><span data-stu-id="8c3a3-133">Represents a generic Exchange item.</span></span>  <br/> |
|[<span data-ttu-id="8c3a3-134">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="8c3a3-134">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="8c3a3-135">Representa una reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="8c3a3-135">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="8c3a3-136">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="8c3a3-136">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="8c3a3-137">Representa una convocatoria de reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="8c3a3-137">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="8c3a3-138">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="8c3a3-138">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="8c3a3-139">Representa una respuesta a una reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="8c3a3-139">Represents a meeting response in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="8c3a3-140">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="8c3a3-140">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="8c3a3-141">Representa una cancelación de reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="8c3a3-141">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="8c3a3-142">Message</span><span class="sxs-lookup"><span data-stu-id="8c3a3-142">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="8c3a3-143">Representa un mensaje de correo electrónico de Exchange.</span><span class="sxs-lookup"><span data-stu-id="8c3a3-143">Represents an Exchange e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="8c3a3-144">Tarea</span><span class="sxs-lookup"><span data-stu-id="8c3a3-144">Task</span></span>](task.md) <br/> |<span data-ttu-id="8c3a3-145">Representa una tarea del almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="8c3a3-145">Represents a task in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="8c3a3-146">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="8c3a3-146">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="8c3a3-147">Representa un elemento de calendario de Exchange.</span><span class="sxs-lookup"><span data-stu-id="8c3a3-147">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="8c3a3-148">Contacto</span><span class="sxs-lookup"><span data-stu-id="8c3a3-148">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="8c3a3-149">Representa un elemento de contacto de Exchange.</span><span class="sxs-lookup"><span data-stu-id="8c3a3-149">Represents an Exchange contact item.</span></span>  <br/> |
|[<span data-ttu-id="8c3a3-150">DistributionList</span><span class="sxs-lookup"><span data-stu-id="8c3a3-150">DistributionList</span></span>](distributionlist.md) <br/> |<span data-ttu-id="8c3a3-151">Representa una lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="8c3a3-151">Represents a distribution list.</span></span>  <br/> |
|[<span data-ttu-id="8c3a3-152">CreateAttachmentResponseMessage</span><span class="sxs-lookup"><span data-stu-id="8c3a3-152">CreateAttachmentResponseMessage</span></span>](createattachmentresponsemessage.md) <br/> |<span data-ttu-id="8c3a3-153">Contiene el estado y el resultado de una sola solicitud CreateAttachment.</span><span class="sxs-lookup"><span data-stu-id="8c3a3-153">Contains the status and result of a single CreateAttachment request.</span></span>  <br/> |
|[<span data-ttu-id="8c3a3-154">GetAttachmentResponseMessage</span><span class="sxs-lookup"><span data-stu-id="8c3a3-154">GetAttachmentResponseMessage</span></span>](getattachmentresponsemessage.md) <br/> |<span data-ttu-id="8c3a3-155">Contiene el estado y el resultado de una solicitud GetAttachment.</span><span class="sxs-lookup"><span data-stu-id="8c3a3-155">Contains the status and result of a GetAttachment request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8c3a3-156">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8c3a3-156">Remarks</span></span>

<span data-ttu-id="8c3a3-157">Los elementos **Attachments** tienen los mismos elementos secundarios, pero se basan en tipos distintos: **ArrayOfAttachmentsType** y **NonEmptyArrayOfAttachmentsType**.</span><span class="sxs-lookup"><span data-stu-id="8c3a3-157">The **Attachments** elements have the same child elements but are based on different types: **ArrayOfAttachmentsType** and **NonEmptyArrayOfAttachmentsType**.</span></span> <span data-ttu-id="8c3a3-158">Los tipos definen si un elemento secundario es necesario.</span><span class="sxs-lookup"><span data-stu-id="8c3a3-158">The types define whether a child element is required.</span></span> <span data-ttu-id="8c3a3-159">**ArrayOfAttachmentsType** solo se usa en el mensaje de respuesta.</span><span class="sxs-lookup"><span data-stu-id="8c3a3-159">The **ArrayOfAttachmentsType** is only used in the response message.</span></span> <span data-ttu-id="8c3a3-160">También es importante tener en cuenta que estos elementos se producen en los espacios de nombres messages y Types.</span><span class="sxs-lookup"><span data-stu-id="8c3a3-160">It is also important to note that these elements occur in both the messages and types namespaces.</span></span> 
  
<span data-ttu-id="8c3a3-161">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="8c3a3-161">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8c3a3-162">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="8c3a3-162">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8c3a3-163">Namespace</span><span class="sxs-lookup"><span data-stu-id="8c3a3-163">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="8c3a3-164">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="8c3a3-164">Schema Name</span></span>  <br/> |<span data-ttu-id="8c3a3-165">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="8c3a3-165">Types schema</span></span>  <br/> |
|<span data-ttu-id="8c3a3-166">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="8c3a3-166">Validation File</span></span>  <br/> |<span data-ttu-id="8c3a3-167">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="8c3a3-167">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="8c3a3-168">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="8c3a3-168">Can be Empty</span></span>  <br/> |<span data-ttu-id="8c3a3-169">Falso</span><span class="sxs-lookup"><span data-stu-id="8c3a3-169">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8c3a3-170">Vea también</span><span class="sxs-lookup"><span data-stu-id="8c3a3-170">See also</span></span>

- [<span data-ttu-id="8c3a3-171">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="8c3a3-171">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

