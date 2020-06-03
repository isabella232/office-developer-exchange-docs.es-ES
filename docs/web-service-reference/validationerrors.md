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
description: El elemento ValidationErrors representa una matriz de errores de validación de regla en cada campo de regla que tiene un error.
ms.openlocfilehash: 0861425b04e03a3e2e54a47a5027d0a11264392d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530278"
---
# <a name="validationerrors"></a><span data-ttu-id="2e12c-103">ValidationErrors</span><span class="sxs-lookup"><span data-stu-id="2e12c-103">ValidationErrors</span></span>

<span data-ttu-id="2e12c-104">El elemento **ValidationErrors** representa una matriz de errores de validación de regla en cada campo de regla que tiene un error.</span><span class="sxs-lookup"><span data-stu-id="2e12c-104">The **ValidationErrors** element represents an array of rule validation errors on each rule field that has an error.</span></span> 
  
```XML
<VaidationErrors>
   <Error/>
</ValidationErrors>
```

 <span data-ttu-id="2e12c-105">**ArrayOfRuleValidationErrorsType**</span><span class="sxs-lookup"><span data-stu-id="2e12c-105">**ArrayOfRuleValidationErrorsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2e12c-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="2e12c-106">Attributes and elements</span></span>

<span data-ttu-id="2e12c-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="2e12c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2e12c-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="2e12c-108">Attributes</span></span>

<span data-ttu-id="2e12c-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="2e12c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2e12c-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="2e12c-110">Child elements</span></span>

|<span data-ttu-id="2e12c-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="2e12c-111">**Element**</span></span>|<span data-ttu-id="2e12c-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2e12c-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2e12c-113">Error</span><span class="sxs-lookup"><span data-stu-id="2e12c-113">Error</span></span>](error.md) <br/> |<span data-ttu-id="2e12c-114">Representa un error de validación único en un valor de propiedad de regla, un valor de propiedad de predicado o un valor de propiedad de acción específicos.</span><span class="sxs-lookup"><span data-stu-id="2e12c-114">Represents a single validation error on a particular rule property value, predicate property value, or action property value</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="2e12c-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="2e12c-115">Parent elements</span></span>

|<span data-ttu-id="2e12c-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="2e12c-116">**Element**</span></span>|<span data-ttu-id="2e12c-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2e12c-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2e12c-118">RuleOperationError</span><span class="sxs-lookup"><span data-stu-id="2e12c-118">RuleOperationError</span></span>](ruleoperationerror.md) <br/> |<span data-ttu-id="2e12c-119">Representa un error de operación de regla.</span><span class="sxs-lookup"><span data-stu-id="2e12c-119">Represents a rule operation error.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="2e12c-120">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="2e12c-120">Text value</span></span>

<span data-ttu-id="2e12c-121">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="2e12c-121">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2e12c-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2e12c-122">Remarks</span></span>

<span data-ttu-id="2e12c-123">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="2e12c-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2e12c-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="2e12c-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2e12c-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="2e12c-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="2e12c-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="2e12c-126">Schema Name</span></span>  <br/> |<span data-ttu-id="2e12c-127">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="2e12c-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="2e12c-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="2e12c-128">Validation File</span></span>  <br/> |<span data-ttu-id="2e12c-129">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="2e12c-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="2e12c-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="2e12c-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="2e12c-131">Verdadero</span><span class="sxs-lookup"><span data-stu-id="2e12c-131">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2e12c-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="2e12c-132">See also</span></span>



- [<span data-ttu-id="2e12c-133">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="2e12c-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

