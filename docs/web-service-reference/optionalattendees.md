---
title: OptionalAttendees
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- OptionalAttendees
api_type:
- schema
ms.assetid: e7c80c4d-3794-45e9-986f-6a8a687df0a4
description: El elemento OptionalAttendees representa a los asistentes que no son necesarios para asistir a una reunión.
ms.openlocfilehash: d5d994f7e85a47b14ab47f58fb73533cf961f7e6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836658"
---
# <a name="optionalattendees"></a><span data-ttu-id="0e7e9-103">OptionalAttendees</span><span class="sxs-lookup"><span data-stu-id="0e7e9-103">OptionalAttendees</span></span>

<span data-ttu-id="0e7e9-104">El elemento **OptionalAttendees** representa a los asistentes que no son necesarios para asistir a una reunión.</span><span class="sxs-lookup"><span data-stu-id="0e7e9-104">The **OptionalAttendees** element represents attendees who are not required to attend a meeting.</span></span> 
  
```xml
<OptionalAttendees>
   <Attendee/>
</OptionalAttendees>
```

 <span data-ttu-id="0e7e9-105">**NonEmptyArrayOfAttendeesType**</span><span class="sxs-lookup"><span data-stu-id="0e7e9-105">**NonEmptyArrayOfAttendeesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0e7e9-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="0e7e9-106">Attributes and elements</span></span>

<span data-ttu-id="0e7e9-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="0e7e9-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0e7e9-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="0e7e9-108">Attributes</span></span>

<span data-ttu-id="0e7e9-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="0e7e9-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0e7e9-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="0e7e9-110">Child elements</span></span>

|<span data-ttu-id="0e7e9-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="0e7e9-111">**Element**</span></span>|<span data-ttu-id="0e7e9-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0e7e9-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0e7e9-113">Attendee</span><span class="sxs-lookup"><span data-stu-id="0e7e9-113">Attendee</span></span>](attendee.md) <br/> |<span data-ttu-id="0e7e9-114">Representa los asistentes y los recursos de una reunión.</span><span class="sxs-lookup"><span data-stu-id="0e7e9-114">Represents attendees and resources for a meeting.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="0e7e9-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="0e7e9-115">Parent elements</span></span>

|<span data-ttu-id="0e7e9-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="0e7e9-116">**Element**</span></span>|<span data-ttu-id="0e7e9-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0e7e9-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0e7e9-118">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="0e7e9-118">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="0e7e9-119">Representa un elemento de calendario de Exchange.</span><span class="sxs-lookup"><span data-stu-id="0e7e9-119">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="0e7e9-120">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="0e7e9-120">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="0e7e9-121">Representa una convocatoria de reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="0e7e9-121">Represents a meeting request in the Exchange store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0e7e9-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0e7e9-122">Remarks</span></span>

<span data-ttu-id="0e7e9-123">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="0e7e9-123">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0e7e9-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="0e7e9-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0e7e9-125">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="0e7e9-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="0e7e9-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="0e7e9-126">Schema name</span></span>  <br/> |<span data-ttu-id="0e7e9-127">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="0e7e9-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="0e7e9-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="0e7e9-128">Validation file</span></span>  <br/> |<span data-ttu-id="0e7e9-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="0e7e9-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="0e7e9-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="0e7e9-130">Can be empty</span></span>  <br/> |<span data-ttu-id="0e7e9-131">False</span><span class="sxs-lookup"><span data-stu-id="0e7e9-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0e7e9-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="0e7e9-132">See also</span></span>



- [<span data-ttu-id="0e7e9-133">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="0e7e9-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

