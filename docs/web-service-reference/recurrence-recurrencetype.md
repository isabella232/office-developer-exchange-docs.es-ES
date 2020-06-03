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
description: El elemento recurrence contiene el patrón de periodicidad de los elementos de calendario y las convocatorias de reunión.
ms.openlocfilehash: d00445c75fb35c3bb99eeed06e30cb1cf2883597
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529892"
---
# <a name="recurrence-recurrencetype"></a><span data-ttu-id="de050-103">Recurrence (RecurrenceType)</span><span class="sxs-lookup"><span data-stu-id="de050-103">Recurrence (RecurrenceType)</span></span>

<span data-ttu-id="de050-104">El elemento **recurrence** contiene el patrón de periodicidad de los elementos de calendario y las convocatorias de reunión.</span><span class="sxs-lookup"><span data-stu-id="de050-104">The **Recurrence** element contains the recurrence pattern for calendar items and meeting requests.</span></span> 
  
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

<span data-ttu-id="de050-105">**RecurrenceType**</span><span class="sxs-lookup"><span data-stu-id="de050-105">**RecurrenceType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="de050-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="de050-106">Attributes and elements</span></span>

<span data-ttu-id="de050-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="de050-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="de050-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="de050-108">Attributes</span></span>

<span data-ttu-id="de050-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="de050-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="de050-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="de050-110">Child elements</span></span>

|<span data-ttu-id="de050-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="de050-111">**Element**</span></span>|<span data-ttu-id="de050-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="de050-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="de050-113">RelativeYearlyRecurrence</span><span class="sxs-lookup"><span data-stu-id="de050-113">RelativeYearlyRecurrence</span></span>](relativeyearlyrecurrence.md) <br/> |<span data-ttu-id="de050-114">Describe un patrón de periodicidad anual relativo.</span><span class="sxs-lookup"><span data-stu-id="de050-114">Describes a relative yearly recurrence pattern.</span></span>  <br/> |
|[<span data-ttu-id="de050-115">AbsoluteYearlyRecurrence</span><span class="sxs-lookup"><span data-stu-id="de050-115">AbsoluteYearlyRecurrence</span></span>](absoluteyearlyrecurrence.md) <br/> |<span data-ttu-id="de050-116">Representa un patrón de periodicidad anual.</span><span class="sxs-lookup"><span data-stu-id="de050-116">Represents a yearly recurrence pattern.</span></span>  <br/> |
|[<span data-ttu-id="de050-117">RelativeMonthlyRecurrence</span><span class="sxs-lookup"><span data-stu-id="de050-117">RelativeMonthlyRecurrence</span></span>](relativemonthlyrecurrence.md) <br/> |<span data-ttu-id="de050-118">Describe un patrón de periodicidad mensual relativo para un elemento de calendario periódico.</span><span class="sxs-lookup"><span data-stu-id="de050-118">Describes a relative monthly recurrence pattern for a recurring calendar item.</span></span>  <br/> |
|[<span data-ttu-id="de050-119">AbsoluteMonthlyRecurrence</span><span class="sxs-lookup"><span data-stu-id="de050-119">AbsoluteMonthlyRecurrence</span></span>](absolutemonthlyrecurrence.md) <br/> |<span data-ttu-id="de050-120">Representa un patrón de periodicidad mensual.</span><span class="sxs-lookup"><span data-stu-id="de050-120">Represents a monthly recurrence pattern.</span></span>  <br/> |
|[<span data-ttu-id="de050-121">WeeklyRecurrence</span><span class="sxs-lookup"><span data-stu-id="de050-121">WeeklyRecurrence</span></span>](weeklyrecurrence.md) <br/> |<span data-ttu-id="de050-122">Describe la frecuencia, en semanas, y los días que se repite un elemento de calendario o una tarea.</span><span class="sxs-lookup"><span data-stu-id="de050-122">Describes the frequency, in weeks, and the days that a calendar item or task recurs.</span></span>  <br/> |
|[<span data-ttu-id="de050-123">DailyRecurrence</span><span class="sxs-lookup"><span data-stu-id="de050-123">DailyRecurrence</span></span>](dailyrecurrence.md) <br/> |<span data-ttu-id="de050-124">Describe la frecuencia, en días, en la que se repite un elemento de calendario o una tarea.</span><span class="sxs-lookup"><span data-stu-id="de050-124">Describes the frequency, in days, in which a calendar item or task recurs.</span></span>  <br/> |
|[<span data-ttu-id="de050-125">NoEndRecurrence</span><span class="sxs-lookup"><span data-stu-id="de050-125">NoEndRecurrence</span></span>](noendrecurrence.md) <br/> |<span data-ttu-id="de050-126">Describe un patrón de periodicidad que no tiene una fecha de finalización definida.</span><span class="sxs-lookup"><span data-stu-id="de050-126">Describes a recurrence pattern that does not have a defined end date.</span></span>  <br/> <span data-ttu-id="de050-127">El uso de este elemento excluye el uso de los elementos [EndDateRecurrence](enddaterecurrence.md) y [NumberedRecurrence](numberedrecurrence.md) .</span><span class="sxs-lookup"><span data-stu-id="de050-127">The use of this element excludes the use of the [EndDateRecurrence](enddaterecurrence.md) and [NumberedRecurrence](numberedrecurrence.md) elements.</span></span>  <br/> |
|[<span data-ttu-id="de050-128">EndDateRecurrence</span><span class="sxs-lookup"><span data-stu-id="de050-128">EndDateRecurrence</span></span>](enddaterecurrence.md) <br/> |<span data-ttu-id="de050-129">Describe la fecha de inicio y la fecha de finalización de un patrón de periodicidad de un elemento.</span><span class="sxs-lookup"><span data-stu-id="de050-129">Describes the start date and the end date of an item recurrence pattern.</span></span>  <br/> <span data-ttu-id="de050-130">El uso de este elemento excluye el uso de los elementos [NoEndRecurrence](noendrecurrence.md) y [NumberedRecurrence](numberedrecurrence.md) .</span><span class="sxs-lookup"><span data-stu-id="de050-130">The use of this element excludes the use of the [NoEndRecurrence](noendrecurrence.md) and [NumberedRecurrence](numberedrecurrence.md) elements.</span></span>  <br/> |
|[<span data-ttu-id="de050-131">NumberedRecurrence</span><span class="sxs-lookup"><span data-stu-id="de050-131">NumberedRecurrence</span></span>](numberedrecurrence.md) <br/> |<span data-ttu-id="de050-132">Describe la fecha de inicio y el número de repeticiones de un elemento periódico.</span><span class="sxs-lookup"><span data-stu-id="de050-132">Describes the start date and the number of occurrences of a recurring item.</span></span>  <br/> <span data-ttu-id="de050-133">El uso de este elemento excluye el uso de los elementos [NoEndRecurrence](noendrecurrence.md) y [EndDateRecurrence](enddaterecurrence.md) .</span><span class="sxs-lookup"><span data-stu-id="de050-133">The use of this element excludes the use of the [NoEndRecurrence](noendrecurrence.md) and [EndDateRecurrence](enddaterecurrence.md) elements.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="de050-134">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="de050-134">Parent elements</span></span>

