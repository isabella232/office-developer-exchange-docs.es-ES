---
title: DayOfWeek (TimeZone)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DayOfWeek
api_type:
- schema
ms.assetid: 416e8892-ebb1-4fac-82cf-e27549a6c175
description: El elemento DayOfWeek representa el día de la semana en el que se produce la transición de la zona horaria.
ms.openlocfilehash: 7816b90000be36cf3a3354d26d978684bfdcfe40
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764051"
---
# <a name="dayofweek-timezone"></a><span data-ttu-id="68997-103">DayOfWeek (TimeZone)</span><span class="sxs-lookup"><span data-stu-id="68997-103">DayOfWeek (TimeZone)</span></span>

<span data-ttu-id="68997-104">El elemento **DayOfWeek** representa el día de la semana en el que se produce la transición de la zona horaria.</span><span class="sxs-lookup"><span data-stu-id="68997-104">The **DayOfWeek** element represents the day of the week on which the time zone transition occurs.</span></span> 
  
```xml
<DayOfWeek>...</DayOfWeek>
```

<span data-ttu-id="68997-105">**DayOfWeekType**</span><span class="sxs-lookup"><span data-stu-id="68997-105">**DayOfWeekType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="68997-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="68997-106">Attributes and elements</span></span>

<span data-ttu-id="68997-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="68997-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="68997-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="68997-108">Attributes</span></span>

<span data-ttu-id="68997-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="68997-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="68997-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="68997-110">Child elements</span></span>

<span data-ttu-id="68997-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="68997-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="68997-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="68997-112">Parent elements</span></span>

|<span data-ttu-id="68997-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="68997-113">**Element**</span></span>|<span data-ttu-id="68997-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="68997-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="68997-115">StandardTime</span><span class="sxs-lookup"><span data-stu-id="68997-115">StandardTime</span></span>](standardtime.md) <br/> | <span data-ttu-id="68997-116">Representa un desplazamiento desde el momento en relación con hora Universal coordinada (UTC), representado por el elemento [Bias (UTC)](bias-utc.md) .</span><span class="sxs-lookup"><span data-stu-id="68997-116">Represents an offset from the time relative to Coordinated Universal Time (UTC) represented by the [Bias (UTC)](bias-utc.md) element.</span></span><br/><br/><span data-ttu-id="68997-117">Este elemento también contiene información sobre la transición a la hora estándar de horario de verano en regiones donde se observa el horario de verano.</span><span class="sxs-lookup"><span data-stu-id="68997-117">This element also contains information about the transition to standard time from daylight saving time in regions where daylight saving time is observed.</span></span><br/><br/><span data-ttu-id="68997-118">Los siguientes son las expresiones de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="68997-118">The following are the XPath expressions to this element:</span></span><br/><br/>`/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/TimeZone/StandardTime`<br/><br/>`/GetUserAvailabilityRequest/TimeZone/StandardTime` <br/> |
|[<span data-ttu-id="68997-119">DaylightTime</span><span class="sxs-lookup"><span data-stu-id="68997-119">DaylightTime</span></span>](daylighttime.md) <br/> | <span data-ttu-id="68997-120">Representa un desplazamiento de la hora con respecto a UTC representada por el elemento [Bias (UTC)](bias-utc.md) en las regiones donde se observa el horario de verano.</span><span class="sxs-lookup"><span data-stu-id="68997-120">Represents an offset from the time relative to UTC represented by the [Bias (UTC)](bias-utc.md) element in regions where daylight saving time is observed.</span></span><br/><br/><span data-ttu-id="68997-121">Este elemento también contiene información acerca de cuándo se produce la transición al horario de verano de tiempo estándar.</span><span class="sxs-lookup"><span data-stu-id="68997-121">This element also contains information about when the transition to daylight saving time from standard time occurs.</span></span><br/><br/><span data-ttu-id="68997-122">Los siguientes son las expresiones de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="68997-122">The following are the XPath expressions to this element:</span></span><br/><br/>`/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/TimeZone/DaylightTime`<br/><br/>`/GetUserAvailabilityRequest/TimeZone/DaylightTime` <br/> |
|[<span data-ttu-id="68997-123">RecurringDayTransition</span><span class="sxs-lookup"><span data-stu-id="68997-123">RecurringDayTransition</span></span>](recurringdaytransition.md) <br/> |<span data-ttu-id="68997-124">Representa una transición de la zona horaria que se produce en el mismo día cada año.</span><span class="sxs-lookup"><span data-stu-id="68997-124">Represents a time zone transition that occurs on the same day each year.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="68997-125">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="68997-125">Text value</span></span>

