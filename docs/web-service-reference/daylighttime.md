---
title: DaylightTime
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DaylightTime
api_type:
- schema
ms.assetid: 9f551ee4-d945-477c-b981-9554b197d26d
description: El elemento DaylightTime representa un desplazamiento del tiempo con respecto a la hora universal coordinada (UTC) que se representa mediante el elemento Bias (UTC) en las regiones en las que se observa el horario de verano. Este elemento también contiene información sobre cuándo se produce la transición al horario de verano desde la hora estándar.
ms.openlocfilehash: 350fcb4ce278f423c62fcc5ecaa160eda71e4a2c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44455656"
---
# <a name="daylighttime"></a><span data-ttu-id="cccf7-104">DaylightTime</span><span class="sxs-lookup"><span data-stu-id="cccf7-104">DaylightTime</span></span>

<span data-ttu-id="cccf7-105">El elemento **DaylightTime** representa un desplazamiento del tiempo con respecto a la hora universal coordinada (UTC) que se representa mediante el elemento [Bias (UTC)](bias-utc.md) en las regiones en las que se observa el horario de verano.</span><span class="sxs-lookup"><span data-stu-id="cccf7-105">The **DaylightTime** element represents an offset from the time relative to Coordinated Universal Time (UTC) that is represented by the [Bias (UTC)](bias-utc.md) element in regions where daylight saving time is observed.</span></span> <span data-ttu-id="cccf7-106">Este elemento también contiene información sobre cuándo se produce la transición al horario de verano desde la hora estándar.</span><span class="sxs-lookup"><span data-stu-id="cccf7-106">This element also contains information about when the transition to daylight saving time from standard time occurs.</span></span> 
  
- [<span data-ttu-id="cccf7-107">Zona horaria (disponibilidad)</span><span class="sxs-lookup"><span data-stu-id="cccf7-107">TimeZone (Availability)</span></span>](timezone-availability.md) 
- [<span data-ttu-id="cccf7-108">DaylightTime</span><span class="sxs-lookup"><span data-stu-id="cccf7-108">DaylightTime</span></span>](daylighttime.md)
  
```xml
<DaylightTime>
   <Bias>int</Bias>
   <Time>string</Time>
   <DayOrder>short</DayOrder>
   <Month>short</Month>
   <DayOfWeek>Sunday or Monday or Tuesday or Wednesday or Thursday or Friday or Saturday</DayOfWeek>
   <Year>string</Year>
</DaylightTime>
```

<span data-ttu-id="cccf7-109">**SerializableTimeZoneTime**</span><span class="sxs-lookup"><span data-stu-id="cccf7-109">**SerializableTimeZoneTime**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="cccf7-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="cccf7-110">Attributes and elements</span></span>

<span data-ttu-id="cccf7-111">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="cccf7-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cccf7-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="cccf7-112">Attributes</span></span>

<span data-ttu-id="cccf7-113">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="cccf7-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="cccf7-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="cccf7-114">Child elements</span></span>

