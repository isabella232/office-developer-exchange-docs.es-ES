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
description: El elemento EventType se usa para crear una suscripción e identifica un tipo de evento que se va a notificar en una notificación.
ms.openlocfilehash: 58c7ce571434b6fb8ac0b1dc2a3f8cd4fd56ff17
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526175"
---
# <a name="eventtype"></a><span data-ttu-id="d68dd-103">EventType</span><span class="sxs-lookup"><span data-stu-id="d68dd-103">EventType</span></span>

<span data-ttu-id="d68dd-104">El elemento **EventType** se usa para crear una suscripción e identifica un tipo de evento que se va a notificar en una notificación.</span><span class="sxs-lookup"><span data-stu-id="d68dd-104">The **EventType** element is used to create a subscription and identifies an event type to be reported in a notification.</span></span> 
  
```xml
<EventType/>
```

 <span data-ttu-id="d68dd-105">**NotificationEventTypeType**</span><span class="sxs-lookup"><span data-stu-id="d68dd-105">**NotificationEventTypeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d68dd-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="d68dd-106">Attributes and elements</span></span>

<span data-ttu-id="d68dd-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="d68dd-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d68dd-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="d68dd-108">Attributes</span></span>

<span data-ttu-id="d68dd-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="d68dd-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d68dd-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="d68dd-110">Child elements</span></span>

<span data-ttu-id="d68dd-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="d68dd-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="d68dd-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="d68dd-112">Parent elements</span></span>

|<span data-ttu-id="d68dd-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="d68dd-113">**Element**</span></span>|<span data-ttu-id="d68dd-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d68dd-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d68dd-115">EventTypes</span><span class="sxs-lookup"><span data-stu-id="d68dd-115">EventTypes</span></span>](eventtypes.md) <br/> |<span data-ttu-id="d68dd-116">Contiene una colección de tipos de eventos de notificación de eventos que se usan para crear una suscripción.</span><span class="sxs-lookup"><span data-stu-id="d68dd-116">Contains a collection of event notification event types that are used to create a subscription.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="d68dd-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="d68dd-117">Text value</span></span>

<span data-ttu-id="d68dd-118">Se requiere un valor de texto.</span><span class="sxs-lookup"><span data-stu-id="d68dd-118">A text value is required.</span></span> <span data-ttu-id="d68dd-119">Los valores posibles son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="d68dd-119">The following are the possible values:</span></span>
  
- <span data-ttu-id="d68dd-120">CopiedEvent</span><span class="sxs-lookup"><span data-stu-id="d68dd-120">CopiedEvent</span></span>
    
- <span data-ttu-id="d68dd-121">CreatedEvent</span><span class="sxs-lookup"><span data-stu-id="d68dd-121">CreatedEvent</span></span>
    
- <span data-ttu-id="d68dd-122">DeletedEvent</span><span class="sxs-lookup"><span data-stu-id="d68dd-122">DeletedEvent</span></span>
    
- <span data-ttu-id="d68dd-123">ModifiedEvent</span><span class="sxs-lookup"><span data-stu-id="d68dd-123">ModifiedEvent</span></span>
    
- <span data-ttu-id="d68dd-124">MovedEvent</span><span class="sxs-lookup"><span data-stu-id="d68dd-124">MovedEvent</span></span>
    
- <span data-ttu-id="d68dd-125">NewMailEvent</span><span class="sxs-lookup"><span data-stu-id="d68dd-125">NewMailEvent</span></span>
    
- <span data-ttu-id="d68dd-126">FreeBusyChangedEvent</span><span class="sxs-lookup"><span data-stu-id="d68dd-126">FreeBusyChangedEvent</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d68dd-127">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d68dd-127">Remarks</span></span>

<span data-ttu-id="d68dd-128">El esquema que describe este elemento se encuentra en el directorio virtual de IIS que hospeda los servicios Web de Exchange. este elemento se introdujo en Exchange Server 2010 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="d68dd-128">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d68dd-129">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="d68dd-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d68dd-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="d68dd-130">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d68dd-131">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="d68dd-131">Schema Name</span></span>  <br/> |<span data-ttu-id="d68dd-132">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="d68dd-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="d68dd-133">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="d68dd-133">Validation File</span></span>  <br/> |<span data-ttu-id="d68dd-134">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="d68dd-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d68dd-135">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="d68dd-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="d68dd-136">Falso</span><span class="sxs-lookup"><span data-stu-id="d68dd-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d68dd-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="d68dd-137">See also</span></span>



[<span data-ttu-id="d68dd-138">Operación subscribe</span><span class="sxs-lookup"><span data-stu-id="d68dd-138">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="d68dd-139">Operación GetEvents</span><span class="sxs-lookup"><span data-stu-id="d68dd-139">GetEvents operation</span></span>](getevents-operation.md)
  
[<span data-ttu-id="d68dd-140">Operación unsubscribe</span><span class="sxs-lookup"><span data-stu-id="d68dd-140">Unsubscribe operation</span></span>](unsubscribe-operation.md)

