---
title: Enviar mensajes de correo electrónico mediante el uso de EWS en Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5290fafe-8b51-4275-a27e-baf497fc969c
description: Obtenga información sobre cómo enviar mensajes de correo electrónico nuevo o borrador, o bien, para enviar un mensaje de correo electrónico retrasada mediante la API administrada de EWS o EWS en Exchange.
ms.openlocfilehash: f09babfcc420d4cbc563ed6605ba555fd9f8c7e9
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763166"
---
# <a name="send-email-messages-by-using-ews-in-exchange"></a><span data-ttu-id="d50bc-103">Enviar mensajes de correo electrónico mediante el uso de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="d50bc-103">Send email messages by using EWS in Exchange</span></span>

<span data-ttu-id="d50bc-104">Obtenga información sobre cómo enviar mensajes de correo electrónico nuevo o borrador, o bien, para enviar un mensaje de correo electrónico retrasada mediante la API administrada de EWS o EWS en Exchange.</span><span class="sxs-lookup"><span data-stu-id="d50bc-104">Learn how to send new or draft email messages, or to send a delayed email message by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="d50bc-105">Si está utilizando la API administrada de EWS o EWS, puede enviar mensajes de correo electrónico de dos maneras.</span><span class="sxs-lookup"><span data-stu-id="d50bc-105">Whether you are using the EWS Managed API or EWS, you can send email messages in two ways.</span></span> <span data-ttu-id="d50bc-106">O bien puede enviar un mensaje existente, como un mensaje almacenado en la carpeta Borrador, o puede crear y enviar un correo electrónico en un solo paso.</span><span class="sxs-lookup"><span data-stu-id="d50bc-106">You can either send an existing message, such as a message stored in your Drafts folder, or you can create and send an email in one step.</span></span> <span data-ttu-id="d50bc-107">Los métodos y las operaciones que se usa para enviar el mensaje son los mismos si se está enviando un mensaje inmediatamente, o enviar un mensaje retrasado.</span><span class="sxs-lookup"><span data-stu-id="d50bc-107">The methods and operations that you use to send the message are the same whether you're sending a message immediately, or sending a delayed message.</span></span>
  
<span data-ttu-id="d50bc-108">**La tabla 1. Métodos de la API administrada de EWS y las operaciones de EWS para el envío de mensajes de correo electrónico**</span><span class="sxs-lookup"><span data-stu-id="d50bc-108">**Table 1. EWS Managed API methods and EWS operations for sending email messages**</span></span>

|<span data-ttu-id="d50bc-109">**Tarea**</span><span class="sxs-lookup"><span data-stu-id="d50bc-109">**Task**</span></span>|<span data-ttu-id="d50bc-110">**Método de la API administrada de EWS**</span><span class="sxs-lookup"><span data-stu-id="d50bc-110">**EWS Managed API method**</span></span>|<span data-ttu-id="d50bc-111">**Operación de EWS**</span><span class="sxs-lookup"><span data-stu-id="d50bc-111">**EWS operation**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d50bc-112">Enviar un nuevo mensaje de correo electrónico</span><span class="sxs-lookup"><span data-stu-id="d50bc-112">Send a new email message</span></span>  <br/> |[<span data-ttu-id="d50bc-113">EmailMessage.SendAndSaveCopy</span><span class="sxs-lookup"><span data-stu-id="d50bc-113">EmailMessage.SendAndSaveCopy</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.sendandsavecopy%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="d50bc-114">CreateItem</span><span class="sxs-lookup"><span data-stu-id="d50bc-114">CreateItem</span></span>](http://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="d50bc-115">Enviar un mensaje de correo electrónico existente</span><span class="sxs-lookup"><span data-stu-id="d50bc-115">Send an existing email message</span></span>  <br/> |[<span data-ttu-id="d50bc-116">EmailMessage.Send</span><span class="sxs-lookup"><span data-stu-id="d50bc-116">EmailMessage.Send</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.send%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="d50bc-117">SendItem</span><span class="sxs-lookup"><span data-stu-id="d50bc-117">SendItem</span></span>](http://msdn.microsoft.com/library/337b89ef-e1b7-45ed-92f3-8abe4200e4c7%28Office.15%29.aspx) <br/> |
   
