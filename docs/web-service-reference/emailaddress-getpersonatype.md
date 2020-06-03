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
ms.openlocfilehash: b58f61202cd94ff282b21138b47b40887b38752a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463457"
---
# <a name="emailaddress-getpersonatype"></a><span data-ttu-id="f2f2e-103">EmailAddress (GetPersonaType)</span><span class="sxs-lookup"><span data-stu-id="f2f2e-103">EmailAddress (GetPersonaType)</span></span>

<span data-ttu-id="f2f2e-104">El elemento **EmailAddress (GetPersonaType)** especifica la dirección de correo electrónico asociada con el rol.</span><span class="sxs-lookup"><span data-stu-id="f2f2e-104">The **EmailAddress (GetPersonaType)** element specifies the email address associated with the persona.</span></span> 
  
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

 <span data-ttu-id="f2f2e-105">**EmailAddressType**</span><span class="sxs-lookup"><span data-stu-id="f2f2e-105">**EmailAddressType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f2f2e-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="f2f2e-106">Attributes and elements</span></span>

<span data-ttu-id="f2f2e-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="f2f2e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f2f2e-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="f2f2e-108">Attributes</span></span>

<span data-ttu-id="f2f2e-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="f2f2e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f2f2e-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="f2f2e-110">Child elements</span></span>

<span data-ttu-id="f2f2e-111">[Name (cadena)](name-string.md)  |  [EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md)  |  [RoutingType (EmailAddressType)](routingtype-emailaddresstype.md)  |  [MailboxType](mailboxtype.md)  |  [Itemid](itemid.md)  |  [OriginalDisplayName](originaldisplayname.md)</span><span class="sxs-lookup"><span data-stu-id="f2f2e-111">[Name (string)](name-string.md) | [EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) | [RoutingType (EmailAddressType)](routingtype-emailaddresstype.md) | [MailboxType](mailboxtype.md) | [ItemId](itemid.md) | [OriginalDisplayName](originaldisplayname.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="f2f2e-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="f2f2e-112">Parent elements</span></span>

[<span data-ttu-id="f2f2e-113">GetPersona</span><span class="sxs-lookup"><span data-stu-id="f2f2e-113">GetPersona</span></span>](getpersona.md)
  
## <a name="remarks"></a><span data-ttu-id="f2f2e-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f2f2e-114">Remarks</span></span>

<span data-ttu-id="f2f2e-115">Este elemento se incorporó en Exchange Server 2013 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="f2f2e-115">This element was introduced in Exchange Server 2013 Service Pack 1 (SP1).</span></span>
  
<span data-ttu-id="f2f2e-116">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="f2f2e-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f2f2e-117">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="f2f2e-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f2f2e-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="f2f2e-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="f2f2e-119">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="f2f2e-119">Schema Name</span></span>  <br/> |<span data-ttu-id="f2f2e-120">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="f2f2e-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="f2f2e-121">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="f2f2e-121">Validation File</span></span>  <br/> |<span data-ttu-id="f2f2e-122">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="f2f2e-122">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="f2f2e-123">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="f2f2e-123">Can be Empty</span></span>  <br/> |<span data-ttu-id="f2f2e-124">Verdadero</span><span class="sxs-lookup"><span data-stu-id="f2f2e-124">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f2f2e-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="f2f2e-125">See also</span></span>

- [<span data-ttu-id="f2f2e-126">GetPersona</span><span class="sxs-lookup"><span data-stu-id="f2f2e-126">GetPersona</span></span>](getpersona.md)
- [<span data-ttu-id="f2f2e-127">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="f2f2e-127">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

