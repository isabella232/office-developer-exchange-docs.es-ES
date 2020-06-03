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
description: El elemento subscribe contiene las propiedades que se usan para crear suscripciones.
ms.openlocfilehash: f60e67654fb6af76e8081036a3463f5be401862d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530961"
---
# <a name="subscribe"></a><span data-ttu-id="871f4-103">Suscribirse</span><span class="sxs-lookup"><span data-stu-id="871f4-103">Subscribe</span></span>

<span data-ttu-id="871f4-104">El elemento **subscribe** contiene las propiedades que se usan para crear suscripciones.</span><span class="sxs-lookup"><span data-stu-id="871f4-104">The **Subscribe** element contains the properties used to create subscriptions.</span></span> 
  
```XML
<Subscribe>
   <PullSubscriptionRequest/>
   <PushSubscriptionRequest/>
   <StreamingSubscriptionRequest/>
</Subscribe>
```

 <span data-ttu-id="871f4-105">**SubscribeType**</span><span class="sxs-lookup"><span data-stu-id="871f4-105">**SubscribeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="871f4-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="871f4-106">Attributes and elements</span></span>

<span data-ttu-id="871f4-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="871f4-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="871f4-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="871f4-108">Attributes</span></span>

<span data-ttu-id="871f4-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="871f4-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="871f4-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="871f4-110">Child elements</span></span>

|<span data-ttu-id="871f4-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="871f4-111">**Element**</span></span>|<span data-ttu-id="871f4-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="871f4-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="871f4-113">PullSubscriptionRequest</span><span class="sxs-lookup"><span data-stu-id="871f4-113">PullSubscriptionRequest</span></span>](pullsubscriptionrequest.md) <br/> |<span data-ttu-id="871f4-114">Representa una suscripción a una notificación de evento basada en extracción.</span><span class="sxs-lookup"><span data-stu-id="871f4-114">Represents a subscription to a pull-based event notification.</span></span>  <br/> |
|[<span data-ttu-id="871f4-115">PushSubscriptionRequest</span><span class="sxs-lookup"><span data-stu-id="871f4-115">PushSubscriptionRequest</span></span>](pushsubscriptionrequest.md) <br/> |<span data-ttu-id="871f4-116">Representa una suscripción a una notificación de evento basada en inserción.</span><span class="sxs-lookup"><span data-stu-id="871f4-116">Represents a subscription to a push-based event notification.</span></span>  <br/> |
|[<span data-ttu-id="871f4-117">StreamingSubscriptionRequest</span><span class="sxs-lookup"><span data-stu-id="871f4-117">StreamingSubscriptionRequest</span></span>](streamingsubscriptionrequest.md) <br/> |<span data-ttu-id="871f4-118">Representa una suscripción a una notificación de eventos de transmisión por secuencias.</span><span class="sxs-lookup"><span data-stu-id="871f4-118">Represents a subscription to a streaming event notification.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="871f4-119">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="871f4-119">Parent elements</span></span>

<span data-ttu-id="871f4-120">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="871f4-120">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="871f4-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="871f4-121">Remarks</span></span>

<span data-ttu-id="871f4-122">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="871f4-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="871f4-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="871f4-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="871f4-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="871f4-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="871f4-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="871f4-125">Schema name</span></span>  <br/> |<span data-ttu-id="871f4-126">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="871f4-126">Messages schema</span></span>  <br/> |
|<span data-ttu-id="871f4-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="871f4-127">Validation file</span></span>  <br/> |<span data-ttu-id="871f4-128">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="871f4-128">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="871f4-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="871f4-129">Can be empty</span></span>  <br/> |<span data-ttu-id="871f4-130">Falso</span><span class="sxs-lookup"><span data-stu-id="871f4-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="871f4-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="871f4-131">See also</span></span>



[<span data-ttu-id="871f4-132">Operación subscribe</span><span class="sxs-lookup"><span data-stu-id="871f4-132">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="871f4-133">Operación GetEvents</span><span class="sxs-lookup"><span data-stu-id="871f4-133">GetEvents operation</span></span>](getevents-operation.md)
  
[<span data-ttu-id="871f4-134">Operación GetStreamingEvents</span><span class="sxs-lookup"><span data-stu-id="871f4-134">GetStreamingEvents operation</span></span>](getstreamingevents-operation.md)
  
[<span data-ttu-id="871f4-135">Operación unsubscribe</span><span class="sxs-lookup"><span data-stu-id="871f4-135">Unsubscribe operation</span></span>](unsubscribe-operation.md)

