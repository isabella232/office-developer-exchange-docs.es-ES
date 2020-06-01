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
description: El elemento Time representa la hora de transición del día a y desde la hora estándar y el horario de verano.
ms.openlocfilehash: 97c89fbcbdb85fcdd4d32a1d44075ac42adef053
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460298"
---
# <a name="time"></a><span data-ttu-id="c55b8-103">Hora</span><span class="sxs-lookup"><span data-stu-id="c55b8-103">Time</span></span>

<span data-ttu-id="c55b8-104">El elemento **Time** representa la hora de transición del día a y desde la hora estándar y el horario de verano.</span><span class="sxs-lookup"><span data-stu-id="c55b8-104">The **Time** element represents the transition time of day to and from standard time and daylight saving time.</span></span> 
  
```xml
<Time>...</Time>
```

 <span data-ttu-id="c55b8-105">**string**</span><span class="sxs-lookup"><span data-stu-id="c55b8-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c55b8-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="c55b8-106">Attributes and elements</span></span>

<span data-ttu-id="c55b8-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="c55b8-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c55b8-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="c55b8-108">Attributes</span></span>

<span data-ttu-id="c55b8-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="c55b8-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c55b8-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c55b8-110">Child elements</span></span>

<span data-ttu-id="c55b8-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="c55b8-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="c55b8-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="c55b8-112">Parent elements</span></span>

|<span data-ttu-id="c55b8-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="c55b8-113">**Element**</span></span>|<span data-ttu-id="c55b8-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c55b8-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c55b8-115">Standardtime Element</span><span class="sxs-lookup"><span data-stu-id="c55b8-115">StandardTime</span></span>](standardtime.md) <br/> | <span data-ttu-id="c55b8-116">Representa un desplazamiento del tiempo con respecto a la hora universal coordinada (UTC) representada por el elemento [Bias (UTC)](bias-utc.md) .</span><span class="sxs-lookup"><span data-stu-id="c55b8-116">Represents an offset from the time relative to Coordinated Universal Time (UTC) represented by the [Bias (UTC)](bias-utc.md) element.</span></span> <span data-ttu-id="c55b8-117">Este elemento también contiene información sobre la transición a la hora estándar del horario de verano en regiones en las que se observa el horario de verano.</span><span class="sxs-lookup"><span data-stu-id="c55b8-117">This element also contains information about the transition to standard time from daylight saving time in regions where daylight saving time is observed.</span></span>  <br/><br/>  <span data-ttu-id="c55b8-118">Las siguientes son las expresiones XPath para el elemento [standardtime Element](standardtime.md) :</span><span class="sxs-lookup"><span data-stu-id="c55b8-118">The following are the XPath expressions to the [StandardTime](standardtime.md) element:</span></span> <br/> <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/TimeZone/StandardTime`<br/> <br/>  `/GetUserAvailabilityRequest/TimeZone/StandardTime` <br/> |
|[<span data-ttu-id="c55b8-119">DaylightTime</span><span class="sxs-lookup"><span data-stu-id="c55b8-119">DaylightTime</span></span>](daylighttime.md) <br/> | <span data-ttu-id="c55b8-120">Representa un desplazamiento del tiempo relativo a la hora UTC representado por el elemento [Bias (UTC)](bias-utc.md) en las regiones en las que se observa el horario de verano.</span><span class="sxs-lookup"><span data-stu-id="c55b8-120">Represents an offset from the time relative to UTC represented by the [Bias (UTC)](bias-utc.md) element in regions where daylight saving time is observed.</span></span> <span data-ttu-id="c55b8-121">Este elemento también contiene información sobre cuándo se produce la transición al horario de verano desde la hora estándar.</span><span class="sxs-lookup"><span data-stu-id="c55b8-121">This element also contains information about when the transition to daylight saving time from standard time occurs.</span></span>  <br/><br/>  <span data-ttu-id="c55b8-122">Las siguientes son las expresiones XPath para el elemento [DaylightTime](daylighttime.md) :</span><span class="sxs-lookup"><span data-stu-id="c55b8-122">The following are the XPath expressions to the [DaylightTime](daylighttime.md) element:</span></span>  <br/><br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/TimeZone/DaylightTime` <br/><br/>  `/GetUserAvailabilityRequest/TimeZone/DaylightTime` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="c55b8-123">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="c55b8-123">Text value</span></span>

<span data-ttu-id="c55b8-124">El valor de texto representa las horas, los minutos y los segundos con el siguiente formato: HH: mm: SS.</span><span class="sxs-lookup"><span data-stu-id="c55b8-124">The text value represents hours, minutes, and seconds in the following format: hh:mm:ss.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c55b8-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c55b8-125">Remarks</span></span>

<span data-ttu-id="c55b8-126">Cuando se produce el elemento **Time** en el elemento [DaylightTime](daylighttime.md) , representa la hora del día en que se produce la transición del horario de verano a la hora estándar.</span><span class="sxs-lookup"><span data-stu-id="c55b8-126">When the **Time** element occurs in the [DaylightTime](daylighttime.md) element, it represents the time of day that the transition from daylight saving time to standard time occurs.</span></span> <span data-ttu-id="c55b8-127">Cuando se produce el elemento [Time](time.md) en el elemento [standardtime Element](standardtime.md) , representa la hora del día a la que se produce la transición de la hora estándar al horario de verano.</span><span class="sxs-lookup"><span data-stu-id="c55b8-127">When the [Time](time.md) element occurs in the [StandardTime](standardtime.md) element, it represents the time of day that the transition from standard time to daylight saving time occurs.</span></span> 
  
<span data-ttu-id="c55b8-128">Este elemento tiene una ocurrencia mínima de cero y una ocurrencia máxima de uno.</span><span class="sxs-lookup"><span data-stu-id="c55b8-128">This element has a minimum occurrence of zero and a maximum occurrence of one.</span></span>
  
## <a name="example"></a><span data-ttu-id="c55b8-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c55b8-129">Example</span></span>

<span data-ttu-id="c55b8-130">La siguiente parte de una solicitud representa un tiempo de transición de 2 A.M.</span><span class="sxs-lookup"><span data-stu-id="c55b8-130">The following part of a request represents a transition time of 2 A.M.</span></span> <span data-ttu-id="c55b8-131">de la hora estándar al horario de verano.</span><span class="sxs-lookup"><span data-stu-id="c55b8-131">from standard time to daylight saving time.</span></span>
  
```xml
<StandardTime>
   <Bias>0</Bias>
   <Time>02:00:00</Time>
   <DayOrder>5</DayOrder>
   <Month>10</Month>
   <DayOfWeek>Sunday</DayOfWeek>
</StandardTime
```

## <a name="element-information"></a><span data-ttu-id="c55b8-132">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="c55b8-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c55b8-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="c55b8-133">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c55b8-134">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="c55b8-134">Schema Name</span></span>  <br/> |<span data-ttu-id="c55b8-135">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="c55b8-135">Types schema</span></span>  <br/> |
|<span data-ttu-id="c55b8-136">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="c55b8-136">Validation File</span></span>  <br/> |<span data-ttu-id="c55b8-137">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="c55b8-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="c55b8-138">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="c55b8-138">Can be Empty</span></span>  <br/> |<span data-ttu-id="c55b8-139">Falso</span><span class="sxs-lookup"><span data-stu-id="c55b8-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c55b8-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="c55b8-140">See also</span></span>

- [<span data-ttu-id="c55b8-141">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="c55b8-141">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
- [<span data-ttu-id="c55b8-142">Obtener disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="c55b8-142">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

