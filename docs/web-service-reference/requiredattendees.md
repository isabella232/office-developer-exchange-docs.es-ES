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
ms.openlocfilehash: a67800687f24dc323c3d80e4166ca9dd34dfc4fc
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44468295"
---
# <a name="requiredattendees"></a><span data-ttu-id="92cc5-103">RequiredAttendees</span><span class="sxs-lookup"><span data-stu-id="92cc5-103">RequiredAttendees</span></span>

<span data-ttu-id="92cc5-104">El elemento **RequiredAttendees** representa a los asistentes necesarios para asistir a una reunión.</span><span class="sxs-lookup"><span data-stu-id="92cc5-104">The **RequiredAttendees** element represents attendees that are required to attend a meeting.</span></span> 
  
```xml
<RequiredAttendees>
   <Attendee/>
</RequiredAttendees>
```

 <span data-ttu-id="92cc5-105">**NonEmptyArrayOfAttendeesType**</span><span class="sxs-lookup"><span data-stu-id="92cc5-105">**NonEmptyArrayOfAttendeesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="92cc5-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="92cc5-106">Attributes and elements</span></span>

<span data-ttu-id="92cc5-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="92cc5-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="92cc5-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="92cc5-108">Attributes</span></span>

<span data-ttu-id="92cc5-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="92cc5-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="92cc5-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="92cc5-110">Child elements</span></span>

|<span data-ttu-id="92cc5-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="92cc5-111">**Element**</span></span>|<span data-ttu-id="92cc5-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="92cc5-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="92cc5-113">Asistente</span><span class="sxs-lookup"><span data-stu-id="92cc5-113">Attendee</span></span>](attendee.md) <br/> |<span data-ttu-id="92cc5-114">Representa los asistentes y los recursos de una reunión.</span><span class="sxs-lookup"><span data-stu-id="92cc5-114">Represents attendees and resources for a meeting.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="92cc5-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="92cc5-115">Parent elements</span></span>

|<span data-ttu-id="92cc5-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="92cc5-116">**Element**</span></span>|<span data-ttu-id="92cc5-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="92cc5-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="92cc5-118">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="92cc5-118">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="92cc5-119">Representa un elemento de calendario de Exchange.</span><span class="sxs-lookup"><span data-stu-id="92cc5-119">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="92cc5-120">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="92cc5-120">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="92cc5-121">Representa una convocatoria de reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="92cc5-121">Represents a meeting request in the Exchange store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="92cc5-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="92cc5-122">Remarks</span></span>

<span data-ttu-id="92cc5-123">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="92cc5-123">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="92cc5-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="92cc5-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="92cc5-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="92cc5-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="92cc5-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="92cc5-126">Schema name</span></span>  <br/> |<span data-ttu-id="92cc5-127">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="92cc5-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="92cc5-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="92cc5-128">Validation file</span></span>  <br/> |<span data-ttu-id="92cc5-129">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="92cc5-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="92cc5-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="92cc5-130">Can be empty</span></span>  <br/> |<span data-ttu-id="92cc5-131">Falso</span><span class="sxs-lookup"><span data-stu-id="92cc5-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="92cc5-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="92cc5-132">See also</span></span>



- [<span data-ttu-id="92cc5-133">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="92cc5-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

