---
title: SetRuleOperation
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SetRuleOperation
api_type:
- schema
ms.assetid: 2106a85b-58fe-49be-b71d-4ca6aa66e060
description: El elemento SetRuleOperation representa una operación para actualizar una regla existente.
ms.openlocfilehash: 9c956394d14c510e8dcc95110ef1874ea7010be0
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19837451"
---
# <a name="setruleoperation"></a><span data-ttu-id="9c0fa-103">SetRuleOperation</span><span class="sxs-lookup"><span data-stu-id="9c0fa-103">SetRuleOperation</span></span>

<span data-ttu-id="9c0fa-104">El elemento **SetRuleOperation** representa una operación para actualizar una regla existente.</span><span class="sxs-lookup"><span data-stu-id="9c0fa-104">The **SetRuleOperation** element represents an operation to update an existing rule.</span></span> 
  
[<span data-ttu-id="9c0fa-105">UpdateInboxRules</span><span class="sxs-lookup"><span data-stu-id="9c0fa-105">UpdateInboxRules</span></span>](updateinboxrules.md)
  
[<span data-ttu-id="9c0fa-106">Operations</span><span class="sxs-lookup"><span data-stu-id="9c0fa-106">Operations</span></span>](operations.md)
  
```XML
<SetRuleOperation>
    <Rule/>
</SetRuleOperation>
```

 <span data-ttu-id="9c0fa-107">**SetRuleOperationType**</span><span class="sxs-lookup"><span data-stu-id="9c0fa-107">**SetRuleOperationType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9c0fa-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="9c0fa-108">Attributes and elements</span></span>

<span data-ttu-id="9c0fa-109">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="9c0fa-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9c0fa-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="9c0fa-110">Attributes</span></span>

<span data-ttu-id="9c0fa-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="9c0fa-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="9c0fa-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="9c0fa-112">Child elements</span></span>

|<span data-ttu-id="9c0fa-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="9c0fa-113">**Element**</span></span>|<span data-ttu-id="9c0fa-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9c0fa-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9c0fa-115">Regla (RuleType)</span><span class="sxs-lookup"><span data-stu-id="9c0fa-115">Rule (RuleType)</span></span>](rule-ruletype.md) <br/> |<span data-ttu-id="9c0fa-116">Representa una regla en el buzón del usuario.</span><span class="sxs-lookup"><span data-stu-id="9c0fa-116">Represents a rule in a user's mailbox.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="9c0fa-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="9c0fa-117">Parent elements</span></span>

|<span data-ttu-id="9c0fa-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="9c0fa-118">**Element**</span></span>|<span data-ttu-id="9c0fa-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9c0fa-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9c0fa-120">Operations</span><span class="sxs-lookup"><span data-stu-id="9c0fa-120">Operations</span></span>](operations.md) <br/> |<span data-ttu-id="9c0fa-121">Contiene una matriz de las operaciones de la regla que se puede realizar en una bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="9c0fa-121">Contains an array of rule operations that can be performed on an Inbox.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="9c0fa-122">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="9c0fa-122">Text value</span></span>

<span data-ttu-id="9c0fa-123">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="9c0fa-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9c0fa-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9c0fa-124">Remarks</span></span>

<span data-ttu-id="9c0fa-125">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="9c0fa-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9c0fa-126">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="9c0fa-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9c0fa-127">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="9c0fa-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="9c0fa-128">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="9c0fa-128">Schema Name</span></span>  <br/> |<span data-ttu-id="9c0fa-129">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="9c0fa-129">Types schema</span></span>  <br/> |
|<span data-ttu-id="9c0fa-130">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="9c0fa-130">Validation File</span></span>  <br/> |<span data-ttu-id="9c0fa-131">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="9c0fa-131">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="9c0fa-132">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="9c0fa-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="9c0fa-133">False</span><span class="sxs-lookup"><span data-stu-id="9c0fa-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9c0fa-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="9c0fa-134">See also</span></span>



[<span data-ttu-id="9c0fa-135">UpdateInboxRules</span><span class="sxs-lookup"><span data-stu-id="9c0fa-135">UpdateInboxRules</span></span>](updateinboxrules.md)
  
[<span data-ttu-id="9c0fa-136">DeleteRuleOperation</span><span class="sxs-lookup"><span data-stu-id="9c0fa-136">DeleteRuleOperation</span></span>](deleteruleoperation.md)
  
[<span data-ttu-id="9c0fa-137">CreateRuleOperation</span><span class="sxs-lookup"><span data-stu-id="9c0fa-137">CreateRuleOperation</span></span>](createruleoperation.md)


- [<span data-ttu-id="9c0fa-138">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="9c0fa-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

