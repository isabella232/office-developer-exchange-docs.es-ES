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
description: El elemento ConversationActions contiene una colección de conversaciones y las acciones que se aplican a ellas.
ms.openlocfilehash: 2db84f78b4b8c92e0a6ef7d69fba7c778fb5f96d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44527106"
---
# <a name="conversationactions"></a><span data-ttu-id="cd9ab-103">ConversationActions</span><span class="sxs-lookup"><span data-stu-id="cd9ab-103">ConversationActions</span></span>

<span data-ttu-id="cd9ab-104">El elemento **ConversationActions** contiene una colección de conversaciones y las acciones que se aplican a ellas.</span><span class="sxs-lookup"><span data-stu-id="cd9ab-104">The **ConversationActions** element contains a collection of conversations and the actions to apply to them.</span></span> 
  
[<span data-ttu-id="cd9ab-105">ApplyConversationAction</span><span class="sxs-lookup"><span data-stu-id="cd9ab-105">ApplyConversationAction</span></span>](applyconversationaction.md)
  
[<span data-ttu-id="cd9ab-106">ConversationActions</span><span class="sxs-lookup"><span data-stu-id="cd9ab-106">ConversationActions</span></span>](conversationactions.md)
  
```XML
<ConversationActions>
   <ConversationAction/>
</ConversationActions>
```

 <span data-ttu-id="cd9ab-107">**NonEmptyArrayOfApplyConversationActionType**</span><span class="sxs-lookup"><span data-stu-id="cd9ab-107">**NonEmptyArrayOfApplyConversationActionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="cd9ab-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="cd9ab-108">Attributes and elements</span></span>

<span data-ttu-id="cd9ab-109">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="cd9ab-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cd9ab-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="cd9ab-110">Attributes</span></span>

<span data-ttu-id="cd9ab-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="cd9ab-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="cd9ab-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="cd9ab-112">Child elements</span></span>

|<span data-ttu-id="cd9ab-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="cd9ab-113">**Element**</span></span>|<span data-ttu-id="cd9ab-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="cd9ab-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cd9ab-115">ConversationAction</span><span class="sxs-lookup"><span data-stu-id="cd9ab-115">ConversationAction</span></span>](conversationaction.md) <br/> |<span data-ttu-id="cd9ab-116">Contiene una sola acción que se aplicará a una única conversación.</span><span class="sxs-lookup"><span data-stu-id="cd9ab-116">Contains a single action to be applied to a single conversation.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="cd9ab-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="cd9ab-117">Parent elements</span></span>

|<span data-ttu-id="cd9ab-118">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="cd9ab-118">**Element**</span></span>|<span data-ttu-id="cd9ab-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="cd9ab-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cd9ab-120">ApplyConversationAction</span><span class="sxs-lookup"><span data-stu-id="cd9ab-120">ApplyConversationAction</span></span>](applyconversationaction.md) <br/> |<span data-ttu-id="cd9ab-121">Define una solicitud para aplicar acciones a los elementos de una conversación.</span><span class="sxs-lookup"><span data-stu-id="cd9ab-121">Defines a request to apply actions to items in a conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="cd9ab-122">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="cd9ab-122">Text value</span></span>

<span data-ttu-id="cd9ab-123">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="cd9ab-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="cd9ab-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="cd9ab-124">Remarks</span></span>

<span data-ttu-id="cd9ab-125">El esquema que describe este elemento se encuentra en el directorio virtual de IIS que hospeda los servicios Web de Exchange. este elemento se introdujo en Exchange Server 2010 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="cd9ab-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="cd9ab-126">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="cd9ab-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cd9ab-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="cd9ab-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="cd9ab-128">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="cd9ab-128">Schema Name</span></span>  <br/> |<span data-ttu-id="cd9ab-129">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="cd9ab-129">Messages schema</span></span>  <br/> |
|<span data-ttu-id="cd9ab-130">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="cd9ab-130">Validation File</span></span>  <br/> |<span data-ttu-id="cd9ab-131">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="cd9ab-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="cd9ab-132">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="cd9ab-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="cd9ab-133">Falso</span><span class="sxs-lookup"><span data-stu-id="cd9ab-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cd9ab-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="cd9ab-134">See also</span></span>



[<span data-ttu-id="cd9ab-135">Operación ApplyConversationAction</span><span class="sxs-lookup"><span data-stu-id="cd9ab-135">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)

