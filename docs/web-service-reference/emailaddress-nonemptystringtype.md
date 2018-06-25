---
title: EmailAddress (NonEmptyStringType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- EmailAddress
api_type:
- schema
ms.assetid: c0c708d1-b016-4902-a294-9af44aea2050
description: El elemento EmailAddress define la dirección SMTP principal de un usuario de buzón de correo.
ms.openlocfilehash: fcf2839c1e2e40a22d6b6a856608f52f2c9c2a1a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764339"
---
# <a name="emailaddress-nonemptystringtype"></a><span data-ttu-id="ebac2-103">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="ebac2-103">EmailAddress (NonEmptyStringType)</span></span>

<span data-ttu-id="ebac2-104">El elemento **EmailAddress** define la dirección SMTP principal de un usuario de buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="ebac2-104">The **EmailAddress** element defines the primary SMTP address of a mailbox user.</span></span> 
  
```XML
<EmailAddress/>
```

 <span data-ttu-id="ebac2-105">**NonEmptyStringType**</span><span class="sxs-lookup"><span data-stu-id="ebac2-105">**NonEmptyStringType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ebac2-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="ebac2-106">Attributes and elements</span></span>

<span data-ttu-id="ebac2-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="ebac2-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ebac2-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="ebac2-108">Attributes</span></span>

<span data-ttu-id="ebac2-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="ebac2-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ebac2-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ebac2-110">Child elements</span></span>

<span data-ttu-id="ebac2-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="ebac2-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="ebac2-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="ebac2-112">Parent elements</span></span>

|<span data-ttu-id="ebac2-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="ebac2-113">**Element**</span></span>|<span data-ttu-id="ebac2-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ebac2-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ebac2-115">ActingAs</span><span class="sxs-lookup"><span data-stu-id="ebac2-115">ActingAs</span></span>](actingas.md) <br/> |<span data-ttu-id="ebac2-116">Identifique quién envía como el autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="ebac2-116">Identifies who the caller is sending as.</span></span>  <br/> |
|[<span data-ttu-id="ebac2-117">Buzón de correo</span><span class="sxs-lookup"><span data-stu-id="ebac2-117">Mailbox</span></span>](mailbox.md) <br/> | <span data-ttu-id="ebac2-118">Identifica una dirección de correo electrónico completa resuelta.</span><span class="sxs-lookup"><span data-stu-id="ebac2-118">Identifies a fully resolved e-mail address.</span></span>  <br/><br/><span data-ttu-id="ebac2-119">Las siguientes son algunas expresiones de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="ebac2-119">The following are some XPath expressions to this element:</span></span><br/><br/>`/CreateItem/ParentFolderId/DistinguishedFolderId/Mailbox`<br/><br/>`/CreateFolder/ParentFolderId/DistinguishedFolderId/Mailbox`<br/><br/>`CreateItem/Items/AcceptItem/ToRecipients/Mailbox`<br/><br/>`SyncFolderItemsResponseMessage/Changes/Create/CalendarItem/ConflictingMeetings/AcceptItem/CcRecipients/Mailbox`<br/><br/><span data-ttu-id="ebac2-120">Los siguientes son elementos de primario adicionales del elemento de buzón de correo:</span><span class="sxs-lookup"><span data-stu-id="ebac2-120">The following are additional parent elements of the Mailbox element:</span></span><br/><br/><span data-ttu-id="ebac2-121">- [BccRecipients](bccrecipients.md)</span><span class="sxs-lookup"><span data-stu-id="ebac2-121">- [BccRecipients](bccrecipients.md)</span></span> <br/><span data-ttu-id="ebac2-122">- [ReplyTo](replyto.md)</span><span class="sxs-lookup"><span data-stu-id="ebac2-122">- [ReplyTo](replyto.md)</span></span> <br/><span data-ttu-id="ebac2-123">- [Remitente](sender.md)</span><span class="sxs-lookup"><span data-stu-id="ebac2-123">- [Sender](sender.md)</span></span> <br/><span data-ttu-id="ebac2-124">- [De](from.md)</span><span class="sxs-lookup"><span data-stu-id="ebac2-124">- [From](from.md)</span></span> <br/><span data-ttu-id="ebac2-125">- [Organizador](organizer.md)</span><span class="sxs-lookup"><span data-stu-id="ebac2-125">- [Organizer](organizer.md)</span></span> <br/><span data-ttu-id="ebac2-126">- [DistinguishedFolderId](distinguishedfolderid.md)</span><span class="sxs-lookup"><span data-stu-id="ebac2-126">- [DistinguishedFolderId](distinguishedfolderid.md)</span></span> <br/><span data-ttu-id="ebac2-127">- [Resolución](resolution.md)</span><span class="sxs-lookup"><span data-stu-id="ebac2-127">- [Resolution](resolution.md)</span></span> <br/><span data-ttu-id="ebac2-128">- [DLExpansion](dlexpansion.md)</span><span class="sxs-lookup"><span data-stu-id="ebac2-128">- [DLExpansion](dlexpansion.md)</span></span> <br/><span data-ttu-id="ebac2-129">- [ATTENDEE](attendee.md)</span><span class="sxs-lookup"><span data-stu-id="ebac2-129">- [Attendee](attendee.md)</span></span> <br/> |
|[<span data-ttu-id="ebac2-130">RoomList</span><span class="sxs-lookup"><span data-stu-id="ebac2-130">RoomList</span></span>](roomlist.md) <br/> |<span data-ttu-id="ebac2-131">Identifica una lista de las salas de reuniones por dirección de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="ebac2-131">Identifies a list of meeting rooms by email address.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="ebac2-132">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="ebac2-132">Text value</span></span>

<span data-ttu-id="ebac2-133">Se requiere un valor de texto que representa una dirección SMTP.</span><span class="sxs-lookup"><span data-stu-id="ebac2-133">A text value that represents an SMTP address is required.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ebac2-134">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ebac2-134">Remarks</span></span>

<span data-ttu-id="ebac2-135">El elemento **EmailAddress** puede representar SMTP o distintivos (DN) de Exchange heredado direcciones de nombre (también conocido como DN).</span><span class="sxs-lookup"><span data-stu-id="ebac2-135">The **EmailAddress** element can represent SMTP or legacy Exchange distinguished name (also known as DN) addresses.</span></span> <span data-ttu-id="ebac2-136">El elemento **EmailAddress** es el único elemento necesario de [buzón de correo](mailbox.md) .</span><span class="sxs-lookup"><span data-stu-id="ebac2-136">The **EmailAddress** element is the only required [Mailbox](mailbox.md) element.</span></span> 
  
<span data-ttu-id="ebac2-137">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="ebac2-137">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ebac2-138">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="ebac2-138">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ebac2-139">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="ebac2-139">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ebac2-140">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="ebac2-140">Schema Name</span></span>  <br/> |<span data-ttu-id="ebac2-141">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="ebac2-141">Types schema</span></span>  <br/> |
|<span data-ttu-id="ebac2-142">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="ebac2-142">Validation File</span></span>  <br/> |<span data-ttu-id="ebac2-143">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="ebac2-143">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="ebac2-144">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="ebac2-144">Can be Empty</span></span>  <br/> |<span data-ttu-id="ebac2-145">False</span><span class="sxs-lookup"><span data-stu-id="ebac2-145">False</span></span>  <br/> |
   

