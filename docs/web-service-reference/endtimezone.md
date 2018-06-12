---
title: EndTimeZone
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- EndTimeZone
api_type:
- schema
ms.assetid: 6c53c337-be60-4d22-9e9e-a0c140c5e913
description: El elemento EndTimeZone define la zona horaria de la hora de finalización de un CalendarItem o MeetingRequest.
ms.openlocfilehash: 65eeedcc7c4d0e616ae54d4e2545fd310e9ad905
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764415"
---
# <a name="endtimezone"></a><span data-ttu-id="fbc93-103">EndTimeZone</span><span class="sxs-lookup"><span data-stu-id="fbc93-103">EndTimeZone</span></span>

<span data-ttu-id="fbc93-104">El elemento **EndTimeZone** define la zona horaria de la hora de finalización de un [CalendarItem](calendaritem.md) o [MeetingRequest](meetingrequest.md).</span><span class="sxs-lookup"><span data-stu-id="fbc93-104">The **EndTimeZone** element defines the time zone for the end time of a [CalendarItem](calendaritem.md) or [MeetingRequest](meetingrequest.md).</span></span>
  
```xml
<EndTimeZone Id="" Name="">
   <Periods/>
   <TransitionsGroups/>
   <Transitions/>
</EndTimeZone>
```

 <span data-ttu-id="fbc93-105">**TimeZoneDefinitionType**</span><span class="sxs-lookup"><span data-stu-id="fbc93-105">**TimeZoneDefinitionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="fbc93-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="fbc93-106">Attributes and elements</span></span>

<span data-ttu-id="fbc93-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="fbc93-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fbc93-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="fbc93-108">Attributes</span></span>

|<span data-ttu-id="fbc93-109">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="fbc93-109">**Attribute**</span></span>|<span data-ttu-id="fbc93-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="fbc93-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="fbc93-111">Id</span><span class="sxs-lookup"><span data-stu-id="fbc93-111">Id</span></span>  <br/> |<span data-ttu-id="fbc93-112">Representa el identificador único de la definición de zona horaria.</span><span class="sxs-lookup"><span data-stu-id="fbc93-112">Represents the unique identifier of the time zone definition.</span></span>  <br/> |
|<span data-ttu-id="fbc93-113">Nombre</span><span class="sxs-lookup"><span data-stu-id="fbc93-113">Name</span></span>  <br/> |<span data-ttu-id="fbc93-114">Representa el nombre descriptivo de la definición de zona horaria.</span><span class="sxs-lookup"><span data-stu-id="fbc93-114">Represents the descriptive name of the time zone definition.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="fbc93-115">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="fbc93-115">Child elements</span></span>

|<span data-ttu-id="fbc93-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="fbc93-116">**Element**</span></span>|<span data-ttu-id="fbc93-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="fbc93-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fbc93-118">Períodos</span><span class="sxs-lookup"><span data-stu-id="fbc93-118">Periods</span></span>](periods.md) <br/> |<span data-ttu-id="fbc93-119">Representa una matriz de elementos de [período](period.md) que definen el desplazamiento de tiempo en diferentes fases de la zona horaria.</span><span class="sxs-lookup"><span data-stu-id="fbc93-119">Represents an array of [Period](period.md) elements that define the time offset at different stages of the time zone.</span></span>  <br/> |
|[<span data-ttu-id="fbc93-120">TransitionsGroups</span><span class="sxs-lookup"><span data-stu-id="fbc93-120">TransitionsGroups</span></span>](transitionsgroups.md) <br/> |<span data-ttu-id="fbc93-121">Representa una matriz de elementos de [TransitionsGroup](transitionsgroup.md) que especifican las transiciones de zona horaria.</span><span class="sxs-lookup"><span data-stu-id="fbc93-121">Represents an array of [TransitionsGroup](transitionsgroup.md) elements that specify time zone transitions.</span></span>  <br/> |
|[<span data-ttu-id="fbc93-122">Transiciones</span><span class="sxs-lookup"><span data-stu-id="fbc93-122">Transitions</span></span>](transitions.md) <br/> |<span data-ttu-id="fbc93-123">Representa una matriz de las transiciones de zona horaria.</span><span class="sxs-lookup"><span data-stu-id="fbc93-123">Represents an array of time zone transitions.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="fbc93-124">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="fbc93-124">Parent elements</span></span>

|<span data-ttu-id="fbc93-125">**Element**</span><span class="sxs-lookup"><span data-stu-id="fbc93-125">**Element**</span></span>|<span data-ttu-id="fbc93-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="fbc93-126">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fbc93-127">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="fbc93-127">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="fbc93-128">Representa un elemento de calendario de Exchange.</span><span class="sxs-lookup"><span data-stu-id="fbc93-128">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="fbc93-129">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="fbc93-129">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="fbc93-130">Representa una convocatoria de reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="fbc93-130">Represents a meeting request in the Exchange store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fbc93-131">Notas</span><span class="sxs-lookup"><span data-stu-id="fbc93-131">Remarks</span></span>

<span data-ttu-id="fbc93-132">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server que tiene instalada la función del servidor acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="fbc93-132">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fbc93-133">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="fbc93-133">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fbc93-134">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="fbc93-134">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="fbc93-135">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="fbc93-135">Schema Name</span></span>  <br/> |<span data-ttu-id="fbc93-136">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="fbc93-136">Types schema</span></span>  <br/> |
|<span data-ttu-id="fbc93-137">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="fbc93-137">Validation File</span></span>  <br/> |<span data-ttu-id="fbc93-138">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="fbc93-138">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="fbc93-139">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="fbc93-139">Can be Empty</span></span>  <br/> |<span data-ttu-id="fbc93-140">False</span><span class="sxs-lookup"><span data-stu-id="fbc93-140">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fbc93-141">Ver también</span><span class="sxs-lookup"><span data-stu-id="fbc93-141">See also</span></span>



- [<span data-ttu-id="fbc93-142">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="fbc93-142">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

