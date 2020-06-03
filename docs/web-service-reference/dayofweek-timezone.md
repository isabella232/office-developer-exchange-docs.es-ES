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
description: El elemento DayOfWeek representa el día de la semana en el que se produce la transición de zona horaria.
ms.openlocfilehash: 7bc05f417268ccfb20adae12e2694d8360023ab2
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457847"
---
# <a name="dayofweek-timezone"></a><span data-ttu-id="d8118-103">DayOfWeek (TimeZone)</span><span class="sxs-lookup"><span data-stu-id="d8118-103">DayOfWeek (TimeZone)</span></span>

<span data-ttu-id="d8118-104">El elemento **DayOfWeek** representa el día de la semana en el que se produce la transición de zona horaria.</span><span class="sxs-lookup"><span data-stu-id="d8118-104">The **DayOfWeek** element represents the day of the week on which the time zone transition occurs.</span></span> 
  
```xml
<DayOfWeek>...</DayOfWeek>
```

<span data-ttu-id="d8118-105">**DayOfWeekType**</span><span class="sxs-lookup"><span data-stu-id="d8118-105">**DayOfWeekType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="d8118-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="d8118-106">Attributes and elements</span></span>

<span data-ttu-id="d8118-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="d8118-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d8118-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="d8118-108">Attributes</span></span>

<span data-ttu-id="d8118-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="d8118-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d8118-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="d8118-110">Child elements</span></span>

<span data-ttu-id="d8118-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="d8118-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="d8118-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="d8118-112">Parent elements</span></span>

|<span data-ttu-id="d8118-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="d8118-113">**Element**</span></span>|<span data-ttu-id="d8118-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d8118-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d8118-115">Standardtime Element</span><span class="sxs-lookup"><span data-stu-id="d8118-115">StandardTime</span></span>](standardtime.md) <br/> | <span data-ttu-id="d8118-116">Representa un desplazamiento del tiempo con respecto a la hora universal coordinada (UTC) representada por el elemento [Bias (UTC)](bias-utc.md) .</span><span class="sxs-lookup"><span data-stu-id="d8118-116">Represents an offset from the time relative to Coordinated Universal Time (UTC) represented by the [Bias (UTC)](bias-utc.md) element.</span></span><br/><br/><span data-ttu-id="d8118-117">Este elemento también contiene información sobre la transición a la hora estándar del horario de verano en regiones en las que se observa el horario de verano.</span><span class="sxs-lookup"><span data-stu-id="d8118-117">This element also contains information about the transition to standard time from daylight saving time in regions where daylight saving time is observed.</span></span><br/><br/><span data-ttu-id="d8118-118">Las siguientes son las expresiones XPath de este elemento:</span><span class="sxs-lookup"><span data-stu-id="d8118-118">The following are the XPath expressions to this element:</span></span><br/><br/>`/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/TimeZone/StandardTime`<br/><br/>`/GetUserAvailabilityRequest/TimeZone/StandardTime` <br/> |
|[<span data-ttu-id="d8118-119">DaylightTime</span><span class="sxs-lookup"><span data-stu-id="d8118-119">DaylightTime</span></span>](daylighttime.md) <br/> | <span data-ttu-id="d8118-120">Representa un desplazamiento del tiempo relativo a la hora UTC representado por el elemento [Bias (UTC)](bias-utc.md) en las regiones en las que se observa el horario de verano.</span><span class="sxs-lookup"><span data-stu-id="d8118-120">Represents an offset from the time relative to UTC represented by the [Bias (UTC)](bias-utc.md) element in regions where daylight saving time is observed.</span></span><br/><br/><span data-ttu-id="d8118-121">Este elemento también contiene información sobre cuándo se produce la transición al horario de verano desde la hora estándar.</span><span class="sxs-lookup"><span data-stu-id="d8118-121">This element also contains information about when the transition to daylight saving time from standard time occurs.</span></span><br/><br/><span data-ttu-id="d8118-122">Las siguientes son las expresiones XPath de este elemento:</span><span class="sxs-lookup"><span data-stu-id="d8118-122">The following are the XPath expressions to this element:</span></span><br/><br/>`/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/TimeZone/DaylightTime`<br/><br/>`/GetUserAvailabilityRequest/TimeZone/DaylightTime` <br/> |
|[<span data-ttu-id="d8118-123">RecurringDayTransition</span><span class="sxs-lookup"><span data-stu-id="d8118-123">RecurringDayTransition</span></span>](recurringdaytransition.md) <br/> |<span data-ttu-id="d8118-124">Representa una transición de zona horaria que se produce el mismo día cada año.</span><span class="sxs-lookup"><span data-stu-id="d8118-124">Represents a time zone transition that occurs on the same day each year.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="d8118-125">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="d8118-125">Text value</span></span>

