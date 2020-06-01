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
description: El elemento bias representa el desplazamiento general desde la hora universal coordinada (UTC). Este valor está en minutos.
ms.openlocfilehash: d95284aa28e59542d1a1ee40686163138b015702
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460249"
---
# <a name="bias-utc"></a><span data-ttu-id="cae64-104">Bias (UTC)</span><span class="sxs-lookup"><span data-stu-id="cae64-104">Bias (UTC)</span></span>

<span data-ttu-id="cae64-105">El elemento **Bias** representa el desplazamiento general desde la hora universal coordinada (UTC).</span><span class="sxs-lookup"><span data-stu-id="cae64-105">The **Bias** element represents the general offset from Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="cae64-106">Este valor está en minutos.</span><span class="sxs-lookup"><span data-stu-id="cae64-106">This value is in minutes.</span></span> 
  
```xml
<TimeZone>
   <Bias>int</Bias>
</TimeZone>
```

<span data-ttu-id="cae64-107">**int**</span><span class="sxs-lookup"><span data-stu-id="cae64-107">**int**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="cae64-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="cae64-108">Attributes and elements</span></span>

<span data-ttu-id="cae64-109">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="cae64-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cae64-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="cae64-110">Attributes</span></span>

<span data-ttu-id="cae64-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="cae64-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="cae64-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="cae64-112">Child elements</span></span>

<span data-ttu-id="cae64-113">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="cae64-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="cae64-114">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="cae64-114">Parent elements</span></span>

|<span data-ttu-id="cae64-115">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="cae64-115">**Element**</span></span>|<span data-ttu-id="cae64-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="cae64-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cae64-117">Zona horaria (disponibilidad)</span><span class="sxs-lookup"><span data-stu-id="cae64-117">TimeZone (Availability)</span></span>](timezone-availability.md) <br/> | <span data-ttu-id="cae64-118">Contenedor que identifica la información de fecha y hora de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="cae64-118">The container that identifies the date-time information of the request.</span></span> <span data-ttu-id="cae64-119">Este elemento contiene información sobre la transición entre el horario estándar y el horario de verano.</span><span class="sxs-lookup"><span data-stu-id="cae64-119">This element contains information about the transition between standard time and daylight saving time.</span></span>  <br/><br/><span data-ttu-id="cae64-120">Las siguientes son las expresiones XPath de este elemento:</span><span class="sxs-lookup"><span data-stu-id="cae64-120">The following are the XPath expressions to this element:</span></span><br/><br/>   `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/TimeZone` <br/><br/>`/GetUserAvailabilityRequest/TimeZone` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="cae64-121">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="cae64-121">Text value</span></span>

<span data-ttu-id="cae64-122">Se requiere un valor de texto.</span><span class="sxs-lookup"><span data-stu-id="cae64-122">A text value is required.</span></span> <span data-ttu-id="cae64-123">El valor de texto representa un número entero.</span><span class="sxs-lookup"><span data-stu-id="cae64-123">The text value represents an integer.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="cae64-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="cae64-124">Remarks</span></span>

<span data-ttu-id="cae64-125">Un segundo elemento [Bias](bias.md) en el esquema representa el desplazamiento con respecto a la hora universal coordinada (UTC).</span><span class="sxs-lookup"><span data-stu-id="cae64-125">A second [Bias](bias.md) element in the schema represents the offset from the Coordinated Universal Time (UTC) offset.</span></span> 
  
## <a name="example"></a><span data-ttu-id="cae64-126">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="cae64-126">Example</span></span>

<span data-ttu-id="cae64-127">En el ejemplo siguiente se muestra parte de una solicitud XML que identifica un desplazamiento de 8 horas a partir de UTC en la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="cae64-127">The following example shows part of an XML request that identifies an offset of 8 hours from UTC on the client application.</span></span>
  
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

## <a name="element-information"></a><span data-ttu-id="cae64-128">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="cae64-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cae64-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="cae64-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="cae64-130">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="cae64-130">Schema Name</span></span>  <br/> |<span data-ttu-id="cae64-131">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="cae64-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="cae64-132">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="cae64-132">Validation File</span></span>  <br/> |<span data-ttu-id="cae64-133">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="cae64-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="cae64-134">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="cae64-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="cae64-135">Falso</span><span class="sxs-lookup"><span data-stu-id="cae64-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cae64-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="cae64-136">See also</span></span>

- [<span data-ttu-id="cae64-137">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="cae64-137">GetUserAvailability operation</span></span>](getuseravailability-operation.md)  
- [<span data-ttu-id="cae64-138">Sesgo</span><span class="sxs-lookup"><span data-stu-id="cae64-138">Bias</span></span>](bias.md)
- [<span data-ttu-id="cae64-139">Obtener disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="cae64-139">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

