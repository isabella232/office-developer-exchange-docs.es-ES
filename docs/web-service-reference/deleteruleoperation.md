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
ms.openlocfilehash: 6b17f7f99f1fd9b9889db00fdf55fba5eef5aba8
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526924"
---
# <a name="deleteruleoperation"></a><span data-ttu-id="fce55-103">DeleteRuleOperation</span><span class="sxs-lookup"><span data-stu-id="fce55-103">DeleteRuleOperation</span></span>

<span data-ttu-id="fce55-104">El elemento **DeleteRuleOperation** contiene una operación para eliminar una regla de bandeja de entrada existente.</span><span class="sxs-lookup"><span data-stu-id="fce55-104">The **DeleteRuleOperation** element contains an operation to delete an existing Inbox rule.</span></span> 
  
- [<span data-ttu-id="fce55-105">UpdateInboxRules</span><span class="sxs-lookup"><span data-stu-id="fce55-105">UpdateInboxRules</span></span>](updateinboxrules.md)
- [<span data-ttu-id="fce55-106">Operations</span><span class="sxs-lookup"><span data-stu-id="fce55-106">Operations</span></span>](operations.md)
  
```XML
<DeleteRuleOperation>
    <RuleId/>
</DeleteRuleOperation>
```

 <span data-ttu-id="fce55-107">**DeleteRuleOperationType**</span><span class="sxs-lookup"><span data-stu-id="fce55-107">**DeleteRuleOperationType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="fce55-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="fce55-108">Attributes and elements</span></span>

<span data-ttu-id="fce55-109">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="fce55-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fce55-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="fce55-110">Attributes</span></span>

<span data-ttu-id="fce55-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="fce55-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="fce55-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="fce55-112">Child elements</span></span>

|<span data-ttu-id="fce55-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="fce55-113">**Element**</span></span>|<span data-ttu-id="fce55-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="fce55-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fce55-115">RuleId</span><span class="sxs-lookup"><span data-stu-id="fce55-115">RuleId</span></span>](ruleid.md) <br/> |<span data-ttu-id="fce55-116">Especifica el identificador de la regla que se va a eliminar.</span><span class="sxs-lookup"><span data-stu-id="fce55-116">Specifies the identifier of the rule to delete.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="fce55-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="fce55-117">Parent elements</span></span>

|<span data-ttu-id="fce55-118">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="fce55-118">**Element**</span></span>|<span data-ttu-id="fce55-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="fce55-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fce55-120">Operations</span><span class="sxs-lookup"><span data-stu-id="fce55-120">Operations</span></span>](operations.md) <br/> |<span data-ttu-id="fce55-121">Contiene una matriz de operaciones de regla que se pueden realizar en una bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="fce55-121">Contains an array of rule operations that can be performed on an Inbox.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="fce55-122">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="fce55-122">Text value</span></span>

<span data-ttu-id="fce55-123">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="fce55-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="fce55-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="fce55-124">Remarks</span></span>

<span data-ttu-id="fce55-125">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="fce55-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fce55-126">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="fce55-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fce55-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="fce55-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="fce55-128">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="fce55-128">Schema Name</span></span>  <br/> |<span data-ttu-id="fce55-129">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="fce55-129">Types schema</span></span>  <br/> |
|<span data-ttu-id="fce55-130">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="fce55-130">Validation File</span></span>  <br/> |<span data-ttu-id="fce55-131">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="fce55-131">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="fce55-132">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="fce55-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="fce55-133">Falso</span><span class="sxs-lookup"><span data-stu-id="fce55-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fce55-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="fce55-134">See also</span></span>

- [<span data-ttu-id="fce55-135">UpdateInboxRules</span><span class="sxs-lookup"><span data-stu-id="fce55-135">UpdateInboxRules</span></span>](updateinboxrules.md) 
- [<span data-ttu-id="fce55-136">SetRuleOperation</span><span class="sxs-lookup"><span data-stu-id="fce55-136">SetRuleOperation</span></span>](setruleoperation.md) 
- [<span data-ttu-id="fce55-137">CreateRuleOperation</span><span class="sxs-lookup"><span data-stu-id="fce55-137">CreateRuleOperation</span></span>](createruleoperation.md)
- [<span data-ttu-id="fce55-138">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="fce55-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

