---
title: RecurringMasterItemIdRanges
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5c9c89b5-4ce8-437b-a332-fa7ed35c8388
description: El elemento RecurringMasterItemIdRanges especifica una matriz de rangos de repetición.
ms.openlocfilehash: 60d987f475bed5d630a1238550e4d14578ebd0d5
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19837016"
---
# <a name="recurringmasteritemidranges"></a><span data-ttu-id="8645d-103">RecurringMasterItemIdRanges</span><span class="sxs-lookup"><span data-stu-id="8645d-103">RecurringMasterItemIdRanges</span></span>

<span data-ttu-id="8645d-104">El elemento **RecurringMasterItemIdRanges** especifica una matriz de rangos de repetición.</span><span class="sxs-lookup"><span data-stu-id="8645d-104">The **RecurringMasterItemIdRanges** element specifies an array of occurrence ranges.</span></span> 
  
```XML
<RecurringMasterItemIdRanges Id="" ChangeKey="">
   <Ranges/>
</RecurringMasterItemIdRanges>
```

 <span data-ttu-id="8645d-105">**RecurringMasterItemIdRangesType**</span><span class="sxs-lookup"><span data-stu-id="8645d-105">**RecurringMasterItemIdRangesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="8645d-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="8645d-106">Attributes and elements</span></span>

<span data-ttu-id="8645d-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="8645d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8645d-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="8645d-108">Attributes</span></span>

|<span data-ttu-id="8645d-109">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="8645d-109">**Attribute**</span></span>|<span data-ttu-id="8645d-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8645d-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8645d-111">**Id**</span><span class="sxs-lookup"><span data-stu-id="8645d-111">**Id**</span></span> <br/> |<span data-ttu-id="8645d-112">El valor de texto del atributo **Id** es el identificador único de un elemento maestro periódico.</span><span class="sxs-lookup"><span data-stu-id="8645d-112">The text value of the **Id** attribute is a recurring master item's unique identifier.</span></span> <span data-ttu-id="8645d-113">Esto es un valor de **tipo string** .</span><span class="sxs-lookup"><span data-stu-id="8645d-113">This is a **string** value.</span></span>  <br/> |
|<span data-ttu-id="8645d-114">**ChangeKey**</span><span class="sxs-lookup"><span data-stu-id="8645d-114">**ChangeKey**</span></span> <br/> |<span data-ttu-id="8645d-115">El valor de texto del atributo **ChangeKey** es cambiar la clave del producto principal periódica.</span><span class="sxs-lookup"><span data-stu-id="8645d-115">The text value of the **ChangeKey** attribute is the recurring master item's change key.</span></span> <span data-ttu-id="8645d-116">Esto es un valor de **tipo string** .</span><span class="sxs-lookup"><span data-stu-id="8645d-116">This is a **string** value.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="8645d-117">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="8645d-117">Child elements</span></span>

[<span data-ttu-id="8645d-118">Ranges</span><span class="sxs-lookup"><span data-stu-id="8645d-118">Ranges</span></span>](ranges.md)
  
### <a name="parent-elements"></a><span data-ttu-id="8645d-119">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="8645d-119">Parent elements</span></span>

<span data-ttu-id="8645d-120">[ItemId](itemids.md) | [GlobalItemIds](globalitemids.md) | [DraftItemIds](draftitemids.md) | [ContactIds](contactids.md) | [GroupIds](groupids.md)</span><span class="sxs-lookup"><span data-stu-id="8645d-120">[ItemIds](itemids.md) | [GlobalItemIds](globalitemids.md) | [DraftItemIds](draftitemids.md) | [ContactIds](contactids.md) | [GroupIds](groupids.md)</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8645d-121">Notas</span><span class="sxs-lookup"><span data-stu-id="8645d-121">Remarks</span></span>

<span data-ttu-id="8645d-122">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="8645d-122">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="8645d-123">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="8645d-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8645d-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="8645d-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8645d-125">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="8645d-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="8645d-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="8645d-126">Schema name</span></span>  <br/> |<span data-ttu-id="8645d-127">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="8645d-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="8645d-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="8645d-128">Validation file</span></span>  <br/> |<span data-ttu-id="8645d-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="8645d-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="8645d-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="8645d-130">Can be empty</span></span>  <br/> ||
   

