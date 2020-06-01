---
title: Operación GetConversationItems
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8ae00a99-b37b-4194-829c-fe300db6ab99
description: Busca información sobre la operación GetConversationItems.
ms.openlocfilehash: ddeb5386e56653a32ca2e6d212518704cd0f0c58
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457784"
---
# <a name="getconversationitems-operation"></a><span data-ttu-id="c7cd6-103">Operación GetConversationItems</span><span class="sxs-lookup"><span data-stu-id="c7cd6-103">GetConversationItems operation</span></span>

<span data-ttu-id="c7cd6-104">Busca información sobre la operación **GetConversationItems** .</span><span class="sxs-lookup"><span data-stu-id="c7cd6-104">Find information about the **GetConversationItems** operation.</span></span> 
  
<span data-ttu-id="c7cd6-105">La operación **GetConversationItems** obtiene uno o más conjuntos de elementos que están organizados en nodos en una conversación.</span><span class="sxs-lookup"><span data-stu-id="c7cd6-105">The **GetConversationItems** operation gets one or more sets of items that are organized in to nodes in a conversation.</span></span> 
  
<span data-ttu-id="c7cd6-106">Esta operación se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="c7cd6-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-getconversationitems-operation"></a><span data-ttu-id="c7cd6-107">Uso de la operación GetConversationItems</span><span class="sxs-lookup"><span data-stu-id="c7cd6-107">Using the GetConversationItems operation</span></span>

<span data-ttu-id="c7cd6-108">Puede usar la operación **GetConversationItems** para obtener elementos en las conversaciones tanto para los buzones de correo principales como para los de archivo.</span><span class="sxs-lookup"><span data-stu-id="c7cd6-108">You can use the **GetConversationItems** operation to get items in conversations for both primary and archive mailboxes.</span></span> 
  
### <a name="getconversationitems-operation-soap-headers"></a><span data-ttu-id="c7cd6-109">Encabezados SOAP de operación GetConversationItems</span><span class="sxs-lookup"><span data-stu-id="c7cd6-109">GetConversationItems operation SOAP headers</span></span>

<span data-ttu-id="c7cd6-110">La operación **GetConversationItems** puede usar los encabezados SOAP que se enumeran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="c7cd6-110">The **GetConversationItems** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="c7cd6-111">**Nombre de encabezado**</span><span class="sxs-lookup"><span data-stu-id="c7cd6-111">**Header name**</span></span>|<span data-ttu-id="c7cd6-112">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="c7cd6-112">**Element**</span></span>|<span data-ttu-id="c7cd6-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c7cd6-113">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c7cd6-114">**Suplantación**</span><span class="sxs-lookup"><span data-stu-id="c7cd6-114">**Impersonation**</span></span> <br/> |[<span data-ttu-id="c7cd6-115">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="c7cd6-115">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="c7cd6-116">Identifica al usuario que está suplantando la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="c7cd6-116">Identifies the user whom the client application is impersonating.</span></span> <span data-ttu-id="c7cd6-117">Este encabezado se aplica a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="c7cd6-117">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="c7cd6-118">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="c7cd6-118">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="c7cd6-119">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="c7cd6-119">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="c7cd6-120">Identifica la versión del esquema para la solicitud de operación.</span><span class="sxs-lookup"><span data-stu-id="c7cd6-120">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="c7cd6-121">El valor mínimo para este elemento es **Exchange2013**.</span><span class="sxs-lookup"><span data-stu-id="c7cd6-121">The minimum value for this element is **Exchange2013**.</span></span> <span data-ttu-id="c7cd6-122">Este encabezado se aplica a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="c7cd6-122">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="c7cd6-123">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="c7cd6-123">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="c7cd6-124">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="c7cd6-124">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="c7cd6-125">Identifica la versión del servidor que respondió a la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c7cd6-125">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="c7cd6-126">Este encabezado se aplica a una respuesta.</span><span class="sxs-lookup"><span data-stu-id="c7cd6-126">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="getconversationitems-operation-request-example-get-items-in-a-single-conversation"></a><span data-ttu-id="c7cd6-127">Ejemplo de solicitud de operación GetConversationItems: obtener elementos en una sola conversación</span><span class="sxs-lookup"><span data-stu-id="c7cd6-127">GetConversationItems operation request example: Get items in a single conversation</span></span>

