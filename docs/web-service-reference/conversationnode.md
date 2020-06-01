---
title: ConversationNode
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b7f7acd3-ed65-441e-9976-8b4ed5f12c0b
description: El elemento ConversationNode especifica un nodo en una conversación.
ms.openlocfilehash: 074209c1b5669db8dd1ea4ba7f9dea064628afbd
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462706"
---
# <a name="conversationnode"></a><span data-ttu-id="ef436-103">ConversationNode</span><span class="sxs-lookup"><span data-stu-id="ef436-103">ConversationNode</span></span>

<span data-ttu-id="ef436-104">El elemento **ConversationNode** especifica un nodo en una conversación.</span><span class="sxs-lookup"><span data-stu-id="ef436-104">The **ConversationNode** element specifies a node in a conversation.</span></span> 
  
```XML
<ConversationNode>
    <InternetMessageId></InternetMessageId>
    <ParentInternetMessageId></ParentInternetMessageId>
    <Items></Items>
</ConversationNode>
```

 <span data-ttu-id="ef436-105">**ConversationNodeType**</span><span class="sxs-lookup"><span data-stu-id="ef436-105">**ConversationNodeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ef436-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="ef436-106">Attributes and elements</span></span>

<span data-ttu-id="ef436-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="ef436-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ef436-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="ef436-108">Attributes</span></span>

<span data-ttu-id="ef436-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="ef436-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ef436-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ef436-110">Child elements</span></span>

|<span data-ttu-id="ef436-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="ef436-111">**Element**</span></span>|<span data-ttu-id="ef436-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ef436-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ef436-113">InternetMessageId</span><span class="sxs-lookup"><span data-stu-id="ef436-113">InternetMessageId</span></span>](internetmessageid.md) <br/> |<span data-ttu-id="ef436-114">Representa el identificador de mensaje de Internet de un elemento.</span><span class="sxs-lookup"><span data-stu-id="ef436-114">Represents the Internet message identifier of an item.</span></span>  <br/> |
|[<span data-ttu-id="ef436-115">ParentInternetMessageId</span><span class="sxs-lookup"><span data-stu-id="ef436-115">ParentInternetMessageId</span></span>](parentinternetmessageid.md) <br/> |<span data-ttu-id="ef436-116">Especifica el identificador del mensaje de Internet primario.</span><span class="sxs-lookup"><span data-stu-id="ef436-116">Specifies the identifier of the parent Internet message.</span></span>  <br/> |
|[<span data-ttu-id="ef436-117">ItemIds (NonEmptyArrayOfItemIdsType)</span><span class="sxs-lookup"><span data-stu-id="ef436-117">ItemIds (NonEmptyArrayOfItemIdsType)</span></span>](itemids-nonemptyarrayofitemidstype.md) <br/> |<span data-ttu-id="ef436-118">Especifica todos los elementos en el nodo de conversación.</span><span class="sxs-lookup"><span data-stu-id="ef436-118">Specifies all the items in the conversation node.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ef436-119">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="ef436-119">Parent elements</span></span>

|<span data-ttu-id="ef436-120">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="ef436-120">**Element**</span></span>|<span data-ttu-id="ef436-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ef436-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ef436-122">ConversationNodes</span><span class="sxs-lookup"><span data-stu-id="ef436-122">ConversationNodes</span></span>](conversationnodes.md) <br/> |<span data-ttu-id="ef436-123">Especifica una colección de nodos de conversación.</span><span class="sxs-lookup"><span data-stu-id="ef436-123">Specifies a collection of conversation nodes.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ef436-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ef436-124">Remarks</span></span>

<span data-ttu-id="ef436-125">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="ef436-125">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="ef436-126">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="ef436-126">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ef436-127">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="ef436-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ef436-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="ef436-128">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ef436-129">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="ef436-129">Schema Name</span></span>  <br/> |<span data-ttu-id="ef436-130">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="ef436-130">Type schema</span></span>  <br/> |
|<span data-ttu-id="ef436-131">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="ef436-131">Validation File</span></span>  <br/> |<span data-ttu-id="ef436-132">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="ef436-132">types.xsd</span></span>  <br/> |
|<span data-ttu-id="ef436-133">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="ef436-133">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="ef436-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="ef436-134">See also</span></span>



- [<span data-ttu-id="ef436-135">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="ef436-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

