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
description: El elemento StatusFrequency representa el valor de tiempo de espera máximo, en minutos, en el que se ha tratado de reintentos por el servidor.
ms.openlocfilehash: 402f8978c0ec6b377dfa020f23595c8954509a07
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19837589"
---
# <a name="statusfrequency"></a><span data-ttu-id="27a1e-103">StatusFrequency</span><span class="sxs-lookup"><span data-stu-id="27a1e-103">StatusFrequency</span></span>

<span data-ttu-id="27a1e-104">El elemento **StatusFrequency** representa el valor de tiempo de espera máximo, en minutos, en el que se ha tratado de reintentos por el servidor.</span><span class="sxs-lookup"><span data-stu-id="27a1e-104">The **StatusFrequency** element represents the maximum timeout value, in minutes, in which retries are attempted by the server.</span></span> 
  
[<span data-ttu-id="27a1e-105">Suscribirse</span><span class="sxs-lookup"><span data-stu-id="27a1e-105">Subscribe</span></span>](subscribe.md)
  
[<span data-ttu-id="27a1e-106">PushSubscriptionRequest</span><span class="sxs-lookup"><span data-stu-id="27a1e-106">PushSubscriptionRequest</span></span>](pushsubscriptionrequest.md)
  
[<span data-ttu-id="27a1e-107">StatusFrequency</span><span class="sxs-lookup"><span data-stu-id="27a1e-107">StatusFrequency</span></span>](statusfrequency.md)
  
```XML
<StatusFrequency/>
```

 <span data-ttu-id="27a1e-108">**SubscriptionStatusFrequencyType**</span><span class="sxs-lookup"><span data-stu-id="27a1e-108">**SubscriptionStatusFrequencyType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="27a1e-109">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="27a1e-109">Attributes and elements</span></span>

<span data-ttu-id="27a1e-110">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="27a1e-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="27a1e-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="27a1e-111">Attributes</span></span>

<span data-ttu-id="27a1e-112">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="27a1e-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="27a1e-113">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="27a1e-113">Child elements</span></span>

<span data-ttu-id="27a1e-114">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="27a1e-114">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="27a1e-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="27a1e-115">Parent elements</span></span>

|<span data-ttu-id="27a1e-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="27a1e-116">**Element**</span></span>|<span data-ttu-id="27a1e-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="27a1e-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="27a1e-118">PushSubscriptionRequest</span><span class="sxs-lookup"><span data-stu-id="27a1e-118">PushSubscriptionRequest</span></span>](pushsubscriptionrequest.md) <br/> |<span data-ttu-id="27a1e-119">Representa una suscripción a una suscripción de notificación de evento basada en inserción.</span><span class="sxs-lookup"><span data-stu-id="27a1e-119">Represents a subscription to a push-based event notification subscription.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="27a1e-120">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="27a1e-120">Text value</span></span>

<span data-ttu-id="27a1e-121">Si se usa este elemento, es necesario un valor de texto que representa un número entero.</span><span class="sxs-lookup"><span data-stu-id="27a1e-121">A text value that represents an integer is required if this element is used.</span></span> <span data-ttu-id="27a1e-122">Los valores posibles para este elemento son 1 y 1440, ambos inclusive.</span><span class="sxs-lookup"><span data-stu-id="27a1e-122">The possible values for this element are 1 to 1440, inclusive.</span></span> <span data-ttu-id="27a1e-123">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="27a1e-123">This element is optional.</span></span> <span data-ttu-id="27a1e-124">El valor predeterminado es 30 minutos.</span><span class="sxs-lookup"><span data-stu-id="27a1e-124">The default value is 30 minutes.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="27a1e-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="27a1e-125">Remarks</span></span>

