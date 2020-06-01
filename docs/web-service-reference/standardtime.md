---
title: Standardtime Element
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
description: El elemento Standardtime Element representa un desplazamiento del tiempo con respecto a la hora universal coordinada (UTC) que se representa mediante el elemento Bias (UTC). Este elemento también contiene información sobre la transición a la hora estándar del horario de verano en regiones en las que se observa el horario de verano.
ms.openlocfilehash: 793f058840d4fd9216f03e660f5be0f7564906cf
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44456405"
---
# <a name="standardtime"></a><span data-ttu-id="e8a6e-104">Standardtime Element</span><span class="sxs-lookup"><span data-stu-id="e8a6e-104">StandardTime</span></span>

<span data-ttu-id="e8a6e-105">El elemento **standardtime Element** representa un desplazamiento del tiempo con respecto a la hora universal coordinada (UTC) que se representa mediante el elemento [Bias (UTC)](bias-utc.md) .</span><span class="sxs-lookup"><span data-stu-id="e8a6e-105">The **StandardTime** element represents an offset from the time relative to Coordinated Universal Time (UTC) that is represented by the [Bias (UTC)](bias-utc.md) element.</span></span> <span data-ttu-id="e8a6e-106">Este elemento también contiene información sobre la transición a la hora estándar del horario de verano en regiones en las que se observa el horario de verano.</span><span class="sxs-lookup"><span data-stu-id="e8a6e-106">This element also contains information about the transition to standard time from daylight saving time in regions where daylight saving time is observed.</span></span> 
  
- [<span data-ttu-id="e8a6e-107">Zona horaria (disponibilidad)</span><span class="sxs-lookup"><span data-stu-id="e8a6e-107">TimeZone (Availability)</span></span>](timezone-availability.md)
- [<span data-ttu-id="e8a6e-108">Standardtime Element</span><span class="sxs-lookup"><span data-stu-id="e8a6e-108">StandardTime</span></span>](standardtime.md)
  
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

 <span data-ttu-id="e8a6e-109">**SerializableTimeZoneTime**</span><span class="sxs-lookup"><span data-stu-id="e8a6e-109">**SerializableTimeZoneTime**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e8a6e-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="e8a6e-110">Attributes and elements</span></span>

<span data-ttu-id="e8a6e-111">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="e8a6e-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e8a6e-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="e8a6e-112">Attributes</span></span>

<span data-ttu-id="e8a6e-113">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="e8a6e-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e8a6e-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="e8a6e-114">Child elements</span></span>

|<span data-ttu-id="e8a6e-115">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="e8a6e-115">**Element**</span></span>|<span data-ttu-id="e8a6e-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e8a6e-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e8a6e-117">Sesgo</span><span class="sxs-lookup"><span data-stu-id="e8a6e-117">Bias</span></span>](bias.md) <br/> |<span data-ttu-id="e8a6e-118">Representa el desplazamiento respecto al desplazamiento de la hora UTC que se identifica mediante el elemento [Bias (UTC)](bias-utc.md) para la hora estándar y el horario de verano.</span><span class="sxs-lookup"><span data-stu-id="e8a6e-118">Represents the offset from the UTC offset that is identified by the [Bias (UTC)](bias-utc.md) element for standard time and daylight saving time.</span></span> <span data-ttu-id="e8a6e-119">Este valor está en minutos.</span><span class="sxs-lookup"><span data-stu-id="e8a6e-119">This value is in minutes.</span></span>  <br/> |
|[<span data-ttu-id="e8a6e-120">Time</span><span class="sxs-lookup"><span data-stu-id="e8a6e-120">Time</span></span>](time.md) <br/> |<span data-ttu-id="e8a6e-121">Representa la hora de transición del día a y desde el horario estándar y el horario de verano.</span><span class="sxs-lookup"><span data-stu-id="e8a6e-121">Represents the transition time of day to and from standard time and daylight saving time.</span></span>  <br/> |
|[<span data-ttu-id="e8a6e-122">DayOrder</span><span class="sxs-lookup"><span data-stu-id="e8a6e-122">DayOrder</span></span>](dayorder.md) <br/> |<span data-ttu-id="e8a6e-123">Representa la _n_th aparición del día especificado en el elemento [DayOfWeek (TimeZone)](dayofweek-timezone.md) que representa la fecha de transición desde y hasta el horario estándar y el horario de verano.</span><span class="sxs-lookup"><span data-stu-id="e8a6e-123">Represents the  _n_th occurrence of the day that is specified in the [DayOfWeek (TimeZone)](dayofweek-timezone.md) element that represents the date of transition from and to standard time and daylight saving time.</span></span>  <br/> |
|[<span data-ttu-id="e8a6e-124">Month</span><span class="sxs-lookup"><span data-stu-id="e8a6e-124">Month</span></span>](month.md) <br/> |<span data-ttu-id="e8a6e-125">Representa el mes de transición del año al y desde el horario estándar y el horario de verano.</span><span class="sxs-lookup"><span data-stu-id="e8a6e-125">Represents the transition month of the year to and from standard time and daylight saving time.</span></span>  <br/> |
|[<span data-ttu-id="e8a6e-126">DayOfWeek (TimeZone)</span><span class="sxs-lookup"><span data-stu-id="e8a6e-126">DayOfWeek (TimeZone)</span></span>](dayofweek-timezone.md) <br/> |<span data-ttu-id="e8a6e-127">Representa el día de la semana en que se produce la transición a y desde la hora estándar y el horario de verano.</span><span class="sxs-lookup"><span data-stu-id="e8a6e-127">Represents the day of the week when the transition to and from standard time and daylight saving time occurs.</span></span>  <br/> |
|[<span data-ttu-id="e8a6e-128">Year</span><span class="sxs-lookup"><span data-stu-id="e8a6e-128">Year</span></span>](year.md) <br/> |<span data-ttu-id="e8a6e-129">Define una zona horaria que cambia según el año.</span><span class="sxs-lookup"><span data-stu-id="e8a6e-129">Defines a time zone that changes depending on the year.</span></span> <span data-ttu-id="e8a6e-130">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="e8a6e-130">This element is optional.</span></span> <span data-ttu-id="e8a6e-131">Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="e8a6e-131">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="e8a6e-132">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="e8a6e-132">Parent elements</span></span>

