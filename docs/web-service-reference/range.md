---
title: Rango
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ee2891e4-3aa6-4258-9727-1f2ee9622508
description: El elemento Range especifica un intervalo de repeticiones de elementos de calendario para un elemento de calendario que se repite.
ms.openlocfilehash: b5fb41709905290326b47e2662383031c34fd9c9
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465313"
---
# <a name="range"></a><span data-ttu-id="0f0af-103">Rango</span><span class="sxs-lookup"><span data-stu-id="0f0af-103">Range</span></span>

<span data-ttu-id="0f0af-104">El elemento **Range** especifica un intervalo de repeticiones de elementos de calendario para un elemento de calendario que se repite.</span><span class="sxs-lookup"><span data-stu-id="0f0af-104">The **Range** element specifies a range of calendar item occurrences for a repeating calendar item.</span></span> 
  
```XML
<Range Start="" End="" Count="" CompareOriginalStartTime=""/>
```

 <span data-ttu-id="0f0af-105">**OccurrencesRangeType**</span><span class="sxs-lookup"><span data-stu-id="0f0af-105">**OccurrencesRangeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0f0af-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="0f0af-106">Attributes and elements</span></span>

<span data-ttu-id="0f0af-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="0f0af-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0f0af-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="0f0af-108">Attributes</span></span>

|<span data-ttu-id="0f0af-109">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="0f0af-109">**Attribute**</span></span>|<span data-ttu-id="0f0af-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0f0af-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0f0af-111">**Start**</span><span class="sxs-lookup"><span data-stu-id="0f0af-111">**Start**</span></span> <br/> |<span data-ttu-id="0f0af-112">El valor de texto del atributo **Start** es la fecha de inicio del intervalo de elementos periódicos.</span><span class="sxs-lookup"><span data-stu-id="0f0af-112">The text value of the **Start** attribute is the start date of the recurring item range.</span></span> <span data-ttu-id="0f0af-113">Se trata de un valor de **fecha y hora** .</span><span class="sxs-lookup"><span data-stu-id="0f0af-113">This is a **dateTime** value.</span></span>  <br/> |
|<span data-ttu-id="0f0af-114">**End**</span><span class="sxs-lookup"><span data-stu-id="0f0af-114">**End**</span></span> <br/> |<span data-ttu-id="0f0af-115">El valor de texto del atributo **final** es la fecha de finalización del intervalo de elementos periódicos.</span><span class="sxs-lookup"><span data-stu-id="0f0af-115">The text value of the **End** attribute is the end date of the recurring item range.</span></span> <span data-ttu-id="0f0af-116">Se trata de un valor de **fecha y hora** .</span><span class="sxs-lookup"><span data-stu-id="0f0af-116">This is a **dateTime** value.</span></span>  <br/> |
|<span data-ttu-id="0f0af-117">**Count**</span><span class="sxs-lookup"><span data-stu-id="0f0af-117">**Count**</span></span> <br/> |<span data-ttu-id="0f0af-118">El valor de texto del atributo **Count** es el número de repeticiones del elemento periódico.</span><span class="sxs-lookup"><span data-stu-id="0f0af-118">The text value of the **Count** attribute is the number of occurrences of the recurring item.</span></span> <span data-ttu-id="0f0af-119">Se trata de un valor **entero** .</span><span class="sxs-lookup"><span data-stu-id="0f0af-119">This is an **integer** value.</span></span>  <br/> |
|<span data-ttu-id="0f0af-120">**CompareOriginalStartTime**</span><span class="sxs-lookup"><span data-stu-id="0f0af-120">**CompareOriginalStartTime**</span></span> <br/> |<span data-ttu-id="0f0af-121">El valor de texto de **true** para el atributo **CompareOriginalStartTime** indica que el cliente debe comparar la hora de inicio original con la nueva hora de inicio.</span><span class="sxs-lookup"><span data-stu-id="0f0af-121">The text value of **true** for the **CompareOriginalStartTime** attribute indicates that the client should compare the original start time with the new start time.</span></span> <span data-ttu-id="0f0af-122">Un valor de **false** indica que el cliente no tiene que comparar la hora de inicio original con la nueva hora de inicio.</span><span class="sxs-lookup"><span data-stu-id="0f0af-122">A value of **false** indicates that the client does not need to compare the original start time with the new start time.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="0f0af-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="0f0af-123">Child elements</span></span>

<span data-ttu-id="0f0af-124">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="0f0af-124">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="0f0af-125">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="0f0af-125">Parent elements</span></span>

[<span data-ttu-id="0f0af-126">Ranges</span><span class="sxs-lookup"><span data-stu-id="0f0af-126">Ranges</span></span>](ranges.md)
  
## <a name="remarks"></a><span data-ttu-id="0f0af-127">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0f0af-127">Remarks</span></span>

<span data-ttu-id="0f0af-128">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="0f0af-128">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="0f0af-129">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="0f0af-129">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0f0af-130">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="0f0af-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0f0af-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="0f0af-131">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="0f0af-132">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="0f0af-132">Schema name</span></span>  <br/> |<span data-ttu-id="0f0af-133">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="0f0af-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="0f0af-134">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="0f0af-134">Validation file</span></span>  <br/> |<span data-ttu-id="0f0af-135">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="0f0af-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="0f0af-136">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="0f0af-136">Can be empty</span></span>  <br/> ||
   

