---
title: Mes
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Month
api_type:
- schema
ms.assetid: b12ac64f-b230-4573-be05-c86a428c4965
description: El elemento Month representa los meses del año de la transición a y desde el horario estándar y del horario de verano.
ms.openlocfilehash: 73d052ef16bc51cd574eb8b04e21546f97347258
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836476"
---
# <a name="month"></a><span data-ttu-id="848bd-103">Mes</span><span class="sxs-lookup"><span data-stu-id="848bd-103">Month</span></span>

<span data-ttu-id="848bd-104">El elemento **Month** representa los meses del año de la transición a y desde el horario estándar y del horario de verano.</span><span class="sxs-lookup"><span data-stu-id="848bd-104">The **Month** element represents the transition month of the year to and from standard time and daylight saving time.</span></span> 
  
```xml
<Month>...</Month>
```

 <span data-ttu-id="848bd-105">**Breve**</span><span class="sxs-lookup"><span data-stu-id="848bd-105">**Short**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="848bd-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="848bd-106">Attributes and elements</span></span>

<span data-ttu-id="848bd-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="848bd-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="848bd-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="848bd-108">Attributes</span></span>

<span data-ttu-id="848bd-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="848bd-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="848bd-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="848bd-110">Child elements</span></span>

<span data-ttu-id="848bd-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="848bd-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="848bd-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="848bd-112">Parent elements</span></span>

|<span data-ttu-id="848bd-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="848bd-113">**Element**</span></span>|<span data-ttu-id="848bd-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="848bd-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="848bd-115">StandardTime</span><span class="sxs-lookup"><span data-stu-id="848bd-115">StandardTime</span></span>](standardtime.md) <br/> | <span data-ttu-id="848bd-116">Representa un desplazamiento desde el momento en relación con hora Universal coordinada (UTC), representado por el elemento [Bias (UTC)](bias-utc.md) .</span><span class="sxs-lookup"><span data-stu-id="848bd-116">Represents an offset from the time relative to Coordinated Universal Time (UTC) represented by the [Bias (UTC)](bias-utc.md) element.</span></span> <span data-ttu-id="848bd-117">Este elemento también contiene información sobre la transición a la hora estándar de horario de verano en regiones donde se observa el horario de verano.</span><span class="sxs-lookup"><span data-stu-id="848bd-117">This element also contains information about the transition to standard time from daylight saving time in regions where daylight saving time is observed.</span></span> <br/> <br/>  <span data-ttu-id="848bd-118">Los siguientes son las expresiones de XPath para el elemento [StandardTime](standardtime.md) :</span><span class="sxs-lookup"><span data-stu-id="848bd-118">The following are the XPath expressions to the [StandardTime](standardtime.md) element:</span></span> <br/> <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/TimeZone/StandardTime` <br/><br/>  `/GetUserAvailabilityRequest/TimeZone/StandardTime` <br/> |
|[<span data-ttu-id="848bd-119">DaylightTime</span><span class="sxs-lookup"><span data-stu-id="848bd-119">DaylightTime</span></span>](daylighttime.md) <br/> | <span data-ttu-id="848bd-120">Representa un desplazamiento de la hora con respecto a UTC representada por el elemento [Bias (UTC)](bias-utc.md) en las regiones donde se observa el horario de verano.</span><span class="sxs-lookup"><span data-stu-id="848bd-120">Represents an offset from the time relative to UTC represented by the [Bias (UTC)](bias-utc.md) element in regions where daylight saving time is observed.</span></span> <span data-ttu-id="848bd-121">Este elemento también contiene información acerca de cuándo se produce la transición al horario de verano de tiempo estándar.</span><span class="sxs-lookup"><span data-stu-id="848bd-121">This element also contains information about when the transition to daylight saving time from standard time occurs.</span></span>  <br/><br/>  <span data-ttu-id="848bd-122">Los siguientes son las expresiones de XPath para el elemento [DaylightTime](daylighttime.md) :</span><span class="sxs-lookup"><span data-stu-id="848bd-122">The following are the XPath expressions to the [DaylightTime](daylighttime.md) element:</span></span>  <br/> <br/> `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/TimeZone/DaylightTime` <br/><br/>  `/GetUserAvailabilityRequest/TimeZone/DaylightTime` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="848bd-123">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="848bd-123">Text value</span></span>

<span data-ttu-id="848bd-124">Se requiere un valor de texto.</span><span class="sxs-lookup"><span data-stu-id="848bd-124">A text value is required.</span></span> <span data-ttu-id="848bd-125">El valor representa la clasificación ordinal del mes por repetición y debe ser un número comprendido entre 1 y 12.</span><span class="sxs-lookup"><span data-stu-id="848bd-125">The value represents the ordinal rank of the month by occurrence and must be a number between 1 and 12.</span></span> <span data-ttu-id="848bd-126">Esto es un tipo de datos entero corto.</span><span class="sxs-lookup"><span data-stu-id="848bd-126">This is a short integer data type.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="848bd-127">Comentarios</span><span class="sxs-lookup"><span data-stu-id="848bd-127">Remarks</span></span>

<span data-ttu-id="848bd-128">Un elemento [StandardTime](standardtime.md) que contiene un elemento [DayOrder](dayorder.md) que tiene un valor de 5, un elemento de **mes** que tiene un valor de 10 y un elemento [DayOfWeek (TimeZone)](dayofweek-timezone.md) que tiene un valor del domingo significa la transición desde el horario estándar para horario de verano se produce el domingo quinto del décimo mes.</span><span class="sxs-lookup"><span data-stu-id="848bd-128">A [StandardTime](standardtime.md) element that contains a [DayOrder](dayorder.md) element that has a value of 5, a **Month** element that has a value of 10, and a [DayOfWeek (TimeZone)](dayofweek-timezone.md) element that has a value of Sunday means that the transition from standard time to daylight saving time occurs on the fifth Sunday of the tenth month.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="848bd-129">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="848bd-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="848bd-130">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="848bd-130">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="848bd-131">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="848bd-131">Schema Name</span></span>  <br/> |<span data-ttu-id="848bd-132">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="848bd-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="848bd-133">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="848bd-133">Validation File</span></span>  <br/> |<span data-ttu-id="848bd-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="848bd-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="848bd-135">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="848bd-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="848bd-136">False</span><span class="sxs-lookup"><span data-stu-id="848bd-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="848bd-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="848bd-137">See also</span></span>

- [<span data-ttu-id="848bd-138">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="848bd-138">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
- [<span data-ttu-id="848bd-139">Obtención de disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="848bd-139">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