## <a name="send-a-new-email-message-by-using-the-ews-managed-api"></a><span data-ttu-id="d50bc-118">Enviar un nuevo mensaje de correo electrónico mediante el uso de la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="d50bc-118">Send a new email message by using the EWS Managed API</span></span>
<span data-ttu-id="d50bc-119"><a name="bk_sendnewewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="d50bc-119"></span></span>

<span data-ttu-id="d50bc-120">En el ejemplo de código siguiente se muestra cómo usar el objeto [EmailMessage](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx) para crear un mensaje de correo electrónico y el método [SendAndSaveCopy](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.sendandsavecopy%28v=exchg.80%29.aspx) para enviar el mensaje al destinatario y guardar el mensaje en la carpeta Elementos enviados.</span><span class="sxs-lookup"><span data-stu-id="d50bc-120">The following code example shows how to use the [EmailMessage](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx) object to create an email message and the [SendAndSaveCopy](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.sendandsavecopy%28v=exchg.80%29.aspx) method to send the message to the recipient and save the message in the Sent Items folder.</span></span> 
  
<span data-ttu-id="d50bc-121">En este ejemplo se da por supuesto que **servicio** es un objeto [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) válido y que se ha autenticado el usuario a un servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="d50bc-121">This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and that the user has been authenticated to an Exchange server.</span></span> 
  
```cs
// Create an email message and provide it with connection 
// configuration information by using an ExchangeService object named service.
EmailMessage message = new EmailMessage(service);
// Set properties on the email message.
message.Subject = "Company Soccer Team";
message.Body = "Are you interested in joining?";
message.ToRecipients.Add("sadie@contoso.com");
// Send the email message and save a copy.
// This method call results in a CreateItem call to EWS.
message.SendAndSaveCopy();
Console.WriteLine("An email with the subject '" + message.Subject + "' has been sent to '" + message.ToRecipients[0] + "' and saved in the SendItems folder.");
```

## <a name="send-a-new-email-message-by-using-ews"></a><span data-ttu-id="d50bc-122">Enviar un nuevo mensaje de correo electrónico mediante el uso de EWS</span><span class="sxs-lookup"><span data-stu-id="d50bc-122">Send a new email message by using EWS</span></span>
<span data-ttu-id="d50bc-123"><a name="bk_sendnewews"> </a></span><span class="sxs-lookup"><span data-stu-id="d50bc-123"></span></span>

