---
title: Horario
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
description: El elemento diurna representa la fecha y hora cuando cambia la hora estándar al horario de verano.
ms.openlocfilehash: bf2041cb4677f837ddb5b399041f1c19a7b5f577
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457462"
---
# <a name="daylight"></a><span data-ttu-id="8109f-103">Horario</span><span class="sxs-lookup"><span data-stu-id="8109f-103">Daylight</span></span>

<span data-ttu-id="8109f-104">El elemento **diurna** representa la fecha y hora cuando cambia la hora estándar al horario de verano.</span><span class="sxs-lookup"><span data-stu-id="8109f-104">The **Daylight** element represents the date and time when the time changes from standard time to daylight saving time.</span></span> 
  
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

<span data-ttu-id="8109f-105">**TimeChangeType**</span><span class="sxs-lookup"><span data-stu-id="8109f-105">**TimeChangeType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="8109f-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="8109f-106">Attributes and elements</span></span>

<span data-ttu-id="8109f-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="8109f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8109f-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="8109f-108">Attributes</span></span>

|<span data-ttu-id="8109f-109">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="8109f-109">**Attribute**</span></span>|<span data-ttu-id="8109f-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8109f-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8109f-111">**TimeZoneName**</span><span class="sxs-lookup"><span data-stu-id="8109f-111">**TimeZoneName**</span></span> <br/> |<span data-ttu-id="8109f-112">Describe el nombre de la zona horaria.</span><span class="sxs-lookup"><span data-stu-id="8109f-112">Describes the name of the time zone.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="8109f-113">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="8109f-113">Child elements</span></span>

|<span data-ttu-id="8109f-114">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="8109f-114">**Element**</span></span>|<span data-ttu-id="8109f-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8109f-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8109f-116">Offset</span><span class="sxs-lookup"><span data-stu-id="8109f-116">Offset</span></span>](offset.md) <br/> |<span data-ttu-id="8109f-117">Describe el desplazamiento desde [BaseOffset](baseoffset.md).</span><span class="sxs-lookup"><span data-stu-id="8109f-117">Describes the offset from the [BaseOffset](baseoffset.md).</span></span> <span data-ttu-id="8109f-118">El desplazamiento base, además de este desplazamiento, identifica el tiempo según si es estándar o el horario de verano.</span><span class="sxs-lookup"><span data-stu-id="8109f-118">The base offset in addition to this offset identifies the time according to whether it is standard or daylight saving time.</span></span>  <br/> |
|[<span data-ttu-id="8109f-119">RelativeYearlyRecurrence</span><span class="sxs-lookup"><span data-stu-id="8109f-119">RelativeYearlyRecurrence</span></span>](relativeyearlyrecurrence.md) <br/> |<span data-ttu-id="8109f-120">Describe un patrón de periodicidad anual relativo para un patrón de fecha de transición de zona horaria.</span><span class="sxs-lookup"><span data-stu-id="8109f-120">Describes a relative yearly recurrence pattern for a time zone transition date pattern.</span></span>  <br/> |
|[<span data-ttu-id="8109f-121">AbsoluteDate</span><span class="sxs-lookup"><span data-stu-id="8109f-121">AbsoluteDate</span></span>](absolutedate.md) <br/> |<span data-ttu-id="8109f-122">Representa la fecha en que cambia el horario estándar o el horario de verano.</span><span class="sxs-lookup"><span data-stu-id="8109f-122">Represents the date when the time changes from standard or daylight saving time.</span></span>  <br/> |
|[<span data-ttu-id="8109f-123">Hora (TimeChangeType)</span><span class="sxs-lookup"><span data-stu-id="8109f-123">Time (TimeChangeType)</span></span>](time-timechangetype.md) <br/> |<span data-ttu-id="8109f-124">Describe el momento en que cambia el tiempo entre el horario estándar y el horario de verano.</span><span class="sxs-lookup"><span data-stu-id="8109f-124">Describes the time when the time changes between standard time and daylight saving time.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="8109f-125">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="8109f-125">Parent elements</span></span>

|<span data-ttu-id="8109f-126">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="8109f-126">**Element**</span></span>|<span data-ttu-id="8109f-127">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8109f-127">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8109f-128">MeetingTimeZone</span><span class="sxs-lookup"><span data-stu-id="8109f-128">MeetingTimeZone</span></span>](meetingtimezone.md) <br/> |<span data-ttu-id="8109f-129">Representa la zona horaria de la ubicación donde se hospeda la reunión.</span><span class="sxs-lookup"><span data-stu-id="8109f-129">Represents the time zone of the location where the meeting is hosted.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8109f-130">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8109f-130">Remarks</span></span>

<span data-ttu-id="8109f-131">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="8109f-131">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8109f-132">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="8109f-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8109f-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="8109f-133">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="8109f-134">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="8109f-134">Schema Name</span></span>  <br/> |<span data-ttu-id="8109f-135">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="8109f-135">Types schema</span></span>  <br/> |
|<span data-ttu-id="8109f-136">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="8109f-136">Validation File</span></span>  <br/> |<span data-ttu-id="8109f-137">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="8109f-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="8109f-138">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="8109f-138">Can be Empty</span></span>  <br/> |<span data-ttu-id="8109f-139">Falso</span><span class="sxs-lookup"><span data-stu-id="8109f-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8109f-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="8109f-140">See also</span></span>

- [<span data-ttu-id="8109f-141">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="8109f-141">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

