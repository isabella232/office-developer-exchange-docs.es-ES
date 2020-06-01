---
title: GlobalUniqueSenders
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GlobalUniqueSenders
api_type:
- schema
ms.assetid: 6bd9e9cb-19c8-45af-b211-dfb8a6003b1b
description: El elemento GlobalUniqueSender contiene una lista de todos los remitentes de los elementos de conversación en el buzón.
ms.openlocfilehash: 0e85e201017e175a9ffc6b923976020d4157d5b7
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459066"
---
# <a name="globaluniquesenders"></a><span data-ttu-id="879b8-103">GlobalUniqueSenders</span><span class="sxs-lookup"><span data-stu-id="879b8-103">GlobalUniqueSenders</span></span>

<span data-ttu-id="879b8-104">El elemento **GlobalUniqueSender** contiene una lista de todos los remitentes de los elementos de conversación en el buzón.</span><span class="sxs-lookup"><span data-stu-id="879b8-104">The **GlobalUniqueSender** element contains a list of all the senders of conversation items in the mailbox.</span></span> 
  
[<span data-ttu-id="879b8-105">FindConversationResponse</span><span class="sxs-lookup"><span data-stu-id="879b8-105">FindConversationResponse</span></span>](findconversationresponse.md)
  
[<span data-ttu-id="879b8-106">Conversaciones</span><span class="sxs-lookup"><span data-stu-id="879b8-106">Conversations</span></span>](conversations-ex15websvcsotherref.md)
  
[<span data-ttu-id="879b8-107">Conversación (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="879b8-107">Conversation (ConversationType)</span></span>](conversation-conversationtype.md)
  
[<span data-ttu-id="879b8-108">GlobalUniqueSenders</span><span class="sxs-lookup"><span data-stu-id="879b8-108">GlobalUniqueSenders</span></span>](globaluniquesenders.md)
  
```XML
<GlobalUniqueSender>
   <String/>
</GlobalUniqueSender>
```

 <span data-ttu-id="879b8-109">**ArrayOfStringsType**</span><span class="sxs-lookup"><span data-stu-id="879b8-109">**ArrayOfStringsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="879b8-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="879b8-110">Attributes and elements</span></span>

<span data-ttu-id="879b8-111">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="879b8-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="879b8-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="879b8-112">Attributes</span></span>

<span data-ttu-id="879b8-113">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="879b8-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="879b8-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="879b8-114">Child elements</span></span>

|<span data-ttu-id="879b8-115">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="879b8-115">**Element**</span></span>|<span data-ttu-id="879b8-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="879b8-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="879b8-117">String</span><span class="sxs-lookup"><span data-stu-id="879b8-117">String</span></span>](string.md) <br/> |<span data-ttu-id="879b8-118">Contiene un remitente de una sola conversación.</span><span class="sxs-lookup"><span data-stu-id="879b8-118">Contains a single conversation sender.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="879b8-119">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="879b8-119">Parent elements</span></span>

|<span data-ttu-id="879b8-120">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="879b8-120">**Element**</span></span>|<span data-ttu-id="879b8-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="879b8-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="879b8-122">Conversación (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="879b8-122">Conversation (ConversationType)</span></span>](conversation-conversationtype.md) <br/> |<span data-ttu-id="879b8-123">Representa una sola conversación.</span><span class="sxs-lookup"><span data-stu-id="879b8-123">Represents a single conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="879b8-124">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="879b8-124">Text value</span></span>

<span data-ttu-id="879b8-125">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="879b8-125">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="879b8-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="879b8-126">Remarks</span></span>

<span data-ttu-id="879b8-127">El esquema que describe este elemento se encuentra en el directorio virtual de IIS que hospeda los servicios Web de Exchange. este elemento se introdujo en Exchange Server 2010 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="879b8-127">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="879b8-128">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="879b8-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="879b8-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="879b8-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="879b8-130">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="879b8-130">Schema name</span></span>  <br/> |<span data-ttu-id="879b8-131">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="879b8-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="879b8-132">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="879b8-132">Validation file</span></span>  <br/> |<span data-ttu-id="879b8-133">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="879b8-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="879b8-134">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="879b8-134">Can be empty</span></span>  <br/> |<span data-ttu-id="879b8-135">Falso</span><span class="sxs-lookup"><span data-stu-id="879b8-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="879b8-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="879b8-136">See also</span></span>



[<span data-ttu-id="879b8-137">Operación FindConversation</span><span class="sxs-lookup"><span data-stu-id="879b8-137">FindConversation operation</span></span>](findconversation-operation.md)
  
[<span data-ttu-id="879b8-138">Operación ApplyConversationAction</span><span class="sxs-lookup"><span data-stu-id="879b8-138">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)


[<span data-ttu-id="879b8-139">Conversaciones en EWS</span><span class="sxs-lookup"><span data-stu-id="879b8-139">Conversations in EWS</span></span>](https://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)

