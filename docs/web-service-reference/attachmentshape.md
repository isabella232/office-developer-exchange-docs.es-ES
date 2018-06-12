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
description: El elemento AttachmentShape identifica propiedades adicionales para devolver en una respuesta a una solicitud de GetAttachment.
ms.openlocfilehash: dc6769faa5fd28ce31b796f86c507aec54abff7a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763571"
---
# <a name="attachmentshape"></a><span data-ttu-id="19ea9-103">AttachmentShape</span><span class="sxs-lookup"><span data-stu-id="19ea9-103">AttachmentShape</span></span>

<span data-ttu-id="19ea9-104">El elemento **AttachmentShape** identifica propiedades adicionales para devolver en una respuesta a una solicitud de [GetAttachment](getattachment.md) .</span><span class="sxs-lookup"><span data-stu-id="19ea9-104">The **AttachmentShape** element identifies additional properties to return in a response to a [GetAttachment](getattachment.md) request.</span></span> 
  
- [<span data-ttu-id="19ea9-105">GetAttachment</span><span class="sxs-lookup"><span data-stu-id="19ea9-105">GetAttachment</span></span>](getattachment.md)
  
- [<span data-ttu-id="19ea9-106">AttachmentShape</span><span class="sxs-lookup"><span data-stu-id="19ea9-106">AttachmentShape</span></span>](attachmentshape.md)
  
```xml
<AttachmentShape>
   <IncludeMimeContent/>
   <BodyType/>
   <FilterHtmlContent/>
   <AdditionalProperties/>
</AttachmentShape>
```

 <span data-ttu-id="19ea9-107">**AttachmentResponseShapeType**</span><span class="sxs-lookup"><span data-stu-id="19ea9-107">**AttachmentResponseShapeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="19ea9-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="19ea9-108">Attributes and elements</span></span>

<span data-ttu-id="19ea9-109">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="19ea9-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="19ea9-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="19ea9-110">Attributes</span></span>

<span data-ttu-id="19ea9-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="19ea9-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="19ea9-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="19ea9-112">Child elements</span></span>

|<span data-ttu-id="19ea9-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="19ea9-113">**Element**</span></span>|<span data-ttu-id="19ea9-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="19ea9-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="19ea9-115">IncludeMimeContent</span><span class="sxs-lookup"><span data-stu-id="19ea9-115">IncludeMimeContent</span></span>](includemimecontent.md) <br/> |<span data-ttu-id="19ea9-116">Especifica si el contenido de extensiones multipropósito de correo Internet (MIME) de un elemento o datos adjuntos se devuelve en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="19ea9-116">Specifies whether the Multipurpose Internet Mail Extensions (MIME) content of an item or attachment is returned in the response.</span></span> <span data-ttu-id="19ea9-117">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="19ea9-117">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="19ea9-118">BodyType</span><span class="sxs-lookup"><span data-stu-id="19ea9-118">BodyType</span></span>](bodytype.md) <br/> |<span data-ttu-id="19ea9-119">Identifica cómo se da el formato de texto del cuerpo en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="19ea9-119">Identifies how the body text is formatted in the response.</span></span> <span data-ttu-id="19ea9-120">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="19ea9-120">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="19ea9-121">FilterHtmlContent</span><span class="sxs-lookup"><span data-stu-id="19ea9-121">FilterHtmlContent</span></span>](filterhtmlcontent.md) <br/> |<span data-ttu-id="19ea9-122">Especifica si el contenido HTML potencialmente no segura se filtra desde un archivo adjunto.</span><span class="sxs-lookup"><span data-stu-id="19ea9-122">Specifies whether potentially unsafe HTML content is filtered from an attachment.</span></span> <span data-ttu-id="19ea9-123">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="19ea9-123">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="19ea9-124">AdditionalProperties</span><span class="sxs-lookup"><span data-stu-id="19ea9-124">AdditionalProperties</span></span>](additionalproperties.md) <br/> |<span data-ttu-id="19ea9-125">Identifica las propiedades adicionales para devolver en una respuesta.</span><span class="sxs-lookup"><span data-stu-id="19ea9-125">Identifies additional properties to return in a response.</span></span> <span data-ttu-id="19ea9-126">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="19ea9-126">This element is optional.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="19ea9-127">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="19ea9-127">Parent elements</span></span>

|<span data-ttu-id="19ea9-128">**Element**</span><span class="sxs-lookup"><span data-stu-id="19ea9-128">**Element**</span></span>|<span data-ttu-id="19ea9-129">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="19ea9-129">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="19ea9-130">GetAttachment</span><span class="sxs-lookup"><span data-stu-id="19ea9-130">GetAttachment</span></span>](getattachment.md) <br/> |<span data-ttu-id="19ea9-131">El elemento que define una solicitud para obtener datos adjuntos de un buzón en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="19ea9-131">The element that defines a request to get an attachment from a mailbox in the Exchange store.</span></span>  <br/> <span data-ttu-id="19ea9-132">La siguiente es la expresión de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="19ea9-132">The following is the XPath expression to this element:</span></span>  <br/>  `/GetAttachment` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="19ea9-133">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="19ea9-133">Text value</span></span>

<span data-ttu-id="19ea9-134">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="19ea9-134">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="19ea9-135">Observaciones</span><span class="sxs-lookup"><span data-stu-id="19ea9-135">Remarks</span></span>

<span data-ttu-id="19ea9-136">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="19ea9-136">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="19ea9-137">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="19ea9-137">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="19ea9-138">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="19ea9-138">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="19ea9-139">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="19ea9-139">Schema Name</span></span>  <br/> |<span data-ttu-id="19ea9-140">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="19ea9-140">Messages schema</span></span>  <br/> |
|<span data-ttu-id="19ea9-141">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="19ea9-141">Validation File</span></span>  <br/> |<span data-ttu-id="19ea9-142">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="19ea9-142">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="19ea9-143">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="19ea9-143">Can be Empty</span></span>  <br/> |<span data-ttu-id="19ea9-144">False</span><span class="sxs-lookup"><span data-stu-id="19ea9-144">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="19ea9-145">Ver también</span><span class="sxs-lookup"><span data-stu-id="19ea9-145">See also</span></span>

- [<span data-ttu-id="19ea9-146">Operación GetAttachment</span><span class="sxs-lookup"><span data-stu-id="19ea9-146">GetAttachment operation</span></span>](getattachment-operation.md)
- [<span data-ttu-id="19ea9-147">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="19ea9-147">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

