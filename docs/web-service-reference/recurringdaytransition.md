---
title: RecurringDayTransition
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RecurringDayTransition
api_type:
- schema
ms.assetid: 1ae28d14-c2b8-4084-9e76-e2e347a884ce
description: El elemento RecurringDayTransition representa una transición de zona horaria que se produce el mismo día cada año.
ms.openlocfilehash: 44c2a6ec4dbaaa52a2772cb5c35a84b14dd77f97
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468470"
---
# <a name="recurringdaytransition"></a><span data-ttu-id="1d0f4-103">RecurringDayTransition</span><span class="sxs-lookup"><span data-stu-id="1d0f4-103">RecurringDayTransition</span></span>

<span data-ttu-id="1d0f4-104">El elemento **RecurringDayTransition** representa una transición de zona horaria que se produce el mismo día cada año.</span><span class="sxs-lookup"><span data-stu-id="1d0f4-104">The **RecurringDayTransition** element represents a time zone transition that occurs on the same day each year.</span></span> 
  
```xml
<RecurringDayTransition>
   <To/>
   <TimeOffset/>
   <Month/>
   <DayOfWeek/>
   <Occurrence/>
</RecurringDayTransition>
```

 <span data-ttu-id="1d0f4-105">**RecurringDayTransitionType**</span><span class="sxs-lookup"><span data-stu-id="1d0f4-105">**RecurringDayTransitionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1d0f4-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="1d0f4-106">Attributes and elements</span></span>

<span data-ttu-id="1d0f4-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="1d0f4-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1d0f4-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="1d0f4-108">Attributes</span></span>

<span data-ttu-id="1d0f4-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="1d0f4-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1d0f4-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="1d0f4-110">Child elements</span></span>

|<span data-ttu-id="1d0f4-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="1d0f4-111">**Element**</span></span>|<span data-ttu-id="1d0f4-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1d0f4-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1d0f4-113">To</span><span class="sxs-lookup"><span data-stu-id="1d0f4-113">To</span></span>](to.md) <br/> |<span data-ttu-id="1d0f4-114">Especifica el [punto](period.md) o [TransitionsGroup](transitionsgroup.md) que es el destino de la transición de zona horaria.</span><span class="sxs-lookup"><span data-stu-id="1d0f4-114">Specifies the [Period](period.md) or [TransitionsGroup](transitionsgroup.md) that is the target of the time zone transition.</span></span>  <br/> |
|[<span data-ttu-id="1d0f4-115">TimeOffset</span><span class="sxs-lookup"><span data-stu-id="1d0f4-115">TimeOffset</span></span>](timeoffset.md) <br/> |<span data-ttu-id="1d0f4-116">Representa el desplazamiento de duración desde la hora universal coordinada (UTC) para la transición de zona horaria.</span><span class="sxs-lookup"><span data-stu-id="1d0f4-116">Represents the duration offset from Coordinated Universal Time (UTC) for the time zone transition.</span></span>  <br/> |
|[<span data-ttu-id="1d0f4-117">Mes (transición de zona horaria)</span><span class="sxs-lookup"><span data-stu-id="1d0f4-117">Month (Time Zone Transition)</span></span>](month-time-zone-transition.md) <br/> |<span data-ttu-id="1d0f4-118">Representa el mes en el que se produce la transición de zona horaria.</span><span class="sxs-lookup"><span data-stu-id="1d0f4-118">Represents the month in which the time zone transition occurs.</span></span>  <br/> |
|[<span data-ttu-id="1d0f4-119">DayOfWeek (TimeZone)</span><span class="sxs-lookup"><span data-stu-id="1d0f4-119">DayOfWeek (TimeZone)</span></span>](dayofweek-timezone.md) <br/> |<span data-ttu-id="1d0f4-120">Representa el día de la semana en el que se produce la transición de zona horaria.</span><span class="sxs-lookup"><span data-stu-id="1d0f4-120">Represents the day of the week on which the time zone transition occurs.</span></span>  <br/> |
|[<span data-ttu-id="1d0f4-121">Aparición (transición de zona horaria)</span><span class="sxs-lookup"><span data-stu-id="1d0f4-121">Occurrence (Time Zone Transition)</span></span>](occurrence-time-zone-transition.md) <br/> |<span data-ttu-id="1d0f4-122">Representa la ocurrencia del día de la semana del mes en que se produce la transición de zona horaria.</span><span class="sxs-lookup"><span data-stu-id="1d0f4-122">Represents the occurrence of the day of the week in the month that the time zone transition occurs.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="1d0f4-123">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="1d0f4-123">Parent elements</span></span>

|<span data-ttu-id="1d0f4-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="1d0f4-124">**Element**</span></span>|<span data-ttu-id="1d0f4-125">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1d0f4-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1d0f4-126">Transiciones</span><span class="sxs-lookup"><span data-stu-id="1d0f4-126">Transitions</span></span>](transitions.md) <br/> |<span data-ttu-id="1d0f4-127">Representa una colección de transiciones de zona horaria.</span><span class="sxs-lookup"><span data-stu-id="1d0f4-127">Represents a collection of time zone transitions.</span></span>  <br/> |
|[<span data-ttu-id="1d0f4-128">TransitionsGroup</span><span class="sxs-lookup"><span data-stu-id="1d0f4-128">TransitionsGroup</span></span>](transitionsgroup.md) <br/> |<span data-ttu-id="1d0f4-129">Representa una colección de transiciones de zona horaria.</span><span class="sxs-lookup"><span data-stu-id="1d0f4-129">Represents a collection of time zone transitions.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1d0f4-130">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1d0f4-130">Remarks</span></span>

<span data-ttu-id="1d0f4-131">Un ejemplo de una transición de zona horaria que podría representarse mediante el elemento [RecurringDayTransition](recurringdaytransition.md) es una transición que se produce el segundo martes de febrero de cada año.</span><span class="sxs-lookup"><span data-stu-id="1d0f4-131">An example of a time zone transition that could be represented by the [RecurringDayTransition](recurringdaytransition.md) element is a transition that occurs on the second Tuesday of February each year.</span></span> 
  
<span data-ttu-id="1d0f4-132">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="1d0f4-132">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1d0f4-133">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="1d0f4-133">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1d0f4-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="1d0f4-134">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="1d0f4-135">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="1d0f4-135">Schema Name</span></span>  <br/> |<span data-ttu-id="1d0f4-136">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="1d0f4-136">Types schema</span></span>  <br/> |
|<span data-ttu-id="1d0f4-137">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="1d0f4-137">Validation File</span></span>  <br/> |<span data-ttu-id="1d0f4-138">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="1d0f4-138">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="1d0f4-139">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="1d0f4-139">Can be Empty</span></span>  <br/> |<span data-ttu-id="1d0f4-140">Falso</span><span class="sxs-lookup"><span data-stu-id="1d0f4-140">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1d0f4-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="1d0f4-141">See also</span></span>



- [<span data-ttu-id="1d0f4-142">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="1d0f4-142">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

