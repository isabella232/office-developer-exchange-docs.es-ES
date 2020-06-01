---
title: ErrorCode
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0bb00cee-c66b-4f34-b99d-355458f5e83b
description: El elemento ErrorCode representa un código de error de validación de regla que describe qué error de validación para cada acción o predicado de regla.
ms.openlocfilehash: 6432aeee786d74a9afcb346cb66765f9001257de
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460081"
---
# <a name="errorcode"></a><span data-ttu-id="dceab-103">ErrorCode</span><span class="sxs-lookup"><span data-stu-id="dceab-103">ErrorCode</span></span>

<span data-ttu-id="dceab-104">El elemento **ErrorCode** representa un código de error de validación de regla que describe qué error de validación para cada acción o predicado de regla.</span><span class="sxs-lookup"><span data-stu-id="dceab-104">The **ErrorCode** element represents a rule validation error code that describes what failed validation for each rule predicate or action.</span></span> 
  
```XML
<ErrorCode/>
```

 <span data-ttu-id="dceab-105">**RuleValidationErrorCodeType**</span><span class="sxs-lookup"><span data-stu-id="dceab-105">**RuleValidationErrorCodeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="dceab-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="dceab-106">Attributes and elements</span></span>

<span data-ttu-id="dceab-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="dceab-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="dceab-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="dceab-108">Attributes</span></span>

<span data-ttu-id="dceab-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="dceab-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="dceab-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="dceab-110">Child elements</span></span>

<span data-ttu-id="dceab-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="dceab-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="dceab-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="dceab-112">Parent elements</span></span>

|<span data-ttu-id="dceab-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="dceab-113">**Element**</span></span>|<span data-ttu-id="dceab-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="dceab-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="dceab-115">Error</span><span class="sxs-lookup"><span data-stu-id="dceab-115">Error</span></span>](error.md) <br/> |<span data-ttu-id="dceab-116">Representa un error de validación único en un valor de propiedad de regla, un valor de propiedad de predicado o un valor de propiedad de acción específicos.</span><span class="sxs-lookup"><span data-stu-id="dceab-116">Represents a single validation error on a particular rule property value, predicate property value, or action property value.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="dceab-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="dceab-117">Text value</span></span>

<span data-ttu-id="dceab-118">El valor de texto de este elemento está restringido a una de las siguientes cadenas:</span><span class="sxs-lookup"><span data-stu-id="dceab-118">The text value for this element is restricted to one of the following strings:</span></span>
  
- <span data-ttu-id="dceab-119">ADOperationFailure</span><span class="sxs-lookup"><span data-stu-id="dceab-119">ADOperationFailure</span></span>
    
- <span data-ttu-id="dceab-120">ConnectedAccountNotFound</span><span class="sxs-lookup"><span data-stu-id="dceab-120">ConnectedAccountNotFound</span></span>
    
- <span data-ttu-id="dceab-121">CreateWithRuleId</span><span class="sxs-lookup"><span data-stu-id="dceab-121">CreateWithRuleId</span></span>
    
- <span data-ttu-id="dceab-122">EmptyValueFound</span><span class="sxs-lookup"><span data-stu-id="dceab-122">EmptyValueFound</span></span>
    
- <span data-ttu-id="dceab-123">DuplicatedPriority</span><span class="sxs-lookup"><span data-stu-id="dceab-123">DuplicatedPriority</span></span>
    
- <span data-ttu-id="dceab-124">DuplicatedOperationOnTheSameRule</span><span class="sxs-lookup"><span data-stu-id="dceab-124">DuplicatedOperationOnTheSameRule</span></span>
    
- <span data-ttu-id="dceab-125">FolderDoesNotExist</span><span class="sxs-lookup"><span data-stu-id="dceab-125">FolderDoesNotExist</span></span>
    
- <span data-ttu-id="dceab-126">InvalidAddress</span><span class="sxs-lookup"><span data-stu-id="dceab-126">InvalidAddress</span></span>
    
