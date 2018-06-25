---
title: InstallAppResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c5e0582d-c1e1-453b-93ed-c31165c82697
description: El elemento InstallAppResponse especifica la respuesta a una solicitud de InstallApp.
ms.openlocfilehash: 8e8da720b3a38e979b3d83810bb798350822146c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19835942"
---
# <a name="installappresponse"></a><span data-ttu-id="f1943-103">InstallAppResponse</span><span class="sxs-lookup"><span data-stu-id="f1943-103">InstallAppResponse</span></span>

<span data-ttu-id="f1943-104">El elemento **InstallAppResponse** especifica la respuesta a una solicitud de **InstallApp** .</span><span class="sxs-lookup"><span data-stu-id="f1943-104">The **InstallAppResponse** element specifies the response to an **InstallApp** request.</span></span> 
  
```xml
<InstallAppResponse ResponseClass="">
    <MessageText></MessageText>
    <ResponseCode></ResponseCode>
    <DescriptiveLinkKey></DescriptiveLinkKey>
    <MessageXml></MessageXml>
</InstallAppResponse>
```

 <span data-ttu-id="f1943-105">**InstallAppResponseType**</span><span class="sxs-lookup"><span data-stu-id="f1943-105">**InstallAppResponseType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f1943-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="f1943-106">Attributes and elements</span></span>

<span data-ttu-id="f1943-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="f1943-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f1943-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="f1943-108">Attributes</span></span>

|<span data-ttu-id="f1943-109">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="f1943-109">**Attribute**</span></span>|<span data-ttu-id="f1943-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f1943-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f1943-111">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="f1943-111">ResponseClass</span></span>  <br/> |<span data-ttu-id="f1943-112">Indica la clase de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f1943-112">Indicates the class of the response.</span></span>  <br/> |
   
#### <a name="responseclass"></a><span data-ttu-id="f1943-113">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="f1943-113">ResponseClass</span></span>

|<span data-ttu-id="f1943-114">**Valor**</span><span class="sxs-lookup"><span data-stu-id="f1943-114">**Value**</span></span>|<span data-ttu-id="f1943-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f1943-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f1943-116">Correcto</span><span class="sxs-lookup"><span data-stu-id="f1943-116">Success</span></span>  <br/> |<span data-ttu-id="f1943-117">Indica éxito.</span><span class="sxs-lookup"><span data-stu-id="f1943-117">Indicates success.</span></span>  <br/> |
|<span data-ttu-id="f1943-118">Advertencia</span><span class="sxs-lookup"><span data-stu-id="f1943-118">Warning</span></span>  <br/> |<span data-ttu-id="f1943-119">Indica una advertencia.</span><span class="sxs-lookup"><span data-stu-id="f1943-119">Indicates a warning.</span></span>  <br/> |
|<span data-ttu-id="f1943-120">Error</span><span class="sxs-lookup"><span data-stu-id="f1943-120">Error</span></span>  <br/> |<span data-ttu-id="f1943-121">Indica un error.</span><span class="sxs-lookup"><span data-stu-id="f1943-121">Indicates an error.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="f1943-122">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="f1943-122">Child elements</span></span>

|<span data-ttu-id="f1943-123">**Element**</span><span class="sxs-lookup"><span data-stu-id="f1943-123">**Element**</span></span>|<span data-ttu-id="f1943-124">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f1943-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f1943-125">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="f1943-125">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="f1943-126">Actualmente no utilizado y reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="f1943-126">Currently unused and reserved for future use.</span></span>  <br/> |
|[<span data-ttu-id="f1943-127">MessageText</span><span class="sxs-lookup"><span data-stu-id="f1943-127">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="f1943-128">Proporciona una descripción de texto del estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f1943-128">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="f1943-129">MessageXml</span><span class="sxs-lookup"><span data-stu-id="f1943-129">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="f1943-130">Proporciona información de la respuesta de error adicionales.</span><span class="sxs-lookup"><span data-stu-id="f1943-130">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="f1943-131">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="f1943-131">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="f1943-132">Proporciona información de estado acerca de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f1943-132">Provides status information about the request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="f1943-133">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="f1943-133">Parent elements</span></span>

|<span data-ttu-id="f1943-134">**Element**</span><span class="sxs-lookup"><span data-stu-id="f1943-134">**Element**</span></span>|<span data-ttu-id="f1943-135">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f1943-135">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f1943-136">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="f1943-136">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="f1943-137">Contiene los mensajes de respuesta para una solicitud de servicios Web de Exchange.</span><span class="sxs-lookup"><span data-stu-id="f1943-137">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="f1943-138">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="f1943-138">Text value</span></span>

<span data-ttu-id="f1943-139">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="f1943-139">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f1943-140">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f1943-140">Remarks</span></span>

<span data-ttu-id="f1943-141">El elemento **GetAppManifestsResponseMessage** es aplicable para los clientes que estén destinados a Exchange Online y versiones de Exchange 2013 a partir de Microsoft Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="f1943-141">The **GetAppManifestsResponseMessage** element is applicable for clients that target Exchange Online and versions of Microsoft Exchange Server starting with Exchange 2013.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="f1943-142">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="f1943-142">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f1943-143">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f1943-143">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="f1943-144">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="f1943-144">Schema Name</span></span>  <br/> |<span data-ttu-id="f1943-145">Esquema de mensaje</span><span class="sxs-lookup"><span data-stu-id="f1943-145">Message schema</span></span>  <br/> |
|<span data-ttu-id="f1943-146">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="f1943-146">Validation File</span></span>  <br/> |<span data-ttu-id="f1943-147">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="f1943-147">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="f1943-148">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="f1943-148">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="f1943-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="f1943-149">See also</span></span>



- [<span data-ttu-id="f1943-150">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="f1943-150">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

