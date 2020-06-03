---
title: RecurringMasterItemIdRanges
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5c9c89b5-4ce8-437b-a332-fa7ed35c8388
description: El elemento RecurringMasterItemIdRanges especifica una matriz de intervalos de repeticiones.
ms.openlocfilehash: 784676844c5c58c65b8cc6177843bf26d351b7d9
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44528758"
---
# <a name="recurringmasteritemidranges"></a><span data-ttu-id="11965-103">RecurringMasterItemIdRanges</span><span class="sxs-lookup"><span data-stu-id="11965-103">RecurringMasterItemIdRanges</span></span>

<span data-ttu-id="11965-104">El elemento **RecurringMasterItemIdRanges** especifica una matriz de intervalos de repeticiones.</span><span class="sxs-lookup"><span data-stu-id="11965-104">The **RecurringMasterItemIdRanges** element specifies an array of occurrence ranges.</span></span> 
  
```XML
<RecurringMasterItemIdRanges Id="" ChangeKey="">
   <Ranges/>
</RecurringMasterItemIdRanges>
```

 <span data-ttu-id="11965-105">**RecurringMasterItemIdRangesType**</span><span class="sxs-lookup"><span data-stu-id="11965-105">**RecurringMasterItemIdRangesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="11965-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="11965-106">Attributes and elements</span></span>

<span data-ttu-id="11965-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="11965-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="11965-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="11965-108">Attributes</span></span>

|<span data-ttu-id="11965-109">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="11965-109">**Attribute**</span></span>|<span data-ttu-id="11965-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="11965-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="11965-111">**Id**</span><span class="sxs-lookup"><span data-stu-id="11965-111">**Id**</span></span> <br/> |<span data-ttu-id="11965-112">El valor de texto del atributo **ID** es un identificador único del elemento maestro periódico.</span><span class="sxs-lookup"><span data-stu-id="11965-112">The text value of the **Id** attribute is a recurring master item's unique identifier.</span></span> <span data-ttu-id="11965-113">Se trata de un valor de **cadena** .</span><span class="sxs-lookup"><span data-stu-id="11965-113">This is a **string** value.</span></span>  <br/> |
|<span data-ttu-id="11965-114">**ChangeKey**</span><span class="sxs-lookup"><span data-stu-id="11965-114">**ChangeKey**</span></span> <br/> |<span data-ttu-id="11965-115">El valor de texto del atributo **changekey** es la clave de cambio periódico del elemento maestro.</span><span class="sxs-lookup"><span data-stu-id="11965-115">The text value of the **ChangeKey** attribute is the recurring master item's change key.</span></span> <span data-ttu-id="11965-116">Se trata de un valor de **cadena** .</span><span class="sxs-lookup"><span data-stu-id="11965-116">This is a **string** value.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="11965-117">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="11965-117">Child elements</span></span>

[<span data-ttu-id="11965-118">Ranges</span><span class="sxs-lookup"><span data-stu-id="11965-118">Ranges</span></span>](ranges.md)
  
### <a name="parent-elements"></a><span data-ttu-id="11965-119">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="11965-119">Parent elements</span></span>

<span data-ttu-id="11965-120">[ItemIds](itemids.md)  |  [GlobalItemIds](globalitemids.md)  |  [DraftItemIds](draftitemids.md)  |  [ContactIds](contactids.md)  |  [GroupIds](groupids.md)</span><span class="sxs-lookup"><span data-stu-id="11965-120">[ItemIds](itemids.md) | [GlobalItemIds](globalitemids.md) | [DraftItemIds](draftitemids.md) | [ContactIds](contactids.md) | [GroupIds](groupids.md)</span></span>
  
## <a name="remarks"></a><span data-ttu-id="11965-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="11965-121">Remarks</span></span>

<span data-ttu-id="11965-122">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="11965-122">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="11965-123">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="11965-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="11965-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="11965-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="11965-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="11965-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="11965-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="11965-126">Schema name</span></span>  <br/> |<span data-ttu-id="11965-127">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="11965-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="11965-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="11965-128">Validation file</span></span>  <br/> |<span data-ttu-id="11965-129">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="11965-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="11965-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="11965-130">Can be empty</span></span>  <br/> ||
   

