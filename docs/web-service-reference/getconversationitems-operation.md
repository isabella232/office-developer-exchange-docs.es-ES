---
title: GetConversationItems operation
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8ae00a99-b37b-4194-829c-fe300db6ab99
description: Obtenga información acerca de la operación de GetConversationItems.
ms.openlocfilehash: 9d9fb9cc04bcbb5846162c77c852defa51dff98b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764788"
---
# <a name="getconversationitems-operation"></a><span data-ttu-id="008fc-103">GetConversationItems operation</span><span class="sxs-lookup"><span data-stu-id="008fc-103">GetConversationItems operation</span></span>

<span data-ttu-id="008fc-104">Obtenga información acerca de la operación de **GetConversationItems** .</span><span class="sxs-lookup"><span data-stu-id="008fc-104">Find information about the **GetConversationItems** operation.</span></span> 
  
<span data-ttu-id="008fc-105">La operación **GetConversationItems** obtiene uno o más conjuntos de elementos que están organizados en nodos en una conversación.</span><span class="sxs-lookup"><span data-stu-id="008fc-105">The **GetConversationItems** operation gets one or more sets of items that are organized in to nodes in a conversation.</span></span> 
  
<span data-ttu-id="008fc-106">Esta operación se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="008fc-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-getconversationitems-operation"></a><span data-ttu-id="008fc-107">Mediante la operación GetConversationItems</span><span class="sxs-lookup"><span data-stu-id="008fc-107">Using the GetConversationItems operation</span></span>

<span data-ttu-id="008fc-108">Puede usar la operación de **GetConversationItems** para obtener los elementos de las conversaciones de ambos primaria y buzones de archivo.</span><span class="sxs-lookup"><span data-stu-id="008fc-108">You can use the **GetConversationItems** operation to get items in conversations for both primary and archive mailboxes.</span></span> 
  
### <a name="getconversationitems-operation-soap-headers"></a><span data-ttu-id="008fc-109">Encabezados SOAP de operación de GetConversationItems</span><span class="sxs-lookup"><span data-stu-id="008fc-109">GetConversationItems operation SOAP headers</span></span>

<span data-ttu-id="008fc-110">La operación de **GetConversationItems** puede utilizar los encabezados SOAP que se enumeran en la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="008fc-110">The **GetConversationItems** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="008fc-111">**Nombre de encabezado**</span><span class="sxs-lookup"><span data-stu-id="008fc-111">**Header name**</span></span>|<span data-ttu-id="008fc-112">**Element**</span><span class="sxs-lookup"><span data-stu-id="008fc-112">**Element**</span></span>|<span data-ttu-id="008fc-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="008fc-113">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="008fc-114">**Suplantación**</span><span class="sxs-lookup"><span data-stu-id="008fc-114">**Impersonation**</span></span> <br/> |[<span data-ttu-id="008fc-115">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="008fc-115">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="008fc-116">Identifica el usuario que está realizando la suplantación de la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="008fc-116">Identifies the user whom the client application is impersonating.</span></span> <span data-ttu-id="008fc-117">Este encabezado es aplicable a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="008fc-117">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="008fc-118">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="008fc-118">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="008fc-119">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="008fc-119">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="008fc-120">Identifica la versión del esquema para la solicitud de la operación.</span><span class="sxs-lookup"><span data-stu-id="008fc-120">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="008fc-121">El valor mínimo para este elemento es **Exchange2013**.</span><span class="sxs-lookup"><span data-stu-id="008fc-121">The minimum value for this element is **Exchange2013**.</span></span> <span data-ttu-id="008fc-122">Este encabezado es aplicable a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="008fc-122">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="008fc-123">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="008fc-123">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="008fc-124">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="008fc-124">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="008fc-125">Identifica la versión del servidor que ha respondido a la solicitud.</span><span class="sxs-lookup"><span data-stu-id="008fc-125">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="008fc-126">Este encabezado es aplicable a una respuesta.</span><span class="sxs-lookup"><span data-stu-id="008fc-126">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="getconversationitems-operation-request-example-get-items-in-a-single-conversation"></a><span data-ttu-id="008fc-127">Ejemplo de solicitud de operación de GetConversationItems: obtener elementos en una conversación único</span><span class="sxs-lookup"><span data-stu-id="008fc-127">GetConversationItems operation request example: Get items in a single conversation</span></span>

<span data-ttu-id="008fc-128">El siguiente ejemplo de una solicitud de operación **GetConversationItems** muestra cómo obtener todos los elementos de una conversación en una conversación única, con la excepción de los elementos ubicados en las carpetas de borrador y elementos eliminados.</span><span class="sxs-lookup"><span data-stu-id="008fc-128">The following example of a **GetConversationItems** operation request shows how to get all conversation items in a single conversation, with the exception of items located in the Deleted Items and Drafts folders.</span></span> <span data-ttu-id="008fc-129">Cada elemento devuelto en la respuesta contendrá un identificador de elemento, un asunto y la hora en que se recibió el artículo en el buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="008fc-129">Each item returned in the response will contain an item identifier, a subject, and the time that the item was received in the mailbox.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="008fc-130">Todos los identificadores de artículo y cambiar claves en este artículo se han abreviado para conservar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="008fc-130">All item identifiers and change keys in this article have been shortened to preserve readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
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

