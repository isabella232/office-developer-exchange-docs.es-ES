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
description: El elemento de notificación contiene información acerca de la suscripción y los eventos que se han producido desde la última notificación.
ms.openlocfilehash: a769d8988eb68d0fa0b02f3838cd891e714571b6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836547"
---
# <a name="notification"></a><span data-ttu-id="7c283-103">Notificación</span><span class="sxs-lookup"><span data-stu-id="7c283-103">Notification</span></span>

<span data-ttu-id="7c283-104">El elemento de **notificación** contiene información acerca de la suscripción y los eventos que se han producido desde la última notificación.</span><span class="sxs-lookup"><span data-stu-id="7c283-104">The **Notification** element contains information about the subscription and the events that have occurred since the last notification.</span></span> 
  
```xml
<Notification>
   <SubscriptionId/>
   <PreviousWatermark/>
   <MoreEvents/>
   <CopiedEvent/>
</Notification>
```

 <span data-ttu-id="7c283-105">**NotificationType**</span><span class="sxs-lookup"><span data-stu-id="7c283-105">**NotificationType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7c283-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="7c283-106">Attributes and elements</span></span>

<span data-ttu-id="7c283-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="7c283-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7c283-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="7c283-108">Attributes</span></span>

<span data-ttu-id="7c283-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="7c283-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7c283-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="7c283-110">Child elements</span></span>

|<span data-ttu-id="7c283-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="7c283-111">**Element**</span></span>|<span data-ttu-id="7c283-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7c283-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7c283-113">SubscriptionId (GetEvents)</span><span class="sxs-lookup"><span data-stu-id="7c283-113">SubscriptionId (GetEvents)</span></span>](subscriptionid-getevents.md) <br/> |<span data-ttu-id="7c283-114">Representa el identificador para una suscripción a.</span><span class="sxs-lookup"><span data-stu-id="7c283-114">Represents the identifier for a subscription.</span></span>  <br/> |
|[<span data-ttu-id="7c283-115">PreviousWatermark</span><span class="sxs-lookup"><span data-stu-id="7c283-115">PreviousWatermark</span></span>](previouswatermark.md) <br/> |<span data-ttu-id="7c283-116">Representa la marca de agua del evento más reciente que se ha comunicado correctamente al cliente para la suscripción.</span><span class="sxs-lookup"><span data-stu-id="7c283-116">Represents the watermark of the latest event that was successfully communicated to the client for the subscription.</span></span>  <br/> |
|[<span data-ttu-id="7c283-117">MoreEvents</span><span class="sxs-lookup"><span data-stu-id="7c283-117">MoreEvents</span></span>](moreevents.md) <br/> |<span data-ttu-id="7c283-118">Indica si hay más eventos en la cola para entregar al cliente.</span><span class="sxs-lookup"><span data-stu-id="7c283-118">Indicates whether there are more events in the queue to be delivered to the client.</span></span>  <br/> |
|[<span data-ttu-id="7c283-119">CopiedEvent</span><span class="sxs-lookup"><span data-stu-id="7c283-119">CopiedEvent</span></span>](copiedevent.md) <br/> |<span data-ttu-id="7c283-120">Representa un evento en el que se copia un elemento o carpeta.</span><span class="sxs-lookup"><span data-stu-id="7c283-120">Represents an event in which an item or folder is copied.</span></span>  <br/> |
|[<span data-ttu-id="7c283-121">CreatedEvent</span><span class="sxs-lookup"><span data-stu-id="7c283-121">CreatedEvent</span></span>](createdevent.md) <br/> |<span data-ttu-id="7c283-122">Representa un evento en el que se crea una carpeta o elemento.</span><span class="sxs-lookup"><span data-stu-id="7c283-122">Represents an event in which an item or folder is created.</span></span>  <br/> |
|[<span data-ttu-id="7c283-123">DeletedEvent</span><span class="sxs-lookup"><span data-stu-id="7c283-123">DeletedEvent</span></span>](deletedevent.md) <br/> |<span data-ttu-id="7c283-124">Representa un evento en el que se elimina un elemento o carpeta.</span><span class="sxs-lookup"><span data-stu-id="7c283-124">Represents an event in which an item or folder is deleted.</span></span>  <br/> |
|[<span data-ttu-id="7c283-125">ModifiedEvent</span><span class="sxs-lookup"><span data-stu-id="7c283-125">ModifiedEvent</span></span>](modifiedevent.md) <br/> |<span data-ttu-id="7c283-126">Representa un evento en el que se modifica una carpeta o elemento.</span><span class="sxs-lookup"><span data-stu-id="7c283-126">Represents an event in which an item or folder is modified.</span></span>  <br/> |
|[<span data-ttu-id="7c283-127">MovedEvent</span><span class="sxs-lookup"><span data-stu-id="7c283-127">MovedEvent</span></span>](movedevent.md) <br/> |<span data-ttu-id="7c283-128">Representa un evento en el que una carpeta o elemento se mueve de una carpeta principal a otra carpeta primaria.</span><span class="sxs-lookup"><span data-stu-id="7c283-128">Represents an event in which an item or folder is moved from one parent folder to another parent folder.</span></span>  <br/> |
|[<span data-ttu-id="7c283-129">NewMailEvent</span><span class="sxs-lookup"><span data-stu-id="7c283-129">NewMailEvent</span></span>](newmailevent.md) <br/> |<span data-ttu-id="7c283-130">Representa un evento que se desencadena por un nuevo elemento de correo en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="7c283-130">Represents an event that is triggered by a new mail item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="7c283-131">Objeto StatusEvent</span><span class="sxs-lookup"><span data-stu-id="7c283-131">StatusEvent</span></span>](statusevent.md) <br/> |<span data-ttu-id="7c283-132">Representa una notificación que no se ha producido ninguna actividad de nuevo en el buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="7c283-132">Represents a notification that no new activity has occurred in the mailbox.</span></span>  <br/> |
|[<span data-ttu-id="7c283-133">FreeBusyChangedEvent</span><span class="sxs-lookup"><span data-stu-id="7c283-133">FreeBusyChangedEvent</span></span>](freebusychangedevent.md) <br/> |<span data-ttu-id="7c283-134">Representa un evento en el que se ha cambiado el tiempo de disponibilidad de un elemento.</span><span class="sxs-lookup"><span data-stu-id="7c283-134">Represents an event in which an item's free/busy time has changed.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="7c283-135">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="7c283-135">Parent elements</span></span>

