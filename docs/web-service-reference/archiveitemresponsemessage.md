---
title: ArchiveItemResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2ac58d6f-e019-4352-b82f-8ac67a171e63
description: El elemento ArchiveItemResponseMessage especifica el mensaje de respuesta a una solicitud ArchiveItem.
ms.openlocfilehash: 24d09d63cab6805194e35031d8590290573de0a9
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463394"
---
# <a name="archiveitemresponsemessage"></a><span data-ttu-id="0aa98-103">ArchiveItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="0aa98-103">ArchiveItemResponseMessage</span></span>

<span data-ttu-id="0aa98-104">El elemento **ArchiveItemResponseMessage** especifica el mensaje de respuesta a una solicitud **ArchiveItem** .</span><span class="sxs-lookup"><span data-stu-id="0aa98-104">The **ArchiveItemResponseMessage** element specifies the response message to an **ArchiveItem** request.</span></span> 
  
```XML
<ArchiveItemResponseMessage ResponseClass="">
    <MessageText></MessageText>
    <ResponseCode></ResponseCode>
    <DescriptiveLinkKey></DescriptiveLinkKey>
    <MessageXml></MessageXml>
    <Items></Items>
</ArchiveItemResponseMessage>
```

 <span data-ttu-id="0aa98-105">**ItemInfoResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="0aa98-105">**ItemInfoResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0aa98-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="0aa98-106">Attributes and elements</span></span>

<span data-ttu-id="0aa98-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="0aa98-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0aa98-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="0aa98-108">Attributes</span></span>

|<span data-ttu-id="0aa98-109">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="0aa98-109">**Attribute**</span></span>|<span data-ttu-id="0aa98-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0aa98-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0aa98-111">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="0aa98-111">ResponseClass</span></span>  <br/> |<span data-ttu-id="0aa98-112">Indica la clase de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0aa98-112">Indicates the class of the response.</span></span>  <br/> |
   
#### <a name="responseclass"></a><span data-ttu-id="0aa98-113">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="0aa98-113">ResponseClass</span></span>

|<span data-ttu-id="0aa98-114">**Valor**</span><span class="sxs-lookup"><span data-stu-id="0aa98-114">**Value**</span></span>|<span data-ttu-id="0aa98-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0aa98-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0aa98-116">Correcto</span><span class="sxs-lookup"><span data-stu-id="0aa98-116">Success</span></span>  <br/> |<span data-ttu-id="0aa98-117">Indica que se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="0aa98-117">Indicates success.</span></span>  <br/> |
|<span data-ttu-id="0aa98-118">Advertencia</span><span class="sxs-lookup"><span data-stu-id="0aa98-118">Warning</span></span>  <br/> |<span data-ttu-id="0aa98-119">Indica una advertencia.</span><span class="sxs-lookup"><span data-stu-id="0aa98-119">Indicates a warning.</span></span>  <br/> |
|<span data-ttu-id="0aa98-120">Error</span><span class="sxs-lookup"><span data-stu-id="0aa98-120">Error</span></span>  <br/> |<span data-ttu-id="0aa98-121">Indica un error.</span><span class="sxs-lookup"><span data-stu-id="0aa98-121">Indicates an error.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="0aa98-122">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="0aa98-122">Child elements</span></span>

|<span data-ttu-id="0aa98-123">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="0aa98-123">**Element**</span></span>|<span data-ttu-id="0aa98-124">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0aa98-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0aa98-125">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="0aa98-125">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="0aa98-126">Actualmente no está en uso y reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="0aa98-126">Currently unused and reserved for future use.</span></span>  <br/> |
|[<span data-ttu-id="0aa98-127">Items</span><span class="sxs-lookup"><span data-stu-id="0aa98-127">Items</span></span>](items.md) <br/> |<span data-ttu-id="0aa98-128">Contiene una matriz de elementos.</span><span class="sxs-lookup"><span data-stu-id="0aa98-128">Contains an array of items.</span></span>  <br/> |
|[<span data-ttu-id="0aa98-129">MessageText</span><span class="sxs-lookup"><span data-stu-id="0aa98-129">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="0aa98-130">Proporciona una descripción de texto del estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0aa98-130">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="0aa98-131">MessageXml</span><span class="sxs-lookup"><span data-stu-id="0aa98-131">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="0aa98-132">Proporciona información de respuesta de error adicional.</span><span class="sxs-lookup"><span data-stu-id="0aa98-132">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="0aa98-133">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="0aa98-133">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="0aa98-134">Proporciona información de estado sobre la solicitud.</span><span class="sxs-lookup"><span data-stu-id="0aa98-134">Provides status information about the request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="0aa98-135">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="0aa98-135">Parent elements</span></span>

|<span data-ttu-id="0aa98-136">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="0aa98-136">**Element**</span></span>|<span data-ttu-id="0aa98-137">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0aa98-137">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0aa98-138">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="0aa98-138">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="0aa98-139">Contiene los mensajes de respuesta de una solicitud de servicios web Exchange.</span><span class="sxs-lookup"><span data-stu-id="0aa98-139">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0aa98-140">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0aa98-140">Remarks</span></span>

<span data-ttu-id="0aa98-141">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="0aa98-141">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="0aa98-142">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="0aa98-142">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0aa98-143">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="0aa98-143">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0aa98-144">Namespace</span><span class="sxs-lookup"><span data-stu-id="0aa98-144">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="0aa98-145">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="0aa98-145">Schema Name</span></span>  <br/> |<span data-ttu-id="0aa98-146">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="0aa98-146">Message schema</span></span>  <br/> |
|<span data-ttu-id="0aa98-147">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="0aa98-147">Validation File</span></span>  <br/> |<span data-ttu-id="0aa98-148">messages. xsd</span><span class="sxs-lookup"><span data-stu-id="0aa98-148">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="0aa98-149">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="0aa98-149">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="0aa98-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="0aa98-150">See also</span></span>

- [<span data-ttu-id="0aa98-151">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="0aa98-151">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

