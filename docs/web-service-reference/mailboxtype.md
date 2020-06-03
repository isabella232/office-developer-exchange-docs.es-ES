---
title: MailboxType
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MailboxType
api_type:
- schema
ms.assetid: 696e5fdb-d8c5-40f0-9e79-885eae65dfa4
description: El elemento MailboxType representa el tipo de buzón que se representa mediante la dirección de correo electrónico.
ms.openlocfilehash: 8c322ab8a87730832f5d199698a369656b058a9a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459801"
---
# <a name="mailboxtype"></a><span data-ttu-id="84353-103">MailboxType</span><span class="sxs-lookup"><span data-stu-id="84353-103">MailboxType</span></span>

<span data-ttu-id="84353-104">El elemento **MailboxType** representa el tipo de buzón que se representa mediante la dirección de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="84353-104">The **MailboxType** element represents the type of mailbox that is represented by the e-mail address.</span></span> 
  
```XML
<MailboxType>Mailbox | PublicDL | PrivateDL | Contact | PublicFolder | Unknown | OneOff | GroupMailbox</MailboxType>
```

<span data-ttu-id="84353-105">**MailboxTypeType**</span><span class="sxs-lookup"><span data-stu-id="84353-105">**MailboxTypeType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="84353-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="84353-106">Attributes and elements</span></span>

<span data-ttu-id="84353-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="84353-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="84353-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="84353-108">Attributes</span></span>

<span data-ttu-id="84353-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="84353-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="84353-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="84353-110">Child elements</span></span>

<span data-ttu-id="84353-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="84353-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="84353-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="84353-112">Parent elements</span></span>

|<span data-ttu-id="84353-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="84353-113">**Element**</span></span>|<span data-ttu-id="84353-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="84353-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="84353-115">Buzón</span><span class="sxs-lookup"><span data-stu-id="84353-115">Mailbox</span></span>](mailbox.md) <br/> |<span data-ttu-id="84353-116">Identifica una dirección de correo electrónico completamente resuelta.</span><span class="sxs-lookup"><span data-stu-id="84353-116">Identifies a fully resolved e-mail address.</span></span>  <br/> |
|[<span data-ttu-id="84353-117">RoomList</span><span class="sxs-lookup"><span data-stu-id="84353-117">RoomList</span></span>](roomlist.md) <br/> |<span data-ttu-id="84353-118">Identifica una lista de salas de reuniones.</span><span class="sxs-lookup"><span data-stu-id="84353-118">Identifies a list of meeting rooms.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="84353-119">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="84353-119">Text value</span></span>

<span data-ttu-id="84353-120">En la siguiente tabla se enumeran los valores posibles para el elemento **MailboxType** .</span><span class="sxs-lookup"><span data-stu-id="84353-120">The following table lists the possible values for the **MailboxType** element.</span></span> 
  
|<span data-ttu-id="84353-121">**Valor**</span><span class="sxs-lookup"><span data-stu-id="84353-121">**Value**</span></span>|<span data-ttu-id="84353-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="84353-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="84353-123">Buzón de correo</span><span class="sxs-lookup"><span data-stu-id="84353-123">Mailbox</span></span>  <br/> |<span data-ttu-id="84353-124">Representa un objeto de Active Directory habilitado para correo.</span><span class="sxs-lookup"><span data-stu-id="84353-124">Represents a mail-enabled Active Directory object.</span></span>  <br/> |
|<span data-ttu-id="84353-125">PublicDL</span><span class="sxs-lookup"><span data-stu-id="84353-125">PublicDL</span></span>  <br/> |<span data-ttu-id="84353-126">Representa una lista de distribución pública.</span><span class="sxs-lookup"><span data-stu-id="84353-126">Represents a public distribution list.</span></span>  <br/> |
|<span data-ttu-id="84353-127">PrivateDL</span><span class="sxs-lookup"><span data-stu-id="84353-127">PrivateDL</span></span>  <br/> |<span data-ttu-id="84353-128">Representa una lista de distribución privada en el buzón de un usuario.</span><span class="sxs-lookup"><span data-stu-id="84353-128">Represents a private distribution list in a user's mailbox.</span></span>  <br/> |
|<span data-ttu-id="84353-129">Contacto</span><span class="sxs-lookup"><span data-stu-id="84353-129">Contact</span></span>  <br/> |<span data-ttu-id="84353-130">Representa un contacto en el buzón de un usuario.</span><span class="sxs-lookup"><span data-stu-id="84353-130">Represents a contact in a user's mailbox.</span></span>  <br/> |
|<span data-ttu-id="84353-131">PublicFolder</span><span class="sxs-lookup"><span data-stu-id="84353-131">PublicFolder</span></span>  <br/> |<span data-ttu-id="84353-132">Representa una carpeta pública.</span><span class="sxs-lookup"><span data-stu-id="84353-132">Represents a public folder.</span></span>  <br/> |
|<span data-ttu-id="84353-133">Desconocido</span><span class="sxs-lookup"><span data-stu-id="84353-133">Unknown</span></span>  <br/> |<span data-ttu-id="84353-134">Representa un tipo de buzón desconocido.</span><span class="sxs-lookup"><span data-stu-id="84353-134">Represents an unknown type of mailbox.</span></span>  <br/> |
|<span data-ttu-id="84353-135">OneOff</span><span class="sxs-lookup"><span data-stu-id="84353-135">OneOff</span></span>  <br/> |<span data-ttu-id="84353-136">Representa un miembro de un solo uso de una lista de distribución personal.</span><span class="sxs-lookup"><span data-stu-id="84353-136">Represents a one-off member of a personal distribution list.</span></span>  <br/> |
|<span data-ttu-id="84353-137">GroupMailbox</span><span class="sxs-lookup"><span data-stu-id="84353-137">GroupMailbox</span></span>  <br/> |<span data-ttu-id="84353-138">Representa un buzón de grupo.</span><span class="sxs-lookup"><span data-stu-id="84353-138">Represents a group mailbox.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="84353-139">Comentarios</span><span class="sxs-lookup"><span data-stu-id="84353-139">Remarks</span></span>

<span data-ttu-id="84353-140">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="84353-140">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="84353-141">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="84353-141">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="84353-142">Namespace</span><span class="sxs-lookup"><span data-stu-id="84353-142">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="84353-143">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="84353-143">Schema Name</span></span>  <br/> |<span data-ttu-id="84353-144">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="84353-144">Types schema</span></span>  <br/> |
|<span data-ttu-id="84353-145">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="84353-145">Validation File</span></span>  <br/> |<span data-ttu-id="84353-146">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="84353-146">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="84353-147">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="84353-147">Can be Empty</span></span>  <br/> |<span data-ttu-id="84353-148">Falso</span><span class="sxs-lookup"><span data-stu-id="84353-148">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="84353-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="84353-149">See also</span></span>

- [<span data-ttu-id="84353-150">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="84353-150">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

