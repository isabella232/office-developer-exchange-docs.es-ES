---
title: MeetingTimeZone
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MeetingTimeZone
api_type:
- schema
ms.assetid: 413b47d9-8126-462c-9a4f-4e771a5e8889
description: El elemento MeetingTimeZone representa la zona horaria de la ubicación donde se hospeda la reunión.
ms.openlocfilehash: ce014ac6d8841e451927a94049cb4e8860886fdf
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836440"
---
# <a name="meetingtimezone"></a><span data-ttu-id="06c07-103">MeetingTimeZone</span><span class="sxs-lookup"><span data-stu-id="06c07-103">MeetingTimeZone</span></span>

<span data-ttu-id="06c07-104">El elemento **MeetingTimeZone** representa la zona horaria de la ubicación donde se hospeda la reunión.</span><span class="sxs-lookup"><span data-stu-id="06c07-104">The **MeetingTimeZone** element represents the time zone of the location where the meeting is hosted.</span></span> 
  
```xml
<MeetingTimeZone>
   <BaseOffset/>
   <Standard/>
   <Daylight/>
</MeetingTimeZone>
```

 <span data-ttu-id="06c07-105">**TimeZoneType**</span><span class="sxs-lookup"><span data-stu-id="06c07-105">**TimeZoneType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="06c07-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="06c07-106">Attributes and elements</span></span>

<span data-ttu-id="06c07-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="06c07-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="06c07-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="06c07-108">Attributes</span></span>

|<span data-ttu-id="06c07-109">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="06c07-109">**Attribute**</span></span>|<span data-ttu-id="06c07-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="06c07-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="06c07-111">**TimeZoneName**</span><span class="sxs-lookup"><span data-stu-id="06c07-111">**TimeZoneName**</span></span> <br/> |<span data-ttu-id="06c07-112">Describe el nombre de la zona horaria.</span><span class="sxs-lookup"><span data-stu-id="06c07-112">Describes the name of the time zone.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="06c07-113">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="06c07-113">Child elements</span></span>

|<span data-ttu-id="06c07-114">**Element**</span><span class="sxs-lookup"><span data-stu-id="06c07-114">**Element**</span></span>|<span data-ttu-id="06c07-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="06c07-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="06c07-116">BaseOffset</span><span class="sxs-lookup"><span data-stu-id="06c07-116">BaseOffset</span></span>](baseoffset.md) <br/> |<span data-ttu-id="06c07-117">Representa el hourly desplazamiento de la hora UTC de la zona horaria actual.</span><span class="sxs-lookup"><span data-stu-id="06c07-117">Represents the hourly offset from UTC for the current time zone.</span></span>  <br/> |
|[<span data-ttu-id="06c07-118">Standard</span><span class="sxs-lookup"><span data-stu-id="06c07-118">Standard</span></span>](standard.md) <br/> |<span data-ttu-id="06c07-119">Representa la fecha y hora cuando se cambia la hora del horario de verano a la hora estándar.</span><span class="sxs-lookup"><span data-stu-id="06c07-119">Represents the date and time when the time changes from daylight saving time to standard time.</span></span>  <br/> |
|[<span data-ttu-id="06c07-120">Horario de verano</span><span class="sxs-lookup"><span data-stu-id="06c07-120">Daylight</span></span>](daylight.md) <br/> |<span data-ttu-id="06c07-121">Representa la fecha y hora en que cambia el tiempo de la hora estándar al horario de verano.</span><span class="sxs-lookup"><span data-stu-id="06c07-121">Represents the date and time when the time changes from standard time to daylight saving time.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="06c07-122">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="06c07-122">Parent elements</span></span>

|<span data-ttu-id="06c07-123">**Element**</span><span class="sxs-lookup"><span data-stu-id="06c07-123">**Element**</span></span>|<span data-ttu-id="06c07-124">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="06c07-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="06c07-125">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="06c07-125">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="06c07-126">Representa un elemento de calendario de Exchange.</span><span class="sxs-lookup"><span data-stu-id="06c07-126">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="06c07-127">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="06c07-127">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="06c07-128">Representa una convocatoria de reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="06c07-128">Represents a meeting request in the Exchange store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="06c07-129">Notas</span><span class="sxs-lookup"><span data-stu-id="06c07-129">Remarks</span></span>

<span data-ttu-id="06c07-130">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="06c07-130">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="06c07-131">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="06c07-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="06c07-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="06c07-132">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="06c07-133">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="06c07-133">Schema Name</span></span>  <br/> |<span data-ttu-id="06c07-134">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="06c07-134">Types schema</span></span>  <br/> |
|<span data-ttu-id="06c07-135">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="06c07-135">Validation File</span></span>  <br/> |<span data-ttu-id="06c07-136">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="06c07-136">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="06c07-137">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="06c07-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="06c07-138">False</span><span class="sxs-lookup"><span data-stu-id="06c07-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="06c07-139">Ver también</span><span class="sxs-lookup"><span data-stu-id="06c07-139">See also</span></span>



- [<span data-ttu-id="06c07-140">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="06c07-140">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

