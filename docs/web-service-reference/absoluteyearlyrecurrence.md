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
ms.openlocfilehash: 19b617dfd5c0a3d206d62439c880da084fd5f5f0
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460417"
---
# <a name="absoluteyearlyrecurrence"></a><span data-ttu-id="44d64-103">AbsoluteYearlyRecurrence</span><span class="sxs-lookup"><span data-stu-id="44d64-103">AbsoluteYearlyRecurrence</span></span>

<span data-ttu-id="44d64-104">El elemento **AbsoluteYearlyRecurrence** representa un patrón de periodicidad anual.</span><span class="sxs-lookup"><span data-stu-id="44d64-104">The **AbsoluteYearlyRecurrence** element represents a yearly recurrence pattern.</span></span> 
  
```xml
<AbsoluteYearlyRecurrence>
   <DayOfMonth/>
   <Month/>
</AbsoluteYearlyRecurrence>
```

 <span data-ttu-id="44d64-105">**AbsoluteYearlyRecurrencePatternType**</span><span class="sxs-lookup"><span data-stu-id="44d64-105">**AbsoluteYearlyRecurrencePatternType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="44d64-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="44d64-106">Attributes and elements</span></span>

<span data-ttu-id="44d64-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="44d64-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="44d64-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="44d64-108">Attributes</span></span>

<span data-ttu-id="44d64-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="44d64-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="44d64-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="44d64-110">Child elements</span></span>

|<span data-ttu-id="44d64-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="44d64-111">**Element**</span></span>|<span data-ttu-id="44d64-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="44d64-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="44d64-113">DayOfMonth</span><span class="sxs-lookup"><span data-stu-id="44d64-113">DayOfMonth</span></span>](dayofmonth.md) <br/> |<span data-ttu-id="44d64-114">Describe el día de un mes en el que se produce un elemento periódico.</span><span class="sxs-lookup"><span data-stu-id="44d64-114">Describes the day in a month on which a recurring item occurs.</span></span> <span data-ttu-id="44d64-115">El intervalo de valores para esta propiedad es de 1 a 31.</span><span class="sxs-lookup"><span data-stu-id="44d64-115">The range of values for this property is 1 to 31.</span></span> <span data-ttu-id="44d64-116">Si, en un mes determinado, este valor es superior al número de días del mes, se asume el último día del mes para esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="44d64-116">If for a particular month this value is larger than the number of days in the month, the last day of the month is assumed for this property.</span></span>  <br/> |
|[<span data-ttu-id="44d64-117">Month (periodicidad de elementos)</span><span class="sxs-lookup"><span data-stu-id="44d64-117">Month (Item Recurrence)</span></span>](month-item-recurrence.md) <br/> |<span data-ttu-id="44d64-118">Describe el mes en el que se produce un elemento periódico anual.</span><span class="sxs-lookup"><span data-stu-id="44d64-118">Describes the month in which a yearly recurring item occurs.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="44d64-119">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="44d64-119">Parent elements</span></span>

|<span data-ttu-id="44d64-120">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="44d64-120">**Element**</span></span>|<span data-ttu-id="44d64-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="44d64-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="44d64-122">Periodicidad (TaskRecurrenceType)</span><span class="sxs-lookup"><span data-stu-id="44d64-122">Recurrence (TaskRecurrenceType)</span></span>](recurrence-taskrecurrencetype.md) <br/> |<span data-ttu-id="44d64-123">Contiene información de periodicidad para tareas periódicas.</span><span class="sxs-lookup"><span data-stu-id="44d64-123">Contains recurrence information for recurring tasks.</span></span>  <br/> |
|[<span data-ttu-id="44d64-124">Recurrence (RecurrenceType)</span><span class="sxs-lookup"><span data-stu-id="44d64-124">Recurrence (RecurrenceType)</span></span>](recurrence-recurrencetype.md) <br/> |<span data-ttu-id="44d64-125">Contiene el patrón de periodicidad para los elementos de calendario y las convocatorias de reunión.</span><span class="sxs-lookup"><span data-stu-id="44d64-125">Contains the recurrence pattern for calendar items and meeting requests.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="44d64-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="44d64-126">Remarks</span></span>

<span data-ttu-id="44d64-127">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="44d64-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="44d64-128">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="44d64-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="44d64-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="44d64-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="44d64-130">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="44d64-130">Schema Name</span></span>  <br/> |<span data-ttu-id="44d64-131">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="44d64-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="44d64-132">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="44d64-132">Validation File</span></span>  <br/> |<span data-ttu-id="44d64-133">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="44d64-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="44d64-134">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="44d64-134">Can Be Empty</span></span>  <br/> |<span data-ttu-id="44d64-135">Falso</span><span class="sxs-lookup"><span data-stu-id="44d64-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="44d64-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="44d64-136">See also</span></span>

- [<span data-ttu-id="44d64-137">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="44d64-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

