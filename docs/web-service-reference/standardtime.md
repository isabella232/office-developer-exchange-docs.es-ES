---
title: StandardTime
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- StandardTime
api_type:
- schema
ms.assetid: 13084726-ab24-4009-be99-c4a4273c9e05
description: El elemento StandardTime representa un desplazamiento desde el momento en relación con hora Universal coordinada (UTC) que está representada por el elemento Bias (UTC). Este elemento también contiene información sobre la transición a la hora estándar de horario de verano en regiones donde se observa el horario de verano.
ms.openlocfilehash: 726c31ffba06c1c437711b88444ec5eba45b520d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19837546"
---
# <a name="standardtime"></a><span data-ttu-id="2d0f7-104">StandardTime</span><span class="sxs-lookup"><span data-stu-id="2d0f7-104">StandardTime</span></span>

<span data-ttu-id="2d0f7-105">El elemento **StandardTime** representa un desplazamiento desde el momento en relación con hora Universal coordinada (UTC) que está representada por el elemento [Bias (UTC)](bias-utc.md) .</span><span class="sxs-lookup"><span data-stu-id="2d0f7-105">The **StandardTime** element represents an offset from the time relative to Coordinated Universal Time (UTC) that is represented by the [Bias (UTC)](bias-utc.md) element.</span></span> <span data-ttu-id="2d0f7-106">Este elemento también contiene información sobre la transición a la hora estándar de horario de verano en regiones donde se observa el horario de verano.</span><span class="sxs-lookup"><span data-stu-id="2d0f7-106">This element also contains information about the transition to standard time from daylight saving time in regions where daylight saving time is observed.</span></span> 
  
- [<span data-ttu-id="2d0f7-107">TimeZone (disponibilidad)</span><span class="sxs-lookup"><span data-stu-id="2d0f7-107">TimeZone (Availability)</span></span>](timezone-availability.md)
- [<span data-ttu-id="2d0f7-108">StandardTime</span><span class="sxs-lookup"><span data-stu-id="2d0f7-108">StandardTime</span></span>](standardtime.md)
  
```xml
<StandardTime>
   <Bias>int</Bias>
   <Time>string</Time>
   <DayOrder>short</DayOrder>
   <Month>short</Month>
   <DayOfWeek>Sunday or Monday or Tuesday or Wednesday or Thursday or Friday or Saturday</DayOfWeek>
   <Year>string</Year>
</StandardTime>
```

 <span data-ttu-id="2d0f7-109">**SerializableTimeZoneTime**</span><span class="sxs-lookup"><span data-stu-id="2d0f7-109">**SerializableTimeZoneTime**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2d0f7-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="2d0f7-110">Attributes and elements</span></span>

<span data-ttu-id="2d0f7-111">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="2d0f7-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2d0f7-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="2d0f7-112">Attributes</span></span>

<span data-ttu-id="2d0f7-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="2d0f7-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2d0f7-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="2d0f7-114">Child elements</span></span>

|<span data-ttu-id="2d0f7-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="2d0f7-115">**Element**</span></span>|<span data-ttu-id="2d0f7-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2d0f7-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2d0f7-117">Bias</span><span class="sxs-lookup"><span data-stu-id="2d0f7-117">Bias</span></span>](bias.md) <br/> |<span data-ttu-id="2d0f7-118">Representa el desplazamiento desde el desplazamiento de UTC que se identifica con el elemento [Bias (UTC)](bias-utc.md) para la hora estándar y el horario de verano.</span><span class="sxs-lookup"><span data-stu-id="2d0f7-118">Represents the offset from the UTC offset that is identified by the [Bias (UTC)](bias-utc.md) element for standard time and daylight saving time.</span></span> <span data-ttu-id="2d0f7-119">Este valor está en minutos.</span><span class="sxs-lookup"><span data-stu-id="2d0f7-119">This value is in minutes.</span></span>  <br/> |
|[<span data-ttu-id="2d0f7-120">Time</span><span class="sxs-lookup"><span data-stu-id="2d0f7-120">Time</span></span>](time.md) <br/> |<span data-ttu-id="2d0f7-121">Representa el tiempo de transición del día a y desde el horario estándar y del horario de verano.</span><span class="sxs-lookup"><span data-stu-id="2d0f7-121">Represents the transition time of day to and from standard time and daylight saving time.</span></span>  <br/> |
|[<span data-ttu-id="2d0f7-122">DayOrder</span><span class="sxs-lookup"><span data-stu-id="2d0f7-122">DayOrder</span></span>](dayorder.md) <br/> |<span data-ttu-id="2d0f7-123">Representa la aparición de _n_th del día que se especifica en el elemento [DayOfWeek (TimeZone)](dayofweek-timezone.md) que representa la fecha de transición desde y a la hora estándar y el horario de verano.</span><span class="sxs-lookup"><span data-stu-id="2d0f7-123">Represents the  _n_th occurrence of the day that is specified in the [DayOfWeek (TimeZone)](dayofweek-timezone.md) element that represents the date of transition from and to standard time and daylight saving time.</span></span>  <br/> |
|[<span data-ttu-id="2d0f7-124">Month</span><span class="sxs-lookup"><span data-stu-id="2d0f7-124">Month</span></span>](month.md) <br/> |<span data-ttu-id="2d0f7-125">Representa el mes de transición del año a y desde el horario estándar y del horario de verano.</span><span class="sxs-lookup"><span data-stu-id="2d0f7-125">Represents the transition month of the year to and from standard time and daylight saving time.</span></span>  <br/> |
|[<span data-ttu-id="2d0f7-126">DayOfWeek (TimeZone)</span><span class="sxs-lookup"><span data-stu-id="2d0f7-126">DayOfWeek (TimeZone)</span></span>](dayofweek-timezone.md) <br/> |<span data-ttu-id="2d0f7-127">Representa el día de la semana cuando se produce la transición a y desde el horario estándar y del horario de verano.</span><span class="sxs-lookup"><span data-stu-id="2d0f7-127">Represents the day of the week when the transition to and from standard time and daylight saving time occurs.</span></span>  <br/> |
|[<span data-ttu-id="2d0f7-128">year</span><span class="sxs-lookup"><span data-stu-id="2d0f7-128">Year</span></span>](year.md) <br/> |<span data-ttu-id="2d0f7-129">Define una zona horaria que cambia según el año.</span><span class="sxs-lookup"><span data-stu-id="2d0f7-129">Defines a time zone that changes depending on the year.</span></span> <span data-ttu-id="2d0f7-130">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="2d0f7-130">This element is optional.</span></span> <span data-ttu-id="2d0f7-131">Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="2d0f7-131">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="2d0f7-132">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="2d0f7-132">Parent elements</span></span>

