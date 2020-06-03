---
title: IncludeNonIndexableItems
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: af7f202b-2889-447e-bdeb-aaad18ce6b46
description: El elemento IncludeNonIndexableItems contiene un valor booleano que indica si se deben incluir los elementos que no se pueden indizar.
ms.openlocfilehash: eab559e938f0b949d79626ae5bf61b3d4a838924
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44460627"
---
# <a name="includenonindexableitems"></a><span data-ttu-id="e0ddf-103">IncludeNonIndexableItems</span><span class="sxs-lookup"><span data-stu-id="e0ddf-103">IncludeNonIndexableItems</span></span>

<span data-ttu-id="e0ddf-104">El elemento **IncludeNonIndexableItems** contiene un valor **booleano** que indica si se deben incluir los elementos que no se pueden indizar.</span><span class="sxs-lookup"><span data-stu-id="e0ddf-104">The **IncludeNonIndexableItems** element contains a **Boolean** value to indicate whether to include items that cannot be indexed.</span></span> 
  
```XML
<IncludeNonIndexableItems>true | false</IncludeNonIndexableItems>
```

 <span data-ttu-id="e0ddf-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="e0ddf-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e0ddf-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="e0ddf-106">Attributes and elements</span></span>

<span data-ttu-id="e0ddf-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="e0ddf-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e0ddf-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="e0ddf-108">Attributes</span></span>

<span data-ttu-id="e0ddf-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="e0ddf-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e0ddf-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="e0ddf-110">Child elements</span></span>

<span data-ttu-id="e0ddf-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="e0ddf-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="e0ddf-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="e0ddf-112">Parent elements</span></span>

[<span data-ttu-id="e0ddf-113">SetHoldOnMailboxes</span><span class="sxs-lookup"><span data-stu-id="e0ddf-113">SetHoldOnMailboxes</span></span>](setholdonmailboxes.md)
  
## <a name="text-value"></a><span data-ttu-id="e0ddf-114">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="e0ddf-114">Text value</span></span>

<span data-ttu-id="e0ddf-115">Un valor de texto de **true** para el elemento **IncludeNonIndexableItems** indica que los elementos que no se pueden indizar se incluyen en la retención de buzones.</span><span class="sxs-lookup"><span data-stu-id="e0ddf-115">A text value of **true** for the **IncludeNonIndexableItems** element indicates that items that cannot be indexed are included with mailbox holds.</span></span> <span data-ttu-id="e0ddf-116">Un valor de **false** indica que los elementos que no se pueden indizar no se incluyen en la retención de buzones.</span><span class="sxs-lookup"><span data-stu-id="e0ddf-116">A value of **false** indicates that the items that cannot be indexed are not included in mailbox holds.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="e0ddf-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e0ddf-117">Remarks</span></span>

<span data-ttu-id="e0ddf-118">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="e0ddf-118">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="e0ddf-119">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="e0ddf-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e0ddf-120">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="e0ddf-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e0ddf-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="e0ddf-121">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="e0ddf-122">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="e0ddf-122">Schema name</span></span>  <br/> |<span data-ttu-id="e0ddf-123">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="e0ddf-123">Messages schema</span></span>  <br/> |
|<span data-ttu-id="e0ddf-124">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="e0ddf-124">Validation file</span></span>  <br/> |<span data-ttu-id="e0ddf-125">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="e0ddf-125">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="e0ddf-126">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="e0ddf-126">Can be empty</span></span>  <br/> |<span data-ttu-id="e0ddf-127">false</span><span class="sxs-lookup"><span data-stu-id="e0ddf-127">false</span></span>  <br/> |
   

