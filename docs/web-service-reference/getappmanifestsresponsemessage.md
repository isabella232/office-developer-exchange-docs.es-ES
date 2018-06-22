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
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764748"
---
# <a name="getappmanifestsresponsemessage"></a><span data-ttu-id="85f9c-103">GetAppManifestsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="85f9c-103">GetAppManifestsResponseMessage</span></span>

<span data-ttu-id="85f9c-104">El elemento **GetAppManifestsResponseMessage** especifica el mensaje de respuesta de una solicitud de **GetAppManifests** .</span><span class="sxs-lookup"><span data-stu-id="85f9c-104">The **GetAppManifestsResponseMessage** element specifies the response message for a **GetAppManifests** request.</span></span> 
  
```XML
<GetAppManifestsResponseMessage ResponseClass=" Success | Warning | Error ">
    <MessageText/>
    <ResponseCode/>
    <DescriptiveLinkKey/>
    <MessageXml/>
</GetAppManifestsResponseMessage>
```

 <span data-ttu-id="85f9c-105">**ResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="85f9c-105">**ResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="85f9c-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="85f9c-106">Attributes and elements</span></span>

<span data-ttu-id="85f9c-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="85f9c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="85f9c-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="85f9c-108">Attributes</span></span>

|<span data-ttu-id="85f9c-109">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="85f9c-109">**Attribute**</span></span>|<span data-ttu-id="85f9c-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="85f9c-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="85f9c-111">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="85f9c-111">ResponseClass</span></span>  <br/> |<span data-ttu-id="85f9c-112">Indica la clase de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="85f9c-112">Indicates the class of the response.</span></span>  <br/> |
   
#### <a name="responseclass"></a><span data-ttu-id="85f9c-113">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="85f9c-113">ResponseClass</span></span>

|<span data-ttu-id="85f9c-114">**Valor**</span><span class="sxs-lookup"><span data-stu-id="85f9c-114">**Value**</span></span>|<span data-ttu-id="85f9c-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="85f9c-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="85f9c-116">Correcto</span><span class="sxs-lookup"><span data-stu-id="85f9c-116">Success</span></span>  <br/> |<span data-ttu-id="85f9c-117">Indica éxito.</span><span class="sxs-lookup"><span data-stu-id="85f9c-117">Indicates success.</span></span>  <br/> |
|<span data-ttu-id="85f9c-118">Advertencia</span><span class="sxs-lookup"><span data-stu-id="85f9c-118">Warning</span></span>  <br/> |<span data-ttu-id="85f9c-119">Indica una advertencia.</span><span class="sxs-lookup"><span data-stu-id="85f9c-119">Indicates a warning.</span></span>  <br/> |
|<span data-ttu-id="85f9c-120">Error</span><span class="sxs-lookup"><span data-stu-id="85f9c-120">Error</span></span>  <br/> |<span data-ttu-id="85f9c-121">Indica un error.</span><span class="sxs-lookup"><span data-stu-id="85f9c-121">Indicates an error.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="85f9c-122">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="85f9c-122">Child elements</span></span>

|<span data-ttu-id="85f9c-123">**Element**</span><span class="sxs-lookup"><span data-stu-id="85f9c-123">**Element**</span></span>|<span data-ttu-id="85f9c-124">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="85f9c-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="85f9c-125">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="85f9c-125">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="85f9c-126">Actualmente no utilizado y reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="85f9c-126">Currently unused and reserved for future use.</span></span>  <br/> |
|[<span data-ttu-id="85f9c-127">MessageText</span><span class="sxs-lookup"><span data-stu-id="85f9c-127">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="85f9c-128">Proporciona una descripción de texto del estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="85f9c-128">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="85f9c-129">MessageXml</span><span class="sxs-lookup"><span data-stu-id="85f9c-129">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="85f9c-130">Proporciona información de la respuesta de error adicionales.</span><span class="sxs-lookup"><span data-stu-id="85f9c-130">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="85f9c-131">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="85f9c-131">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="85f9c-132">Proporciona información de estado acerca de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="85f9c-132">Provides status information about the request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="85f9c-133">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="85f9c-133">Parent elements</span></span>

|<span data-ttu-id="85f9c-134">**Element**</span><span class="sxs-lookup"><span data-stu-id="85f9c-134">**Element**</span></span>|<span data-ttu-id="85f9c-135">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="85f9c-135">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="85f9c-136">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="85f9c-136">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="85f9c-137">Contiene los mensajes de respuesta para una solicitud de servicios Web de Exchange.</span><span class="sxs-lookup"><span data-stu-id="85f9c-137">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="85f9c-138">Notas</span><span class="sxs-lookup"><span data-stu-id="85f9c-138">Remarks</span></span>

<span data-ttu-id="85f9c-139">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="85f9c-139">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="85f9c-140">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="85f9c-140">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="85f9c-141">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="85f9c-141">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="85f9c-142">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="85f9c-142">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="85f9c-143">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="85f9c-143">Schema Name</span></span>  <br/> |<span data-ttu-id="85f9c-144">Esquema de mensaje</span><span class="sxs-lookup"><span data-stu-id="85f9c-144">Message schema</span></span>  <br/> |
|<span data-ttu-id="85f9c-145">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="85f9c-145">Validation File</span></span>  <br/> |<span data-ttu-id="85f9c-146">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="85f9c-146">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="85f9c-147">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="85f9c-147">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="85f9c-148">Ver también</span><span class="sxs-lookup"><span data-stu-id="85f9c-148">See also</span></span>



- [<span data-ttu-id="85f9c-149">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="85f9c-149">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

