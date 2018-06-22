---
title: EmailAddress (GetPersonaType)
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 052055b5-4630-40ed-9b24-9e7f4bf7ba1d
description: El elemento EmailAddress (GetPersonaType) especifica la dirección de correo electrónico asociada con el rol.
ms.openlocfilehash: a28a4a61a9719875fe99e1c950bcd3ec3af9ab13
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764333"
---
# <a name="emailaddress-getpersonatype"></a><span data-ttu-id="0eb10-103">EmailAddress (GetPersonaType)</span><span class="sxs-lookup"><span data-stu-id="0eb10-103">EmailAddress (GetPersonaType)</span></span>

<span data-ttu-id="0eb10-104">El elemento **EmailAddress (GetPersonaType)** especifica la dirección de correo electrónico asociada con el rol.</span><span class="sxs-lookup"><span data-stu-id="0eb10-104">The **EmailAddress (GetPersonaType)** element specifies the email address associated with the persona.</span></span> 
  
```XML
<EmailAddress>
    <Name></Name>
    <EmailAddress></EmailAddress>
    <RoutingType></RoutingType>
    <MailboxType></MailboxType>
    <ItemId></ItemId>
    <OriginalDisplayName></OriginalDisplayName>
</EmailAddress>>
```

 <span data-ttu-id="0eb10-105">**EmailAddressType**</span><span class="sxs-lookup"><span data-stu-id="0eb10-105">**EmailAddressType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0eb10-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="0eb10-106">Attributes and elements</span></span>

<span data-ttu-id="0eb10-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="0eb10-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0eb10-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="0eb10-108">Attributes</span></span>

<span data-ttu-id="0eb10-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="0eb10-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0eb10-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="0eb10-110">Child elements</span></span>

<span data-ttu-id="0eb10-111">[Name (cadena)](name-string.md) | [EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) | [RoutingType (EmailAddressType)](routingtype-emailaddresstype.md) | [MailboxType](mailboxtype.md) | [ItemId](itemid.md) | [OriginalDisplayName](originaldisplayname.md)</span><span class="sxs-lookup"><span data-stu-id="0eb10-111">[Name (string)](name-string.md) | [EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) | [RoutingType (EmailAddressType)](routingtype-emailaddresstype.md) | [MailboxType](mailboxtype.md) | [ItemId](itemid.md) | [OriginalDisplayName](originaldisplayname.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="0eb10-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="0eb10-112">Parent elements</span></span>

[<span data-ttu-id="0eb10-113">GetPersona</span><span class="sxs-lookup"><span data-stu-id="0eb10-113">GetPersona</span></span>](getpersona.md)
  
## <a name="remarks"></a><span data-ttu-id="0eb10-114">Notas</span><span class="sxs-lookup"><span data-stu-id="0eb10-114">Remarks</span></span>

<span data-ttu-id="0eb10-115">Este elemento se incorporó en Exchange Server 2013 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="0eb10-115">This element was introduced in Exchange Server 2013 Service Pack 1 (SP1).</span></span>
  
<span data-ttu-id="0eb10-116">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="0eb10-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0eb10-117">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="0eb10-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0eb10-118">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="0eb10-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="0eb10-119">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="0eb10-119">Schema Name</span></span>  <br/> |<span data-ttu-id="0eb10-120">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="0eb10-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="0eb10-121">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="0eb10-121">Validation File</span></span>  <br/> |<span data-ttu-id="0eb10-122">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="0eb10-122">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="0eb10-123">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="0eb10-123">Can be Empty</span></span>  <br/> |<span data-ttu-id="0eb10-124">Verdadero</span><span class="sxs-lookup"><span data-stu-id="0eb10-124">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0eb10-125">Ver también</span><span class="sxs-lookup"><span data-stu-id="0eb10-125">See also</span></span>

- [<span data-ttu-id="0eb10-126">GetPersona</span><span class="sxs-lookup"><span data-stu-id="0eb10-126">GetPersona</span></span>](getpersona.md)
- [<span data-ttu-id="0eb10-127">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="0eb10-127">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

