---
title: Dirección (cadena)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Address
api_type:
- schema
ms.assetid: a3cdfcbd-d0c5-46d6-8daa-52405fc63ff0
description: El elemento dirección representa la dirección de correo electrónico del usuario de buzón de correo.
ms.openlocfilehash: 07c634d6166d88a8912bc66081a13671e600c801
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763415"
---
# <a name="address-string"></a><span data-ttu-id="4ad72-103">Dirección (cadena)</span><span class="sxs-lookup"><span data-stu-id="4ad72-103">Address (string)</span></span>

<span data-ttu-id="4ad72-104">El elemento **dirección** representa la dirección de correo electrónico del usuario de buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="4ad72-104">The **Address** element represents the e-mail address of the mailbox user.</span></span> 
  
```xml
<Address>...</Address>
```

 <span data-ttu-id="4ad72-105">**string**</span><span class="sxs-lookup"><span data-stu-id="4ad72-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4ad72-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="4ad72-106">Attributes and elements</span></span>

<span data-ttu-id="4ad72-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="4ad72-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4ad72-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="4ad72-108">Attributes</span></span>

<span data-ttu-id="4ad72-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="4ad72-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4ad72-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="4ad72-110">Child elements</span></span>

<span data-ttu-id="4ad72-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="4ad72-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="4ad72-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="4ad72-112">Parent elements</span></span>

|<span data-ttu-id="4ad72-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="4ad72-113">**Element**</span></span>|<span data-ttu-id="4ad72-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4ad72-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4ad72-115">Correo electrónico (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="4ad72-115">Email (EmailAddressType)</span></span>](email-emailaddresstype.md) <br/> |<span data-ttu-id="4ad72-116">Especifica la dirección de correo electrónico del objeto MailboxData.</span><span class="sxs-lookup"><span data-stu-id="4ad72-116">Specifies the e-mail address of the MailboxData object.</span></span> <span data-ttu-id="4ad72-117">Este elemento se usa en la [operación GetUserAvailability](getuseravailability-operation.md).</span><span class="sxs-lookup"><span data-stu-id="4ad72-117">This element is used in the [GetUserAvailability operation](getuseravailability-operation.md).</span></span><br/><br/> <span data-ttu-id="4ad72-118">La siguiente es la expresión de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="4ad72-118">The following is the XPath to this element:</span></span><br/><br/>  `/GetUserAvailabilityRequest/MailboxDataArray/MailboxData[i]/Email` <br/> |
|[<span data-ttu-id="4ad72-119">Buzón de correo (disponibilidad)</span><span class="sxs-lookup"><span data-stu-id="4ad72-119">Mailbox (Availability)</span></span>](mailbox-availability.md) <br/> | <span data-ttu-id="4ad72-120">Representa el usuario del buzón para una solicitud SetUserOofSettings o GetUserOofSettings.</span><span class="sxs-lookup"><span data-stu-id="4ad72-120">Represents the mailbox user for a SetUserOofSettings or GetUserOofSettings request.</span></span><br/><br/>  <span data-ttu-id="4ad72-121">Los siguientes son las expresiones de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="4ad72-121">The following are the XPath expressions to this element:</span></span><br/><br/>  `/GetUserOofSettingsRequest/Mailbox` <br/>  `/SetUserOofSettingsRequest/Mailbox` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="4ad72-122">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="4ad72-122">Text value</span></span>

<span data-ttu-id="4ad72-123">Si se usa este elemento, se requiere un valor de texto.</span><span class="sxs-lookup"><span data-stu-id="4ad72-123">A text value is required if this element is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4ad72-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4ad72-124">Remarks</span></span>

<span data-ttu-id="4ad72-125">Este elemento puede aparecer como máximo una vez en el elemento de [correo electrónico (EmailAddressType)](email-emailaddresstype.md) y el elemento de [buzón de correo (disponibilidad)](mailbox-availability.md) .</span><span class="sxs-lookup"><span data-stu-id="4ad72-125">This element can occur at most one time in the [Email (EmailAddressType)](email-emailaddresstype.md) element and the [Mailbox (Availability)](mailbox-availability.md) element.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="4ad72-126">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="4ad72-126">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="4ad72-127">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="4ad72-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4ad72-128">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="4ad72-128">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="4ad72-129">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="4ad72-129">Schema Name</span></span>  <br/> |<span data-ttu-id="4ad72-130">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="4ad72-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="4ad72-131">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="4ad72-131">Validation File</span></span>  <br/> |<span data-ttu-id="4ad72-132">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="4ad72-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="4ad72-133">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="4ad72-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="4ad72-134">False</span><span class="sxs-lookup"><span data-stu-id="4ad72-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4ad72-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="4ad72-135">See also</span></span>

- [<span data-ttu-id="4ad72-136">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="4ad72-136">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
- [<span data-ttu-id="4ad72-137">Operación GetUserOofSettings</span><span class="sxs-lookup"><span data-stu-id="4ad72-137">GetUserOofSettings operation</span></span>](getuseroofsettings-operation.md)
- [<span data-ttu-id="4ad72-138">Operación SetUserOofSettings</span><span class="sxs-lookup"><span data-stu-id="4ad72-138">SetUserOofSettings operation</span></span>](setuseroofsettings-operation.md)
- [<span data-ttu-id="4ad72-139">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="4ad72-139">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)
- [<span data-ttu-id="4ad72-140">GetUserOofSettingsRequest</span><span class="sxs-lookup"><span data-stu-id="4ad72-140">GetUserOofSettingsRequest</span></span>](getuseroofsettingsrequest.md)
- [<span data-ttu-id="4ad72-141">SetUserOofSettingsRequest</span><span class="sxs-lookup"><span data-stu-id="4ad72-141">SetUserOofSettingsRequest</span></span>](setuseroofsettingsrequest.md)
- [<span data-ttu-id="4ad72-142">Obtención de disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="4ad72-142">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

