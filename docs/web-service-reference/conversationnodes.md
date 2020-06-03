---
title: ConversationNodes
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5c8a35b8-a940-4b3e-8768-9ba95766fd79
description: El elemento ConversationNodes especifica una colección de nodos de conversación.
ms.openlocfilehash: 39ffb97f1004535e2fc70b58f8d56afe129e8ee2
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461397"
---
# <a name="conversationnodes"></a><span data-ttu-id="437c9-103">ConversationNodes</span><span class="sxs-lookup"><span data-stu-id="437c9-103">ConversationNodes</span></span>

<span data-ttu-id="437c9-104">El elemento **ConversationNodes** especifica una colección de nodos de conversación.</span><span class="sxs-lookup"><span data-stu-id="437c9-104">The **ConversationNodes** element specifies a collection of conversation nodes.</span></span> 
  
```XML
<ConversationNodes>
    <ConversationNode></ConversationNode>
</ConversationNodes>
```

 <span data-ttu-id="437c9-105">**ArrayOfConversationNodesType**</span><span class="sxs-lookup"><span data-stu-id="437c9-105">**ArrayOfConversationNodesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="437c9-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="437c9-106">Attributes and elements</span></span>

<span data-ttu-id="437c9-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="437c9-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="437c9-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="437c9-108">Attributes</span></span>

<span data-ttu-id="437c9-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="437c9-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="437c9-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="437c9-110">Child elements</span></span>

|<span data-ttu-id="437c9-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="437c9-111">**Element**</span></span>|<span data-ttu-id="437c9-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="437c9-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="437c9-113">ConversationNode</span><span class="sxs-lookup"><span data-stu-id="437c9-113">ConversationNode</span></span>](conversationnode.md) <br/> |<span data-ttu-id="437c9-114">Especifica un nodo de una conversación.</span><span class="sxs-lookup"><span data-stu-id="437c9-114">Specifies a node in a conversation.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="437c9-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="437c9-115">Parent elements</span></span>

|<span data-ttu-id="437c9-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="437c9-116">**Element**</span></span>|<span data-ttu-id="437c9-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="437c9-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="437c9-118">Conversación (ConversationResponseType)</span><span class="sxs-lookup"><span data-stu-id="437c9-118">Conversation (ConversationResponseType)</span></span>](conversation-conversationresponsetype.md) <br/> |<span data-ttu-id="437c9-119">Representa una única conversación devuelta en una respuesta **GetConversationItems** .</span><span class="sxs-lookup"><span data-stu-id="437c9-119">Represents a single conversation returned in a **GetConversationItems** response.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="437c9-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="437c9-120">Remarks</span></span>

<span data-ttu-id="437c9-121">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="437c9-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="437c9-122">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="437c9-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="437c9-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="437c9-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="437c9-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="437c9-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="437c9-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="437c9-125">Schema Name</span></span>  <br/> |<span data-ttu-id="437c9-126">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="437c9-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="437c9-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="437c9-127">Validation File</span></span>  <br/> |<span data-ttu-id="437c9-128">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="437c9-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="437c9-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="437c9-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="437c9-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="437c9-130">See also</span></span>



- [<span data-ttu-id="437c9-131">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="437c9-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

