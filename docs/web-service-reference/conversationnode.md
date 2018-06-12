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
ms.openlocfilehash: c8289e5f30bfd25eb12d54e3be0c561786308dc6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763879"
---
# <a name="conversationnode"></a><span data-ttu-id="80235-103">ConversationNode</span><span class="sxs-lookup"><span data-stu-id="80235-103">ConversationNode</span></span>

<span data-ttu-id="80235-104">El elemento **ConversationNode** especifica un nodo en una conversación.</span><span class="sxs-lookup"><span data-stu-id="80235-104">The **ConversationNode** element specifies a node in a conversation.</span></span> 
  
```XML
<ConversationNode>
    <InternetMessageId></InternetMessageId>
    <ParentInternetMessageId></ParentInternetMessageId>
    <Items></Items>
</ConversationNode>
```

 <span data-ttu-id="80235-105">**ConversationNodeType**</span><span class="sxs-lookup"><span data-stu-id="80235-105">**ConversationNodeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="80235-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="80235-106">Attributes and elements</span></span>

<span data-ttu-id="80235-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="80235-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="80235-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="80235-108">Attributes</span></span>

<span data-ttu-id="80235-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="80235-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="80235-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="80235-110">Child elements</span></span>

|<span data-ttu-id="80235-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="80235-111">**Element**</span></span>|<span data-ttu-id="80235-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="80235-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="80235-113">InternetMessageId</span><span class="sxs-lookup"><span data-stu-id="80235-113">InternetMessageId</span></span>](internetmessageid.md) <br/> |<span data-ttu-id="80235-114">Representa el identificador de mensaje de Internet de un elemento.</span><span class="sxs-lookup"><span data-stu-id="80235-114">Represents the Internet message identifier of an item.</span></span>  <br/> |
|[<span data-ttu-id="80235-115">ParentInternetMessageId</span><span class="sxs-lookup"><span data-stu-id="80235-115">ParentInternetMessageId</span></span>](parentinternetmessageid.md) <br/> |<span data-ttu-id="80235-116">Especifica el identificador del mensaje de Internet primario.</span><span class="sxs-lookup"><span data-stu-id="80235-116">Specifies the identifier of the parent Internet message.</span></span>  <br/> |
|[<span data-ttu-id="80235-117">ItemId (NonEmptyArrayOfItemIdsType)</span><span class="sxs-lookup"><span data-stu-id="80235-117">ItemIds (NonEmptyArrayOfItemIdsType)</span></span>](itemids-nonemptyarrayofitemidstype.md) <br/> |<span data-ttu-id="80235-118">Especifica todos los elementos en el nodo de conversación.</span><span class="sxs-lookup"><span data-stu-id="80235-118">Specifies all the items in the conversation node.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="80235-119">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="80235-119">Parent elements</span></span>

|<span data-ttu-id="80235-120">**Element**</span><span class="sxs-lookup"><span data-stu-id="80235-120">**Element**</span></span>|<span data-ttu-id="80235-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="80235-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="80235-122">ConversationNodes</span><span class="sxs-lookup"><span data-stu-id="80235-122">ConversationNodes</span></span>](conversationnodes.md) <br/> |<span data-ttu-id="80235-123">Especifica una colección de nodos de conversación.</span><span class="sxs-lookup"><span data-stu-id="80235-123">Specifies a collection of conversation nodes.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="80235-124">Notas</span><span class="sxs-lookup"><span data-stu-id="80235-124">Remarks</span></span>

<span data-ttu-id="80235-125">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="80235-125">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="80235-126">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="80235-126">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="80235-127">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="80235-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="80235-128">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="80235-128">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="80235-129">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="80235-129">Schema Name</span></span>  <br/> |<span data-ttu-id="80235-130">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="80235-130">Type schema</span></span>  <br/> |
|<span data-ttu-id="80235-131">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="80235-131">Validation File</span></span>  <br/> |<span data-ttu-id="80235-132">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="80235-132">types.xsd</span></span>  <br/> |
|<span data-ttu-id="80235-133">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="80235-133">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="80235-134">Ver también</span><span class="sxs-lookup"><span data-stu-id="80235-134">See also</span></span>



- [<span data-ttu-id="80235-135">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="80235-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

