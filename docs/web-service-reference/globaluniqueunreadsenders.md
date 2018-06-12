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
description: El elemento GlobalUniqueUnreadSenders especifica una lista de todas las personas que han enviado los mensajes que están actualmente no leídos en esta conversación a través de todas las carpetas del buzón de correo.
ms.openlocfilehash: ae088577f5aac0c7c3ee9c11fde184b70ab12e64
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19835749"
---
# <a name="globaluniqueunreadsenders"></a><span data-ttu-id="37097-103">GlobalUniqueUnreadSenders</span><span class="sxs-lookup"><span data-stu-id="37097-103">GlobalUniqueUnreadSenders</span></span>

<span data-ttu-id="37097-104">El elemento **GlobalUniqueUnreadSenders** especifica una lista de todas las personas que han enviado los mensajes que están actualmente no leídos en esta conversación a través de todas las carpetas del buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="37097-104">The **GlobalUniqueUnreadSenders** element specifies a list of all the people who have sent messages that are currently unread in this conversation across all folders in the mailbox.</span></span> 
  
[<span data-ttu-id="37097-105">FindConversationResponse</span><span class="sxs-lookup"><span data-stu-id="37097-105">FindConversationResponse</span></span>](findconversationresponse.md)
  
[<span data-ttu-id="37097-106">Conversaciones</span><span class="sxs-lookup"><span data-stu-id="37097-106">Conversations</span></span>](conversations-ex15websvcsotherref.md)
  
[<span data-ttu-id="37097-107">Conversación (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="37097-107">Conversation (ConversationType)</span></span>](conversation-conversationtype.md)
  
[<span data-ttu-id="37097-108">GlobalUniqueUnreadSenders</span><span class="sxs-lookup"><span data-stu-id="37097-108">GlobalUniqueUnreadSenders</span></span>](globaluniqueunreadsenders.md)
  
```XML
<GlobalUniqueUnreadSenders>
   <String/>
</GlobalUniqueUnreadSenders>
```

 <span data-ttu-id="37097-109">**ArrayOfStringsType**</span><span class="sxs-lookup"><span data-stu-id="37097-109">**ArrayOfStringsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="37097-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="37097-110">Attributes and elements</span></span>

<span data-ttu-id="37097-111">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="37097-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="37097-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="37097-112">Attributes</span></span>

<span data-ttu-id="37097-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="37097-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="37097-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="37097-114">Child elements</span></span>

|<span data-ttu-id="37097-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="37097-115">**Element**</span></span>|<span data-ttu-id="37097-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="37097-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="37097-117">String</span><span class="sxs-lookup"><span data-stu-id="37097-117">String</span></span>](string.md) <br/> |<span data-ttu-id="37097-118">Contiene un remitente conversación único.</span><span class="sxs-lookup"><span data-stu-id="37097-118">Contains a single conversation sender.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="37097-119">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="37097-119">Parent elements</span></span>

|<span data-ttu-id="37097-120">**Element**</span><span class="sxs-lookup"><span data-stu-id="37097-120">**Element**</span></span>|<span data-ttu-id="37097-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="37097-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="37097-122">Conversación (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="37097-122">Conversation (ConversationType)</span></span>](conversation-conversationtype.md) <br/> |<span data-ttu-id="37097-123">Representa una sola conversación.</span><span class="sxs-lookup"><span data-stu-id="37097-123">Represents a single conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="37097-124">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="37097-124">Text value</span></span>

<span data-ttu-id="37097-125">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="37097-125">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="37097-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="37097-126">Remarks</span></span>

<span data-ttu-id="37097-127">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda Exchange Web Services.This elemento fue introdujo en Exchange Server 2010 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="37097-127">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="37097-128">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="37097-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="37097-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="37097-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="37097-130">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="37097-130">Schema name</span></span>  <br/> |<span data-ttu-id="37097-131">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="37097-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="37097-132">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="37097-132">Validation file</span></span>  <br/> |<span data-ttu-id="37097-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="37097-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="37097-134">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="37097-134">Can be empty</span></span>  <br/> |<span data-ttu-id="37097-135">False</span><span class="sxs-lookup"><span data-stu-id="37097-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="37097-136">Ver también</span><span class="sxs-lookup"><span data-stu-id="37097-136">See also</span></span>



[<span data-ttu-id="37097-137">Operación de FindConversation</span><span class="sxs-lookup"><span data-stu-id="37097-137">FindConversation operation</span></span>](findconversation-operation.md)
  
[<span data-ttu-id="37097-138">Operación ApplyConversationAction</span><span class="sxs-lookup"><span data-stu-id="37097-138">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)


[<span data-ttu-id="37097-139">Conversaciones de EWS</span><span class="sxs-lookup"><span data-stu-id="37097-139">Conversations in EWS</span></span>](http://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)

