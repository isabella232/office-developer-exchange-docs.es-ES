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
description: El elemento FileAttachment representa un archivo que está adjunto a un elemento en el almacén de Exchange.
ms.openlocfilehash: db9b541fb2527ae3c09cbdb33bedea7fb215bd30
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461019"
---
# <a name="fileattachment"></a><span data-ttu-id="5a869-103">FileAttachment</span><span class="sxs-lookup"><span data-stu-id="5a869-103">FileAttachment</span></span>

<span data-ttu-id="5a869-104">El elemento **FileAttachment** representa un archivo que está adjunto a un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="5a869-104">The **FileAttachment** element represents a file that is attached to an item in the Exchange store.</span></span> 
  
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

 <span data-ttu-id="5a869-105">**FileAttachmentType**</span><span class="sxs-lookup"><span data-stu-id="5a869-105">**FileAttachmentType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="5a869-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="5a869-106">Attributes and elements</span></span>

<span data-ttu-id="5a869-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="5a869-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5a869-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="5a869-108">Attributes</span></span>

<span data-ttu-id="5a869-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="5a869-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5a869-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="5a869-110">Child elements</span></span>

|<span data-ttu-id="5a869-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="5a869-111">**Element**</span></span>|<span data-ttu-id="5a869-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5a869-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5a869-113">AttachmentId</span><span class="sxs-lookup"><span data-stu-id="5a869-113">AttachmentId</span></span>](attachmentid.md) <br/> |<span data-ttu-id="5a869-114">Identifica los datos adjuntos del archivo.</span><span class="sxs-lookup"><span data-stu-id="5a869-114">Identifies the file attachment.</span></span>  <br/> |
|[<span data-ttu-id="5a869-115">Nombre (AttachmentType)</span><span class="sxs-lookup"><span data-stu-id="5a869-115">Name (AttachmentType)</span></span>](name-attachmenttype.md) <br/> |<span data-ttu-id="5a869-116">Representa el nombre de los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="5a869-116">Represents the name of the attachment.</span></span>  <br/> |
|[<span data-ttu-id="5a869-117">ContentType</span><span class="sxs-lookup"><span data-stu-id="5a869-117">ContentType</span></span>](contenttype.md) <br/> |<span data-ttu-id="5a869-118">Describe el tipo de extensiones multipropósito de correo Internet (MIME) del contenido de datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="5a869-118">Describes the Multipurpose Internet Mail Extensions (MIME) type of the attachment content.</span></span>  <br/> |
|[<span data-ttu-id="5a869-119">ContentId</span><span class="sxs-lookup"><span data-stu-id="5a869-119">ContentId</span></span>](contentid.md) <br/> |<span data-ttu-id="5a869-120">Representa un identificador para el contenido de un dato adjunto.</span><span class="sxs-lookup"><span data-stu-id="5a869-120">Represents an identifier for the contents of an attachment.</span></span> <span data-ttu-id="5a869-121">[Contentid](contentid.md) se puede establecer en cualquier valor de cadena.</span><span class="sxs-lookup"><span data-stu-id="5a869-121">[ContentId](contentid.md) can be set to any string value.</span></span> <span data-ttu-id="5a869-122">Las aplicaciones pueden usar [contentid](contentid.md) para implementar sus propios mecanismos de identificación.</span><span class="sxs-lookup"><span data-stu-id="5a869-122">Applications can use [ContentId](contentid.md) to implement their own identification mechanisms.</span></span>  <br/> |
|[<span data-ttu-id="5a869-123">ContentLocation</span><span class="sxs-lookup"><span data-stu-id="5a869-123">ContentLocation</span></span>](contentlocation.md) <br/> |<span data-ttu-id="5a869-124">Contiene el identificador uniforme de recursos (URI) que corresponde a la ubicación del contenido de los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="5a869-124">Contains the Uniform Resource Identifier (URI) that corresponds to the location of the content of the attachment.</span></span>  <br/> |
|[<span data-ttu-id="5a869-125">Tamaño</span><span class="sxs-lookup"><span data-stu-id="5a869-125">Size</span></span>](size.md) <br/> |<span data-ttu-id="5a869-126">Representa el tamaño en bytes de los datos adjuntos del archivo.</span><span class="sxs-lookup"><span data-stu-id="5a869-126">Represents the size in bytes of the file attachment.</span></span>  <br/> |
|[<span data-ttu-id="5a869-127">LastModifiedTime</span><span class="sxs-lookup"><span data-stu-id="5a869-127">LastModifiedTime</span></span>](lastmodifiedtime.md) <br/> |<span data-ttu-id="5a869-128">Representa el momento en que se modificó por última vez el archivo adjunto.</span><span class="sxs-lookup"><span data-stu-id="5a869-128">Represents when the file attachment was last modified.</span></span>  <br/> |
|[<span data-ttu-id="5a869-129">IsInline</span><span class="sxs-lookup"><span data-stu-id="5a869-129">IsInline</span></span>](isinline.md) <br/> |<span data-ttu-id="5a869-130">Indica si los datos adjuntos aparecen en línea dentro de un elemento.</span><span class="sxs-lookup"><span data-stu-id="5a869-130">Represents whether the attachment appears inline within an item.</span></span>  <br/> |
|[<span data-ttu-id="5a869-131">IsContactPhoto</span><span class="sxs-lookup"><span data-stu-id="5a869-131">IsContactPhoto</span></span>](iscontactphoto.md) <br/> |<span data-ttu-id="5a869-132">Indica si el archivo adjunto es una imagen de contacto.</span><span class="sxs-lookup"><span data-stu-id="5a869-132">Indicates whether the file attachment is a contact picture.</span></span>  <br/> |
|[<span data-ttu-id="5a869-133">Content</span><span class="sxs-lookup"><span data-stu-id="5a869-133">Content</span></span>](content.md) <br/> |<span data-ttu-id="5a869-134">Contiene el contenido codificado en base64 del archivo de datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="5a869-134">Contains the Base64-encoded contents of the file attachment.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="5a869-135">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="5a869-135">Parent elements</span></span>

|<span data-ttu-id="5a869-136">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="5a869-136">**Element**</span></span>|<span data-ttu-id="5a869-137">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5a869-137">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5a869-138">Datos adjuntos</span><span class="sxs-lookup"><span data-stu-id="5a869-138">Attachments</span></span>](attachments-ex15websvcsotherref.md) <br/> |<span data-ttu-id="5a869-139">Contiene los elementos o archivos adjuntos a un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="5a869-139">Contains the items or files that are attached to an item in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="5a869-140">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="5a869-140">Text value</span></span>

<span data-ttu-id="5a869-141">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="5a869-141">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5a869-142">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5a869-142">Remarks</span></span>

<span data-ttu-id="5a869-143">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="5a869-143">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5a869-144">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="5a869-144">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5a869-145">Namespace</span><span class="sxs-lookup"><span data-stu-id="5a869-145">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="5a869-146">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="5a869-146">Schema name</span></span>  <br/> |<span data-ttu-id="5a869-147">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="5a869-147">Types schema</span></span>  <br/> |
|<span data-ttu-id="5a869-148">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="5a869-148">Validation file</span></span>  <br/> |<span data-ttu-id="5a869-149">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="5a869-149">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="5a869-150">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="5a869-150">Can be empty</span></span>  <br/> |<span data-ttu-id="5a869-151">Falso</span><span class="sxs-lookup"><span data-stu-id="5a869-151">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5a869-152">Vea también</span><span class="sxs-lookup"><span data-stu-id="5a869-152">See also</span></span>



- [<span data-ttu-id="5a869-153">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="5a869-153">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

