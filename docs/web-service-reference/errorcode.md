---
title: ErrorCode
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0bb00cee-c66b-4f34-b99d-355458f5e83b
description: El elemento ErrorCode representa un código de error de validación de regla que describe qué error de validación para cada predicado de la regla o la acción.
ms.openlocfilehash: ed8e2fa72b0eb007925742e6d194f3a391b3f3cb
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764442"
---
# <a name="errorcode"></a><span data-ttu-id="fa8d5-103">ErrorCode</span><span class="sxs-lookup"><span data-stu-id="fa8d5-103">ErrorCode</span></span>

<span data-ttu-id="fa8d5-104">El elemento **ErrorCode** representa un código de error de validación de regla que describe qué error de validación para cada predicado de la regla o la acción.</span><span class="sxs-lookup"><span data-stu-id="fa8d5-104">The **ErrorCode** element represents a rule validation error code that describes what failed validation for each rule predicate or action.</span></span> 
  
```XML
<ErrorCode/>
```

 <span data-ttu-id="fa8d5-105">**RuleValidationErrorCodeType**</span><span class="sxs-lookup"><span data-stu-id="fa8d5-105">**RuleValidationErrorCodeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="fa8d5-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="fa8d5-106">Attributes and elements</span></span>

<span data-ttu-id="fa8d5-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="fa8d5-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fa8d5-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="fa8d5-108">Attributes</span></span>

<span data-ttu-id="fa8d5-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="fa8d5-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="fa8d5-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="fa8d5-110">Child elements</span></span>

<span data-ttu-id="fa8d5-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="fa8d5-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="fa8d5-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="fa8d5-112">Parent elements</span></span>

|<span data-ttu-id="fa8d5-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="fa8d5-113">**Element**</span></span>|<span data-ttu-id="fa8d5-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="fa8d5-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fa8d5-115">Error</span><span class="sxs-lookup"><span data-stu-id="fa8d5-115">Error</span></span>](error.md) <br/> |<span data-ttu-id="fa8d5-116">Representa un error de validación único en un valor de la propiedad de regla concreto, valor de la propiedad predicado o valor de la propiedad acción.</span><span class="sxs-lookup"><span data-stu-id="fa8d5-116">Represents a single validation error on a particular rule property value, predicate property value, or action property value.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="fa8d5-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="fa8d5-117">Text value</span></span>

<span data-ttu-id="fa8d5-118">El valor de texto para este elemento está restringido a una de las siguientes cadenas:</span><span class="sxs-lookup"><span data-stu-id="fa8d5-118">The text value for this element is restricted to one of the following strings:</span></span>
  
- <span data-ttu-id="fa8d5-119">ADOperationFailure</span><span class="sxs-lookup"><span data-stu-id="fa8d5-119">ADOperationFailure</span></span>
    
- <span data-ttu-id="fa8d5-120">ConnectedAccountNotFound</span><span class="sxs-lookup"><span data-stu-id="fa8d5-120">ConnectedAccountNotFound</span></span>
    
- <span data-ttu-id="fa8d5-121">CreateWithRuleId</span><span class="sxs-lookup"><span data-stu-id="fa8d5-121">CreateWithRuleId</span></span>
    
- <span data-ttu-id="fa8d5-122">EmptyValueFound</span><span class="sxs-lookup"><span data-stu-id="fa8d5-122">EmptyValueFound</span></span>
    
- <span data-ttu-id="fa8d5-123">DuplicatedPriority</span><span class="sxs-lookup"><span data-stu-id="fa8d5-123">DuplicatedPriority</span></span>
    
- <span data-ttu-id="fa8d5-124">DuplicatedOperationOnTheSameRule</span><span class="sxs-lookup"><span data-stu-id="fa8d5-124">DuplicatedOperationOnTheSameRule</span></span>
    
- <span data-ttu-id="fa8d5-125">FolderDoesNotExist</span><span class="sxs-lookup"><span data-stu-id="fa8d5-125">FolderDoesNotExist</span></span>
    
- <span data-ttu-id="fa8d5-126">InvalidAddress</span><span class="sxs-lookup"><span data-stu-id="fa8d5-126">InvalidAddress</span></span>
    
