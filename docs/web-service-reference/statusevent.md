---
title: Objeto StatusEvent
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
description: El elemento de objeto StatusEvent representa una notificación que no se ha producido ninguna actividad de nuevo en el buzón de correo.
ms.openlocfilehash: e214918f9795e9e29061d4aac72ab144d2b24267
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19837592"
---
# <a name="statusevent"></a><span data-ttu-id="867e4-103">Objeto StatusEvent</span><span class="sxs-lookup"><span data-stu-id="867e4-103">StatusEvent</span></span>

<span data-ttu-id="867e4-104">El elemento de **objeto StatusEvent** representa una notificación que no se ha producido ninguna actividad de nuevo en el buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="867e4-104">The **StatusEvent** element represents a notification that no new activity has occurred in the mailbox.</span></span> 
  
```xml
<StatusEvent>
   <Watermark/>
</StatusEvent>
```

 <span data-ttu-id="867e4-105">**BaseNotificationEventType**</span><span class="sxs-lookup"><span data-stu-id="867e4-105">**BaseNotificationEventType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="867e4-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="867e4-106">Attributes and elements</span></span>

<span data-ttu-id="867e4-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="867e4-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="867e4-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="867e4-108">Attributes</span></span>

<span data-ttu-id="867e4-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="867e4-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="867e4-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="867e4-110">Child elements</span></span>

|<span data-ttu-id="867e4-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="867e4-111">**Element**</span></span>|<span data-ttu-id="867e4-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="867e4-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="867e4-113">Marca de agua</span><span class="sxs-lookup"><span data-stu-id="867e4-113">Watermark</span></span>](watermark.md) <br/> |<span data-ttu-id="867e4-114">Representa la última marca de agua válido para una suscripción a.</span><span class="sxs-lookup"><span data-stu-id="867e4-114">Represents the last valid watermark for a subscription.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="867e4-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="867e4-115">Parent elements</span></span>

|<span data-ttu-id="867e4-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="867e4-116">**Element**</span></span>|<span data-ttu-id="867e4-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="867e4-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="867e4-118">Notificación</span><span class="sxs-lookup"><span data-stu-id="867e4-118">Notification</span></span>](notification-ex15websvcsotherref.md) <br/> |<span data-ttu-id="867e4-119">Contiene información acerca de la suscripción y los eventos que se han producido desde la última notificación.</span><span class="sxs-lookup"><span data-stu-id="867e4-119">Contains information about the subscription and the events that have occurred since the last notification.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="867e4-120">Notas</span><span class="sxs-lookup"><span data-stu-id="867e4-120">Remarks</span></span>

<span data-ttu-id="867e4-121">El elemento de **objeto StatusEvent** se devuelve en una notificación para uno de los siguientes motivos:</span><span class="sxs-lookup"><span data-stu-id="867e4-121">The **StatusEvent** element is returned in a notification for one of the following reasons:</span></span> 
  
- <span data-ttu-id="867e4-122">Un cliente de extracción emite una solicitud GetEvents en una suscripción que no tiene ninguna actividad.</span><span class="sxs-lookup"><span data-stu-id="867e4-122">A pull client issues a GetEvents request on a subscription that has no activity.</span></span>
    
- <span data-ttu-id="867e4-123">Un cliente de inserción no tiene eventos en la cola cuando se ha alcanzado el [StatusFrequency](statusfrequency.md) .</span><span class="sxs-lookup"><span data-stu-id="867e4-123">A push client has no events in the queue when the [StatusFrequency](statusfrequency.md) has been reached.</span></span> 
    
