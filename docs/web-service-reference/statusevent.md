---
title: StatusEvent
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- StatusEvent
api_type:
- schema
ms.assetid: d3901818-2640-4bed-aad8-21a61aee62a1
description: El elemento StatusEvent representa una notificación de que no se ha producido ninguna actividad nueva en el buzón.
ms.openlocfilehash: 8158a47937a810be2ea22346384b4e61da56ac48
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468260"
---
# <a name="statusevent"></a><span data-ttu-id="3691c-103">StatusEvent</span><span class="sxs-lookup"><span data-stu-id="3691c-103">StatusEvent</span></span>

<span data-ttu-id="3691c-104">El elemento **StatusEvent** representa una notificación de que no se ha producido ninguna actividad nueva en el buzón.</span><span class="sxs-lookup"><span data-stu-id="3691c-104">The **StatusEvent** element represents a notification that no new activity has occurred in the mailbox.</span></span> 
  
```xml
<StatusEvent>
   <Watermark/>
</StatusEvent>
```

 <span data-ttu-id="3691c-105">**BaseNotificationEventType**</span><span class="sxs-lookup"><span data-stu-id="3691c-105">**BaseNotificationEventType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3691c-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="3691c-106">Attributes and elements</span></span>

<span data-ttu-id="3691c-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="3691c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3691c-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="3691c-108">Attributes</span></span>

<span data-ttu-id="3691c-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="3691c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3691c-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="3691c-110">Child elements</span></span>

|<span data-ttu-id="3691c-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="3691c-111">**Element**</span></span>|<span data-ttu-id="3691c-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3691c-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3691c-113">Watermark</span><span class="sxs-lookup"><span data-stu-id="3691c-113">Watermark</span></span>](watermark.md) <br/> |<span data-ttu-id="3691c-114">Representa la última marca de agua válida para una suscripción.</span><span class="sxs-lookup"><span data-stu-id="3691c-114">Represents the last valid watermark for a subscription.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="3691c-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="3691c-115">Parent elements</span></span>

|<span data-ttu-id="3691c-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="3691c-116">**Element**</span></span>|<span data-ttu-id="3691c-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3691c-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3691c-118">Notificación</span><span class="sxs-lookup"><span data-stu-id="3691c-118">Notification</span></span>](notification-ex15websvcsotherref.md) <br/> |<span data-ttu-id="3691c-119">Contiene información sobre la suscripción y los eventos que se han producido desde la última notificación.</span><span class="sxs-lookup"><span data-stu-id="3691c-119">Contains information about the subscription and the events that have occurred since the last notification.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3691c-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3691c-120">Remarks</span></span>

<span data-ttu-id="3691c-121">El elemento **StatusEvent** se devuelve en una notificación por una de las siguientes razones:</span><span class="sxs-lookup"><span data-stu-id="3691c-121">The **StatusEvent** element is returned in a notification for one of the following reasons:</span></span> 
  
- <span data-ttu-id="3691c-122">Un cliente de extracción emite una solicitud GetEvents en una suscripción que no tiene actividad.</span><span class="sxs-lookup"><span data-stu-id="3691c-122">A pull client issues a GetEvents request on a subscription that has no activity.</span></span>
    
- <span data-ttu-id="3691c-123">Un cliente de inserción no tiene eventos en la cola cuando se ha alcanzado el [StatusFrequency](statusfrequency.md) .</span><span class="sxs-lookup"><span data-stu-id="3691c-123">A push client has no events in the queue when the [StatusFrequency](statusfrequency.md) has been reached.</span></span> 
    
<span data-ttu-id="3691c-124">La **StatusEvent**[marca de agua](watermark.md) StatusEvent se usa en una aplicación cliente de la misma manera que las marcas de agua de otro tipo de evento.</span><span class="sxs-lookup"><span data-stu-id="3691c-124">The **StatusEvent**[Watermark](watermark.md) is used by a client application in the same manner as the other event type watermarks.</span></span> <span data-ttu-id="3691c-125">Sin embargo, la marca de agua de **StatusEvent** no es la misma que las marcas de agua usadas para otros eventos.</span><span class="sxs-lookup"><span data-stu-id="3691c-125">However, the watermark for the **StatusEvent** is not the same as the watermarks used for other events.</span></span> <span data-ttu-id="3691c-126">Por ejemplo, una suscripción tiene eventos con marcas de agua de 1, 2 y 3, y estos eventos se han comunicado correctamente en una notificación.</span><span class="sxs-lookup"><span data-stu-id="3691c-126">For example, a subscription has events with watermarks 1, 2, and 3 and those events have been successfully communicated in a notification.</span></span> <span data-ttu-id="3691c-127">Se produce un período de inactividad y se envía una solicitud **GetEvents** .</span><span class="sxs-lookup"><span data-stu-id="3691c-127">A period of inactivity occurs and a **GetEvents** request is sent.</span></span> <span data-ttu-id="3691c-128">El servidor de acceso de cliente (CAS) devuelve un evento status e incluye la última marca de agua, 3, como [PreviousWatermark](previouswatermark.md) y la [marca de agua](watermark.md)actual.</span><span class="sxs-lookup"><span data-stu-id="3691c-128">The Client Access server (CAS) returns a status event and includes the last watermark, 3, as both the [PreviousWatermark](previouswatermark.md) and the current [Watermark](watermark.md).</span></span>
  
<span data-ttu-id="3691c-129">La marca de agua no seguirá siendo la misma en todos los casos.</span><span class="sxs-lookup"><span data-stu-id="3691c-129">The watermark will not remain the same in all cases.</span></span> <span data-ttu-id="3691c-130">Las entradas del evento se mantienen durante 30 días.</span><span class="sxs-lookup"><span data-stu-id="3691c-130">Event entries are maintained for 30 days.</span></span> <span data-ttu-id="3691c-131">Para mantener una suscripción activa, las entidades de certificación actualizan periódicamente las marcas de agua de las colas de suscripción.</span><span class="sxs-lookup"><span data-stu-id="3691c-131">To maintain an active subscription, the CAS periodically updates the watermarks for subscription queues.</span></span> <span data-ttu-id="3691c-132">Las marcas de agua actualizadas se envían a los clientes para mantener una suscripción activa.</span><span class="sxs-lookup"><span data-stu-id="3691c-132">The updated watermarks are sent to clients to maintain an active subscription.</span></span>
  
<span data-ttu-id="3691c-133">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="3691c-133">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3691c-134">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="3691c-134">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3691c-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="3691c-135">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="3691c-136">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="3691c-136">Schema name</span></span>  <br/> |<span data-ttu-id="3691c-137">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="3691c-137">Types schema</span></span>  <br/> |
|<span data-ttu-id="3691c-138">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="3691c-138">Validation file</span></span>  <br/> |<span data-ttu-id="3691c-139">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="3691c-139">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="3691c-140">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="3691c-140">Can be empty</span></span>  <br/> |<span data-ttu-id="3691c-141">Falso</span><span class="sxs-lookup"><span data-stu-id="3691c-141">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3691c-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="3691c-142">See also</span></span>



[<span data-ttu-id="3691c-143">Operación subscribe</span><span class="sxs-lookup"><span data-stu-id="3691c-143">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="3691c-144">Operación GetEvents</span><span class="sxs-lookup"><span data-stu-id="3691c-144">GetEvents operation</span></span>](getevents-operation.md)
  
[<span data-ttu-id="3691c-145">Operación unsubscribe</span><span class="sxs-lookup"><span data-stu-id="3691c-145">Unsubscribe operation</span></span>](unsubscribe-operation.md)