<span data-ttu-id="d8118-126">Se requiere un valor de texto.</span><span class="sxs-lookup"><span data-stu-id="d8118-126">A text value is required.</span></span> <span data-ttu-id="d8118-127">El valor de texto se representa mediante una enumeración que tiene los siguientes valores posibles:</span><span class="sxs-lookup"><span data-stu-id="d8118-127">The text value is represented by an enumeration that has the following possible values:</span></span>
  
- <span data-ttu-id="d8118-128">Domingo</span><span class="sxs-lookup"><span data-stu-id="d8118-128">Sunday</span></span>    
- <span data-ttu-id="d8118-129">lunes</span><span class="sxs-lookup"><span data-stu-id="d8118-129">Monday</span></span>    
- <span data-ttu-id="d8118-130">martes</span><span class="sxs-lookup"><span data-stu-id="d8118-130">Tuesday</span></span>    
- <span data-ttu-id="d8118-131">miércoles</span><span class="sxs-lookup"><span data-stu-id="d8118-131">Wednesday</span></span>    
- <span data-ttu-id="d8118-132">jueves</span><span class="sxs-lookup"><span data-stu-id="d8118-132">Thursday</span></span>    
- <span data-ttu-id="d8118-133">viernes</span><span class="sxs-lookup"><span data-stu-id="d8118-133">Friday</span></span>    
- <span data-ttu-id="d8118-134">Sábado</span><span class="sxs-lookup"><span data-stu-id="d8118-134">Saturday</span></span>    
- <span data-ttu-id="d8118-135">Day</span><span class="sxs-lookup"><span data-stu-id="d8118-135">Day</span></span>    
- <span data-ttu-id="d8118-136">Día de la semana</span><span class="sxs-lookup"><span data-stu-id="d8118-136">Weekday</span></span>   
- <span data-ttu-id="d8118-137">WeekendDay</span><span class="sxs-lookup"><span data-stu-id="d8118-137">WeekendDay</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d8118-138">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d8118-138">Remarks</span></span>

<span data-ttu-id="d8118-139">Un elemento [standardtime Element](standardtime.md) que contiene un elemento [DayOrder](dayorder.md) que tiene un valor de 5, un elemento [Month](month.md) que tiene un valor de 10 y un elemento **DayOfWeek** que tiene un valor de domingo, significa que la transición de la hora estándar al horario de verano se produce el quinto domingo del décimo mes.</span><span class="sxs-lookup"><span data-stu-id="d8118-139">A [StandardTime](standardtime.md) element that contains a [DayOrder](dayorder.md) element that has a value of 5, a [Month](month.md) element that has a value of 10, and a **DayOfWeek** element that has a value of Sunday means that the transition from standard time to daylight saving time occurs on the fifth Sunday of the tenth month.</span></span> 
  
<span data-ttu-id="d8118-140">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="d8118-140">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d8118-141">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="d8118-141">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d8118-142">Namespace</span><span class="sxs-lookup"><span data-stu-id="d8118-142">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d8118-143">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="d8118-143">Schema Name</span></span>  <br/> |<span data-ttu-id="d8118-144">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="d8118-144">Types schema</span></span>  <br/> |
|<span data-ttu-id="d8118-145">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="d8118-145">Validation File</span></span>  <br/> |<span data-ttu-id="d8118-146">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="d8118-146">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d8118-147">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="d8118-147">Can be Empty</span></span>  <br/> |<span data-ttu-id="d8118-148">Falso</span><span class="sxs-lookup"><span data-stu-id="d8118-148">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d8118-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="d8118-149">See also</span></span>

- [<span data-ttu-id="d8118-150">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="d8118-150">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
- [<span data-ttu-id="d8118-151">Obtener disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="d8118-151">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

