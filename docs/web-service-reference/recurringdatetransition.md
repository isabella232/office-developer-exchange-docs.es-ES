---
title: RecurringDateTransition
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RecurringDateTransition
api_type:
- schema
ms.assetid: 52fe1e05-3c50-40a1-8752-5c3c64c9f1ed
description: El elemento RecurringDateTransition representa una transición de la zona horaria que se produce en una fecha específica de cada año.
ms.openlocfilehash: 7cd8f3452a744e0c9a98fd3698dffb9ed8721a6c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19837014"
---
# <a name="recurringdatetransition"></a><span data-ttu-id="2a3ec-103">RecurringDateTransition</span><span class="sxs-lookup"><span data-stu-id="2a3ec-103">RecurringDateTransition</span></span>

<span data-ttu-id="2a3ec-104">El elemento **RecurringDateTransition** representa una transición de la zona horaria que se produce en una fecha específica de cada año.</span><span class="sxs-lookup"><span data-stu-id="2a3ec-104">The **RecurringDateTransition** element represents a time zone transition that occurs on a specific date each year.</span></span> 
  
```xml
<RecurringDateTransition>
   <To/>
   <TimeOffset/>
   <Month/>
   <Day/>
</RecurringDateTransition>
```

 <span data-ttu-id="2a3ec-105">**RecurringDateTransitionType**</span><span class="sxs-lookup"><span data-stu-id="2a3ec-105">**RecurringDateTransitionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2a3ec-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="2a3ec-106">Attributes and elements</span></span>

<span data-ttu-id="2a3ec-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="2a3ec-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2a3ec-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="2a3ec-108">Attributes</span></span>

<span data-ttu-id="2a3ec-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="2a3ec-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2a3ec-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="2a3ec-110">Child elements</span></span>

|<span data-ttu-id="2a3ec-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="2a3ec-111">**Element**</span></span>|<span data-ttu-id="2a3ec-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2a3ec-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2a3ec-113">To</span><span class="sxs-lookup"><span data-stu-id="2a3ec-113">To</span></span>](to.md) <br/> |<span data-ttu-id="2a3ec-114">Especifica el [período](period.md) o [TransitionsGroup](transitionsgroup.md) que es el destino de la transición de la zona horaria.</span><span class="sxs-lookup"><span data-stu-id="2a3ec-114">Specifies the [Period](period.md) or [TransitionsGroup](transitionsgroup.md) that is the target of the time zone transition.</span></span>  <br/> |
|[<span data-ttu-id="2a3ec-115">TimeOffset</span><span class="sxs-lookup"><span data-stu-id="2a3ec-115">TimeOffset</span></span>](timeoffset.md) <br/> |<span data-ttu-id="2a3ec-116">Representa el desplazamiento de la duración de la hora Universal coordinada (UTC) para la transición de la zona horaria.</span><span class="sxs-lookup"><span data-stu-id="2a3ec-116">Represents the duration offset from Coordinated Universal Time (UTC) for the time zone transition.</span></span>  <br/> |
|[<span data-ttu-id="2a3ec-117">Mes (transición de la zona horaria)</span><span class="sxs-lookup"><span data-stu-id="2a3ec-117">Month (Time Zone Transition)</span></span>](month-time-zone-transition.md) <br/> |<span data-ttu-id="2a3ec-118">Representa el mes en el que se produce la transición de la zona horaria.</span><span class="sxs-lookup"><span data-stu-id="2a3ec-118">Represents the month in which the time zone transition occurs.</span></span>  <br/> |
|[<span data-ttu-id="2a3ec-119">Día</span><span class="sxs-lookup"><span data-stu-id="2a3ec-119">Day</span></span>](day.md) <br/> |<span data-ttu-id="2a3ec-120">Representa el día del mes en el que se produce la transición de la zona horaria.</span><span class="sxs-lookup"><span data-stu-id="2a3ec-120">Represents the day of the month on which the time zone transition occurs.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="2a3ec-121">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="2a3ec-121">Parent elements</span></span>

|<span data-ttu-id="2a3ec-122">**Element**</span><span class="sxs-lookup"><span data-stu-id="2a3ec-122">**Element**</span></span>|<span data-ttu-id="2a3ec-123">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2a3ec-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2a3ec-124">Transiciones</span><span class="sxs-lookup"><span data-stu-id="2a3ec-124">Transitions</span></span>](transitions.md) <br/> |<span data-ttu-id="2a3ec-125">Representa una colección de transiciones de zona horaria.</span><span class="sxs-lookup"><span data-stu-id="2a3ec-125">Represents a collection of time zone transitions.</span></span>  <br/> |
|[<span data-ttu-id="2a3ec-126">TransitionsGroup</span><span class="sxs-lookup"><span data-stu-id="2a3ec-126">TransitionsGroup</span></span>](transitionsgroup.md) <br/> |<span data-ttu-id="2a3ec-127">Representa una colección de transiciones de zona horaria.</span><span class="sxs-lookup"><span data-stu-id="2a3ec-127">Represents a collection of time zone transitions.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2a3ec-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2a3ec-128">Remarks</span></span>

<span data-ttu-id="2a3ec-129">Un ejemplo de una transición de la zona horaria que se puede representar en el elemento [RecurringDateTransition](recurringdatetransition.md) es una transición que se produce el 15 de marzo de cada año.</span><span class="sxs-lookup"><span data-stu-id="2a3ec-129">An example of a time zone transition that could be represented by the [RecurringDateTransition](recurringdatetransition.md) element is a transition that occurs on March 15 each year.</span></span> 
  
<span data-ttu-id="2a3ec-130">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server que tiene instalada la función del servidor acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="2a3ec-130">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2a3ec-131">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="2a3ec-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2a3ec-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="2a3ec-132">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="2a3ec-133">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="2a3ec-133">Schema Name</span></span>  <br/> |<span data-ttu-id="2a3ec-134">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="2a3ec-134">Types schema</span></span>  <br/> |
|<span data-ttu-id="2a3ec-135">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="2a3ec-135">Validation File</span></span>  <br/> |<span data-ttu-id="2a3ec-136">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="2a3ec-136">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="2a3ec-137">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="2a3ec-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="2a3ec-138">False</span><span class="sxs-lookup"><span data-stu-id="2a3ec-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2a3ec-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="2a3ec-139">See also</span></span>



- [<span data-ttu-id="2a3ec-140">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="2a3ec-140">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

