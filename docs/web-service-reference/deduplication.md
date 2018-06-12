---
title: Desduplicación
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a38acc3d-29a8-4466-81a4-73cb30fe5e80
description: El elemento de desduplicación indica si el resultado de búsqueda debe quitar los elementos duplicados.
ms.openlocfilehash: 3f06bb1dccd0677b7fd43c4ad82eda54a0c3f812
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764065"
---
# <a name="deduplication"></a><span data-ttu-id="48995-103">Desduplicación</span><span class="sxs-lookup"><span data-stu-id="48995-103">Deduplication</span></span>

<span data-ttu-id="48995-104">El elemento de **desduplicación** indica si el resultado de búsqueda debe quitar los elementos duplicados.</span><span class="sxs-lookup"><span data-stu-id="48995-104">The **Deduplication** element indicates whether the search result should remove duplicate items.</span></span> 
  
```XML
<Deduplication> true | false </Deduplication>
```

<span data-ttu-id="48995-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="48995-105">**Boolean**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="48995-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="48995-106">Attributes and elements</span></span>

<span data-ttu-id="48995-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="48995-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="48995-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="48995-108">Attributes</span></span>

<span data-ttu-id="48995-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="48995-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="48995-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="48995-110">Child elements</span></span>

<span data-ttu-id="48995-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="48995-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="48995-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="48995-112">Parent elements</span></span>

<span data-ttu-id="48995-113">[SearchMailboxes](searchmailboxes.md) | [SetHoldOnMailboxes](setholdonmailboxes.md)</span><span class="sxs-lookup"><span data-stu-id="48995-113">[SearchMailboxes](searchmailboxes.md) | [SetHoldOnMailboxes](setholdonmailboxes.md)</span></span>
  
## <a name="text-value"></a><span data-ttu-id="48995-114">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="48995-114">Text value</span></span>

<span data-ttu-id="48995-115">Un valor de texto de **true** para el elemento de desduplicación indica que los resultados de búsqueda no pueden contener elementos duplicados.</span><span class="sxs-lookup"><span data-stu-id="48995-115">A text value of **true** for the Deduplication element indicates that search results may not contain duplicate items.</span></span> <span data-ttu-id="48995-116">Un valor de **false** indica que los resultados de búsqueda pueden contener elementos duplicados.</span><span class="sxs-lookup"><span data-stu-id="48995-116">A value of **false** indicates that search results may contain duplicate items.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="48995-117">Notas</span><span class="sxs-lookup"><span data-stu-id="48995-117">Remarks</span></span>

<span data-ttu-id="48995-118">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="48995-118">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="48995-119">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="48995-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="48995-120">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="48995-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="48995-121">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="48995-121">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="48995-122">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="48995-122">Schema name</span></span>  <br/> |<span data-ttu-id="48995-123">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="48995-123">Types schema</span></span>  <br/> |
|<span data-ttu-id="48995-124">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="48995-124">Validation file</span></span>  <br/> |<span data-ttu-id="48995-125">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="48995-125">types.xsd</span></span>  <br/> |
|<span data-ttu-id="48995-126">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="48995-126">Can be empty</span></span>  <br/> |<span data-ttu-id="48995-127">falso</span><span class="sxs-lookup"><span data-stu-id="48995-127">false</span></span>  <br/> |
   