<span data-ttu-id="008fc-131">En este ejemplo de una solicitud **GetConversationItems** no incluye las siguientes opciones:</span><span class="sxs-lookup"><span data-stu-id="008fc-131">This example of a **GetConversationItems** request does not include the following options:</span></span> 
  
- <span data-ttu-id="008fc-132">El elemento [MaxItemsToReturn](maxitemstoreturn.md) , que establece el número máximo de elementos para devolver en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="008fc-132">The [MaxItemsToReturn](maxitemstoreturn.md) element, which sets the maximum number of items to return in the response.</span></span> 
    
- <span data-ttu-id="008fc-133">El elemento [MailboxScope](mailboxscope.md) , que establece el ámbito de buzón de correo al que indica si la operación de **GetConversationItems** es que se debe realizar en el buzón principal, en el buzón de archivo o ambos buzones de correo.</span><span class="sxs-lookup"><span data-stu-id="008fc-133">The [MailboxScope](mailboxscope.md) element, which sets the mailbox scope by indicating whether the **GetConversationItems** operation is to be performed on the primary mailbox, the archive mailbox, or both mailboxes.</span></span> 
    
- <span data-ttu-id="008fc-134">El elemento de [estado de sincronización (base64Binary)](syncstate-base64binary.md) , que establece el estado de sincronización para obtener sólo los elementos de la conversación que son nuevos o actualizados en la conversación.</span><span class="sxs-lookup"><span data-stu-id="008fc-134">The [SyncState (base64Binary)](syncstate-base64binary.md) element, which sets the synchronization state to only get conversation items that are new or updated in the conversation.</span></span> <span data-ttu-id="008fc-135">Este elemento se establece para cada conversación.</span><span class="sxs-lookup"><span data-stu-id="008fc-135">This element is set for each conversation.</span></span> 
    
<span data-ttu-id="008fc-136">La solicitud SOAP body contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="008fc-136">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="008fc-137">GetConversationItems</span><span class="sxs-lookup"><span data-stu-id="008fc-137">GetConversationItems</span></span>](getconversationitems.md)
    
- [<span data-ttu-id="008fc-138">ItemShape</span><span class="sxs-lookup"><span data-stu-id="008fc-138">ItemShape</span></span>](itemshape.md)
    
- [<span data-ttu-id="008fc-139">BaseShape</span><span class="sxs-lookup"><span data-stu-id="008fc-139">BaseShape</span></span>](baseshape.md)
    
- [<span data-ttu-id="008fc-140">AdditionalProperties</span><span class="sxs-lookup"><span data-stu-id="008fc-140">AdditionalProperties</span></span>](additionalproperties.md)
    
- [<span data-ttu-id="008fc-141">FieldURI</span><span class="sxs-lookup"><span data-stu-id="008fc-141">FieldURI</span></span>](fielduri.md)
    
- [<span data-ttu-id="008fc-142">FoldersToIgnore</span><span class="sxs-lookup"><span data-stu-id="008fc-142">FoldersToIgnore</span></span>](folderstoignore.md)
    
- [<span data-ttu-id="008fc-143">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="008fc-143">DistinguishedFolderId</span></span>](distinguishedfolderid.md)
    
- [<span data-ttu-id="008fc-144">SortOrder (ConversationNodeSortOrder)</span><span class="sxs-lookup"><span data-stu-id="008fc-144">SortOrder (ConversationNodeSortOrder)</span></span>](sortorder-conversationnodesortorder.md)
    
- [<span data-ttu-id="008fc-145">Conversaciones</span><span class="sxs-lookup"><span data-stu-id="008fc-145">Conversations</span></span>](conversations-ex15websvcsotherref.md)
    
- [<span data-ttu-id="008fc-146">Conversación (ConversationRequestType)</span><span class="sxs-lookup"><span data-stu-id="008fc-146">Conversation (ConversationRequestType)</span></span>](conversation-conversationrequesttype.md)
    
- [<span data-ttu-id="008fc-147">ConversationId</span><span class="sxs-lookup"><span data-stu-id="008fc-147">ConversationId</span></span>](conversationid.md)
    
## <a name="successful-getconversationitems-operation-response"></a><span data-ttu-id="008fc-148">Respuesta es correcta de operación GetConversationItems</span><span class="sxs-lookup"><span data-stu-id="008fc-148">Successful GetConversationItems operation response</span></span>

