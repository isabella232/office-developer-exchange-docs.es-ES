---
title: Trabajar con las conversaciones con EWS en Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 7750528c-acb2-43e5-a1e1-ee201c0e1730
description: Obtenga información sobre cómo buscar conversaciones, las acciones se aplican a las conversaciones y obtener elementos en conversaciones mediante el uso de la API administrada de EWS o EWS en Exchange.
ms.openlocfilehash: 71ef7674086607e1544111071928f3dd74073a77
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763201"
---
# <a name="work-with-conversations-by-using-ews-in-exchange"></a><span data-ttu-id="ac0ef-103">Trabajar con las conversaciones con EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="ac0ef-103">Work with conversations by using EWS in Exchange</span></span>

<span data-ttu-id="ac0ef-104">Obtenga información sobre cómo buscar conversaciones, las acciones se aplican a las conversaciones y obtener elementos en conversaciones mediante el uso de la API administrada de EWS o EWS en Exchange.</span><span class="sxs-lookup"><span data-stu-id="ac0ef-104">Learn about how to find conversations, apply actions to conversations, and get items in conversations by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="ac0ef-105">En el contexto de Exchange, las conversaciones son una forma de grupo y administrar un conjunto relacionado de mensajes de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="ac0ef-105">In the context of Exchange, conversations are a way to group and manage a related set of email messages.</span></span> <span data-ttu-id="ac0ef-106">También pueden proporcionar una manera de ver los mensajes relacionados.</span><span class="sxs-lookup"><span data-stu-id="ac0ef-106">They can also provide a way to view related messages.</span></span> <span data-ttu-id="ac0ef-107">Exchange define las conversaciones en función del valor de **Identificador de mensaje** del primer mensaje de correo electrónico en un subproceso.</span><span class="sxs-lookup"><span data-stu-id="ac0ef-107">Exchange defines conversations based on the **Message-ID** value of the first email message in a thread.</span></span> <span data-ttu-id="ac0ef-108">Encabezado de **Identificador de mensaje** del mensaje original en sus **referencias de** hacer referencia a todos los mensajes o respuestas de relacionados y **En respuesta a** los encabezados.</span><span class="sxs-lookup"><span data-stu-id="ac0ef-108">All replies and related messages reference the original message's **Message-ID** header in their **References** and **In-Reply-To** headers.</span></span> 
  
<span data-ttu-id="ac0ef-109">Además, dentro de la envoltura SOAP, para cada mensaje recibido en un buzón de correo, Exchange establece los elementos y propiedades específicas.</span><span class="sxs-lookup"><span data-stu-id="ac0ef-109">Additionally, inside the SOAP envelope, for each message received in a mailbox, Exchange sets specific properties and elements.</span></span>
  
<span data-ttu-id="ac0ef-110">**La tabla 1. Propiedades de conversación y los elementos que se establezca en todos los mensajes de correo electrónico**</span><span class="sxs-lookup"><span data-stu-id="ac0ef-110">**Table 1. Conversation properties and elements set on all email messages**</span></span>

