---
title: ATTENDEE
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
description: El elemento de Attendee representa los asistentes y los recursos de una reunión.
ms.openlocfilehash: 60cb0839c2f6de69b833c11f4594d40c14cd8887
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763573"
---
# <a name="attendee"></a><span data-ttu-id="b871c-103">ATTENDEE</span><span class="sxs-lookup"><span data-stu-id="b871c-103">Attendee</span></span>

<span data-ttu-id="b871c-104">El elemento de **Attendee** representa los asistentes y los recursos de una reunión.</span><span class="sxs-lookup"><span data-stu-id="b871c-104">The **Attendee** element represents attendees and resources for a meeting.</span></span> 
  
```xml
<Attendee>
   <Mailbox/>
   <ResponseType/>
   <LastResponseTime/>
</Attendee>
```

 <span data-ttu-id="b871c-105">**AttendeeType**</span><span class="sxs-lookup"><span data-stu-id="b871c-105">**AttendeeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b871c-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="b871c-106">Attributes and elements</span></span>

<span data-ttu-id="b871c-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="b871c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b871c-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="b871c-108">Attributes</span></span>

<span data-ttu-id="b871c-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="b871c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b871c-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b871c-110">Child elements</span></span>

|<span data-ttu-id="b871c-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="b871c-111">**Element**</span></span>|<span data-ttu-id="b871c-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b871c-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b871c-113">Buzón de correo</span><span class="sxs-lookup"><span data-stu-id="b871c-113">Mailbox</span></span>](mailbox.md) <br/> |<span data-ttu-id="b871c-114">Identifica una dirección de correo electrónico completa resuelta.</span><span class="sxs-lookup"><span data-stu-id="b871c-114">Identifies a fully resolved e-mail address.</span></span>  <br/> |
|[<span data-ttu-id="b871c-115">ResponseType</span><span class="sxs-lookup"><span data-stu-id="b871c-115">ResponseType</span></span>](responsetype.md) <br/> |<span data-ttu-id="b871c-116">Representa el tipo de respuesta de destinatarios que se recibe de una reunión.</span><span class="sxs-lookup"><span data-stu-id="b871c-116">Represents the type of recipient response that is received for a meeting.</span></span> <span data-ttu-id="b871c-117">Esta propiedad sólo es relevante para el elemento de calendario del organizador de una reunión.</span><span class="sxs-lookup"><span data-stu-id="b871c-117">This property is only relevant to a meeting organizer's calendar item.</span></span>  <br/> |
|[<span data-ttu-id="b871c-118">LastResponseTime</span><span class="sxs-lookup"><span data-stu-id="b871c-118">LastResponseTime</span></span>](lastresponsetime.md) <br/> |<span data-ttu-id="b871c-119">Representa la fecha y hora de la respuesta más reciente que se recibe.</span><span class="sxs-lookup"><span data-stu-id="b871c-119">Represents the date and time of the latest response that is received.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="b871c-120">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="b871c-120">Parent elements</span></span>

|<span data-ttu-id="b871c-121">**Element**</span><span class="sxs-lookup"><span data-stu-id="b871c-121">**Element**</span></span>|<span data-ttu-id="b871c-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b871c-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b871c-123">RequiredAttendees</span><span class="sxs-lookup"><span data-stu-id="b871c-123">RequiredAttendees</span></span>](requiredattendees.md) <br/> |<span data-ttu-id="b871c-124">Representa a los asistentes necesarios para asistir a una reunión.</span><span class="sxs-lookup"><span data-stu-id="b871c-124">Represents attendees that are required to attend a meeting.</span></span>  <br/> |
|[<span data-ttu-id="b871c-125">OptionalAttendees</span><span class="sxs-lookup"><span data-stu-id="b871c-125">OptionalAttendees</span></span>](optionalattendees.md) <br/> |<span data-ttu-id="b871c-126">Representa a los asistentes que no sean necesarios para asistir a una reunión.</span><span class="sxs-lookup"><span data-stu-id="b871c-126">Represents attendees that are not required to attend a meeting.</span></span>  <br/> |
|[<span data-ttu-id="b871c-127">Recursos</span><span class="sxs-lookup"><span data-stu-id="b871c-127">Resources</span></span>](resources.md) <br/> |<span data-ttu-id="b871c-128">Representa un recurso para una reunión programado.</span><span class="sxs-lookup"><span data-stu-id="b871c-128">Represents a scheduled resource for a meeting.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b871c-129">Notas</span><span class="sxs-lookup"><span data-stu-id="b871c-129">Remarks</span></span>

<span data-ttu-id="b871c-130">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="b871c-130">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b871c-131">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="b871c-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b871c-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b871c-132">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="b871c-133">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="b871c-133">Schema name</span></span>  <br/> |<span data-ttu-id="b871c-134">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="b871c-134">Types schema</span></span>  <br/> |
|<span data-ttu-id="b871c-135">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="b871c-135">Validation file</span></span>  <br/> |<span data-ttu-id="b871c-136">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="b871c-136">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="b871c-137">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="b871c-137">Can be empty</span></span>  <br/> |<span data-ttu-id="b871c-138">False</span><span class="sxs-lookup"><span data-stu-id="b871c-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b871c-139">Ver también</span><span class="sxs-lookup"><span data-stu-id="b871c-139">See also</span></span>

- [<span data-ttu-id="b871c-140">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="b871c-140">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

