---
title: Conversación (ConversationType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Conversation
api_type:
- schema
ms.assetid: 59d014cd-5886-49ea-8d36-ba5de7e675de
description: El elemento Conversation representa una única conversación.
ms.openlocfilehash: 9969a6cfe1f977b1c24e03771f231f4eb03d1ac6
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458939"
---
# <a name="conversation-conversationtype"></a><span data-ttu-id="fba46-103">Conversación (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="fba46-103">Conversation (ConversationType)</span></span>

<span data-ttu-id="fba46-104">El elemento **Conversation** representa una única conversación.</span><span class="sxs-lookup"><span data-stu-id="fba46-104">The **Conversation** element represents a single conversation.</span></span> 
  
[<span data-ttu-id="fba46-105">FindConversationResponse</span><span class="sxs-lookup"><span data-stu-id="fba46-105">FindConversationResponse</span></span>](findconversationresponse.md)
  
[<span data-ttu-id="fba46-106">Conversaciones</span><span class="sxs-lookup"><span data-stu-id="fba46-106">Conversations</span></span>](conversations-ex15websvcsotherref.md)
  
[<span data-ttu-id="fba46-107">Conversación (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="fba46-107">Conversation (ConversationType)</span></span>](conversation-conversationtype.md)
  
```XML
<Conversation>
   <ConversationId/>
   <ConversationTopic/>
   <UniqueRecipients/>
   <GlobalUniqueRecipients/>
   <UniqueUnreadSenders/>
   <GlobalUniqueUnreadSenders/>
   <UniqueSenders/>
   <GlobalUniqueSenders/>
   <LastDeliveryTime/>
   <GlobalLastDeliveryTime/>
   <Categories/>
   <GlobalCategories/>
   <FlagStatus/>
   <GlobalFlagStatus/>
   <HasAttachments/>
   <GlobalHasAttachments/>
   <MessageCount/>
   <GlobalMessageCount/>
   <UnreadCount/>
   <GlobalUnreadCount/>
   <Size/>   <GlobalSize/>
   <ItemClasses/>
   <GlobalItemClasses/>
   <Importance/>
   <GlobalImportance/>
   <ItemIds/>
   <GlobalItemIds/>
</Conversation>
```

 <span data-ttu-id="fba46-108">**ConversationType**</span><span class="sxs-lookup"><span data-stu-id="fba46-108">**ConversationType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="fba46-109">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="fba46-109">Attributes and elements</span></span>

<span data-ttu-id="fba46-110">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="fba46-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fba46-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="fba46-111">Attributes</span></span>

<span data-ttu-id="fba46-112">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="fba46-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="fba46-113">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="fba46-113">Child elements</span></span>

|<span data-ttu-id="fba46-114">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="fba46-114">**Element**</span></span>|<span data-ttu-id="fba46-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="fba46-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fba46-116">ConversationId</span><span class="sxs-lookup"><span data-stu-id="fba46-116">ConversationId</span></span>](conversationid.md) <br/> |<span data-ttu-id="fba46-117">Representa el identificador de una conversación.</span><span class="sxs-lookup"><span data-stu-id="fba46-117">Represents the identifier of a conversation.</span></span>  <br/> |
|[<span data-ttu-id="fba46-118">ConversationTopic</span><span class="sxs-lookup"><span data-stu-id="fba46-118">ConversationTopic</span></span>](conversationtopic.md) <br/> |<span data-ttu-id="fba46-119">Representa el tema de conversación.</span><span class="sxs-lookup"><span data-stu-id="fba46-119">Represents the conversation topic.</span></span> <span data-ttu-id="fba46-120">Este elemento es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="fba46-120">This element is read-only.</span></span>  <br/> |
|[<span data-ttu-id="fba46-121">UniqueRecipients</span><span class="sxs-lookup"><span data-stu-id="fba46-121">UniqueRecipients</span></span>](uniquerecipients.md) <br/> |<span data-ttu-id="fba46-122">Contiene la lista de destinatarios de una conversación agregada desde una carpeta determinada.</span><span class="sxs-lookup"><span data-stu-id="fba46-122">Contains the recipient list of a conversation aggregated from a particular folder.</span></span> <span data-ttu-id="fba46-123">Este elemento es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="fba46-123">This element is read-only.</span></span>  <br/> |
|[<span data-ttu-id="fba46-124">GlobalUniqueRecipients</span><span class="sxs-lookup"><span data-stu-id="fba46-124">GlobalUniqueRecipients</span></span>](globaluniquerecipients.md) <br/> |<span data-ttu-id="fba46-125">Contiene la lista de destinatarios de una conversación agregada en un buzón.</span><span class="sxs-lookup"><span data-stu-id="fba46-125">Contains the recipient list of a conversation aggregated across a mailbox.</span></span> <span data-ttu-id="fba46-126">Este elemento es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="fba46-126">This element is read-only.</span></span>  <br/> |
|[<span data-ttu-id="fba46-127">UniqueUnreadSenders</span><span class="sxs-lookup"><span data-stu-id="fba46-127">UniqueUnreadSenders</span></span>](uniqueunreadsenders.md) <br/> |<span data-ttu-id="fba46-128">Contiene una lista de todas las personas que han enviado mensajes que actualmente no están leídos en esta conversación en la carpeta actual.</span><span class="sxs-lookup"><span data-stu-id="fba46-128">Contains a list of all the people who have sent messages that are currently unread in this conversation in the current folder.</span></span> <span data-ttu-id="fba46-129">Este elemento es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="fba46-129">This element is read-only.</span></span>  <br/> |
|[<span data-ttu-id="fba46-130">GlobalUniqueUnreadSenders</span><span class="sxs-lookup"><span data-stu-id="fba46-130">GlobalUniqueUnreadSenders</span></span>](globaluniqueunreadsenders.md) <br/> |<span data-ttu-id="fba46-131">Contiene una lista de todas las personas que han enviado mensajes que actualmente no están leídos en esta conversación en todas las carpetas del buzón.</span><span class="sxs-lookup"><span data-stu-id="fba46-131">Contains a list of all the people who have sent messages that are currently unread in this conversation across all folders in the mailbox.</span></span>  <br/> |
|[<span data-ttu-id="fba46-132">UniqueSenders</span><span class="sxs-lookup"><span data-stu-id="fba46-132">UniqueSenders</span></span>](uniquesenders.md) <br/> |<span data-ttu-id="fba46-133">Contiene una lista de todos los remitentes de los elementos de conversación de la carpeta actual.</span><span class="sxs-lookup"><span data-stu-id="fba46-133">Contains a list of all the senders of conversation items in the current folder.</span></span> <span data-ttu-id="fba46-134">Este elemento es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="fba46-134">This element is read-only.</span></span>  <br/> |
|[<span data-ttu-id="fba46-135">GlobalUniqueSenders</span><span class="sxs-lookup"><span data-stu-id="fba46-135">GlobalUniqueSenders</span></span>](globaluniquesenders.md) <br/> |<span data-ttu-id="fba46-136">Contiene una lista de todos los remitentes de los elementos de la conversación en el buzón.</span><span class="sxs-lookup"><span data-stu-id="fba46-136">Contains a list of all the senders of conversation items in the mailbox.</span></span>  <br/> |
|[<span data-ttu-id="fba46-137">LastDeliveryTime</span><span class="sxs-lookup"><span data-stu-id="fba46-137">LastDeliveryTime</span></span>](lastdeliverytime.md) <br/> |<span data-ttu-id="fba46-138">Contiene la hora de entrega del mensaje que se recibió por última vez en esta conversación en la carpeta actual.</span><span class="sxs-lookup"><span data-stu-id="fba46-138">Contains the delivery time of the message that was last received in this conversation in the current folder.</span></span>  <br/> |
|[<span data-ttu-id="fba46-139">GlobalLastDeliveryTime</span><span class="sxs-lookup"><span data-stu-id="fba46-139">GlobalLastDeliveryTime</span></span>](globallastdeliverytime.md) <br/> |<span data-ttu-id="fba46-140">Contiene la hora de entrega del mensaje que se recibió por última vez en esta conversación en todas las carpetas del buzón.</span><span class="sxs-lookup"><span data-stu-id="fba46-140">Contains the delivery time of the message that was last received in this conversation across all folders in the mailbox.</span></span>  <br/> |
|[<span data-ttu-id="fba46-141">Categorías</span><span class="sxs-lookup"><span data-stu-id="fba46-141">Categories</span></span>](categories-ex15websvcsotherref.md) <br/> |<span data-ttu-id="fba46-142">Contiene una colección de cadenas que identifican las categorías que se aplican a todos los elementos de la conversación en la carpeta actual.</span><span class="sxs-lookup"><span data-stu-id="fba46-142">Contains a collection of strings that identify the categories that are applied to all conversation items in the current folder.</span></span>  <br/> |
|[<span data-ttu-id="fba46-143">GlobalCategories</span><span class="sxs-lookup"><span data-stu-id="fba46-143">GlobalCategories</span></span>](globalcategories.md) <br/> |<span data-ttu-id="fba46-144">Contiene la lista de categorías para todos los elementos de la conversación en un buzón.</span><span class="sxs-lookup"><span data-stu-id="fba46-144">Contains the category list for all conversation items in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="fba46-145">FlagStatus</span><span class="sxs-lookup"><span data-stu-id="fba46-145">FlagStatus</span></span>](flagstatus.md) <br/> |<span data-ttu-id="fba46-146">Contiene el estado de marca agregada para los elementos de la conversación en la carpeta actual.</span><span class="sxs-lookup"><span data-stu-id="fba46-146">Contains the aggregated flag status for conversation items in the current folder.</span></span>  <br/> |
|[<span data-ttu-id="fba46-147">GlobalFlagStatus</span><span class="sxs-lookup"><span data-stu-id="fba46-147">GlobalFlagStatus</span></span>](globalflagstatus.md) <br/> |<span data-ttu-id="fba46-148">Contiene el estado de marca agregada para todos los elementos de conversación en un buzón.</span><span class="sxs-lookup"><span data-stu-id="fba46-148">Contains the aggregated flag status for all conversation items in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="fba46-149">HasAttachments</span><span class="sxs-lookup"><span data-stu-id="fba46-149">HasAttachments</span></span>](hasattachments.md) <br/> |<span data-ttu-id="fba46-150">Contiene un valor que indica si al menos un elemento de la conversación de la carpeta actual tiene datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="fba46-150">Contains a value that indicates whether at least one conversation item in the current folder has an attachment.</span></span>  <br/> |
|[<span data-ttu-id="fba46-151">GlobalHasAttachments</span><span class="sxs-lookup"><span data-stu-id="fba46-151">GlobalHasAttachments</span></span>](globalhasattachments.md) <br/> |<span data-ttu-id="fba46-152">Contiene un valor que indica si al menos un elemento de conversación de un buzón tiene datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="fba46-152">Contains a value that indicates whether at least one conversation item in a mailbox has an attachment.</span></span>  <br/> |
|[<span data-ttu-id="fba46-153">MessageCount</span><span class="sxs-lookup"><span data-stu-id="fba46-153">MessageCount</span></span>](messagecount.md) <br/> |<span data-ttu-id="fba46-154">Contiene el número total de elementos de la conversación en la carpeta actual.</span><span class="sxs-lookup"><span data-stu-id="fba46-154">Contains the total number of conversation items in the current folder.</span></span>  <br/> |
|[<span data-ttu-id="fba46-155">GlobalMessageCount</span><span class="sxs-lookup"><span data-stu-id="fba46-155">GlobalMessageCount</span></span>](globalmessagecount.md) <br/> |<span data-ttu-id="fba46-156">Contiene el número total de elementos de la conversación en el buzón.</span><span class="sxs-lookup"><span data-stu-id="fba46-156">Contains the total number of conversation items in the mailbox.</span></span>  <br/> |
|[<span data-ttu-id="fba46-157">UnreadCount</span><span class="sxs-lookup"><span data-stu-id="fba46-157">UnreadCount</span></span>](unreadcount.md) <br/> |<span data-ttu-id="fba46-158">Contiene el número de elementos de conversación no leídos dentro de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="fba46-158">Contains the count of unread conversation items within a folder.</span></span>  <br/> |
|[<span data-ttu-id="fba46-159">GlobalUnreadCount</span><span class="sxs-lookup"><span data-stu-id="fba46-159">GlobalUnreadCount</span></span>](globalunreadcount.md) <br/> |<span data-ttu-id="fba46-160">Contiene un recuento de todos los elementos de conversación no leídos del buzón.</span><span class="sxs-lookup"><span data-stu-id="fba46-160">Contains a count of all the unread conversation items in the mailbox.</span></span>  <br/> |
|[<span data-ttu-id="fba46-161">Tamaño</span><span class="sxs-lookup"><span data-stu-id="fba46-161">Size</span></span>](size.md) <br/> |<span data-ttu-id="fba46-162">Contiene el tamaño de conversación calculado a partir del tamaño de todos los elementos de la conversación en la carpeta actual.</span><span class="sxs-lookup"><span data-stu-id="fba46-162">Contains the conversation size calculated from the size of all conversation items in the current folder.</span></span>  <br/> |
|[<span data-ttu-id="fba46-163">GlobalSize</span><span class="sxs-lookup"><span data-stu-id="fba46-163">GlobalSize</span></span>](globalsize.md) <br/> |<span data-ttu-id="fba46-164">Contiene el tamaño de la conversación calculado a partir del tamaño de todos los elementos de la conversación en el buzón.</span><span class="sxs-lookup"><span data-stu-id="fba46-164">Contains the size of the conversation calculated from the size of all conversation items in the mailbox.</span></span>  <br/> |
|[<span data-ttu-id="fba46-165">ItemClasses (ArrayOfItemClassType)</span><span class="sxs-lookup"><span data-stu-id="fba46-165">ItemClasses (ArrayOfItemClassType)</span></span>](itemclasses-arrayofitemclasstype.md) <br/> |<span data-ttu-id="fba46-166">Contiene una lista de clases de elementos que representa todas las clases de elementos de los elementos de la conversación de la carpeta actual.</span><span class="sxs-lookup"><span data-stu-id="fba46-166">Contains a list of item classes that represents all the item classes of the conversation items in the current folder.</span></span>  <br/> |
|[<span data-ttu-id="fba46-167">GlobalItemClasses</span><span class="sxs-lookup"><span data-stu-id="fba46-167">GlobalItemClasses</span></span>](globalitemclasses.md) <br/> |<span data-ttu-id="fba46-168">Contiene una lista de clases de elementos que representa todas las clases de elementos de los elementos de la conversación en un buzón.</span><span class="sxs-lookup"><span data-stu-id="fba46-168">Contains a list of item classes that represents all the item classes of the conversation items in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="fba46-169">Importance</span><span class="sxs-lookup"><span data-stu-id="fba46-169">Importance</span></span>](importance.md) <br/> |<span data-ttu-id="fba46-170">Contiene la importancia agregada para todos los elementos de la conversación de la carpeta actual.</span><span class="sxs-lookup"><span data-stu-id="fba46-170">Contains the aggregated importance for all conversation items in the current folder.</span></span>  <br/> |
|[<span data-ttu-id="fba46-171">GlobalImportance</span><span class="sxs-lookup"><span data-stu-id="fba46-171">GlobalImportance</span></span>](globalimportance.md) <br/> |<span data-ttu-id="fba46-172">Contiene la importancia agregada para todos los elementos de la conversación en un buzón.</span><span class="sxs-lookup"><span data-stu-id="fba46-172">Contains the aggregated importance for all conversation items in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="fba46-173">ItemIds</span><span class="sxs-lookup"><span data-stu-id="fba46-173">ItemIds</span></span>](itemids.md) <br/> |<span data-ttu-id="fba46-174">Contiene la colección de identificadores de elemento para todos los elementos de la conversación en la carpeta actual.</span><span class="sxs-lookup"><span data-stu-id="fba46-174">Contains the collection of item identifiers for all conversation items in the current folder.</span></span>  <br/> |
|[<span data-ttu-id="fba46-175">GlobalItemIds</span><span class="sxs-lookup"><span data-stu-id="fba46-175">GlobalItemIds</span></span>](globalitemids.md) <br/> |<span data-ttu-id="fba46-176">Contiene la colección de identificadores de elemento para todos los elementos de conversación en un buzón.</span><span class="sxs-lookup"><span data-stu-id="fba46-176">Contains the collection of item identifiers for all conversation items in a mailbox.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="fba46-177">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="fba46-177">Parent elements</span></span>

