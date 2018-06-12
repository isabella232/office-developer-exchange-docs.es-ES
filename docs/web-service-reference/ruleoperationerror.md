---
title: RuleOperationError
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RuleOperationError
api_type:
- schema
ms.assetid: b447e610-d37c-40d3-9158-aa108a9f248e
description: El elemento RuleOperationError representa un error de la operación de regla.
ms.openlocfilehash: ff42addea0f55b13794e2c910d4d865ad0b17bc3
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19837265"
---
# <a name="ruleoperationerror"></a><span data-ttu-id="e609d-103">RuleOperationError</span><span class="sxs-lookup"><span data-stu-id="e609d-103">RuleOperationError</span></span>

<span data-ttu-id="e609d-104">El elemento **RuleOperationError** representa un error de la operación de regla.</span><span class="sxs-lookup"><span data-stu-id="e609d-104">The **RuleOperationError** element represents a rule operation error.</span></span> 
  
```XML
<RuleOperationError>
    <OperationIndex/>
    <ValidationErrors/>
</RuleOperationError>
```

 <span data-ttu-id="e609d-105">**RuleOperationErrorType**</span><span class="sxs-lookup"><span data-stu-id="e609d-105">**RuleOperationErrorType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e609d-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="e609d-106">Attributes and elements</span></span>

<span data-ttu-id="e609d-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="e609d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e609d-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="e609d-108">Attributes</span></span>

<span data-ttu-id="e609d-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="e609d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e609d-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="e609d-110">Child elements</span></span>

|<span data-ttu-id="e609d-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="e609d-111">**Element**</span></span>|<span data-ttu-id="e609d-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e609d-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e609d-113">OperationIndex</span><span class="sxs-lookup"><span data-stu-id="e609d-113">OperationIndex</span></span>](operationindex.md) <br/> |<span data-ttu-id="e609d-114">Indica el índice de la operación en la solicitud que provocó el error de la operación de regla.</span><span class="sxs-lookup"><span data-stu-id="e609d-114">Indicates the index of the operation in the request that caused the rule operation error.</span></span>  <br/> |
|[<span data-ttu-id="e609d-115">ValidationErrors</span><span class="sxs-lookup"><span data-stu-id="e609d-115">ValidationErrors</span></span>](validationerrors.md) <br/> |<span data-ttu-id="e609d-116">Representa una matriz de errores de validación de la regla en cada campo de regla que tiene un error.</span><span class="sxs-lookup"><span data-stu-id="e609d-116">Represents an array of rule validation errors on each rule field that has an error.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="e609d-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="e609d-117">Parent elements</span></span>

|<span data-ttu-id="e609d-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="e609d-118">**Element**</span></span>|<span data-ttu-id="e609d-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e609d-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e609d-120">RuleOperationErrors</span><span class="sxs-lookup"><span data-stu-id="e609d-120">RuleOperationErrors</span></span>](ruleoperationerrors.md) <br/> |<span data-ttu-id="e609d-121">Representa una matriz de errores de validación de la regla en cada campo de regla que tiene un error.</span><span class="sxs-lookup"><span data-stu-id="e609d-121">Represents an array of rule validation errors on each rule field that has an error.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="e609d-122">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="e609d-122">Text value</span></span>

<span data-ttu-id="e609d-123">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="e609d-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e609d-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e609d-124">Remarks</span></span>

<span data-ttu-id="e609d-125">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="e609d-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e609d-126">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="e609d-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e609d-127">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e609d-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="e609d-128">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="e609d-128">Schema Name</span></span>  <br/> |<span data-ttu-id="e609d-129">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="e609d-129">Messages schema</span></span>  <br/> |
|<span data-ttu-id="e609d-130">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="e609d-130">Validation File</span></span>  <br/> |<span data-ttu-id="e609d-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="e609d-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="e609d-132">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="e609d-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="e609d-133">Verdadero</span><span class="sxs-lookup"><span data-stu-id="e609d-133">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e609d-134">Ver también</span><span class="sxs-lookup"><span data-stu-id="e609d-134">See also</span></span>



- [<span data-ttu-id="e609d-135">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="e609d-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

