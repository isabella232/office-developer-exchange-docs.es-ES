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
description: El elemento RootItemId identifica el elemento raíz de los datos adjuntos eliminados.
ms.openlocfilehash: d8badd465fd5a93e1a6354d55ac5c4b080897152
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457098"
---
# <a name="rootitemid"></a><span data-ttu-id="b0360-103">RootItemId</span><span class="sxs-lookup"><span data-stu-id="b0360-103">RootItemId</span></span>

<span data-ttu-id="b0360-104">El elemento **RootItemId** identifica el elemento raíz de los datos adjuntos eliminados.</span><span class="sxs-lookup"><span data-stu-id="b0360-104">The **RootItemId** element identifies the root item of a deleted attachment.</span></span> 
  
[<span data-ttu-id="b0360-105">DeleteAttachmentResponse</span><span class="sxs-lookup"><span data-stu-id="b0360-105">DeleteAttachmentResponse</span></span>](deleteattachmentresponse.md)
  
[<span data-ttu-id="b0360-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="b0360-106">ResponseMessages</span></span>](responsemessages.md)
  
[<span data-ttu-id="b0360-107">DeleteAttachmentResponseMessage</span><span class="sxs-lookup"><span data-stu-id="b0360-107">DeleteAttachmentResponseMessage</span></span>](deleteattachmentresponsemessage.md)
  
[<span data-ttu-id="b0360-108">RootItemId</span><span class="sxs-lookup"><span data-stu-id="b0360-108">RootItemId</span></span>](rootitemid.md)
  
```xml
<RootItemId RootItemId="" RootItemChangeKey="" />
```

 <span data-ttu-id="b0360-109">**RootItemIdType**</span><span class="sxs-lookup"><span data-stu-id="b0360-109">**RootItemIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b0360-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="b0360-110">Attributes and elements</span></span>

<span data-ttu-id="b0360-111">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="b0360-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b0360-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="b0360-112">Attributes</span></span>

|<span data-ttu-id="b0360-113">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="b0360-113">**Attribute**</span></span>|<span data-ttu-id="b0360-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b0360-114">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b0360-115">**RootItemId**</span><span class="sxs-lookup"><span data-stu-id="b0360-115">**RootItemId**</span></span> <br/> |<span data-ttu-id="b0360-116">Identifica el elemento raíz de un dato adjunto eliminado.</span><span class="sxs-lookup"><span data-stu-id="b0360-116">Identifies the root item of a deleted attachment.</span></span>  <br/> |
|<span data-ttu-id="b0360-117">**RootItemChangeKey**</span><span class="sxs-lookup"><span data-stu-id="b0360-117">**RootItemChangeKey**</span></span> <br/> |<span data-ttu-id="b0360-118">Identifica la nueva clave de cambio del elemento raíz de un archivo adjunto eliminado.</span><span class="sxs-lookup"><span data-stu-id="b0360-118">Identifies the new change key of the root item of a deleted attachment.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="b0360-119">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b0360-119">Child elements</span></span>

<span data-ttu-id="b0360-120">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="b0360-120">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="b0360-121">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="b0360-121">Parent elements</span></span>

|<span data-ttu-id="b0360-122">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="b0360-122">**Element**</span></span>|<span data-ttu-id="b0360-123">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b0360-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b0360-124">DeleteAttachmentResponseMessage</span><span class="sxs-lookup"><span data-stu-id="b0360-124">DeleteAttachmentResponseMessage</span></span>](deleteattachmentresponsemessage.md) <br/> |<span data-ttu-id="b0360-125">Contiene el estado y el resultado de una solicitud DeleteAttachment.</span><span class="sxs-lookup"><span data-stu-id="b0360-125">Contains the status and result of a DeleteAttachment request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b0360-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b0360-126">Remarks</span></span>

<span data-ttu-id="b0360-127">El elemento **RootItemId** solo se usa en respuestas DeleteAttachment.</span><span class="sxs-lookup"><span data-stu-id="b0360-127">The **RootItemId** element is only used in DeleteAttachment responses.</span></span> <span data-ttu-id="b0360-128">Esto identifica el identificador del elemento raíz y, lo que es más importante, la nueva clave de cambio para el elemento primario.</span><span class="sxs-lookup"><span data-stu-id="b0360-128">This identifies the root item identifier, and more importantly, the new change key to the parent item.</span></span> 
  
<span data-ttu-id="b0360-129">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="b0360-129">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b0360-130">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="b0360-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b0360-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="b0360-131">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="b0360-132">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="b0360-132">Schema name</span></span>  <br/> |<span data-ttu-id="b0360-133">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="b0360-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="b0360-134">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="b0360-134">Validation file</span></span>  <br/> |<span data-ttu-id="b0360-135">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="b0360-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="b0360-136">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="b0360-136">Can be empty</span></span>  <br/> |<span data-ttu-id="b0360-137">Falso</span><span class="sxs-lookup"><span data-stu-id="b0360-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b0360-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="b0360-138">See also</span></span>



[<span data-ttu-id="b0360-139">DeleteAttachment</span><span class="sxs-lookup"><span data-stu-id="b0360-139">DeleteAttachment</span></span>](deleteattachment.md)
  
[<span data-ttu-id="b0360-140">Operación DeleteAttachment</span><span class="sxs-lookup"><span data-stu-id="b0360-140">DeleteAttachment operation</span></span>](deleteattachment-operation.md)


- [<span data-ttu-id="b0360-141">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="b0360-141">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

