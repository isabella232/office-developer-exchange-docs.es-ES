---
title: Notificación
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Notification
api_type:
- schema
ms.assetid: c9070936-0930-438e-839c-91127256a6c8
description: El elemento Notification contiene información sobre la suscripción y los eventos que se han producido desde la última notificación.
ms.openlocfilehash: c4a5206c14985ec46cf40162a9ce4eaec68242ff
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530390"
---
# <a name="notification"></a><span data-ttu-id="2fa6c-103">Notificación</span><span class="sxs-lookup"><span data-stu-id="2fa6c-103">Notification</span></span>

<span data-ttu-id="2fa6c-104">El elemento **Notification** contiene información sobre la suscripción y los eventos que se han producido desde la última notificación.</span><span class="sxs-lookup"><span data-stu-id="2fa6c-104">The **Notification** element contains information about the subscription and the events that have occurred since the last notification.</span></span> 
  
```xml
<Notification>
   <SubscriptionId/>
   <PreviousWatermark/>
   <MoreEvents/>
   <CopiedEvent/>
</Notification>
```

```xml
<Notification>
   <SubscriptionId/>
   <PreviousWatermark/>
   <MoreEvents/>
   <CreatedEvent/>
</Notification>
```

```xml
<Notification>
   <SubscriptionId/>
   <PreviousWatermark/>
   <MoreEvents/>
   <DeletedEvent/>
</Notification>
```

```xml
<Notification>
   <SubscriptionId/>
   <PreviousWatermark/>
   <MoreEvents/>
   <ModifiedEvent/>
</Notification>
```

```xml
<Notification>
   <SubscriptionId/>
   <PreviousWatermark/>
   <MoreEvents/>
   <MovedEvent/>
</Notification>
```

```xml
<Notification>
   <SubscriptionId/>
   <PreviousWatermark/>
   <MoreEvents/>
   <NewMailEvent/>
</Notification>
```

```xml
<Notification>
   <SubscriptionId/>
   <PreviousWatermark/>
   <MoreEvents/>
   <StatusEvent/>
</Notification>
```

```xml
<Notification>
   <SubscriptionId/>
   <PreviousWatermark/>
   <MoreEvents/>
   <FreeBusyChangedEvent/>
</Notification>
```

<span data-ttu-id="2fa6c-105">**NotificationType**</span><span class="sxs-lookup"><span data-stu-id="2fa6c-105">**NotificationType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="2fa6c-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="2fa6c-106">Attributes and elements</span></span>

<span data-ttu-id="2fa6c-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="2fa6c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2fa6c-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="2fa6c-108">Attributes</span></span>

<span data-ttu-id="2fa6c-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="2fa6c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2fa6c-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="2fa6c-110">Child elements</span></span>

|<span data-ttu-id="2fa6c-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="2fa6c-111">**Element**</span></span>|<span data-ttu-id="2fa6c-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2fa6c-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2fa6c-113">SubscriptionId (GetEvents)</span><span class="sxs-lookup"><span data-stu-id="2fa6c-113">SubscriptionId (GetEvents)</span></span>](subscriptionid-getevents.md) <br/> |<span data-ttu-id="2fa6c-114">Representa el identificador de una suscripción.</span><span class="sxs-lookup"><span data-stu-id="2fa6c-114">Represents the identifier for a subscription.</span></span>  <br/> |
|[<span data-ttu-id="2fa6c-115">PreviousWatermark</span><span class="sxs-lookup"><span data-stu-id="2fa6c-115">PreviousWatermark</span></span>](previouswatermark.md) <br/> |<span data-ttu-id="2fa6c-116">Representa la marca de agua del último evento que se comunicó correctamente al cliente para la suscripción.</span><span class="sxs-lookup"><span data-stu-id="2fa6c-116">Represents the watermark of the latest event that was successfully communicated to the client for the subscription.</span></span>  <br/> |
|[<span data-ttu-id="2fa6c-117">MoreEvents</span><span class="sxs-lookup"><span data-stu-id="2fa6c-117">MoreEvents</span></span>](moreevents.md) <br/> |<span data-ttu-id="2fa6c-118">Indica si hay más eventos en la cola que se entreguen al cliente.</span><span class="sxs-lookup"><span data-stu-id="2fa6c-118">Indicates whether there are more events in the queue to be delivered to the client.</span></span>  <br/> |
|[<span data-ttu-id="2fa6c-119">CopiedEvent</span><span class="sxs-lookup"><span data-stu-id="2fa6c-119">CopiedEvent</span></span>](copiedevent.md) <br/> |<span data-ttu-id="2fa6c-120">Representa un evento en el que se copia un elemento o una carpeta.</span><span class="sxs-lookup"><span data-stu-id="2fa6c-120">Represents an event in which an item or folder is copied.</span></span>  <br/> |
|[<span data-ttu-id="2fa6c-121">CreatedEvent</span><span class="sxs-lookup"><span data-stu-id="2fa6c-121">CreatedEvent</span></span>](createdevent.md) <br/> |<span data-ttu-id="2fa6c-122">Representa un evento en el que se crea un elemento o una carpeta.</span><span class="sxs-lookup"><span data-stu-id="2fa6c-122">Represents an event in which an item or folder is created.</span></span>  <br/> |
|[<span data-ttu-id="2fa6c-123">DeletedEvent</span><span class="sxs-lookup"><span data-stu-id="2fa6c-123">DeletedEvent</span></span>](deletedevent.md) <br/> |<span data-ttu-id="2fa6c-124">Representa un evento en el que se elimina un elemento o una carpeta.</span><span class="sxs-lookup"><span data-stu-id="2fa6c-124">Represents an event in which an item or folder is deleted.</span></span>  <br/> |
|[<span data-ttu-id="2fa6c-125">ModifiedEvent</span><span class="sxs-lookup"><span data-stu-id="2fa6c-125">ModifiedEvent</span></span>](modifiedevent.md) <br/> |<span data-ttu-id="2fa6c-126">Representa un evento en el que se modifica un elemento o una carpeta.</span><span class="sxs-lookup"><span data-stu-id="2fa6c-126">Represents an event in which an item or folder is modified.</span></span>  <br/> |
|[<span data-ttu-id="2fa6c-127">MovedEvent</span><span class="sxs-lookup"><span data-stu-id="2fa6c-127">MovedEvent</span></span>](movedevent.md) <br/> |<span data-ttu-id="2fa6c-128">Representa un evento en el que se mueve un elemento o una carpeta de una carpeta principal a otra carpeta principal.</span><span class="sxs-lookup"><span data-stu-id="2fa6c-128">Represents an event in which an item or folder is moved from one parent folder to another parent folder.</span></span>  <br/> |
|[<span data-ttu-id="2fa6c-129">NewMailEvent</span><span class="sxs-lookup"><span data-stu-id="2fa6c-129">NewMailEvent</span></span>](newmailevent.md) <br/> |<span data-ttu-id="2fa6c-130">Representa un evento desencadenado por un nuevo elemento de correo en un buzón.</span><span class="sxs-lookup"><span data-stu-id="2fa6c-130">Represents an event that is triggered by a new mail item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="2fa6c-131">StatusEvent</span><span class="sxs-lookup"><span data-stu-id="2fa6c-131">StatusEvent</span></span>](statusevent.md) <br/> |<span data-ttu-id="2fa6c-132">Representa una notificación de que no se ha producido ninguna actividad nueva en el buzón.</span><span class="sxs-lookup"><span data-stu-id="2fa6c-132">Represents a notification that no new activity has occurred in the mailbox.</span></span>  <br/> |
|[<span data-ttu-id="2fa6c-133">FreeBusyChangedEvent</span><span class="sxs-lookup"><span data-stu-id="2fa6c-133">FreeBusyChangedEvent</span></span>](freebusychangedevent.md) <br/> |<span data-ttu-id="2fa6c-134">Representa un evento en el que ha cambiado la hora de disponibilidad de un elemento.</span><span class="sxs-lookup"><span data-stu-id="2fa6c-134">Represents an event in which an item's free/busy time has changed.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="2fa6c-135">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="2fa6c-135">Parent elements</span></span>

