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
description: El elemento RecipientTrackingEvent contiene información de un evento único para un destinatario.
ms.openlocfilehash: e9a014cdfac122f112205cfa5032535a770f9d82
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465488"
---
# <a name="recipienttrackingevent"></a><span data-ttu-id="faace-103">RecipientTrackingEvent</span><span class="sxs-lookup"><span data-stu-id="faace-103">RecipientTrackingEvent</span></span>

<span data-ttu-id="faace-104">El elemento **RecipientTrackingEvent** contiene información de un evento único para un destinatario.</span><span class="sxs-lookup"><span data-stu-id="faace-104">The **RecipientTrackingEvent** element contains information for a single event for a recipient.</span></span> 
  
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

 <span data-ttu-id="faace-105">**RecipientTrackingEventType**</span><span class="sxs-lookup"><span data-stu-id="faace-105">**RecipientTrackingEventType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="faace-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="faace-106">Attributes and elements</span></span>

<span data-ttu-id="faace-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="faace-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="faace-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="faace-108">Attributes</span></span>

<span data-ttu-id="faace-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="faace-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="faace-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="faace-110">Child elements</span></span>

|<span data-ttu-id="faace-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="faace-111">**Element**</span></span>|<span data-ttu-id="faace-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="faace-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="faace-113">Fecha (MessageTracking)</span><span class="sxs-lookup"><span data-stu-id="faace-113">Date (MessageTracking)</span></span>](date-messagetracking.md) <br/> |<span data-ttu-id="faace-114">Se requiere este elemento.</span><span class="sxs-lookup"><span data-stu-id="faace-114">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="faace-115">Destinatario</span><span class="sxs-lookup"><span data-stu-id="faace-115">Recipient</span></span>](recipient.md) <br/> |<span data-ttu-id="faace-116">Se requiere este elemento.</span><span class="sxs-lookup"><span data-stu-id="faace-116">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="faace-117">DeliveryStatus</span><span class="sxs-lookup"><span data-stu-id="faace-117">DeliveryStatus</span></span>](deliverystatus.md) <br/> |<span data-ttu-id="faace-118">Se requiere este elemento.</span><span class="sxs-lookup"><span data-stu-id="faace-118">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="faace-119">EventDescription</span><span class="sxs-lookup"><span data-stu-id="faace-119">EventDescription</span></span>](eventdescription.md) <br/> |<span data-ttu-id="faace-120">Se requiere este elemento.</span><span class="sxs-lookup"><span data-stu-id="faace-120">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="faace-121">EventData</span><span class="sxs-lookup"><span data-stu-id="faace-121">EventData</span></span>](eventdata.md) <br/> |<span data-ttu-id="faace-122">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="faace-122">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="faace-123">Servidor (MessageTracking)</span><span class="sxs-lookup"><span data-stu-id="faace-123">Server (MessageTracking)</span></span>](server-messagetracking.md) <br/> |<span data-ttu-id="faace-124">Se requiere este elemento.</span><span class="sxs-lookup"><span data-stu-id="faace-124">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="faace-125">InternalId</span><span class="sxs-lookup"><span data-stu-id="faace-125">InternalId</span></span>](internalid.md) <br/> |<span data-ttu-id="faace-126">Se requiere este elemento.</span><span class="sxs-lookup"><span data-stu-id="faace-126">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="faace-127">BccRecipient</span><span class="sxs-lookup"><span data-stu-id="faace-127">BccRecipient</span></span>](bccrecipient.md) <br/> |<span data-ttu-id="faace-128">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="faace-128">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="faace-129">HiddenRecipient</span><span class="sxs-lookup"><span data-stu-id="faace-129">HiddenRecipient</span></span>](hiddenrecipient.md) <br/> |<span data-ttu-id="faace-130">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="faace-130">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="faace-131">UniquePathId</span><span class="sxs-lookup"><span data-stu-id="faace-131">UniquePathId</span></span>](uniquepathid.md) <br/> |<span data-ttu-id="faace-132">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="faace-132">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="faace-133">RootAddress</span><span class="sxs-lookup"><span data-stu-id="faace-133">RootAddress</span></span>](rootaddress.md) <br/> |<span data-ttu-id="faace-134">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="faace-134">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="faace-135">Propiedades (ArrayOfTrackingPropertiesType)</span><span class="sxs-lookup"><span data-stu-id="faace-135">Properties (ArrayOfTrackingPropertiesType)</span></span>](properties-arrayoftrackingpropertiestype.md) <br/> |<span data-ttu-id="faace-136">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="faace-136">This element is optional.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="faace-137">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="faace-137">Parent elements</span></span>

|<span data-ttu-id="faace-138">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="faace-138">**Element**</span></span>|<span data-ttu-id="faace-139">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="faace-139">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="faace-140">RecipientTrackingEvents</span><span class="sxs-lookup"><span data-stu-id="faace-140">RecipientTrackingEvents</span></span>](recipienttrackingevents.md) <br/> |<span data-ttu-id="faace-141">Contiene una lista de uno o más eventos de seguimiento de un destinatario.</span><span class="sxs-lookup"><span data-stu-id="faace-141">Contains a list of one or more tracking events for a recipient.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="faace-142">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="faace-142">Text value</span></span>

<span data-ttu-id="faace-143">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="faace-143">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="faace-144">Comentarios</span><span class="sxs-lookup"><span data-stu-id="faace-144">Remarks</span></span>

<span data-ttu-id="faace-145">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="faace-145">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="faace-146">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="faace-146">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="faace-147">Namespace</span><span class="sxs-lookup"><span data-stu-id="faace-147">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="faace-148">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="faace-148">Schema Name</span></span>  <br/> |<span data-ttu-id="faace-149">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="faace-149">Types schema</span></span>  <br/> |
|<span data-ttu-id="faace-150">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="faace-150">Validation File</span></span>  <br/> |<span data-ttu-id="faace-151">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="faace-151">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="faace-152">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="faace-152">Can be Empty</span></span>  <br/> |<span data-ttu-id="faace-153">Falso</span><span class="sxs-lookup"><span data-stu-id="faace-153">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="faace-154">Vea también</span><span class="sxs-lookup"><span data-stu-id="faace-154">See also</span></span>



[<span data-ttu-id="faace-155">Operación GetMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="faace-155">GetMessageTrackingReport operation</span></span>](getmessagetrackingreport-operation.md)


- [<span data-ttu-id="faace-156">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="faace-156">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

