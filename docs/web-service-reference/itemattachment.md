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
description: El elemento ItemAttachment representa un elemento de Exchange que está adjunto a otro elemento de Exchange.
ms.openlocfilehash: c3a07fa091c05654a03cbff58fb20204c26c9061
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526441"
---
# <a name="itemattachment"></a><span data-ttu-id="96e2d-103">ItemAttachment</span><span class="sxs-lookup"><span data-stu-id="96e2d-103">ItemAttachment</span></span>

<span data-ttu-id="96e2d-104">El elemento **ItemAttachment** representa un elemento de Exchange que está adjunto a otro elemento de Exchange.</span><span class="sxs-lookup"><span data-stu-id="96e2d-104">The **ItemAttachment** element represents an Exchange item that is attached to another Exchange item.</span></span> 
  
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

<span data-ttu-id="96e2d-105">**ItemAttachmentType**</span><span class="sxs-lookup"><span data-stu-id="96e2d-105">**ItemAttachmentType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="96e2d-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="96e2d-106">Attributes and elements</span></span>

<span data-ttu-id="96e2d-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="96e2d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="96e2d-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="96e2d-108">Attributes</span></span>

<span data-ttu-id="96e2d-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="96e2d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="96e2d-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="96e2d-110">Child elements</span></span>

