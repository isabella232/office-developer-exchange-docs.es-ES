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
description: El elemento Value identifica un único destinatario o departamento de remitentes.
ms.openlocfilehash: 908ea451800abc343fb6e4d4a4ed98d57223bd23
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465243"
---
# <a name="value-protectionrulevaluetype"></a><span data-ttu-id="c8097-103">Valor (ProtectionRuleValueType)</span><span class="sxs-lookup"><span data-stu-id="c8097-103">Value (ProtectionRuleValueType)</span></span>

<span data-ttu-id="c8097-104">El elemento **Value** identifica un único destinatario o departamento de remitentes.</span><span class="sxs-lookup"><span data-stu-id="c8097-104">The **Value** element identifies a single recipient or sender department.</span></span> 
  
```XML
<Value/>
```

<span data-ttu-id="c8097-105">**ProtectionRuleValueType**</span><span class="sxs-lookup"><span data-stu-id="c8097-105">**ProtectionRuleValueType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="c8097-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="c8097-106">Attributes and elements</span></span>

<span data-ttu-id="c8097-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="c8097-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c8097-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="c8097-108">Attributes</span></span>

<span data-ttu-id="c8097-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="c8097-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c8097-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c8097-110">Child elements</span></span>

<span data-ttu-id="c8097-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="c8097-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="c8097-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="c8097-112">Parent elements</span></span>

|<span data-ttu-id="c8097-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="c8097-113">**Element**</span></span>|<span data-ttu-id="c8097-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c8097-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c8097-115">Destinatarioes</span><span class="sxs-lookup"><span data-stu-id="c8097-115">RecipientIs</span></span>](recipientis.md) <br/> |<span data-ttu-id="c8097-116">Especifica que cualquier destinatario del mensaje de correo electrónico coincide con cualquiera de los destinatarios especificados en los elementos secundarios de **valor** .</span><span class="sxs-lookup"><span data-stu-id="c8097-116">Specifies that any recipient of the email message matches any of the specified recipients in the child **Value** elements.</span></span>  <br/> |
|[<span data-ttu-id="c8097-117">SenderDepartments</span><span class="sxs-lookup"><span data-stu-id="c8097-117">SenderDepartments</span></span>](senderdepartments.md) <br/> |<span data-ttu-id="c8097-118">Especifica que el Departamento del remitente coincide con cualquiera de los departamentos especificados en los elementos secundarios de **valor** .</span><span class="sxs-lookup"><span data-stu-id="c8097-118">Specifies that the department of the sender matches any of the specified departments in the child **Value** elements.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="c8097-119">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="c8097-119">Text value</span></span>

<span data-ttu-id="c8097-120">Este elemento debe contener un valor de cadena no vacío.</span><span class="sxs-lookup"><span data-stu-id="c8097-120">This element must contain a nonempty string value.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c8097-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c8097-121">Remarks</span></span>

<span data-ttu-id="c8097-122">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="c8097-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c8097-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="c8097-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c8097-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="c8097-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c8097-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="c8097-125">Schema Name</span></span>  <br/> |<span data-ttu-id="c8097-126">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="c8097-126">Types schema</span></span>  <br/> |
|<span data-ttu-id="c8097-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="c8097-127">Validation File</span></span>  <br/> |<span data-ttu-id="c8097-128">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="c8097-128">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="c8097-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="c8097-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="c8097-130">Falso</span><span class="sxs-lookup"><span data-stu-id="c8097-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c8097-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="c8097-131">See also</span></span>

- [<span data-ttu-id="c8097-132">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="c8097-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

