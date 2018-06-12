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
description: El elemento StreamingSubscriptionRequest representa una suscripción a una suscripción de notificación de evento transmisión por secuencias.
ms.openlocfilehash: 088ec3b8048d70803b4837548ca918c0005d91bb
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19837601"
---
# <a name="streamingsubscriptionrequest"></a><span data-ttu-id="3b753-103">StreamingSubscriptionRequest</span><span class="sxs-lookup"><span data-stu-id="3b753-103">StreamingSubscriptionRequest</span></span>

<span data-ttu-id="3b753-104">El elemento **StreamingSubscriptionRequest** representa una suscripción a una suscripción de notificación de evento transmisión por secuencias.</span><span class="sxs-lookup"><span data-stu-id="3b753-104">The **StreamingSubscriptionRequest** element represents a subscription to a streaming event notification subscription.</span></span> 
  
[<span data-ttu-id="3b753-105">Suscribirse</span><span class="sxs-lookup"><span data-stu-id="3b753-105">Subscribe</span></span>](subscribe.md)
  
[<span data-ttu-id="3b753-106">StreamingSubscriptionRequest</span><span class="sxs-lookup"><span data-stu-id="3b753-106">StreamingSubscriptionRequest</span></span>](streamingsubscriptionrequest.md)
  
```xml
<StreamingSubscriptionRequest SubscribeToAllFolders="">
   <FolderIds/>
   <EventTypes/>
</StreamingSubscriptionRequest>
```

 <span data-ttu-id="3b753-107">**StreamingSubscriptionRequest**</span><span class="sxs-lookup"><span data-stu-id="3b753-107">**StreamingSubscriptionRequest**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3b753-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="3b753-108">Attributes and elements</span></span>

<span data-ttu-id="3b753-109">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="3b753-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3b753-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="3b753-110">Attributes</span></span>

|<span data-ttu-id="3b753-111">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="3b753-111">**Attribute**</span></span>|<span data-ttu-id="3b753-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3b753-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3b753-113">**SubscribeToAllFolders**</span><span class="sxs-lookup"><span data-stu-id="3b753-113">**SubscribeToAllFolders**</span></span> <br/> |<span data-ttu-id="3b753-114">Indica si el servidor se suscribirá a todas las carpetas en el buzón del usuario.</span><span class="sxs-lookup"><span data-stu-id="3b753-114">Indicates whether the server will subscribe to all folders in the user's mailbox.</span></span> <span data-ttu-id="3b753-115">Un valor de **true** indica que el servidor se suscribirá.</span><span class="sxs-lookup"><span data-stu-id="3b753-115">A value of **true** indicates that the server will subscribe.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="3b753-116">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="3b753-116">Child elements</span></span>

|<span data-ttu-id="3b753-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="3b753-117">**Element**</span></span>|<span data-ttu-id="3b753-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3b753-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3b753-119">FolderIds</span><span class="sxs-lookup"><span data-stu-id="3b753-119">FolderIds</span></span>](folderids.md) <br/> |<span data-ttu-id="3b753-120">Contiene una matriz de identificadores de carpeta que se usa para identificar las carpetas para supervisar las notificaciones de eventos.</span><span class="sxs-lookup"><span data-stu-id="3b753-120">Contains an array of folder identifiers that are used to identify folders to monitor for event notifications.</span></span>  <br/> |
|[<span data-ttu-id="3b753-121">Debe establecer</span><span class="sxs-lookup"><span data-stu-id="3b753-121">EventTypes</span></span>](eventtypes.md) <br/> |<span data-ttu-id="3b753-122">Contiene una colección de las notificaciones de eventos que se usan para crear una suscripción.</span><span class="sxs-lookup"><span data-stu-id="3b753-122">Contains a collection of event notifications that are used to create a subscription.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="3b753-123">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="3b753-123">Parent elements</span></span>

|<span data-ttu-id="3b753-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="3b753-124">**Element**</span></span>|<span data-ttu-id="3b753-125">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3b753-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3b753-126">Suscribirse</span><span class="sxs-lookup"><span data-stu-id="3b753-126">Subscribe</span></span>](subscribe.md) <br/> |<span data-ttu-id="3b753-127">Contiene las propiedades que se usan para crear las suscripciones.</span><span class="sxs-lookup"><span data-stu-id="3b753-127">Contains the properties that are used to create subscriptions.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="3b753-128">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="3b753-128">Text value</span></span>

<span data-ttu-id="3b753-129">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="3b753-129">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3b753-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3b753-130">Remarks</span></span>

<span data-ttu-id="3b753-131">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda Exchange Web Services.This elemento fue introdujo en Exchange Server 2010 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="3b753-131">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3b753-132">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="3b753-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3b753-133">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3b753-133">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="3b753-134">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="3b753-134">Schema name</span></span>  <br/> |<span data-ttu-id="3b753-135">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="3b753-135">Messages schema</span></span>  <br/> |
|<span data-ttu-id="3b753-136">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="3b753-136">Validation file</span></span>  <br/> |<span data-ttu-id="3b753-137">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="3b753-137">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="3b753-138">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="3b753-138">Can be empty</span></span>  <br/> |<span data-ttu-id="3b753-139">False</span><span class="sxs-lookup"><span data-stu-id="3b753-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3b753-140">Ver también</span><span class="sxs-lookup"><span data-stu-id="3b753-140">See also</span></span>



[<span data-ttu-id="3b753-141">Operación de suscripción</span><span class="sxs-lookup"><span data-stu-id="3b753-141">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="3b753-142">Operación GetEvents</span><span class="sxs-lookup"><span data-stu-id="3b753-142">GetEvents operation</span></span>](getevents-operation.md)
  
[<span data-ttu-id="3b753-143">Operación GetStreamingEvents</span><span class="sxs-lookup"><span data-stu-id="3b753-143">GetStreamingEvents operation</span></span>](getstreamingevents-operation.md)
  
[<span data-ttu-id="3b753-144">Cancelar la operación de suscripción</span><span class="sxs-lookup"><span data-stu-id="3b753-144">Unsubscribe operation</span></span>](unsubscribe-operation.md)

