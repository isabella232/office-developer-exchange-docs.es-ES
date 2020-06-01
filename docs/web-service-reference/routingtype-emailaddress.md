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
ms.openlocfilehash: 2193e72c38c687669f6e052b4d2526029aa89d89
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459037"
---
# <a name="routingtype-emailaddress"></a><span data-ttu-id="11996-103">RoutingType (EmailAddress)</span><span class="sxs-lookup"><span data-stu-id="11996-103">RoutingType (EmailAddress)</span></span>

<span data-ttu-id="11996-104">El elemento **RoutingType** representa el protocolo de enrutamiento para el destinatario.</span><span class="sxs-lookup"><span data-stu-id="11996-104">The **RoutingType** element represents the routing protocol for the recipient.</span></span> 
  
```XML
<RoutingType/>
```

 <span data-ttu-id="11996-105">**string**</span><span class="sxs-lookup"><span data-stu-id="11996-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="11996-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="11996-106">Attributes and elements</span></span>

<span data-ttu-id="11996-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="11996-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="11996-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="11996-108">Attributes</span></span>

<span data-ttu-id="11996-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="11996-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="11996-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="11996-110">Child elements</span></span>

<span data-ttu-id="11996-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="11996-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="11996-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="11996-112">Parent elements</span></span>

|<span data-ttu-id="11996-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="11996-113">**Element**</span></span>|<span data-ttu-id="11996-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="11996-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="11996-115">Correo electrónico (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="11996-115">Email (EmailAddressType)</span></span>](email-emailaddresstype.md) <br/> |<span data-ttu-id="11996-116">Especifica la dirección de correo electrónico del objeto MailboxData.</span><span class="sxs-lookup"><span data-stu-id="11996-116">Specifies the e-mail address of the MailboxData object.</span></span> <span data-ttu-id="11996-117">Este elemento se usa en la [operación GetUserAvailability](getuseravailability-operation.md).</span><span class="sxs-lookup"><span data-stu-id="11996-117">This element is used in the [GetUserAvailability operation](getuseravailability-operation.md).</span></span>  <br/><br/> <span data-ttu-id="11996-118">A continuación se encuentra la expresión XPath de este elemento:</span><span class="sxs-lookup"><span data-stu-id="11996-118">The following is the XPath to this element:</span></span>  <br/><br/>  `/GetUserAvailabilityRequest/MailboxDataArray/MailboxData[i]/Email` <br/> |
|[<span data-ttu-id="11996-119">Buzón de correo (disponibilidad)</span><span class="sxs-lookup"><span data-stu-id="11996-119">Mailbox (Availability)</span></span>](mailbox-availability.md) <br/> | <span data-ttu-id="11996-120">Representa el usuario del buzón de correo para una solicitud SetUserOofSettings o GetUserOofSettings.</span><span class="sxs-lookup"><span data-stu-id="11996-120">Represents the mailbox user for a SetUserOofSettings or GetUserOofSettings request.</span></span>  <br/><br/>  <span data-ttu-id="11996-121">Las siguientes son las expresiones XPath de este elemento:</span><span class="sxs-lookup"><span data-stu-id="11996-121">The following are the XPath expressions to this element:</span></span> <br/> <br/>  `/GetUserOofSettingsRequest/Mailbox` <br/><br/>  `/SetUserOofSettingsRequest/Mailbox` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="11996-122">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="11996-122">Text value</span></span>

<span data-ttu-id="11996-123">Un valor de texto es opcional.</span><span class="sxs-lookup"><span data-stu-id="11996-123">A text value is optional.</span></span> <span data-ttu-id="11996-124">Los valores posibles son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="11996-124">The following are the possible values:</span></span>

* <span data-ttu-id="11996-125">SMTP</span><span class="sxs-lookup"><span data-stu-id="11996-125">SMTP</span></span>
* <span data-ttu-id="11996-126">PRECIO</span><span class="sxs-lookup"><span data-stu-id="11996-126">EX</span></span>

<span data-ttu-id="11996-127">Si no se proporciona ningún valor, se usa el valor predeterminado de SMTP.</span><span class="sxs-lookup"><span data-stu-id="11996-127">If no value is provided, the default value of SMTP is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="11996-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="11996-128">Remarks</span></span>

<span data-ttu-id="11996-129">Este elemento se puede producir al menos una vez en el elemento [email (EmailAddressType)](email-emailaddresstype.md) .</span><span class="sxs-lookup"><span data-stu-id="11996-129">This element can occur at most one time in the [Email (EmailAddressType)](email-emailaddresstype.md) element.</span></span> <span data-ttu-id="11996-130">Este elemento no es obligatorio.</span><span class="sxs-lookup"><span data-stu-id="11996-130">This element is not required.</span></span> <span data-ttu-id="11996-131">Este elemento existe para la inclusión de protocolos futuros.</span><span class="sxs-lookup"><span data-stu-id="11996-131">This element exists for the inclusion of future protocols.</span></span> <span data-ttu-id="11996-132">Se usa otro elemento **RoutingType** para obtener acceso a los elementos del buzón de un usuario.</span><span class="sxs-lookup"><span data-stu-id="11996-132">Another **RoutingType** element is used for accessing items in a user's mailbox.</span></span> 
  
<span data-ttu-id="11996-133">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="11996-133">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="11996-134">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="11996-134">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="11996-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="11996-135">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="11996-136">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="11996-136">Schema Name</span></span>  <br/> |<span data-ttu-id="11996-137">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="11996-137">Types schema</span></span>  <br/> |
|<span data-ttu-id="11996-138">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="11996-138">Validation File</span></span>  <br/> |<span data-ttu-id="11996-139">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="11996-139">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="11996-140">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="11996-140">Can be Empty</span></span>  <br/> |<span data-ttu-id="11996-141">Falso</span><span class="sxs-lookup"><span data-stu-id="11996-141">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="11996-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="11996-142">See also</span></span>

- [<span data-ttu-id="11996-143">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="11996-143">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
- [<span data-ttu-id="11996-144">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="11996-144">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)
- [<span data-ttu-id="11996-145">Obtener disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="11996-145">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

