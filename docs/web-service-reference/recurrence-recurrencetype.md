---
title: Recurrence (RecurrenceType)
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
ms.assetid: 3d1c2c1c-4103-47ce-ad3c-ad16ec6e9b12
description: El elemento de periodicidad contiene el patrón de periodicidad para los elementos de calendario y las convocatorias de reunión.
ms.openlocfilehash: d9c6009e11eb5b66cdd749b8e085935060f99ab7
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/28/2018
ms.locfileid: "21353353"
---
# <a name="recurrence-recurrencetype"></a><span data-ttu-id="ddb11-103">Recurrence (RecurrenceType)</span><span class="sxs-lookup"><span data-stu-id="ddb11-103">Recurrence (RecurrenceType)</span></span>

<span data-ttu-id="ddb11-104">El elemento de **Periodicidad** contiene el patrón de periodicidad para los elementos de calendario y las convocatorias de reunión.</span><span class="sxs-lookup"><span data-stu-id="ddb11-104">The **Recurrence** element contains the recurrence pattern for calendar items and meeting requests.</span></span> 
  
```xml
<Recurrence>
      <RelativeYearlyRecurrence/>
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
      <RelativeMonthlyRecurrence/> 
      <NumberedRecurrence/>
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
      <RelativeYearlyRecurrence/> 
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
      <DailyRecurrence/> 
      <NoEndRecurrence/>
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
      <DailyRecurrence/> 
      <EndDateRecurrence/>
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
      <DailyRecurrence/> 
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
      <AbsoluteMonthlyRecurrence/> 
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
      <WeeklyRecurrence/> 
      <NoEndRecurrence/> 
</Recurrence>
```

```xml
<Recurrence>
      <WeeklyRecurrence/> 
      <NumberedRecurrence/> 
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
      <RelativeMonthlyRecurrence/> 
      <EndDateRecurrence/>
</Recurrence>
```

<span data-ttu-id="ddb11-105">**RecurrenceType**</span><span class="sxs-lookup"><span data-stu-id="ddb11-105">**RecurrenceType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="ddb11-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="ddb11-106">Attributes and elements</span></span>

<span data-ttu-id="ddb11-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="ddb11-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ddb11-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="ddb11-108">Attributes</span></span>

<span data-ttu-id="ddb11-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="ddb11-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ddb11-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ddb11-110">Child elements</span></span>

