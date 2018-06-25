---
title: Estándar
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Standard
api_type:
- schema
ms.assetid: d598f0a6-e296-423f-8ce5-3da57cfd8189
description: El elemento estándar representa la fecha y hora cuando se cambia la hora del horario de verano a la hora estándar.
ms.openlocfilehash: 1c9be4cf35773583078bc8e16ddf44433d3ad98c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19837536"
---
# <a name="standard"></a><span data-ttu-id="5d5f4-103">Estándar</span><span class="sxs-lookup"><span data-stu-id="5d5f4-103">Standard</span></span>

<span data-ttu-id="5d5f4-104">El elemento **estándar** representa la fecha y hora cuando se cambia la hora del horario de verano a la hora estándar.</span><span class="sxs-lookup"><span data-stu-id="5d5f4-104">The **Standard** element represents the date and time when the time changes from daylight saving time to standard time.</span></span> 
  
```xml
<Standard TimeZoneName="">
   <Offset/>
   <RelativeYearlyRecurrence/>
   <Time/>
</Standard>
```

 <span data-ttu-id="5d5f4-105">**TimeChangeType**</span><span class="sxs-lookup"><span data-stu-id="5d5f4-105">**TimeChangeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="5d5f4-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="5d5f4-106">Attributes and elements</span></span>

<span data-ttu-id="5d5f4-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="5d5f4-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5d5f4-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="5d5f4-108">Attributes</span></span>

|<span data-ttu-id="5d5f4-109">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="5d5f4-109">**Attribute**</span></span>|<span data-ttu-id="5d5f4-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5d5f4-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5d5f4-111">**TimeZoneName**</span><span class="sxs-lookup"><span data-stu-id="5d5f4-111">**TimeZoneName**</span></span> <br/> |<span data-ttu-id="5d5f4-112">Describe el nombre de la zona horaria.</span><span class="sxs-lookup"><span data-stu-id="5d5f4-112">Describes the name of the time zone.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="5d5f4-113">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="5d5f4-113">Child elements</span></span>

|<span data-ttu-id="5d5f4-114">**Element**</span><span class="sxs-lookup"><span data-stu-id="5d5f4-114">**Element**</span></span>|<span data-ttu-id="5d5f4-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5d5f4-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5d5f4-116">Offset</span><span class="sxs-lookup"><span data-stu-id="5d5f4-116">Offset</span></span>](offset.md) <br/> |<span data-ttu-id="5d5f4-117">Describe el desplazamiento desde el [BaseOffset](baseoffset.md).</span><span class="sxs-lookup"><span data-stu-id="5d5f4-117">Describes the offset from the [BaseOffset](baseoffset.md).</span></span> <span data-ttu-id="5d5f4-118">Junto con el elemento **BaseOffset** , el elemento de **desplazamiento** identifica si el tiempo es la hora estándar o el horario de verano.</span><span class="sxs-lookup"><span data-stu-id="5d5f4-118">Together with the **BaseOffset** element, the **Offset** element identifies whether the time is standard time or daylight saving time.</span></span>  <br/> |
|[<span data-ttu-id="5d5f4-119">RelativeYearlyRecurrence</span><span class="sxs-lookup"><span data-stu-id="5d5f4-119">RelativeYearlyRecurrence</span></span>](relativeyearlyrecurrence.md) <br/> |<span data-ttu-id="5d5f4-120">Describe un patrón de periodicidad anual relativa para una fecha de transición de la zona horaria.</span><span class="sxs-lookup"><span data-stu-id="5d5f4-120">Describes a relative yearly recurrence pattern for a time zone transition date.</span></span>  <br/> |
|[<span data-ttu-id="5d5f4-121">AbsoluteDate</span><span class="sxs-lookup"><span data-stu-id="5d5f4-121">AbsoluteDate</span></span>](absolutedate.md) <br/> |<span data-ttu-id="5d5f4-122">Representa la fecha cuando se cambia el tiempo de hora estándar o el horario de verano.</span><span class="sxs-lookup"><span data-stu-id="5d5f4-122">Represents the date when the time changes from standard time or daylight saving time.</span></span>  <br/> |
|[<span data-ttu-id="5d5f4-123">Tiempo (TimeChangeType)</span><span class="sxs-lookup"><span data-stu-id="5d5f4-123">Time (TimeChangeType)</span></span>](time-timechangetype.md) <br/> |<span data-ttu-id="5d5f4-124">Describe la hora cuando se cambia el tiempo entre la hora estándar y el horario de verano.</span><span class="sxs-lookup"><span data-stu-id="5d5f4-124">Describes the time when the time changes between standard time and daylight saving time.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="5d5f4-125">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="5d5f4-125">Parent elements</span></span>

|<span data-ttu-id="5d5f4-126">**Element**</span><span class="sxs-lookup"><span data-stu-id="5d5f4-126">**Element**</span></span>|<span data-ttu-id="5d5f4-127">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5d5f4-127">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5d5f4-128">MeetingTimeZone</span><span class="sxs-lookup"><span data-stu-id="5d5f4-128">MeetingTimeZone</span></span>](meetingtimezone.md) <br/> |<span data-ttu-id="5d5f4-129">Representa la zona horaria de la ubicación donde se hospeda la reunión.</span><span class="sxs-lookup"><span data-stu-id="5d5f4-129">Represents the time zone of the location where the meeting is hosted.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5d5f4-130">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5d5f4-130">Remarks</span></span>

<span data-ttu-id="5d5f4-131">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="5d5f4-131">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5d5f4-132">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="5d5f4-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5d5f4-133">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="5d5f4-133">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="5d5f4-134">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="5d5f4-134">Schema Name</span></span>  <br/> |<span data-ttu-id="5d5f4-135">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="5d5f4-135">Types schema</span></span>  <br/> |
|<span data-ttu-id="5d5f4-136">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="5d5f4-136">Validation File</span></span>  <br/> |<span data-ttu-id="5d5f4-137">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="5d5f4-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="5d5f4-138">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="5d5f4-138">Can be Empty</span></span>  <br/> |<span data-ttu-id="5d5f4-139">False</span><span class="sxs-lookup"><span data-stu-id="5d5f4-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5d5f4-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="5d5f4-140">See also</span></span>



- [<span data-ttu-id="5d5f4-141">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="5d5f4-141">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

