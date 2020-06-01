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
description: El elemento periods representa una matriz de puntos que definen el desplazamiento de tiempo en diferentes etapas de la zona horaria.
ms.openlocfilehash: 773457a6e4c0237eaeaf23109a7022427cc7dd0d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467777"
---
# <a name="periods"></a><span data-ttu-id="b865f-103">Períodos</span><span class="sxs-lookup"><span data-stu-id="b865f-103">Periods</span></span>

<span data-ttu-id="b865f-104">El elemento **periods** representa una matriz de puntos que definen el desplazamiento de tiempo en diferentes etapas de la zona horaria.</span><span class="sxs-lookup"><span data-stu-id="b865f-104">The **Periods** element represents an array of periods that define the time offset at different stages of the time zone.</span></span> 
  
```xml
<Periods>
   <Period/>
</Periods>
```

 <span data-ttu-id="b865f-105">**NonEmptyArrayOfPeriodsType**</span><span class="sxs-lookup"><span data-stu-id="b865f-105">**NonEmptyArrayOfPeriodsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b865f-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="b865f-106">Attributes and elements</span></span>

<span data-ttu-id="b865f-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="b865f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b865f-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="b865f-108">Attributes</span></span>

<span data-ttu-id="b865f-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="b865f-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b865f-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b865f-110">Child elements</span></span>

|<span data-ttu-id="b865f-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="b865f-111">**Element**</span></span>|<span data-ttu-id="b865f-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b865f-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b865f-113">Period</span><span class="sxs-lookup"><span data-stu-id="b865f-113">Period</span></span>](period.md) <br/> |<span data-ttu-id="b865f-114">Define el nombre, el desplazamiento de tiempo y el identificador único de una fase específica de la zona horaria.</span><span class="sxs-lookup"><span data-stu-id="b865f-114">Defines the name, time offset, and unique identifier for a specific stage of the time zone.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="b865f-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="b865f-115">Parent elements</span></span>

|<span data-ttu-id="b865f-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="b865f-116">**Element**</span></span>|<span data-ttu-id="b865f-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b865f-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b865f-118">StartTimeZone</span><span class="sxs-lookup"><span data-stu-id="b865f-118">StartTimeZone</span></span>](starttimezone.md) <br/> |<span data-ttu-id="b865f-119">Define la zona horaria de la hora de inicio de un [CalendarItem](calendaritem.md) o [MeetingRequest](meetingrequest.md).</span><span class="sxs-lookup"><span data-stu-id="b865f-119">Defines the time zone for the start time of a [CalendarItem](calendaritem.md) or [MeetingRequest](meetingrequest.md).</span></span>  <br/> |
|[<span data-ttu-id="b865f-120">EndTimeZone</span><span class="sxs-lookup"><span data-stu-id="b865f-120">EndTimeZone</span></span>](endtimezone.md) <br/> |<span data-ttu-id="b865f-121">Define la zona horaria de la hora de finalización de [CalendarItem](calendaritem.md) o [MeetingRequest](meetingrequest.md).</span><span class="sxs-lookup"><span data-stu-id="b865f-121">Defines the time zone for the end time of a [CalendarItem](calendaritem.md) or [MeetingRequest](meetingrequest.md).</span></span>  <br/> |
|[<span data-ttu-id="b865f-122">TimeZoneDefinition</span><span class="sxs-lookup"><span data-stu-id="b865f-122">TimeZoneDefinition</span></span>](timezonedefinition.md) <br/> |<span data-ttu-id="b865f-123">Define una zona horaria.</span><span class="sxs-lookup"><span data-stu-id="b865f-123">Defines a time zone.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b865f-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b865f-124">Remarks</span></span>

<span data-ttu-id="b865f-125">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="b865f-125">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b865f-126">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="b865f-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b865f-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="b865f-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="b865f-128">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="b865f-128">Schema Name</span></span>  <br/> |<span data-ttu-id="b865f-129">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="b865f-129">Types schema</span></span>  <br/> |
|<span data-ttu-id="b865f-130">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="b865f-130">Validation File</span></span>  <br/> |<span data-ttu-id="b865f-131">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="b865f-131">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="b865f-132">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="b865f-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="b865f-133">Falso</span><span class="sxs-lookup"><span data-stu-id="b865f-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b865f-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="b865f-134">See also</span></span>



- [<span data-ttu-id="b865f-135">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="b865f-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

