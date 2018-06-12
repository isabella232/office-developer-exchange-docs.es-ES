---
title: CreateRuleOperation
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CreateRuleOperation
api_type:
- schema
ms.assetid: e9f70726-db08-4089-839e-a41007d0a473
description: El elemento CreateRuleOperation representa una operación para crear una nueva regla de bandeja de entrada.
ms.openlocfilehash: c531f222ffe886e6ef53a99609cfa27e84fd6107
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763970"
---
# <a name="createruleoperation"></a><span data-ttu-id="574c3-103">CreateRuleOperation</span><span class="sxs-lookup"><span data-stu-id="574c3-103">CreateRuleOperation</span></span>

<span data-ttu-id="574c3-104">El elemento **CreateRuleOperation** representa una operación para crear una nueva regla de bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="574c3-104">The **CreateRuleOperation** element represents an operation to create a new Inbox rule.</span></span> 
  
[<span data-ttu-id="574c3-105">UpdateInboxRules</span><span class="sxs-lookup"><span data-stu-id="574c3-105">UpdateInboxRules</span></span>](updateinboxrules.md)
  
[<span data-ttu-id="574c3-106">Operations</span><span class="sxs-lookup"><span data-stu-id="574c3-106">Operations</span></span>](operations.md)
  
```xml
<CreateRuleOperation>
    <Rule/>
</CreateRuleOperation>
```

 <span data-ttu-id="574c3-107">**CreateRuleOperationType**</span><span class="sxs-lookup"><span data-stu-id="574c3-107">**CreateRuleOperationType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="574c3-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="574c3-108">Attributes and elements</span></span>

<span data-ttu-id="574c3-109">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="574c3-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="574c3-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="574c3-110">Attributes</span></span>

<span data-ttu-id="574c3-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="574c3-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="574c3-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="574c3-112">Child elements</span></span>

|<span data-ttu-id="574c3-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="574c3-113">**Element**</span></span>|<span data-ttu-id="574c3-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="574c3-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="574c3-115">Regla (RuleType)</span><span class="sxs-lookup"><span data-stu-id="574c3-115">Rule (RuleType)</span></span>](rule-ruletype.md) <br/> |<span data-ttu-id="574c3-116">Representa una regla que se creará en el buzón del usuario.</span><span class="sxs-lookup"><span data-stu-id="574c3-116">Represents a rule to be created in a user's mailbox.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="574c3-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="574c3-117">Parent elements</span></span>

|<span data-ttu-id="574c3-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="574c3-118">**Element**</span></span>|<span data-ttu-id="574c3-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="574c3-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="574c3-120">Operations</span><span class="sxs-lookup"><span data-stu-id="574c3-120">Operations</span></span>](operations.md) <br/> |<span data-ttu-id="574c3-121">Contiene las operaciones que se pueden realizar en una bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="574c3-121">Contains the operations that can be performed on an Inbox.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="574c3-122">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="574c3-122">Text value</span></span>

<span data-ttu-id="574c3-123">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="574c3-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="574c3-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="574c3-124">Remarks</span></span>

<span data-ttu-id="574c3-125">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="574c3-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="574c3-126">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="574c3-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="574c3-127">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="574c3-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="574c3-128">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="574c3-128">Schema Name</span></span>  <br/> |<span data-ttu-id="574c3-129">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="574c3-129">Types schema</span></span>  <br/> |
|<span data-ttu-id="574c3-130">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="574c3-130">Validation File</span></span>  <br/> |<span data-ttu-id="574c3-131">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="574c3-131">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="574c3-132">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="574c3-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="574c3-133">False</span><span class="sxs-lookup"><span data-stu-id="574c3-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="574c3-134">Ver también</span><span class="sxs-lookup"><span data-stu-id="574c3-134">See also</span></span>



[<span data-ttu-id="574c3-135">UpdateInboxRules</span><span class="sxs-lookup"><span data-stu-id="574c3-135">UpdateInboxRules</span></span>](updateinboxrules.md)
  
[<span data-ttu-id="574c3-136">SetRuleOperation</span><span class="sxs-lookup"><span data-stu-id="574c3-136">SetRuleOperation</span></span>](setruleoperation.md)
  
[<span data-ttu-id="574c3-137">DeleteRuleOperation</span><span class="sxs-lookup"><span data-stu-id="574c3-137">DeleteRuleOperation</span></span>](deleteruleoperation.md)


- [<span data-ttu-id="574c3-138">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="574c3-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

