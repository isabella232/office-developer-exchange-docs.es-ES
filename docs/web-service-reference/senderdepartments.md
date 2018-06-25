---
title: SenderDepartments
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SenderDepartments
api_type:
- schema
ms.assetid: b016cdde-d597-40ac-87c4-63ca68bd539d
description: El elemento SenderDepartments especifica que el departamento del remitente coincide con cualquiera de los departamentos especificados en los elementos de valor (ProtectionRuleValueType) secundarios.
ms.openlocfilehash: d40e6299bd46ede559cc2cce3bcc9d1611e96bd7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19837331"
---
# <a name="senderdepartments"></a><span data-ttu-id="c5108-103">SenderDepartments</span><span class="sxs-lookup"><span data-stu-id="c5108-103">SenderDepartments</span></span>

<span data-ttu-id="c5108-104">El elemento **SenderDepartments** especifica que el departamento del remitente coincide con cualquiera de los departamentos especificados en el [valor (ProtectionRuleValueType)](value-protectionrulevaluetype.md) los elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="c5108-104">The **SenderDepartments** element specifies that the department of the sender matches any of the specified departments in the child [Value (ProtectionRuleValueType)](value-protectionrulevaluetype.md) elements.</span></span> 
  
```XML
<SenderDepartments>
   <Value/>
</SenderDepartments>
```

 <span data-ttu-id="c5108-105">**ProtectionRuleSenderDepartmentsType**</span><span class="sxs-lookup"><span data-stu-id="c5108-105">**ProtectionRuleSenderDepartmentsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c5108-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="c5108-106">Attributes and elements</span></span>

<span data-ttu-id="c5108-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="c5108-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c5108-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="c5108-108">Attributes</span></span>

<span data-ttu-id="c5108-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="c5108-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c5108-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c5108-110">Child elements</span></span>

|<span data-ttu-id="c5108-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="c5108-111">**Element**</span></span>|<span data-ttu-id="c5108-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c5108-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c5108-113">Valor (ProtectionRuleValueType)</span><span class="sxs-lookup"><span data-stu-id="c5108-113">Value (ProtectionRuleValueType)</span></span>](value-protectionrulevaluetype.md) <br/> |<span data-ttu-id="c5108-114">Identifica un departamento único remitente.</span><span class="sxs-lookup"><span data-stu-id="c5108-114">Identifies a single sender department.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="c5108-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="c5108-115">Parent elements</span></span>

|<span data-ttu-id="c5108-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="c5108-116">**Element**</span></span>|<span data-ttu-id="c5108-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c5108-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c5108-118">Condición</span><span class="sxs-lookup"><span data-stu-id="c5108-118">Condition</span></span>](condition.md) <br/> |<span data-ttu-id="c5108-119">Identifica la condición que debe cumplirse para el elemento de acción de la regla que se va a ejecutar.</span><span class="sxs-lookup"><span data-stu-id="c5108-119">Identifies the condition that must be satisfied for the action part of the rule to be executed.</span></span>  <br/> |
|[<span data-ttu-id="c5108-120">Y (ProtectionRuleAndType)</span><span class="sxs-lookup"><span data-stu-id="c5108-120">And (ProtectionRuleAndType)</span></span>](and-protectionruleandtype.md) <br/> |<span data-ttu-id="c5108-121">Especifica que deben coincidir con todos los elementos secundarios para evaluar en **true**.</span><span class="sxs-lookup"><span data-stu-id="c5108-121">Specifies that all child elements must match to evaluate to **true**.</span></span> <span data-ttu-id="c5108-122">Especifica que debe haber más de una condición de secundarios de regla de protección.</span><span class="sxs-lookup"><span data-stu-id="c5108-122">Specifies that there must be more than one protection rule child condition.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c5108-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c5108-123">Remarks</span></span>

<span data-ttu-id="c5108-124">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="c5108-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c5108-125">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="c5108-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c5108-126">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c5108-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c5108-127">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="c5108-127">Schema Name</span></span>  <br/> |<span data-ttu-id="c5108-128">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="c5108-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="c5108-129">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="c5108-129">Validation File</span></span>  <br/> |<span data-ttu-id="c5108-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="c5108-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="c5108-131">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="c5108-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="c5108-132">False</span><span class="sxs-lookup"><span data-stu-id="c5108-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c5108-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="c5108-133">See also</span></span>



- [<span data-ttu-id="c5108-134">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="c5108-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

