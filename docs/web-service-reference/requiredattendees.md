---
title: RequiredAttendees
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RequiredAttendees
api_type:
- schema
ms.assetid: 422f8d44-b0eb-49ca-af0f-0e22b54c78d2
description: El elemento RequiredAttendees representa a los asistentes necesarios para asistir a una reunión.
ms.openlocfilehash: 9630be828f459808b61602448a4675aac07b0106
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19837149"
---
# <a name="requiredattendees"></a><span data-ttu-id="d903d-103">RequiredAttendees</span><span class="sxs-lookup"><span data-stu-id="d903d-103">RequiredAttendees</span></span>

<span data-ttu-id="d903d-104">El elemento **RequiredAttendees** representa a los asistentes necesarios para asistir a una reunión.</span><span class="sxs-lookup"><span data-stu-id="d903d-104">The **RequiredAttendees** element represents attendees that are required to attend a meeting.</span></span> 
  
```xml
<RequiredAttendees>
   <Attendee/>
</RequiredAttendees>
```

 <span data-ttu-id="d903d-105">**NonEmptyArrayOfAttendeesType**</span><span class="sxs-lookup"><span data-stu-id="d903d-105">**NonEmptyArrayOfAttendeesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d903d-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="d903d-106">Attributes and elements</span></span>

<span data-ttu-id="d903d-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="d903d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d903d-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="d903d-108">Attributes</span></span>

<span data-ttu-id="d903d-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="d903d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d903d-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="d903d-110">Child elements</span></span>

|<span data-ttu-id="d903d-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="d903d-111">**Element**</span></span>|<span data-ttu-id="d903d-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d903d-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d903d-113">Attendee</span><span class="sxs-lookup"><span data-stu-id="d903d-113">Attendee</span></span>](attendee.md) <br/> |<span data-ttu-id="d903d-114">Representa los asistentes y los recursos de una reunión.</span><span class="sxs-lookup"><span data-stu-id="d903d-114">Represents attendees and resources for a meeting.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d903d-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="d903d-115">Parent elements</span></span>

|<span data-ttu-id="d903d-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="d903d-116">**Element**</span></span>|<span data-ttu-id="d903d-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d903d-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d903d-118">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="d903d-118">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="d903d-119">Representa un elemento de calendario de Exchange.</span><span class="sxs-lookup"><span data-stu-id="d903d-119">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="d903d-120">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="d903d-120">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="d903d-121">Representa una convocatoria de reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="d903d-121">Represents a meeting request in the Exchange store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d903d-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d903d-122">Remarks</span></span>

<span data-ttu-id="d903d-123">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="d903d-123">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d903d-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="d903d-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d903d-125">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d903d-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d903d-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="d903d-126">Schema name</span></span>  <br/> |<span data-ttu-id="d903d-127">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="d903d-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="d903d-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="d903d-128">Validation file</span></span>  <br/> |<span data-ttu-id="d903d-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="d903d-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d903d-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="d903d-130">Can be empty</span></span>  <br/> |<span data-ttu-id="d903d-131">False</span><span class="sxs-lookup"><span data-stu-id="d903d-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d903d-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="d903d-132">See also</span></span>



- [<span data-ttu-id="d903d-133">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="d903d-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

