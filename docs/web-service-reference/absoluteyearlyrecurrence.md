---
title: AbsoluteYearlyRecurrence
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AbsoluteYearlyRecurrence
api_type:
- schema
ms.assetid: 96f53e2c-3893-4f6e-a78a-ac179f45c5db
description: El elemento AbsoluteYearlyRecurrence representa un patrón de periodicidad anual.
ms.openlocfilehash: 205da336a6a6ca4fd39120e83ab264e1543354e8
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764526"
---
# <a name="absoluteyearlyrecurrence"></a><span data-ttu-id="a9225-103">AbsoluteYearlyRecurrence</span><span class="sxs-lookup"><span data-stu-id="a9225-103">AbsoluteYearlyRecurrence</span></span>

<span data-ttu-id="a9225-104">El elemento **AbsoluteYearlyRecurrence** representa un patrón de periodicidad anual.</span><span class="sxs-lookup"><span data-stu-id="a9225-104">The **AbsoluteYearlyRecurrence** element represents a yearly recurrence pattern.</span></span> 
  
```xml
<AbsoluteYearlyRecurrence>
   <DayOfMonth/>
   <Month/>
</AbsoluteYearlyRecurrence>
```

 <span data-ttu-id="a9225-105">**AbsoluteYearlyRecurrencePatternType**</span><span class="sxs-lookup"><span data-stu-id="a9225-105">**AbsoluteYearlyRecurrencePatternType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a9225-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="a9225-106">Attributes and elements</span></span>

<span data-ttu-id="a9225-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="a9225-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a9225-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="a9225-108">Attributes</span></span>

<span data-ttu-id="a9225-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="a9225-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a9225-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="a9225-110">Child elements</span></span>

|<span data-ttu-id="a9225-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="a9225-111">**Element**</span></span>|<span data-ttu-id="a9225-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a9225-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a9225-113">DayOfMonth</span><span class="sxs-lookup"><span data-stu-id="a9225-113">DayOfMonth</span></span>](dayofmonth.md) <br/> |<span data-ttu-id="a9225-114">Describe el día en un mes en el que se produce un elemento periódico.</span><span class="sxs-lookup"><span data-stu-id="a9225-114">Describes the day in a month on which a recurring item occurs.</span></span> <span data-ttu-id="a9225-115">El intervalo de valores de esta propiedad es 1 y 31.</span><span class="sxs-lookup"><span data-stu-id="a9225-115">The range of values for this property is 1 to 31.</span></span> <span data-ttu-id="a9225-116">Si para un mes determinado que este valor es mayor que el número de días del mes, se supone que el último día del mes para esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="a9225-116">If for a particular month this value is larger than the number of days in the month, the last day of the month is assumed for this property.</span></span>  <br/> |
|[<span data-ttu-id="a9225-117">Mes (elemento periodicidad)</span><span class="sxs-lookup"><span data-stu-id="a9225-117">Month (Item Recurrence)</span></span>](month-item-recurrence.md) <br/> |<span data-ttu-id="a9225-118">Describe el mes en el que se produce un elemento periódico anual.</span><span class="sxs-lookup"><span data-stu-id="a9225-118">Describes the month in which a yearly recurring item occurs.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="a9225-119">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="a9225-119">Parent elements</span></span>

|<span data-ttu-id="a9225-120">**Element**</span><span class="sxs-lookup"><span data-stu-id="a9225-120">**Element**</span></span>|<span data-ttu-id="a9225-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a9225-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a9225-122">Periodicidad (TaskRecurrenceType)</span><span class="sxs-lookup"><span data-stu-id="a9225-122">Recurrence (TaskRecurrenceType)</span></span>](recurrence-taskrecurrencetype.md) <br/> |<span data-ttu-id="a9225-123">Contiene información sobre la periodicidad para las tareas repetitivas.</span><span class="sxs-lookup"><span data-stu-id="a9225-123">Contains recurrence information for recurring tasks.</span></span>  <br/> |
|[<span data-ttu-id="a9225-124">Periodicidad (RecurrenceType)</span><span class="sxs-lookup"><span data-stu-id="a9225-124">Recurrence (RecurrenceType)</span></span>](recurrence-recurrencetype.md) <br/> |<span data-ttu-id="a9225-125">Contiene el patrón de periodicidad para los elementos de calendario y las convocatorias de reunión.</span><span class="sxs-lookup"><span data-stu-id="a9225-125">Contains the recurrence pattern for calendar items and meeting requests.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a9225-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a9225-126">Remarks</span></span>

<span data-ttu-id="a9225-127">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="a9225-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a9225-128">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="a9225-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a9225-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a9225-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a9225-130">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="a9225-130">Schema Name</span></span>  <br/> |<span data-ttu-id="a9225-131">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="a9225-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="a9225-132">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="a9225-132">Validation File</span></span>  <br/> |<span data-ttu-id="a9225-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="a9225-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="a9225-134">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="a9225-134">Can Be Empty</span></span>  <br/> |<span data-ttu-id="a9225-135">False</span><span class="sxs-lookup"><span data-stu-id="a9225-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a9225-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="a9225-136">See also</span></span>

- [<span data-ttu-id="a9225-137">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="a9225-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

