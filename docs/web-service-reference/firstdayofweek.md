---
title: Primerdíadelasemana
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
description: El elemento FirstDayOfWeek especifica el primer día de la semana.
ms.openlocfilehash: 1b4aee8e1ce2548cd6b0047623b0bcda47ad316b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530975"
---
# <a name="firstdayofweek"></a><span data-ttu-id="a6646-103">Primerdíadelasemana</span><span class="sxs-lookup"><span data-stu-id="a6646-103">FirstDayOfWeek</span></span>

<span data-ttu-id="a6646-104">El elemento **FirstDayOfWeek** especifica el primer día de la semana.</span><span class="sxs-lookup"><span data-stu-id="a6646-104">The **FirstDayOfWeek** element specifies the first day of the week.</span></span> 
  
```XML
<FirstDayOfWeek> Sunday | Monday | Tuesday | Wednesday | Thursday | Friday | Saturday</FirstDayOfWeek>
```

 <span data-ttu-id="a6646-105">**DayOfWeekType**</span><span class="sxs-lookup"><span data-stu-id="a6646-105">**DayOfWeekType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a6646-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="a6646-106">Attributes and elements</span></span>

<span data-ttu-id="a6646-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="a6646-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a6646-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="a6646-108">Attributes</span></span>

<span data-ttu-id="a6646-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="a6646-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a6646-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="a6646-110">Child elements</span></span>

<span data-ttu-id="a6646-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="a6646-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="a6646-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="a6646-112">Parent elements</span></span>

|<span data-ttu-id="a6646-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="a6646-113">**Element**</span></span>|<span data-ttu-id="a6646-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a6646-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a6646-115">WeeklyRecurrence</span><span class="sxs-lookup"><span data-stu-id="a6646-115">WeeklyRecurrence</span></span>](weeklyrecurrence.md) <br/> |<span data-ttu-id="a6646-116">Describe un patrón de periodicidad semanal.</span><span class="sxs-lookup"><span data-stu-id="a6646-116">Describes a weekly recurrence pattern.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="a6646-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="a6646-117">Text value</span></span>

<span data-ttu-id="a6646-118">El valor de texto del elemento **FirstDayOfWeek** indica el día de la semana que se utiliza como primer día de la semana.</span><span class="sxs-lookup"><span data-stu-id="a6646-118">The text value of the **FirstDayOfWeek** element indicates which day of the week is used as the first day of the week.</span></span> <span data-ttu-id="a6646-119">A continuación se muestran los valores de texto posibles:</span><span class="sxs-lookup"><span data-stu-id="a6646-119">The following are the possible text values:</span></span> 
  
- <span data-ttu-id="a6646-120">Domingo</span><span class="sxs-lookup"><span data-stu-id="a6646-120">Sunday</span></span>
    
- <span data-ttu-id="a6646-121">lunes</span><span class="sxs-lookup"><span data-stu-id="a6646-121">Monday</span></span>
    
- <span data-ttu-id="a6646-122">martes</span><span class="sxs-lookup"><span data-stu-id="a6646-122">Tuesday</span></span>
    
- <span data-ttu-id="a6646-123">miércoles</span><span class="sxs-lookup"><span data-stu-id="a6646-123">Wednesday</span></span>
    
- <span data-ttu-id="a6646-124">jueves</span><span class="sxs-lookup"><span data-stu-id="a6646-124">Thursday</span></span>
    
- <span data-ttu-id="a6646-125">viernes</span><span class="sxs-lookup"><span data-stu-id="a6646-125">Friday</span></span>
    
- <span data-ttu-id="a6646-126">Sábado</span><span class="sxs-lookup"><span data-stu-id="a6646-126">Saturday</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a6646-127">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a6646-127">Remarks</span></span>

<span data-ttu-id="a6646-128">El esquema que describe este elemento se encuentra en el directorio virtual de IIS que hospeda los servicios Web de Exchange. este elemento se introdujo en Exchange Server 2010 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="a6646-128">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a6646-129">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="a6646-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a6646-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="a6646-130">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a6646-131">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="a6646-131">Schema Name</span></span>  <br/> |<span data-ttu-id="a6646-132">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="a6646-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="a6646-133">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="a6646-133">Validation File</span></span>  <br/> |<span data-ttu-id="a6646-134">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="a6646-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="a6646-135">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="a6646-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="a6646-136">Falso</span><span class="sxs-lookup"><span data-stu-id="a6646-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a6646-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="a6646-137">See also</span></span>



- [<span data-ttu-id="a6646-138">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="a6646-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

