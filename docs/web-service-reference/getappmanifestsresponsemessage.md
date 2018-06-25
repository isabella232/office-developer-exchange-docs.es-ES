---
title: GetAppManifestsResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 815908f1-4223-42d8-92dc-f8bdfc6b5df8
description: El elemento GetAppManifestsResponseMessage especifica el mensaje de respuesta de una solicitud de GetAppManifests.
ms.openlocfilehash: 05eeef7f7194c1dc05be93ed13ebff93d5013e94
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764748"
---
# <a name="getappmanifestsresponsemessage"></a><span data-ttu-id="86bbf-103">GetAppManifestsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="86bbf-103">GetAppManifestsResponseMessage</span></span>

<span data-ttu-id="86bbf-104">El elemento **GetAppManifestsResponseMessage** especifica el mensaje de respuesta de una solicitud de **GetAppManifests** .</span><span class="sxs-lookup"><span data-stu-id="86bbf-104">The **GetAppManifestsResponseMessage** element specifies the response message for a **GetAppManifests** request.</span></span> 
  
```XML
<GetAppManifestsResponseMessage ResponseClass=" Success | Warning | Error ">
    <MessageText/>
    <ResponseCode/>
    <DescriptiveLinkKey/>
    <MessageXml/>
</GetAppManifestsResponseMessage>
```

 <span data-ttu-id="86bbf-105">**ResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="86bbf-105">**ResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="86bbf-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="86bbf-106">Attributes and elements</span></span>

<span data-ttu-id="86bbf-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="86bbf-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="86bbf-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="86bbf-108">Attributes</span></span>

|<span data-ttu-id="86bbf-109">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="86bbf-109">**Attribute**</span></span>|<span data-ttu-id="86bbf-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="86bbf-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="86bbf-111">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="86bbf-111">ResponseClass</span></span>  <br/> |<span data-ttu-id="86bbf-112">Indica la clase de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="86bbf-112">Indicates the class of the response.</span></span>  <br/> |
   
#### <a name="responseclass"></a><span data-ttu-id="86bbf-113">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="86bbf-113">ResponseClass</span></span>

|<span data-ttu-id="86bbf-114">**Valor**</span><span class="sxs-lookup"><span data-stu-id="86bbf-114">**Value**</span></span>|<span data-ttu-id="86bbf-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="86bbf-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="86bbf-116">Correcto</span><span class="sxs-lookup"><span data-stu-id="86bbf-116">Success</span></span>  <br/> |<span data-ttu-id="86bbf-117">Indica éxito.</span><span class="sxs-lookup"><span data-stu-id="86bbf-117">Indicates success.</span></span>  <br/> |
|<span data-ttu-id="86bbf-118">Advertencia</span><span class="sxs-lookup"><span data-stu-id="86bbf-118">Warning</span></span>  <br/> |<span data-ttu-id="86bbf-119">Indica una advertencia.</span><span class="sxs-lookup"><span data-stu-id="86bbf-119">Indicates a warning.</span></span>  <br/> |
|<span data-ttu-id="86bbf-120">Error</span><span class="sxs-lookup"><span data-stu-id="86bbf-120">Error</span></span>  <br/> |<span data-ttu-id="86bbf-121">Indica un error.</span><span class="sxs-lookup"><span data-stu-id="86bbf-121">Indicates an error.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="86bbf-122">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="86bbf-122">Child elements</span></span>

|<span data-ttu-id="86bbf-123">**Element**</span><span class="sxs-lookup"><span data-stu-id="86bbf-123">**Element**</span></span>|<span data-ttu-id="86bbf-124">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="86bbf-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="86bbf-125">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="86bbf-125">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="86bbf-126">Actualmente no utilizado y reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="86bbf-126">Currently unused and reserved for future use.</span></span>  <br/> |
|[<span data-ttu-id="86bbf-127">MessageText</span><span class="sxs-lookup"><span data-stu-id="86bbf-127">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="86bbf-128">Proporciona una descripción de texto del estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="86bbf-128">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="86bbf-129">MessageXml</span><span class="sxs-lookup"><span data-stu-id="86bbf-129">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="86bbf-130">Proporciona información de la respuesta de error adicionales.</span><span class="sxs-lookup"><span data-stu-id="86bbf-130">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="86bbf-131">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="86bbf-131">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="86bbf-132">Proporciona información de estado acerca de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="86bbf-132">Provides status information about the request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="86bbf-133">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="86bbf-133">Parent elements</span></span>

|<span data-ttu-id="86bbf-134">**Element**</span><span class="sxs-lookup"><span data-stu-id="86bbf-134">**Element**</span></span>|<span data-ttu-id="86bbf-135">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="86bbf-135">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="86bbf-136">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="86bbf-136">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="86bbf-137">Contiene los mensajes de respuesta para una solicitud de servicios Web de Exchange.</span><span class="sxs-lookup"><span data-stu-id="86bbf-137">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="86bbf-138">Comentarios</span><span class="sxs-lookup"><span data-stu-id="86bbf-138">Remarks</span></span>

<span data-ttu-id="86bbf-139">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="86bbf-139">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="86bbf-140">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="86bbf-140">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="86bbf-141">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="86bbf-141">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="86bbf-142">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="86bbf-142">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="86bbf-143">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="86bbf-143">Schema Name</span></span>  <br/> |<span data-ttu-id="86bbf-144">Esquema de mensaje</span><span class="sxs-lookup"><span data-stu-id="86bbf-144">Message schema</span></span>  <br/> |
|<span data-ttu-id="86bbf-145">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="86bbf-145">Validation File</span></span>  <br/> |<span data-ttu-id="86bbf-146">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="86bbf-146">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="86bbf-147">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="86bbf-147">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="86bbf-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="86bbf-148">See also</span></span>



- [<span data-ttu-id="86bbf-149">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="86bbf-149">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

