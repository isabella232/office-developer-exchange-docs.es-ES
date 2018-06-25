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
description: El elemento de conversación representa una sola conversación.
ms.openlocfilehash: e1ae055d6a77fc5a9b483341830b978e0c1a5b5a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763870"
---
# <a name="conversation-conversationtype"></a><span data-ttu-id="54a5f-103">Conversación (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="54a5f-103">Conversation (ConversationType)</span></span>

<span data-ttu-id="54a5f-104">El elemento de **conversación** representa una sola conversación.</span><span class="sxs-lookup"><span data-stu-id="54a5f-104">The **Conversation** element represents a single conversation.</span></span> 
  
[<span data-ttu-id="54a5f-105">FindConversationResponse</span><span class="sxs-lookup"><span data-stu-id="54a5f-105">FindConversationResponse</span></span>](findconversationresponse.md)
  
[<span data-ttu-id="54a5f-106">Conversaciones</span><span class="sxs-lookup"><span data-stu-id="54a5f-106">Conversations</span></span>](conversations-ex15websvcsotherref.md)
  
[<span data-ttu-id="54a5f-107">Conversación (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="54a5f-107">Conversation (ConversationType)</span></span>](conversation-conversationtype.md)
  
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

 <span data-ttu-id="54a5f-108">**ConversationType**</span><span class="sxs-lookup"><span data-stu-id="54a5f-108">**ConversationType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="54a5f-109">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="54a5f-109">Attributes and elements</span></span>

<span data-ttu-id="54a5f-110">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="54a5f-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="54a5f-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="54a5f-111">Attributes</span></span>

<span data-ttu-id="54a5f-112">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="54a5f-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="54a5f-113">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="54a5f-113">Child elements</span></span>

|<span data-ttu-id="54a5f-114">**Element**</span><span class="sxs-lookup"><span data-stu-id="54a5f-114">**Element**</span></span>|<span data-ttu-id="54a5f-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="54a5f-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="54a5f-116">ConversationId</span><span class="sxs-lookup"><span data-stu-id="54a5f-116">ConversationId</span></span>](conversationid.md) <br/> |<span data-ttu-id="54a5f-117">Representa el identificador de una conversación.</span><span class="sxs-lookup"><span data-stu-id="54a5f-117">Represents the identifier of a conversation.</span></span>  <br/> |
|[<span data-ttu-id="54a5f-118">ConversationTopic</span><span class="sxs-lookup"><span data-stu-id="54a5f-118">ConversationTopic</span></span>](conversationtopic.md) <br/> |<span data-ttu-id="54a5f-119">Representa el tema de conversación.</span><span class="sxs-lookup"><span data-stu-id="54a5f-119">Represents the conversation topic.</span></span> <span data-ttu-id="54a5f-120">Este elemento es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="54a5f-120">This element is read-only.</span></span>  <br/> |
|[<span data-ttu-id="54a5f-121">UniqueRecipients</span><span class="sxs-lookup"><span data-stu-id="54a5f-121">UniqueRecipients</span></span>](uniquerecipients.md) <br/> |<span data-ttu-id="54a5f-122">Contiene la lista de destinatarios de una conversación de agregados de una carpeta determinada.</span><span class="sxs-lookup"><span data-stu-id="54a5f-122">Contains the recipient list of a conversation aggregated from a particular folder.</span></span> <span data-ttu-id="54a5f-123">Este elemento es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="54a5f-123">This element is read-only.</span></span>  <br/> |
|[<span data-ttu-id="54a5f-124">GlobalUniqueRecipients</span><span class="sxs-lookup"><span data-stu-id="54a5f-124">GlobalUniqueRecipients</span></span>](globaluniquerecipients.md) <br/> |<span data-ttu-id="54a5f-125">Contiene la lista de destinatarios de una conversación agregada a través de un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="54a5f-125">Contains the recipient list of a conversation aggregated across a mailbox.</span></span> <span data-ttu-id="54a5f-126">Este elemento es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="54a5f-126">This element is read-only.</span></span>  <br/> |
|[<span data-ttu-id="54a5f-127">UniqueUnreadSenders</span><span class="sxs-lookup"><span data-stu-id="54a5f-127">UniqueUnreadSenders</span></span>](uniqueunreadsenders.md) <br/> |<span data-ttu-id="54a5f-128">Contiene una lista de todas las personas que han enviado los mensajes que están actualmente no leídos en esta conversación en la carpeta actual.</span><span class="sxs-lookup"><span data-stu-id="54a5f-128">Contains a list of all the people who have sent messages that are currently unread in this conversation in the current folder.</span></span> <span data-ttu-id="54a5f-129">Este elemento es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="54a5f-129">This element is read-only.</span></span>  <br/> |
|[<span data-ttu-id="54a5f-130">GlobalUniqueUnreadSenders</span><span class="sxs-lookup"><span data-stu-id="54a5f-130">GlobalUniqueUnreadSenders</span></span>](globaluniqueunreadsenders.md) <br/> |<span data-ttu-id="54a5f-131">Contiene una lista de todas las personas que han enviado los mensajes que están actualmente no leídos en esta conversación a través de todas las carpetas del buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="54a5f-131">Contains a list of all the people who have sent messages that are currently unread in this conversation across all folders in the mailbox.</span></span>  <br/> |
|[<span data-ttu-id="54a5f-132">UniqueSenders</span><span class="sxs-lookup"><span data-stu-id="54a5f-132">UniqueSenders</span></span>](uniquesenders.md) <br/> |<span data-ttu-id="54a5f-133">Contiene una lista de todos los remitentes de los elementos de una conversación en la carpeta actual.</span><span class="sxs-lookup"><span data-stu-id="54a5f-133">Contains a list of all the senders of conversation items in the current folder.</span></span> <span data-ttu-id="54a5f-134">Este elemento es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="54a5f-134">This element is read-only.</span></span>  <br/> |
|[<span data-ttu-id="54a5f-135">GlobalUniqueSenders</span><span class="sxs-lookup"><span data-stu-id="54a5f-135">GlobalUniqueSenders</span></span>](globaluniquesenders.md) <br/> |<span data-ttu-id="54a5f-136">Contiene una lista de todos los remitentes de los elementos de la conversación en el buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="54a5f-136">Contains a list of all the senders of conversation items in the mailbox.</span></span>  <br/> |
|[<span data-ttu-id="54a5f-137">LastDeliveryTime</span><span class="sxs-lookup"><span data-stu-id="54a5f-137">LastDeliveryTime</span></span>](lastdeliverytime.md) <br/> |<span data-ttu-id="54a5f-138">Contiene la hora de entrega del mensaje que se recibió por última vez en esta conversación en la carpeta actual.</span><span class="sxs-lookup"><span data-stu-id="54a5f-138">Contains the delivery time of the message that was last received in this conversation in the current folder.</span></span>  <br/> |
|[<span data-ttu-id="54a5f-139">GlobalLastDeliveryTime</span><span class="sxs-lookup"><span data-stu-id="54a5f-139">GlobalLastDeliveryTime</span></span>](globallastdeliverytime.md) <br/> |<span data-ttu-id="54a5f-140">Contiene la hora de entrega del mensaje que se recibió por última vez en esta conversación a través de todas las carpetas del buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="54a5f-140">Contains the delivery time of the message that was last received in this conversation across all folders in the mailbox.</span></span>  <br/> |
|[<span data-ttu-id="54a5f-141">Categories</span><span class="sxs-lookup"><span data-stu-id="54a5f-141">Categories</span></span>](categories-ex15websvcsotherref.md) <br/> |<span data-ttu-id="54a5f-142">Contiene una colección de cadenas que identifican las categorías que se aplican a todos los elementos de una conversación en la carpeta actual.</span><span class="sxs-lookup"><span data-stu-id="54a5f-142">Contains a collection of strings that identify the categories that are applied to all conversation items in the current folder.</span></span>  <br/> |
|[<span data-ttu-id="54a5f-143">GlobalCategories</span><span class="sxs-lookup"><span data-stu-id="54a5f-143">GlobalCategories</span></span>](globalcategories.md) <br/> |<span data-ttu-id="54a5f-144">Contiene la lista de categorías para todos los elementos de la conversación en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="54a5f-144">Contains the category list for all conversation items in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="54a5f-145">FlagStatus</span><span class="sxs-lookup"><span data-stu-id="54a5f-145">FlagStatus</span></span>](flagstatus.md) <br/> |<span data-ttu-id="54a5f-146">Contiene el estado del indicador agregados por los elementos de conversación en la carpeta actual.</span><span class="sxs-lookup"><span data-stu-id="54a5f-146">Contains the aggregated flag status for conversation items in the current folder.</span></span>  <br/> |
|[<span data-ttu-id="54a5f-147">GlobalFlagStatus</span><span class="sxs-lookup"><span data-stu-id="54a5f-147">GlobalFlagStatus</span></span>](globalflagstatus.md) <br/> |<span data-ttu-id="54a5f-148">Contiene el estado del indicador agregada para todos los elementos de la conversación en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="54a5f-148">Contains the aggregated flag status for all conversation items in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="54a5f-149">HasAttachments</span><span class="sxs-lookup"><span data-stu-id="54a5f-149">HasAttachments</span></span>](hasattachments.md) <br/> |<span data-ttu-id="54a5f-150">Contiene un valor que indica si el elemento de al menos una conversación en la carpeta actual tiene datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="54a5f-150">Contains a value that indicates whether at least one conversation item in the current folder has an attachment.</span></span>  <br/> |
|[<span data-ttu-id="54a5f-151">GlobalHasAttachments</span><span class="sxs-lookup"><span data-stu-id="54a5f-151">GlobalHasAttachments</span></span>](globalhasattachments.md) <br/> |<span data-ttu-id="54a5f-152">Contiene un valor que indica si el elemento de al menos una conversación en un buzón tiene datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="54a5f-152">Contains a value that indicates whether at least one conversation item in a mailbox has an attachment.</span></span>  <br/> |
|[<span data-ttu-id="54a5f-153">MessageCount</span><span class="sxs-lookup"><span data-stu-id="54a5f-153">MessageCount</span></span>](messagecount.md) <br/> |<span data-ttu-id="54a5f-154">Contiene el número total de elementos de una conversación en la carpeta actual.</span><span class="sxs-lookup"><span data-stu-id="54a5f-154">Contains the total number of conversation items in the current folder.</span></span>  <br/> |
|[<span data-ttu-id="54a5f-155">GlobalMessageCount</span><span class="sxs-lookup"><span data-stu-id="54a5f-155">GlobalMessageCount</span></span>](globalmessagecount.md) <br/> |<span data-ttu-id="54a5f-156">Contiene el número total de elementos de la conversación en el buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="54a5f-156">Contains the total number of conversation items in the mailbox.</span></span>  <br/> |
|[<span data-ttu-id="54a5f-157">UnreadCount</span><span class="sxs-lookup"><span data-stu-id="54a5f-157">UnreadCount</span></span>](unreadcount.md) <br/> |<span data-ttu-id="54a5f-158">Contiene el recuento de elementos no leídos conversación dentro de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="54a5f-158">Contains the count of unread conversation items within a folder.</span></span>  <br/> |
|[<span data-ttu-id="54a5f-159">GlobalUnreadCount</span><span class="sxs-lookup"><span data-stu-id="54a5f-159">GlobalUnreadCount</span></span>](globalunreadcount.md) <br/> |<span data-ttu-id="54a5f-160">Contiene un recuento de todos los elementos no leídos de conversación en el buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="54a5f-160">Contains a count of all the unread conversation items in the mailbox.</span></span>  <br/> |
|[<span data-ttu-id="54a5f-161">Size</span><span class="sxs-lookup"><span data-stu-id="54a5f-161">Size</span></span>](size.md) <br/> |<span data-ttu-id="54a5f-162">Contiene el tamaño de conversación que se calcula a partir del tamaño de todos los elementos de una conversación en la carpeta actual.</span><span class="sxs-lookup"><span data-stu-id="54a5f-162">Contains the conversation size calculated from the size of all conversation items in the current folder.</span></span>  <br/> |
|[<span data-ttu-id="54a5f-163">GlobalSize</span><span class="sxs-lookup"><span data-stu-id="54a5f-163">GlobalSize</span></span>](globalsize.md) <br/> |<span data-ttu-id="54a5f-164">Contiene el tamaño de la conversación que se calcula a partir del tamaño de todos los elementos de la conversación en el buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="54a5f-164">Contains the size of the conversation calculated from the size of all conversation items in the mailbox.</span></span>  <br/> |
|[<span data-ttu-id="54a5f-165">ItemClasses (ArrayOfItemClassType)</span><span class="sxs-lookup"><span data-stu-id="54a5f-165">ItemClasses (ArrayOfItemClassType)</span></span>](itemclasses-arrayofitemclasstype.md) <br/> |<span data-ttu-id="54a5f-166">Contiene una lista de las clases de elementos que representa todas las clases de elemento de los elementos de conversación en la carpeta actual.</span><span class="sxs-lookup"><span data-stu-id="54a5f-166">Contains a list of item classes that represents all the item classes of the conversation items in the current folder.</span></span>  <br/> |
|[<span data-ttu-id="54a5f-167">GlobalItemClasses</span><span class="sxs-lookup"><span data-stu-id="54a5f-167">GlobalItemClasses</span></span>](globalitemclasses.md) <br/> |<span data-ttu-id="54a5f-168">Contiene una lista de las clases de elementos que representa todas las clases de elemento de los elementos de la conversación en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="54a5f-168">Contains a list of item classes that represents all the item classes of the conversation items in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="54a5f-169">Importancia</span><span class="sxs-lookup"><span data-stu-id="54a5f-169">Importance</span></span>](importance.md) <br/> |<span data-ttu-id="54a5f-170">Contiene la importancia agregada para todos los elementos de una conversación en la carpeta actual.</span><span class="sxs-lookup"><span data-stu-id="54a5f-170">Contains the aggregated importance for all conversation items in the current folder.</span></span>  <br/> |
|[<span data-ttu-id="54a5f-171">GlobalImportance</span><span class="sxs-lookup"><span data-stu-id="54a5f-171">GlobalImportance</span></span>](globalimportance.md) <br/> |<span data-ttu-id="54a5f-172">Contiene la importancia agregada para todos los elementos de la conversación en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="54a5f-172">Contains the aggregated importance for all conversation items in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="54a5f-173">ItemId</span><span class="sxs-lookup"><span data-stu-id="54a5f-173">ItemIds</span></span>](itemids.md) <br/> |<span data-ttu-id="54a5f-174">Contiene la colección de identificadores de elemento para todos los elementos de una conversación en la carpeta actual.</span><span class="sxs-lookup"><span data-stu-id="54a5f-174">Contains the collection of item identifiers for all conversation items in the current folder.</span></span>  <br/> |
|[<span data-ttu-id="54a5f-175">GlobalItemIds</span><span class="sxs-lookup"><span data-stu-id="54a5f-175">GlobalItemIds</span></span>](globalitemids.md) <br/> |<span data-ttu-id="54a5f-176">Contiene la colección de identificadores de elemento para todos los elementos de la conversación en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="54a5f-176">Contains the collection of item identifiers for all conversation items in a mailbox.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="54a5f-177">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="54a5f-177">Parent elements</span></span>

