---
title: Punto
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Period
api_type:
- schema
ms.assetid: 2f9cf6af-c531-4d7d-90c9-1a1db504d890
description: El elemento period define el nombre, el desplazamiento de tiempo y el identificador único de una fase específica de la zona horaria.
ms.openlocfilehash: a7c36a9de01fd0484a7df75de3b5525992ef7ee7
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459724"
---
# <a name="period"></a><span data-ttu-id="464c0-103">Punto</span><span class="sxs-lookup"><span data-stu-id="464c0-103">Period</span></span>

<span data-ttu-id="464c0-104">El elemento **period** define el nombre, el desplazamiento de tiempo y el identificador único de una fase específica de la zona horaria.</span><span class="sxs-lookup"><span data-stu-id="464c0-104">The **Period** element defines the name, time offset, and unique identifier for a specific stage of the time zone.</span></span> 
  
```xml
<Period Bias="" Name="" Id=""/>
```

 <span data-ttu-id="464c0-105">**PeriodType**</span><span class="sxs-lookup"><span data-stu-id="464c0-105">**PeriodType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="464c0-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="464c0-106">Attributes and elements</span></span>

<span data-ttu-id="464c0-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="464c0-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="464c0-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="464c0-108">Attributes</span></span>

|<span data-ttu-id="464c0-109">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="464c0-109">**Attribute**</span></span>|<span data-ttu-id="464c0-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="464c0-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="464c0-111">Sesgo</span><span class="sxs-lookup"><span data-stu-id="464c0-111">Bias</span></span>  <br/> |<span data-ttu-id="464c0-112">Un valor XS: Duration que representa el desplazamiento de tiempo desde la hora universal coordinada (UTC) para el período.</span><span class="sxs-lookup"><span data-stu-id="464c0-112">An xs:duration value that represents the time offset from Coordinated Universal Time (UTC) for the period.</span></span>  <br/> |
|<span data-ttu-id="464c0-113">Nombre</span><span class="sxs-lookup"><span data-stu-id="464c0-113">Name</span></span>  <br/> |<span data-ttu-id="464c0-114">Un valor de tipo String que representa el nombre descriptivo del punto.</span><span class="sxs-lookup"><span data-stu-id="464c0-114">A string value that represents the descriptive name of the period.</span></span>  <br/> |
|<span data-ttu-id="464c0-115">Id</span><span class="sxs-lookup"><span data-stu-id="464c0-115">Id</span></span>  <br/> |<span data-ttu-id="464c0-116">Un valor de tipo String que representa el identificador del período.</span><span class="sxs-lookup"><span data-stu-id="464c0-116">A string value that represents the identifier for the period.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="464c0-117">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="464c0-117">Child elements</span></span>

<span data-ttu-id="464c0-118">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="464c0-118">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="464c0-119">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="464c0-119">Parent elements</span></span>

|<span data-ttu-id="464c0-120">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="464c0-120">**Element**</span></span>|<span data-ttu-id="464c0-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="464c0-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="464c0-122">Períodos</span><span class="sxs-lookup"><span data-stu-id="464c0-122">Periods</span></span>](periods.md) <br/> |<span data-ttu-id="464c0-123">Representa una matriz de puntos que definen el desplazamiento de tiempo en diferentes etapas de la zona horaria.</span><span class="sxs-lookup"><span data-stu-id="464c0-123">Represents an array of periods that define the time offset at different stages of the time zone.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="464c0-124">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="464c0-124">Text value</span></span>

<span data-ttu-id="464c0-125">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="464c0-125">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="464c0-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="464c0-126">Remarks</span></span>

<span data-ttu-id="464c0-127">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="464c0-127">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="464c0-128">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="464c0-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="464c0-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="464c0-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="464c0-130">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="464c0-130">Schema Name</span></span>  <br/> |<span data-ttu-id="464c0-131">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="464c0-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="464c0-132">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="464c0-132">Validation File</span></span>  <br/> |<span data-ttu-id="464c0-133">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="464c0-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="464c0-134">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="464c0-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="464c0-135">Falso</span><span class="sxs-lookup"><span data-stu-id="464c0-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="464c0-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="464c0-136">See also</span></span>



- [<span data-ttu-id="464c0-137">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="464c0-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

