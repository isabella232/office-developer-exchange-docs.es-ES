---
title: GlobalItemClasses
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GlobalItemClasses
api_type:
- schema
ms.assetid: 72634700-6d75-44c0-80b7-8c31743c04d6
description: El elemento GlobalItemClasses contiene una lista de clases de elementos que representa todas las clases de elementos de los elementos de la conversación en un buzón.
ms.openlocfilehash: e4cb8a8886f8262e8cb4a550b054e81ea18a5e11
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459436"
---
# <a name="globalitemclasses"></a><span data-ttu-id="a46f8-103">GlobalItemClasses</span><span class="sxs-lookup"><span data-stu-id="a46f8-103">GlobalItemClasses</span></span>

<span data-ttu-id="a46f8-104">El elemento **GlobalItemClasses** contiene una lista de clases de elementos que representa todas las clases de elementos de los elementos de la conversación en un buzón.</span><span class="sxs-lookup"><span data-stu-id="a46f8-104">The **GlobalItemClasses** element contains a list of item classes that represents all the item classes of the conversation items in a mailbox.</span></span> 
  
[<span data-ttu-id="a46f8-105">FindConversationResponse</span><span class="sxs-lookup"><span data-stu-id="a46f8-105">FindConversationResponse</span></span>](findconversationresponse.md)
  
[<span data-ttu-id="a46f8-106">Conversaciones</span><span class="sxs-lookup"><span data-stu-id="a46f8-106">Conversations</span></span>](conversations-ex15websvcsotherref.md)
  
[<span data-ttu-id="a46f8-107">Conversación (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="a46f8-107">Conversation (ConversationType)</span></span>](conversation-conversationtype.md)
  
[<span data-ttu-id="a46f8-108">GlobalItemClasses</span><span class="sxs-lookup"><span data-stu-id="a46f8-108">GlobalItemClasses</span></span>](globalitemclasses.md)
  
```XML
<GlobalItemClasses>
    <String/>
</GlobalItemClasses>
```

 <span data-ttu-id="a46f8-109">**ArrayOfItemClassType**</span><span class="sxs-lookup"><span data-stu-id="a46f8-109">**ArrayOfItemClassType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a46f8-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="a46f8-110">Attributes and elements</span></span>

<span data-ttu-id="a46f8-111">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="a46f8-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a46f8-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="a46f8-112">Attributes</span></span>

<span data-ttu-id="a46f8-113">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="a46f8-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a46f8-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="a46f8-114">Child elements</span></span>

|<span data-ttu-id="a46f8-115">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="a46f8-115">**Element**</span></span>|<span data-ttu-id="a46f8-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a46f8-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a46f8-117">ItemClass</span><span class="sxs-lookup"><span data-stu-id="a46f8-117">ItemClass</span></span>](itemclass.md) <br/> |<span data-ttu-id="a46f8-118">Representa la clase de mensaje de un elemento.</span><span class="sxs-lookup"><span data-stu-id="a46f8-118">Represents the message class of an item.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="a46f8-119">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="a46f8-119">Parent elements</span></span>

|<span data-ttu-id="a46f8-120">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="a46f8-120">**Element**</span></span>|<span data-ttu-id="a46f8-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a46f8-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a46f8-122">Conversación (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="a46f8-122">Conversation (ConversationType)</span></span>](conversation-conversationtype.md) <br/> |<span data-ttu-id="a46f8-123">Representa una sola conversación.</span><span class="sxs-lookup"><span data-stu-id="a46f8-123">Represents a single conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="a46f8-124">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="a46f8-124">Text value</span></span>

<span data-ttu-id="a46f8-125">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="a46f8-125">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a46f8-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a46f8-126">Remarks</span></span>

<span data-ttu-id="a46f8-127">El esquema que describe este elemento se encuentra en el directorio virtual de IIS que hospeda los servicios Web de Exchange. este elemento se introdujo en Exchange Server 2010 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="a46f8-127">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a46f8-128">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="a46f8-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a46f8-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="a46f8-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a46f8-130">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="a46f8-130">Schema name</span></span>  <br/> |<span data-ttu-id="a46f8-131">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="a46f8-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="a46f8-132">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="a46f8-132">Validation file</span></span>  <br/> |<span data-ttu-id="a46f8-133">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="a46f8-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="a46f8-134">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="a46f8-134">Can be empty</span></span>  <br/> |<span data-ttu-id="a46f8-135">Falso</span><span class="sxs-lookup"><span data-stu-id="a46f8-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a46f8-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="a46f8-136">See also</span></span>



[<span data-ttu-id="a46f8-137">Operación FindConversation</span><span class="sxs-lookup"><span data-stu-id="a46f8-137">FindConversation operation</span></span>](findconversation-operation.md)
  
[<span data-ttu-id="a46f8-138">Operación ApplyConversationAction</span><span class="sxs-lookup"><span data-stu-id="a46f8-138">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)


[<span data-ttu-id="a46f8-139">Conversaciones en EWS</span><span class="sxs-lookup"><span data-stu-id="a46f8-139">Conversations in EWS</span></span>](https://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)

