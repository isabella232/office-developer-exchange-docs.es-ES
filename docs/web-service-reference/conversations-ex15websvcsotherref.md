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
description: El elemento de conversaciones contiene una matriz de las conversaciones que se devuelven en la respuesta de FindConversation.
ms.openlocfilehash: cd36364bd975d1464af9a1114c64c29543b4ec47
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763885"
---
# <a name="conversations"></a><span data-ttu-id="144da-103">Conversaciones</span><span class="sxs-lookup"><span data-stu-id="144da-103">Conversations</span></span>

<span data-ttu-id="144da-104">El elemento de **conversaciones** contiene una matriz de las conversaciones que se devuelven en la respuesta de **FindConversation** .</span><span class="sxs-lookup"><span data-stu-id="144da-104">The **Conversations** element contains an array of conversations that are returned in the **FindConversation** response.</span></span> 
  
[<span data-ttu-id="144da-105">FindConversationResponse</span><span class="sxs-lookup"><span data-stu-id="144da-105">FindConversationResponse</span></span>](findconversationresponse.md)
  
[<span data-ttu-id="144da-106">Conversaciones</span><span class="sxs-lookup"><span data-stu-id="144da-106">Conversations</span></span>](conversations-ex15websvcsotherref.md)
  
```xml
<Conversations>
   <Conversation/>
</Conversations>
```

 <span data-ttu-id="144da-107">**ArrayOfConversationsType**</span><span class="sxs-lookup"><span data-stu-id="144da-107">**ArrayOfConversationsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="144da-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="144da-108">Attributes and elements</span></span>

<span data-ttu-id="144da-109">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="144da-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="144da-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="144da-110">Attributes</span></span>

<span data-ttu-id="144da-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="144da-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="144da-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="144da-112">Child elements</span></span>

|<span data-ttu-id="144da-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="144da-113">**Element**</span></span>|<span data-ttu-id="144da-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="144da-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="144da-115">Conversación (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="144da-115">Conversation (ConversationType)</span></span>](conversation-conversationtype.md) <br/> |<span data-ttu-id="144da-116">Representa una sola conversación.</span><span class="sxs-lookup"><span data-stu-id="144da-116">Represents a single conversation.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="144da-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="144da-117">Parent elements</span></span>

|<span data-ttu-id="144da-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="144da-118">**Element**</span></span>|<span data-ttu-id="144da-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="144da-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="144da-120">FindConversationResponse</span><span class="sxs-lookup"><span data-stu-id="144da-120">FindConversationResponse</span></span>](findconversationresponse.md) <br/> |<span data-ttu-id="144da-121">Define una respuesta a una solicitud de **FindConversation** .</span><span class="sxs-lookup"><span data-stu-id="144da-121">Defines a response to a **FindConversation** request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="144da-122">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="144da-122">Text value</span></span>

<span data-ttu-id="144da-123">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="144da-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="144da-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="144da-124">Remarks</span></span>

<span data-ttu-id="144da-125">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda Exchange Web Services.This elemento fue introdujo en Exchange Server 2010 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="144da-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="144da-126">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="144da-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="144da-127">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="144da-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="144da-128">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="144da-128">Schema name</span></span>  <br/> |<span data-ttu-id="144da-129">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="144da-129">Messages schema</span></span>  <br/> |
|<span data-ttu-id="144da-130">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="144da-130">Validation file</span></span>  <br/> |<span data-ttu-id="144da-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="144da-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="144da-132">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="144da-132">Can be empty</span></span>  <br/> |<span data-ttu-id="144da-133">False</span><span class="sxs-lookup"><span data-stu-id="144da-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="144da-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="144da-134">See also</span></span>



[<span data-ttu-id="144da-135">Operación de FindConversation</span><span class="sxs-lookup"><span data-stu-id="144da-135">FindConversation operation</span></span>](findconversation-operation.md)


[<span data-ttu-id="144da-136">Conversaciones de EWS</span><span class="sxs-lookup"><span data-stu-id="144da-136">Conversations in EWS</span></span>](http://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)

