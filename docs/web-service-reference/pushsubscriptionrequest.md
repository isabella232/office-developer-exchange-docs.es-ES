---
title: PushSubscriptionRequest
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PushSubscriptionRequest
api_type:
- schema
ms.assetid: 70caa0ca-40a1-421f-b4e6-0658f22d0b8e
description: El elemento PushSubscriptionRequest representa una suscripción a una suscripción de notificación de eventos basada en inserción.
ms.openlocfilehash: dcdb767ed175468aa4ec940f3147c164e4707e40
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465516"
---
# <a name="pushsubscriptionrequest"></a><span data-ttu-id="46720-103">PushSubscriptionRequest</span><span class="sxs-lookup"><span data-stu-id="46720-103">PushSubscriptionRequest</span></span>

<span data-ttu-id="46720-104">El elemento **PushSubscriptionRequest** representa una suscripción a una suscripción de notificación de eventos basada en inserción.</span><span class="sxs-lookup"><span data-stu-id="46720-104">The **PushSubscriptionRequest** element represents a subscription to a push-based event notification subscription.</span></span> 
  
[<span data-ttu-id="46720-105">Suscribirse</span><span class="sxs-lookup"><span data-stu-id="46720-105">Subscribe</span></span>](subscribe.md)
  
[<span data-ttu-id="46720-106">PushSubscriptionRequest</span><span class="sxs-lookup"><span data-stu-id="46720-106">PushSubscriptionRequest</span></span>](pushsubscriptionrequest.md)
  
```XML
<PushSubscriptionRequest SubscribeToAllFolders="">
   <FolderIds/>
   <EventTypes/>
   <Watermark/>
   <StatusFrequency/>
   <URL/>
</PushSubscriptionRequest>
```

 <span data-ttu-id="46720-107">**PushSubscriptionRequestType**</span><span class="sxs-lookup"><span data-stu-id="46720-107">**PushSubscriptionRequestType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="46720-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="46720-108">Attributes and elements</span></span>

<span data-ttu-id="46720-109">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="46720-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="46720-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="46720-110">Attributes</span></span>

|<span data-ttu-id="46720-111">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="46720-111">**Attribute**</span></span>|<span data-ttu-id="46720-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="46720-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="46720-113">**SubscribeToAllFolders**</span><span class="sxs-lookup"><span data-stu-id="46720-113">**SubscribeToAllFolders**</span></span> <br/> |<span data-ttu-id="46720-114">Indica si se va a suscribir a todas las carpetas disponibles.</span><span class="sxs-lookup"><span data-stu-id="46720-114">Indicates whether to subscribe to all available folders.</span></span> <span data-ttu-id="46720-115">Este atributo es opcional.</span><span class="sxs-lookup"><span data-stu-id="46720-115">This attribute is optional.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="46720-116">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="46720-116">Child elements</span></span>

