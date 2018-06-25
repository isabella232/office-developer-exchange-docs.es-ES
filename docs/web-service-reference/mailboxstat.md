---
title: MailboxStat
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5f24dc30-3ac2-4c82-9dfc-be9dbdb585be
description: El elemento MailboxStat especifica las estadísticas de un buzón de correo buscado por la búsqueda de detección.
ms.openlocfilehash: 692f15904467ce192074b14f7c2a742b3e76de8e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836296"
---
# <a name="mailboxstat"></a><span data-ttu-id="f72de-103">MailboxStat</span><span class="sxs-lookup"><span data-stu-id="f72de-103">MailboxStat</span></span>

<span data-ttu-id="f72de-104">El elemento **MailboxStat** especifica las estadísticas de un buzón de correo buscado por la búsqueda de detección.</span><span class="sxs-lookup"><span data-stu-id="f72de-104">The **MailboxStat** element specifies statistics for a mailbox searched by discovery search.</span></span> 
  
```XML
<MailboxStat>
   <MailboxId/>
   <DisplayName/>
   <ItemCount/>
   <Size/>
</MailboxStat>
```

<span data-ttu-id="f72de-105">**MailboxStatisticsItemType**</span><span class="sxs-lookup"><span data-stu-id="f72de-105">**MailboxStatisticsItemType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="f72de-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="f72de-106">Attributes and elements</span></span>

<span data-ttu-id="f72de-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="f72de-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f72de-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="f72de-108">Attributes</span></span>

<span data-ttu-id="f72de-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="f72de-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f72de-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="f72de-110">Child elements</span></span>

<span data-ttu-id="f72de-111">[MailboxId](mailboxid.md) | [DisplayName (string)](displayname-string.md) | [ItemCount](itemcount.md) | [tamaño (long)](size-long.md)</span><span class="sxs-lookup"><span data-stu-id="f72de-111">[MailboxId](mailboxid.md) | [DisplayName (string)](displayname-string.md) | [ItemCount](itemcount.md) | [Size (long)](size-long.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="f72de-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="f72de-112">Parent elements</span></span>

[<span data-ttu-id="f72de-113">MailboxStats</span><span class="sxs-lookup"><span data-stu-id="f72de-113">MailboxStats</span></span>](mailboxstats.md)
  
## <a name="remarks"></a><span data-ttu-id="f72de-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f72de-114">Remarks</span></span>

<span data-ttu-id="f72de-115">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="f72de-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="f72de-116">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="f72de-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f72de-117">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="f72de-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f72de-118">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f72de-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f72de-119">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="f72de-119">Schema name</span></span>  <br/> |<span data-ttu-id="f72de-120">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="f72de-120">Types schema</span></span>  <br/> |
|<span data-ttu-id="f72de-121">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="f72de-121">Validation file</span></span>  <br/> |<span data-ttu-id="f72de-122">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="f72de-122">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="f72de-123">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="f72de-123">Can be empty</span></span>  <br/> |<span data-ttu-id="f72de-124">falso</span><span class="sxs-lookup"><span data-stu-id="f72de-124">false</span></span>  <br/> |
   

