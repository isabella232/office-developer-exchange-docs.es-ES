---
title: DeleteRuleOperation
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DeleteRuleOperation
api_type:
- schema
ms.assetid: c5e251af-f795-43cc-baaf-95d84475677c
description: El elemento DeleteRuleOperation contiene una operación para eliminar una regla de bandeja de entrada existente.
ms.openlocfilehash: 3410361e0b896fb0ef01c1873c9f8b0ac99afe58
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764109"
---
# <a name="deleteruleoperation"></a><span data-ttu-id="2abca-103">DeleteRuleOperation</span><span class="sxs-lookup"><span data-stu-id="2abca-103">DeleteRuleOperation</span></span>

<span data-ttu-id="2abca-104">El elemento **DeleteRuleOperation** contiene una operación para eliminar una regla de bandeja de entrada existente.</span><span class="sxs-lookup"><span data-stu-id="2abca-104">The **DeleteRuleOperation** element contains an operation to delete an existing Inbox rule.</span></span> 
  
- [<span data-ttu-id="2abca-105">UpdateInboxRules</span><span class="sxs-lookup"><span data-stu-id="2abca-105">UpdateInboxRules</span></span>](updateinboxrules.md)
- [<span data-ttu-id="2abca-106">Operations</span><span class="sxs-lookup"><span data-stu-id="2abca-106">Operations</span></span>](operations.md)
  
```XML
<DeleteRuleOperation>
    <RuleId/>
</DeleteRuleOperation>
```

 <span data-ttu-id="2abca-107">**DeleteRuleOperationType**</span><span class="sxs-lookup"><span data-stu-id="2abca-107">**DeleteRuleOperationType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2abca-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="2abca-108">Attributes and elements</span></span>

<span data-ttu-id="2abca-109">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="2abca-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2abca-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="2abca-110">Attributes</span></span>

<span data-ttu-id="2abca-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="2abca-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2abca-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="2abca-112">Child elements</span></span>

|<span data-ttu-id="2abca-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="2abca-113">**Element**</span></span>|<span data-ttu-id="2abca-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2abca-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2abca-115">Identificador de regla</span><span class="sxs-lookup"><span data-stu-id="2abca-115">RuleId</span></span>](ruleid.md) <br/> |<span data-ttu-id="2abca-116">Especifica el identificador de la regla para eliminar.</span><span class="sxs-lookup"><span data-stu-id="2abca-116">Specifies the identifier of the rule to delete.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="2abca-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="2abca-117">Parent elements</span></span>

|<span data-ttu-id="2abca-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="2abca-118">**Element**</span></span>|<span data-ttu-id="2abca-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2abca-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2abca-120">Operations</span><span class="sxs-lookup"><span data-stu-id="2abca-120">Operations</span></span>](operations.md) <br/> |<span data-ttu-id="2abca-121">Contiene una matriz de las operaciones de la regla que se puede realizar en una bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="2abca-121">Contains an array of rule operations that can be performed on an Inbox.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="2abca-122">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="2abca-122">Text value</span></span>

<span data-ttu-id="2abca-123">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="2abca-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2abca-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2abca-124">Remarks</span></span>

<span data-ttu-id="2abca-125">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="2abca-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2abca-126">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="2abca-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2abca-127">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="2abca-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="2abca-128">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="2abca-128">Schema Name</span></span>  <br/> |<span data-ttu-id="2abca-129">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="2abca-129">Types schema</span></span>  <br/> |
|<span data-ttu-id="2abca-130">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="2abca-130">Validation File</span></span>  <br/> |<span data-ttu-id="2abca-131">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="2abca-131">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="2abca-132">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="2abca-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="2abca-133">False</span><span class="sxs-lookup"><span data-stu-id="2abca-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2abca-134">Ver también</span><span class="sxs-lookup"><span data-stu-id="2abca-134">See also</span></span>

- [<span data-ttu-id="2abca-135">UpdateInboxRules</span><span class="sxs-lookup"><span data-stu-id="2abca-135">UpdateInboxRules</span></span>](updateinboxrules.md) 
- [<span data-ttu-id="2abca-136">SetRuleOperation</span><span class="sxs-lookup"><span data-stu-id="2abca-136">SetRuleOperation</span></span>](setruleoperation.md) 
- [<span data-ttu-id="2abca-137">CreateRuleOperation</span><span class="sxs-lookup"><span data-stu-id="2abca-137">CreateRuleOperation</span></span>](createruleoperation.md)
- [<span data-ttu-id="2abca-138">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="2abca-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

