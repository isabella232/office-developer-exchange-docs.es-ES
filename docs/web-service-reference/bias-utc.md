---
title: Bias (UTC)
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
ms.assetid: 15790d5a-5134-457b-8f2b-d9dee1f807a2
description: El elemento Bias representa el desplazamiento general de la hora Universal coordinada (UTC). Este valor está en minutos.
ms.openlocfilehash: 43613593565ca15be97bd2a98dbe5c512dbe5fc7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763617"
---
# <a name="bias-utc"></a><span data-ttu-id="3fdbd-104">Bias (UTC)</span><span class="sxs-lookup"><span data-stu-id="3fdbd-104">Bias (UTC)</span></span>

<span data-ttu-id="3fdbd-105">El elemento **Bias** representa el desplazamiento general de la hora Universal coordinada (UTC).</span><span class="sxs-lookup"><span data-stu-id="3fdbd-105">The **Bias** element represents the general offset from Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="3fdbd-106">Este valor está en minutos.</span><span class="sxs-lookup"><span data-stu-id="3fdbd-106">This value is in minutes.</span></span> 
  
```xml
<TimeZone>
   <Bias>int</Bias>
</TimeZone>
```

<span data-ttu-id="3fdbd-107">**int**</span><span class="sxs-lookup"><span data-stu-id="3fdbd-107">**int**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="3fdbd-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="3fdbd-108">Attributes and elements</span></span>

<span data-ttu-id="3fdbd-109">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="3fdbd-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3fdbd-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="3fdbd-110">Attributes</span></span>

<span data-ttu-id="3fdbd-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="3fdbd-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3fdbd-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="3fdbd-112">Child elements</span></span>

<span data-ttu-id="3fdbd-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="3fdbd-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="3fdbd-114">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="3fdbd-114">Parent elements</span></span>

|<span data-ttu-id="3fdbd-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="3fdbd-115">**Element**</span></span>|<span data-ttu-id="3fdbd-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3fdbd-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3fdbd-117">TimeZone (disponibilidad)</span><span class="sxs-lookup"><span data-stu-id="3fdbd-117">TimeZone (Availability)</span></span>](timezone-availability.md) <br/> | <span data-ttu-id="3fdbd-118">El contenedor que identifica la información de fecha y hora de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="3fdbd-118">The container that identifies the date-time information of the request.</span></span> <span data-ttu-id="3fdbd-119">Este elemento contiene información sobre la transición entre la hora estándar y el horario de verano.</span><span class="sxs-lookup"><span data-stu-id="3fdbd-119">This element contains information about the transition between standard time and daylight saving time.</span></span>  <br/><br/><span data-ttu-id="3fdbd-120">Los siguientes son las expresiones de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="3fdbd-120">The following are the XPath expressions to this element:</span></span><br/><br/>   `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/TimeZone` <br/><br/>`/GetUserAvailabilityRequest/TimeZone` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="3fdbd-121">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="3fdbd-121">Text value</span></span>

<span data-ttu-id="3fdbd-122">Se requiere un valor de texto.</span><span class="sxs-lookup"><span data-stu-id="3fdbd-122">A text value is required.</span></span> <span data-ttu-id="3fdbd-123">El valor de texto representa un número entero.</span><span class="sxs-lookup"><span data-stu-id="3fdbd-123">The text value represents an integer.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3fdbd-124">Notas</span><span class="sxs-lookup"><span data-stu-id="3fdbd-124">Remarks</span></span>

<span data-ttu-id="3fdbd-125">Un segundo elemento [Bias](bias.md) en el esquema representa el desplazamiento desde el desplazamiento de hora Universal coordinada (UTC).</span><span class="sxs-lookup"><span data-stu-id="3fdbd-125">A second [Bias](bias.md) element in the schema represents the offset from the Coordinated Universal Time (UTC) offset.</span></span> 
  
## <a name="example"></a><span data-ttu-id="3fdbd-126">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3fdbd-126">Example</span></span>

<span data-ttu-id="3fdbd-127">En el ejemplo siguiente se muestra parte de una solicitud XML que identifica un desplazamiento de 8 horas de la hora UTC en la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="3fdbd-127">The following example shows part of an XML request that identifies an offset of 8 hours from UTC on the client application.</span></span>
  
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

## <a name="element-information"></a><span data-ttu-id="3fdbd-128">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="3fdbd-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3fdbd-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3fdbd-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="3fdbd-130">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="3fdbd-130">Schema Name</span></span>  <br/> |<span data-ttu-id="3fdbd-131">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="3fdbd-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="3fdbd-132">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="3fdbd-132">Validation File</span></span>  <br/> |<span data-ttu-id="3fdbd-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="3fdbd-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="3fdbd-134">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="3fdbd-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="3fdbd-135">False</span><span class="sxs-lookup"><span data-stu-id="3fdbd-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3fdbd-136">Ver también</span><span class="sxs-lookup"><span data-stu-id="3fdbd-136">See also</span></span>

- [<span data-ttu-id="3fdbd-137">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="3fdbd-137">GetUserAvailability operation</span></span>](getuseravailability-operation.md)  
- [<span data-ttu-id="3fdbd-138">Bias</span><span class="sxs-lookup"><span data-stu-id="3fdbd-138">Bias</span></span>](bias.md)
- [<span data-ttu-id="3fdbd-139">Obtención de disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="3fdbd-139">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

