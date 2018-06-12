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
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763763"
---
# <a name="condition"></a><span data-ttu-id="7088c-103">Condición</span><span class="sxs-lookup"><span data-stu-id="7088c-103">Condition</span></span>

<span data-ttu-id="7088c-104">El elemento **Condition** identifica la condición que debe cumplirse para el elemento de acción de la regla que se va a ejecutar.</span><span class="sxs-lookup"><span data-stu-id="7088c-104">The **Condition** element identifies the condition that must be satisfied for the action part of the rule to be executed.</span></span> 
  
```xml
<Condition>
   <AllInternal/>
</Condition>
```

 <span data-ttu-id="7088c-105">**ProtectionRuleConditionType**</span><span class="sxs-lookup"><span data-stu-id="7088c-105">**ProtectionRuleConditionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7088c-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="7088c-106">Attributes and elements</span></span>

<span data-ttu-id="7088c-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="7088c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7088c-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="7088c-108">Attributes</span></span>

<span data-ttu-id="7088c-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="7088c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7088c-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="7088c-110">Child elements</span></span>

|<span data-ttu-id="7088c-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="7088c-111">**Element**</span></span>|<span data-ttu-id="7088c-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7088c-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7088c-113">AllInternal</span><span class="sxs-lookup"><span data-stu-id="7088c-113">AllInternal</span></span>](allinternal.md) <br/> |<span data-ttu-id="7088c-114">Se evalúa como **true** si todos los destinatarios de un mensaje de correo electrónico son internos a la organización del remitente.</span><span class="sxs-lookup"><span data-stu-id="7088c-114">Evaluates to **true** if all recipients of an e-mail message are internal to the sender's organization.</span></span>  <br/> |
|[<span data-ttu-id="7088c-115">Y (ProtectionRuleAndType)</span><span class="sxs-lookup"><span data-stu-id="7088c-115">And (ProtectionRuleAndType)</span></span>](and-protectionruleandtype.md) <br/> |<span data-ttu-id="7088c-116">Especifica que deben coincidir con todos los elementos secundarios para evaluar en **true**.</span><span class="sxs-lookup"><span data-stu-id="7088c-116">Specifies that all child elements must match to evaluate to **true**.</span></span> <span data-ttu-id="7088c-117">Especifica que debe haber más de una condición de secundarios de regla de protección.</span><span class="sxs-lookup"><span data-stu-id="7088c-117">Specifies that there must be more than one protection rule child condition.</span></span>  <br/> |
|[<span data-ttu-id="7088c-118">RecipientIs</span><span class="sxs-lookup"><span data-stu-id="7088c-118">RecipientIs</span></span>](recipientis.md) <br/> |<span data-ttu-id="7088c-119">Especifica que todos los destinatarios del mensaje de correo electrónico coincide con cualquiera de los destinatarios especificados en el [valor (ProtectionRuleValueType)](value-protectionrulevaluetype.md) los elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="7088c-119">Specifies that any recipient of the e-mail message matches any of the specified recipients in the child [Value (ProtectionRuleValueType)](value-protectionrulevaluetype.md) elements.</span></span>  <br/> |
|[<span data-ttu-id="7088c-120">SenderDepartments</span><span class="sxs-lookup"><span data-stu-id="7088c-120">SenderDepartments</span></span>](senderdepartments.md) <br/> |<span data-ttu-id="7088c-121">Especifica que el departamento del remitente coincide con cualquiera de los departamentos especificados en el [valor (ProtectionRuleValueType)](value-protectionrulevaluetype.md) los elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="7088c-121">Specifies that the department of the sender matches any of the specified departments in the child [Value (ProtectionRuleValueType)](value-protectionrulevaluetype.md) elements.</span></span>  <br/> |
|[<span data-ttu-id="7088c-122">True</span><span class="sxs-lookup"><span data-stu-id="7088c-122">True</span></span>](true.md) <br/> |<span data-ttu-id="7088c-123">Especifica una condición que siempre coincide con.</span><span class="sxs-lookup"><span data-stu-id="7088c-123">Specifies a condition that always matches.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="7088c-124">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="7088c-124">Parent elements</span></span>

|<span data-ttu-id="7088c-125">**Element**</span><span class="sxs-lookup"><span data-stu-id="7088c-125">**Element**</span></span>|<span data-ttu-id="7088c-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7088c-126">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7088c-127">Rule</span><span class="sxs-lookup"><span data-stu-id="7088c-127">Rule</span></span>](rule.md) <br/> |<span data-ttu-id="7088c-128">Contiene una regla de protección única.</span><span class="sxs-lookup"><span data-stu-id="7088c-128">Contains a single protection rule.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="7088c-129">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="7088c-129">Text value</span></span>

<span data-ttu-id="7088c-130">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="7088c-130">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7088c-131">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7088c-131">Remarks</span></span>

<span data-ttu-id="7088c-132">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="7088c-132">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7088c-133">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="7088c-133">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7088c-134">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="7088c-134">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="7088c-135">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="7088c-135">Schema Name</span></span>  <br/> |<span data-ttu-id="7088c-136">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="7088c-136">Types schema</span></span>  <br/> |
|<span data-ttu-id="7088c-137">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="7088c-137">Validation File</span></span>  <br/> |<span data-ttu-id="7088c-138">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="7088c-138">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="7088c-139">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="7088c-139">Can be Empty</span></span>  <br/> |<span data-ttu-id="7088c-140">False</span><span class="sxs-lookup"><span data-stu-id="7088c-140">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7088c-141">Ver también</span><span class="sxs-lookup"><span data-stu-id="7088c-141">See also</span></span>



- [<span data-ttu-id="7088c-142">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="7088c-142">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

