---
title: Month
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
description: El elemento month representa el mes de transición del año a y desde la hora estándar y el horario de verano.
ms.openlocfilehash: f102dca4ed9e833b9742844cfd612c81dfd05e70
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468624"
---
# <a name="month"></a><span data-ttu-id="e444a-103">Month</span><span class="sxs-lookup"><span data-stu-id="e444a-103">Month</span></span>

<span data-ttu-id="e444a-104">El elemento **Month** representa el mes de transición del año a y desde la hora estándar y el horario de verano.</span><span class="sxs-lookup"><span data-stu-id="e444a-104">The **Month** element represents the transition month of the year to and from standard time and daylight saving time.</span></span> 
  
```xml
<Month>...</Month>
```

 <span data-ttu-id="e444a-105">**Short**</span><span class="sxs-lookup"><span data-stu-id="e444a-105">**Short**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e444a-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="e444a-106">Attributes and elements</span></span>

<span data-ttu-id="e444a-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="e444a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e444a-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="e444a-108">Attributes</span></span>

<span data-ttu-id="e444a-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="e444a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e444a-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="e444a-110">Child elements</span></span>

<span data-ttu-id="e444a-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="e444a-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="e444a-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="e444a-112">Parent elements</span></span>

|<span data-ttu-id="e444a-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="e444a-113">**Element**</span></span>|<span data-ttu-id="e444a-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e444a-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e444a-115">Standardtime Element</span><span class="sxs-lookup"><span data-stu-id="e444a-115">StandardTime</span></span>](standardtime.md) <br/> | <span data-ttu-id="e444a-116">Representa un desplazamiento del tiempo con respecto a la hora universal coordinada (UTC) representada por el elemento [Bias (UTC)](bias-utc.md) .</span><span class="sxs-lookup"><span data-stu-id="e444a-116">Represents an offset from the time relative to Coordinated Universal Time (UTC) represented by the [Bias (UTC)](bias-utc.md) element.</span></span> <span data-ttu-id="e444a-117">Este elemento también contiene información sobre la transición a la hora estándar del horario de verano en regiones en las que se observa el horario de verano.</span><span class="sxs-lookup"><span data-stu-id="e444a-117">This element also contains information about the transition to standard time from daylight saving time in regions where daylight saving time is observed.</span></span> <br/> <br/>  <span data-ttu-id="e444a-118">Las siguientes son las expresiones XPath para el elemento [standardtime Element](standardtime.md) :</span><span class="sxs-lookup"><span data-stu-id="e444a-118">The following are the XPath expressions to the [StandardTime](standardtime.md) element:</span></span> <br/> <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/TimeZone/StandardTime` <br/><br/>  `/GetUserAvailabilityRequest/TimeZone/StandardTime` <br/> |
|[<span data-ttu-id="e444a-119">DaylightTime</span><span class="sxs-lookup"><span data-stu-id="e444a-119">DaylightTime</span></span>](daylighttime.md) <br/> | <span data-ttu-id="e444a-120">Representa un desplazamiento del tiempo relativo a la hora UTC representado por el elemento [Bias (UTC)](bias-utc.md) en las regiones en las que se observa el horario de verano.</span><span class="sxs-lookup"><span data-stu-id="e444a-120">Represents an offset from the time relative to UTC represented by the [Bias (UTC)](bias-utc.md) element in regions where daylight saving time is observed.</span></span> <span data-ttu-id="e444a-121">Este elemento también contiene información sobre cuándo se produce la transición al horario de verano desde la hora estándar.</span><span class="sxs-lookup"><span data-stu-id="e444a-121">This element also contains information about when the transition to daylight saving time from standard time occurs.</span></span>  <br/><br/>  <span data-ttu-id="e444a-122">Las siguientes son las expresiones XPath para el elemento [DaylightTime](daylighttime.md) :</span><span class="sxs-lookup"><span data-stu-id="e444a-122">The following are the XPath expressions to the [DaylightTime](daylighttime.md) element:</span></span>  <br/> <br/> `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/TimeZone/DaylightTime` <br/><br/>  `/GetUserAvailabilityRequest/TimeZone/DaylightTime` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="e444a-123">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="e444a-123">Text value</span></span>

<span data-ttu-id="e444a-124">Se requiere un valor de texto.</span><span class="sxs-lookup"><span data-stu-id="e444a-124">A text value is required.</span></span> <span data-ttu-id="e444a-125">El valor representa el rango ordinal del mes por su ocurrencia y debe ser un número comprendido entre 1 y 12.</span><span class="sxs-lookup"><span data-stu-id="e444a-125">The value represents the ordinal rank of the month by occurrence and must be a number between 1 and 12.</span></span> <span data-ttu-id="e444a-126">Se trata de un tipo de datos entero corto.</span><span class="sxs-lookup"><span data-stu-id="e444a-126">This is a short integer data type.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e444a-127">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e444a-127">Remarks</span></span>

<span data-ttu-id="e444a-128">Un elemento [standardtime Element](standardtime.md) que contiene un elemento [DayOrder](dayorder.md) que tiene un valor de 5, un elemento **Month** que tiene un valor de 10, y un elemento [DayOfWeek (TimeZone)](dayofweek-timezone.md) que tiene un valor de domingo, significa que la transición de la hora estándar al horario de verano se produce el quinto domingo del décimo mes.</span><span class="sxs-lookup"><span data-stu-id="e444a-128">A [StandardTime](standardtime.md) element that contains a [DayOrder](dayorder.md) element that has a value of 5, a **Month** element that has a value of 10, and a [DayOfWeek (TimeZone)](dayofweek-timezone.md) element that has a value of Sunday means that the transition from standard time to daylight saving time occurs on the fifth Sunday of the tenth month.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="e444a-129">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="e444a-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e444a-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="e444a-130">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="e444a-131">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="e444a-131">Schema Name</span></span>  <br/> |<span data-ttu-id="e444a-132">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="e444a-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="e444a-133">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="e444a-133">Validation File</span></span>  <br/> |<span data-ttu-id="e444a-134">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="e444a-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="e444a-135">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="e444a-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="e444a-136">Falso</span><span class="sxs-lookup"><span data-stu-id="e444a-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e444a-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="e444a-137">See also</span></span>

- [<span data-ttu-id="e444a-138">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="e444a-138">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
- [<span data-ttu-id="e444a-139">Obtener disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="e444a-139">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

