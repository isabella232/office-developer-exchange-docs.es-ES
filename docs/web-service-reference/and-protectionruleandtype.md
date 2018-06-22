---
title: Y (ProtectionRuleAndType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- And
api_type:
- schema
ms.assetid: 7fafd1c8-cd29-43a0-b383-f6595f934f48
description: El elemento y especifica que todos los elementos secundarios deben coincidir para que se evalúa como verdadero.
ms.openlocfilehash: 9e0128ee3fa2b6ffdc5975946694475afec53c25
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763437"
---
# <a name="and-protectionruleandtype"></a><span data-ttu-id="aeb62-103">Y (ProtectionRuleAndType)</span><span class="sxs-lookup"><span data-stu-id="aeb62-103">And (ProtectionRuleAndType)</span></span>

<span data-ttu-id="aeb62-104">El elemento **y** especifica que todos los elementos secundarios deben coincidir para que se evalúa como **true**.</span><span class="sxs-lookup"><span data-stu-id="aeb62-104">The **And** element specifies that all child elements must match to evaluate to **true**.</span></span>
  
```xml
<And>
   <AllInternal/>
   <And/>
   <RecipientIs/>
   <SenderDepartments/>
   <True/>
</And>
```

 <span data-ttu-id="aeb62-105">**ProtectionRuleAndType**</span><span class="sxs-lookup"><span data-stu-id="aeb62-105">**ProtectionRuleAndType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="aeb62-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="aeb62-106">Attributes and elements</span></span>

<span data-ttu-id="aeb62-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="aeb62-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="aeb62-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="aeb62-108">Attributes</span></span>

<span data-ttu-id="aeb62-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="aeb62-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="aeb62-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="aeb62-110">Child elements</span></span>

|<span data-ttu-id="aeb62-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="aeb62-111">**Element**</span></span>|<span data-ttu-id="aeb62-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="aeb62-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="aeb62-113">AllInternal</span><span class="sxs-lookup"><span data-stu-id="aeb62-113">AllInternal</span></span>](allinternal.md) <br/> |<span data-ttu-id="aeb62-114">Se evalúa como **true** si todos los destinatarios de un mensaje de correo electrónico son internos a la organización del remitente.</span><span class="sxs-lookup"><span data-stu-id="aeb62-114">Evaluates to **true** if all recipients of an e-mail message are internal to the sender's organization.</span></span>  <br/> |
|<span data-ttu-id="aeb62-115">**And**</span><span class="sxs-lookup"><span data-stu-id="aeb62-115">**And**</span></span> <br/> |<span data-ttu-id="aeb62-116">Especifica que deben coincidir con todos los elementos secundarios para evaluar en **true**.</span><span class="sxs-lookup"><span data-stu-id="aeb62-116">Specifies that all child elements must match to evaluate to **true**.</span></span>  <br/> |
|[<span data-ttu-id="aeb62-117">RecipientIs</span><span class="sxs-lookup"><span data-stu-id="aeb62-117">RecipientIs</span></span>](recipientis.md) <br/> |<span data-ttu-id="aeb62-118">Especifica que todos los destinatarios del mensaje de correo electrónico coincide con cualquiera de los destinatarios especificados en el [valor (ProtectionRuleValueType)](value-protectionrulevaluetype.md) los elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="aeb62-118">Specifies that any recipient of the e-mail message matches any of the specified recipients in the child [Value (ProtectionRuleValueType)](value-protectionrulevaluetype.md) elements.</span></span>  <br/> |
|[<span data-ttu-id="aeb62-119">SenderDepartments</span><span class="sxs-lookup"><span data-stu-id="aeb62-119">SenderDepartments</span></span>](senderdepartments.md) <br/> |<span data-ttu-id="aeb62-120">Especifica que el departamento del remitente coincide con cualquiera de los departamentos especificados en el [valor (ProtectionRuleValueType)](value-protectionrulevaluetype.md) los elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="aeb62-120">Specifies that the department of the sender matches any of the specified departments in the child [Value (ProtectionRuleValueType)](value-protectionrulevaluetype.md) elements.</span></span>  <br/> |
|[<span data-ttu-id="aeb62-121">True</span><span class="sxs-lookup"><span data-stu-id="aeb62-121">True</span></span>](true.md) <br/> |<span data-ttu-id="aeb62-122">Especifica una condición que siempre coincide con.</span><span class="sxs-lookup"><span data-stu-id="aeb62-122">Specifies a condition that always matches.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="aeb62-123">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="aeb62-123">Parent elements</span></span>

|<span data-ttu-id="aeb62-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="aeb62-124">**Element**</span></span>|<span data-ttu-id="aeb62-125">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="aeb62-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="aeb62-126">Condición</span><span class="sxs-lookup"><span data-stu-id="aeb62-126">Condition</span></span>](condition.md) <br/> |<span data-ttu-id="aeb62-127">Identifica la condición que debe cumplirse para el elemento de acción de la regla que se va a ejecutar.</span><span class="sxs-lookup"><span data-stu-id="aeb62-127">Identifies the condition that must be satisfied for the action part of the rule to be executed.</span></span>  <br/> |
|<span data-ttu-id="aeb62-128">**And**</span><span class="sxs-lookup"><span data-stu-id="aeb62-128">**And**</span></span> <br/> |<span data-ttu-id="aeb62-129">Especifica que deben coincidir con todos los elementos secundarios para evaluar en **true**.</span><span class="sxs-lookup"><span data-stu-id="aeb62-129">Specifies that all child elements must match to evaluate to **true**.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="aeb62-130">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="aeb62-130">Text value</span></span>

<span data-ttu-id="aeb62-131">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="aeb62-131">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="aeb62-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="aeb62-132">Remarks</span></span>

<span data-ttu-id="aeb62-133">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="aeb62-133">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="aeb62-134">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="aeb62-134">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="aeb62-135">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="aeb62-135">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="aeb62-136">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="aeb62-136">Schema Name</span></span>  <br/> |<span data-ttu-id="aeb62-137">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="aeb62-137">Types schema</span></span>  <br/> |
|<span data-ttu-id="aeb62-138">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="aeb62-138">Validation File</span></span>  <br/> |<span data-ttu-id="aeb62-139">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="aeb62-139">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="aeb62-140">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="aeb62-140">Can be Empty</span></span>  <br/> |<span data-ttu-id="aeb62-141">False</span><span class="sxs-lookup"><span data-stu-id="aeb62-141">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="aeb62-142">Ver también</span><span class="sxs-lookup"><span data-stu-id="aeb62-142">See also</span></span>

- [<span data-ttu-id="aeb62-143">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="aeb62-143">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