<span data-ttu-id="867e4-124">El **objeto StatusEvent**[marca de agua](watermark.md) se usa en una aplicación cliente de la misma manera que las demás marcas de agua de tipo de evento.</span><span class="sxs-lookup"><span data-stu-id="867e4-124">The **StatusEvent**[Watermark](watermark.md) is used by a client application in the same manner as the other event type watermarks.</span></span> <span data-ttu-id="867e4-125">Sin embargo, la marca de agua para el **objeto StatusEvent** no es el mismo que las marcas de agua que se usa para otros eventos.</span><span class="sxs-lookup"><span data-stu-id="867e4-125">However, the watermark for the **StatusEvent** is not the same as the watermarks used for other events.</span></span> <span data-ttu-id="867e4-126">Por ejemplo, una suscripción tiene eventos con marcas de agua de 1, 2 y 3 y los eventos se han comunicado correctamente en una notificación.</span><span class="sxs-lookup"><span data-stu-id="867e4-126">For example, a subscription has events with watermarks 1, 2, and 3 and those events have been successfully communicated in a notification.</span></span> <span data-ttu-id="867e4-127">Se produce un período de inactividad y se envía una solicitud de **GetEvents** .</span><span class="sxs-lookup"><span data-stu-id="867e4-127">A period of inactivity occurs and a **GetEvents** request is sent.</span></span> <span data-ttu-id="867e4-128">El servidor de acceso de cliente (CAS) devuelve un evento de estado e incluye la última marca de agua, 3, como la [PreviousWatermark](previouswatermark.md) y la actual [marca de agua](watermark.md).</span><span class="sxs-lookup"><span data-stu-id="867e4-128">The Client Access server (CAS) returns a status event and includes the last watermark, 3, as both the [PreviousWatermark](previouswatermark.md) and the current [Watermark](watermark.md).</span></span>
  
<span data-ttu-id="867e4-129">La marca de agua no seguirá siendo la misma en todos los casos.</span><span class="sxs-lookup"><span data-stu-id="867e4-129">The watermark will not remain the same in all cases.</span></span> <span data-ttu-id="867e4-130">Entradas de eventos se mantienen durante 30 días.</span><span class="sxs-lookup"><span data-stu-id="867e4-130">Event entries are maintained for 30 days.</span></span> <span data-ttu-id="867e4-131">Para mantener una suscripción activa, las entidades Emisoras actualizan periódicamente las marcas de agua para las colas de suscripción.</span><span class="sxs-lookup"><span data-stu-id="867e4-131">To maintain an active subscription, the CAS periodically updates the watermarks for subscription queues.</span></span> <span data-ttu-id="867e4-132">Las marcas de agua actualizados se envían a los clientes para mantener una suscripción activa.</span><span class="sxs-lookup"><span data-stu-id="867e4-132">The updated watermarks are sent to clients to maintain an active subscription.</span></span>
  
<span data-ttu-id="867e4-133">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="867e4-133">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="867e4-134">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="867e4-134">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="867e4-135">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="867e4-135">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="867e4-136">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="867e4-136">Schema name</span></span>  <br/> |<span data-ttu-id="867e4-137">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="867e4-137">Types schema</span></span>  <br/> |
|<span data-ttu-id="867e4-138">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="867e4-138">Validation file</span></span>  <br/> |<span data-ttu-id="867e4-139">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="867e4-139">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="867e4-140">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="867e4-140">Can be empty</span></span>  <br/> |<span data-ttu-id="867e4-141">False</span><span class="sxs-lookup"><span data-stu-id="867e4-141">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="867e4-142">Ver también</span><span class="sxs-lookup"><span data-stu-id="867e4-142">See also</span></span>



[<span data-ttu-id="867e4-143">Operación de suscripción</span><span class="sxs-lookup"><span data-stu-id="867e4-143">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="867e4-144">Operación GetEvents</span><span class="sxs-lookup"><span data-stu-id="867e4-144">GetEvents operation</span></span>](getevents-operation.md)
  
[<span data-ttu-id="867e4-145">Cancelar la operación de suscripción</span><span class="sxs-lookup"><span data-stu-id="867e4-145">Unsubscribe operation</span></span>](unsubscribe-operation.md)

