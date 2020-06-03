---
title: SetHoldOnMailboxes
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: fd5b9f0e-23e8-428c-8168-2d6b4ecd6beb
description: El elemento SetHoldOnMailboxes contiene una solicitud de SetHoldOnMailboxes.
ms.openlocfilehash: c96ff50cb1204d86abc66829e1c5da7124f407f1
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44448355"
---
# <a name="setholdonmailboxes"></a><span data-ttu-id="58ac5-103">SetHoldOnMailboxes</span><span class="sxs-lookup"><span data-stu-id="58ac5-103">SetHoldOnMailboxes</span></span>

<span data-ttu-id="58ac5-104">El elemento **SetHoldOnMailboxes** contiene una solicitud de **SetHoldOnMailboxes** .</span><span class="sxs-lookup"><span data-stu-id="58ac5-104">The **SetHoldOnMailboxes** element contains a **SetHoldOnMailboxes** request.</span></span> 
  
```XML
<SetHoldOnMailboxes>
   <ActionType/>
   <HoldId/>
   <Query/>
   <Mailboxes/>
   <Language/>
   <IncludeNonIndexableItems/>
   <Deduplication/>
   <InPlaceHoldIdentity/>
</SetHoldOnMailboxes>
```

 <span data-ttu-id="58ac5-105">**SetHoldOnMailboxesType**</span><span class="sxs-lookup"><span data-stu-id="58ac5-105">**SetHoldOnMailboxesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="58ac5-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="58ac5-106">Attributes and elements</span></span>

<span data-ttu-id="58ac5-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="58ac5-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="58ac5-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="58ac5-108">Attributes</span></span>

<span data-ttu-id="58ac5-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="58ac5-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="58ac5-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="58ac5-110">Child elements</span></span>

<span data-ttu-id="58ac5-111">[ActionType (HoldActionType)](actiontype-holdactiontype.md)  |  [HoldId](holdid.md)  |  [Consulta](query.md)  |  [Buzones de correo (ArrayOfStringsType)](mailboxes-arrayofstringstype.md)  |  [Idioma](language.md)  |  [IncludeNonIndexableItems](includenonindexableitems.md)  |  [Desduplicación](deduplication.md)  |  [InPlaceHoldIdentity](inplaceholdidentity.md)</span><span class="sxs-lookup"><span data-stu-id="58ac5-111">[ActionType (HoldActionType)](actiontype-holdactiontype.md) | [HoldId](holdid.md) | [Query](query.md) | [Mailboxes (ArrayOfStringsType)](mailboxes-arrayofstringstype.md) | [Language](language.md) | [IncludeNonIndexableItems](includenonindexableitems.md) | [Deduplication](deduplication.md) | [InPlaceHoldIdentity](inplaceholdidentity.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="58ac5-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="58ac5-112">Parent elements</span></span>

<span data-ttu-id="58ac5-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="58ac5-113">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="58ac5-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="58ac5-114">Remarks</span></span>

<span data-ttu-id="58ac5-115">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="58ac5-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="58ac5-116">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="58ac5-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="58ac5-117">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="58ac5-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="58ac5-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="58ac5-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="58ac5-119">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="58ac5-119">Schema name</span></span>  <br/> |<span data-ttu-id="58ac5-120">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="58ac5-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="58ac5-121">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="58ac5-121">Validation file</span></span>  <br/> |<span data-ttu-id="58ac5-122">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="58ac5-122">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="58ac5-123">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="58ac5-123">Can be empty</span></span>  <br/> ||
   

