---
title: MailboxData
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MailboxData
api_type:
- schema
ms.assetid: e9e3f50c-5a7b-49c7-a9ea-117959c08352
description: El elemento MailboxData representa un usuario de buzón de correo individual y opciones para el tipo de datos que se devolverá sobre el usuario del buzón.
ms.openlocfilehash: df60294e7d83b1459e5cca7d75c2b6b4bb9d931d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836281"
---
# <a name="mailboxdata"></a><span data-ttu-id="5b3df-103">MailboxData</span><span class="sxs-lookup"><span data-stu-id="5b3df-103">MailboxData</span></span>

<span data-ttu-id="5b3df-104">El elemento **MailboxData** representa un usuario de buzón de correo individual y opciones para el tipo de datos que se devolverá sobre el usuario del buzón.</span><span class="sxs-lookup"><span data-stu-id="5b3df-104">The **MailboxData** element represents an individual mailbox user and options for the type of data to be returned about the mailbox user.</span></span> 
  
- [<span data-ttu-id="5b3df-105">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="5b3df-105">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)
  
- [<span data-ttu-id="5b3df-106">MailboxDataArray</span><span class="sxs-lookup"><span data-stu-id="5b3df-106">MailboxDataArray</span></span>](mailboxdataarray.md)
  
- [<span data-ttu-id="5b3df-107">MailboxData</span><span class="sxs-lookup"><span data-stu-id="5b3df-107">MailboxData</span></span>](mailboxdata.md)
  
```xml
<MailboxData>
   <Email>...</Email>
   <AttendeeType>...</AttendeeType>
   <ExcludeConflicts>...</ExcludeConflicts>
<MailboxData>
```

<span data-ttu-id="5b3df-108">**MailboxData**</span><span class="sxs-lookup"><span data-stu-id="5b3df-108">**MailboxData**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="5b3df-109">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="5b3df-109">Attributes and elements</span></span>

<span data-ttu-id="5b3df-110">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="5b3df-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5b3df-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="5b3df-111">Attributes</span></span>

<span data-ttu-id="5b3df-112">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="5b3df-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5b3df-113">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="5b3df-113">Child elements</span></span>

|<span data-ttu-id="5b3df-114">**Element**</span><span class="sxs-lookup"><span data-stu-id="5b3df-114">**Element**</span></span>|<span data-ttu-id="5b3df-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5b3df-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5b3df-116">Correo electrónico (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="5b3df-116">Email (EmailAddressType)</span></span>](email-emailaddresstype.md) <br/> |<span data-ttu-id="5b3df-117">Representa el usuario del buzón para una consulta GetUserAvailability.</span><span class="sxs-lookup"><span data-stu-id="5b3df-117">Represents the mailbox user for a GetUserAvailability query.</span></span>  <br/> |
|[<span data-ttu-id="5b3df-118">AttendeeType</span><span class="sxs-lookup"><span data-stu-id="5b3df-118">AttendeeType</span></span>](attendeetype.md) <br/> |<span data-ttu-id="5b3df-119">Representa el tipo de asistente identificado en el elemento de [correo electrónico (EmailAddressType)](email-emailaddresstype.md) .</span><span class="sxs-lookup"><span data-stu-id="5b3df-119">Represents the type of attendee identified in the [Email (EmailAddressType)](email-emailaddresstype.md) element.</span></span> <span data-ttu-id="5b3df-120">Se usa en las solicitudes de sugerencias de reunión.</span><span class="sxs-lookup"><span data-stu-id="5b3df-120">This is used in requests for meeting suggestions.</span></span>  <br/> |
|[<span data-ttu-id="5b3df-121">ExcludeConflicts</span><span class="sxs-lookup"><span data-stu-id="5b3df-121">ExcludeConflicts</span></span>](excludeconflicts.md) <br/> |<span data-ttu-id="5b3df-122">Especifica si se devuelven sugerida veces para tiempos de calendario que entre en conflicto entre los asistentes.</span><span class="sxs-lookup"><span data-stu-id="5b3df-122">Specifies whether to return suggested times for calendar times that conflict among the attendees.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="5b3df-123">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="5b3df-123">Parent elements</span></span>

|<span data-ttu-id="5b3df-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="5b3df-124">**Element**</span></span>|<span data-ttu-id="5b3df-125">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5b3df-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5b3df-126">MailboxDataArray</span><span class="sxs-lookup"><span data-stu-id="5b3df-126">MailboxDataArray</span></span>](mailboxdataarray.md) <br/> |<span data-ttu-id="5b3df-127">Contiene una lista de buzones de correo para consultar la información de disponibilidad.</span><span class="sxs-lookup"><span data-stu-id="5b3df-127">Contains a list of mailboxes to query for availability information.</span></span>  <br/> <span data-ttu-id="5b3df-128">La siguiente es la expresión de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="5b3df-128">The following is the XPath to this element:</span></span>  <br/>  `/GetUserAvailabilityRequest/MailboxDataArray[i]` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5b3df-129">Notas</span><span class="sxs-lookup"><span data-stu-id="5b3df-129">Remarks</span></span>

<span data-ttu-id="5b3df-130">Una aplicación cliente puede definir uno a muchos elementos **MailboxData** .</span><span class="sxs-lookup"><span data-stu-id="5b3df-130">A client application can define one to many **MailboxData** elements.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="5b3df-131">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="5b3df-131">The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange Server 2007 that has the Client Access server role installed.</span></span> 
  
## <a name="example"></a><span data-ttu-id="5b3df-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5b3df-132">Example</span></span>

```xml
<MailboxDataArray>
  <MailboxData xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
    <Email>
      <Name></Name>
      <Address>someone@ExServer.example.com</Address>
      <RoutingType>SMTP</RoutingType>
    </Email>
    <AttendeeType>Organizer</AttendeeType>
    <ExcludeConflicts>false</ExcludeConflicts>
  </MailboxData>
</MailboxDataArray>
```

## <a name="element-information"></a><span data-ttu-id="5b3df-133">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="5b3df-133">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5b3df-134">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="5b3df-134">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="5b3df-135">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="5b3df-135">Schema Name</span></span>  <br/> |<span data-ttu-id="5b3df-136">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="5b3df-136">Types schema</span></span>  <br/> |
|<span data-ttu-id="5b3df-137">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="5b3df-137">Validation File</span></span>  <br/> |<span data-ttu-id="5b3df-138">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="5b3df-138">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="5b3df-139">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="5b3df-139">Can be Empty</span></span>  <br/> |<span data-ttu-id="5b3df-140">False</span><span class="sxs-lookup"><span data-stu-id="5b3df-140">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5b3df-141">Ver también</span><span class="sxs-lookup"><span data-stu-id="5b3df-141">See also</span></span>

- [<span data-ttu-id="5b3df-142">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="5b3df-142">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
- [<span data-ttu-id="5b3df-143">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="5b3df-143">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)
- [<span data-ttu-id="5b3df-144">Obtención de disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="5b3df-144">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)
