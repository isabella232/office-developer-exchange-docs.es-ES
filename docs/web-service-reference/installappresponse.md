---
title: InstallAppResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c5e0582d-c1e1-453b-93ed-c31165c82697
description: El elemento InstallAppResponse especifica la respuesta a una solicitud InstallApp.
ms.openlocfilehash: 0f7690e2df7e71c4e478dec191671af24f96294b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465670"
---
# <a name="installappresponse"></a><span data-ttu-id="1b241-103">InstallAppResponse</span><span class="sxs-lookup"><span data-stu-id="1b241-103">InstallAppResponse</span></span>

<span data-ttu-id="1b241-104">El elemento **InstallAppResponse** especifica la respuesta a una solicitud **InstallApp** .</span><span class="sxs-lookup"><span data-stu-id="1b241-104">The **InstallAppResponse** element specifies the response to an **InstallApp** request.</span></span> 
  
```xml
<InstallAppResponse ResponseClass="">
    <MessageText></MessageText>
    <ResponseCode></ResponseCode>
    <DescriptiveLinkKey></DescriptiveLinkKey>
    <MessageXml></MessageXml>
</InstallAppResponse>
```

 <span data-ttu-id="1b241-105">**InstallAppResponseType**</span><span class="sxs-lookup"><span data-stu-id="1b241-105">**InstallAppResponseType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1b241-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="1b241-106">Attributes and elements</span></span>

<span data-ttu-id="1b241-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="1b241-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1b241-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="1b241-108">Attributes</span></span>

|<span data-ttu-id="1b241-109">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="1b241-109">**Attribute**</span></span>|<span data-ttu-id="1b241-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1b241-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1b241-111">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="1b241-111">ResponseClass</span></span>  <br/> |<span data-ttu-id="1b241-112">Indica la clase de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1b241-112">Indicates the class of the response.</span></span>  <br/> |
   
#### <a name="responseclass"></a><span data-ttu-id="1b241-113">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="1b241-113">ResponseClass</span></span>

|<span data-ttu-id="1b241-114">**Valor**</span><span class="sxs-lookup"><span data-stu-id="1b241-114">**Value**</span></span>|<span data-ttu-id="1b241-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1b241-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1b241-116">Correcto</span><span class="sxs-lookup"><span data-stu-id="1b241-116">Success</span></span>  <br/> |<span data-ttu-id="1b241-117">Indica que se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="1b241-117">Indicates success.</span></span>  <br/> |
|<span data-ttu-id="1b241-118">Advertencia</span><span class="sxs-lookup"><span data-stu-id="1b241-118">Warning</span></span>  <br/> |<span data-ttu-id="1b241-119">Indica una advertencia.</span><span class="sxs-lookup"><span data-stu-id="1b241-119">Indicates a warning.</span></span>  <br/> |
|<span data-ttu-id="1b241-120">Error</span><span class="sxs-lookup"><span data-stu-id="1b241-120">Error</span></span>  <br/> |<span data-ttu-id="1b241-121">Indica un error.</span><span class="sxs-lookup"><span data-stu-id="1b241-121">Indicates an error.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="1b241-122">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="1b241-122">Child elements</span></span>

|<span data-ttu-id="1b241-123">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="1b241-123">**Element**</span></span>|<span data-ttu-id="1b241-124">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1b241-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1b241-125">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="1b241-125">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="1b241-126">Actualmente no está en uso y reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="1b241-126">Currently unused and reserved for future use.</span></span>  <br/> |
|[<span data-ttu-id="1b241-127">MessageText</span><span class="sxs-lookup"><span data-stu-id="1b241-127">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="1b241-128">Proporciona una descripción de texto del estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1b241-128">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="1b241-129">MessageXml</span><span class="sxs-lookup"><span data-stu-id="1b241-129">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="1b241-130">Proporciona información de respuesta de error adicional.</span><span class="sxs-lookup"><span data-stu-id="1b241-130">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="1b241-131">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="1b241-131">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="1b241-132">Proporciona información de estado sobre la solicitud.</span><span class="sxs-lookup"><span data-stu-id="1b241-132">Provides status information about the request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="1b241-133">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="1b241-133">Parent elements</span></span>

|<span data-ttu-id="1b241-134">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="1b241-134">**Element**</span></span>|<span data-ttu-id="1b241-135">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1b241-135">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1b241-136">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="1b241-136">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="1b241-137">Contiene los mensajes de respuesta de una solicitud de servicios web Exchange.</span><span class="sxs-lookup"><span data-stu-id="1b241-137">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="1b241-138">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="1b241-138">Text value</span></span>

<span data-ttu-id="1b241-139">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="1b241-139">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1b241-140">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1b241-140">Remarks</span></span>

<span data-ttu-id="1b241-141">El elemento **GetAppManifestsResponseMessage** se aplica a los clientes de Exchange Online y versiones de Microsoft Exchange Server que empiecen por Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="1b241-141">The **GetAppManifestsResponseMessage** element is applicable for clients that target Exchange Online and versions of Microsoft Exchange Server starting with Exchange 2013.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="1b241-142">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="1b241-142">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1b241-143">Namespace</span><span class="sxs-lookup"><span data-stu-id="1b241-143">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="1b241-144">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="1b241-144">Schema Name</span></span>  <br/> |<span data-ttu-id="1b241-145">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="1b241-145">Message schema</span></span>  <br/> |
|<span data-ttu-id="1b241-146">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="1b241-146">Validation File</span></span>  <br/> |<span data-ttu-id="1b241-147">messages. xsd</span><span class="sxs-lookup"><span data-stu-id="1b241-147">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="1b241-148">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="1b241-148">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="1b241-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="1b241-149">See also</span></span>



- [<span data-ttu-id="1b241-150">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="1b241-150">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

