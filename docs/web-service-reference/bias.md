---
title: Sesgo
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Bias
api_type:
- schema
ms.assetid: ae10aa44-e6d3-483d-a3e6-bb9c45966810
description: El elemento bias representa el desplazamiento del desplazamiento de la hora universal coordinada (UTC) identificado por el elemento Bias (UTC) para el horario estándar y el horario de verano. Este valor está en minutos.
ms.openlocfilehash: 6c9dce88f3eece9c793fb018114f07a85c7cb89b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460242"
---
# <a name="bias"></a><span data-ttu-id="08197-104">Sesgo</span><span class="sxs-lookup"><span data-stu-id="08197-104">Bias</span></span>

<span data-ttu-id="08197-105">El elemento **Bias** representa el desplazamiento del desplazamiento de la hora universal coordinada (UTC) identificado por el elemento [Bias (UTC)](bias-utc.md) para el horario estándar y el horario de verano.</span><span class="sxs-lookup"><span data-stu-id="08197-105">The **Bias** element represents the offset from the Coordinated Universal Time (UTC) offset identified by the [Bias (UTC)](bias-utc.md) element for standard time and daylight saving time.</span></span> <span data-ttu-id="08197-106">Este valor está en minutos.</span><span class="sxs-lookup"><span data-stu-id="08197-106">This value is in minutes.</span></span> 
  
```xml
<Bias>...</Bias>
```

<span data-ttu-id="08197-107">**int**</span><span class="sxs-lookup"><span data-stu-id="08197-107">**int**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="08197-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="08197-108">Attributes and elements</span></span>

<span data-ttu-id="08197-109">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="08197-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="08197-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="08197-110">Attributes</span></span>

<span data-ttu-id="08197-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="08197-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="08197-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="08197-112">Child elements</span></span>

<span data-ttu-id="08197-113">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="08197-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="08197-114">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="08197-114">Parent elements</span></span>

|<span data-ttu-id="08197-115">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="08197-115">**Element**</span></span>|<span data-ttu-id="08197-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="08197-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="08197-117">Standardtime Element</span><span class="sxs-lookup"><span data-stu-id="08197-117">StandardTime</span></span>](standardtime.md) <br/> | <span data-ttu-id="08197-118">Representa un desplazamiento del tiempo relativo a la hora UTC representado por el elemento [Bias (UTC)](bias-utc.md) .</span><span class="sxs-lookup"><span data-stu-id="08197-118">Represents an offset from the time relative to UTC represented by the [Bias (UTC)](bias-utc.md) element.</span></span> <span data-ttu-id="08197-119">Este elemento también contiene información sobre la transición a la hora estándar del horario de verano en regiones en las que se observa el horario de verano.</span><span class="sxs-lookup"><span data-stu-id="08197-119">This element also contains information about the transition to standard time from daylight saving time in regions where daylight saving time is observed.</span></span><br/><br/><span data-ttu-id="08197-120">Las siguientes son las expresiones XPath para el elemento [standardtime Element](standardtime.md) :</span><span class="sxs-lookup"><span data-stu-id="08197-120">The following are the XPath expressions to the [StandardTime](standardtime.md) element:</span></span><br/><br/>   `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/TimeZone/StandardTime` <br/><br/> `/GetUserAvailabilityRequest/TimeZone/StandardTime` <br/> |
|[<span data-ttu-id="08197-121">DaylightTime</span><span class="sxs-lookup"><span data-stu-id="08197-121">DaylightTime</span></span>](daylighttime.md) <br/> | <span data-ttu-id="08197-122">Representa un desplazamiento del tiempo relativo a la hora UTC representado por el elemento [Bias (UTC)](bias-utc.md) en las regiones en las que se observa el horario de verano.</span><span class="sxs-lookup"><span data-stu-id="08197-122">Represents an offset from the time relative to UTC represented by the [Bias (UTC)](bias-utc.md) element in regions where daylight saving time is observed.</span></span> <span data-ttu-id="08197-123">Este elemento también contiene información sobre cuándo se produce la transición al horario de verano desde la hora estándar.</span><span class="sxs-lookup"><span data-stu-id="08197-123">This element also contains information about when the transition to daylight saving time from standard time occurs.</span></span>  <br/><br/><span data-ttu-id="08197-124">Las siguientes son las expresiones XPath para el elemento [DaylightTime](daylighttime.md) :</span><span class="sxs-lookup"><span data-stu-id="08197-124">The following are the XPath expressions to the [DaylightTime](daylighttime.md) element:</span></span><br/><br/> `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/TimeZone/DaylightTime` <br/><br/> `/GetUserAvailabilityRequest/TimeZone/DaylightTime` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="08197-125">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="08197-125">Text value</span></span>

<span data-ttu-id="08197-126">Se requiere un valor de texto.</span><span class="sxs-lookup"><span data-stu-id="08197-126">A text value is required.</span></span> <span data-ttu-id="08197-127">El valor de texto representa un número entero.</span><span class="sxs-lookup"><span data-stu-id="08197-127">The text value represents an integer.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="08197-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="08197-128">Remarks</span></span>

<span data-ttu-id="08197-129">El desplazamiento que se usa para determinar la hora local solo puede ser proporcionado por uno de los elementos **Bias** .</span><span class="sxs-lookup"><span data-stu-id="08197-129">The offset used to determine the local time can only be provided by one of the **Bias** elements.</span></span> <span data-ttu-id="08197-130">La suma de los valores del elemento bias proporcionado por el elemento [DaylightTime](daylighttime.md) o el elemento [standardtime Element](standardtime.md) más el elemento [Bias (UTC)](bias-utc.md) identifica la hora local.</span><span class="sxs-lookup"><span data-stu-id="08197-130">The sum of the values of the Bias element provided by the [DaylightTime](daylighttime.md) element or the [StandardTime](standardtime.md) element plus the [Bias (UTC)](bias-utc.md) element identifies the local time.</span></span> 
  
## <a name="example"></a><span data-ttu-id="08197-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="08197-131">Example</span></span>

<span data-ttu-id="08197-132">En el ejemplo siguiente se muestra parte de una solicitud XML que identifica a un usuario que observa el horario de verano mediante el ajuste del desplazamiento con respecto a la hora UTC de-60 minutos.</span><span class="sxs-lookup"><span data-stu-id="08197-132">The following example shows part of an XML request that identifies a user who observes daylight saving time by adjusting the offset from UTC by -60 minutes.</span></span> <span data-ttu-id="08197-133">Esto hace que la diferencia sea de 420 minutos respecto a la hora UTC.</span><span class="sxs-lookup"><span data-stu-id="08197-133">This effectively makes the bias 420 minutes from UTC.</span></span>
  
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

## <a name="element-information"></a><span data-ttu-id="08197-134">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="08197-134">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="08197-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="08197-135">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="08197-136">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="08197-136">Schema Name</span></span>  <br/> |<span data-ttu-id="08197-137">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="08197-137">Types schema</span></span>  <br/> |
|<span data-ttu-id="08197-138">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="08197-138">Validation File</span></span>  <br/> |<span data-ttu-id="08197-139">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="08197-139">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="08197-140">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="08197-140">Can be Empty</span></span>  <br/> |<span data-ttu-id="08197-141">Falso</span><span class="sxs-lookup"><span data-stu-id="08197-141">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="08197-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="08197-142">See also</span></span>

- [<span data-ttu-id="08197-143">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="08197-143">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
- [<span data-ttu-id="08197-144">Obtener disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="08197-144">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

