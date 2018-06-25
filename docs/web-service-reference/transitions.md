---
title: Transiciones
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Transitions
api_type:
- schema
ms.assetid: 26f38f1c-96a3-440e-805c-1437886d11c5
description: El elemento transiciones representa una matriz de las transiciones de zona horaria.
ms.openlocfilehash: df7cacdef71c3fdfaa3ecadb486843ea30e6109d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19840723"
---
# <a name="transitions"></a><span data-ttu-id="a36b1-103">Transiciones</span><span class="sxs-lookup"><span data-stu-id="a36b1-103">Transitions</span></span>

<span data-ttu-id="a36b1-104">El elemento **transiciones** representa una matriz de las transiciones de zona horaria.</span><span class="sxs-lookup"><span data-stu-id="a36b1-104">The **Transitions** element represents an array of time zone transitions.</span></span> 
  
```xml
<Transitions Id="">
   <Transition/>
   <AbsoluteDateTransition/>
   <RecurringDayTransition/>
   <RecurringDateTransition/>
</Transitions>
```

 <span data-ttu-id="a36b1-105">**ArrayOfTransitionsType**</span><span class="sxs-lookup"><span data-stu-id="a36b1-105">**ArrayOfTransitionsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a36b1-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="a36b1-106">Attributes and elements</span></span>

<span data-ttu-id="a36b1-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="a36b1-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a36b1-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="a36b1-108">Attributes</span></span>

|<span data-ttu-id="a36b1-109">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="a36b1-109">**Attribute**</span></span>|<span data-ttu-id="a36b1-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a36b1-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a36b1-111">Id</span><span class="sxs-lookup"><span data-stu-id="a36b1-111">Id</span></span>  <br/> |<span data-ttu-id="a36b1-112">Representa el identificador único de la definición de zona horaria.</span><span class="sxs-lookup"><span data-stu-id="a36b1-112">Represents the unique identifier of the time zone definition.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="a36b1-113">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="a36b1-113">Child elements</span></span>

|<span data-ttu-id="a36b1-114">**Element**</span><span class="sxs-lookup"><span data-stu-id="a36b1-114">**Element**</span></span>|<span data-ttu-id="a36b1-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a36b1-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a36b1-116">AbsoluteDateTransition</span><span class="sxs-lookup"><span data-stu-id="a36b1-116">AbsoluteDateTransition</span></span>](absolutedatetransition.md) <br/> |<span data-ttu-id="a36b1-117">Representa una transición de la zona horaria que se produce en una fecha específica y a una hora específica.</span><span class="sxs-lookup"><span data-stu-id="a36b1-117">Represents a time zone transition that occurs on a specific date and at a specific time.</span></span>  <br/> |
|[<span data-ttu-id="a36b1-118">RecurringDayTransition</span><span class="sxs-lookup"><span data-stu-id="a36b1-118">RecurringDayTransition</span></span>](recurringdaytransition.md) <br/> |<span data-ttu-id="a36b1-119">Representa una transición de la zona horaria que se produce en el mismo día cada año.</span><span class="sxs-lookup"><span data-stu-id="a36b1-119">Represents a time zone transition that occurs on the same day each year.</span></span>  <br/> |
|[<span data-ttu-id="a36b1-120">RecurringDateTransition</span><span class="sxs-lookup"><span data-stu-id="a36b1-120">RecurringDateTransition</span></span>](recurringdatetransition.md) <br/> |<span data-ttu-id="a36b1-121">Representa una transición de la zona horaria que se produce en un día del año especificado.</span><span class="sxs-lookup"><span data-stu-id="a36b1-121">Represents a time zone transition that occurs on a specified day of the year.</span></span>  <br/> |
|[<span data-ttu-id="a36b1-122">Transición</span><span class="sxs-lookup"><span data-stu-id="a36b1-122">Transition</span></span>](transition.md) <br/> |<span data-ttu-id="a36b1-123">Representa una transición de la zona horaria.</span><span class="sxs-lookup"><span data-stu-id="a36b1-123">Represents a time zone transition.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="a36b1-124">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="a36b1-124">Parent elements</span></span>

|<span data-ttu-id="a36b1-125">**Element**</span><span class="sxs-lookup"><span data-stu-id="a36b1-125">**Element**</span></span>|<span data-ttu-id="a36b1-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a36b1-126">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a36b1-127">StartTimeZone</span><span class="sxs-lookup"><span data-stu-id="a36b1-127">StartTimeZone</span></span>](starttimezone.md) <br/> |<span data-ttu-id="a36b1-128">Define la zona horaria de la hora de inicio de un [CalendarItem](calendaritem.md) o [MeetingRequest](meetingrequest.md).</span><span class="sxs-lookup"><span data-stu-id="a36b1-128">Defines the time zone for the start time of a [CalendarItem](calendaritem.md) or [MeetingRequest](meetingrequest.md).</span></span>  <br/> |
|[<span data-ttu-id="a36b1-129">EndTimeZone</span><span class="sxs-lookup"><span data-stu-id="a36b1-129">EndTimeZone</span></span>](endtimezone.md) <br/> |<span data-ttu-id="a36b1-130">Define la zona horaria de la hora de finalización de un [CalendarItem](calendaritem.md) o [MeetingRequest](meetingrequest.md).</span><span class="sxs-lookup"><span data-stu-id="a36b1-130">Defines the time zone for the end time of a [CalendarItem](calendaritem.md) or [MeetingRequest](meetingrequest.md).</span></span>  <br/> |
|[<span data-ttu-id="a36b1-131">Definición de zona horaria</span><span class="sxs-lookup"><span data-stu-id="a36b1-131">TimeZoneDefinition</span></span>](timezonedefinition.md) <br/> |<span data-ttu-id="a36b1-132">Define una zona horaria.</span><span class="sxs-lookup"><span data-stu-id="a36b1-132">Defines a time zone.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="a36b1-133">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="a36b1-133">Text value</span></span>

<span data-ttu-id="a36b1-134">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="a36b1-134">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a36b1-135">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a36b1-135">Remarks</span></span>

<span data-ttu-id="a36b1-136">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="a36b1-136">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a36b1-137">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="a36b1-137">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a36b1-138">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a36b1-138">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a36b1-139">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="a36b1-139">Schema Name</span></span>  <br/> |<span data-ttu-id="a36b1-140">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="a36b1-140">Types schema</span></span>  <br/> |
|<span data-ttu-id="a36b1-141">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="a36b1-141">Validation File</span></span>  <br/> |<span data-ttu-id="a36b1-142">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="a36b1-142">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="a36b1-143">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="a36b1-143">Can be Empty</span></span>  <br/> |<span data-ttu-id="a36b1-144">False</span><span class="sxs-lookup"><span data-stu-id="a36b1-144">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a36b1-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="a36b1-145">See also</span></span>



- [<span data-ttu-id="a36b1-146">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="a36b1-146">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

