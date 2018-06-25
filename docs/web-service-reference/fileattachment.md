---
title: FileAttachment
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FileAttachment
api_type:
- schema
ms.assetid: 3ecea174-73d1-47fd-8917-6065cef1d565
description: El elemento FileAttachment representa un archivo que se adjunta a un elemento en el almacén de Exchange.
ms.openlocfilehash: 5ce7aef753313aa9430f640bb3c26f652b8c1c43
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764600"
---
# <a name="fileattachment"></a><span data-ttu-id="e428d-103">FileAttachment</span><span class="sxs-lookup"><span data-stu-id="e428d-103">FileAttachment</span></span>

<span data-ttu-id="e428d-104">El elemento **FileAttachment** representa un archivo que se adjunta a un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="e428d-104">The **FileAttachment** element represents a file that is attached to an item in the Exchange store.</span></span> 
  
```XML
<FileAttachment>
   <AttachmentId/>
   <Name/>
   <ContentType/>
   <ContentId/>
   <ContentLocation/>
   <Size/>
   <LastModifiedTime/>
   <IsInline/>
   <IsContactPhoto/>
   <Content/>
</FileAttachment>
```

 <span data-ttu-id="e428d-105">**FileAttachmentType**</span><span class="sxs-lookup"><span data-stu-id="e428d-105">**FileAttachmentType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e428d-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="e428d-106">Attributes and elements</span></span>

<span data-ttu-id="e428d-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="e428d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e428d-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="e428d-108">Attributes</span></span>

<span data-ttu-id="e428d-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="e428d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e428d-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="e428d-110">Child elements</span></span>

