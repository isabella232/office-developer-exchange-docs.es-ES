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
ms.openlocfilehash: 0ffd4178e711e3117497eed682e3fd3e0594989b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763426"
---
# <a name="allinternal"></a><span data-ttu-id="ed457-103">AllInternal</span><span class="sxs-lookup"><span data-stu-id="ed457-103">AllInternal</span></span>

<span data-ttu-id="ed457-104">El elemento **AllInternal** se evalúa como **true** si todos los destinatarios de un mensaje de correo electrónico son internos a la organización del remitente.</span><span class="sxs-lookup"><span data-stu-id="ed457-104">The **AllInternal** element evaluates to **true** if all recipients of an e-mail message are internal to the sender's organization.</span></span> 
  
```xml
<AllInternal/>
```

 <span data-ttu-id="ed457-105">**ProtectionRuleAllInternalType**</span><span class="sxs-lookup"><span data-stu-id="ed457-105">**ProtectionRuleAllInternalType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ed457-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="ed457-106">Attributes and elements</span></span>

<span data-ttu-id="ed457-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="ed457-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ed457-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="ed457-108">Attributes</span></span>

<span data-ttu-id="ed457-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="ed457-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ed457-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ed457-110">Child elements</span></span>

<span data-ttu-id="ed457-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="ed457-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="ed457-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="ed457-112">Parent elements</span></span>

|<span data-ttu-id="ed457-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="ed457-113">**Element**</span></span>|<span data-ttu-id="ed457-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ed457-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ed457-115">Condición</span><span class="sxs-lookup"><span data-stu-id="ed457-115">Condition</span></span>](condition.md) <br/> |<span data-ttu-id="ed457-116">Identifica la condición que debe cumplirse para el elemento de acción de la regla que se va a ejecutar.</span><span class="sxs-lookup"><span data-stu-id="ed457-116">Identifies the condition that must be satisfied for the action part of the rule to be executed.</span></span>  <br/> |
|[<span data-ttu-id="ed457-117">Y (ProtectionRuleAndType)</span><span class="sxs-lookup"><span data-stu-id="ed457-117">And (ProtectionRuleAndType)</span></span>](and-protectionruleandtype.md) <br/> |<span data-ttu-id="ed457-118">Especifica que deben coincidir con todos los elementos secundarios para evaluar en **true**.</span><span class="sxs-lookup"><span data-stu-id="ed457-118">Specifies that all child elements must match to evaluate to **true**.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="ed457-119">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="ed457-119">Text value</span></span>

<span data-ttu-id="ed457-120">El elemento **AllInternal** debe estar vacío.</span><span class="sxs-lookup"><span data-stu-id="ed457-120">The **AllInternal** element must be empty.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="ed457-121">Notas</span><span class="sxs-lookup"><span data-stu-id="ed457-121">Remarks</span></span>

<span data-ttu-id="ed457-122">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="ed457-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ed457-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="ed457-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ed457-124">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="ed457-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ed457-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="ed457-125">Schema Name</span></span>  <br/> |<span data-ttu-id="ed457-126">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="ed457-126">Types schema</span></span>  <br/> |
|<span data-ttu-id="ed457-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="ed457-127">Validation File</span></span>  <br/> |<span data-ttu-id="ed457-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="ed457-128">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="ed457-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="ed457-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="ed457-130">False</span><span class="sxs-lookup"><span data-stu-id="ed457-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ed457-131">Ver también</span><span class="sxs-lookup"><span data-stu-id="ed457-131">See also</span></span>

- [<span data-ttu-id="ed457-132">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="ed457-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

