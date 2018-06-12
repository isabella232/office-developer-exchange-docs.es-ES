---
title: RootItemId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RootItemId
api_type:
- schema
ms.assetid: f613c705-17ce-48ce-aa64-4dc2cea25e31
description: El elemento RootItemId identifica el elemento raíz de un archivo adjunto eliminado.
ms.openlocfilehash: 484b185db63c9692eaca7e43c49d6e95375a1a98
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19837251"
---
# <a name="rootitemid"></a><span data-ttu-id="7ca4f-103">RootItemId</span><span class="sxs-lookup"><span data-stu-id="7ca4f-103">RootItemId</span></span>

<span data-ttu-id="7ca4f-104">El elemento **RootItemId** identifica el elemento raíz de un archivo adjunto eliminado.</span><span class="sxs-lookup"><span data-stu-id="7ca4f-104">The **RootItemId** element identifies the root item of a deleted attachment.</span></span> 
  
[<span data-ttu-id="7ca4f-105">DeleteAttachmentResponse</span><span class="sxs-lookup"><span data-stu-id="7ca4f-105">DeleteAttachmentResponse</span></span>](deleteattachmentresponse.md)
  
[<span data-ttu-id="7ca4f-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="7ca4f-106">ResponseMessages</span></span>](responsemessages.md)
  
[<span data-ttu-id="7ca4f-107">DeleteAttachmentResponseMessage</span><span class="sxs-lookup"><span data-stu-id="7ca4f-107">DeleteAttachmentResponseMessage</span></span>](deleteattachmentresponsemessage.md)
  
[<span data-ttu-id="7ca4f-108">RootItemId</span><span class="sxs-lookup"><span data-stu-id="7ca4f-108">RootItemId</span></span>](rootitemid.md)
  
```xml
<RootItemId RootItemId="" RootItemChangeKey="" />
```

 <span data-ttu-id="7ca4f-109">**RootItemIdType**</span><span class="sxs-lookup"><span data-stu-id="7ca4f-109">**RootItemIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7ca4f-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="7ca4f-110">Attributes and elements</span></span>

<span data-ttu-id="7ca4f-111">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="7ca4f-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7ca4f-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="7ca4f-112">Attributes</span></span>

|<span data-ttu-id="7ca4f-113">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="7ca4f-113">**Attribute**</span></span>|<span data-ttu-id="7ca4f-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7ca4f-114">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7ca4f-115">**RootItemId**</span><span class="sxs-lookup"><span data-stu-id="7ca4f-115">**RootItemId**</span></span> <br/> |<span data-ttu-id="7ca4f-116">Identifica el elemento raíz de un archivo adjunto eliminado.</span><span class="sxs-lookup"><span data-stu-id="7ca4f-116">Identifies the root item of a deleted attachment.</span></span>  <br/> |
|<span data-ttu-id="7ca4f-117">**RootItemChangeKey**</span><span class="sxs-lookup"><span data-stu-id="7ca4f-117">**RootItemChangeKey**</span></span> <br/> |<span data-ttu-id="7ca4f-118">Identifica la nueva clave de cambio del elemento raíz de un archivo adjunto eliminado.</span><span class="sxs-lookup"><span data-stu-id="7ca4f-118">Identifies the new change key of the root item of a deleted attachment.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="7ca4f-119">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="7ca4f-119">Child elements</span></span>

<span data-ttu-id="7ca4f-120">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="7ca4f-120">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="7ca4f-121">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="7ca4f-121">Parent elements</span></span>

|<span data-ttu-id="7ca4f-122">**Element**</span><span class="sxs-lookup"><span data-stu-id="7ca4f-122">**Element**</span></span>|<span data-ttu-id="7ca4f-123">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7ca4f-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7ca4f-124">DeleteAttachmentResponseMessage</span><span class="sxs-lookup"><span data-stu-id="7ca4f-124">DeleteAttachmentResponseMessage</span></span>](deleteattachmentresponsemessage.md) <br/> |<span data-ttu-id="7ca4f-125">Contiene el estado y el resultado de una solicitud de DeleteAttachment.</span><span class="sxs-lookup"><span data-stu-id="7ca4f-125">Contains the status and result of a DeleteAttachment request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7ca4f-126">Notas</span><span class="sxs-lookup"><span data-stu-id="7ca4f-126">Remarks</span></span>

<span data-ttu-id="7ca4f-127">El elemento **RootItemId** solo se usa en las respuestas DeleteAttachment.</span><span class="sxs-lookup"><span data-stu-id="7ca4f-127">The **RootItemId** element is only used in DeleteAttachment responses.</span></span> <span data-ttu-id="7ca4f-128">Esto identifica el identificador del elemento raíz y lo que es más importante, la nueva clave de cambio para el elemento primario.</span><span class="sxs-lookup"><span data-stu-id="7ca4f-128">This identifies the root item identifier, and more importantly, the new change key to the parent item.</span></span> 
  
<span data-ttu-id="7ca4f-129">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="7ca4f-129">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7ca4f-130">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="7ca4f-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7ca4f-131">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="7ca4f-131">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="7ca4f-132">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="7ca4f-132">Schema name</span></span>  <br/> |<span data-ttu-id="7ca4f-133">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="7ca4f-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="7ca4f-134">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="7ca4f-134">Validation file</span></span>  <br/> |<span data-ttu-id="7ca4f-135">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="7ca4f-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="7ca4f-136">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="7ca4f-136">Can be empty</span></span>  <br/> |<span data-ttu-id="7ca4f-137">False</span><span class="sxs-lookup"><span data-stu-id="7ca4f-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7ca4f-138">Ver también</span><span class="sxs-lookup"><span data-stu-id="7ca4f-138">See also</span></span>



[<span data-ttu-id="7ca4f-139">DeleteAttachment</span><span class="sxs-lookup"><span data-stu-id="7ca4f-139">DeleteAttachment</span></span>](deleteattachment.md)
  
[<span data-ttu-id="7ca4f-140">Operación DeleteAttachment</span><span class="sxs-lookup"><span data-stu-id="7ca4f-140">DeleteAttachment operation</span></span>](deleteattachment-operation.md)


- [<span data-ttu-id="7ca4f-141">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="7ca4f-141">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

