---
title: MailboxHoldStatus
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 92608b77-8aa4-403b-a4de-01e3a60af3e0
description: El elemento MailboxHoldStatus especifica el estado de retención del buzón de correo.
ms.openlocfilehash: 2ac575275fc00d2e3ba38cb4ec7335567ee82da6
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468813"
---
# <a name="mailboxholdstatus"></a><span data-ttu-id="f1303-103">MailboxHoldStatus</span><span class="sxs-lookup"><span data-stu-id="f1303-103">MailboxHoldStatus</span></span>

<span data-ttu-id="f1303-104">El elemento **MailboxHoldStatus** especifica el estado de retención del buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="f1303-104">The **MailboxHoldStatus** element specifies the hold status of the mailbox.</span></span> 
  
```XML
<MailboxHoldStatus>
   <Mailbox/>
   <Status/>
   <AdditionalInfo/>
</MailboxHoldStatus>
```

<span data-ttu-id="f1303-105">**MailboxHoldStatusType**</span><span class="sxs-lookup"><span data-stu-id="f1303-105">**MailboxHoldStatusType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="f1303-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="f1303-106">Attributes and elements</span></span>

<span data-ttu-id="f1303-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="f1303-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f1303-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="f1303-108">Attributes</span></span>

<span data-ttu-id="f1303-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="f1303-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f1303-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="f1303-110">Child elements</span></span>

<span data-ttu-id="f1303-111">[Mailbox (cadena)](mailbox-string.md)  |  [Estado (HoldStatusType)](status-holdstatustype.md)  |  [AdditionalInfo](additionalinfo.md)</span><span class="sxs-lookup"><span data-stu-id="f1303-111">[Mailbox (string)](mailbox-string.md) | [Status (HoldStatusType)](status-holdstatustype.md) | [AdditionalInfo](additionalinfo.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="f1303-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="f1303-112">Parent elements</span></span>

[<span data-ttu-id="f1303-113">MailboxHoldStatuses</span><span class="sxs-lookup"><span data-stu-id="f1303-113">MailboxHoldStatuses</span></span>](mailboxholdstatuses.md)
  
## <a name="remarks"></a><span data-ttu-id="f1303-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f1303-114">Remarks</span></span>

<span data-ttu-id="f1303-115">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="f1303-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="f1303-116">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="f1303-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f1303-117">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="f1303-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f1303-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="f1303-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f1303-119">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="f1303-119">Schema name</span></span>  <br/> |<span data-ttu-id="f1303-120">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="f1303-120">Types schema</span></span>  <br/> |
|<span data-ttu-id="f1303-121">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="f1303-121">Validation file</span></span>  <br/> |<span data-ttu-id="f1303-122">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="f1303-122">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="f1303-123">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="f1303-123">Can be empty</span></span>  <br/> ||
   

