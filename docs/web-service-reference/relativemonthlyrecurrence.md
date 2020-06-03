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
description: El elemento RelativeMonthlyRecurrence describe un patrón de periodicidad mensual relativo.
ms.openlocfilehash: 90aa0e43684bfb09a3e13cf86ec96f680e80a714
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457511"
---
# <a name="relativemonthlyrecurrence"></a><span data-ttu-id="b74ee-103">RelativeMonthlyRecurrence</span><span class="sxs-lookup"><span data-stu-id="b74ee-103">RelativeMonthlyRecurrence</span></span>

<span data-ttu-id="b74ee-104">El elemento **RelativeMonthlyRecurrence** describe un patrón de periodicidad mensual relativo.</span><span class="sxs-lookup"><span data-stu-id="b74ee-104">The **RelativeMonthlyRecurrence** element describes a relative monthly recurrence pattern.</span></span> 
  
```xml
<RelativeMonthlyRecurrence>
   <Interval/>
   <DaysOfWeek/>
   <DayOfWeekIndex/>
</RelativeMonthlyRecurrence>
```

 <span data-ttu-id="b74ee-105">**RelativeMonthlyRecurrencePatternType**</span><span class="sxs-lookup"><span data-stu-id="b74ee-105">**RelativeMonthlyRecurrencePatternType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b74ee-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="b74ee-106">Attributes and elements</span></span>

<span data-ttu-id="b74ee-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="b74ee-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b74ee-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="b74ee-108">Attributes</span></span>

<span data-ttu-id="b74ee-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="b74ee-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b74ee-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b74ee-110">Child elements</span></span>

|<span data-ttu-id="b74ee-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="b74ee-111">**Element**</span></span>|<span data-ttu-id="b74ee-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b74ee-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b74ee-113">Intervalo de</span><span class="sxs-lookup"><span data-stu-id="b74ee-113">Interval</span></span>](interval.md) <br/> |<span data-ttu-id="b74ee-114">Define el intervalo entre dos elementos de patrón periódicos mensuales consecutivos.</span><span class="sxs-lookup"><span data-stu-id="b74ee-114">Defines the interval between two consecutive monthly recurring pattern items.</span></span> <span data-ttu-id="b74ee-115">El intervalo para este valor es de 1 a 99.</span><span class="sxs-lookup"><span data-stu-id="b74ee-115">The range for this value is 1 to 99.</span></span>  <br/> |
|[<span data-ttu-id="b74ee-116">DaysOfWeek (DayOfWeekType)</span><span class="sxs-lookup"><span data-stu-id="b74ee-116">DaysOfWeek (DayOfWeekType)</span></span>](daysofweek-dayofweektype.md) <br/> |<span data-ttu-id="b74ee-117">Describe qué días de la semana se encuentran en el patrón de periodicidad mensual relativo.</span><span class="sxs-lookup"><span data-stu-id="b74ee-117">Describes which days of the week are in the relative monthly recurrence pattern.</span></span>  <br/> |
|[<span data-ttu-id="b74ee-118">DayOfWeekIndex</span><span class="sxs-lookup"><span data-stu-id="b74ee-118">DayOfWeekIndex</span></span>](dayofweekindex.md) <br/> |<span data-ttu-id="b74ee-119">Describe la semana que se usa en un patrón de periodicidad mensual relativo.</span><span class="sxs-lookup"><span data-stu-id="b74ee-119">Describes which week is used in a relative monthly recurrence pattern.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="b74ee-120">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="b74ee-120">Parent elements</span></span>

|<span data-ttu-id="b74ee-121">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="b74ee-121">**Element**</span></span>|<span data-ttu-id="b74ee-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b74ee-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b74ee-123">Recurrence (RecurrenceType)</span><span class="sxs-lookup"><span data-stu-id="b74ee-123">Recurrence (RecurrenceType)</span></span>](recurrence-recurrencetype.md) <br/> |<span data-ttu-id="b74ee-124">Contiene el patrón de periodicidad para los elementos de calendario y las convocatorias de reunión.</span><span class="sxs-lookup"><span data-stu-id="b74ee-124">Contains the recurrence pattern for calendar items and meeting requests.</span></span>  <br/> |
|[<span data-ttu-id="b74ee-125">Periodicidad (TaskRecurrenceType)</span><span class="sxs-lookup"><span data-stu-id="b74ee-125">Recurrence (TaskRecurrenceType)</span></span>](recurrence-taskrecurrencetype.md) <br/> |<span data-ttu-id="b74ee-126">Contiene información de periodicidad para tareas periódicas.</span><span class="sxs-lookup"><span data-stu-id="b74ee-126">Contains recurrence information for recurring tasks.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b74ee-127">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b74ee-127">Remarks</span></span>

<span data-ttu-id="b74ee-128">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="b74ee-128">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b74ee-129">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="b74ee-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b74ee-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="b74ee-130">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="b74ee-131">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="b74ee-131">Schema Name</span></span>  <br/> |<span data-ttu-id="b74ee-132">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="b74ee-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="b74ee-133">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="b74ee-133">Validation File</span></span>  <br/> |<span data-ttu-id="b74ee-134">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="b74ee-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="b74ee-135">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="b74ee-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="b74ee-136">Falso</span><span class="sxs-lookup"><span data-stu-id="b74ee-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b74ee-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="b74ee-137">See also</span></span>



- [<span data-ttu-id="b74ee-138">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="b74ee-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

