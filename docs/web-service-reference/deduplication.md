---
title: Desduplicación
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a38acc3d-29a8-4466-81a4-73cb30fe5e80
description: El elemento de desduplicación indica si el resultado de la búsqueda debe quitar elementos duplicados.
ms.openlocfilehash: c39f980658aba7036cfabb3b51af5a41005f97b6
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463716"
---
# <a name="deduplication"></a><span data-ttu-id="1bcf2-103">Desduplicación</span><span class="sxs-lookup"><span data-stu-id="1bcf2-103">Deduplication</span></span>

<span data-ttu-id="1bcf2-104">El elemento de **desduplicación** indica si el resultado de la búsqueda debe quitar elementos duplicados.</span><span class="sxs-lookup"><span data-stu-id="1bcf2-104">The **Deduplication** element indicates whether the search result should remove duplicate items.</span></span> 
  
```XML
<Deduplication> true | false </Deduplication>
```

<span data-ttu-id="1bcf2-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="1bcf2-105">**Boolean**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="1bcf2-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="1bcf2-106">Attributes and elements</span></span>

<span data-ttu-id="1bcf2-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="1bcf2-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1bcf2-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="1bcf2-108">Attributes</span></span>

<span data-ttu-id="1bcf2-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="1bcf2-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1bcf2-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="1bcf2-110">Child elements</span></span>

<span data-ttu-id="1bcf2-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="1bcf2-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="1bcf2-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="1bcf2-112">Parent elements</span></span>

<span data-ttu-id="1bcf2-113">[SearchMailboxes](searchmailboxes.md)  |  [SetHoldOnMailboxes](setholdonmailboxes.md)</span><span class="sxs-lookup"><span data-stu-id="1bcf2-113">[SearchMailboxes](searchmailboxes.md) | [SetHoldOnMailboxes](setholdonmailboxes.md)</span></span>
  
## <a name="text-value"></a><span data-ttu-id="1bcf2-114">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="1bcf2-114">Text value</span></span>

<span data-ttu-id="1bcf2-115">Un valor de texto de **true** para el elemento de desduplicación indica que los resultados de la búsqueda no pueden contener elementos duplicados.</span><span class="sxs-lookup"><span data-stu-id="1bcf2-115">A text value of **true** for the Deduplication element indicates that search results may not contain duplicate items.</span></span> <span data-ttu-id="1bcf2-116">Un valor de **false** indica que los resultados de la búsqueda pueden contener elementos duplicados.</span><span class="sxs-lookup"><span data-stu-id="1bcf2-116">A value of **false** indicates that search results may contain duplicate items.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="1bcf2-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1bcf2-117">Remarks</span></span>

<span data-ttu-id="1bcf2-118">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="1bcf2-118">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="1bcf2-119">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="1bcf2-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1bcf2-120">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="1bcf2-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1bcf2-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="1bcf2-121">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="1bcf2-122">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="1bcf2-122">Schema name</span></span>  <br/> |<span data-ttu-id="1bcf2-123">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="1bcf2-123">Types schema</span></span>  <br/> |
|<span data-ttu-id="1bcf2-124">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="1bcf2-124">Validation file</span></span>  <br/> |<span data-ttu-id="1bcf2-125">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="1bcf2-125">types.xsd</span></span>  <br/> |
|<span data-ttu-id="1bcf2-126">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="1bcf2-126">Can be empty</span></span>  <br/> |<span data-ttu-id="1bcf2-127">false</span><span class="sxs-lookup"><span data-stu-id="1bcf2-127">false</span></span>  <br/> |
   

