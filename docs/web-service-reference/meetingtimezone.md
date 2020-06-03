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
ms.openlocfilehash: aef4ac4e7571ded6920cbaf90e2895d421068f55
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465474"
---
# <a name="meetingtimezone"></a><span data-ttu-id="ab741-103">MeetingTimeZone</span><span class="sxs-lookup"><span data-stu-id="ab741-103">MeetingTimeZone</span></span>

<span data-ttu-id="ab741-104">El elemento **MeetingTimeZone** representa la zona horaria de la ubicación donde se hospeda la reunión.</span><span class="sxs-lookup"><span data-stu-id="ab741-104">The **MeetingTimeZone** element represents the time zone of the location where the meeting is hosted.</span></span> 
  
```xml
<MeetingTimeZone>
   <BaseOffset/>
   <Standard/>
   <Daylight/>
</MeetingTimeZone>
```

 <span data-ttu-id="ab741-105">**TimeZoneType**</span><span class="sxs-lookup"><span data-stu-id="ab741-105">**TimeZoneType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ab741-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="ab741-106">Attributes and elements</span></span>

<span data-ttu-id="ab741-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="ab741-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ab741-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="ab741-108">Attributes</span></span>

|<span data-ttu-id="ab741-109">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="ab741-109">**Attribute**</span></span>|<span data-ttu-id="ab741-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ab741-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ab741-111">**TimeZoneName**</span><span class="sxs-lookup"><span data-stu-id="ab741-111">**TimeZoneName**</span></span> <br/> |<span data-ttu-id="ab741-112">Describe el nombre de la zona horaria.</span><span class="sxs-lookup"><span data-stu-id="ab741-112">Describes the name of the time zone.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="ab741-113">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ab741-113">Child elements</span></span>

|<span data-ttu-id="ab741-114">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="ab741-114">**Element**</span></span>|<span data-ttu-id="ab741-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ab741-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ab741-116">BaseOffset</span><span class="sxs-lookup"><span data-stu-id="ab741-116">BaseOffset</span></span>](baseoffset.md) <br/> |<span data-ttu-id="ab741-117">Representa la desviación por horas respecto a la hora UTC de la zona horaria actual.</span><span class="sxs-lookup"><span data-stu-id="ab741-117">Represents the hourly offset from UTC for the current time zone.</span></span>  <br/> |
|[<span data-ttu-id="ab741-118">Estándar</span><span class="sxs-lookup"><span data-stu-id="ab741-118">Standard</span></span>](standard.md) <br/> |<span data-ttu-id="ab741-119">Representa la fecha y la hora en que cambia el horario de verano a la hora estándar.</span><span class="sxs-lookup"><span data-stu-id="ab741-119">Represents the date and time when the time changes from daylight saving time to standard time.</span></span>  <br/> |
|[<span data-ttu-id="ab741-120">Horario</span><span class="sxs-lookup"><span data-stu-id="ab741-120">Daylight</span></span>](daylight.md) <br/> |<span data-ttu-id="ab741-121">Representa la fecha y hora en que la hora cambia de la hora estándar al horario de verano.</span><span class="sxs-lookup"><span data-stu-id="ab741-121">Represents the date and time when the time changes from standard time to daylight saving time.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ab741-122">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="ab741-122">Parent elements</span></span>

|<span data-ttu-id="ab741-123">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="ab741-123">**Element**</span></span>|<span data-ttu-id="ab741-124">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ab741-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ab741-125">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="ab741-125">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="ab741-126">Representa un elemento de calendario de Exchange.</span><span class="sxs-lookup"><span data-stu-id="ab741-126">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="ab741-127">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="ab741-127">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="ab741-128">Representa una convocatoria de reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="ab741-128">Represents a meeting request in the Exchange store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ab741-129">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ab741-129">Remarks</span></span>

<span data-ttu-id="ab741-130">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="ab741-130">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ab741-131">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="ab741-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ab741-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="ab741-132">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ab741-133">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="ab741-133">Schema Name</span></span>  <br/> |<span data-ttu-id="ab741-134">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="ab741-134">Types schema</span></span>  <br/> |
|<span data-ttu-id="ab741-135">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="ab741-135">Validation File</span></span>  <br/> |<span data-ttu-id="ab741-136">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="ab741-136">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="ab741-137">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="ab741-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="ab741-138">Falso</span><span class="sxs-lookup"><span data-stu-id="ab741-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ab741-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="ab741-139">See also</span></span>



- [<span data-ttu-id="ab741-140">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="ab741-140">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

