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
ms.openlocfilehash: 5006238590c4cd7556a92fb1fbe13292383412b8
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530369"
---
# <a name="weeklyrecurrence"></a><span data-ttu-id="02f56-103">WeeklyRecurrence</span><span class="sxs-lookup"><span data-stu-id="02f56-103">WeeklyRecurrence</span></span>

<span data-ttu-id="02f56-104">El elemento **WeeklyRecurrence** describe un patrón de periodicidad semanal.</span><span class="sxs-lookup"><span data-stu-id="02f56-104">The **WeeklyRecurrence** element describes a weekly recurrence pattern.</span></span> 
  
```XML
<WeeklyRecurrence>
   <Interval/>
   <DaysOfWeek/>
   <FirstDayOfWeek/>
</WeeklyRecurrence>
```

 <span data-ttu-id="02f56-105">**WeeklyRecurrencePatternType**</span><span class="sxs-lookup"><span data-stu-id="02f56-105">**WeeklyRecurrencePatternType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="02f56-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="02f56-106">Attributes and elements</span></span>

<span data-ttu-id="02f56-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="02f56-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="02f56-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="02f56-108">Attributes</span></span>

<span data-ttu-id="02f56-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="02f56-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="02f56-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="02f56-110">Child elements</span></span>

|<span data-ttu-id="02f56-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="02f56-111">**Element**</span></span>|<span data-ttu-id="02f56-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="02f56-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="02f56-113">Intervalo de</span><span class="sxs-lookup"><span data-stu-id="02f56-113">Interval</span></span>](interval.md) <br/> |<span data-ttu-id="02f56-114">Define el intervalo, en semanas, entre dos elementos de patrón de periodicidad semanal consecutivos.</span><span class="sxs-lookup"><span data-stu-id="02f56-114">Defines the interval, in weeks, between two consecutive weekly recurrence pattern items.</span></span> <span data-ttu-id="02f56-115">El valor puede estar comprendido entre 1 y 99.</span><span class="sxs-lookup"><span data-stu-id="02f56-115">The value can be in the range from 1 to 99.</span></span>  <br/> |
|[<span data-ttu-id="02f56-116">DaysOfWeek (DaysOfWeekType)</span><span class="sxs-lookup"><span data-stu-id="02f56-116">DaysOfWeek (DaysOfWeekType)</span></span>](daysofweek-daysofweektype.md) <br/> |<span data-ttu-id="02f56-117">Describe qué días de la semana hay en el patrón de periodicidad semanal.</span><span class="sxs-lookup"><span data-stu-id="02f56-117">Describes which days of the week are in the weekly recurrence pattern.</span></span>  <br/> |
|[<span data-ttu-id="02f56-118">FirstDayOfWeek</span><span class="sxs-lookup"><span data-stu-id="02f56-118">FirstDayOfWeek</span></span>](firstdayofweek.md) <br/> |<span data-ttu-id="02f56-119">Especifica el primer día de la semana.</span><span class="sxs-lookup"><span data-stu-id="02f56-119">Specifies the first day of the week.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="02f56-120">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="02f56-120">Parent elements</span></span>

|<span data-ttu-id="02f56-121">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="02f56-121">**Element**</span></span>|<span data-ttu-id="02f56-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="02f56-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="02f56-123">Periodicidad (TaskRecurrenceType)</span><span class="sxs-lookup"><span data-stu-id="02f56-123">Recurrence (TaskRecurrenceType)</span></span>](recurrence-taskrecurrencetype.md) <br/> |<span data-ttu-id="02f56-124">Contiene información de periodicidad para tareas periódicas.</span><span class="sxs-lookup"><span data-stu-id="02f56-124">Contains recurrence information for recurring tasks.</span></span>  <br/> |
|[<span data-ttu-id="02f56-125">Recurrence (RecurrenceType)</span><span class="sxs-lookup"><span data-stu-id="02f56-125">Recurrence (RecurrenceType)</span></span>](recurrence-recurrencetype.md) <br/> |<span data-ttu-id="02f56-126">Contiene el patrón de periodicidad para los elementos de calendario y las convocatorias de reunión.</span><span class="sxs-lookup"><span data-stu-id="02f56-126">Contains the recurrence pattern for calendar items and meeting requests.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="02f56-127">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="02f56-127">Text value</span></span>

<span data-ttu-id="02f56-128">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="02f56-128">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="02f56-129">Comentarios</span><span class="sxs-lookup"><span data-stu-id="02f56-129">Remarks</span></span>

<span data-ttu-id="02f56-130">La información de desplazamiento de zona horaria se pierde si las fechas de [Inicio](start.md) y [finalización](end-ex15websvcsotherref.md) del elemento maestro periódico no tienen una fecha igual a la primera aparición de un patrón de periodicidad semanal.</span><span class="sxs-lookup"><span data-stu-id="02f56-130">The time zone offset information is lost if the [Start](start.md) and [End ](end-ex15websvcsotherref.md) dates of the recurring master item do not have a date that is equal to the first occurrence of a weekly recurrence pattern.</span></span> 
  
<span data-ttu-id="02f56-131">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="02f56-131">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="02f56-132">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="02f56-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="02f56-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="02f56-133">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="02f56-134">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="02f56-134">Schema Name</span></span>  <br/> |<span data-ttu-id="02f56-135">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="02f56-135">Types schema</span></span>  <br/> |
|<span data-ttu-id="02f56-136">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="02f56-136">Validation File</span></span>  <br/> |<span data-ttu-id="02f56-137">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="02f56-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="02f56-138">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="02f56-138">Can be Empty</span></span>  <br/> |<span data-ttu-id="02f56-139">Falso</span><span class="sxs-lookup"><span data-stu-id="02f56-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="02f56-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="02f56-140">See also</span></span>



- [<span data-ttu-id="02f56-141">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="02f56-141">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

