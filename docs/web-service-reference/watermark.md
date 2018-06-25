---
title: Marca de agua
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Watermark
api_type:
- schema
ms.assetid: e1545046-94f9-4ac7-af1c-ea81dfb6822c
description: El elemento de marca de agua representa un marcador de evento en la cola de eventos de buzón de correo.
ms.openlocfilehash: 1867aa781bc24f5eb3bdb4648fa494a2a7ea396a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19840975"
---
# <a name="watermark"></a><span data-ttu-id="133dc-103">Marca de agua</span><span class="sxs-lookup"><span data-stu-id="133dc-103">Watermark</span></span>

<span data-ttu-id="133dc-104">El elemento de **marca de agua** representa un marcador de evento en la cola de eventos de buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="133dc-104">The **Watermark** element represents an event bookmark in the mailbox event queue.</span></span> 
  
```xml
<Watermark/>
```

 <span data-ttu-id="133dc-105">**WatermarkType**</span><span class="sxs-lookup"><span data-stu-id="133dc-105">**WatermarkType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="133dc-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="133dc-106">Attributes and elements</span></span>

<span data-ttu-id="133dc-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="133dc-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="133dc-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="133dc-108">Attributes</span></span>

<span data-ttu-id="133dc-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="133dc-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="133dc-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="133dc-110">Child elements</span></span>

<span data-ttu-id="133dc-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="133dc-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="133dc-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="133dc-112">Parent elements</span></span>

|<span data-ttu-id="133dc-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="133dc-113">**Element**</span></span>|<span data-ttu-id="133dc-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="133dc-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="133dc-115">PullSubscriptionRequest</span><span class="sxs-lookup"><span data-stu-id="133dc-115">PullSubscriptionRequest</span></span>](pullsubscriptionrequest.md) <br/> |<span data-ttu-id="133dc-116">Representa una suscripción a una suscripción de notificación de eventos basado en la extracción.</span><span class="sxs-lookup"><span data-stu-id="133dc-116">Represents a subscription to a pull-based event notification subscription.</span></span>  <br/> |
|[<span data-ttu-id="133dc-117">PushSubscriptionRequest</span><span class="sxs-lookup"><span data-stu-id="133dc-117">PushSubscriptionRequest</span></span>](pushsubscriptionrequest.md) <br/> |<span data-ttu-id="133dc-118">Representa una suscripción a una suscripción de notificación de evento basada en inserción.</span><span class="sxs-lookup"><span data-stu-id="133dc-118">Represents a subscription to a push-based event notification subscription.</span></span>  <br/> |
|[<span data-ttu-id="133dc-119">GetEvents</span><span class="sxs-lookup"><span data-stu-id="133dc-119">GetEvents</span></span>](getevents.md) <br/> |<span data-ttu-id="133dc-120">Representa la operación usada por los clientes de extracción para las notificaciones de solicitud desde el servidor.</span><span class="sxs-lookup"><span data-stu-id="133dc-120">Represents the operation used by pull clients to request notifications from the server.</span></span>  <br/> |
|[<span data-ttu-id="133dc-121">CopiedEvent</span><span class="sxs-lookup"><span data-stu-id="133dc-121">CopiedEvent</span></span>](copiedevent.md) <br/> |<span data-ttu-id="133dc-122">Representa un evento donde se copia una carpeta o elemento.</span><span class="sxs-lookup"><span data-stu-id="133dc-122">Represents an event where an item or folder is copied.</span></span>  <br/> |
|[<span data-ttu-id="133dc-123">CreatedEvent</span><span class="sxs-lookup"><span data-stu-id="133dc-123">CreatedEvent</span></span>](createdevent.md) <br/> |<span data-ttu-id="133dc-124">Representa un evento que se crea una carpeta o elemento.</span><span class="sxs-lookup"><span data-stu-id="133dc-124">Represents an event where an item or folder is created.</span></span>  <br/> |
|[<span data-ttu-id="133dc-125">DeletedEvent</span><span class="sxs-lookup"><span data-stu-id="133dc-125">DeletedEvent</span></span>](deletedevent.md) <br/> |<span data-ttu-id="133dc-126">Representa un evento que se elimina un elemento o carpeta.</span><span class="sxs-lookup"><span data-stu-id="133dc-126">Represents an event where an item or folder is deleted.</span></span>  <br/> |
|[<span data-ttu-id="133dc-127">ModifiedEvent</span><span class="sxs-lookup"><span data-stu-id="133dc-127">ModifiedEvent</span></span>](modifiedevent.md) <br/> |<span data-ttu-id="133dc-128">Representa un evento que se modifica una carpeta o elemento.</span><span class="sxs-lookup"><span data-stu-id="133dc-128">Represents an event where an item or folder is modified.</span></span>  <br/> |
|[<span data-ttu-id="133dc-129">MovedEvent</span><span class="sxs-lookup"><span data-stu-id="133dc-129">MovedEvent</span></span>](movedevent.md) <br/> |<span data-ttu-id="133dc-130">Representa un evento donde una carpeta o elemento se mueve desde la carpeta principal de una a otra carpeta primaria.</span><span class="sxs-lookup"><span data-stu-id="133dc-130">Represents an event where an item or folder is moved from one parent folder to another parent folder.</span></span>  <br/> |
|[<span data-ttu-id="133dc-131">NewMailEvent</span><span class="sxs-lookup"><span data-stu-id="133dc-131">NewMailEvent</span></span>](newmailevent.md) <br/> |<span data-ttu-id="133dc-132">Representa un evento activado por un nuevo elemento de correo en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="133dc-132">Represents an event triggered by a new mail item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="133dc-133">Objeto StatusEvent</span><span class="sxs-lookup"><span data-stu-id="133dc-133">StatusEvent</span></span>](statusevent.md) <br/> |<span data-ttu-id="133dc-134">Representa una notificación que no se ha producido ninguna actividad de nuevo en el buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="133dc-134">Represents a notification that no new activity has occurred in the mailbox.</span></span>  <br/> |
|[<span data-ttu-id="133dc-135">SubscribeResponseMessage</span><span class="sxs-lookup"><span data-stu-id="133dc-135">SubscribeResponseMessage</span></span>](subscriberesponsemessage.md) <br/> |<span data-ttu-id="133dc-136">Contiene el estado y el resultado de una solicitud Subscribe.</span><span class="sxs-lookup"><span data-stu-id="133dc-136">Contains the status and result of a Subscribe request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="133dc-137">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="133dc-137">Text value</span></span>

