---
title: Aparición (transición de zona horaria)
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
description: El elemento Representation representa la ocurrencia del día de la semana del mes en que se produce la transición de zona horaria.
ms.openlocfilehash: 846f6b22f43bcda07b9408d768d0845a5acfe668
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467980"
---
# <a name="occurrence-time-zone-transition"></a><span data-ttu-id="62629-103">Aparición (transición de zona horaria)</span><span class="sxs-lookup"><span data-stu-id="62629-103">Occurrence (Time Zone Transition)</span></span>

<span data-ttu-id="62629-104">El **elemento** Representation representa la ocurrencia del día de la semana del mes en que se produce la transición de zona horaria.</span><span class="sxs-lookup"><span data-stu-id="62629-104">The **Occurrence** element represents the occurrence of the day of the week in the month that the time zone transition occurs.</span></span> 
  
```xml
<Occurrence/>
```

<span data-ttu-id="62629-105">**int**</span><span class="sxs-lookup"><span data-stu-id="62629-105">**int**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="62629-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="62629-106">Attributes and elements</span></span>

<span data-ttu-id="62629-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="62629-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="62629-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="62629-108">Attributes</span></span>

<span data-ttu-id="62629-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="62629-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="62629-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="62629-110">Child elements</span></span>

<span data-ttu-id="62629-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="62629-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="62629-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="62629-112">Parent elements</span></span>

|<span data-ttu-id="62629-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="62629-113">**Element**</span></span>|<span data-ttu-id="62629-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="62629-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="62629-115">RecurringDayTransition</span><span class="sxs-lookup"><span data-stu-id="62629-115">RecurringDayTransition</span></span>](recurringdaytransition.md) <br/> |<span data-ttu-id="62629-116">Representa una transición de zona horaria que se produce el mismo día cada año.</span><span class="sxs-lookup"><span data-stu-id="62629-116">Represents a time zone transition that occurs on the same day each year.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="62629-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="62629-117">Text value</span></span>

<span data-ttu-id="62629-118">El valor de texto es un entero que representa la ocurrencia del día de la semana del mes en que se produce la transición de zona horaria.</span><span class="sxs-lookup"><span data-stu-id="62629-118">The text value is an integer that represents the occurrence of the day of the week in the month that the time zone transition occurs.</span></span> <span data-ttu-id="62629-119">En la siguiente tabla se enumeran los valores posibles.</span><span class="sxs-lookup"><span data-stu-id="62629-119">The following table lists the possible values.</span></span>
  
|<span data-ttu-id="62629-120">**Valor**</span><span class="sxs-lookup"><span data-stu-id="62629-120">**Value**</span></span>|<span data-ttu-id="62629-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="62629-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="62629-122">1</span><span class="sxs-lookup"><span data-stu-id="62629-122">1</span></span>  <br/> |<span data-ttu-id="62629-123">Primera aparición del día de la semana especificado desde el principio del mes.</span><span class="sxs-lookup"><span data-stu-id="62629-123">The first occurrence of the specified day of the week from the beginning of the month.</span></span>  <br/> |
|<span data-ttu-id="62629-124">segundo</span><span class="sxs-lookup"><span data-stu-id="62629-124">2</span></span>  <br/> |<span data-ttu-id="62629-125">Segunda aparición del día de la semana especificado desde el principio del mes.</span><span class="sxs-lookup"><span data-stu-id="62629-125">The second occurrence of the specified day of the week from the beginning of the month.</span></span>  <br/> |
|<span data-ttu-id="62629-126">3</span><span class="sxs-lookup"><span data-stu-id="62629-126">3</span></span>  <br/> |<span data-ttu-id="62629-127">La tercera repetición del día de la semana especificado desde el principio del mes.</span><span class="sxs-lookup"><span data-stu-id="62629-127">The third occurrence of the specified day of the week from the beginning of the month.</span></span>  <br/> |
|<span data-ttu-id="62629-128">4 </span><span class="sxs-lookup"><span data-stu-id="62629-128">4</span></span>  <br/> |<span data-ttu-id="62629-129">La cuarta aparición del día de la semana especificado desde el principio del mes.</span><span class="sxs-lookup"><span data-stu-id="62629-129">The fourth occurrence of the specified day of the week from the beginning of the month.</span></span>  <br/> |
|<span data-ttu-id="62629-130">-1</span><span class="sxs-lookup"><span data-stu-id="62629-130">-1</span></span>  <br/> |<span data-ttu-id="62629-131">Primera aparición del día de la semana especificado a partir del final del mes.</span><span class="sxs-lookup"><span data-stu-id="62629-131">The first occurrence of the specified day of the week from the end of the month.</span></span>  <br/> |
|<span data-ttu-id="62629-132">-2</span><span class="sxs-lookup"><span data-stu-id="62629-132">-2</span></span>  <br/> |<span data-ttu-id="62629-133">Segunda aparición del día de la semana especificado a partir del final del mes.</span><span class="sxs-lookup"><span data-stu-id="62629-133">The second occurrence of the specified day of the week from the end of the month.</span></span>  <br/> |
|<span data-ttu-id="62629-134">-3</span><span class="sxs-lookup"><span data-stu-id="62629-134">-3</span></span>  <br/> |<span data-ttu-id="62629-135">Tercera aparición del día de la semana especificado a partir del final del mes.</span><span class="sxs-lookup"><span data-stu-id="62629-135">The third occurrence of the specified day of the week from the end of the month.</span></span>  <br/> |
|<span data-ttu-id="62629-136">-4</span><span class="sxs-lookup"><span data-stu-id="62629-136">-4</span></span>  <br/> |<span data-ttu-id="62629-137">La cuarta aparición del día de la semana especificado a partir del final del mes.</span><span class="sxs-lookup"><span data-stu-id="62629-137">The fourth occurrence of the specified day of the week from the end of the month.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="62629-138">Comentarios</span><span class="sxs-lookup"><span data-stu-id="62629-138">Remarks</span></span>

<span data-ttu-id="62629-139">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="62629-139">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="62629-140">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="62629-140">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="62629-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="62629-141">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="62629-142">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="62629-142">Schema Name</span></span>  <br/> |<span data-ttu-id="62629-143">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="62629-143">Types schema</span></span>  <br/> |
|<span data-ttu-id="62629-144">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="62629-144">Validation File</span></span>  <br/> |<span data-ttu-id="62629-145">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="62629-145">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="62629-146">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="62629-146">Can be Empty</span></span>  <br/> |<span data-ttu-id="62629-147">Falso</span><span class="sxs-lookup"><span data-stu-id="62629-147">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="62629-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="62629-148">See also</span></span>

- [<span data-ttu-id="62629-149">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="62629-149">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

