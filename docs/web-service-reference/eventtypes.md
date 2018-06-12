---
title: Debe establecer
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- EventTypes
api_type:
- schema
ms.assetid: 29ded9e5-f191-4aa3-bc3e-500de2fc8818
description: El elemento debe establecer contiene una colección de tipos de notificación de evento que se usan para crear una suscripción.
ms.openlocfilehash: f4c622376f6b607ed390511d7bb5f0f723889420
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764454"
---
# <a name="eventtypes"></a><span data-ttu-id="e33f4-103">Debe establecer</span><span class="sxs-lookup"><span data-stu-id="e33f4-103">EventTypes</span></span>

<span data-ttu-id="e33f4-104">El elemento **debe establecer** contiene una colección de tipos de notificación de evento que se usan para crear una suscripción.</span><span class="sxs-lookup"><span data-stu-id="e33f4-104">The **EventTypes** element contains a collection of event notification types that are used to create a subscription.</span></span> 
  
```xml
<EventTypes>
   <EventType/>
</EventTypes>
```

 <span data-ttu-id="e33f4-105">**NonEmptyArrayOfNotificationEventTypesType**</span><span class="sxs-lookup"><span data-stu-id="e33f4-105">**NonEmptyArrayOfNotificationEventTypesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e33f4-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="e33f4-106">Attributes and elements</span></span>

<span data-ttu-id="e33f4-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="e33f4-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e33f4-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="e33f4-108">Attributes</span></span>

<span data-ttu-id="e33f4-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="e33f4-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e33f4-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="e33f4-110">Child elements</span></span>

|<span data-ttu-id="e33f4-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="e33f4-111">**Element**</span></span>|<span data-ttu-id="e33f4-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e33f4-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e33f4-113">EventType</span><span class="sxs-lookup"><span data-stu-id="e33f4-113">EventType</span></span>](eventtype.md) <br/> |<span data-ttu-id="e33f4-114">Representa un tipo de notificación de evento solicitado que se usa para crear una suscripción.</span><span class="sxs-lookup"><span data-stu-id="e33f4-114">Represents a requested event notification type that is used to create a subscription.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="e33f4-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="e33f4-115">Parent elements</span></span>

|<span data-ttu-id="e33f4-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="e33f4-116">**Element**</span></span>|<span data-ttu-id="e33f4-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e33f4-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e33f4-118">PullSubscriptionRequest</span><span class="sxs-lookup"><span data-stu-id="e33f4-118">PullSubscriptionRequest</span></span>](pullsubscriptionrequest.md) <br/> |<span data-ttu-id="e33f4-119">Representa una suscripción a una suscripción de notificación de eventos basado en la extracción.</span><span class="sxs-lookup"><span data-stu-id="e33f4-119">Represents a subscription to a pull-based event notification subscription.</span></span>  <br/> |
|[<span data-ttu-id="e33f4-120">PushSubscriptionRequest</span><span class="sxs-lookup"><span data-stu-id="e33f4-120">PushSubscriptionRequest</span></span>](pushsubscriptionrequest.md) <br/> |<span data-ttu-id="e33f4-121">Representa una suscripción a una suscripción de notificación de evento basada en inserción.</span><span class="sxs-lookup"><span data-stu-id="e33f4-121">Represents a subscription to a push-based event notification subscription.</span></span>  <br/> |
|[<span data-ttu-id="e33f4-122">StreamingSubscriptionRequest</span><span class="sxs-lookup"><span data-stu-id="e33f4-122">StreamingSubscriptionRequest</span></span>](streamingsubscriptionrequest.md) <br/> |<span data-ttu-id="e33f4-123">Representa una suscripción a una suscripción de notificación de evento transmisión por secuencias.</span><span class="sxs-lookup"><span data-stu-id="e33f4-123">Represents a subscription to a streaming event notification subscription.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="e33f4-124">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="e33f4-124">Text value</span></span>

<span data-ttu-id="e33f4-125">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="e33f4-125">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e33f4-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e33f4-126">Remarks</span></span>

<span data-ttu-id="e33f4-127">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="e33f4-127">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e33f4-128">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="e33f4-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e33f4-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e33f4-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="e33f4-130">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="e33f4-130">Schema Name</span></span>  <br/> |<span data-ttu-id="e33f4-131">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="e33f4-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="e33f4-132">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="e33f4-132">Validation File</span></span>  <br/> |<span data-ttu-id="e33f4-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="e33f4-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="e33f4-134">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="e33f4-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="e33f4-135">False</span><span class="sxs-lookup"><span data-stu-id="e33f4-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e33f4-136">Ver también</span><span class="sxs-lookup"><span data-stu-id="e33f4-136">See also</span></span>



[<span data-ttu-id="e33f4-137">Operación de suscripción</span><span class="sxs-lookup"><span data-stu-id="e33f4-137">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="e33f4-138">Operación GetEvents</span><span class="sxs-lookup"><span data-stu-id="e33f4-138">GetEvents operation</span></span>](getevents-operation.md)
  
[<span data-ttu-id="e33f4-139">Operación GetStreamingEvents</span><span class="sxs-lookup"><span data-stu-id="e33f4-139">GetStreamingEvents operation</span></span>](getstreamingevents-operation.md)
  
[<span data-ttu-id="e33f4-140">Cancelar la operación de suscripción</span><span class="sxs-lookup"><span data-stu-id="e33f4-140">Unsubscribe operation</span></span>](unsubscribe-operation.md)

