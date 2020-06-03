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
description: El elemento AttendeeType representa el tipo de asistente que se identifica en el elemento email (EmailAddressType). Este elemento se usa en las solicitudes de sugerencias de reunión.
ms.openlocfilehash: 104b9f38cc891310ecb47c0b47837a912ced6ab7
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462300"
---
# <a name="attendeetype"></a><span data-ttu-id="ac5c6-104">AttendeeType</span><span class="sxs-lookup"><span data-stu-id="ac5c6-104">AttendeeType</span></span>

<span data-ttu-id="ac5c6-105">El elemento **AttendeeType** representa el tipo de asistente que se identifica en el elemento [email (EmailAddressType)](email-emailaddresstype.md) .</span><span class="sxs-lookup"><span data-stu-id="ac5c6-105">The **AttendeeType** element represents the type of attendee that is identified in the [Email (EmailAddressType)](email-emailaddresstype.md) element.</span></span> <span data-ttu-id="ac5c6-106">Este elemento se usa en las solicitudes de sugerencias de reunión.</span><span class="sxs-lookup"><span data-stu-id="ac5c6-106">This element is used in requests for meeting suggestions.</span></span> 
  
- [<span data-ttu-id="ac5c6-107">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="ac5c6-107">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)
  
- [<span data-ttu-id="ac5c6-108">MailboxDataArray</span><span class="sxs-lookup"><span data-stu-id="ac5c6-108">MailboxDataArray</span></span>](mailboxdataarray.md)
  
- [<span data-ttu-id="ac5c6-109">MailboxData</span><span class="sxs-lookup"><span data-stu-id="ac5c6-109">MailboxData</span></span>](mailboxdata.md)
  
- [<span data-ttu-id="ac5c6-110">AttendeeType</span><span class="sxs-lookup"><span data-stu-id="ac5c6-110">AttendeeType</span></span>](attendeetype.md)
  
```xml
<AttendeeType>Organizer or Required or Optional or Room or Resource</AttendeeType>
```

 <span data-ttu-id="ac5c6-111">**MeetingAttendeeType**</span><span class="sxs-lookup"><span data-stu-id="ac5c6-111">**MeetingAttendeeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ac5c6-112">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="ac5c6-112">Attributes and elements</span></span>

<span data-ttu-id="ac5c6-113">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="ac5c6-113">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ac5c6-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="ac5c6-114">Attributes</span></span>

<span data-ttu-id="ac5c6-115">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="ac5c6-115">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ac5c6-116">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ac5c6-116">Child elements</span></span>

<span data-ttu-id="ac5c6-117">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="ac5c6-117">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="ac5c6-118">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="ac5c6-118">Parent elements</span></span>

|<span data-ttu-id="ac5c6-119">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="ac5c6-119">**Element**</span></span>|<span data-ttu-id="ac5c6-120">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ac5c6-120">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ac5c6-121">MailboxData</span><span class="sxs-lookup"><span data-stu-id="ac5c6-121">MailboxData</span></span>](mailboxdata.md) <br/> |<span data-ttu-id="ac5c6-122">Representa un usuario de buzón individual y opciones para el tipo de datos que se devolverán sobre el usuario del buzón.</span><span class="sxs-lookup"><span data-stu-id="ac5c6-122">Represents an individual mailbox user and options for the type of data to be returned about the mailbox user.</span></span>  <br/> <span data-ttu-id="ac5c6-123">A continuación se encuentra la expresión XPath de este elemento:</span><span class="sxs-lookup"><span data-stu-id="ac5c6-123">The following is the XPath to this element:</span></span>  <br/>  `/GetUserAvailabilityRequest/MailboxDataArray[i]/MailboxData` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="ac5c6-124">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="ac5c6-124">Text value</span></span>

<span data-ttu-id="ac5c6-125">Se requiere un valor de texto para este elemento.</span><span class="sxs-lookup"><span data-stu-id="ac5c6-125">A text value is required for this element.</span></span> <span data-ttu-id="ac5c6-126">En la siguiente tabla se enumeran los valores posibles para este elemento.</span><span class="sxs-lookup"><span data-stu-id="ac5c6-126">The following table lists the possible values for this element.</span></span>
  
