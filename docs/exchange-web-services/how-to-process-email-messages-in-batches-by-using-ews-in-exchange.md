---
title: Mensajes de correo electrónico de proceso por lotes mediante el uso de EWS en Exchange
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 96390f92-cab1-4de6-9ec2-a55678fc20af
description: Obtenga información sobre cómo crear, obtener, actualizar y eliminar lotes de mensajes de correo electrónico en una sola llamada mediante la API administrada de EWS o EWS en Exchange.
ms.openlocfilehash: b7dcc8f0961a34061b0476e2136193bf21731d99
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/28/2018
ms.locfileid: "21354046"
---
# <a name="process-email-messages-in-batches-by-using-ews-in-exchange"></a><span data-ttu-id="ef985-103">Mensajes de correo electrónico de proceso por lotes mediante el uso de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="ef985-103">Process email messages in batches by using EWS in Exchange</span></span>

<span data-ttu-id="ef985-104">Obtenga información sobre cómo crear, obtener, actualizar y eliminar lotes de mensajes de correo electrónico en una sola llamada mediante la API administrada de EWS o EWS en Exchange.</span><span class="sxs-lookup"><span data-stu-id="ef985-104">Learn how to create, get, update, and delete batches of email messages in a single call by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="ef985-105">Puede usar la API administrada de EWS o realiza EWS para trabajar con lotes de mensajes de correo electrónico para reducir el número de llamadas de un cliente a un servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="ef985-105">You can use the EWS Managed API or EWS to work with batches of email messages to reduce the number of calls a client makes to an Exchange server.</span></span> <span data-ttu-id="ef985-106">Cuando se usa la API administrada de EWS para crear, obtener, actualizar, eliminar y enviar mensajes por lotes, use métodos del objeto [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) , mientras que cuando se trabaja con los mensajes de correo electrónico única, use métodos del objeto [EmailMessage](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="ef985-106">When you use the EWS Managed API to create, get, update, delete, and send messages in batches, you use [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object methods, whereas when you work with single email messages, you use [EmailMessage](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx) object methods.</span></span> <span data-ttu-id="ef985-107">Si usa EWS, use las mismas operaciones para trabajar con un solo y lotes de mensajes de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="ef985-107">If you are using EWS, you use the same operations to work with both single and batches of email messages.</span></span> 
  
<span data-ttu-id="ef985-108">**La tabla 1. Métodos de la API administrada de EWS y las operaciones de EWS para trabajar con lotes de mensajes de correo electrónico**</span><span class="sxs-lookup"><span data-stu-id="ef985-108">**Table 1. EWS Managed API methods and EWS operations for working with batches of email messages**</span></span>

|<span data-ttu-id="ef985-109">**Con el fin...**</span><span class="sxs-lookup"><span data-stu-id="ef985-109">**In order to…**</span></span>|<span data-ttu-id="ef985-110">**Use este método de la API administrada de EWS**</span><span class="sxs-lookup"><span data-stu-id="ef985-110">**Use this EWS Managed API method**</span></span>|<span data-ttu-id="ef985-111">**Use esta operación de EWS**</span><span class="sxs-lookup"><span data-stu-id="ef985-111">**Use this EWS operation**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ef985-112">Crear mensajes de correo electrónico por lotes</span><span class="sxs-lookup"><span data-stu-id="ef985-112">Create email messages in batches</span></span>  <br/> |[<span data-ttu-id="ef985-113">ExchangeService.CreateItems</span><span class="sxs-lookup"><span data-stu-id="ef985-113">ExchangeService.CreateItems</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.createitems%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="ef985-114">CreateItem</span><span class="sxs-lookup"><span data-stu-id="ef985-114">CreateItem</span></span>](http://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="ef985-115">Obtener mensajes de correo electrónico por lotes</span><span class="sxs-lookup"><span data-stu-id="ef985-115">Get email messages in batches</span></span>  <br/> |[<span data-ttu-id="ef985-116">ExchangeService.BindToItems</span><span class="sxs-lookup"><span data-stu-id="ef985-116">ExchangeService.BindToItems</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.bindtoitems%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="ef985-117">GetItem</span><span class="sxs-lookup"><span data-stu-id="ef985-117">GetItem</span></span>](http://msdn.microsoft.com/library/e8492e3b-1c8d-4b14-8070-9530f8306edd%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="ef985-118">Mensajes de correo electrónico de actualización por lotes</span><span class="sxs-lookup"><span data-stu-id="ef985-118">Update email messages in batches</span></span>  <br/> |[<span data-ttu-id="ef985-119">ExchangeService.UpdateItems</span><span class="sxs-lookup"><span data-stu-id="ef985-119">ExchangeService.UpdateItems</span></span>](http://msdn.microsoft.com/en-us/library/dd634705%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="ef985-120">UpdateItem</span><span class="sxs-lookup"><span data-stu-id="ef985-120">UpdateItem</span></span>](http://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="ef985-121">Eliminar mensajes de correo electrónico por lotes</span><span class="sxs-lookup"><span data-stu-id="ef985-121">Delete email messages in batches</span></span>  <br/> |[<span data-ttu-id="ef985-122">ExchangeService.DeleteItems</span><span class="sxs-lookup"><span data-stu-id="ef985-122">ExchangeService.DeleteItems</span></span>](http://msdn.microsoft.com/en-us/library/dd635460%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="ef985-123">DeleteItem</span><span class="sxs-lookup"><span data-stu-id="ef985-123">DeleteItem</span></span>](../web-service-reference/deleteitem-operation.md) <br/> |
   
<span data-ttu-id="ef985-124">En este artículo, aprenderá cómo completar tareas básicas de lotes de mensajes de correo electrónico mediante el uso de la API administrada de EWS o EWS.</span><span class="sxs-lookup"><span data-stu-id="ef985-124">In this article, you'll learn how to complete basic tasks for batches of email messages by using the EWS Managed API or EWS.</span></span>
  
## <a name="create-email-messages-in-batches-by-using-the-ews-managed-api"></a><span data-ttu-id="ef985-125">Crear mensajes de correo electrónico en lotes mediante el uso de la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="ef985-125">Create email messages in batches by using the EWS Managed API</span></span>
<span data-ttu-id="ef985-126"><a name="bk_createewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="ef985-126"></span></span>

<span data-ttu-id="ef985-127">Puede crear mensajes por lotes con el método de la API administrada de EWS **CreateItems** , tal como se muestra en el siguiente ejemplo.</span><span class="sxs-lookup"><span data-stu-id="ef985-127">You can create messages in batches by using the EWS Managed API **CreateItems** method, as shown in the following example.</span></span> <span data-ttu-id="ef985-128">En este ejemplo se crean tres objetos [EmailMessage](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx) localmente, agrega cada mensaje a una colección, a continuación, se llama al método **CreateItems** en la colección de mensajes.</span><span class="sxs-lookup"><span data-stu-id="ef985-128">This example creates three [EmailMessage](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx) objects locally, adds each message to a collection, then calls the **CreateItems** method on the collection of messages.</span></span> 
  
<span data-ttu-id="ef985-129">En este ejemplo se da por supuesto que **servicio** es un objeto [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) válido y que se ha autenticado el usuario a un servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="ef985-129">This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and that the user has been authenticated to an Exchange server.</span></span> 
  
```cs
public static Collection<ItemId> CreateDraftEmailInBatch(ExchangeService service)
{
    // These are unsaved local instances of an EmailMessage object.
    // Despite the required parameter of an ExchangeService object (service), no call
    // to an Exchange server is made when the objects are instantiated.
    // A call to the Exchange server is made when the service.CreateItems() method is called.
    EmailMessage message1 = new EmailMessage(service);
    EmailMessage message2 = new EmailMessage(service);
    EmailMessage message3 = new EmailMessage(service);
    // Set the properties on the first message.
    message1.Subject = "Project priorities";
    message1.Body = "(1) Buy pizza, (2) Eat pizza";
    message1.ToRecipients.Add("sadie@contoso.com");
    // Set the properties on the second message.
    message2.Subject = "Company Soccer Team";
    message2.Body = "Are you interested in joining?";
    message2.ToRecipients.Add("magdalena@contoso.com");
    // Set the properties on the third message.
    message3.Subject = "Code Blast";
    message3.Body = "Are you interested in getting together to finish the methods for the ContosoLive project?";
    message3.ToRecipients.Add("mack@contoso.com");
    // Add the EmailMessage objects to a collection.
    Collection<EmailMessage> messageItems = new Collection<EmailMessage>() { message1, message2, message3 };
    // Create the batch of email messages on the server.
    // This method call results in an CreateItem call to EWS.
    ServiceResponseCollection<ServiceResponse> response = service.CreateItems(messageItems, WellKnownFolderName.Drafts, MessageDisposition.SaveOnly, null);
    // Instantiate a collection of item IDs to populate from the values that are returned by the Exchange server.
    Collection<ItemId> itemIds = new Collection<ItemId>();
    // Collect the item IDs from the created email messages.
    foreach (EmailMessage message in messageItems)
    {
        try
        {
            itemIds.Add(message.Id);
            Console.WriteLine("Email message '{0}' created successfully.", message.Subject);
        }
        catch (Exception ex)
        {
            // Print out the exception and the last eight characters of the item ID.
            Console.WriteLine("Exception while creating message {0}: {1}", message.Id.ToString().Substring(144), ex.Message);
        }
    }
    // Check for success of the CreateItems method call.
    if (response.OverallResult == ServiceResult.Success)
    {
            Console.WriteLine("All locally created messages were successfully saved to the Drafts folder.");
            Console.WriteLine("\r\n");
    }
   
    // If the method did not return success, print the result message for each email.
    else
    {
        int counter = 1;
        foreach (ServiceResponse resp in response)
        {
            // Print out the result and the last eight characters of the item ID.
            Console.WriteLine("Result (message {0}), id {1}: {2}", counter, itemIds[counter - 1].ToString().Substring(144), resp.Result);
            Console.WriteLine("Error Code: {0}", resp.ErrorCode);
            Console.WriteLine("ErrorMessage: {0}\r\n", resp.ErrorMessage);
            Console.WriteLine("\r\n");
            counter++;
        }
    }
    return itemIds;
}
```

<span data-ttu-id="ef985-130">Tenga en cuenta que en el ejemplo se guarda sólo los mensajes en la carpeta Borradores; no envía los mensajes.</span><span class="sxs-lookup"><span data-stu-id="ef985-130">Note that the example only saves the messages in the Drafts folder; it does not send the messages.</span></span> <span data-ttu-id="ef985-131">Para obtener más información acerca de cómo enviar los mensajes, vea [enviar mensajes de correo electrónico en lotes mediante el uso de la API administrada de EWS](#bk_sendewsma).</span><span class="sxs-lookup"><span data-stu-id="ef985-131">For more about how to send the messages, see [Send email messages in batches by using the EWS Managed API](#bk_sendewsma).</span></span>
  
## <a name="create-email-messages-in-batches-by-using-ews"></a><span data-ttu-id="ef985-132">Crear mensajes de correo electrónico en lotes mediante EWS</span><span class="sxs-lookup"><span data-stu-id="ef985-132">Create email messages in batches by using EWS</span></span>
<span data-ttu-id="ef985-133"><a name="bk_createews"> </a></span><span class="sxs-lookup"><span data-stu-id="ef985-133"></span></span>

<span data-ttu-id="ef985-134">Puede crear mensajes de correo electrónico en lotes mediante la operación [CreateItem](http://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) EWS, tal como se muestra en el siguiente ejemplo de código.</span><span class="sxs-lookup"><span data-stu-id="ef985-134">You can create email messages in batches by using the [CreateItem](http://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) EWS operation, as shown in the following code example.</span></span> <span data-ttu-id="ef985-135">También es la solicitud XML que la API administrada de EWS envía al usar la API administrada de EWS para [crear mensajes de correo electrónico en lotes](#bk_createewsma).</span><span class="sxs-lookup"><span data-stu-id="ef985-135">This is also the XML request that the EWS Managed API sends when you use the EWS Managed API to [create email messages in batches](#bk_createewsma).</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
  </soap:Header>
  <soap:Body>
    <m:CreateItem MessageDisposition="SaveOnly">
      <m:SavedItemFolderId>
        <t:DistinguishedFolderId Id="drafts" />
      </m:SavedItemFolderId>
      <m:Items>
        <t:Message>
          <t:Subject>Project priorities</t:Subject>
          <t:Body BodyType="HTML">(1) Buy pizza, (2) Eat pizza</t:Body>
          <t:ToRecipients>
            <t:Mailbox>
              <t:EmailAddress>sadie@contoso.com</t:EmailAddress>
            </t:Mailbox>
          </t:ToRecipients>
        </t:Message>
        <t:Message>
          <t:Subject>Company Soccer Team</t:Subject>
          <t:Body BodyType="HTML">Are you interested in joining?</t:Body>
          <t:ToRecipients>
            <t:Mailbox>
              <t:EmailAddress>magdalena@contoso.com</t:EmailAddress>
            </t:Mailbox>
          </t:ToRecipients>
        </t:Message>
        <t:Message>
          <t:Subject>Code Blast</t:Subject>
          <t:Body BodyType="HTML">Are you interested in getting together to finish the methods for the ContosoLive project?</t:Body>
          <t:ToRecipients>
            <t:Mailbox>
              <t:EmailAddress>mack@contoso.com</t:EmailAddress>
            </t:Mailbox>
          </t:ToRecipients>
        </t:Message>
      </m:Items>
    </m:CreateItem>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="ef985-136">El servidor responde a la solicitud **CreateItem** con un mensaje de [CreateItemResponse](http://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) que incluye un valor [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) de **NoError** para cada uno de los mensajes nuevos, lo que indica que cada correo electrónico se ha creado y guardado correctamente .</span><span class="sxs-lookup"><span data-stu-id="ef985-136">The server responds to the **CreateItem** request with a [CreateItemResponse](http://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) value of **NoError** for each of the new messages, which indicates that each email was created and saved successfully.</span></span> 
  
<span data-ttu-id="ef985-137">Tenga en cuenta que en el ejemplo se guarda sólo los mensajes en la carpeta Borradores; no envía los mensajes.</span><span class="sxs-lookup"><span data-stu-id="ef985-137">Note that the example only saves the messages in the Drafts folder; it does not send the messages.</span></span> <span data-ttu-id="ef985-138">Para obtener más información acerca de cómo enviar los mensajes, vea [enviar mensajes de correo electrónico en lotes mediante el uso de EWS](#bk_sendews).</span><span class="sxs-lookup"><span data-stu-id="ef985-138">For more about how to send the messages, see [Send email messages in batches by using EWS](#bk_sendews).</span></span>
  
## <a name="send-email-messages-in-batches-by-using-the-ews-managed-api"></a><span data-ttu-id="ef985-139">Enviar mensajes de correo electrónico en lotes mediante el uso de la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="ef985-139">Send email messages in batches by using the EWS Managed API</span></span>
<span data-ttu-id="ef985-140"><a name="bk_sendewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="ef985-140"></span></span>

<span data-ttu-id="ef985-141">Usar el mismo código para enviar mensajes de correo electrónico en lotes que usar para crear mensajes de correo electrónico en lotes, excepto en que algunos de los parámetros del método [CreateItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.createitems%28v=exchg.80%29.aspx) cambiar.</span><span class="sxs-lookup"><span data-stu-id="ef985-141">You use the same code to send email messages in batches that you use to create email messages in batches, except that a few of the [CreateItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.createitems%28v=exchg.80%29.aspx) method parameters change.</span></span> <span data-ttu-id="ef985-142">Por lo tanto, para enviar mensajes de correo electrónico mediante el uso de la API administrada de EWS, use el código que se utiliza para [crear mensajes de correo electrónico en lotes](#bk_createewsma)y reemplace la llamada al método **CreateItems** con la llamada en el siguiente ejemplo.</span><span class="sxs-lookup"><span data-stu-id="ef985-142">So, to send email messages by using the EWS Managed API, use the code you use to [create email messages in batches](#bk_createewsma), and replace the call to the **CreateItems** method with the call in the following example.</span></span> <span data-ttu-id="ef985-143">En este ejemplo, los mensajes se crean en la carpeta Elementos enviados y la disposición de mensaje se cambia a [MessageDisposition.SendAndSaveCopy](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.messagedisposition%28v=exchg.80%29.aspx), por lo que se envía el mensaje y no sólo guardado localmente.</span><span class="sxs-lookup"><span data-stu-id="ef985-143">In this example, the messages are created in the Sent Items folder, and the message disposition is changed to [MessageDisposition.SendAndSaveCopy](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.messagedisposition%28v=exchg.80%29.aspx), so that the message is sent, and not just saved locally.</span></span>
  
```cs
// Create and send the batch of email messages on the server.
// This method call results in an CreateItem call to EWS.
ServiceResponseCollection<ServiceResponse> response = service.CreateItems(messageItems, WellKnownFolderName.SentItems, MessageDisposition.SendAndSaveCopy, null);
```

## <a name="send-email-messages-in-batches-by-using-ews"></a><span data-ttu-id="ef985-144">Enviar mensajes de correo electrónico en lotes mediante el uso de EWS</span><span class="sxs-lookup"><span data-stu-id="ef985-144">Send email messages in batches by using EWS</span></span>
<span data-ttu-id="ef985-145"><a name="bk_sendews"> </a></span><span class="sxs-lookup"><span data-stu-id="ef985-145"></span></span>

<span data-ttu-id="ef985-146">Usar el mismo código para enviar mensajes de correo electrónico en lotes que usar para crear mensajes de correo electrónico en lotes, excepto en que algunos de los valores de atributo cambiar para la operación **CreateItem** .</span><span class="sxs-lookup"><span data-stu-id="ef985-146">You use the same code to send email messages in batches that you use to create email messages in batches, except that a few of the attribute values change for the **CreateItem** operation.</span></span> <span data-ttu-id="ef985-147">Por lo tanto, para enviar mensajes de correo electrónico mediante el uso de EWS, use el código que use para [crear el mensaje de correo electrónico en lotes](#bk_createews)y cambie el valor de **MessageDisposition** a "SendAndSaveCopy" y cambie el [DistinguishedFolderId](http://msdn.microsoft.com/library/50018162-2941-4227-8a5b-d6b4686bb32f%28Office.15%29.aspx) a "elementos enviados", como se muestra en el ejemplo de código siguiente.</span><span class="sxs-lookup"><span data-stu-id="ef985-147">So, to send email messages by using EWS, use the code you use to [create email message in batches](#bk_createews), and change the **MessageDisposition** value to "SendAndSaveCopy", and change the [DistinguishedFolderId](http://msdn.microsoft.com/library/50018162-2941-4227-8a5b-d6b4686bb32f%28Office.15%29.aspx) to "sentitems", as shown in the following code example.</span></span> 
  
```XML
<m:CreateItem MessageDisposition="SendAndSaveCopy">
  <m:SavedItemFolderId>
    <t:DistinguishedFolderId Id="sentitems" />
  </m:SavedItemFolderId>
```

<span data-ttu-id="ef985-148">El servidor responde a la solicitud **CreateItem** con un mensaje de [CreateItemResponse](http://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) que incluye un valor [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) de **NoError** para cada uno de los mensajes nuevos, lo que indica que se ha creado y se ha enviado correctamente cada correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="ef985-148">The server responds to the **CreateItem** request with a [CreateItemResponse](http://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) value of **NoError** for each of the new messages, which indicates that each email was created and sent successfully.</span></span> 
  
## <a name="get-email-messages-in-batches-by-using-the-ews-managed-api"></a><span data-ttu-id="ef985-149">Obtener mensajes de correo electrónico en lotes mediante el uso de la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="ef985-149">Get email messages in batches by using the EWS Managed API</span></span>
<span data-ttu-id="ef985-150"><a name="bk_getewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="ef985-150"></span></span>

<span data-ttu-id="ef985-151">Para obtener los mensajes de correo electrónico en lotes mediante el método de la API administrada de EWS [BindToItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.bindtoitems%28v=exchg.80%29.aspx) , tal como se muestra en el siguiente ejemplo.</span><span class="sxs-lookup"><span data-stu-id="ef985-151">You can get email messages in batches by using the EWS Managed API [BindToItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.bindtoitems%28v=exchg.80%29.aspx) method, as shown in the following example.</span></span> 
  
<span data-ttu-id="ef985-152">En este ejemplo se da por supuesto que **servicio** es un objeto [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) válido y que se ha autenticado el usuario a un servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="ef985-152">This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and that the user has been authenticated to an Exchange server.</span></span> 
  
```cs
public static Collection<EmailMessage> BatchGetEmailItems(ExchangeService service, Collection<ItemId> itemIds)
{
    // Create a property set that limits the properties returned by the Bind method to only those that are required.
    PropertySet propSet = new PropertySet(BasePropertySet.IdOnly, EmailMessageSchema.Subject, EmailMessageSchema.ToRecipients);
    // Get the items from the server.
    // This method call results in a GetItem call to EWS.
    ServiceResponseCollection<GetItemResponse> response = service.BindToItems(itemIds, propSet);
           
    // Instantiate a collection of EmailMessage objects to populate from the values that are returned by the Exchange server.
    Collection<EmailMessage> messageItems = new Collection<EmailMessage>();
    foreach (GetItemResponse getItemResponse in response)
    {
        try
        {
            Item item = getItemResponse.Item;
            EmailMessage message = (EmailMessage)item;
            messageItems.Add(message);
            // Print out confirmation and the last eight characters of the item ID.
            Console.WriteLine("Found item {0}.", message.Id.ToString().Substring(144));
        }
        catch (Exception ex)
        {
           Console.WriteLine("Exception while getting a message: {0}", ex.Message);
        }
    }
    // Check for success of the BindToItems method call.
    if (response.OverallResult == ServiceResult.Success)
    {
        Console.WriteLine("All email messages retrieved successfully.");
        Console.WriteLine("\r\n");
    }
        return messageItems;
}
```

## <a name="get-email-messages-in-batches-by-using-ews"></a><span data-ttu-id="ef985-153">Obtener mensajes de correo electrónico en lotes mediante el uso de EWS</span><span class="sxs-lookup"><span data-stu-id="ef985-153">Get email messages in batches by using EWS</span></span>
<span data-ttu-id="ef985-154"><a name="bk_getews"> </a></span><span class="sxs-lookup"><span data-stu-id="ef985-154"></span></span>

<span data-ttu-id="ef985-155">Puede obtener mensajes de correo electrónico en lotes mediante la operación de EWS [GetItem](http://msdn.microsoft.com/library/e8492e3b-1c8d-4b14-8070-9530f8306edd%28Office.15%29.aspx) y el código en el siguiente ejemplo.</span><span class="sxs-lookup"><span data-stu-id="ef985-155">You can get email messages in batches by using the [GetItem](http://msdn.microsoft.com/library/e8492e3b-1c8d-4b14-8070-9530f8306edd%28Office.15%29.aspx) EWS operation and the code in the following example.</span></span> <span data-ttu-id="ef985-156">También es la solicitud XML que la API administrada de EWS envía al usar la API administrada de EWS para [obtener los mensajes de correo electrónico en lotes](#bk_getewsma).</span><span class="sxs-lookup"><span data-stu-id="ef985-156">This is also the XML request that the EWS Managed API sends when you use the EWS Managed API to [get email messages in batches](#bk_getewsma).</span></span> 
  
<span data-ttu-id="ef985-157">Los atributos **ItemId** y **ChangeKey** se han abreviado para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="ef985-157">The **ItemId** and **ChangeKey** attributes have been shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
  </soap:Header>
  <soap:Body>
    <m:GetItem>
      <m:ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="item:Subject" />
          <t:FieldURI FieldURI="message:ToRecipients" />
        </t:AdditionalProperties>
      </m:ItemShape>
      <m:ItemIds>
        <t:ItemId Id="m4NxAAA="
                  ChangeKey="CQAAABYAAAApjGm7TnMWQ5TzjbhziLL0AAF/yKB0" />
        <t:ItemId Id="m4NyAAA="
                  ChangeKey="CQAAABYAAAApjGm7TnMWQ5TzjbhziLL0AAF/yKB1" />
        <t:ItemId Id="m4NzAAA="
                  ChangeKey="CQAAABYAAAApjGm7TnMWQ5TzjbhziLL0AAF/yKB2" />
      </m:ItemIds>
    </m:GetItem>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="ef985-158">El servidor responde a la solicitud de **GetItem** con un mensaje de [GetItemResponse](http://msdn.microsoft.com/library/8b66de1b-26a6-476c-9585-a96059125716%28Office.15%29.aspx) que incluye las [Propiedades de primera clase](email-properties-and-elements-in-ews-in-exchange.md) para cada uno de los mensajes solicitados.</span><span class="sxs-lookup"><span data-stu-id="ef985-158">The server responds to the **GetItem** request with a [GetItemResponse](http://msdn.microsoft.com/library/8b66de1b-26a6-476c-9585-a96059125716%28Office.15%29.aspx) message that includes the [first class properties](email-properties-and-elements-in-ews-in-exchange.md) for each of the requested messages.</span></span> 
  
## <a name="update-email-messages-in-batches-by-using-the-ews-managed-api"></a><span data-ttu-id="ef985-159">Mensajes de correo electrónico de actualización por lotes mediante el uso de la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="ef985-159">Update email messages in batches by using the EWS Managed API</span></span>
<span data-ttu-id="ef985-160"><a name="bk_updateewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="ef985-160"></span></span>

<span data-ttu-id="ef985-161">Para obtener los mensajes de correo electrónico en lotes mediante el método de la API administrada de EWS [UpdateItems](http://msdn.microsoft.com/en-us/library/dd634705%28v=exchg.80%29.aspx) , tal como se muestra en el siguiente ejemplo.</span><span class="sxs-lookup"><span data-stu-id="ef985-161">You can get email messages in batches by using the EWS Managed API [UpdateItems](http://msdn.microsoft.com/en-us/library/dd634705%28v=exchg.80%29.aspx) method, as shown in the following example.</span></span> 
  
<span data-ttu-id="ef985-162">Para obtener una lista de propiedades del mensaje de correo electrónico puede escribir, vea [de correo electrónico las propiedades y los elementos de EWS en Exchange](email-properties-and-elements-in-ews-in-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="ef985-162">For a list of writable email message properties, see [Email properties and elements in EWS in Exchange](email-properties-and-elements-in-ews-in-exchange.md).</span></span>
  
<span data-ttu-id="ef985-163">Para obtener información detallada acerca de cómo enviar un mensaje de borrador después de que se ha actualizado, consulte [envío de mensajes de correo electrónico mediante el uso de la API administrada de EWS](#bk_sendewsma).</span><span class="sxs-lookup"><span data-stu-id="ef985-163">For details about how to send a draft message after it's been updated, see [Sending email messages by using the EWS Managed API](#bk_sendewsma).</span></span>
  
<span data-ttu-id="ef985-164">En este ejemplo se da por supuesto que **servicio** es un objeto [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) válido y que se ha autenticado el usuario a un servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="ef985-164">This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and that the user has been authenticated to an Exchange server.</span></span> 
  
```cs
public static Collection<EmailMessage> BatchUpdateEmailItems(ExchangeService service, Collection<EmailMessage> messageItems)
{
    // Update the subject of each message locally.
    foreach (EmailMessage message in messageItems)
    {
        // Update the Subject of the email.
        message.Subject = "Updated subject at " + DateTime.Now;
        // Print out confirmation with the last eight characters of the item ID and the email subject.
        Console.WriteLine("Updated local email message {0} with the subject '{1}'.", message.Id.ToString().Substring(144), message.Subject);
    }
    // Send the item updates to the server.
    // This method call results in an UpdateItem call to EWS.
    ServiceResponseCollection<UpdateItemResponse> response = service.UpdateItems(messageItems, WellKnownFolderName.Drafts, ConflictResolutionMode.AutoResolve, MessageDisposition.SaveOnly, null);
    // Check for success of the UpdateItems method call.
    if (response.OverallResult == ServiceResult.Success)
    {
        Console.WriteLine("All email messages updated successfully.\r\n");
    }
    // If the method did not return success, print the result message for each email.
    else
    {
        Console.WriteLine("All emails were not successfully saved on the server.\r\n");
        int counter = 1;
        foreach (ServiceResponse resp in response)
        {
            Console.WriteLine("Result for (message {0}): {1}", counter, resp.Result);
            Console.WriteLine("Error Code: {0}", resp.ErrorCode);
            Console.WriteLine("ErrorMessage: {0}\r\n", resp.ErrorMessage);
            counter++;
        }
    }
    return messageItems;
}    
```

## <a name="update-email-messages-in-batches-by-using-ews"></a><span data-ttu-id="ef985-165">Mensajes de correo electrónico de actualización por lotes mediante el uso de EWS</span><span class="sxs-lookup"><span data-stu-id="ef985-165">Update email messages in batches by using EWS</span></span>
<span data-ttu-id="ef985-166"><a name="bk_updateews"> </a></span><span class="sxs-lookup"><span data-stu-id="ef985-166"></span></span>

<span data-ttu-id="ef985-167">Puede actualizar los mensajes de correo electrónico en lotes mediante la operación de EWS [GetItem](http://msdn.microsoft.com/library/e8492e3b-1c8d-4b14-8070-9530f8306edd%28Office.15%29.aspx) , tal como se muestra en el siguiente ejemplo de código.</span><span class="sxs-lookup"><span data-stu-id="ef985-167">You can update email messages in batches by using the [GetItem](http://msdn.microsoft.com/library/e8492e3b-1c8d-4b14-8070-9530f8306edd%28Office.15%29.aspx) EWS operation, as shown in following code example.</span></span> <span data-ttu-id="ef985-168">También es la solicitud XML que la API administrada de EWS envía al usar la API administrada de EWS para [actualizar los mensajes de correo electrónico en lotes](#bk_updateewsma).</span><span class="sxs-lookup"><span data-stu-id="ef985-168">This is also the XML request that the EWS Managed API sends when you use the EWS Managed API to [update email messages in batches](#bk_updateewsma).</span></span>
  
<span data-ttu-id="ef985-169">Para obtener una lista de elementos de mensaje de correo electrónico puede escribir, vea [de correo electrónico las propiedades y los elementos de EWS en Exchange](email-properties-and-elements-in-ews-in-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="ef985-169">For a list of writable email message elements, see [Email properties and elements in EWS in Exchange](email-properties-and-elements-in-ews-in-exchange.md).</span></span>
  
<span data-ttu-id="ef985-170">Para obtener información detallada acerca de cómo enviar un mensaje de borrador después de que se ha actualizado, vea [Enviar un borrador de mensaje de correo electrónico mediante el uso de EWS](how-to-send-email-messages-by-using-ews-in-exchange.md#bk_senddraftews).</span><span class="sxs-lookup"><span data-stu-id="ef985-170">For details about how to send a draft message after it's been updated, see [Send a draft email message by using EWS](how-to-send-email-messages-by-using-ews-in-exchange.md#bk_senddraftews).</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
  </soap:Header>
  <soap:Body>
    <m:UpdateItem MessageDisposition="SaveOnly"
                  ConflictResolution="AutoResolve">
      <m:SavedItemFolderId>
        <t:DistinguishedFolderId Id="drafts" />
      </m:SavedItemFolderId>
      <m:ItemChanges>
        <t:ItemChange>
          <t:ItemId Id="m4OVAAA="
                    ChangeKey="CQAAABYAAAApjGm7TnMWQ5TzjbhziLL0AAF/yKCy" />
          <t:Updates>
            <t:SetItemField>
              <t:FieldURI FieldURI="item:Subject" />
              <t:Message>
                <t:Subject>Updated subject at 1/17/2014 2:58:09 PM</t:Subject>
              </t:Message>
            </t:SetItemField>
          </t:Updates>
        </t:ItemChange>
        <t:ItemChange>
          <t:ItemId Id="m4OWAAA="
                    ChangeKey="CQAAABYAAAApjGm7TnMWQ5TzjbhziLL0AAF/yKCz" />
          <t:Updates>
            <t:SetItemField>
              <t:FieldURI FieldURI="item:Subject" />
              <t:Message>
                <t:Subject>Updated subject at 1/17/2014 2:58:09 PM</t:Subject>
              </t:Message>
            </t:SetItemField>
          </t:Updates>
        </t:ItemChange>
        <t:ItemChange>
          <t:ItemId Id="m4OXAAA="
                    ChangeKey="CQAAABYAAAApjGm7TnMWQ5TzjbhziLL0AAF/yKC0" />
          <t:Updates>
            <t:SetItemField>
              <t:FieldURI FieldURI="item:Subject" />
              <t:Message>
                <t:Subject>Updated subject at 1/17/2014 2:58:09 PM</t:Subject>
              </t:Message>
            </t:SetItemField>
          </t:Updates>
        </t:ItemChange>
      </m:ItemChanges>
    </m:UpdateItem>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="ef985-171">El servidor responde a la solicitud de **UpdateItem** con un mensaje de [UpdateItemResponse](http://msdn.microsoft.com/library/023b79b4-c675-4669-9112-d85499ec4fc4%28Office.15%29.aspx) que incluye un valor [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) de **NoError**, lo que indica que cada una de las actualizaciones se guardó correctamente en el servidor.</span><span class="sxs-lookup"><span data-stu-id="ef985-171">The server responds to the **UpdateItem** request with an [UpdateItemResponse](http://msdn.microsoft.com/library/023b79b4-c675-4669-9112-d85499ec4fc4%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) value of **NoError**, which indicates that each of the updates was saved successfully on the server.</span></span> <span data-ttu-id="ef985-172">Se informa de los conflictos en el elemento [ConflictResult](http://msdn.microsoft.com/library/08cdd547-4de7-4c7a-b60f-e618dc217d20%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="ef985-172">Any conflicts are reported in the [ConflictResult](http://msdn.microsoft.com/library/08cdd547-4de7-4c7a-b60f-e618dc217d20%28Office.15%29.aspx) element.</span></span> 
  
## <a name="delete-email-messages-in-batches-by-using-the-ews-managed-api"></a><span data-ttu-id="ef985-173">Eliminar mensajes de correo electrónico en lotes mediante la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="ef985-173">Delete email messages in batches by using the EWS Managed API</span></span>
<span data-ttu-id="ef985-174"><a name="bk_deleteewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="ef985-174"></span></span>

<span data-ttu-id="ef985-175">Puede eliminar mensajes por lotes con el método de la API administrada de EWS [DeleteItems](http://msdn.microsoft.com/en-us/library/dd635460%28v=exchg.80%29.aspx) , tal como se muestra en el siguiente ejemplo.</span><span class="sxs-lookup"><span data-stu-id="ef985-175">You can delete messages in batches by using the EWS Managed API [DeleteItems](http://msdn.microsoft.com/en-us/library/dd635460%28v=exchg.80%29.aspx) method, as shown in the following example.</span></span> 
  
<span data-ttu-id="ef985-176">En este ejemplo se da por supuesto que **servicio** es un objeto [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) válido y que se ha autenticado el usuario a un servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="ef985-176">This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and that the user has been authenticated to an Exchange server.</span></span> 
  
```cs
public static void BatchDeleteEmailItems(ExchangeService service, Collection<ItemId> itemIds)
{
    // Delete the batch of email message objects.
    // This method call results in an DeleteItem call to EWS.
    ServiceResponseCollection<ServiceResponse> response = service.DeleteItems(itemIds, DeleteMode.SoftDelete, null, AffectedTaskOccurrence.AllOccurrences);
    
    // Check for success of the DeleteItems method call.
    // DeleteItems returns success even if it does not find all the item IDs.
    if (response.OverallResult == ServiceResult.Success)
    {
        Console.WriteLine("Email messages deleted successfully.\r\n");
    }
    // If the method did not return success, print a message.
    else
    {
        Console.WriteLine("Not all email messages deleted successfully.\r\n");
    }
}
```

## <a name="delete-email-messages-in-batches-by-using-ews"></a><span data-ttu-id="ef985-177">Eliminar mensajes de correo electrónico en lotes mediante EWS</span><span class="sxs-lookup"><span data-stu-id="ef985-177">Delete email messages in batches by using EWS</span></span>
<span data-ttu-id="ef985-178"><a name="bk_deleteews"> </a></span><span class="sxs-lookup"><span data-stu-id="ef985-178"></span></span>

<span data-ttu-id="ef985-179">Puede eliminar mensajes de correo electrónico en lotes mediante la operación de EWS [DeleteItem](../web-service-reference/deleteitem-operation.md) , tal como se muestra en el siguiente ejemplo de código.</span><span class="sxs-lookup"><span data-stu-id="ef985-179">You can delete email messages in batches by using the [DeleteItem](../web-service-reference/deleteitem-operation.md) EWS operation, as shown in the following code example.</span></span> <span data-ttu-id="ef985-180">También es la solicitud XML que la API administrada de EWS envía al usar la API administrada de EWS para [Eliminar mensajes de correo electrónico en lotes](#bk_deleteewsma).</span><span class="sxs-lookup"><span data-stu-id="ef985-180">This is also the XML request that the EWS Managed API sends when you use the EWS Managed API to [delete email messages in batches](#bk_deleteewsma).</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
  </soap:Header>
  <soap:Body>
    <m:DeleteItem DeleteType="SoftDelete"
                  AffectedTaskOccurrences="AllOccurrences">
      <m:ItemIds>
        <t:ItemId Id="m4OkAAA="
                  ChangeKey="CQAAABYAAAApjGm7TnMWQ5TzjbhziLL0AAF/yKDE" />
        <t:ItemId Id="m4OlAAA="
                  ChangeKey="CQAAABYAAAApjGm7TnMWQ5TzjbhziLL0AAF/yKDF" />
        <t:ItemId Id="m4OmAAA="
                  ChangeKey="CQAAABYAAAApjGm7TnMWQ5TzjbhziLL0AAF/yKDG" />
      </m:ItemIds>
    </m:DeleteItem>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="ef985-181">El servidor responde a la solicitud de **DeleteItem** con un mensaje de [DeleteItemResponse](http://msdn.microsoft.com/library/86463d66-fe47-4a19-a81b-e24841e816ab%28Office.15%29.aspx) que incluye un valor [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) de **NoError** para cada elemento que se ha quitado.</span><span class="sxs-lookup"><span data-stu-id="ef985-181">The server responds to the **DeleteItem** request with a [DeleteItemResponse](http://msdn.microsoft.com/library/86463d66-fe47-4a19-a81b-e24841e816ab%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) value of **NoError** for each item that was removed.</span></span> <span data-ttu-id="ef985-182">Tenga en cuenta que la operación también devuelve success si no se pudo encontrar el identificador de elemento.</span><span class="sxs-lookup"><span data-stu-id="ef985-182">Note that the operation also returns success if the item ID could not be found.</span></span> 
  
## <a name="verifying-that-a-batch-process-completed-successfully"></a><span data-ttu-id="ef985-183">Comprobar que un proceso por lotes se completó correctamente</span><span class="sxs-lookup"><span data-stu-id="ef985-183">Verifying that a batch process completed successfully</span></span>
<span data-ttu-id="ef985-184"><a name="bk_successful"> </a></span><span class="sxs-lookup"><span data-stu-id="ef985-184"></span></span>

<span data-ttu-id="ef985-185">Cuando no se puede procesar uno o más mensajes de correo electrónico en una solicitud por lotes como se ha solicitado, se devuelve un error de cada mensaje de correo electrónico que no se pudo, y el resto de los mensajes de correo electrónico en el lote se procesan según lo previsto.</span><span class="sxs-lookup"><span data-stu-id="ef985-185">When one or more email messages in a batched request can't be processed as requested, an error is returned for each email message that failed, and the rest of the emails in the batch are processed as expected.</span></span> <span data-ttu-id="ef985-186">Pueden producirse errores en el procesamiento por lotes si el elemento se ha eliminado y por lo tanto, no se envía, recuperar o actualizado, o si el elemento movido a una carpeta diferente y por lo tanto, tiene un nuevo identificador de elemento y no se puede modificar con el identificador de elemento que se envía.</span><span class="sxs-lookup"><span data-stu-id="ef985-186">Failures in batch processing can occur if the item was deleted, and therefore can't be sent, retrieved, or updated, or if the item moved to a different folder, and therefore has a new item ID, and cannot be modified with the item ID sent.</span></span> <span data-ttu-id="ef985-187">La información de esta sección muestra cómo obtener los detalles del error acerca de los errores de procesamiento por lotes de mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="ef985-187">The information in this section shows how to get error details about failures in batch processing of email message.</span></span>
  
<span data-ttu-id="ef985-188">Para comprobar el éxito de un proceso por lotes mediante el uso de la API administrada de EWS, puede comprobar que la propiedad [OverallResult](http://msdn.microsoft.com/en-us/library/dd634515%28v=exchg.80%29.aspx) de la [ServiceResponseCollection](http://msdn.microsoft.com/en-us/library/dd633715%28v=exchg.80%29.aspx) es igual a [ServiceResult.Success](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceresult%28v=exchg.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="ef985-188">To verify the success of a batch process by using the EWS Managed API, you can check that the [OverallResult](http://msdn.microsoft.com/en-us/library/dd634515%28v=exchg.80%29.aspx) property of the [ServiceResponseCollection](http://msdn.microsoft.com/en-us/library/dd633715%28v=exchg.80%29.aspx) is equal to [ServiceResult.Success](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceresult%28v=exchg.80%29.aspx).</span></span> <span data-ttu-id="ef985-189">Si es así, todos los correos electrónicos se procesan correctamente.</span><span class="sxs-lookup"><span data-stu-id="ef985-189">If so, all the emails were processed successfully.</span></span> <span data-ttu-id="ef985-190">Si el **OverallResult** no es igual a **ServiceResult.Success**, uno o varios de los mensajes de correo electrónico no se procesó correctamente.</span><span class="sxs-lookup"><span data-stu-id="ef985-190">If the **OverallResult** is not equal to **ServiceResult.Success**, one or more of the emails were not processed successfully.</span></span> <span data-ttu-id="ef985-191">Cada uno de los objetos devueltos en la **ServiceResponseCollection** contiene las siguientes propiedades:</span><span class="sxs-lookup"><span data-stu-id="ef985-191">Each of the objects returned in the **ServiceResponseCollection** contains the following properties:</span></span> 
  
- [<span data-ttu-id="ef985-192">ErrorCode</span><span class="sxs-lookup"><span data-stu-id="ef985-192">ErrorCode</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceresponse.errorcode%28v=exchg.80%29.aspx)
    
- [<span data-ttu-id="ef985-193">ErrorDetails</span><span class="sxs-lookup"><span data-stu-id="ef985-193">ErrorDetails</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceresponse.errordetails%28v=exchg.80%29.aspx)
    
- [<span data-ttu-id="ef985-194">ErrorMessage</span><span class="sxs-lookup"><span data-stu-id="ef985-194">ErrorMessage</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceresponse.errormessage%28v=exchg.80%29.aspx)
    
- [<span data-ttu-id="ef985-195">ErrorProperties</span><span class="sxs-lookup"><span data-stu-id="ef985-195">ErrorProperties</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceresponse.errorproperties%28v=exchg.80%29.aspx)
    
- [<span data-ttu-id="ef985-196">Resultado</span><span class="sxs-lookup"><span data-stu-id="ef985-196">Result</span></span>](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.serviceresponse.result%28v=exchg.80%29.aspx)
    
<span data-ttu-id="ef985-197">Estas propiedades contienen información acerca de por qué los mensajes de correo electrónico no se podrían procesar como se solicitó.</span><span class="sxs-lookup"><span data-stu-id="ef985-197">These properties contain information about why the email messages could not be processed as requested.</span></span> <span data-ttu-id="ef985-198">Los ejemplos de este artículo imprimen los **resultados**, **ErrorCode**y **ErrorMessage** para cada mensaje de error.</span><span class="sxs-lookup"><span data-stu-id="ef985-198">The examples in this article print out the **Result**, **ErrorCode**, and **ErrorMessage** for each failed message.</span></span> <span data-ttu-id="ef985-199">Puede utilizar estos resultados para investigar el problema.</span><span class="sxs-lookup"><span data-stu-id="ef985-199">You can use these results to investigate the issue.</span></span> 
  
<span data-ttu-id="ef985-200">Para EWS, para comprobar el éxito de un proceso por lotes, consulte el atributo [ResponseClass](http://msdn.microsoft.com/library/bf57265a-d354-4cd7-bbfc-d93e19cbede6%28Office.15%29.aspx) para cada elemento que se está procesando.</span><span class="sxs-lookup"><span data-stu-id="ef985-200">For EWS, to verify the success of a batched process, check the [ResponseClass](http://msdn.microsoft.com/library/bf57265a-d354-4cd7-bbfc-d93e19cbede6%28Office.15%29.aspx) attribute for each item being processed.</span></span> <span data-ttu-id="ef985-201">La siguiente es la estructura básica de la **ResponseMessageType**, el tipo base de qué respuesta todos los mensajes se derivan.</span><span class="sxs-lookup"><span data-stu-id="ef985-201">The following is the basic structure of the **ResponseMessageType**, the base type from which all response messages are derived.</span></span> 
  
```XML
<ResponseMessage ResponseClass="Success | Warning | Error">
            <MessageText/>
            <ResponseCode/>
            <DescriptiveLinkKey/>
            <MessageXml/>
</ResponseMessage>
```

<span data-ttu-id="ef985-202">El atributo **ResponseClass** se establece en **correcto** si el correo electrónico se procesó correctamente, o el **Error** si el correo electrónico no se procesó correctamente.</span><span class="sxs-lookup"><span data-stu-id="ef985-202">The **ResponseClass** attribute is set to **Success** if the email was processed successfully, or **Error** if the email was not processed successfully.</span></span> <span data-ttu-id="ef985-203">Para los mensajes de correo electrónico, no se producirá una **Advertencia** durante el procesamiento por lotes.</span><span class="sxs-lookup"><span data-stu-id="ef985-203">For email messages, you will not encounter a **Warning** during batch processing.</span></span> <span data-ttu-id="ef985-204">Si la **ResponseClass** es **correcto**, el elemento [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) que sigue también siempre se establece en **NoError**.</span><span class="sxs-lookup"><span data-stu-id="ef985-204">If the **ResponseClass** is **Success**, the [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) element that follows is also always set to **NoError**.</span></span> <span data-ttu-id="ef985-205">Si la **ResponseClass** es **Error**, debe comprobar los valores de los elementos [MessageText](http://msdn.microsoft.com/library/59a23bdc-0d9a-4942-8b3c-9cdb11db1ab1%28Office.15%29.aspx), **ResponseCode**y [MessageXml](http://msdn.microsoft.com/library/bcaf9e35-d351-48f3-baad-f90c633cba8a%28Office.15%29.aspx) para determinar la causa del problema.</span><span class="sxs-lookup"><span data-stu-id="ef985-205">If the **ResponseClass** is **Error**, you need to check the values of the [MessageText](http://msdn.microsoft.com/library/59a23bdc-0d9a-4942-8b3c-9cdb11db1ab1%28Office.15%29.aspx), **ResponseCode**, and [MessageXml](http://msdn.microsoft.com/library/bcaf9e35-d351-48f3-baad-f90c633cba8a%28Office.15%29.aspx) elements to determine what caused the problem.</span></span> <span data-ttu-id="ef985-206">[DescriptiveLinkKey](http://msdn.microsoft.com/library/f7f36749-00f3-4915-b17c-e3caa0af6e67%28Office.15%29.aspx) se utiliza actualmente.</span><span class="sxs-lookup"><span data-stu-id="ef985-206">[DescriptiveLinkKey](http://msdn.microsoft.com/library/f7f36749-00f3-4915-b17c-e3caa0af6e67%28Office.15%29.aspx) is currently unused.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ef985-207">Vea también</span><span class="sxs-lookup"><span data-stu-id="ef985-207">See also</span></span>


- [<span data-ttu-id="ef985-208">Correo electrónico y EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="ef985-208">Email and EWS in Exchange</span></span>](email-and-ews-in-exchange.md)
    
- [<span data-ttu-id="ef985-209">Enviar mensajes de correo electrónico mediante el uso de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="ef985-209">Send email messages by using EWS in Exchange</span></span>](how-to-send-email-messages-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="ef985-210">Responder a mensajes de correo electrónico mediante el uso de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="ef985-210">Respond to email messages by using EWS in Exchange</span></span>](how-to-respond-to-email-messages-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="ef985-211">Mover y copiar los mensajes de correo electrónico mediante el uso de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="ef985-211">Move and copy email messages by using EWS in Exchange</span></span>](how-to-move-and-copy-email-messages-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="ef985-212">Limitación de implicaciones para las solicitudes de lote EWS</span><span class="sxs-lookup"><span data-stu-id="ef985-212">Throttling implications for EWS batch requests</span></span>](ews-throttling-in-exchange.md#bk_ThrottlingBatch)
    

