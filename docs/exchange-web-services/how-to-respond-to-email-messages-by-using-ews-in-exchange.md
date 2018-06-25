---
title: Responder a mensajes de correo electrónico mediante el uso de EWS en Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9d584991-4d67-4d36-ae2f-99970af8488f
description: Obtenga información sobre cómo responder a mensajes de correo electrónico mediante el uso de la API administrada de EWS o EWS en Exchange.
ms.openlocfilehash: 2f1428251084a7f2bf8d589a788c143f34b64d5c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763168"
---
# <a name="respond-to-email-messages-by-using-ews-in-exchange"></a><span data-ttu-id="09aa2-103">Responder a mensajes de correo electrónico mediante el uso de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="09aa2-103">Respond to email messages by using EWS in Exchange</span></span>

<span data-ttu-id="09aa2-104">Obtenga información sobre cómo responder a mensajes de correo electrónico mediante el uso de la API administrada de EWS o EWS en Exchange.</span><span class="sxs-lookup"><span data-stu-id="09aa2-104">Learn how to respond to email messages by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="09aa2-105">Puede usar la API administrada de EWS o EWS para responder a los mensajes, responder a ellos o reenviarlos a los destinatarios.</span><span class="sxs-lookup"><span data-stu-id="09aa2-105">You can use the EWS Managed API or EWS to respond to messages by replying to them or forwarding them to recipients.</span></span>
  
<span data-ttu-id="09aa2-106">**La tabla 1. Métodos de la API administrada de EWS y las operaciones de EWS para responder a mensajes de correo electrónico**</span><span class="sxs-lookup"><span data-stu-id="09aa2-106">**Table 1. EWS Managed API methods and EWS operations for responding to email messages**</span></span>

