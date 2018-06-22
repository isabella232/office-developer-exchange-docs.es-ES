---
title: DayOrder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DayOrder
api_type:
- schema
ms.assetid: 3022f839-12a2-42a9-820e-3ea585ce8657
description: El elemento DayOrder representa la repetición número n del día especificado en el elemento DayOfWeek (TimeZone) que representa la fecha de transición desde y a la hora estándar y el horario de verano.
ms.openlocfilehash: 03ee678611a6cf58a7256ded67ab4d0a8a06a7ee
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764056"
---
# <a name="dayorder"></a><span data-ttu-id="1af5a-103">DayOrder</span><span class="sxs-lookup"><span data-stu-id="1af5a-103">DayOrder</span></span>

<span data-ttu-id="1af5a-104">El elemento **DayOrder** representa la aparición de _n_th del día especificado en el elemento [DayOfWeek (TimeZone)](dayofweek-timezone.md) que representa la fecha de transición desde y a la hora estándar y el horario de verano.</span><span class="sxs-lookup"><span data-stu-id="1af5a-104">The **DayOrder** element represents the  _n_th occurrence of the day specified in the [DayOfWeek (TimeZone)](dayofweek-timezone.md) element that represents the date of transition from and to standard time and daylight saving time.</span></span> 
  
```xml
<DayOrder>...</DayOrder>
```

<span data-ttu-id="1af5a-105">**breve**</span><span class="sxs-lookup"><span data-stu-id="1af5a-105">**short**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="1af5a-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="1af5a-106">Attributes and elements</span></span>

<span data-ttu-id="1af5a-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="1af5a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1af5a-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="1af5a-108">Attributes</span></span>

<span data-ttu-id="1af5a-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="1af5a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1af5a-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="1af5a-110">Child elements</span></span>

<span data-ttu-id="1af5a-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="1af5a-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="1af5a-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="1af5a-112">Parent elements</span></span>

|<span data-ttu-id="1af5a-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="1af5a-113">**Element**</span></span>|<span data-ttu-id="1af5a-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1af5a-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1af5a-115">StandardTime</span><span class="sxs-lookup"><span data-stu-id="1af5a-115">StandardTime</span></span>](standardtime.md) <br/> | <span data-ttu-id="1af5a-116">Representa un desplazamiento desde el momento en relación con hora Universal coordinada (UTC), representado por el elemento [Bias (UTC)](bias-utc.md) .</span><span class="sxs-lookup"><span data-stu-id="1af5a-116">Represents an offset from the time relative to Coordinated Universal Time (UTC) represented by the [Bias (UTC)](bias-utc.md) element.</span></span><br/><br/><span data-ttu-id="1af5a-117">Este elemento también contiene información sobre la transición a la hora estándar de horario de verano en regiones donde se observa el horario de verano.</span><span class="sxs-lookup"><span data-stu-id="1af5a-117">This element also contains information about the transition to standard time from daylight saving time in regions where daylight saving time is observed.</span></span><br/><br/><span data-ttu-id="1af5a-118">Los siguientes son las expresiones de XPath para el elemento [StandardTime](standardtime.md) :</span><span class="sxs-lookup"><span data-stu-id="1af5a-118">The following are the XPath expressions to the [StandardTime](standardtime.md) element:</span></span><br/><br/>`/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/TimeZone/StandardTime`<br/><br/>`/GetUserAvailabilityRequest/TimeZone/StandardTime` <br/> |
|[<span data-ttu-id="1af5a-119">DaylightTime</span><span class="sxs-lookup"><span data-stu-id="1af5a-119">DaylightTime</span></span>](daylighttime.md) <br/> | <span data-ttu-id="1af5a-120">Representa un desplazamiento de la hora con respecto a UTC representada por el elemento [Bias (UTC)](bias-utc.md) en las regiones donde se observa el horario de verano.</span><span class="sxs-lookup"><span data-stu-id="1af5a-120">Represents an offset from the time relative to UTC represented by the [Bias (UTC)](bias-utc.md) element in regions where daylight saving time is observed.</span></span><br/><br/><span data-ttu-id="1af5a-121">Este elemento también contiene información acerca de cuándo se produce la transición al horario de verano de tiempo estándar.</span><span class="sxs-lookup"><span data-stu-id="1af5a-121">This element also contains information about when the transition to daylight saving time from standard time occurs.</span></span><br/><br/><span data-ttu-id="1af5a-122">Los siguientes son las expresiones de XPath para el elemento [DaylightTime](daylighttime.md) :</span><span class="sxs-lookup"><span data-stu-id="1af5a-122">The following are the XPath expressions to the [DaylightTime](daylighttime.md) element:</span></span><br/><br/>`/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/TimeZone/DaylightTime`<br/><br/>`/GetUserAvailabilityRequest/TimeZone/DaylightTime` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="1af5a-123">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="1af5a-123">Text value</span></span>

<span data-ttu-id="1af5a-124">Se requiere un valor de texto.</span><span class="sxs-lookup"><span data-stu-id="1af5a-124">A text value is required.</span></span> <span data-ttu-id="1af5a-125">El valor para el elemento **DayOrder** puede ser 1 al 5.</span><span class="sxs-lookup"><span data-stu-id="1af5a-125">The value for the **DayOrder** element can be 1 through 5.</span></span> <span data-ttu-id="1af5a-126">El valor máximo para este elemento puede ser 4 o 5, dependiendo del mes y año.</span><span class="sxs-lookup"><span data-stu-id="1af5a-126">The maximum value for this element can be either 4 or 5, depending on the month and year.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="1af5a-127">Notas</span><span class="sxs-lookup"><span data-stu-id="1af5a-127">Remarks</span></span>

<span data-ttu-id="1af5a-128">Un elemento [StandardTime](standardtime.md) que contiene un elemento **DayOrder** que tiene un valor de 5, un elemento de [mes](month.md) que tiene un valor de 10 y un elemento [DayOfWeek (TimeZone)](dayofweek-timezone.md) que tiene un valor del domingo significa la transición desde el horario estándar para horario de verano se produce el domingo quinto del décimo mes.</span><span class="sxs-lookup"><span data-stu-id="1af5a-128">A [StandardTime](standardtime.md) element that contains a **DayOrder** element that has a value of 5, a [Month](month.md) element that has a value of 10, and a [DayOfWeek (TimeZone)](dayofweek-timezone.md) element that has a value of Sunday means that the transition from standard time to daylight saving time occurs on the fifth Sunday of the tenth month.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="1af5a-129">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="1af5a-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1af5a-130">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="1af5a-130">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="1af5a-131">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="1af5a-131">Schema Name</span></span>  <br/> |<span data-ttu-id="1af5a-132">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="1af5a-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="1af5a-133">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="1af5a-133">Validation File</span></span>  <br/> |<span data-ttu-id="1af5a-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="1af5a-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="1af5a-135">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="1af5a-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="1af5a-136">False</span><span class="sxs-lookup"><span data-stu-id="1af5a-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1af5a-137">Ver también</span><span class="sxs-lookup"><span data-stu-id="1af5a-137">See also</span></span>

- [<span data-ttu-id="1af5a-138">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="1af5a-138">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
- [<span data-ttu-id="1af5a-139">Obtención de disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="1af5a-139">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

