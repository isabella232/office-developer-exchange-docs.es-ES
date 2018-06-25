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
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764047"
---
# <a name="daylight"></a><span data-ttu-id="4f2f9-103">Horario de verano</span><span class="sxs-lookup"><span data-stu-id="4f2f9-103">Daylight</span></span>

<span data-ttu-id="4f2f9-104">El elemento de **horario de verano** representa la fecha y hora en que cambia el tiempo de la hora estándar al horario de verano.</span><span class="sxs-lookup"><span data-stu-id="4f2f9-104">The **Daylight** element represents the date and time when the time changes from standard time to daylight saving time.</span></span> 
  
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

<span data-ttu-id="4f2f9-105">**TimeChangeType**</span><span class="sxs-lookup"><span data-stu-id="4f2f9-105">**TimeChangeType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="4f2f9-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="4f2f9-106">Attributes and elements</span></span>

<span data-ttu-id="4f2f9-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="4f2f9-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4f2f9-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="4f2f9-108">Attributes</span></span>

|<span data-ttu-id="4f2f9-109">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="4f2f9-109">**Attribute**</span></span>|<span data-ttu-id="4f2f9-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4f2f9-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4f2f9-111">**TimeZoneName**</span><span class="sxs-lookup"><span data-stu-id="4f2f9-111">**TimeZoneName**</span></span> <br/> |<span data-ttu-id="4f2f9-112">Describe el nombre de la zona horaria.</span><span class="sxs-lookup"><span data-stu-id="4f2f9-112">Describes the name of the time zone.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="4f2f9-113">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="4f2f9-113">Child elements</span></span>

|<span data-ttu-id="4f2f9-114">**Element**</span><span class="sxs-lookup"><span data-stu-id="4f2f9-114">**Element**</span></span>|<span data-ttu-id="4f2f9-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4f2f9-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4f2f9-116">Offset</span><span class="sxs-lookup"><span data-stu-id="4f2f9-116">Offset</span></span>](offset.md) <br/> |<span data-ttu-id="4f2f9-117">Describe el desplazamiento desde el [BaseOffset](baseoffset.md).</span><span class="sxs-lookup"><span data-stu-id="4f2f9-117">Describes the offset from the [BaseOffset](baseoffset.md).</span></span> <span data-ttu-id="4f2f9-118">La base de desplazamiento además de este desplazamiento identifica la hora según si es estándar o de horario de verano.</span><span class="sxs-lookup"><span data-stu-id="4f2f9-118">The base offset in addition to this offset identifies the time according to whether it is standard or daylight saving time.</span></span>  <br/> |
|[<span data-ttu-id="4f2f9-119">RelativeYearlyRecurrence</span><span class="sxs-lookup"><span data-stu-id="4f2f9-119">RelativeYearlyRecurrence</span></span>](relativeyearlyrecurrence.md) <br/> |<span data-ttu-id="4f2f9-120">Describe un patrón de periodicidad anual relativa para un modelo de fecha de transición de zona horaria.</span><span class="sxs-lookup"><span data-stu-id="4f2f9-120">Describes a relative yearly recurrence pattern for a time zone transition date pattern.</span></span>  <br/> |
|[<span data-ttu-id="4f2f9-121">AbsoluteDate</span><span class="sxs-lookup"><span data-stu-id="4f2f9-121">AbsoluteDate</span></span>](absolutedate.md) <br/> |<span data-ttu-id="4f2f9-122">Representa la fecha cuando se cambia la hora del estándar o de horario de verano.</span><span class="sxs-lookup"><span data-stu-id="4f2f9-122">Represents the date when the time changes from standard or daylight saving time.</span></span>  <br/> |
|[<span data-ttu-id="4f2f9-123">Tiempo (TimeChangeType)</span><span class="sxs-lookup"><span data-stu-id="4f2f9-123">Time (TimeChangeType)</span></span>](time-timechangetype.md) <br/> |<span data-ttu-id="4f2f9-124">Describe la hora cuando se cambia el tiempo entre la hora estándar y el horario de verano.</span><span class="sxs-lookup"><span data-stu-id="4f2f9-124">Describes the time when the time changes between standard time and daylight saving time.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="4f2f9-125">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="4f2f9-125">Parent elements</span></span>

|<span data-ttu-id="4f2f9-126">**Element**</span><span class="sxs-lookup"><span data-stu-id="4f2f9-126">**Element**</span></span>|<span data-ttu-id="4f2f9-127">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4f2f9-127">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4f2f9-128">MeetingTimeZone</span><span class="sxs-lookup"><span data-stu-id="4f2f9-128">MeetingTimeZone</span></span>](meetingtimezone.md) <br/> |<span data-ttu-id="4f2f9-129">Representa la zona horaria de la ubicación donde se hospeda la reunión.</span><span class="sxs-lookup"><span data-stu-id="4f2f9-129">Represents the time zone of the location where the meeting is hosted.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4f2f9-130">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4f2f9-130">Remarks</span></span>

<span data-ttu-id="4f2f9-131">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="4f2f9-131">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4f2f9-132">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="4f2f9-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4f2f9-133">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="4f2f9-133">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="4f2f9-134">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="4f2f9-134">Schema Name</span></span>  <br/> |<span data-ttu-id="4f2f9-135">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="4f2f9-135">Types schema</span></span>  <br/> |
|<span data-ttu-id="4f2f9-136">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="4f2f9-136">Validation File</span></span>  <br/> |<span data-ttu-id="4f2f9-137">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="4f2f9-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="4f2f9-138">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="4f2f9-138">Can be Empty</span></span>  <br/> |<span data-ttu-id="4f2f9-139">False</span><span class="sxs-lookup"><span data-stu-id="4f2f9-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4f2f9-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="4f2f9-140">See also</span></span>

- [<span data-ttu-id="4f2f9-141">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="4f2f9-141">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

