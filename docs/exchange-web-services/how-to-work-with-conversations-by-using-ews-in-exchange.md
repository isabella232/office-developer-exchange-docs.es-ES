---
title: Trabajar con conversaciones mediante EWS en Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 7750528c-acb2-43e5-a1e1-ee201c0e1730
description: Obtenga información sobre cómo buscar conversaciones, aplicar acciones a las conversaciones y obtener elementos en las conversaciones mediante la API administrada ews o EWS en Exchange.
ms.openlocfilehash: b2cf00b1f6f69ec1a1989d3f452ff6c0102dc95e
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59521097"
---
# <a name="work-with-conversations-by-using-ews-in-exchange"></a>Trabajar con conversaciones mediante EWS en Exchange

Obtenga información sobre cómo buscar conversaciones, aplicar acciones a las conversaciones y obtener elementos en las conversaciones mediante la API administrada ews o EWS en Exchange.
  
En el contexto de Exchange, las conversaciones son una forma de agrupar y administrar un conjunto relacionado de mensajes de correo electrónico. También pueden proporcionar una forma de ver mensajes relacionados. Exchange define las conversaciones en función del valor **id. de** mensaje del primer mensaje de correo electrónico de un subproceso. Todas las respuestas y mensajes relacionados hacen referencia al encabezado **Message-ID** del mensaje original en sus encabezados **References** y **In-Reply-To.** 
  
Además, dentro del sobre SOAP, para cada mensaje recibido en un buzón, Exchange establece propiedades y elementos específicos.
  
**Tabla 1. Propiedades y elementos de conversación establecidos en todos los mensajes de correo electrónico**

