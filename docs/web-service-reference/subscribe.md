---
title: Suscribirse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Subscribe
api_type:
- schema
ms.assetid: 6c2ee57d-e216-4a94-92db-faa3cb0e244a
description: El elemento de Subscribe contiene las propiedades usadas para crear las suscripciones.
ms.openlocfilehash: 9f23f566f9105c655b289ed9b434c5e7b917207f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19837618"
---
# <a name="subscribe"></a><span data-ttu-id="86bc8-103">Suscribirse</span><span class="sxs-lookup"><span data-stu-id="86bc8-103">Subscribe</span></span>

<span data-ttu-id="86bc8-104">El elemento de **Subscribe** contiene las propiedades usadas para crear las suscripciones.</span><span class="sxs-lookup"><span data-stu-id="86bc8-104">The **Subscribe** element contains the properties used to create subscriptions.</span></span> 
  
```XML
<Subscribe>
   <PullSubscriptionRequest/>
   <PushSubscriptionRequest/>
   <StreamingSubscriptionRequest/>
</Subscribe>
```

 <span data-ttu-id="86bc8-105">**SubscribeType**</span><span class="sxs-lookup"><span data-stu-id="86bc8-105">**SubscribeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="86bc8-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="86bc8-106">Attributes and elements</span></span>

<span data-ttu-id="86bc8-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="86bc8-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="86bc8-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="86bc8-108">Attributes</span></span>

<span data-ttu-id="86bc8-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="86bc8-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="86bc8-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="86bc8-110">Child elements</span></span>

|<span data-ttu-id="86bc8-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="86bc8-111">**Element**</span></span>|<span data-ttu-id="86bc8-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="86bc8-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="86bc8-113">PullSubscriptionRequest</span><span class="sxs-lookup"><span data-stu-id="86bc8-113">PullSubscriptionRequest</span></span>](pullsubscriptionrequest.md) <br/> |<span data-ttu-id="86bc8-114">Representa una suscripción a una notificación de eventos basado en la extracción.</span><span class="sxs-lookup"><span data-stu-id="86bc8-114">Represents a subscription to a pull-based event notification.</span></span>  <br/> |
|[<span data-ttu-id="86bc8-115">PushSubscriptionRequest</span><span class="sxs-lookup"><span data-stu-id="86bc8-115">PushSubscriptionRequest</span></span>](pushsubscriptionrequest.md) <br/> |<span data-ttu-id="86bc8-116">Representa una suscripción a una notificación de evento basada en inserción.</span><span class="sxs-lookup"><span data-stu-id="86bc8-116">Represents a subscription to a push-based event notification.</span></span>  <br/> |
|[<span data-ttu-id="86bc8-117">StreamingSubscriptionRequest</span><span class="sxs-lookup"><span data-stu-id="86bc8-117">StreamingSubscriptionRequest</span></span>](streamingsubscriptionrequest.md) <br/> |<span data-ttu-id="86bc8-118">Representa una suscripción a una notificación de evento de transmisión por secuencias.</span><span class="sxs-lookup"><span data-stu-id="86bc8-118">Represents a subscription to a streaming event notification.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="86bc8-119">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="86bc8-119">Parent elements</span></span>

<span data-ttu-id="86bc8-120">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="86bc8-120">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="86bc8-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="86bc8-121">Remarks</span></span>

<span data-ttu-id="86bc8-122">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="86bc8-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="86bc8-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="86bc8-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="86bc8-124">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="86bc8-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="86bc8-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="86bc8-125">Schema name</span></span>  <br/> |<span data-ttu-id="86bc8-126">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="86bc8-126">Messages schema</span></span>  <br/> |
|<span data-ttu-id="86bc8-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="86bc8-127">Validation file</span></span>  <br/> |<span data-ttu-id="86bc8-128">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="86bc8-128">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="86bc8-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="86bc8-129">Can be empty</span></span>  <br/> |<span data-ttu-id="86bc8-130">False</span><span class="sxs-lookup"><span data-stu-id="86bc8-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="86bc8-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="86bc8-131">See also</span></span>



[<span data-ttu-id="86bc8-132">Operación de suscripción</span><span class="sxs-lookup"><span data-stu-id="86bc8-132">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="86bc8-133">Operación GetEvents</span><span class="sxs-lookup"><span data-stu-id="86bc8-133">GetEvents operation</span></span>](getevents-operation.md)
  
[<span data-ttu-id="86bc8-134">Operación GetStreamingEvents</span><span class="sxs-lookup"><span data-stu-id="86bc8-134">GetStreamingEvents operation</span></span>](getstreamingevents-operation.md)
  
[<span data-ttu-id="86bc8-135">Cancelar la operación de suscripción</span><span class="sxs-lookup"><span data-stu-id="86bc8-135">Unsubscribe operation</span></span>](unsubscribe-operation.md)