|<span data-ttu-id="2fa6c-136">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="2fa6c-136">**Element**</span></span>|<span data-ttu-id="2fa6c-137">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2fa6c-137">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2fa6c-138">GetEventsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="2fa6c-138">GetEventsResponseMessage</span></span>](geteventsresponsemessage.md) <br/> |<span data-ttu-id="2fa6c-139">Contiene el estado y el resultado de una sola solicitud GetEvents.</span><span class="sxs-lookup"><span data-stu-id="2fa6c-139">Contains the status and result of a single GetEvents request.</span></span>  <br/> |
|[<span data-ttu-id="2fa6c-140">SendNotificationResponseMessage</span><span class="sxs-lookup"><span data-stu-id="2fa6c-140">SendNotificationResponseMessage</span></span>](sendnotificationresponsemessage.md) <br/> |<span data-ttu-id="2fa6c-141">Contiene el estado y el resultado de una sola solicitud SendNotification.</span><span class="sxs-lookup"><span data-stu-id="2fa6c-141">Contains the status and result of a single SendNotification request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="2fa6c-142">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="2fa6c-142">Text value</span></span>

<span data-ttu-id="2fa6c-143">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="2fa6c-143">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2fa6c-144">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2fa6c-144">Remarks</span></span>

<span data-ttu-id="2fa6c-145">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="2fa6c-145">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2fa6c-146">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="2fa6c-146">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2fa6c-147">Namespace</span><span class="sxs-lookup"><span data-stu-id="2fa6c-147">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="2fa6c-148">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="2fa6c-148">Schema Name</span></span>  <br/> |<span data-ttu-id="2fa6c-149">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="2fa6c-149">Types schema</span></span>  <br/> |
|<span data-ttu-id="2fa6c-150">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="2fa6c-150">Validation File</span></span>  <br/> |<span data-ttu-id="2fa6c-151">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="2fa6c-151">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="2fa6c-152">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="2fa6c-152">Can be Empty</span></span>  <br/> |<span data-ttu-id="2fa6c-153">Falso</span><span class="sxs-lookup"><span data-stu-id="2fa6c-153">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2fa6c-154">Vea también</span><span class="sxs-lookup"><span data-stu-id="2fa6c-154">See also</span></span>

- [<span data-ttu-id="2fa6c-155">Operación subscribe</span><span class="sxs-lookup"><span data-stu-id="2fa6c-155">Subscribe operation</span></span>](subscribe-operation.md) 
- [<span data-ttu-id="2fa6c-156">Operación GetEvents</span><span class="sxs-lookup"><span data-stu-id="2fa6c-156">GetEvents operation</span></span>](getevents-operation.md) 
- [<span data-ttu-id="2fa6c-157">Operación GetStreamingEvents</span><span class="sxs-lookup"><span data-stu-id="2fa6c-157">GetStreamingEvents operation</span></span>](getstreamingevents-operation.md) 
- [<span data-ttu-id="2fa6c-158">Operación unsubscribe</span><span class="sxs-lookup"><span data-stu-id="2fa6c-158">Unsubscribe operation</span></span>](unsubscribe-operation.md)

