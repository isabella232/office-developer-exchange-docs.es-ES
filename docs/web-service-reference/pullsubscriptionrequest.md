---
title: PullSubscriptionRequest
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PullSubscriptionRequest
api_type:
- schema
ms.assetid: 145c5cc7-a894-4f0b-a6ea-358cddfb5c33
description: El elemento PullSubscriptionRequest representa una suscripción a una suscripción de notificación de eventos basada en extracción.
ms.openlocfilehash: fb9712c9e1481678c2821ee344052783d5c25bf9
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468869"
---
# <a name="pullsubscriptionrequest"></a><span data-ttu-id="5cfc3-103">PullSubscriptionRequest</span><span class="sxs-lookup"><span data-stu-id="5cfc3-103">PullSubscriptionRequest</span></span>

<span data-ttu-id="5cfc3-104">El elemento **PullSubscriptionRequest** representa una suscripción a una suscripción de notificación de eventos basada en extracción.</span><span class="sxs-lookup"><span data-stu-id="5cfc3-104">The **PullSubscriptionRequest** element represents a subscription to a pull-based event notification subscription.</span></span> 
  
[<span data-ttu-id="5cfc3-105">Suscribirse</span><span class="sxs-lookup"><span data-stu-id="5cfc3-105">Subscribe</span></span>](subscribe.md)
  
[<span data-ttu-id="5cfc3-106">PullSubscriptionRequest</span><span class="sxs-lookup"><span data-stu-id="5cfc3-106">PullSubscriptionRequest</span></span>](pullsubscriptionrequest.md)
  
```XML
<PullSubscriptionRequest SubscribeToAllFolders="">
   <FolderIds/>
   <EventTypes/>
   <Watermark/>
   <Timeout/>
</PullSubscriptionRequest>
```

 <span data-ttu-id="5cfc3-107">**PullSubscriptionRequestType**</span><span class="sxs-lookup"><span data-stu-id="5cfc3-107">**PullSubscriptionRequestType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="5cfc3-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="5cfc3-108">Attributes and elements</span></span>

<span data-ttu-id="5cfc3-109">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="5cfc3-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5cfc3-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="5cfc3-110">Attributes</span></span>

|<span data-ttu-id="5cfc3-111">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="5cfc3-111">**Attribute**</span></span>|<span data-ttu-id="5cfc3-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5cfc3-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5cfc3-113">**SubscribeToAllFolders**</span><span class="sxs-lookup"><span data-stu-id="5cfc3-113">**SubscribeToAllFolders**</span></span> <br/> |<span data-ttu-id="5cfc3-114">Indica si se va a suscribir a todas las carpetas disponibles.</span><span class="sxs-lookup"><span data-stu-id="5cfc3-114">Indicates whether to subscribe to all available folders.</span></span> <span data-ttu-id="5cfc3-115">Este atributo es opcional.</span><span class="sxs-lookup"><span data-stu-id="5cfc3-115">This attribute is optional.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="5cfc3-116">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="5cfc3-116">Child elements</span></span>

