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
description: El elemento RelativeYearlyRecurrence describe un patrón de periodicidad anual relativo.
ms.openlocfilehash: 2abe09ddfe52c24211ef5d0a392ddecaf15bf7bf
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44456747"
---
# <a name="relativeyearlyrecurrence"></a><span data-ttu-id="d5ad9-103">RelativeYearlyRecurrence</span><span class="sxs-lookup"><span data-stu-id="d5ad9-103">RelativeYearlyRecurrence</span></span>

<span data-ttu-id="d5ad9-104">El elemento **RelativeYearlyRecurrence** describe un patrón de periodicidad anual relativo.</span><span class="sxs-lookup"><span data-stu-id="d5ad9-104">The **RelativeYearlyRecurrence** element describes a relative yearly recurrence pattern.</span></span> 
  
```xml
<RelativeYearlyRecurrence>
   <DaysOfWeek/>
   <DayOfWeekIndex/>
   <Month/>
</RelativeYearlyRecurrence>
```

 <span data-ttu-id="d5ad9-105">**RelativeYearlyRecurrencePatternType**</span><span class="sxs-lookup"><span data-stu-id="d5ad9-105">**RelativeYearlyRecurrencePatternType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d5ad9-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="d5ad9-106">Attributes and elements</span></span>

<span data-ttu-id="d5ad9-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="d5ad9-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d5ad9-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="d5ad9-108">Attributes</span></span>

<span data-ttu-id="d5ad9-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="d5ad9-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d5ad9-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="d5ad9-110">Child elements</span></span>

|<span data-ttu-id="d5ad9-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="d5ad9-111">**Element**</span></span>|<span data-ttu-id="d5ad9-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d5ad9-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d5ad9-113">DaysOfWeek (DayOfWeekType)</span><span class="sxs-lookup"><span data-stu-id="d5ad9-113">DaysOfWeek (DayOfWeekType)</span></span>](daysofweek-dayofweektype.md) <br/> |<span data-ttu-id="d5ad9-114">Describe los días de la semana que se usan en los patrones de periodicidad de los elementos.</span><span class="sxs-lookup"><span data-stu-id="d5ad9-114">Describes the days of the week that are used in item recurrence patterns.</span></span>  <br/> |
|[<span data-ttu-id="d5ad9-115">DayOfWeekIndex</span><span class="sxs-lookup"><span data-stu-id="d5ad9-115">DayOfWeekIndex</span></span>](dayofweekindex.md) <br/> |<span data-ttu-id="d5ad9-116">Describe qué semana de un mes se usa en un patrón de periodicidad anual relativo.</span><span class="sxs-lookup"><span data-stu-id="d5ad9-116">Describes which week in a month is used in a relative yearly recurrence pattern.</span></span>  <br/> |
|[<span data-ttu-id="d5ad9-117">Month (periodicidad de elementos)</span><span class="sxs-lookup"><span data-stu-id="d5ad9-117">Month (Item Recurrence)</span></span>](month-item-recurrence.md) <br/> |<span data-ttu-id="d5ad9-118">Describe el mes en que se produce un elemento periódico anual.</span><span class="sxs-lookup"><span data-stu-id="d5ad9-118">Describes the month when a yearly recurring item occurs.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d5ad9-119">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="d5ad9-119">Parent elements</span></span>

|<span data-ttu-id="d5ad9-120">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="d5ad9-120">**Element**</span></span>|<span data-ttu-id="d5ad9-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d5ad9-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d5ad9-122">Periodicidad (TaskRecurrenceType)</span><span class="sxs-lookup"><span data-stu-id="d5ad9-122">Recurrence (TaskRecurrenceType)</span></span>](recurrence-taskrecurrencetype.md) <br/> |<span data-ttu-id="d5ad9-123">Contiene información de periodicidad para tareas periódicas.</span><span class="sxs-lookup"><span data-stu-id="d5ad9-123">Contains recurrence information for recurring tasks.</span></span>  <br/> |
|[<span data-ttu-id="d5ad9-124">Recurrence (RecurrenceType)</span><span class="sxs-lookup"><span data-stu-id="d5ad9-124">Recurrence (RecurrenceType)</span></span>](recurrence-recurrencetype.md) <br/> |<span data-ttu-id="d5ad9-125">Contiene el patrón de periodicidad para los elementos de calendario y las convocatorias de reunión.</span><span class="sxs-lookup"><span data-stu-id="d5ad9-125">Contains the recurrence pattern for calendar items and meeting requests.</span></span>  <br/> |
|[<span data-ttu-id="d5ad9-126">Estándar</span><span class="sxs-lookup"><span data-stu-id="d5ad9-126">Standard</span></span>](standard.md) <br/> |<span data-ttu-id="d5ad9-127">Representa la fecha y la hora en que cambia el horario de verano a la hora estándar.</span><span class="sxs-lookup"><span data-stu-id="d5ad9-127">Represents the date and time when the time changes from daylight saving time to standard time.</span></span>  <br/> |
|[<span data-ttu-id="d5ad9-128">Horario</span><span class="sxs-lookup"><span data-stu-id="d5ad9-128">Daylight</span></span>](daylight.md) <br/> |<span data-ttu-id="d5ad9-129">Representa la fecha y hora en que la hora cambia de la hora estándar al horario de verano.</span><span class="sxs-lookup"><span data-stu-id="d5ad9-129">Represents the date and time when the time changes from standard time to daylight saving time.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d5ad9-130">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d5ad9-130">Remarks</span></span>

<span data-ttu-id="d5ad9-131">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="d5ad9-131">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d5ad9-132">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="d5ad9-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d5ad9-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="d5ad9-133">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d5ad9-134">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="d5ad9-134">Schema Name</span></span>  <br/> |<span data-ttu-id="d5ad9-135">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="d5ad9-135">Types schema</span></span>  <br/> |
|<span data-ttu-id="d5ad9-136">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="d5ad9-136">Validation File</span></span>  <br/> |<span data-ttu-id="d5ad9-137">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="d5ad9-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d5ad9-138">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="d5ad9-138">Can be Empty</span></span>  <br/> |<span data-ttu-id="d5ad9-139">Falso</span><span class="sxs-lookup"><span data-stu-id="d5ad9-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d5ad9-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="d5ad9-140">See also</span></span>



- [<span data-ttu-id="d5ad9-141">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="d5ad9-141">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

