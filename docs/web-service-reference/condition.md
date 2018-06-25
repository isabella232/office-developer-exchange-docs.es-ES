---
title: Condición
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Condition
api_type:
- schema
ms.assetid: 0790a3f2-cb31-4036-a757-7821aa0722cb
description: El elemento Condition identifica la condición que debe cumplirse para el elemento de acción de la regla que se va a ejecutar.
ms.openlocfilehash: ed605946f99aa63416337cd0e731c931176a8ed4
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763763"
---
# <a name="condition"></a><span data-ttu-id="e1e24-103">Condición</span><span class="sxs-lookup"><span data-stu-id="e1e24-103">Condition</span></span>

<span data-ttu-id="e1e24-104">El elemento **Condition** identifica la condición que debe cumplirse para el elemento de acción de la regla que se va a ejecutar.</span><span class="sxs-lookup"><span data-stu-id="e1e24-104">The **Condition** element identifies the condition that must be satisfied for the action part of the rule to be executed.</span></span> 
  
```xml
<Condition>
   <AllInternal/>
</Condition>
```

 <span data-ttu-id="e1e24-105">**ProtectionRuleConditionType**</span><span class="sxs-lookup"><span data-stu-id="e1e24-105">**ProtectionRuleConditionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e1e24-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="e1e24-106">Attributes and elements</span></span>

<span data-ttu-id="e1e24-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="e1e24-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e1e24-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="e1e24-108">Attributes</span></span>

<span data-ttu-id="e1e24-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="e1e24-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e1e24-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="e1e24-110">Child elements</span></span>

|<span data-ttu-id="e1e24-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="e1e24-111">**Element**</span></span>|<span data-ttu-id="e1e24-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e1e24-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e1e24-113">AllInternal</span><span class="sxs-lookup"><span data-stu-id="e1e24-113">AllInternal</span></span>](allinternal.md) <br/> |<span data-ttu-id="e1e24-114">Se evalúa como **true** si todos los destinatarios de un mensaje de correo electrónico son internos a la organización del remitente.</span><span class="sxs-lookup"><span data-stu-id="e1e24-114">Evaluates to **true** if all recipients of an e-mail message are internal to the sender's organization.</span></span>  <br/> |
|[<span data-ttu-id="e1e24-115">Y (ProtectionRuleAndType)</span><span class="sxs-lookup"><span data-stu-id="e1e24-115">And (ProtectionRuleAndType)</span></span>](and-protectionruleandtype.md) <br/> |<span data-ttu-id="e1e24-116">Especifica que deben coincidir con todos los elementos secundarios para evaluar en **true**.</span><span class="sxs-lookup"><span data-stu-id="e1e24-116">Specifies that all child elements must match to evaluate to **true**.</span></span> <span data-ttu-id="e1e24-117">Especifica que debe haber más de una condición de secundarios de regla de protección.</span><span class="sxs-lookup"><span data-stu-id="e1e24-117">Specifies that there must be more than one protection rule child condition.</span></span>  <br/> |
|[<span data-ttu-id="e1e24-118">RecipientIs</span><span class="sxs-lookup"><span data-stu-id="e1e24-118">RecipientIs</span></span>](recipientis.md) <br/> |<span data-ttu-id="e1e24-119">Especifica que todos los destinatarios del mensaje de correo electrónico coincide con cualquiera de los destinatarios especificados en el [valor (ProtectionRuleValueType)](value-protectionrulevaluetype.md) los elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="e1e24-119">Specifies that any recipient of the e-mail message matches any of the specified recipients in the child [Value (ProtectionRuleValueType)](value-protectionrulevaluetype.md) elements.</span></span>  <br/> |
|[<span data-ttu-id="e1e24-120">SenderDepartments</span><span class="sxs-lookup"><span data-stu-id="e1e24-120">SenderDepartments</span></span>](senderdepartments.md) <br/> |<span data-ttu-id="e1e24-121">Especifica que el departamento del remitente coincide con cualquiera de los departamentos especificados en el [valor (ProtectionRuleValueType)](value-protectionrulevaluetype.md) los elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="e1e24-121">Specifies that the department of the sender matches any of the specified departments in the child [Value (ProtectionRuleValueType)](value-protectionrulevaluetype.md) elements.</span></span>  <br/> |
|[<span data-ttu-id="e1e24-122">True</span><span class="sxs-lookup"><span data-stu-id="e1e24-122">True</span></span>](true.md) <br/> |<span data-ttu-id="e1e24-123">Especifica una condición que siempre coincide con.</span><span class="sxs-lookup"><span data-stu-id="e1e24-123">Specifies a condition that always matches.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="e1e24-124">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="e1e24-124">Parent elements</span></span>

|<span data-ttu-id="e1e24-125">**Element**</span><span class="sxs-lookup"><span data-stu-id="e1e24-125">**Element**</span></span>|<span data-ttu-id="e1e24-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e1e24-126">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e1e24-127">Rule</span><span class="sxs-lookup"><span data-stu-id="e1e24-127">Rule</span></span>](rule.md) <br/> |<span data-ttu-id="e1e24-128">Contiene una regla de protección única.</span><span class="sxs-lookup"><span data-stu-id="e1e24-128">Contains a single protection rule.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="e1e24-129">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="e1e24-129">Text value</span></span>

<span data-ttu-id="e1e24-130">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="e1e24-130">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e1e24-131">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e1e24-131">Remarks</span></span>

<span data-ttu-id="e1e24-132">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="e1e24-132">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e1e24-133">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="e1e24-133">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e1e24-134">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e1e24-134">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="e1e24-135">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="e1e24-135">Schema Name</span></span>  <br/> |<span data-ttu-id="e1e24-136">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="e1e24-136">Types schema</span></span>  <br/> |
|<span data-ttu-id="e1e24-137">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="e1e24-137">Validation File</span></span>  <br/> |<span data-ttu-id="e1e24-138">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="e1e24-138">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="e1e24-139">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="e1e24-139">Can be Empty</span></span>  <br/> |<span data-ttu-id="e1e24-140">False</span><span class="sxs-lookup"><span data-stu-id="e1e24-140">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e1e24-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="e1e24-141">See also</span></span>



- [<span data-ttu-id="e1e24-142">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="e1e24-142">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

