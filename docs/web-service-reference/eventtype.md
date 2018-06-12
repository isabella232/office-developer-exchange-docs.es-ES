---
title: EventType
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- EventType
api_type:
- schema
ms.assetid: 04b70f9e-c226-4130-958e-0db0275cf58b
description: El elemento EventType se usa para crear una suscripción e identifica un tipo de evento que se notificará en una notificación.
ms.openlocfilehash: fb54c9e042f105d10e68cb0e9b48feae7ed8bf7b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764452"
---
# <a name="eventtype"></a><span data-ttu-id="b83a0-103">EventType</span><span class="sxs-lookup"><span data-stu-id="b83a0-103">EventType</span></span>

<span data-ttu-id="b83a0-104">El elemento **EventType** se usa para crear una suscripción e identifica un tipo de evento que se notificará en una notificación.</span><span class="sxs-lookup"><span data-stu-id="b83a0-104">The **EventType** element is used to create a subscription and identifies an event type to be reported in a notification.</span></span> 
  
```xml
<EventType/>
```

 <span data-ttu-id="b83a0-105">**NotificationEventTypeType**</span><span class="sxs-lookup"><span data-stu-id="b83a0-105">**NotificationEventTypeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b83a0-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="b83a0-106">Attributes and elements</span></span>

<span data-ttu-id="b83a0-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="b83a0-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b83a0-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="b83a0-108">Attributes</span></span>

<span data-ttu-id="b83a0-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="b83a0-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b83a0-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b83a0-110">Child elements</span></span>

<span data-ttu-id="b83a0-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="b83a0-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="b83a0-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="b83a0-112">Parent elements</span></span>

|<span data-ttu-id="b83a0-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="b83a0-113">**Element**</span></span>|<span data-ttu-id="b83a0-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b83a0-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b83a0-115">Debe establecer</span><span class="sxs-lookup"><span data-stu-id="b83a0-115">EventTypes</span></span>](eventtypes.md) <br/> |<span data-ttu-id="b83a0-116">Contiene una colección de tipos de eventos de notificación de evento que se usan para crear una suscripción.</span><span class="sxs-lookup"><span data-stu-id="b83a0-116">Contains a collection of event notification event types that are used to create a subscription.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="b83a0-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="b83a0-117">Text value</span></span>

<span data-ttu-id="b83a0-118">Se requiere un valor de texto.</span><span class="sxs-lookup"><span data-stu-id="b83a0-118">A text value is required.</span></span> <span data-ttu-id="b83a0-119">Los valores posibles son:</span><span class="sxs-lookup"><span data-stu-id="b83a0-119">The following are the possible values:</span></span>
  
- <span data-ttu-id="b83a0-120">CopiedEvent</span><span class="sxs-lookup"><span data-stu-id="b83a0-120">CopiedEvent</span></span>
    
- <span data-ttu-id="b83a0-121">CreatedEvent</span><span class="sxs-lookup"><span data-stu-id="b83a0-121">CreatedEvent</span></span>
    
- <span data-ttu-id="b83a0-122">DeletedEvent</span><span class="sxs-lookup"><span data-stu-id="b83a0-122">DeletedEvent</span></span>
    
- <span data-ttu-id="b83a0-123">ModifiedEvent</span><span class="sxs-lookup"><span data-stu-id="b83a0-123">ModifiedEvent</span></span>
    
- <span data-ttu-id="b83a0-124">MovedEvent</span><span class="sxs-lookup"><span data-stu-id="b83a0-124">MovedEvent</span></span>
    
- <span data-ttu-id="b83a0-125">NewMailEvent</span><span class="sxs-lookup"><span data-stu-id="b83a0-125">NewMailEvent</span></span>
    
- <span data-ttu-id="b83a0-126">FreeBusyChangedEvent</span><span class="sxs-lookup"><span data-stu-id="b83a0-126">FreeBusyChangedEvent</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b83a0-127">Notas</span><span class="sxs-lookup"><span data-stu-id="b83a0-127">Remarks</span></span>

<span data-ttu-id="b83a0-128">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda Exchange Web Services.This elemento fue introdujo en Exchange Server 2010 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="b83a0-128">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b83a0-129">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="b83a0-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b83a0-130">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b83a0-130">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="b83a0-131">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="b83a0-131">Schema Name</span></span>  <br/> |<span data-ttu-id="b83a0-132">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="b83a0-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="b83a0-133">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="b83a0-133">Validation File</span></span>  <br/> |<span data-ttu-id="b83a0-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="b83a0-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="b83a0-135">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="b83a0-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="b83a0-136">False</span><span class="sxs-lookup"><span data-stu-id="b83a0-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b83a0-137">Ver también</span><span class="sxs-lookup"><span data-stu-id="b83a0-137">See also</span></span>



[<span data-ttu-id="b83a0-138">Operación de suscripción</span><span class="sxs-lookup"><span data-stu-id="b83a0-138">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="b83a0-139">Operación GetEvents</span><span class="sxs-lookup"><span data-stu-id="b83a0-139">GetEvents operation</span></span>](getevents-operation.md)
  
[<span data-ttu-id="b83a0-140">Cancelar la operación de suscripción</span><span class="sxs-lookup"><span data-stu-id="b83a0-140">Unsubscribe operation</span></span>](unsubscribe-operation.md)

