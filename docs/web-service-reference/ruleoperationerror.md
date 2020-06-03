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
description: El elemento RuleOperationError representa un error de operación de regla.
ms.openlocfilehash: b5e0105a1fdb1564b3115a4c3a8411019f725483
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44464962"
---
# <a name="ruleoperationerror"></a><span data-ttu-id="590a2-103">RuleOperationError</span><span class="sxs-lookup"><span data-stu-id="590a2-103">RuleOperationError</span></span>

<span data-ttu-id="590a2-104">El elemento **RuleOperationError** representa un error de operación de regla.</span><span class="sxs-lookup"><span data-stu-id="590a2-104">The **RuleOperationError** element represents a rule operation error.</span></span> 
  
```XML
<RuleOperationError>
    <OperationIndex/>
    <ValidationErrors/>
</RuleOperationError>
```

 <span data-ttu-id="590a2-105">**RuleOperationErrorType**</span><span class="sxs-lookup"><span data-stu-id="590a2-105">**RuleOperationErrorType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="590a2-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="590a2-106">Attributes and elements</span></span>

<span data-ttu-id="590a2-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="590a2-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="590a2-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="590a2-108">Attributes</span></span>

<span data-ttu-id="590a2-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="590a2-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="590a2-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="590a2-110">Child elements</span></span>

|<span data-ttu-id="590a2-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="590a2-111">**Element**</span></span>|<span data-ttu-id="590a2-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="590a2-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="590a2-113">OperationIndex</span><span class="sxs-lookup"><span data-stu-id="590a2-113">OperationIndex</span></span>](operationindex.md) <br/> |<span data-ttu-id="590a2-114">Indica el índice de la operación en la solicitud que causó el error de la operación de la regla.</span><span class="sxs-lookup"><span data-stu-id="590a2-114">Indicates the index of the operation in the request that caused the rule operation error.</span></span>  <br/> |
|[<span data-ttu-id="590a2-115">ValidationErrors</span><span class="sxs-lookup"><span data-stu-id="590a2-115">ValidationErrors</span></span>](validationerrors.md) <br/> |<span data-ttu-id="590a2-116">Representa una matriz de errores de validación de regla en cada campo de regla que tiene un error.</span><span class="sxs-lookup"><span data-stu-id="590a2-116">Represents an array of rule validation errors on each rule field that has an error.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="590a2-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="590a2-117">Parent elements</span></span>

|<span data-ttu-id="590a2-118">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="590a2-118">**Element**</span></span>|<span data-ttu-id="590a2-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="590a2-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="590a2-120">RuleOperationErrors</span><span class="sxs-lookup"><span data-stu-id="590a2-120">RuleOperationErrors</span></span>](ruleoperationerrors.md) <br/> |<span data-ttu-id="590a2-121">Representa una matriz de errores de validación de regla en cada campo de regla que tiene un error.</span><span class="sxs-lookup"><span data-stu-id="590a2-121">Represents an array of rule validation errors on each rule field that has an error.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="590a2-122">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="590a2-122">Text value</span></span>

<span data-ttu-id="590a2-123">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="590a2-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="590a2-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="590a2-124">Remarks</span></span>

<span data-ttu-id="590a2-125">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="590a2-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="590a2-126">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="590a2-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="590a2-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="590a2-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="590a2-128">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="590a2-128">Schema Name</span></span>  <br/> |<span data-ttu-id="590a2-129">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="590a2-129">Messages schema</span></span>  <br/> |
|<span data-ttu-id="590a2-130">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="590a2-130">Validation File</span></span>  <br/> |<span data-ttu-id="590a2-131">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="590a2-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="590a2-132">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="590a2-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="590a2-133">Verdadero</span><span class="sxs-lookup"><span data-stu-id="590a2-133">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="590a2-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="590a2-134">See also</span></span>



- [<span data-ttu-id="590a2-135">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="590a2-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

