---
title: InboxRules
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- InboxRules
api_type:
- schema
ms.assetid: 7bb9896c-bd12-49ae-842a-a10b5f9a2ef6
description: El elemento InboxRules representa una matriz de reglas en el buzón de correo del usuario.
ms.openlocfilehash: a3107c3c317a912d0bd3e60d03da4168f2f3a0a9
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458274"
---
# <a name="inboxrules"></a><span data-ttu-id="c1a60-103">InboxRules</span><span class="sxs-lookup"><span data-stu-id="c1a60-103">InboxRules</span></span>

<span data-ttu-id="c1a60-104">El elemento **InboxRules** representa una matriz de reglas en el buzón de correo del usuario.</span><span class="sxs-lookup"><span data-stu-id="c1a60-104">The **InboxRules** element represents an array of rules in the user's mailbox.</span></span> 
  
[<span data-ttu-id="c1a60-105">GetInboxRulesResponse</span><span class="sxs-lookup"><span data-stu-id="c1a60-105">GetInboxRulesResponse</span></span>](getinboxrulesresponse.md)
  
[<span data-ttu-id="c1a60-106">InboxRules</span><span class="sxs-lookup"><span data-stu-id="c1a60-106">InboxRules</span></span>](inboxrules.md)
  
```XML
<InboxRules>
   <Rule/>
</InboxRules>
```

 <span data-ttu-id="c1a60-107">**ArrayOfRulesType**</span><span class="sxs-lookup"><span data-stu-id="c1a60-107">**ArrayOfRulesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c1a60-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="c1a60-108">Attributes and elements</span></span>

<span data-ttu-id="c1a60-109">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="c1a60-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c1a60-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="c1a60-110">Attributes</span></span>

<span data-ttu-id="c1a60-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="c1a60-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c1a60-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c1a60-112">Child elements</span></span>

|<span data-ttu-id="c1a60-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="c1a60-113">**Element**</span></span>|<span data-ttu-id="c1a60-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c1a60-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c1a60-115">Regla (RuleType)</span><span class="sxs-lookup"><span data-stu-id="c1a60-115">Rule (RuleType)</span></span>](rule-ruletype.md) <br/> |<span data-ttu-id="c1a60-116">Contiene una sola regla y representa una regla en el buzón de correo del usuario.</span><span class="sxs-lookup"><span data-stu-id="c1a60-116">Contains a single rule and represents a rule in the user's mailbox.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="c1a60-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="c1a60-117">Parent elements</span></span>

|<span data-ttu-id="c1a60-118">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="c1a60-118">**Element**</span></span>|<span data-ttu-id="c1a60-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c1a60-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c1a60-120">GetInboxRulesResponse</span><span class="sxs-lookup"><span data-stu-id="c1a60-120">GetInboxRulesResponse</span></span>](getinboxrulesresponse.md) <br/> |<span data-ttu-id="c1a60-121">Define una respuesta a una solicitud de [operación de GetInboxRules](getinboxrules-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="c1a60-121">Defines a response to a [GetInboxRules operation](getinboxrules-operation.md) request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="c1a60-122">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="c1a60-122">Text value</span></span>

<span data-ttu-id="c1a60-123">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="c1a60-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c1a60-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c1a60-124">Remarks</span></span>

<span data-ttu-id="c1a60-125">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="c1a60-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c1a60-126">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="c1a60-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c1a60-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="c1a60-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="c1a60-128">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="c1a60-128">Schema Name</span></span>  <br/> |<span data-ttu-id="c1a60-129">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="c1a60-129">Messages schema</span></span>  <br/> |
|<span data-ttu-id="c1a60-130">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="c1a60-130">Validation File</span></span>  <br/> |<span data-ttu-id="c1a60-131">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="c1a60-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="c1a60-132">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="c1a60-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="c1a60-133">Verdadero</span><span class="sxs-lookup"><span data-stu-id="c1a60-133">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c1a60-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="c1a60-134">See also</span></span>



[<span data-ttu-id="c1a60-135">GetInboxRules</span><span class="sxs-lookup"><span data-stu-id="c1a60-135">GetInboxRules</span></span>](getinboxrules.md)
  
[<span data-ttu-id="c1a60-136">Operación de GetInboxRules</span><span class="sxs-lookup"><span data-stu-id="c1a60-136">GetInboxRules operation</span></span>](getinboxrules-operation.md)


- [<span data-ttu-id="c1a60-137">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="c1a60-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

