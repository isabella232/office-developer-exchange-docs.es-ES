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
description: El elemento Name representa el nombre para mostrar del usuario del buzón.
ms.openlocfilehash: 2c6b29f1b069f9cc72ac84e7aebfff99437e630a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/01/2020
ms.locfileid: "44466958"
---
# <a name="name-emailaddress"></a><span data-ttu-id="cac62-103">Nombre (EmailAddress)</span><span class="sxs-lookup"><span data-stu-id="cac62-103">Name (EmailAddress)</span></span>

<span data-ttu-id="cac62-104">El elemento **Name** representa el nombre para mostrar del usuario del buzón.</span><span class="sxs-lookup"><span data-stu-id="cac62-104">The **Name** element represents the display name of the mailbox user.</span></span> 
  
```xml
<Name/>
```

<span data-ttu-id="cac62-105">**String**</span><span class="sxs-lookup"><span data-stu-id="cac62-105">**String**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="cac62-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="cac62-106">Attributes and elements</span></span>

<span data-ttu-id="cac62-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="cac62-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cac62-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="cac62-108">Attributes</span></span>

<span data-ttu-id="cac62-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="cac62-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="cac62-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="cac62-110">Child elements</span></span>

<span data-ttu-id="cac62-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="cac62-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="cac62-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="cac62-112">Parent elements</span></span>

|<span data-ttu-id="cac62-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="cac62-113">**Element**</span></span>|<span data-ttu-id="cac62-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="cac62-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cac62-115">Correo electrónico (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="cac62-115">Email (EmailAddressType)</span></span>](email-emailaddresstype.md) <br/> |<span data-ttu-id="cac62-116">Representa el usuario del buzón de correo para una consulta de GetUserAvailability.</span><span class="sxs-lookup"><span data-stu-id="cac62-116">Represents the mailbox user for a GetUserAvailability query.</span></span>  <br/> <br/><span data-ttu-id="cac62-117">A continuación se encuentra la expresión XPath de este elemento:</span><span class="sxs-lookup"><span data-stu-id="cac62-117">The following is the XPath to this element:</span></span>  <br/><br/>  `/GetUserAvailabilityRequest/MailboxDataArray/MailboxData[i]/Email` <br/> |
|[<span data-ttu-id="cac62-118">Buzón de correo (disponibilidad)</span><span class="sxs-lookup"><span data-stu-id="cac62-118">Mailbox (Availability)</span></span>](mailbox-availability.md) <br/> | <span data-ttu-id="cac62-119">Representa el usuario del buzón de correo para una solicitud SetUserOofSettings o GetUserOofSettings.</span><span class="sxs-lookup"><span data-stu-id="cac62-119">Represents the mailbox user for a SetUserOofSettings or GetUserOofSettings request.</span></span>  <br/><br/>  <span data-ttu-id="cac62-120">Las siguientes son las expresiones XPath de este elemento:</span><span class="sxs-lookup"><span data-stu-id="cac62-120">The following are the XPath expressions to this element:</span></span>  <br/><br/>  `/GetUserOofSettingsRequest/Mailbox` <br/><br/>  `/SetUserOofSettingsRequest/Mailbox` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="cac62-121">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="cac62-121">Text value</span></span>

<span data-ttu-id="cac62-122">Es necesario un valor de texto si se usa este elemento.</span><span class="sxs-lookup"><span data-stu-id="cac62-122">A text value is required if this element is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="cac62-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="cac62-123">Remarks</span></span>

<span data-ttu-id="cac62-124">Este elemento se puede producir al menos una vez en el elemento [email (EmailAddressType)](email-emailaddresstype.md) .</span><span class="sxs-lookup"><span data-stu-id="cac62-124">This element can occur at most one time in the [Email (EmailAddressType)](email-emailaddresstype.md) element.</span></span> <span data-ttu-id="cac62-125">Este elemento no es obligatorio.</span><span class="sxs-lookup"><span data-stu-id="cac62-125">This element is not required.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="cac62-126">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="cac62-126">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="cac62-127">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="cac62-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cac62-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="cac62-128">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="cac62-129">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="cac62-129">Schema Name</span></span>  <br/> |<span data-ttu-id="cac62-130">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="cac62-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="cac62-131">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="cac62-131">Validation File</span></span>  <br/> |<span data-ttu-id="cac62-132">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="cac62-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="cac62-133">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="cac62-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="cac62-134">Falso</span><span class="sxs-lookup"><span data-stu-id="cac62-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cac62-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="cac62-135">See also</span></span>

- [<span data-ttu-id="cac62-136">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="cac62-136">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
- [<span data-ttu-id="cac62-137">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="cac62-137">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)
- [<span data-ttu-id="cac62-138">Obtener disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="cac62-138">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