|<span data-ttu-id="2d0f7-133">**Element**</span><span class="sxs-lookup"><span data-stu-id="2d0f7-133">**Element**</span></span>|<span data-ttu-id="2d0f7-134">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2d0f7-134">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2d0f7-135">TimeZone (disponibilidad)</span><span class="sxs-lookup"><span data-stu-id="2d0f7-135">TimeZone (Availability)</span></span>](timezone-availability.md) <br/> | <span data-ttu-id="2d0f7-136">Contiene elementos que identifican la información de zona horaria.</span><span class="sxs-lookup"><span data-stu-id="2d0f7-136">Contains elements that identify time zone information.</span></span> <span data-ttu-id="2d0f7-137">Este elemento también contiene información sobre la transición entre la hora estándar y el horario de verano.</span><span class="sxs-lookup"><span data-stu-id="2d0f7-137">This element also contains information about the transition between standard time and daylight saving time.</span></span> <br/><br/><span data-ttu-id="2d0f7-138">Los siguientes son las expresiones de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="2d0f7-138">The following are the XPath expressions to this element:</span></span> <br/> <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/TimeZone` <br/> <br/> `/GetUserAvailabilityRequest/TimeZone` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2d0f7-139">Notas</span><span class="sxs-lookup"><span data-stu-id="2d0f7-139">Remarks</span></span>

<span data-ttu-id="2d0f7-140">El elemento **StandardTime** representa un tiempo de desfase que está representado por el elemento [Bias (UTC)](bias-utc.md) .</span><span class="sxs-lookup"><span data-stu-id="2d0f7-140">The **StandardTime** element represents an offset time that is represented by the [Bias (UTC)](bias-utc.md) element.</span></span> <span data-ttu-id="2d0f7-141">Cuando el elemento de [inclinación](bias.md) secundario es igual a 0, el tiempo estándar es igual que el desplazamiento de diferencia de la hora UTC que está representada por el elemento [Bias (UTC)](bias-utc.md) .</span><span class="sxs-lookup"><span data-stu-id="2d0f7-141">When the child [Bias](bias.md) element equals 0, the standard time is equal to the bias offset from UTC that is represented by the [Bias (UTC)](bias-utc.md) element.</span></span> 
  
## <a name="example"></a><span data-ttu-id="2d0f7-142">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2d0f7-142">Example</span></span>

<span data-ttu-id="2d0f7-143">En el ejemplo siguiente se muestra un área donde se observa el horario de verano.</span><span class="sxs-lookup"><span data-stu-id="2d0f7-143">The following example shows a region where daylight saving time is observed.</span></span> <span data-ttu-id="2d0f7-144">Se observa la transición desde el horario de verano a la hora estándar a las 2 A.M.</span><span class="sxs-lookup"><span data-stu-id="2d0f7-144">The transition from daylight saving time to standard time is observed at 2 A.M.</span></span> <span data-ttu-id="2d0f7-145">en el quinto domingo del décimo mes.</span><span class="sxs-lookup"><span data-stu-id="2d0f7-145">on the fifth Sunday of the tenth month.</span></span>
  
```xml
<TimeZone xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
  <Bias>480</Bias>
  <StandardTime>
    <Bias>0</Bias>
    <Time>02:00:00</Time>
    <DayOrder>5</DayOrder>
    <Month>10</Month>
    <DayOfWeek>Sunday</DayOfWeek>
  </StandardTime>
  <DaylightTime>
    <Bias>-60</Bias>
    <Time>02:00:00</Time>
    <DayOrder>1</DayOrder>
    <Month>4</Month>
    <DayOfWeek>Sunday</DayOfWeek>
  </DaylightTime>
</TimeZone>
```

## <a name="element-information"></a><span data-ttu-id="2d0f7-146">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="2d0f7-146">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2d0f7-147">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="2d0f7-147">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="2d0f7-148">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="2d0f7-148">Schema Name</span></span>  <br/> |<span data-ttu-id="2d0f7-149">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="2d0f7-149">Types schema</span></span>  <br/> |
|<span data-ttu-id="2d0f7-150">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="2d0f7-150">Validation File</span></span>  <br/> |<span data-ttu-id="2d0f7-151">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="2d0f7-151">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="2d0f7-152">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="2d0f7-152">Can be Empty</span></span>  <br/> |<span data-ttu-id="2d0f7-153">False</span><span class="sxs-lookup"><span data-stu-id="2d0f7-153">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2d0f7-154">Ver también</span><span class="sxs-lookup"><span data-stu-id="2d0f7-154">See also</span></span>

- [<span data-ttu-id="2d0f7-155">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="2d0f7-155">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
- [<span data-ttu-id="2d0f7-156">Obtención de disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="2d0f7-156">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

