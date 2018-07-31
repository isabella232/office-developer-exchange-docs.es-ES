---
title: ItemAttachment
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ItemAttachment
api_type:
- schema
ms.assetid: 089ee599-f45e-46f5-a18a-5cfb3d2851ff
description: El elemento ItemAttachment representa un elemento de Exchange que está vinculado a otro elemento de Exchange.
ms.openlocfilehash: 7bd3d22430fe04f1b28ae240102500609fe8d703
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/28/2018
ms.locfileid: "21353150"
---
# <a name="itemattachment"></a><span data-ttu-id="4c6c4-103">ItemAttachment</span><span class="sxs-lookup"><span data-stu-id="4c6c4-103">ItemAttachment</span></span>

<span data-ttu-id="4c6c4-104">El elemento **ItemAttachment** representa un elemento de Exchange que está vinculado a otro elemento de Exchange.</span><span class="sxs-lookup"><span data-stu-id="4c6c4-104">The **ItemAttachment** element represents an Exchange item that is attached to another Exchange item.</span></span> 
  
```xml
<ItemAttachment>
   <AttachmentId/>
   <Name/>
   <ContentType/>
   <ContentId/>
   <ContentLocation/>
   <Size/>
   <LastModifiedTime/>
   <IsInline/>
   <Item/>
</ItemAttachment>
```

```xml
<ItemAttachment>
   <AttachmentId/>
   <Name/>
   <ContentType/>
   <ContentId/>
   <ContentLocation/>
   <Size/>
   <LastModifiedTime/>
   <IsInline/>
   <Message/>
</ItemAttachment>
```

```xml
<ItemAttachment>
   <AttachmentId/>
   <Name/>
   <ContentType/>
   <ContentId/>
   <ContentLocation/>
   <Size/>
   <LastModifiedTime/>
   <IsInline/>
   <CalendarItem/>
</ItemAttachment>
```

```xml
<ItemAttachment>
   <AttachmentId/>
   <Name/>
   <ContentType/>
   <ContentId/>
   <ContentLocation/>
   <Size/>
   <LastModifiedTime/>
   <IsInline/>
   <Contact/>
</ItemAttachment>
```

```xml
<ItemAttachment>
   <AttachmentId/>
   <Name/>
   <ContentType/>
   <ContentId/>
   <ContentLocation/>
   <Size/>
   <LastModifiedTime/>
   <IsInline/>
   <Task/>
</ItemAttachment>
```

```xml
<ItemAttachment>
   <AttachmentId/>
   <Name/>
   <ContentType/>
   <ContentId/>
   <ContentLocation/>
   <Size/>
   <LastModifiedTime/>
   <IsInline/>
   <MeetingMessage/>
</ItemAttachment>
```

```xml
<ItemAttachment>
   <AttachmentId/>
   <Name/>
   <ContentType/>
   <ContentId/>
   <ContentLocation/>
   <Size/>
   <LastModifiedTime/>
   <IsInline/>
   <MeetingRequest/>
</ItemAttachment>
```

```xml
<ItemAttachment>
   <AttachmentId/>
   <Name/>
   <ContentType/>
   <ContentId/>
   <ContentLocation/>
   <Size/>
   <LastModifiedTime/>
   <IsInline/>
   <MeetingResponse/>
</ItemAttachment>
```

```xml
<ItemAttachment>
   <AttachmentId/>
   <Name/>
   <ContentType/>
   <ContentId/>
   <ContentLocation/>
   <Size/>
   <LastModifiedTime/>
   <IsInline/>
   <MeetingCancellation/>
</ItemAttachment>
```

<span data-ttu-id="4c6c4-105">**ItemAttachmentType**</span><span class="sxs-lookup"><span data-stu-id="4c6c4-105">**ItemAttachmentType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="4c6c4-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="4c6c4-106">Attributes and elements</span></span>

<span data-ttu-id="4c6c4-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="4c6c4-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4c6c4-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="4c6c4-108">Attributes</span></span>

<span data-ttu-id="4c6c4-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="4c6c4-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4c6c4-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="4c6c4-110">Child elements</span></span>

