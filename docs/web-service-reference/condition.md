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
description: El elemento Condition identifica la condición que debe cumplirse para que se ejecute la parte de acción de la regla.
ms.openlocfilehash: 2aea11197f072a4dbe21292bb47075d6f273d31b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463226"
---
# <a name="condition"></a><span data-ttu-id="ccabe-103">Condición</span><span class="sxs-lookup"><span data-stu-id="ccabe-103">Condition</span></span>

<span data-ttu-id="ccabe-104">El elemento **Condition** identifica la condición que debe cumplirse para que se ejecute la parte de acción de la regla.</span><span class="sxs-lookup"><span data-stu-id="ccabe-104">The **Condition** element identifies the condition that must be satisfied for the action part of the rule to be executed.</span></span> 
  
```xml
<Condition>
   <AllInternal/>
</Condition>
```

```xml
<Condition> 
    <SenderDepartments/> 
</Condition>
```

```xml
<Condition> 
    <True/> 
</Condition>
```

```xml
<Condition> 
    <Recipients/> 
</Condition>
```

```xml
<Condition> 
    <And/> 
</Condition>
```

<span data-ttu-id="ccabe-105">**ProtectionRuleConditionType**</span><span class="sxs-lookup"><span data-stu-id="ccabe-105">**ProtectionRuleConditionType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="ccabe-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="ccabe-106">Attributes and elements</span></span>

<span data-ttu-id="ccabe-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="ccabe-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ccabe-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="ccabe-108">Attributes</span></span>

<span data-ttu-id="ccabe-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="ccabe-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ccabe-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ccabe-110">Child elements</span></span>

|<span data-ttu-id="ccabe-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="ccabe-111">**Element**</span></span>|<span data-ttu-id="ccabe-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ccabe-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ccabe-113">AllInternal</span><span class="sxs-lookup"><span data-stu-id="ccabe-113">AllInternal</span></span>](allinternal.md) <br/> |<span data-ttu-id="ccabe-114">Se evalúa como **true** si todos los destinatarios de un mensaje de correo electrónico son internos a la organización del remitente.</span><span class="sxs-lookup"><span data-stu-id="ccabe-114">Evaluates to **true** if all recipients of an e-mail message are internal to the sender's organization.</span></span>  <br/> |
|[<span data-ttu-id="ccabe-115">And (ProtectionRuleAndType)</span><span class="sxs-lookup"><span data-stu-id="ccabe-115">And (ProtectionRuleAndType)</span></span>](and-protectionruleandtype.md) <br/> |<span data-ttu-id="ccabe-116">Especifica que todos los elementos secundarios deben coincidir para evaluarse en **true**.</span><span class="sxs-lookup"><span data-stu-id="ccabe-116">Specifies that all child elements must match to evaluate to **true**.</span></span> <span data-ttu-id="ccabe-117">Especifica que debe haber más de una condición secundaria de regla de protección.</span><span class="sxs-lookup"><span data-stu-id="ccabe-117">Specifies that there must be more than one protection rule child condition.</span></span>  <br/> |
|[<span data-ttu-id="ccabe-118">Destinatarioes</span><span class="sxs-lookup"><span data-stu-id="ccabe-118">RecipientIs</span></span>](recipientis.md) <br/> |<span data-ttu-id="ccabe-119">Especifica que cualquier destinatario del mensaje de correo electrónico coincide con cualquiera de los destinatarios especificados en los elementos de [valor secundario (ProtectionRuleValueType)](value-protectionrulevaluetype.md) .</span><span class="sxs-lookup"><span data-stu-id="ccabe-119">Specifies that any recipient of the e-mail message matches any of the specified recipients in the child [Value (ProtectionRuleValueType)](value-protectionrulevaluetype.md) elements.</span></span>  <br/> |
|[<span data-ttu-id="ccabe-120">SenderDepartments</span><span class="sxs-lookup"><span data-stu-id="ccabe-120">SenderDepartments</span></span>](senderdepartments.md) <br/> |<span data-ttu-id="ccabe-121">Especifica que el Departamento del remitente coincide con cualquiera de los departamentos especificados en los elementos de [valor secundario (ProtectionRuleValueType)](value-protectionrulevaluetype.md) .</span><span class="sxs-lookup"><span data-stu-id="ccabe-121">Specifies that the department of the sender matches any of the specified departments in the child [Value (ProtectionRuleValueType)](value-protectionrulevaluetype.md) elements.</span></span>  <br/> |
|[<span data-ttu-id="ccabe-122">True</span><span class="sxs-lookup"><span data-stu-id="ccabe-122">True</span></span>](true.md) <br/> |<span data-ttu-id="ccabe-123">Especifica una condición que siempre coincide.</span><span class="sxs-lookup"><span data-stu-id="ccabe-123">Specifies a condition that always matches.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ccabe-124">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="ccabe-124">Parent elements</span></span>

|<span data-ttu-id="ccabe-125">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="ccabe-125">**Element**</span></span>|<span data-ttu-id="ccabe-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ccabe-126">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ccabe-127">Rule</span><span class="sxs-lookup"><span data-stu-id="ccabe-127">Rule</span></span>](rule.md) <br/> |<span data-ttu-id="ccabe-128">Contiene una regla de protección única.</span><span class="sxs-lookup"><span data-stu-id="ccabe-128">Contains a single protection rule.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="ccabe-129">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="ccabe-129">Text value</span></span>

<span data-ttu-id="ccabe-130">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="ccabe-130">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ccabe-131">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ccabe-131">Remarks</span></span>

<span data-ttu-id="ccabe-132">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="ccabe-132">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ccabe-133">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="ccabe-133">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ccabe-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="ccabe-134">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ccabe-135">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="ccabe-135">Schema Name</span></span>  <br/> |<span data-ttu-id="ccabe-136">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="ccabe-136">Types schema</span></span>  <br/> |
|<span data-ttu-id="ccabe-137">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="ccabe-137">Validation File</span></span>  <br/> |<span data-ttu-id="ccabe-138">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="ccabe-138">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="ccabe-139">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="ccabe-139">Can be Empty</span></span>  <br/> |<span data-ttu-id="ccabe-140">Falso</span><span class="sxs-lookup"><span data-stu-id="ccabe-140">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ccabe-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="ccabe-141">See also</span></span>

- [<span data-ttu-id="ccabe-142">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="ccabe-142">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