<span data-ttu-id="d50bc-124">En el ejemplo de código siguiente se muestra cómo usar la operación [CreateItem](http://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) con un valor de **MessageDisposition** de **SendAndSaveCopy** para crear un mensaje de correo electrónico, enviar el mensaje al destinatario y guardar el mensaje en la carpeta Elementos enviados.</span><span class="sxs-lookup"><span data-stu-id="d50bc-124">The following code example shows how to use the [CreateItem](http://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) operation with a **MessageDisposition** value of **SendAndSaveCopy** to create an email message, send the message to the recipient, and save the message in the Sent Items folder.</span></span> <span data-ttu-id="d50bc-125">Esto también es la solicitud XML que la API administrada de EWS envía cuándo [Enviar un nuevo mensaje de correo electrónico](#bk_sendnewewsma).</span><span class="sxs-lookup"><span data-stu-id="d50bc-125">This is also the XML request that the EWS Managed API sends when you [send a new email message](#bk_sendnewewsma).</span></span>
  
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
    <m:CreateItem MessageDisposition="SendAndSaveCopy">
      <m:SavedItemFolderId>
        <t:DistinguishedFolderId Id="sentitems" />
      </m:SavedItemFolderId>
      <m:Items>
        <t:Message>
          <t:Subject>Company Soccer Team</t:Subject>
          <t:Body BodyType="HTML">Are you interested in joining?</t:Body>
          <t:ToRecipients>
            <t:Mailbox>
              <t:EmailAddress>sadie@contoso.com </t:EmailAddress>
              </t:Mailbox>
          </t:ToRecipients>
        </t:Message>
      </m:Items>
    </m:CreateItem>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="d50bc-126">El servidor responde a la solicitud **CreateItem** con un mensaje de [CreateItemResponse](http://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) que incluye un valor [ResponseCode](http://msdn.microsoft.com/en-us/library/aa580757%28v=exchg.150%29.aspx) **NoError**, lo que indica que el correo electrónico se ha creado correctamente y la [ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) de la recientemente mensaje de creación.</span><span class="sxs-lookup"><span data-stu-id="d50bc-126">The server responds to the **CreateItem** request with a [CreateItemResponse](http://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/en-us/library/aa580757%28v=exchg.150%29.aspx) value of **NoError**, which indicates that the email was created successfully, and the [ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) of the newly created message.</span></span> 
  
## <a name="send-a-draft-email-message-by-using-the-ews-managed-api"></a><span data-ttu-id="d50bc-127">Enviar un borrador de mensaje de correo electrónico mediante el uso de la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="d50bc-127">Send a draft email message by using the EWS Managed API</span></span>
<span data-ttu-id="d50bc-128"><a name="bk_senddraftewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="d50bc-128"></span></span>

<span data-ttu-id="d50bc-129">En el ejemplo de código siguiente se muestra cómo enviar un mensaje que se almacena en la carpeta Borradores, tal como se muestra en [crear un mensaje de correo electrónico mediante el uso de la API administrada de EWS](email-and-ews-in-exchange.md#bk_createewsma).</span><span class="sxs-lookup"><span data-stu-id="d50bc-129">The following code example shows how to send a message that was stored in the Drafts folder, as shown in [Create an email message by using the EWS Managed API](email-and-ews-in-exchange.md#bk_createewsma).</span></span> <span data-ttu-id="d50bc-130">En primer lugar, use el método [Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) para recuperar el mensaje y, a continuación, utilice el método [Send](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.send%28v=exchg.80%29.aspx) para enviar el mensaje de correo electrónico, tal como se muestra en el siguiente ejemplo de código.</span><span class="sxs-lookup"><span data-stu-id="d50bc-130">First, use the [Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) method to retrieve the message, and then use the [Send](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.send%28v=exchg.80%29.aspx) method to send the email message, as shown in the following code example.</span></span> <span data-ttu-id="d50bc-131">Tenga en cuenta que este método no guarda el mensaje enviado en la carpeta Elementos enviados.</span><span class="sxs-lookup"><span data-stu-id="d50bc-131">Note that this method does not save the sent message in the Sent Items folder.</span></span> 
  
<span data-ttu-id="d50bc-132">En este caso, las propiedades [EmailMessageSchema.Subject](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.itemschema.subject%28v=exchg.80%29.aspx) y [EmailMessageSchema.ToRecipients](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessageschema.torecipients%28v=exchg.80%29.aspx) se agregan a la [PropertySet](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.propertyset%28v=exchg.80%29.aspx) para que los valores que pueden incluirse en el resultado de la consola.</span><span class="sxs-lookup"><span data-stu-id="d50bc-132">In this case, the [EmailMessageSchema.Subject](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.itemschema.subject%28v=exchg.80%29.aspx) and [EmailMessageSchema.ToRecipients](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessageschema.torecipients%28v=exchg.80%29.aspx) properties are added to the [PropertySet](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.propertyset%28v=exchg.80%29.aspx) so that the values can be included in the console output.</span></span> 
  
<span data-ttu-id="d50bc-133">En este ejemplo se da por supuesto que **servicio** es un objeto [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) válido y que se ha autenticado el usuario a un servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="d50bc-133">This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and that the user has been authenticated to an Exchange server.</span></span> 
  
```cs
// As a best practice, create a property set that limits the properties returned by the Bind method to only those that are required.
PropertySet propSet = new PropertySet(BasePropertySet.IdOnly, EmailMessageSchema.Subject, EmailMessageSchema.ToRecipients);
// This method call results in a GetItem call to EWS.
EmailMessage message = EmailMessage.Bind(service, ItemId, propSet);
// Send the email message.
// This method call results in a SendItem call to EWS.
message.Send();
Console.WriteLine("An email with the subject '" + message.Subject + "' has been sent to '" + message.ToRecipients[0] + "'.");
```

## <a name="send-a-draft-email-message-by-using-ews"></a><span data-ttu-id="d50bc-134">Enviar un borrador de mensaje de correo electrónico mediante el uso de EWS</span><span class="sxs-lookup"><span data-stu-id="d50bc-134">Send a draft email message by using EWS</span></span>
<span data-ttu-id="d50bc-135"><a name="bk_senddraftews"> </a></span><span class="sxs-lookup"><span data-stu-id="d50bc-135"></span></span>

<span data-ttu-id="d50bc-136">Ejemplos de código siguientes muestran cómo enviar un mensaje que estaba anteriormente almacenado en la carpeta Borradores, tal como se muestra en [crear un mensaje de correo electrónico mediante el uso de EWS](email-and-ews-in-exchange.md#bk_createews).</span><span class="sxs-lookup"><span data-stu-id="d50bc-136">The following code examples show how to send a message that was previously stored in the Drafts folder, as shown in [Create an email message by using EWS](email-and-ews-in-exchange.md#bk_createews).</span></span> <span data-ttu-id="d50bc-137">En primer lugar, use la operación [GetItem](http://msdn.microsoft.com/library/e8492e3b-1c8d-4b14-8070-9530f8306edd%28Office.15%29.aspx) para recuperar el mensaje de correo electrónico para enviar.</span><span class="sxs-lookup"><span data-stu-id="d50bc-137">First use the [GetItem](http://msdn.microsoft.com/library/e8492e3b-1c8d-4b14-8070-9530f8306edd%28Office.15%29.aspx) operation to retrieve the email message to send.</span></span> <span data-ttu-id="d50bc-138">A continuación, use la operación de [SendItem](http://msdn.microsoft.com/library/337b89ef-e1b7-45ed-92f3-8abe4200e4c7%28Office.15%29.aspx) para enviar el mensaje de correo electrónico a los destinatarios y vuelva a guardarla en la carpeta Elementos enviados.</span><span class="sxs-lookup"><span data-stu-id="d50bc-138">Then use the [SendItem](http://msdn.microsoft.com/library/337b89ef-e1b7-45ed-92f3-8abe4200e4c7%28Office.15%29.aspx) operation to send the email message to recipients and save it in the Sent Items folder.</span></span> 
  
<span data-ttu-id="d50bc-139">El primer mensaje, el mensaje de solicitud **GetItem** , especifica la [ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) del mensaje de correo electrónico de borrador para enlazar a y elementos en el elemento [ItemShape](http://msdn.microsoft.com/library/c5604161-bbc0-40bc-ad75-ff7e837d745f%28Office.15%29.aspx) limitar los resultados a incluir en la respuesta **GetItem** .</span><span class="sxs-lookup"><span data-stu-id="d50bc-139">The first message, the **GetItem** request message, specifies the [ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) of the draft email message to bind to, and elements in the [ItemShape](http://msdn.microsoft.com/library/c5604161-bbc0-40bc-ad75-ff7e837d745f%28Office.15%29.aspx) element limit the results to include in the **GetItem** response.</span></span> <span data-ttu-id="d50bc-140">El elemento **ItemShape** tiene un [BaseShape](http://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx) de **IdOnly**y el elemento [AdditionalProperties](http://msdn.microsoft.com/library/7a269aed-dcfd-4c3e-9e14-094e53828101%28Office.15%29.aspx) incluye el [FieldURI](http://msdn.microsoft.com/library/24af8e3b-3074-4c8c-8d0a-52446508d044%28Office.15%29.aspx) los valores de la propiedad **Subject** desde el esquema de elemento y el **ToRecipients** propiedad del esquema de mensaje, lo que significa que sólo los elementos **ItemId**, el [asunto](http://msdn.microsoft.com/library/c140d6c2-deb1-4f67-a908-9397197c4ae7%28Office.15%29.aspx)y [ToRecipients](http://msdn.microsoft.com/library/72dc3be8-30bb-4ae1-acf4-fb94ff490631%28Office.15%29.aspx) se devolverán al cliente en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d50bc-140">The **ItemShape** element has a [BaseShape](http://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx) of **IdOnly**, and the [AdditionalProperties](http://msdn.microsoft.com/library/7a269aed-dcfd-4c3e-9e14-094e53828101%28Office.15%29.aspx) element includes the [FieldURI](http://msdn.microsoft.com/library/24af8e3b-3074-4c8c-8d0a-52446508d044%28Office.15%29.aspx) values for the **Subject** property from the Item schema and the **ToRecipients** property from the Message schema, which means that only the **ItemId**, [Subject](http://msdn.microsoft.com/library/c140d6c2-deb1-4f67-a908-9397197c4ae7%28Office.15%29.aspx), and [ToRecipients](http://msdn.microsoft.com/library/72dc3be8-30bb-4ae1-acf4-fb94ff490631%28Office.15%29.aspx) elements will be returned to the client in the response.</span></span> <span data-ttu-id="d50bc-141">Para obtener más información acerca de cómo limitar los valores devueltos en las llamadas y el significado del elemento **BaseShape** , vea [conjuntos de propiedades y respuesta de formas en EWS en Exchange](property-sets-and-response-shapes-in-ews-in-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="d50bc-141">For more information about limiting the values returned in calls and the meaning of the **BaseShape** element, see [Property sets and response shapes in EWS in Exchange](property-sets-and-response-shapes-in-ews-in-exchange.md).</span></span>
  
<span data-ttu-id="d50bc-142">También es la solicitud XML que se envía por la API administrada de EWS al llamar al método [enlazar](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="d50bc-142">This is also the XML request that is sent by the EWS Managed API when calling the [Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) method.</span></span> <span data-ttu-id="d50bc-143">Los valores de algunos elementos y atributos se han abreviado para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="d50bc-143">The values of some attributes and elements have been shortened for readability.</span></span> 
  
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
        <t:ItemId Id="AAMkADE4=" />
      </m:ItemIds>
    </m:GetItem>
  </soap:Body>
</soap:Envelope>
```

En el ejemplo siguiente se muestra la respuesta XML que el servidor devuelve una vez que procesa la operación **GetItem** . La respuesta indica que el mensaje de correo electrónico se recuperó correctamente e incluye los elementos del **asunto** y **ToRecipient** como se solicitó. <span data-ttu-id="d50bc-146">Los valores de algunos elementos y atributos se han abreviado para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="d50bc-146">The values of some attributes and elements have been shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="842"
                         MinorBuildNumber="10"
                         Version="V2_8"
                         xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
                       xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:GetItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Items>
            <t:Message>
              <t:ItemId Id="AAMkADE4="
                        ChangeKey="CQAAABYA" />
              <t:Subject>Project priorities</t:Subject>
              <t:ToRecipients>
                <t:Mailbox>
                  <t:Name>sadie@contoso.com</t:Name>
                  <t:EmailAddress>sadie@contoso.com</t:EmailAddress>
                  <t:RoutingType>SMTP</t:RoutingType>
                  <t:MailboxType>OneOff</t:MailboxType>
                </t:Mailbox>
              </t:ToRecipients>
            </t:Message>
          </m:Items>
        </m:GetItemResponseMessage>
      </m:ResponseMessages>
    </m:GetItemResponse>
  </s:Body>
</s:Envelope>
```

<span data-ttu-id="d50bc-147">El segundo mensaje, el mensaje de solicitud **SendItem** , especifica la [ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) del mensaje de correo electrónico para enviar, así como [SavedItemFolderId](http://msdn.microsoft.com/library/4b8b475c-9ca5-48c9-acb0-8848b53be1ce%28Office.15%29.aspx), que especifica la carpeta en la que se va a guardar el elemento enviado.</span><span class="sxs-lookup"><span data-stu-id="d50bc-147">The second message, the **SendItem** request message, specifies the [ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) of the email message to send, as well as the [SavedItemFolderId](http://msdn.microsoft.com/library/4b8b475c-9ca5-48c9-acb0-8848b53be1ce%28Office.15%29.aspx), which specifies the folder in which to save the sent item.</span></span>
  
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
    <m:SendItem SaveItemToFolder="true">
      <m:ItemIds>
        <t:ItemId Id="AAMkADE4="
                  ChangeKey="CQAAABYA" />
      </m:ItemIds>
      <m:SavedItemFolderId>
        <t:DistinguishedFolderId Id="sentitems" />
      </m:SavedItemFolderId>
    </m:SendItem>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="d50bc-148">El servidor responde a la solicitud de **SendItem** con un mensaje de [SendItemResponse](http://msdn.microsoft.com/library/26ac41c7-57d9-473e-ab7a-bae93e1d2aba%28Office.15%29.aspx) que incluye un valor [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) de **NoError**, lo que indica que el correo electrónico se ha enviado correctamente.</span><span class="sxs-lookup"><span data-stu-id="d50bc-148">The server responds to the **SendItem** request with a [SendItemResponse](http://msdn.microsoft.com/library/26ac41c7-57d9-473e-ab7a-bae93e1d2aba%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) value of **NoError**, which indicates that the email was sent successfully.</span></span>
  
## <a name="send-a-delayed-email-message-by-using-the-ews-managed-api"></a><span data-ttu-id="d50bc-149">Enviar un mensaje de correo electrónico retrasada mediante el uso de la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="d50bc-149">Send a delayed email message by using the EWS Managed API</span></span>
<span data-ttu-id="d50bc-150"><a name="bk_senddelayedewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="d50bc-150"></span></span>

<span data-ttu-id="d50bc-151">En el ejemplo de código siguiente se muestra cómo usar el objeto [EmailMessage](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx) para crear un mensaje de correo electrónico, la clase [ExtendedPropertyDefinition](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.extendedpropertydefinition%28v=exchg.80%29.aspx) para crear una definición de propiedad para la propiedad [PidTagDeferredSendTime](http://msdn.microsoft.com/en-us/library/cc840017.aspx) (0x3FEF0040) y la Método [SendAndSaveCopy](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.sendandsavecopy%28v=exchg.80%29.aspx) para enviar un mensaje retrasado y guardar el mensaje en la carpeta Elementos enviados.</span><span class="sxs-lookup"><span data-stu-id="d50bc-151">The following code example shows how to use the [EmailMessage](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx) object to create an email message, the [ExtendedPropertyDefinition](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.extendedpropertydefinition%28v=exchg.80%29.aspx) class to create a property definition for the [PidTagDeferredSendTime](http://msdn.microsoft.com/en-us/library/cc840017.aspx) (0x3FEF0040) property, and the [SendAndSaveCopy](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.sendandsavecopy%28v=exchg.80%29.aspx) method to send a delayed message and save the message in the Sent Items folder.</span></span> 
  
<span data-ttu-id="d50bc-152">En este ejemplo se da por supuesto que **servicio** es un objeto [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) válido y que se ha autenticado el usuario a un servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="d50bc-152">This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and that the user has been authenticated to an Exchange server.</span></span> 
  
```cs
// Create a new email message. 
EmailMessage message = new EmailMessage(service);
// Specify the email recipient and subject. 
message.ToRecipients.Add("sadie@contoso.com");
message.Subject = "Delayed email";
// Identify the extended property that can be used to specify when to send the email. 
ExtendedPropertyDefinition PidTagDeferredSendTime = new ExtendedPropertyDefinition(16367, MapiPropertyType.SystemTime);
// Set the time that will be used to specify when the email is sent. 
// In this example, the email will be sent one minute after the next line executes, 
// provided that the message.SendAndSaveCopy request is processed by the server within one minute. 
string sendTime = DateTime.Now.AddMinutes(1).ToUniversalTime().ToString();
// Specify when to send the email by setting the value of the extended property. 
message.SetExtendedProperty(PidTagDeferredSendTime, sendTime);
// Specify the email body. 
StringBuilder str = new StringBuilder();
str.AppendLine("The client submitted the SendAndSaveCopy request at: " + DateTime.Now.ToUniversalTime().ToString() + ".");
str.AppendLine("The email message will be sent at: " + sendTime + ".");
message.Body = str.ToString();
Console.WriteLine("");
Console.WriteLine("The client submitted the SendAndSaveCopy request at: " + DateTime.Now.ToUniversalTime().ToString() + ".");
Console.WriteLine("The email message will be sent at: " + sendTime + ".");
// Submit the request to send the email message. 
message.SendAndSaveCopy();
```

## <a name="send-a-delayed-email-message-by-using-ews"></a><span data-ttu-id="d50bc-153">Enviar un mensaje de correo electrónico retrasada mediante el uso de EWS</span><span class="sxs-lookup"><span data-stu-id="d50bc-153">Send a delayed email message by using EWS</span></span>
<span data-ttu-id="d50bc-154"><a name="bk_senddelayedews"> </a></span><span class="sxs-lookup"><span data-stu-id="d50bc-154"></span></span>

<span data-ttu-id="d50bc-155">En el ejemplo de código siguiente se muestra cómo usar la operación [CreateItem](http://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) con un valor de **MessageDisposition** de **SendAndSaveCopy** para crear un mensaje de correo electrónico, el elemento [ExtendedProperty](http://msdn.microsoft.com/library/f9701409-b620-4afe-b9ee-4c1e95507af7%28Office.15%29.aspx) para crear una definición de propiedad para el [ PidTagDeferredSendTime](http://msdn.microsoft.com/en-us/library/cc840017.aspx) (0x3FEF0040) (propiedad) para establecer una hora para enviar el mensaje y el elemento [SavedItemFolderId](http://msdn.microsoft.com/library/4b8b475c-9ca5-48c9-acb0-8848b53be1ce%28Office.15%29.aspx) para guardar el mensaje enviado en la carpeta Elementos enviados.</span><span class="sxs-lookup"><span data-stu-id="d50bc-155">The following code example shows how to use the [CreateItem](http://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) operation with a **MessageDisposition** value of **SendAndSaveCopy** to create an email message, the [ExtendedProperty](http://msdn.microsoft.com/library/f9701409-b620-4afe-b9ee-4c1e95507af7%28Office.15%29.aspx) element to create a property definition for the [PidTagDeferredSendTime](http://msdn.microsoft.com/en-us/library/cc840017.aspx) (0x3FEF0040) property to set a time to send the message, and the [SavedItemFolderId](http://msdn.microsoft.com/library/4b8b475c-9ca5-48c9-acb0-8848b53be1ce%28Office.15%29.aspx) element to save the sent message in the Sent Items folder.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange207_SP1" />
  </soap:Header>
  <soap:Body>
    <m:CreateItem MessageDisposition="SendAndSaveCopy">
      <m:SavedItemFolderId>
        <t:DistinguishedFolderId Id="sentitems" />
      </m:SavedItemFolderId>
      <m:Items>
        <t:Message>
          <t:Subject>Delayed email</t:Subject>
          <t:Body BodyType="HTML">
            The client submitted the SendAndSaveCopy request at: 1/2/2014 9:08:52 PM.
            The email message will be sent at: 1/2/2014 9:09:52 PM.
          </t:Body>
          <t:ExtendedProperty>
            <t:ExtendedFieldURI PropertyTag="16367"
                                PropertyType="SystemTime" />
            <t:Value>2014-01-02T21:09:52.000</t:Value>
          </t:ExtendedProperty>
          <t:ToRecipients>
            <t:Mailbox>
              <t:EmailAddress>sadie@contoso.com</t:EmailAddress>
            </t:Mailbox>
          </t:ToRecipients>
        </t:Message>
      </m:Items>
    </m:CreateItem>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="d50bc-156">El servidor responde a la solicitud **CreateItem** con un mensaje de [CreateItemResponse](http://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) que incluye un valor [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) **NoError**, lo que indica que el correo electrónico se ha creado correctamente y la [ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) de la recientemente mensaje de creación.</span><span class="sxs-lookup"><span data-stu-id="d50bc-156">The server responds to the **CreateItem** request with a [CreateItemResponse](http://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) value of **NoError**, which indicates that the email was created successfully, and the [ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) of the newly created message.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d50bc-157">Vea también</span><span class="sxs-lookup"><span data-stu-id="d50bc-157">See also</span></span>


- [<span data-ttu-id="d50bc-158">Correo electrónico y EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="d50bc-158">Email and EWS in Exchange</span></span>](email-and-ews-in-exchange.md)
    
- [<span data-ttu-id="d50bc-159">Responder a mensajes de correo electrónico mediante el uso de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="d50bc-159">Respond to email messages by using EWS in Exchange</span></span>](how-to-respond-to-email-messages-by-using-ews-in-exchange.md)
    