|<span data-ttu-id="46720-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="46720-117">**Element**</span></span>|<span data-ttu-id="46720-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="46720-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="46720-119">FolderIds</span><span class="sxs-lookup"><span data-stu-id="46720-119">FolderIds</span></span>](folderids.md) <br/> |<span data-ttu-id="46720-120">Contiene una matriz de identificadores de carpeta que se usan para identificar las carpetas que se van a supervisar para las notificaciones de eventos.</span><span class="sxs-lookup"><span data-stu-id="46720-120">Contains an array of folder identifiers that are used to identify folders to monitor for event notifications.</span></span>  <br/> |
|[<span data-ttu-id="46720-121">EventTypes</span><span class="sxs-lookup"><span data-stu-id="46720-121">EventTypes</span></span>](eventtypes.md) <br/> |<span data-ttu-id="46720-122">Contiene una colección de notificaciones de eventos que se usan para crear una suscripción.</span><span class="sxs-lookup"><span data-stu-id="46720-122">Contains a collection of event notifications that are used to create a subscription.</span></span>  <br/> |
|[<span data-ttu-id="46720-123">Watermark</span><span class="sxs-lookup"><span data-stu-id="46720-123">Watermark</span></span>](watermark.md) <br/> |<span data-ttu-id="46720-124">Representa un marcador de evento en la tabla de eventos del buzón.</span><span class="sxs-lookup"><span data-stu-id="46720-124">Represents an event bookmark in the mailbox events table.</span></span> <span data-ttu-id="46720-125">Se usa para crear una suscripción que empieza en un evento representado por la marca de agua.</span><span class="sxs-lookup"><span data-stu-id="46720-125">This is used to create a subscription starting at an event represented by the watermark.</span></span> <span data-ttu-id="46720-126">Si no se encuentra la marca de agua de una solicitud de suscripción, se devolverá una respuesta de error al cliente.</span><span class="sxs-lookup"><span data-stu-id="46720-126">If the watermark from a Subscribe request is not found, an error response will be returned to the client.</span></span> <span data-ttu-id="46720-127">Esto puede ocurrir si la marca de agua es superior a 30 días o si la marca de agua nunca estaba presente en el buzón.</span><span class="sxs-lookup"><span data-stu-id="46720-127">This may occur if the watermark is older than 30 days or if the watermark was never present in the mailbox.</span></span>  <br/> |
|[<span data-ttu-id="46720-128">StatusFrequency</span><span class="sxs-lookup"><span data-stu-id="46720-128">StatusFrequency</span></span>](statusfrequency.md) <br/> |<span data-ttu-id="46720-129">Representa la frecuencia, especificada en minutos, a la que se enviarán los mensajes de notificación al cliente cuando no se ha producido ningún evento.</span><span class="sxs-lookup"><span data-stu-id="46720-129">Represents the frequency, specified in minutes, at which notification messages will be sent to the client when no events have occurred.</span></span>  <br/> |
|[<span data-ttu-id="46720-130">Dirección URL</span><span class="sxs-lookup"><span data-stu-id="46720-130">Url </span></span>](url-ex15websvcsotherref.md) <br/> |<span data-ttu-id="46720-131">Representa la ubicación del servicio Web de cliente para las notificaciones de inserción.</span><span class="sxs-lookup"><span data-stu-id="46720-131">Represents the location of the client Web service for push notifications.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="46720-132">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="46720-132">Parent elements</span></span>

|<span data-ttu-id="46720-133">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="46720-133">**Element**</span></span>|<span data-ttu-id="46720-134">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="46720-134">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="46720-135">Suscribirse</span><span class="sxs-lookup"><span data-stu-id="46720-135">Subscribe</span></span>](subscribe.md) <br/> |<span data-ttu-id="46720-136">Contiene las propiedades utilizadas para crear suscripciones.</span><span class="sxs-lookup"><span data-stu-id="46720-136">Contains the properties used to create subscriptions.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="46720-137">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="46720-137">Text value</span></span>

<span data-ttu-id="46720-138">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="46720-138">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="46720-139">Comentarios</span><span class="sxs-lookup"><span data-stu-id="46720-139">Remarks</span></span>

<span data-ttu-id="46720-140">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="46720-140">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="46720-141">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="46720-141">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="46720-142">Namespace</span><span class="sxs-lookup"><span data-stu-id="46720-142">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="46720-143">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="46720-143">Schema name</span></span>  <br/> |<span data-ttu-id="46720-144">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="46720-144">Messages schema</span></span>  <br/> |
|<span data-ttu-id="46720-145">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="46720-145">Validation file</span></span>  <br/> |<span data-ttu-id="46720-146">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="46720-146">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="46720-147">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="46720-147">Can be empty</span></span>  <br/> |<span data-ttu-id="46720-148">Falso</span><span class="sxs-lookup"><span data-stu-id="46720-148">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="46720-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="46720-149">See also</span></span>



[<span data-ttu-id="46720-150">Operación subscribe</span><span class="sxs-lookup"><span data-stu-id="46720-150">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="46720-151">Operación GetEvents</span><span class="sxs-lookup"><span data-stu-id="46720-151">GetEvents operation</span></span>](getevents-operation.md)
  
[<span data-ttu-id="46720-152">Operación unsubscribe</span><span class="sxs-lookup"><span data-stu-id="46720-152">Unsubscribe operation</span></span>](unsubscribe-operation.md)

