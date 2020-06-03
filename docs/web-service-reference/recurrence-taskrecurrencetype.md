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
description: El elemento recurrence contiene información de periodicidad para tareas periódicas.
ms.openlocfilehash: 933fd6b003d8d193e1561f2a22b65ac00237c345
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44528835"
---
# <a name="recurrence-taskrecurrencetype"></a><span data-ttu-id="f574b-103">Periodicidad (TaskRecurrenceType)</span><span class="sxs-lookup"><span data-stu-id="f574b-103">Recurrence (TaskRecurrenceType)</span></span>

<span data-ttu-id="f574b-104">El elemento **recurrence** contiene información de periodicidad para tareas periódicas.</span><span class="sxs-lookup"><span data-stu-id="f574b-104">The **Recurrence** element contains recurrence information for recurring tasks.</span></span> 
  
```xml
<Recurrence>
      <RelativeYearlyRecurrence/>
      <NoEndRecurrence/>
</Recurrence>
```

```xml
<Recurrence>
      <WeeklyRecurrence/> 
      <NoEndRecurrence/> 
</Recurrence>
```

```xml
<Recurrence>
      <RelativeMonthlyRecurrence/> 
      <NumberedRecurrence/>
</Recurrence>
```

```xml
<Recurrence>
      <AbsoluteMonthlyRecurrence/> 
      <EndDateRecurrence/>
</Recurrence>
```

```xml
<Recurrence>
      <MonthlyRegeneration/> 
      <NumberedRecurrence/>
</Recurrence>
```

```xml
<Recurrence>
      <DailyRegeneration/> 
      <EndDateRecurrence/> 
</Recurrence>
```

```xml
<Recurrence>
       <DailyRegeneration/> 
       <NumberedRecurrence/>
</Recurrence>
```

```xml
<Recurrence>
      <DailyRegeneration/> 
      <NoEndRecurrence/>
</Recurrence>
```

```xml
<Recurrence>
       <MonthlyRegeneration/> 
       <NoEndRecurrence/> 
</Recurrence>
```

```xml
<Recurrence>
      <YearlyRegeneration/> 
      <NoEndRecurrence/> 
</Recurrence>
```

```xml
<Recurrence>
      <YearlyRegeneration/> 
      <EndDateRecurrence/>
</Recurrence>
```

```xml
<Recurrence>
      <AbsoluteMonthlyRecurrence/> 
      <NumberedRecurrence/> 
</Recurrence>
```

```xml
<Recurrence>
      <WeeklyRegeneration/> 
      <NumberedRecurrence/>
</Recurrence>
```

```xml
<Recurrence>
      <RelativeMonthlyRecurrence/> 
      <EndDateRecurrence/> 
</Recurrence>
```

```xml
<Recurrence>
      <RelativeYearlyRecurrence/> 
      <NumberedRecurrence/>
</Recurrence>
```

```xml
<Recurrence>
      <WeeklyRegeneration/> 
      <NoEndRecurrence/> 
</Recurrence>
```

```xml
<Recurrence>
      <AbsoluteYearlyRecurrence/> 
      <NumberedRecurrence/> 
</Recurrence>
```

```xml
<Recurrence>
      <RelativeMonthlyRecurrence/> 
      <NoEndRecurrence/>
</Recurrence>
```

```xml
<Recurrence>
      <YearlyRegeneration/> 
      <NumberedRecurrence/>
</Recurrence>
```

```xml
<Recurrence>
      <WeeklyRecurrence/> 
      <EndDateRecurrence/> 
</Recurrence>
```

```xml
<Recurrence>
      <RelativeYearlyRecurrence/> 
      <EndDateRecurrence/>
</Recurrence>
```

```xml
<Recurrence>
       <MonthlyRegeneration/> 
       <EndDateRecurrence/>
</Recurrence>
```

```xml
<Recurrence>
      <AbsoluteYearlyRecurrence/> 
      <NoEndRecurrence/> 
</Recurrence>
```

```xml
<Recurrence>
      <AbsoluteMonthlyRecurrence/> 
      <NoEndRecurrence/> 
</Recurrence>
```

```xml
<Recurrence>
       <DailyRecurrence/> 
       <EndDateRecurrence/>
</Recurrence>
```

```xml
<Recurrence>
      <WeeklyRegeneration/> 
      <EndDateRecurrence/>
</Recurrence>
```

```xml
<Recurrence>
      <AbsoluteYearlyRecurrence/> 
      <EndDateRecurrence/> 
</Recurrence>
```

```xml
<Recurrence>
      <DailyRecurrence/> 
      <NoEndRecurrence/>
</Recurrence>
```

```xml
<Recurrence>
      <DailyRecurrence/> 
      <NumberedRecurrence/>
</Recurrence>
```

```xml
<Recurrence>
      <WeeklyRecurrence/> 
      <NumberedRecurrence/>
</Recurrence>
```


<span data-ttu-id="f574b-105">**TaskRecurrenceType**</span><span class="sxs-lookup"><span data-stu-id="f574b-105">**TaskRecurrenceType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="f574b-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="f574b-106">Attributes and elements</span></span>

