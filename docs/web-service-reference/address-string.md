---
title: Address (cadena)
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
description: El elemento Address representa la dirección de correo electrónico del usuario del buzón.
ms.openlocfilehash: 839107050f22df5c00cb4dea9c531563df52933d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463646"
---
# <a name="address-string"></a><span data-ttu-id="c924c-103">Address (cadena)</span><span class="sxs-lookup"><span data-stu-id="c924c-103">Address (string)</span></span>

<span data-ttu-id="c924c-104">El elemento **Address** representa la dirección de correo electrónico del usuario del buzón.</span><span class="sxs-lookup"><span data-stu-id="c924c-104">The **Address** element represents the e-mail address of the mailbox user.</span></span> 
  
```xml
<Address>...</Address>
```

 <span data-ttu-id="c924c-105">**string**</span><span class="sxs-lookup"><span data-stu-id="c924c-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c924c-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="c924c-106">Attributes and elements</span></span>

<span data-ttu-id="c924c-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="c924c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c924c-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="c924c-108">Attributes</span></span>

<span data-ttu-id="c924c-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="c924c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c924c-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c924c-110">Child elements</span></span>

<span data-ttu-id="c924c-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="c924c-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="c924c-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="c924c-112">Parent elements</span></span>

|<span data-ttu-id="c924c-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="c924c-113">**Element**</span></span>|<span data-ttu-id="c924c-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c924c-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c924c-115">Correo electrónico (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="c924c-115">Email (EmailAddressType)</span></span>](email-emailaddresstype.md) <br/> |<span data-ttu-id="c924c-116">Especifica la dirección de correo electrónico del objeto MailboxData.</span><span class="sxs-lookup"><span data-stu-id="c924c-116">Specifies the e-mail address of the MailboxData object.</span></span> <span data-ttu-id="c924c-117">Este elemento se usa en la [operación GetUserAvailability](getuseravailability-operation.md).</span><span class="sxs-lookup"><span data-stu-id="c924c-117">This element is used in the [GetUserAvailability operation](getuseravailability-operation.md).</span></span><br/><br/> <span data-ttu-id="c924c-118">A continuación se encuentra la expresión XPath de este elemento:</span><span class="sxs-lookup"><span data-stu-id="c924c-118">The following is the XPath to this element:</span></span><br/><br/>  `/GetUserAvailabilityRequest/MailboxDataArray/MailboxData[i]/Email` <br/> |
|[<span data-ttu-id="c924c-119">Buzón de correo (disponibilidad)</span><span class="sxs-lookup"><span data-stu-id="c924c-119">Mailbox (Availability)</span></span>](mailbox-availability.md) <br/> | <span data-ttu-id="c924c-120">Representa el usuario del buzón de correo para una solicitud SetUserOofSettings o GetUserOofSettings.</span><span class="sxs-lookup"><span data-stu-id="c924c-120">Represents the mailbox user for a SetUserOofSettings or GetUserOofSettings request.</span></span><br/><br/>  <span data-ttu-id="c924c-121">Las siguientes son las expresiones XPath de este elemento:</span><span class="sxs-lookup"><span data-stu-id="c924c-121">The following are the XPath expressions to this element:</span></span><br/><br/>  `/GetUserOofSettingsRequest/Mailbox` <br/>  `/SetUserOofSettingsRequest/Mailbox` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="c924c-122">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="c924c-122">Text value</span></span>

<span data-ttu-id="c924c-123">Es necesario un valor de texto si se usa este elemento.</span><span class="sxs-lookup"><span data-stu-id="c924c-123">A text value is required if this element is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c924c-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c924c-124">Remarks</span></span>

<span data-ttu-id="c924c-125">Este elemento se puede producir al menos una vez en el elemento [email (EmailAddressType)](email-emailaddresstype.md) y en el elemento [Mailbox (Availability)](mailbox-availability.md) .</span><span class="sxs-lookup"><span data-stu-id="c924c-125">This element can occur at most one time in the [Email (EmailAddressType)](email-emailaddresstype.md) element and the [Mailbox (Availability)](mailbox-availability.md) element.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="c924c-126">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="c924c-126">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="c924c-127">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="c924c-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c924c-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="c924c-128">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c924c-129">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="c924c-129">Schema Name</span></span>  <br/> |<span data-ttu-id="c924c-130">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="c924c-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="c924c-131">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="c924c-131">Validation File</span></span>  <br/> |<span data-ttu-id="c924c-132">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="c924c-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="c924c-133">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="c924c-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="c924c-134">Falso</span><span class="sxs-lookup"><span data-stu-id="c924c-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c924c-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="c924c-135">See also</span></span>

- [<span data-ttu-id="c924c-136">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="c924c-136">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
- [<span data-ttu-id="c924c-137">Operación GetUserOofSettings</span><span class="sxs-lookup"><span data-stu-id="c924c-137">GetUserOofSettings operation</span></span>](getuseroofsettings-operation.md)
- [<span data-ttu-id="c924c-138">Operación SetUserOofSettings</span><span class="sxs-lookup"><span data-stu-id="c924c-138">SetUserOofSettings operation</span></span>](setuseroofsettings-operation.md)
- [<span data-ttu-id="c924c-139">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="c924c-139">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)
- [<span data-ttu-id="c924c-140">GetUserOofSettingsRequest</span><span class="sxs-lookup"><span data-stu-id="c924c-140">GetUserOofSettingsRequest</span></span>](getuseroofsettingsrequest.md)
- [<span data-ttu-id="c924c-141">SetUserOofSettingsRequest</span><span class="sxs-lookup"><span data-stu-id="c924c-141">SetUserOofSettingsRequest</span></span>](setuseroofsettingsrequest.md)
- [<span data-ttu-id="c924c-142">Obtener disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="c924c-142">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

