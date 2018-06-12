---
title: FirstDayOfWeek
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FirstDayOfWeek
api_type:
- schema
ms.assetid: d6cf1bd3-a19b-4d5f-9e25-8e337a4939e0
description: El elemento de FirstDayOfWeek especifica el primer día de la semana.
ms.openlocfilehash: 99858d17213d077ce7c51ad1c746588f2f3939a7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764660"
---
# <a name="firstdayofweek"></a><span data-ttu-id="fa92f-103">FirstDayOfWeek</span><span class="sxs-lookup"><span data-stu-id="fa92f-103">FirstDayOfWeek</span></span>

<span data-ttu-id="fa92f-104">El elemento de **FirstDayOfWeek** especifica el primer día de la semana.</span><span class="sxs-lookup"><span data-stu-id="fa92f-104">The **FirstDayOfWeek** element specifies the first day of the week.</span></span> 
  
```XML
<FirstDayOfWeek> Sunday | Monday | Tuesday | Wednesday | Thursday | Friday | Saturday</FirstDayOfWeek>
```

 <span data-ttu-id="fa92f-105">**DayOfWeekType**</span><span class="sxs-lookup"><span data-stu-id="fa92f-105">**DayOfWeekType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="fa92f-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="fa92f-106">Attributes and elements</span></span>

<span data-ttu-id="fa92f-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="fa92f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fa92f-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="fa92f-108">Attributes</span></span>

<span data-ttu-id="fa92f-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="fa92f-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="fa92f-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="fa92f-110">Child elements</span></span>

<span data-ttu-id="fa92f-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="fa92f-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="fa92f-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="fa92f-112">Parent elements</span></span>

|<span data-ttu-id="fa92f-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="fa92f-113">**Element**</span></span>|<span data-ttu-id="fa92f-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="fa92f-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fa92f-115">WeeklyRecurrence</span><span class="sxs-lookup"><span data-stu-id="fa92f-115">WeeklyRecurrence</span></span>](weeklyrecurrence.md) <br/> |<span data-ttu-id="fa92f-116">Describe un patrón de periodicidad semanal.</span><span class="sxs-lookup"><span data-stu-id="fa92f-116">Describes a weekly recurrence pattern.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="fa92f-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="fa92f-117">Text value</span></span>

<span data-ttu-id="fa92f-118">El valor de texto del elemento **FirstDayOfWeek** indica qué día de la semana se utiliza como el primer día de la semana.</span><span class="sxs-lookup"><span data-stu-id="fa92f-118">The text value of the **FirstDayOfWeek** element indicates which day of the week is used as the first day of the week.</span></span> <span data-ttu-id="fa92f-119">Los siguientes son los valores de texto posibles:</span><span class="sxs-lookup"><span data-stu-id="fa92f-119">The following are the possible text values:</span></span> 
  
- <span data-ttu-id="fa92f-120">Domingo</span><span class="sxs-lookup"><span data-stu-id="fa92f-120">Sunday</span></span>
    
- <span data-ttu-id="fa92f-121">Lunes</span><span class="sxs-lookup"><span data-stu-id="fa92f-121">Monday</span></span>
    
- <span data-ttu-id="fa92f-122">Martes</span><span class="sxs-lookup"><span data-stu-id="fa92f-122">Tuesday</span></span>
    
- <span data-ttu-id="fa92f-123">Miércoles</span><span class="sxs-lookup"><span data-stu-id="fa92f-123">Wednesday</span></span>
    
- <span data-ttu-id="fa92f-124">Jueves</span><span class="sxs-lookup"><span data-stu-id="fa92f-124">Thursday</span></span>
    
- <span data-ttu-id="fa92f-125">Viernes</span><span class="sxs-lookup"><span data-stu-id="fa92f-125">Friday</span></span>
    
- <span data-ttu-id="fa92f-126">Sábado</span><span class="sxs-lookup"><span data-stu-id="fa92f-126">Saturday</span></span>
    
## <a name="remarks"></a><span data-ttu-id="fa92f-127">Notas</span><span class="sxs-lookup"><span data-stu-id="fa92f-127">Remarks</span></span>

<span data-ttu-id="fa92f-128">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda Exchange Web Services.This elemento fue introdujo en Exchange Server 2010 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="fa92f-128">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fa92f-129">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="fa92f-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fa92f-130">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="fa92f-130">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="fa92f-131">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="fa92f-131">Schema Name</span></span>  <br/> |<span data-ttu-id="fa92f-132">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="fa92f-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="fa92f-133">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="fa92f-133">Validation File</span></span>  <br/> |<span data-ttu-id="fa92f-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="fa92f-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="fa92f-135">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="fa92f-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="fa92f-136">False</span><span class="sxs-lookup"><span data-stu-id="fa92f-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fa92f-137">Ver también</span><span class="sxs-lookup"><span data-stu-id="fa92f-137">See also</span></span>



- [<span data-ttu-id="fa92f-138">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="fa92f-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

