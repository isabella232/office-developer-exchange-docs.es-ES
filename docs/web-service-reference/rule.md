---
title: Rule
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
description: El elemento rule contiene una única regla de protección.
ms.openlocfilehash: 6c18a2bd026893cd333bc7007203abf04a6f0be7
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465004"
---
# <a name="rule"></a><span data-ttu-id="791e6-103">Rule</span><span class="sxs-lookup"><span data-stu-id="791e6-103">Rule</span></span>

<span data-ttu-id="791e6-104">El elemento **Rule** contiene una única regla de protección.</span><span class="sxs-lookup"><span data-stu-id="791e6-104">The **Rule** element contains a single protection rule.</span></span> 
  
```XML
<Rule Name="" UserOverridable=="" Priority="">
   <Condition/>
   <Action/>
</Rule>
```

 <span data-ttu-id="791e6-105">**ProtectionRuleType**</span><span class="sxs-lookup"><span data-stu-id="791e6-105">**ProtectionRuleType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="791e6-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="791e6-106">Attributes and elements</span></span>

<span data-ttu-id="791e6-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="791e6-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="791e6-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="791e6-108">Attributes</span></span>

|<span data-ttu-id="791e6-109">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="791e6-109">**Attribute**</span></span>|<span data-ttu-id="791e6-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="791e6-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="791e6-111">**Name**</span><span class="sxs-lookup"><span data-stu-id="791e6-111">**Name**</span></span> <br/> |<span data-ttu-id="791e6-112">Identifica el nombre de la regla.</span><span class="sxs-lookup"><span data-stu-id="791e6-112">Identifies the name of the rule.</span></span> <span data-ttu-id="791e6-113">Un atributo necesario de tipo String con una longitud mínima de 1.</span><span class="sxs-lookup"><span data-stu-id="791e6-113">A required attribute of type string with a minimum length of 1.</span></span>  <br/> |
|<span data-ttu-id="791e6-114">**UserOverridable**</span><span class="sxs-lookup"><span data-stu-id="791e6-114">**UserOverridable**</span></span> <br/> |<span data-ttu-id="791e6-115">Especifica si la regla es obligatoria.</span><span class="sxs-lookup"><span data-stu-id="791e6-115">Specifies whether the rule is mandatory.</span></span> <span data-ttu-id="791e6-116">Si la regla es obligatoria, el valor de este atributo debe ser **false**.</span><span class="sxs-lookup"><span data-stu-id="791e6-116">If the rule is mandatory, this attribute value must be **false**.</span></span> <span data-ttu-id="791e6-117">Un atributo obligatorio de tipo Boolean.</span><span class="sxs-lookup"><span data-stu-id="791e6-117">A required attribute of type Boolean.</span></span>  <br/> |
|<span data-ttu-id="791e6-118">**Prioridad**</span><span class="sxs-lookup"><span data-stu-id="791e6-118">**Priority**</span></span> <br/> |<span data-ttu-id="791e6-119">Especifica la prioridad de la regla.</span><span class="sxs-lookup"><span data-stu-id="791e6-119">Specifies the rule priority.</span></span> <span data-ttu-id="791e6-120">Un atributo obligatorio de tipo int con un valor mínimo de 1.</span><span class="sxs-lookup"><span data-stu-id="791e6-120">A required attribute of type int with a minimum value of 1.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="791e6-121">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="791e6-121">Child elements</span></span>

|<span data-ttu-id="791e6-122">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="791e6-122">**Element**</span></span>|<span data-ttu-id="791e6-123">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="791e6-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="791e6-124">Condición</span><span class="sxs-lookup"><span data-stu-id="791e6-124">Condition</span></span>](condition.md) <br/> |<span data-ttu-id="791e6-125">Identifica la condición que debe cumplirse para que se ejecute la parte de acción de la regla.</span><span class="sxs-lookup"><span data-stu-id="791e6-125">Identifies the condition that must be satisfied for the action part of the rule to be executed.</span></span>  <br/> |
|[<span data-ttu-id="791e6-126">Acción (ProtectionRuleActionType)</span><span class="sxs-lookup"><span data-stu-id="791e6-126">Action (ProtectionRuleActionType)</span></span>](action-protectionruleactiontype.md) <br/> |<span data-ttu-id="791e6-127">Identifica qué acción debe ejecutarse si la parte de condición de la regla coincide.</span><span class="sxs-lookup"><span data-stu-id="791e6-127">Identifies what action must be executed if the condition part of the rule matches.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="791e6-128">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="791e6-128">Parent elements</span></span>

|<span data-ttu-id="791e6-129">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="791e6-129">**Element**</span></span>|<span data-ttu-id="791e6-130">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="791e6-130">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="791e6-131">Reglas</span><span class="sxs-lookup"><span data-stu-id="791e6-131">Rules </span></span>](rules-ex15websvcsotherref.md) <br/> |<span data-ttu-id="791e6-132">Contiene una matriz de reglas de protección.</span><span class="sxs-lookup"><span data-stu-id="791e6-132">Contains an array of protection rules.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="791e6-133">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="791e6-133">Text value</span></span>

<span data-ttu-id="791e6-134">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="791e6-134">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="791e6-135">Comentarios</span><span class="sxs-lookup"><span data-stu-id="791e6-135">Remarks</span></span>

<span data-ttu-id="791e6-136">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="791e6-136">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="791e6-137">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="791e6-137">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="791e6-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="791e6-138">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="791e6-139">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="791e6-139">Schema Name</span></span>  <br/> |<span data-ttu-id="791e6-140">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="791e6-140">Types schema</span></span>  <br/> |
|<span data-ttu-id="791e6-141">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="791e6-141">Validation File</span></span>  <br/> |<span data-ttu-id="791e6-142">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="791e6-142">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="791e6-143">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="791e6-143">Can be Empty</span></span>  <br/> |<span data-ttu-id="791e6-144">Falso</span><span class="sxs-lookup"><span data-stu-id="791e6-144">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="791e6-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="791e6-145">See also</span></span>



- [<span data-ttu-id="791e6-146">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="791e6-146">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

