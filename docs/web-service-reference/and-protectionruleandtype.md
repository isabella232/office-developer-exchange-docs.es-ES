---
title: And (ProtectionRuleAndType)
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
description: El elemento y especifica que todos los elementos secundarios deben coincidir para que se evalúen como true.
ms.openlocfilehash: ba898ccd77518971afaf713d1c7c7955f46465d5
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44464738"
---
# <a name="and-protectionruleandtype"></a><span data-ttu-id="37db6-103">And (ProtectionRuleAndType)</span><span class="sxs-lookup"><span data-stu-id="37db6-103">And (ProtectionRuleAndType)</span></span>

<span data-ttu-id="37db6-104">El elemento **y** especifica que todos los elementos secundarios deben coincidir para que se evalúen como **true**.</span><span class="sxs-lookup"><span data-stu-id="37db6-104">The **And** element specifies that all child elements must match to evaluate to **true**.</span></span>
  
```xml
<And>
   <AllInternal/>
   <And/>
   <RecipientIs/>
   <SenderDepartments/>
   <True/>
</And>
```

 <span data-ttu-id="37db6-105">**ProtectionRuleAndType**</span><span class="sxs-lookup"><span data-stu-id="37db6-105">**ProtectionRuleAndType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="37db6-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="37db6-106">Attributes and elements</span></span>

<span data-ttu-id="37db6-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="37db6-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="37db6-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="37db6-108">Attributes</span></span>

<span data-ttu-id="37db6-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="37db6-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="37db6-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="37db6-110">Child elements</span></span>

|<span data-ttu-id="37db6-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="37db6-111">**Element**</span></span>|<span data-ttu-id="37db6-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="37db6-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="37db6-113">AllInternal</span><span class="sxs-lookup"><span data-stu-id="37db6-113">AllInternal</span></span>](allinternal.md) <br/> |<span data-ttu-id="37db6-114">Se evalúa como **true** si todos los destinatarios de un mensaje de correo electrónico son internos a la organización del remitente.</span><span class="sxs-lookup"><span data-stu-id="37db6-114">Evaluates to **true** if all recipients of an e-mail message are internal to the sender's organization.</span></span>  <br/> |
|<span data-ttu-id="37db6-115">**And**</span><span class="sxs-lookup"><span data-stu-id="37db6-115">**And**</span></span> <br/> |<span data-ttu-id="37db6-116">Especifica que todos los elementos secundarios deben coincidir para evaluarse en **true**.</span><span class="sxs-lookup"><span data-stu-id="37db6-116">Specifies that all child elements must match to evaluate to **true**.</span></span>  <br/> |
|[<span data-ttu-id="37db6-117">Destinatarioes</span><span class="sxs-lookup"><span data-stu-id="37db6-117">RecipientIs</span></span>](recipientis.md) <br/> |<span data-ttu-id="37db6-118">Especifica que cualquier destinatario del mensaje de correo electrónico coincide con cualquiera de los destinatarios especificados en los elementos de [valor secundario (ProtectionRuleValueType)](value-protectionrulevaluetype.md) .</span><span class="sxs-lookup"><span data-stu-id="37db6-118">Specifies that any recipient of the e-mail message matches any of the specified recipients in the child [Value (ProtectionRuleValueType)](value-protectionrulevaluetype.md) elements.</span></span>  <br/> |
|[<span data-ttu-id="37db6-119">SenderDepartments</span><span class="sxs-lookup"><span data-stu-id="37db6-119">SenderDepartments</span></span>](senderdepartments.md) <br/> |<span data-ttu-id="37db6-120">Especifica que el Departamento del remitente coincide con cualquiera de los departamentos especificados en los elementos de [valor secundario (ProtectionRuleValueType)](value-protectionrulevaluetype.md) .</span><span class="sxs-lookup"><span data-stu-id="37db6-120">Specifies that the department of the sender matches any of the specified departments in the child [Value (ProtectionRuleValueType)](value-protectionrulevaluetype.md) elements.</span></span>  <br/> |
|[<span data-ttu-id="37db6-121">True</span><span class="sxs-lookup"><span data-stu-id="37db6-121">True</span></span>](true.md) <br/> |<span data-ttu-id="37db6-122">Especifica una condición que siempre coincide.</span><span class="sxs-lookup"><span data-stu-id="37db6-122">Specifies a condition that always matches.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="37db6-123">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="37db6-123">Parent elements</span></span>

|<span data-ttu-id="37db6-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="37db6-124">**Element**</span></span>|<span data-ttu-id="37db6-125">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="37db6-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="37db6-126">Condición</span><span class="sxs-lookup"><span data-stu-id="37db6-126">Condition</span></span>](condition.md) <br/> |<span data-ttu-id="37db6-127">Identifica la condición que debe cumplirse para que se ejecute la parte de acción de la regla.</span><span class="sxs-lookup"><span data-stu-id="37db6-127">Identifies the condition that must be satisfied for the action part of the rule to be executed.</span></span>  <br/> |
|<span data-ttu-id="37db6-128">**And**</span><span class="sxs-lookup"><span data-stu-id="37db6-128">**And**</span></span> <br/> |<span data-ttu-id="37db6-129">Especifica que todos los elementos secundarios deben coincidir para evaluarse en **true**.</span><span class="sxs-lookup"><span data-stu-id="37db6-129">Specifies that all child elements must match to evaluate to **true**.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="37db6-130">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="37db6-130">Text value</span></span>

<span data-ttu-id="37db6-131">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="37db6-131">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="37db6-132">Comentarios</span><span class="sxs-lookup"><span data-stu-id="37db6-132">Remarks</span></span>

<span data-ttu-id="37db6-133">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="37db6-133">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="37db6-134">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="37db6-134">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="37db6-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="37db6-135">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="37db6-136">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="37db6-136">Schema Name</span></span>  <br/> |<span data-ttu-id="37db6-137">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="37db6-137">Types schema</span></span>  <br/> |
|<span data-ttu-id="37db6-138">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="37db6-138">Validation File</span></span>  <br/> |<span data-ttu-id="37db6-139">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="37db6-139">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="37db6-140">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="37db6-140">Can be Empty</span></span>  <br/> |<span data-ttu-id="37db6-141">Falso</span><span class="sxs-lookup"><span data-stu-id="37db6-141">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="37db6-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="37db6-142">See also</span></span>

- [<span data-ttu-id="37db6-143">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="37db6-143">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

