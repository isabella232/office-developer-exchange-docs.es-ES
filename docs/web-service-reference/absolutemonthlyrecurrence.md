---
title: AbsoluteMonthlyRecurrence
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AbsoluteMonthlyRecurrence
api_type:
- schema
ms.assetid: 178fa0ae-9dfc-417f-933c-d657d31c2161
description: El elemento AbsoluteMonthlyRecurrence representa un patrón de periodicidad mensual.
ms.openlocfilehash: 3176cd30a1cfe7b2310f960ce377ab7a277e795a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44460438"
---
# <a name="absolutemonthlyrecurrence"></a><span data-ttu-id="6c392-103">AbsoluteMonthlyRecurrence</span><span class="sxs-lookup"><span data-stu-id="6c392-103">AbsoluteMonthlyRecurrence</span></span>

<span data-ttu-id="6c392-104">El elemento **AbsoluteMonthlyRecurrence** representa un patrón de periodicidad mensual.</span><span class="sxs-lookup"><span data-stu-id="6c392-104">The **AbsoluteMonthlyRecurrence** element represents a monthly recurrence pattern.</span></span> 
  
```xml
<AbsoluteMonthlyRecurrence>
   <Interval/>
   <DayOfMonth/>
</AbsoluteMonthlyRecurrence>
```

 <span data-ttu-id="6c392-105">**AbsoluteMonthlyRecurrencePatternType**</span><span class="sxs-lookup"><span data-stu-id="6c392-105">**AbsoluteMonthlyRecurrencePatternType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6c392-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="6c392-106">Attributes and elements</span></span>

<span data-ttu-id="6c392-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="6c392-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6c392-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="6c392-108">Attributes</span></span>

<span data-ttu-id="6c392-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="6c392-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6c392-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="6c392-110">Child elements</span></span>

|<span data-ttu-id="6c392-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="6c392-111">**Element**</span></span>|<span data-ttu-id="6c392-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6c392-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6c392-113">DayOfMonth</span><span class="sxs-lookup"><span data-stu-id="6c392-113">DayOfMonth</span></span>](dayofmonth.md) <br/> |<span data-ttu-id="6c392-114">Describe el día de un mes en que se produce un elemento periódico.</span><span class="sxs-lookup"><span data-stu-id="6c392-114">Describes the day in a month that a recurring item occurs.</span></span> <span data-ttu-id="6c392-115">El intervalo de valores para esta propiedad es de 1 a 31.</span><span class="sxs-lookup"><span data-stu-id="6c392-115">The range of values for this property is 1 to 31.</span></span> <span data-ttu-id="6c392-116">Si, en un mes determinado, este valor es superior al número de días del mes, se asume el último día del mes para esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="6c392-116">If for a particular month this value is larger than the number of days in the month, the last day of the month is assumed for this property.</span></span>  <br/> |
|[<span data-ttu-id="6c392-117">Intervalo de</span><span class="sxs-lookup"><span data-stu-id="6c392-117">Interval</span></span>](interval.md) <br/> |<span data-ttu-id="6c392-118">Define el intervalo entre dos elementos periódicos consecutivos.</span><span class="sxs-lookup"><span data-stu-id="6c392-118">Defines the interval between two consecutive recurring items.</span></span> <span data-ttu-id="6c392-119">Por ejemplo, si el elemento **Interval** tiene un valor de 5, el elemento periódico se produce cada 5 meses.</span><span class="sxs-lookup"><span data-stu-id="6c392-119">For example, if the **Interval** element has a value of 5, the recurring item occurs every 5 months.</span></span> <span data-ttu-id="6c392-120">El intervalo de valores válidos es de 1 a 99.</span><span class="sxs-lookup"><span data-stu-id="6c392-120">The range of valid values is from 1 to 99.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="6c392-121">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="6c392-121">Parent elements</span></span>

|<span data-ttu-id="6c392-122">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="6c392-122">**Element**</span></span>|<span data-ttu-id="6c392-123">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6c392-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6c392-124">Periodicidad (TaskRecurrenceType)</span><span class="sxs-lookup"><span data-stu-id="6c392-124">Recurrence (TaskRecurrenceType)</span></span>](recurrence-taskrecurrencetype.md) <br/> |<span data-ttu-id="6c392-125">Contiene información de periodicidad para tareas periódicas.</span><span class="sxs-lookup"><span data-stu-id="6c392-125">Contains recurrence information for recurring tasks.</span></span>  <br/> |
|[<span data-ttu-id="6c392-126">Recurrence (RecurrenceType)</span><span class="sxs-lookup"><span data-stu-id="6c392-126">Recurrence (RecurrenceType)</span></span>](recurrence-recurrencetype.md) <br/> |<span data-ttu-id="6c392-127">Contiene el patrón de periodicidad para los elementos de calendario y las convocatorias de reunión.</span><span class="sxs-lookup"><span data-stu-id="6c392-127">Contains the recurrence pattern for calendar items and meeting requests.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6c392-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6c392-128">Remarks</span></span>

<span data-ttu-id="6c392-129">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="6c392-129">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6c392-130">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="6c392-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6c392-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="6c392-131">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="6c392-132">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="6c392-132">Schema Name</span></span>  <br/> |<span data-ttu-id="6c392-133">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="6c392-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="6c392-134">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="6c392-134">Validation File</span></span>  <br/> |<span data-ttu-id="6c392-135">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="6c392-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="6c392-136">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="6c392-136">Can Be Empty</span></span>  <br/> |<span data-ttu-id="6c392-137">Falso</span><span class="sxs-lookup"><span data-stu-id="6c392-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6c392-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="6c392-138">See also</span></span>

- [<span data-ttu-id="6c392-139">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="6c392-139">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

