---
title: MailboxHoldStatus
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 92608b77-8aa4-403b-a4de-01e3a60af3e0
description: El elemento MailboxHoldStatus especifica el estado de retención del buzón.
ms.openlocfilehash: 6703c909d0a7b4e83e190807fc3202ecd4699e7f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836288"
---
# <a name="mailboxholdstatus"></a><span data-ttu-id="b54e5-103">MailboxHoldStatus</span><span class="sxs-lookup"><span data-stu-id="b54e5-103">MailboxHoldStatus</span></span>

<span data-ttu-id="b54e5-104">El elemento **MailboxHoldStatus** especifica el estado de retención del buzón.</span><span class="sxs-lookup"><span data-stu-id="b54e5-104">The **MailboxHoldStatus** element specifies the hold status of the mailbox.</span></span> 
  
```XML
<MailboxHoldStatus>
   <Mailbox/>
   <Status/>
   <AdditionalInfo/>
</MailboxHoldStatus>
```

<span data-ttu-id="b54e5-105">**MailboxHoldStatusType**</span><span class="sxs-lookup"><span data-stu-id="b54e5-105">**MailboxHoldStatusType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="b54e5-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="b54e5-106">Attributes and elements</span></span>

<span data-ttu-id="b54e5-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="b54e5-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b54e5-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="b54e5-108">Attributes</span></span>

<span data-ttu-id="b54e5-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="b54e5-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b54e5-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b54e5-110">Child elements</span></span>

<span data-ttu-id="b54e5-111">[Buzón de correo (string)](mailbox-string.md) | [estado (HoldStatusType)](status-holdstatustype.md) | [AdditionalInfo](additionalinfo.md)</span><span class="sxs-lookup"><span data-stu-id="b54e5-111">[Mailbox (string)](mailbox-string.md) | [Status (HoldStatusType)](status-holdstatustype.md) | [AdditionalInfo](additionalinfo.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="b54e5-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="b54e5-112">Parent elements</span></span>

[<span data-ttu-id="b54e5-113">MailboxHoldStatuses</span><span class="sxs-lookup"><span data-stu-id="b54e5-113">MailboxHoldStatuses</span></span>](mailboxholdstatuses.md)
  
## <a name="remarks"></a><span data-ttu-id="b54e5-114">Notas</span><span class="sxs-lookup"><span data-stu-id="b54e5-114">Remarks</span></span>

<span data-ttu-id="b54e5-115">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="b54e5-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="b54e5-116">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="b54e5-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b54e5-117">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="b54e5-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b54e5-118">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b54e5-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="b54e5-119">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="b54e5-119">Schema name</span></span>  <br/> |<span data-ttu-id="b54e5-120">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="b54e5-120">Types schema</span></span>  <br/> |
|<span data-ttu-id="b54e5-121">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="b54e5-121">Validation file</span></span>  <br/> |<span data-ttu-id="b54e5-122">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="b54e5-122">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="b54e5-123">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="b54e5-123">Can be empty</span></span>  <br/> ||
   

