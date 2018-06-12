---
title: WeeklyRecurrence
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- WeeklyRecurrence
api_type:
- schema
ms.assetid: 69c41dd5-597c-45bc-be3f-e2f2b5615aa3
description: El elemento WeeklyRecurrence describe un patrón de periodicidad semanal.
ms.openlocfilehash: 78bc76dd63c6737786df02f336217dc8de9a3a67
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19840993"
---
# <a name="weeklyrecurrence"></a><span data-ttu-id="39a9e-103">WeeklyRecurrence</span><span class="sxs-lookup"><span data-stu-id="39a9e-103">WeeklyRecurrence</span></span>

<span data-ttu-id="39a9e-104">El elemento **WeeklyRecurrence** describe un patrón de periodicidad semanal.</span><span class="sxs-lookup"><span data-stu-id="39a9e-104">The **WeeklyRecurrence** element describes a weekly recurrence pattern.</span></span> 
  
```XML
<WeeklyRecurrence>
   <Interval/>
   <DaysOfWeek/>
   <FirstDayOfWeek/>
</WeeklyRecurrence>
```

 <span data-ttu-id="39a9e-105">**WeeklyRecurrencePatternType**</span><span class="sxs-lookup"><span data-stu-id="39a9e-105">**WeeklyRecurrencePatternType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="39a9e-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="39a9e-106">Attributes and elements</span></span>

<span data-ttu-id="39a9e-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="39a9e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="39a9e-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="39a9e-108">Attributes</span></span>

<span data-ttu-id="39a9e-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="39a9e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="39a9e-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="39a9e-110">Child elements</span></span>

|<span data-ttu-id="39a9e-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="39a9e-111">**Element**</span></span>|<span data-ttu-id="39a9e-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="39a9e-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="39a9e-113">Interval</span><span class="sxs-lookup"><span data-stu-id="39a9e-113">Interval</span></span>](interval.md) <br/> |<span data-ttu-id="39a9e-114">Define el intervalo de semanas entre dos consecutivos elementos de patrón de periodicidad semanal.</span><span class="sxs-lookup"><span data-stu-id="39a9e-114">Defines the interval, in weeks, between two consecutive weekly recurrence pattern items.</span></span> <span data-ttu-id="39a9e-115">El valor puede ser comprendido entre 1 y 99.</span><span class="sxs-lookup"><span data-stu-id="39a9e-115">The value can be in the range from 1 to 99.</span></span>  <br/> |
|[<span data-ttu-id="39a9e-116">DaysOfWeek (DaysOfWeekType)</span><span class="sxs-lookup"><span data-stu-id="39a9e-116">DaysOfWeek (DaysOfWeekType)</span></span>](daysofweek-daysofweektype.md) <br/> |<span data-ttu-id="39a9e-117">Se describen los días de la semana en el patrón de periodicidad semanal.</span><span class="sxs-lookup"><span data-stu-id="39a9e-117">Describes which days of the week are in the weekly recurrence pattern.</span></span>  <br/> |
|[<span data-ttu-id="39a9e-118">FirstDayOfWeek</span><span class="sxs-lookup"><span data-stu-id="39a9e-118">FirstDayOfWeek</span></span>](firstdayofweek.md) <br/> |<span data-ttu-id="39a9e-119">Especifica el primer día de la semana.</span><span class="sxs-lookup"><span data-stu-id="39a9e-119">Specifies the first day of the week.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="39a9e-120">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="39a9e-120">Parent elements</span></span>

|<span data-ttu-id="39a9e-121">**Element**</span><span class="sxs-lookup"><span data-stu-id="39a9e-121">**Element**</span></span>|<span data-ttu-id="39a9e-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="39a9e-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="39a9e-123">Periodicidad (TaskRecurrenceType)</span><span class="sxs-lookup"><span data-stu-id="39a9e-123">Recurrence (TaskRecurrenceType)</span></span>](recurrence-taskrecurrencetype.md) <br/> |<span data-ttu-id="39a9e-124">Contiene información sobre la periodicidad para las tareas repetitivas.</span><span class="sxs-lookup"><span data-stu-id="39a9e-124">Contains recurrence information for recurring tasks.</span></span>  <br/> |
|[<span data-ttu-id="39a9e-125">Periodicidad (RecurrenceType)</span><span class="sxs-lookup"><span data-stu-id="39a9e-125">Recurrence (RecurrenceType)</span></span>](recurrence-recurrencetype.md) <br/> |<span data-ttu-id="39a9e-126">Contiene el patrón de periodicidad para los elementos de calendario y las convocatorias de reunión.</span><span class="sxs-lookup"><span data-stu-id="39a9e-126">Contains the recurrence pattern for calendar items and meeting requests.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="39a9e-127">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="39a9e-127">Text value</span></span>

<span data-ttu-id="39a9e-128">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="39a9e-128">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="39a9e-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="39a9e-129">Remarks</span></span>

<span data-ttu-id="39a9e-130">Si las fechas de [comienzo](start.md) y de [finalización](end-ex15websvcsotherref.md) del elemento maestro periódico no tienen una fecha que es igual a la primera aparición de un patrón de periodicidad semanal, se pierde la información de desplazamiento de zona horaria.</span><span class="sxs-lookup"><span data-stu-id="39a9e-130">The time zone offset information is lost if the [Start](start.md) and [End ](end-ex15websvcsotherref.md) dates of the recurring master item do not have a date that is equal to the first occurrence of a weekly recurrence pattern.</span></span> 
  
<span data-ttu-id="39a9e-131">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="39a9e-131">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="39a9e-132">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="39a9e-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="39a9e-133">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="39a9e-133">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="39a9e-134">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="39a9e-134">Schema Name</span></span>  <br/> |<span data-ttu-id="39a9e-135">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="39a9e-135">Types schema</span></span>  <br/> |
|<span data-ttu-id="39a9e-136">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="39a9e-136">Validation File</span></span>  <br/> |<span data-ttu-id="39a9e-137">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="39a9e-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="39a9e-138">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="39a9e-138">Can be Empty</span></span>  <br/> |<span data-ttu-id="39a9e-139">False</span><span class="sxs-lookup"><span data-stu-id="39a9e-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="39a9e-140">Ver también</span><span class="sxs-lookup"><span data-stu-id="39a9e-140">See also</span></span>



- [<span data-ttu-id="39a9e-141">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="39a9e-141">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

