---
title: Regla (RuleType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Rule
api_type:
- schema
ms.assetid: 259a1f62-b235-4964-88bf-2d1f1c05a563
description: El elemento rule contiene una sola regla y representa una regla en el buzón de un usuario.
ms.openlocfilehash: cdbd21df235a62a9e201e1eaae1d82a8ac10cdd2
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465082"
---
# <a name="rule-ruletype"></a><span data-ttu-id="6ac09-103">Regla (RuleType)</span><span class="sxs-lookup"><span data-stu-id="6ac09-103">Rule (RuleType)</span></span>

<span data-ttu-id="6ac09-104">El elemento **Rule** contiene una sola regla y representa una regla en el buzón de un usuario.</span><span class="sxs-lookup"><span data-stu-id="6ac09-104">The **Rule** element contains a single rule and represents a rule in a user's mailbox.</span></span> 
  
```XML
<Rule>
    <RuleId>
    <DisplayName>
    <Priority>
    <IsEnabled>
    <IsNotSupported>
    <IsInError>
    <Conditions>
    <Exceptions>
    <Actions>
</Rule>
```

 <span data-ttu-id="6ac09-105">**RuleType**</span><span class="sxs-lookup"><span data-stu-id="6ac09-105">**RuleType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6ac09-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="6ac09-106">Attributes and elements</span></span>

<span data-ttu-id="6ac09-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="6ac09-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6ac09-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="6ac09-108">Attributes</span></span>

<span data-ttu-id="6ac09-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="6ac09-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6ac09-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="6ac09-110">Child elements</span></span>

|<span data-ttu-id="6ac09-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="6ac09-111">**Element**</span></span>|<span data-ttu-id="6ac09-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6ac09-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6ac09-113">RuleId</span><span class="sxs-lookup"><span data-stu-id="6ac09-113">RuleId</span></span>](ruleid.md) <br/> |<span data-ttu-id="6ac09-114">Especifica el identificador de la regla.</span><span class="sxs-lookup"><span data-stu-id="6ac09-114">Specifies the rule identifier.</span></span>  <br/> |
|[<span data-ttu-id="6ac09-115">DisplayName (cadena)</span><span class="sxs-lookup"><span data-stu-id="6ac09-115">DisplayName (string)</span></span>](displayname-string.md) <br/> |<span data-ttu-id="6ac09-116">Contiene el nombre para mostrar de una regla.</span><span class="sxs-lookup"><span data-stu-id="6ac09-116">Contains the display name of a rule.</span></span>  <br/> |
|[<span data-ttu-id="6ac09-117">Prioridad</span><span class="sxs-lookup"><span data-stu-id="6ac09-117">Priority</span></span>](priority.md) <br/> |<span data-ttu-id="6ac09-118">Indica el orden en que se ejecutará una regla.</span><span class="sxs-lookup"><span data-stu-id="6ac09-118">Indicates the order in which a rule is to be run.</span></span>  <br/> |
|[<span data-ttu-id="6ac09-119">IsEnabled</span><span class="sxs-lookup"><span data-stu-id="6ac09-119">IsEnabled</span></span>](isenabled.md) <br/> |<span data-ttu-id="6ac09-120">Indica si la regla está habilitada.</span><span class="sxs-lookup"><span data-stu-id="6ac09-120">Indicates whether the rule is enabled.</span></span>  <br/> |
|[<span data-ttu-id="6ac09-121">IsNotSupported</span><span class="sxs-lookup"><span data-stu-id="6ac09-121">IsNotSupported</span></span>](isnotsupported.md) <br/> |<span data-ttu-id="6ac09-122">Indica si la regla no se puede modificar con las API de código administrado.</span><span class="sxs-lookup"><span data-stu-id="6ac09-122">Indicates whether the rule cannot be modified with the managed code APIs.</span></span>  <br/> |
|[<span data-ttu-id="6ac09-123">IsInError</span><span class="sxs-lookup"><span data-stu-id="6ac09-123">IsInError</span></span>](isinerror.md) <br/> |<span data-ttu-id="6ac09-124">Indica si la regla es una condición de error.</span><span class="sxs-lookup"><span data-stu-id="6ac09-124">Indicates whether the rule is in an error condition.</span></span>  <br/> |
|[<span data-ttu-id="6ac09-125">Condiciones</span><span class="sxs-lookup"><span data-stu-id="6ac09-125">Conditions</span></span>](conditions.md) <br/> |<span data-ttu-id="6ac09-126">Identifica las condiciones que, cuando se cumplan, desencadenarán las acciones de regla de una regla.</span><span class="sxs-lookup"><span data-stu-id="6ac09-126">Identifies the conditions that, when fulfilled, will trigger the rule actions for a rule.</span></span>  <br/> |
|[<span data-ttu-id="6ac09-127">Excepciones</span><span class="sxs-lookup"><span data-stu-id="6ac09-127">Exceptions</span></span>](exceptions.md) <br/> |<span data-ttu-id="6ac09-128">Identifica las excepciones que representan todas las condiciones de excepción de regla disponibles para la regla de bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="6ac09-128">Identifies the exceptions that represent all the available rule exception conditions for the inbox rule.</span></span>  <br/> |
|[<span data-ttu-id="6ac09-129">Actions</span><span class="sxs-lookup"><span data-stu-id="6ac09-129">Actions</span></span>](actions.md) <br/> |<span data-ttu-id="6ac09-130">Representa las acciones que se van a realizar en un mensaje cuando se cumplan las condiciones.</span><span class="sxs-lookup"><span data-stu-id="6ac09-130">Represents the actions to be taken on a message when the conditions are fulfilled.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="6ac09-131">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="6ac09-131">Parent elements</span></span>

|<span data-ttu-id="6ac09-132">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="6ac09-132">**Element**</span></span>|<span data-ttu-id="6ac09-133">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6ac09-133">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6ac09-134">CreateRuleOperation</span><span class="sxs-lookup"><span data-stu-id="6ac09-134">CreateRuleOperation</span></span>](createruleoperation.md) <br/> |<span data-ttu-id="6ac09-135">Representa una operación para crear una nueva regla.</span><span class="sxs-lookup"><span data-stu-id="6ac09-135">Represents an operation to create a new rule.</span></span>  <br/> |
|[<span data-ttu-id="6ac09-136">InboxRules</span><span class="sxs-lookup"><span data-stu-id="6ac09-136">InboxRules</span></span>](inboxrules.md) <br/> |<span data-ttu-id="6ac09-137">Representa una matriz de reglas en el buzón de correo del usuario.</span><span class="sxs-lookup"><span data-stu-id="6ac09-137">Represents an array of rules in the user's mailbox.</span></span>  <br/> |
|[<span data-ttu-id="6ac09-138">SetRuleOperation</span><span class="sxs-lookup"><span data-stu-id="6ac09-138">SetRuleOperation</span></span>](setruleoperation.md) <br/> |<span data-ttu-id="6ac09-139">Representa una operación para actualizar una regla existente.</span><span class="sxs-lookup"><span data-stu-id="6ac09-139">Represents an operation to update an existing rule.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="6ac09-140">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="6ac09-140">Text value</span></span>

