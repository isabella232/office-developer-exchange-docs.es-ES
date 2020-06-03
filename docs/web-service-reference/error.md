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
description: El elemento error representa un error de validación único en un valor de propiedad de regla, un valor de propiedad de predicado o un valor de propiedad de acción específicos.
ms.openlocfilehash: 9c28f63aa79446d89152868c81c85ffa7b3a8b39
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44460683"
---
# <a name="error"></a><span data-ttu-id="e49ad-103">Error</span><span class="sxs-lookup"><span data-stu-id="e49ad-103">Error</span></span>

<span data-ttu-id="e49ad-104">El elemento **error** representa un error de validación único en un valor de propiedad de regla, un valor de propiedad de predicado o un valor de propiedad de acción específicos.</span><span class="sxs-lookup"><span data-stu-id="e49ad-104">The **Error** element represents a single validation error on a particular rule property value, predicate property value, or action property value.</span></span> 
  
```XML
<Error>
   <FieldUri/>
   <ErrorCode/>
   <ErrorMessage/>
   <FieldValue/>
</Error>
```

 <span data-ttu-id="e49ad-105">**RuleValidationErrorType**</span><span class="sxs-lookup"><span data-stu-id="e49ad-105">**RuleValidationErrorType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e49ad-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="e49ad-106">Attributes and elements</span></span>

<span data-ttu-id="e49ad-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="e49ad-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e49ad-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="e49ad-108">Attributes</span></span>

<span data-ttu-id="e49ad-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="e49ad-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e49ad-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="e49ad-110">Child elements</span></span>

|<span data-ttu-id="e49ad-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="e49ad-111">**Element**</span></span>|<span data-ttu-id="e49ad-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e49ad-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e49ad-113">FieldUri (regla)</span><span class="sxs-lookup"><span data-stu-id="e49ad-113">FieldUri (Rule)</span></span>](fielduri-rule.md) <br/> |<span data-ttu-id="e49ad-114">Especifica el URI al campo de regla que causó el error de validación.</span><span class="sxs-lookup"><span data-stu-id="e49ad-114">Specifies the URI to the rule field that caused the validation error.</span></span>  <br/> |
|[<span data-ttu-id="e49ad-115">ErrorCode</span><span class="sxs-lookup"><span data-stu-id="e49ad-115">ErrorCode</span></span>](errorcode.md) <br/> |<span data-ttu-id="e49ad-116">Representa un código de error de validación de regla que describe qué validación con error para cada acción o predicado de regla.</span><span class="sxs-lookup"><span data-stu-id="e49ad-116">Represents a rule validation error code that describes what failed validation for each rule predicate or action.</span></span>  <br/> |
|[<span data-ttu-id="e49ad-117">ErrorMessage</span><span class="sxs-lookup"><span data-stu-id="e49ad-117">ErrorMessage</span></span>](errormessage.md) <br/> |<span data-ttu-id="e49ad-118">Representa el motivo del error de validación.</span><span class="sxs-lookup"><span data-stu-id="e49ad-118">Represents the reason for the validation error.</span></span>  <br/> |
|[<span data-ttu-id="e49ad-119">FieldValue</span><span class="sxs-lookup"><span data-stu-id="e49ad-119">FieldValue</span></span>](fieldvalue.md) <br/> |<span data-ttu-id="e49ad-120">Representa el valor del campo que causó el error de validación.</span><span class="sxs-lookup"><span data-stu-id="e49ad-120">Represents the value of the field that caused the validation error.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="e49ad-121">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="e49ad-121">Parent elements</span></span>

|<span data-ttu-id="e49ad-122">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="e49ad-122">**Element**</span></span>|<span data-ttu-id="e49ad-123">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e49ad-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e49ad-124">ValidationErrors</span><span class="sxs-lookup"><span data-stu-id="e49ad-124">ValidationErrors</span></span>](validationerrors.md) <br/> |<span data-ttu-id="e49ad-125">Representa una matriz de errores de validación de regla en cada campo de regla que tiene un error.</span><span class="sxs-lookup"><span data-stu-id="e49ad-125">Represents an array of rule validation errors on each rule field that has an error.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="e49ad-126">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="e49ad-126">Text value</span></span>

<span data-ttu-id="e49ad-127">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="e49ad-127">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e49ad-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e49ad-128">Remarks</span></span>

<span data-ttu-id="e49ad-129">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="e49ad-129">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e49ad-130">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="e49ad-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e49ad-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="e49ad-131">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="e49ad-132">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="e49ad-132">Schema Name</span></span>  <br/> |<span data-ttu-id="e49ad-133">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="e49ad-133">Messages schema</span></span>  <br/> |
|<span data-ttu-id="e49ad-134">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="e49ad-134">Validation File</span></span>  <br/> |<span data-ttu-id="e49ad-135">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="e49ad-135">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="e49ad-136">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="e49ad-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="e49ad-137">Verdadero</span><span class="sxs-lookup"><span data-stu-id="e49ad-137">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e49ad-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="e49ad-138">See also</span></span>



- [<span data-ttu-id="e49ad-139">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="e49ad-139">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

