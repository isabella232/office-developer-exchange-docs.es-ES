---
title: DaysOfWeek (DaysOfWeekType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DaysOfWeek
api_type:
- schema
ms.assetid: c56f997d-28f3-4590-97b0-cb71f016dbe4
description: El elemento DaysOfWeek describe los días de la semana que se usan en los patrones de periodicidad de elemento.
ms.openlocfilehash: 0b730ff5a7bc9aa6b324fc080022d056c5342296
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764061"
---
# <a name="daysofweek-daysofweektype"></a><span data-ttu-id="da764-103">DaysOfWeek (DaysOfWeekType)</span><span class="sxs-lookup"><span data-stu-id="da764-103">DaysOfWeek (DaysOfWeekType)</span></span>

<span data-ttu-id="da764-104">El elemento **DaysOfWeek** describe los días de la semana que se usan en los patrones de periodicidad de elemento.</span><span class="sxs-lookup"><span data-stu-id="da764-104">The **DaysOfWeek** element describes days of the week that are used in item recurrence patterns.</span></span> 
  
```XML
<DaysOfWeek/>
```

<span data-ttu-id="da764-105">**DaysOfWeekType**</span><span class="sxs-lookup"><span data-stu-id="da764-105">**DaysOfWeekType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="da764-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="da764-106">Attributes and elements</span></span>

<span data-ttu-id="da764-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="da764-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="da764-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="da764-108">Attributes</span></span>

<span data-ttu-id="da764-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="da764-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="da764-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="da764-110">Child elements</span></span>

<span data-ttu-id="da764-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="da764-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="da764-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="da764-112">Parent elements</span></span>

|<span data-ttu-id="da764-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="da764-113">**Element**</span></span>|<span data-ttu-id="da764-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="da764-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="da764-115">WeeklyRecurrence</span><span class="sxs-lookup"><span data-stu-id="da764-115">WeeklyRecurrence</span></span>](weeklyrecurrence.md) <br/> |<span data-ttu-id="da764-116">Describe un patrón de periodicidad semanal.</span><span class="sxs-lookup"><span data-stu-id="da764-116">Describes a weekly recurrence pattern.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="da764-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="da764-117">Text value</span></span>

<span data-ttu-id="da764-118">Se requiere un valor de texto.</span><span class="sxs-lookup"><span data-stu-id="da764-118">A text value is required.</span></span> <span data-ttu-id="da764-119">Los valores posibles son:</span><span class="sxs-lookup"><span data-stu-id="da764-119">The following are the possible values:</span></span>
  
- <span data-ttu-id="da764-120">Domingo</span><span class="sxs-lookup"><span data-stu-id="da764-120">Sunday</span></span>    
- <span data-ttu-id="da764-121">Lunes</span><span class="sxs-lookup"><span data-stu-id="da764-121">Monday</span></span>    
- <span data-ttu-id="da764-122">Martes</span><span class="sxs-lookup"><span data-stu-id="da764-122">Tuesday</span></span>    
- <span data-ttu-id="da764-123">Miércoles</span><span class="sxs-lookup"><span data-stu-id="da764-123">Wednesday</span></span>    
- <span data-ttu-id="da764-124">Jueves</span><span class="sxs-lookup"><span data-stu-id="da764-124">Thursday</span></span>    
- <span data-ttu-id="da764-125">Viernes</span><span class="sxs-lookup"><span data-stu-id="da764-125">Friday</span></span>    
- <span data-ttu-id="da764-126">Sábado</span><span class="sxs-lookup"><span data-stu-id="da764-126">Saturday</span></span>    
- <span data-ttu-id="da764-127">Día (este valor no es válido para un patrón de periodicidad semanal)</span><span class="sxs-lookup"><span data-stu-id="da764-127">Day (this value is not valid for a weekly recurrence pattern)</span></span>    
- <span data-ttu-id="da764-128">Weekday (este valor no es válido para un patrón de periodicidad semanal)</span><span class="sxs-lookup"><span data-stu-id="da764-128">Weekday (this value is not valid for a weekly recurrence pattern)</span></span>    
- <span data-ttu-id="da764-129">WeekendDay (este valor no es válido para un patrón de periodicidad semanal)</span><span class="sxs-lookup"><span data-stu-id="da764-129">WeekendDay (this value is not valid for a weekly recurrence pattern)</span></span>
    
<span data-ttu-id="da764-130">Un patrón de periodicidad semanal puede contener varios valores.</span><span class="sxs-lookup"><span data-stu-id="da764-130">A weekly recurrence pattern can contain multiple values.</span></span> <span data-ttu-id="da764-131">Los valores están separados por un carácter de espacio.</span><span class="sxs-lookup"><span data-stu-id="da764-131">Values are separated by a space character.</span></span> <span data-ttu-id="da764-132">Por ejemplo, para una periodicidad semanal el martes y los jueves, el valor de texto será "Martes jueves".</span><span class="sxs-lookup"><span data-stu-id="da764-132">For example, for a weekly recurrence on Tuesdays and Thursdays, the text value will be "Tuesday Thursday".</span></span>
  
## <a name="remarks"></a><span data-ttu-id="da764-133">Notas</span><span class="sxs-lookup"><span data-stu-id="da764-133">Remarks</span></span>

<span data-ttu-id="da764-134">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2010 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="da764-134">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="da764-135">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="da764-135">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="da764-136">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="da764-136">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="da764-137">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="da764-137">Schema Name</span></span>  <br/> |<span data-ttu-id="da764-138">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="da764-138">Types schema</span></span>  <br/> |
|<span data-ttu-id="da764-139">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="da764-139">Validation File</span></span>  <br/> |<span data-ttu-id="da764-140">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="da764-140">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="da764-141">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="da764-141">Can be Empty</span></span>  <br/> |<span data-ttu-id="da764-142">False</span><span class="sxs-lookup"><span data-stu-id="da764-142">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="da764-143">Ver también</span><span class="sxs-lookup"><span data-stu-id="da764-143">See also</span></span>

- [<span data-ttu-id="da764-144">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="da764-144">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

