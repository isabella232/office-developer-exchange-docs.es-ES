---
title: MailboxStat
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5f24dc30-3ac2-4c82-9dfc-be9dbdb585be
description: El elemento MailboxStat especifica las estadísticas de un buzón buscado por la búsqueda de detección.
ms.openlocfilehash: 417f63f5e1aa34c2157b1d5ad868461113afec7b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44451435"
---
# <a name="mailboxstat"></a><span data-ttu-id="bca5c-103">MailboxStat</span><span class="sxs-lookup"><span data-stu-id="bca5c-103">MailboxStat</span></span>

<span data-ttu-id="bca5c-104">El elemento **MailboxStat** especifica las estadísticas de un buzón buscado por la búsqueda de detección.</span><span class="sxs-lookup"><span data-stu-id="bca5c-104">The **MailboxStat** element specifies statistics for a mailbox searched by discovery search.</span></span> 
  
```XML
<MailboxStat>
   <MailboxId/>
   <DisplayName/>
   <ItemCount/>
   <Size/>
</MailboxStat>
```

<span data-ttu-id="bca5c-105">**MailboxStatisticsItemType**</span><span class="sxs-lookup"><span data-stu-id="bca5c-105">**MailboxStatisticsItemType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="bca5c-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="bca5c-106">Attributes and elements</span></span>

<span data-ttu-id="bca5c-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="bca5c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="bca5c-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="bca5c-108">Attributes</span></span>

<span data-ttu-id="bca5c-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="bca5c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="bca5c-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="bca5c-110">Child elements</span></span>

<span data-ttu-id="bca5c-111">[Se especifica mailboxid](mailboxid.md)  |  [DisplayName (cadena)](displayname-string.md)  |  [ItemCount](itemcount.md)  |  [Tamaño (largo)](size-long.md)</span><span class="sxs-lookup"><span data-stu-id="bca5c-111">[MailboxId](mailboxid.md) | [DisplayName (string)](displayname-string.md) | [ItemCount](itemcount.md) | [Size (long)](size-long.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="bca5c-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="bca5c-112">Parent elements</span></span>

[<span data-ttu-id="bca5c-113">MailboxStats</span><span class="sxs-lookup"><span data-stu-id="bca5c-113">MailboxStats</span></span>](mailboxstats.md)
  
## <a name="remarks"></a><span data-ttu-id="bca5c-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="bca5c-114">Remarks</span></span>

<span data-ttu-id="bca5c-115">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="bca5c-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="bca5c-116">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="bca5c-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="bca5c-117">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="bca5c-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bca5c-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="bca5c-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="bca5c-119">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="bca5c-119">Schema name</span></span>  <br/> |<span data-ttu-id="bca5c-120">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="bca5c-120">Types schema</span></span>  <br/> |
|<span data-ttu-id="bca5c-121">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="bca5c-121">Validation file</span></span>  <br/> |<span data-ttu-id="bca5c-122">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="bca5c-122">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="bca5c-123">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="bca5c-123">Can be empty</span></span>  <br/> |<span data-ttu-id="bca5c-124">false</span><span class="sxs-lookup"><span data-stu-id="bca5c-124">false</span></span>  <br/> |
   

