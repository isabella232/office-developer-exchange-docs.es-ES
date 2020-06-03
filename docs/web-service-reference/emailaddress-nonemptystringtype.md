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
ms.openlocfilehash: fcc3e650d5fc32344022ed6f015d4096a4461f63
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463135"
---
# <a name="emailaddress-nonemptystringtype"></a><span data-ttu-id="ad72b-103">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="ad72b-103">EmailAddress (NonEmptyStringType)</span></span>

<span data-ttu-id="ad72b-104">El elemento **EmailAddress** define la dirección SMTP principal de un usuario de buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="ad72b-104">The **EmailAddress** element defines the primary SMTP address of a mailbox user.</span></span> 
  
```XML
<EmailAddress/>
```

 <span data-ttu-id="ad72b-105">**NonEmptyStringType**</span><span class="sxs-lookup"><span data-stu-id="ad72b-105">**NonEmptyStringType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ad72b-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="ad72b-106">Attributes and elements</span></span>

<span data-ttu-id="ad72b-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="ad72b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ad72b-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="ad72b-108">Attributes</span></span>

<span data-ttu-id="ad72b-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="ad72b-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ad72b-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ad72b-110">Child elements</span></span>

<span data-ttu-id="ad72b-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="ad72b-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="ad72b-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="ad72b-112">Parent elements</span></span>

|<span data-ttu-id="ad72b-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="ad72b-113">**Element**</span></span>|<span data-ttu-id="ad72b-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ad72b-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ad72b-115">Acciones</span><span class="sxs-lookup"><span data-stu-id="ad72b-115">ActingAs</span></span>](actingas.md) <br/> |<span data-ttu-id="ad72b-116">Identifica quién envía el autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="ad72b-116">Identifies who the caller is sending as.</span></span>  <br/> |
|[<span data-ttu-id="ad72b-117">Buzón</span><span class="sxs-lookup"><span data-stu-id="ad72b-117">Mailbox</span></span>](mailbox.md) <br/> | <span data-ttu-id="ad72b-118">Identifica una dirección de correo electrónico completamente resuelta.</span><span class="sxs-lookup"><span data-stu-id="ad72b-118">Identifies a fully resolved e-mail address.</span></span>  <br/><br/><span data-ttu-id="ad72b-119">Las siguientes son algunas expresiones XPath de este elemento:</span><span class="sxs-lookup"><span data-stu-id="ad72b-119">The following are some XPath expressions to this element:</span></span><br/><br/>`/CreateItem/ParentFolderId/DistinguishedFolderId/Mailbox`<br/><br/>`/CreateFolder/ParentFolderId/DistinguishedFolderId/Mailbox`<br/><br/>`CreateItem/Items/AcceptItem/ToRecipients/Mailbox`<br/><br/>`SyncFolderItemsResponseMessage/Changes/Create/CalendarItem/ConflictingMeetings/AcceptItem/CcRecipients/Mailbox`<br/><br/><span data-ttu-id="ad72b-120">Los siguientes son elementos primarios adicionales del elemento Mailbox:</span><span class="sxs-lookup"><span data-stu-id="ad72b-120">The following are additional parent elements of the Mailbox element:</span></span><br/><br/><span data-ttu-id="ad72b-121">- [BccRecipients](bccrecipients.md)</span><span class="sxs-lookup"><span data-stu-id="ad72b-121">- [BccRecipients](bccrecipients.md)</span></span> <br/><span data-ttu-id="ad72b-122">- [ReplyTo](replyto.md)</span><span class="sxs-lookup"><span data-stu-id="ad72b-122">- [ReplyTo](replyto.md)</span></span> <br/><span data-ttu-id="ad72b-123">- [Remitente](sender.md)</span><span class="sxs-lookup"><span data-stu-id="ad72b-123">- [Sender](sender.md)</span></span> <br/><span data-ttu-id="ad72b-124">- [De](from.md)</span><span class="sxs-lookup"><span data-stu-id="ad72b-124">- [From](from.md)</span></span> <br/><span data-ttu-id="ad72b-125">- [Organizador](organizer.md)</span><span class="sxs-lookup"><span data-stu-id="ad72b-125">- [Organizer](organizer.md)</span></span> <br/><span data-ttu-id="ad72b-126">- [DistinguishedFolderId](distinguishedfolderid.md)</span><span class="sxs-lookup"><span data-stu-id="ad72b-126">- [DistinguishedFolderId](distinguishedfolderid.md)</span></span> <br/><span data-ttu-id="ad72b-127">- [N](resolution.md)</span><span class="sxs-lookup"><span data-stu-id="ad72b-127">- [Resolution](resolution.md)</span></span> <br/><span data-ttu-id="ad72b-128">- [DLExpansion](dlexpansion.md)</span><span class="sxs-lookup"><span data-stu-id="ad72b-128">- [DLExpansion](dlexpansion.md)</span></span> <br/><span data-ttu-id="ad72b-129">- [Asistente](attendee.md)</span><span class="sxs-lookup"><span data-stu-id="ad72b-129">- [Attendee](attendee.md)</span></span> <br/> |
|[<span data-ttu-id="ad72b-130">RoomList</span><span class="sxs-lookup"><span data-stu-id="ad72b-130">RoomList</span></span>](roomlist.md) <br/> |<span data-ttu-id="ad72b-131">Identifica una lista de salas de reuniones por dirección de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="ad72b-131">Identifies a list of meeting rooms by email address.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="ad72b-132">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="ad72b-132">Text value</span></span>

<span data-ttu-id="ad72b-133">Se necesita un valor de texto que represente una dirección SMTP.</span><span class="sxs-lookup"><span data-stu-id="ad72b-133">A text value that represents an SMTP address is required.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ad72b-134">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ad72b-134">Remarks</span></span>

<span data-ttu-id="ad72b-135">El elemento **EmailAddress** puede representar direcciones SMTP o heredadas de nombres distintivos de Exchange (también conocidos como DN).</span><span class="sxs-lookup"><span data-stu-id="ad72b-135">The **EmailAddress** element can represent SMTP or legacy Exchange distinguished name (also known as DN) addresses.</span></span> <span data-ttu-id="ad72b-136">El elemento **EmailAddress** es el único elemento necesario del [buzón de correo](mailbox.md) .</span><span class="sxs-lookup"><span data-stu-id="ad72b-136">The **EmailAddress** element is the only required [Mailbox](mailbox.md) element.</span></span> 
  
<span data-ttu-id="ad72b-137">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="ad72b-137">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ad72b-138">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="ad72b-138">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ad72b-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="ad72b-139">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ad72b-140">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="ad72b-140">Schema Name</span></span>  <br/> |<span data-ttu-id="ad72b-141">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="ad72b-141">Types schema</span></span>  <br/> |
|<span data-ttu-id="ad72b-142">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="ad72b-142">Validation File</span></span>  <br/> |<span data-ttu-id="ad72b-143">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="ad72b-143">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="ad72b-144">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="ad72b-144">Can be Empty</span></span>  <br/> |<span data-ttu-id="ad72b-145">Falso</span><span class="sxs-lookup"><span data-stu-id="ad72b-145">False</span></span>  <br/> |
   