<span data-ttu-id="f574b-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="f574b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f574b-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="f574b-108">Attributes</span></span>

<span data-ttu-id="f574b-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="f574b-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f574b-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="f574b-110">Child elements</span></span>

|<span data-ttu-id="f574b-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="f574b-111">**Element**</span></span>|<span data-ttu-id="f574b-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f574b-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f574b-113">RelativeYearlyRecurrence</span><span class="sxs-lookup"><span data-stu-id="f574b-113">RelativeYearlyRecurrence</span></span>](relativeyearlyrecurrence.md) <br/> |<span data-ttu-id="f574b-114">Describe un patrón de periodicidad anual relativo para una tarea repetitiva.</span><span class="sxs-lookup"><span data-stu-id="f574b-114">Describes a relative yearly recurrence pattern for a recurring task.</span></span>  <br/> |
|[<span data-ttu-id="f574b-115">AbsoluteYearlyRecurrence</span><span class="sxs-lookup"><span data-stu-id="f574b-115">AbsoluteYearlyRecurrence</span></span>](absoluteyearlyrecurrence.md) <br/> |<span data-ttu-id="f574b-116">Representa un patrón de periodicidad anual para una tarea repetitiva.</span><span class="sxs-lookup"><span data-stu-id="f574b-116">Represents a yearly recurrence pattern for a recurring task.</span></span>  <br/> |
|[<span data-ttu-id="f574b-117">RelativeMonthlyRecurrence</span><span class="sxs-lookup"><span data-stu-id="f574b-117">RelativeMonthlyRecurrence</span></span>](relativemonthlyrecurrence.md) <br/> |<span data-ttu-id="f574b-118">Describe un patrón de periodicidad mensual relativo para una tarea repetitiva.</span><span class="sxs-lookup"><span data-stu-id="f574b-118">Describes a relative monthly recurrence pattern for a recurring task.</span></span>  <br/> |
|[<span data-ttu-id="f574b-119">AbsoluteMonthlyRecurrence</span><span class="sxs-lookup"><span data-stu-id="f574b-119">AbsoluteMonthlyRecurrence</span></span>](absolutemonthlyrecurrence.md) <br/> |<span data-ttu-id="f574b-120">Representa un patrón de periodicidad mensual para una tarea repetitiva.</span><span class="sxs-lookup"><span data-stu-id="f574b-120">Represents a monthly recurrence pattern for a recurring task.</span></span>  <br/> |
|[<span data-ttu-id="f574b-121">WeeklyRecurrence</span><span class="sxs-lookup"><span data-stu-id="f574b-121">WeeklyRecurrence</span></span>](weeklyrecurrence.md) <br/> |<span data-ttu-id="f574b-122">Describe la frecuencia, en semanas, y los días que una tarea se repite.</span><span class="sxs-lookup"><span data-stu-id="f574b-122">Describes the frequency, in weeks, and the days on which a task recurs.</span></span>  <br/> |
|[<span data-ttu-id="f574b-123">DailyRecurrence</span><span class="sxs-lookup"><span data-stu-id="f574b-123">DailyRecurrence</span></span>](dailyrecurrence.md) <br/> |<span data-ttu-id="f574b-124">Describe la frecuencia, en días, en la que una tarea se repite.</span><span class="sxs-lookup"><span data-stu-id="f574b-124">Describes the frequency, in days, in which a task recurs.</span></span>  <br/> |
|[<span data-ttu-id="f574b-125">DailyRegeneration</span><span class="sxs-lookup"><span data-stu-id="f574b-125">DailyRegeneration</span></span>](dailyregeneration.md) <br/> |<span data-ttu-id="f574b-126">Describe cuántos días tras la finalización de la tarea actual vencerá la próxima vez que se produzca.</span><span class="sxs-lookup"><span data-stu-id="f574b-126">Describes how many days after the completion of the current task the next occurrence will be due.</span></span>  <br/> |
|[<span data-ttu-id="f574b-127">WeeklyRegeneration</span><span class="sxs-lookup"><span data-stu-id="f574b-127">WeeklyRegeneration</span></span>](weeklyregeneration.md) <br/> |<span data-ttu-id="f574b-128">Describe el número de semanas después de la finalización de la tarea actual, la próxima vez que se deba.</span><span class="sxs-lookup"><span data-stu-id="f574b-128">Describes how many weeks after the completion of the current task the next occurrence will be due.</span></span>  <br/> |
|[<span data-ttu-id="f574b-129">MonthlyRegeneration</span><span class="sxs-lookup"><span data-stu-id="f574b-129">MonthlyRegeneration</span></span>](monthlyregeneration.md) <br/> |<span data-ttu-id="f574b-130">Describe cuántos meses después de la finalización de la tarea actual vencerá la próxima vez que se produzca.</span><span class="sxs-lookup"><span data-stu-id="f574b-130">Describes how many months after the completion of the current task the next occurrence will be due.</span></span>  <br/> |
|[<span data-ttu-id="f574b-131">YearlyRegeneration</span><span class="sxs-lookup"><span data-stu-id="f574b-131">YearlyRegeneration</span></span>](yearlyregeneration.md) <br/> |<span data-ttu-id="f574b-132">Describe cuántos años tras la finalización de la tarea actual vencerá la próxima vez que se produzca.</span><span class="sxs-lookup"><span data-stu-id="f574b-132">Describes how many years after the completion of the current task the next occurrence will be due.</span></span>  <br/> |
|[<span data-ttu-id="f574b-133">NoEndRecurrence</span><span class="sxs-lookup"><span data-stu-id="f574b-133">NoEndRecurrence</span></span>](noendrecurrence.md) <br/> |<span data-ttu-id="f574b-134">Describe un patrón de periodicidad que no tiene una fecha de finalización definida.</span><span class="sxs-lookup"><span data-stu-id="f574b-134">Describes a recurrence pattern that does not have a defined end date.</span></span>  <br/> <span data-ttu-id="f574b-135">El uso de este elemento excluye el uso de los elementos [EndDateRecurrence](enddaterecurrence.md) y [NumberedRecurrence](numberedrecurrence.md) .</span><span class="sxs-lookup"><span data-stu-id="f574b-135">The use of this element excludes the use of the [EndDateRecurrence](enddaterecurrence.md) and [NumberedRecurrence](numberedrecurrence.md) elements.</span></span>  <br/> |
|[<span data-ttu-id="f574b-136">EndDateRecurrence</span><span class="sxs-lookup"><span data-stu-id="f574b-136">EndDateRecurrence</span></span>](enddaterecurrence.md) <br/> |<span data-ttu-id="f574b-137">Describe la fecha de inicio y la fecha de finalización de un patrón de periodicidad de un elemento.</span><span class="sxs-lookup"><span data-stu-id="f574b-137">Describes the start date and the end date of an item recurrence pattern.</span></span>  <br/> <span data-ttu-id="f574b-138">El uso de este elemento excluye el uso de los elementos [NoEndRecurrence](noendrecurrence.md) y [NumberedRecurrence](numberedrecurrence.md) .</span><span class="sxs-lookup"><span data-stu-id="f574b-138">The use of this element excludes the use of the [NoEndRecurrence](noendrecurrence.md) and [NumberedRecurrence](numberedrecurrence.md) elements.</span></span>  <br/> <span data-ttu-id="f574b-139">[EndDateRecurrence](enddaterecurrence.md) no se puede usar junto con un patrón de regeneración.</span><span class="sxs-lookup"><span data-stu-id="f574b-139">[EndDateRecurrence](enddaterecurrence.md) cannot be used together with a regeneration pattern.</span></span>  <br/> |
|[<span data-ttu-id="f574b-140">NumberedRecurrence</span><span class="sxs-lookup"><span data-stu-id="f574b-140">NumberedRecurrence</span></span>](numberedrecurrence.md) <br/> |<span data-ttu-id="f574b-141">Describe la fecha de inicio y el número de repeticiones de un elemento periódico.</span><span class="sxs-lookup"><span data-stu-id="f574b-141">Describes the start date and the number of occurrences of a recurring item.</span></span>  <br/> <span data-ttu-id="f574b-142">El uso de este elemento excluye el uso de los elementos [NoEndRecurrence](noendrecurrence.md) y [EndDateRecurrence](enddaterecurrence.md) .</span><span class="sxs-lookup"><span data-stu-id="f574b-142">The use of this element excludes the use of the [NoEndRecurrence](noendrecurrence.md) and [EndDateRecurrence](enddaterecurrence.md) elements.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="f574b-143">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="f574b-143">Parent elements</span></span>