|<span data-ttu-id="4c6c4-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="4c6c4-111">**Element**</span></span>|<span data-ttu-id="4c6c4-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4c6c4-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4c6c4-113">AttachmentId</span><span class="sxs-lookup"><span data-stu-id="4c6c4-113">AttachmentId</span></span>](attachmentid.md) <br/> |<span data-ttu-id="4c6c4-114">Identifica los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="4c6c4-114">Identifies the attachment.</span></span>  <br/> |
|[<span data-ttu-id="4c6c4-115">Name (AttachmentType)</span><span class="sxs-lookup"><span data-stu-id="4c6c4-115">Name (AttachmentType)</span></span>](name-attachmenttype.md) <br/> |<span data-ttu-id="4c6c4-116">Representa el nombre de los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="4c6c4-116">Represents the name of the attachment.</span></span>  <br/> |
|[<span data-ttu-id="4c6c4-117">ContentType</span><span class="sxs-lookup"><span data-stu-id="4c6c4-117">ContentType</span></span>](contenttype.md) <br/> |<span data-ttu-id="4c6c4-118">Describe el tipo de extensiones multipropósito de correo Internet (MIME) del contenido de los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="4c6c4-118">Describes the Multipurpose Internet Mail Extensions (MIME) type of the attachment content.</span></span>  <br/> |
|[<span data-ttu-id="4c6c4-119">ContentId</span><span class="sxs-lookup"><span data-stu-id="4c6c4-119">ContentId</span></span>](contentid.md) <br/> |<span data-ttu-id="4c6c4-120">Representa un identificador para el contenido de los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="4c6c4-120">Represents an identifier to the contents of the attachment.</span></span> <span data-ttu-id="4c6c4-121">[ContentId](contentid.md) se puede establecer en cualquier valor de cadena.</span><span class="sxs-lookup"><span data-stu-id="4c6c4-121">[ContentId](contentid.md) can be set to any string value.</span></span> <span data-ttu-id="4c6c4-122">Las aplicaciones pueden usar [ContentId](contentid.md) para implementar sus propios mecanismos de identificación.</span><span class="sxs-lookup"><span data-stu-id="4c6c4-122">Applications can use [ContentId](contentid.md) to implement their own identification mechanisms.</span></span>  <br/> |
|[<span data-ttu-id="4c6c4-123">ContentLocation</span><span class="sxs-lookup"><span data-stu-id="4c6c4-123">ContentLocation</span></span>](contentlocation.md) <br/> |<span data-ttu-id="4c6c4-124">Contiene el identificador uniforme de recursos (URI) que corresponde a la ubicación del contenido de los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="4c6c4-124">Contains the Uniform Resource Identifier (URI) that corresponds to the location of the content of the attachment.</span></span>  <br/> |
|[<span data-ttu-id="4c6c4-125">Size</span><span class="sxs-lookup"><span data-stu-id="4c6c4-125">Size</span></span>](size.md) <br/> |<span data-ttu-id="4c6c4-126">Representa el tamaño en bytes del archivo adjunto.</span><span class="sxs-lookup"><span data-stu-id="4c6c4-126">Represents the size in bytes of the file attachment.</span></span>  <br/> |
|[<span data-ttu-id="4c6c4-127">LastModifiedTime</span><span class="sxs-lookup"><span data-stu-id="4c6c4-127">LastModifiedTime</span></span>](lastmodifiedtime.md) <br/> |<span data-ttu-id="4c6c4-128">Representa cuando se modificó por última vez los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="4c6c4-128">Represents when the attachment was last modified.</span></span>  <br/> |
|[<span data-ttu-id="4c6c4-129">IsInline</span><span class="sxs-lookup"><span data-stu-id="4c6c4-129">IsInline</span></span>](isinline.md) <br/> |<span data-ttu-id="4c6c4-130">Representa si el archivo adjunto aparece en línea dentro de un elemento.</span><span class="sxs-lookup"><span data-stu-id="4c6c4-130">Represents whether the attachment appears inline within an item.</span></span>  <br/> |
|[<span data-ttu-id="4c6c4-131">Item</span><span class="sxs-lookup"><span data-stu-id="4c6c4-131">Item</span></span>](item.md) <br/> |<span data-ttu-id="4c6c4-132">Representa los datos adjuntos un elemento genérico de Exchange.</span><span class="sxs-lookup"><span data-stu-id="4c6c4-132">Represents a generic Exchange item attachment.</span></span>  <br/> |
|[<span data-ttu-id="4c6c4-133">Message</span><span class="sxs-lookup"><span data-stu-id="4c6c4-133">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="4c6c4-134">Representa los datos adjuntos un mensaje de correo electrónico de Exchange.</span><span class="sxs-lookup"><span data-stu-id="4c6c4-134">Represents an Exchange e-mail message attachment.</span></span>  <br/> |
|[<span data-ttu-id="4c6c4-135">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="4c6c4-135">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="4c6c4-136">Representa los datos adjuntos un elemento de calendario de Exchange.</span><span class="sxs-lookup"><span data-stu-id="4c6c4-136">Represents an Exchange calendar item attachment.</span></span>  <br/> |
|[<span data-ttu-id="4c6c4-137">Contact</span><span class="sxs-lookup"><span data-stu-id="4c6c4-137">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="4c6c4-138">Representa datos adjuntos del elemento de contacto de Exchange.</span><span class="sxs-lookup"><span data-stu-id="4c6c4-138">Represents an Exchange contact item attachment.</span></span>  <br/> |
|[<span data-ttu-id="4c6c4-139">Tarea</span><span class="sxs-lookup"><span data-stu-id="4c6c4-139">Task</span></span>](task.md) <br/> |<span data-ttu-id="4c6c4-140">Representa datos adjuntos de tareas de Exchange.</span><span class="sxs-lookup"><span data-stu-id="4c6c4-140">Represents an Exchange task attachment.</span></span>  <br/> |
|[<span data-ttu-id="4c6c4-141">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="4c6c4-141">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="4c6c4-142">Representa una reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="4c6c4-142">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="4c6c4-143">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="4c6c4-143">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="4c6c4-144">Representa una convocatoria de reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="4c6c4-144">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="4c6c4-145">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="4c6c4-145">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="4c6c4-146">Representa una respuesta a la reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="4c6c4-146">Represents a meeting response in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="4c6c4-147">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="4c6c4-147">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="4c6c4-148">Representa la cancelación de la reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="4c6c4-148">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="4c6c4-149">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="4c6c4-149">Parent elements</span></span>

|<span data-ttu-id="4c6c4-150">**Element**</span><span class="sxs-lookup"><span data-stu-id="4c6c4-150">**Element**</span></span>|<span data-ttu-id="4c6c4-151">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4c6c4-151">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4c6c4-152">Datos adjuntos</span><span class="sxs-lookup"><span data-stu-id="4c6c4-152">Attachments</span></span>](attachments-ex15websvcsotherref.md) <br/> |<span data-ttu-id="4c6c4-153">Contiene los elementos o archivos que están adjuntos a un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="4c6c4-153">Contains the items and/or files that are attached to an item in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="4c6c4-154">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="4c6c4-154">Text value</span></span>

<span data-ttu-id="4c6c4-155">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="4c6c4-155">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4c6c4-156">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4c6c4-156">Remarks</span></span>

<span data-ttu-id="4c6c4-157">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="4c6c4-157">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4c6c4-158">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="4c6c4-158">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4c6c4-159">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="4c6c4-159">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="4c6c4-160">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="4c6c4-160">Schema Name</span></span>  <br/> |<span data-ttu-id="4c6c4-161">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="4c6c4-161">Types schema</span></span>  <br/> |
|<span data-ttu-id="4c6c4-162">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="4c6c4-162">Validation File</span></span>  <br/> |<span data-ttu-id="4c6c4-163">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="4c6c4-163">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="4c6c4-164">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="4c6c4-164">Can be Empty</span></span>  <br/> |<span data-ttu-id="4c6c4-165">False</span><span class="sxs-lookup"><span data-stu-id="4c6c4-165">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4c6c4-166">Vea también</span><span class="sxs-lookup"><span data-stu-id="4c6c4-166">See also</span></span>

- [<span data-ttu-id="4c6c4-167">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="4c6c4-167">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

