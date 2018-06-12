---
title: Períodos
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Periods
api_type:
- schema
ms.assetid: 7920d81d-abba-4232-8bfe-49267b6c9a36
description: El elemento de períodos representa una matriz de los períodos que definen el desplazamiento de tiempo en diferentes fases de la zona horaria.
ms.openlocfilehash: f2f9cf7c724b453d2b1975fcf72c55bc02caa54b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836729"
---
# <a name="periods"></a><span data-ttu-id="d5b31-103">Períodos</span><span class="sxs-lookup"><span data-stu-id="d5b31-103">Periods</span></span>

<span data-ttu-id="d5b31-104">El elemento de **períodos** representa una matriz de los períodos que definen el desplazamiento de tiempo en diferentes fases de la zona horaria.</span><span class="sxs-lookup"><span data-stu-id="d5b31-104">The **Periods** element represents an array of periods that define the time offset at different stages of the time zone.</span></span> 
  
```xml
<Periods>
   <Period/>
</Periods>
```

 <span data-ttu-id="d5b31-105">**NonEmptyArrayOfPeriodsType**</span><span class="sxs-lookup"><span data-stu-id="d5b31-105">**NonEmptyArrayOfPeriodsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d5b31-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="d5b31-106">Attributes and elements</span></span>

<span data-ttu-id="d5b31-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="d5b31-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d5b31-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="d5b31-108">Attributes</span></span>

<span data-ttu-id="d5b31-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="d5b31-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d5b31-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="d5b31-110">Child elements</span></span>

|<span data-ttu-id="d5b31-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="d5b31-111">**Element**</span></span>|<span data-ttu-id="d5b31-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d5b31-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d5b31-113">Period</span><span class="sxs-lookup"><span data-stu-id="d5b31-113">Period</span></span>](period.md) <br/> |<span data-ttu-id="d5b31-114">Define el nombre, el desplazamiento de tiempo y el identificador único para una región específica de la zona horaria.</span><span class="sxs-lookup"><span data-stu-id="d5b31-114">Defines the name, time offset, and unique identifier for a specific stage of the time zone.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d5b31-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="d5b31-115">Parent elements</span></span>

|<span data-ttu-id="d5b31-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="d5b31-116">**Element**</span></span>|<span data-ttu-id="d5b31-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d5b31-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d5b31-118">StartTimeZone</span><span class="sxs-lookup"><span data-stu-id="d5b31-118">StartTimeZone</span></span>](starttimezone.md) <br/> |<span data-ttu-id="d5b31-119">Define la zona horaria de la hora de inicio de un [CalendarItem](calendaritem.md) o [MeetingRequest](meetingrequest.md).</span><span class="sxs-lookup"><span data-stu-id="d5b31-119">Defines the time zone for the start time of a [CalendarItem](calendaritem.md) or [MeetingRequest](meetingrequest.md).</span></span>  <br/> |
|[<span data-ttu-id="d5b31-120">EndTimeZone</span><span class="sxs-lookup"><span data-stu-id="d5b31-120">EndTimeZone</span></span>](endtimezone.md) <br/> |<span data-ttu-id="d5b31-121">Define la zona horaria de la hora de finalización de un [CalendarItem](calendaritem.md) o [MeetingRequest](meetingrequest.md).</span><span class="sxs-lookup"><span data-stu-id="d5b31-121">Defines the time zone for the end time of a [CalendarItem](calendaritem.md) or [MeetingRequest](meetingrequest.md).</span></span>  <br/> |
|[<span data-ttu-id="d5b31-122">Definición de zona horaria</span><span class="sxs-lookup"><span data-stu-id="d5b31-122">TimeZoneDefinition</span></span>](timezonedefinition.md) <br/> |<span data-ttu-id="d5b31-123">Define una zona horaria.</span><span class="sxs-lookup"><span data-stu-id="d5b31-123">Defines a time zone.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d5b31-124">Notas</span><span class="sxs-lookup"><span data-stu-id="d5b31-124">Remarks</span></span>

<span data-ttu-id="d5b31-125">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server que tiene instalada la función del servidor acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="d5b31-125">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d5b31-126">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="d5b31-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d5b31-127">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d5b31-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d5b31-128">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="d5b31-128">Schema Name</span></span>  <br/> |<span data-ttu-id="d5b31-129">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="d5b31-129">Types schema</span></span>  <br/> |
|<span data-ttu-id="d5b31-130">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="d5b31-130">Validation File</span></span>  <br/> |<span data-ttu-id="d5b31-131">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="d5b31-131">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d5b31-132">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="d5b31-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="d5b31-133">False</span><span class="sxs-lookup"><span data-stu-id="d5b31-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d5b31-134">Ver también</span><span class="sxs-lookup"><span data-stu-id="d5b31-134">See also</span></span>



- [<span data-ttu-id="d5b31-135">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="d5b31-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