- <span data-ttu-id="dceab-127">InvalidDateRange</span><span class="sxs-lookup"><span data-stu-id="dceab-127">InvalidDateRange</span></span>
    
- <span data-ttu-id="dceab-128">InvalidFolderId</span><span class="sxs-lookup"><span data-stu-id="dceab-128">InvalidFolderId</span></span>
    
- <span data-ttu-id="dceab-129">InvalidSizeRange</span><span class="sxs-lookup"><span data-stu-id="dceab-129">InvalidSizeRange</span></span>
    
- <span data-ttu-id="dceab-130">InvalidValue</span><span class="sxs-lookup"><span data-stu-id="dceab-130">InvalidValue</span></span>
    
- <span data-ttu-id="dceab-131">MessageClassificationNotFound</span><span class="sxs-lookup"><span data-stu-id="dceab-131">MessageClassificationNotFound</span></span>
    
- <span data-ttu-id="dceab-132">MissingAction</span><span class="sxs-lookup"><span data-stu-id="dceab-132">MissingAction</span></span>
    
- <span data-ttu-id="dceab-133">MissingParameter</span><span class="sxs-lookup"><span data-stu-id="dceab-133">MissingParameter</span></span>
    
- <span data-ttu-id="dceab-134">MissingRangeValue</span><span class="sxs-lookup"><span data-stu-id="dceab-134">MissingRangeValue</span></span>
    
- <span data-ttu-id="dceab-135">NotSettable</span><span class="sxs-lookup"><span data-stu-id="dceab-135">NotSettable</span></span>
    
- <span data-ttu-id="dceab-136">RecipientDoesNotExist</span><span class="sxs-lookup"><span data-stu-id="dceab-136">RecipientDoesNotExist</span></span>
    
- <span data-ttu-id="dceab-137">RuleNotFound</span><span class="sxs-lookup"><span data-stu-id="dceab-137">RuleNotFound</span></span>
    
- <span data-ttu-id="dceab-138">SizeLessThanZero</span><span class="sxs-lookup"><span data-stu-id="dceab-138">SizeLessThanZero</span></span>
    
- <span data-ttu-id="dceab-139">StringValueTooBig</span><span class="sxs-lookup"><span data-stu-id="dceab-139">StringValueTooBig</span></span>
    
- <span data-ttu-id="dceab-140">UnsupportedAddress</span><span class="sxs-lookup"><span data-stu-id="dceab-140">UnsupportedAddress</span></span>
    
- <span data-ttu-id="dceab-141">UnexpectedError</span><span class="sxs-lookup"><span data-stu-id="dceab-141">UnexpectedError</span></span>
    
- <span data-ttu-id="dceab-142">UnsupportedRule</span><span class="sxs-lookup"><span data-stu-id="dceab-142">UnsupportedRule</span></span>
    
## <a name="remarks"></a><span data-ttu-id="dceab-143">Comentarios</span><span class="sxs-lookup"><span data-stu-id="dceab-143">Remarks</span></span>

<span data-ttu-id="dceab-144">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="dceab-144">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="dceab-145">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="dceab-145">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="dceab-146">Namespace</span><span class="sxs-lookup"><span data-stu-id="dceab-146">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="dceab-147">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="dceab-147">Schema Name</span></span>  <br/> |<span data-ttu-id="dceab-148">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="dceab-148">Messages schema</span></span>  <br/> |
|<span data-ttu-id="dceab-149">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="dceab-149">Validation File</span></span>  <br/> |<span data-ttu-id="dceab-150">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="dceab-150">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="dceab-151">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="dceab-151">Can be Empty</span></span>  <br/> |<span data-ttu-id="dceab-152">Falso</span><span class="sxs-lookup"><span data-stu-id="dceab-152">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="dceab-153">Vea también</span><span class="sxs-lookup"><span data-stu-id="dceab-153">See also</span></span>



- [<span data-ttu-id="dceab-154">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="dceab-154">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

