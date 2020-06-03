---
title: DayOfWeekIndex
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DayOfWeekIndex
api_type:
- schema
ms.assetid: 82420338-a1f7-4887-b338-b2d93b2c2bf1
description: El elemento DayOfWeekIndex describe qué semana de un mes se usa en un patrón de periodicidad relativo.
ms.openlocfilehash: c9235d83a944f9c8883439dd2adf190b88977f16
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529213"
---
# <a name="dayofweekindex"></a><span data-ttu-id="5bb25-103">DayOfWeekIndex</span><span class="sxs-lookup"><span data-stu-id="5bb25-103">DayOfWeekIndex</span></span>

<span data-ttu-id="5bb25-104">El elemento **DayOfWeekIndex** describe qué semana de un mes se usa en un patrón de periodicidad relativo.</span><span class="sxs-lookup"><span data-stu-id="5bb25-104">The **DayOfWeekIndex** element describes which week in a month is used in a relative recurrence pattern.</span></span> 
  
```xml
<DayOfWeekIndex/>
```

<span data-ttu-id="5bb25-105">**DayOfWeekIndexType**</span><span class="sxs-lookup"><span data-stu-id="5bb25-105">**DayOfWeekIndexType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="5bb25-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="5bb25-106">Attributes and elements</span></span>

<span data-ttu-id="5bb25-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="5bb25-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5bb25-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="5bb25-108">Attributes</span></span>

<span data-ttu-id="5bb25-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="5bb25-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5bb25-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="5bb25-110">Child elements</span></span>

<span data-ttu-id="5bb25-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="5bb25-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="5bb25-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="5bb25-112">Parent elements</span></span>

|<span data-ttu-id="5bb25-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="5bb25-113">**Element**</span></span>|<span data-ttu-id="5bb25-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5bb25-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5bb25-115">RelativeYearlyRecurrence</span><span class="sxs-lookup"><span data-stu-id="5bb25-115">RelativeYearlyRecurrence</span></span>](relativeyearlyrecurrence.md) <br/> |<span data-ttu-id="5bb25-116">Describe un patrón de periodicidad anual relativo.</span><span class="sxs-lookup"><span data-stu-id="5bb25-116">Describes a relative yearly recurrence pattern.</span></span>  <br/> |
|[<span data-ttu-id="5bb25-117">RelativeMonthlyRecurrence</span><span class="sxs-lookup"><span data-stu-id="5bb25-117">RelativeMonthlyRecurrence</span></span>](relativemonthlyrecurrence.md) <br/> |<span data-ttu-id="5bb25-118">Describe un patrón de periodicidad mensual relativo.</span><span class="sxs-lookup"><span data-stu-id="5bb25-118">Describes a relative monthly recurrence pattern.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="5bb25-119">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="5bb25-119">Text value</span></span>

<span data-ttu-id="5bb25-120">Se requiere un valor de texto.</span><span class="sxs-lookup"><span data-stu-id="5bb25-120">A text value is required.</span></span> <span data-ttu-id="5bb25-121">Los valores posibles son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="5bb25-121">The following are the possible values:</span></span>
  
- <span data-ttu-id="5bb25-122">Primero</span><span class="sxs-lookup"><span data-stu-id="5bb25-122">First</span></span>    
- <span data-ttu-id="5bb25-123">Segundo</span><span class="sxs-lookup"><span data-stu-id="5bb25-123">Second</span></span>    
- <span data-ttu-id="5bb25-124">Tercera</span><span class="sxs-lookup"><span data-stu-id="5bb25-124">Third</span></span>    
- <span data-ttu-id="5bb25-125">Cuarta</span><span class="sxs-lookup"><span data-stu-id="5bb25-125">Fourth</span></span>    
- <span data-ttu-id="5bb25-126">Último</span><span class="sxs-lookup"><span data-stu-id="5bb25-126">Last</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5bb25-127">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5bb25-127">Remarks</span></span>

<span data-ttu-id="5bb25-128">Por ejemplo, el segundo lunes de un mes puede producirse la tercera semana de ese mes.</span><span class="sxs-lookup"><span data-stu-id="5bb25-128">For example, the second Monday of a month may occur in the third week of that month.</span></span> <span data-ttu-id="5bb25-129">Si un mes comienza un viernes, la primera semana del mes solo contiene unos días y no contiene un lunes.</span><span class="sxs-lookup"><span data-stu-id="5bb25-129">If a month starts on a Friday, the first week of the month only contains a few days and does not contain a Monday.</span></span> <span data-ttu-id="5bb25-130">Por lo tanto, el primer lunes tendría que producirse la segunda semana.</span><span class="sxs-lookup"><span data-stu-id="5bb25-130">Therefore, the first Monday would have to occur in the second week.</span></span>
  
<span data-ttu-id="5bb25-131">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="5bb25-131">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5bb25-132">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="5bb25-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5bb25-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="5bb25-133">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="5bb25-134">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="5bb25-134">Schema name</span></span>  <br/> |<span data-ttu-id="5bb25-135">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="5bb25-135">Types schema</span></span>  <br/> |
|<span data-ttu-id="5bb25-136">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="5bb25-136">Validation file</span></span>  <br/> |<span data-ttu-id="5bb25-137">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="5bb25-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="5bb25-138">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="5bb25-138">Can be empty</span></span>  <br/> |<span data-ttu-id="5bb25-139">Falso</span><span class="sxs-lookup"><span data-stu-id="5bb25-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5bb25-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="5bb25-140">See also</span></span>

- [<span data-ttu-id="5bb25-141">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="5bb25-141">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