|<span data-ttu-id="96e2d-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="96e2d-111">**Element**</span></span>|<span data-ttu-id="96e2d-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="96e2d-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="96e2d-113">AttachmentId</span><span class="sxs-lookup"><span data-stu-id="96e2d-113">AttachmentId</span></span>](attachmentid.md) <br/> |<span data-ttu-id="96e2d-114">Identifica los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="96e2d-114">Identifies the attachment.</span></span>  <br/> |
|[<span data-ttu-id="96e2d-115">Nombre (AttachmentType)</span><span class="sxs-lookup"><span data-stu-id="96e2d-115">Name (AttachmentType)</span></span>](name-attachmenttype.md) <br/> |<span data-ttu-id="96e2d-116">Representa el nombre de los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="96e2d-116">Represents the name of the attachment.</span></span>  <br/> |
|[<span data-ttu-id="96e2d-117">ContentType</span><span class="sxs-lookup"><span data-stu-id="96e2d-117">ContentType</span></span>](contenttype.md) <br/> |<span data-ttu-id="96e2d-118">Describe el tipo de extensiones multipropósito de correo Internet (MIME) del contenido de datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="96e2d-118">Describes the Multipurpose Internet Mail Extensions (MIME) type of the attachment content.</span></span>  <br/> |
|[<span data-ttu-id="96e2d-119">ContentId</span><span class="sxs-lookup"><span data-stu-id="96e2d-119">ContentId</span></span>](contentid.md) <br/> |<span data-ttu-id="96e2d-120">Representa un identificador para el contenido de los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="96e2d-120">Represents an identifier to the contents of the attachment.</span></span> <span data-ttu-id="96e2d-121">[Contentid](contentid.md) se puede establecer en cualquier valor de cadena.</span><span class="sxs-lookup"><span data-stu-id="96e2d-121">[ContentId](contentid.md) can be set to any string value.</span></span> <span data-ttu-id="96e2d-122">Las aplicaciones pueden usar [contentid](contentid.md) para implementar sus propios mecanismos de identificación.</span><span class="sxs-lookup"><span data-stu-id="96e2d-122">Applications can use [ContentId](contentid.md) to implement their own identification mechanisms.</span></span>  <br/> |
|[<span data-ttu-id="96e2d-123">ContentLocation</span><span class="sxs-lookup"><span data-stu-id="96e2d-123">ContentLocation</span></span>](contentlocation.md) <br/> |<span data-ttu-id="96e2d-124">Contiene el identificador uniforme de recursos (URI) que corresponde a la ubicación del contenido de los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="96e2d-124">Contains the Uniform Resource Identifier (URI) that corresponds to the location of the content of the attachment.</span></span>  <br/> |
|[<span data-ttu-id="96e2d-125">Tamaño</span><span class="sxs-lookup"><span data-stu-id="96e2d-125">Size</span></span>](size.md) <br/> |<span data-ttu-id="96e2d-126">Representa el tamaño en bytes de los datos adjuntos del archivo.</span><span class="sxs-lookup"><span data-stu-id="96e2d-126">Represents the size in bytes of the file attachment.</span></span>  <br/> |
|[<span data-ttu-id="96e2d-127">LastModifiedTime</span><span class="sxs-lookup"><span data-stu-id="96e2d-127">LastModifiedTime</span></span>](lastmodifiedtime.md) <br/> |<span data-ttu-id="96e2d-128">Representa Cuándo se modificó por última vez los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="96e2d-128">Represents when the attachment was last modified.</span></span>  <br/> |
|[<span data-ttu-id="96e2d-129">IsInline</span><span class="sxs-lookup"><span data-stu-id="96e2d-129">IsInline</span></span>](isinline.md) <br/> |<span data-ttu-id="96e2d-130">Indica si los datos adjuntos aparecen en línea dentro de un elemento.</span><span class="sxs-lookup"><span data-stu-id="96e2d-130">Represents whether the attachment appears inline within an item.</span></span>  <br/> |
|[<span data-ttu-id="96e2d-131">Elemento</span><span class="sxs-lookup"><span data-stu-id="96e2d-131">Item</span></span>](item.md) <br/> |<span data-ttu-id="96e2d-132">Representa un elemento de Exchange genérico adjunto.</span><span class="sxs-lookup"><span data-stu-id="96e2d-132">Represents a generic Exchange item attachment.</span></span>  <br/> |
|[<span data-ttu-id="96e2d-133">Message</span><span class="sxs-lookup"><span data-stu-id="96e2d-133">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="96e2d-134">Representa un dato adjunto de un mensaje de correo electrónico de Exchange.</span><span class="sxs-lookup"><span data-stu-id="96e2d-134">Represents an Exchange e-mail message attachment.</span></span>  <br/> |
|[<span data-ttu-id="96e2d-135">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="96e2d-135">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="96e2d-136">Representa un dato adjunto de elemento de calendario de Exchange.</span><span class="sxs-lookup"><span data-stu-id="96e2d-136">Represents an Exchange calendar item attachment.</span></span>  <br/> |
|[<span data-ttu-id="96e2d-137">Contacto</span><span class="sxs-lookup"><span data-stu-id="96e2d-137">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="96e2d-138">Representa un elemento adjunto de un elemento de contacto de Exchange.</span><span class="sxs-lookup"><span data-stu-id="96e2d-138">Represents an Exchange contact item attachment.</span></span>  <br/> |
|[<span data-ttu-id="96e2d-139">Tarea</span><span class="sxs-lookup"><span data-stu-id="96e2d-139">Task</span></span>](task.md) <br/> |<span data-ttu-id="96e2d-140">Representa un archivo adjunto de tarea de Exchange.</span><span class="sxs-lookup"><span data-stu-id="96e2d-140">Represents an Exchange task attachment.</span></span>  <br/> |
|[<span data-ttu-id="96e2d-141">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="96e2d-141">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="96e2d-142">Representa una reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="96e2d-142">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="96e2d-143">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="96e2d-143">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="96e2d-144">Representa una convocatoria de reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="96e2d-144">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="96e2d-145">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="96e2d-145">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="96e2d-146">Representa una respuesta a una reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="96e2d-146">Represents a meeting response in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="96e2d-147">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="96e2d-147">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="96e2d-148">Representa una cancelación de reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="96e2d-148">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="96e2d-149">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="96e2d-149">Parent elements</span></span>

|<span data-ttu-id="96e2d-150">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="96e2d-150">**Element**</span></span>|<span data-ttu-id="96e2d-151">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="96e2d-151">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="96e2d-152">Datos adjuntos</span><span class="sxs-lookup"><span data-stu-id="96e2d-152">Attachments</span></span>](attachments-ex15websvcsotherref.md) <br/> |<span data-ttu-id="96e2d-153">Contiene los elementos o los archivos que están adjuntos a un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="96e2d-153">Contains the items and/or files that are attached to an item in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="96e2d-154">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="96e2d-154">Text value</span></span>

<span data-ttu-id="96e2d-155">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="96e2d-155">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="96e2d-156">Comentarios</span><span class="sxs-lookup"><span data-stu-id="96e2d-156">Remarks</span></span>

<span data-ttu-id="96e2d-157">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="96e2d-157">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="96e2d-158">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="96e2d-158">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="96e2d-159">Namespace</span><span class="sxs-lookup"><span data-stu-id="96e2d-159">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="96e2d-160">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="96e2d-160">Schema Name</span></span>  <br/> |<span data-ttu-id="96e2d-161">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="96e2d-161">Types schema</span></span>  <br/> |
|<span data-ttu-id="96e2d-162">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="96e2d-162">Validation File</span></span>  <br/> |<span data-ttu-id="96e2d-163">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="96e2d-163">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="96e2d-164">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="96e2d-164">Can be Empty</span></span>  <br/> |<span data-ttu-id="96e2d-165">Falso</span><span class="sxs-lookup"><span data-stu-id="96e2d-165">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="96e2d-166">Vea también</span><span class="sxs-lookup"><span data-stu-id="96e2d-166">See also</span></span>

- [<span data-ttu-id="96e2d-167">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="96e2d-167">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

