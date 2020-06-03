---
title: EmailAddress (EmailAddressType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0cdabfcb-7658-4c7d-bb03-1e776ed11e43
description: El elemento EmailAddress especifica la dirección SMTP completamente resuelta para el buzón de sitio o el rol asociado.
ms.openlocfilehash: 8b04b75e91cc16be7f88c9a0ac08c5e36855056e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463464"
---
# <a name="emailaddress-emailaddresstype"></a><span data-ttu-id="f0ef4-103">EmailAddress (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="f0ef4-103">EmailAddress (EmailAddressType)</span></span>

<span data-ttu-id="f0ef4-104">El elemento **EmailAddress** especifica la dirección SMTP completamente resuelta para el buzón de sitio o el rol asociado.</span><span class="sxs-lookup"><span data-stu-id="f0ef4-104">The **EmailAddress** element specifies the fully resolved SMTP address for the site mailbox or the associated persona.</span></span> 
  
```xml
<EmailAddress>
    <Name></Name>
    <EmailAddress></EmailAddress>
    <RoutingType></RoutingType>
    <MailboxType></MailboxType>
    <ItemId></ItemId>
</EmailAddress>
```

 <span data-ttu-id="f0ef4-105">**EmailAddressType**</span><span class="sxs-lookup"><span data-stu-id="f0ef4-105">**EmailAddressType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f0ef4-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="f0ef4-106">Attributes and elements</span></span>

<span data-ttu-id="f0ef4-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="f0ef4-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f0ef4-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="f0ef4-108">Attributes</span></span>

<span data-ttu-id="f0ef4-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="f0ef4-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f0ef4-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="f0ef4-110">Child elements</span></span>

|<span data-ttu-id="f0ef4-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="f0ef4-111">**Element**</span></span>|<span data-ttu-id="f0ef4-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f0ef4-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f0ef4-113">Name (cadena)</span><span class="sxs-lookup"><span data-stu-id="f0ef4-113">Name (string)</span></span>](name-string.md) <br/> |<span data-ttu-id="f0ef4-114">Especifica un nombre de refinador de búsqueda o una clave o el nombre de un usuario de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="f0ef4-114">Specifies a search refiner name or key or the name of an email user.</span></span>  <br/> |
|[<span data-ttu-id="f0ef4-115">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="f0ef4-115">EmailAddress (NonEmptyStringType)</span></span>](emailaddress-nonemptystringtype.md) <br/> |<span data-ttu-id="f0ef4-116">Define la dirección SMTP principal de un usuario de buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="f0ef4-116">Defines the primary SMTP address of a mailbox user.</span></span>  <br/> |
|[<span data-ttu-id="f0ef4-117">RoutingType (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="f0ef4-117">RoutingType (EmailAddressType)</span></span>](routingtype-emailaddresstype.md) <br/> |<span data-ttu-id="f0ef4-118">Especifica el tipo de enrutamiento de una dirección de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="f0ef4-118">Specifies the routing type of an email address.</span></span>  <br/> |
|[<span data-ttu-id="f0ef4-119">MailboxType</span><span class="sxs-lookup"><span data-stu-id="f0ef4-119">MailboxType</span></span>](mailboxtype.md) <br/> |<span data-ttu-id="f0ef4-120">Representa el tipo de buzón que se representa mediante la dirección de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="f0ef4-120">Represents the type of mailbox that is represented by the e-mail address.</span></span>  <br/> |
|[<span data-ttu-id="f0ef4-121">ItemId</span><span class="sxs-lookup"><span data-stu-id="f0ef4-121">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="f0ef4-122">Contiene el identificador único y la clave de cambio de un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="f0ef4-122">Contains the unique identifier and change key of an item in the Exchange store.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="f0ef4-123">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="f0ef4-123">Parent elements</span></span>

|<span data-ttu-id="f0ef4-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="f0ef4-124">**Element**</span></span>|<span data-ttu-id="f0ef4-125">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f0ef4-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f0ef4-126">Rol</span><span class="sxs-lookup"><span data-stu-id="f0ef4-126">Persona</span></span>](persona.md) <br/> |<span data-ttu-id="f0ef4-127">Especifica un conjunto de datos de rol devueltos por una solicitud **GetPersona** .</span><span class="sxs-lookup"><span data-stu-id="f0ef4-127">Specifies a set of persona data returned by a **GetPersona** request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="f0ef4-128">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="f0ef4-128">Text value</span></span>

<span data-ttu-id="f0ef4-129">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="f0ef4-129">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f0ef4-130">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f0ef4-130">Remarks</span></span>

<span data-ttu-id="f0ef4-131">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="f0ef4-131">This element is optional.</span></span>
  
<span data-ttu-id="f0ef4-132">El elemento **EmailAddress** se aplica a los clientes de Exchange Online y versiones de Microsoft Exchange Server que empiecen por Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="f0ef4-132">The **EmailAddress** element is applicable for clients that target Exchange Online and versions of Microsoft Exchange Server starting with Exchange 2013.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="f0ef4-133">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="f0ef4-133">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f0ef4-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="f0ef4-134">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f0ef4-135">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="f0ef4-135">Schema Name</span></span>  <br/> |<span data-ttu-id="f0ef4-136">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="f0ef4-136">Type schema</span></span>  <br/> |
|<span data-ttu-id="f0ef4-137">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="f0ef4-137">Validation File</span></span>  <br/> |<span data-ttu-id="f0ef4-138">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="f0ef4-138">types.xsd</span></span>  <br/> |
|<span data-ttu-id="f0ef4-139">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="f0ef4-139">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="f0ef4-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="f0ef4-140">See also</span></span>

- [<span data-ttu-id="f0ef4-141">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="f0ef4-141">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