<span data-ttu-id="6ac09-141">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="6ac09-141">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6ac09-142">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6ac09-142">Remarks</span></span>

<span data-ttu-id="6ac09-143">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="6ac09-143">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6ac09-144">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="6ac09-144">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6ac09-145">Namespace</span><span class="sxs-lookup"><span data-stu-id="6ac09-145">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="6ac09-146">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="6ac09-146">Schema Name</span></span>  <br/> |<span data-ttu-id="6ac09-147">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="6ac09-147">Types schema</span></span>  <br/> |
|<span data-ttu-id="6ac09-148">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="6ac09-148">Validation File</span></span>  <br/> |<span data-ttu-id="6ac09-149">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="6ac09-149">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="6ac09-150">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="6ac09-150">Can be Empty</span></span>  <br/> |<span data-ttu-id="6ac09-151">Verdadero</span><span class="sxs-lookup"><span data-stu-id="6ac09-151">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6ac09-152">Vea también</span><span class="sxs-lookup"><span data-stu-id="6ac09-152">See also</span></span>



[<span data-ttu-id="6ac09-153">UpdateInboxRules</span><span class="sxs-lookup"><span data-stu-id="6ac09-153">UpdateInboxRules</span></span>](updateinboxrules.md)
  
[<span data-ttu-id="6ac09-154">SetRuleOperation</span><span class="sxs-lookup"><span data-stu-id="6ac09-154">SetRuleOperation</span></span>](setruleoperation.md)
  
[<span data-ttu-id="6ac09-155">CreateRuleOperation</span><span class="sxs-lookup"><span data-stu-id="6ac09-155">CreateRuleOperation</span></span>](createruleoperation.md)


- [<span data-ttu-id="6ac09-156">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="6ac09-156">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

