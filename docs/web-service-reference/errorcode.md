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
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764442"
---
# <a name="errorcode"></a><span data-ttu-id="9096a-103">ErrorCode</span><span class="sxs-lookup"><span data-stu-id="9096a-103">ErrorCode</span></span>

<span data-ttu-id="9096a-104">El elemento **ErrorCode** representa un código de error de validación de regla que describe qué error de validación para cada predicado de la regla o la acción.</span><span class="sxs-lookup"><span data-stu-id="9096a-104">The **ErrorCode** element represents a rule validation error code that describes what failed validation for each rule predicate or action.</span></span> 
  
```XML
<ErrorCode/>
```

 <span data-ttu-id="9096a-105">**RuleValidationErrorCodeType**</span><span class="sxs-lookup"><span data-stu-id="9096a-105">**RuleValidationErrorCodeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9096a-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="9096a-106">Attributes and elements</span></span>

<span data-ttu-id="9096a-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="9096a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9096a-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="9096a-108">Attributes</span></span>

<span data-ttu-id="9096a-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="9096a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="9096a-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="9096a-110">Child elements</span></span>

<span data-ttu-id="9096a-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="9096a-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="9096a-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="9096a-112">Parent elements</span></span>

|<span data-ttu-id="9096a-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="9096a-113">**Element**</span></span>|<span data-ttu-id="9096a-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9096a-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9096a-115">Error</span><span class="sxs-lookup"><span data-stu-id="9096a-115">Error</span></span>](error.md) <br/> |<span data-ttu-id="9096a-116">Representa un error de validación único en un valor de la propiedad de regla concreto, valor de la propiedad predicado o valor de la propiedad acción.</span><span class="sxs-lookup"><span data-stu-id="9096a-116">Represents a single validation error on a particular rule property value, predicate property value, or action property value.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="9096a-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="9096a-117">Text value</span></span>

<span data-ttu-id="9096a-118">El valor de texto para este elemento está restringido a una de las siguientes cadenas:</span><span class="sxs-lookup"><span data-stu-id="9096a-118">The text value for this element is restricted to one of the following strings:</span></span>
  
- <span data-ttu-id="9096a-119">ADOperationFailure</span><span class="sxs-lookup"><span data-stu-id="9096a-119">ADOperationFailure</span></span>
    
- <span data-ttu-id="9096a-120">ConnectedAccountNotFound</span><span class="sxs-lookup"><span data-stu-id="9096a-120">ConnectedAccountNotFound</span></span>
    
- <span data-ttu-id="9096a-121">CreateWithRuleId</span><span class="sxs-lookup"><span data-stu-id="9096a-121">CreateWithRuleId</span></span>
    
- <span data-ttu-id="9096a-122">EmptyValueFound</span><span class="sxs-lookup"><span data-stu-id="9096a-122">EmptyValueFound</span></span>
    
- <span data-ttu-id="9096a-123">DuplicatedPriority</span><span class="sxs-lookup"><span data-stu-id="9096a-123">DuplicatedPriority</span></span>
    
- <span data-ttu-id="9096a-124">DuplicatedOperationOnTheSameRule</span><span class="sxs-lookup"><span data-stu-id="9096a-124">DuplicatedOperationOnTheSameRule</span></span>
    
- <span data-ttu-id="9096a-125">FolderDoesNotExist</span><span class="sxs-lookup"><span data-stu-id="9096a-125">FolderDoesNotExist</span></span>
    
- <span data-ttu-id="9096a-126">InvalidAddress</span><span class="sxs-lookup"><span data-stu-id="9096a-126">InvalidAddress</span></span>
    
- <span data-ttu-id="9096a-127">InvalidDateRange</span><span class="sxs-lookup"><span data-stu-id="9096a-127">InvalidDateRange</span></span>
    
- <span data-ttu-id="9096a-128">InvalidFolderId</span><span class="sxs-lookup"><span data-stu-id="9096a-128">InvalidFolderId</span></span>
    
- <span data-ttu-id="9096a-129">InvalidSizeRange</span><span class="sxs-lookup"><span data-stu-id="9096a-129">InvalidSizeRange</span></span>
    
- <span data-ttu-id="9096a-130">InvalidValue</span><span class="sxs-lookup"><span data-stu-id="9096a-130">InvalidValue</span></span>
    
- <span data-ttu-id="9096a-131">MessageClassificationNotFound</span><span class="sxs-lookup"><span data-stu-id="9096a-131">MessageClassificationNotFound</span></span>
    
- <span data-ttu-id="9096a-132">MissingAction</span><span class="sxs-lookup"><span data-stu-id="9096a-132">MissingAction</span></span>
    
- <span data-ttu-id="9096a-133">MissingParameter</span><span class="sxs-lookup"><span data-stu-id="9096a-133">MissingParameter</span></span>
    
- <span data-ttu-id="9096a-134">MissingRangeValue</span><span class="sxs-lookup"><span data-stu-id="9096a-134">MissingRangeValue</span></span>
    
- <span data-ttu-id="9096a-135">NotSettable</span><span class="sxs-lookup"><span data-stu-id="9096a-135">NotSettable</span></span>
    
- <span data-ttu-id="9096a-136">RecipientDoesNotExist</span><span class="sxs-lookup"><span data-stu-id="9096a-136">RecipientDoesNotExist</span></span>
    
- <span data-ttu-id="9096a-137">RuleNotFound</span><span class="sxs-lookup"><span data-stu-id="9096a-137">RuleNotFound</span></span>
    
- <span data-ttu-id="9096a-138">SizeLessThanZero</span><span class="sxs-lookup"><span data-stu-id="9096a-138">SizeLessThanZero</span></span>
    
- <span data-ttu-id="9096a-139">StringValueTooBig</span><span class="sxs-lookup"><span data-stu-id="9096a-139">StringValueTooBig</span></span>
    
- <span data-ttu-id="9096a-140">UnsupportedAddress</span><span class="sxs-lookup"><span data-stu-id="9096a-140">UnsupportedAddress</span></span>
    
- <span data-ttu-id="9096a-141">UnexpectedError</span><span class="sxs-lookup"><span data-stu-id="9096a-141">UnexpectedError</span></span>
    
- <span data-ttu-id="9096a-142">UnsupportedRule</span><span class="sxs-lookup"><span data-stu-id="9096a-142">UnsupportedRule</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9096a-143">Notas</span><span class="sxs-lookup"><span data-stu-id="9096a-143">Remarks</span></span>

<span data-ttu-id="9096a-144">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="9096a-144">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9096a-145">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="9096a-145">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9096a-146">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="9096a-146">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="9096a-147">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="9096a-147">Schema Name</span></span>  <br/> |<span data-ttu-id="9096a-148">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="9096a-148">Messages schema</span></span>  <br/> |
|<span data-ttu-id="9096a-149">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="9096a-149">Validation File</span></span>  <br/> |<span data-ttu-id="9096a-150">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="9096a-150">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="9096a-151">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="9096a-151">Can be Empty</span></span>  <br/> |<span data-ttu-id="9096a-152">False</span><span class="sxs-lookup"><span data-stu-id="9096a-152">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9096a-153">Ver también</span><span class="sxs-lookup"><span data-stu-id="9096a-153">See also</span></span>



- [<span data-ttu-id="9096a-154">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="9096a-154">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