|<span data-ttu-id="fba46-178">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="fba46-178">**Element**</span></span>|<span data-ttu-id="fba46-179">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="fba46-179">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fba46-180">Conversaciones</span><span class="sxs-lookup"><span data-stu-id="fba46-180">Conversations</span></span>](conversations-ex15websvcsotherref.md) <br/> |<span data-ttu-id="fba46-181">Contiene una matriz de conversaciones que se devuelven en la respuesta **FindConversation** .</span><span class="sxs-lookup"><span data-stu-id="fba46-181">Contains an array of conversations that are returned in the **FindConversation** response.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="fba46-182">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="fba46-182">Text value</span></span>

<span data-ttu-id="fba46-183">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="fba46-183">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="fba46-184">Comentarios</span><span class="sxs-lookup"><span data-stu-id="fba46-184">Remarks</span></span>

<span data-ttu-id="fba46-185">El esquema que describe este elemento se encuentra en el directorio virtual de IIS que hospeda los servicios Web de Exchange. este elemento se introdujo en Exchange Server 2010 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="fba46-185">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fba46-186">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="fba46-186">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fba46-187">Namespace</span><span class="sxs-lookup"><span data-stu-id="fba46-187">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="fba46-188">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="fba46-188">Schema name</span></span>  <br/> |<span data-ttu-id="fba46-189">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="fba46-189">Types schema</span></span>  <br/> |
|<span data-ttu-id="fba46-190">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="fba46-190">Validation file</span></span>  <br/> |<span data-ttu-id="fba46-191">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="fba46-191">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="fba46-192">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="fba46-192">Can be empty</span></span>  <br/> |<span data-ttu-id="fba46-193">Falso</span><span class="sxs-lookup"><span data-stu-id="fba46-193">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fba46-194">Vea también</span><span class="sxs-lookup"><span data-stu-id="fba46-194">See also</span></span>



[<span data-ttu-id="fba46-195">Operación FindConversation</span><span class="sxs-lookup"><span data-stu-id="fba46-195">FindConversation operation</span></span>](findconversation-operation.md)
  
[<span data-ttu-id="fba46-196">Operación ApplyConversationAction</span><span class="sxs-lookup"><span data-stu-id="fba46-196">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)


[<span data-ttu-id="fba46-197">Conversaciones en EWS</span><span class="sxs-lookup"><span data-stu-id="fba46-197">Conversations in EWS</span></span>](https://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)

