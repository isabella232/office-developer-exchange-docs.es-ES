---
title: Horario de verano
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Daylight
api_type:
- schema
ms.assetid: ea400839-fba8-4a5e-a5d1-9b677afc0ff9
description: El elemento de horario de verano representa la fecha y hora en que cambia el tiempo de la hora estándar al horario de verano.
ms.openlocfilehash: cdb6ed305f1d77a73b952f8c659991f3b2a8df7a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764047"
---
# <a name="daylight"></a><span data-ttu-id="77d3b-103">Horario de verano</span><span class="sxs-lookup"><span data-stu-id="77d3b-103">Daylight</span></span>

<span data-ttu-id="77d3b-104">El elemento de **horario de verano** representa la fecha y hora en que cambia el tiempo de la hora estándar al horario de verano.</span><span class="sxs-lookup"><span data-stu-id="77d3b-104">The **Daylight** element represents the date and time when the time changes from standard time to daylight saving time.</span></span> 
  
```xml
<Daylight TimeZoneName="">
   <Offset/>
   <RelativeYearlyRecurrence/>
   <Time/>
</Daylight>
```

```xml
<Daylight TimeZoneName="">
   <Offset/>
   <AbsoluteDate/>
   <Time/>
</Daylight>
```

<span data-ttu-id="77d3b-105">**TimeChangeType**</span><span class="sxs-lookup"><span data-stu-id="77d3b-105">**TimeChangeType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="77d3b-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="77d3b-106">Attributes and elements</span></span>

<span data-ttu-id="77d3b-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="77d3b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="77d3b-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="77d3b-108">Attributes</span></span>

|<span data-ttu-id="77d3b-109">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="77d3b-109">**Attribute**</span></span>|<span data-ttu-id="77d3b-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="77d3b-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="77d3b-111">**TimeZoneName**</span><span class="sxs-lookup"><span data-stu-id="77d3b-111">**TimeZoneName**</span></span> <br/> |<span data-ttu-id="77d3b-112">Describe el nombre de la zona horaria.</span><span class="sxs-lookup"><span data-stu-id="77d3b-112">Describes the name of the time zone.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="77d3b-113">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="77d3b-113">Child elements</span></span>

|<span data-ttu-id="77d3b-114">**Element**</span><span class="sxs-lookup"><span data-stu-id="77d3b-114">**Element**</span></span>|<span data-ttu-id="77d3b-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="77d3b-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="77d3b-116">Offset</span><span class="sxs-lookup"><span data-stu-id="77d3b-116">Offset</span></span>](offset.md) <br/> |<span data-ttu-id="77d3b-117">Describe el desplazamiento desde el [BaseOffset](baseoffset.md).</span><span class="sxs-lookup"><span data-stu-id="77d3b-117">Describes the offset from the [BaseOffset](baseoffset.md).</span></span> <span data-ttu-id="77d3b-118">La base de desplazamiento además de este desplazamiento identifica la hora según si es estándar o de horario de verano.</span><span class="sxs-lookup"><span data-stu-id="77d3b-118">The base offset in addition to this offset identifies the time according to whether it is standard or daylight saving time.</span></span>  <br/> |
|[<span data-ttu-id="77d3b-119">RelativeYearlyRecurrence</span><span class="sxs-lookup"><span data-stu-id="77d3b-119">RelativeYearlyRecurrence</span></span>](relativeyearlyrecurrence.md) <br/> |<span data-ttu-id="77d3b-120">Describe un patrón de periodicidad anual relativa para un modelo de fecha de transición de zona horaria.</span><span class="sxs-lookup"><span data-stu-id="77d3b-120">Describes a relative yearly recurrence pattern for a time zone transition date pattern.</span></span>  <br/> |
|[<span data-ttu-id="77d3b-121">AbsoluteDate</span><span class="sxs-lookup"><span data-stu-id="77d3b-121">AbsoluteDate</span></span>](absolutedate.md) <br/> |<span data-ttu-id="77d3b-122">Representa la fecha cuando se cambia la hora del estándar o de horario de verano.</span><span class="sxs-lookup"><span data-stu-id="77d3b-122">Represents the date when the time changes from standard or daylight saving time.</span></span>  <br/> |
|[<span data-ttu-id="77d3b-123">Tiempo (TimeChangeType)</span><span class="sxs-lookup"><span data-stu-id="77d3b-123">Time (TimeChangeType)</span></span>](time-timechangetype.md) <br/> |<span data-ttu-id="77d3b-124">Describe la hora cuando se cambia el tiempo entre la hora estándar y el horario de verano.</span><span class="sxs-lookup"><span data-stu-id="77d3b-124">Describes the time when the time changes between standard time and daylight saving time.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="77d3b-125">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="77d3b-125">Parent elements</span></span>

|<span data-ttu-id="77d3b-126">**Element**</span><span class="sxs-lookup"><span data-stu-id="77d3b-126">**Element**</span></span>|<span data-ttu-id="77d3b-127">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="77d3b-127">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="77d3b-128">MeetingTimeZone</span><span class="sxs-lookup"><span data-stu-id="77d3b-128">MeetingTimeZone</span></span>](meetingtimezone.md) <br/> |<span data-ttu-id="77d3b-129">Representa la zona horaria de la ubicación donde se hospeda la reunión.</span><span class="sxs-lookup"><span data-stu-id="77d3b-129">Represents the time zone of the location where the meeting is hosted.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="77d3b-130">Notas</span><span class="sxs-lookup"><span data-stu-id="77d3b-130">Remarks</span></span>

<span data-ttu-id="77d3b-131">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="77d3b-131">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="77d3b-132">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="77d3b-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="77d3b-133">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="77d3b-133">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="77d3b-134">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="77d3b-134">Schema Name</span></span>  <br/> |<span data-ttu-id="77d3b-135">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="77d3b-135">Types schema</span></span>  <br/> |
|<span data-ttu-id="77d3b-136">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="77d3b-136">Validation File</span></span>  <br/> |<span data-ttu-id="77d3b-137">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="77d3b-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="77d3b-138">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="77d3b-138">Can be Empty</span></span>  <br/> |<span data-ttu-id="77d3b-139">False</span><span class="sxs-lookup"><span data-stu-id="77d3b-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="77d3b-140">Ver también</span><span class="sxs-lookup"><span data-stu-id="77d3b-140">See also</span></span>

- [<span data-ttu-id="77d3b-141">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="77d3b-141">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

