---
title: AttendeeType
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AttendeeType
api_type:
- schema
ms.assetid: 048043a8-dbad-45a0-97c8-4cad63d8898b
description: El elemento AttendeeType representa el tipo de asistente que se identifica en el elemento de correo electrónico (EmailAddressType). Este elemento se usa en las solicitudes de sugerencias de reunión.
ms.openlocfilehash: a08532ed78296102ee252c1e0c40beee7ca8ea5d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763578"
---
# <a name="attendeetype"></a><span data-ttu-id="891ff-104">AttendeeType</span><span class="sxs-lookup"><span data-stu-id="891ff-104">AttendeeType</span></span>

<span data-ttu-id="891ff-105">El elemento **AttendeeType** representa el tipo de asistente que se identifica en el elemento de [correo electrónico (EmailAddressType)](email-emailaddresstype.md) .</span><span class="sxs-lookup"><span data-stu-id="891ff-105">The **AttendeeType** element represents the type of attendee that is identified in the [Email (EmailAddressType)](email-emailaddresstype.md) element.</span></span> <span data-ttu-id="891ff-106">Este elemento se usa en las solicitudes de sugerencias de reunión.</span><span class="sxs-lookup"><span data-stu-id="891ff-106">This element is used in requests for meeting suggestions.</span></span> 
  
- [<span data-ttu-id="891ff-107">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="891ff-107">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)
  
- [<span data-ttu-id="891ff-108">MailboxDataArray</span><span class="sxs-lookup"><span data-stu-id="891ff-108">MailboxDataArray</span></span>](mailboxdataarray.md)
  
- [<span data-ttu-id="891ff-109">MailboxData</span><span class="sxs-lookup"><span data-stu-id="891ff-109">MailboxData</span></span>](mailboxdata.md)
  
- [<span data-ttu-id="891ff-110">AttendeeType</span><span class="sxs-lookup"><span data-stu-id="891ff-110">AttendeeType</span></span>](attendeetype.md)
  
```xml
<AttendeeType>Organizer or Required or Optional or Room or Resource</AttendeeType>
```

 <span data-ttu-id="891ff-111">**MeetingAttendeeType**</span><span class="sxs-lookup"><span data-stu-id="891ff-111">**MeetingAttendeeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="891ff-112">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="891ff-112">Attributes and elements</span></span>

<span data-ttu-id="891ff-113">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="891ff-113">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="891ff-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="891ff-114">Attributes</span></span>

<span data-ttu-id="891ff-115">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="891ff-115">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="891ff-116">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="891ff-116">Child elements</span></span>

<span data-ttu-id="891ff-117">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="891ff-117">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="891ff-118">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="891ff-118">Parent elements</span></span>

|<span data-ttu-id="891ff-119">**Element**</span><span class="sxs-lookup"><span data-stu-id="891ff-119">**Element**</span></span>|<span data-ttu-id="891ff-120">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="891ff-120">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="891ff-121">MailboxData</span><span class="sxs-lookup"><span data-stu-id="891ff-121">MailboxData</span></span>](mailboxdata.md) <br/> |<span data-ttu-id="891ff-122">Representa un usuario de buzón de correo individual y opciones para el tipo de datos que se devolverá sobre el usuario del buzón.</span><span class="sxs-lookup"><span data-stu-id="891ff-122">Represents an individual mailbox user and options for the type of data to be returned about the mailbox user.</span></span>  <br/> <span data-ttu-id="891ff-123">La siguiente es la expresión de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="891ff-123">The following is the XPath to this element:</span></span>  <br/>  `/GetUserAvailabilityRequest/MailboxDataArray[i]/MailboxData` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="891ff-124">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="891ff-124">Text value</span></span>

<span data-ttu-id="891ff-125">Un valor de texto es necesario para este elemento.</span><span class="sxs-lookup"><span data-stu-id="891ff-125">A text value is required for this element.</span></span> <span data-ttu-id="891ff-126">En la siguiente tabla se enumera los valores posibles para este elemento.</span><span class="sxs-lookup"><span data-stu-id="891ff-126">The following table lists the possible values for this element.</span></span>
  
