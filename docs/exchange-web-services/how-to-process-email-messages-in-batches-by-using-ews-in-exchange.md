---
title: Procesar mensajes de correo electrónico en lotes mediante EWS en Exchange
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.assetid: 96390f92-cab1-4de6-9ec2-a55678fc20af
description: Obtenga información sobre cómo crear, obtener, actualizar y eliminar lotes de mensajes de correo electrónico en una sola llamada usando la API administrada de EWS o EWS en Exchange.
localization_priority: Priority
ms.openlocfilehash: 2592076c9c5b57356d96872f006dd7b0abfc328a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44527778"
---
# <a name="process-email-messages-in-batches-by-using-ews-in-exchange"></a><span data-ttu-id="651bd-103">Procesar mensajes de correo electrónico en lotes mediante EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="651bd-103">Process email messages in batches by using EWS in Exchange</span></span>

<span data-ttu-id="651bd-104">Obtenga información sobre cómo crear, obtener, actualizar y eliminar lotes de mensajes de correo electrónico en una sola llamada usando la API administrada de EWS o EWS en Exchange.</span><span class="sxs-lookup"><span data-stu-id="651bd-104">Learn how to create, get, update, and delete batches of email messages in a single call by using the EWS Managed API or EWS in Exchange.</span></span>

<span data-ttu-id="651bd-105">Puede usar la API administrada de EWS o EWS para trabajar con lotes de mensajes de correo electrónico para reducir el número de llamadas que un cliente realiza a un servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="651bd-105">You can use the EWS Managed API or EWS to work with batches of email messages to reduce the number of calls a client makes to an Exchange server.</span></span> <span data-ttu-id="651bd-106">Cuando se usa la API administrada de EWS para crear, obtener, actualizar, eliminar y enviar mensajes por lotes, se usan los métodos del objeto [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) , mientras que cuando se trabaja con mensajes de correo electrónico individuales, se usan los métodos del objeto [EmailMessage](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="651bd-106">When you use the EWS Managed API to create, get, update, delete, and send messages in batches, you use [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object methods, whereas when you work with single email messages, you use [EmailMessage](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx) object methods.</span></span> <span data-ttu-id="651bd-107">Si usa EWS, use las mismas operaciones para trabajar con los mensajes de correo electrónico individuales y de lotes.</span><span class="sxs-lookup"><span data-stu-id="651bd-107">If you are using EWS, you use the same operations to work with both single and batches of email messages.</span></span>

<span data-ttu-id="651bd-108">**Tabla 1. Métodos de API administrada de EWS y operaciones EWS para trabajar con lotes de mensajes de correo electrónico**</span><span class="sxs-lookup"><span data-stu-id="651bd-108">**Table 1. EWS Managed API methods and EWS operations for working with batches of email messages**</span></span>

|<span data-ttu-id="651bd-109">**Para**</span><span class="sxs-lookup"><span data-stu-id="651bd-109">**In order to…**</span></span>|<span data-ttu-id="651bd-110">**Usar este método de API administrada de EWS**</span><span class="sxs-lookup"><span data-stu-id="651bd-110">**Use this EWS Managed API method**</span></span>|<span data-ttu-id="651bd-111">**Usar esta operación de EWS**</span><span class="sxs-lookup"><span data-stu-id="651bd-111">**Use this EWS operation**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="651bd-112">Crear mensajes de correo electrónico por lotes</span><span class="sxs-lookup"><span data-stu-id="651bd-112">Create email messages in batches</span></span>  <br/> |[<span data-ttu-id="651bd-113">ExchangeService. CreateItems</span><span class="sxs-lookup"><span data-stu-id="651bd-113">ExchangeService.CreateItems</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.createitems%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="651bd-114">CreateItem</span><span class="sxs-lookup"><span data-stu-id="651bd-114">CreateItem</span></span>](https://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="651bd-115">Obtener mensajes de correo electrónico por lotes</span><span class="sxs-lookup"><span data-stu-id="651bd-115">Get email messages in batches</span></span>  <br/> |[<span data-ttu-id="651bd-116">ExchangeService. BindToItems</span><span class="sxs-lookup"><span data-stu-id="651bd-116">ExchangeService.BindToItems</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.bindtoitems%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="651bd-117">GetItem</span><span class="sxs-lookup"><span data-stu-id="651bd-117">GetItem</span></span>](https://msdn.microsoft.com/library/e8492e3b-1c8d-4b14-8070-9530f8306edd%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="651bd-118">Actualizar mensajes de correo electrónico por lotes</span><span class="sxs-lookup"><span data-stu-id="651bd-118">Update email messages in batches</span></span>  <br/> |[<span data-ttu-id="651bd-119">ExchangeService. UpdateItems</span><span class="sxs-lookup"><span data-stu-id="651bd-119">ExchangeService.UpdateItems</span></span>](https://msdn.microsoft.com/library/dd634705%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="651bd-120">UpdateItem</span><span class="sxs-lookup"><span data-stu-id="651bd-120">UpdateItem</span></span>](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="651bd-121">Eliminar mensajes de correo electrónico por lotes</span><span class="sxs-lookup"><span data-stu-id="651bd-121">Delete email messages in batches</span></span>  <br/> |[<span data-ttu-id="651bd-122">ExchangeService. DeleteItems</span><span class="sxs-lookup"><span data-stu-id="651bd-122">ExchangeService.DeleteItems</span></span>](https://msdn.microsoft.com/library/dd635460%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="651bd-123">DeleteItem</span><span class="sxs-lookup"><span data-stu-id="651bd-123">DeleteItem</span></span>](../web-service-reference/deleteitem-operation.md) <br/> |

<span data-ttu-id="651bd-124">En este artículo, aprenderá a completar tareas básicas para lotes de mensajes de correo electrónico mediante la API administrada de EWS o EWS.</span><span class="sxs-lookup"><span data-stu-id="651bd-124">In this article, you'll learn how to complete basic tasks for batches of email messages by using the EWS Managed API or EWS.</span></span>

## <a name="create-email-messages-in-batches-by-using-the-ews-managed-api"></a><span data-ttu-id="651bd-125">Crear mensajes de correo electrónico en lotes mediante la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="651bd-125">Create email messages in batches by using the EWS Managed API</span></span>
<span data-ttu-id="651bd-126"><a name="bk_createewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="651bd-126"><a name="bk_createewsma"> </a></span></span>

<span data-ttu-id="651bd-127">Puede crear mensajes en lotes con el método **CreateItems** de la API administrada de EWS, como se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="651bd-127">You can create messages in batches by using the EWS Managed API **CreateItems** method, as shown in the following example.</span></span> <span data-ttu-id="651bd-128">En este ejemplo se crean tres objetos [EmailMessage](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx) de forma local, se agrega cada mensaje a una colección y, a continuación, se llama al método **CreateItems** en la colección de mensajes.</span><span class="sxs-lookup"><span data-stu-id="651bd-128">This example creates three [EmailMessage](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx) objects locally, adds each message to a collection, then calls the **CreateItems** method on the collection of messages.</span></span>

<span data-ttu-id="651bd-129">En este ejemplo se supone que el **servicio** es un objeto [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) válido y que el usuario se ha autenticado en un servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="651bd-129">This example assumes that **service** is a valid [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and that the user has been authenticated to an Exchange server.</span></span>

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

<span data-ttu-id="651bd-130">Tenga en cuenta que en el ejemplo solo se guardan los mensajes en la carpeta Borradores; no envía los mensajes.</span><span class="sxs-lookup"><span data-stu-id="651bd-130">Note that the example only saves the messages in the Drafts folder; it does not send the messages.</span></span> <span data-ttu-id="651bd-131">Para obtener más información sobre cómo enviar los mensajes, vea [enviar mensajes de correo electrónico en lotes mediante la API administrada de EWS](#bk_sendewsma).</span><span class="sxs-lookup"><span data-stu-id="651bd-131">For more about how to send the messages, see [Send email messages in batches by using the EWS Managed API](#bk_sendewsma).</span></span>

## <a name="create-email-messages-in-batches-by-using-ews"></a><span data-ttu-id="651bd-132">Crear mensajes de correo electrónico en lotes mediante EWS</span><span class="sxs-lookup"><span data-stu-id="651bd-132">Create email messages in batches by using EWS</span></span>
<span data-ttu-id="651bd-133"><a name="bk_createews"> </a></span><span class="sxs-lookup"><span data-stu-id="651bd-133"><a name="bk_createews"> </a></span></span>

<span data-ttu-id="651bd-134">Puede crear mensajes de correo electrónico en lotes mediante la operación de EWS del [CreateItem](https://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) , como se muestra en el siguiente ejemplo de código.</span><span class="sxs-lookup"><span data-stu-id="651bd-134">You can create email messages in batches by using the [CreateItem](https://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) EWS operation, as shown in the following code example.</span></span> <span data-ttu-id="651bd-135">También es la solicitud XML que la API administrada de EWS envía cuando usa la API administrada de EWS para [crear mensajes de correo electrónico en lotes](#bk_createewsma).</span><span class="sxs-lookup"><span data-stu-id="651bd-135">This is also the XML request that the EWS Managed API sends when you use the EWS Managed API to [create email messages in batches](#bk_createewsma).</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
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

<span data-ttu-id="651bd-136">El servidor responde a la solicitud **CreateItem** con un mensaje [CreateItemResponse](https://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) que incluye un valor [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) de **NoError** para cada uno de los nuevos mensajes, lo que indica que cada mensaje se creó y guardó correctamente.</span><span class="sxs-lookup"><span data-stu-id="651bd-136">The server responds to the **CreateItem** request with a [CreateItemResponse](https://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) message that includes a [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) value of **NoError** for each of the new messages, which indicates that each email was created and saved successfully.</span></span>

<span data-ttu-id="651bd-137">Tenga en cuenta que en el ejemplo solo se guardan los mensajes en la carpeta Borradores; no envía los mensajes.</span><span class="sxs-lookup"><span data-stu-id="651bd-137">Note that the example only saves the messages in the Drafts folder; it does not send the messages.</span></span> <span data-ttu-id="651bd-138">Para obtener más información sobre cómo enviar los mensajes, consulte [enviar mensajes de correo electrónico en lotes mediante EWS](#bk_sendews).</span><span class="sxs-lookup"><span data-stu-id="651bd-138">For more about how to send the messages, see [Send email messages in batches by using EWS](#bk_sendews).</span></span>

## <a name="send-email-messages-in-batches-by-using-the-ews-managed-api"></a><span data-ttu-id="651bd-139">Enviar mensajes de correo electrónico por lotes mediante la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="651bd-139">Send email messages in batches by using the EWS Managed API</span></span>
<span data-ttu-id="651bd-140"><a name="bk_sendewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="651bd-140"><a name="bk_sendewsma"> </a></span></span>

<span data-ttu-id="651bd-141">Se usa el mismo código para enviar mensajes de correo electrónico en lotes que se usan para crear mensajes de correo electrónico en lotes, excepto en que algunos de los parámetros del método [CreateItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.createitems%28v=exchg.80%29.aspx) cambian.</span><span class="sxs-lookup"><span data-stu-id="651bd-141">You use the same code to send email messages in batches that you use to create email messages in batches, except that a few of the [CreateItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.createitems%28v=exchg.80%29.aspx) method parameters change.</span></span> <span data-ttu-id="651bd-142">Por lo tanto, para enviar mensajes de correo electrónico mediante la API administrada de EWS, use el código que usa para [crear mensajes de correo electrónico en lotes](#bk_createewsma)y reemplace la llamada al método **CreateItems** por la llamada en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="651bd-142">So, to send email messages by using the EWS Managed API, use the code you use to [create email messages in batches](#bk_createewsma), and replace the call to the **CreateItems** method with the call in the following example.</span></span> <span data-ttu-id="651bd-143">En este ejemplo, los mensajes se crean en la carpeta elementos enviados y la disposición del mensaje se cambia a [MessageDisposition. SendAndSaveCopy](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.messagedisposition%28v=exchg.80%29.aspx), de modo que el mensaje se envía y no se acaba de guardar localmente.</span><span class="sxs-lookup"><span data-stu-id="651bd-143">In this example, the messages are created in the Sent Items folder, and the message disposition is changed to [MessageDisposition.SendAndSaveCopy](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.messagedisposition%28v=exchg.80%29.aspx), so that the message is sent, and not just saved locally.</span></span>

```cs
// Create and send the batch of email messages on the server.
// This method call results in an CreateItem call to EWS.
ServiceResponseCollection<ServiceResponse> response = service.CreateItems(messageItems, WellKnownFolderName.SentItems, MessageDisposition.SendAndSaveCopy, null);
```

## <a name="send-email-messages-in-batches-by-using-ews"></a><span data-ttu-id="651bd-144">Enviar mensajes de correo electrónico por lotes mediante EWS</span><span class="sxs-lookup"><span data-stu-id="651bd-144">Send email messages in batches by using EWS</span></span>
<span data-ttu-id="651bd-145"><a name="bk_sendews"> </a></span><span class="sxs-lookup"><span data-stu-id="651bd-145"><a name="bk_sendews"> </a></span></span>

<span data-ttu-id="651bd-146">Se usa el mismo código para enviar mensajes de correo electrónico en lotes que se usan para crear mensajes de correo electrónico en lotes, excepto en que algunos de los valores de atributo cambian para la operación **CreateItem** .</span><span class="sxs-lookup"><span data-stu-id="651bd-146">You use the same code to send email messages in batches that you use to create email messages in batches, except that a few of the attribute values change for the **CreateItem** operation.</span></span> <span data-ttu-id="651bd-147">Por lo tanto, para enviar mensajes de correo electrónico con EWS, use el código que usa para [crear mensajes de correo electrónico por lotes](#bk_createews)y cambie el valor de **MessageDisposition** a "SendAndSaveCopy" y cambie el [DistinguishedFolderId](https://msdn.microsoft.com/library/50018162-2941-4227-8a5b-d6b4686bb32f%28Office.15%29.aspx) a "sentitems", como se muestra en el siguiente ejemplo de código.</span><span class="sxs-lookup"><span data-stu-id="651bd-147">So, to send email messages by using EWS, use the code you use to [create email message in batches](#bk_createews), and change the **MessageDisposition** value to "SendAndSaveCopy", and change the [DistinguishedFolderId](https://msdn.microsoft.com/library/50018162-2941-4227-8a5b-d6b4686bb32f%28Office.15%29.aspx) to "sentitems", as shown in the following code example.</span></span>

```XML
<m:CreateItem MessageDisposition="SendAndSaveCopy">
  <m:SavedItemFolderId>
    <t:DistinguishedFolderId Id="sentitems" />
  </m:SavedItemFolderId>
```

<span data-ttu-id="651bd-148">El servidor responde a la solicitud **CreateItem** con un mensaje [CreateItemResponse](https://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) que incluye un valor [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) de **NoError** para cada uno de los nuevos mensajes, lo que indica que cada mensaje de correo electrónico se ha creado y enviado correctamente.</span><span class="sxs-lookup"><span data-stu-id="651bd-148">The server responds to the **CreateItem** request with a [CreateItemResponse](https://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) message that includes a [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) value of **NoError** for each of the new messages, which indicates that each email was created and sent successfully.</span></span>

## <a name="get-email-messages-in-batches-by-using-the-ews-managed-api"></a><span data-ttu-id="651bd-149">Obtener mensajes de correo electrónico en lotes mediante la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="651bd-149">Get email messages in batches by using the EWS Managed API</span></span>
<span data-ttu-id="651bd-150"><a name="bk_getewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="651bd-150"><a name="bk_getewsma"> </a></span></span>

<span data-ttu-id="651bd-151">Puede obtener mensajes de correo electrónico en lotes con el método [BindToItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.bindtoitems%28v=exchg.80%29.aspx) de la API administrada de EWS, como se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="651bd-151">You can get email messages in batches by using the EWS Managed API [BindToItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.bindtoitems%28v=exchg.80%29.aspx) method, as shown in the following example.</span></span>

<span data-ttu-id="651bd-152">En este ejemplo se supone que el **servicio** es un objeto [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) válido y que el usuario se ha autenticado en un servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="651bd-152">This example assumes that **service** is a valid [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and that the user has been authenticated to an Exchange server.</span></span>

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

## <a name="get-email-messages-in-batches-by-using-ews"></a><span data-ttu-id="651bd-153">Obtener mensajes de correo electrónico en lotes mediante EWS</span><span class="sxs-lookup"><span data-stu-id="651bd-153">Get email messages in batches by using EWS</span></span>
<span data-ttu-id="651bd-154"><a name="bk_getews"> </a></span><span class="sxs-lookup"><span data-stu-id="651bd-154"><a name="bk_getews"> </a></span></span>

<span data-ttu-id="651bd-155">Puede obtener mensajes de correo electrónico en lotes mediante la operación EWS de [GetItem](https://msdn.microsoft.com/library/e8492e3b-1c8d-4b14-8070-9530f8306edd%28Office.15%29.aspx) y el código del siguiente ejemplo.</span><span class="sxs-lookup"><span data-stu-id="651bd-155">You can get email messages in batches by using the [GetItem](https://msdn.microsoft.com/library/e8492e3b-1c8d-4b14-8070-9530f8306edd%28Office.15%29.aspx) EWS operation and the code in the following example.</span></span> <span data-ttu-id="651bd-156">También es la solicitud XML que la API administrada de EWS envía cuando usa la API administrada de EWS para [obtener mensajes de correo electrónico en lotes](#bk_getewsma).</span><span class="sxs-lookup"><span data-stu-id="651bd-156">This is also the XML request that the EWS Managed API sends when you use the EWS Managed API to [get email messages in batches](#bk_getewsma).</span></span>

<span data-ttu-id="651bd-157">Los atributos **Itemid** y **changekey** se han abreviado para facilitar su lectura.</span><span class="sxs-lookup"><span data-stu-id="651bd-157">The **ItemId** and **ChangeKey** attributes have been shortened for readability.</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
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

<span data-ttu-id="651bd-158">El servidor responde a la solicitud **GetItem** con un mensaje [GetItemResponse](https://msdn.microsoft.com/library/8b66de1b-26a6-476c-9585-a96059125716%28Office.15%29.aspx) que incluye las propiedades de la [primera clase](email-properties-and-elements-in-ews-in-exchange.md) para cada uno de los mensajes solicitados.</span><span class="sxs-lookup"><span data-stu-id="651bd-158">The server responds to the **GetItem** request with a [GetItemResponse](https://msdn.microsoft.com/library/8b66de1b-26a6-476c-9585-a96059125716%28Office.15%29.aspx) message that includes the [first class properties](email-properties-and-elements-in-ews-in-exchange.md) for each of the requested messages.</span></span>

## <a name="update-email-messages-in-batches-by-using-the-ews-managed-api"></a><span data-ttu-id="651bd-159">Actualizar mensajes de correo electrónico en lotes mediante la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="651bd-159">Update email messages in batches by using the EWS Managed API</span></span>
<span data-ttu-id="651bd-160"><a name="bk_updateewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="651bd-160"><a name="bk_updateewsma"> </a></span></span>

<span data-ttu-id="651bd-161">Puede obtener mensajes de correo electrónico en lotes con el método [UpdateItems](https://msdn.microsoft.com/library/dd634705%28v=exchg.80%29.aspx) de la API administrada de EWS, como se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="651bd-161">You can get email messages in batches by using the EWS Managed API [UpdateItems](https://msdn.microsoft.com/library/dd634705%28v=exchg.80%29.aspx) method, as shown in the following example.</span></span>

<span data-ttu-id="651bd-162">Para obtener una lista de las propiedades de mensajes de correo electrónico que se puede escribir, consulte [email Properties and Elements in EWS in Exchange](email-properties-and-elements-in-ews-in-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="651bd-162">For a list of writable email message properties, see [Email properties and elements in EWS in Exchange](email-properties-and-elements-in-ews-in-exchange.md).</span></span>

<span data-ttu-id="651bd-163">Para obtener información detallada sobre cómo enviar un borrador de mensaje una vez actualizado, vea [enviar mensajes de correo electrónico mediante la API administrada de EWS](#bk_sendewsma).</span><span class="sxs-lookup"><span data-stu-id="651bd-163">For details about how to send a draft message after it's been updated, see [Sending email messages by using the EWS Managed API](#bk_sendewsma).</span></span>

<span data-ttu-id="651bd-164">En este ejemplo se supone que el **servicio** es un objeto [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) válido y que el usuario se ha autenticado en un servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="651bd-164">This example assumes that **service** is a valid [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and that the user has been authenticated to an Exchange server.</span></span>

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

## <a name="update-email-messages-in-batches-by-using-ews"></a><span data-ttu-id="651bd-165">Actualizar mensajes de correo electrónico en lotes mediante EWS</span><span class="sxs-lookup"><span data-stu-id="651bd-165">Update email messages in batches by using EWS</span></span>
<span data-ttu-id="651bd-166"><a name="bk_updateews"> </a></span><span class="sxs-lookup"><span data-stu-id="651bd-166"><a name="bk_updateews"> </a></span></span>

<span data-ttu-id="651bd-167">Puede actualizar los mensajes de correo electrónico en lotes mediante la operación de EWS de [GetItem](https://msdn.microsoft.com/library/e8492e3b-1c8d-4b14-8070-9530f8306edd%28Office.15%29.aspx) , tal como se muestra en el siguiente ejemplo de código.</span><span class="sxs-lookup"><span data-stu-id="651bd-167">You can update email messages in batches by using the [GetItem](https://msdn.microsoft.com/library/e8492e3b-1c8d-4b14-8070-9530f8306edd%28Office.15%29.aspx) EWS operation, as shown in following code example.</span></span> <span data-ttu-id="651bd-168">También es la solicitud XML que la API administrada de EWS envía cuando usa la API administrada de EWS para [actualizar los mensajes de correo electrónico en lotes](#bk_updateewsma).</span><span class="sxs-lookup"><span data-stu-id="651bd-168">This is also the XML request that the EWS Managed API sends when you use the EWS Managed API to [update email messages in batches](#bk_updateewsma).</span></span>

<span data-ttu-id="651bd-169">Para obtener una lista de los elementos de mensajes de correo electrónico que se puede escribir, consulte [email Properties and Elements in EWS in Exchange](email-properties-and-elements-in-ews-in-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="651bd-169">For a list of writable email message elements, see [Email properties and elements in EWS in Exchange](email-properties-and-elements-in-ews-in-exchange.md).</span></span>

<span data-ttu-id="651bd-170">Para obtener información detallada sobre cómo enviar un borrador de mensaje una vez actualizado, vea [Enviar un borrador de mensaje de correo electrónico mediante EWS](how-to-send-email-messages-by-using-ews-in-exchange.md#bk_senddraftews).</span><span class="sxs-lookup"><span data-stu-id="651bd-170">For details about how to send a draft message after it's been updated, see [Send a draft email message by using EWS](how-to-send-email-messages-by-using-ews-in-exchange.md#bk_senddraftews).</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
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

<span data-ttu-id="651bd-171">El servidor responde a la solicitud **UpdateItem** con un mensaje [UpdateItemResponse](https://msdn.microsoft.com/library/023b79b4-c675-4669-9112-d85499ec4fc4%28Office.15%29.aspx) que incluye un [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) valor de **NoError**, lo que indica que cada una de las actualizaciones se guardaron correctamente en el servidor.</span><span class="sxs-lookup"><span data-stu-id="651bd-171">The server responds to the **UpdateItem** request with an [UpdateItemResponse](https://msdn.microsoft.com/library/023b79b4-c675-4669-9112-d85499ec4fc4%28Office.15%29.aspx) message that includes a [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) value of **NoError**, which indicates that each of the updates was saved successfully on the server.</span></span> <span data-ttu-id="651bd-172">Los conflictos se notifican en el elemento [ConflictResult](https://msdn.microsoft.com/library/08cdd547-4de7-4c7a-b60f-e618dc217d20%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="651bd-172">Any conflicts are reported in the [ConflictResult](https://msdn.microsoft.com/library/08cdd547-4de7-4c7a-b60f-e618dc217d20%28Office.15%29.aspx) element.</span></span>

## <a name="delete-email-messages-in-batches-by-using-the-ews-managed-api"></a><span data-ttu-id="651bd-173">Eliminar mensajes de correo electrónico en lotes mediante la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="651bd-173">Delete email messages in batches by using the EWS Managed API</span></span>
<span data-ttu-id="651bd-174"><a name="bk_deleteewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="651bd-174"><a name="bk_deleteewsma"> </a></span></span>

<span data-ttu-id="651bd-175">Puede eliminar mensajes en lotes con el método [DeleteItems](https://msdn.microsoft.com/library/dd635460%28v=exchg.80%29.aspx) de la API administrada de EWS, como se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="651bd-175">You can delete messages in batches by using the EWS Managed API [DeleteItems](https://msdn.microsoft.com/library/dd635460%28v=exchg.80%29.aspx) method, as shown in the following example.</span></span>

<span data-ttu-id="651bd-176">En este ejemplo se supone que el **servicio** es un objeto [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) válido y que el usuario se ha autenticado en un servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="651bd-176">This example assumes that **service** is a valid [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and that the user has been authenticated to an Exchange server.</span></span>

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

## <a name="delete-email-messages-in-batches-by-using-ews"></a><span data-ttu-id="651bd-177">Eliminar mensajes de correo electrónico en lotes mediante EWS</span><span class="sxs-lookup"><span data-stu-id="651bd-177">Delete email messages in batches by using EWS</span></span>
<span data-ttu-id="651bd-178"><a name="bk_deleteews"> </a></span><span class="sxs-lookup"><span data-stu-id="651bd-178"><a name="bk_deleteews"> </a></span></span>

<span data-ttu-id="651bd-179">Puede eliminar mensajes de correo electrónico en lotes mediante la operación de EWS [DeleteItem](../web-service-reference/deleteitem-operation.md) , tal como se muestra en el siguiente ejemplo de código.</span><span class="sxs-lookup"><span data-stu-id="651bd-179">You can delete email messages in batches by using the [DeleteItem](../web-service-reference/deleteitem-operation.md) EWS operation, as shown in the following code example.</span></span> <span data-ttu-id="651bd-180">También es la solicitud XML que la API administrada de EWS envía cuando usa la API administrada de EWS para [eliminar mensajes de correo electrónico en lotes](#bk_deleteewsma).</span><span class="sxs-lookup"><span data-stu-id="651bd-180">This is also the XML request that the EWS Managed API sends when you use the EWS Managed API to [delete email messages in batches](#bk_deleteewsma).</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
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

<span data-ttu-id="651bd-181">El servidor responde a la solicitud **DeleteItem** con un mensaje [DeleteItemResponse](https://msdn.microsoft.com/library/86463d66-fe47-4a19-a81b-e24841e816ab%28Office.15%29.aspx) que incluye un valor [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) de **NoError** para cada elemento que se ha quitado.</span><span class="sxs-lookup"><span data-stu-id="651bd-181">The server responds to the **DeleteItem** request with a [DeleteItemResponse](https://msdn.microsoft.com/library/86463d66-fe47-4a19-a81b-e24841e816ab%28Office.15%29.aspx) message that includes a [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) value of **NoError** for each item that was removed.</span></span> <span data-ttu-id="651bd-182">Tenga en cuenta que la operación también devuelve SUCCESS si no se encuentra el identificador de elemento.</span><span class="sxs-lookup"><span data-stu-id="651bd-182">Note that the operation also returns success if the item ID could not be found.</span></span>

## <a name="verifying-that-a-batch-process-completed-successfully"></a><span data-ttu-id="651bd-183">Comprobación de la finalización correcta de un proceso por lotes</span><span class="sxs-lookup"><span data-stu-id="651bd-183">Verifying that a batch process completed successfully</span></span>
<span data-ttu-id="651bd-184"><a name="bk_successful"> </a></span><span class="sxs-lookup"><span data-stu-id="651bd-184"><a name="bk_successful"> </a></span></span>

<span data-ttu-id="651bd-185">Cuando no se pueden procesar uno o varios mensajes de correo electrónico en una solicitud por lotes como se solicitó, se devuelve un error para cada mensaje de correo electrónico en el que se ha producido un error y el resto de los correos electrónicos del lote se procesan como se esperaba.</span><span class="sxs-lookup"><span data-stu-id="651bd-185">When one or more email messages in a batched request can't be processed as requested, an error is returned for each email message that failed, and the rest of the emails in the batch are processed as expected.</span></span> <span data-ttu-id="651bd-186">Los errores en el procesamiento por lotes pueden producirse si el elemento se eliminó y, por lo tanto, no se puede enviar, recuperar o actualizar, o si el elemento se movió a una carpeta diferente y, por lo tanto, tiene un identificador de elemento nuevo y no se puede modificar con el identificador de elemento enviado.</span><span class="sxs-lookup"><span data-stu-id="651bd-186">Failures in batch processing can occur if the item was deleted, and therefore can't be sent, retrieved, or updated, or if the item moved to a different folder, and therefore has a new item ID, and cannot be modified with the item ID sent.</span></span> <span data-ttu-id="651bd-187">La información de esta sección muestra cómo obtener detalles de error sobre los errores en el procesamiento por lotes del mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="651bd-187">The information in this section shows how to get error details about failures in batch processing of email message.</span></span>

<span data-ttu-id="651bd-188">Para comprobar que el proceso por lotes se ha realizado correctamente mediante la API administrada de EWS, puede comprobar que la propiedad [OverallResult](https://msdn.microsoft.com/library/dd634515%28v=exchg.80%29.aspx) de [ServiceResponseCollection](https://msdn.microsoft.com/library/dd633715%28v=exchg.80%29.aspx) es igual a [ServiceResult. Success](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresult%28v=exchg.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="651bd-188">To verify the success of a batch process by using the EWS Managed API, you can check that the [OverallResult](https://msdn.microsoft.com/library/dd634515%28v=exchg.80%29.aspx) property of the [ServiceResponseCollection](https://msdn.microsoft.com/library/dd633715%28v=exchg.80%29.aspx) is equal to [ServiceResult.Success](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresult%28v=exchg.80%29.aspx).</span></span> <span data-ttu-id="651bd-189">Si es así, todos los correos electrónicos se procesaron correctamente.</span><span class="sxs-lookup"><span data-stu-id="651bd-189">If so, all the emails were processed successfully.</span></span> <span data-ttu-id="651bd-190">Si **OverallResult** no es igual a **ServiceResult. Success**, no se procesaron correctamente uno o más de los mensajes de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="651bd-190">If the **OverallResult** is not equal to **ServiceResult.Success**, one or more of the emails were not processed successfully.</span></span> <span data-ttu-id="651bd-191">Cada uno de los objetos devueltos en **ServiceResponseCollection** contiene las siguientes propiedades:</span><span class="sxs-lookup"><span data-stu-id="651bd-191">Each of the objects returned in the **ServiceResponseCollection** contains the following properties:</span></span>

- [<span data-ttu-id="651bd-192">ErrorCode</span><span class="sxs-lookup"><span data-stu-id="651bd-192">ErrorCode</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponse.errorcode%28v=exchg.80%29.aspx)

- [<span data-ttu-id="651bd-193">ErrorDetails</span><span class="sxs-lookup"><span data-stu-id="651bd-193">ErrorDetails</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponse.errordetails%28v=exchg.80%29.aspx)

- [<span data-ttu-id="651bd-194">ErrorMessage</span><span class="sxs-lookup"><span data-stu-id="651bd-194">ErrorMessage</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponse.errormessage%28v=exchg.80%29.aspx)

- [<span data-ttu-id="651bd-195">ErrorProperties</span><span class="sxs-lookup"><span data-stu-id="651bd-195">ErrorProperties</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponse.errorproperties%28v=exchg.80%29.aspx)

- [<span data-ttu-id="651bd-196">Resultado</span><span class="sxs-lookup"><span data-stu-id="651bd-196">Result</span></span>](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.serviceresponse.result%28v=exchg.80%29.aspx)

<span data-ttu-id="651bd-197">Estas propiedades contienen información sobre por qué los mensajes de correo electrónico no se pudieron procesar como se ha solicitado.</span><span class="sxs-lookup"><span data-stu-id="651bd-197">These properties contain information about why the email messages could not be processed as requested.</span></span> <span data-ttu-id="651bd-198">Los ejemplos de este artículo imprimen el **resultado**, **ErrorCode**y **errorMessage** de cada mensaje con errores.</span><span class="sxs-lookup"><span data-stu-id="651bd-198">The examples in this article print out the **Result**, **ErrorCode**, and **ErrorMessage** for each failed message.</span></span> <span data-ttu-id="651bd-199">Puede usar estos resultados para investigar el problema.</span><span class="sxs-lookup"><span data-stu-id="651bd-199">You can use these results to investigate the issue.</span></span>

<span data-ttu-id="651bd-200">Para EWS, para comprobar que el proceso por lotes se ha realizado correctamente, compruebe el atributo [ResponseClass](https://msdn.microsoft.com/library/bf57265a-d354-4cd7-bbfc-d93e19cbede6%28Office.15%29.aspx) para cada elemento que se está procesando.</span><span class="sxs-lookup"><span data-stu-id="651bd-200">For EWS, to verify the success of a batched process, check the [ResponseClass](https://msdn.microsoft.com/library/bf57265a-d354-4cd7-bbfc-d93e19cbede6%28Office.15%29.aspx) attribute for each item being processed.</span></span> <span data-ttu-id="651bd-201">La siguiente es la estructura básica de **ResponseMessageType**, el tipo base del que se derivan todos los mensajes de respuesta.</span><span class="sxs-lookup"><span data-stu-id="651bd-201">The following is the basic structure of the **ResponseMessageType**, the base type from which all response messages are derived.</span></span>

```XML
<ResponseMessage ResponseClass="Success | Warning | Error">
            <MessageText/>
            <ResponseCode/>
            <DescriptiveLinkKey/>
            <MessageXml/>
</ResponseMessage>
```

<span data-ttu-id="651bd-202">El atributo **ResponseClass** se establece en **Success** si el correo electrónico se ha procesado correctamente, o **error** si el correo electrónico no se ha procesado correctamente.</span><span class="sxs-lookup"><span data-stu-id="651bd-202">The **ResponseClass** attribute is set to **Success** if the email was processed successfully, or **Error** if the email was not processed successfully.</span></span> <span data-ttu-id="651bd-203">Para los mensajes de correo electrónico, no encontrará ninguna **ADVERTENCIA** durante el procesamiento por lotes.</span><span class="sxs-lookup"><span data-stu-id="651bd-203">For email messages, you will not encounter a **Warning** during batch processing.</span></span> <span data-ttu-id="651bd-204">Si el **ResponseClass** es **correcto**, el elemento [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) que sigue también se establece siempre en **NoError**.</span><span class="sxs-lookup"><span data-stu-id="651bd-204">If the **ResponseClass** is **Success**, the [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) element that follows is also always set to **NoError**.</span></span> <span data-ttu-id="651bd-205">Si el **ResponseClass** es **error**, debe comprobar los valores de los elementos [MessageText](https://msdn.microsoft.com/library/59a23bdc-0d9a-4942-8b3c-9cdb11db1ab1%28Office.15%29.aspx), **ResponseCode**y [MessageXml](https://msdn.microsoft.com/library/bcaf9e35-d351-48f3-baad-f90c633cba8a%28Office.15%29.aspx) para determinar la causa del problema.</span><span class="sxs-lookup"><span data-stu-id="651bd-205">If the **ResponseClass** is **Error**, you need to check the values of the [MessageText](https://msdn.microsoft.com/library/59a23bdc-0d9a-4942-8b3c-9cdb11db1ab1%28Office.15%29.aspx), **ResponseCode**, and [MessageXml](https://msdn.microsoft.com/library/bcaf9e35-d351-48f3-baad-f90c633cba8a%28Office.15%29.aspx) elements to determine what caused the problem.</span></span> <span data-ttu-id="651bd-206">[DescriptiveLinkKey](https://msdn.microsoft.com/library/f7f36749-00f3-4915-b17c-e3caa0af6e67%28Office.15%29.aspx) actualmente no está en uso.</span><span class="sxs-lookup"><span data-stu-id="651bd-206">[DescriptiveLinkKey](https://msdn.microsoft.com/library/f7f36749-00f3-4915-b17c-e3caa0af6e67%28Office.15%29.aspx) is currently unused.</span></span>

## <a name="see-also"></a><span data-ttu-id="651bd-207">Vea también</span><span class="sxs-lookup"><span data-stu-id="651bd-207">See also</span></span>


- [<span data-ttu-id="651bd-208">Correo electrónico y EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="651bd-208">Email and EWS in Exchange</span></span>](email-and-ews-in-exchange.md)

- [<span data-ttu-id="651bd-209">Enviar mensajes de correo electrónico mediante EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="651bd-209">Send email messages by using EWS in Exchange</span></span>](how-to-send-email-messages-by-using-ews-in-exchange.md)

- [<span data-ttu-id="651bd-210">Responder a mensajes de correo electrónico mediante EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="651bd-210">Respond to email messages by using EWS in Exchange</span></span>](how-to-respond-to-email-messages-by-using-ews-in-exchange.md)

- [<span data-ttu-id="651bd-211">Mover y copiar mensajes de correo electrónico mediante EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="651bd-211">Move and copy email messages by using EWS in Exchange</span></span>](how-to-move-and-copy-email-messages-by-using-ews-in-exchange.md)

- [<span data-ttu-id="651bd-212">Implicaciones de limitación de solicitudes por lotes de EWS</span><span class="sxs-lookup"><span data-stu-id="651bd-212">Throttling implications for EWS batch requests</span></span>](ews-throttling-in-exchange.md#throttling-implications-for-ews-batch-requests)
