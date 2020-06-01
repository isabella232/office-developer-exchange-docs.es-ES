---
title: StatusFrequency
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- StatusFrequency
api_type:
- schema
ms.assetid: 917474e2-a426-4166-b825-53783a41dad4
description: El elemento StatusFrequency representa el valor de tiempo de espera máximo, en minutos, en el que el servidor intenta realizar reintentos.
ms.openlocfilehash: db14ecfd54584188b3da16bb369db6c8089c70f4
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/01/2020
ms.locfileid: "44468246"
---
# <a name="statusfrequency"></a><span data-ttu-id="9acec-103">StatusFrequency</span><span class="sxs-lookup"><span data-stu-id="9acec-103">StatusFrequency</span></span>

<span data-ttu-id="9acec-104">El elemento **StatusFrequency** representa el valor de tiempo de espera máximo, en minutos, en el que el servidor intenta realizar reintentos.</span><span class="sxs-lookup"><span data-stu-id="9acec-104">The **StatusFrequency** element represents the maximum timeout value, in minutes, in which retries are attempted by the server.</span></span> 
  
[<span data-ttu-id="9acec-105">Suscribirse</span><span class="sxs-lookup"><span data-stu-id="9acec-105">Subscribe</span></span>](subscribe.md)
  
[<span data-ttu-id="9acec-106">PushSubscriptionRequest</span><span class="sxs-lookup"><span data-stu-id="9acec-106">PushSubscriptionRequest</span></span>](pushsubscriptionrequest.md)
  
[<span data-ttu-id="9acec-107">StatusFrequency</span><span class="sxs-lookup"><span data-stu-id="9acec-107">StatusFrequency</span></span>](statusfrequency.md)
  
```XML
<StatusFrequency/>
```

 <span data-ttu-id="9acec-108">**SubscriptionStatusFrequencyType**</span><span class="sxs-lookup"><span data-stu-id="9acec-108">**SubscriptionStatusFrequencyType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9acec-109">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="9acec-109">Attributes and elements</span></span>

<span data-ttu-id="9acec-110">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="9acec-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9acec-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="9acec-111">Attributes</span></span>

<span data-ttu-id="9acec-112">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="9acec-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="9acec-113">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="9acec-113">Child elements</span></span>

<span data-ttu-id="9acec-114">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="9acec-114">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="9acec-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="9acec-115">Parent elements</span></span>

|<span data-ttu-id="9acec-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="9acec-116">**Element**</span></span>|<span data-ttu-id="9acec-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9acec-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9acec-118">PushSubscriptionRequest</span><span class="sxs-lookup"><span data-stu-id="9acec-118">PushSubscriptionRequest</span></span>](pushsubscriptionrequest.md) <br/> |<span data-ttu-id="9acec-119">Representa una suscripción a una suscripción de notificación de eventos basada en inserción.</span><span class="sxs-lookup"><span data-stu-id="9acec-119">Represents a subscription to a push-based event notification subscription.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="9acec-120">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="9acec-120">Text value</span></span>

<span data-ttu-id="9acec-121">Es necesario un valor de texto que representa un entero si se usa este elemento.</span><span class="sxs-lookup"><span data-stu-id="9acec-121">A text value that represents an integer is required if this element is used.</span></span> <span data-ttu-id="9acec-122">Los valores posibles para este elemento son de 1 a 1440, ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="9acec-122">The possible values for this element are 1 to 1440, inclusive.</span></span> <span data-ttu-id="9acec-123">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="9acec-123">This element is optional.</span></span> <span data-ttu-id="9acec-124">El valor predeterminado es de 30 minutos.</span><span class="sxs-lookup"><span data-stu-id="9acec-124">The default value is 30 minutes.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9acec-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9acec-125">Remarks</span></span>

