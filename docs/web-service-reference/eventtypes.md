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
description: El elemento EventTypes contiene una colección de tipos de notificación de eventos que se usan para crear una suscripción.
ms.openlocfilehash: 45ce1ed0699c8140029ae3fb7f667a5132f4731e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530631"
---
# <a name="eventtypes"></a><span data-ttu-id="35c52-103">EventTypes</span><span class="sxs-lookup"><span data-stu-id="35c52-103">EventTypes</span></span>

<span data-ttu-id="35c52-104">El elemento **EventTypes** contiene una colección de tipos de notificación de eventos que se usan para crear una suscripción.</span><span class="sxs-lookup"><span data-stu-id="35c52-104">The **EventTypes** element contains a collection of event notification types that are used to create a subscription.</span></span> 
  
```xml
<EventTypes>
   <EventType/>
</EventTypes>
```

 <span data-ttu-id="35c52-105">**NonEmptyArrayOfNotificationEventTypesType**</span><span class="sxs-lookup"><span data-stu-id="35c52-105">**NonEmptyArrayOfNotificationEventTypesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="35c52-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="35c52-106">Attributes and elements</span></span>

<span data-ttu-id="35c52-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="35c52-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="35c52-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="35c52-108">Attributes</span></span>

<span data-ttu-id="35c52-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="35c52-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="35c52-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="35c52-110">Child elements</span></span>

|<span data-ttu-id="35c52-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="35c52-111">**Element**</span></span>|<span data-ttu-id="35c52-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="35c52-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="35c52-113">EventType</span><span class="sxs-lookup"><span data-stu-id="35c52-113">EventType</span></span>](eventtype.md) <br/> |<span data-ttu-id="35c52-114">Representa un tipo de notificación de eventos solicitado que se usa para crear una suscripción.</span><span class="sxs-lookup"><span data-stu-id="35c52-114">Represents a requested event notification type that is used to create a subscription.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="35c52-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="35c52-115">Parent elements</span></span>

|<span data-ttu-id="35c52-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="35c52-116">**Element**</span></span>|<span data-ttu-id="35c52-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="35c52-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="35c52-118">PullSubscriptionRequest</span><span class="sxs-lookup"><span data-stu-id="35c52-118">PullSubscriptionRequest</span></span>](pullsubscriptionrequest.md) <br/> |<span data-ttu-id="35c52-119">Representa una suscripción a una suscripción de notificación de eventos basada en extracción.</span><span class="sxs-lookup"><span data-stu-id="35c52-119">Represents a subscription to a pull-based event notification subscription.</span></span>  <br/> |
|[<span data-ttu-id="35c52-120">PushSubscriptionRequest</span><span class="sxs-lookup"><span data-stu-id="35c52-120">PushSubscriptionRequest</span></span>](pushsubscriptionrequest.md) <br/> |<span data-ttu-id="35c52-121">Representa una suscripción a una suscripción de notificación de eventos basada en inserción.</span><span class="sxs-lookup"><span data-stu-id="35c52-121">Represents a subscription to a push-based event notification subscription.</span></span>  <br/> |
|[<span data-ttu-id="35c52-122">StreamingSubscriptionRequest</span><span class="sxs-lookup"><span data-stu-id="35c52-122">StreamingSubscriptionRequest</span></span>](streamingsubscriptionrequest.md) <br/> |<span data-ttu-id="35c52-123">Representa una suscripción a una suscripción de notificación de eventos de transmisión por secuencias.</span><span class="sxs-lookup"><span data-stu-id="35c52-123">Represents a subscription to a streaming event notification subscription.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="35c52-124">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="35c52-124">Text value</span></span>

<span data-ttu-id="35c52-125">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="35c52-125">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="35c52-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="35c52-126">Remarks</span></span>

<span data-ttu-id="35c52-127">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="35c52-127">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="35c52-128">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="35c52-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="35c52-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="35c52-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="35c52-130">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="35c52-130">Schema Name</span></span>  <br/> |<span data-ttu-id="35c52-131">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="35c52-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="35c52-132">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="35c52-132">Validation File</span></span>  <br/> |<span data-ttu-id="35c52-133">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="35c52-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="35c52-134">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="35c52-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="35c52-135">Falso</span><span class="sxs-lookup"><span data-stu-id="35c52-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="35c52-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="35c52-136">See also</span></span>



[<span data-ttu-id="35c52-137">Operación subscribe</span><span class="sxs-lookup"><span data-stu-id="35c52-137">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="35c52-138">Operación GetEvents</span><span class="sxs-lookup"><span data-stu-id="35c52-138">GetEvents operation</span></span>](getevents-operation.md)
  
[<span data-ttu-id="35c52-139">Operación GetStreamingEvents</span><span class="sxs-lookup"><span data-stu-id="35c52-139">GetStreamingEvents operation</span></span>](getstreamingevents-operation.md)
  
[<span data-ttu-id="35c52-140">Operación unsubscribe</span><span class="sxs-lookup"><span data-stu-id="35c52-140">Unsubscribe operation</span></span>](unsubscribe-operation.md)

