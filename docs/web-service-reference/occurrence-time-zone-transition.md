---
title: Aparición (transición de la zona horaria)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Occurrence
api_type:
- schema
ms.assetid: 5c1142b1-c51f-42e1-bbb2-57e00cad0fdb
description: El elemento de repetición representa la aparición del día de la semana del mes en el que se produce la transición de la zona horaria.
ms.openlocfilehash: bc5160480cc6881bb9d724aa61323f5717d1f2fa
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836636"
---
# <a name="occurrence-time-zone-transition"></a><span data-ttu-id="a1022-103">Aparición (transición de la zona horaria)</span><span class="sxs-lookup"><span data-stu-id="a1022-103">Occurrence (Time Zone Transition)</span></span>

<span data-ttu-id="a1022-104">El elemento de **repetición** representa la aparición del día de la semana del mes en el que se produce la transición de la zona horaria.</span><span class="sxs-lookup"><span data-stu-id="a1022-104">The **Occurrence** element represents the occurrence of the day of the week in the month that the time zone transition occurs.</span></span> 
  
```xml
<Occurrence/>
```

<span data-ttu-id="a1022-105">**int**</span><span class="sxs-lookup"><span data-stu-id="a1022-105">**int**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="a1022-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="a1022-106">Attributes and elements</span></span>

<span data-ttu-id="a1022-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="a1022-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a1022-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="a1022-108">Attributes</span></span>

<span data-ttu-id="a1022-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="a1022-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a1022-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="a1022-110">Child elements</span></span>

<span data-ttu-id="a1022-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="a1022-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="a1022-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="a1022-112">Parent elements</span></span>

|<span data-ttu-id="a1022-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="a1022-113">**Element**</span></span>|<span data-ttu-id="a1022-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a1022-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a1022-115">RecurringDayTransition</span><span class="sxs-lookup"><span data-stu-id="a1022-115">RecurringDayTransition</span></span>](recurringdaytransition.md) <br/> |<span data-ttu-id="a1022-116">Representa una transición de la zona horaria que se produce en el mismo día cada año.</span><span class="sxs-lookup"><span data-stu-id="a1022-116">Represents a time zone transition that occurs on the same day each year.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="a1022-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="a1022-117">Text value</span></span>

<span data-ttu-id="a1022-118">El valor de texto es un entero que representa la aparición del día de la semana del mes en el que se produce la transición de la zona horaria.</span><span class="sxs-lookup"><span data-stu-id="a1022-118">The text value is an integer that represents the occurrence of the day of the week in the month that the time zone transition occurs.</span></span> <span data-ttu-id="a1022-119">En la siguiente tabla se enumera los valores posibles.</span><span class="sxs-lookup"><span data-stu-id="a1022-119">The following table lists the possible values.</span></span>
  
|<span data-ttu-id="a1022-120">**Valor**</span><span class="sxs-lookup"><span data-stu-id="a1022-120">**Value**</span></span>|<span data-ttu-id="a1022-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a1022-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a1022-122">1</span><span class="sxs-lookup"><span data-stu-id="a1022-122">1</span></span>  <br/> |<span data-ttu-id="a1022-123">La primera aparición del día de la semana desde el comienzo del mes especificado.</span><span class="sxs-lookup"><span data-stu-id="a1022-123">The first occurrence of the specified day of the week from the beginning of the month.</span></span>  <br/> |
|<span data-ttu-id="a1022-124">2</span><span class="sxs-lookup"><span data-stu-id="a1022-124">2</span></span>  <br/> |<span data-ttu-id="a1022-125">La segunda aparición del día de la semana desde el comienzo del mes especificado.</span><span class="sxs-lookup"><span data-stu-id="a1022-125">The second occurrence of the specified day of the week from the beginning of the month.</span></span>  <br/> |
|<span data-ttu-id="a1022-126">3</span><span class="sxs-lookup"><span data-stu-id="a1022-126">3</span></span>  <br/> |<span data-ttu-id="a1022-127">La tercera aparición de día de la semana desde el comienzo del mes especificado.</span><span class="sxs-lookup"><span data-stu-id="a1022-127">The third occurrence of the specified day of the week from the beginning of the month.</span></span>  <br/> |
|<span data-ttu-id="a1022-128">4</span><span class="sxs-lookup"><span data-stu-id="a1022-128">4</span></span>  <br/> |<span data-ttu-id="a1022-129">La aparición cuarto de día de la semana desde el comienzo del mes especificado.</span><span class="sxs-lookup"><span data-stu-id="a1022-129">The fourth occurrence of the specified day of the week from the beginning of the month.</span></span>  <br/> |
|<span data-ttu-id="a1022-130">-1</span><span class="sxs-lookup"><span data-stu-id="a1022-130">-1</span></span>  <br/> |<span data-ttu-id="a1022-131">La primera aparición del día de la semana, desde el final del mes especificado.</span><span class="sxs-lookup"><span data-stu-id="a1022-131">The first occurrence of the specified day of the week from the end of the month.</span></span>  <br/> |
|<span data-ttu-id="a1022-132">-2</span><span class="sxs-lookup"><span data-stu-id="a1022-132">-2</span></span>  <br/> |<span data-ttu-id="a1022-133">La segunda aparición del día de la semana, desde el final del mes especificado.</span><span class="sxs-lookup"><span data-stu-id="a1022-133">The second occurrence of the specified day of the week from the end of the month.</span></span>  <br/> |
|<span data-ttu-id="a1022-134">-3</span><span class="sxs-lookup"><span data-stu-id="a1022-134">-3</span></span>  <br/> |<span data-ttu-id="a1022-135">La tercera aparición de día de la semana, desde el final del mes especificado.</span><span class="sxs-lookup"><span data-stu-id="a1022-135">The third occurrence of the specified day of the week from the end of the month.</span></span>  <br/> |
|<span data-ttu-id="a1022-136">-4</span><span class="sxs-lookup"><span data-stu-id="a1022-136">-4</span></span>  <br/> |<span data-ttu-id="a1022-137">La cuarta aparición del día de la semana, desde el final del mes especificado.</span><span class="sxs-lookup"><span data-stu-id="a1022-137">The fourth occurrence of the specified day of the week from the end of the month.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a1022-138">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a1022-138">Remarks</span></span>

<span data-ttu-id="a1022-139">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server que tiene instalada la función del servidor acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="a1022-139">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a1022-140">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="a1022-140">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a1022-141">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a1022-141">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a1022-142">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="a1022-142">Schema Name</span></span>  <br/> |<span data-ttu-id="a1022-143">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="a1022-143">Types schema</span></span>  <br/> |
|<span data-ttu-id="a1022-144">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="a1022-144">Validation File</span></span>  <br/> |<span data-ttu-id="a1022-145">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="a1022-145">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="a1022-146">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="a1022-146">Can be Empty</span></span>  <br/> |<span data-ttu-id="a1022-147">False</span><span class="sxs-lookup"><span data-stu-id="a1022-147">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a1022-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="a1022-148">See also</span></span>

- [<span data-ttu-id="a1022-149">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="a1022-149">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

