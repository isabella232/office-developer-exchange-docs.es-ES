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
description: El elemento UniqueRecipients contiene la lista de destinatarios de una conversación en una carpeta determinada. Este elemento es de sólo lectura.
ms.openlocfilehash: 710559e599c6cec1db371165f01187f8960024f6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19840782"
---
# <a name="uniquerecipients"></a><span data-ttu-id="2c385-104">UniqueRecipients</span><span class="sxs-lookup"><span data-stu-id="2c385-104">UniqueRecipients</span></span>

<span data-ttu-id="2c385-105">El elemento **UniqueRecipients** contiene la lista de destinatarios de una conversación en una carpeta determinada.</span><span class="sxs-lookup"><span data-stu-id="2c385-105">The **UniqueRecipients** element contains the recipient list of a conversation in a particular folder.</span></span> <span data-ttu-id="2c385-106">Este elemento es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="2c385-106">This element is read-only.</span></span> 
  
[<span data-ttu-id="2c385-107">FindConversationResponse</span><span class="sxs-lookup"><span data-stu-id="2c385-107">FindConversationResponse</span></span>](findconversationresponse.md)
  
[<span data-ttu-id="2c385-108">Conversaciones</span><span class="sxs-lookup"><span data-stu-id="2c385-108">Conversations</span></span>](conversations-ex15websvcsotherref.md)
  
[<span data-ttu-id="2c385-109">Conversación (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="2c385-109">Conversation (ConversationType)</span></span>](conversation-conversationtype.md)
  
[<span data-ttu-id="2c385-110">UniqueRecipients</span><span class="sxs-lookup"><span data-stu-id="2c385-110">UniqueRecipients</span></span>](uniquerecipients.md)
  
```XML
<UniqueRecpients>
   <String/>
</UniqueRecpients>
```

 <span data-ttu-id="2c385-111">**ArrayOfStringsType**</span><span class="sxs-lookup"><span data-stu-id="2c385-111">**ArrayOfStringsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2c385-112">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="2c385-112">Attributes and elements</span></span>

<span data-ttu-id="2c385-113">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="2c385-113">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2c385-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="2c385-114">Attributes</span></span>

<span data-ttu-id="2c385-115">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="2c385-115">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2c385-116">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="2c385-116">Child elements</span></span>

|<span data-ttu-id="2c385-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="2c385-117">**Element**</span></span>|<span data-ttu-id="2c385-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2c385-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2c385-119">String</span><span class="sxs-lookup"><span data-stu-id="2c385-119">String</span></span>](string.md) <br/> |<span data-ttu-id="2c385-120">Representa a un único destinatario de una conversación.</span><span class="sxs-lookup"><span data-stu-id="2c385-120">Represents a unique recipient of a conversation.</span></span> <span data-ttu-id="2c385-121">Este elemento es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="2c385-121">This element is read-only.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="2c385-122">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="2c385-122">Parent elements</span></span>

|<span data-ttu-id="2c385-123">**Element**</span><span class="sxs-lookup"><span data-stu-id="2c385-123">**Element**</span></span>|<span data-ttu-id="2c385-124">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2c385-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2c385-125">Conversación (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="2c385-125">Conversation (ConversationType)</span></span>](conversation-conversationtype.md) <br/> |<span data-ttu-id="2c385-126">Representa una sola conversación.</span><span class="sxs-lookup"><span data-stu-id="2c385-126">Represents a single conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="2c385-127">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="2c385-127">Text value</span></span>

<span data-ttu-id="2c385-128">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="2c385-128">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2c385-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2c385-129">Remarks</span></span>

<span data-ttu-id="2c385-130">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda Exchange Web Services.This elemento fue introdujo en Exchange Server 2010 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="2c385-130">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2c385-131">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="2c385-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2c385-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="2c385-132">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="2c385-133">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="2c385-133">Schema name</span></span>  <br/> |<span data-ttu-id="2c385-134">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="2c385-134">Messages schema</span></span>  <br/> |
|<span data-ttu-id="2c385-135">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="2c385-135">Validation file</span></span>  <br/> |<span data-ttu-id="2c385-136">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="2c385-136">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="2c385-137">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="2c385-137">Can be empty</span></span>  <br/> |<span data-ttu-id="2c385-138">False</span><span class="sxs-lookup"><span data-stu-id="2c385-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2c385-139">Ver también</span><span class="sxs-lookup"><span data-stu-id="2c385-139">See also</span></span>



[<span data-ttu-id="2c385-140">Operación de FindConversation</span><span class="sxs-lookup"><span data-stu-id="2c385-140">FindConversation operation</span></span>](findconversation-operation.md)


[<span data-ttu-id="2c385-141">Conversaciones de EWS</span><span class="sxs-lookup"><span data-stu-id="2c385-141">Conversations in EWS</span></span>](http://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)

