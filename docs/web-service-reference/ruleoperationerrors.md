---
title: RuleOperationErrors
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f15c7b9e-a670-4a11-bb62-2a298c91f142
description: El elemento RuleOperationErrors representa una matriz de errores de validación de regla en cada campo de regla que tiene un error.
ms.openlocfilehash: d547155f3cbf9eedd0f9bfac7bf3768b3630b50e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/01/2020
ms.locfileid: "44464955"
---
# <a name="ruleoperationerrors"></a><span data-ttu-id="85caf-103">RuleOperationErrors</span><span class="sxs-lookup"><span data-stu-id="85caf-103">RuleOperationErrors</span></span>

<span data-ttu-id="85caf-104">El elemento **RuleOperationErrors** representa una matriz de errores de validación de regla en cada campo de regla que tiene un error.</span><span class="sxs-lookup"><span data-stu-id="85caf-104">The **RuleOperationErrors** element represents an array of rule validation errors on each rule field that has an error.</span></span> 
  
[<span data-ttu-id="85caf-105">UpdateInboxRulesResponse</span><span class="sxs-lookup"><span data-stu-id="85caf-105">UpdateInboxRulesResponse</span></span>](updateinboxrulesresponse.md)
  
[<span data-ttu-id="85caf-106">RuleOperationErrors</span><span class="sxs-lookup"><span data-stu-id="85caf-106">RuleOperationErrors</span></span>](ruleoperationerrors.md)
  
```XML
<RuleOperationErrors>
    <RuleOperationError>
</RuleOperationErrors>
```

 <span data-ttu-id="85caf-107">**ArrayOfRuleOperationErrorsType**</span><span class="sxs-lookup"><span data-stu-id="85caf-107">**ArrayOfRuleOperationErrorsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="85caf-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="85caf-108">Attributes and elements</span></span>

<span data-ttu-id="85caf-109">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="85caf-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="85caf-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="85caf-110">Attributes</span></span>

<span data-ttu-id="85caf-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="85caf-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="85caf-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="85caf-112">Child elements</span></span>

|<span data-ttu-id="85caf-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="85caf-113">**Element**</span></span>|<span data-ttu-id="85caf-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="85caf-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="85caf-115">RuleOperationError</span><span class="sxs-lookup"><span data-stu-id="85caf-115">RuleOperationError</span></span>](ruleoperationerror.md) <br/> |<span data-ttu-id="85caf-116">Representa un error de operación de regla.</span><span class="sxs-lookup"><span data-stu-id="85caf-116">Represents a rule operation error.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="85caf-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="85caf-117">Parent elements</span></span>

|<span data-ttu-id="85caf-118">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="85caf-118">**Element**</span></span>|<span data-ttu-id="85caf-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="85caf-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="85caf-120">UpdateInboxRulesResponse</span><span class="sxs-lookup"><span data-stu-id="85caf-120">UpdateInboxRulesResponse</span></span>](updateinboxrulesresponse.md) <br/> |<span data-ttu-id="85caf-121">Define una respuesta a una solicitud [UpdateInboxRules](updateinboxrules.md) .</span><span class="sxs-lookup"><span data-stu-id="85caf-121">Defines a response to an [UpdateInboxRules](updateinboxrules.md) request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="85caf-122">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="85caf-122">Text value</span></span>

<span data-ttu-id="85caf-123">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="85caf-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="85caf-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="85caf-124">Remarks</span></span>

<span data-ttu-id="85caf-125">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="85caf-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="85caf-126">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="85caf-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="85caf-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="85caf-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="85caf-128">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="85caf-128">Schema name</span></span>  <br/> |<span data-ttu-id="85caf-129">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="85caf-129">Messages schema</span></span>  <br/> |
|<span data-ttu-id="85caf-130">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="85caf-130">Validation file</span></span>  <br/> |<span data-ttu-id="85caf-131">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="85caf-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="85caf-132">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="85caf-132">Can be empty</span></span>  <br/> |<span data-ttu-id="85caf-133">Verdadero</span><span class="sxs-lookup"><span data-stu-id="85caf-133">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="85caf-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="85caf-134">See also</span></span>



[<span data-ttu-id="85caf-135">UpdateInboxRules</span><span class="sxs-lookup"><span data-stu-id="85caf-135">UpdateInboxRules</span></span>](updateinboxrules.md)


- [<span data-ttu-id="85caf-136">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="85caf-136">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

