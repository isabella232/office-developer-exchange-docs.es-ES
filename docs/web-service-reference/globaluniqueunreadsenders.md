---
title: GlobalUniqueUnreadSenders
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GlobalUniqueUnreadSenders
api_type:
- schema
ms.assetid: 490abe30-7608-407a-923b-a4b3ddbca610
description: El elemento GlobalUniqueUnreadSenders especifica una lista de todas las personas que han enviado mensajes que actualmente no están leídos en esta conversación en todas las carpetas del buzón.
ms.openlocfilehash: 5a26053158a262d65993dba4be90888ee97f2112
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530821"
---
# <a name="globaluniqueunreadsenders"></a><span data-ttu-id="d23fc-103">GlobalUniqueUnreadSenders</span><span class="sxs-lookup"><span data-stu-id="d23fc-103">GlobalUniqueUnreadSenders</span></span>

<span data-ttu-id="d23fc-104">El elemento **GlobalUniqueUnreadSenders** especifica una lista de todas las personas que han enviado mensajes que actualmente no están leídos en esta conversación en todas las carpetas del buzón.</span><span class="sxs-lookup"><span data-stu-id="d23fc-104">The **GlobalUniqueUnreadSenders** element specifies a list of all the people who have sent messages that are currently unread in this conversation across all folders in the mailbox.</span></span> 
  
[<span data-ttu-id="d23fc-105">FindConversationResponse</span><span class="sxs-lookup"><span data-stu-id="d23fc-105">FindConversationResponse</span></span>](findconversationresponse.md)
  
[<span data-ttu-id="d23fc-106">Conversaciones</span><span class="sxs-lookup"><span data-stu-id="d23fc-106">Conversations</span></span>](conversations-ex15websvcsotherref.md)
  
[<span data-ttu-id="d23fc-107">Conversación (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="d23fc-107">Conversation (ConversationType)</span></span>](conversation-conversationtype.md)
  
[<span data-ttu-id="d23fc-108">GlobalUniqueUnreadSenders</span><span class="sxs-lookup"><span data-stu-id="d23fc-108">GlobalUniqueUnreadSenders</span></span>](globaluniqueunreadsenders.md)
  
```XML
<GlobalUniqueUnreadSenders>
   <String/>
</GlobalUniqueUnreadSenders>
```

 <span data-ttu-id="d23fc-109">**ArrayOfStringsType**</span><span class="sxs-lookup"><span data-stu-id="d23fc-109">**ArrayOfStringsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d23fc-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="d23fc-110">Attributes and elements</span></span>

<span data-ttu-id="d23fc-111">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="d23fc-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d23fc-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="d23fc-112">Attributes</span></span>

<span data-ttu-id="d23fc-113">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="d23fc-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d23fc-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="d23fc-114">Child elements</span></span>

|<span data-ttu-id="d23fc-115">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="d23fc-115">**Element**</span></span>|<span data-ttu-id="d23fc-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d23fc-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d23fc-117">String</span><span class="sxs-lookup"><span data-stu-id="d23fc-117">String</span></span>](string.md) <br/> |<span data-ttu-id="d23fc-118">Contiene un remitente de una sola conversación.</span><span class="sxs-lookup"><span data-stu-id="d23fc-118">Contains a single conversation sender.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d23fc-119">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="d23fc-119">Parent elements</span></span>

|<span data-ttu-id="d23fc-120">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="d23fc-120">**Element**</span></span>|<span data-ttu-id="d23fc-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d23fc-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d23fc-122">Conversación (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="d23fc-122">Conversation (ConversationType)</span></span>](conversation-conversationtype.md) <br/> |<span data-ttu-id="d23fc-123">Representa una sola conversación.</span><span class="sxs-lookup"><span data-stu-id="d23fc-123">Represents a single conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="d23fc-124">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="d23fc-124">Text value</span></span>

<span data-ttu-id="d23fc-125">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="d23fc-125">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d23fc-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d23fc-126">Remarks</span></span>

<span data-ttu-id="d23fc-127">El esquema que describe este elemento se encuentra en el directorio virtual de IIS que hospeda los servicios Web de Exchange. este elemento se introdujo en Exchange Server 2010 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="d23fc-127">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d23fc-128">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="d23fc-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d23fc-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="d23fc-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d23fc-130">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="d23fc-130">Schema name</span></span>  <br/> |<span data-ttu-id="d23fc-131">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="d23fc-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="d23fc-132">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="d23fc-132">Validation file</span></span>  <br/> |<span data-ttu-id="d23fc-133">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="d23fc-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d23fc-134">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="d23fc-134">Can be empty</span></span>  <br/> |<span data-ttu-id="d23fc-135">Falso</span><span class="sxs-lookup"><span data-stu-id="d23fc-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d23fc-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="d23fc-136">See also</span></span>



[<span data-ttu-id="d23fc-137">Operación FindConversation</span><span class="sxs-lookup"><span data-stu-id="d23fc-137">FindConversation operation</span></span>](findconversation-operation.md)
  
[<span data-ttu-id="d23fc-138">Operación ApplyConversationAction</span><span class="sxs-lookup"><span data-stu-id="d23fc-138">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)


[<span data-ttu-id="d23fc-139">Conversaciones en EWS</span><span class="sxs-lookup"><span data-stu-id="d23fc-139">Conversations in EWS</span></span>](https://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)

