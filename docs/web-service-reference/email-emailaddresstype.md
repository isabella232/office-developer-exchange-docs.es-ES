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
description: El elemento email representa al usuario del buzón de una consulta de GetUserAvailability.
ms.openlocfilehash: 2ed8de9c011a385ec6c4ebd2f8d1d47304343a0e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459233"
---
# <a name="email-emailaddresstype"></a><span data-ttu-id="8e444-103">Correo electrónico (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="8e444-103">Email (EmailAddressType)</span></span>

<span data-ttu-id="8e444-104">El elemento **email** representa al usuario del buzón de una consulta de GetUserAvailability.</span><span class="sxs-lookup"><span data-stu-id="8e444-104">The **Email** element represents the mailbox user for a GetUserAvailability query.</span></span> 
  
- [<span data-ttu-id="8e444-105">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="8e444-105">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)  
- [<span data-ttu-id="8e444-106">MailboxDataArray</span><span class="sxs-lookup"><span data-stu-id="8e444-106">MailboxDataArray</span></span>](mailboxdataarray.md) 
- [<span data-ttu-id="8e444-107">MailboxData</span><span class="sxs-lookup"><span data-stu-id="8e444-107">MailboxData</span></span>](mailboxdata.md) 
- [<span data-ttu-id="8e444-108">Correo electrónico (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="8e444-108">Email (EmailAddressType)</span></span>](email-emailaddresstype.md)
  
```xml
<Email>
   <Name>...</Name>
   <Address>...</Address>
   <RoutingType>...</RoutingType>
</Email>
```

 <span data-ttu-id="8e444-109">**EmailAddressType**</span><span class="sxs-lookup"><span data-stu-id="8e444-109">**EmailAddressType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="8e444-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="8e444-110">Attributes and elements</span></span>

<span data-ttu-id="8e444-111">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="8e444-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8e444-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="8e444-112">Attributes</span></span>

<span data-ttu-id="8e444-113">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="8e444-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="8e444-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="8e444-114">Child elements</span></span>

|<span data-ttu-id="8e444-115">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="8e444-115">**Element**</span></span>|<span data-ttu-id="8e444-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8e444-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8e444-117">Nombre (EmailAddress)</span><span class="sxs-lookup"><span data-stu-id="8e444-117">Name (EmailAddress)</span></span>](name-emailaddress.md) <br/> |<span data-ttu-id="8e444-118">Representa el nombre para mostrar del usuario del buzón.</span><span class="sxs-lookup"><span data-stu-id="8e444-118">Represents the display name of the mailbox user.</span></span>  <br/> |
|[<span data-ttu-id="8e444-119">Address (cadena)</span><span class="sxs-lookup"><span data-stu-id="8e444-119">Address (string)</span></span>](address-string.md) <br/> |<span data-ttu-id="8e444-120">Representa la dirección de correo electrónico del usuario del buzón.</span><span class="sxs-lookup"><span data-stu-id="8e444-120">Represents the e-mail address of the mailbox user.</span></span>  <br/> |
|[<span data-ttu-id="8e444-121">RoutingType (EmailAddress)</span><span class="sxs-lookup"><span data-stu-id="8e444-121">RoutingType (EmailAddress)</span></span>](routingtype-emailaddress.md) <br/> |<span data-ttu-id="8e444-122">Representa el protocolo de enrutamiento para el mensaje.</span><span class="sxs-lookup"><span data-stu-id="8e444-122">Represents the routing protocol for the message.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="8e444-123">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="8e444-123">Parent elements</span></span>

|<span data-ttu-id="8e444-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="8e444-124">**Element**</span></span>|<span data-ttu-id="8e444-125">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8e444-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8e444-126">MailboxData</span><span class="sxs-lookup"><span data-stu-id="8e444-126">MailboxData</span></span>](mailboxdata.md) <br/> |<span data-ttu-id="8e444-127">Representa un usuario de buzón individual y opciones para el tipo de datos que se devolverán sobre el usuario del buzón.</span><span class="sxs-lookup"><span data-stu-id="8e444-127">Represents an individual mailbox user and options for the type of data to be returned about the mailbox user.</span></span>  <br/> <span data-ttu-id="8e444-128">A continuación se encuentra la expresión XPath de este elemento:</span><span class="sxs-lookup"><span data-stu-id="8e444-128">The following is the XPath to this element:</span></span>  <br/>  `/GetUserAvailabilityRequest/MailboxDataArray[i]/MailboxData` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8e444-129">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8e444-129">Remarks</span></span>

<span data-ttu-id="8e444-130">El esquema que describe este elemento se encuentra en el directorio/EWS/del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="8e444-130">The schema that describes this element is located in the /EWS/ directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8e444-131">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="8e444-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8e444-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="8e444-132">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="8e444-133">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="8e444-133">Schema Name</span></span>  <br/> |<span data-ttu-id="8e444-134">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="8e444-134">Types schema</span></span>  <br/> |
|<span data-ttu-id="8e444-135">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="8e444-135">Validation File</span></span>  <br/> |<span data-ttu-id="8e444-136">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="8e444-136">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="8e444-137">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="8e444-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="8e444-138">Falso</span><span class="sxs-lookup"><span data-stu-id="8e444-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8e444-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="8e444-139">See also</span></span>

- [<span data-ttu-id="8e444-140">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="8e444-140">GetUserAvailability operation</span></span>](getuseravailability-operation.md)  
- [<span data-ttu-id="8e444-141">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="8e444-141">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)
- [<span data-ttu-id="8e444-142">Obtener disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="8e444-142">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

