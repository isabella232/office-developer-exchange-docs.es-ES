---
title: Destinatarioes
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
description: El elemento recipient indica que cualquier destinatario del mensaje de correo electrónico coincide con cualquiera de los destinatarios especificados en los elementos de valor secundario (ProtectionRuleValueType).
ms.openlocfilehash: 8f27c4484ce310c62f9bab0e6ffeea2bfac1d3ef
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463884"
---
# <a name="recipientis"></a><span data-ttu-id="aee6f-103">Destinatarioes</span><span class="sxs-lookup"><span data-stu-id="aee6f-103">RecipientIs</span></span>

<span data-ttu-id="aee6f-104">El elemento **Recipient** indica que cualquier destinatario del mensaje de correo electrónico coincide con cualquiera de los destinatarios especificados en los elementos de [valor secundario (ProtectionRuleValueType)](value-protectionrulevaluetype.md) .</span><span class="sxs-lookup"><span data-stu-id="aee6f-104">The **RecipientIs** element specifies that any recipient of the e-mail message matches any of the specified recipients in the child [Value (ProtectionRuleValueType)](value-protectionrulevaluetype.md) elements.</span></span> 
  
```xml
<RecipientIs>   <Value/></RecipientIs>
```

 <span data-ttu-id="aee6f-105">**ProtectionRuleRecipientIsType**</span><span class="sxs-lookup"><span data-stu-id="aee6f-105">**ProtectionRuleRecipientIsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="aee6f-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="aee6f-106">Attributes and elements</span></span>

<span data-ttu-id="aee6f-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="aee6f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="aee6f-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="aee6f-108">Attributes</span></span>

<span data-ttu-id="aee6f-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="aee6f-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="aee6f-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="aee6f-110">Child elements</span></span>

|<span data-ttu-id="aee6f-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="aee6f-111">**Element**</span></span>|<span data-ttu-id="aee6f-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="aee6f-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="aee6f-113">Valor (ProtectionRuleValueType)</span><span class="sxs-lookup"><span data-stu-id="aee6f-113">Value (ProtectionRuleValueType)</span></span>](value-protectionrulevaluetype.md) <br/> |<span data-ttu-id="aee6f-114">Identifica a un destinatario.</span><span class="sxs-lookup"><span data-stu-id="aee6f-114">Identifies a recipient.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="aee6f-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="aee6f-115">Parent elements</span></span>

|<span data-ttu-id="aee6f-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="aee6f-116">**Element**</span></span>|<span data-ttu-id="aee6f-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="aee6f-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="aee6f-118">Condición</span><span class="sxs-lookup"><span data-stu-id="aee6f-118">Condition</span></span>](condition.md) <br/> |<span data-ttu-id="aee6f-119">Identifica la condición que debe cumplirse para que se ejecute la parte de acción de la regla.</span><span class="sxs-lookup"><span data-stu-id="aee6f-119">Identifies the condition that must be satisfied for the action part of the rule to be executed.</span></span>  <br/> |
|[<span data-ttu-id="aee6f-120">And (ProtectionRuleAndType)</span><span class="sxs-lookup"><span data-stu-id="aee6f-120">And (ProtectionRuleAndType)</span></span>](and-protectionruleandtype.md) <br/> |<span data-ttu-id="aee6f-121">Indica que todos los elementos secundarios deben coincidir para evaluarse en **true**.</span><span class="sxs-lookup"><span data-stu-id="aee6f-121">Indicates that all child elements must match to evaluate to **true**.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="aee6f-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="aee6f-122">Remarks</span></span>

<span data-ttu-id="aee6f-123">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2010 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="aee6f-123">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="aee6f-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="aee6f-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="aee6f-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="aee6f-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="aee6f-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="aee6f-126">Schema Name</span></span>  <br/> |<span data-ttu-id="aee6f-127">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="aee6f-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="aee6f-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="aee6f-128">Validation File</span></span>  <br/> |<span data-ttu-id="aee6f-129">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="aee6f-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="aee6f-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="aee6f-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="aee6f-131">Falso</span><span class="sxs-lookup"><span data-stu-id="aee6f-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="aee6f-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="aee6f-132">See also</span></span>



- [<span data-ttu-id="aee6f-133">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="aee6f-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

