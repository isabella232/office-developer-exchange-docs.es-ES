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
description: El elemento PullSubscriptionRequest representa una suscripción a una suscripción de notificación de eventos basado en la extracción.
ms.openlocfilehash: 5f757bf1f79f7e2a00fb886db50e6ea0eaed1a4a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836932"
---
# <a name="pullsubscriptionrequest"></a><span data-ttu-id="ef5bb-103">PullSubscriptionRequest</span><span class="sxs-lookup"><span data-stu-id="ef5bb-103">PullSubscriptionRequest</span></span>

<span data-ttu-id="ef5bb-104">El elemento **PullSubscriptionRequest** representa una suscripción a una suscripción de notificación de eventos basado en la extracción.</span><span class="sxs-lookup"><span data-stu-id="ef5bb-104">The **PullSubscriptionRequest** element represents a subscription to a pull-based event notification subscription.</span></span> 
  
[<span data-ttu-id="ef5bb-105">Suscribirse</span><span class="sxs-lookup"><span data-stu-id="ef5bb-105">Subscribe</span></span>](subscribe.md)
  
[<span data-ttu-id="ef5bb-106">PullSubscriptionRequest</span><span class="sxs-lookup"><span data-stu-id="ef5bb-106">PullSubscriptionRequest</span></span>](pullsubscriptionrequest.md)
  
```XML
<PullSubscriptionRequest SubscribeToAllFolders="">
   <FolderIds/>
   <EventTypes/>
   <Watermark/>
   <Timeout/>
</PullSubscriptionRequest>
```

 <span data-ttu-id="ef5bb-107">**PullSubscriptionRequestType**</span><span class="sxs-lookup"><span data-stu-id="ef5bb-107">**PullSubscriptionRequestType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ef5bb-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="ef5bb-108">Attributes and elements</span></span>

<span data-ttu-id="ef5bb-109">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="ef5bb-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ef5bb-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="ef5bb-110">Attributes</span></span>

|<span data-ttu-id="ef5bb-111">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="ef5bb-111">**Attribute**</span></span>|<span data-ttu-id="ef5bb-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ef5bb-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ef5bb-113">**SubscribeToAllFolders**</span><span class="sxs-lookup"><span data-stu-id="ef5bb-113">**SubscribeToAllFolders**</span></span> <br/> |<span data-ttu-id="ef5bb-114">Indica si se debe suscribirse a todas las carpetas disponibles.</span><span class="sxs-lookup"><span data-stu-id="ef5bb-114">Indicates whether to subscribe to all available folders.</span></span> <span data-ttu-id="ef5bb-115">Este atributo es opcional.</span><span class="sxs-lookup"><span data-stu-id="ef5bb-115">This attribute is optional.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="ef5bb-116">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ef5bb-116">Child elements</span></span>