|<span data-ttu-id="e428d-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="e428d-111">**Element**</span></span>|<span data-ttu-id="e428d-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e428d-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e428d-113">AttachmentId</span><span class="sxs-lookup"><span data-stu-id="e428d-113">AttachmentId</span></span>](attachmentid.md) <br/> |<span data-ttu-id="e428d-114">Identifica el archivo adjunto.</span><span class="sxs-lookup"><span data-stu-id="e428d-114">Identifies the file attachment.</span></span>  <br/> |
|[<span data-ttu-id="e428d-115">Nombre (AttachmentType)</span><span class="sxs-lookup"><span data-stu-id="e428d-115">Name (AttachmentType)</span></span>](name-attachmenttype.md) <br/> |<span data-ttu-id="e428d-116">Representa el nombre de los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="e428d-116">Represents the name of the attachment.</span></span>  <br/> |
|[<span data-ttu-id="e428d-117">ContentType</span><span class="sxs-lookup"><span data-stu-id="e428d-117">ContentType</span></span>](contenttype.md) <br/> |<span data-ttu-id="e428d-118">Describe el tipo de extensiones multipropósito de correo Internet (MIME) del contenido de los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="e428d-118">Describes the Multipurpose Internet Mail Extensions (MIME) type of the attachment content.</span></span>  <br/> |
|[<span data-ttu-id="e428d-119">ContentId</span><span class="sxs-lookup"><span data-stu-id="e428d-119">ContentId</span></span>](contentid.md) <br/> |<span data-ttu-id="e428d-120">Representa un identificador para el contenido de los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="e428d-120">Represents an identifier for the contents of an attachment.</span></span> <span data-ttu-id="e428d-121">[ContentId](contentid.md) se puede establecer en cualquier valor de cadena.</span><span class="sxs-lookup"><span data-stu-id="e428d-121">[ContentId](contentid.md) can be set to any string value.</span></span> <span data-ttu-id="e428d-122">Las aplicaciones pueden usar [ContentId](contentid.md) para implementar sus propios mecanismos de identificación.</span><span class="sxs-lookup"><span data-stu-id="e428d-122">Applications can use [ContentId](contentid.md) to implement their own identification mechanisms.</span></span>  <br/> |
|[<span data-ttu-id="e428d-123">ContentLocation</span><span class="sxs-lookup"><span data-stu-id="e428d-123">ContentLocation</span></span>](contentlocation.md) <br/> |<span data-ttu-id="e428d-124">Contiene el identificador uniforme de recursos (URI) que corresponde a la ubicación del contenido de los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="e428d-124">Contains the Uniform Resource Identifier (URI) that corresponds to the location of the content of the attachment.</span></span>  <br/> |
|[<span data-ttu-id="e428d-125">Size</span><span class="sxs-lookup"><span data-stu-id="e428d-125">Size</span></span>](size.md) <br/> |<span data-ttu-id="e428d-126">Representa el tamaño en bytes del archivo adjunto.</span><span class="sxs-lookup"><span data-stu-id="e428d-126">Represents the size in bytes of the file attachment.</span></span>  <br/> |
|[<span data-ttu-id="e428d-127">LastModifiedTime</span><span class="sxs-lookup"><span data-stu-id="e428d-127">LastModifiedTime</span></span>](lastmodifiedtime.md) <br/> |<span data-ttu-id="e428d-128">Representa cuando se modificó por última vez el archivo adjunto.</span><span class="sxs-lookup"><span data-stu-id="e428d-128">Represents when the file attachment was last modified.</span></span>  <br/> |
|[<span data-ttu-id="e428d-129">IsInline</span><span class="sxs-lookup"><span data-stu-id="e428d-129">IsInline</span></span>](isinline.md) <br/> |<span data-ttu-id="e428d-130">Representa si el archivo adjunto aparece en línea dentro de un elemento.</span><span class="sxs-lookup"><span data-stu-id="e428d-130">Represents whether the attachment appears inline within an item.</span></span>  <br/> |
|[<span data-ttu-id="e428d-131">IsContactPhoto</span><span class="sxs-lookup"><span data-stu-id="e428d-131">IsContactPhoto</span></span>](iscontactphoto.md) <br/> |<span data-ttu-id="e428d-132">Indica si el archivo adjunto es una imagen del contacto.</span><span class="sxs-lookup"><span data-stu-id="e428d-132">Indicates whether the file attachment is a contact picture.</span></span>  <br/> |
|[<span data-ttu-id="e428d-133">Contenido</span><span class="sxs-lookup"><span data-stu-id="e428d-133">Content</span></span>](content.md) <br/> |<span data-ttu-id="e428d-134">Contiene el contenido con codificación Base64 de los datos adjuntos del archivo.</span><span class="sxs-lookup"><span data-stu-id="e428d-134">Contains the Base64-encoded contents of the file attachment.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="e428d-135">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="e428d-135">Parent elements</span></span>

|<span data-ttu-id="e428d-136">**Element**</span><span class="sxs-lookup"><span data-stu-id="e428d-136">**Element**</span></span>|<span data-ttu-id="e428d-137">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e428d-137">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e428d-138">Datos adjuntos</span><span class="sxs-lookup"><span data-stu-id="e428d-138">Attachments</span></span>](attachments-ex15websvcsotherref.md) <br/> |<span data-ttu-id="e428d-139">Contiene los elementos o archivos que se adjuntan a un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="e428d-139">Contains the items or files that are attached to an item in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="e428d-140">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="e428d-140">Text value</span></span>

<span data-ttu-id="e428d-141">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="e428d-141">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e428d-142">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e428d-142">Remarks</span></span>

<span data-ttu-id="e428d-143">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="e428d-143">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e428d-144">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="e428d-144">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e428d-145">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e428d-145">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="e428d-146">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="e428d-146">Schema name</span></span>  <br/> |<span data-ttu-id="e428d-147">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="e428d-147">Types schema</span></span>  <br/> |
|<span data-ttu-id="e428d-148">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="e428d-148">Validation file</span></span>  <br/> |<span data-ttu-id="e428d-149">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="e428d-149">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="e428d-150">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="e428d-150">Can be empty</span></span>  <br/> |<span data-ttu-id="e428d-151">False</span><span class="sxs-lookup"><span data-stu-id="e428d-151">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e428d-152">Vea también</span><span class="sxs-lookup"><span data-stu-id="e428d-152">See also</span></span>



- [<span data-ttu-id="e428d-153">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="e428d-153">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

