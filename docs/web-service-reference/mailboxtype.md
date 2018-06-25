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
description: El elemento MailboxType representa el tipo de buzón de correo que está representada por la dirección de correo electrónico.
ms.openlocfilehash: d7232377951e8d9c8f191ac856058bc28467cadd
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836305"
---
# <a name="mailboxtype"></a><span data-ttu-id="7536e-103">MailboxType</span><span class="sxs-lookup"><span data-stu-id="7536e-103">MailboxType</span></span>

<span data-ttu-id="7536e-104">El elemento **MailboxType** representa el tipo de buzón de correo que está representada por la dirección de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="7536e-104">The **MailboxType** element represents the type of mailbox that is represented by the e-mail address.</span></span> 
  
```XML
<MailboxType>Mailbox | PublicDL | PrivateDL | Contact | PublicFolder | Unknown | OneOff | GroupMailbox</MailboxType>
```

<span data-ttu-id="7536e-105">**MailboxTypeType**</span><span class="sxs-lookup"><span data-stu-id="7536e-105">**MailboxTypeType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="7536e-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="7536e-106">Attributes and elements</span></span>

<span data-ttu-id="7536e-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="7536e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7536e-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="7536e-108">Attributes</span></span>

<span data-ttu-id="7536e-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="7536e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7536e-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="7536e-110">Child elements</span></span>

<span data-ttu-id="7536e-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="7536e-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="7536e-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="7536e-112">Parent elements</span></span>

|<span data-ttu-id="7536e-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="7536e-113">**Element**</span></span>|<span data-ttu-id="7536e-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7536e-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7536e-115">Buzón de correo</span><span class="sxs-lookup"><span data-stu-id="7536e-115">Mailbox</span></span>](mailbox.md) <br/> |<span data-ttu-id="7536e-116">Identifica una dirección de correo electrónico completa resuelta.</span><span class="sxs-lookup"><span data-stu-id="7536e-116">Identifies a fully resolved e-mail address.</span></span>  <br/> |
|[<span data-ttu-id="7536e-117">RoomList</span><span class="sxs-lookup"><span data-stu-id="7536e-117">RoomList</span></span>](roomlist.md) <br/> |<span data-ttu-id="7536e-118">Identifica una lista de las salas de reuniones.</span><span class="sxs-lookup"><span data-stu-id="7536e-118">Identifies a list of meeting rooms.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="7536e-119">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="7536e-119">Text value</span></span>

<span data-ttu-id="7536e-120">En la siguiente tabla se enumera los valores posibles para el elemento **MailboxType** .</span><span class="sxs-lookup"><span data-stu-id="7536e-120">The following table lists the possible values for the **MailboxType** element.</span></span> 
  
|<span data-ttu-id="7536e-121">**Valor**</span><span class="sxs-lookup"><span data-stu-id="7536e-121">**Value**</span></span>|<span data-ttu-id="7536e-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7536e-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7536e-123">Buz?n de correo</span><span class="sxs-lookup"><span data-stu-id="7536e-123">Mailbox</span></span>  <br/> |<span data-ttu-id="7536e-124">Representa un objeto de Active Directory habilitados para correo.</span><span class="sxs-lookup"><span data-stu-id="7536e-124">Represents a mail-enabled Active Directory object.</span></span>  <br/> |
|<span data-ttu-id="7536e-125">PublicDL</span><span class="sxs-lookup"><span data-stu-id="7536e-125">PublicDL</span></span>  <br/> |<span data-ttu-id="7536e-126">Representa una lista de distribución públicas.</span><span class="sxs-lookup"><span data-stu-id="7536e-126">Represents a public distribution list.</span></span>  <br/> |
|<span data-ttu-id="7536e-127">PrivateDL</span><span class="sxs-lookup"><span data-stu-id="7536e-127">PrivateDL</span></span>  <br/> |<span data-ttu-id="7536e-128">Representa una lista de distribución privada en el buzón del usuario.</span><span class="sxs-lookup"><span data-stu-id="7536e-128">Represents a private distribution list in a user's mailbox.</span></span>  <br/> |
|<span data-ttu-id="7536e-129">Contacto</span><span class="sxs-lookup"><span data-stu-id="7536e-129">Contact</span></span>  <br/> |<span data-ttu-id="7536e-130">Representa un contacto en el buzón del usuario.</span><span class="sxs-lookup"><span data-stu-id="7536e-130">Represents a contact in a user's mailbox.</span></span>  <br/> |
|<span data-ttu-id="7536e-131">PublicFolder</span><span class="sxs-lookup"><span data-stu-id="7536e-131">PublicFolder</span></span>  <br/> |<span data-ttu-id="7536e-132">Representa una carpeta pública.</span><span class="sxs-lookup"><span data-stu-id="7536e-132">Represents a public folder.</span></span>  <br/> |
|<span data-ttu-id="7536e-133">Desconocido</span><span class="sxs-lookup"><span data-stu-id="7536e-133">Unknown</span></span>  <br/> |<span data-ttu-id="7536e-134">Representa un tipo desconocido de buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="7536e-134">Represents an unknown type of mailbox.</span></span>  <br/> |
|<span data-ttu-id="7536e-135">OneOff</span><span class="sxs-lookup"><span data-stu-id="7536e-135">OneOff</span></span>  <br/> |<span data-ttu-id="7536e-136">Representa a un miembro de uso único de una lista de distribución personal.</span><span class="sxs-lookup"><span data-stu-id="7536e-136">Represents a one-off member of a personal distribution list.</span></span>  <br/> |
|<span data-ttu-id="7536e-137">GroupMailbox</span><span class="sxs-lookup"><span data-stu-id="7536e-137">GroupMailbox</span></span>  <br/> |<span data-ttu-id="7536e-138">Representa un buzón de grupo.</span><span class="sxs-lookup"><span data-stu-id="7536e-138">Represents a group mailbox.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7536e-139">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7536e-139">Remarks</span></span>

<span data-ttu-id="7536e-140">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="7536e-140">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7536e-141">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="7536e-141">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7536e-142">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="7536e-142">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="7536e-143">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="7536e-143">Schema Name</span></span>  <br/> |<span data-ttu-id="7536e-144">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="7536e-144">Types schema</span></span>  <br/> |
|<span data-ttu-id="7536e-145">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="7536e-145">Validation File</span></span>  <br/> |<span data-ttu-id="7536e-146">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="7536e-146">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="7536e-147">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="7536e-147">Can be Empty</span></span>  <br/> |<span data-ttu-id="7536e-148">False</span><span class="sxs-lookup"><span data-stu-id="7536e-148">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7536e-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="7536e-149">See also</span></span>

- [<span data-ttu-id="7536e-150">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="7536e-150">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

