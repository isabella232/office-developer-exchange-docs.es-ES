---
title: Standard
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
ms.openlocfilehash: c121e959f243d982cfe50ed6b4ef39a82dae2cc8
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/28/2018
ms.locfileid: "21353437"
---
# <a name="standard"></a><span data-ttu-id="baab3-103">Standard</span><span class="sxs-lookup"><span data-stu-id="baab3-103">Standard</span></span>

<span data-ttu-id="baab3-104">El elemento **estándar** representa la fecha y hora cuando se cambia la hora del horario de verano a la hora estándar.</span><span class="sxs-lookup"><span data-stu-id="baab3-104">The **Standard** element represents the date and time when the time changes from daylight saving time to standard time.</span></span> 
  
```xml
<Standard TimeZoneName="">
   <Offset/>
   <RelativeYearlyRecurrence/>
   <Time/>
</Standard>
```

```xml
<Standard TimeZoneName="">
   <Offset/>
   <AbsoluteDate/>
   <Time/>
</Standard>
```

<span data-ttu-id="baab3-105">**TimeChangeType**</span><span class="sxs-lookup"><span data-stu-id="baab3-105">**TimeChangeType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="baab3-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="baab3-106">Attributes and elements</span></span>

<span data-ttu-id="baab3-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="baab3-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="baab3-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="baab3-108">Attributes</span></span>

|<span data-ttu-id="baab3-109">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="baab3-109">**Attribute**</span></span>|<span data-ttu-id="baab3-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="baab3-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="baab3-111">**TimeZoneName**</span><span class="sxs-lookup"><span data-stu-id="baab3-111">**TimeZoneName**</span></span> <br/> |<span data-ttu-id="baab3-112">Describe el nombre de la zona horaria.</span><span class="sxs-lookup"><span data-stu-id="baab3-112">Describes the name of the time zone.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="baab3-113">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="baab3-113">Child elements</span></span>

|<span data-ttu-id="baab3-114">**Element**</span><span class="sxs-lookup"><span data-stu-id="baab3-114">**Element**</span></span>|<span data-ttu-id="baab3-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="baab3-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="baab3-116">Offset</span><span class="sxs-lookup"><span data-stu-id="baab3-116">Offset</span></span>](offset.md) <br/> |<span data-ttu-id="baab3-117">Describe el desplazamiento desde el [BaseOffset](baseoffset.md).</span><span class="sxs-lookup"><span data-stu-id="baab3-117">Describes the offset from the [BaseOffset](baseoffset.md).</span></span> <span data-ttu-id="baab3-118">Junto con el elemento **BaseOffset** , el elemento de **desplazamiento** identifica si el tiempo es la hora estándar o el horario de verano.</span><span class="sxs-lookup"><span data-stu-id="baab3-118">Together with the **BaseOffset** element, the **Offset** element identifies whether the time is standard time or daylight saving time.</span></span>  <br/> |
|[<span data-ttu-id="baab3-119">RelativeYearlyRecurrence</span><span class="sxs-lookup"><span data-stu-id="baab3-119">RelativeYearlyRecurrence</span></span>](relativeyearlyrecurrence.md) <br/> |<span data-ttu-id="baab3-120">Describe un patrón de periodicidad anual relativa para una fecha de transición de la zona horaria.</span><span class="sxs-lookup"><span data-stu-id="baab3-120">Describes a relative yearly recurrence pattern for a time zone transition date.</span></span>  <br/> |
|[<span data-ttu-id="baab3-121">AbsoluteDate</span><span class="sxs-lookup"><span data-stu-id="baab3-121">AbsoluteDate</span></span>](absolutedate.md) <br/> |<span data-ttu-id="baab3-122">Representa la fecha cuando se cambia el tiempo de hora estándar o el horario de verano.</span><span class="sxs-lookup"><span data-stu-id="baab3-122">Represents the date when the time changes from standard time or daylight saving time.</span></span>  <br/> |
|[<span data-ttu-id="baab3-123">Time (TimeChangeType)</span><span class="sxs-lookup"><span data-stu-id="baab3-123">Time (TimeChangeType)</span></span>](time-timechangetype.md) <br/> |<span data-ttu-id="baab3-124">Describe la hora cuando se cambia el tiempo entre la hora estándar y el horario de verano.</span><span class="sxs-lookup"><span data-stu-id="baab3-124">Describes the time when the time changes between standard time and daylight saving time.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="baab3-125">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="baab3-125">Parent elements</span></span>

|<span data-ttu-id="baab3-126">**Element**</span><span class="sxs-lookup"><span data-stu-id="baab3-126">**Element**</span></span>|<span data-ttu-id="baab3-127">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="baab3-127">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="baab3-128">MeetingTimeZone</span><span class="sxs-lookup"><span data-stu-id="baab3-128">MeetingTimeZone</span></span>](meetingtimezone.md) <br/> |<span data-ttu-id="baab3-129">Representa la zona horaria de la ubicación donde se hospeda la reunión.</span><span class="sxs-lookup"><span data-stu-id="baab3-129">Represents the time zone of the location where the meeting is hosted.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="baab3-130">Comentarios</span><span class="sxs-lookup"><span data-stu-id="baab3-130">Remarks</span></span>

<span data-ttu-id="baab3-131">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="baab3-131">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="baab3-132">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="baab3-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="baab3-133">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="baab3-133">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="baab3-134">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="baab3-134">Schema Name</span></span>  <br/> |<span data-ttu-id="baab3-135">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="baab3-135">Types schema</span></span>  <br/> |
|<span data-ttu-id="baab3-136">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="baab3-136">Validation File</span></span>  <br/> |<span data-ttu-id="baab3-137">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="baab3-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="baab3-138">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="baab3-138">Can be Empty</span></span>  <br/> |<span data-ttu-id="baab3-139">False</span><span class="sxs-lookup"><span data-stu-id="baab3-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="baab3-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="baab3-140">See also</span></span>

- [<span data-ttu-id="baab3-141">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="baab3-141">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

