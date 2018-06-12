---
title: Error
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Error
api_type:
- schema
ms.assetid: b1f54673-578a-496b-99f5-0fde2c669278
description: El elemento Error representa un error de validación único en un valor de la propiedad de regla concreto, valor de la propiedad predicado o valor de la propiedad acción.
ms.openlocfilehash: adb2de56b7610aa92b5bf5b8d43ac22f35021b64
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764437"
---
# <a name="error"></a><span data-ttu-id="b8f82-103">Error</span><span class="sxs-lookup"><span data-stu-id="b8f82-103">Error</span></span>

<span data-ttu-id="b8f82-104">El elemento **Error** representa un error de validación único en un valor de la propiedad de regla concreto, valor de la propiedad predicado o valor de la propiedad acción.</span><span class="sxs-lookup"><span data-stu-id="b8f82-104">The **Error** element represents a single validation error on a particular rule property value, predicate property value, or action property value.</span></span> 
  
```XML
<Error>
   <FieldUri/>
   <ErrorCode/>
   <ErrorMessage/>
   <FieldValue/>
</Error>
```

 <span data-ttu-id="b8f82-105">**RuleValidationErrorType**</span><span class="sxs-lookup"><span data-stu-id="b8f82-105">**RuleValidationErrorType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b8f82-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="b8f82-106">Attributes and elements</span></span>

<span data-ttu-id="b8f82-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="b8f82-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b8f82-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="b8f82-108">Attributes</span></span>

<span data-ttu-id="b8f82-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="b8f82-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b8f82-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b8f82-110">Child elements</span></span>

|<span data-ttu-id="b8f82-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="b8f82-111">**Element**</span></span>|<span data-ttu-id="b8f82-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b8f82-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b8f82-113">FieldUri (regla)</span><span class="sxs-lookup"><span data-stu-id="b8f82-113">FieldUri (Rule)</span></span>](fielduri-rule.md) <br/> |<span data-ttu-id="b8f82-114">Especifica el URI para el campo de regla que causó el error de validación.</span><span class="sxs-lookup"><span data-stu-id="b8f82-114">Specifies the URI to the rule field that caused the validation error.</span></span>  <br/> |
|[<span data-ttu-id="b8f82-115">ErrorCode</span><span class="sxs-lookup"><span data-stu-id="b8f82-115">ErrorCode</span></span>](errorcode.md) <br/> |<span data-ttu-id="b8f82-116">Representa un código de error de validación de regla que describe qué error de validación para cada predicado de la regla o la acción.</span><span class="sxs-lookup"><span data-stu-id="b8f82-116">Represents a rule validation error code that describes what failed validation for each rule predicate or action.</span></span>  <br/> |
|[<span data-ttu-id="b8f82-117">ErrorMessage</span><span class="sxs-lookup"><span data-stu-id="b8f82-117">ErrorMessage</span></span>](errormessage.md) <br/> |<span data-ttu-id="b8f82-118">Representa el motivo del error de validación.</span><span class="sxs-lookup"><span data-stu-id="b8f82-118">Represents the reason for the validation error.</span></span>  <br/> |
|[<span data-ttu-id="b8f82-119">FieldValue</span><span class="sxs-lookup"><span data-stu-id="b8f82-119">FieldValue</span></span>](fieldvalue.md) <br/> |<span data-ttu-id="b8f82-120">Representa el valor del campo que causó el error de validación.</span><span class="sxs-lookup"><span data-stu-id="b8f82-120">Represents the value of the field that caused the validation error.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="b8f82-121">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="b8f82-121">Parent elements</span></span>

|<span data-ttu-id="b8f82-122">**Element**</span><span class="sxs-lookup"><span data-stu-id="b8f82-122">**Element**</span></span>|<span data-ttu-id="b8f82-123">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b8f82-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b8f82-124">ValidationErrors</span><span class="sxs-lookup"><span data-stu-id="b8f82-124">ValidationErrors</span></span>](validationerrors.md) <br/> |<span data-ttu-id="b8f82-125">Representa una matriz de errores de validación de la regla en cada campo de regla que tiene un error.</span><span class="sxs-lookup"><span data-stu-id="b8f82-125">Represents an array of rule validation errors on each rule field that has an error.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="b8f82-126">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="b8f82-126">Text value</span></span>

<span data-ttu-id="b8f82-127">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="b8f82-127">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b8f82-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b8f82-128">Remarks</span></span>

<span data-ttu-id="b8f82-129">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="b8f82-129">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b8f82-130">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="b8f82-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b8f82-131">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b8f82-131">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="b8f82-132">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="b8f82-132">Schema Name</span></span>  <br/> |<span data-ttu-id="b8f82-133">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="b8f82-133">Messages schema</span></span>  <br/> |
|<span data-ttu-id="b8f82-134">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="b8f82-134">Validation File</span></span>  <br/> |<span data-ttu-id="b8f82-135">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="b8f82-135">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="b8f82-136">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="b8f82-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="b8f82-137">Verdadero</span><span class="sxs-lookup"><span data-stu-id="b8f82-137">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b8f82-138">Ver también</span><span class="sxs-lookup"><span data-stu-id="b8f82-138">See also</span></span>



- [<span data-ttu-id="b8f82-139">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="b8f82-139">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

