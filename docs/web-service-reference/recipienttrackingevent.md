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
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836989"
---
# <a name="recipienttrackingevent"></a><span data-ttu-id="00417-103">RecipientTrackingEvent</span><span class="sxs-lookup"><span data-stu-id="00417-103">RecipientTrackingEvent</span></span>

<span data-ttu-id="00417-104">El elemento **RecipientTrackingEvent** contiene información de un solo evento de un destinatario.</span><span class="sxs-lookup"><span data-stu-id="00417-104">The **RecipientTrackingEvent** element contains information for a single event for a recipient.</span></span> 
  
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

 <span data-ttu-id="00417-105">**RecipientTrackingEventType**</span><span class="sxs-lookup"><span data-stu-id="00417-105">**RecipientTrackingEventType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="00417-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="00417-106">Attributes and elements</span></span>

<span data-ttu-id="00417-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="00417-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="00417-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="00417-108">Attributes</span></span>

<span data-ttu-id="00417-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="00417-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="00417-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="00417-110">Child elements</span></span>

|<span data-ttu-id="00417-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="00417-111">**Element**</span></span>|<span data-ttu-id="00417-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="00417-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="00417-113">Fecha (MessageTracking)</span><span class="sxs-lookup"><span data-stu-id="00417-113">Date (MessageTracking)</span></span>](date-messagetracking.md) <br/> |<span data-ttu-id="00417-114">Se requiere este elemento.</span><span class="sxs-lookup"><span data-stu-id="00417-114">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="00417-115">Recipient</span><span class="sxs-lookup"><span data-stu-id="00417-115">Recipient</span></span>](recipient.md) <br/> |<span data-ttu-id="00417-116">Se requiere este elemento.</span><span class="sxs-lookup"><span data-stu-id="00417-116">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="00417-117">DeliveryStatus</span><span class="sxs-lookup"><span data-stu-id="00417-117">DeliveryStatus</span></span>](deliverystatus.md) <br/> |<span data-ttu-id="00417-118">Se requiere este elemento.</span><span class="sxs-lookup"><span data-stu-id="00417-118">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="00417-119">EventDescription</span><span class="sxs-lookup"><span data-stu-id="00417-119">EventDescription</span></span>](eventdescription.md) <br/> |<span data-ttu-id="00417-120">Se requiere este elemento.</span><span class="sxs-lookup"><span data-stu-id="00417-120">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="00417-121">EventData</span><span class="sxs-lookup"><span data-stu-id="00417-121">EventData</span></span>](eventdata.md) <br/> |<span data-ttu-id="00417-122">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="00417-122">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="00417-123">Servidor (MessageTracking)</span><span class="sxs-lookup"><span data-stu-id="00417-123">Server (MessageTracking)</span></span>](server-messagetracking.md) <br/> |<span data-ttu-id="00417-124">Se requiere este elemento.</span><span class="sxs-lookup"><span data-stu-id="00417-124">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="00417-125">InternalId</span><span class="sxs-lookup"><span data-stu-id="00417-125">InternalId</span></span>](internalid.md) <br/> |<span data-ttu-id="00417-126">Se requiere este elemento.</span><span class="sxs-lookup"><span data-stu-id="00417-126">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="00417-127">BccRecipient</span><span class="sxs-lookup"><span data-stu-id="00417-127">BccRecipient</span></span>](bccrecipient.md) <br/> |<span data-ttu-id="00417-128">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="00417-128">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="00417-129">HiddenRecipient</span><span class="sxs-lookup"><span data-stu-id="00417-129">HiddenRecipient</span></span>](hiddenrecipient.md) <br/> |<span data-ttu-id="00417-130">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="00417-130">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="00417-131">UniquePathId</span><span class="sxs-lookup"><span data-stu-id="00417-131">UniquePathId</span></span>](uniquepathid.md) <br/> |<span data-ttu-id="00417-132">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="00417-132">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="00417-133">RootAddress</span><span class="sxs-lookup"><span data-stu-id="00417-133">RootAddress</span></span>](rootaddress.md) <br/> |<span data-ttu-id="00417-134">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="00417-134">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="00417-135">Propiedades (ArrayOfTrackingPropertiesType)</span><span class="sxs-lookup"><span data-stu-id="00417-135">Properties (ArrayOfTrackingPropertiesType)</span></span>](properties-arrayoftrackingpropertiestype.md) <br/> |<span data-ttu-id="00417-136">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="00417-136">This element is optional.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="00417-137">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="00417-137">Parent elements</span></span>

|<span data-ttu-id="00417-138">**Element**</span><span class="sxs-lookup"><span data-stu-id="00417-138">**Element**</span></span>|<span data-ttu-id="00417-139">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="00417-139">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="00417-140">RecipientTrackingEvents</span><span class="sxs-lookup"><span data-stu-id="00417-140">RecipientTrackingEvents</span></span>](recipienttrackingevents.md) <br/> |<span data-ttu-id="00417-141">Contiene una lista de uno o más eventos de seguimiento para un destinatario.</span><span class="sxs-lookup"><span data-stu-id="00417-141">Contains a list of one or more tracking events for a recipient.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="00417-142">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="00417-142">Text value</span></span>

<span data-ttu-id="00417-143">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="00417-143">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="00417-144">Observaciones</span><span class="sxs-lookup"><span data-stu-id="00417-144">Remarks</span></span>

<span data-ttu-id="00417-145">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="00417-145">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="00417-146">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="00417-146">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="00417-147">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="00417-147">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="00417-148">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="00417-148">Schema Name</span></span>  <br/> |<span data-ttu-id="00417-149">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="00417-149">Types schema</span></span>  <br/> |
|<span data-ttu-id="00417-150">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="00417-150">Validation File</span></span>  <br/> |<span data-ttu-id="00417-151">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="00417-151">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="00417-152">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="00417-152">Can be Empty</span></span>  <br/> |<span data-ttu-id="00417-153">False</span><span class="sxs-lookup"><span data-stu-id="00417-153">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="00417-154">Ver también</span><span class="sxs-lookup"><span data-stu-id="00417-154">See also</span></span>



[<span data-ttu-id="00417-155">Operación GetMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="00417-155">GetMessageTrackingReport operation</span></span>](getmessagetrackingreport-operation.md)


- [<span data-ttu-id="00417-156">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="00417-156">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