|<span data-ttu-id="ddb11-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="ddb11-111">**Element**</span></span>|<span data-ttu-id="ddb11-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ddb11-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ddb11-113">RelativeYearlyRecurrence</span><span class="sxs-lookup"><span data-stu-id="ddb11-113">RelativeYearlyRecurrence</span></span>](relativeyearlyrecurrence.md) <br/> |<span data-ttu-id="ddb11-114">Describe un patrón de periodicidad anual relativa.</span><span class="sxs-lookup"><span data-stu-id="ddb11-114">Describes a relative yearly recurrence pattern.</span></span>  <br/> |
|[<span data-ttu-id="ddb11-115">AbsoluteYearlyRecurrence</span><span class="sxs-lookup"><span data-stu-id="ddb11-115">AbsoluteYearlyRecurrence</span></span>](absoluteyearlyrecurrence.md) <br/> |<span data-ttu-id="ddb11-116">Representa un patrón de periodicidad anual.</span><span class="sxs-lookup"><span data-stu-id="ddb11-116">Represents a yearly recurrence pattern.</span></span>  <br/> |
|[<span data-ttu-id="ddb11-117">RelativeMonthlyRecurrence</span><span class="sxs-lookup"><span data-stu-id="ddb11-117">RelativeMonthlyRecurrence</span></span>](relativemonthlyrecurrence.md) <br/> |<span data-ttu-id="ddb11-118">Describe un patrón de periodicidad mensual relativa para un elemento periódico del calendario.</span><span class="sxs-lookup"><span data-stu-id="ddb11-118">Describes a relative monthly recurrence pattern for a recurring calendar item.</span></span>  <br/> |
|[<span data-ttu-id="ddb11-119">AbsoluteMonthlyRecurrence</span><span class="sxs-lookup"><span data-stu-id="ddb11-119">AbsoluteMonthlyRecurrence</span></span>](absolutemonthlyrecurrence.md) <br/> |<span data-ttu-id="ddb11-120">Representa un patrón de periodicidad mensual.</span><span class="sxs-lookup"><span data-stu-id="ddb11-120">Represents a monthly recurrence pattern.</span></span>  <br/> |
|[<span data-ttu-id="ddb11-121">WeeklyRecurrence</span><span class="sxs-lookup"><span data-stu-id="ddb11-121">WeeklyRecurrence</span></span>](weeklyrecurrence.md) <br/> |<span data-ttu-id="ddb11-122">Describe la frecuencia, en semanas y los días que se repite un elemento de calendario o tarea.</span><span class="sxs-lookup"><span data-stu-id="ddb11-122">Describes the frequency, in weeks, and the days that a calendar item or task recurs.</span></span>  <br/> |
|[<span data-ttu-id="ddb11-123">DailyRecurrence</span><span class="sxs-lookup"><span data-stu-id="ddb11-123">DailyRecurrence</span></span>](dailyrecurrence.md) <br/> |<span data-ttu-id="ddb11-124">Describe la frecuencia, en días, en que se repite un elemento de calendario o tarea.</span><span class="sxs-lookup"><span data-stu-id="ddb11-124">Describes the frequency, in days, in which a calendar item or task recurs.</span></span>  <br/> |
|[<span data-ttu-id="ddb11-125">NoEndRecurrence</span><span class="sxs-lookup"><span data-stu-id="ddb11-125">NoEndRecurrence</span></span>](noendrecurrence.md) <br/> |<span data-ttu-id="ddb11-126">Describe un patrón de periodicidad que no tiene una fecha de finalización definidas.</span><span class="sxs-lookup"><span data-stu-id="ddb11-126">Describes a recurrence pattern that does not have a defined end date.</span></span>  <br/> <span data-ttu-id="ddb11-127">El uso de este elemento excluye el uso de los elementos [EndDateRecurrence](enddaterecurrence.md) y [NumberedRecurrence](numberedrecurrence.md) .</span><span class="sxs-lookup"><span data-stu-id="ddb11-127">The use of this element excludes the use of the [EndDateRecurrence](enddaterecurrence.md) and [NumberedRecurrence](numberedrecurrence.md) elements.</span></span>  <br/> |
|[<span data-ttu-id="ddb11-128">EndDateRecurrence</span><span class="sxs-lookup"><span data-stu-id="ddb11-128">EndDateRecurrence</span></span>](enddaterecurrence.md) <br/> |<span data-ttu-id="ddb11-129">Describe la fecha de inicio y la fecha de finalización de un patrón de periodicidad de elemento.</span><span class="sxs-lookup"><span data-stu-id="ddb11-129">Describes the start date and the end date of an item recurrence pattern.</span></span>  <br/> <span data-ttu-id="ddb11-130">El uso de este elemento excluye el uso de los elementos [NoEndRecurrence](noendrecurrence.md) y [NumberedRecurrence](numberedrecurrence.md) .</span><span class="sxs-lookup"><span data-stu-id="ddb11-130">The use of this element excludes the use of the [NoEndRecurrence](noendrecurrence.md) and [NumberedRecurrence](numberedrecurrence.md) elements.</span></span>  <br/> |
|[<span data-ttu-id="ddb11-131">NumberedRecurrence</span><span class="sxs-lookup"><span data-stu-id="ddb11-131">NumberedRecurrence</span></span>](numberedrecurrence.md) <br/> |<span data-ttu-id="ddb11-132">Describe la fecha de inicio y el número de repeticiones de un elemento periódico.</span><span class="sxs-lookup"><span data-stu-id="ddb11-132">Describes the start date and the number of occurrences of a recurring item.</span></span>  <br/> <span data-ttu-id="ddb11-133">El uso de este elemento excluye el uso de los elementos [NoEndRecurrence](noendrecurrence.md) y [EndDateRecurrence](enddaterecurrence.md) .</span><span class="sxs-lookup"><span data-stu-id="ddb11-133">The use of this element excludes the use of the [NoEndRecurrence](noendrecurrence.md) and [EndDateRecurrence](enddaterecurrence.md) elements.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ddb11-134">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="ddb11-134">Parent elements</span></span>

|<span data-ttu-id="ddb11-135">**Element**</span><span class="sxs-lookup"><span data-stu-id="ddb11-135">**Element**</span></span>|<span data-ttu-id="ddb11-136">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ddb11-136">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ddb11-137">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="ddb11-137">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="ddb11-138">Representa un elemento de calendario de Exchange.</span><span class="sxs-lookup"><span data-stu-id="ddb11-138">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="ddb11-139">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="ddb11-139">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="ddb11-140">Representa una convocatoria de reunión en el almacén de Exchange</span><span class="sxs-lookup"><span data-stu-id="ddb11-140">Represents a meeting request in the Exchange store</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ddb11-141">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ddb11-141">Remarks</span></span>

<span data-ttu-id="ddb11-142">Este elemento es válida si [CalendarItemType](calendaritemtype.md) tiene el valor RecurringMaster.</span><span class="sxs-lookup"><span data-stu-id="ddb11-142">This element is valid if [CalendarItemType](calendaritemtype.md) has the RecurringMaster value.</span></span> 
  
<span data-ttu-id="ddb11-143">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="ddb11-143">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ddb11-144">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="ddb11-144">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ddb11-145">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="ddb11-145">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ddb11-146">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="ddb11-146">Schema name</span></span>  <br/> |<span data-ttu-id="ddb11-147">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="ddb11-147">Types schema</span></span>  <br/> |
|<span data-ttu-id="ddb11-148">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="ddb11-148">Validation file</span></span>  <br/> |<span data-ttu-id="ddb11-149">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="ddb11-149">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="ddb11-150">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="ddb11-150">Can be empty</span></span>  <br/> |<span data-ttu-id="ddb11-151">False</span><span class="sxs-lookup"><span data-stu-id="ddb11-151">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ddb11-152">Vea también</span><span class="sxs-lookup"><span data-stu-id="ddb11-152">See also</span></span>

- [<span data-ttu-id="ddb11-153">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="ddb11-153">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