|<span data-ttu-id="891ff-127">**Valor**</span><span class="sxs-lookup"><span data-stu-id="891ff-127">**Value**</span></span>|<span data-ttu-id="891ff-128">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="891ff-128">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="891ff-129">Organizador</span><span class="sxs-lookup"><span data-stu-id="891ff-129">Organizer</span></span>  <br/> |<span data-ttu-id="891ff-130">El usuario del buzón y el asistente que creó el elemento de calendario.</span><span class="sxs-lookup"><span data-stu-id="891ff-130">The mailbox user and attendee who created the calendar item.</span></span>  <br/> |
|<span data-ttu-id="891ff-131">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="891ff-131">Required</span></span>  <br/> |<span data-ttu-id="891ff-132">Un usuario de buzón de correo que sea un asistente necesario a la reunión.</span><span class="sxs-lookup"><span data-stu-id="891ff-132">A mailbox user who is a required attendee to the meeting.</span></span>  <br/> |
|<span data-ttu-id="891ff-133">Opcional</span><span class="sxs-lookup"><span data-stu-id="891ff-133">Optional</span></span>  <br/> |<span data-ttu-id="891ff-134">Un usuario de buzón de correo que es un asistente opcional para la reunión.</span><span class="sxs-lookup"><span data-stu-id="891ff-134">A mailbox user who is an optional attendee to the meeting.</span></span>  <br/> |
|<span data-ttu-id="891ff-135">Salón</span><span class="sxs-lookup"><span data-stu-id="891ff-135">Room</span></span>  <br/> |<span data-ttu-id="891ff-136">Una entidad de buzón de correo que representa un recurso de sala utilizado para la reunión.</span><span class="sxs-lookup"><span data-stu-id="891ff-136">A mailbox entity that represents a room resource used for the meeting.</span></span>  <br/> |
|<span data-ttu-id="891ff-137">Recurso</span><span class="sxs-lookup"><span data-stu-id="891ff-137">Resource</span></span>  <br/> |<span data-ttu-id="891ff-138">Un recurso, como una TV o proyectores que está programada para su uso en la reunión.</span><span class="sxs-lookup"><span data-stu-id="891ff-138">A resource such as a TV or projector that is scheduled for use in the meeting.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="891ff-139">Notas</span><span class="sxs-lookup"><span data-stu-id="891ff-139">Remarks</span></span>

<span data-ttu-id="891ff-140">Este elemento es un elemento secundario necesario del elemento [MailboxData](mailboxdata.md) .</span><span class="sxs-lookup"><span data-stu-id="891ff-140">This element is a required child element of the [MailboxData](mailboxdata.md) element.</span></span> <span data-ttu-id="891ff-141">Este elemento sólo puede aparecer una vez en el elemento [MailboxData](mailboxdata.md) .</span><span class="sxs-lookup"><span data-stu-id="891ff-141">This element can only occur once in the [MailboxData](mailboxdata.md) element.</span></span> <span data-ttu-id="891ff-142">El esquema que describe este elemento se encuentra en el directorio /EWS/ del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="891ff-142">The schema that describes this element is located in the /EWS/ directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="891ff-143">El tipo de esquema de AttendeeType se usa para representar a los asistentes a un elemento de calendario.</span><span class="sxs-lookup"><span data-stu-id="891ff-143">The AttendeeType schema type is used to represent attendees to a calendar item.</span></span> <span data-ttu-id="891ff-144">No confunda este elemento con elementos del tipo de esquema AttendeeType.</span><span class="sxs-lookup"><span data-stu-id="891ff-144">Do not confuse this element with elements of the AttendeeType schema type.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="891ff-145">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="891ff-145">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="891ff-146">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="891ff-146">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="891ff-147">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="891ff-147">Schema Name</span></span>  <br/> |<span data-ttu-id="891ff-148">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="891ff-148">Types schema</span></span>  <br/> |
|<span data-ttu-id="891ff-149">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="891ff-149">Validation File</span></span>  <br/> |<span data-ttu-id="891ff-150">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="891ff-150">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="891ff-151">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="891ff-151">Can be Empty</span></span>  <br/> |<span data-ttu-id="891ff-152">False</span><span class="sxs-lookup"><span data-stu-id="891ff-152">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="891ff-153">Ver también</span><span class="sxs-lookup"><span data-stu-id="891ff-153">See also</span></span>

- [<span data-ttu-id="891ff-154">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="891ff-154">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
- [<span data-ttu-id="891ff-155">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="891ff-155">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)
- [<span data-ttu-id="891ff-156">Obtención de disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="891ff-156">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

