---
title: AllInternal
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AllInternal
api_type:
- schema
ms.assetid: b7e5072f-5d9f-4ee0-b58b-4d75d878ea1c
description: El elemento AllInternal se evalúa como true si todos los destinatarios de un mensaje de correo electrónico son internos a la organización del remitente.
ms.openlocfilehash: c5ffe15eca5d680994acb62913ebf5effacce214
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44464836"
---
# <a name="allinternal"></a><span data-ttu-id="debaf-103">AllInternal</span><span class="sxs-lookup"><span data-stu-id="debaf-103">AllInternal</span></span>

<span data-ttu-id="debaf-104">El elemento **AllInternal** se evalúa como **true** si todos los destinatarios de un mensaje de correo electrónico son internos a la organización del remitente.</span><span class="sxs-lookup"><span data-stu-id="debaf-104">The **AllInternal** element evaluates to **true** if all recipients of an e-mail message are internal to the sender's organization.</span></span> 
  
```xml
<AllInternal/>
```

 <span data-ttu-id="debaf-105">**ProtectionRuleAllInternalType**</span><span class="sxs-lookup"><span data-stu-id="debaf-105">**ProtectionRuleAllInternalType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="debaf-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="debaf-106">Attributes and elements</span></span>

<span data-ttu-id="debaf-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="debaf-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="debaf-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="debaf-108">Attributes</span></span>

<span data-ttu-id="debaf-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="debaf-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="debaf-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="debaf-110">Child elements</span></span>

<span data-ttu-id="debaf-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="debaf-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="debaf-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="debaf-112">Parent elements</span></span>

|<span data-ttu-id="debaf-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="debaf-113">**Element**</span></span>|<span data-ttu-id="debaf-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="debaf-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="debaf-115">Condición</span><span class="sxs-lookup"><span data-stu-id="debaf-115">Condition</span></span>](condition.md) <br/> |<span data-ttu-id="debaf-116">Identifica la condición que debe cumplirse para que se ejecute la parte de acción de la regla.</span><span class="sxs-lookup"><span data-stu-id="debaf-116">Identifies the condition that must be satisfied for the action part of the rule to be executed.</span></span>  <br/> |
|[<span data-ttu-id="debaf-117">And (ProtectionRuleAndType)</span><span class="sxs-lookup"><span data-stu-id="debaf-117">And (ProtectionRuleAndType)</span></span>](and-protectionruleandtype.md) <br/> |<span data-ttu-id="debaf-118">Especifica que todos los elementos secundarios deben coincidir para evaluarse en **true**.</span><span class="sxs-lookup"><span data-stu-id="debaf-118">Specifies that all child elements must match to evaluate to **true**.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="debaf-119">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="debaf-119">Text value</span></span>

<span data-ttu-id="debaf-120">El elemento **AllInternal** debe estar vacío.</span><span class="sxs-lookup"><span data-stu-id="debaf-120">The **AllInternal** element must be empty.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="debaf-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="debaf-121">Remarks</span></span>

<span data-ttu-id="debaf-122">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="debaf-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="debaf-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="debaf-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="debaf-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="debaf-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="debaf-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="debaf-125">Schema Name</span></span>  <br/> |<span data-ttu-id="debaf-126">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="debaf-126">Types schema</span></span>  <br/> |
|<span data-ttu-id="debaf-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="debaf-127">Validation File</span></span>  <br/> |<span data-ttu-id="debaf-128">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="debaf-128">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="debaf-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="debaf-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="debaf-130">Falso</span><span class="sxs-lookup"><span data-stu-id="debaf-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="debaf-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="debaf-131">See also</span></span>

- [<span data-ttu-id="debaf-132">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="debaf-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