<span data-ttu-id="68997-126">Se requiere un valor de texto.</span><span class="sxs-lookup"><span data-stu-id="68997-126">A text value is required.</span></span> <span data-ttu-id="68997-127">El valor de texto está representado por una enumeración que tiene los siguientes valores posibles:</span><span class="sxs-lookup"><span data-stu-id="68997-127">The text value is represented by an enumeration that has the following possible values:</span></span>
  
- <span data-ttu-id="68997-128">Domingo</span><span class="sxs-lookup"><span data-stu-id="68997-128">Sunday</span></span>    
- <span data-ttu-id="68997-129">Lunes</span><span class="sxs-lookup"><span data-stu-id="68997-129">Monday</span></span>    
- <span data-ttu-id="68997-130">Martes</span><span class="sxs-lookup"><span data-stu-id="68997-130">Tuesday</span></span>    
- <span data-ttu-id="68997-131">Miércoles</span><span class="sxs-lookup"><span data-stu-id="68997-131">Wednesday</span></span>    
- <span data-ttu-id="68997-132">Jueves</span><span class="sxs-lookup"><span data-stu-id="68997-132">Thursday</span></span>    
- <span data-ttu-id="68997-133">Viernes</span><span class="sxs-lookup"><span data-stu-id="68997-133">Friday</span></span>    
- <span data-ttu-id="68997-134">Sábado</span><span class="sxs-lookup"><span data-stu-id="68997-134">Saturday</span></span>    
- <span data-ttu-id="68997-135">Día</span><span class="sxs-lookup"><span data-stu-id="68997-135">Day</span></span>    
- <span data-ttu-id="68997-136">Día de la semana</span><span class="sxs-lookup"><span data-stu-id="68997-136">Weekday</span></span>   
- <span data-ttu-id="68997-137">WeekendDay</span><span class="sxs-lookup"><span data-stu-id="68997-137">WeekendDay</span></span>
    
## <a name="remarks"></a><span data-ttu-id="68997-138">Notas</span><span class="sxs-lookup"><span data-stu-id="68997-138">Remarks</span></span>

<span data-ttu-id="68997-139">Un elemento [StandardTime](standardtime.md) que contiene un elemento [DayOrder](dayorder.md) que tiene un valor de 5, un elemento de [mes](month.md) que tiene un valor de 10 y un elemento **DayOfWeek** que tiene un valor del domingo significa la transición desde el horario estándar al horario de verano ahorro de tiempo se produce el domingo quinto del décimo mes.</span><span class="sxs-lookup"><span data-stu-id="68997-139">A [StandardTime](standardtime.md) element that contains a [DayOrder](dayorder.md) element that has a value of 5, a [Month](month.md) element that has a value of 10, and a **DayOfWeek** element that has a value of Sunday means that the transition from standard time to daylight saving time occurs on the fifth Sunday of the tenth month.</span></span> 
  
<span data-ttu-id="68997-140">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="68997-140">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="68997-141">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="68997-141">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="68997-142">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="68997-142">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="68997-143">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="68997-143">Schema Name</span></span>  <br/> |<span data-ttu-id="68997-144">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="68997-144">Types schema</span></span>  <br/> |
|<span data-ttu-id="68997-145">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="68997-145">Validation File</span></span>  <br/> |<span data-ttu-id="68997-146">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="68997-146">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="68997-147">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="68997-147">Can be Empty</span></span>  <br/> |<span data-ttu-id="68997-148">False</span><span class="sxs-lookup"><span data-stu-id="68997-148">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="68997-149">Ver también</span><span class="sxs-lookup"><span data-stu-id="68997-149">See also</span></span>

- [<span data-ttu-id="68997-150">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="68997-150">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
- [<span data-ttu-id="68997-151">Obtención de disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="68997-151">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

