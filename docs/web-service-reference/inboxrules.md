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
description: El elemento InboxRules representa una matriz de las reglas en el buzón del usuario.
ms.openlocfilehash: 47fcad5dde06f3af9fbae7e70adbfd8b225081c2
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19835899"
---
# <a name="inboxrules"></a><span data-ttu-id="3a3a4-103">InboxRules</span><span class="sxs-lookup"><span data-stu-id="3a3a4-103">InboxRules</span></span>

<span data-ttu-id="3a3a4-104">El elemento **InboxRules** representa una matriz de las reglas en el buzón del usuario.</span><span class="sxs-lookup"><span data-stu-id="3a3a4-104">The **InboxRules** element represents an array of rules in the user's mailbox.</span></span> 
  
[<span data-ttu-id="3a3a4-105">GetInboxRulesResponse</span><span class="sxs-lookup"><span data-stu-id="3a3a4-105">GetInboxRulesResponse</span></span>](getinboxrulesresponse.md)
  
[<span data-ttu-id="3a3a4-106">InboxRules</span><span class="sxs-lookup"><span data-stu-id="3a3a4-106">InboxRules</span></span>](inboxrules.md)
  
```XML
<InboxRules>
   <Rule/>
</InboxRules>
```

 <span data-ttu-id="3a3a4-107">**ArrayOfRulesType**</span><span class="sxs-lookup"><span data-stu-id="3a3a4-107">**ArrayOfRulesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3a3a4-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="3a3a4-108">Attributes and elements</span></span>

<span data-ttu-id="3a3a4-109">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="3a3a4-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3a3a4-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="3a3a4-110">Attributes</span></span>

<span data-ttu-id="3a3a4-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="3a3a4-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3a3a4-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="3a3a4-112">Child elements</span></span>

|<span data-ttu-id="3a3a4-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="3a3a4-113">**Element**</span></span>|<span data-ttu-id="3a3a4-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3a3a4-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3a3a4-115">Regla (RuleType)</span><span class="sxs-lookup"><span data-stu-id="3a3a4-115">Rule (RuleType)</span></span>](rule-ruletype.md) <br/> |<span data-ttu-id="3a3a4-116">Contiene una sola regla y representa una regla en el buzón del usuario.</span><span class="sxs-lookup"><span data-stu-id="3a3a4-116">Contains a single rule and represents a rule in the user's mailbox.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="3a3a4-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="3a3a4-117">Parent elements</span></span>

|<span data-ttu-id="3a3a4-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="3a3a4-118">**Element**</span></span>|<span data-ttu-id="3a3a4-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3a3a4-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3a3a4-120">GetInboxRulesResponse</span><span class="sxs-lookup"><span data-stu-id="3a3a4-120">GetInboxRulesResponse</span></span>](getinboxrulesresponse.md) <br/> |<span data-ttu-id="3a3a4-121">Define una respuesta a una solicitud de [operación GetInboxRules](getinboxrules-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="3a3a4-121">Defines a response to a [GetInboxRules operation](getinboxrules-operation.md) request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="3a3a4-122">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="3a3a4-122">Text value</span></span>

<span data-ttu-id="3a3a4-123">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="3a3a4-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3a3a4-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3a3a4-124">Remarks</span></span>

<span data-ttu-id="3a3a4-125">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="3a3a4-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3a3a4-126">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="3a3a4-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3a3a4-127">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3a3a4-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="3a3a4-128">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="3a3a4-128">Schema Name</span></span>  <br/> |<span data-ttu-id="3a3a4-129">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="3a3a4-129">Messages schema</span></span>  <br/> |
|<span data-ttu-id="3a3a4-130">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="3a3a4-130">Validation File</span></span>  <br/> |<span data-ttu-id="3a3a4-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="3a3a4-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="3a3a4-132">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="3a3a4-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="3a3a4-133">Verdadero</span><span class="sxs-lookup"><span data-stu-id="3a3a4-133">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3a3a4-134">Ver también</span><span class="sxs-lookup"><span data-stu-id="3a3a4-134">See also</span></span>



[<span data-ttu-id="3a3a4-135">GetInboxRules</span><span class="sxs-lookup"><span data-stu-id="3a3a4-135">GetInboxRules</span></span>](getinboxrules.md)
  
[<span data-ttu-id="3a3a4-136">Operación de GetInboxRules</span><span class="sxs-lookup"><span data-stu-id="3a3a4-136">GetInboxRules operation</span></span>](getinboxrules-operation.md)


- [<span data-ttu-id="3a3a4-137">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="3a3a4-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
