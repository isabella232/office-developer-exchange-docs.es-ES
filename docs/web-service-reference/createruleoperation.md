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
ms.openlocfilehash: df857544e6d5840a3f738740114195e4c4bb5798
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460774"
---
# <a name="createruleoperation"></a><span data-ttu-id="daa94-103">CreateRuleOperation</span><span class="sxs-lookup"><span data-stu-id="daa94-103">CreateRuleOperation</span></span>

<span data-ttu-id="daa94-104">El elemento **CreateRuleOperation** representa una operación para crear una nueva regla de bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="daa94-104">The **CreateRuleOperation** element represents an operation to create a new Inbox rule.</span></span> 
  
[<span data-ttu-id="daa94-105">UpdateInboxRules</span><span class="sxs-lookup"><span data-stu-id="daa94-105">UpdateInboxRules</span></span>](updateinboxrules.md)
  
[<span data-ttu-id="daa94-106">Operations</span><span class="sxs-lookup"><span data-stu-id="daa94-106">Operations</span></span>](operations.md)
  
```xml
<CreateRuleOperation>
    <Rule/>
</CreateRuleOperation>
```

 <span data-ttu-id="daa94-107">**CreateRuleOperationType**</span><span class="sxs-lookup"><span data-stu-id="daa94-107">**CreateRuleOperationType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="daa94-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="daa94-108">Attributes and elements</span></span>

<span data-ttu-id="daa94-109">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="daa94-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="daa94-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="daa94-110">Attributes</span></span>

<span data-ttu-id="daa94-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="daa94-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="daa94-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="daa94-112">Child elements</span></span>

|<span data-ttu-id="daa94-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="daa94-113">**Element**</span></span>|<span data-ttu-id="daa94-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="daa94-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="daa94-115">Regla (RuleType)</span><span class="sxs-lookup"><span data-stu-id="daa94-115">Rule (RuleType)</span></span>](rule-ruletype.md) <br/> |<span data-ttu-id="daa94-116">Representa una regla que se va a crear en el buzón de un usuario.</span><span class="sxs-lookup"><span data-stu-id="daa94-116">Represents a rule to be created in a user's mailbox.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="daa94-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="daa94-117">Parent elements</span></span>

|<span data-ttu-id="daa94-118">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="daa94-118">**Element**</span></span>|<span data-ttu-id="daa94-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="daa94-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="daa94-120">Operations</span><span class="sxs-lookup"><span data-stu-id="daa94-120">Operations</span></span>](operations.md) <br/> |<span data-ttu-id="daa94-121">Contiene las operaciones que se pueden realizar en una bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="daa94-121">Contains the operations that can be performed on an Inbox.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="daa94-122">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="daa94-122">Text value</span></span>

<span data-ttu-id="daa94-123">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="daa94-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="daa94-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="daa94-124">Remarks</span></span>

<span data-ttu-id="daa94-125">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="daa94-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="daa94-126">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="daa94-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="daa94-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="daa94-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="daa94-128">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="daa94-128">Schema Name</span></span>  <br/> |<span data-ttu-id="daa94-129">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="daa94-129">Types schema</span></span>  <br/> |
|<span data-ttu-id="daa94-130">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="daa94-130">Validation File</span></span>  <br/> |<span data-ttu-id="daa94-131">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="daa94-131">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="daa94-132">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="daa94-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="daa94-133">Falso</span><span class="sxs-lookup"><span data-stu-id="daa94-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="daa94-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="daa94-134">See also</span></span>



[<span data-ttu-id="daa94-135">UpdateInboxRules</span><span class="sxs-lookup"><span data-stu-id="daa94-135">UpdateInboxRules</span></span>](updateinboxrules.md)
  
[<span data-ttu-id="daa94-136">SetRuleOperation</span><span class="sxs-lookup"><span data-stu-id="daa94-136">SetRuleOperation</span></span>](setruleoperation.md)
  
[<span data-ttu-id="daa94-137">DeleteRuleOperation</span><span class="sxs-lookup"><span data-stu-id="daa94-137">DeleteRuleOperation</span></span>](deleteruleoperation.md)


- [<span data-ttu-id="daa94-138">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="daa94-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