|<span data-ttu-id="54a5f-178">**Element**</span><span class="sxs-lookup"><span data-stu-id="54a5f-178">**Element**</span></span>|<span data-ttu-id="54a5f-179">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="54a5f-179">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="54a5f-180">Conversaciones</span><span class="sxs-lookup"><span data-stu-id="54a5f-180">Conversations</span></span>](conversations-ex15websvcsotherref.md) <br/> |<span data-ttu-id="54a5f-181">Contiene una matriz de las conversaciones que se devuelven en la respuesta de **FindConversation** .</span><span class="sxs-lookup"><span data-stu-id="54a5f-181">Contains an array of conversations that are returned in the **FindConversation** response.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="54a5f-182">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="54a5f-182">Text value</span></span>

<span data-ttu-id="54a5f-183">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="54a5f-183">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="54a5f-184">Comentarios</span><span class="sxs-lookup"><span data-stu-id="54a5f-184">Remarks</span></span>

<span data-ttu-id="54a5f-185">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda Exchange Web Services.This elemento fue introdujo en Exchange Server 2010 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="54a5f-185">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="54a5f-186">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="54a5f-186">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="54a5f-187">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="54a5f-187">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="54a5f-188">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="54a5f-188">Schema name</span></span>  <br/> |<span data-ttu-id="54a5f-189">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="54a5f-189">Types schema</span></span>  <br/> |
|<span data-ttu-id="54a5f-190">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="54a5f-190">Validation file</span></span>  <br/> |<span data-ttu-id="54a5f-191">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="54a5f-191">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="54a5f-192">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="54a5f-192">Can be empty</span></span>  <br/> |<span data-ttu-id="54a5f-193">False</span><span class="sxs-lookup"><span data-stu-id="54a5f-193">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="54a5f-194">Vea también</span><span class="sxs-lookup"><span data-stu-id="54a5f-194">See also</span></span>



[<span data-ttu-id="54a5f-195">Operación de FindConversation</span><span class="sxs-lookup"><span data-stu-id="54a5f-195">FindConversation operation</span></span>](findconversation-operation.md)
  
[<span data-ttu-id="54a5f-196">Operación ApplyConversationAction</span><span class="sxs-lookup"><span data-stu-id="54a5f-196">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)


[<span data-ttu-id="54a5f-197">Conversaciones de EWS</span><span class="sxs-lookup"><span data-stu-id="54a5f-197">Conversations in EWS</span></span>](http://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)

