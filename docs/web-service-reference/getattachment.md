---
title: GetAttachment
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetAttachment
api_type:
- schema
ms.assetid: 9443cf96-b451-4530-b868-490dff798673
description: El elemento GetAttachment es el elemento raíz de una solicitud para obtener datos adjuntos del almacén de Exchange.
ms.openlocfilehash: d03d086ff443db87b0104a2ec83599eb9eaea6b9
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463982"
---
# <a name="getattachment"></a><span data-ttu-id="480be-103">GetAttachment</span><span class="sxs-lookup"><span data-stu-id="480be-103">GetAttachment</span></span>

<span data-ttu-id="480be-104">El elemento **GetAttachment** es el elemento raíz de una solicitud para obtener datos adjuntos del almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="480be-104">The **GetAttachment** element is the root element in a request to get an attachment from the Exchange store.</span></span> 
  
```xml
<GetAttachment>
   <AttachmentShape/>
   <AttachmentIds/>
</GetAttachment>
```

 <span data-ttu-id="480be-105">**GetAttachmentType**</span><span class="sxs-lookup"><span data-stu-id="480be-105">**GetAttachmentType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="480be-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="480be-106">Attributes and elements</span></span>

<span data-ttu-id="480be-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="480be-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="480be-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="480be-108">Attributes</span></span>

<span data-ttu-id="480be-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="480be-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="480be-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="480be-110">Child elements</span></span>

|<span data-ttu-id="480be-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="480be-111">**Element**</span></span>|<span data-ttu-id="480be-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="480be-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="480be-113">AttachmentShape</span><span class="sxs-lookup"><span data-stu-id="480be-113">AttachmentShape</span></span>](attachmentshape.md) <br/> |<span data-ttu-id="480be-114">Identifica las propiedades adicionales de elementos extendidos que se van a devolver en una respuesta a una solicitud [GetAttachment](getattachment.md) .</span><span class="sxs-lookup"><span data-stu-id="480be-114">Identifies additional extended item properties to return in a response to a [GetAttachment](getattachment.md) request.</span></span> <span data-ttu-id="480be-115">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="480be-115">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="480be-116">Identificadores</span><span class="sxs-lookup"><span data-stu-id="480be-116">AttachmentIds</span></span>](attachmentids.md) <br/> |<span data-ttu-id="480be-117">Contiene una matriz de identificadores de datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="480be-117">Contains an array of attachment identifiers.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="480be-118">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="480be-118">Parent elements</span></span>

<span data-ttu-id="480be-119">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="480be-119">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="480be-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="480be-120">Remarks</span></span>

<span data-ttu-id="480be-121">El elemento [AttachmentShape](attachmentshape.md) no es necesario para identificar las propiedades devueltas en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="480be-121">The [AttachmentShape](attachmentshape.md) element is not required to identify the properties returned in the response.</span></span> <span data-ttu-id="480be-122">La [operación GetAttachment](getattachment-operation.md) devuelve el nombre, ContentType, contentid, ContentLocation y las propiedades de contenido de los datos adjuntos de archivo.</span><span class="sxs-lookup"><span data-stu-id="480be-122">The [GetAttachment operation](getattachment-operation.md) returns the Name, ContentType, ContentId, ContentLocation, and the Content properties for file attachments.</span></span> <span data-ttu-id="480be-123">Para los datos adjuntos de elementos, las propiedades devueltas son el nombre, ContentType, ContentId, ContentLocation y todas las propiedades del elemento adjunto.</span><span class="sxs-lookup"><span data-stu-id="480be-123">For item attachments, the returned properties are the Name, ContentType, ContentId, ContentLocation, and all the attached item's properties.</span></span> <span data-ttu-id="480be-124">Esto equivale a usar la forma base AllProperties en una solicitud [GetItem](getitem.md) .</span><span class="sxs-lookup"><span data-stu-id="480be-124">This is equivalent to using the AllProperties base shape in a [GetItem](getitem.md) request.</span></span> 
  
<span data-ttu-id="480be-125">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="480be-125">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="480be-126">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="480be-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="480be-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="480be-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="480be-128">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="480be-128">Schema Name</span></span>  <br/> |<span data-ttu-id="480be-129">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="480be-129">Messages schema</span></span>  <br/> |
|<span data-ttu-id="480be-130">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="480be-130">Validation File</span></span>  <br/> |<span data-ttu-id="480be-131">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="480be-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="480be-132">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="480be-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="480be-133">Falso</span><span class="sxs-lookup"><span data-stu-id="480be-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="480be-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="480be-134">See also</span></span>



[<span data-ttu-id="480be-135">Operación GetAttachment</span><span class="sxs-lookup"><span data-stu-id="480be-135">GetAttachment operation</span></span>](getattachment-operation.md)
  
[<span data-ttu-id="480be-136">GetAttachmentResponse</span><span class="sxs-lookup"><span data-stu-id="480be-136">GetAttachmentResponse</span></span>](getattachmentresponse.md)

