---
title: GetAppMarketplaceUrlResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: dc3368ec-78c2-4f8d-8394-4891e90dafd2
description: El elemento GetAppMarketplaceUrlResponse especifica la respuesta a una solicitud GetAppMarketplaceUrl.
ms.openlocfilehash: 7ff000908a2f73f41575cae8a7795644dd60565d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530856"
---
# <a name="getappmarketplaceurlresponse"></a><span data-ttu-id="06d6f-103">GetAppMarketplaceUrlResponse</span><span class="sxs-lookup"><span data-stu-id="06d6f-103">GetAppMarketplaceUrlResponse</span></span>

<span data-ttu-id="06d6f-104">El elemento **GetAppMarketplaceUrlResponse** especifica la respuesta a una solicitud **GetAppMarketplaceUrl** .</span><span class="sxs-lookup"><span data-stu-id="06d6f-104">The **GetAppMarketplaceUrlResponse** element specifies the response to a **GetAppMarketplaceUrl** request.</span></span> 
  
```XML
<GetAppMarketplaceUrlResponse ResponseClass=" Success | Warning | Error ">
    <AppMarketplaceUrl/>
    <MessageText/>
    <ResponseCode/>
    <DescriptiveLinkKey/>
    <MessageXml/>
</GetAppMarketplaceUrlResponse>
```

 <span data-ttu-id="06d6f-105">**GetAppMarketplaceUrlResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="06d6f-105">**GetAppMarketplaceUrlResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="06d6f-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="06d6f-106">Attributes and elements</span></span>

<span data-ttu-id="06d6f-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="06d6f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="06d6f-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="06d6f-108">Attributes</span></span>

|<span data-ttu-id="06d6f-109">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="06d6f-109">**Attribute**</span></span>|<span data-ttu-id="06d6f-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="06d6f-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="06d6f-111">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="06d6f-111">ResponseClass</span></span>  <br/> |<span data-ttu-id="06d6f-112">Indica la clase de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="06d6f-112">Indicates the class of the response.</span></span>  <br/> |
   
#### <a name="responseclass"></a><span data-ttu-id="06d6f-113">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="06d6f-113">ResponseClass</span></span>

|<span data-ttu-id="06d6f-114">**Valor**</span><span class="sxs-lookup"><span data-stu-id="06d6f-114">**Value**</span></span>|<span data-ttu-id="06d6f-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="06d6f-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="06d6f-116">Correcto</span><span class="sxs-lookup"><span data-stu-id="06d6f-116">Success</span></span>  <br/> |<span data-ttu-id="06d6f-117">Indica que se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="06d6f-117">Indicates success.</span></span>  <br/> |
|<span data-ttu-id="06d6f-118">Advertencia</span><span class="sxs-lookup"><span data-stu-id="06d6f-118">Warning</span></span>  <br/> |<span data-ttu-id="06d6f-119">Indica una advertencia.</span><span class="sxs-lookup"><span data-stu-id="06d6f-119">Indicates a warning.</span></span>  <br/> |
|<span data-ttu-id="06d6f-120">Error</span><span class="sxs-lookup"><span data-stu-id="06d6f-120">Error</span></span>  <br/> |<span data-ttu-id="06d6f-121">Indica un error.</span><span class="sxs-lookup"><span data-stu-id="06d6f-121">Indicates an error.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="06d6f-122">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="06d6f-122">Child elements</span></span>

|<span data-ttu-id="06d6f-123">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="06d6f-123">**Element**</span></span>|<span data-ttu-id="06d6f-124">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="06d6f-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="06d6f-125">AppMarketplaceUrl</span><span class="sxs-lookup"><span data-stu-id="06d6f-125">AppMarketplaceUrl</span></span>](appmarketplaceurl.md) <br/> |<span data-ttu-id="06d6f-126">Especifica la dirección URL de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="06d6f-126">Specifies the URL for the app.</span></span>  <br/> |
|[<span data-ttu-id="06d6f-127">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="06d6f-127">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="06d6f-128">Actualmente no está en uso y reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="06d6f-128">Currently unused and reserved for future use.</span></span>  <br/> |
|[<span data-ttu-id="06d6f-129">MessageText</span><span class="sxs-lookup"><span data-stu-id="06d6f-129">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="06d6f-130">Proporciona una descripción de texto del estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="06d6f-130">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="06d6f-131">MessageXml</span><span class="sxs-lookup"><span data-stu-id="06d6f-131">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="06d6f-132">Proporciona información de respuesta de error adicional.</span><span class="sxs-lookup"><span data-stu-id="06d6f-132">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="06d6f-133">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="06d6f-133">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="06d6f-134">Proporciona información de estado sobre la solicitud.</span><span class="sxs-lookup"><span data-stu-id="06d6f-134">Provides status information about the request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="06d6f-135">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="06d6f-135">Parent elements</span></span>

|<span data-ttu-id="06d6f-136">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="06d6f-136">**Element**</span></span>|<span data-ttu-id="06d6f-137">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="06d6f-137">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="06d6f-138">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="06d6f-138">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="06d6f-139">Contiene los mensajes de respuesta de una solicitud de servicios web Exchange.</span><span class="sxs-lookup"><span data-stu-id="06d6f-139">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="06d6f-140">Comentarios</span><span class="sxs-lookup"><span data-stu-id="06d6f-140">Remarks</span></span>

<span data-ttu-id="06d6f-141">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="06d6f-141">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="06d6f-142">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="06d6f-142">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="06d6f-143">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="06d6f-143">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="06d6f-144">Namespace</span><span class="sxs-lookup"><span data-stu-id="06d6f-144">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="06d6f-145">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="06d6f-145">Schema Name</span></span>  <br/> |<span data-ttu-id="06d6f-146">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="06d6f-146">Message schema</span></span>  <br/> |
|<span data-ttu-id="06d6f-147">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="06d6f-147">Validation File</span></span>  <br/> |<span data-ttu-id="06d6f-148">messages. xsd</span><span class="sxs-lookup"><span data-stu-id="06d6f-148">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="06d6f-149">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="06d6f-149">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="06d6f-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="06d6f-150">See also</span></span>



- [<span data-ttu-id="06d6f-151">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="06d6f-151">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

