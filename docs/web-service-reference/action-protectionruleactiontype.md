---
title: Acción (ProtectionRuleActionType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Action
api_type:
- schema
ms.assetid: ca090dec-e2c5-49c8-a057-8d1f2409147f
description: El elemento Action identifica qué acción debe ejecutarse si la parte de condición de la regla coincide.
ms.openlocfilehash: 220a6fea16abb9ea823ae6239537b8c121702589
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44527512"
---
# <a name="action-protectionruleactiontype"></a><span data-ttu-id="6000c-103">Acción (ProtectionRuleActionType)</span><span class="sxs-lookup"><span data-stu-id="6000c-103">Action (ProtectionRuleActionType)</span></span>

<span data-ttu-id="6000c-104">El elemento **Action** identifica qué acción debe ejecutarse si la parte de condición de la regla coincide.</span><span class="sxs-lookup"><span data-stu-id="6000c-104">The **Action** element identifies what action must be executed if the condition part of the rule matches.</span></span> 
  
```xml
<Action Name="">
   <Argument/>
</Action>

```

 <span data-ttu-id="6000c-105">**ProtectionRuleActionType**</span><span class="sxs-lookup"><span data-stu-id="6000c-105">**ProtectionRuleActionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6000c-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="6000c-106">Attributes and elements</span></span>

<span data-ttu-id="6000c-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="6000c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6000c-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="6000c-108">Attributes</span></span>

|<span data-ttu-id="6000c-109">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="6000c-109">**Attribute**</span></span>|<span data-ttu-id="6000c-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6000c-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6000c-111">**Name**</span><span class="sxs-lookup"><span data-stu-id="6000c-111">**Name**</span></span> <br/> |<span data-ttu-id="6000c-112">Identifica el nombre de la acción.</span><span class="sxs-lookup"><span data-stu-id="6000c-112">Identifies the name of the action.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="6000c-113">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="6000c-113">Child elements</span></span>

|<span data-ttu-id="6000c-114">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="6000c-114">**Element**</span></span>|<span data-ttu-id="6000c-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6000c-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6000c-116">Argumento</span><span class="sxs-lookup"><span data-stu-id="6000c-116">Argument</span></span>](argument.md) <br/> |<span data-ttu-id="6000c-117">Especifica los argumentos de la acción.</span><span class="sxs-lookup"><span data-stu-id="6000c-117">Specifies arguments to the action.</span></span> <span data-ttu-id="6000c-118">Este elemento no se producirá si la acción especificada no requiere que se especifiquen argumentos.</span><span class="sxs-lookup"><span data-stu-id="6000c-118">This element will not occur if the specified action does not require arguments to be specified.</span></span> <span data-ttu-id="6000c-119">Este elemento puede producirse una o varias veces si una acción requiere uno o más argumentos.</span><span class="sxs-lookup"><span data-stu-id="6000c-119">This element can occur one or more times if an action requires one or more arguments.</span></span> <span data-ttu-id="6000c-120">La acción **RightsProtectMessage** contendrá un solo argumento.</span><span class="sxs-lookup"><span data-stu-id="6000c-120">The **RightsProtectMessage** action will contain a single argument.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="6000c-121">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="6000c-121">Parent elements</span></span>

|<span data-ttu-id="6000c-122">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="6000c-122">**Element**</span></span>|<span data-ttu-id="6000c-123">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6000c-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6000c-124">Rule</span><span class="sxs-lookup"><span data-stu-id="6000c-124">Rule</span></span>](rule.md) <br/> |<span data-ttu-id="6000c-125">Contiene una regla de protección única.</span><span class="sxs-lookup"><span data-stu-id="6000c-125">Contains a single protection rule.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6000c-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6000c-126">Remarks</span></span>

<span data-ttu-id="6000c-127">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="6000c-127">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6000c-128">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="6000c-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6000c-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="6000c-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="6000c-130">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="6000c-130">Schema Name</span></span>  <br/> |<span data-ttu-id="6000c-131">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="6000c-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="6000c-132">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="6000c-132">Validation File</span></span>  <br/> |<span data-ttu-id="6000c-133">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="6000c-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="6000c-134">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="6000c-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="6000c-135">Falso</span><span class="sxs-lookup"><span data-stu-id="6000c-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6000c-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="6000c-136">See also</span></span>

- [<span data-ttu-id="6000c-137">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="6000c-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

