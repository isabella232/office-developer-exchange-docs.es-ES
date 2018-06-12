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
ms.openlocfilehash: 7d226de908c4d5a474129e3e1f2344ec1318f538
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19837413"
---
# <a name="setholdonmailboxes"></a><span data-ttu-id="152c1-103">SetHoldOnMailboxes</span><span class="sxs-lookup"><span data-stu-id="152c1-103">SetHoldOnMailboxes</span></span>

<span data-ttu-id="152c1-104">El elemento **SetHoldOnMailboxes** contiene una solicitud de **SetHoldOnMailboxes** .</span><span class="sxs-lookup"><span data-stu-id="152c1-104">The **SetHoldOnMailboxes** element contains a **SetHoldOnMailboxes** request.</span></span> 
  
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

 <span data-ttu-id="152c1-105">**SetHoldOnMailboxesType**</span><span class="sxs-lookup"><span data-stu-id="152c1-105">**SetHoldOnMailboxesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="152c1-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="152c1-106">Attributes and elements</span></span>

<span data-ttu-id="152c1-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="152c1-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="152c1-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="152c1-108">Attributes</span></span>

<span data-ttu-id="152c1-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="152c1-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="152c1-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="152c1-110">Child elements</span></span>

<span data-ttu-id="152c1-111">[ActionType (HoldActionType)](actiontype-holdactiontype.md) | [HoldId](holdid.md) | [consulta](query.md) | [buzones (ArrayOfStringsType)](mailboxes-arrayofstringstype.md) | [idioma](language.md) | [IncludeNonIndexableItems](includenonindexableitems.md) | [desduplicación ](deduplication.md)  |  [InPlaceHoldIdentity](inplaceholdidentity.md)</span><span class="sxs-lookup"><span data-stu-id="152c1-111">[ActionType (HoldActionType)](actiontype-holdactiontype.md) | [HoldId](holdid.md) | [Query](query.md) | [Mailboxes (ArrayOfStringsType)](mailboxes-arrayofstringstype.md) | [Language](language.md) | [IncludeNonIndexableItems](includenonindexableitems.md) | [Deduplication](deduplication.md) | [InPlaceHoldIdentity](inplaceholdidentity.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="152c1-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="152c1-112">Parent elements</span></span>

<span data-ttu-id="152c1-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="152c1-113">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="152c1-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="152c1-114">Remarks</span></span>

<span data-ttu-id="152c1-115">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="152c1-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="152c1-116">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="152c1-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="152c1-117">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="152c1-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="152c1-118">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="152c1-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="152c1-119">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="152c1-119">Schema name</span></span>  <br/> |<span data-ttu-id="152c1-120">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="152c1-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="152c1-121">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="152c1-121">Validation file</span></span>  <br/> |<span data-ttu-id="152c1-122">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="152c1-122">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="152c1-123">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="152c1-123">Can be empty</span></span>  <br/> ||
   

