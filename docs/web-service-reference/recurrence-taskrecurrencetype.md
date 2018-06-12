---
title: Periodicidad (TaskRecurrenceType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Recurrence
api_type:
- schema
ms.assetid: 99f8414a-9110-4721-a6e5-ebf225d7ed0a
description: El elemento de periodicidad contiene información de periodicidad de las tareas repetitivas.
ms.openlocfilehash: ae2bb35e89a0a50c7ca67cb0e580427150afb99e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19837006"
---
# <a name="recurrence-taskrecurrencetype"></a><span data-ttu-id="3135b-103">Periodicidad (TaskRecurrenceType)</span><span class="sxs-lookup"><span data-stu-id="3135b-103">Recurrence (TaskRecurrenceType)</span></span>

<span data-ttu-id="3135b-104">El elemento de **Periodicidad** contiene información de periodicidad de las tareas repetitivas.</span><span class="sxs-lookup"><span data-stu-id="3135b-104">The **Recurrence** element contains recurrence information for recurring tasks.</span></span> 
  
```xml
<Recurrence>
      <RelativeYearlyRecurrence/>
      <NoEndRecurrence/>
</Recurrence>
```

 <span data-ttu-id="3135b-105">**TaskRecurrenceType**</span><span class="sxs-lookup"><span data-stu-id="3135b-105">**TaskRecurrenceType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3135b-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="3135b-106">Attributes and elements</span></span>

<span data-ttu-id="3135b-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="3135b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3135b-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="3135b-108">Attributes</span></span>

<span data-ttu-id="3135b-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="3135b-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3135b-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="3135b-110">Child elements</span></span>

|<span data-ttu-id="3135b-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="3135b-111">**Element**</span></span>|<span data-ttu-id="3135b-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3135b-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3135b-113">RelativeYearlyRecurrence</span><span class="sxs-lookup"><span data-stu-id="3135b-113">RelativeYearlyRecurrence</span></span>](relativeyearlyrecurrence.md) <br/> |<span data-ttu-id="3135b-114">Describe un patrón de periodicidad anual relativa de una tarea periódica.</span><span class="sxs-lookup"><span data-stu-id="3135b-114">Describes a relative yearly recurrence pattern for a recurring task.</span></span>  <br/> |
|[<span data-ttu-id="3135b-115">AbsoluteYearlyRecurrence</span><span class="sxs-lookup"><span data-stu-id="3135b-115">AbsoluteYearlyRecurrence</span></span>](absoluteyearlyrecurrence.md) <br/> |<span data-ttu-id="3135b-116">Representa un patrón de periodicidad anual de una tarea periódica.</span><span class="sxs-lookup"><span data-stu-id="3135b-116">Represents a yearly recurrence pattern for a recurring task.</span></span>  <br/> |
|[<span data-ttu-id="3135b-117">RelativeMonthlyRecurrence</span><span class="sxs-lookup"><span data-stu-id="3135b-117">RelativeMonthlyRecurrence</span></span>](relativemonthlyrecurrence.md) <br/> |<span data-ttu-id="3135b-118">Describe un patrón de periodicidad mensual relativa de una tarea periódica.</span><span class="sxs-lookup"><span data-stu-id="3135b-118">Describes a relative monthly recurrence pattern for a recurring task.</span></span>  <br/> |
|[<span data-ttu-id="3135b-119">AbsoluteMonthlyRecurrence</span><span class="sxs-lookup"><span data-stu-id="3135b-119">AbsoluteMonthlyRecurrence</span></span>](absolutemonthlyrecurrence.md) <br/> |<span data-ttu-id="3135b-120">Representa un patrón de periodicidad mensual para una tarea periódica.</span><span class="sxs-lookup"><span data-stu-id="3135b-120">Represents a monthly recurrence pattern for a recurring task.</span></span>  <br/> |
|[<span data-ttu-id="3135b-121">WeeklyRecurrence</span><span class="sxs-lookup"><span data-stu-id="3135b-121">WeeklyRecurrence</span></span>](weeklyrecurrence.md) <br/> |<span data-ttu-id="3135b-122">Describe la frecuencia, en semanas y los días en que se repite una tarea.</span><span class="sxs-lookup"><span data-stu-id="3135b-122">Describes the frequency, in weeks, and the days on which a task recurs.</span></span>  <br/> |
|[<span data-ttu-id="3135b-123">DailyRecurrence</span><span class="sxs-lookup"><span data-stu-id="3135b-123">DailyRecurrence</span></span>](dailyrecurrence.md) <br/> |<span data-ttu-id="3135b-124">Describe la frecuencia, en días, en el que se repite una tarea.</span><span class="sxs-lookup"><span data-stu-id="3135b-124">Describes the frequency, in days, in which a task recurs.</span></span>  <br/> |
|[<span data-ttu-id="3135b-125">DailyRegeneration</span><span class="sxs-lookup"><span data-stu-id="3135b-125">DailyRegeneration</span></span>](dailyregeneration.md) <br/> |<span data-ttu-id="3135b-126">Describe el número de días después de la finalización de la tarea actual de la siguiente aparición será vencimiento.</span><span class="sxs-lookup"><span data-stu-id="3135b-126">Describes how many days after the completion of the current task the next occurrence will be due.</span></span>  <br/> |
|[<span data-ttu-id="3135b-127">WeeklyRegeneration</span><span class="sxs-lookup"><span data-stu-id="3135b-127">WeeklyRegeneration</span></span>](weeklyregeneration.md) <br/> |<span data-ttu-id="3135b-128">Describe cuántas semanas después de la finalización de la tarea actual de la siguiente aparición será vencimiento.</span><span class="sxs-lookup"><span data-stu-id="3135b-128">Describes how many weeks after the completion of the current task the next occurrence will be due.</span></span>  <br/> |
|[<span data-ttu-id="3135b-129">MonthlyRegeneration</span><span class="sxs-lookup"><span data-stu-id="3135b-129">MonthlyRegeneration</span></span>](monthlyregeneration.md) <br/> |<span data-ttu-id="3135b-130">Describe el número de meses después de la finalización de la tarea actual de la siguiente aparición será vencimiento.</span><span class="sxs-lookup"><span data-stu-id="3135b-130">Describes how many months after the completion of the current task the next occurrence will be due.</span></span>  <br/> |
|[<span data-ttu-id="3135b-131">YearlyRegeneration</span><span class="sxs-lookup"><span data-stu-id="3135b-131">YearlyRegeneration</span></span>](yearlyregeneration.md) <br/> |<span data-ttu-id="3135b-132">Describe cómo muchos años después de la finalización de la tarea actual de la siguiente aparición será vencimiento.</span><span class="sxs-lookup"><span data-stu-id="3135b-132">Describes how many years after the completion of the current task the next occurrence will be due.</span></span>  <br/> |
|[<span data-ttu-id="3135b-133">NoEndRecurrence</span><span class="sxs-lookup"><span data-stu-id="3135b-133">NoEndRecurrence</span></span>](noendrecurrence.md) <br/> |<span data-ttu-id="3135b-134">Describe un patrón de periodicidad que no tiene una fecha de finalización definidas.</span><span class="sxs-lookup"><span data-stu-id="3135b-134">Describes a recurrence pattern that does not have a defined end date.</span></span>  <br/> <span data-ttu-id="3135b-135">El uso de este elemento excluye el uso de los elementos [EndDateRecurrence](enddaterecurrence.md) y [NumberedRecurrence](numberedrecurrence.md) .</span><span class="sxs-lookup"><span data-stu-id="3135b-135">The use of this element excludes the use of the [EndDateRecurrence](enddaterecurrence.md) and [NumberedRecurrence](numberedrecurrence.md) elements.</span></span>  <br/> |
|[<span data-ttu-id="3135b-136">EndDateRecurrence</span><span class="sxs-lookup"><span data-stu-id="3135b-136">EndDateRecurrence</span></span>](enddaterecurrence.md) <br/> |<span data-ttu-id="3135b-137">Describe la fecha de inicio y la fecha de finalización de un patrón de periodicidad de elemento.</span><span class="sxs-lookup"><span data-stu-id="3135b-137">Describes the start date and the end date of an item recurrence pattern.</span></span>  <br/> <span data-ttu-id="3135b-138">El uso de este elemento excluye el uso de los elementos [NoEndRecurrence](noendrecurrence.md) y [NumberedRecurrence](numberedrecurrence.md) .</span><span class="sxs-lookup"><span data-stu-id="3135b-138">The use of this element excludes the use of the [NoEndRecurrence](noendrecurrence.md) and [NumberedRecurrence](numberedrecurrence.md) elements.</span></span>  <br/> <span data-ttu-id="3135b-139">[EndDateRecurrence](enddaterecurrence.md) no se puede usar junto con un patrón de regeneración.</span><span class="sxs-lookup"><span data-stu-id="3135b-139">[EndDateRecurrence](enddaterecurrence.md) cannot be used together with a regeneration pattern.</span></span>  <br/> |
|[<span data-ttu-id="3135b-140">NumberedRecurrence</span><span class="sxs-lookup"><span data-stu-id="3135b-140">NumberedRecurrence</span></span>](numberedrecurrence.md) <br/> |<span data-ttu-id="3135b-141">Describe la fecha de inicio y el número de repeticiones de un elemento periódico.</span><span class="sxs-lookup"><span data-stu-id="3135b-141">Describes the start date and the number of occurrences of a recurring item.</span></span>  <br/> <span data-ttu-id="3135b-142">El uso de este elemento excluye el uso de los elementos [NoEndRecurrence](noendrecurrence.md) y [EndDateRecurrence](enddaterecurrence.md) .</span><span class="sxs-lookup"><span data-stu-id="3135b-142">The use of this element excludes the use of the [NoEndRecurrence](noendrecurrence.md) and [EndDateRecurrence](enddaterecurrence.md) elements.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="3135b-143">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="3135b-143">Parent elements</span></span>

|<span data-ttu-id="3135b-144">**Element**</span><span class="sxs-lookup"><span data-stu-id="3135b-144">**Element**</span></span>|<span data-ttu-id="3135b-145">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3135b-145">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3135b-146">Tarea</span><span class="sxs-lookup"><span data-stu-id="3135b-146">Task</span></span>](task.md) <br/> |<span data-ttu-id="3135b-147">Representa una tarea en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="3135b-147">Represents a task in the Exchange store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3135b-148">Notas</span><span class="sxs-lookup"><span data-stu-id="3135b-148">Remarks</span></span>

<span data-ttu-id="3135b-149">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="3135b-149">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3135b-150">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="3135b-150">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3135b-151">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3135b-151">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="3135b-152">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="3135b-152">Schema name</span></span>  <br/> |<span data-ttu-id="3135b-153">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="3135b-153">Types schema</span></span>  <br/> |
|<span data-ttu-id="3135b-154">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="3135b-154">Validation file</span></span>  <br/> |<span data-ttu-id="3135b-155">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="3135b-155">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="3135b-156">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="3135b-156">Can be empty</span></span>  <br/> |<span data-ttu-id="3135b-157">False</span><span class="sxs-lookup"><span data-stu-id="3135b-157">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3135b-158">Ver también</span><span class="sxs-lookup"><span data-stu-id="3135b-158">See also</span></span>



- [<span data-ttu-id="3135b-159">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="3135b-159">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