|<span data-ttu-id="ef5bb-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="ef5bb-117">**Element**</span></span>|<span data-ttu-id="ef5bb-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ef5bb-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ef5bb-119">FolderIds</span><span class="sxs-lookup"><span data-stu-id="ef5bb-119">FolderIds</span></span>](folderids.md) <br/> |<span data-ttu-id="ef5bb-120">Contiene una matriz de identificadores de carpeta que se usa para identificar las carpetas para supervisar las notificaciones de eventos.</span><span class="sxs-lookup"><span data-stu-id="ef5bb-120">Contains an array of folder identifiers that are used to identify folders to monitor for event notifications.</span></span>  <br/> |
|[<span data-ttu-id="ef5bb-121">Debe establecer</span><span class="sxs-lookup"><span data-stu-id="ef5bb-121">EventTypes</span></span>](eventtypes.md) <br/> |<span data-ttu-id="ef5bb-122">Contiene una colección de las notificaciones de eventos que se usan para crear una suscripción.</span><span class="sxs-lookup"><span data-stu-id="ef5bb-122">Contains a collection of event notifications that are used to create a subscription.</span></span>  <br/> |
|[<span data-ttu-id="ef5bb-123">Marca de agua</span><span class="sxs-lookup"><span data-stu-id="ef5bb-123">Watermark</span></span>](watermark.md) <br/> |<span data-ttu-id="ef5bb-124">Representa un marcador de evento en la tabla de eventos de buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="ef5bb-124">Represents an event bookmark in the mailbox events table.</span></span> <span data-ttu-id="ef5bb-125">Esto se usa para crear una suscripción que se inicia en un evento que está representado por la marca de agua.</span><span class="sxs-lookup"><span data-stu-id="ef5bb-125">This is used to create a subscription that starts at an event that is represented by the watermark.</span></span> <span data-ttu-id="ef5bb-126">Si no se encuentra la marca de agua de una solicitud Subscribe, se devolverá una respuesta de error al cliente.</span><span class="sxs-lookup"><span data-stu-id="ef5bb-126">If the watermark from a Subscribe request is not found, an error response will be returned to the client.</span></span> <span data-ttu-id="ef5bb-127">Este error puede producirse si la marca de agua es más antiguo que 30 días o si la marca de agua nunca estaba presente en el buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="ef5bb-127">This error may occur if the watermark is older than 30 days or if the watermark was never present in the mailbox.</span></span>  <br/> |
|[<span data-ttu-id="ef5bb-128">Timeout</span><span class="sxs-lookup"><span data-stu-id="ef5bb-128">Timeout</span></span>](timeout.md) <br/> |<span data-ttu-id="ef5bb-129">Representa la duración, en minutos, que puede permanecer inactiva sin una solicitud GetEvents desde el cliente de la suscripción.</span><span class="sxs-lookup"><span data-stu-id="ef5bb-129">Represents the duration, in minutes, that the subscription can remain idle without a GetEvents request from the client.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ef5bb-130">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="ef5bb-130">Parent elements</span></span>

|<span data-ttu-id="ef5bb-131">**Element**</span><span class="sxs-lookup"><span data-stu-id="ef5bb-131">**Element**</span></span>|<span data-ttu-id="ef5bb-132">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ef5bb-132">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ef5bb-133">Suscribirse</span><span class="sxs-lookup"><span data-stu-id="ef5bb-133">Subscribe</span></span>](subscribe.md) <br/> |<span data-ttu-id="ef5bb-134">Contiene las propiedades que se usan para crear las suscripciones.</span><span class="sxs-lookup"><span data-stu-id="ef5bb-134">Contains the properties that are used to create subscriptions.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="ef5bb-135">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="ef5bb-135">Text value</span></span>

<span data-ttu-id="ef5bb-136">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="ef5bb-136">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ef5bb-137">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ef5bb-137">Remarks</span></span>

<span data-ttu-id="ef5bb-138">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="ef5bb-138">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ef5bb-139">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="ef5bb-139">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ef5bb-140">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="ef5bb-140">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="ef5bb-141">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="ef5bb-141">Schema name</span></span>  <br/> |<span data-ttu-id="ef5bb-142">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="ef5bb-142">Messages schema</span></span>  <br/> |
|<span data-ttu-id="ef5bb-143">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="ef5bb-143">Validation file</span></span>  <br/> |<span data-ttu-id="ef5bb-144">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="ef5bb-144">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="ef5bb-145">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="ef5bb-145">Can be empty</span></span>  <br/> |<span data-ttu-id="ef5bb-146">False</span><span class="sxs-lookup"><span data-stu-id="ef5bb-146">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ef5bb-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="ef5bb-147">See also</span></span>



[<span data-ttu-id="ef5bb-148">PushSubscriptionRequest</span><span class="sxs-lookup"><span data-stu-id="ef5bb-148">PushSubscriptionRequest</span></span>](pushsubscriptionrequest.md)
  
[<span data-ttu-id="ef5bb-149">Operación de suscripción</span><span class="sxs-lookup"><span data-stu-id="ef5bb-149">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="ef5bb-150">Operación GetEvents</span><span class="sxs-lookup"><span data-stu-id="ef5bb-150">GetEvents operation</span></span>](getevents-operation.md)
  
[<span data-ttu-id="ef5bb-151">Cancelar la operación de suscripción</span><span class="sxs-lookup"><span data-stu-id="ef5bb-151">Unsubscribe operation</span></span>](unsubscribe-operation.md)


- [<span data-ttu-id="ef5bb-152">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="ef5bb-152">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