|<span data-ttu-id="de050-135">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="de050-135">**Element**</span></span>|<span data-ttu-id="de050-136">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="de050-136">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="de050-137">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="de050-137">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="de050-138">Representa un elemento de calendario de Exchange.</span><span class="sxs-lookup"><span data-stu-id="de050-138">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="de050-139">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="de050-139">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="de050-140">Representa una convocatoria de reunión en el almacén de Exchange</span><span class="sxs-lookup"><span data-stu-id="de050-140">Represents a meeting request in the Exchange store</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="de050-141">Comentarios</span><span class="sxs-lookup"><span data-stu-id="de050-141">Remarks</span></span>

<span data-ttu-id="de050-142">Este elemento es válido si [CalendarItemType](calendaritemtype.md) tiene el valor RecurringMaster.</span><span class="sxs-lookup"><span data-stu-id="de050-142">This element is valid if [CalendarItemType](calendaritemtype.md) has the RecurringMaster value.</span></span> 
  
<span data-ttu-id="de050-143">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="de050-143">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="de050-144">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="de050-144">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="de050-145">Namespace</span><span class="sxs-lookup"><span data-stu-id="de050-145">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="de050-146">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="de050-146">Schema name</span></span>  <br/> |<span data-ttu-id="de050-147">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="de050-147">Types schema</span></span>  <br/> |
|<span data-ttu-id="de050-148">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="de050-148">Validation file</span></span>  <br/> |<span data-ttu-id="de050-149">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="de050-149">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="de050-150">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="de050-150">Can be empty</span></span>  <br/> |<span data-ttu-id="de050-151">Falso</span><span class="sxs-lookup"><span data-stu-id="de050-151">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="de050-152">Vea también</span><span class="sxs-lookup"><span data-stu-id="de050-152">See also</span></span>

- [<span data-ttu-id="de050-153">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="de050-153">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

