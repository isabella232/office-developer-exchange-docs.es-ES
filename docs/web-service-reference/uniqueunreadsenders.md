---
title: UniqueUnreadSenders
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UniqueUnreadSenders
api_type:
- schema
ms.assetid: eb7d1274-ce2e-4ef8-b47f-e911174aab0c
description: El elemento UniqueUnreadSenders contiene una lista de todas las personas que han enviado mensajes que actualmente no están leídos en esta conversación en la carpeta actual. Este elemento es de sólo lectura.
ms.openlocfilehash: 0e45362e88be4930b8bc2f641c1fb00cc63c0605
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458855"
---
# <a name="uniqueunreadsenders"></a><span data-ttu-id="4a72c-104">UniqueUnreadSenders</span><span class="sxs-lookup"><span data-stu-id="4a72c-104">UniqueUnreadSenders</span></span>

<span data-ttu-id="4a72c-105">El elemento **UniqueUnreadSenders** contiene una lista de todas las personas que han enviado mensajes que actualmente no están leídos en esta conversación en la carpeta actual.</span><span class="sxs-lookup"><span data-stu-id="4a72c-105">The **UniqueUnreadSenders** element contains a list of all the people who have sent messages that are currently unread in this conversation in the current folder.</span></span> <span data-ttu-id="4a72c-106">Este elemento es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="4a72c-106">This element is read-only.</span></span> 
  
[<span data-ttu-id="4a72c-107">FindConversationResponse</span><span class="sxs-lookup"><span data-stu-id="4a72c-107">FindConversationResponse</span></span>](findconversationresponse.md)
  
[<span data-ttu-id="4a72c-108">Conversaciones</span><span class="sxs-lookup"><span data-stu-id="4a72c-108">Conversations</span></span>](conversations-ex15websvcsotherref.md)
  
[<span data-ttu-id="4a72c-109">Conversación (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="4a72c-109">Conversation (ConversationType)</span></span>](conversation-conversationtype.md)
  
[<span data-ttu-id="4a72c-110">UniqueUnreadSenders</span><span class="sxs-lookup"><span data-stu-id="4a72c-110">UniqueUnreadSenders</span></span>](uniqueunreadsenders.md)
  
```XML
<UniqueUnreadSenders>
   <String/>
</UniqueUnreadSenders>
```

 <span data-ttu-id="4a72c-111">**ArrayOfStringsType**</span><span class="sxs-lookup"><span data-stu-id="4a72c-111">**ArrayOfStringsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4a72c-112">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="4a72c-112">Attributes and elements</span></span>

<span data-ttu-id="4a72c-113">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="4a72c-113">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4a72c-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="4a72c-114">Attributes</span></span>

<span data-ttu-id="4a72c-115">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="4a72c-115">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4a72c-116">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="4a72c-116">Child elements</span></span>

|<span data-ttu-id="4a72c-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="4a72c-117">**Element**</span></span>|<span data-ttu-id="4a72c-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4a72c-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4a72c-119">String</span><span class="sxs-lookup"><span data-stu-id="4a72c-119">String</span></span>](string.md) <br/> |<span data-ttu-id="4a72c-120">Contiene un remitente de una sola conversación.</span><span class="sxs-lookup"><span data-stu-id="4a72c-120">Contains a single conversation sender.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="4a72c-121">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="4a72c-121">Parent elements</span></span>

|<span data-ttu-id="4a72c-122">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="4a72c-122">**Element**</span></span>|<span data-ttu-id="4a72c-123">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4a72c-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4a72c-124">Conversación (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="4a72c-124">Conversation (ConversationType)</span></span>](conversation-conversationtype.md) <br/> |<span data-ttu-id="4a72c-125">Representa una sola conversación.</span><span class="sxs-lookup"><span data-stu-id="4a72c-125">Represents a single conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="4a72c-126">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="4a72c-126">Text value</span></span>

<span data-ttu-id="4a72c-127">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="4a72c-127">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4a72c-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4a72c-128">Remarks</span></span>

<span data-ttu-id="4a72c-129">Este elemento se introdujo en Exchange Server 2010 Service Pack 1 (SP1). El esquema que describe este elemento se encuentra en el directorio virtual de IIS que hospeda los servicios Web de Exchange.</span><span class="sxs-lookup"><span data-stu-id="4a72c-129">This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4a72c-130">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="4a72c-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4a72c-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="4a72c-131">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="4a72c-132">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="4a72c-132">Schema name</span></span>  <br/> |<span data-ttu-id="4a72c-133">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="4a72c-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="4a72c-134">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="4a72c-134">Validation file</span></span>  <br/> |<span data-ttu-id="4a72c-135">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="4a72c-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="4a72c-136">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="4a72c-136">Can be empty</span></span>  <br/> |<span data-ttu-id="4a72c-137">Falso</span><span class="sxs-lookup"><span data-stu-id="4a72c-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4a72c-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="4a72c-138">See also</span></span>



[<span data-ttu-id="4a72c-139">Operación FindConversation</span><span class="sxs-lookup"><span data-stu-id="4a72c-139">FindConversation operation</span></span>](findconversation-operation.md)
  
[<span data-ttu-id="4a72c-140">Operación ApplyConversationAction</span><span class="sxs-lookup"><span data-stu-id="4a72c-140">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)


[<span data-ttu-id="4a72c-141">Conversaciones en EWS</span><span class="sxs-lookup"><span data-stu-id="4a72c-141">Conversations in EWS</span></span>](https://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)

