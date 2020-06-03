---
title: Watermark
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
description: El elemento marca de agua representa un marcador de evento en la cola de eventos del buzón.
ms.openlocfilehash: a717196101fea698b0b8c66f92a3d420fda9a421
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459766"
---
# <a name="watermark"></a><span data-ttu-id="98468-103">Watermark</span><span class="sxs-lookup"><span data-stu-id="98468-103">Watermark</span></span>

<span data-ttu-id="98468-104">El elemento **marca de agua** representa un marcador de evento en la cola de eventos del buzón.</span><span class="sxs-lookup"><span data-stu-id="98468-104">The **Watermark** element represents an event bookmark in the mailbox event queue.</span></span> 
  
```xml
<Watermark/>
```

 <span data-ttu-id="98468-105">**WatermarkType**</span><span class="sxs-lookup"><span data-stu-id="98468-105">**WatermarkType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="98468-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="98468-106">Attributes and elements</span></span>

<span data-ttu-id="98468-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="98468-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="98468-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="98468-108">Attributes</span></span>

<span data-ttu-id="98468-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="98468-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="98468-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="98468-110">Child elements</span></span>

<span data-ttu-id="98468-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="98468-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="98468-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="98468-112">Parent elements</span></span>

|<span data-ttu-id="98468-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="98468-113">**Element**</span></span>|<span data-ttu-id="98468-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="98468-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="98468-115">PullSubscriptionRequest</span><span class="sxs-lookup"><span data-stu-id="98468-115">PullSubscriptionRequest</span></span>](pullsubscriptionrequest.md) <br/> |<span data-ttu-id="98468-116">Representa una suscripción a una suscripción de notificación de eventos basada en extracción.</span><span class="sxs-lookup"><span data-stu-id="98468-116">Represents a subscription to a pull-based event notification subscription.</span></span>  <br/> |
|[<span data-ttu-id="98468-117">PushSubscriptionRequest</span><span class="sxs-lookup"><span data-stu-id="98468-117">PushSubscriptionRequest</span></span>](pushsubscriptionrequest.md) <br/> |<span data-ttu-id="98468-118">Representa una suscripción a una suscripción de notificación de eventos basada en inserción.</span><span class="sxs-lookup"><span data-stu-id="98468-118">Represents a subscription to a push-based event notification subscription.</span></span>  <br/> |
|[<span data-ttu-id="98468-119">GetEvents</span><span class="sxs-lookup"><span data-stu-id="98468-119">GetEvents</span></span>](getevents.md) <br/> |<span data-ttu-id="98468-120">Representa la operación usada por los clientes de extracción para solicitar notificaciones del servidor.</span><span class="sxs-lookup"><span data-stu-id="98468-120">Represents the operation used by pull clients to request notifications from the server.</span></span>  <br/> |
|[<span data-ttu-id="98468-121">CopiedEvent</span><span class="sxs-lookup"><span data-stu-id="98468-121">CopiedEvent</span></span>](copiedevent.md) <br/> |<span data-ttu-id="98468-122">Representa un evento en el que se copia un elemento o una carpeta.</span><span class="sxs-lookup"><span data-stu-id="98468-122">Represents an event where an item or folder is copied.</span></span>  <br/> |
|[<span data-ttu-id="98468-123">CreatedEvent</span><span class="sxs-lookup"><span data-stu-id="98468-123">CreatedEvent</span></span>](createdevent.md) <br/> |<span data-ttu-id="98468-124">Representa un evento en el que se crea un elemento o una carpeta.</span><span class="sxs-lookup"><span data-stu-id="98468-124">Represents an event where an item or folder is created.</span></span>  <br/> |
|[<span data-ttu-id="98468-125">DeletedEvent</span><span class="sxs-lookup"><span data-stu-id="98468-125">DeletedEvent</span></span>](deletedevent.md) <br/> |<span data-ttu-id="98468-126">Representa un evento en el que se elimina un elemento o carpeta.</span><span class="sxs-lookup"><span data-stu-id="98468-126">Represents an event where an item or folder is deleted.</span></span>  <br/> |
|[<span data-ttu-id="98468-127">ModifiedEvent</span><span class="sxs-lookup"><span data-stu-id="98468-127">ModifiedEvent</span></span>](modifiedevent.md) <br/> |<span data-ttu-id="98468-128">Representa un evento en el que se modifica un elemento o una carpeta.</span><span class="sxs-lookup"><span data-stu-id="98468-128">Represents an event where an item or folder is modified.</span></span>  <br/> |
|[<span data-ttu-id="98468-129">MovedEvent</span><span class="sxs-lookup"><span data-stu-id="98468-129">MovedEvent</span></span>](movedevent.md) <br/> |<span data-ttu-id="98468-130">Representa un evento en el que se mueve un elemento o una carpeta de una carpeta principal a otra carpeta principal.</span><span class="sxs-lookup"><span data-stu-id="98468-130">Represents an event where an item or folder is moved from one parent folder to another parent folder.</span></span>  <br/> |
|[<span data-ttu-id="98468-131">NewMailEvent</span><span class="sxs-lookup"><span data-stu-id="98468-131">NewMailEvent</span></span>](newmailevent.md) <br/> |<span data-ttu-id="98468-132">Representa un evento desencadenado por un nuevo elemento de correo en un buzón.</span><span class="sxs-lookup"><span data-stu-id="98468-132">Represents an event triggered by a new mail item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="98468-133">StatusEvent</span><span class="sxs-lookup"><span data-stu-id="98468-133">StatusEvent</span></span>](statusevent.md) <br/> |<span data-ttu-id="98468-134">Representa una notificación de que no se ha producido ninguna actividad nueva en el buzón.</span><span class="sxs-lookup"><span data-stu-id="98468-134">Represents a notification that no new activity has occurred in the mailbox.</span></span>  <br/> |
|[<span data-ttu-id="98468-135">SubscribeResponseMessage</span><span class="sxs-lookup"><span data-stu-id="98468-135">SubscribeResponseMessage</span></span>](subscriberesponsemessage.md) <br/> |<span data-ttu-id="98468-136">Contiene el estado y el resultado de una solicitud subscribe.</span><span class="sxs-lookup"><span data-stu-id="98468-136">Contains the status and result of a Subscribe request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="98468-137">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="98468-137">Text value</span></span>

