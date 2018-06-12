---
title: Hora
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Time
api_type:
- schema
ms.assetid: c4b98be7-141c-4ba8-97ef-9ad1ed19f61f
description: El elemento de tiempo representa el tiempo de transición del día a y desde el horario estándar y del horario de verano.
ms.openlocfilehash: 716487fb7ed64dbaa6fa97caf1ea608e4673d2ef
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19840652"
---
# <a name="time"></a><span data-ttu-id="636d0-103">Time</span><span class="sxs-lookup"><span data-stu-id="636d0-103">Time</span></span>

<span data-ttu-id="636d0-104">El elemento de **tiempo** representa el tiempo de transición del día a y desde el horario estándar y del horario de verano.</span><span class="sxs-lookup"><span data-stu-id="636d0-104">The **Time** element represents the transition time of day to and from standard time and daylight saving time.</span></span> 
  
```xml
<Time>...</Time>
```

 <span data-ttu-id="636d0-105">**string**</span><span class="sxs-lookup"><span data-stu-id="636d0-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="636d0-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="636d0-106">Attributes and elements</span></span>

<span data-ttu-id="636d0-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="636d0-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="636d0-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="636d0-108">Attributes</span></span>

<span data-ttu-id="636d0-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="636d0-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="636d0-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="636d0-110">Child elements</span></span>

<span data-ttu-id="636d0-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="636d0-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="636d0-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="636d0-112">Parent elements</span></span>

|<span data-ttu-id="636d0-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="636d0-113">**Element**</span></span>|<span data-ttu-id="636d0-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="636d0-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="636d0-115">StandardTime</span><span class="sxs-lookup"><span data-stu-id="636d0-115">StandardTime</span></span>](standardtime.md) <br/> | <span data-ttu-id="636d0-116">Representa un desplazamiento desde el momento en relación con hora Universal coordinada (UTC), representado por el elemento [Bias (UTC)](bias-utc.md) .</span><span class="sxs-lookup"><span data-stu-id="636d0-116">Represents an offset from the time relative to Coordinated Universal Time (UTC) represented by the [Bias (UTC)](bias-utc.md) element.</span></span> <span data-ttu-id="636d0-117">Este elemento también contiene información sobre la transición a la hora estándar de horario de verano en regiones donde se observa el horario de verano.</span><span class="sxs-lookup"><span data-stu-id="636d0-117">This element also contains information about the transition to standard time from daylight saving time in regions where daylight saving time is observed.</span></span>  <br/><br/>  <span data-ttu-id="636d0-118">Los siguientes son las expresiones de XPath para el elemento [StandardTime](standardtime.md) :</span><span class="sxs-lookup"><span data-stu-id="636d0-118">The following are the XPath expressions to the [StandardTime](standardtime.md) element:</span></span> <br/> <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/TimeZone/StandardTime`<br/> <br/>  `/GetUserAvailabilityRequest/TimeZone/StandardTime` <br/> |
|[<span data-ttu-id="636d0-119">DaylightTime</span><span class="sxs-lookup"><span data-stu-id="636d0-119">DaylightTime</span></span>](daylighttime.md) <br/> | <span data-ttu-id="636d0-120">Representa un desplazamiento de la hora con respecto a UTC representada por el elemento [Bias (UTC)](bias-utc.md) en las regiones donde se observa el horario de verano.</span><span class="sxs-lookup"><span data-stu-id="636d0-120">Represents an offset from the time relative to UTC represented by the [Bias (UTC)](bias-utc.md) element in regions where daylight saving time is observed.</span></span> <span data-ttu-id="636d0-121">Este elemento también contiene información acerca de cuándo se produce la transición al horario de verano de tiempo estándar.</span><span class="sxs-lookup"><span data-stu-id="636d0-121">This element also contains information about when the transition to daylight saving time from standard time occurs.</span></span>  <br/><br/>  <span data-ttu-id="636d0-122">Los siguientes son las expresiones de XPath para el elemento [DaylightTime](daylighttime.md) :</span><span class="sxs-lookup"><span data-stu-id="636d0-122">The following are the XPath expressions to the [DaylightTime](daylighttime.md) element:</span></span>  <br/><br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/TimeZone/DaylightTime` <br/><br/>  `/GetUserAvailabilityRequest/TimeZone/DaylightTime` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="636d0-123">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="636d0-123">Text value</span></span>

<span data-ttu-id="636d0-124">El valor de texto representa horas, minutos y segundos en el siguiente formato: ss.</span><span class="sxs-lookup"><span data-stu-id="636d0-124">The text value represents hours, minutes, and seconds in the following format: hh:mm:ss.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="636d0-125">Notas</span><span class="sxs-lookup"><span data-stu-id="636d0-125">Remarks</span></span>

<span data-ttu-id="636d0-126">Cuando se produce el elemento de **tiempo** en el elemento [DaylightTime](daylighttime.md) , representa la hora del día en que se produce la transición desde el horario de verano a la hora estándar.</span><span class="sxs-lookup"><span data-stu-id="636d0-126">When the **Time** element occurs in the [DaylightTime](daylighttime.md) element, it represents the time of day that the transition from daylight saving time to standard time occurs.</span></span> <span data-ttu-id="636d0-127">Cuando se produce el elemento de [tiempo](time.md) en el elemento [StandardTime](standardtime.md) , que representa la hora del día en que se produce la transición desde el horario estándar al horario de verano.</span><span class="sxs-lookup"><span data-stu-id="636d0-127">When the [Time](time.md) element occurs in the [StandardTime](standardtime.md) element, it represents the time of day that the transition from standard time to daylight saving time occurs.</span></span> 
  
<span data-ttu-id="636d0-128">Este elemento tiene una repetición mínima de cero y una máxima aparición de uno.</span><span class="sxs-lookup"><span data-stu-id="636d0-128">This element has a minimum occurrence of zero and a maximum occurrence of one.</span></span>
  
## <a name="example"></a><span data-ttu-id="636d0-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="636d0-129">Example</span></span>

<span data-ttu-id="636d0-130">La siguiente parte de una solicitud representa un tiempo de transición de 2 A.M.</span><span class="sxs-lookup"><span data-stu-id="636d0-130">The following part of a request represents a transition time of 2 A.M.</span></span> <span data-ttu-id="636d0-131">desde el horario estándar al horario de verano.</span><span class="sxs-lookup"><span data-stu-id="636d0-131">from standard time to daylight saving time.</span></span>
  
```xml
<StandardTime>
   <Bias>0</Bias>
   <Time>02:00:00</Time>
   <DayOrder>5</DayOrder>
   <Month>10</Month>
   <DayOfWeek>Sunday</DayOfWeek>
</StandardTime
```

## <a name="element-information"></a><span data-ttu-id="636d0-132">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="636d0-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="636d0-133">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="636d0-133">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="636d0-134">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="636d0-134">Schema Name</span></span>  <br/> |<span data-ttu-id="636d0-135">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="636d0-135">Types schema</span></span>  <br/> |
|<span data-ttu-id="636d0-136">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="636d0-136">Validation File</span></span>  <br/> |<span data-ttu-id="636d0-137">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="636d0-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="636d0-138">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="636d0-138">Can be Empty</span></span>  <br/> |<span data-ttu-id="636d0-139">False</span><span class="sxs-lookup"><span data-stu-id="636d0-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="636d0-140">Ver también</span><span class="sxs-lookup"><span data-stu-id="636d0-140">See also</span></span>

- [<span data-ttu-id="636d0-141">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="636d0-141">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
- [<span data-ttu-id="636d0-142">Obtención de disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="636d0-142">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