|<span data-ttu-id="ac0ef-111">**Propiedad de la API administrada de EWS**</span><span class="sxs-lookup"><span data-stu-id="ac0ef-111">**EWS Managed API property**</span></span>|<span data-ttu-id="ac0ef-112">**Elemento EWS**</span><span class="sxs-lookup"><span data-stu-id="ac0ef-112">**EWS element**</span></span>|<span data-ttu-id="ac0ef-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ac0ef-113">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ac0ef-114">ConversationTopic</span><span class="sxs-lookup"><span data-stu-id="ac0ef-114">ConversationTopic</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.conversationtopic%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="ac0ef-115">ConversationTopic</span><span class="sxs-lookup"><span data-stu-id="ac0ef-115">ConversationTopic</span></span>](http://msdn.microsoft.com/library/46cacf42-4039-4c8a-9b20-c42cdd9f2760%28Office.15%29.aspx) <br/> |<span data-ttu-id="ac0ef-116">Contiene un formulario normalizado del valor de asunto que se estableció en el mensaje original.</span><span class="sxs-lookup"><span data-stu-id="ac0ef-116">Contains a normalized form of the subject value that was set on the original message.</span></span> <span data-ttu-id="ac0ef-117">Esto es el mismo que el encabezado del mensaje de **Tema de subproceso** .</span><span class="sxs-lookup"><span data-stu-id="ac0ef-117">This is the same as the **Thread-Topic** message header.</span></span> <span data-ttu-id="ac0ef-118">Este valor es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="ac0ef-118">This value is read-only.</span></span>  <br/> |
|[<span data-ttu-id="ac0ef-119">ConversationIndex</span><span class="sxs-lookup"><span data-stu-id="ac0ef-119">ConversationIndex</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.conversationindex%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="ac0ef-120">ConversationIndex</span><span class="sxs-lookup"><span data-stu-id="ac0ef-120">ConversationIndex</span></span>](http://msdn.microsoft.com/library/fdf47e22-8d93-4ae4-883b-0c9f07f48724%28Office.15%29.aspx) <br/> |<span data-ttu-id="ac0ef-121">Representa la posición del elemento en la conversación.</span><span class="sxs-lookup"><span data-stu-id="ac0ef-121">Represents the position of the item in the conversation.</span></span> <span data-ttu-id="ac0ef-122">Esto es el mismo que el encabezado del mensaje de **Subproceso de índice** .</span><span class="sxs-lookup"><span data-stu-id="ac0ef-122">This is the same as the **Thread-Index** message header.</span></span> <span data-ttu-id="ac0ef-123">Este valor es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="ac0ef-123">This value is read-only.</span></span>  <br/> |
   
<span data-ttu-id="ac0ef-124">Exchange aplica el mismo valor de **ConversationTopic** respuestas en el primer mensaje y, a continuación, actualiza el valor de **ConversationIndex** para representar la posición del mensaje en relación con el mensaje original.</span><span class="sxs-lookup"><span data-stu-id="ac0ef-124">Exchange applies the same **ConversationTopic** value to replies to the first message and then updates the **ConversationIndex** value to represent the message's position relative to the original message.</span></span> <span data-ttu-id="ac0ef-125">Si cambia el asunto de la secuencia de correo electrónico, Exchange aplica a un nuevo valor **ConversationTopic** y nuevos valores **ConversationIndex** a la nueva conversación.</span><span class="sxs-lookup"><span data-stu-id="ac0ef-125">If the subject of the email thread changes, Exchange applies a new **ConversationTopic** value and new **ConversationIndex** values to the new conversation.</span></span> 
  
<span data-ttu-id="ac0ef-126">**Tabla 2. Métodos de la API administrada de EWS y las operaciones de EWS para trabajar con las conversaciones**</span><span class="sxs-lookup"><span data-stu-id="ac0ef-126">**Table 2. EWS Managed API methods and EWS operations for working with conversations**</span></span>

|<span data-ttu-id="ac0ef-127">**Con el fin...**</span><span class="sxs-lookup"><span data-stu-id="ac0ef-127">**In order to…**</span></span>|<span data-ttu-id="ac0ef-128">**Use este método de la API administrada de EWS o métodos**</span><span class="sxs-lookup"><span data-stu-id="ac0ef-128">**Use this EWS Managed API method or methods**</span></span>|<span data-ttu-id="ac0ef-129">**Use esta operación de EWS**</span><span class="sxs-lookup"><span data-stu-id="ac0ef-129">**Use this EWS operation**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ac0ef-130">Buscar conversaciones</span><span class="sxs-lookup"><span data-stu-id="ac0ef-130">Find conversations</span></span>  <br/> |[<span data-ttu-id="ac0ef-131">ExchangeService.FindConversation</span><span class="sxs-lookup"><span data-stu-id="ac0ef-131">ExchangeService.FindConversation</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.findconversation%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="ac0ef-132">FindConversation</span><span class="sxs-lookup"><span data-stu-id="ac0ef-132">FindConversation</span></span>](http://msdn.microsoft.com/library/2384908a-c203-45b6-98aa-efd6a4c23aac%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="ac0ef-133">Aplicar acciones de conversación</span><span class="sxs-lookup"><span data-stu-id="ac0ef-133">Apply conversation actions</span></span>  <br/> |[<span data-ttu-id="ac0ef-134">Conversation.EnableAlwaysCategorizeItems</span><span class="sxs-lookup"><span data-stu-id="ac0ef-134">Conversation.EnableAlwaysCategorizeItems</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.conversation.enablealwayscategorizeitems%28v=exchg.80%29.aspx) <br/> [<span data-ttu-id="ac0ef-135">Conversation.EnableAlwaysDeleteItems</span><span class="sxs-lookup"><span data-stu-id="ac0ef-135">Conversation.EnableAlwaysDeleteItems</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.conversation.enablealwaysdeleteitems%28v=exchg.80%29.aspx) <br/> [<span data-ttu-id="ac0ef-136">Conversation.EnableAlwaysMoveItems</span><span class="sxs-lookup"><span data-stu-id="ac0ef-136">Conversation.EnableAlwaysMoveItems</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.conversation.enablealwaysmoveitems%28v=exchg.80%29.aspx) <br/> [<span data-ttu-id="ac0ef-137">ExchangeService.CopyItemsInConversations</span><span class="sxs-lookup"><span data-stu-id="ac0ef-137">ExchangeService.CopyItemsInConversations</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.copyitemsinconversations%28v=exchg.80%29.aspx) <br/> [<span data-ttu-id="ac0ef-138">ExchangeService.DeleteItemsInConversations</span><span class="sxs-lookup"><span data-stu-id="ac0ef-138">ExchangeService.DeleteItemsInConversations</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.deleteitemsinconversations%28v=exchg.80%29.aspx) <br/> [<span data-ttu-id="ac0ef-139">ExchangeService.DisableAlwaysCategorizeItemsInConversations</span><span class="sxs-lookup"><span data-stu-id="ac0ef-139">ExchangeService.DisableAlwaysCategorizeItemsInConversations</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.disablealwayscategorizeitemsinconversations%28v=exchg.80%29.aspx) <br/> [<span data-ttu-id="ac0ef-140">ExchangeService.DisableAlwaysDeleteItemsInConversations</span><span class="sxs-lookup"><span data-stu-id="ac0ef-140">ExchangeService.DisableAlwaysDeleteItemsInConversations</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.disablealwaysdeleteitemsinconversations%28v=exchg.80%29.aspx) <br/> [<span data-ttu-id="ac0ef-141">ExchangeService.DisableAlwaysMoveItemsInConversations</span><span class="sxs-lookup"><span data-stu-id="ac0ef-141">ExchangeService.DisableAlwaysMoveItemsInConversations</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.disablealwaysmoveitemsinconversations%28v=exchg.80%29.aspx) <br/> [<span data-ttu-id="ac0ef-142">ExchangeService.EnableAlwaysCategorizeItemsInConversations</span><span class="sxs-lookup"><span data-stu-id="ac0ef-142">ExchangeService.EnableAlwaysCategorizeItemsInConversations</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.enablealwayscategorizeitemsinconversations%28v=exchg.80%29.aspx) <br/> [<span data-ttu-id="ac0ef-143">ExchangeService.EnableAlwaysDeleteItemsInConversations</span><span class="sxs-lookup"><span data-stu-id="ac0ef-143">ExchangeService.EnableAlwaysDeleteItemsInConversations</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.enablealwaysdeleteitemsinconversations%28v=exchg.80%29.aspx) <br/> [<span data-ttu-id="ac0ef-144">ExchangeService.EnableAlwaysMoveItemsInConversations</span><span class="sxs-lookup"><span data-stu-id="ac0ef-144">ExchangeService.EnableAlwaysMoveItemsInConversations</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.enablealwaysmoveitemsinconversations%28v=exchg.80%29.aspx) <br/> [<span data-ttu-id="ac0ef-145">ExchangeService.MoveItemsInConversations</span><span class="sxs-lookup"><span data-stu-id="ac0ef-145">ExchangeService.MoveItemsInConversations</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.moveitemsinconversations%28v=exchg.80%29.aspx) <br/> [<span data-ttu-id="ac0ef-146">ExchangeService.SetFlagStatusForItemsInConversations</span><span class="sxs-lookup"><span data-stu-id="ac0ef-146">ExchangeService.SetFlagStatusForItemsInConversations</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.setflagstatusforitemsinconversations%28v=exchg.80%29.aspx) <br/> [<span data-ttu-id="ac0ef-147">ExchangeService.SetReadStateForItemsInConversations</span><span class="sxs-lookup"><span data-stu-id="ac0ef-147">ExchangeService.SetReadStateForItemsInConversations</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.setreadstateforitemsinconversations%28v=exchg.80%29.aspx) <br/> [<span data-ttu-id="ac0ef-148">ExchangeService.SetRetentionPolicyForItemsInConversations</span><span class="sxs-lookup"><span data-stu-id="ac0ef-148">ExchangeService.SetRetentionPolicyForItemsInConversations</span></span>](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.exchangeservice.setretentionpolicyforitemsinconversations%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="ac0ef-149">ApplyConversationAction</span><span class="sxs-lookup"><span data-stu-id="ac0ef-149">ApplyConversationAction</span></span>](http://msdn.microsoft.com/library/73d7943d-d361-4f8b-9948-d85f886efa1a%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="ac0ef-150">Obtener elementos en las conversaciones de uno o más</span><span class="sxs-lookup"><span data-stu-id="ac0ef-150">Get items in one or more conversations</span></span>  <br/> |[<span data-ttu-id="ac0ef-151">ExchangeService.GetConversationItems</span><span class="sxs-lookup"><span data-stu-id="ac0ef-151">ExchangeService.GetConversationItems</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.getconversationitems%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="ac0ef-152">GetConversationItems</span><span class="sxs-lookup"><span data-stu-id="ac0ef-152">GetConversationItems</span></span>](http://msdn.microsoft.com/library/8ae00a99-b37b-4194-829c-fe300db6ab99%28Office.15%29.aspx) <br/> |

<span data-ttu-id="ac0ef-153"><a name="bk_findewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="ac0ef-153"></span></span>

## <a name="find-a-conversation-by-using-the-ews-managed-api"></a><span data-ttu-id="ac0ef-154">Buscar una conversación mediante el uso de la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="ac0ef-154">Find a conversation by using the EWS Managed API</span></span>

<span data-ttu-id="ac0ef-155">Puede buscar conversaciones mediante el método de la API administrada de EWS [ExchangeService.FindConversation](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.findconversation%28v=exchg.80%29.aspx) , tal como se muestra en el siguiente ejemplo.</span><span class="sxs-lookup"><span data-stu-id="ac0ef-155">You can find conversations by using the [ExchangeService.FindConversation](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.findconversation%28v=exchg.80%29.aspx) EWS Managed API method, as shown in the following example.</span></span> <span data-ttu-id="ac0ef-156">En este ejemplo se obtiene las 10 primeros conversaciones en la carpeta Bandeja de entrada que tienen un asunto que contiene la palabra "noticias".</span><span class="sxs-lookup"><span data-stu-id="ac0ef-156">This example gets the first 10 conversations in the Inbox folder that have a subject that contains the word "news".</span></span> <span data-ttu-id="ac0ef-157">En el ejemplo, a continuación, escribe el tema de conversación, última hora de entrega y lista global de destinatarios único en la ventana de la consola.</span><span class="sxs-lookup"><span data-stu-id="ac0ef-157">The example then writes the conversation topic, last delivery time, and global unique recipient list to the console window.</span></span> 
  
<span data-ttu-id="ac0ef-158">En este ejemplo se da por supuesto que **servicio** es un objeto [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) válido y que se ha autenticado el usuario a un servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="ac0ef-158">This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and that the user has been authenticated to an Exchange server.</span></span> 
  
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

<span data-ttu-id="ac0ef-159"><a name="bk_findews"> </a></span><span class="sxs-lookup"><span data-stu-id="ac0ef-159"></span></span>

## <a name="find-a-conversation-by-using-ews"></a><span data-ttu-id="ac0ef-160">Buscar una conversación mediante el uso de EWS</span><span class="sxs-lookup"><span data-stu-id="ac0ef-160">Find a conversation by using EWS</span></span>

<span data-ttu-id="ac0ef-161">Puede buscar conversaciones mediante el uso de la operación de EWS [FindConversation](http://msdn.microsoft.com/library/2384908a-c203-45b6-98aa-efd6a4c23aac%28Office.15%29.aspx) , tal como se muestra en el siguiente ejemplo.</span><span class="sxs-lookup"><span data-stu-id="ac0ef-161">You can find conversations by using the [FindConversation](http://msdn.microsoft.com/library/2384908a-c203-45b6-98aa-efd6a4c23aac%28Office.15%29.aspx) EWS operation, as shown in the following example.</span></span> <span data-ttu-id="ac0ef-162">En este ejemplo se obtiene las diez primeros conversaciones en la carpeta Bandeja de entrada que tienen un asunto que contiene la palabra "noticias".</span><span class="sxs-lookup"><span data-stu-id="ac0ef-162">This example gets the first ten conversations in the Inbox folder that have a subject that contains the word "news".</span></span> <span data-ttu-id="ac0ef-163">También es la solicitud XML que la API administrada de EWS envía al usar la API administrada de EWS para [Buscar una conversación](#bk_findewsma).</span><span class="sxs-lookup"><span data-stu-id="ac0ef-163">This is also the XML request that the EWS Managed API sends when you use the EWS Managed API to [find a conversation](#bk_findewsma).</span></span>
  
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

<span data-ttu-id="ac0ef-164">El servidor responde a la solicitud de **FindConversation** con un mensaje de [FindConversationResponse](http://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) que incluye un valor [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) de **NoError** para indicar que la operación que se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="ac0ef-164">The server responds to the **FindConversation** request with a [FindConversationResponse](http://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) value of **NoError** to indicate that the operation completed successfully.</span></span> <span data-ttu-id="ac0ef-165">La respuesta incluye también la conversación sólo en el buzón de correo que tiene un asunto que contiene la palabra "noticias".</span><span class="sxs-lookup"><span data-stu-id="ac0ef-165">The response also includes the only conversation in the mailbox that has a subject that contains the word "news".</span></span> 
  
<span data-ttu-id="ac0ef-166">Los elementos **ItemId**, **ChangeKey**y **ConversationId** se han abreviado para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="ac0ef-166">The **ItemId**, **ChangeKey**, and **ConversationId** elements have been shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="883"
                         MinorBuildNumber="10"
                         Version="V2_10"
                         xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <FindConversationResponse ResponseClass="Success"
                              xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
      <Conversations>
        <Conversation xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
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

<span data-ttu-id="ac0ef-167"><a name="bk_applyewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="ac0ef-167"></span></span>

## <a name="apply-conversation-actions-by-using-the-ews-managed-api"></a><span data-ttu-id="ac0ef-168">Aplicar acciones de conversación mediante el uso de la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="ac0ef-168">Apply conversation actions by using the EWS Managed API</span></span>

<span data-ttu-id="ac0ef-169">Puede aplicar acciones de conversación a una conversación con un número de métodos de la API administrada de EWS, tal como se muestra en el siguiente ejemplo.</span><span class="sxs-lookup"><span data-stu-id="ac0ef-169">You can apply conversation actions to a conversation by using a number of EWS Managed API methods, as shown in the following example.</span></span> <span data-ttu-id="ac0ef-170">En este ejemplo se agregan categorías a los elementos existentes en una conversación y se aplica a las mismas categorías a elementos futuros de la conversación.</span><span class="sxs-lookup"><span data-stu-id="ac0ef-170">This example adds categories to existing items in a conversation and applies the same categories to future items in the conversation.</span></span> <span data-ttu-id="ac0ef-171">También muestra cómo habilitar el movimiento automático de los elementos de la conversación a una carpeta.</span><span class="sxs-lookup"><span data-stu-id="ac0ef-171">It also shows how to enable the automatic moving of items in the conversation to a folder.</span></span> <span data-ttu-id="ac0ef-172">En este ejemplo, se mueven los elementos en la carpeta Borradores.</span><span class="sxs-lookup"><span data-stu-id="ac0ef-172">In this example, items are moved to the Drafts folder.</span></span>
  
<span data-ttu-id="ac0ef-173">En este ejemplo se da por supuesto que **servicio** es un objeto [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) válido y que se ha autenticado el usuario a un servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="ac0ef-173">This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and that the user has been authenticated to an Exchange server.</span></span> 
  
<span data-ttu-id="ac0ef-174">Para obtener una lista completa de los métodos que se aplican las acciones de conversación, vea la tabla 2.</span><span class="sxs-lookup"><span data-stu-id="ac0ef-174">For a complete list of methods that apply conversation actions, see Table 2.</span></span>
  
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

<span data-ttu-id="ac0ef-175"><a name="bk_applyews"> </a></span><span class="sxs-lookup"><span data-stu-id="ac0ef-175"></span></span>

## <a name="apply-conversation-actions-by-using-ews"></a><span data-ttu-id="ac0ef-176">Aplicar acciones de conversación mediante el uso de EWS</span><span class="sxs-lookup"><span data-stu-id="ac0ef-176">Apply conversation actions by using EWS</span></span>

<span data-ttu-id="ac0ef-177">Puede aplicar acciones de conversación, tales como clasificar, eliminar y mover, mediante la operación [ApplyConversationAction](http://msdn.microsoft.com/library/73d7943d-d361-4f8b-9948-d85f886efa1a%28Office.15%29.aspx) , tal como se muestra en el siguiente ejemplo.</span><span class="sxs-lookup"><span data-stu-id="ac0ef-177">You can apply conversation actions, such as categorize, delete, and move, by using the [ApplyConversationAction](http://msdn.microsoft.com/library/73d7943d-d361-4f8b-9948-d85f886efa1a%28Office.15%29.aspx) operation, as shown in the following example.</span></span> <span data-ttu-id="ac0ef-178">En este ejemplo se agregan categorías a los elementos existentes en una conversación y se aplica a las mismas categorías a elementos futuros de la conversación.</span><span class="sxs-lookup"><span data-stu-id="ac0ef-178">This example adds categories to existing items in a conversation and applies the same categories to future items in the conversation.</span></span> <span data-ttu-id="ac0ef-179">También se muestra cómo habilitar el movimiento automático de los elementos de la conversación en una carpeta; en este ejemplo, se mueven los elementos en la carpeta Borradores.</span><span class="sxs-lookup"><span data-stu-id="ac0ef-179">It also shows how to enable the automatic moving of items in the conversation to a folder; in this example, items are moved to the Drafts folder.</span></span> <span data-ttu-id="ac0ef-180">También es la solicitud XML que la API administrada de EWS envía al usar la API administrada de EWS para [aplicar acciones de conversación](#bk_applyewsma).</span><span class="sxs-lookup"><span data-stu-id="ac0ef-180">This is also the XML request that the EWS Managed API sends when you use the EWS Managed API to [apply conversation actions](#bk_applyewsma).</span></span>
  
<span data-ttu-id="ac0ef-181">El elemento **ConversationId** se ha acortado para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="ac0ef-181">The **ConversationId** element has been shortened for readability.</span></span> 
  
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

<span data-ttu-id="ac0ef-182">El servidor responde a la solicitud de **ApplyConversationAction** con un mensaje de [ApplyConversationActionResponse](http://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) que incluye un valor [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) de **NoError** para indicar que la operación que se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="ac0ef-182">The server responds to the **ApplyConversationAction** request with a [ApplyConversationActionResponse](http://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) value of **NoError** to indicate that the operation completed successfully.</span></span> 

<span data-ttu-id="ac0ef-183"><a name="bk_getitemssingleewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="ac0ef-183"></span></span>

## <a name="get-items-in-a-single-conversation-by-using-the-conversation-identifier-in-the-ews-managed-api"></a><span data-ttu-id="ac0ef-184">Obtener elementos en una conversación única usando el identificador de conversación en la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="ac0ef-184">Get items in a single conversation by using the conversation identifier in the EWS Managed API</span></span>

<span data-ttu-id="ac0ef-185">Puede obtener elementos en una conversación con el método de la API administrada de EWS [ExchangeService.GetConversationItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.getconversationitems%28v=exchg.80%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="ac0ef-185">You can get items in a conversation by using the [ExchangeService.GetConversationItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.getconversationitems%28v=exchg.80%29.aspx) EWS Managed API method.</span></span> <span data-ttu-id="ac0ef-186">En este ejemplo se proporciona el conjunto de nodos de conversación para la primera conversación en la Bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="ac0ef-186">This example provides the set of conversation nodes for the first conversation in the Inbox.</span></span> <span data-ttu-id="ac0ef-187">El identificador de elemento, el asunto y la hora de recepción para cada elemento se devuelven en la respuesta, junto con las propiedades conversación índice de conversación de índice y primario.</span><span class="sxs-lookup"><span data-stu-id="ac0ef-187">The item identifier, subject, and received time for each item are returned in the response, along with the conversation index and parent conversation index properties.</span></span> <span data-ttu-id="ac0ef-188">Puede usar las propiedades de índice de conversación para reconstruir la jerarquía de nodos.</span><span class="sxs-lookup"><span data-stu-id="ac0ef-188">You can use the conversation index properties to reconstruct the node hierarchy.</span></span> 
  
<span data-ttu-id="ac0ef-189">En este ejemplo, se omiten todos los elementos de una conversación en las carpetas de elementos eliminados y borradores de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="ac0ef-189">In this example, all conversation items in the default Deleted Items and Drafts folders are ignored.</span></span>
  
<span data-ttu-id="ac0ef-190">En este ejemplo se da por supuesto que **servicio** es un objeto [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) válido y que se ha autenticado el usuario a un servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="ac0ef-190">This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and that the user has been authenticated to an Exchange server.</span></span> 
  
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

<span data-ttu-id="ac0ef-191">Se recomienda que almacena en caché la propiedad de **estado de sincronización** para las solicitudes posteriores obtener los elementos de la conversación.</span><span class="sxs-lookup"><span data-stu-id="ac0ef-191">We recommend that you cache the **SyncState** property for subsequent requests to get items in the conversation.</span></span> 

<span data-ttu-id="ac0ef-192"><a name="bk_getitemsmanyewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="ac0ef-192"></span></span>

## <a name="get-items-in-many-conversations-by-using-the-conversationrequest-object-in-the-ews-managed-api"></a><span data-ttu-id="ac0ef-193">Obtener elementos en muchas conversaciones mediante el objeto ConversationRequest en la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="ac0ef-193">Get items in many conversations by using the ConversationRequest object in the EWS Managed API</span></span>

<span data-ttu-id="ac0ef-194">Puede usar el objeto [ConversationRequest](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.conversationrequest%28v=exchg.80%29.aspx) y el método de la API administrada de EWS [ExchangeService.GetConversationItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.getconversationitems%28v=exchg.80%29.aspx) para obtener elementos de las conversaciones de dos o más.</span><span class="sxs-lookup"><span data-stu-id="ac0ef-194">You can use the [ConversationRequest](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.conversationrequest%28v=exchg.80%29.aspx) object and the [ExchangeService.GetConversationItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.getconversationitems%28v=exchg.80%29.aspx) EWS Managed API method to get items from two or more conversations.</span></span> <span data-ttu-id="ac0ef-195">En este ejemplo se proporciona un conjunto de nodos de conversación para las dos primeras conversaciones en la Bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="ac0ef-195">This example provides a set of conversation nodes for the first two conversations in the Inbox.</span></span> <span data-ttu-id="ac0ef-196">En la respuesta, junto con la conversación primario conversación índice las propiedades index y se devolverá el identificador de elemento, el asunto y la hora de recepción para cada elemento.</span><span class="sxs-lookup"><span data-stu-id="ac0ef-196">The item identifier, subject, and the received time for each item will be returned in the response, along with the conversation index and parent conversation index properties.</span></span> <span data-ttu-id="ac0ef-197">Puede usar las propiedades de índice de conversación para reconstruir la jerarquía de nodos.</span><span class="sxs-lookup"><span data-stu-id="ac0ef-197">You can use the conversation index properties to reconstruct the node hierarchy.</span></span> <span data-ttu-id="ac0ef-198">En este ejemplo se supone que los dos primeros elementos en la Bandeja de entrada son de conversaciones diferentes.</span><span class="sxs-lookup"><span data-stu-id="ac0ef-198">This example assumes that the first two items in the Inbox are from different conversations.</span></span> 
  
<span data-ttu-id="ac0ef-199">En este ejemplo, se omiten todos los elementos de una conversación en las carpetas de elementos eliminados y borradores de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="ac0ef-199">In this example, all conversation items in the default Deleted Items and Drafts folders are ignored.</span></span>
  
<span data-ttu-id="ac0ef-200">En este ejemplo se da por supuesto que **servicio** es un objeto [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) válido y que se ha autenticado el usuario a un servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="ac0ef-200">This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and that the user has been authenticated to an Exchange server.</span></span> 
  
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

<span data-ttu-id="ac0ef-201">Como procedimiento recomendado, se recomienda que devolver sólo las propiedades que requiere la aplicación cliente, en lugar de utilizar la opción **FirstClassProperties** para la clase **BasePropertySet** .</span><span class="sxs-lookup"><span data-stu-id="ac0ef-201">As a best practice, we recommend that you return only the properties that the client application requires, rather than using the **FirstClassProperties** option for the **BasePropertySet** class.</span></span> <span data-ttu-id="ac0ef-202">Se recomienda que almacena en caché la propiedad de **estado de sincronización** para las solicitudes posteriores obtener los elementos de la conversación.</span><span class="sxs-lookup"><span data-stu-id="ac0ef-202">We recommend that you cache the **SyncState** property for subsequent requests to get items in the conversation.</span></span> 

<span data-ttu-id="ac0ef-203"><a name="bk_getitemsews"> </a></span><span class="sxs-lookup"><span data-stu-id="ac0ef-203"></span></span>

## <a name="get-items-in-conversations-by-using-the-conversation-identifier-in-ews"></a><span data-ttu-id="ac0ef-204">Obtener elementos en conversaciones mediante el identificador de conversación de EWS</span><span class="sxs-lookup"><span data-stu-id="ac0ef-204">Get items in conversations by using the conversation identifier in EWS</span></span>

<span data-ttu-id="ac0ef-205">Puede obtener elementos en una conversación mediante el uso de la operación de EWS [GetConversationItems](http://msdn.microsoft.com/library/8ae00a99-b37b-4194-829c-fe300db6ab99%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="ac0ef-205">You can get items in a conversation by using the [GetConversationItems](http://msdn.microsoft.com/library/8ae00a99-b37b-4194-829c-fe300db6ab99%28Office.15%29.aspx) EWS operation.</span></span> <span data-ttu-id="ac0ef-206">En este ejemplo se proporciona un conjunto de nodos de conversación para la primera conversación en la Bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="ac0ef-206">This example provides a set of conversation nodes for the first conversation in the Inbox.</span></span> <span data-ttu-id="ac0ef-207">El identificador de elemento, el asunto y la hora de recepción para cada elemento se devuelven en la respuesta, junto con las propiedades conversación índice de conversación de índice y primario.</span><span class="sxs-lookup"><span data-stu-id="ac0ef-207">The item identifier, subject, and received time for each item are returned in the response, along with the conversation index and parent conversation index properties.</span></span> <span data-ttu-id="ac0ef-208">Puede usar las propiedades de índice de conversación para reconstruir la jerarquía de nodos.</span><span class="sxs-lookup"><span data-stu-id="ac0ef-208">You can use the conversation index properties to reconstruct the node hierarchy.</span></span> 
  
<span data-ttu-id="ac0ef-209">En este ejemplo, se omiten todos los elementos de una conversación en las carpetas de elementos eliminados y borradores de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="ac0ef-209">In this example, all conversation items in the default Deleted Items and Drafts folders are ignored.</span></span>
  
<span data-ttu-id="ac0ef-210">El elemento **ConversationId** se ha acortado para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="ac0ef-210">The **ConversationId** element has been shortened for readability.</span></span> 
  
<span data-ttu-id="ac0ef-211">Para obtener los elementos de más de una conversación, incluir elementos adicionales de **conversación** .</span><span class="sxs-lookup"><span data-stu-id="ac0ef-211">To get items from more than one conversation, include additional **Conversation** elements.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m=http://schemas.microsoft.com/exchange/services/2006/messages
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
          <t:ConversationId Id="LUQFH6Q=" />
        </t:Conversation>
      </m:Conversations>
    </m:GetConversationItems>
  </soap:Body>
</soap:Envelope>
```

El servidor responde a la solicitud de **GetConversationItems** con un mensaje de [GetConversationItemsResponse](http://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) que incluye un valor [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) de **NoError** para indicar que la operación que se realizó correctamente. <span data-ttu-id="ac0ef-213">La respuesta incluye también la [ConversationNodes](http://msdn.microsoft.com/library/5c8a35b8-a940-4b3e-8768-9ba95766fd79%28Office.15%29.aspx) en la conversación.</span><span class="sxs-lookup"><span data-stu-id="ac0ef-213">The response also includes the [ConversationNodes](http://msdn.microsoft.com/library/5c8a35b8-a940-4b3e-8768-9ba95766fd79%28Office.15%29.aspx) in the conversation.</span></span> 
  
<span data-ttu-id="ac0ef-214">Los elementos **ItemId**, **estado de sincronización**y **ConversationId** se han abreviado para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="ac0ef-214">The **ItemId**, **SyncState**, and **ConversationId** elements have been shortened for readability.</span></span> 
  
```XML
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="873"
                         MinorBuildNumber="9"
                         Version="V2_9"
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

<span data-ttu-id="ac0ef-215"><a name="bk_versiondiffs"> </a></span><span class="sxs-lookup"><span data-stu-id="ac0ef-215"></span></span>

## <a name="version-differences"></a><span data-ttu-id="ac0ef-216">Diferencias de versión</span><span class="sxs-lookup"><span data-stu-id="ac0ef-216">Version differences</span></span>

<span data-ttu-id="ac0ef-217">Cuando se usa Exchange Server 2010 Service Pack 1 (SP1), el método [FindConversation](http://msdn.microsoft.com/en-us/library/office/jj220668%28v=exchg.80%29.aspx) tiene menos opciones disponibles, y la operación de [FindConversation](http://msdn.microsoft.com/library/2384908a-c203-45b6-98aa-efd6a4c23aac%28Office.15%29.aspx) tiene menos elementos en la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ac0ef-217">When you are using Exchange Server 2010 Service Pack 1 (SP1), the [FindConversation](http://msdn.microsoft.com/en-us/library/office/jj220668%28v=exchg.80%29.aspx) method has fewer options available, and the [FindConversation](http://msdn.microsoft.com/library/2384908a-c203-45b6-98aa-efd6a4c23aac%28Office.15%29.aspx) operation has fewer elements in the request.</span></span> 
  
<span data-ttu-id="ac0ef-218">**Tabla 3. Compatibilidad con la versión de Exchange 2010 SP1 para FindConversation**</span><span class="sxs-lookup"><span data-stu-id="ac0ef-218">**Table 3. Exchange 2010 SP1 version support for FindConversation**</span></span>

|<span data-ttu-id="ac0ef-219">**Método de la API administrada de EWS**</span><span class="sxs-lookup"><span data-stu-id="ac0ef-219">**EWS Managed API method**</span></span>|<span data-ttu-id="ac0ef-220">**Elementos EWS**</span><span class="sxs-lookup"><span data-stu-id="ac0ef-220">**EWS elements**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ac0ef-221">FindConversation (ViewBase, FolderId)</span><span class="sxs-lookup"><span data-stu-id="ac0ef-221">FindConversation (ViewBase, FolderId)</span></span>](http://msdn.microsoft.com/en-us/library/office/jj220668%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="ac0ef-222">IndexedPageItemView</span><span class="sxs-lookup"><span data-stu-id="ac0ef-222">IndexedPageItemView</span></span>](http://msdn.microsoft.com/library/6d1b0b04-cc35-4a57-bd7a-824136d14fda%28Office.15%29.aspx) <br/> [<span data-ttu-id="ac0ef-223">SortOrder</span><span class="sxs-lookup"><span data-stu-id="ac0ef-223">SortOrder</span></span>](http://msdn.microsoft.com/library/c2413f0b-8c03-46ae-9990-13338b3c53a6%28Office.15%29.aspx) <br/> [<span data-ttu-id="ac0ef-224">Id</span><span class="sxs-lookup"><span data-stu-id="ac0ef-224">ParentFolderId</span></span>](http://msdn.microsoft.com/library/0e3e6e5f-06d0-499b-8ca4-d36036521658%28Office.15%29.aspx) <br/> |
   
<span data-ttu-id="ac0ef-225">El método de la API administrada de EWS [GetConversationItems](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.exchangeservice.getconversationitems%28v=exchg.80%29.aspx) y la operación de EWS [GetConversationItems](http://msdn.microsoft.com/library/8ae00a99-b37b-4194-829c-fe300db6ab99%28Office.15%29.aspx) se introdujeron en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="ac0ef-225">The [GetConversationItems](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.exchangeservice.getconversationitems%28v=exchg.80%29.aspx) EWS Managed API method and the [GetConversationItems](http://msdn.microsoft.com/library/8ae00a99-b37b-4194-829c-fe300db6ab99%28Office.15%29.aspx) EWS operation were introduced in Exchange Server 2013.</span></span> <span data-ttu-id="ac0ef-226">Las aplicaciones que estén destinados a versiones anteriores de Exchange sólo pueden aplicar acciones de conversación a las conversaciones, como se muestra en la tabla 2.</span><span class="sxs-lookup"><span data-stu-id="ac0ef-226">Applications that target earlier versions of Exchange can only apply conversation actions to conversations, as listed in Table 2.</span></span> 
  
<span data-ttu-id="ac0ef-227">El método de la API administrada de EWS **FindConversation** y el método EWS **FindConversation** no están disponibles en la versión inicial de Exchange 2010 o de Exchange 2007.</span><span class="sxs-lookup"><span data-stu-id="ac0ef-227">The **FindConversation** EWS Managed API method and the **FindConversation** EWS method are not available in the initial release version of Exchange 2010 or in Exchange 2007.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ac0ef-228">Ver también</span><span class="sxs-lookup"><span data-stu-id="ac0ef-228">See also</span></span>

- [<span data-ttu-id="ac0ef-229">Correo electrónico y EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="ac0ef-229">Email and EWS in Exchange</span></span>](email-and-ews-in-exchange.md)
- [<span data-ttu-id="ac0ef-230">Use los filtros de búsqueda con EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="ac0ef-230">Use search filters with EWS in Exchange</span></span>](how-to-use-search-filters-with-ews-in-exchange.md)   
- [<span data-ttu-id="ac0ef-231">Exchange 2013: Buscar conversaciones en los buzones de correo mediante programación</span><span class="sxs-lookup"><span data-stu-id="ac0ef-231">Exchange 2013: Find conversations in mailboxes programmatically</span></span>](http://code.msdn.microsoft.com/exchange/Exchange-2013-Find-d4b6b3af)    
- [<span data-ttu-id="ac0ef-232">Exchange 2013: Aplicar acciones para administrar las conversaciones de un buzón de correo</span><span class="sxs-lookup"><span data-stu-id="ac0ef-232">Exchange 2013: Apply actions to manage conversations in a mailbox</span></span>](http://code.msdn.microsoft.com/exchange/Exchange-2013-Apply-accde0b5)
    