|<span data-ttu-id="7c283-136">**Element**</span><span class="sxs-lookup"><span data-stu-id="7c283-136">**Element**</span></span>|<span data-ttu-id="7c283-137">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7c283-137">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7c283-138">GetEventsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="7c283-138">GetEventsResponseMessage</span></span>](geteventsresponsemessage.md) <br/> |<span data-ttu-id="7c283-139">Contiene el estado y el resultado de una única solicitud GetEvents.</span><span class="sxs-lookup"><span data-stu-id="7c283-139">Contains the status and result of a single GetEvents request.</span></span>  <br/> |
|[<span data-ttu-id="7c283-140">SendNotificationResponseMessage</span><span class="sxs-lookup"><span data-stu-id="7c283-140">SendNotificationResponseMessage</span></span>](sendnotificationresponsemessage.md) <br/> |<span data-ttu-id="7c283-141">Contiene el estado y el resultado de una única solicitud de SendNotification.</span><span class="sxs-lookup"><span data-stu-id="7c283-141">Contains the status and result of a single SendNotification request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="7c283-142">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="7c283-142">Text value</span></span>

<span data-ttu-id="7c283-143">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="7c283-143">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7c283-144">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7c283-144">Remarks</span></span>

<span data-ttu-id="7c283-145">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="7c283-145">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7c283-146">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="7c283-146">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7c283-147">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="7c283-147">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="7c283-148">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="7c283-148">Schema Name</span></span>  <br/> |<span data-ttu-id="7c283-149">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="7c283-149">Types schema</span></span>  <br/> |
|<span data-ttu-id="7c283-150">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="7c283-150">Validation File</span></span>  <br/> |<span data-ttu-id="7c283-151">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="7c283-151">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="7c283-152">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="7c283-152">Can be Empty</span></span>  <br/> |<span data-ttu-id="7c283-153">False</span><span class="sxs-lookup"><span data-stu-id="7c283-153">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7c283-154">Ver también</span><span class="sxs-lookup"><span data-stu-id="7c283-154">See also</span></span>



[<span data-ttu-id="7c283-155">Operación de suscripción</span><span class="sxs-lookup"><span data-stu-id="7c283-155">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="7c283-156">Operación GetEvents</span><span class="sxs-lookup"><span data-stu-id="7c283-156">GetEvents operation</span></span>](getevents-operation.md)
  
[<span data-ttu-id="7c283-157">Operación GetStreamingEvents</span><span class="sxs-lookup"><span data-stu-id="7c283-157">GetStreamingEvents operation</span></span>](getstreamingevents-operation.md)
  
[<span data-ttu-id="7c283-158">Cancelar la operación de suscripción</span><span class="sxs-lookup"><span data-stu-id="7c283-158">Unsubscribe operation</span></span>](unsubscribe-operation.md)

