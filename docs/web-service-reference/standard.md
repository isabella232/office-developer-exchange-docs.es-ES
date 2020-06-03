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
description: El elemento estándar representa la fecha y hora cuando cambia el horario de verano a la hora estándar.
ms.openlocfilehash: 1214a1debb53c9a31ca7c92a0c9e5c0722960d75
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467567"
---
# <a name="standard"></a><span data-ttu-id="c2ecc-103">Estándar</span><span class="sxs-lookup"><span data-stu-id="c2ecc-103">Standard</span></span>

<span data-ttu-id="c2ecc-104">El elemento **estándar** representa la fecha y hora cuando cambia el horario de verano a la hora estándar.</span><span class="sxs-lookup"><span data-stu-id="c2ecc-104">The **Standard** element represents the date and time when the time changes from daylight saving time to standard time.</span></span> 
  
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

<span data-ttu-id="c2ecc-105">**TimeChangeType**</span><span class="sxs-lookup"><span data-stu-id="c2ecc-105">**TimeChangeType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="c2ecc-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="c2ecc-106">Attributes and elements</span></span>

<span data-ttu-id="c2ecc-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="c2ecc-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c2ecc-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="c2ecc-108">Attributes</span></span>

|<span data-ttu-id="c2ecc-109">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="c2ecc-109">**Attribute**</span></span>|<span data-ttu-id="c2ecc-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c2ecc-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c2ecc-111">**TimeZoneName**</span><span class="sxs-lookup"><span data-stu-id="c2ecc-111">**TimeZoneName**</span></span> <br/> |<span data-ttu-id="c2ecc-112">Describe el nombre de la zona horaria.</span><span class="sxs-lookup"><span data-stu-id="c2ecc-112">Describes the name of the time zone.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="c2ecc-113">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c2ecc-113">Child elements</span></span>

|<span data-ttu-id="c2ecc-114">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="c2ecc-114">**Element**</span></span>|<span data-ttu-id="c2ecc-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c2ecc-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c2ecc-116">Offset</span><span class="sxs-lookup"><span data-stu-id="c2ecc-116">Offset</span></span>](offset.md) <br/> |<span data-ttu-id="c2ecc-117">Describe el desplazamiento desde [BaseOffset](baseoffset.md).</span><span class="sxs-lookup"><span data-stu-id="c2ecc-117">Describes the offset from the [BaseOffset](baseoffset.md).</span></span> <span data-ttu-id="c2ecc-118">Junto con el elemento **BaseOffset** , el elemento **offset** identifica si la hora es estándar o el horario de verano.</span><span class="sxs-lookup"><span data-stu-id="c2ecc-118">Together with the **BaseOffset** element, the **Offset** element identifies whether the time is standard time or daylight saving time.</span></span>  <br/> |
|[<span data-ttu-id="c2ecc-119">RelativeYearlyRecurrence</span><span class="sxs-lookup"><span data-stu-id="c2ecc-119">RelativeYearlyRecurrence</span></span>](relativeyearlyrecurrence.md) <br/> |<span data-ttu-id="c2ecc-120">Describe un patrón de periodicidad anual relativo para una fecha de transición de zona horaria.</span><span class="sxs-lookup"><span data-stu-id="c2ecc-120">Describes a relative yearly recurrence pattern for a time zone transition date.</span></span>  <br/> |
|[<span data-ttu-id="c2ecc-121">AbsoluteDate</span><span class="sxs-lookup"><span data-stu-id="c2ecc-121">AbsoluteDate</span></span>](absolutedate.md) <br/> |<span data-ttu-id="c2ecc-122">Representa la fecha en que cambia el horario estándar o el horario de verano.</span><span class="sxs-lookup"><span data-stu-id="c2ecc-122">Represents the date when the time changes from standard time or daylight saving time.</span></span>  <br/> |
|[<span data-ttu-id="c2ecc-123">Hora (TimeChangeType)</span><span class="sxs-lookup"><span data-stu-id="c2ecc-123">Time (TimeChangeType)</span></span>](time-timechangetype.md) <br/> |<span data-ttu-id="c2ecc-124">Describe el momento en que cambia el tiempo entre el horario estándar y el horario de verano.</span><span class="sxs-lookup"><span data-stu-id="c2ecc-124">Describes the time when the time changes between standard time and daylight saving time.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="c2ecc-125">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="c2ecc-125">Parent elements</span></span>

|<span data-ttu-id="c2ecc-126">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="c2ecc-126">**Element**</span></span>|<span data-ttu-id="c2ecc-127">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c2ecc-127">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c2ecc-128">MeetingTimeZone</span><span class="sxs-lookup"><span data-stu-id="c2ecc-128">MeetingTimeZone</span></span>](meetingtimezone.md) <br/> |<span data-ttu-id="c2ecc-129">Representa la zona horaria de la ubicación donde se hospeda la reunión.</span><span class="sxs-lookup"><span data-stu-id="c2ecc-129">Represents the time zone of the location where the meeting is hosted.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c2ecc-130">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c2ecc-130">Remarks</span></span>

<span data-ttu-id="c2ecc-131">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="c2ecc-131">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c2ecc-132">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="c2ecc-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c2ecc-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="c2ecc-133">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c2ecc-134">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="c2ecc-134">Schema Name</span></span>  <br/> |<span data-ttu-id="c2ecc-135">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="c2ecc-135">Types schema</span></span>  <br/> |
|<span data-ttu-id="c2ecc-136">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="c2ecc-136">Validation File</span></span>  <br/> |<span data-ttu-id="c2ecc-137">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="c2ecc-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="c2ecc-138">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="c2ecc-138">Can be Empty</span></span>  <br/> |<span data-ttu-id="c2ecc-139">Falso</span><span class="sxs-lookup"><span data-stu-id="c2ecc-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c2ecc-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="c2ecc-140">See also</span></span>

- [<span data-ttu-id="c2ecc-141">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="c2ecc-141">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