<span data-ttu-id="c7cd6-128">El siguiente ejemplo de una solicitud de operación de **GetConversationItems** muestra cómo obtener todos los elementos de la conversación en una sola conversación, con la excepción de los elementos que se encuentran en las carpetas elementos eliminados y borradores.</span><span class="sxs-lookup"><span data-stu-id="c7cd6-128">The following example of a **GetConversationItems** operation request shows how to get all conversation items in a single conversation, with the exception of items located in the Deleted Items and Drafts folders.</span></span> <span data-ttu-id="c7cd6-129">Cada elemento devuelto en la respuesta contendrá un identificador de elemento, un asunto y la hora en que se recibió el elemento en el buzón.</span><span class="sxs-lookup"><span data-stu-id="c7cd6-129">Each item returned in the response will contain an item identifier, a subject, and the time that the item was received in the mailbox.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="c7cd6-130">Todos los identificadores de elemento y las claves de cambio de este artículo se han reducido para preservar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="c7cd6-130">All item identifiers and change keys in this article have been shortened to preserve readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013" />
   </soap:Header>
   <soap:Body>
      <m:GetConversationItems>
         <m:ItemShape>
            <t:BaseShape>IdOnly</t:BaseShape>
            <t:AdditionalProperties>
               <t:FieldURI FieldURI="item:Subject" />
               <t:FieldURI FieldURI="item:DateTimeReceived" />
            </t:AdditionalProperties>
         </m:ItemShape>
         <m:FoldersToIgnore>
            <t:DistinguishedFolderId Id="deleteditems" />
            <t:DistinguishedFolderId Id="drafts" />
         </m:FoldersToIgnore>
         <m:SortOrder>TreeOrderDescending</m:SortOrder>
         <m:Conversations>
            <t:Conversation>
               <t:ConversationId Id="AAQkADEzOTExYjJkakJCs=" />
            </t:Conversation>
         </m:Conversations>
      </m:GetConversationItems>
   </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="c7cd6-131">En este ejemplo de una solicitud **GetConversationItems** no se incluyen las siguientes opciones:</span><span class="sxs-lookup"><span data-stu-id="c7cd6-131">This example of a **GetConversationItems** request does not include the following options:</span></span> 
  
- <span data-ttu-id="c7cd6-132">El elemento [MaxItemsToReturn](maxitemstoreturn.md) , que establece el número máximo de elementos que se devolverá en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c7cd6-132">The [MaxItemsToReturn](maxitemstoreturn.md) element, which sets the maximum number of items to return in the response.</span></span> 
    
- <span data-ttu-id="c7cd6-133">El elemento [MailboxScope](mailboxscope.md) , que establece el ámbito del buzón de correo indicando si la operación **GetConversationItems** debe realizarse en el buzón principal, el buzón de archivo o ambos buzones.</span><span class="sxs-lookup"><span data-stu-id="c7cd6-133">The [MailboxScope](mailboxscope.md) element, which sets the mailbox scope by indicating whether the **GetConversationItems** operation is to be performed on the primary mailbox, the archive mailbox, or both mailboxes.</span></span> 
    
- <span data-ttu-id="c7cd6-134">El elemento [SyncState (base64Binary)](syncstate-base64binary.md) , que establece el estado de sincronización para obtener solo los elementos de la conversación que son nuevos o se actualizan en la conversación.</span><span class="sxs-lookup"><span data-stu-id="c7cd6-134">The [SyncState (base64Binary)](syncstate-base64binary.md) element, which sets the synchronization state to only get conversation items that are new or updated in the conversation.</span></span> <span data-ttu-id="c7cd6-135">Este elemento se establece para cada conversación.</span><span class="sxs-lookup"><span data-stu-id="c7cd6-135">This element is set for each conversation.</span></span> 
    
<span data-ttu-id="c7cd6-136">El cuerpo SOAP de la solicitud contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="c7cd6-136">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="c7cd6-137">GetConversationItems</span><span class="sxs-lookup"><span data-stu-id="c7cd6-137">GetConversationItems</span></span>](getconversationitems.md)
    
