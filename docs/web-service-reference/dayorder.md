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
description: El elemento DayOrder representa el número n de ocurrencias del día especificado en el elemento DayOfWeek (TimeZone) que representa la fecha de transición desde y hasta el horario estándar y el horario de verano.
ms.openlocfilehash: 53a8cb979bdb7aefead5623b4680f4c1a4ef5509
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526966"
---
# <a name="dayorder"></a><span data-ttu-id="53097-103">DayOrder</span><span class="sxs-lookup"><span data-stu-id="53097-103">DayOrder</span></span>

<span data-ttu-id="53097-104">El elemento **DayOrder** representa la _n_th aparición del día especificado en el elemento [DayOfWeek (TimeZone)](dayofweek-timezone.md) que representa la fecha de transición desde y hasta el horario estándar y el horario de verano.</span><span class="sxs-lookup"><span data-stu-id="53097-104">The **DayOrder** element represents the  _n_th occurrence of the day specified in the [DayOfWeek (TimeZone)](dayofweek-timezone.md) element that represents the date of transition from and to standard time and daylight saving time.</span></span> 
  
```xml
<DayOrder>...</DayOrder>
```

<span data-ttu-id="53097-105">**Short**</span><span class="sxs-lookup"><span data-stu-id="53097-105">**short**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="53097-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="53097-106">Attributes and elements</span></span>

<span data-ttu-id="53097-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="53097-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="53097-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="53097-108">Attributes</span></span>

<span data-ttu-id="53097-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="53097-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="53097-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="53097-110">Child elements</span></span>

<span data-ttu-id="53097-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="53097-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="53097-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="53097-112">Parent elements</span></span>

|<span data-ttu-id="53097-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="53097-113">**Element**</span></span>|<span data-ttu-id="53097-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="53097-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="53097-115">Standardtime Element</span><span class="sxs-lookup"><span data-stu-id="53097-115">StandardTime</span></span>](standardtime.md) <br/> | <span data-ttu-id="53097-116">Representa un desplazamiento del tiempo con respecto a la hora universal coordinada (UTC) representada por el elemento [Bias (UTC)](bias-utc.md) .</span><span class="sxs-lookup"><span data-stu-id="53097-116">Represents an offset from the time relative to Coordinated Universal Time (UTC) represented by the [Bias (UTC)](bias-utc.md) element.</span></span><br/><br/><span data-ttu-id="53097-117">Este elemento también contiene información sobre la transición a la hora estándar del horario de verano en regiones en las que se observa el horario de verano.</span><span class="sxs-lookup"><span data-stu-id="53097-117">This element also contains information about the transition to standard time from daylight saving time in regions where daylight saving time is observed.</span></span><br/><br/><span data-ttu-id="53097-118">Las siguientes son las expresiones XPath para el elemento [standardtime Element](standardtime.md) :</span><span class="sxs-lookup"><span data-stu-id="53097-118">The following are the XPath expressions to the [StandardTime](standardtime.md) element:</span></span><br/><br/>`/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/TimeZone/StandardTime`<br/><br/>`/GetUserAvailabilityRequest/TimeZone/StandardTime` <br/> |
|[<span data-ttu-id="53097-119">DaylightTime</span><span class="sxs-lookup"><span data-stu-id="53097-119">DaylightTime</span></span>](daylighttime.md) <br/> | <span data-ttu-id="53097-120">Representa un desplazamiento del tiempo relativo a la hora UTC representado por el elemento [Bias (UTC)](bias-utc.md) en las regiones en las que se observa el horario de verano.</span><span class="sxs-lookup"><span data-stu-id="53097-120">Represents an offset from the time relative to UTC represented by the [Bias (UTC)](bias-utc.md) element in regions where daylight saving time is observed.</span></span><br/><br/><span data-ttu-id="53097-121">Este elemento también contiene información sobre cuándo se produce la transición al horario de verano desde la hora estándar.</span><span class="sxs-lookup"><span data-stu-id="53097-121">This element also contains information about when the transition to daylight saving time from standard time occurs.</span></span><br/><br/><span data-ttu-id="53097-122">Las siguientes son las expresiones XPath para el elemento [DaylightTime](daylighttime.md) :</span><span class="sxs-lookup"><span data-stu-id="53097-122">The following are the XPath expressions to the [DaylightTime](daylighttime.md) element:</span></span><br/><br/>`/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/TimeZone/DaylightTime`<br/><br/>`/GetUserAvailabilityRequest/TimeZone/DaylightTime` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="53097-123">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="53097-123">Text value</span></span>

<span data-ttu-id="53097-124">Se requiere un valor de texto.</span><span class="sxs-lookup"><span data-stu-id="53097-124">A text value is required.</span></span> <span data-ttu-id="53097-125">El valor del elemento **DayOrder** puede estar comprendido entre 1 y 5.</span><span class="sxs-lookup"><span data-stu-id="53097-125">The value for the **DayOrder** element can be 1 through 5.</span></span> <span data-ttu-id="53097-126">El valor máximo para este elemento puede ser 4 o 5, según el mes y el año.</span><span class="sxs-lookup"><span data-stu-id="53097-126">The maximum value for this element can be either 4 or 5, depending on the month and year.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="53097-127">Comentarios</span><span class="sxs-lookup"><span data-stu-id="53097-127">Remarks</span></span>

<span data-ttu-id="53097-128">Un elemento [standardtime Element](standardtime.md) que contiene un elemento **DayOrder** que tiene un valor de 5, un elemento [Month](month.md) que tiene un valor de 10, y un elemento [DayOfWeek (TimeZone)](dayofweek-timezone.md) que tiene un valor de domingo, significa que la transición de la hora estándar al horario de verano se produce el quinto domingo del décimo mes.</span><span class="sxs-lookup"><span data-stu-id="53097-128">A [StandardTime](standardtime.md) element that contains a **DayOrder** element that has a value of 5, a [Month](month.md) element that has a value of 10, and a [DayOfWeek (TimeZone)](dayofweek-timezone.md) element that has a value of Sunday means that the transition from standard time to daylight saving time occurs on the fifth Sunday of the tenth month.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="53097-129">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="53097-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="53097-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="53097-130">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="53097-131">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="53097-131">Schema Name</span></span>  <br/> |<span data-ttu-id="53097-132">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="53097-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="53097-133">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="53097-133">Validation File</span></span>  <br/> |<span data-ttu-id="53097-134">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="53097-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="53097-135">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="53097-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="53097-136">Falso</span><span class="sxs-lookup"><span data-stu-id="53097-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="53097-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="53097-137">See also</span></span>

- [<span data-ttu-id="53097-138">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="53097-138">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
- [<span data-ttu-id="53097-139">Obtener disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="53097-139">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

