---
title: UniqueRecipients
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UniqueRecipients
api_type:
- schema
ms.assetid: 9f46ed05-5370-46ee-80f5-83f97224c76e
description: El elemento UniqueRecipients contiene la lista de destinatarios de una conversación en una carpeta concreta. Este elemento es de sólo lectura.
ms.openlocfilehash: d7f6b0aa01aceb6a251fb0c46d89b34cad260acd
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530729"
---
# <a name="uniquerecipients"></a><span data-ttu-id="63128-104">UniqueRecipients</span><span class="sxs-lookup"><span data-stu-id="63128-104">UniqueRecipients</span></span>

<span data-ttu-id="63128-105">El elemento **UniqueRecipients** contiene la lista de destinatarios de una conversación en una carpeta concreta.</span><span class="sxs-lookup"><span data-stu-id="63128-105">The **UniqueRecipients** element contains the recipient list of a conversation in a particular folder.</span></span> <span data-ttu-id="63128-106">Este elemento es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="63128-106">This element is read-only.</span></span> 
  
[<span data-ttu-id="63128-107">FindConversationResponse</span><span class="sxs-lookup"><span data-stu-id="63128-107">FindConversationResponse</span></span>](findconversationresponse.md)
  
[<span data-ttu-id="63128-108">Conversaciones</span><span class="sxs-lookup"><span data-stu-id="63128-108">Conversations</span></span>](conversations-ex15websvcsotherref.md)
  
[<span data-ttu-id="63128-109">Conversación (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="63128-109">Conversation (ConversationType)</span></span>](conversation-conversationtype.md)
  
[<span data-ttu-id="63128-110">UniqueRecipients</span><span class="sxs-lookup"><span data-stu-id="63128-110">UniqueRecipients</span></span>](uniquerecipients.md)
  
```XML
<UniqueRecpients>
   <String/>
</UniqueRecpients>
```

 <span data-ttu-id="63128-111">**ArrayOfStringsType**</span><span class="sxs-lookup"><span data-stu-id="63128-111">**ArrayOfStringsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="63128-112">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="63128-112">Attributes and elements</span></span>

<span data-ttu-id="63128-113">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="63128-113">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="63128-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="63128-114">Attributes</span></span>

<span data-ttu-id="63128-115">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="63128-115">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="63128-116">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="63128-116">Child elements</span></span>

|<span data-ttu-id="63128-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="63128-117">**Element**</span></span>|<span data-ttu-id="63128-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="63128-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="63128-119">String</span><span class="sxs-lookup"><span data-stu-id="63128-119">String</span></span>](string.md) <br/> |<span data-ttu-id="63128-120">Representa un destinatario único de una conversación.</span><span class="sxs-lookup"><span data-stu-id="63128-120">Represents a unique recipient of a conversation.</span></span> <span data-ttu-id="63128-121">Este elemento es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="63128-121">This element is read-only.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="63128-122">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="63128-122">Parent elements</span></span>

|<span data-ttu-id="63128-123">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="63128-123">**Element**</span></span>|<span data-ttu-id="63128-124">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="63128-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="63128-125">Conversación (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="63128-125">Conversation (ConversationType)</span></span>](conversation-conversationtype.md) <br/> |<span data-ttu-id="63128-126">Representa una sola conversación.</span><span class="sxs-lookup"><span data-stu-id="63128-126">Represents a single conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="63128-127">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="63128-127">Text value</span></span>

<span data-ttu-id="63128-128">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="63128-128">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="63128-129">Comentarios</span><span class="sxs-lookup"><span data-stu-id="63128-129">Remarks</span></span>

<span data-ttu-id="63128-130">El esquema que describe este elemento se encuentra en el directorio virtual de IIS que hospeda los servicios Web de Exchange. este elemento se introdujo en Exchange Server 2010 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="63128-130">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="63128-131">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="63128-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="63128-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="63128-132">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="63128-133">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="63128-133">Schema name</span></span>  <br/> |<span data-ttu-id="63128-134">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="63128-134">Messages schema</span></span>  <br/> |
|<span data-ttu-id="63128-135">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="63128-135">Validation file</span></span>  <br/> |<span data-ttu-id="63128-136">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="63128-136">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="63128-137">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="63128-137">Can be empty</span></span>  <br/> |<span data-ttu-id="63128-138">Falso</span><span class="sxs-lookup"><span data-stu-id="63128-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="63128-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="63128-139">See also</span></span>



[<span data-ttu-id="63128-140">Operación FindConversation</span><span class="sxs-lookup"><span data-stu-id="63128-140">FindConversation operation</span></span>](findconversation-operation.md)


[<span data-ttu-id="63128-141">Conversaciones en EWS</span><span class="sxs-lookup"><span data-stu-id="63128-141">Conversations in EWS</span></span>](https://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)