|<span data-ttu-id="f574b-144">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="f574b-144">**Element**</span></span>|<span data-ttu-id="f574b-145">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f574b-145">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f574b-146">Tarea</span><span class="sxs-lookup"><span data-stu-id="f574b-146">Task</span></span>](task.md) <br/> |<span data-ttu-id="f574b-147">Representa una tarea del almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="f574b-147">Represents a task in the Exchange store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f574b-148">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f574b-148">Remarks</span></span>

<span data-ttu-id="f574b-149">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="f574b-149">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f574b-150">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="f574b-150">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f574b-151">Namespace</span><span class="sxs-lookup"><span data-stu-id="f574b-151">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f574b-152">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="f574b-152">Schema name</span></span>  <br/> |<span data-ttu-id="f574b-153">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="f574b-153">Types schema</span></span>  <br/> |
|<span data-ttu-id="f574b-154">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="f574b-154">Validation file</span></span>  <br/> |<span data-ttu-id="f574b-155">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="f574b-155">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="f574b-156">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="f574b-156">Can be empty</span></span>  <br/> |<span data-ttu-id="f574b-157">Falso</span><span class="sxs-lookup"><span data-stu-id="f574b-157">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f574b-158">Vea también</span><span class="sxs-lookup"><span data-stu-id="f574b-158">See also</span></span>

- [<span data-ttu-id="f574b-159">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="f574b-159">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