<span data-ttu-id="27a1e-126">El valor de **StatusFrequency** se usa en el servidor para volver a intentar una notificación de inserción cuando no recibe una respuesta a una notificación de inserción o ping de estado desde el cliente.</span><span class="sxs-lookup"><span data-stu-id="27a1e-126">The **StatusFrequency** value is used by the server to retry a push notification when it does not receive a response to a push notification or status ping from the client.</span></span> <span data-ttu-id="27a1e-127">Si el servidor no recibe una respuesta, reintentos enviar la notificación de varias veces antes de que ésta detiene el envío de la notificación.</span><span class="sxs-lookup"><span data-stu-id="27a1e-127">If the server does not receive a response, it retries sending the notification several times before it stops sending the notification.</span></span> <span data-ttu-id="27a1e-128">En EWS, el intervalo de reintento de forma predeterminada es de 30 segundos y reintentos subsiguientes siempre son doble a la hora de último intervalo de reintento.</span><span class="sxs-lookup"><span data-stu-id="27a1e-128">In EWS, the default retry interval is 30 seconds and subsequent retries are always double the time of the last retry interval.</span></span> <span data-ttu-id="27a1e-129">Número de reintentos no es exacto como que se pueden retrasar debido a otras cargas que hay en el servidor.</span><span class="sxs-lookup"><span data-stu-id="27a1e-129">Retry times are not exact as they can be delayed due to other loads on the server.</span></span> <span data-ttu-id="27a1e-130">En la tabla siguiente se muestra cómo se producen los intervalos de reintento en los 30 minutos máximo permitidos por el valor de **StatusFrequency** predeterminado (suponiendo que el servidor no encuentra la los retrasos).</span><span class="sxs-lookup"><span data-stu-id="27a1e-130">The following table shows how the retry intervals occur in the 30 minutes allotted by the default **StatusFrequency** value (assuming the server did not encounter any delays).</span></span> 
  
|<span data-ttu-id="27a1e-131">**Reintentar**</span><span class="sxs-lookup"><span data-stu-id="27a1e-131">**Retry**</span></span>|<span data-ttu-id="27a1e-132">**Segundos**</span><span class="sxs-lookup"><span data-stu-id="27a1e-132">**Seconds**</span></span>|<span data-ttu-id="27a1e-133">**Time**</span><span class="sxs-lookup"><span data-stu-id="27a1e-133">**Time**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="27a1e-134">0</span><span class="sxs-lookup"><span data-stu-id="27a1e-134">0</span></span>  <br/> |<span data-ttu-id="27a1e-135">0</span><span class="sxs-lookup"><span data-stu-id="27a1e-135">0</span></span>  <br/> |<span data-ttu-id="27a1e-136">Sincronización inicial</span><span class="sxs-lookup"><span data-stu-id="27a1e-136">Initial sync</span></span>  <br/> |
|<span data-ttu-id="27a1e-137">1</span><span class="sxs-lookup"><span data-stu-id="27a1e-137">1</span></span>  <br/> |<span data-ttu-id="27a1e-138">30</span><span class="sxs-lookup"><span data-stu-id="27a1e-138">30</span></span>  <br/> |<span data-ttu-id="27a1e-139">00:30</span><span class="sxs-lookup"><span data-stu-id="27a1e-139">00:30</span></span>  <br/> |
|<span data-ttu-id="27a1e-140">2</span><span class="sxs-lookup"><span data-stu-id="27a1e-140">2</span></span>  <br/> |<span data-ttu-id="27a1e-141">60</span><span class="sxs-lookup"><span data-stu-id="27a1e-141">60</span></span>  <br/> |<span data-ttu-id="27a1e-142">01:00</span><span class="sxs-lookup"><span data-stu-id="27a1e-142">01:00</span></span>  <br/> |
|<span data-ttu-id="27a1e-143">3</span><span class="sxs-lookup"><span data-stu-id="27a1e-143">3</span></span>  <br/> |<span data-ttu-id="27a1e-144">120</span><span class="sxs-lookup"><span data-stu-id="27a1e-144">120</span></span>  <br/> |<span data-ttu-id="27a1e-145">02:00</span><span class="sxs-lookup"><span data-stu-id="27a1e-145">02:00</span></span>  <br/> |
|<span data-ttu-id="27a1e-146">4</span><span class="sxs-lookup"><span data-stu-id="27a1e-146">4</span></span>  <br/> |<span data-ttu-id="27a1e-147">240</span><span class="sxs-lookup"><span data-stu-id="27a1e-147">240</span></span>  <br/> |<span data-ttu-id="27a1e-148">04:00</span><span class="sxs-lookup"><span data-stu-id="27a1e-148">04:00</span></span>  <br/> |
|<span data-ttu-id="27a1e-149">5</span><span class="sxs-lookup"><span data-stu-id="27a1e-149">5</span></span>  <br/> |<span data-ttu-id="27a1e-150">480</span><span class="sxs-lookup"><span data-stu-id="27a1e-150">480</span></span>  <br/> |<span data-ttu-id="27a1e-151">08:00</span><span class="sxs-lookup"><span data-stu-id="27a1e-151">08:00</span></span>  <br/> |
|<span data-ttu-id="27a1e-152">6</span><span class="sxs-lookup"><span data-stu-id="27a1e-152">6</span></span>  <br/> |<span data-ttu-id="27a1e-153">960</span><span class="sxs-lookup"><span data-stu-id="27a1e-153">960</span></span>  <br/> |<span data-ttu-id="27a1e-154">16:00</span><span class="sxs-lookup"><span data-stu-id="27a1e-154">16:00</span></span>  <br/> |
|<span data-ttu-id="27a1e-155">7</span><span class="sxs-lookup"><span data-stu-id="27a1e-155">7</span></span>  <br/> |<span data-ttu-id="27a1e-156">1920</span><span class="sxs-lookup"><span data-stu-id="27a1e-156">1920</span></span>  <br/> |<span data-ttu-id="27a1e-157">32:00 - **StatusFrequency** valor de predeterminado de 30 superado, reintento no enviado</span><span class="sxs-lookup"><span data-stu-id="27a1e-157">32:00 - **StatusFrequency** default value of 30 exceeded, retry not sent</span></span>  <br/> |
   