<span data-ttu-id="9acec-126">El servidor usa el valor **StatusFrequency** para volver a intentar una notificación de inserción cuando no recibe una respuesta a una notificación de inserción o ping de estado del cliente.</span><span class="sxs-lookup"><span data-stu-id="9acec-126">The **StatusFrequency** value is used by the server to retry a push notification when it does not receive a response to a push notification or status ping from the client.</span></span> <span data-ttu-id="9acec-127">Si el servidor no recibe una respuesta, vuelve a intentar enviar la notificación varias veces antes de dejar de enviar la notificación.</span><span class="sxs-lookup"><span data-stu-id="9acec-127">If the server does not receive a response, it retries sending the notification several times before it stops sending the notification.</span></span> <span data-ttu-id="9acec-128">En EWS, el intervalo de reintento predeterminado es de 30 segundos y los reintentos siguientes siempre se duplican en el momento del último intervalo de reintento.</span><span class="sxs-lookup"><span data-stu-id="9acec-128">In EWS, the default retry interval is 30 seconds and subsequent retries are always double the time of the last retry interval.</span></span> <span data-ttu-id="9acec-129">Las horas de reintento no son exactas, ya que se pueden retrasar debido a otras cargas en el servidor.</span><span class="sxs-lookup"><span data-stu-id="9acec-129">Retry times are not exact as they can be delayed due to other loads on the server.</span></span> <span data-ttu-id="9acec-130">En la tabla siguiente se muestra cómo se producen los intervalos de reintento en los 30 minutos asignados por el valor de **StatusFrequency** predeterminado (si el servidor no ha encontrado ningún retraso).</span><span class="sxs-lookup"><span data-stu-id="9acec-130">The following table shows how the retry intervals occur in the 30 minutes allotted by the default **StatusFrequency** value (assuming the server did not encounter any delays).</span></span> 
  
|<span data-ttu-id="9acec-131">**Reintentar**</span><span class="sxs-lookup"><span data-stu-id="9acec-131">**Retry**</span></span>|<span data-ttu-id="9acec-132">**Segundos**</span><span class="sxs-lookup"><span data-stu-id="9acec-132">**Seconds**</span></span>|<span data-ttu-id="9acec-133">**Time**</span><span class="sxs-lookup"><span data-stu-id="9acec-133">**Time**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="9acec-134">comprendi</span><span class="sxs-lookup"><span data-stu-id="9acec-134">0</span></span>  <br/> |<span data-ttu-id="9acec-135">comprendi</span><span class="sxs-lookup"><span data-stu-id="9acec-135">0</span></span>  <br/> |<span data-ttu-id="9acec-136">Sincronización inicial</span><span class="sxs-lookup"><span data-stu-id="9acec-136">Initial sync</span></span>  <br/> |
|<span data-ttu-id="9acec-137">1 </span><span class="sxs-lookup"><span data-stu-id="9acec-137">1</span></span>  <br/> |<span data-ttu-id="9acec-138">semestre</span><span class="sxs-lookup"><span data-stu-id="9acec-138">30</span></span>  <br/> |<span data-ttu-id="9acec-139">00:30</span><span class="sxs-lookup"><span data-stu-id="9acec-139">00:30</span></span>  <br/> |
|<span data-ttu-id="9acec-140">segundo</span><span class="sxs-lookup"><span data-stu-id="9acec-140">2</span></span>  <br/> |<span data-ttu-id="9acec-141">60</span><span class="sxs-lookup"><span data-stu-id="9acec-141">60</span></span>  <br/> |<span data-ttu-id="9acec-142">01:00</span><span class="sxs-lookup"><span data-stu-id="9acec-142">01:00</span></span>  <br/> |
|<span data-ttu-id="9acec-143">3</span><span class="sxs-lookup"><span data-stu-id="9acec-143">3</span></span>  <br/> |<span data-ttu-id="9acec-144">120</span><span class="sxs-lookup"><span data-stu-id="9acec-144">120</span></span>  <br/> |<span data-ttu-id="9acec-145">02:00</span><span class="sxs-lookup"><span data-stu-id="9acec-145">02:00</span></span>  <br/> |
|<span data-ttu-id="9acec-146">4 </span><span class="sxs-lookup"><span data-stu-id="9acec-146">4</span></span>  <br/> |<span data-ttu-id="9acec-147">240</span><span class="sxs-lookup"><span data-stu-id="9acec-147">240</span></span>  <br/> |<span data-ttu-id="9acec-148">04:00</span><span class="sxs-lookup"><span data-stu-id="9acec-148">04:00</span></span>  <br/> |
|<span data-ttu-id="9acec-149">5 </span><span class="sxs-lookup"><span data-stu-id="9acec-149">5</span></span>  <br/> |<span data-ttu-id="9acec-150">480</span><span class="sxs-lookup"><span data-stu-id="9acec-150">480</span></span>  <br/> |<span data-ttu-id="9acec-151">08:00</span><span class="sxs-lookup"><span data-stu-id="9acec-151">08:00</span></span>  <br/> |
|<span data-ttu-id="9acec-152">6 </span><span class="sxs-lookup"><span data-stu-id="9acec-152">6</span></span>  <br/> |<span data-ttu-id="9acec-153">960</span><span class="sxs-lookup"><span data-stu-id="9acec-153">960</span></span>  <br/> |<span data-ttu-id="9acec-154">16:00</span><span class="sxs-lookup"><span data-stu-id="9acec-154">16:00</span></span>  <br/> |
|<span data-ttu-id="9acec-155">7 </span><span class="sxs-lookup"><span data-stu-id="9acec-155">7</span></span>  <br/> |<span data-ttu-id="9acec-156">1920</span><span class="sxs-lookup"><span data-stu-id="9acec-156">1920</span></span>  <br/> |<span data-ttu-id="9acec-157">32:00- **StatusFrequency** valor predeterminado de 30 superado, reintentar no enviado</span><span class="sxs-lookup"><span data-stu-id="9acec-157">32:00 - **StatusFrequency** default value of 30 exceeded, retry not sent</span></span>  <br/> |
   
