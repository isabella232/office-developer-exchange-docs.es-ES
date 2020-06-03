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
description: El elemento SenderDepartments especifica que el Departamento del remitente coincide con cualquiera de los departamentos especificados en los elementos de valor secundario (ProtectionRuleValueType).
ms.openlocfilehash: cf15b974b9c0cfb09767661f17334defc4041e43
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530348"
---
# <a name="senderdepartments"></a><span data-ttu-id="cae12-103">SenderDepartments</span><span class="sxs-lookup"><span data-stu-id="cae12-103">SenderDepartments</span></span>

<span data-ttu-id="cae12-104">El elemento **SenderDepartments** especifica que el Departamento del remitente coincide con cualquiera de los departamentos especificados en los elementos de [valor secundario (ProtectionRuleValueType)](value-protectionrulevaluetype.md) .</span><span class="sxs-lookup"><span data-stu-id="cae12-104">The **SenderDepartments** element specifies that the department of the sender matches any of the specified departments in the child [Value (ProtectionRuleValueType)](value-protectionrulevaluetype.md) elements.</span></span> 
  
```XML
<SenderDepartments>
   <Value/>
</SenderDepartments>
```

 <span data-ttu-id="cae12-105">**ProtectionRuleSenderDepartmentsType**</span><span class="sxs-lookup"><span data-stu-id="cae12-105">**ProtectionRuleSenderDepartmentsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="cae12-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="cae12-106">Attributes and elements</span></span>

<span data-ttu-id="cae12-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="cae12-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cae12-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="cae12-108">Attributes</span></span>

<span data-ttu-id="cae12-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="cae12-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="cae12-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="cae12-110">Child elements</span></span>

|<span data-ttu-id="cae12-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="cae12-111">**Element**</span></span>|<span data-ttu-id="cae12-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="cae12-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cae12-113">Valor (ProtectionRuleValueType)</span><span class="sxs-lookup"><span data-stu-id="cae12-113">Value (ProtectionRuleValueType)</span></span>](value-protectionrulevaluetype.md) <br/> |<span data-ttu-id="cae12-114">Identifica un único departamento de remitentes.</span><span class="sxs-lookup"><span data-stu-id="cae12-114">Identifies a single sender department.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="cae12-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="cae12-115">Parent elements</span></span>

|<span data-ttu-id="cae12-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="cae12-116">**Element**</span></span>|<span data-ttu-id="cae12-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="cae12-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cae12-118">Condición</span><span class="sxs-lookup"><span data-stu-id="cae12-118">Condition</span></span>](condition.md) <br/> |<span data-ttu-id="cae12-119">Identifica la condición que debe cumplirse para que se ejecute la parte de acción de la regla.</span><span class="sxs-lookup"><span data-stu-id="cae12-119">Identifies the condition that must be satisfied for the action part of the rule to be executed.</span></span>  <br/> |
|[<span data-ttu-id="cae12-120">And (ProtectionRuleAndType)</span><span class="sxs-lookup"><span data-stu-id="cae12-120">And (ProtectionRuleAndType)</span></span>](and-protectionruleandtype.md) <br/> |<span data-ttu-id="cae12-121">Especifica que todos los elementos secundarios deben coincidir para evaluarse en **true**.</span><span class="sxs-lookup"><span data-stu-id="cae12-121">Specifies that all child elements must match to evaluate to **true**.</span></span> <span data-ttu-id="cae12-122">Especifica que debe haber más de una condición secundaria de regla de protección.</span><span class="sxs-lookup"><span data-stu-id="cae12-122">Specifies that there must be more than one protection rule child condition.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cae12-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="cae12-123">Remarks</span></span>

<span data-ttu-id="cae12-124">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="cae12-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="cae12-125">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="cae12-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cae12-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="cae12-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="cae12-127">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="cae12-127">Schema Name</span></span>  <br/> |<span data-ttu-id="cae12-128">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="cae12-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="cae12-129">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="cae12-129">Validation File</span></span>  <br/> |<span data-ttu-id="cae12-130">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="cae12-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="cae12-131">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="cae12-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="cae12-132">Falso</span><span class="sxs-lookup"><span data-stu-id="cae12-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cae12-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="cae12-133">See also</span></span>



- [<span data-ttu-id="cae12-134">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="cae12-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

