---
title: EventTypes
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
ms.openlocfilehash: 7ea783dc0bf73abf992616b1f86c7621c5b36fc8
ms.sourcegitcommit: 25cbbc6707e4ec0621c5c46baf7fe49be42d3297
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/07/2018
ms.locfileid: "25440840"
---
# <a name="eventtypes"></a><span data-ttu-id="afbff-103">EventTypes</span><span class="sxs-lookup"><span data-stu-id="afbff-103">EventTypes</span></span>

<span data-ttu-id="afbff-104">El elemento **debe establecer** contiene una colección de tipos de notificación de evento que se usan para crear una suscripción.</span><span class="sxs-lookup"><span data-stu-id="afbff-104">The **EventTypes** element contains a collection of event notification types that are used to create a subscription.</span></span> 
  
```xml
<EventTypes>
   <EventType/>
</EventTypes>
```

 <span data-ttu-id="afbff-105">**NonEmptyArrayOfNotificationEventTypesType**</span><span class="sxs-lookup"><span data-stu-id="afbff-105">**NonEmptyArrayOfNotificationEventTypesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="afbff-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="afbff-106">Attributes and elements</span></span>

<span data-ttu-id="afbff-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="afbff-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="afbff-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="afbff-108">Attributes</span></span>

<span data-ttu-id="afbff-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="afbff-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="afbff-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="afbff-110">Child elements</span></span>

|<span data-ttu-id="afbff-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="afbff-111">**Element**</span></span>|<span data-ttu-id="afbff-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="afbff-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="afbff-113">EventType</span><span class="sxs-lookup"><span data-stu-id="afbff-113">EventType</span></span>](eventtype.md) <br/> |<span data-ttu-id="afbff-114">Representa un tipo de notificación de evento solicitado que se usa para crear una suscripción.</span><span class="sxs-lookup"><span data-stu-id="afbff-114">Represents a requested event notification type that is used to create a subscription.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="afbff-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="afbff-115">Parent elements</span></span>

|<span data-ttu-id="afbff-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="afbff-116">**Element**</span></span>|<span data-ttu-id="afbff-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="afbff-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="afbff-118">PullSubscriptionRequest</span><span class="sxs-lookup"><span data-stu-id="afbff-118">PullSubscriptionRequest</span></span>](pullsubscriptionrequest.md) <br/> |<span data-ttu-id="afbff-119">Representa una suscripción a una suscripción de notificación de eventos basado en la extracción.</span><span class="sxs-lookup"><span data-stu-id="afbff-119">Represents a subscription to a pull-based event notification subscription.</span></span>  <br/> |
|[<span data-ttu-id="afbff-120">PushSubscriptionRequest</span><span class="sxs-lookup"><span data-stu-id="afbff-120">PushSubscriptionRequest</span></span>](pushsubscriptionrequest.md) <br/> |<span data-ttu-id="afbff-121">Representa una suscripción a una suscripción de notificación de evento basada en inserción.</span><span class="sxs-lookup"><span data-stu-id="afbff-121">Represents a subscription to a push-based event notification subscription.</span></span>  <br/> |
|[<span data-ttu-id="afbff-122">StreamingSubscriptionRequest</span><span class="sxs-lookup"><span data-stu-id="afbff-122">StreamingSubscriptionRequest</span></span>](streamingsubscriptionrequest.md) <br/> |<span data-ttu-id="afbff-123">Representa una suscripción a una suscripción de notificación de evento transmisión por secuencias.</span><span class="sxs-lookup"><span data-stu-id="afbff-123">Represents a subscription to a streaming event notification subscription.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="afbff-124">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="afbff-124">Text value</span></span>

<span data-ttu-id="afbff-125">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="afbff-125">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="afbff-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="afbff-126">Remarks</span></span>

<span data-ttu-id="afbff-127">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="afbff-127">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="afbff-128">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="afbff-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="afbff-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="afbff-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="afbff-130">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="afbff-130">Schema Name</span></span>  <br/> |<span data-ttu-id="afbff-131">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="afbff-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="afbff-132">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="afbff-132">Validation File</span></span>  <br/> |<span data-ttu-id="afbff-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="afbff-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="afbff-134">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="afbff-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="afbff-135">False</span><span class="sxs-lookup"><span data-stu-id="afbff-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="afbff-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="afbff-136">See also</span></span>



[<span data-ttu-id="afbff-137">Operación Subscribe</span><span class="sxs-lookup"><span data-stu-id="afbff-137">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="afbff-138">Operación GetEvents</span><span class="sxs-lookup"><span data-stu-id="afbff-138">GetEvents operation</span></span>](getevents-operation.md)
  
[<span data-ttu-id="afbff-139">Operación GetStreamingEvents</span><span class="sxs-lookup"><span data-stu-id="afbff-139">GetStreamingEvents operation</span></span>](getstreamingevents-operation.md)
  
[<span data-ttu-id="afbff-140">Operación Unsubscribe</span><span class="sxs-lookup"><span data-stu-id="afbff-140">Unsubscribe operation</span></span>](unsubscribe-operation.md)

