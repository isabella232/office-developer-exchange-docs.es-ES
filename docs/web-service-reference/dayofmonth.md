---
title: DayOfMonth
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DayOfMonth
api_type:
- schema
ms.assetid: 09b7504e-08d8-42f9-88cc-a2a37a2e2b8b
description: El elemento DayOfMonth describe el día en un mes en el que se produce un elemento periódico.
ms.openlocfilehash: 0d0d95849a2562e06b88872b2857cc5e6ca67af3
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764048"
---
# <a name="dayofmonth"></a><span data-ttu-id="5a187-103">DayOfMonth</span><span class="sxs-lookup"><span data-stu-id="5a187-103">DayOfMonth</span></span>

<span data-ttu-id="5a187-104">El elemento **DayOfMonth** describe el día en un mes en el que se produce un elemento periódico.</span><span class="sxs-lookup"><span data-stu-id="5a187-104">The **DayOfMonth** element describes the day in a month that a recurring item occurs.</span></span> 
  
```xml
<DayOfMonth/>
```

<span data-ttu-id="5a187-105">**int**</span><span class="sxs-lookup"><span data-stu-id="5a187-105">**int**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="5a187-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="5a187-106">Attributes and elements</span></span>

<span data-ttu-id="5a187-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="5a187-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5a187-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="5a187-108">Attributes</span></span>

<span data-ttu-id="5a187-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="5a187-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5a187-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="5a187-110">Child elements</span></span>

<span data-ttu-id="5a187-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="5a187-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="5a187-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="5a187-112">Parent elements</span></span>

|<span data-ttu-id="5a187-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="5a187-113">**Element**</span></span>|<span data-ttu-id="5a187-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5a187-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5a187-115">AbsoluteYearlyRecurrence</span><span class="sxs-lookup"><span data-stu-id="5a187-115">AbsoluteYearlyRecurrence</span></span>](absoluteyearlyrecurrence.md) <br/> |<span data-ttu-id="5a187-116">Representa un patrón de periodicidad anual.</span><span class="sxs-lookup"><span data-stu-id="5a187-116">Represents a yearly recurrence pattern.</span></span>  <br/> |
|[<span data-ttu-id="5a187-117">AbsoluteMonthlyRecurrence</span><span class="sxs-lookup"><span data-stu-id="5a187-117">AbsoluteMonthlyRecurrence</span></span>](absolutemonthlyrecurrence.md) <br/> |<span data-ttu-id="5a187-118">Representa un patrón de periodicidad mensual.</span><span class="sxs-lookup"><span data-stu-id="5a187-118">Represents a monthly recurrence pattern.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="5a187-119">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="5a187-119">Text value</span></span>

<span data-ttu-id="5a187-120">Se requiere un valor de texto que representa un número entero en el intervalo de 1 a 31.</span><span class="sxs-lookup"><span data-stu-id="5a187-120">A text value that represents an integer in the range of 1 to 31 is required.</span></span> <span data-ttu-id="5a187-121">Si para un mes determinado que este valor es mayor que el número de días del mes, se supone que el último día del mes.</span><span class="sxs-lookup"><span data-stu-id="5a187-121">If for a particular month this value is larger than the number of days in the month, the last day of the month is assumed.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5a187-122">Notas</span><span class="sxs-lookup"><span data-stu-id="5a187-122">Remarks</span></span>

<span data-ttu-id="5a187-123">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="5a187-123">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5a187-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="5a187-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5a187-125">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="5a187-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="5a187-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="5a187-126">Schema name</span></span>  <br/> |<span data-ttu-id="5a187-127">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="5a187-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="5a187-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="5a187-128">Validation file</span></span>  <br/> |<span data-ttu-id="5a187-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="5a187-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="5a187-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="5a187-130">Can be empty</span></span>  <br/> |<span data-ttu-id="5a187-131">False</span><span class="sxs-lookup"><span data-stu-id="5a187-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5a187-132">Ver también</span><span class="sxs-lookup"><span data-stu-id="5a187-132">See also</span></span>

- [<span data-ttu-id="5a187-133">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="5a187-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