|<span data-ttu-id="ac5c6-127">**Valor**</span><span class="sxs-lookup"><span data-stu-id="ac5c6-127">**Value**</span></span>|<span data-ttu-id="ac5c6-128">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ac5c6-128">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ac5c6-129">Organizador</span><span class="sxs-lookup"><span data-stu-id="ac5c6-129">Organizer</span></span>  <br/> |<span data-ttu-id="ac5c6-130">El usuario del buzón de correo y el asistente que creó el elemento de calendario.</span><span class="sxs-lookup"><span data-stu-id="ac5c6-130">The mailbox user and attendee who created the calendar item.</span></span>  <br/> |
|<span data-ttu-id="ac5c6-131">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="ac5c6-131">Required</span></span>  <br/> |<span data-ttu-id="ac5c6-132">Un usuario de buzón de correo que es un asistente requerido para la reunión.</span><span class="sxs-lookup"><span data-stu-id="ac5c6-132">A mailbox user who is a required attendee to the meeting.</span></span>  <br/> |
|<span data-ttu-id="ac5c6-133">Opcional</span><span class="sxs-lookup"><span data-stu-id="ac5c6-133">Optional</span></span>  <br/> |<span data-ttu-id="ac5c6-134">Un usuario de buzón de correo que es un asistente opcional a la reunión.</span><span class="sxs-lookup"><span data-stu-id="ac5c6-134">A mailbox user who is an optional attendee to the meeting.</span></span>  <br/> |
|<span data-ttu-id="ac5c6-135">Sala</span><span class="sxs-lookup"><span data-stu-id="ac5c6-135">Room</span></span>  <br/> |<span data-ttu-id="ac5c6-136">Entidad de buzón de correo que representa un recurso de sala usado para la reunión.</span><span class="sxs-lookup"><span data-stu-id="ac5c6-136">A mailbox entity that represents a room resource used for the meeting.</span></span>  <br/> |
|<span data-ttu-id="ac5c6-137">Resource</span><span class="sxs-lookup"><span data-stu-id="ac5c6-137">Resource</span></span>  <br/> |<span data-ttu-id="ac5c6-138">Un recurso como un televisor o un proyector programados para su uso en la reunión.</span><span class="sxs-lookup"><span data-stu-id="ac5c6-138">A resource such as a TV or projector that is scheduled for use in the meeting.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ac5c6-139">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ac5c6-139">Remarks</span></span>

<span data-ttu-id="ac5c6-140">Este elemento es un elemento secundario necesario del elemento [MailboxData](mailboxdata.md) .</span><span class="sxs-lookup"><span data-stu-id="ac5c6-140">This element is a required child element of the [MailboxData](mailboxdata.md) element.</span></span> <span data-ttu-id="ac5c6-141">Este elemento solo puede producirse una vez en el elemento [MailboxData](mailboxdata.md) .</span><span class="sxs-lookup"><span data-stu-id="ac5c6-141">This element can only occur once in the [MailboxData](mailboxdata.md) element.</span></span> <span data-ttu-id="ac5c6-142">El esquema que describe este elemento se encuentra en el directorio/EWS/del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="ac5c6-142">The schema that describes this element is located in the /EWS/ directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="ac5c6-143">El tipo de esquema AttendeeType se usa para representar a los asistentes a un elemento de calendario.</span><span class="sxs-lookup"><span data-stu-id="ac5c6-143">The AttendeeType schema type is used to represent attendees to a calendar item.</span></span> <span data-ttu-id="ac5c6-144">No confunda este elemento con los elementos del tipo de esquema AttendeeType.</span><span class="sxs-lookup"><span data-stu-id="ac5c6-144">Do not confuse this element with elements of the AttendeeType schema type.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="ac5c6-145">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="ac5c6-145">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ac5c6-146">Namespace</span><span class="sxs-lookup"><span data-stu-id="ac5c6-146">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ac5c6-147">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="ac5c6-147">Schema Name</span></span>  <br/> |<span data-ttu-id="ac5c6-148">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="ac5c6-148">Types schema</span></span>  <br/> |
|<span data-ttu-id="ac5c6-149">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="ac5c6-149">Validation File</span></span>  <br/> |<span data-ttu-id="ac5c6-150">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="ac5c6-150">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="ac5c6-151">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="ac5c6-151">Can be Empty</span></span>  <br/> |<span data-ttu-id="ac5c6-152">Falso</span><span class="sxs-lookup"><span data-stu-id="ac5c6-152">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ac5c6-153">Vea también</span><span class="sxs-lookup"><span data-stu-id="ac5c6-153">See also</span></span>

- [<span data-ttu-id="ac5c6-154">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="ac5c6-154">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
- [<span data-ttu-id="ac5c6-155">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="ac5c6-155">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)
- [<span data-ttu-id="ac5c6-156">Obtener disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="ac5c6-156">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