- [<span data-ttu-id="c7cd6-138">ItemShape</span><span class="sxs-lookup"><span data-stu-id="c7cd6-138">ItemShape</span></span>](itemshape.md)
    
- [<span data-ttu-id="c7cd6-139">BaseShape</span><span class="sxs-lookup"><span data-stu-id="c7cd6-139">BaseShape</span></span>](baseshape.md)
    
- [<span data-ttu-id="c7cd6-140">AdditionalProperties</span><span class="sxs-lookup"><span data-stu-id="c7cd6-140">AdditionalProperties</span></span>](additionalproperties.md)
    
- [<span data-ttu-id="c7cd6-141">FieldURI</span><span class="sxs-lookup"><span data-stu-id="c7cd6-141">FieldURI</span></span>](fielduri.md)
    
- [<span data-ttu-id="c7cd6-142">FoldersToIgnore</span><span class="sxs-lookup"><span data-stu-id="c7cd6-142">FoldersToIgnore</span></span>](folderstoignore.md)
    
- [<span data-ttu-id="c7cd6-143">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="c7cd6-143">DistinguishedFolderId</span></span>](distinguishedfolderid.md)
    
- [<span data-ttu-id="c7cd6-144">SortOrder (ConversationNodeSortOrder)</span><span class="sxs-lookup"><span data-stu-id="c7cd6-144">SortOrder (ConversationNodeSortOrder)</span></span>](sortorder-conversationnodesortorder.md)
    
- [<span data-ttu-id="c7cd6-145">Conversaciones</span><span class="sxs-lookup"><span data-stu-id="c7cd6-145">Conversations</span></span>](conversations-ex15websvcsotherref.md)
    
- [<span data-ttu-id="c7cd6-146">Conversación (ConversationRequestType)</span><span class="sxs-lookup"><span data-stu-id="c7cd6-146">Conversation (ConversationRequestType)</span></span>](conversation-conversationrequesttype.md)
    
- [<span data-ttu-id="c7cd6-147">ConversationId</span><span class="sxs-lookup"><span data-stu-id="c7cd6-147">ConversationId</span></span>](conversationid.md)
    
## <a name="successful-getconversationitems-operation-response"></a><span data-ttu-id="c7cd6-148">Respuesta de operación GetConversationItems correcta</span><span class="sxs-lookup"><span data-stu-id="c7cd6-148">Successful GetConversationItems operation response</span></span>

