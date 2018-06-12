---
title: WithinSizeRange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- WithinSizeRange
api_type:
- schema
ms.assetid: 6f98650e-3399-4f87-9b7f-40bf20cdb821
description: El elemento WithinSizeRange especifica los tamaños máximos y mínimos que deben ser los mensajes entrantes en orden para la condición o la excepción que se debe aplicar.
ms.openlocfilehash: 7711db9ca68f972f080c98197e30c7710620119a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19841009"
---
# <a name="withinsizerange"></a><span data-ttu-id="278d3-103">WithinSizeRange</span><span class="sxs-lookup"><span data-stu-id="278d3-103">WithinSizeRange</span></span>

<span data-ttu-id="278d3-104">El elemento **WithinSizeRange** especifica los tamaños máximos y mínimos que deben ser los mensajes entrantes en orden para la condición o la excepción que se debe aplicar.</span><span class="sxs-lookup"><span data-stu-id="278d3-104">The **WithinSizeRange** element specifies the minimum and maximum sizes that incoming messages must be in order for the condition or exception to apply.</span></span> 
  
```XML
<WithinSizeRange>
     <MinimumSize/>
     <MaximumSize/>
</WithinSizeRange>
```

 <span data-ttu-id="278d3-105">**RulePredicateSizeRangeType**</span><span class="sxs-lookup"><span data-stu-id="278d3-105">**RulePredicateSizeRangeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="278d3-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="278d3-106">Attributes and elements</span></span>

<span data-ttu-id="278d3-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="278d3-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="278d3-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="278d3-108">Attributes</span></span>

<span data-ttu-id="278d3-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="278d3-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="278d3-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="278d3-110">Child elements</span></span>

|<span data-ttu-id="278d3-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="278d3-111">**Element**</span></span>|<span data-ttu-id="278d3-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="278d3-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="278d3-113">MinimumSize</span><span class="sxs-lookup"><span data-stu-id="278d3-113">MinimumSize</span></span>](minimumsize.md) <br/> |<span data-ttu-id="278d3-114">Especifica el tamaño mínimo que un mensaje debe estar en orden para la condición o la excepción que se debe aplicar.</span><span class="sxs-lookup"><span data-stu-id="278d3-114">Specifies the minimum size that a message must be in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="278d3-115">MaximumSize</span><span class="sxs-lookup"><span data-stu-id="278d3-115">MaximumSize</span></span>](maximumsize.md) <br/> |<span data-ttu-id="278d3-116">Especifica el tamaño máximo que un mensaje debe estar en orden para la condición o la excepción que se debe aplicar.</span><span class="sxs-lookup"><span data-stu-id="278d3-116">Specifies the maximum size that a message must be in order for the condition or exception to apply.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="278d3-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="278d3-117">Parent elements</span></span>

|<span data-ttu-id="278d3-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="278d3-118">**Element**</span></span>|<span data-ttu-id="278d3-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="278d3-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="278d3-120">Condiciones</span><span class="sxs-lookup"><span data-stu-id="278d3-120">Conditions</span></span>](conditions.md) <br/> |<span data-ttu-id="278d3-121">Representa las condiciones que, cuando se cumplen los requisitos, se activará las acciones de regla para una regla.</span><span class="sxs-lookup"><span data-stu-id="278d3-121">Represents the conditions that, when fulfilled, will trigger the rule actions for a rule.</span></span>  <br/> |
|[<span data-ttu-id="278d3-122">Excepciones</span><span class="sxs-lookup"><span data-stu-id="278d3-122">Exceptions</span></span>](exceptions.md) <br/> |<span data-ttu-id="278d3-123">Representa todas las condiciones de excepción de regla disponibles para una regla de bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="278d3-123">Represents all the available rule exception conditions for an Inbox rule.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="278d3-124">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="278d3-124">Text value</span></span>

<span data-ttu-id="278d3-125">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="278d3-125">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="278d3-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="278d3-126">Remarks</span></span>

<span data-ttu-id="278d3-127">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="278d3-127">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="278d3-128">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="278d3-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="278d3-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="278d3-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="278d3-130">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="278d3-130">Schema Name</span></span>  <br/> |<span data-ttu-id="278d3-131">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="278d3-131">Messages schema</span></span>  <br/> |
|<span data-ttu-id="278d3-132">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="278d3-132">Validation File</span></span>  <br/> |<span data-ttu-id="278d3-133">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="278d3-133">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="278d3-134">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="278d3-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="278d3-135">Verdadero</span><span class="sxs-lookup"><span data-stu-id="278d3-135">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="278d3-136">Ver también</span><span class="sxs-lookup"><span data-stu-id="278d3-136">See also</span></span>



- [<span data-ttu-id="278d3-137">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="278d3-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

