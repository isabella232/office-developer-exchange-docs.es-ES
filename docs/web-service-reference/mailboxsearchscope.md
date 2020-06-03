---
title: MailboxSearchScope
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ef4a4203-61e5-46b8-9fa4-d1a10e785aa2
description: El elemento MailboxSearchScope especifica un buzón y un ámbito de búsqueda para una búsqueda de detección.
ms.openlocfilehash: 20f528ddfb4812de8468af33bcb0b47d7d851f1d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457189"
---
# <a name="mailboxsearchscope"></a><span data-ttu-id="40b1a-103">MailboxSearchScope</span><span class="sxs-lookup"><span data-stu-id="40b1a-103">MailboxSearchScope</span></span>

<span data-ttu-id="40b1a-104">El elemento **MailboxSearchScope** especifica un buzón y un ámbito de búsqueda para una búsqueda de detección.</span><span class="sxs-lookup"><span data-stu-id="40b1a-104">The **MailboxSearchScope** element specifies a mailbox and a search scope for a discovery search.</span></span> 
  
```XML
<MailboxSearchScope>
   <Mailbox/>
   <SearchScope/>
<MailboxSearchScope>
```

<span data-ttu-id="40b1a-105">**MailboxSearchScopeType**</span><span class="sxs-lookup"><span data-stu-id="40b1a-105">**MailboxSearchScopeType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="40b1a-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="40b1a-106">Attributes and elements</span></span>

<span data-ttu-id="40b1a-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="40b1a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="40b1a-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="40b1a-108">Attributes</span></span>

<span data-ttu-id="40b1a-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="40b1a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="40b1a-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="40b1a-110">Child elements</span></span>

<span data-ttu-id="40b1a-111">[Mailbox (cadena)](mailbox-string.md)  |  [SearchScope](searchscope.md)</span><span class="sxs-lookup"><span data-stu-id="40b1a-111">[Mailbox (string)](mailbox-string.md) | [SearchScope](searchscope.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="40b1a-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="40b1a-112">Parent elements</span></span>

[<span data-ttu-id="40b1a-113">MailboxSearchScopes</span><span class="sxs-lookup"><span data-stu-id="40b1a-113">MailboxSearchScopes</span></span>](mailboxsearchscopes.md)
  
## <a name="remarks"></a><span data-ttu-id="40b1a-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="40b1a-114">Remarks</span></span>

<span data-ttu-id="40b1a-115">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="40b1a-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="40b1a-116">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="40b1a-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="40b1a-117">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="40b1a-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="40b1a-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="40b1a-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="40b1a-119">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="40b1a-119">Schema name</span></span>  <br/> |<span data-ttu-id="40b1a-120">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="40b1a-120">Types schema</span></span>  <br/> |
|<span data-ttu-id="40b1a-121">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="40b1a-121">Validation file</span></span>  <br/> |<span data-ttu-id="40b1a-122">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="40b1a-122">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="40b1a-123">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="40b1a-123">Can be empty</span></span>  <br/> ||
   