<span data-ttu-id="c7cd6-149">En el ejemplo siguiente se muestra una respuesta correcta a una solicitud de operación de **GetConversationItems** para obtener elementos en una única conversación.</span><span class="sxs-lookup"><span data-stu-id="c7cd6-149">The following example shows a successful response to a **GetConversationItems** operation request to get items in a single conversation.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15"
                           MinorVersion="0"
                           MajorBuildNumber="545"
                           MinorBuildNumber="11"
                           Version="Exchange2013"
                           xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types"
                           xmlns="https://schemas.microsoft.com/exchange/services/2006/types"
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <m:GetConversationItemsResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                                      xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
         <m:ResponseMessages>
            <m:GetConversationItemsResponseMessage ResponseClass="Success">
               <m:ResponseCode>NoError</m:ResponseCode>
               <m:Conversation>
                  <t:ConversationId Id="AAQkADEzOTExYjJkakJCs=" />
                  <t:SyncState>AQIAAABNVkUwAgIAAABhHqHUAwIAAABNVkUxBAIAAABhHqHfBAIAAABhHqHV</t:SyncState>
                  <t:ConversationNodes>
                     <t:ConversationNode>
                        <t:InternetMessageId>6a4838fa804045e09d40c1a39b9ea916@contoso.com</t:InternetMessageId>
                        <t:ParentInternetMessageId>15a56698d503438fbdaa18186d5b81b7@contoso.com</t:ParentInternetMessageId>
                        <t:Items>
                           <t:Message>
                              <t:ItemId Id="AAMkADEzOTQrAABhHqHfAAA=" ChangeKey="CQAAABYAAACYAABhPpaq" />
                              <t:Subject>RE: Daily issue scrub</t:Subject>
                              <t:DateTimeReceived>2012-10-30T18:42:27Z</t:DateTimeReceived>
                           </t:Message>
                        </t:Items>
                     </t:ConversationNode>
                     <t:ConversationNode>
                        <t:InternetMessageId>2695d2b837954d68846b0c30491f5af1@contoso.com</t:InternetMessageId>
                        <t:ParentInternetMessageId>15a56698d503438fbdaa18186d5b81b7@contoso.com</t:ParentInternetMessageId>
                        <t:Items>
                           <t:Message>
                              <t:ItemId Id="AAMkADEzOTExYjJkLTYxZDAt" ChangeKey="CQAAABQrAABhPpaP" />
                              <t:Subject>RE: Daily issue scrub</t:Subject>
                              <t:DateTimeReceived>2012-10-30T17:38:26Z</t:DateTimeReceived>
                           </t:Message>
                        </t:Items>
                     </t:ConversationNode>
                     <t:ConversationNode>
                        <t:InternetMessageId>15a56698d503438fbdaa18186d5b81b7@contoso.com</t:InternetMessageId>
                        <t:ParentInternetMessageId>d3113e59c89c4288ae13100d033f8dbc@contoso.com</t:ParentInternetMessageId>
                        <t:Items>
                           <t:Message>
                              <t:ItemId Id="AAMkADEzOTFNVkUxAAA=" ChangeKey="CQAAABY4QrAABhPvYK" />
                              <t:Subject>RE: Daily issue scrub</t:Subject>
                              <t:DateTimeReceived>2012-10-30T17:37:00Z</t:DateTimeReceived>
                           </t:Message>
                        </t:Items>
                     </t:ConversationNode>
                     <t:ConversationNode>
                        <t:InternetMessageId>d3113e59c89c4288ae13100d033f8dbc@contoso.com</t:InternetMessageId>
                        <t:ParentInternetMessageId>189b712056c2430dbce334b40496ad00@contoso.com</t:ParentInternetMessageId>
                        <t:Items>
                           <t:Message>
                              <t:ItemId Id="AAMkm4QrAABhHqHUAAA=" ChangeKey="CQAAABQrAABhPpaN" />
                              <t:Subject>RE: Daily issue scrub</t:Subject>
                              <t:DateTimeReceived>2012-10-30T17:37:05Z</t:DateTimeReceived>
                           </t:Message>
                        </t:Items>
                     </t:ConversationNode>
                     <t:ConversationNode>
                        <t:InternetMessageId>189b712056c2430dbce334b40496ad00@contoso.com</t:InternetMessageId>
                        <t:Items>
                           <t:Message>
                              <t:ItemId Id="AAMkArAABNVkUwAAA=" ChangeKey="CQAAABm4QrAABhPvYJ" />
                              <t:Subject>Daily issue scrub</t:Subject>
                              <t:DateTimeReceived>2012-10-30T17:36:00Z</t:DateTimeReceived>
                           </t:Message>
                        </t:Items>
                     </t:ConversationNode>
                  </t:ConversationNodes>
               </m:Conversation>
            </m:GetConversationItemsResponseMessage>
         </m:ResponseMessages>
      </m:GetConversationItemsResponse>
   </s:Body>
