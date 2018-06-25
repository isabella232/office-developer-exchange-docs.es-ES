---
title: EmailAddress (EmailAddressType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0cdabfcb-7658-4c7d-bb03-1e776ed11e43
description: El elemento EmailAddress especifica la dirección SMTP completa resuelta para el buzón de sitio o de la persona asociada.
ms.openlocfilehash: c31a37fc0dbdcc2b501b82346a17a0a3b4775556
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764332"
---
# <a name="emailaddress-emailaddresstype"></a><span data-ttu-id="280c8-103">EmailAddress (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="280c8-103">EmailAddress (EmailAddressType)</span></span>

<span data-ttu-id="280c8-104">El elemento **EmailAddress** especifica la dirección SMTP completa resuelta para el buzón de sitio o de la persona asociada.</span><span class="sxs-lookup"><span data-stu-id="280c8-104">The **EmailAddress** element specifies the fully resolved SMTP address for the site mailbox or the associated persona.</span></span> 
  
```xml
<EmailAddress>
    <Name></Name>
    <EmailAddress></EmailAddress>
    <RoutingType></RoutingType>
    <MailboxType></MailboxType>
    <ItemId></ItemId>
</EmailAddress>
```

 <span data-ttu-id="280c8-105">**EmailAddressType**</span><span class="sxs-lookup"><span data-stu-id="280c8-105">**EmailAddressType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="280c8-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="280c8-106">Attributes and elements</span></span>

<span data-ttu-id="280c8-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="280c8-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="280c8-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="280c8-108">Attributes</span></span>

<span data-ttu-id="280c8-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="280c8-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="280c8-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="280c8-110">Child elements</span></span>

|<span data-ttu-id="280c8-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="280c8-111">**Element**</span></span>|<span data-ttu-id="280c8-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="280c8-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="280c8-113">Name (cadena)</span><span class="sxs-lookup"><span data-stu-id="280c8-113">Name (string)</span></span>](name-string.md) <br/> |<span data-ttu-id="280c8-114">Especifica un nombre de búsqueda refinador o clave o el nombre de un usuario de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="280c8-114">Specifies a search refiner name or key or the name of an email user.</span></span>  <br/> |
|[<span data-ttu-id="280c8-115">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="280c8-115">EmailAddress (NonEmptyStringType)</span></span>](emailaddress-nonemptystringtype.md) <br/> |<span data-ttu-id="280c8-116">Define la dirección SMTP principal de un usuario de buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="280c8-116">Defines the primary SMTP address of a mailbox user.</span></span>  <br/> |
|[<span data-ttu-id="280c8-117">RoutingType (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="280c8-117">RoutingType (EmailAddressType)</span></span>](routingtype-emailaddresstype.md) <br/> |<span data-ttu-id="280c8-118">Especifica el tipo de distribución de una dirección de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="280c8-118">Specifies the routing type of an email address.</span></span>  <br/> |
|[<span data-ttu-id="280c8-119">MailboxType</span><span class="sxs-lookup"><span data-stu-id="280c8-119">MailboxType</span></span>](mailboxtype.md) <br/> |<span data-ttu-id="280c8-120">Representa el tipo de buzón de correo que está representada por la dirección de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="280c8-120">Represents the type of mailbox that is represented by the e-mail address.</span></span>  <br/> |
|[<span data-ttu-id="280c8-121">ItemId</span><span class="sxs-lookup"><span data-stu-id="280c8-121">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="280c8-122">Contiene el único identificador y cambiar la clave de un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="280c8-122">Contains the unique identifier and change key of an item in the Exchange store.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="280c8-123">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="280c8-123">Parent elements</span></span>

|<span data-ttu-id="280c8-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="280c8-124">**Element**</span></span>|<span data-ttu-id="280c8-125">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="280c8-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="280c8-126">Rol</span><span class="sxs-lookup"><span data-stu-id="280c8-126">Persona</span></span>](persona.md) <br/> |<span data-ttu-id="280c8-127">Especifica un conjunto de datos de rol devueltos por una solicitud de **GetPersona** .</span><span class="sxs-lookup"><span data-stu-id="280c8-127">Specifies a set of persona data returned by a **GetPersona** request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="280c8-128">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="280c8-128">Text value</span></span>

<span data-ttu-id="280c8-129">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="280c8-129">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="280c8-130">Comentarios</span><span class="sxs-lookup"><span data-stu-id="280c8-130">Remarks</span></span>

<span data-ttu-id="280c8-131">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="280c8-131">This element is optional.</span></span>
  
<span data-ttu-id="280c8-132">El elemento **EmailAddress** es aplicable para los clientes que estén destinados a Exchange Online y versiones de Exchange 2013 a partir de Microsoft Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="280c8-132">The **EmailAddress** element is applicable for clients that target Exchange Online and versions of Microsoft Exchange Server starting with Exchange 2013.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="280c8-133">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="280c8-133">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="280c8-134">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="280c8-134">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="280c8-135">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="280c8-135">Schema Name</span></span>  <br/> |<span data-ttu-id="280c8-136">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="280c8-136">Type schema</span></span>  <br/> |
|<span data-ttu-id="280c8-137">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="280c8-137">Validation File</span></span>  <br/> |<span data-ttu-id="280c8-138">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="280c8-138">types.xsd</span></span>  <br/> |
|<span data-ttu-id="280c8-139">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="280c8-139">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="280c8-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="280c8-140">See also</span></span>

- [<span data-ttu-id="280c8-141">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="280c8-141">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

