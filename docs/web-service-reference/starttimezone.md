---
title: StartTimeZone
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- StartTimeZone
api_type:
- schema
ms.assetid: d38c4dc1-4ecb-42a1-8d57-a451b16a2de2
description: El elemento StartTimeZone define la zona horaria de la hora de inicio de un CalendarItem o MeetingRequest.
ms.openlocfilehash: 6d21869c4b3be048db27dcc9f128fff868aebcb5
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19837559"
---
# <a name="starttimezone"></a><span data-ttu-id="7f546-103">StartTimeZone</span><span class="sxs-lookup"><span data-stu-id="7f546-103">StartTimeZone</span></span>

<span data-ttu-id="7f546-104">El elemento **StartTimeZone** define la zona horaria de la hora de inicio de un [CalendarItem](calendaritem.md) o [MeetingRequest](meetingrequest.md).</span><span class="sxs-lookup"><span data-stu-id="7f546-104">The **StartTimeZone** element defines the time zone for the start time of a [CalendarItem](calendaritem.md) or [MeetingRequest](meetingrequest.md).</span></span>
  
```xml
<StartTimeZone Id="" Name="">
   <Periods/>
   <TransitionsGroups/>
   <Transitions/>
</StartTimeZone>
```

<span data-ttu-id="7f546-105">**TimeZoneDefinitionType**</span><span class="sxs-lookup"><span data-stu-id="7f546-105">**TimeZoneDefinitionType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="7f546-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="7f546-106">Attributes and elements</span></span>

<span data-ttu-id="7f546-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="7f546-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7f546-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="7f546-108">Attributes</span></span>

|<span data-ttu-id="7f546-109">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="7f546-109">**Attribute**</span></span>|<span data-ttu-id="7f546-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7f546-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7f546-111">Id</span><span class="sxs-lookup"><span data-stu-id="7f546-111">Id</span></span>  <br/> |<span data-ttu-id="7f546-112">Representa el identificador único de la definición de zona horaria.</span><span class="sxs-lookup"><span data-stu-id="7f546-112">Represents the unique identifier of the time zone definition.</span></span>  <br/> |
|<span data-ttu-id="7f546-113">Nombre</span><span class="sxs-lookup"><span data-stu-id="7f546-113">Name</span></span>  <br/> |<span data-ttu-id="7f546-114">Representa el nombre descriptivo de la definición de zona horaria.</span><span class="sxs-lookup"><span data-stu-id="7f546-114">Represents the descriptive name of the time zone definition.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="7f546-115">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="7f546-115">Child elements</span></span>

|<span data-ttu-id="7f546-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="7f546-116">**Element**</span></span>|<span data-ttu-id="7f546-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7f546-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7f546-118">Períodos</span><span class="sxs-lookup"><span data-stu-id="7f546-118">Periods</span></span>](periods.md) <br/> |<span data-ttu-id="7f546-119">Representa una matriz de elementos de [período](period.md) que definen el desplazamiento de tiempo en diferentes fases de la zona horaria.</span><span class="sxs-lookup"><span data-stu-id="7f546-119">Represents an array of [Period](period.md) elements that define the time offset at different stages of the time zone.</span></span>  <br/> |
|[<span data-ttu-id="7f546-120">TransitionsGroups</span><span class="sxs-lookup"><span data-stu-id="7f546-120">TransitionsGroups</span></span>](transitionsgroups.md) <br/> |<span data-ttu-id="7f546-121">Representa una matriz de elementos de [TransitionsGroup](transitionsgroup.md) que especifican las transiciones de zona horaria.</span><span class="sxs-lookup"><span data-stu-id="7f546-121">Represents an array of [TransitionsGroup](transitionsgroup.md) elements that specify time zone transitions.</span></span>  <br/> |
|[<span data-ttu-id="7f546-122">Transiciones</span><span class="sxs-lookup"><span data-stu-id="7f546-122">Transitions</span></span>](transitions.md) <br/> |<span data-ttu-id="7f546-123">Representa una matriz de las transiciones de zona horaria.</span><span class="sxs-lookup"><span data-stu-id="7f546-123">Represents an array of time zone transitions.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="7f546-124">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="7f546-124">Parent elements</span></span>

|<span data-ttu-id="7f546-125">**Element**</span><span class="sxs-lookup"><span data-stu-id="7f546-125">**Element**</span></span>|<span data-ttu-id="7f546-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7f546-126">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7f546-127">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="7f546-127">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="7f546-128">Representa un elemento de calendario de Exchange.</span><span class="sxs-lookup"><span data-stu-id="7f546-128">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="7f546-129">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="7f546-129">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="7f546-130">Representa una convocatoria de reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="7f546-130">Represents a meeting request in the Exchange store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7f546-131">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7f546-131">Remarks</span></span>

<span data-ttu-id="7f546-132">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server que tiene instalada la función del servidor acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="7f546-132">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7f546-133">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="7f546-133">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7f546-134">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="7f546-134">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="7f546-135">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="7f546-135">Schema Name</span></span>  <br/> |<span data-ttu-id="7f546-136">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="7f546-136">Types schema</span></span>  <br/> |
|<span data-ttu-id="7f546-137">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="7f546-137">Validation File</span></span>  <br/> |<span data-ttu-id="7f546-138">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="7f546-138">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="7f546-139">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="7f546-139">Can be Empty</span></span>  <br/> |<span data-ttu-id="7f546-140">False</span><span class="sxs-lookup"><span data-stu-id="7f546-140">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7f546-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="7f546-141">See also</span></span>

- [<span data-ttu-id="7f546-142">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="7f546-142">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

