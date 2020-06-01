---
title: UniqueSenders
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UniqueSenders
api_type:
- schema
ms.assetid: 1f55f2fe-b2f2-4169-83c1-fa5c752bd695
description: El elemento UniqueSenders contiene una lista de todos los remitentes de los elementos de conversación de la carpeta actual. Este elemento es de sólo lectura.
ms.openlocfilehash: 5c9a98a3083d02f3900cc263e0b99a570203b544
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459878"
---
# <a name="uniquesenders"></a><span data-ttu-id="f9bc0-104">UniqueSenders</span><span class="sxs-lookup"><span data-stu-id="f9bc0-104">UniqueSenders</span></span>

<span data-ttu-id="f9bc0-105">El elemento **UniqueSenders** contiene una lista de todos los remitentes de los elementos de conversación de la carpeta actual.</span><span class="sxs-lookup"><span data-stu-id="f9bc0-105">The **UniqueSenders** element contains a list of all the senders of conversation items in the current folder.</span></span> <span data-ttu-id="f9bc0-106">Este elemento es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="f9bc0-106">This element is read-only.</span></span> 
  
[<span data-ttu-id="f9bc0-107">FindConversationResponse</span><span class="sxs-lookup"><span data-stu-id="f9bc0-107">FindConversationResponse</span></span>](findconversationresponse.md)
  
[<span data-ttu-id="f9bc0-108">Conversaciones</span><span class="sxs-lookup"><span data-stu-id="f9bc0-108">Conversations</span></span>](conversations-ex15websvcsotherref.md)
  
[<span data-ttu-id="f9bc0-109">Conversación (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="f9bc0-109">Conversation (ConversationType)</span></span>](conversation-conversationtype.md)
  
[<span data-ttu-id="f9bc0-110">UniqueSenders</span><span class="sxs-lookup"><span data-stu-id="f9bc0-110">UniqueSenders</span></span>](uniquesenders.md)
  
```XML
<UniqueSenders>
   <String/>
</UniqueSenders>
```

 <span data-ttu-id="f9bc0-111">**ArrayOfStringsType**</span><span class="sxs-lookup"><span data-stu-id="f9bc0-111">**ArrayOfStringsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f9bc0-112">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="f9bc0-112">Attributes and elements</span></span>

<span data-ttu-id="f9bc0-113">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="f9bc0-113">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f9bc0-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="f9bc0-114">Attributes</span></span>

<span data-ttu-id="f9bc0-115">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="f9bc0-115">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f9bc0-116">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="f9bc0-116">Child elements</span></span>

|<span data-ttu-id="f9bc0-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="f9bc0-117">**Element**</span></span>|<span data-ttu-id="f9bc0-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f9bc0-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f9bc0-119">String</span><span class="sxs-lookup"><span data-stu-id="f9bc0-119">String</span></span>](string.md) <br/> |<span data-ttu-id="f9bc0-120">Contiene un remitente de una sola conversación.</span><span class="sxs-lookup"><span data-stu-id="f9bc0-120">Contains a single conversation sender.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="f9bc0-121">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="f9bc0-121">Parent elements</span></span>

|<span data-ttu-id="f9bc0-122">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="f9bc0-122">**Element**</span></span>|<span data-ttu-id="f9bc0-123">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f9bc0-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f9bc0-124">Conversación (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="f9bc0-124">Conversation (ConversationType)</span></span>](conversation-conversationtype.md) <br/> |<span data-ttu-id="f9bc0-125">Representa una sola conversación.</span><span class="sxs-lookup"><span data-stu-id="f9bc0-125">Represents a single conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="f9bc0-126">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="f9bc0-126">Text value</span></span>

<span data-ttu-id="f9bc0-127">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="f9bc0-127">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f9bc0-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f9bc0-128">Remarks</span></span>

<span data-ttu-id="f9bc0-129">El esquema que describe este elemento se encuentra en el directorio virtual de IIS que hospeda los servicios Web de Exchange. este elemento se introdujo en Exchange Server 2010 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="f9bc0-129">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f9bc0-130">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="f9bc0-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f9bc0-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="f9bc0-131">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f9bc0-132">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="f9bc0-132">Schema name</span></span>  <br/> |<span data-ttu-id="f9bc0-133">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="f9bc0-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="f9bc0-134">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="f9bc0-134">Validation file</span></span>  <br/> |<span data-ttu-id="f9bc0-135">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="f9bc0-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="f9bc0-136">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="f9bc0-136">Can be empty</span></span>  <br/> |<span data-ttu-id="f9bc0-137">Falso</span><span class="sxs-lookup"><span data-stu-id="f9bc0-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f9bc0-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="f9bc0-138">See also</span></span>



[<span data-ttu-id="f9bc0-139">Operación FindConversation</span><span class="sxs-lookup"><span data-stu-id="f9bc0-139">FindConversation operation</span></span>](findconversation-operation.md)
  
[<span data-ttu-id="f9bc0-140">Operación ApplyConversationAction</span><span class="sxs-lookup"><span data-stu-id="f9bc0-140">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)


[<span data-ttu-id="f9bc0-141">Conversaciones en EWS</span><span class="sxs-lookup"><span data-stu-id="f9bc0-141">Conversations in EWS</span></span>](https://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)