</s:Envelope>
```

<span data-ttu-id="c7cd6-150">Le recomendamos que guarde el SyncState para las solicitudes de operaciones de **GetConversationItems** posteriores.</span><span class="sxs-lookup"><span data-stu-id="c7cd6-150">We recommend that you save the SyncState for subsequent **GetConversationItems** operation requests.</span></span> 
  
<span data-ttu-id="c7cd6-151">El cuerpo SOAP de respuesta contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="c7cd6-151">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="c7cd6-152">GetConversationItemsResponse</span><span class="sxs-lookup"><span data-stu-id="c7cd6-152">GetConversationItemsResponse</span></span>](getconversationitemsresponse.md)
    
- [<span data-ttu-id="c7cd6-153">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="c7cd6-153">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="c7cd6-154">GetConversationItemsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="c7cd6-154">GetConversationItemsResponseMessage</span></span>](getconversationitemsresponsemessage.md)
    
- [<span data-ttu-id="c7cd6-155">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="c7cd6-155">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="c7cd6-156">Conversación (ConversationResponseType)</span><span class="sxs-lookup"><span data-stu-id="c7cd6-156">Conversation (ConversationResponseType)</span></span>](conversation-conversationresponsetype.md)
    
- [<span data-ttu-id="c7cd6-157">ConversationId</span><span class="sxs-lookup"><span data-stu-id="c7cd6-157">ConversationId</span></span>](conversationid.md)
    
- [<span data-ttu-id="c7cd6-158">SyncState (base64Binary)</span><span class="sxs-lookup"><span data-stu-id="c7cd6-158">SyncState (base64Binary)</span></span>](syncstate-base64binary.md)
    
- [<span data-ttu-id="c7cd6-159">ConversationNodes</span><span class="sxs-lookup"><span data-stu-id="c7cd6-159">ConversationNodes</span></span>](conversationnodes.md)
    
- [<span data-ttu-id="c7cd6-160">ConversationNode</span><span class="sxs-lookup"><span data-stu-id="c7cd6-160">ConversationNode</span></span>](conversationnode.md)
    
- [<span data-ttu-id="c7cd6-161">InternetMessageId</span><span class="sxs-lookup"><span data-stu-id="c7cd6-161">InternetMessageId</span></span>](internetmessageid.md)
    
- [<span data-ttu-id="c7cd6-162">Elementos (NonEmptyArrayOfAllItemsType)</span><span class="sxs-lookup"><span data-stu-id="c7cd6-162">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md)
    
- [<span data-ttu-id="c7cd6-163">Mensaje</span><span class="sxs-lookup"><span data-stu-id="c7cd6-163">Message</span></span>](message-ex15websvcsotherref.md)
    
- [<span data-ttu-id="c7cd6-164">ItemId</span><span class="sxs-lookup"><span data-stu-id="c7cd6-164">ItemId</span></span>](itemid.md)
    
- [<span data-ttu-id="c7cd6-165">Asunto</span><span class="sxs-lookup"><span data-stu-id="c7cd6-165">Subject</span></span>](subject.md)
    
- [<span data-ttu-id="c7cd6-166">DateTimeReceived</span><span class="sxs-lookup"><span data-stu-id="c7cd6-166">DateTimeReceived</span></span>](datetimereceived.md)
    
## <a name="getconversationitems-operation-error-response"></a><span data-ttu-id="c7cd6-167">Respuesta de error de operación de GetConversationItems</span><span class="sxs-lookup"><span data-stu-id="c7cd6-167">GetConversationItems operation error response</span></span>

<span data-ttu-id="c7cd6-168">En el ejemplo siguiente se muestra una respuesta de error a una solicitud de operación de **GetConversationItems** para obtener elementos de una conversación que ya no existe en el buzón o para los que todos los elementos de la conversación se encuentran en carpetas que se omiten.</span><span class="sxs-lookup"><span data-stu-id="c7cd6-168">The following example shows an error response to a **GetConversationItems** operation request to get items in a conversation that either no longer exists in the mailbox, or for which all the conversation items are located in folders that are ignored.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="556" MinorBuildNumber="8" Version="Exchange2013" xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" xmlns="https://schemas.microsoft.com/exchange/services/2006/types" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetConversationItemsResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:GetConversationItemsResponseMessage ResponseClass="Error">
          <m:MessageText>The specified object was not found in the store.</m:MessageText>
          <m:ResponseCode>ErrorItemNotFound</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
        </m:GetConversationItemsResponseMessage>
      </m:ResponseMessages>
    </m:GetConversationItemsResponse>
  </s:Body>
</s:Envelope>
```

## <a name="see-also"></a><span data-ttu-id="c7cd6-169">Vea también</span><span class="sxs-lookup"><span data-stu-id="c7cd6-169">See also</span></span>

- [<span data-ttu-id="c7cd6-170">Operaciones de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="c7cd6-170">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
    
- [<span data-ttu-id="c7cd6-171">Operación ApplyConversationAction</span><span class="sxs-lookup"><span data-stu-id="c7cd6-171">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)
    
- [<span data-ttu-id="c7cd6-172">Operación FindConversation</span><span class="sxs-lookup"><span data-stu-id="c7cd6-172">FindConversation operation</span></span>](findconversation-operation.md)
    