<span data-ttu-id="27a1e-158">Si el cliente no recibe los mensajes de notificación desde el servidor durante un período de tiempo que supere los dos veces el tiempo especificado por **StatusFrequency**, el cliente debe realizar una acción como volver a crear la suscripción.</span><span class="sxs-lookup"><span data-stu-id="27a1e-158">If the client does not receive notification messages from the server for a period of time that exceeds twice the time specified by **StatusFrequency**, the client should take an action such as recreating the subscription.</span></span> 
  
<span data-ttu-id="27a1e-159">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="27a1e-159">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="27a1e-160">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="27a1e-160">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="27a1e-161">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="27a1e-161">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="27a1e-162">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="27a1e-162">Schema name</span></span>  <br/> |<span data-ttu-id="27a1e-163">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="27a1e-163">Types schema</span></span>  <br/> |
|<span data-ttu-id="27a1e-164">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="27a1e-164">Validation file</span></span>  <br/> |<span data-ttu-id="27a1e-165">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="27a1e-165">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="27a1e-166">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="27a1e-166">Can be empty</span></span>  <br/> |<span data-ttu-id="27a1e-167">False</span><span class="sxs-lookup"><span data-stu-id="27a1e-167">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="27a1e-168">Vea también</span><span class="sxs-lookup"><span data-stu-id="27a1e-168">See also</span></span>



[<span data-ttu-id="27a1e-169">Operación de suscripción</span><span class="sxs-lookup"><span data-stu-id="27a1e-169">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="27a1e-170">Operación GetEvents</span><span class="sxs-lookup"><span data-stu-id="27a1e-170">GetEvents operation</span></span>](getevents-operation.md)
  
[<span data-ttu-id="27a1e-171">Cancelar la operación de suscripción</span><span class="sxs-lookup"><span data-stu-id="27a1e-171">Unsubscribe operation</span></span>](unsubscribe-operation.md)
  
[<span data-ttu-id="27a1e-172">Marca de agua</span><span class="sxs-lookup"><span data-stu-id="27a1e-172">Watermark</span></span>](watermark.md)

