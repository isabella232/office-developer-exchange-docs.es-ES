---
title: RecipientTrackingEvent
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RecipientTrackingEvent
api_type:
- schema
ms.assetid: 2bffdac7-c2f5-4805-ae7e-bd865301acb6
description: El elemento RecipientTrackingEvent contiene información de un solo evento de un destinatario.
ms.openlocfilehash: c5488ba105f9a853a490d6f0f4ff9ff15b537e23
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836989"
---
# <a name="recipienttrackingevent"></a><span data-ttu-id="8da56-103">RecipientTrackingEvent</span><span class="sxs-lookup"><span data-stu-id="8da56-103">RecipientTrackingEvent</span></span>

<span data-ttu-id="8da56-104">El elemento **RecipientTrackingEvent** contiene información de un solo evento de un destinatario.</span><span class="sxs-lookup"><span data-stu-id="8da56-104">The **RecipientTrackingEvent** element contains information for a single event for a recipient.</span></span> 
  
```XML
<RecipientTrackingEvent>
   <Date/>
   <Recipient/>
   <DeliveryStatus/>
   <EventDescription/>
   <EventData/>
   <Server/>
   <InternalId/>
   <BccRecipient/>
   <HiddenRecipient/>
   <UniquePathId/>
   <RootAddress/>
   <Properties/>
</RecipientTrackingEvent>
```

 <span data-ttu-id="8da56-105">**RecipientTrackingEventType**</span><span class="sxs-lookup"><span data-stu-id="8da56-105">**RecipientTrackingEventType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="8da56-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="8da56-106">Attributes and elements</span></span>

<span data-ttu-id="8da56-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="8da56-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8da56-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="8da56-108">Attributes</span></span>

<span data-ttu-id="8da56-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="8da56-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="8da56-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="8da56-110">Child elements</span></span>

|<span data-ttu-id="8da56-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="8da56-111">**Element**</span></span>|<span data-ttu-id="8da56-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8da56-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8da56-113">Fecha (MessageTracking)</span><span class="sxs-lookup"><span data-stu-id="8da56-113">Date (MessageTracking)</span></span>](date-messagetracking.md) <br/> |<span data-ttu-id="8da56-114">Se requiere este elemento.</span><span class="sxs-lookup"><span data-stu-id="8da56-114">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="8da56-115">Recipient</span><span class="sxs-lookup"><span data-stu-id="8da56-115">Recipient</span></span>](recipient.md) <br/> |<span data-ttu-id="8da56-116">Se requiere este elemento.</span><span class="sxs-lookup"><span data-stu-id="8da56-116">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="8da56-117">DeliveryStatus</span><span class="sxs-lookup"><span data-stu-id="8da56-117">DeliveryStatus</span></span>](deliverystatus.md) <br/> |<span data-ttu-id="8da56-118">Se requiere este elemento.</span><span class="sxs-lookup"><span data-stu-id="8da56-118">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="8da56-119">EventDescription</span><span class="sxs-lookup"><span data-stu-id="8da56-119">EventDescription</span></span>](eventdescription.md) <br/> |<span data-ttu-id="8da56-120">Se requiere este elemento.</span><span class="sxs-lookup"><span data-stu-id="8da56-120">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="8da56-121">EventData</span><span class="sxs-lookup"><span data-stu-id="8da56-121">EventData</span></span>](eventdata.md) <br/> |<span data-ttu-id="8da56-122">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="8da56-122">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="8da56-123">Servidor (MessageTracking)</span><span class="sxs-lookup"><span data-stu-id="8da56-123">Server (MessageTracking)</span></span>](server-messagetracking.md) <br/> |<span data-ttu-id="8da56-124">Se requiere este elemento.</span><span class="sxs-lookup"><span data-stu-id="8da56-124">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="8da56-125">InternalId</span><span class="sxs-lookup"><span data-stu-id="8da56-125">InternalId</span></span>](internalid.md) <br/> |<span data-ttu-id="8da56-126">Se requiere este elemento.</span><span class="sxs-lookup"><span data-stu-id="8da56-126">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="8da56-127">BccRecipient</span><span class="sxs-lookup"><span data-stu-id="8da56-127">BccRecipient</span></span>](bccrecipient.md) <br/> |<span data-ttu-id="8da56-128">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="8da56-128">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="8da56-129">HiddenRecipient</span><span class="sxs-lookup"><span data-stu-id="8da56-129">HiddenRecipient</span></span>](hiddenrecipient.md) <br/> |<span data-ttu-id="8da56-130">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="8da56-130">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="8da56-131">UniquePathId</span><span class="sxs-lookup"><span data-stu-id="8da56-131">UniquePathId</span></span>](uniquepathid.md) <br/> |<span data-ttu-id="8da56-132">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="8da56-132">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="8da56-133">RootAddress</span><span class="sxs-lookup"><span data-stu-id="8da56-133">RootAddress</span></span>](rootaddress.md) <br/> |<span data-ttu-id="8da56-134">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="8da56-134">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="8da56-135">Propiedades (ArrayOfTrackingPropertiesType)</span><span class="sxs-lookup"><span data-stu-id="8da56-135">Properties (ArrayOfTrackingPropertiesType)</span></span>](properties-arrayoftrackingpropertiestype.md) <br/> |<span data-ttu-id="8da56-136">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="8da56-136">This element is optional.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="8da56-137">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="8da56-137">Parent elements</span></span>

|<span data-ttu-id="8da56-138">**Element**</span><span class="sxs-lookup"><span data-stu-id="8da56-138">**Element**</span></span>|<span data-ttu-id="8da56-139">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8da56-139">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8da56-140">RecipientTrackingEvents</span><span class="sxs-lookup"><span data-stu-id="8da56-140">RecipientTrackingEvents</span></span>](recipienttrackingevents.md) <br/> |<span data-ttu-id="8da56-141">Contiene una lista de uno o más eventos de seguimiento para un destinatario.</span><span class="sxs-lookup"><span data-stu-id="8da56-141">Contains a list of one or more tracking events for a recipient.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="8da56-142">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="8da56-142">Text value</span></span>

<span data-ttu-id="8da56-143">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="8da56-143">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8da56-144">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8da56-144">Remarks</span></span>

<span data-ttu-id="8da56-145">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="8da56-145">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8da56-146">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="8da56-146">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8da56-147">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="8da56-147">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="8da56-148">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="8da56-148">Schema Name</span></span>  <br/> |<span data-ttu-id="8da56-149">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="8da56-149">Types schema</span></span>  <br/> |
|<span data-ttu-id="8da56-150">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="8da56-150">Validation File</span></span>  <br/> |<span data-ttu-id="8da56-151">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="8da56-151">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="8da56-152">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="8da56-152">Can be Empty</span></span>  <br/> |<span data-ttu-id="8da56-153">False</span><span class="sxs-lookup"><span data-stu-id="8da56-153">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8da56-154">Vea también</span><span class="sxs-lookup"><span data-stu-id="8da56-154">See also</span></span>



[<span data-ttu-id="8da56-155">Operación GetMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="8da56-155">GetMessageTrackingReport operation</span></span>](getmessagetrackingreport-operation.md)


- [<span data-ttu-id="8da56-156">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="8da56-156">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

