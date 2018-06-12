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
description: El elemento Period define el nombre, el desplazamiento de tiempo y el identificador único para una región específica de la zona horaria.
ms.openlocfilehash: 3b5d5877e6d9baffdfe536a0feec3b25b6d2883f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836726"
---
# <a name="period"></a><span data-ttu-id="3c4f8-103">Punto</span><span class="sxs-lookup"><span data-stu-id="3c4f8-103">Period</span></span>

<span data-ttu-id="3c4f8-104">El elemento de **período** define el nombre, el desplazamiento de tiempo y el identificador único para una región específica de la zona horaria.</span><span class="sxs-lookup"><span data-stu-id="3c4f8-104">The **Period** element defines the name, time offset, and unique identifier for a specific stage of the time zone.</span></span> 
  
```xml
<Period Bias="" Name="" Id=""/>
```

 <span data-ttu-id="3c4f8-105">**PeriodType**</span><span class="sxs-lookup"><span data-stu-id="3c4f8-105">**PeriodType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3c4f8-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="3c4f8-106">Attributes and elements</span></span>

<span data-ttu-id="3c4f8-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="3c4f8-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3c4f8-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="3c4f8-108">Attributes</span></span>

|<span data-ttu-id="3c4f8-109">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="3c4f8-109">**Attribute**</span></span>|<span data-ttu-id="3c4f8-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3c4f8-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3c4f8-111">Bias</span><span class="sxs-lookup"><span data-stu-id="3c4f8-111">Bias</span></span>  <br/> |<span data-ttu-id="3c4f8-112">Un valor de Duration que representa el desplazamiento de tiempo de la hora Universal coordinada (UTC) para el período.</span><span class="sxs-lookup"><span data-stu-id="3c4f8-112">An xs:duration value that represents the time offset from Coordinated Universal Time (UTC) for the period.</span></span>  <br/> |
|<span data-ttu-id="3c4f8-113">Nombre</span><span class="sxs-lookup"><span data-stu-id="3c4f8-113">Name</span></span>  <br/> |<span data-ttu-id="3c4f8-114">Un valor de tipo string que representa el nombre descriptivo del período.</span><span class="sxs-lookup"><span data-stu-id="3c4f8-114">A string value that represents the descriptive name of the period.</span></span>  <br/> |
|<span data-ttu-id="3c4f8-115">Id</span><span class="sxs-lookup"><span data-stu-id="3c4f8-115">Id</span></span>  <br/> |<span data-ttu-id="3c4f8-116">Un valor de tipo string que representa el identificador para el período.</span><span class="sxs-lookup"><span data-stu-id="3c4f8-116">A string value that represents the identifier for the period.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="3c4f8-117">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="3c4f8-117">Child elements</span></span>

<span data-ttu-id="3c4f8-118">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="3c4f8-118">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="3c4f8-119">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="3c4f8-119">Parent elements</span></span>

|<span data-ttu-id="3c4f8-120">**Element**</span><span class="sxs-lookup"><span data-stu-id="3c4f8-120">**Element**</span></span>|<span data-ttu-id="3c4f8-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3c4f8-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3c4f8-122">Períodos</span><span class="sxs-lookup"><span data-stu-id="3c4f8-122">Periods</span></span>](periods.md) <br/> |<span data-ttu-id="3c4f8-123">Representa una matriz de los períodos que definen el desplazamiento de tiempo en diferentes fases de la zona horaria.</span><span class="sxs-lookup"><span data-stu-id="3c4f8-123">Represents an array of periods that define the time offset at different stages of the time zone.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="3c4f8-124">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="3c4f8-124">Text value</span></span>

<span data-ttu-id="3c4f8-125">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="3c4f8-125">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3c4f8-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3c4f8-126">Remarks</span></span>

<span data-ttu-id="3c4f8-127">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="3c4f8-127">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3c4f8-128">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="3c4f8-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3c4f8-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3c4f8-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="3c4f8-130">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="3c4f8-130">Schema Name</span></span>  <br/> |<span data-ttu-id="3c4f8-131">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="3c4f8-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="3c4f8-132">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="3c4f8-132">Validation File</span></span>  <br/> |<span data-ttu-id="3c4f8-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="3c4f8-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="3c4f8-134">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="3c4f8-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="3c4f8-135">False</span><span class="sxs-lookup"><span data-stu-id="3c4f8-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3c4f8-136">Ver también</span><span class="sxs-lookup"><span data-stu-id="3c4f8-136">See also</span></span>



- [<span data-ttu-id="3c4f8-137">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="3c4f8-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

