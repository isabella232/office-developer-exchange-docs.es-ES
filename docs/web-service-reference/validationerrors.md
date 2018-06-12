---
title: ValidationErrors
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ValidationErrors
api_type:
- schema
ms.assetid: 009526aa-22e7-4f5c-be88-079175aa9122
description: El elemento ValidationErrors representa una matriz de errores de validación de la regla en cada campo de regla que tiene un error.
ms.openlocfilehash: c95c8057ad2d16a314d33e3738553b495355fd76
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19840937"
---
# <a name="validationerrors"></a><span data-ttu-id="26cf1-103">ValidationErrors</span><span class="sxs-lookup"><span data-stu-id="26cf1-103">ValidationErrors</span></span>

<span data-ttu-id="26cf1-104">El elemento **ValidationErrors** representa una matriz de errores de validación de la regla en cada campo de regla que tiene un error.</span><span class="sxs-lookup"><span data-stu-id="26cf1-104">The **ValidationErrors** element represents an array of rule validation errors on each rule field that has an error.</span></span> 
  
```XML
<VaidationErrors>
   <Error/>
</ValidationErrors>
```

 <span data-ttu-id="26cf1-105">**ArrayOfRuleValidationErrorsType**</span><span class="sxs-lookup"><span data-stu-id="26cf1-105">**ArrayOfRuleValidationErrorsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="26cf1-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="26cf1-106">Attributes and elements</span></span>

<span data-ttu-id="26cf1-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="26cf1-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="26cf1-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="26cf1-108">Attributes</span></span>

<span data-ttu-id="26cf1-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="26cf1-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="26cf1-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="26cf1-110">Child elements</span></span>

|<span data-ttu-id="26cf1-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="26cf1-111">**Element**</span></span>|<span data-ttu-id="26cf1-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="26cf1-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="26cf1-113">Error</span><span class="sxs-lookup"><span data-stu-id="26cf1-113">Error</span></span>](error.md) <br/> |<span data-ttu-id="26cf1-114">Representa un error de validación único en un valor de la propiedad de regla concreto, valor de la propiedad predicado o valor de la propiedad acción</span><span class="sxs-lookup"><span data-stu-id="26cf1-114">Represents a single validation error on a particular rule property value, predicate property value, or action property value</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="26cf1-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="26cf1-115">Parent elements</span></span>

|<span data-ttu-id="26cf1-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="26cf1-116">**Element**</span></span>|<span data-ttu-id="26cf1-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="26cf1-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="26cf1-118">RuleOperationError</span><span class="sxs-lookup"><span data-stu-id="26cf1-118">RuleOperationError</span></span>](ruleoperationerror.md) <br/> |<span data-ttu-id="26cf1-119">Representa un error de la operación de regla.</span><span class="sxs-lookup"><span data-stu-id="26cf1-119">Represents a rule operation error.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="26cf1-120">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="26cf1-120">Text value</span></span>

<span data-ttu-id="26cf1-121">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="26cf1-121">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="26cf1-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="26cf1-122">Remarks</span></span>

<span data-ttu-id="26cf1-123">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="26cf1-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="26cf1-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="26cf1-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="26cf1-125">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="26cf1-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="26cf1-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="26cf1-126">Schema Name</span></span>  <br/> |<span data-ttu-id="26cf1-127">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="26cf1-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="26cf1-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="26cf1-128">Validation File</span></span>  <br/> |<span data-ttu-id="26cf1-129">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="26cf1-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="26cf1-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="26cf1-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="26cf1-131">Verdadero</span><span class="sxs-lookup"><span data-stu-id="26cf1-131">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="26cf1-132">Ver también</span><span class="sxs-lookup"><span data-stu-id="26cf1-132">See also</span></span>



- [<span data-ttu-id="26cf1-133">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="26cf1-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

