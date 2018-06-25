---
title: Valor (ProtectionRuleValueType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Value
api_type:
- schema
ms.assetid: b039bd6e-2198-47cf-9c78-a5e8b9d51c98
description: El elemento de valor identifica un solo departamento de remitente o destinatario.
ms.openlocfilehash: 6173f94dcfb83eafd62e35f185a5e8c669d50f6c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19840951"
---
# <a name="value-protectionrulevaluetype"></a><span data-ttu-id="d4e2d-103">Valor (ProtectionRuleValueType)</span><span class="sxs-lookup"><span data-stu-id="d4e2d-103">Value (ProtectionRuleValueType)</span></span>

<span data-ttu-id="d4e2d-104">El elemento de **valor** identifica un solo departamento de remitente o destinatario.</span><span class="sxs-lookup"><span data-stu-id="d4e2d-104">The **Value** element identifies a single recipient or sender department.</span></span> 
  
```XML
<Value/>
```

<span data-ttu-id="d4e2d-105">**ProtectionRuleValueType**</span><span class="sxs-lookup"><span data-stu-id="d4e2d-105">**ProtectionRuleValueType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="d4e2d-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="d4e2d-106">Attributes and elements</span></span>

<span data-ttu-id="d4e2d-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="d4e2d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d4e2d-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="d4e2d-108">Attributes</span></span>

<span data-ttu-id="d4e2d-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="d4e2d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d4e2d-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="d4e2d-110">Child elements</span></span>

<span data-ttu-id="d4e2d-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="d4e2d-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="d4e2d-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="d4e2d-112">Parent elements</span></span>

|<span data-ttu-id="d4e2d-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="d4e2d-113">**Element**</span></span>|<span data-ttu-id="d4e2d-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d4e2d-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d4e2d-115">RecipientIs</span><span class="sxs-lookup"><span data-stu-id="d4e2d-115">RecipientIs</span></span>](recipientis.md) <br/> |<span data-ttu-id="d4e2d-116">Especifica que todos los destinatarios del mensaje de correo electrónico coincide con cualquiera de los destinatarios especificados en el **valor de** los elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="d4e2d-116">Specifies that any recipient of the email message matches any of the specified recipients in the child **Value** elements.</span></span>  <br/> |
|[<span data-ttu-id="d4e2d-117">SenderDepartments</span><span class="sxs-lookup"><span data-stu-id="d4e2d-117">SenderDepartments</span></span>](senderdepartments.md) <br/> |<span data-ttu-id="d4e2d-118">Especifica que el departamento del remitente coincide con cualquiera de los departamentos especificados en el **valor de** los elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="d4e2d-118">Specifies that the department of the sender matches any of the specified departments in the child **Value** elements.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="d4e2d-119">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="d4e2d-119">Text value</span></span>

<span data-ttu-id="d4e2d-120">Este elemento debe contener un valor de cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="d4e2d-120">This element must contain a nonempty string value.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d4e2d-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d4e2d-121">Remarks</span></span>

<span data-ttu-id="d4e2d-122">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="d4e2d-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d4e2d-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="d4e2d-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d4e2d-124">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d4e2d-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d4e2d-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="d4e2d-125">Schema Name</span></span>  <br/> |<span data-ttu-id="d4e2d-126">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="d4e2d-126">Types schema</span></span>  <br/> |
|<span data-ttu-id="d4e2d-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="d4e2d-127">Validation File</span></span>  <br/> |<span data-ttu-id="d4e2d-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="d4e2d-128">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d4e2d-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="d4e2d-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="d4e2d-130">False</span><span class="sxs-lookup"><span data-stu-id="d4e2d-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d4e2d-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="d4e2d-131">See also</span></span>

- [<span data-ttu-id="d4e2d-132">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="d4e2d-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

