---
title: Regla
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Rule
api_type:
- schema
ms.assetid: c30f3851-bd56-4473-9106-dc85e9619486
description: El elemento de regla contiene una regla de protección única.
ms.openlocfilehash: 9abbb70381c214211172d2d5ba1ed43ee4797f17
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19837263"
---
# <a name="rule"></a><span data-ttu-id="c8310-103">Regla</span><span class="sxs-lookup"><span data-stu-id="c8310-103">Rule</span></span>

<span data-ttu-id="c8310-104">El elemento de **regla** contiene una regla de protección única.</span><span class="sxs-lookup"><span data-stu-id="c8310-104">The **Rule** element contains a single protection rule.</span></span> 
  
```XML
<Rule Name="" UserOverridable=="" Priority="">
   <Condition/>
   <Action/>
</Rule>
```

 <span data-ttu-id="c8310-105">**ProtectionRuleType**</span><span class="sxs-lookup"><span data-stu-id="c8310-105">**ProtectionRuleType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c8310-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="c8310-106">Attributes and elements</span></span>

<span data-ttu-id="c8310-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="c8310-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c8310-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="c8310-108">Attributes</span></span>

|<span data-ttu-id="c8310-109">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="c8310-109">**Attribute**</span></span>|<span data-ttu-id="c8310-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c8310-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c8310-111">**Name**</span><span class="sxs-lookup"><span data-stu-id="c8310-111">**Name**</span></span> <br/> |<span data-ttu-id="c8310-112">Identifica el nombre de la regla.</span><span class="sxs-lookup"><span data-stu-id="c8310-112">Identifies the name of the rule.</span></span> <span data-ttu-id="c8310-113">Un atributo requerido de tipo string con una longitud mínima de 1.</span><span class="sxs-lookup"><span data-stu-id="c8310-113">A required attribute of type string with a minimum length of 1.</span></span>  <br/> |
|<span data-ttu-id="c8310-114">**UserOverridable**</span><span class="sxs-lookup"><span data-stu-id="c8310-114">**UserOverridable**</span></span> <br/> |<span data-ttu-id="c8310-115">Especifica si la regla es obligatoria.</span><span class="sxs-lookup"><span data-stu-id="c8310-115">Specifies whether the rule is mandatory.</span></span> <span data-ttu-id="c8310-116">Si la regla es obligatoria, este valor de atributo debe ser **false**.</span><span class="sxs-lookup"><span data-stu-id="c8310-116">If the rule is mandatory, this attribute value must be **false**.</span></span> <span data-ttu-id="c8310-117">Un atributo requerido de tipo Boolean.</span><span class="sxs-lookup"><span data-stu-id="c8310-117">A required attribute of type Boolean.</span></span>  <br/> |
|<span data-ttu-id="c8310-118">**Priority**</span><span class="sxs-lookup"><span data-stu-id="c8310-118">**Priority**</span></span> <br/> |<span data-ttu-id="c8310-119">Especifica la prioridad de la regla.</span><span class="sxs-lookup"><span data-stu-id="c8310-119">Specifies the rule priority.</span></span> <span data-ttu-id="c8310-120">Requiere un atributo de tipo int, con un valor mínimo de 1.</span><span class="sxs-lookup"><span data-stu-id="c8310-120">A required attribute of type int with a minimum value of 1.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="c8310-121">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c8310-121">Child elements</span></span>

|<span data-ttu-id="c8310-122">**Element**</span><span class="sxs-lookup"><span data-stu-id="c8310-122">**Element**</span></span>|<span data-ttu-id="c8310-123">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c8310-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c8310-124">Condición</span><span class="sxs-lookup"><span data-stu-id="c8310-124">Condition</span></span>](condition.md) <br/> |<span data-ttu-id="c8310-125">Identifica la condición que debe cumplirse para el elemento de acción de la regla que se va a ejecutar.</span><span class="sxs-lookup"><span data-stu-id="c8310-125">Identifies the condition that must be satisfied for the action part of the rule to be executed.</span></span>  <br/> |
|[<span data-ttu-id="c8310-126">Acción (ProtectionRuleActionType)</span><span class="sxs-lookup"><span data-stu-id="c8310-126">Action (ProtectionRuleActionType)</span></span>](action-protectionruleactiontype.md) <br/> |<span data-ttu-id="c8310-127">Identifica la acción que se debe ejecutar si coincide con la parte de la condición de la regla.</span><span class="sxs-lookup"><span data-stu-id="c8310-127">Identifies what action must be executed if the condition part of the rule matches.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="c8310-128">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="c8310-128">Parent elements</span></span>

|<span data-ttu-id="c8310-129">**Element**</span><span class="sxs-lookup"><span data-stu-id="c8310-129">**Element**</span></span>|<span data-ttu-id="c8310-130">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c8310-130">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c8310-131">Reglas</span><span class="sxs-lookup"><span data-stu-id="c8310-131">Rules </span></span>](rules-ex15websvcsotherref.md) <br/> |<span data-ttu-id="c8310-132">Contiene una matriz de las reglas de protección.</span><span class="sxs-lookup"><span data-stu-id="c8310-132">Contains an array of protection rules.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="c8310-133">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="c8310-133">Text value</span></span>

<span data-ttu-id="c8310-134">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="c8310-134">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c8310-135">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c8310-135">Remarks</span></span>

<span data-ttu-id="c8310-136">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="c8310-136">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c8310-137">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="c8310-137">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c8310-138">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c8310-138">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c8310-139">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="c8310-139">Schema Name</span></span>  <br/> |<span data-ttu-id="c8310-140">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="c8310-140">Types schema</span></span>  <br/> |
|<span data-ttu-id="c8310-141">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="c8310-141">Validation File</span></span>  <br/> |<span data-ttu-id="c8310-142">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="c8310-142">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="c8310-143">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="c8310-143">Can be Empty</span></span>  <br/> |<span data-ttu-id="c8310-144">False</span><span class="sxs-lookup"><span data-stu-id="c8310-144">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c8310-145">Ver también</span><span class="sxs-lookup"><span data-stu-id="c8310-145">See also</span></span>



- [<span data-ttu-id="c8310-146">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="c8310-146">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

