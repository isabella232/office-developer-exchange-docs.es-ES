---
title: Asistente
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Attendee
api_type:
- schema
ms.assetid: 393c3d7e-7416-458a-b976-270b88eaaa03
description: El elemento Attendee representa los asistentes y los recursos de una reunión.
ms.openlocfilehash: f376e59b27017e0a9d27692cb1a4ae759cd1af0e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457651"
---
# <a name="attendee"></a><span data-ttu-id="db0e2-103">Asistente</span><span class="sxs-lookup"><span data-stu-id="db0e2-103">Attendee</span></span>

<span data-ttu-id="db0e2-104">El elemento **Attendee** representa los asistentes y los recursos de una reunión.</span><span class="sxs-lookup"><span data-stu-id="db0e2-104">The **Attendee** element represents attendees and resources for a meeting.</span></span> 
  
```xml
<Attendee>
   <Mailbox/>
   <ResponseType/>
   <LastResponseTime/>
</Attendee>
```

 <span data-ttu-id="db0e2-105">**AttendeeType**</span><span class="sxs-lookup"><span data-stu-id="db0e2-105">**AttendeeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="db0e2-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="db0e2-106">Attributes and elements</span></span>

<span data-ttu-id="db0e2-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="db0e2-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="db0e2-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="db0e2-108">Attributes</span></span>

<span data-ttu-id="db0e2-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="db0e2-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="db0e2-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="db0e2-110">Child elements</span></span>

|<span data-ttu-id="db0e2-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="db0e2-111">**Element**</span></span>|<span data-ttu-id="db0e2-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="db0e2-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="db0e2-113">Buzón</span><span class="sxs-lookup"><span data-stu-id="db0e2-113">Mailbox</span></span>](mailbox.md) <br/> |<span data-ttu-id="db0e2-114">Identifica una dirección de correo electrónico completamente resuelta.</span><span class="sxs-lookup"><span data-stu-id="db0e2-114">Identifies a fully resolved e-mail address.</span></span>  <br/> |
|[<span data-ttu-id="db0e2-115">ResponseType</span><span class="sxs-lookup"><span data-stu-id="db0e2-115">ResponseType</span></span>](responsetype.md) <br/> |<span data-ttu-id="db0e2-116">Representa el tipo de respuesta de destinatario que se recibe para una reunión.</span><span class="sxs-lookup"><span data-stu-id="db0e2-116">Represents the type of recipient response that is received for a meeting.</span></span> <span data-ttu-id="db0e2-117">Esta propiedad sólo es relevante para el elemento de calendario de un organizador de la reunión.</span><span class="sxs-lookup"><span data-stu-id="db0e2-117">This property is only relevant to a meeting organizer's calendar item.</span></span>  <br/> |
|[<span data-ttu-id="db0e2-118">LastResponseTime</span><span class="sxs-lookup"><span data-stu-id="db0e2-118">LastResponseTime</span></span>](lastresponsetime.md) <br/> |<span data-ttu-id="db0e2-119">Representa la fecha y la hora de la última respuesta que se ha recibido.</span><span class="sxs-lookup"><span data-stu-id="db0e2-119">Represents the date and time of the latest response that is received.</span></span>  <br/> |
|[<span data-ttu-id="db0e2-120">ProposedStart</span><span class="sxs-lookup"><span data-stu-id="db0e2-120">ProposedStart</span></span>](proposedstart-attendeetype.md) <br/> |<span data-ttu-id="db0e2-121">Representa la hora de inicio propuesta de un asistente para una reunión.</span><span class="sxs-lookup"><span data-stu-id="db0e2-121">Represents an attendee's proposed start time for a meeting.</span></span> <br/> |
|[<span data-ttu-id="db0e2-122">ProposedEnd</span><span class="sxs-lookup"><span data-stu-id="db0e2-122">ProposedEnd</span></span>](proposedend-attendeetype.md) <br/> |<span data-ttu-id="db0e2-123">Representa la hora de finalización propuesta de un asistente para una reunión.</span><span class="sxs-lookup"><span data-stu-id="db0e2-123">Represents an attendee's proposed end time for a meeting.</span></span> <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="db0e2-124">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="db0e2-124">Parent elements</span></span>

|<span data-ttu-id="db0e2-125">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="db0e2-125">**Element**</span></span>|<span data-ttu-id="db0e2-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="db0e2-126">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="db0e2-127">RequiredAttendees</span><span class="sxs-lookup"><span data-stu-id="db0e2-127">RequiredAttendees</span></span>](requiredattendees.md) <br/> |<span data-ttu-id="db0e2-128">Representa a los asistentes necesarios para asistir a una reunión.</span><span class="sxs-lookup"><span data-stu-id="db0e2-128">Represents attendees that are required to attend a meeting.</span></span>  <br/> |
|[<span data-ttu-id="db0e2-129">OptionalAttendees</span><span class="sxs-lookup"><span data-stu-id="db0e2-129">OptionalAttendees</span></span>](optionalattendees.md) <br/> |<span data-ttu-id="db0e2-130">Representa a los asistentes que no necesitan asistir a una reunión.</span><span class="sxs-lookup"><span data-stu-id="db0e2-130">Represents attendees that are not required to attend a meeting.</span></span>  <br/> |
|[<span data-ttu-id="db0e2-131">Recursos</span><span class="sxs-lookup"><span data-stu-id="db0e2-131">Resources</span></span>](resources.md) <br/> |<span data-ttu-id="db0e2-132">Representa un recurso programado para una reunión.</span><span class="sxs-lookup"><span data-stu-id="db0e2-132">Represents a scheduled resource for a meeting.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="db0e2-133">Comentarios</span><span class="sxs-lookup"><span data-stu-id="db0e2-133">Remarks</span></span>

<span data-ttu-id="db0e2-134">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="db0e2-134">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="db0e2-135">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="db0e2-135">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="db0e2-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="db0e2-136">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="db0e2-137">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="db0e2-137">Schema name</span></span>  <br/> |<span data-ttu-id="db0e2-138">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="db0e2-138">Types schema</span></span>  <br/> |
|<span data-ttu-id="db0e2-139">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="db0e2-139">Validation file</span></span>  <br/> |<span data-ttu-id="db0e2-140">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="db0e2-140">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="db0e2-141">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="db0e2-141">Can be empty</span></span>  <br/> |<span data-ttu-id="db0e2-142">Falso</span><span class="sxs-lookup"><span data-stu-id="db0e2-142">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="db0e2-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="db0e2-143">See also</span></span>

- [<span data-ttu-id="db0e2-144">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="db0e2-144">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

