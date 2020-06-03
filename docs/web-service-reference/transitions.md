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
description: El elemento Transitions representa una matriz de transiciones de zona horaria.
ms.openlocfilehash: d48fb8872b2f7e052f733c32e5dd1c9b4d04d898
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467441"
---
# <a name="transitions"></a><span data-ttu-id="fdf96-103">Transiciones</span><span class="sxs-lookup"><span data-stu-id="fdf96-103">Transitions</span></span>

<span data-ttu-id="fdf96-104">El elemento **Transitions** representa una matriz de transiciones de zona horaria.</span><span class="sxs-lookup"><span data-stu-id="fdf96-104">The **Transitions** element represents an array of time zone transitions.</span></span> 
  
```xml
<Transitions Id="">
   <Transition/>
   <AbsoluteDateTransition/>
   <RecurringDayTransition/>
   <RecurringDateTransition/>
</Transitions>
```

 <span data-ttu-id="fdf96-105">**ArrayOfTransitionsType**</span><span class="sxs-lookup"><span data-stu-id="fdf96-105">**ArrayOfTransitionsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="fdf96-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="fdf96-106">Attributes and elements</span></span>

<span data-ttu-id="fdf96-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="fdf96-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fdf96-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="fdf96-108">Attributes</span></span>

|<span data-ttu-id="fdf96-109">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="fdf96-109">**Attribute**</span></span>|<span data-ttu-id="fdf96-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="fdf96-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="fdf96-111">Id</span><span class="sxs-lookup"><span data-stu-id="fdf96-111">Id</span></span>  <br/> |<span data-ttu-id="fdf96-112">Representa el identificador único de la definición de zona horaria.</span><span class="sxs-lookup"><span data-stu-id="fdf96-112">Represents the unique identifier of the time zone definition.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="fdf96-113">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="fdf96-113">Child elements</span></span>

|<span data-ttu-id="fdf96-114">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="fdf96-114">**Element**</span></span>|<span data-ttu-id="fdf96-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="fdf96-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fdf96-116">AbsoluteDateTransition</span><span class="sxs-lookup"><span data-stu-id="fdf96-116">AbsoluteDateTransition</span></span>](absolutedatetransition.md) <br/> |<span data-ttu-id="fdf96-117">Representa una transición de zona horaria que se produce en una fecha específica y a una hora específica.</span><span class="sxs-lookup"><span data-stu-id="fdf96-117">Represents a time zone transition that occurs on a specific date and at a specific time.</span></span>  <br/> |
|[<span data-ttu-id="fdf96-118">RecurringDayTransition</span><span class="sxs-lookup"><span data-stu-id="fdf96-118">RecurringDayTransition</span></span>](recurringdaytransition.md) <br/> |<span data-ttu-id="fdf96-119">Representa una transición de zona horaria que se produce el mismo día cada año.</span><span class="sxs-lookup"><span data-stu-id="fdf96-119">Represents a time zone transition that occurs on the same day each year.</span></span>  <br/> |
|[<span data-ttu-id="fdf96-120">RecurringDateTransition</span><span class="sxs-lookup"><span data-stu-id="fdf96-120">RecurringDateTransition</span></span>](recurringdatetransition.md) <br/> |<span data-ttu-id="fdf96-121">Representa una transición de zona horaria que se produce en un día del año especificado.</span><span class="sxs-lookup"><span data-stu-id="fdf96-121">Represents a time zone transition that occurs on a specified day of the year.</span></span>  <br/> |
|[<span data-ttu-id="fdf96-122">Transición</span><span class="sxs-lookup"><span data-stu-id="fdf96-122">Transition</span></span>](transition.md) <br/> |<span data-ttu-id="fdf96-123">Representa una transición de zona horaria.</span><span class="sxs-lookup"><span data-stu-id="fdf96-123">Represents a time zone transition.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="fdf96-124">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="fdf96-124">Parent elements</span></span>

|<span data-ttu-id="fdf96-125">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="fdf96-125">**Element**</span></span>|<span data-ttu-id="fdf96-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="fdf96-126">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fdf96-127">StartTimeZone</span><span class="sxs-lookup"><span data-stu-id="fdf96-127">StartTimeZone</span></span>](starttimezone.md) <br/> |<span data-ttu-id="fdf96-128">Define la zona horaria de la hora de inicio de un [CalendarItem](calendaritem.md) o [MeetingRequest](meetingrequest.md).</span><span class="sxs-lookup"><span data-stu-id="fdf96-128">Defines the time zone for the start time of a [CalendarItem](calendaritem.md) or [MeetingRequest](meetingrequest.md).</span></span>  <br/> |
|[<span data-ttu-id="fdf96-129">EndTimeZone</span><span class="sxs-lookup"><span data-stu-id="fdf96-129">EndTimeZone</span></span>](endtimezone.md) <br/> |<span data-ttu-id="fdf96-130">Define la zona horaria de la hora de finalización de [CalendarItem](calendaritem.md) o [MeetingRequest](meetingrequest.md).</span><span class="sxs-lookup"><span data-stu-id="fdf96-130">Defines the time zone for the end time of a [CalendarItem](calendaritem.md) or [MeetingRequest](meetingrequest.md).</span></span>  <br/> |
|[<span data-ttu-id="fdf96-131">TimeZoneDefinition</span><span class="sxs-lookup"><span data-stu-id="fdf96-131">TimeZoneDefinition</span></span>](timezonedefinition.md) <br/> |<span data-ttu-id="fdf96-132">Define una zona horaria.</span><span class="sxs-lookup"><span data-stu-id="fdf96-132">Defines a time zone.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="fdf96-133">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="fdf96-133">Text value</span></span>

<span data-ttu-id="fdf96-134">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="fdf96-134">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="fdf96-135">Comentarios</span><span class="sxs-lookup"><span data-stu-id="fdf96-135">Remarks</span></span>

<span data-ttu-id="fdf96-136">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="fdf96-136">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fdf96-137">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="fdf96-137">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fdf96-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="fdf96-138">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="fdf96-139">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="fdf96-139">Schema Name</span></span>  <br/> |<span data-ttu-id="fdf96-140">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="fdf96-140">Types schema</span></span>  <br/> |
|<span data-ttu-id="fdf96-141">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="fdf96-141">Validation File</span></span>  <br/> |<span data-ttu-id="fdf96-142">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="fdf96-142">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="fdf96-143">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="fdf96-143">Can be Empty</span></span>  <br/> |<span data-ttu-id="fdf96-144">Falso</span><span class="sxs-lookup"><span data-stu-id="fdf96-144">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fdf96-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="fdf96-145">See also</span></span>



- [<span data-ttu-id="fdf96-146">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="fdf96-146">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

