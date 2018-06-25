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
description: El elemento DayOfWeekIndex describe qué semana en un mes se utiliza en un patrón de periodicidad relativa.
ms.openlocfilehash: 4987685d0c3cefdfad4f5be1368776a5b859bf94
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764057"
---
# <a name="dayofweekindex"></a><span data-ttu-id="0125e-103">DayOfWeekIndex</span><span class="sxs-lookup"><span data-stu-id="0125e-103">DayOfWeekIndex</span></span>

<span data-ttu-id="0125e-104">El elemento **DayOfWeekIndex** describe qué semana en un mes se utiliza en un patrón de periodicidad relativa.</span><span class="sxs-lookup"><span data-stu-id="0125e-104">The **DayOfWeekIndex** element describes which week in a month is used in a relative recurrence pattern.</span></span> 
  
```xml
<DayOfWeekIndex/>
```

<span data-ttu-id="0125e-105">**DayOfWeekIndexType**</span><span class="sxs-lookup"><span data-stu-id="0125e-105">**DayOfWeekIndexType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="0125e-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="0125e-106">Attributes and elements</span></span>

<span data-ttu-id="0125e-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="0125e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0125e-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="0125e-108">Attributes</span></span>

<span data-ttu-id="0125e-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="0125e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0125e-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="0125e-110">Child elements</span></span>

<span data-ttu-id="0125e-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="0125e-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="0125e-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="0125e-112">Parent elements</span></span>

|<span data-ttu-id="0125e-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="0125e-113">**Element**</span></span>|<span data-ttu-id="0125e-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0125e-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0125e-115">RelativeYearlyRecurrence</span><span class="sxs-lookup"><span data-stu-id="0125e-115">RelativeYearlyRecurrence</span></span>](relativeyearlyrecurrence.md) <br/> |<span data-ttu-id="0125e-116">Describe un patrón de periodicidad anual relativa.</span><span class="sxs-lookup"><span data-stu-id="0125e-116">Describes a relative yearly recurrence pattern.</span></span>  <br/> |
|[<span data-ttu-id="0125e-117">RelativeMonthlyRecurrence</span><span class="sxs-lookup"><span data-stu-id="0125e-117">RelativeMonthlyRecurrence</span></span>](relativemonthlyrecurrence.md) <br/> |<span data-ttu-id="0125e-118">Describe un patrón de periodicidad mensual relativa.</span><span class="sxs-lookup"><span data-stu-id="0125e-118">Describes a relative monthly recurrence pattern.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="0125e-119">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="0125e-119">Text value</span></span>

<span data-ttu-id="0125e-120">Se requiere un valor de texto.</span><span class="sxs-lookup"><span data-stu-id="0125e-120">A text value is required.</span></span> <span data-ttu-id="0125e-121">Los valores posibles son:</span><span class="sxs-lookup"><span data-stu-id="0125e-121">The following are the possible values:</span></span>
  
- <span data-ttu-id="0125e-122">Primera</span><span class="sxs-lookup"><span data-stu-id="0125e-122">First</span></span>    
- <span data-ttu-id="0125e-123">Segunda</span><span class="sxs-lookup"><span data-stu-id="0125e-123">Second</span></span>    
- <span data-ttu-id="0125e-124">Tercera</span><span class="sxs-lookup"><span data-stu-id="0125e-124">Third</span></span>    
- <span data-ttu-id="0125e-125">Cuarta</span><span class="sxs-lookup"><span data-stu-id="0125e-125">Fourth</span></span>    
- <span data-ttu-id="0125e-126">Último</span><span class="sxs-lookup"><span data-stu-id="0125e-126">Last</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0125e-127">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0125e-127">Remarks</span></span>

<span data-ttu-id="0125e-128">Por ejemplo, pueden producirse el segundo lunes de cada mes en la tercera semana del mes.</span><span class="sxs-lookup"><span data-stu-id="0125e-128">For example, the second Monday of a month may occur in the third week of that month.</span></span> <span data-ttu-id="0125e-129">Si se inicia un mes un viernes, la primera semana del mes sólo contiene unos días y no contiene un lunes.</span><span class="sxs-lookup"><span data-stu-id="0125e-129">If a month starts on a Friday, the first week of the month only contains a few days and does not contain a Monday.</span></span> <span data-ttu-id="0125e-130">Por lo tanto, el primer lunes tendría que se producen en la segunda semana.</span><span class="sxs-lookup"><span data-stu-id="0125e-130">Therefore, the first Monday would have to occur in the second week.</span></span>
  
<span data-ttu-id="0125e-131">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="0125e-131">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0125e-132">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="0125e-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0125e-133">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="0125e-133">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="0125e-134">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="0125e-134">Schema name</span></span>  <br/> |<span data-ttu-id="0125e-135">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="0125e-135">Types schema</span></span>  <br/> |
|<span data-ttu-id="0125e-136">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="0125e-136">Validation file</span></span>  <br/> |<span data-ttu-id="0125e-137">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="0125e-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="0125e-138">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="0125e-138">Can be empty</span></span>  <br/> |<span data-ttu-id="0125e-139">False</span><span class="sxs-lookup"><span data-stu-id="0125e-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0125e-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="0125e-140">See also</span></span>

- [<span data-ttu-id="0125e-141">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="0125e-141">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