<span data-ttu-id="98468-138">Un valor de texto puede ser obligatorio u opcional en función de cómo se use este elemento.</span><span class="sxs-lookup"><span data-stu-id="98468-138">A text value may be required or optional depending on how this element is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="98468-139">Comentarios</span><span class="sxs-lookup"><span data-stu-id="98468-139">Remarks</span></span>

<span data-ttu-id="98468-140">Si una solicitud de suscripción contiene una marca de agua, la suscripción se crea desde la marca de agua hacia delante.</span><span class="sxs-lookup"><span data-stu-id="98468-140">If a Subscribe request contains a watermark, the subscription is created from the watermark forward.</span></span> <span data-ttu-id="98468-141">Si la solicitud de suscripción contiene una marca de agua que no se encuentra en la tabla de eventos del buzón de correo, `ErrorInvalidWatermark` se devuelve un error a la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="98468-141">If the Subscribe request contains a watermark that is not found in the mailbox events table, an  `ErrorInvalidWatermark` error is returned to the client application.</span></span> <span data-ttu-id="98468-142">Esto puede ocurrir si la marca de agua es demasiado antigua y se ha quitado de la ventana de 30 días de la tabla eventos o si la marca de agua no se ha puesto en alguna ocasión en la tabla eventos.</span><span class="sxs-lookup"><span data-stu-id="98468-142">This may occur if the watermark is too old and has been removed from the 30 day window of the events table or if the watermark was not ever present in the events table.</span></span> <span data-ttu-id="98468-143">Esto puede ocurrir, por ejemplo, si se obtiene una marca de agua de una suscripción diferente para un buzón de una base de datos diferente.</span><span class="sxs-lookup"><span data-stu-id="98468-143">This can happen, for example, if a watermark is obtained from a different subscription for a mailbox in a different database.</span></span> 
  
<span data-ttu-id="98468-144">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="98468-144">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="98468-145">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="98468-145">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="98468-146">Namespace</span><span class="sxs-lookup"><span data-stu-id="98468-146">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="98468-147">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="98468-147">Schema name</span></span>  <br/> |<span data-ttu-id="98468-148">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="98468-148">Types schema</span></span>  <br/> |
|<span data-ttu-id="98468-149">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="98468-149">Validation file</span></span>  <br/> |<span data-ttu-id="98468-150">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="98468-150">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="98468-151">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="98468-151">Can be empty</span></span>  <br/> |<span data-ttu-id="98468-152">Falso</span><span class="sxs-lookup"><span data-stu-id="98468-152">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="98468-153">Vea también</span><span class="sxs-lookup"><span data-stu-id="98468-153">See also</span></span>



[<span data-ttu-id="98468-154">Operación subscribe</span><span class="sxs-lookup"><span data-stu-id="98468-154">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="98468-155">Operación GetEvents</span><span class="sxs-lookup"><span data-stu-id="98468-155">GetEvents operation</span></span>](getevents-operation.md)
  
[<span data-ttu-id="98468-156">Operación unsubscribe</span><span class="sxs-lookup"><span data-stu-id="98468-156">Unsubscribe operation</span></span>](unsubscribe-operation.md)

