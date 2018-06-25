---
title: Nombre (EmailAddress)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Name
api_type:
- schema
ms.assetid: c719c55f-d625-4e64-846f-50ac91881443
description: El elemento Name representa el nombre para mostrar del usuario de buzón de correo.
ms.openlocfilehash: 6d30f06c3bfd77d2715798349ab084cdf81f21a6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836505"
---
# <a name="name-emailaddress"></a><span data-ttu-id="4e2c4-103">Nombre (EmailAddress)</span><span class="sxs-lookup"><span data-stu-id="4e2c4-103">Name (EmailAddress)</span></span>

<span data-ttu-id="4e2c4-104">El elemento **Name** representa el nombre para mostrar del usuario de buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="4e2c4-104">The **Name** element represents the display name of the mailbox user.</span></span> 
  
```xml
<Name/>
```

<span data-ttu-id="4e2c4-105">**String**</span><span class="sxs-lookup"><span data-stu-id="4e2c4-105">**String**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="4e2c4-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="4e2c4-106">Attributes and elements</span></span>

<span data-ttu-id="4e2c4-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="4e2c4-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4e2c4-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="4e2c4-108">Attributes</span></span>

<span data-ttu-id="4e2c4-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="4e2c4-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4e2c4-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="4e2c4-110">Child elements</span></span>

<span data-ttu-id="4e2c4-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="4e2c4-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="4e2c4-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="4e2c4-112">Parent elements</span></span>

|<span data-ttu-id="4e2c4-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="4e2c4-113">**Element**</span></span>|<span data-ttu-id="4e2c4-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4e2c4-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4e2c4-115">Correo electrónico (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="4e2c4-115">Email (EmailAddressType)</span></span>](email-emailaddresstype.md) <br/> |<span data-ttu-id="4e2c4-116">Representa el usuario del buzón para una consulta GetUserAvailability.</span><span class="sxs-lookup"><span data-stu-id="4e2c4-116">Represents the mailbox user for a GetUserAvailability query.</span></span>  <br/> <br/><span data-ttu-id="4e2c4-117">La siguiente es la expresión de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="4e2c4-117">The following is the XPath to this element:</span></span>  <br/><br/>  `/GetUserAvailabilityRequest/MailboxDataArray/MailboxData[i]/Email` <br/> |
|[<span data-ttu-id="4e2c4-118">Buzón de correo (disponibilidad)</span><span class="sxs-lookup"><span data-stu-id="4e2c4-118">Mailbox (Availability)</span></span>](mailbox-availability.md) <br/> | <span data-ttu-id="4e2c4-119">Representa el usuario del buzón para una solicitud SetUserOofSettings o GetUserOofSettings.</span><span class="sxs-lookup"><span data-stu-id="4e2c4-119">Represents the mailbox user for a SetUserOofSettings or GetUserOofSettings request.</span></span>  <br/><br/>  <span data-ttu-id="4e2c4-120">Los siguientes son las expresiones de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="4e2c4-120">The following are the XPath expressions to this element:</span></span>  <br/><br/>  `/GetUserOofSettingsRequest/Mailbox` <br/><br/>  `/SetUserOofSettingsRequest/Mailbox` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="4e2c4-121">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="4e2c4-121">Text value</span></span>

<span data-ttu-id="4e2c4-122">Si se usa este elemento, se requiere un valor de texto.</span><span class="sxs-lookup"><span data-stu-id="4e2c4-122">A text value is required if this element is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4e2c4-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4e2c4-123">Remarks</span></span>

<span data-ttu-id="4e2c4-124">Este elemento puede aparecer como máximo una vez en el elemento de [correo electrónico (EmailAddressType)](email-emailaddresstype.md) .</span><span class="sxs-lookup"><span data-stu-id="4e2c4-124">This element can occur at most one time in the [Email (EmailAddressType)](email-emailaddresstype.md) element.</span></span> <span data-ttu-id="4e2c4-125">Este elemento no es necesario.</span><span class="sxs-lookup"><span data-stu-id="4e2c4-125">This element is not required.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="4e2c4-126">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="4e2c4-126">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="4e2c4-127">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="4e2c4-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4e2c4-128">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="4e2c4-128">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="4e2c4-129">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="4e2c4-129">Schema Name</span></span>  <br/> |<span data-ttu-id="4e2c4-130">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="4e2c4-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="4e2c4-131">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="4e2c4-131">Validation File</span></span>  <br/> |<span data-ttu-id="4e2c4-132">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="4e2c4-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="4e2c4-133">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="4e2c4-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="4e2c4-134">False</span><span class="sxs-lookup"><span data-stu-id="4e2c4-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4e2c4-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="4e2c4-135">See also</span></span>

- [<span data-ttu-id="4e2c4-136">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="4e2c4-136">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
- [<span data-ttu-id="4e2c4-137">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="4e2c4-137">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)
- [<span data-ttu-id="4e2c4-138">Obtención de disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="4e2c4-138">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

