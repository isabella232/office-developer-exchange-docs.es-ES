---
title: RoutingType (EmailAddress)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RoutingType
api_type:
- schema
ms.assetid: 74d83198-0d9d-4c78-a2bc-9a671859ff37
description: El elemento RoutingType representa el protocolo de enrutamiento para el destinatario.
ms.openlocfilehash: a0a6cf312bcb1d4b4818a82bc8d8d3e3f33ad6f6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19837255"
---
# <a name="routingtype-emailaddress"></a><span data-ttu-id="94c8b-103">RoutingType (EmailAddress)</span><span class="sxs-lookup"><span data-stu-id="94c8b-103">RoutingType (EmailAddress)</span></span>

<span data-ttu-id="94c8b-104">El elemento **RoutingType** representa el protocolo de enrutamiento para el destinatario.</span><span class="sxs-lookup"><span data-stu-id="94c8b-104">The **RoutingType** element represents the routing protocol for the recipient.</span></span> 
  
```XML
<RoutingType/>
```

 <span data-ttu-id="94c8b-105">**string**</span><span class="sxs-lookup"><span data-stu-id="94c8b-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="94c8b-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="94c8b-106">Attributes and elements</span></span>

<span data-ttu-id="94c8b-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="94c8b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="94c8b-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="94c8b-108">Attributes</span></span>

<span data-ttu-id="94c8b-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="94c8b-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="94c8b-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="94c8b-110">Child elements</span></span>

<span data-ttu-id="94c8b-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="94c8b-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="94c8b-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="94c8b-112">Parent elements</span></span>

|<span data-ttu-id="94c8b-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="94c8b-113">**Element**</span></span>|<span data-ttu-id="94c8b-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="94c8b-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="94c8b-115">Correo electrónico (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="94c8b-115">Email (EmailAddressType)</span></span>](email-emailaddresstype.md) <br/> |<span data-ttu-id="94c8b-116">Especifica la dirección de correo electrónico del objeto MailboxData.</span><span class="sxs-lookup"><span data-stu-id="94c8b-116">Specifies the e-mail address of the MailboxData object.</span></span> <span data-ttu-id="94c8b-117">Este elemento se usa en la [operación GetUserAvailability](getuseravailability-operation.md).</span><span class="sxs-lookup"><span data-stu-id="94c8b-117">This element is used in the [GetUserAvailability operation](getuseravailability-operation.md).</span></span>  <br/><br/> <span data-ttu-id="94c8b-118">La siguiente es la expresión de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="94c8b-118">The following is the XPath to this element:</span></span>  <br/><br/>  `/GetUserAvailabilityRequest/MailboxDataArray/MailboxData[i]/Email` <br/> |
|[<span data-ttu-id="94c8b-119">Buzón de correo (disponibilidad)</span><span class="sxs-lookup"><span data-stu-id="94c8b-119">Mailbox (Availability)</span></span>](mailbox-availability.md) <br/> | <span data-ttu-id="94c8b-120">Representa el usuario del buzón para una solicitud SetUserOofSettings o GetUserOofSettings.</span><span class="sxs-lookup"><span data-stu-id="94c8b-120">Represents the mailbox user for a SetUserOofSettings or GetUserOofSettings request.</span></span>  <br/><br/>  <span data-ttu-id="94c8b-121">Los siguientes son las expresiones de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="94c8b-121">The following are the XPath expressions to this element:</span></span> <br/> <br/>  `/GetUserOofSettingsRequest/Mailbox` <br/><br/>  `/SetUserOofSettingsRequest/Mailbox` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="94c8b-122">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="94c8b-122">Text value</span></span>

<span data-ttu-id="94c8b-123">Un valor de texto es opcional.</span><span class="sxs-lookup"><span data-stu-id="94c8b-123">A text value is optional.</span></span> <span data-ttu-id="94c8b-124">El único valor válido es SMTP.</span><span class="sxs-lookup"><span data-stu-id="94c8b-124">The only valid value is SMTP.</span></span> <span data-ttu-id="94c8b-125">Si no se proporciona ningún valor, se usa el valor predeterminado de SMTP.</span><span class="sxs-lookup"><span data-stu-id="94c8b-125">If no value is provided, the default value of SMTP is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="94c8b-126">Notas</span><span class="sxs-lookup"><span data-stu-id="94c8b-126">Remarks</span></span>

<span data-ttu-id="94c8b-127">Este elemento puede aparecer como máximo una vez en el elemento de [correo electrónico (EmailAddressType)](email-emailaddresstype.md) .</span><span class="sxs-lookup"><span data-stu-id="94c8b-127">This element can occur at most one time in the [Email (EmailAddressType)](email-emailaddresstype.md) element.</span></span> <span data-ttu-id="94c8b-128">Este elemento no es necesario.</span><span class="sxs-lookup"><span data-stu-id="94c8b-128">This element is not required.</span></span> <span data-ttu-id="94c8b-129">Este elemento existe para la inclusión de protocolos futuros.</span><span class="sxs-lookup"><span data-stu-id="94c8b-129">This element exists for the inclusion of future protocols.</span></span> <span data-ttu-id="94c8b-130">Otro elemento de **RoutingType** se usa para obtener acceso a los elementos en el buzón del usuario.</span><span class="sxs-lookup"><span data-stu-id="94c8b-130">Another **RoutingType** element is used for accessing items in a user's mailbox.</span></span> 
  
<span data-ttu-id="94c8b-131">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="94c8b-131">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="94c8b-132">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="94c8b-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="94c8b-133">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="94c8b-133">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="94c8b-134">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="94c8b-134">Schema Name</span></span>  <br/> |<span data-ttu-id="94c8b-135">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="94c8b-135">Types schema</span></span>  <br/> |
|<span data-ttu-id="94c8b-136">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="94c8b-136">Validation File</span></span>  <br/> |<span data-ttu-id="94c8b-137">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="94c8b-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="94c8b-138">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="94c8b-138">Can be Empty</span></span>  <br/> |<span data-ttu-id="94c8b-139">False</span><span class="sxs-lookup"><span data-stu-id="94c8b-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="94c8b-140">Ver también</span><span class="sxs-lookup"><span data-stu-id="94c8b-140">See also</span></span>

- [<span data-ttu-id="94c8b-141">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="94c8b-141">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
- [<span data-ttu-id="94c8b-142">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="94c8b-142">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)
- [<span data-ttu-id="94c8b-143">Obtención de disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="94c8b-143">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

