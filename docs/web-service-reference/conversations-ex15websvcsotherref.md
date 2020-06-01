---
title: Conversaciones
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Conversations
api_type:
- schema
ms.assetid: 1d18f98c-6457-45e9-a934-32da20885ac6
description: El elemento Conversations contiene una matriz de conversaciones que se devuelven en la respuesta FindConversation.
ms.openlocfilehash: 8af1023db51dd955c544422520ec5565f09f5372
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463800"
---
# <a name="conversations"></a><span data-ttu-id="cba5a-103">Conversaciones</span><span class="sxs-lookup"><span data-stu-id="cba5a-103">Conversations</span></span>

<span data-ttu-id="cba5a-104">El elemento **Conversations** contiene una matriz de conversaciones que se devuelven en la respuesta **FindConversation** .</span><span class="sxs-lookup"><span data-stu-id="cba5a-104">The **Conversations** element contains an array of conversations that are returned in the **FindConversation** response.</span></span> 
  
[<span data-ttu-id="cba5a-105">FindConversationResponse</span><span class="sxs-lookup"><span data-stu-id="cba5a-105">FindConversationResponse</span></span>](findconversationresponse.md)
  
[<span data-ttu-id="cba5a-106">Conversaciones</span><span class="sxs-lookup"><span data-stu-id="cba5a-106">Conversations</span></span>](conversations-ex15websvcsotherref.md)
  
```xml
<Conversations>
   <Conversation/>
</Conversations>
```

 <span data-ttu-id="cba5a-107">**ArrayOfConversationsType**</span><span class="sxs-lookup"><span data-stu-id="cba5a-107">**ArrayOfConversationsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="cba5a-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="cba5a-108">Attributes and elements</span></span>

<span data-ttu-id="cba5a-109">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="cba5a-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cba5a-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="cba5a-110">Attributes</span></span>

<span data-ttu-id="cba5a-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="cba5a-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="cba5a-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="cba5a-112">Child elements</span></span>

|<span data-ttu-id="cba5a-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="cba5a-113">**Element**</span></span>|<span data-ttu-id="cba5a-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="cba5a-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cba5a-115">Conversación (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="cba5a-115">Conversation (ConversationType)</span></span>](conversation-conversationtype.md) <br/> |<span data-ttu-id="cba5a-116">Representa una sola conversación.</span><span class="sxs-lookup"><span data-stu-id="cba5a-116">Represents a single conversation.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="cba5a-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="cba5a-117">Parent elements</span></span>

|<span data-ttu-id="cba5a-118">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="cba5a-118">**Element**</span></span>|<span data-ttu-id="cba5a-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="cba5a-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cba5a-120">FindConversationResponse</span><span class="sxs-lookup"><span data-stu-id="cba5a-120">FindConversationResponse</span></span>](findconversationresponse.md) <br/> |<span data-ttu-id="cba5a-121">Define una respuesta a una solicitud **FindConversation** .</span><span class="sxs-lookup"><span data-stu-id="cba5a-121">Defines a response to a **FindConversation** request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="cba5a-122">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="cba5a-122">Text value</span></span>

<span data-ttu-id="cba5a-123">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="cba5a-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="cba5a-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="cba5a-124">Remarks</span></span>

<span data-ttu-id="cba5a-125">El esquema que describe este elemento se encuentra en el directorio virtual de IIS que hospeda los servicios Web de Exchange. este elemento se introdujo en Exchange Server 2010 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="cba5a-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="cba5a-126">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="cba5a-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cba5a-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="cba5a-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="cba5a-128">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="cba5a-128">Schema name</span></span>  <br/> |<span data-ttu-id="cba5a-129">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="cba5a-129">Messages schema</span></span>  <br/> |
|<span data-ttu-id="cba5a-130">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="cba5a-130">Validation file</span></span>  <br/> |<span data-ttu-id="cba5a-131">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="cba5a-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="cba5a-132">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="cba5a-132">Can be empty</span></span>  <br/> |<span data-ttu-id="cba5a-133">Falso</span><span class="sxs-lookup"><span data-stu-id="cba5a-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cba5a-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="cba5a-134">See also</span></span>



[<span data-ttu-id="cba5a-135">Operación FindConversation</span><span class="sxs-lookup"><span data-stu-id="cba5a-135">FindConversation operation</span></span>](findconversation-operation.md)


[<span data-ttu-id="cba5a-136">Conversaciones en EWS</span><span class="sxs-lookup"><span data-stu-id="cba5a-136">Conversations in EWS</span></span>](https://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)