|<span data-ttu-id="5cfc3-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="5cfc3-117">**Element**</span></span>|<span data-ttu-id="5cfc3-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5cfc3-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5cfc3-119">FolderIds</span><span class="sxs-lookup"><span data-stu-id="5cfc3-119">FolderIds</span></span>](folderids.md) <br/> |<span data-ttu-id="5cfc3-120">Contiene una matriz de identificadores de carpeta que se usan para identificar las carpetas que se van a supervisar para las notificaciones de eventos.</span><span class="sxs-lookup"><span data-stu-id="5cfc3-120">Contains an array of folder identifiers that are used to identify folders to monitor for event notifications.</span></span>  <br/> |
|[<span data-ttu-id="5cfc3-121">EventTypes</span><span class="sxs-lookup"><span data-stu-id="5cfc3-121">EventTypes</span></span>](eventtypes.md) <br/> |<span data-ttu-id="5cfc3-122">Contiene una colección de notificaciones de eventos que se usan para crear una suscripción.</span><span class="sxs-lookup"><span data-stu-id="5cfc3-122">Contains a collection of event notifications that are used to create a subscription.</span></span>  <br/> |
|[<span data-ttu-id="5cfc3-123">Watermark</span><span class="sxs-lookup"><span data-stu-id="5cfc3-123">Watermark</span></span>](watermark.md) <br/> |<span data-ttu-id="5cfc3-124">Representa un marcador de evento en la tabla de eventos del buzón.</span><span class="sxs-lookup"><span data-stu-id="5cfc3-124">Represents an event bookmark in the mailbox events table.</span></span> <span data-ttu-id="5cfc3-125">Se usa para crear una suscripción que comienza en un evento que está representado por la marca de agua.</span><span class="sxs-lookup"><span data-stu-id="5cfc3-125">This is used to create a subscription that starts at an event that is represented by the watermark.</span></span> <span data-ttu-id="5cfc3-126">Si no se encuentra la marca de agua de una solicitud de suscripción, se devolverá una respuesta de error al cliente.</span><span class="sxs-lookup"><span data-stu-id="5cfc3-126">If the watermark from a Subscribe request is not found, an error response will be returned to the client.</span></span> <span data-ttu-id="5cfc3-127">Este error puede producirse si la marca de agua es superior a 30 días o si la marca de agua nunca estaba presente en el buzón.</span><span class="sxs-lookup"><span data-stu-id="5cfc3-127">This error may occur if the watermark is older than 30 days or if the watermark was never present in the mailbox.</span></span>  <br/> |
|[<span data-ttu-id="5cfc3-128">Timeout</span><span class="sxs-lookup"><span data-stu-id="5cfc3-128">Timeout</span></span>](timeout.md) <br/> |<span data-ttu-id="5cfc3-129">Representa la duración, en minutos, que la suscripción puede permanecer inactiva sin una solicitud GetEvents del cliente.</span><span class="sxs-lookup"><span data-stu-id="5cfc3-129">Represents the duration, in minutes, that the subscription can remain idle without a GetEvents request from the client.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="5cfc3-130">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="5cfc3-130">Parent elements</span></span>

|<span data-ttu-id="5cfc3-131">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="5cfc3-131">**Element**</span></span>|<span data-ttu-id="5cfc3-132">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5cfc3-132">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5cfc3-133">Suscribirse</span><span class="sxs-lookup"><span data-stu-id="5cfc3-133">Subscribe</span></span>](subscribe.md) <br/> |<span data-ttu-id="5cfc3-134">Contiene las propiedades que se usan para crear suscripciones.</span><span class="sxs-lookup"><span data-stu-id="5cfc3-134">Contains the properties that are used to create subscriptions.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="5cfc3-135">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="5cfc3-135">Text value</span></span>

<span data-ttu-id="5cfc3-136">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="5cfc3-136">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5cfc3-137">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5cfc3-137">Remarks</span></span>

<span data-ttu-id="5cfc3-138">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="5cfc3-138">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5cfc3-139">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="5cfc3-139">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5cfc3-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="5cfc3-140">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="5cfc3-141">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="5cfc3-141">Schema name</span></span>  <br/> |<span data-ttu-id="5cfc3-142">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="5cfc3-142">Messages schema</span></span>  <br/> |
|<span data-ttu-id="5cfc3-143">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="5cfc3-143">Validation file</span></span>  <br/> |<span data-ttu-id="5cfc3-144">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="5cfc3-144">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="5cfc3-145">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="5cfc3-145">Can be empty</span></span>  <br/> |<span data-ttu-id="5cfc3-146">Falso</span><span class="sxs-lookup"><span data-stu-id="5cfc3-146">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5cfc3-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="5cfc3-147">See also</span></span>



[<span data-ttu-id="5cfc3-148">PushSubscriptionRequest</span><span class="sxs-lookup"><span data-stu-id="5cfc3-148">PushSubscriptionRequest</span></span>](pushsubscriptionrequest.md)
  
[<span data-ttu-id="5cfc3-149">Operación subscribe</span><span class="sxs-lookup"><span data-stu-id="5cfc3-149">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="5cfc3-150">Operación GetEvents</span><span class="sxs-lookup"><span data-stu-id="5cfc3-150">GetEvents operation</span></span>](getevents-operation.md)
  
[<span data-ttu-id="5cfc3-151">Operación unsubscribe</span><span class="sxs-lookup"><span data-stu-id="5cfc3-151">Unsubscribe operation</span></span>](unsubscribe-operation.md)


- [<span data-ttu-id="5cfc3-152">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="5cfc3-152">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