|**Propiedad de API administrada ews**|**Elemento EWS**|**Descripción**|
|:-----|:-----|:-----|
|[ConversationTopic](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.conversationtopic%28v=exchg.80%29.aspx) <br/> |[ConversationTopic](https://msdn.microsoft.com/library/46cacf42-4039-4c8a-9b20-c42cdd9f2760%28Office.15%29.aspx) <br/> |Contiene una forma normalizada del valor de asunto que se estableció en el mensaje original. Esto es lo mismo que el **encabezado del mensaje Thread-Topic.** Este valor es de solo lectura.  <br/> |
|[ConversationIndex](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.conversationindex%28v=exchg.80%29.aspx) <br/> |[ConversationIndex](https://msdn.microsoft.com/library/fdf47e22-8d93-4ae4-883b-0c9f07f48724%28Office.15%29.aspx) <br/> |Representa la posición del elemento en la conversación. Esto es lo mismo que el **encabezado del mensaje Thread-Index.** Este valor es de solo lectura.  <br/> |
   
Exchange aplica el mismo valor **ConversationTopic** a las respuestas al primer mensaje y, a continuación, actualiza el valor **ConversationIndex** para representar la posición del mensaje con respecto al mensaje original. Si el asunto del subproceso de correo electrónico cambia, Exchange aplica un nuevo valor **ConversationTopic** y nuevos valores **conversationIndex** a la nueva conversación. 
  
**Tabla 2. Métodos de API administrada ews y operaciones ews para trabajar con conversaciones**

|**Para**|**Usar este método o métodos de la API administrada ews**|**Usar esta operación EWS**|
|:-----|:-----|:-----|
|Buscar conversaciones  <br/> |[ExchangeService.FindConversation](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.findconversation%28v=exchg.80%29.aspx) <br/> |[FindConversation](https://msdn.microsoft.com/library/2384908a-c203-45b6-98aa-efd6a4c23aac%28Office.15%29.aspx) <br/> |
|Aplicar acciones de conversación  <br/> |[Conversation.EnableAlwaysCategorizeItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.conversation.enablealwayscategorizeitems%28v=exchg.80%29.aspx) <br/> [Conversation.EnableAlwaysDeleteItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.conversation.enablealwaysdeleteitems%28v=exchg.80%29.aspx) <br/> [Conversation.EnableAlwaysMoveItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.conversation.enablealwaysmoveitems%28v=exchg.80%29.aspx) <br/> [ExchangeService.CopyItemsInConversations](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.copyitemsinconversations%28v=exchg.80%29.aspx) <br/> [ExchangeService.DeleteItemsInConversations](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.deleteitemsinconversations%28v=exchg.80%29.aspx) <br/> [ExchangeService.DisableAlwaysCategorizeItemsInConversations](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.disablealwayscategorizeitemsinconversations%28v=exchg.80%29.aspx) <br/> [ExchangeService.DisableAlwaysDeleteItemsInConversations](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.disablealwaysdeleteitemsinconversations%28v=exchg.80%29.aspx) <br/> [ExchangeService.DisableAlwaysMoveItemsInConversations](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.disablealwaysmoveitemsinconversations%28v=exchg.80%29.aspx) <br/> [ExchangeService.EnableAlwaysCategorizeItemsInConversations](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.enablealwayscategorizeitemsinconversations%28v=exchg.80%29.aspx) <br/> [ExchangeService.EnableAlwaysDeleteItemsInConversations](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.enablealwaysdeleteitemsinconversations%28v=exchg.80%29.aspx) <br/> [ExchangeService.EnableAlwaysMoveItemsInConversations](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.enablealwaysmoveitemsinconversations%28v=exchg.80%29.aspx) <br/> [ExchangeService.MoveItemsInConversations](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.moveitemsinconversations%28v=exchg.80%29.aspx) <br/> [ExchangeService.SetFlagStatusForItemsInConversations](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.setflagstatusforitemsinconversations%28v=exchg.80%29.aspx) <br/> [ExchangeService.SetReadStateForItemsInConversations](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.setreadstateforitemsinconversations%28v=exchg.80%29.aspx) <br/> [ExchangeService.SetRetentionPolicyForItemsInConversations](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice.setretentionpolicyforitemsinconversations%28v=exchg.80%29.aspx) <br/> |[ApplyConversationAction](https://msdn.microsoft.com/library/73d7943d-d361-4f8b-9948-d85f886efa1a%28Office.15%29.aspx) <br/> |
|Obtener elementos en una o más conversaciones  <br/> |[ExchangeService.GetConversationItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.getconversationitems%28v=exchg.80%29.aspx) <br/> |[GetConversationItems](https://msdn.microsoft.com/library/8ae00a99-b37b-4194-829c-fe300db6ab99%28Office.15%29.aspx) <br/> |

<a name="bk_findewsma"> </a>

## <a name="find-a-conversation-by-using-the-ews-managed-api"></a>Buscar una conversación mediante la API administrada de EWS

Puede encontrar conversaciones mediante el método de api administrada EWS [ExchangeService.FindConversation,](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.findconversation%28v=exchg.80%29.aspx) como se muestra en el ejemplo siguiente. En este ejemplo se obtienen las primeras 10 conversaciones de la carpeta Bandeja de entrada que tienen un asunto que contiene la palabra "news". A continuación, el ejemplo escribe el tema de conversación, el último tiempo de entrega y la lista global de destinatarios únicos en la ventana de la consola. 
  
En este ejemplo se supone que **el servicio** es un objeto [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) válido y que el usuario se ha autenticado en un Exchange servidor. 
  
```cs
static void FindConversation(ExchangeService service)
{
    // Create the view of conversations returned in the response. This view will return at most 10 results.
    ConversationIndexedItemView view = new ConversationIndexedItemView(10);
    // Create the query string to search for.
    String queryString = "subject:news";
    // Search the Inbox for conversations and return a results set with the specified view.
    // This method call results in a FindConversation call to EWS. 
    ICollection<Conversation> conversations = service.FindConversation(view, WellKnownFolderName.Inbox, queryString);
    // Examine properties on each conversation returned in the response.
    foreach (Conversation conversation in conversations)
    {
        Console.WriteLine("Conversation Topic: " + conversation.Topic);
        Console.WriteLine("Last Delivered: " + conversation.LastDeliveryTime.ToString());
        ApplyConversationActions(service, conversation);
        foreach (string GlUniqRec in conversation.GlobalUniqueRecipients)
        {
            Console.WriteLine("Global Unique Recipient: " + GlUniqRec);
        }
        Console.WriteLine("");
    }
}
```

<a name="bk_findews"> </a>

## <a name="find-a-conversation-by-using-ews"></a>Buscar una conversación con EWS

Puede encontrar conversaciones mediante la operación [EWS FindConversation,](https://msdn.microsoft.com/library/2384908a-c203-45b6-98aa-efd6a4c23aac%28Office.15%29.aspx) como se muestra en el ejemplo siguiente. En este ejemplo se obtienen las primeras diez conversaciones de la carpeta Bandeja de entrada que tienen un asunto que contiene la palabra "news". Esta es también la solicitud XML que envía la API administrada ews cuando se usa la API administrada ews para [buscar una conversación](#bk_findewsma).
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2013" />
  </soap:Header>
  <soap:Body>
    <m:FindConversation>
      <m:IndexedPageItemView MaxEntriesReturned="10"
                             Offset="0"
                             BasePoint="Beginning" />
      <m:ParentFolderId>
        <t:DistinguishedFolderId Id="inbox" />
      </m:ParentFolderId>
      <m:QueryString>subject:news</m:QueryString>
    </m:FindConversation>
  </soap:Body>
</soap:Envelope>

```

El servidor responde a la solicitud **FindConversation** con un mensaje [FindConversationResponse](https://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) que incluye un valor [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) de **NoError** para indicar que la operación se completó correctamente. La respuesta también incluye la única conversación en el buzón que tiene un asunto que contiene la palabra "noticias". 
  
Los **elementos ItemId,** **ChangeKey** y **ConversationId** se han acortado para mejorar la legibilidad. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="883"
                         MinorBuildNumber="10"
                         Version="V2_10"
                         xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <FindConversationResponse ResponseClass="Success"
                              xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
      <Conversations>
        <Conversation xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
          <ConversationId Id="aO2NM+Q=" />
          <ConversationTopic>Today's top news headlines</ConversationTopic>
          <UniqueRecipients>
            <String>Sadie Daniels</String>
          </UniqueRecipients>
          <GlobalUniqueRecipients>
            <String>Sadie Daniels</String>
          </GlobalUniqueRecipients>
          <UniqueUnreadSenders>
            <String>Ronnie Sturgis</String>
          </UniqueUnreadSenders>
          <GlobalUniqueUnreadSenders>
            <String>Ronnie Sturgis</String>
          </GlobalUniqueUnreadSenders>
          <UniqueSenders>
            <String>Ronnie Sturgis</String>
          </UniqueSenders>
          <GlobalUniqueSenders>
            <String>Ronnie Sturgis</String>
          </GlobalUniqueSenders>
          <LastDeliveryTime>2014-02-18T20:42:26Z</LastDeliveryTime>
          <GlobalLastDeliveryTime>2014-02-18T20:42:26Z</GlobalLastDeliveryTime>
          <HasAttachments>false</HasAttachments>
          <GlobalHasAttachments>false</GlobalHasAttachments>
          <MessageCount>1</MessageCount>
          <GlobalMessageCount>1</GlobalMessageCount>
          <UnreadCount>1</UnreadCount>
          <GlobalUnreadCount>1</GlobalUnreadCount>
          <Size>9330</Size>
          <GlobalSize>9330</GlobalSize>
          <ItemClasses>
            <ItemClass>IPM.Note</ItemClass>
          </ItemClasses>
          <GlobalItemClasses>
            <ItemClass>IPM.Note</ItemClass>
          </GlobalItemClasses>
          <Importance>Normal</Importance>
          <GlobalImportance>Normal</GlobalImportance>
          <ItemIds>
            <ItemId Id="sVCyAAA="
                    ChangeKey="CQAAAA==" />
          </ItemIds>
          <GlobalItemIds>
            <ItemId Id="sVCyAAA="
                    ChangeKey="CQAAAA==" />
          </GlobalItemIds>
          <LastModifiedTime>2014-02-18T20:42:26Z</LastModifiedTime>
          <InstanceKey>AQAAAAAAAQABAAAACbFYggAAAAA=</InstanceKey>
          <HasIrm>false</HasIrm>
          <GlobalHasIrm>false</GlobalHasIrm>
        </Conversation>
      </Conversations>
      <TotalConversationsInView>1</TotalConversationsInView>
      <IndexedOffset>1</IndexedOffset>
    </FindConversationResponse>
  </s:Body>
</s:Envelope>

```

<a name="bk_applyewsma"> </a>

## <a name="apply-conversation-actions-by-using-the-ews-managed-api"></a>Aplicar acciones de conversación mediante la API administrada de EWS

Puede aplicar acciones de conversación a una conversación mediante varios métodos de LA API administrada ews, como se muestra en el ejemplo siguiente. En este ejemplo se agregan categorías a elementos existentes de una conversación y se aplican las mismas categorías a los elementos futuros de la conversación. También muestra cómo habilitar el movimiento automático de elementos de la conversación a una carpeta. En este ejemplo, los elementos se mueven a la carpeta Borradores.
  
En este ejemplo se supone que **el servicio** es un objeto [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) válido y que el usuario se ha autenticado en un Exchange servidor. 
  
Para obtener una lista completa de los métodos que aplican acciones de conversación, vea la tabla 2.
  
```cs
static void ApplyConversationActions(ExchangeService service, Conversation conversation)
{
   // Create a list of categories to apply to a conversation.
   List<string> categories = new List<string>();
   categories.Add("Customer");
   categories.Add("System Integrator");
   // Apply categorization to all items in the conversation and process the request
   // synchronously after enabling this rule and after all item categorization has been applied. 
   // This method call results in an ApplyConversationAction call to EWS.
   conversation.EnableAlwaysCategorizeItems(categories, true);
   // Apply an always move rule to all items in the conversation and move the items
   // to the Drafts folder. Process the request asynchronously and return the response. 
   // immediately. This method call results in an ApplyConversationAction call to EWS.
   conversation.EnableAlwaysMoveItems(WellKnownFolderName.Drafts, false);
}

```

<a name="bk_applyews"> </a>

## <a name="apply-conversation-actions-by-using-ews"></a>Aplicar acciones de conversación mediante EWS

Puede aplicar acciones de conversación, como clasificar, eliminar y mover, mediante la [operación ApplyConversationAction,](https://msdn.microsoft.com/library/73d7943d-d361-4f8b-9948-d85f886efa1a%28Office.15%29.aspx) como se muestra en el ejemplo siguiente. En este ejemplo se agregan categorías a elementos existentes de una conversación y se aplican las mismas categorías a los elementos futuros de la conversación. También muestra cómo habilitar el movimiento automático de elementos de la conversación a una carpeta; en este ejemplo, los elementos se mueven a la carpeta Borradores. Esta es también la solicitud XML que envía la API administrada ews cuando se usa la API administrada ews para [aplicar acciones de conversación.](#bk_applyewsma)
  
El **elemento ConversationId** se ha acortado para mejorar la legibilidad. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2013" />
  </soap:Header>
  <soap:Body>
    <m:ApplyConversationAction>
      <m:ConversationActions>
        <t:ConversationAction>
          <t:Action>AlwaysMove</t:Action>
          <t:ConversationId Id="jG6WVpg=" />
          <t:ProcessRightAway>false</t:ProcessRightAway>
          <t:DestinationFolderId>
            <t:DistinguishedFolderId Id="drafts" />
          </t:DestinationFolderId>
        </t:ConversationAction>
      </m:ConversationActions>
    </m:ApplyConversationAction>
  </soap:Body>
</soap:Envelope>
```

El servidor responde a la **solicitud ApplyConversationAction** con un mensaje [ApplyConversationActionResponse](https://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) que incluye un valor [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) de **NoError** para indicar que la operación se completó correctamente. 

<a name="bk_getitemssingleewsma"> </a>

## <a name="get-items-in-a-single-conversation-by-using-the-conversation-identifier-in-the-ews-managed-api"></a>Obtener elementos en una sola conversación mediante el identificador de conversación en la API administrada de EWS

Puede obtener elementos en una conversación mediante el método de api administrada EWS [ExchangeService.GetConversationItems.](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.getconversationitems%28v=exchg.80%29.aspx) En este ejemplo se proporciona el conjunto de nodos de conversación de la primera conversación de la Bandeja de entrada. El identificador de elemento, el asunto y el tiempo recibido para cada elemento se devuelven en la respuesta, junto con el índice de conversación y las propiedades del índice de conversación principal. Puede usar las propiedades del índice de conversación para reconstruir la jerarquía de nodos. 
  
En este ejemplo, se omiten todos los elementos de conversación de las carpetas Elementos eliminados y Borradores predeterminados.
  
En este ejemplo se supone que **el servicio** es un objeto [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) válido y que el usuario se ha autenticado en un Exchange servidor. 
  
```cs
static void GetConversationItemsSingleConversation(ExchangeService service)
{
   try
   {
      // Find the first item in the mailbox.
      // This method call results in an FindItem call to EWS.
      FindItemsResults<Item> results = service.FindItems(WellKnownFolderName.Inbox,
                                                         new ItemView(1));
      // Get the conversation identifier of the item. 
      ConversationId convId = results.Items[0].ConversationId;
      // Specify the properties that will be 
      // returned for the items in the conversation.
      PropertySet properties = new PropertySet(BasePropertySet.IdOnly,
                                                ItemSchema.Subject,
                                                ItemSchema.DateTimeReceived);
      // Identify the folders to ignore.
      Collection<FolderId> foldersToIgnore = new Collection<FolderId>() 
          { WellKnownFolderName.DeletedItems, WellKnownFolderName.Drafts };
      // Request the conversation items.
      // This method call results in an GetConversationItems call to EWS.
      ConversationResponse response = service.GetConversationItems(convId,
                                                   properties,
                                                  null,
                                                  foldersToIgnore,
                                                  ConversationSortOrder.TreeOrderDescending);
      // Get the synchronization state of the conversation.
      Console.WriteLine("SyncState: " + response.SyncState);
      Collection<Item> items = new Collection<Item>();
      // Process each node of conversation items.
      foreach (ConversationNode node in response.ConversationNodes)
      {
         Console.WriteLine("Parent conversation index: " + node.ParentConversationIndex);
         Console.WriteLine("Conversation index: " + node.ConversationIndex);
         Console.WriteLine("Conversation node items:");
         // Process each item in the conversation node.
         foreach (Item item in node.Items)
         {
            Console.WriteLine("   Item ID: " + item.Id.UniqueId);
            Console.WriteLine("   Subject: " + item.Subject);
            Console.WriteLine("   Received: " + item.DateTimeReceived);
            items.Add(item);
         }
      }
   }
   // This exception occurs if there is an error with the service.
   catch (ServiceResponseException srException)
   {
      Console.WriteLine(srException);
   }
}

```

Se recomienda almacenar en caché la **propiedad SyncState** para las solicitudes posteriores para obtener elementos en la conversación. 

<a name="bk_getitemsmanyewsma"> </a>

## <a name="get-items-in-many-conversations-by-using-the-conversationrequest-object-in-the-ews-managed-api"></a>Obtener elementos en muchas conversaciones mediante el objeto ConversationRequest en la API administrada de EWS

Puede usar el [objeto ConversationRequest](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.conversationrequest%28v=exchg.80%29.aspx) y el método de api administrada EWS [ExchangeService.GetConversationItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.getconversationitems%28v=exchg.80%29.aspx) para obtener elementos de dos o más conversaciones. En este ejemplo se proporciona un conjunto de nodos de conversación para las dos primeras conversaciones de la Bandeja de entrada. El identificador de elemento, el asunto y el tiempo recibido para cada elemento se devolverán en la respuesta, junto con el índice de conversación y las propiedades del índice de conversación principal. Puede usar las propiedades del índice de conversación para reconstruir la jerarquía de nodos. En este ejemplo se supone que los dos primeros elementos de la Bandeja de entrada son de conversaciones diferentes. 
  
En este ejemplo, se omiten todos los elementos de conversación de las carpetas Elementos eliminados y Borradores predeterminados.
  
En este ejemplo se supone que **el servicio** es un objeto [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) válido y que el usuario se ha autenticado en un Exchange servidor. 
  
```cs
static void GetConversationItemsManyConversations(ExchangeService service)
{
   try
   {
      // Find the first two items in the Inbox. This item will be used to call the GetConversationItems operation.
      // This method call results in an FindItem call to EWS.
      FindItemsResults<Item> results = service.FindItems(WellKnownFolderName.Inbox, new ItemView(2));
      // Get the conversation identifier of the first two items in the Inbox. 
      ConversationId convId1 = results.Items[0].ConversationId;
      ConversationId convId2 = results.Items[1].ConversationId;
      
      // Identify two conversation requests. 
      ConversationRequest convR1 = new ConversationRequest();
      convR1.ConversationId = convId1;
      ConversationRequest convR2 = new ConversationRequest();
      convR2.ConversationId = convId2;
      // Create a collection of conversations to fetch. 
      Collection<ConversationRequest> conversations = new Collection<ConversationRequest>();
      conversations.Add(convR1);
      conversations.Add(convR2);
      // Specify the properties that will be returned for the items in the conversation.
      PropertySet properties = new PropertySet(BasePropertySet.IdOnly,
                                                ItemSchema.Subject,
                                                ItemSchema.DateTimeReceived);
      // Identify the folders to ignore.
      Collection<FolderId> foldersToIgnore = new Collection<FolderId>() 
          { WellKnownFolderName.DeletedItems, WellKnownFolderName.Drafts };
      // Request the conversation items.
      // This method call results in an GetConversationItems call to EWS.
      ServiceResponseCollection<GetConversationItemsResponse> responses = 
          service.GetConversationItems(conversations, properties, foldersToIgnore, 
          ConversationSortOrder.TreeOrderDescending);
      // Process each conversation.
      foreach (GetConversationItemsResponse resp in responses)
      {
         // Identify the synchronization state of the conversation.
         Console.WriteLine("Sync State: " + resp.Conversation.SyncState);
         // Process each node in the conversation.
         foreach (ConversationNode node in resp.Conversation.ConversationNodes)
         {
            Console.WriteLine("Parent conversation index: " + node.ParentConversationIndex);
            Console.WriteLine("Conversation index: " + node.ConversationIndex);
            Console.WriteLine("Conversation node items:");
            // Process each item in the conversation node.
            foreach (Item item in node.Items)
            {
               Console.WriteLine("   Item ID: " + item.Id.UniqueId);
               Console.WriteLine("   Subject: " + item.Subject);
               Console.WriteLine("   Received: " + item.DateTimeReceived);
            }
         }
      }
   }
   // This exception occurs if there is an error with the service.
   catch (ServiceResponseException srException)
   { 
      Console.WriteLine(srException);
   }
}

```

Como procedimiento recomendado, se recomienda devolver solo las propiedades que requiere la aplicación cliente, en lugar de usar la opción **FirstClassProperties** para la **clase BasePropertySet.** Se recomienda almacenar en caché la **propiedad SyncState** para las solicitudes posteriores para obtener elementos en la conversación. 

<a name="bk_getitemsews"> </a>

## <a name="get-items-in-conversations-by-using-the-conversation-identifier-in-ews"></a>Obtener elementos en conversaciones mediante el identificador de conversación en EWS

Puede obtener elementos en una conversación mediante la operación [EWS GetConversationItems.](https://msdn.microsoft.com/library/8ae00a99-b37b-4194-829c-fe300db6ab99%28Office.15%29.aspx) En este ejemplo se proporciona un conjunto de nodos de conversación para la primera conversación de la Bandeja de entrada. El identificador de elemento, el asunto y el tiempo recibido para cada elemento se devuelven en la respuesta, junto con el índice de conversación y las propiedades del índice de conversación principal. Puede usar las propiedades del índice de conversación para reconstruir la jerarquía de nodos. 
  
En este ejemplo, se omiten todos los elementos de conversación de las carpetas Elementos eliminados y Borradores predeterminados.
  
El **elemento ConversationId** se ha acortado para mejorar la legibilidad. 
  
Para obtener elementos de más de una conversación, incluya elementos **de conversación adicionales.** 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m=https://schemas.microsoft.com/exchange/services/2006/messages
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
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
          <t:ConversationId Id="LUQFH6Q=" />
        </t:Conversation>
      </m:Conversations>
    </m:GetConversationItems>
  </soap:Body>
</soap:Envelope>
```

El servidor responde a la solicitud **GetConversationItems** con un mensaje [GetConversationItemsResponse](https://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) que incluye un valor [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) de **NoError** para indicar que la operación se completó correctamente. La respuesta también incluye [los ConversationNodes](https://msdn.microsoft.com/library/5c8a35b8-a940-4b3e-8768-9ba95766fd79%28Office.15%29.aspx) en la conversación. 
  
Los **elementos ItemId,** **SyncState** y **ConversationId** se han acortado para mejorar la legibilidad. 
  
```XML
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="873"
                         MinorBuildNumber="9"
                         Version="V2_9"
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
            <t:ConversationId Id="LUQFH6Q=" />
            <t:SyncState>AAAAYAm1</t:SyncState>
            <t:ConversationNodes>
              <t:ConversationNode>
                <t:InternetMessageId>&amp;lt;994051d7c1a346efbfce8dec2cbad509
                    @SN2SR01MB006.com&amp;gt;</t:InternetMessageId>
                <t:ParentInternetMessageId>&amp;lt;faa2b1df30074380abe3527b0cd18ca5
                    @SN2SR01MB001.com&amp;gt;</t:ParentInternetMessageId>
                <t:Items>
                  <t:Message>
                    <t:ItemId Id="AYB1NAAA="
                              ChangeKey="CQAAABYAAAD/oydcA+SPQZGbKWNyvNIZAAAAYCHq" />
                    <t:Subject>RE: Review Proposal for Tailspin Toys</t:Subject>
                    <t:DateTimeReceived>2014-01-02T13:15:00Z</t:DateTimeReceived>
                  </t:Message>
                </t:Items>
              </t:ConversationNode>
              <t:ConversationNode>
                <t:InternetMessageId>&amp;lt;faa2b1df30074380abe3527b0cd18ca5
                    @SN2SR01MB001.com&amp;gt;</t:InternetMessageId>
                <t:ParentInternetMessageId>&amp;lt;6a8e7658524b41cda7cdc3f23c1074a5
                    @SN2SR01MB001.com&amp;gt;</t:ParentInternetMessageId>
                <t:Items>
                  <t:Message>
                    <t:ItemId Id="lQAAAA=="
                              ChangeKey="CQAAABYAAAD/oydcA+SPQZGbKWNyvNIZAAAAYAu8" />
                    <t:Subject>RE: Review Proposal for Tailspin Toys</t:Subject>
                    <t:DateTimeReceived>2014-01-02T10:02:08Z</t:DateTimeReceived>
                  </t:Message>
                </t:Items>
              </t:ConversationNode>
              <t:ConversationNode>
                <t:InternetMessageId>&amp;lt;bcdb185495834370a874a1e7ebedbb96
                    @SN2SR01MB005.com&amp;gt;</t:InternetMessageId>
                <t:ParentInternetMessageId>&amp;lt;e52a4de6b98d484887e141da094a2ce6
                    @SN2SR01MB006.com&amp;gt;</t:ParentInternetMessageId>
                <t:Items>
                  <t:Message>
                    <t:ItemId Id="igAAAA=="
                              ChangeKey="CQAAABYAAAD/oydcA+SPQZGbKWNyvNIZAAAAYAuj" />
                    <t:Subject>RE: Review Proposal for Tailspin Toys</t:Subject>
                    <t:DateTimeReceived>2014-01-02T16:20:10Z</t:DateTimeReceived>
                  </t:Message>
                </t:Items>
              </t:ConversationNode>
              <t:ConversationNode>
                <t:InternetMessageId>&amp;lt;e52a4de6b98d484887e141da094a2ce6
                    @SN2SR01MB006.com&amp;gt;</t:InternetMessageId>
                <t:ParentInternetMessageId>&amp;lt;f0db3ead01db4fe087d98022149aa16f
                    @SN2SR01MB001.com&amp;gt;</t:ParentInternetMessageId>
                <t:Items>
                  <t:Message>
                    <t:ItemId Id="iwAAAA=="
                              ChangeKey="CQAAABYAAAD/oydcA+SPQZGbKWNyvNIZAAAAYAul" />
                    <t:Subject>RE: Review Proposal for Tailspin Toys</t:Subject>
                    <t:DateTimeReceived>2014-01-02T15:30:10Z</t:DateTimeReceived>
                  </t:Message>
                </t:Items>
              </t:ConversationNode>
              <t:ConversationNode>
                <t:InternetMessageId>&amp;lt;f0db3ead01db4fe087d98022149aa16f
                    @SN2SR01MB001.com&amp;gt;</t:InternetMessageId>
                <t:ParentInternetMessageId>&amp;lt;88b1884ecaaa4f68b081c009d827e8c6
                    @SN2SR01MB003.com&amp;gt;</t:ParentInternetMessageId>
                <t:Items>
                  <t:Message>
                    <t:ItemId Id="jQAAAA=="
                              ChangeKey="CQAAABYAAAD/oydcA+SPQZGbKWNyvNIZAAAAYAuq" />
                    <t:Subject>RE: Review Proposal for Tailspin Toys</t:Subject>
                    <t:DateTimeReceived>2014-01-02T14:20:10Z</t:DateTimeReceived>
                  </t:Message>
                </t:Items>
              </t:ConversationNode>
              <t:ConversationNode>
                <t:InternetMessageId>&amp;lt;88b1884ecaaa4f68b081c009d827e8c6
                    @SN2SR01MB003.com&amp;gt;</t:InternetMessageId>
                <t:ParentInternetMessageId>&amp;lt;faa2b1df30074380abe3527b0cd18ca5
                    @SN2SR01MB001.com&amp;gt;</t:ParentInternetMessageId>
                <t:Items>
                  <t:Message>
                    <t:ItemId Id="kAAAAA=="
                              ChangeKey="CQAAABYAAAD/oydcA+SPQZGbKWNyvNIZAAAAYAux" />
                    <t:Subject>RE: Review Proposal for Tailspin Toys</t:Subject>
                    <t:DateTimeReceived>2014-01-02T12:52:09Z</t:DateTimeReceived>
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

<a name="bk_versiondiffs"> </a>

## <a name="version-differences"></a>Diferencias de versión

Cuando usa Exchange Server 2010 Service Pack 1 (SP1), el método [FindConversation](https://msdn.microsoft.com/library/office/jj220668%28v=exchg.80%29.aspx) tiene menos opciones disponibles y la operación [FindConversation](https://msdn.microsoft.com/library/2384908a-c203-45b6-98aa-efd6a4c23aac%28Office.15%29.aspx) tiene menos elementos en la solicitud. 
  
**Tabla 3. Exchange versión de 2010 SP1 para FindConversation**

|**Método de la API administrada de EWS**|**Elementos EWS**|
|:-----|:-----|
|[FindConversation (ViewBase, FolderId)](https://msdn.microsoft.com/library/office/jj220668%28v=exchg.80%29.aspx) <br/> |[IndexedPageItemView](https://msdn.microsoft.com/library/6d1b0b04-cc35-4a57-bd7a-824136d14fda%28Office.15%29.aspx) <br/> [SortOrder](https://msdn.microsoft.com/library/c2413f0b-8c03-46ae-9990-13338b3c53a6%28Office.15%29.aspx) <br/> [ParentFolderId](https://msdn.microsoft.com/library/0e3e6e5f-06d0-499b-8ca4-d36036521658%28Office.15%29.aspx) <br/> |
   
El método de API administrada EWS [GetConversationItems](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice.getconversationitems%28v=exchg.80%29.aspx) y la operación EWS [GetConversationItems](https://msdn.microsoft.com/library/8ae00a99-b37b-4194-829c-fe300db6ab99%28Office.15%29.aspx) se introdujeron en Exchange Server 2013. Las aplicaciones destinadas a versiones anteriores de Exchange solo pueden aplicar acciones de conversación a las conversaciones, como se muestra en la tabla 2. 
  
El método de la API administrada ews **FindConversation** y el método **EWS FindConversation** no están disponibles en la versión de lanzamiento inicial de Exchange 2010 o en Exchange 2007. 
  
## <a name="see-also"></a>Ver también

- [Correo electrónico y EWS en Exchange](email-and-ews-in-exchange.md)
- [Usar filtros de búsqueda con EWS en Exchange](how-to-use-search-filters-with-ews-in-exchange.md)   
- [Exchange 2013: Buscar conversaciones en buzones mediante programación](https://code.msdn.microsoft.com/exchange/Exchange-2013-Find-d4b6b3af)    
- [Exchange 2013: Aplicar acciones para administrar conversaciones en un buzón](https://code.msdn.microsoft.com/exchange/Exchange-2013-Apply-accde0b5)
    