- <span data-ttu-id="fa8d5-127">InvalidDateRange</span><span class="sxs-lookup"><span data-stu-id="fa8d5-127">InvalidDateRange</span></span>
    
- <span data-ttu-id="fa8d5-128">InvalidFolderId</span><span class="sxs-lookup"><span data-stu-id="fa8d5-128">InvalidFolderId</span></span>
    
- <span data-ttu-id="fa8d5-129">InvalidSizeRange</span><span class="sxs-lookup"><span data-stu-id="fa8d5-129">InvalidSizeRange</span></span>
    
- <span data-ttu-id="fa8d5-130">InvalidValue</span><span class="sxs-lookup"><span data-stu-id="fa8d5-130">InvalidValue</span></span>
    
- <span data-ttu-id="fa8d5-131">MessageClassificationNotFound</span><span class="sxs-lookup"><span data-stu-id="fa8d5-131">MessageClassificationNotFound</span></span>
    
- <span data-ttu-id="fa8d5-132">MissingAction</span><span class="sxs-lookup"><span data-stu-id="fa8d5-132">MissingAction</span></span>
    
- <span data-ttu-id="fa8d5-133">MissingParameter</span><span class="sxs-lookup"><span data-stu-id="fa8d5-133">MissingParameter</span></span>
    
- <span data-ttu-id="fa8d5-134">MissingRangeValue</span><span class="sxs-lookup"><span data-stu-id="fa8d5-134">MissingRangeValue</span></span>
    
- <span data-ttu-id="fa8d5-135">NotSettable</span><span class="sxs-lookup"><span data-stu-id="fa8d5-135">NotSettable</span></span>
    
- <span data-ttu-id="fa8d5-136">RecipientDoesNotExist</span><span class="sxs-lookup"><span data-stu-id="fa8d5-136">RecipientDoesNotExist</span></span>
    
- <span data-ttu-id="fa8d5-137">RuleNotFound</span><span class="sxs-lookup"><span data-stu-id="fa8d5-137">RuleNotFound</span></span>
    
- <span data-ttu-id="fa8d5-138">SizeLessThanZero</span><span class="sxs-lookup"><span data-stu-id="fa8d5-138">SizeLessThanZero</span></span>
    
- <span data-ttu-id="fa8d5-139">StringValueTooBig</span><span class="sxs-lookup"><span data-stu-id="fa8d5-139">StringValueTooBig</span></span>
    
- <span data-ttu-id="fa8d5-140">UnsupportedAddress</span><span class="sxs-lookup"><span data-stu-id="fa8d5-140">UnsupportedAddress</span></span>
    
- <span data-ttu-id="fa8d5-141">UnexpectedError</span><span class="sxs-lookup"><span data-stu-id="fa8d5-141">UnexpectedError</span></span>
    
- <span data-ttu-id="fa8d5-142">UnsupportedRule</span><span class="sxs-lookup"><span data-stu-id="fa8d5-142">UnsupportedRule</span></span>
    
## <a name="remarks"></a><span data-ttu-id="fa8d5-143">Comentarios</span><span class="sxs-lookup"><span data-stu-id="fa8d5-143">Remarks</span></span>

<span data-ttu-id="fa8d5-144">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="fa8d5-144">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fa8d5-145">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="fa8d5-145">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fa8d5-146">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="fa8d5-146">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="fa8d5-147">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="fa8d5-147">Schema Name</span></span>  <br/> |<span data-ttu-id="fa8d5-148">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="fa8d5-148">Messages schema</span></span>  <br/> |
|<span data-ttu-id="fa8d5-149">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="fa8d5-149">Validation File</span></span>  <br/> |<span data-ttu-id="fa8d5-150">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="fa8d5-150">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="fa8d5-151">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="fa8d5-151">Can be Empty</span></span>  <br/> |<span data-ttu-id="fa8d5-152">False</span><span class="sxs-lookup"><span data-stu-id="fa8d5-152">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fa8d5-153">Vea también</span><span class="sxs-lookup"><span data-stu-id="fa8d5-153">See also</span></span>



- [<span data-ttu-id="fa8d5-154">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="fa8d5-154">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