<span data-ttu-id="008fc-149">En el ejemplo siguiente se muestra una respuesta correcta a una solicitud de operación de **GetConversationItems** para obtener los elementos de una única conversación.</span><span class="sxs-lookup"><span data-stu-id="008fc-149">The following example shows a successful response to a **GetConversationItems** operation request to get items in a single conversation.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15"
                           MinorVersion="0"
                           MajorBuildNumber="545"
                           MinorBuildNumber="11"
                           Version="Exchange2013"
                           xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types"
                           xmlns="http://schemas.microsoft.com/exchange/services/2006/types"
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <m:GetConversationItemsResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
                                      xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
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

<span data-ttu-id="008fc-150">Se recomienda que se guarde el estado de sincronización para las solicitudes posteriores de operación **GetConversationItems** .</span><span class="sxs-lookup"><span data-stu-id="008fc-150">We recommend that you save the SyncState for subsequent **GetConversationItems** operation requests.</span></span> 
  
<span data-ttu-id="008fc-151">La respuesta SOAP body contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="008fc-151">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="008fc-152">GetConversationItemsResponse</span><span class="sxs-lookup"><span data-stu-id="008fc-152">GetConversationItemsResponse</span></span>](getconversationitemsresponse.md)
    
- [<span data-ttu-id="008fc-153">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="008fc-153">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="008fc-154">GetConversationItemsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="008fc-154">GetConversationItemsResponseMessage</span></span>](getconversationitemsresponsemessage.md)
    
- [<span data-ttu-id="008fc-155">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="008fc-155">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="008fc-156">Conversación (ConversationResponseType)</span><span class="sxs-lookup"><span data-stu-id="008fc-156">Conversation (ConversationResponseType)</span></span>](conversation-conversationresponsetype.md)
    
- [<span data-ttu-id="008fc-157">ConversationId</span><span class="sxs-lookup"><span data-stu-id="008fc-157">ConversationId</span></span>](conversationid.md)
    
- [<span data-ttu-id="008fc-158">Estado de sincronización (base64Binary)</span><span class="sxs-lookup"><span data-stu-id="008fc-158">SyncState (base64Binary)</span></span>](syncstate-base64binary.md)
    
- [<span data-ttu-id="008fc-159">ConversationNodes</span><span class="sxs-lookup"><span data-stu-id="008fc-159">ConversationNodes</span></span>](conversationnodes.md)
    
- [<span data-ttu-id="008fc-160">ConversationNode</span><span class="sxs-lookup"><span data-stu-id="008fc-160">ConversationNode</span></span>](conversationnode.md)
    
- [<span data-ttu-id="008fc-161">InternetMessageId</span><span class="sxs-lookup"><span data-stu-id="008fc-161">InternetMessageId</span></span>](internetmessageid.md)
    
- [<span data-ttu-id="008fc-162">Elementos (NonEmptyArrayOfAllItemsType)</span><span class="sxs-lookup"><span data-stu-id="008fc-162">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md)
    
- [<span data-ttu-id="008fc-163">Message</span><span class="sxs-lookup"><span data-stu-id="008fc-163">Message</span></span>](message-ex15websvcsotherref.md)
    
- [<span data-ttu-id="008fc-164">ItemId</span><span class="sxs-lookup"><span data-stu-id="008fc-164">ItemId</span></span>](itemid.md)
    
- [<span data-ttu-id="008fc-165">Subject</span><span class="sxs-lookup"><span data-stu-id="008fc-165">Subject</span></span>](subject.md)
    
- [<span data-ttu-id="008fc-166">DateTimeReceived</span><span class="sxs-lookup"><span data-stu-id="008fc-166">DateTimeReceived</span></span>](datetimereceived.md)
    
## <a name="getconversationitems-operation-error-response"></a><span data-ttu-id="008fc-167">Respuesta de error de la operación de GetConversationItems</span><span class="sxs-lookup"><span data-stu-id="008fc-167">GetConversationItems operation error response</span></span>

<span data-ttu-id="008fc-168">En el ejemplo siguiente se muestra una respuesta de error a una solicitud de operación de **GetConversationItems** para obtener los elementos en una conversación que cualquiera ya no existe en el buzón de correo, o para que todos los elementos de la conversación se encuentran en las carpetas que se pasan por alto.</span><span class="sxs-lookup"><span data-stu-id="008fc-168">The following example shows an error response to a **GetConversationItems** operation request to get items in a conversation that either no longer exists in the mailbox, or for which all the conversation items are located in folders that are ignored.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="556" MinorBuildNumber="8" Version="Exchange2013" xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" xmlns="http://schemas.microsoft.com/exchange/services/2006/types" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetConversationItemsResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
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

## <a name="see-also"></a><span data-ttu-id="008fc-169">Vea también</span><span class="sxs-lookup"><span data-stu-id="008fc-169">See also</span></span>

- [<span data-ttu-id="008fc-170">Operaciones de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="008fc-170">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
    
- [<span data-ttu-id="008fc-171">Operación ApplyConversationAction</span><span class="sxs-lookup"><span data-stu-id="008fc-171">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)
    
- [<span data-ttu-id="008fc-172">Operación de FindConversation</span><span class="sxs-lookup"><span data-stu-id="008fc-172">FindConversation operation</span></span>](findconversation-operation.md)
    
