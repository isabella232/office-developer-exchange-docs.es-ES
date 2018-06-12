---
title: RelativeMonthlyRecurrence
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RelativeMonthlyRecurrence
api_type:
- schema
ms.assetid: a76595db-7460-44ac-ac2a-53241caa33a7
description: El elemento RelativeMonthlyRecurrence describe un patrón de periodicidad mensual relativa.
ms.openlocfilehash: 9b695052c38e2693946837bf99f03baea093df08
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19837053"
---
# <a name="relativemonthlyrecurrence"></a><span data-ttu-id="028a1-103">RelativeMonthlyRecurrence</span><span class="sxs-lookup"><span data-stu-id="028a1-103">RelativeMonthlyRecurrence</span></span>

<span data-ttu-id="028a1-104">El elemento **RelativeMonthlyRecurrence** describe un patrón de periodicidad mensual relativa.</span><span class="sxs-lookup"><span data-stu-id="028a1-104">The **RelativeMonthlyRecurrence** element describes a relative monthly recurrence pattern.</span></span> 
  
```xml
<RelativeMonthlyRecurrence>
   <Interval/>
   <DaysOfWeek/>
   <DayOfWeekIndex/>
</RelativeMonthlyRecurrence>
```

 <span data-ttu-id="028a1-105">**RelativeMonthlyRecurrencePatternType**</span><span class="sxs-lookup"><span data-stu-id="028a1-105">**RelativeMonthlyRecurrencePatternType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="028a1-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="028a1-106">Attributes and elements</span></span>

<span data-ttu-id="028a1-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="028a1-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="028a1-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="028a1-108">Attributes</span></span>

<span data-ttu-id="028a1-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="028a1-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="028a1-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="028a1-110">Child elements</span></span>

|<span data-ttu-id="028a1-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="028a1-111">**Element**</span></span>|<span data-ttu-id="028a1-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="028a1-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="028a1-113">Interval</span><span class="sxs-lookup"><span data-stu-id="028a1-113">Interval</span></span>](interval.md) <br/> |<span data-ttu-id="028a1-114">Define el intervalo entre dos elementos modelo periódica mensual consecutivos.</span><span class="sxs-lookup"><span data-stu-id="028a1-114">Defines the interval between two consecutive monthly recurring pattern items.</span></span> <span data-ttu-id="028a1-115">El intervalo para este valor es de 1 a 99.</span><span class="sxs-lookup"><span data-stu-id="028a1-115">The range for this value is 1 to 99.</span></span>  <br/> |
|[<span data-ttu-id="028a1-116">DaysOfWeek (DayOfWeekType)</span><span class="sxs-lookup"><span data-stu-id="028a1-116">DaysOfWeek (DayOfWeekType)</span></span>](daysofweek-dayofweektype.md) <br/> |<span data-ttu-id="028a1-117">Se describen los días de la semana en el patrón de periodicidad mensual relativa.</span><span class="sxs-lookup"><span data-stu-id="028a1-117">Describes which days of the week are in the relative monthly recurrence pattern.</span></span>  <br/> |
|[<span data-ttu-id="028a1-118">DayOfWeekIndex</span><span class="sxs-lookup"><span data-stu-id="028a1-118">DayOfWeekIndex</span></span>](dayofweekindex.md) <br/> |<span data-ttu-id="028a1-119">Describe qué semana se usa en un patrón de periodicidad mensual relativa.</span><span class="sxs-lookup"><span data-stu-id="028a1-119">Describes which week is used in a relative monthly recurrence pattern.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="028a1-120">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="028a1-120">Parent elements</span></span>

|<span data-ttu-id="028a1-121">**Element**</span><span class="sxs-lookup"><span data-stu-id="028a1-121">**Element**</span></span>|<span data-ttu-id="028a1-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="028a1-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="028a1-123">Periodicidad (RecurrenceType)</span><span class="sxs-lookup"><span data-stu-id="028a1-123">Recurrence (RecurrenceType)</span></span>](recurrence-recurrencetype.md) <br/> |<span data-ttu-id="028a1-124">Contiene el patrón de periodicidad para los elementos de calendario y las convocatorias de reunión.</span><span class="sxs-lookup"><span data-stu-id="028a1-124">Contains the recurrence pattern for calendar items and meeting requests.</span></span>  <br/> |
|[<span data-ttu-id="028a1-125">Periodicidad (TaskRecurrenceType)</span><span class="sxs-lookup"><span data-stu-id="028a1-125">Recurrence (TaskRecurrenceType)</span></span>](recurrence-taskrecurrencetype.md) <br/> |<span data-ttu-id="028a1-126">Contiene información sobre la periodicidad para las tareas repetitivas.</span><span class="sxs-lookup"><span data-stu-id="028a1-126">Contains recurrence information for recurring tasks.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="028a1-127">Notas</span><span class="sxs-lookup"><span data-stu-id="028a1-127">Remarks</span></span>

<span data-ttu-id="028a1-128">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="028a1-128">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="028a1-129">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="028a1-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="028a1-130">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="028a1-130">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="028a1-131">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="028a1-131">Schema Name</span></span>  <br/> |<span data-ttu-id="028a1-132">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="028a1-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="028a1-133">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="028a1-133">Validation File</span></span>  <br/> |<span data-ttu-id="028a1-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="028a1-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="028a1-135">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="028a1-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="028a1-136">False</span><span class="sxs-lookup"><span data-stu-id="028a1-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="028a1-137">Ver también</span><span class="sxs-lookup"><span data-stu-id="028a1-137">See also</span></span>



- [<span data-ttu-id="028a1-138">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="028a1-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

