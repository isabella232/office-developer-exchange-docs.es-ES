---
title: StreamingSubscriptionRequest
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- StreamingSubscriptionRequest
api_type:
- schema
ms.assetid: d18f3b60-ebb6-4133-b895-a6ec8942d039
description: El elemento StreamingSubscriptionRequest representa una suscripción a una suscripción de notificación de eventos de streaming.
ms.openlocfilehash: b469ba7598420189c1db0e2fe676a279390eb6bf
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44468232"
---
# <a name="streamingsubscriptionrequest"></a><span data-ttu-id="eba48-103">StreamingSubscriptionRequest</span><span class="sxs-lookup"><span data-stu-id="eba48-103">StreamingSubscriptionRequest</span></span>

<span data-ttu-id="eba48-104">El elemento **StreamingSubscriptionRequest** representa una suscripción a una suscripción de notificación de eventos de streaming.</span><span class="sxs-lookup"><span data-stu-id="eba48-104">The **StreamingSubscriptionRequest** element represents a subscription to a streaming event notification subscription.</span></span> 
  
[<span data-ttu-id="eba48-105">Suscribirse</span><span class="sxs-lookup"><span data-stu-id="eba48-105">Subscribe</span></span>](subscribe.md)
  
[<span data-ttu-id="eba48-106">StreamingSubscriptionRequest</span><span class="sxs-lookup"><span data-stu-id="eba48-106">StreamingSubscriptionRequest</span></span>](streamingsubscriptionrequest.md)
  
```xml
<StreamingSubscriptionRequest SubscribeToAllFolders="">
   <FolderIds/>
   <EventTypes/>
</StreamingSubscriptionRequest>
```

 <span data-ttu-id="eba48-107">**StreamingSubscriptionRequest**</span><span class="sxs-lookup"><span data-stu-id="eba48-107">**StreamingSubscriptionRequest**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="eba48-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="eba48-108">Attributes and elements</span></span>

<span data-ttu-id="eba48-109">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="eba48-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="eba48-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="eba48-110">Attributes</span></span>

|<span data-ttu-id="eba48-111">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="eba48-111">**Attribute**</span></span>|<span data-ttu-id="eba48-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="eba48-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="eba48-113">**SubscribeToAllFolders**</span><span class="sxs-lookup"><span data-stu-id="eba48-113">**SubscribeToAllFolders**</span></span> <br/> |<span data-ttu-id="eba48-114">Indica si el servidor se suscribirá a todas las carpetas del buzón de correo del usuario.</span><span class="sxs-lookup"><span data-stu-id="eba48-114">Indicates whether the server will subscribe to all folders in the user's mailbox.</span></span> <span data-ttu-id="eba48-115">Un valor de **true** indica que se suscribirá el servidor.</span><span class="sxs-lookup"><span data-stu-id="eba48-115">A value of **true** indicates that the server will subscribe.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="eba48-116">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="eba48-116">Child elements</span></span>

|<span data-ttu-id="eba48-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="eba48-117">**Element**</span></span>|<span data-ttu-id="eba48-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="eba48-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="eba48-119">FolderIds</span><span class="sxs-lookup"><span data-stu-id="eba48-119">FolderIds</span></span>](folderids.md) <br/> |<span data-ttu-id="eba48-120">Contiene una matriz de identificadores de carpeta que se usan para identificar las carpetas que se van a supervisar para las notificaciones de eventos.</span><span class="sxs-lookup"><span data-stu-id="eba48-120">Contains an array of folder identifiers that are used to identify folders to monitor for event notifications.</span></span>  <br/> |
|[<span data-ttu-id="eba48-121">EventTypes</span><span class="sxs-lookup"><span data-stu-id="eba48-121">EventTypes</span></span>](eventtypes.md) <br/> |<span data-ttu-id="eba48-122">Contiene una colección de notificaciones de eventos que se usan para crear una suscripción.</span><span class="sxs-lookup"><span data-stu-id="eba48-122">Contains a collection of event notifications that are used to create a subscription.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="eba48-123">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="eba48-123">Parent elements</span></span>

|<span data-ttu-id="eba48-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="eba48-124">**Element**</span></span>|<span data-ttu-id="eba48-125">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="eba48-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="eba48-126">Suscribirse</span><span class="sxs-lookup"><span data-stu-id="eba48-126">Subscribe</span></span>](subscribe.md) <br/> |<span data-ttu-id="eba48-127">Contiene las propiedades que se usan para crear suscripciones.</span><span class="sxs-lookup"><span data-stu-id="eba48-127">Contains the properties that are used to create subscriptions.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="eba48-128">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="eba48-128">Text value</span></span>

<span data-ttu-id="eba48-129">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="eba48-129">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="eba48-130">Comentarios</span><span class="sxs-lookup"><span data-stu-id="eba48-130">Remarks</span></span>

<span data-ttu-id="eba48-131">El esquema que describe este elemento se encuentra en el directorio virtual de IIS que hospeda los servicios Web de Exchange. este elemento se introdujo en Exchange Server 2010 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="eba48-131">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="eba48-132">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="eba48-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="eba48-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="eba48-133">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="eba48-134">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="eba48-134">Schema name</span></span>  <br/> |<span data-ttu-id="eba48-135">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="eba48-135">Messages schema</span></span>  <br/> |
|<span data-ttu-id="eba48-136">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="eba48-136">Validation file</span></span>  <br/> |<span data-ttu-id="eba48-137">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="eba48-137">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="eba48-138">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="eba48-138">Can be empty</span></span>  <br/> |<span data-ttu-id="eba48-139">Falso</span><span class="sxs-lookup"><span data-stu-id="eba48-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="eba48-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="eba48-140">See also</span></span>



[<span data-ttu-id="eba48-141">Operación subscribe</span><span class="sxs-lookup"><span data-stu-id="eba48-141">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="eba48-142">Operación GetEvents</span><span class="sxs-lookup"><span data-stu-id="eba48-142">GetEvents operation</span></span>](getevents-operation.md)
  
[<span data-ttu-id="eba48-143">Operación GetStreamingEvents</span><span class="sxs-lookup"><span data-stu-id="eba48-143">GetStreamingEvents operation</span></span>](getstreamingevents-operation.md)
  
[<span data-ttu-id="eba48-144">Operación unsubscribe</span><span class="sxs-lookup"><span data-stu-id="eba48-144">Unsubscribe operation</span></span>](unsubscribe-operation.md)

