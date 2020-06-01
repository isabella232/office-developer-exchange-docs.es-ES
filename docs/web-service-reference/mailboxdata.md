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
description: El elemento MailboxData representa un usuario de buzón individual y opciones para el tipo de datos que se devolverá sobre el usuario del buzón.
ms.openlocfilehash: bfcb8c01d40af81097c7d9868006fe9b7b5519d4
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467252"
---
# <a name="mailboxdata"></a><span data-ttu-id="95da7-103">MailboxData</span><span class="sxs-lookup"><span data-stu-id="95da7-103">MailboxData</span></span>

<span data-ttu-id="95da7-104">El elemento **MailboxData** representa un usuario de buzón individual y opciones para el tipo de datos que se devolverá sobre el usuario del buzón.</span><span class="sxs-lookup"><span data-stu-id="95da7-104">The **MailboxData** element represents an individual mailbox user and options for the type of data to be returned about the mailbox user.</span></span> 
  
- [<span data-ttu-id="95da7-105">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="95da7-105">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)
  
- [<span data-ttu-id="95da7-106">MailboxDataArray</span><span class="sxs-lookup"><span data-stu-id="95da7-106">MailboxDataArray</span></span>](mailboxdataarray.md)
  
- [<span data-ttu-id="95da7-107">MailboxData</span><span class="sxs-lookup"><span data-stu-id="95da7-107">MailboxData</span></span>](mailboxdata.md)
  
```xml
<MailboxData>
   <Email>...</Email>
   <AttendeeType>...</AttendeeType>
   <ExcludeConflicts>...</ExcludeConflicts>
<MailboxData>
```

<span data-ttu-id="95da7-108">**MailboxData**</span><span class="sxs-lookup"><span data-stu-id="95da7-108">**MailboxData**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="95da7-109">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="95da7-109">Attributes and elements</span></span>

<span data-ttu-id="95da7-110">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="95da7-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="95da7-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="95da7-111">Attributes</span></span>

<span data-ttu-id="95da7-112">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="95da7-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="95da7-113">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="95da7-113">Child elements</span></span>

|<span data-ttu-id="95da7-114">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="95da7-114">**Element**</span></span>|<span data-ttu-id="95da7-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="95da7-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="95da7-116">Correo electrónico (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="95da7-116">Email (EmailAddressType)</span></span>](email-emailaddresstype.md) <br/> |<span data-ttu-id="95da7-117">Representa el usuario del buzón de correo para una consulta de GetUserAvailability.</span><span class="sxs-lookup"><span data-stu-id="95da7-117">Represents the mailbox user for a GetUserAvailability query.</span></span>  <br/> |
|[<span data-ttu-id="95da7-118">AttendeeType</span><span class="sxs-lookup"><span data-stu-id="95da7-118">AttendeeType</span></span>](attendeetype.md) <br/> |<span data-ttu-id="95da7-119">Representa el tipo de asistente identificado en el elemento [email (EmailAddressType)](email-emailaddresstype.md) .</span><span class="sxs-lookup"><span data-stu-id="95da7-119">Represents the type of attendee identified in the [Email (EmailAddressType)](email-emailaddresstype.md) element.</span></span> <span data-ttu-id="95da7-120">Se usa en las solicitudes de sugerencias de reunión.</span><span class="sxs-lookup"><span data-stu-id="95da7-120">This is used in requests for meeting suggestions.</span></span>  <br/> |
|[<span data-ttu-id="95da7-121">ExcludeConflicts</span><span class="sxs-lookup"><span data-stu-id="95da7-121">ExcludeConflicts</span></span>](excludeconflicts.md) <br/> |<span data-ttu-id="95da7-122">Especifica si se van a devolver horas sugeridas para las horas del calendario que entran en conflicto entre los asistentes.</span><span class="sxs-lookup"><span data-stu-id="95da7-122">Specifies whether to return suggested times for calendar times that conflict among the attendees.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="95da7-123">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="95da7-123">Parent elements</span></span>

|<span data-ttu-id="95da7-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="95da7-124">**Element**</span></span>|<span data-ttu-id="95da7-125">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="95da7-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="95da7-126">MailboxDataArray</span><span class="sxs-lookup"><span data-stu-id="95da7-126">MailboxDataArray</span></span>](mailboxdataarray.md) <br/> |<span data-ttu-id="95da7-127">Contiene una lista de buzones para consultar la información de disponibilidad.</span><span class="sxs-lookup"><span data-stu-id="95da7-127">Contains a list of mailboxes to query for availability information.</span></span>  <br/> <span data-ttu-id="95da7-128">A continuación se encuentra la expresión XPath de este elemento:</span><span class="sxs-lookup"><span data-stu-id="95da7-128">The following is the XPath to this element:</span></span>  <br/>  `/GetUserAvailabilityRequest/MailboxDataArray[i]` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="95da7-129">Comentarios</span><span class="sxs-lookup"><span data-stu-id="95da7-129">Remarks</span></span>

<span data-ttu-id="95da7-130">Una aplicación cliente puede definir de uno a varios elementos **MailboxData** .</span><span class="sxs-lookup"><span data-stu-id="95da7-130">A client application can define one to many **MailboxData** elements.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="95da7-131">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Exchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="95da7-131">The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange Server 2007 that has the Client Access server role installed.</span></span> 
  
## <a name="example"></a><span data-ttu-id="95da7-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="95da7-132">Example</span></span>

```xml
<MailboxDataArray>
  <MailboxData xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
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

## <a name="element-information"></a><span data-ttu-id="95da7-133">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="95da7-133">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="95da7-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="95da7-134">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="95da7-135">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="95da7-135">Schema Name</span></span>  <br/> |<span data-ttu-id="95da7-136">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="95da7-136">Types schema</span></span>  <br/> |
|<span data-ttu-id="95da7-137">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="95da7-137">Validation File</span></span>  <br/> |<span data-ttu-id="95da7-138">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="95da7-138">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="95da7-139">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="95da7-139">Can be Empty</span></span>  <br/> |<span data-ttu-id="95da7-140">Falso</span><span class="sxs-lookup"><span data-stu-id="95da7-140">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="95da7-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="95da7-141">See also</span></span>

- [<span data-ttu-id="95da7-142">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="95da7-142">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
- [<span data-ttu-id="95da7-143">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="95da7-143">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)
- [<span data-ttu-id="95da7-144">Obtener disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="95da7-144">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