|<span data-ttu-id="cccf7-115">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="cccf7-115">**Element**</span></span>|<span data-ttu-id="cccf7-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="cccf7-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cccf7-117">Sesgo</span><span class="sxs-lookup"><span data-stu-id="cccf7-117">Bias</span></span>](bias.md) <br/> |<span data-ttu-id="cccf7-118">Representa el desplazamiento respecto al desplazamiento de la hora UTC que se identifica mediante el elemento [Bias (UTC)](bias-utc.md) para la hora estándar y el horario de verano.</span><span class="sxs-lookup"><span data-stu-id="cccf7-118">Represents the offset from the UTC offset that is identified by the [Bias (UTC)](bias-utc.md) element for standard time and daylight saving time.</span></span> <span data-ttu-id="cccf7-119">Este valor está en minutos.</span><span class="sxs-lookup"><span data-stu-id="cccf7-119">This value is in minutes.</span></span>  <br/> |
|[<span data-ttu-id="cccf7-120">Time</span><span class="sxs-lookup"><span data-stu-id="cccf7-120">Time</span></span>](time.md) <br/> |<span data-ttu-id="cccf7-121">Representa la hora de transición del día a y desde el horario estándar y el horario de verano.</span><span class="sxs-lookup"><span data-stu-id="cccf7-121">Represents the transition time of day to and from standard time and daylight saving time.</span></span>  <br/> |
|[<span data-ttu-id="cccf7-122">DayOrder</span><span class="sxs-lookup"><span data-stu-id="cccf7-122">DayOrder</span></span>](dayorder.md) <br/> |<span data-ttu-id="cccf7-123">Representa la _n_th aparición del día especificado en el elemento [DayOfWeek (TimeZone)](dayofweek-timezone.md) que representa la fecha de transición desde y hasta el horario estándar y el horario de verano.</span><span class="sxs-lookup"><span data-stu-id="cccf7-123">Represents the  _n_th occurrence of the day that is specified in the [DayOfWeek (TimeZone)](dayofweek-timezone.md) element that represents the date of transition from and to standard time and daylight saving time.</span></span>  <br/> |
|[<span data-ttu-id="cccf7-124">Month</span><span class="sxs-lookup"><span data-stu-id="cccf7-124">Month</span></span>](month.md) <br/> |<span data-ttu-id="cccf7-125">Representa el mes de transición del año al y desde el horario estándar y el horario de verano.</span><span class="sxs-lookup"><span data-stu-id="cccf7-125">Represents the transition month of the year to and from standard time and daylight saving time.</span></span>  <br/> |
|[<span data-ttu-id="cccf7-126">DayOfWeek (TimeZone)</span><span class="sxs-lookup"><span data-stu-id="cccf7-126">DayOfWeek (TimeZone)</span></span>](dayofweek-timezone.md) <br/> |<span data-ttu-id="cccf7-127">Representa el día de la semana en que se produce la transición a y desde la hora estándar y el horario de verano.</span><span class="sxs-lookup"><span data-stu-id="cccf7-127">Represents the day of the week when the transition to and from standard time and daylight saving time occurs.</span></span>  <br/> |
|[<span data-ttu-id="cccf7-128">Year</span><span class="sxs-lookup"><span data-stu-id="cccf7-128">Year</span></span>](year.md) <br/> |<span data-ttu-id="cccf7-129">Se usa para definir una zona horaria que cambia según el año.</span><span class="sxs-lookup"><span data-stu-id="cccf7-129">Used to define a time zone that changes depending on the year.</span></span> <span data-ttu-id="cccf7-130">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="cccf7-130">This element is optional.</span></span> <span data-ttu-id="cccf7-131">Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="cccf7-131">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="cccf7-132">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="cccf7-132">Parent elements</span></span>

|<span data-ttu-id="cccf7-133">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="cccf7-133">**Element**</span></span>|<span data-ttu-id="cccf7-134">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="cccf7-134">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cccf7-135">Zona horaria (disponibilidad)</span><span class="sxs-lookup"><span data-stu-id="cccf7-135">TimeZone (Availability)</span></span>](timezone-availability.md) <br/> | <span data-ttu-id="cccf7-136">Contiene los elementos que identifican la información de la zona horaria.</span><span class="sxs-lookup"><span data-stu-id="cccf7-136">Contains elements that identify time zone information.</span></span><br/><br/><span data-ttu-id="cccf7-137">Este elemento también contiene información sobre la transición entre el horario estándar y el horario de verano.</span><span class="sxs-lookup"><span data-stu-id="cccf7-137">This element also contains information about the transition between standard time and daylight saving time.</span></span><br/><br/>`/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/TimeZone` <br/><br/>`/GetUserAvailabilityRequest/TimeZone` <br/> |
   
## <a name="example"></a><span data-ttu-id="cccf7-138">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="cccf7-138">Example</span></span>

<span data-ttu-id="cccf7-139">La siguiente solicitud de GetUserAvailability parcial representa una aplicación cliente en una ubicación que reconoce el horario de verano.</span><span class="sxs-lookup"><span data-stu-id="cccf7-139">The following partial GetUserAvailability request represents a client application in a location that recognizes daylight saving time.</span></span>
  
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

## <a name="element-information"></a><span data-ttu-id="cccf7-140">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="cccf7-140">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cccf7-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="cccf7-141">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="cccf7-142">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="cccf7-142">Schema Name</span></span>  <br/> |<span data-ttu-id="cccf7-143">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="cccf7-143">Types schema</span></span>  <br/> |
|<span data-ttu-id="cccf7-144">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="cccf7-144">Validation File</span></span>  <br/> |<span data-ttu-id="cccf7-145">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="cccf7-145">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="cccf7-146">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="cccf7-146">Can be Empty</span></span>  <br/> |<span data-ttu-id="cccf7-147">Falso</span><span class="sxs-lookup"><span data-stu-id="cccf7-147">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cccf7-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="cccf7-148">See also</span></span>

- [<span data-ttu-id="cccf7-149">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="cccf7-149">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
- [<span data-ttu-id="cccf7-150">Obtener disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="cccf7-150">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

