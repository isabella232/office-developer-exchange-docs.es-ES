---
title: GetAppManifestsResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 815908f1-4223-42d8-92dc-f8bdfc6b5df8
description: El elemento GetAppManifestsResponseMessage especifica el mensaje de respuesta para una solicitud de GetAppManifests.
ms.openlocfilehash: 26a521d8647a010fe956596eaf63d4df4756edb2
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459535"
---
# <a name="getappmanifestsresponsemessage"></a><span data-ttu-id="f2474-103">GetAppManifestsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="f2474-103">GetAppManifestsResponseMessage</span></span>

<span data-ttu-id="f2474-104">El elemento **GetAppManifestsResponseMessage** especifica el mensaje de respuesta para una solicitud de **GetAppManifests** .</span><span class="sxs-lookup"><span data-stu-id="f2474-104">The **GetAppManifestsResponseMessage** element specifies the response message for a **GetAppManifests** request.</span></span> 
  
```XML
<GetAppManifestsResponseMessage ResponseClass=" Success | Warning | Error ">
    <MessageText/>
    <ResponseCode/>
    <DescriptiveLinkKey/>
    <MessageXml/>
</GetAppManifestsResponseMessage>
```

 <span data-ttu-id="f2474-105">**ResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="f2474-105">**ResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f2474-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="f2474-106">Attributes and elements</span></span>

<span data-ttu-id="f2474-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="f2474-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f2474-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="f2474-108">Attributes</span></span>

|<span data-ttu-id="f2474-109">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="f2474-109">**Attribute**</span></span>|<span data-ttu-id="f2474-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f2474-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f2474-111">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="f2474-111">ResponseClass</span></span>  <br/> |<span data-ttu-id="f2474-112">Indica la clase de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f2474-112">Indicates the class of the response.</span></span>  <br/> |
   
#### <a name="responseclass"></a><span data-ttu-id="f2474-113">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="f2474-113">ResponseClass</span></span>

|<span data-ttu-id="f2474-114">**Valor**</span><span class="sxs-lookup"><span data-stu-id="f2474-114">**Value**</span></span>|<span data-ttu-id="f2474-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f2474-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f2474-116">Correcto</span><span class="sxs-lookup"><span data-stu-id="f2474-116">Success</span></span>  <br/> |<span data-ttu-id="f2474-117">Indica que se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="f2474-117">Indicates success.</span></span>  <br/> |
|<span data-ttu-id="f2474-118">Advertencia</span><span class="sxs-lookup"><span data-stu-id="f2474-118">Warning</span></span>  <br/> |<span data-ttu-id="f2474-119">Indica una advertencia.</span><span class="sxs-lookup"><span data-stu-id="f2474-119">Indicates a warning.</span></span>  <br/> |
|<span data-ttu-id="f2474-120">Error</span><span class="sxs-lookup"><span data-stu-id="f2474-120">Error</span></span>  <br/> |<span data-ttu-id="f2474-121">Indica un error.</span><span class="sxs-lookup"><span data-stu-id="f2474-121">Indicates an error.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="f2474-122">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="f2474-122">Child elements</span></span>

|<span data-ttu-id="f2474-123">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="f2474-123">**Element**</span></span>|<span data-ttu-id="f2474-124">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f2474-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f2474-125">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="f2474-125">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="f2474-126">Actualmente no está en uso y reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="f2474-126">Currently unused and reserved for future use.</span></span>  <br/> |
|[<span data-ttu-id="f2474-127">MessageText</span><span class="sxs-lookup"><span data-stu-id="f2474-127">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="f2474-128">Proporciona una descripción de texto del estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f2474-128">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="f2474-129">MessageXml</span><span class="sxs-lookup"><span data-stu-id="f2474-129">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="f2474-130">Proporciona información de respuesta de error adicional.</span><span class="sxs-lookup"><span data-stu-id="f2474-130">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="f2474-131">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="f2474-131">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="f2474-132">Proporciona información de estado sobre la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f2474-132">Provides status information about the request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="f2474-133">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="f2474-133">Parent elements</span></span>

|<span data-ttu-id="f2474-134">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="f2474-134">**Element**</span></span>|<span data-ttu-id="f2474-135">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f2474-135">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f2474-136">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="f2474-136">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="f2474-137">Contiene los mensajes de respuesta de una solicitud de servicios web Exchange.</span><span class="sxs-lookup"><span data-stu-id="f2474-137">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f2474-138">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f2474-138">Remarks</span></span>

<span data-ttu-id="f2474-139">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="f2474-139">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="f2474-140">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="f2474-140">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f2474-141">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="f2474-141">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f2474-142">Namespace</span><span class="sxs-lookup"><span data-stu-id="f2474-142">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="f2474-143">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="f2474-143">Schema Name</span></span>  <br/> |<span data-ttu-id="f2474-144">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="f2474-144">Message schema</span></span>  <br/> |
|<span data-ttu-id="f2474-145">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="f2474-145">Validation File</span></span>  <br/> |<span data-ttu-id="f2474-146">messages. xsd</span><span class="sxs-lookup"><span data-stu-id="f2474-146">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="f2474-147">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="f2474-147">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="f2474-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="f2474-148">See also</span></span>



- [<span data-ttu-id="f2474-149">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="f2474-149">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

