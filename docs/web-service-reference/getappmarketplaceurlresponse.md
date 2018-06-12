---
title: GetAppMarketplaceUrlResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: dc3368ec-78c2-4f8d-8394-4891e90dafd2
description: El elemento GetAppMarketplaceUrlResponse especifica la respuesta a una solicitud de GetAppMarketplaceUrl.
ms.openlocfilehash: 553ebfc4615280c77d4a1ef9e5db3e5d10a0f2a4
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764750"
---
# <a name="getappmarketplaceurlresponse"></a><span data-ttu-id="23382-103">GetAppMarketplaceUrlResponse</span><span class="sxs-lookup"><span data-stu-id="23382-103">GetAppMarketplaceUrlResponse</span></span>

<span data-ttu-id="23382-104">El elemento **GetAppMarketplaceUrlResponse** especifica la respuesta a una solicitud de **GetAppMarketplaceUrl** .</span><span class="sxs-lookup"><span data-stu-id="23382-104">The **GetAppMarketplaceUrlResponse** element specifies the response to a **GetAppMarketplaceUrl** request.</span></span> 
  
```XML
<GetAppMarketplaceUrlResponse ResponseClass=" Success | Warning | Error ">
    <AppMarketplaceUrl/>
    <MessageText/>
    <ResponseCode/>
    <DescriptiveLinkKey/>
    <MessageXml/>
</GetAppMarketplaceUrlResponse>
```

 <span data-ttu-id="23382-105">**GetAppMarketplaceUrlResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="23382-105">**GetAppMarketplaceUrlResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="23382-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="23382-106">Attributes and elements</span></span>

<span data-ttu-id="23382-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="23382-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="23382-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="23382-108">Attributes</span></span>

|<span data-ttu-id="23382-109">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="23382-109">**Attribute**</span></span>|<span data-ttu-id="23382-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="23382-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="23382-111">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="23382-111">ResponseClass</span></span>  <br/> |<span data-ttu-id="23382-112">Indica la clase de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="23382-112">Indicates the class of the response.</span></span>  <br/> |
   
#### <a name="responseclass"></a><span data-ttu-id="23382-113">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="23382-113">ResponseClass</span></span>

|<span data-ttu-id="23382-114">**Valor**</span><span class="sxs-lookup"><span data-stu-id="23382-114">**Value**</span></span>|<span data-ttu-id="23382-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="23382-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="23382-116">Correcto</span><span class="sxs-lookup"><span data-stu-id="23382-116">Success</span></span>  <br/> |<span data-ttu-id="23382-117">Indica éxito.</span><span class="sxs-lookup"><span data-stu-id="23382-117">Indicates success.</span></span>  <br/> |
|<span data-ttu-id="23382-118">Advertencia</span><span class="sxs-lookup"><span data-stu-id="23382-118">Warning</span></span>  <br/> |<span data-ttu-id="23382-119">Indica una advertencia.</span><span class="sxs-lookup"><span data-stu-id="23382-119">Indicates a warning.</span></span>  <br/> |
|<span data-ttu-id="23382-120">Error</span><span class="sxs-lookup"><span data-stu-id="23382-120">Error</span></span>  <br/> |<span data-ttu-id="23382-121">Indica un error.</span><span class="sxs-lookup"><span data-stu-id="23382-121">Indicates an error.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="23382-122">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="23382-122">Child elements</span></span>

|<span data-ttu-id="23382-123">**Element**</span><span class="sxs-lookup"><span data-stu-id="23382-123">**Element**</span></span>|<span data-ttu-id="23382-124">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="23382-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="23382-125">AppMarketplaceUrl</span><span class="sxs-lookup"><span data-stu-id="23382-125">AppMarketplaceUrl</span></span>](appmarketplaceurl.md) <br/> |<span data-ttu-id="23382-126">Especifica la dirección URL de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="23382-126">Specifies the URL for the app.</span></span>  <br/> |
|[<span data-ttu-id="23382-127">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="23382-127">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="23382-128">Actualmente no utilizado y reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="23382-128">Currently unused and reserved for future use.</span></span>  <br/> |
|[<span data-ttu-id="23382-129">MessageText</span><span class="sxs-lookup"><span data-stu-id="23382-129">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="23382-130">Proporciona una descripción de texto del estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="23382-130">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="23382-131">MessageXml</span><span class="sxs-lookup"><span data-stu-id="23382-131">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="23382-132">Proporciona información de la respuesta de error adicionales.</span><span class="sxs-lookup"><span data-stu-id="23382-132">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="23382-133">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="23382-133">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="23382-134">Proporciona información de estado acerca de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="23382-134">Provides status information about the request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="23382-135">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="23382-135">Parent elements</span></span>

|<span data-ttu-id="23382-136">**Element**</span><span class="sxs-lookup"><span data-stu-id="23382-136">**Element**</span></span>|<span data-ttu-id="23382-137">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="23382-137">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="23382-138">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="23382-138">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="23382-139">Contiene los mensajes de respuesta para una solicitud de servicios Web de Exchange.</span><span class="sxs-lookup"><span data-stu-id="23382-139">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="23382-140">Notas</span><span class="sxs-lookup"><span data-stu-id="23382-140">Remarks</span></span>

<span data-ttu-id="23382-141">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="23382-141">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="23382-142">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="23382-142">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="23382-143">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="23382-143">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="23382-144">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="23382-144">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="23382-145">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="23382-145">Schema Name</span></span>  <br/> |<span data-ttu-id="23382-146">Esquema de mensaje</span><span class="sxs-lookup"><span data-stu-id="23382-146">Message schema</span></span>  <br/> |
|<span data-ttu-id="23382-147">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="23382-147">Validation File</span></span>  <br/> |<span data-ttu-id="23382-148">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="23382-148">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="23382-149">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="23382-149">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="23382-150">Ver también</span><span class="sxs-lookup"><span data-stu-id="23382-150">See also</span></span>



- [<span data-ttu-id="23382-151">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="23382-151">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

