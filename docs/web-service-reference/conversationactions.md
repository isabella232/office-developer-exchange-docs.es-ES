---
title: ConversationActions
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ConversationActions
api_type:
- schema
ms.assetid: 3d6c663d-4bd9-4eec-b95a-cd683f592672
description: El elemento ConversationActions contiene una colección de las conversaciones y las acciones que se debe aplicar a ellos.
ms.openlocfilehash: 3dff7ff66f758f1cd2eb3cd7b8126294d2799fc0
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763873"
---
# <a name="conversationactions"></a><span data-ttu-id="9da20-103">ConversationActions</span><span class="sxs-lookup"><span data-stu-id="9da20-103">ConversationActions</span></span>

<span data-ttu-id="9da20-104">El elemento **ConversationActions** contiene una colección de las conversaciones y las acciones que se debe aplicar a ellos.</span><span class="sxs-lookup"><span data-stu-id="9da20-104">The **ConversationActions** element contains a collection of conversations and the actions to apply to them.</span></span> 
  
[<span data-ttu-id="9da20-105">ApplyConversationAction</span><span class="sxs-lookup"><span data-stu-id="9da20-105">ApplyConversationAction</span></span>](applyconversationaction.md)
  
[<span data-ttu-id="9da20-106">ConversationActions</span><span class="sxs-lookup"><span data-stu-id="9da20-106">ConversationActions</span></span>](conversationactions.md)
  
```XML
<ConversationActions>
   <ConversationAction/>
</ConversationActions>
```

 <span data-ttu-id="9da20-107">**NonEmptyArrayOfApplyConversationActionType**</span><span class="sxs-lookup"><span data-stu-id="9da20-107">**NonEmptyArrayOfApplyConversationActionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9da20-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="9da20-108">Attributes and elements</span></span>

<span data-ttu-id="9da20-109">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="9da20-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9da20-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="9da20-110">Attributes</span></span>

<span data-ttu-id="9da20-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="9da20-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="9da20-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="9da20-112">Child elements</span></span>

|<span data-ttu-id="9da20-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="9da20-113">**Element**</span></span>|<span data-ttu-id="9da20-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9da20-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9da20-115">ConversationAction</span><span class="sxs-lookup"><span data-stu-id="9da20-115">ConversationAction</span></span>](conversationaction.md) <br/> |<span data-ttu-id="9da20-116">Contiene una única acción que se aplicará a una conversación único.</span><span class="sxs-lookup"><span data-stu-id="9da20-116">Contains a single action to be applied to a single conversation.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="9da20-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="9da20-117">Parent elements</span></span>

|<span data-ttu-id="9da20-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="9da20-118">**Element**</span></span>|<span data-ttu-id="9da20-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9da20-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9da20-120">ApplyConversationAction</span><span class="sxs-lookup"><span data-stu-id="9da20-120">ApplyConversationAction</span></span>](applyconversationaction.md) <br/> |<span data-ttu-id="9da20-121">Define una solicitud para aplicar acciones a los elementos en una conversación.</span><span class="sxs-lookup"><span data-stu-id="9da20-121">Defines a request to apply actions to items in a conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="9da20-122">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="9da20-122">Text value</span></span>

<span data-ttu-id="9da20-123">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="9da20-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9da20-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9da20-124">Remarks</span></span>

<span data-ttu-id="9da20-125">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda Exchange Web Services.This elemento fue introdujo en Exchange Server 2010 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="9da20-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9da20-126">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="9da20-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9da20-127">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="9da20-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="9da20-128">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="9da20-128">Schema Name</span></span>  <br/> |<span data-ttu-id="9da20-129">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="9da20-129">Messages schema</span></span>  <br/> |
|<span data-ttu-id="9da20-130">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="9da20-130">Validation File</span></span>  <br/> |<span data-ttu-id="9da20-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="9da20-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="9da20-132">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="9da20-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="9da20-133">False</span><span class="sxs-lookup"><span data-stu-id="9da20-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9da20-134">Ver también</span><span class="sxs-lookup"><span data-stu-id="9da20-134">See also</span></span>



[<span data-ttu-id="9da20-135">Operación ApplyConversationAction</span><span class="sxs-lookup"><span data-stu-id="9da20-135">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)