|<span data-ttu-id="e8a6e-133">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="e8a6e-133">**Element**</span></span>|<span data-ttu-id="e8a6e-134">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e8a6e-134">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e8a6e-135">Zona horaria (disponibilidad)</span><span class="sxs-lookup"><span data-stu-id="e8a6e-135">TimeZone (Availability)</span></span>](timezone-availability.md) <br/> | <span data-ttu-id="e8a6e-136">Contiene los elementos que identifican la información de la zona horaria.</span><span class="sxs-lookup"><span data-stu-id="e8a6e-136">Contains elements that identify time zone information.</span></span> <span data-ttu-id="e8a6e-137">Este elemento también contiene información sobre la transición entre el horario estándar y el horario de verano.</span><span class="sxs-lookup"><span data-stu-id="e8a6e-137">This element also contains information about the transition between standard time and daylight saving time.</span></span> <br/><br/><span data-ttu-id="e8a6e-138">Las siguientes son las expresiones XPath de este elemento:</span><span class="sxs-lookup"><span data-stu-id="e8a6e-138">The following are the XPath expressions to this element:</span></span> <br/> <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/TimeZone` <br/> <br/> `/GetUserAvailabilityRequest/TimeZone` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e8a6e-139">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e8a6e-139">Remarks</span></span>

<span data-ttu-id="e8a6e-140">El elemento **standardtime Element** representa una hora de desplazamiento que se representa mediante el elemento [Bias (UTC)](bias-utc.md) .</span><span class="sxs-lookup"><span data-stu-id="e8a6e-140">The **StandardTime** element represents an offset time that is represented by the [Bias (UTC)](bias-utc.md) element.</span></span> <span data-ttu-id="e8a6e-141">Cuando el elemento de [diferencia](bias.md) secundaria es igual a 0, la hora estándar es igual al desplazamiento de diferencia con respecto a la hora UTC que se representa mediante el elemento [Bias (UTC)](bias-utc.md) .</span><span class="sxs-lookup"><span data-stu-id="e8a6e-141">When the child [Bias](bias.md) element equals 0, the standard time is equal to the bias offset from UTC that is represented by the [Bias (UTC)](bias-utc.md) element.</span></span> 
  
## <a name="example"></a><span data-ttu-id="e8a6e-142">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e8a6e-142">Example</span></span>

<span data-ttu-id="e8a6e-143">En el ejemplo siguiente se muestra una región en la que se observa el horario de verano.</span><span class="sxs-lookup"><span data-stu-id="e8a6e-143">The following example shows a region where daylight saving time is observed.</span></span> <span data-ttu-id="e8a6e-144">La transición del horario de verano a la hora estándar se observa a las 2 A.M.</span><span class="sxs-lookup"><span data-stu-id="e8a6e-144">The transition from daylight saving time to standard time is observed at 2 A.M.</span></span> <span data-ttu-id="e8a6e-145">el quinto domingo del décimo mes.</span><span class="sxs-lookup"><span data-stu-id="e8a6e-145">on the fifth Sunday of the tenth month.</span></span>
  
```xml
<TimeZone xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
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

## <a name="element-information"></a><span data-ttu-id="e8a6e-146">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="e8a6e-146">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e8a6e-147">Namespace</span><span class="sxs-lookup"><span data-stu-id="e8a6e-147">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="e8a6e-148">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="e8a6e-148">Schema Name</span></span>  <br/> |<span data-ttu-id="e8a6e-149">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="e8a6e-149">Types schema</span></span>  <br/> |
|<span data-ttu-id="e8a6e-150">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="e8a6e-150">Validation File</span></span>  <br/> |<span data-ttu-id="e8a6e-151">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="e8a6e-151">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="e8a6e-152">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="e8a6e-152">Can be Empty</span></span>  <br/> |<span data-ttu-id="e8a6e-153">Falso</span><span class="sxs-lookup"><span data-stu-id="e8a6e-153">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e8a6e-154">Vea también</span><span class="sxs-lookup"><span data-stu-id="e8a6e-154">See also</span></span>

- [<span data-ttu-id="e8a6e-155">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="e8a6e-155">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
- [<span data-ttu-id="e8a6e-156">Obtener disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="e8a6e-156">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

