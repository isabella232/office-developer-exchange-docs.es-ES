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
ms.lasthandoff: 06/11/2018
ms.locfileid: "19835942"
---
# <a name="installappresponse"></a><span data-ttu-id="dd632-103">InstallAppResponse</span><span class="sxs-lookup"><span data-stu-id="dd632-103">InstallAppResponse</span></span>

<span data-ttu-id="dd632-104">El elemento **InstallAppResponse** especifica la respuesta a una solicitud de **InstallApp** .</span><span class="sxs-lookup"><span data-stu-id="dd632-104">The **InstallAppResponse** element specifies the response to an **InstallApp** request.</span></span> 
  
```xml
<InstallAppResponse ResponseClass="">
    <MessageText></MessageText>
    <ResponseCode></ResponseCode>
    <DescriptiveLinkKey></DescriptiveLinkKey>
    <MessageXml></MessageXml>
</InstallAppResponse>
```

 <span data-ttu-id="dd632-105">**InstallAppResponseType**</span><span class="sxs-lookup"><span data-stu-id="dd632-105">**InstallAppResponseType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="dd632-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="dd632-106">Attributes and elements</span></span>

<span data-ttu-id="dd632-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="dd632-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="dd632-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="dd632-108">Attributes</span></span>

|<span data-ttu-id="dd632-109">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="dd632-109">**Attribute**</span></span>|<span data-ttu-id="dd632-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="dd632-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="dd632-111">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="dd632-111">ResponseClass</span></span>  <br/> |<span data-ttu-id="dd632-112">Indica la clase de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="dd632-112">Indicates the class of the response.</span></span>  <br/> |
   
#### <a name="responseclass"></a><span data-ttu-id="dd632-113">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="dd632-113">ResponseClass</span></span>

|<span data-ttu-id="dd632-114">**Valor**</span><span class="sxs-lookup"><span data-stu-id="dd632-114">**Value**</span></span>|<span data-ttu-id="dd632-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="dd632-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="dd632-116">Correcto</span><span class="sxs-lookup"><span data-stu-id="dd632-116">Success</span></span>  <br/> |<span data-ttu-id="dd632-117">Indica éxito.</span><span class="sxs-lookup"><span data-stu-id="dd632-117">Indicates success.</span></span>  <br/> |
|<span data-ttu-id="dd632-118">Advertencia</span><span class="sxs-lookup"><span data-stu-id="dd632-118">Warning</span></span>  <br/> |<span data-ttu-id="dd632-119">Indica una advertencia.</span><span class="sxs-lookup"><span data-stu-id="dd632-119">Indicates a warning.</span></span>  <br/> |
|<span data-ttu-id="dd632-120">Error</span><span class="sxs-lookup"><span data-stu-id="dd632-120">Error</span></span>  <br/> |<span data-ttu-id="dd632-121">Indica un error.</span><span class="sxs-lookup"><span data-stu-id="dd632-121">Indicates an error.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="dd632-122">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="dd632-122">Child elements</span></span>

|<span data-ttu-id="dd632-123">**Element**</span><span class="sxs-lookup"><span data-stu-id="dd632-123">**Element**</span></span>|<span data-ttu-id="dd632-124">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="dd632-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="dd632-125">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="dd632-125">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="dd632-126">Actualmente no utilizado y reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="dd632-126">Currently unused and reserved for future use.</span></span>  <br/> |
|[<span data-ttu-id="dd632-127">MessageText</span><span class="sxs-lookup"><span data-stu-id="dd632-127">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="dd632-128">Proporciona una descripción de texto del estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="dd632-128">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="dd632-129">MessageXml</span><span class="sxs-lookup"><span data-stu-id="dd632-129">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="dd632-130">Proporciona información de la respuesta de error adicionales.</span><span class="sxs-lookup"><span data-stu-id="dd632-130">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="dd632-131">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="dd632-131">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="dd632-132">Proporciona información de estado acerca de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="dd632-132">Provides status information about the request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="dd632-133">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="dd632-133">Parent elements</span></span>

|<span data-ttu-id="dd632-134">**Element**</span><span class="sxs-lookup"><span data-stu-id="dd632-134">**Element**</span></span>|<span data-ttu-id="dd632-135">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="dd632-135">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="dd632-136">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="dd632-136">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="dd632-137">Contiene los mensajes de respuesta para una solicitud de servicios Web de Exchange.</span><span class="sxs-lookup"><span data-stu-id="dd632-137">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="dd632-138">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="dd632-138">Text value</span></span>

<span data-ttu-id="dd632-139">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="dd632-139">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="dd632-140">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dd632-140">Remarks</span></span>

<span data-ttu-id="dd632-141">El elemento **GetAppManifestsResponseMessage** es aplicable para los clientes que estén destinados a Exchange Online y versiones de Exchange 2013 a partir de Microsoft Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="dd632-141">The **GetAppManifestsResponseMessage** element is applicable for clients that target Exchange Online and versions of Microsoft Exchange Server starting with Exchange 2013.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="dd632-142">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="dd632-142">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="dd632-143">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="dd632-143">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="dd632-144">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="dd632-144">Schema Name</span></span>  <br/> |<span data-ttu-id="dd632-145">Esquema de mensaje</span><span class="sxs-lookup"><span data-stu-id="dd632-145">Message schema</span></span>  <br/> |
|<span data-ttu-id="dd632-146">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="dd632-146">Validation File</span></span>  <br/> |<span data-ttu-id="dd632-147">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="dd632-147">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="dd632-148">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="dd632-148">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="dd632-149">Ver también</span><span class="sxs-lookup"><span data-stu-id="dd632-149">See also</span></span>



- [<span data-ttu-id="dd632-150">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="dd632-150">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