|<span data-ttu-id="09aa2-107">**Tarea**</span><span class="sxs-lookup"><span data-stu-id="09aa2-107">**Task**</span></span>|<span data-ttu-id="09aa2-108">**Método de la API administrada de EWS**</span><span class="sxs-lookup"><span data-stu-id="09aa2-108">**EWS Managed API method**</span></span>|<span data-ttu-id="09aa2-109">**Operación de EWS**</span><span class="sxs-lookup"><span data-stu-id="09aa2-109">**EWS operation**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="09aa2-110">Responder a un mensaje de correo electrónico</span><span class="sxs-lookup"><span data-stu-id="09aa2-110">Reply to an email message</span></span>  <br/> |[<span data-ttu-id="09aa2-111">EmailMessage.Reply</span><span class="sxs-lookup"><span data-stu-id="09aa2-111">EmailMessage.Reply</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.reply%28v=exchg.80%29.aspx) <br/> [<span data-ttu-id="09aa2-112">EmailMessage.CreateReply</span><span class="sxs-lookup"><span data-stu-id="09aa2-112">EmailMessage.CreateReply</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.createreply%28v=exchg.80%29.aspx) <br/> |<span data-ttu-id="09aa2-113">[CreateItem](http://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx), donde el elemento de [elementos](http://msdn.microsoft.com/library/d61ef1cc-ddfc-480a-9625-7b436cb33ae0%28Office.15%29.aspx) tiene un elemento secundario de [ReplyToItem](http://msdn.microsoft.com/library/35ee751a-41c0-4216-ad8b-78f7ada43a2f%28Office.15%29.aspx) o [ReplyAllToItem](http://msdn.microsoft.com/library/8ca970ca-ca73-40db-9233-7b271cc5f44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="09aa2-113">[CreateItem](http://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx), where the [Items](http://msdn.microsoft.com/library/d61ef1cc-ddfc-480a-9625-7b436cb33ae0%28Office.15%29.aspx) element has a child element of either [ReplyToItem](http://msdn.microsoft.com/library/35ee751a-41c0-4216-ad8b-78f7ada43a2f%28Office.15%29.aspx) or [ReplyAllToItem](http://msdn.microsoft.com/library/8ca970ca-ca73-40db-9233-7b271cc5f44f%28Office.15%29.aspx).</span></span>  <br/> |
|<span data-ttu-id="09aa2-114">Reenviar un mensaje de correo electrónico</span><span class="sxs-lookup"><span data-stu-id="09aa2-114">Forward an email message</span></span>  <br/> |[<span data-ttu-id="09aa2-115">EmailMessage.Forward</span><span class="sxs-lookup"><span data-stu-id="09aa2-115">EmailMessage.Forward</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.forward%28v=exchg.80%29.aspx) <br/> [<span data-ttu-id="09aa2-116">EmailMessage.CreateForward</span><span class="sxs-lookup"><span data-stu-id="09aa2-116">EmailMessage.CreateForward</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.createforward%28v=exchg.80%29.aspx) <br/> |<span data-ttu-id="09aa2-117">[CreateItem](http://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx), donde el elemento de [elementos](http://msdn.microsoft.com/library/d61ef1cc-ddfc-480a-9625-7b436cb33ae0%28Office.15%29.aspx) tiene un elemento secundario de [ForwardItem](http://msdn.microsoft.com/library/97786086-8b91-4471-8af8-d21e8d66de87%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="09aa2-117">[CreateItem](http://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx), where the [Items](http://msdn.microsoft.com/library/d61ef1cc-ddfc-480a-9625-7b436cb33ae0%28Office.15%29.aspx) element has a child element of [ForwardItem](http://msdn.microsoft.com/library/97786086-8b91-4471-8af8-d21e8d66de87%28Office.15%29.aspx).</span></span>  <br/> |
   
## <a name="reply-to-an-email-message-by-using-the-ews-managed-api"></a><span data-ttu-id="09aa2-118">Responder a un mensaje de correo electrónico mediante el uso de la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="09aa2-118">Reply to an email message by using the EWS Managed API</span></span>
<span data-ttu-id="09aa2-119"><a name="bk_replyewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="09aa2-119"></span></span>

<span data-ttu-id="09aa2-120">La API administrada de EWS proporciona dos métodos que puede usar para responder a mensajes: [respuesta](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.reply%28v=exchg.80%29.aspx) y [CreateReply](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.createreply%28v=exchg.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="09aa2-120">The EWS Managed API provides two methods that you can use to respond to messages: [Reply](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.reply%28v=exchg.80%29.aspx) and [CreateReply](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.createreply%28v=exchg.80%29.aspx).</span></span> <span data-ttu-id="09aa2-121">El método de **respuesta** sólo toma dos parámetros: el mensaje de respuesta a anteponga el cuerpo existente y un valor **booleano** que indica si la respuesta debe ir a todos los destinatarios (true) o sólo el remitente (false).</span><span class="sxs-lookup"><span data-stu-id="09aa2-121">The **Reply** method only takes two parameters: the response message to prepend to the existing body, and a **Boolean** value that indicates whether the response should go to all recipients (true) or just the sender (false).</span></span> <span data-ttu-id="09aa2-122">Si necesita agregar destinatarios adicionales a un mensaje, establecer propiedades adicionales en una respuesta o agregar datos adjuntos, utilice el método **CreateReply** , que le permite establecer todas las [Propiedades de primera clase](email-properties-and-elements-in-ews-in-exchange.md) que están disponibles en un [EmailMessage ](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx)objeto.</span><span class="sxs-lookup"><span data-stu-id="09aa2-122">If you need to add additional recipients to a message, set additional properties on a response, or add an attachment, use the **CreateReply** method, which enables you to set all the [first-class properties](email-properties-and-elements-in-ews-in-exchange.md) that are available on an [EmailMessage](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx) object.</span></span> 
  
<span data-ttu-id="09aa2-123">En el ejemplo de código siguiente se muestra cómo utilizar el método **Reply** para responder a un mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="09aa2-123">The following code example shows how to use the **Reply** method to respond to an email message.</span></span> 
  
<span data-ttu-id="09aa2-124">En este ejemplo se da por supuesto que **servicio** es un objeto [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) válido y que se ha autenticado el usuario a un servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="09aa2-124">This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and that the user has been authenticated to an Exchange server.</span></span> <span data-ttu-id="09aa2-125">La variable local *ItemId* es el [identificador](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) del elemento para responder a.</span><span class="sxs-lookup"><span data-stu-id="09aa2-125">The local variable  *ItemId*  is the [Id](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) of the item to respond to.</span></span> <span data-ttu-id="09aa2-126">En el ejemplo se llama al [método FindRecentlySent](#bk_findlast) para comprobar que el mensaje se marcó como respondió a.</span><span class="sxs-lookup"><span data-stu-id="09aa2-126">The example calls the [FindRecentlySent method](#bk_findlast) to verify that the message was marked as replied to.</span></span> 
  
```cs
// As a best practice, limit the properties returned by the Bind method to only those that are required.
PropertySet propSet = new PropertySet(BasePropertySet.IdOnly, ItemSchema.LastModifiedTime);
// Bind to the email message to reply to by using the ItemId.
// This method call results in a GetItem call to EWS.
EmailMessage message = EmailMessage.Bind(service, ItemId, propSet);
string myReply = "This is the message body of the email reply.";
bool replyToAll = false;
// Send the response message.
// This method call results in a CreateItem call to EWS.
message.Reply(myReply, replyToAll);
// Verify that the response was sent by calling FindRecentlySent.
FindRecentlySent(message);
```

<span data-ttu-id="09aa2-127">En el ejemplo de código siguiente se muestra cómo utilizar el método **CreateReply** para responder a un mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="09aa2-127">The following code example shows how to use the **CreateReply** method to respond to an email message.</span></span> 
  
```cs
// Bind to the email message to reply to by using the ItemId.
// This method call results in a GetItem call to EWS.
EmailMessage message = EmailMessage.Bind(service, ItemId, BasePropertySet.IdOnly);
// Create the reply response message from the original email message.
// Indicate whether the message is a reply or reply all type of reply.
bool replyToAll = true;
ResponseMessage responseMessage = message.CreateReply(replyToAll);
// Prepend the reply to the message body. 
string myReply = "This is the message body of the email reply.";
responseMessage.BodyPrefix = myReply;
// Send the response message.
// This method call results in a CreateItem call to EWS.
responseMessage.SendAndSaveCopy();
// Check that the response was sent by calling FindRecentlySent.
FindRecentlySent(message);
```

<span data-ttu-id="09aa2-128">Si necesita agregar datos adjuntos al mensaje de respuesta, reemplace la llamada al método **SendAndSaveCopy** con el siguiente código.</span><span class="sxs-lookup"><span data-stu-id="09aa2-128">If you need to add an attachment to the response message, replace the call to the **SendAndSaveCopy** method with the following code.</span></span> 
  
```cs
EmailMessage reply = responseMessage.Save();
reply.Attachments.AddFileAttachment("attachmentname.txt");
reply.Update(ConflictResolutionMode.AutoResolve);
reply.SendAndSaveCopy();
```

## <a name="reply-to-an-email-message-by-using-ews"></a><span data-ttu-id="09aa2-129">Responder a un mensaje de correo electrónico mediante el uso de EWS</span><span class="sxs-lookup"><span data-stu-id="09aa2-129">Reply to an email message by using EWS</span></span>
<span data-ttu-id="09aa2-130"><a name="bk_replyews"> </a></span><span class="sxs-lookup"><span data-stu-id="09aa2-130"></span></span>

<span data-ttu-id="09aa2-131">En el ejemplo de código siguiente se muestra cómo responder a un mensaje mediante el uso de EWS.</span><span class="sxs-lookup"><span data-stu-id="09aa2-131">The following code example shows how to reply to a message by using EWS.</span></span> <span data-ttu-id="09aa2-132">Use la operación [CreateItem](http://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) con el atributo **MessageDisposition** establecido en **SendAndSaveCopy** para enviar el mensaje y guardar la respuesta en la carpeta Elementos enviados.</span><span class="sxs-lookup"><span data-stu-id="09aa2-132">Use the [CreateItem](http://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) operation with the **MessageDisposition** attribute set to **SendAndSaveCopy** to send the message and save the response in the Sent Items folder.</span></span> <span data-ttu-id="09aa2-133">Incluir el elemento de [ReplyAllToItem](http://msdn.microsoft.com/library/8ca970ca-ca73-40db-9233-7b271cc5f44f%28Office.15%29.aspx) como un elemento secundario del elemento de [elementos](http://msdn.microsoft.com/library/d61ef1cc-ddfc-480a-9625-7b436cb33ae0%28Office.15%29.aspx) para responder a todos los usuarios en el subproceso de mensaje o incluir el elemento [ReplyToItem](http://msdn.microsoft.com/library/35ee751a-41c0-4216-ad8b-78f7ada43a2f%28Office.15%29.aspx) para responder sólo al remitente.</span><span class="sxs-lookup"><span data-stu-id="09aa2-133">Include either the [ReplyAllToItem](http://msdn.microsoft.com/library/8ca970ca-ca73-40db-9233-7b271cc5f44f%28Office.15%29.aspx) element as a child of the [Items](http://msdn.microsoft.com/library/d61ef1cc-ddfc-480a-9625-7b436cb33ae0%28Office.15%29.aspx) element to reply to everyone on the message thread, or include the [ReplyToItem](http://msdn.microsoft.com/library/35ee751a-41c0-4216-ad8b-78f7ada43a2f%28Office.15%29.aspx) element to reply only to the sender.</span></span> 
  
<span data-ttu-id="09aa2-134">También es la solicitud XML que la API administrada de EWS envía al llamar a la [respuesta](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.reply%28v=exchg.80%29.aspx) o el método [CreateReply](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.createreply%28v=exchg.80%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="09aa2-134">This is also the XML request that the EWS Managed API sends when calling either the [Reply](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.reply%28v=exchg.80%29.aspx) or the [CreateReply](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.createreply%28v=exchg.80%29.aspx) method.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version=" Exchange2007_SP1" />
  </soap:Header>
  <soap:Body>
    <m:CreateItem MessageDisposition="SendAndSaveCopy">
      <m:Items>
        <t:ReplyAllToItem>
          <t:ReferenceItemId Id="AAMkADE4="
                             ChangeKey="CQAAABYA" />
          <t:NewBodyContent BodyType="HTML">This is the message body of the email reply.</t:NewBodyContent>
        </t:ReplyAllToItem>
      </m:Items>
    </m:CreateItem>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="09aa2-135">El servidor responde a la solicitud **CreateItem** con un mensaje de [CreateItemResponse](http://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) que incluye un valor de elemento [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) de **NoError**, lo que indica que la respuesta se ha creado y se ha enviado correctamente.</span><span class="sxs-lookup"><span data-stu-id="09aa2-135">The server responds to the **CreateItem** request with a [CreateItemResponse](http://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) element value of **NoError**, which indicates that the reply was created and sent successfully.</span></span>
  
<span data-ttu-id="09aa2-136">Si necesita agregar datos adjuntos al mensaje de respuesta, llamar a la operación **CreateItem** anteriormente especificados, pero cambie el **MessageDisposition** a **SaveOnly**.</span><span class="sxs-lookup"><span data-stu-id="09aa2-136">If you need to add an attachment to your response message, call the **CreateItem** operation as specified above, but change the **MessageDisposition** to **SaveOnly**.</span></span> <span data-ttu-id="09aa2-137">A continuación, llame a la operación [CreateAttachment](http://msdn.microsoft.com/library/e066db95-6963-4507-a8d0-8efad287f550%28Office.15%29.aspx) , seguida de la operación de [SendItem](http://msdn.microsoft.com/library/337b89ef-e1b7-45ed-92f3-8abe4200e4c7%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="09aa2-137">Then call the [CreateAttachment](http://msdn.microsoft.com/library/e066db95-6963-4507-a8d0-8efad287f550%28Office.15%29.aspx) operation, followed by the [SendItem](http://msdn.microsoft.com/library/337b89ef-e1b7-45ed-92f3-8abe4200e4c7%28Office.15%29.aspx) operation.</span></span> 
  
## <a name="forward-an-email-message-by-using-the-ews-managed-api"></a><span data-ttu-id="09aa2-138">Reenviar un mensaje de correo electrónico mediante el uso de la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="09aa2-138">Forward an email message by using the EWS Managed API</span></span>
<span data-ttu-id="09aa2-139"><a name="bk_forwardewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="09aa2-139"></span></span>

<span data-ttu-id="09aa2-140">La API administrada de EWS proporciona dos métodos que puede usar para reenviar los mensajes: [hacia delante](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.forward%28v=exchg.80%29.aspx) y [CreateForward](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.createforward%28v=exchg.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="09aa2-140">The EWS Managed API provides two methods that you can use to forward messages: [Forward](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.forward%28v=exchg.80%29.aspx) and [CreateForward](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.createforward%28v=exchg.80%29.aspx).</span></span> <span data-ttu-id="09aa2-141">El método **desviar** sólo toma dos parámetros: el mensaje anteponer para el cuerpo existente y una matriz o colección de destinatarios, dependiendo de la sobrecarga que desee utilizar.</span><span class="sxs-lookup"><span data-stu-id="09aa2-141">The **Forward** method only takes two parameters: the message to prepend to the existing body, and an array or collection of recipients, depending on the overload you choose to use.</span></span> <span data-ttu-id="09aa2-142">Si necesita agregar datos adjuntos al mensaje está reenvío o establecer propiedades adicionales en el nuevo mensaje, utilice el método **CreateForward** , que le permite establecer todas las propiedades que están disponibles en un objeto [EmailMessage](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="09aa2-142">If you need to add an attachment to the message you're forwarding, or set additional properties on the new message, use the **CreateForward** method, which enables you to set all the properties that are available on an [EmailMessage](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx) object.</span></span> 
  
<span data-ttu-id="09aa2-143">En el ejemplo de código siguiente se muestra cómo usar el método **Forward** para reenviar un mensaje de correo electrónico a un destinatario.</span><span class="sxs-lookup"><span data-stu-id="09aa2-143">The following code example shows how to use the **Forward** method to forward an email message to one recipient.</span></span> 
  
<span data-ttu-id="09aa2-144">En este ejemplo se da por supuesto que **servicio** es un objeto [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) válido y que se ha autenticado el usuario a un servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="09aa2-144">This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and that the user has been authenticated to an Exchange server.</span></span> <span data-ttu-id="09aa2-145">La variable local *ItemId* es el [identificador](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) del elemento para reenviar.</span><span class="sxs-lookup"><span data-stu-id="09aa2-145">The local variable  *ItemId*  is the [Id](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) of the item to forward.</span></span> <span data-ttu-id="09aa2-146">En el ejemplo se llama al [método FindRecentlySent](#bk_findlast) para comprobar que el mensaje se marcó como reenviar.</span><span class="sxs-lookup"><span data-stu-id="09aa2-146">The example calls the [FindRecentlySent method](#bk_findlast) to verify that the message was marked as forwarded.</span></span> 
  
```cs
// Bind to the email message to reply to by using the ItemId.
// This method call results in a GetItem call to EWS.
EmailMessage message = EmailMessage.Bind(service, ItemId, BasePropertySet.IdOnly);
string myForward = "This is the message body of the forwarded email.";
// Send the response message.
// This method call results in a CreateItem call to EWS.
message.Forward(myForward, "sadie@contoso.com");
// Verify that the forwarded response was sent by calling FindRecentlySent.
FindRecentlySent(message);
```

<span data-ttu-id="09aa2-147">En el ejemplo de código siguiente se muestra cómo utilizar el método **CreateForward** para reenviar un mensaje de correo electrónico a un destinatario.</span><span class="sxs-lookup"><span data-stu-id="09aa2-147">The following code example shows how to use the **CreateForward** method to forward an email message to one recipient.</span></span> 
  
```cs
// Bind to the email message to reply to by using the ItemId.
// This method call results in a GetItem call to EWS.
EmailMessage message = EmailMessage.Bind(service, ItemId, BasePropertySet.IdOnly);
// Create the reply response message from the original email message.
// Indicate whether the message is a reply or reply all type of reply.
ResponseMessage forwardMessage = message.CreateForward();
// Set properties on the email message.
forwardMessage.ToRecipients.Add("sadie@contoso.com");
forwardMessage.Body = "Sadie,<br><br>I thought you'd be interested in this thread.<br><br>-Mack";
// Send and save a copy of the replied email message in the default Sent Items folder. 
forwardMessage.SendAndSaveCopy();
// Verify that the forwarded message was sent by calling FindRecentlySent.
FindRecentlySent(message);
```

<span data-ttu-id="09aa2-148">Si necesita agregar datos adjuntos al mensaje reenviado, reemplace la llamada al método **SendAndSaveCopy** con el siguiente código.</span><span class="sxs-lookup"><span data-stu-id="09aa2-148">If you need to add an attachment to the forwarded message, replace the call to the **SendAndSaveCopy** method with the following code.</span></span> 
  
```cs
EmailMessage forward = forwardMessage.Save();
forward.Attachments.AddFileAttachment("attachmentname.txt");
forward.Update(ConflictResolutionMode.AutoResolve);
forward.SendAndSaveCopy();
```

## <a name="forward-an-email-message-by-using-ews"></a><span data-ttu-id="09aa2-149">Reenviar un mensaje de correo electrónico mediante el uso de EWS</span><span class="sxs-lookup"><span data-stu-id="09aa2-149">Forward an email message by using EWS</span></span>
<span data-ttu-id="09aa2-150"><a name="bk_forwardews"> </a></span><span class="sxs-lookup"><span data-stu-id="09aa2-150"></span></span>

<span data-ttu-id="09aa2-151">En el ejemplo de código siguiente se muestra cómo reenviar un mensaje mediante el uso de EWS.</span><span class="sxs-lookup"><span data-stu-id="09aa2-151">The following code example shows how to forward a message by using EWS.</span></span> <span data-ttu-id="09aa2-152">Use la operación [CreateItem](http://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) con el atributo **MessageDisposition** establecido en **SendAndSaveCopy** para enviar el mensaje y guardar la respuesta en la carpeta Elementos enviados.</span><span class="sxs-lookup"><span data-stu-id="09aa2-152">Use the [CreateItem](http://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) operation with the **MessageDisposition** attribute set to **SendAndSaveCopy** to send the message and save the response in the Sent Items folder.</span></span> <span data-ttu-id="09aa2-153">El elemento [ForwardItem](http://msdn.microsoft.com/library/97786086-8b91-4471-8af8-d21e8d66de87%28Office.15%29.aspx) indica que el elemento es un mensaje reenviado.</span><span class="sxs-lookup"><span data-stu-id="09aa2-153">The [ForwardItem](http://msdn.microsoft.com/library/97786086-8b91-4471-8af8-d21e8d66de87%28Office.15%29.aspx) element indicates that the item is a forwarded message.</span></span> 
  
<span data-ttu-id="09aa2-154">También es la solicitud XML que la API administrada de EWS envía al llamar a la [hacia delante](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.forward%28v=exchg.80%29.aspx) o el método [CreateForward](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.createforward%28v=exchg.80%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="09aa2-154">This is also the XML request that the EWS Managed API sends when calling either the [Forward](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.forward%28v=exchg.80%29.aspx) or the [CreateForward](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.createforward%28v=exchg.80%29.aspx) method.</span></span> 
  
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
      <m:Items>
        <t:ForwardItem>
          <t:ToRecipients>
            <t:Mailbox>
              <t:EmailAddress>sadie@contoso.com</t:EmailAddress>
            </t:Mailbox>
          </t:ToRecipients>
          <t:ReferenceItemId Id="AAAMkADE="
                             ChangeKey="CQAAABYA" />
          <t:NewBodyContent BodyType="HTML">This is the message body of the forwarded email.</t:NewBodyContent>
        </t:ForwardItem>
      </m:Items>
    </m:CreateItem>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="09aa2-155">El servidor responde a la solicitud **CreateItem** con un mensaje de [CreateItemResponse](http://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) que incluye un valor de elemento [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) de **NoError**, lo que indica que se ha creado y se ha enviado correctamente el mensaje reenviado.</span><span class="sxs-lookup"><span data-stu-id="09aa2-155">The server responds to the **CreateItem** request with a [CreateItemResponse](http://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) element value of **NoError**, which indicates that the forwarded message was created and sent successfully.</span></span>
  
<span data-ttu-id="09aa2-156">Si necesita agregar datos adjuntos al mensaje de respuesta, llamar a la operación **CreateItem** , pero cambie el **MessageDisposition** a **SaveOnly**.</span><span class="sxs-lookup"><span data-stu-id="09aa2-156">If you need to add an attachment to your response message, call the **CreateItem** operation, but change the **MessageDisposition** to **SaveOnly**.</span></span> <span data-ttu-id="09aa2-157">A continuación, llame a la operación [CreateAttachment](http://msdn.microsoft.com/library/e066db95-6963-4507-a8d0-8efad287f550%28Office.15%29.aspx) , seguida de la operación de [SendItem](http://msdn.microsoft.com/library/337b89ef-e1b7-45ed-92f3-8abe4200e4c7%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="09aa2-157">Then call the [CreateAttachment](http://msdn.microsoft.com/library/e066db95-6963-4507-a8d0-8efad287f550%28Office.15%29.aspx) operation, followed by the [SendItem](http://msdn.microsoft.com/library/337b89ef-e1b7-45ed-92f3-8abe4200e4c7%28Office.15%29.aspx) operation.</span></span> 
  
## <a name="find-the-message-last-replied-to-or-forwarded-by-using-the-ews-managed-api"></a><span data-ttu-id="09aa2-158">Busque el mensaje por última vez respondió o reenvió mediante el uso de la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="09aa2-158">Find the message last replied to or forwarded by using the EWS Managed API</span></span>
<span data-ttu-id="09aa2-159"><a name="bk_findlast"> </a></span><span class="sxs-lookup"><span data-stu-id="09aa2-159"></span></span>

<span data-ttu-id="09aa2-160">En el ejemplo de código siguiente se muestra cómo buscar el último verbo que se ejecuta y el tiempo que se ha ejecutado el verbo último en el elemento especificado.</span><span class="sxs-lookup"><span data-stu-id="09aa2-160">The following code example shows how to find the last verb executed and the time the last verb was executed on the item specified.</span></span> <span data-ttu-id="09aa2-161">Se llama a este método desde otros ejemplos de código de API administrada de EWS en este tema para comprobar que los elementos respondió o reenvió se marca como respondido a o reenviados en la Bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="09aa2-161">This method is called from other EWS Managed API code examples in this topic to verify that the items you replied to or forwarded were marked as replied to or forwarded in your Inbox.</span></span> 
  
<span data-ttu-id="09aa2-162">En el ejemplo se utiliza la propiedad de [PidTagLastVerbExecuted](http://msdn.microsoft.com/en-us/library/cc841968.aspx) (0x10820003) ampliado para determinar si el mensaje fue una respuesta, un responder a todos o un reenviar y [PidTagLastVerbExecutionTime](http://msdn.microsoft.com/en-us/library/cc839918.aspx) (0x10820040) extendido (propiedad) para determinar cuándo el responder o reenviar se envió.</span><span class="sxs-lookup"><span data-stu-id="09aa2-162">The example uses the [PidTagLastVerbExecuted](http://msdn.microsoft.com/en-us/library/cc841968.aspx) (0x10820003) extended property to determine whether the message was a reply, a reply all, or a forward, and the [PidTagLastVerbExecutionTime](http://msdn.microsoft.com/en-us/library/cc839918.aspx) (0x10820040) extended property to determine when the reply or forward was sent.</span></span> 
  
```cs
public static void FindRecentlySent(EmailMessage messageToCheck)
{
    // Create extended property definitions for PidTagLastVerbExecuted and PidTagLastVerbExecutionTime.
    ExtendedPropertyDefinition PidTagLastVerbExecuted = new ExtendedPropertyDefinition(0x1081, MapiPropertyType.Integer);
    ExtendedPropertyDefinition PidTagLastVerbExecutionTime = new ExtendedPropertyDefinition(0x1082, MapiPropertyType.SystemTime);
    PropertySet propSet = new PropertySet(BasePropertySet.IdOnly, EmailMessageSchema.Subject, PidTagLastVerbExecutionTime, PidTagLastVerbExecuted);
    messageToCheck = EmailMessage.Bind(service, messageToCheck.Id, propSet);
    // Determine the last verb executed on the message and display output.
    object responseType;
    if (messageToCheck.TryGetProperty(PidTagLastVerbExecuted, out responseType))
    {
        object ReplyTime = null;
        switch (((Int32)responseType))
        {
            case 102: Console.WriteLine("A reply was sent to the '" + messageToCheck.Subject.ToString() + "' email message at");
                break;
            case 103: Console.WriteLine("A reply all was sent to the '" + messageToCheck.Subject.ToString() + "' email message at");
                break;
            case 104: Console.WriteLine("The '" + messageToCheck.Subject.ToString() + "' email message was forwarded at");
                break;
        }
        if (messageToCheck.TryGetProperty(PidTagLastVerbExecutionTime, out ReplyTime))
        {
            Console.WriteLine(((DateTime)ReplyTime).ToString() + ".");
        }
    }
    else
    {
        Console.WriteLine("No changes were made to  '" + messageToCheck.Subject.ToString() + "'.");
    }
}
```

## <a name="see-also"></a><span data-ttu-id="09aa2-163">Vea también</span><span class="sxs-lookup"><span data-stu-id="09aa2-163">See also</span></span>


- [<span data-ttu-id="09aa2-164">Correo electrónico y EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="09aa2-164">Email and EWS in Exchange</span></span>](email-and-ews-in-exchange.md)
    
- [<span data-ttu-id="09aa2-165">Enviar mensajes de correo electrónico mediante el uso de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="09aa2-165">Send email messages by using EWS in Exchange</span></span>](how-to-send-email-messages-by-using-ews-in-exchange.md)
    

