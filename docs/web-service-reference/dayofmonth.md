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
description: El elemento DayOfMonth describe el día de un mes en que se produce un elemento periódico.
ms.openlocfilehash: dc333a46283d5e8eba3a79f62f8c22c22f56e190
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44442832"
---
# <a name="dayofmonth"></a><span data-ttu-id="6d16a-103">DayOfMonth</span><span class="sxs-lookup"><span data-stu-id="6d16a-103">DayOfMonth</span></span>

<span data-ttu-id="6d16a-104">El elemento **DayOfMonth** describe el día de un mes en que se produce un elemento periódico.</span><span class="sxs-lookup"><span data-stu-id="6d16a-104">The **DayOfMonth** element describes the day in a month that a recurring item occurs.</span></span> 
  
```xml
<DayOfMonth/>
```

<span data-ttu-id="6d16a-105">**int**</span><span class="sxs-lookup"><span data-stu-id="6d16a-105">**int**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="6d16a-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="6d16a-106">Attributes and elements</span></span>

<span data-ttu-id="6d16a-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="6d16a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6d16a-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="6d16a-108">Attributes</span></span>

<span data-ttu-id="6d16a-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="6d16a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6d16a-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="6d16a-110">Child elements</span></span>

<span data-ttu-id="6d16a-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="6d16a-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="6d16a-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="6d16a-112">Parent elements</span></span>

|<span data-ttu-id="6d16a-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="6d16a-113">**Element**</span></span>|<span data-ttu-id="6d16a-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6d16a-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6d16a-115">AbsoluteYearlyRecurrence</span><span class="sxs-lookup"><span data-stu-id="6d16a-115">AbsoluteYearlyRecurrence</span></span>](absoluteyearlyrecurrence.md) <br/> |<span data-ttu-id="6d16a-116">Representa un patrón de periodicidad anual.</span><span class="sxs-lookup"><span data-stu-id="6d16a-116">Represents a yearly recurrence pattern.</span></span>  <br/> |
|[<span data-ttu-id="6d16a-117">AbsoluteMonthlyRecurrence</span><span class="sxs-lookup"><span data-stu-id="6d16a-117">AbsoluteMonthlyRecurrence</span></span>](absolutemonthlyrecurrence.md) <br/> |<span data-ttu-id="6d16a-118">Representa un patrón de periodicidad mensual.</span><span class="sxs-lookup"><span data-stu-id="6d16a-118">Represents a monthly recurrence pattern.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="6d16a-119">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="6d16a-119">Text value</span></span>

<span data-ttu-id="6d16a-120">Un valor de texto que representa un número entero en el intervalo de 1 a 31 es obligatorio.</span><span class="sxs-lookup"><span data-stu-id="6d16a-120">A text value that represents an integer in the range of 1 to 31 is required.</span></span> <span data-ttu-id="6d16a-121">Si, en un mes determinado, este valor es superior al número de días del mes, se supone el último día del mes.</span><span class="sxs-lookup"><span data-stu-id="6d16a-121">If for a particular month this value is larger than the number of days in the month, the last day of the month is assumed.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6d16a-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6d16a-122">Remarks</span></span>

<span data-ttu-id="6d16a-123">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="6d16a-123">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6d16a-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="6d16a-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6d16a-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="6d16a-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="6d16a-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="6d16a-126">Schema name</span></span>  <br/> |<span data-ttu-id="6d16a-127">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="6d16a-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="6d16a-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="6d16a-128">Validation file</span></span>  <br/> |<span data-ttu-id="6d16a-129">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="6d16a-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="6d16a-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="6d16a-130">Can be empty</span></span>  <br/> |<span data-ttu-id="6d16a-131">Falso</span><span class="sxs-lookup"><span data-stu-id="6d16a-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6d16a-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="6d16a-132">See also</span></span>

- [<span data-ttu-id="6d16a-133">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="6d16a-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

