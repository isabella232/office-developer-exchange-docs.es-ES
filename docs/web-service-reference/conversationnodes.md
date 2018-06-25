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
ms.openlocfilehash: 62ec061f6d03abb9db7e511722e5570e70d65772
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763888"
---
# <a name="conversationnodes"></a><span data-ttu-id="6b89a-103">ConversationNodes</span><span class="sxs-lookup"><span data-stu-id="6b89a-103">ConversationNodes</span></span>

<span data-ttu-id="6b89a-104">El elemento **ConversationNodes** especifica una colección de nodos de conversación.</span><span class="sxs-lookup"><span data-stu-id="6b89a-104">The **ConversationNodes** element specifies a collection of conversation nodes.</span></span> 
  
```XML
<ConversationNodes>
    <ConversationNode></ConversationNode>
</ConversationNodes>
```

 <span data-ttu-id="6b89a-105">**ArrayOfConversationNodesType**</span><span class="sxs-lookup"><span data-stu-id="6b89a-105">**ArrayOfConversationNodesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6b89a-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="6b89a-106">Attributes and elements</span></span>

<span data-ttu-id="6b89a-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="6b89a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6b89a-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="6b89a-108">Attributes</span></span>

<span data-ttu-id="6b89a-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="6b89a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6b89a-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="6b89a-110">Child elements</span></span>

|<span data-ttu-id="6b89a-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="6b89a-111">**Element**</span></span>|<span data-ttu-id="6b89a-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6b89a-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6b89a-113">ConversationNode</span><span class="sxs-lookup"><span data-stu-id="6b89a-113">ConversationNode</span></span>](conversationnode.md) <br/> |<span data-ttu-id="6b89a-114">Especifica un nodo en una conversación.</span><span class="sxs-lookup"><span data-stu-id="6b89a-114">Specifies a node in a conversation.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="6b89a-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="6b89a-115">Parent elements</span></span>

|<span data-ttu-id="6b89a-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="6b89a-116">**Element**</span></span>|<span data-ttu-id="6b89a-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6b89a-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6b89a-118">Conversación (ConversationResponseType)</span><span class="sxs-lookup"><span data-stu-id="6b89a-118">Conversation (ConversationResponseType)</span></span>](conversation-conversationresponsetype.md) <br/> |<span data-ttu-id="6b89a-119">Representa una sola conversación devuelta en una respuesta de **GetConversationItems** .</span><span class="sxs-lookup"><span data-stu-id="6b89a-119">Represents a single conversation returned in a **GetConversationItems** response.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6b89a-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6b89a-120">Remarks</span></span>

<span data-ttu-id="6b89a-121">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6b89a-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="6b89a-122">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="6b89a-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6b89a-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="6b89a-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6b89a-124">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="6b89a-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="6b89a-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="6b89a-125">Schema Name</span></span>  <br/> |<span data-ttu-id="6b89a-126">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="6b89a-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="6b89a-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="6b89a-127">Validation File</span></span>  <br/> |<span data-ttu-id="6b89a-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="6b89a-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="6b89a-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="6b89a-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="6b89a-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="6b89a-130">See also</span></span>



- [<span data-ttu-id="6b89a-131">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="6b89a-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

