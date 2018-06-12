---
title: Marca de tiempo
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- TimeStamp
api_type:
- schema
ms.assetid: 5eae859a-5a74-4bf6-b196-d1b2fd38501a
description: El elemento de marca de tiempo representa la marca de hora de un evento de buzón de correo.
ms.openlocfilehash: d020d9a4cf3a128d26e0ff2b83be9f3deb024339
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19840719"
---
# <a name="timestamp"></a><span data-ttu-id="920fc-103">Marca de tiempo</span><span class="sxs-lookup"><span data-stu-id="920fc-103">TimeStamp</span></span>

<span data-ttu-id="920fc-104">El elemento de **marca de tiempo** representa la marca de hora de un evento de buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="920fc-104">The **Timestamp** element represents the timestamp of a mailbox event.</span></span> 
  
```xml
<TimeStamp/>
```

 <span data-ttu-id="920fc-105">**DateTime**</span><span class="sxs-lookup"><span data-stu-id="920fc-105">**DateTime**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="920fc-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="920fc-106">Attributes and elements</span></span>

<span data-ttu-id="920fc-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="920fc-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="920fc-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="920fc-108">Attributes</span></span>

<span data-ttu-id="920fc-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="920fc-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="920fc-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="920fc-110">Child elements</span></span>

<span data-ttu-id="920fc-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="920fc-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="920fc-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="920fc-112">Parent elements</span></span>

|<span data-ttu-id="920fc-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="920fc-113">**Element**</span></span>|<span data-ttu-id="920fc-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="920fc-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="920fc-115">CopiedEvent</span><span class="sxs-lookup"><span data-stu-id="920fc-115">CopiedEvent</span></span>](copiedevent.md) <br/> |<span data-ttu-id="920fc-116">Representa un evento donde se copia una carpeta o elemento.</span><span class="sxs-lookup"><span data-stu-id="920fc-116">Represents an event where an item or folder is copied.</span></span>  <br/> |
|[<span data-ttu-id="920fc-117">CreatedEvent</span><span class="sxs-lookup"><span data-stu-id="920fc-117">CreatedEvent</span></span>](createdevent.md) <br/> |<span data-ttu-id="920fc-118">Representa un evento que se crea una carpeta o elemento.</span><span class="sxs-lookup"><span data-stu-id="920fc-118">Represents an event where an item or folder is created.</span></span>  <br/> |
|[<span data-ttu-id="920fc-119">DeletedEvent</span><span class="sxs-lookup"><span data-stu-id="920fc-119">DeletedEvent</span></span>](deletedevent.md) <br/> |<span data-ttu-id="920fc-120">Representa un evento que se elimina un elemento o carpeta.</span><span class="sxs-lookup"><span data-stu-id="920fc-120">Represents an event where an item or folder is deleted.</span></span>  <br/> |
|[<span data-ttu-id="920fc-121">ModifiedEvent</span><span class="sxs-lookup"><span data-stu-id="920fc-121">ModifiedEvent</span></span>](modifiedevent.md) <br/> |<span data-ttu-id="920fc-122">Representa un evento que se modifica una carpeta o elemento.</span><span class="sxs-lookup"><span data-stu-id="920fc-122">Represents an event where an item or folder is modified.</span></span>  <br/> |
|[<span data-ttu-id="920fc-123">MovedEvent</span><span class="sxs-lookup"><span data-stu-id="920fc-123">MovedEvent</span></span>](movedevent.md) <br/> |<span data-ttu-id="920fc-124">Representa un evento donde una carpeta o elemento se mueve desde la carpeta principal de una a otra carpeta primaria.</span><span class="sxs-lookup"><span data-stu-id="920fc-124">Represents an event where an item or folder is moved from one parent folder to another parent folder.</span></span>  <br/> |
|[<span data-ttu-id="920fc-125">NewMailEvent</span><span class="sxs-lookup"><span data-stu-id="920fc-125">NewMailEvent</span></span>](newmailevent.md) <br/> |<span data-ttu-id="920fc-126">Representa un evento activado por un nuevo elemento de correo en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="920fc-126">Represents an event triggered by a new mail item in a mailbox.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="920fc-127">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="920fc-127">Text value</span></span>

<span data-ttu-id="920fc-128">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="920fc-128">This property is read-only.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="920fc-129">Notas</span><span class="sxs-lookup"><span data-stu-id="920fc-129">Remarks</span></span>

<span data-ttu-id="920fc-130">Este elemento está principalmente disponible para su uso en la determinación de cliente de la frecuencia de los eventos.</span><span class="sxs-lookup"><span data-stu-id="920fc-130">This element is primarily available for use in client determination of event frequency.</span></span> <span data-ttu-id="920fc-131">Esto no está presente en el [objeto StatusEvent](statusevent.md).</span><span class="sxs-lookup"><span data-stu-id="920fc-131">This is not present in [StatusEvent](statusevent.md).</span></span>
  
<span data-ttu-id="920fc-132">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="920fc-132">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="920fc-133">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="920fc-133">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="920fc-134">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="920fc-134">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="920fc-135">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="920fc-135">Schema name</span></span>  <br/> |<span data-ttu-id="920fc-136">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="920fc-136">Types schema</span></span>  <br/> |
|<span data-ttu-id="920fc-137">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="920fc-137">Validation file</span></span>  <br/> |<span data-ttu-id="920fc-138">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="920fc-138">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="920fc-139">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="920fc-139">Can be empty</span></span>  <br/> |<span data-ttu-id="920fc-140">False</span><span class="sxs-lookup"><span data-stu-id="920fc-140">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="920fc-141">Ver también</span><span class="sxs-lookup"><span data-stu-id="920fc-141">See also</span></span>



[<span data-ttu-id="920fc-142">Operación de suscripción</span><span class="sxs-lookup"><span data-stu-id="920fc-142">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="920fc-143">Operación GetEvents</span><span class="sxs-lookup"><span data-stu-id="920fc-143">GetEvents operation</span></span>](getevents-operation.md)
  
[<span data-ttu-id="920fc-144">Cancelar la operación de suscripción</span><span class="sxs-lookup"><span data-stu-id="920fc-144">Unsubscribe operation</span></span>](unsubscribe-operation.md)

