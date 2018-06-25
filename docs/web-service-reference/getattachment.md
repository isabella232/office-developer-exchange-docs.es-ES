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
description: El elemento de GetAttachment es el elemento raíz en una solicitud para obtener datos adjuntos desde el almacén de Exchange.
ms.openlocfilehash: fb639c86a0654e8f9e9601310f7c2f5b0fc7d729
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764756"
---
# <a name="getattachment"></a><span data-ttu-id="1aa04-103">GetAttachment</span><span class="sxs-lookup"><span data-stu-id="1aa04-103">GetAttachment</span></span>

<span data-ttu-id="1aa04-104">El elemento de **GetAttachment** es el elemento raíz en una solicitud para obtener datos adjuntos desde el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="1aa04-104">The **GetAttachment** element is the root element in a request to get an attachment from the Exchange store.</span></span> 
  
```xml
<GetAttachment>
   <AttachmentShape/>
   <AttachmentIds/>
</GetAttachment>
```

 <span data-ttu-id="1aa04-105">**GetAttachmentType**</span><span class="sxs-lookup"><span data-stu-id="1aa04-105">**GetAttachmentType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1aa04-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="1aa04-106">Attributes and elements</span></span>

<span data-ttu-id="1aa04-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="1aa04-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1aa04-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="1aa04-108">Attributes</span></span>

<span data-ttu-id="1aa04-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="1aa04-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1aa04-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="1aa04-110">Child elements</span></span>

|<span data-ttu-id="1aa04-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="1aa04-111">**Element**</span></span>|<span data-ttu-id="1aa04-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1aa04-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1aa04-113">AttachmentShape</span><span class="sxs-lookup"><span data-stu-id="1aa04-113">AttachmentShape</span></span>](attachmentshape.md) <br/> |<span data-ttu-id="1aa04-114">Identifica las propiedades de elemento extendido adicional para devolver en una respuesta a una solicitud de [GetAttachment](getattachment.md) .</span><span class="sxs-lookup"><span data-stu-id="1aa04-114">Identifies additional extended item properties to return in a response to a [GetAttachment](getattachment.md) request.</span></span> <span data-ttu-id="1aa04-115">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="1aa04-115">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="1aa04-116">AttachmentIds</span><span class="sxs-lookup"><span data-stu-id="1aa04-116">AttachmentIds</span></span>](attachmentids.md) <br/> |<span data-ttu-id="1aa04-117">Contiene una matriz de identificadores de los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="1aa04-117">Contains an array of attachment identifiers.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="1aa04-118">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="1aa04-118">Parent elements</span></span>

<span data-ttu-id="1aa04-119">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="1aa04-119">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1aa04-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1aa04-120">Remarks</span></span>

<span data-ttu-id="1aa04-121">El elemento [AttachmentShape](attachmentshape.md) no es necesario para identificar las propiedades devueltas en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1aa04-121">The [AttachmentShape](attachmentshape.md) element is not required to identify the properties returned in the response.</span></span> <span data-ttu-id="1aa04-122">La [operación GetAttachment](getattachment-operation.md) devuelve el nombre, ContentType, ContentId, ContentLocation y las propiedades de contenido para datos adjuntos de archivo.</span><span class="sxs-lookup"><span data-stu-id="1aa04-122">The [GetAttachment operation](getattachment-operation.md) returns the Name, ContentType, ContentId, ContentLocation, and the Content properties for file attachments.</span></span> <span data-ttu-id="1aa04-123">Los datos adjuntos de elemento, las propiedades devueltas son el nombre, ContentType, ContentId, ContentLocation y las propiedades de todos los adjuntos del elemento.</span><span class="sxs-lookup"><span data-stu-id="1aa04-123">For item attachments, the returned properties are the Name, ContentType, ContentId, ContentLocation, and all the attached item's properties.</span></span> <span data-ttu-id="1aa04-124">Esto es equivalente al uso de la forma base AllProperties en una solicitud [GetItem](getitem.md) .</span><span class="sxs-lookup"><span data-stu-id="1aa04-124">This is equivalent to using the AllProperties base shape in a [GetItem](getitem.md) request.</span></span> 
  
<span data-ttu-id="1aa04-125">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="1aa04-125">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1aa04-126">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="1aa04-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1aa04-127">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="1aa04-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="1aa04-128">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="1aa04-128">Schema Name</span></span>  <br/> |<span data-ttu-id="1aa04-129">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="1aa04-129">Messages schema</span></span>  <br/> |
|<span data-ttu-id="1aa04-130">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="1aa04-130">Validation File</span></span>  <br/> |<span data-ttu-id="1aa04-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="1aa04-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="1aa04-132">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="1aa04-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="1aa04-133">False</span><span class="sxs-lookup"><span data-stu-id="1aa04-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1aa04-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="1aa04-134">See also</span></span>



[<span data-ttu-id="1aa04-135">Operación GetAttachment</span><span class="sxs-lookup"><span data-stu-id="1aa04-135">GetAttachment operation</span></span>](getattachment-operation.md)
  
[<span data-ttu-id="1aa04-136">GetAttachmentResponse</span><span class="sxs-lookup"><span data-stu-id="1aa04-136">GetAttachmentResponse</span></span>](getattachmentresponse.md)