<span data-ttu-id="133dc-138">Un valor de texto puede ser obligatorio u opcional dependiendo de cómo se usa este elemento.</span><span class="sxs-lookup"><span data-stu-id="133dc-138">A text value may be required or optional depending on how this element is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="133dc-139">Comentarios</span><span class="sxs-lookup"><span data-stu-id="133dc-139">Remarks</span></span>

<span data-ttu-id="133dc-140">Si una solicitud Subscribe contiene una marca de agua, se crea la suscripción de la marca de agua.</span><span class="sxs-lookup"><span data-stu-id="133dc-140">If a Subscribe request contains a watermark, the subscription is created from the watermark forward.</span></span> <span data-ttu-id="133dc-141">Si la solicitud Subscribe contiene una marca de agua que no se encuentra en la tabla de eventos de buzón de correo, un `ErrorInvalidWatermark` error se devuelve a la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="133dc-141">If the Subscribe request contains a watermark that is not found in the mailbox events table, an  `ErrorInvalidWatermark` error is returned to the client application.</span></span> <span data-ttu-id="133dc-142">Esto puede ocurrir si la marca de agua es demasiado antigua y se ha quitado de la ventana de 30 días de la tabla de eventos o si la marca de agua no fue nunca presentes en la tabla eventos.</span><span class="sxs-lookup"><span data-stu-id="133dc-142">This may occur if the watermark is too old and has been removed from the 30 day window of the events table or if the watermark was not ever present in the events table.</span></span> <span data-ttu-id="133dc-143">Esto puede suceder, por ejemplo, si se obtiene una marca de agua de una suscripción a diferente para un buzón de correo en una base de datos diferente.</span><span class="sxs-lookup"><span data-stu-id="133dc-143">This can happen, for example, if a watermark is obtained from a different subscription for a mailbox in a different database.</span></span> 
  
<span data-ttu-id="133dc-144">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="133dc-144">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="133dc-145">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="133dc-145">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="133dc-146">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="133dc-146">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="133dc-147">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="133dc-147">Schema name</span></span>  <br/> |<span data-ttu-id="133dc-148">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="133dc-148">Types schema</span></span>  <br/> |
|<span data-ttu-id="133dc-149">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="133dc-149">Validation file</span></span>  <br/> |<span data-ttu-id="133dc-150">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="133dc-150">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="133dc-151">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="133dc-151">Can be empty</span></span>  <br/> |<span data-ttu-id="133dc-152">False</span><span class="sxs-lookup"><span data-stu-id="133dc-152">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="133dc-153">Vea también</span><span class="sxs-lookup"><span data-stu-id="133dc-153">See also</span></span>



[<span data-ttu-id="133dc-154">Operación de suscripción</span><span class="sxs-lookup"><span data-stu-id="133dc-154">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="133dc-155">Operación GetEvents</span><span class="sxs-lookup"><span data-stu-id="133dc-155">GetEvents operation</span></span>](getevents-operation.md)
  
[<span data-ttu-id="133dc-156">Cancelar la operación de suscripción</span><span class="sxs-lookup"><span data-stu-id="133dc-156">Unsubscribe operation</span></span>](unsubscribe-operation.md)

