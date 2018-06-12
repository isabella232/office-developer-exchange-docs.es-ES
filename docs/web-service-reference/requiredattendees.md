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
ms.lasthandoff: 06/11/2018
ms.locfileid: "19837149"
---
# <a name="requiredattendees"></a><span data-ttu-id="81dda-103">RequiredAttendees</span><span class="sxs-lookup"><span data-stu-id="81dda-103">RequiredAttendees</span></span>

<span data-ttu-id="81dda-104">El elemento **RequiredAttendees** representa a los asistentes necesarios para asistir a una reunión.</span><span class="sxs-lookup"><span data-stu-id="81dda-104">The **RequiredAttendees** element represents attendees that are required to attend a meeting.</span></span> 
  
```xml
<RequiredAttendees>
   <Attendee/>
</RequiredAttendees>
```

 <span data-ttu-id="81dda-105">**NonEmptyArrayOfAttendeesType**</span><span class="sxs-lookup"><span data-stu-id="81dda-105">**NonEmptyArrayOfAttendeesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="81dda-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="81dda-106">Attributes and elements</span></span>

<span data-ttu-id="81dda-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="81dda-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="81dda-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="81dda-108">Attributes</span></span>

<span data-ttu-id="81dda-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="81dda-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="81dda-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="81dda-110">Child elements</span></span>

|<span data-ttu-id="81dda-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="81dda-111">**Element**</span></span>|<span data-ttu-id="81dda-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="81dda-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="81dda-113">Attendee</span><span class="sxs-lookup"><span data-stu-id="81dda-113">Attendee</span></span>](attendee.md) <br/> |<span data-ttu-id="81dda-114">Representa los asistentes y los recursos de una reunión.</span><span class="sxs-lookup"><span data-stu-id="81dda-114">Represents attendees and resources for a meeting.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="81dda-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="81dda-115">Parent elements</span></span>

|<span data-ttu-id="81dda-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="81dda-116">**Element**</span></span>|<span data-ttu-id="81dda-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="81dda-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="81dda-118">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="81dda-118">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="81dda-119">Representa un elemento de calendario de Exchange.</span><span class="sxs-lookup"><span data-stu-id="81dda-119">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="81dda-120">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="81dda-120">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="81dda-121">Representa una convocatoria de reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="81dda-121">Represents a meeting request in the Exchange store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="81dda-122">Notas</span><span class="sxs-lookup"><span data-stu-id="81dda-122">Remarks</span></span>

<span data-ttu-id="81dda-123">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="81dda-123">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="81dda-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="81dda-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="81dda-125">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="81dda-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="81dda-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="81dda-126">Schema name</span></span>  <br/> |<span data-ttu-id="81dda-127">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="81dda-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="81dda-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="81dda-128">Validation file</span></span>  <br/> |<span data-ttu-id="81dda-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="81dda-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="81dda-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="81dda-130">Can be empty</span></span>  <br/> |<span data-ttu-id="81dda-131">False</span><span class="sxs-lookup"><span data-stu-id="81dda-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="81dda-132">Ver también</span><span class="sxs-lookup"><span data-stu-id="81dda-132">See also</span></span>



- [<span data-ttu-id="81dda-133">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="81dda-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

