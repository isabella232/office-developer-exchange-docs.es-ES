---
title: Correo electrónico (EmailAddressType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Email
api_type:
- schema
ms.assetid: dfffa1d5-2c3c-4f56-af63-5853df462e58
description: El elemento de correo electrónico representa al usuario de buzón de correo para una consulta GetUserAvailability.
ms.openlocfilehash: 0e7848d7c4f5001ed86b06d11af1d7623b4bf1f0
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764327"
---
# <a name="email-emailaddresstype"></a><span data-ttu-id="c367b-103">Correo electrónico (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="c367b-103">Email (EmailAddressType)</span></span>

<span data-ttu-id="c367b-104">El elemento de **correo electrónico** representa al usuario de buzón de correo para una consulta GetUserAvailability.</span><span class="sxs-lookup"><span data-stu-id="c367b-104">The **Email** element represents the mailbox user for a GetUserAvailability query.</span></span> 
  
- [<span data-ttu-id="c367b-105">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="c367b-105">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)  
- [<span data-ttu-id="c367b-106">MailboxDataArray</span><span class="sxs-lookup"><span data-stu-id="c367b-106">MailboxDataArray</span></span>](mailboxdataarray.md) 
- [<span data-ttu-id="c367b-107">MailboxData</span><span class="sxs-lookup"><span data-stu-id="c367b-107">MailboxData</span></span>](mailboxdata.md) 
- [<span data-ttu-id="c367b-108">Correo electrónico (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="c367b-108">Email (EmailAddressType)</span></span>](email-emailaddresstype.md)
  
```xml
<Email>
   <Name>...</Name>
   <Address>...</Address>
   <RoutingType>...</RoutingType>
</Email>
```

 <span data-ttu-id="c367b-109">**EmailAddressType**</span><span class="sxs-lookup"><span data-stu-id="c367b-109">**EmailAddressType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c367b-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="c367b-110">Attributes and elements</span></span>

<span data-ttu-id="c367b-111">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="c367b-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c367b-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="c367b-112">Attributes</span></span>

<span data-ttu-id="c367b-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="c367b-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c367b-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c367b-114">Child elements</span></span>

|<span data-ttu-id="c367b-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="c367b-115">**Element**</span></span>|<span data-ttu-id="c367b-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c367b-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c367b-117">Nombre (EmailAddress)</span><span class="sxs-lookup"><span data-stu-id="c367b-117">Name (EmailAddress)</span></span>](name-emailaddress.md) <br/> |<span data-ttu-id="c367b-118">Representa el nombre para mostrar del usuario de buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="c367b-118">Represents the display name of the mailbox user.</span></span>  <br/> |
|[<span data-ttu-id="c367b-119">Dirección (cadena)</span><span class="sxs-lookup"><span data-stu-id="c367b-119">Address (string)</span></span>](address-string.md) <br/> |<span data-ttu-id="c367b-120">Representa la dirección de correo electrónico del usuario de buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="c367b-120">Represents the e-mail address of the mailbox user.</span></span>  <br/> |
|[<span data-ttu-id="c367b-121">RoutingType (EmailAddress)</span><span class="sxs-lookup"><span data-stu-id="c367b-121">RoutingType (EmailAddress)</span></span>](routingtype-emailaddress.md) <br/> |<span data-ttu-id="c367b-122">Representa el protocolo de enrutamiento para el mensaje.</span><span class="sxs-lookup"><span data-stu-id="c367b-122">Represents the routing protocol for the message.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="c367b-123">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="c367b-123">Parent elements</span></span>

|<span data-ttu-id="c367b-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="c367b-124">**Element**</span></span>|<span data-ttu-id="c367b-125">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c367b-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c367b-126">MailboxData</span><span class="sxs-lookup"><span data-stu-id="c367b-126">MailboxData</span></span>](mailboxdata.md) <br/> |<span data-ttu-id="c367b-127">Representa un usuario de buzón de correo individual y opciones para el tipo de datos que se devolverá sobre el usuario del buzón.</span><span class="sxs-lookup"><span data-stu-id="c367b-127">Represents an individual mailbox user and options for the type of data to be returned about the mailbox user.</span></span>  <br/> <span data-ttu-id="c367b-128">La siguiente es la expresión de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="c367b-128">The following is the XPath to this element:</span></span>  <br/>  `/GetUserAvailabilityRequest/MailboxDataArray[i]/MailboxData` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c367b-129">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c367b-129">Remarks</span></span>

<span data-ttu-id="c367b-130">El esquema que describe este elemento se encuentra en el directorio /EWS/ del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="c367b-130">The schema that describes this element is located in the /EWS/ directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c367b-131">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="c367b-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c367b-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c367b-132">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c367b-133">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="c367b-133">Schema Name</span></span>  <br/> |<span data-ttu-id="c367b-134">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="c367b-134">Types schema</span></span>  <br/> |
|<span data-ttu-id="c367b-135">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="c367b-135">Validation File</span></span>  <br/> |<span data-ttu-id="c367b-136">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="c367b-136">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="c367b-137">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="c367b-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="c367b-138">False</span><span class="sxs-lookup"><span data-stu-id="c367b-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c367b-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="c367b-139">See also</span></span>

- [<span data-ttu-id="c367b-140">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="c367b-140">GetUserAvailability operation</span></span>](getuseravailability-operation.md)  
- [<span data-ttu-id="c367b-141">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="c367b-141">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)
- [<span data-ttu-id="c367b-142">Obtención de disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="c367b-142">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

