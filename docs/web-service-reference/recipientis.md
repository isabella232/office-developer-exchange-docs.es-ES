---
title: RecipientIs
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RecipientIs
api_type:
- schema
ms.assetid: 5d2fd7ce-6137-4b3c-a716-c0218dcc8a09
description: El elemento RecipientIs especifica que todos los destinatarios del mensaje de correo electrónico coincide con cualquiera de los destinatarios especificados en los elementos de valor (ProtectionRuleValueType) secundarios.
ms.openlocfilehash: b6d5c150cd874d1aced7f2d83ff36409e0738728
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836975"
---
# <a name="recipientis"></a><span data-ttu-id="731f2-103">RecipientIs</span><span class="sxs-lookup"><span data-stu-id="731f2-103">RecipientIs</span></span>

<span data-ttu-id="731f2-104">El elemento **RecipientIs** especifica que todos los destinatarios del mensaje de correo electrónico coincide con cualquiera de los destinatarios especificados en el [valor (ProtectionRuleValueType)](value-protectionrulevaluetype.md) los elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="731f2-104">The **RecipientIs** element specifies that any recipient of the e-mail message matches any of the specified recipients in the child [Value (ProtectionRuleValueType)](value-protectionrulevaluetype.md) elements.</span></span> 
  
```xml
<RecipientIs>   <Value/></RecipientIs>
```

 <span data-ttu-id="731f2-105">**ProtectionRuleRecipientIsType**</span><span class="sxs-lookup"><span data-stu-id="731f2-105">**ProtectionRuleRecipientIsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="731f2-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="731f2-106">Attributes and elements</span></span>

<span data-ttu-id="731f2-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="731f2-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="731f2-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="731f2-108">Attributes</span></span>

<span data-ttu-id="731f2-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="731f2-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="731f2-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="731f2-110">Child elements</span></span>

|<span data-ttu-id="731f2-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="731f2-111">**Element**</span></span>|<span data-ttu-id="731f2-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="731f2-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="731f2-113">Valor (ProtectionRuleValueType)</span><span class="sxs-lookup"><span data-stu-id="731f2-113">Value (ProtectionRuleValueType)</span></span>](value-protectionrulevaluetype.md) <br/> |<span data-ttu-id="731f2-114">Identifica a un destinatario.</span><span class="sxs-lookup"><span data-stu-id="731f2-114">Identifies a recipient.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="731f2-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="731f2-115">Parent elements</span></span>

|<span data-ttu-id="731f2-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="731f2-116">**Element**</span></span>|<span data-ttu-id="731f2-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="731f2-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="731f2-118">Condición</span><span class="sxs-lookup"><span data-stu-id="731f2-118">Condition</span></span>](condition.md) <br/> |<span data-ttu-id="731f2-119">Identifica la condición que debe cumplirse para el elemento de acción de la regla que se va a ejecutar.</span><span class="sxs-lookup"><span data-stu-id="731f2-119">Identifies the condition that must be satisfied for the action part of the rule to be executed.</span></span>  <br/> |
|[<span data-ttu-id="731f2-120">Y (ProtectionRuleAndType)</span><span class="sxs-lookup"><span data-stu-id="731f2-120">And (ProtectionRuleAndType)</span></span>](and-protectionruleandtype.md) <br/> |<span data-ttu-id="731f2-121">Indica que deben coincidir con todos los elementos secundarios para evaluar en **true**.</span><span class="sxs-lookup"><span data-stu-id="731f2-121">Indicates that all child elements must match to evaluate to **true**.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="731f2-122">Notas</span><span class="sxs-lookup"><span data-stu-id="731f2-122">Remarks</span></span>

<span data-ttu-id="731f2-123">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2010 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="731f2-123">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="731f2-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="731f2-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="731f2-125">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="731f2-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="731f2-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="731f2-126">Schema Name</span></span>  <br/> |<span data-ttu-id="731f2-127">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="731f2-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="731f2-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="731f2-128">Validation File</span></span>  <br/> |<span data-ttu-id="731f2-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="731f2-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="731f2-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="731f2-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="731f2-131">False</span><span class="sxs-lookup"><span data-stu-id="731f2-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="731f2-132">Ver también</span><span class="sxs-lookup"><span data-stu-id="731f2-132">See also</span></span>



- [<span data-ttu-id="731f2-133">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="731f2-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

