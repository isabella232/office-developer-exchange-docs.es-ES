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
description: El elemento GlobalItemClasses contiene una lista de las clases de elementos que representa todas las clases de elemento de los elementos de la conversación en un buzón de correo.
ms.openlocfilehash: a8f947d37c1335f1eaba5550a2b3a0aece0246ee
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19835735"
---
# <a name="globalitemclasses"></a><span data-ttu-id="13fb3-103">GlobalItemClasses</span><span class="sxs-lookup"><span data-stu-id="13fb3-103">GlobalItemClasses</span></span>

<span data-ttu-id="13fb3-104">El elemento **GlobalItemClasses** contiene una lista de las clases de elementos que representa todas las clases de elemento de los elementos de la conversación en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="13fb3-104">The **GlobalItemClasses** element contains a list of item classes that represents all the item classes of the conversation items in a mailbox.</span></span> 
  
[<span data-ttu-id="13fb3-105">FindConversationResponse</span><span class="sxs-lookup"><span data-stu-id="13fb3-105">FindConversationResponse</span></span>](findconversationresponse.md)
  
[<span data-ttu-id="13fb3-106">Conversaciones</span><span class="sxs-lookup"><span data-stu-id="13fb3-106">Conversations</span></span>](conversations-ex15websvcsotherref.md)
  
[<span data-ttu-id="13fb3-107">Conversación (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="13fb3-107">Conversation (ConversationType)</span></span>](conversation-conversationtype.md)
  
[<span data-ttu-id="13fb3-108">GlobalItemClasses</span><span class="sxs-lookup"><span data-stu-id="13fb3-108">GlobalItemClasses</span></span>](globalitemclasses.md)
  
```XML
<GlobalItemClasses>
    <String/>
</GlobalItemClasses>
```

 <span data-ttu-id="13fb3-109">**ArrayOfItemClassType**</span><span class="sxs-lookup"><span data-stu-id="13fb3-109">**ArrayOfItemClassType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="13fb3-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="13fb3-110">Attributes and elements</span></span>

<span data-ttu-id="13fb3-111">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="13fb3-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="13fb3-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="13fb3-112">Attributes</span></span>

<span data-ttu-id="13fb3-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="13fb3-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="13fb3-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="13fb3-114">Child elements</span></span>

|<span data-ttu-id="13fb3-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="13fb3-115">**Element**</span></span>|<span data-ttu-id="13fb3-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="13fb3-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="13fb3-117">ItemClass</span><span class="sxs-lookup"><span data-stu-id="13fb3-117">ItemClass</span></span>](itemclass.md) <br/> |<span data-ttu-id="13fb3-118">Representa la clase de mensaje de un elemento.</span><span class="sxs-lookup"><span data-stu-id="13fb3-118">Represents the message class of an item.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="13fb3-119">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="13fb3-119">Parent elements</span></span>

|<span data-ttu-id="13fb3-120">**Element**</span><span class="sxs-lookup"><span data-stu-id="13fb3-120">**Element**</span></span>|<span data-ttu-id="13fb3-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="13fb3-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="13fb3-122">Conversación (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="13fb3-122">Conversation (ConversationType)</span></span>](conversation-conversationtype.md) <br/> |<span data-ttu-id="13fb3-123">Representa una sola conversación.</span><span class="sxs-lookup"><span data-stu-id="13fb3-123">Represents a single conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="13fb3-124">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="13fb3-124">Text value</span></span>

<span data-ttu-id="13fb3-125">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="13fb3-125">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="13fb3-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="13fb3-126">Remarks</span></span>

<span data-ttu-id="13fb3-127">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda Exchange Web Services.This elemento fue introdujo en Exchange Server 2010 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="13fb3-127">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="13fb3-128">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="13fb3-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="13fb3-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="13fb3-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="13fb3-130">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="13fb3-130">Schema name</span></span>  <br/> |<span data-ttu-id="13fb3-131">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="13fb3-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="13fb3-132">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="13fb3-132">Validation file</span></span>  <br/> |<span data-ttu-id="13fb3-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="13fb3-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="13fb3-134">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="13fb3-134">Can be empty</span></span>  <br/> |<span data-ttu-id="13fb3-135">False</span><span class="sxs-lookup"><span data-stu-id="13fb3-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="13fb3-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="13fb3-136">See also</span></span>



[<span data-ttu-id="13fb3-137">Operación de FindConversation</span><span class="sxs-lookup"><span data-stu-id="13fb3-137">FindConversation operation</span></span>](findconversation-operation.md)
  
[<span data-ttu-id="13fb3-138">Operación ApplyConversationAction</span><span class="sxs-lookup"><span data-stu-id="13fb3-138">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)


[<span data-ttu-id="13fb3-139">Conversaciones de EWS</span><span class="sxs-lookup"><span data-stu-id="13fb3-139">Conversations in EWS</span></span>](http://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)

