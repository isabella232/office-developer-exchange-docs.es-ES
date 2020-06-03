---
title: AttachmentShape
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AttachmentShape
api_type:
- schema
ms.assetid: 734914b5-3a16-4744-90a5-741fd30c4676
description: El elemento AttachmentShape identifica propiedades adicionales que se van a devolver en una respuesta a una solicitud GetAttachment.
ms.openlocfilehash: e70fbaad0f649c5afdc151b777efef0f8927ba1c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529668"
---
# <a name="attachmentshape"></a><span data-ttu-id="8e88b-103">AttachmentShape</span><span class="sxs-lookup"><span data-stu-id="8e88b-103">AttachmentShape</span></span>

<span data-ttu-id="8e88b-104">El elemento **AttachmentShape** identifica propiedades adicionales que se van a devolver en una respuesta a una solicitud [GetAttachment](getattachment.md) .</span><span class="sxs-lookup"><span data-stu-id="8e88b-104">The **AttachmentShape** element identifies additional properties to return in a response to a [GetAttachment](getattachment.md) request.</span></span> 
  
- [<span data-ttu-id="8e88b-105">GetAttachment</span><span class="sxs-lookup"><span data-stu-id="8e88b-105">GetAttachment</span></span>](getattachment.md)
  
- [<span data-ttu-id="8e88b-106">AttachmentShape</span><span class="sxs-lookup"><span data-stu-id="8e88b-106">AttachmentShape</span></span>](attachmentshape.md)
  
```xml
<AttachmentShape>
   <IncludeMimeContent/>
   <BodyType/>
   <FilterHtmlContent/>
   <AdditionalProperties/>
</AttachmentShape>
```

 <span data-ttu-id="8e88b-107">**AttachmentResponseShapeType**</span><span class="sxs-lookup"><span data-stu-id="8e88b-107">**AttachmentResponseShapeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="8e88b-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="8e88b-108">Attributes and elements</span></span>

<span data-ttu-id="8e88b-109">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="8e88b-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8e88b-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="8e88b-110">Attributes</span></span>

<span data-ttu-id="8e88b-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="8e88b-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="8e88b-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="8e88b-112">Child elements</span></span>

|<span data-ttu-id="8e88b-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="8e88b-113">**Element**</span></span>|<span data-ttu-id="8e88b-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8e88b-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8e88b-115">IncludeMimeContent</span><span class="sxs-lookup"><span data-stu-id="8e88b-115">IncludeMimeContent</span></span>](includemimecontent.md) <br/> |<span data-ttu-id="8e88b-116">Especifica si se devuelve el contenido de extensiones multipropósito de correo Internet (MIME) de un elemento o datos adjuntos en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8e88b-116">Specifies whether the Multipurpose Internet Mail Extensions (MIME) content of an item or attachment is returned in the response.</span></span> <span data-ttu-id="8e88b-117">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="8e88b-117">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="8e88b-118">BodyType</span><span class="sxs-lookup"><span data-stu-id="8e88b-118">BodyType</span></span>](bodytype.md) <br/> |<span data-ttu-id="8e88b-119">Identifica cómo se aplica formato al texto del cuerpo en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8e88b-119">Identifies how the body text is formatted in the response.</span></span> <span data-ttu-id="8e88b-120">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="8e88b-120">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="8e88b-121">FilterHtmlContent</span><span class="sxs-lookup"><span data-stu-id="8e88b-121">FilterHtmlContent</span></span>](filterhtmlcontent.md) <br/> |<span data-ttu-id="8e88b-122">Especifica si se filtra contenido HTML potencialmente no seguro de datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="8e88b-122">Specifies whether potentially unsafe HTML content is filtered from an attachment.</span></span> <span data-ttu-id="8e88b-123">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="8e88b-123">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="8e88b-124">AdditionalProperties</span><span class="sxs-lookup"><span data-stu-id="8e88b-124">AdditionalProperties</span></span>](additionalproperties.md) <br/> |<span data-ttu-id="8e88b-125">Identifica las propiedades adicionales que se devolverán en una respuesta.</span><span class="sxs-lookup"><span data-stu-id="8e88b-125">Identifies additional properties to return in a response.</span></span> <span data-ttu-id="8e88b-126">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="8e88b-126">This element is optional.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="8e88b-127">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="8e88b-127">Parent elements</span></span>

|<span data-ttu-id="8e88b-128">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="8e88b-128">**Element**</span></span>|<span data-ttu-id="8e88b-129">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8e88b-129">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8e88b-130">GetAttachment</span><span class="sxs-lookup"><span data-stu-id="8e88b-130">GetAttachment</span></span>](getattachment.md) <br/> |<span data-ttu-id="8e88b-131">Elemento que define una solicitud para obtener datos adjuntos de un buzón de correo en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="8e88b-131">The element that defines a request to get an attachment from a mailbox in the Exchange store.</span></span>  <br/> <span data-ttu-id="8e88b-132">La siguiente es la expresión XPath a este elemento:</span><span class="sxs-lookup"><span data-stu-id="8e88b-132">The following is the XPath expression to this element:</span></span>  <br/>  `/GetAttachment` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="8e88b-133">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="8e88b-133">Text value</span></span>

<span data-ttu-id="8e88b-134">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="8e88b-134">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8e88b-135">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8e88b-135">Remarks</span></span>

<span data-ttu-id="8e88b-136">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="8e88b-136">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8e88b-137">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="8e88b-137">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8e88b-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="8e88b-138">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="8e88b-139">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="8e88b-139">Schema Name</span></span>  <br/> |<span data-ttu-id="8e88b-140">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="8e88b-140">Messages schema</span></span>  <br/> |
|<span data-ttu-id="8e88b-141">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="8e88b-141">Validation File</span></span>  <br/> |<span data-ttu-id="8e88b-142">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="8e88b-142">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="8e88b-143">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="8e88b-143">Can be Empty</span></span>  <br/> |<span data-ttu-id="8e88b-144">Falso</span><span class="sxs-lookup"><span data-stu-id="8e88b-144">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8e88b-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="8e88b-145">See also</span></span>

- [<span data-ttu-id="8e88b-146">Operación GetAttachment</span><span class="sxs-lookup"><span data-stu-id="8e88b-146">GetAttachment operation</span></span>](getattachment-operation.md)
- [<span data-ttu-id="8e88b-147">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="8e88b-147">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