<span data-ttu-id="9acec-158">Si el cliente no recibe mensajes de notificación del servidor durante un período de tiempo superior al doble del tiempo especificado por **StatusFrequency**, el cliente debe realizar una acción, como volver a crear la suscripción.</span><span class="sxs-lookup"><span data-stu-id="9acec-158">If the client does not receive notification messages from the server for a period of time that exceeds twice the time specified by **StatusFrequency**, the client should take an action such as recreating the subscription.</span></span> 
  
<span data-ttu-id="9acec-159">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="9acec-159">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9acec-160">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="9acec-160">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9acec-161">Namespace</span><span class="sxs-lookup"><span data-stu-id="9acec-161">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="9acec-162">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="9acec-162">Schema name</span></span>  <br/> |<span data-ttu-id="9acec-163">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="9acec-163">Types schema</span></span>  <br/> |
|<span data-ttu-id="9acec-164">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="9acec-164">Validation file</span></span>  <br/> |<span data-ttu-id="9acec-165">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="9acec-165">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="9acec-166">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="9acec-166">Can be empty</span></span>  <br/> |<span data-ttu-id="9acec-167">Falso</span><span class="sxs-lookup"><span data-stu-id="9acec-167">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9acec-168">Vea también</span><span class="sxs-lookup"><span data-stu-id="9acec-168">See also</span></span>



[<span data-ttu-id="9acec-169">Operación subscribe</span><span class="sxs-lookup"><span data-stu-id="9acec-169">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="9acec-170">Operación GetEvents</span><span class="sxs-lookup"><span data-stu-id="9acec-170">GetEvents operation</span></span>](getevents-operation.md)
  
[<span data-ttu-id="9acec-171">Operación unsubscribe</span><span class="sxs-lookup"><span data-stu-id="9acec-171">Unsubscribe operation</span></span>](unsubscribe-operation.md)
  
[<span data-ttu-id="9acec-172">Watermark</span><span class="sxs-lookup"><span data-stu-id="9acec-172">Watermark</span></span>](watermark.md)

