---
title: RelativeYearlyRecurrence
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RelativeYearlyRecurrence
api_type:
- schema
ms.assetid: 25b67876-9979-4a30-a637-357ea10a93b8
description: El elemento RelativeYearlyRecurrence describe un patrón de periodicidad anual relativa.
ms.openlocfilehash: ce8d2b134ce1fa34cbce8bd2fa921cab18d908a4
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19837057"
---
# <a name="relativeyearlyrecurrence"></a><span data-ttu-id="c92e0-103">RelativeYearlyRecurrence</span><span class="sxs-lookup"><span data-stu-id="c92e0-103">RelativeYearlyRecurrence</span></span>

<span data-ttu-id="c92e0-104">El elemento **RelativeYearlyRecurrence** describe un patrón de periodicidad anual relativa.</span><span class="sxs-lookup"><span data-stu-id="c92e0-104">The **RelativeYearlyRecurrence** element describes a relative yearly recurrence pattern.</span></span> 
  
```xml
<RelativeYearlyRecurrence>
   <DaysOfWeek/>
   <DayOfWeekIndex/>
   <Month/>
</RelativeYearlyRecurrence>
```

 <span data-ttu-id="c92e0-105">**RelativeYearlyRecurrencePatternType**</span><span class="sxs-lookup"><span data-stu-id="c92e0-105">**RelativeYearlyRecurrencePatternType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c92e0-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="c92e0-106">Attributes and elements</span></span>

<span data-ttu-id="c92e0-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="c92e0-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c92e0-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="c92e0-108">Attributes</span></span>

<span data-ttu-id="c92e0-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="c92e0-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c92e0-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c92e0-110">Child elements</span></span>

|<span data-ttu-id="c92e0-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="c92e0-111">**Element**</span></span>|<span data-ttu-id="c92e0-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c92e0-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c92e0-113">DaysOfWeek (DayOfWeekType)</span><span class="sxs-lookup"><span data-stu-id="c92e0-113">DaysOfWeek (DayOfWeekType)</span></span>](daysofweek-dayofweektype.md) <br/> |<span data-ttu-id="c92e0-114">Describe los días de la semana que se usan en los patrones de periodicidad de elemento.</span><span class="sxs-lookup"><span data-stu-id="c92e0-114">Describes the days of the week that are used in item recurrence patterns.</span></span>  <br/> |
|[<span data-ttu-id="c92e0-115">DayOfWeekIndex</span><span class="sxs-lookup"><span data-stu-id="c92e0-115">DayOfWeekIndex</span></span>](dayofweekindex.md) <br/> |<span data-ttu-id="c92e0-116">Describe qué semana en un mes se utiliza en un patrón de periodicidad anual relativa.</span><span class="sxs-lookup"><span data-stu-id="c92e0-116">Describes which week in a month is used in a relative yearly recurrence pattern.</span></span>  <br/> |
|[<span data-ttu-id="c92e0-117">Mes (elemento periodicidad)</span><span class="sxs-lookup"><span data-stu-id="c92e0-117">Month (Item Recurrence)</span></span>](month-item-recurrence.md) <br/> |<span data-ttu-id="c92e0-118">Describe el mes cuando se produce un elemento periódico anual.</span><span class="sxs-lookup"><span data-stu-id="c92e0-118">Describes the month when a yearly recurring item occurs.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="c92e0-119">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="c92e0-119">Parent elements</span></span>

|<span data-ttu-id="c92e0-120">**Element**</span><span class="sxs-lookup"><span data-stu-id="c92e0-120">**Element**</span></span>|<span data-ttu-id="c92e0-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c92e0-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c92e0-122">Periodicidad (TaskRecurrenceType)</span><span class="sxs-lookup"><span data-stu-id="c92e0-122">Recurrence (TaskRecurrenceType)</span></span>](recurrence-taskrecurrencetype.md) <br/> |<span data-ttu-id="c92e0-123">Contiene información sobre la periodicidad para las tareas repetitivas.</span><span class="sxs-lookup"><span data-stu-id="c92e0-123">Contains recurrence information for recurring tasks.</span></span>  <br/> |
|[<span data-ttu-id="c92e0-124">Periodicidad (RecurrenceType)</span><span class="sxs-lookup"><span data-stu-id="c92e0-124">Recurrence (RecurrenceType)</span></span>](recurrence-recurrencetype.md) <br/> |<span data-ttu-id="c92e0-125">Contiene el patrón de periodicidad para los elementos de calendario y las convocatorias de reunión.</span><span class="sxs-lookup"><span data-stu-id="c92e0-125">Contains the recurrence pattern for calendar items and meeting requests.</span></span>  <br/> |
|[<span data-ttu-id="c92e0-126">Standard</span><span class="sxs-lookup"><span data-stu-id="c92e0-126">Standard</span></span>](standard.md) <br/> |<span data-ttu-id="c92e0-127">Representa la fecha y hora cuando se cambia la hora del horario de verano a la hora estándar.</span><span class="sxs-lookup"><span data-stu-id="c92e0-127">Represents the date and time when the time changes from daylight saving time to standard time.</span></span>  <br/> |
|[<span data-ttu-id="c92e0-128">Horario de verano</span><span class="sxs-lookup"><span data-stu-id="c92e0-128">Daylight</span></span>](daylight.md) <br/> |<span data-ttu-id="c92e0-129">Representa la fecha y hora en que cambia el tiempo de la hora estándar al horario de verano.</span><span class="sxs-lookup"><span data-stu-id="c92e0-129">Represents the date and time when the time changes from standard time to daylight saving time.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c92e0-130">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c92e0-130">Remarks</span></span>

<span data-ttu-id="c92e0-131">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="c92e0-131">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c92e0-132">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="c92e0-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c92e0-133">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c92e0-133">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c92e0-134">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="c92e0-134">Schema Name</span></span>  <br/> |<span data-ttu-id="c92e0-135">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="c92e0-135">Types schema</span></span>  <br/> |
|<span data-ttu-id="c92e0-136">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="c92e0-136">Validation File</span></span>  <br/> |<span data-ttu-id="c92e0-137">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="c92e0-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="c92e0-138">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="c92e0-138">Can be Empty</span></span>  <br/> |<span data-ttu-id="c92e0-139">False</span><span class="sxs-lookup"><span data-stu-id="c92e0-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c92e0-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="c92e0-140">See also</span></span>



- [<span data-ttu-id="c92e0-141">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="c92e0-141">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

