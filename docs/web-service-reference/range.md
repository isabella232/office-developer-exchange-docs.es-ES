---
title: Rango
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ee2891e4-3aa6-4258-9727-1f2ee9622508
description: El elemento de intervalo especifica el intervalo de repeticiones del elemento de calendario para un elemento de calendario periódico.
ms.openlocfilehash: 0264c541604808b46a50e292b8ff75f205796295
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836946"
---
# <a name="range"></a><span data-ttu-id="e6b3f-103">Rango</span><span class="sxs-lookup"><span data-stu-id="e6b3f-103">Range</span></span>

<span data-ttu-id="e6b3f-104">El elemento **Range** especifica el intervalo de repeticiones del elemento de calendario para un elemento de calendario periódico.</span><span class="sxs-lookup"><span data-stu-id="e6b3f-104">The **Range** element specifies a range of calendar item occurrences for a repeating calendar item.</span></span> 
  
```XML
<Range Start="" End="" Count="" CompareOriginalStartTime=""/>
```

 <span data-ttu-id="e6b3f-105">**OccurrencesRangeType**</span><span class="sxs-lookup"><span data-stu-id="e6b3f-105">**OccurrencesRangeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e6b3f-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="e6b3f-106">Attributes and elements</span></span>

<span data-ttu-id="e6b3f-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="e6b3f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e6b3f-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="e6b3f-108">Attributes</span></span>

|<span data-ttu-id="e6b3f-109">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="e6b3f-109">**Attribute**</span></span>|<span data-ttu-id="e6b3f-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e6b3f-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e6b3f-111">**Start**</span><span class="sxs-lookup"><span data-stu-id="e6b3f-111">**Start**</span></span> <br/> |<span data-ttu-id="e6b3f-112">El valor de texto del atributo **Iniciar** es la fecha de inicio del intervalo de elemento periódico.</span><span class="sxs-lookup"><span data-stu-id="e6b3f-112">The text value of the **Start** attribute is the start date of the recurring item range.</span></span> <span data-ttu-id="e6b3f-113">Esto es un valor de **fecha y hora** .</span><span class="sxs-lookup"><span data-stu-id="e6b3f-113">This is a **dateTime** value.</span></span>  <br/> |
|<span data-ttu-id="e6b3f-114">**End**</span><span class="sxs-lookup"><span data-stu-id="e6b3f-114">**End**</span></span> <br/> |<span data-ttu-id="e6b3f-115">El valor de texto del atributo **final** es la fecha de finalización del intervalo de elemento periódico.</span><span class="sxs-lookup"><span data-stu-id="e6b3f-115">The text value of the **End** attribute is the end date of the recurring item range.</span></span> <span data-ttu-id="e6b3f-116">Esto es un valor de **fecha y hora** .</span><span class="sxs-lookup"><span data-stu-id="e6b3f-116">This is a **dateTime** value.</span></span>  <br/> |
|<span data-ttu-id="e6b3f-117">**Count**</span><span class="sxs-lookup"><span data-stu-id="e6b3f-117">**Count**</span></span> <br/> |<span data-ttu-id="e6b3f-118">El valor de texto del atributo **Count** es el número de repeticiones del elemento periódico.</span><span class="sxs-lookup"><span data-stu-id="e6b3f-118">The text value of the **Count** attribute is the number of occurrences of the recurring item.</span></span> <span data-ttu-id="e6b3f-119">Esto es un valor **entero** .</span><span class="sxs-lookup"><span data-stu-id="e6b3f-119">This is an **integer** value.</span></span>  <br/> |
|<span data-ttu-id="e6b3f-120">**CompareOriginalStartTime**</span><span class="sxs-lookup"><span data-stu-id="e6b3f-120">**CompareOriginalStartTime**</span></span> <br/> |<span data-ttu-id="e6b3f-121">El valor de texto de **true** para el atributo **CompareOriginalStartTime** indica que el cliente debe comparar la hora de inicio original con la nueva hora de inicio.</span><span class="sxs-lookup"><span data-stu-id="e6b3f-121">The text value of **true** for the **CompareOriginalStartTime** attribute indicates that the client should compare the original start time with the new start time.</span></span> <span data-ttu-id="e6b3f-122">Un valor de **false** indica que el cliente no es necesario comparar la hora de inicio original con la nueva hora de inicio.</span><span class="sxs-lookup"><span data-stu-id="e6b3f-122">A value of **false** indicates that the client does not need to compare the original start time with the new start time.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="e6b3f-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="e6b3f-123">Child elements</span></span>

<span data-ttu-id="e6b3f-124">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="e6b3f-124">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="e6b3f-125">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="e6b3f-125">Parent elements</span></span>

[<span data-ttu-id="e6b3f-126">Ranges</span><span class="sxs-lookup"><span data-stu-id="e6b3f-126">Ranges</span></span>](ranges.md)
  
## <a name="remarks"></a><span data-ttu-id="e6b3f-127">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e6b3f-127">Remarks</span></span>

<span data-ttu-id="e6b3f-128">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="e6b3f-128">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="e6b3f-129">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="e6b3f-129">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e6b3f-130">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="e6b3f-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e6b3f-131">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e6b3f-131">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="e6b3f-132">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="e6b3f-132">Schema name</span></span>  <br/> |<span data-ttu-id="e6b3f-133">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="e6b3f-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="e6b3f-134">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="e6b3f-134">Validation file</span></span>  <br/> |<span data-ttu-id="e6b3f-135">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="e6b3f-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="e6b3f-136">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="e6b3f-136">Can be empty</span></span>  <br/> ||
   

