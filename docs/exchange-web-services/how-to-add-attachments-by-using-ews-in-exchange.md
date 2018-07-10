---
title: Agregar datos adjuntos mediante el uso de EWS en Exchange
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 0cbce436-2ae6-4fcc-bd8b-f517a0724e55
description: Obtenga información sobre cómo crear nuevos elementos con datos adjuntos, o agregar datos adjuntos a elementos existentes mediante la API administrada de EWS o EWS en Exchange.
ms.openlocfilehash: dbfff879c92dafeec588d79cddd92e294b763c06
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763063"
---
# <a name="add-attachments-by-using-ews-in-exchange"></a><span data-ttu-id="99039-103">Agregar datos adjuntos mediante el uso de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="99039-103">Add attachments by using EWS in Exchange</span></span>

<span data-ttu-id="99039-104">Obtenga información sobre cómo crear nuevos elementos con datos adjuntos, o agregar datos adjuntos a elementos existentes mediante la API administrada de EWS o EWS en Exchange.</span><span class="sxs-lookup"><span data-stu-id="99039-104">Learn how to create new items with attachments, or add attachments to existing items by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="99039-105">Puede agregar datos adjuntos de archivos o datos adjuntos de elemento para elementos nuevos o existentes mediante el uso de la API administrada de EWS o EWS.</span><span class="sxs-lookup"><span data-stu-id="99039-105">You can add file attachments or item attachments to new or existing items by using the EWS Managed API or EWS.</span></span> <span data-ttu-id="99039-106">Si está utilizando la API administrada de EWS, use el mismo método para agregar datos adjuntos a elementos nuevos o existentes; Sin embargo, el método cambia si está utilizando un archivo o elemento de datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="99039-106">If you are using the EWS Managed API, you use the same method to add attachments to new or existing items; however, the method changes if you're using a file or item attachment.</span></span> <span data-ttu-id="99039-107">Por el contrario, si usa EWS, use la misma operación para agregar datos adjuntos de un archivo o un elemento a un elemento, pero la operación cambia si va a agregar los datos adjuntos a un elemento nuevo o existente.</span><span class="sxs-lookup"><span data-stu-id="99039-107">Conversely, if you are using EWS, you use the same operation to add either a file or item attachment to an item, but the operation changes if you're adding the attachment to a new or existing item.</span></span>
  
<span data-ttu-id="99039-108">**La tabla 1. Métodos de la API administrada de EWS y las operaciones de EWS para agregar datos adjuntos**</span><span class="sxs-lookup"><span data-stu-id="99039-108">**Table 1. EWS Managed API methods and EWS operations for adding attachments**</span></span>

|<span data-ttu-id="99039-109">**Tarea**</span><span class="sxs-lookup"><span data-stu-id="99039-109">**Task**</span></span>|<span data-ttu-id="99039-110">**Método de la API administrada de EWS**</span><span class="sxs-lookup"><span data-stu-id="99039-110">**EWS Managed API method**</span></span>|<span data-ttu-id="99039-111">**Operación de EWS**</span><span class="sxs-lookup"><span data-stu-id="99039-111">**EWS operation**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="99039-112">Agregar un archivo adjunto a un correo electrónico nuevo o existente</span><span class="sxs-lookup"><span data-stu-id="99039-112">Add a file attachment to a new or existing email</span></span>  <br/> |[<span data-ttu-id="99039-113">AttachmentCollection.AddFileAttachment</span><span class="sxs-lookup"><span data-stu-id="99039-113">AttachmentCollection.AddFileAttachment</span></span>](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.attachmentcollection.addfileattachment%28v=exchg.80%29.aspx) <br/> |<span data-ttu-id="99039-114">[CreateItem](http://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) para un correo electrónico nuevo</span><span class="sxs-lookup"><span data-stu-id="99039-114">[CreateItem](http://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) for a new email</span></span>  <br/> <span data-ttu-id="99039-115">[CreateAttachment](http://msdn.microsoft.com/library/e066db95-6963-4507-a8d0-8efad287f550%28Office.15%29.aspx) para agregar a un correo electrónico existente</span><span class="sxs-lookup"><span data-stu-id="99039-115">[CreateAttachment](http://msdn.microsoft.com/library/e066db95-6963-4507-a8d0-8efad287f550%28Office.15%29.aspx) to add to an existing email</span></span>  <br/> |
|<span data-ttu-id="99039-116">Agregar datos adjuntos de elemento para un correo electrónico nuevo o existente</span><span class="sxs-lookup"><span data-stu-id="99039-116">Add an item attachment to a new or existing email</span></span>  <br/> |[<span data-ttu-id="99039-117">AttachmentCollection.AddItemAttachment</span><span class="sxs-lookup"><span data-stu-id="99039-117">AttachmentCollection.AddItemAttachment</span></span>](http://msdn.microsoft.com/es-es/library/dd634986%28v=exchg.80%29.aspx) <br/> |<span data-ttu-id="99039-118">[CreateItem](http://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) para un correo electrónico nuevo</span><span class="sxs-lookup"><span data-stu-id="99039-118">[CreateItem](http://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) for a new email</span></span>  <br/> <span data-ttu-id="99039-119">[CreateAttachment](http://msdn.microsoft.com/library/e066db95-6963-4507-a8d0-8efad287f550%28Office.15%29.aspx) para agregar a un correo electrónico existente</span><span class="sxs-lookup"><span data-stu-id="99039-119">[CreateAttachment](http://msdn.microsoft.com/library/e066db95-6963-4507-a8d0-8efad287f550%28Office.15%29.aspx) to add to an existing email</span></span>  <br/> |
   
## <a name="create-an-email-with-file-and-item-attachments-by-using-the-ews-managed-api"></a><span data-ttu-id="99039-120">Crear un correo electrónico con datos adjuntos de archivo y elemento mediante el uso de la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="99039-120">Create an email with file and item attachments by using the EWS Managed API</span></span>
<span data-ttu-id="99039-121"><a name="bk_createattachewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="99039-121"></span></span>

<span data-ttu-id="99039-122">En el ejemplo de código siguiente se muestra cómo crear un correo electrónico con varios datos adjuntos de archivos y datos adjuntos de elemento por:</span><span class="sxs-lookup"><span data-stu-id="99039-122">The following code example shows how to create an email with multiple file attachments and an item attachment by:</span></span> 
  
1. <span data-ttu-id="99039-123">Uso del objeto [EmailMessage](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx) para crear un mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="99039-123">Using the [EmailMessage](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx) object to create an email message.</span></span> 
    
2. <span data-ttu-id="99039-124">Uso de los métodos [AttachmentCollection.AddFileAttachment](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.attachmentcollection.addfileattachment%28v=exchg.80%29.aspx) y [AttachmentCollection.AddItemAttachment](http://msdn.microsoft.com/es-es/library/dd634986%28v=exchg.80%29.aspx) para agregar datos adjuntos al mensaje.</span><span class="sxs-lookup"><span data-stu-id="99039-124">Using the [AttachmentCollection.AddFileAttachment](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.attachmentcollection.addfileattachment%28v=exchg.80%29.aspx) and [AttachmentCollection.AddItemAttachment](http://msdn.microsoft.com/es-es/library/dd634986%28v=exchg.80%29.aspx) methods to add attachments to the message.</span></span> 
    
3. <span data-ttu-id="99039-125">Con el método [EmailMessage.SendAndSaveCopy](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.emailmessage.sendandsavecopy%28v=exchg.80%29.aspx) para enviar el mensaje a los destinatarios y guardar el mensaje en la carpeta Elementos enviados.</span><span class="sxs-lookup"><span data-stu-id="99039-125">Using the [EmailMessage.SendAndSaveCopy](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.emailmessage.sendandsavecopy%28v=exchg.80%29.aspx) method to send the message to the recipients and save the message in the Sent Items folder.</span></span> 
    
<span data-ttu-id="99039-126">Este ejemplo de código muestra las cuatro maneras en que puede agregarse un archivo adjunto a un elemento mediante el uso de la API administrada de EWS:</span><span class="sxs-lookup"><span data-stu-id="99039-126">This code example shows the four ways in which a file attachment can be added to an item by using the EWS Managed API:</span></span>
  
- <span data-ttu-id="99039-127">Mediante el uso de una ubicación de archivo completo.</span><span class="sxs-lookup"><span data-stu-id="99039-127">By using a fully qualified file location.</span></span>
    
- <span data-ttu-id="99039-128">Mediante el uso de una ubicación de archivo completo y un nuevo nombre de datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="99039-128">By using a fully qualified file location and a new attachment name.</span></span>
    
- <span data-ttu-id="99039-129">Mediante el uso de una matriz de bytes.</span><span class="sxs-lookup"><span data-stu-id="99039-129">By using a byte array.</span></span>
    
- <span data-ttu-id="99039-130">Mediante el uso de una secuencia.</span><span class="sxs-lookup"><span data-stu-id="99039-130">By using a stream.</span></span>
    
<span data-ttu-id="99039-131">Tenga en cuenta que los datos adjuntos del elemento en este ejemplo se crean al mismo tiempo que el mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="99039-131">Note that the item attachment in this example is created at the same time as the email message.</span></span> <span data-ttu-id="99039-132">Para agregar un mensaje de correo electrónico existente como datos adjuntos de elemento, vea [Agregar un elemento existente a una nueva dirección de correo mediante el uso de la MimeContent y la API administrada de EWS](#bk_addexistingemailewsma).</span><span class="sxs-lookup"><span data-stu-id="99039-132">To add an existing email message as an item attachment, see [Add an existing item to a new email by using the MimeContent and the EWS Managed API](#bk_addexistingemailewsma).</span></span>
  
<span data-ttu-id="99039-133">En este ejemplo se da por supuesto que **servicio** es un objeto [ExchangeService](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) válido y que se ha autenticado el usuario a un servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="99039-133">This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and that the user has been authenticated to an Exchange server.</span></span> 
  
```cs
public static void CreateEmailWithAttachments(ExchangeService service)
{
    // Create an email message and set properties on the message.
    EmailMessage message = new EmailMessage(service);
    // Set properties on the email message.
    message.Subject = "Message with Attachments";
    message.Body = "This message contains four file attachments 
        and one message item attachment.";
    message.ToRecipients.Add("sadie@contoso.com");
    message.ToRecipients.Add("ronnie@contoso.com");
    // Add a file attachment by using the fully qualified location of the file. 
    message.Attachments.AddFileAttachment("C:\\temp\\FileAttachment.txt");
    // Add a file attachment by using the fully qualified string name, 
    // and specify the name of the attachment as it will appear in the email.
    // The new name of the file attachment is SecondAttachment.txt.
    message.Attachments.AddFileAttachment("SecondAttachment.txt", "C:\\temp\\FileAttachment2.txt");
    // Add a file attachment by using a byte array.
    // In this example, theBytes is the byte array that represents the content of the image file to attach.
    byte[] theBytes = File.ReadAllBytes("C:\\Temp\\Tulips.jpg");
    // The byte array file attachment is named ThirdAttachment.jpg.
    message.Attachments.AddFileAttachment("ThirdAttachment.jpg", theBytes);
    // Add a file attachment by using a stream.
    FileStream theStream = new FileStream("C:\\temp\\FileAttachment4.txt", FileMode.OpenOrCreate);
    // The streamed file attachment is named FourthAttachment.txt.
    message.Attachments.AddFileAttachment("FourthAttachment.txt", theStream);
    // Add an email message as an item attachment and set properties on the item.
    ItemAttachment<EmailMessage> itemAttachment = message.Attachments.AddItemAttachment<EmailMessage>();
    itemAttachment.Name = "Attached Message Item";
    itemAttachment.Item.Subject = "Message Item Subject";
    itemAttachment.Item.Body = "Message Item Body";
    itemAttachment.Item.ToRecipients.Add("sadie@contoso.com");
    itemAttachment.Item.ToRecipients.Add("ronnie@contoso.com");
    // Send the mail and save a copy in the Sent Items folder.
    // This method results in a CreateItem and SendItem call to EWS.
    message.SendAndSaveCopy();
}
```

## <a name="create-an-email-with-file-and-item-attachments-by-using-ews"></a><span data-ttu-id="99039-134">Crear un correo electrónico con datos adjuntos de archivo y elemento mediante el uso de EWS</span><span class="sxs-lookup"><span data-stu-id="99039-134">Create an email with file and item attachments by using EWS</span></span>
<span data-ttu-id="99039-135"><a name="bk_createattachews"> </a></span><span class="sxs-lookup"><span data-stu-id="99039-135"></span></span>

<span data-ttu-id="99039-136">En el ejemplo de código siguiente se muestra cómo usar la operación [CreateItem](http://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) para crear un mensaje de correo electrónico con cuatro archivos adjuntos y los datos adjuntos de un elemento.</span><span class="sxs-lookup"><span data-stu-id="99039-136">The following code example shows how to use the [CreateItem](http://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) operation to create an email message with four file attachments and one item attachment.</span></span> <span data-ttu-id="99039-137">Esto también es una de las solicitudes XML que se envía la API administrada de EWS cuándo [crear un correo electrónico con datos adjuntos de archivo y elemento](#bk_createattachewsma).</span><span class="sxs-lookup"><span data-stu-id="99039-137">This is also one of the XML requests that the EWS Managed API sends when you [create an email with file and item attachments](#bk_createattachewsma).</span></span>
  
<span data-ttu-id="99039-138">Tenga en cuenta que los datos adjuntos del elemento en este ejemplo se crean al mismo tiempo que el mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="99039-138">Note that the item attachment in this example is created at the same time as the email message.</span></span> <span data-ttu-id="99039-139">Para agregar un mensaje de correo electrónico existente como datos adjuntos de elemento, vea [Agregar un elemento existente a una nueva dirección de correo mediante el uso de la MimeContent y la API administrada de EWS](#bk_addexistingemailewsma).</span><span class="sxs-lookup"><span data-stu-id="99039-139">To add an existing email message as an item attachment, see [Add an existing item to a new email by using the MimeContent and the EWS Managed API](#bk_addexistingemailewsma).</span></span>
  
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
      <m:Items>
        <t:Message>
          <t:Subject>Message with Attachments</t:Subject>
          <t:Body BodyType="HTML">This message contains four file attachments 
              and one message item attachment.</t:Body>
          <t:Attachments>
            <t:FileAttachment>
              <t:Name>FileAttachment.txt</t:Name>
              <t:IsInline>false</t:IsInline>
              <t:IsContactPhoto>false</t:IsContactPhoto>
              <t:Content>VGhpcyBpcyBhIGZpbGUgYXR0YWNobWVudC4=</t:Content>
            </t:FileAttachment>
            <t:FileAttachment>
              <t:Name>SecondAttachment.txt</t:Name>
              <t:IsInline>false</t:IsInline>
              <t:IsContactPhoto>false</t:IsContactPhoto>
              <t:Content>VGhpcyBpcyB0aGUgc2Vjb25kIGZpbGUgYXR0YWNobWVudC4=</t:Content>
            </t:FileAttachment>
            <t:FileAttachment>
              <t:Name>ThirdAttachment.jpg</t:Name>
              <t:IsInline>false</t:IsInline>
              <t:IsContactPhoto>false</t:IsContactPhoto>
              <t:Content>nAoAXNIZMVEZs5GKhdzRcLH/9k=</t:Content>
            </t:FileAttachment>
            <t:FileAttachment>
              <t:Name>FourthAttachment.txt</t:Name>
              <t:IsInline>false</t:IsInline>
              <t:IsContactPhoto>false</t:IsContactPhoto>
              <t:Content>obWVudC4=…</t:Content>
            </t:FileAttachment>
            <t:ItemAttachment>
              <t:Name>Attached Message Item</t:Name>
              <t:IsInline>false</t:IsInline>
              <t:Message>
                <t:Subject>Message Item Subject</t:Subject>
                <t:Body BodyType="HTML">Message Item Body</t:Body>
                <t:ToRecipients>
                  <t:Mailbox>
                    <t:EmailAddress>sadie@contoso.com</t:EmailAddress>
                  </t:Mailbox>
                  <t:Mailbox>
                    <t:EmailAddress>mack@contoso.com</t:EmailAddress>
                  </t:Mailbox>
                </t:ToRecipients>
              </t:Message>
            </t:ItemAttachment>
          </t:Attachments>
          <t:ToRecipients>
            <t:Mailbox>
              <t:EmailAddress>sadie@contoso.com</t:EmailAddress>
            </t:Mailbox>
            <t:Mailbox>
              <t:EmailAddress>ronnie@contoso.com</t:EmailAddress>
            </t:Mailbox>
          </t:ToRecipients>
        </t:Message>
      </m:Items>
    </m:CreateItem>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="99039-140">El servidor responde a la solicitud **CreateItem** con un mensaje de [CreateItemResponse](http://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) que incluye un valor [ResponseCode](http://msdn.microsoft.com/es-es/library/aa580757%28v=exchg.150%29.aspx) de **NoError**, lo que indica que el correo electrónico y los datos adjuntos se han creado correctamente.</span><span class="sxs-lookup"><span data-stu-id="99039-140">The server responds to the **CreateItem** request with a [CreateItemResponse](http://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/es-es/library/aa580757%28v=exchg.150%29.aspx) value of **NoError**, which indicates that the email and the attachments were created successfully.</span></span> <span data-ttu-id="99039-141">También se incluye el [ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) del mensaje recién creado y los valores de [AttachmentId](http://msdn.microsoft.com/library/55a5fd77-60d1-40fa-8144-770600cedc6a%28Office.15%29.aspx) para cada uno de los datos adjuntos en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="99039-141">The [ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) of the newly created message and the [AttachmentId](http://msdn.microsoft.com/library/55a5fd77-60d1-40fa-8144-770600cedc6a%28Office.15%29.aspx) values for each of the attachments is also included in the response.</span></span> <span data-ttu-id="99039-142">Los valores de algunos atributos se han abreviado para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="99039-142">The values of some attributes have been shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="939"
                         MinorBuildNumber="12"
                         Version="V2_11"
                         xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:CreateItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
                          xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:CreateItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Items>
            <t:Message>
              <t:ItemId Id="upV4AAA="
                        ChangeKey="CQAAABYAAAAFI5DJmZv+TLtyLOLIF1S5AAAXuktU" />
              <t:Attachments>
                <t:FileAttachment>
                  <t:AttachmentId Id="6ts3NuI=" />
                </t:FileAttachment>
                <t:FileAttachment>
                  <t:AttachmentId Id="gOIZx1I=" />
                </t:FileAttachment>
                <t:FileAttachment>
                  <t:AttachmentId Id="esRan5I=" />
                </t:FileAttachment>
                <t:FileAttachment>
                  <t:AttachmentId Id="t7sU6s=" />
                </t:FileAttachment>
                <t:ItemAttachment>
                  <t:AttachmentId Id="XgDCggM=" />
                </t:ItemAttachment>
              </t:Attachments>
            </t:Message>
          </m:Items>
        </m:CreateItemResponseMessage>
      </m:ResponseMessages>
    </m:CreateItemResponse>
  </s:Body>
</s:Envelope>
```

<span data-ttu-id="99039-143">Para [enviar el recién creado mensaje](how-to-send-email-messages-by-using-ews-in-exchange.md), llame a la operación de [SendItem](http://msdn.microsoft.com/library/337b89ef-e1b7-45ed-92f3-8abe4200e4c7%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="99039-143">To [send this newly created message](how-to-send-email-messages-by-using-ews-in-exchange.md), call the [SendItem](http://msdn.microsoft.com/library/337b89ef-e1b7-45ed-92f3-8abe4200e4c7%28Office.15%29.aspx) operation.</span></span> 
  
## <a name="add-an-existing-item-to-a-new-email-by-using-the-mimecontent-and-the-ews-managed-api"></a><span data-ttu-id="99039-144">Agregar un elemento existente a una nueva dirección de correo mediante el uso de la MimeContent y la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="99039-144">Add an existing item to a new email by using the MimeContent and the EWS Managed API</span></span>
<span data-ttu-id="99039-145"><a name="bk_addexistingemailewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="99039-145"></span></span>

<span data-ttu-id="99039-146">Para agregar un elemento existente como datos adjuntos de elemento a otro elemento, debe crear un nuevo elemento de datos adjuntos y copie el contenido del elemento existente en el nuevo elemento.</span><span class="sxs-lookup"><span data-stu-id="99039-146">To add an existing item as an item attachment to another item, you need to create a new item attachment and copy the content of the existing item to the new item.</span></span> <span data-ttu-id="99039-147">Hay dos formas de hacer esto:</span><span class="sxs-lookup"><span data-stu-id="99039-147">There are two ways to do this:</span></span> 
  
1. <span data-ttu-id="99039-148">Si está trabajando con mensajes de correo electrónico en concreto, puede copiar el valor de la propiedad [MimeContent](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.item.mimecontent%28v=exchg.80%29.aspx) desde el correo electrónico en los datos adjuntos del elemento recién creado.</span><span class="sxs-lookup"><span data-stu-id="99039-148">If you're working with email messages specifically, you can copy the value of the [MimeContent](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.item.mimecontent%28v=exchg.80%29.aspx) property from the email into the newly created item attachment.</span></span> <span data-ttu-id="99039-149">Algunas propiedades, perderá durante este proceso, por ejemplo, siga los indicadores y las categorías, pero funciona muy bien para mensajes de correo electrónico estándar.</span><span class="sxs-lookup"><span data-stu-id="99039-149">You will lose some properties during this process, such as follow up flags and categories, but it works great for standard email messages.</span></span> 
    
2. <span data-ttu-id="99039-150">Si necesita plena fidelidad para todos los tipos de elemento, puede enlazar a un elemento existente y copie todas las propiedades y las propiedades extendidas en los nuevos datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="99039-150">If you need full fidelity for all item types, you can bind to an existing item and copy all the properties and extended properties into the new attachment.</span></span>
    
<span data-ttu-id="99039-151">En el ejemplo de código siguiente se muestra el primer enfoque, copiando la **MimeContent** en los datos adjuntos del elemento nuevo.</span><span class="sxs-lookup"><span data-stu-id="99039-151">The following code example shows the first approach, copying the **MimeContent** into the new item attachment.</span></span> <span data-ttu-id="99039-152">En este ejemplo siguiente es un procedimiento que muestra cómo se puede modificar el código para utilizar el segundo enfoque.</span><span class="sxs-lookup"><span data-stu-id="99039-152">Following this example is a procedure that shows how you can modify the code to use the second approach.</span></span> 
  
<span data-ttu-id="99039-153">En este ejemplo se da por supuesto que **servicio** es un objeto [ExchangeService](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) válido y que se ha autenticado el usuario a un servidor de Exchange, y que los **itemId** es [ItemId](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.itemid%28v=exchg.80%29.aspx) del elemento para adjuntar.</span><span class="sxs-lookup"><span data-stu-id="99039-153">This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and that the user has been authenticated to an Exchange server, and that the **itemId** is the [ItemId](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.itemid%28v=exchg.80%29.aspx) of the item to attach.</span></span> 
  
```cs
public static void CreateEmailExistingItem(ExchangeService service, ItemId itemId)
{        
    // This method results in a GetItem call to EWS.
    EmailMessage msgToAttach = EmailMessage.Bind(service,itemId, 
        new PropertySet(ItemSchema.MimeContent, ItemSchema.Subject));
    // Create an email message and set properties on the message.
    EmailMessage message = new EmailMessage(service);
    message.Subject = "Message with Item Attachment (MimeContent)";
    message.Body = "The attachment to this message was created by copying
        the MimeContent from the original message and adding it to a new item attachment.";
    message.ToRecipients.Add("sadie@contoso.com");
    // Add an email message item attachment and set properties on the item.
    ItemAttachment<EmailMessage> itemAttachment = message.Attachments.AddItemAttachment<EmailMessage>();
    itemAttachment.Item.MimeContent = msgToAttach.MimeContent;
    itemAttachment.Name = msgToAttach.Subject;
    // Send the mail and save a copy in the Sent Items folder.
    // This method results in a CreateItem and SendItem call to EWS.
    message.SendAndSaveCopy();
}
```

<span data-ttu-id="99039-154">Para modificar este ejemplo para copiar cada una de las propiedades en el elemento existente en los datos adjuntos del elemento nuevo, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="99039-154">To modify this example to copy each of the properties on the existing item into the new item attachment, do the following:</span></span> 
  
1. <span data-ttu-id="99039-155">Cambiar la propiedad establecida para incluir **PropertySet.FirstClassProperties** y cualquier propiedades adicionales o las propiedades extendidas que necesita.</span><span class="sxs-lookup"><span data-stu-id="99039-155">Change the property set to include **PropertySet.FirstClassProperties** and any additional properties or extended properties you need.</span></span> 
    
  ```cs
  // Add additional properties to the PropertySet.
  EmailMessage msgToAttach = EmailMessage.Bind(service, itemId, new PropertySet(PropertySet.FirstClassProperties));
  ```

2. <span data-ttu-id="99039-156">Quite la línea siguiente, ya que no necesita la propiedad **MimeContent** .</span><span class="sxs-lookup"><span data-stu-id="99039-156">Remove the following line, because you do not need the **MimeContent** property.</span></span> 
    
  ```cs
  itemAttachment.Item.MimeContent = msgToAttach.MimeContent;
  ```

3. <span data-ttu-id="99039-157">Repita esta línea para cada propiedad copiar los nuevos datos adjuntos del elemento existente.</span><span class="sxs-lookup"><span data-stu-id="99039-157">Repeat this line for each property to copy from the existing item to the new attachment.</span></span> <span data-ttu-id="99039-158">No copiar el **ItemId** a los nuevos datos adjuntos de elemento porque es una propiedad de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="99039-158">Do not copy the **ItemId** into the new item attachment because that's a read-only property.</span></span> 
    
  ```cs
  itemAttachment.Item.Subject = msgToAttach.Subject;
  ```

4. <span data-ttu-id="99039-159">Establezca la propiedad [PidTagMessageFlags](http://msdn.microsoft.com/es-es/library/cc839733.aspx) (0x0E070003) en los datos adjuntos a **enviado**.</span><span class="sxs-lookup"><span data-stu-id="99039-159">Set the [PidTagMessageFlags](http://msdn.microsoft.com/es-es/library/cc839733.aspx) (0x0E070003) property on the attachment to **Sent**.</span></span>
    
  ```cs
  ExtendedPropertyDefinition sent = new ExtendedPropertyDefinition(3591, MapiPropertyType.Integer);
  msgToAttach.Item.SetExtendedProperty(sent, "1");
  ```

## <a name="add-an-existing-item-to-a-new-email-by-using-the-mimecontent-and-ews"></a><span data-ttu-id="99039-160">Agregar un elemento existente a una nueva dirección de correo mediante el uso de la MimeContent y EWS</span><span class="sxs-lookup"><span data-stu-id="99039-160">Add an existing item to a new email by using the MimeContent and EWS</span></span>
<span data-ttu-id="99039-161"><a name="bk_addexistingemailews"> </a></span><span class="sxs-lookup"><span data-stu-id="99039-161"></span></span>

<span data-ttu-id="99039-162">Existen dos maneras de agregar un elemento existente a un nuevo elemento:</span><span class="sxs-lookup"><span data-stu-id="99039-162">There are two ways to add an existing item to a new item:</span></span> 
  
1. <span data-ttu-id="99039-163">Si está trabajando con mensajes de correo electrónico en concreto, puede copiar el valor del elemento [MimeContent](http://msdn.microsoft.com/library/4f472a08-5653-4c54-ba65-831dfe32f20f%28Office.15%29.aspx) desde el correo electrónico en los datos adjuntos del elemento recién creado.</span><span class="sxs-lookup"><span data-stu-id="99039-163">If you're working with email messages specifically, you can copy the value of the [MimeContent](http://msdn.microsoft.com/library/4f472a08-5653-4c54-ba65-831dfe32f20f%28Office.15%29.aspx) element from the email into the newly created item attachment.</span></span> <span data-ttu-id="99039-164">Algunas propiedades, perderá durante este proceso, por ejemplo, siga los indicadores y las categorías, pero funciona muy bien para mensajes de correo electrónico estándar.</span><span class="sxs-lookup"><span data-stu-id="99039-164">You will lose some properties during this process, such as follow up flags and categories, but it works great for standard email messages.</span></span> 
    
2. <span data-ttu-id="99039-165">Si necesita plena fidelidad para todos los tipos de elemento, puede enlazar a un elemento existente y copie todas las propiedades y las propiedades extendidas en los nuevos datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="99039-165">If you need full fidelity for all item types, you can bind to an existing item and copy all the properties and extended properties into the new attachment.</span></span>
    
<span data-ttu-id="99039-166">En el ejemplo de código siguiente se muestra cómo usar el elemento **MimeContent** para copiar el contenido del elemento original en el valor de **MimeContent** de los datos adjuntos del elemento nuevo.</span><span class="sxs-lookup"><span data-stu-id="99039-166">The following code example shows how to use the **MimeContent** element to copy the content of the original item into the **MimeContent** value of the new item attachment.</span></span> <span data-ttu-id="99039-167">El ejemplo utiliza las siguientes operaciones:</span><span class="sxs-lookup"><span data-stu-id="99039-167">The example uses the following operations:</span></span> 
  
1. <span data-ttu-id="99039-168">[GetItem](http://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) : para obtener el **MimeContent** y el [asunto](http://msdn.microsoft.com/library/c140d6c2-deb1-4f67-a908-9397197c4ae7%28Office.15%29.aspx) del mensaje que se convertirán en los datos adjuntos del elemento en el nuevo mensaje.</span><span class="sxs-lookup"><span data-stu-id="99039-168">[GetItem](http://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) — To get the **MimeContent** and [Subject](http://msdn.microsoft.com/library/c140d6c2-deb1-4f67-a908-9397197c4ae7%28Office.15%29.aspx) of the message that will become the item attachment on the new message.</span></span> 
    
2. <span data-ttu-id="99039-169">[CreateItem](http://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) : para crear el nuevo mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="99039-169">[CreateItem](http://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) — To create the new email message.</span></span> 
    
3. <span data-ttu-id="99039-170">[CreateAttachment](http://msdn.microsoft.com/library/e066db95-6963-4507-a8d0-8efad287f550%28Office.15%29.aspx): para crear los nuevos datos adjuntos, utilizando el **MimeContent** y el **asunto** recuperados por la operación **GetItem** .</span><span class="sxs-lookup"><span data-stu-id="99039-170">[CreateAttachment](http://msdn.microsoft.com/library/e066db95-6963-4507-a8d0-8efad287f550%28Office.15%29.aspx)— To create the new attachment, using the **MimeContent** and **Subject** retrieved by the **GetItem** operation.</span></span> 
    
4. <span data-ttu-id="99039-171">[SendItem](http://msdn.microsoft.com/library/337b89ef-e1b7-45ed-92f3-8abe4200e4c7%28Office.15%29.aspx) : enviar y guardar el mensaje.</span><span class="sxs-lookup"><span data-stu-id="99039-171">[SendItem](http://msdn.microsoft.com/library/337b89ef-e1b7-45ed-92f3-8abe4200e4c7%28Office.15%29.aspx) — To send and save the message.</span></span> 
    
<span data-ttu-id="99039-172">En el ejemplo se inicia, se recupera el **MimeContent** y el **asunto** del elemento existente.</span><span class="sxs-lookup"><span data-stu-id="99039-172">The example starts by retrieving the **MimeContent** and the **Subject** of the existing item.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <m:GetItem>
      <m:ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="item:MimeContent" />
          <t:FieldURI FieldURI="item:Subject" />
        </t:AdditionalProperties>
      </m:ItemShape>
      <m:ItemIds>
        <t:ItemId Id="jCrTAAA=" />
      </m:ItemIds>
    </m:GetItem>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="99039-173">El servidor responde a la solicitud de **GetItem** con un mensaje de [GetItemResponse](http://msdn.microsoft.com/library/8b66de1b-26a6-476c-9585-a96059125716%28Office.15%29.aspx) que incluye un valor [ResponseCode](http://msdn.microsoft.com/es-es/library/aa580757%28v=exchg.150%29.aspx) de **NoError**, lo que indica que se ha recuperado el correo electrónico y el **MimeContent** y ** Asunto** del correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="99039-173">The server responds to the **GetItem** request with a [GetItemResponse](http://msdn.microsoft.com/library/8b66de1b-26a6-476c-9585-a96059125716%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/es-es/library/aa580757%28v=exchg.150%29.aspx) value of **NoError**, which indicates that the email was retrieved successfully, and the **MimeContent** and **Subject** of the email.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="944"
                         MinorBuildNumber="11"
                         Version="V2_12"
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
              <t:MimeContent CharacterSet="UTF-8">tDQe/Eo=…</t:MimeContent>
              <t:ItemId Id="jCrTAAA="
                        ChangeKey="CQAAABYAAAAFI5DJmZv+TLtyLOLIF1S5AAAZi+7u" />
              <t:Subject>Play tennis?</t:Subject>
            </t:Message>
          </m:Items>
        </m:GetItemResponseMessage>
      </m:ResponseMessages>
    </m:GetItemResponse>
  </s:Body>
</s:Envelope>
```

<span data-ttu-id="99039-174">A continuación, llame a la operación **CreateItem** para crear el nuevo mensaje de correo.</span><span class="sxs-lookup"><span data-stu-id="99039-174">Next, call the **CreateItem** operation to create the new email.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2010" />
  </soap:Header>
  <soap:Body>
    <m:CreateItem MessageDisposition="SaveOnly">
      <m:Items>
        <t:Message>
          <t:Subject>Message with Item Attachment (MimeContent)</t:Subject>
          <t:Body BodyType="HTML">The attachment to this message was created by copying the MimeContent from the original message and adding it to a new item attachment.</t:Body>
          <t:ToRecipients>
            <t:Mailbox>
              <t:EmailAddress>primary@contoso1000.onmicrosoft.com</t:EmailAddress>
            </t:Mailbox>
          </t:ToRecipients>
        </t:Message>
      </m:Items>
    </m:CreateItem>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="99039-175">El servidor responde a la solicitud **CreateItem** con un mensaje de [CreateItemResponse](http://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) que incluye un valor [ResponseCode](http://msdn.microsoft.com/es-es/library/aa580757%28v=exchg.150%29.aspx) de **NoError**, lo que indica que el correo electrónico se ha creado correctamente.</span><span class="sxs-lookup"><span data-stu-id="99039-175">The server responds to the **CreateItem** request with a [CreateItemResponse](http://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/es-es/library/aa580757%28v=exchg.150%29.aspx) value of **NoError**, which indicates that the email was created successfully.</span></span>
  
<span data-ttu-id="99039-176">A continuación, crear los datos adjuntos del elemento nuevo mediante el uso de la **MimeContent** y el **asunto** recuperados por la operación **GetItem** .</span><span class="sxs-lookup"><span data-stu-id="99039-176">Next, create the new item attachment by using the **MimeContent** and **Subject** retrieved by the **GetItem** operation.</span></span> <span data-ttu-id="99039-177">El valor del elemento [ParentItemId](http://msdn.microsoft.com/library/72dc4391-72db-44d2-85d9-4718d59886a7%28Office.15%29.aspx) se rellena con el valor de **ItemId** devuelto en la respuesta **CreateItem** .</span><span class="sxs-lookup"><span data-stu-id="99039-177">The value of the [ParentItemId](http://msdn.microsoft.com/library/72dc4391-72db-44d2-85d9-4718d59886a7%28Office.15%29.aspx) element is populated by using the **ItemId** value returned in the **CreateItem** response.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2010" />
  </soap:Header>
  <soap:Body>
    <m:CreateAttachment>
      <m:ParentItemId Id="jDKsAAA=" />
      <m:Attachments>
        <t:ItemAttachment>
          <t:Name>Play tennis?</t:Name>
          <t:IsInline>false</t:IsInline>
          <t:Message>
            <t:MimeContent CharacterSet="UTF-8">tDQe/Eo=…</t:MimeContent>
          </t:Message>
        </t:ItemAttachment>
      </m:Attachments>
    </m:CreateAttachment>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="99039-178">El servidor responde a la solicitud de **CreateAttachment** con un mensaje de [CreateAttachmentResponse](http://msdn.microsoft.com/library/cf6bd8bb-5317-4a03-bd75-297dd359b5da%28Office.15%29.aspx) que incluye un valor [ResponseCode](http://msdn.microsoft.com/es-es/library/aa580757%28v=exchg.150%29.aspx) **NoError**, lo que indica que los datos adjuntos se crean correctamente y el [ AttachmentId](http://msdn.microsoft.com/library/55a5fd77-60d1-40fa-8144-770600cedc6a%28Office.15%29.aspx) de los datos adjuntos recién creado.</span><span class="sxs-lookup"><span data-stu-id="99039-178">The server responds to the **CreateAttachment** request with a [CreateAttachmentResponse](http://msdn.microsoft.com/library/cf6bd8bb-5317-4a03-bd75-297dd359b5da%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/es-es/library/aa580757%28v=exchg.150%29.aspx) value of **NoError**, which indicates that the attachment was created successfully, and the [AttachmentId](http://msdn.microsoft.com/library/55a5fd77-60d1-40fa-8144-770600cedc6a%28Office.15%29.aspx) of the newly created attachment.</span></span> 
  
<span data-ttu-id="99039-179">Ahora que se ha creado el nuevo mensaje y el artículo se ha conectado, puede [enviar el recién creado mensaje](how-to-send-email-messages-by-using-ews-in-exchange.md) mediante una llamada a la operación de [SendItem](http://msdn.microsoft.com/library/337b89ef-e1b7-45ed-92f3-8abe4200e4c7%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="99039-179">Now that the new message has been created, and the item was attached, you can [send this newly created message](how-to-send-email-messages-by-using-ews-in-exchange.md) by calling the [SendItem](http://msdn.microsoft.com/library/337b89ef-e1b7-45ed-92f3-8abe4200e4c7%28Office.15%29.aspx) operation.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2010" />
  </soap:Header>
  <soap:Body>
    <m:SendItem SaveItemToFolder="true">
      <m:ItemIds>
        <t:ItemId Id="jDKsAAA="
                  ChangeKey="CQAAABYAAAAFI5DJmZv+TLtyLOLIF1S5AAAZi/q/" />
      </m:ItemIds>
      <m:SavedItemFolderId>
        <t:DistinguishedFolderId Id="sentitems" />
      </m:SavedItemFolderId>
    </m:SendItem>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="99039-180">El servidor responde a la solicitud de **SendItem** con un mensaje de [SendItemResponse](http://msdn.microsoft.com/library/26ac41c7-57d9-473e-ab7a-bae93e1d2aba%28Office.15%29.aspx) que incluye un valor [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) de **NoError**, lo que indica que el correo electrónico se ha enviado correctamente.</span><span class="sxs-lookup"><span data-stu-id="99039-180">The server responds to the **SendItem** request with a [SendItemResponse](http://msdn.microsoft.com/library/26ac41c7-57d9-473e-ab7a-bae93e1d2aba%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) value of **NoError**, which indicates that the email was sent successfully.</span></span>
  
## <a name="create-an-email-with-an-inline-attachment-by-using-the-ews-managed-api"></a><span data-ttu-id="99039-181">Crear un correo electrónico con datos adjuntos en línea mediante el uso de la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="99039-181">Create an email with an inline attachment by using the EWS Managed API</span></span>
<span data-ttu-id="99039-182"><a name="bk_createinlineattachewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="99039-182"></span></span>

<span data-ttu-id="99039-183">En el ejemplo de código siguiente se muestra cómo crear un correo electrónico con datos adjuntos en línea por:</span><span class="sxs-lookup"><span data-stu-id="99039-183">The following code example shows how to create an email with an inline attachment by:</span></span>
  
1. <span data-ttu-id="99039-184">Uso del objeto [EmailMessage](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx) para crear un mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="99039-184">Using the [EmailMessage](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx) object to create an email message.</span></span> 
    
2. <span data-ttu-id="99039-185">Si se establece la propiedad [EmailMessage.Body](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.item.body%28v=exchg.80%29.aspx) a un cuerpo HTML que incluye datos adjuntos en línea.</span><span class="sxs-lookup"><span data-stu-id="99039-185">Setting the [EmailMessage.Body](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.item.body%28v=exchg.80%29.aspx) property to an HTML body that includes an inline attachment.</span></span> 
    
3. <span data-ttu-id="99039-186">Con el método [AttachmentCollection.AddFileAttachment](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.attachmentcollection.addfileattachment%28v=exchg.80%29.aspx) para agregar los datos adjuntos al mensaje.</span><span class="sxs-lookup"><span data-stu-id="99039-186">Using the [AttachmentCollection.AddFileAttachment](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.attachmentcollection.addfileattachment%28v=exchg.80%29.aspx) method to add the attachment to the message.</span></span> 
    
4. <span data-ttu-id="99039-187">Usar el método [EmailMessage.SendAndSaveCopy](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.emailmessage.sendandsavecopy%28v=exchg.80%29.aspx) para enviar el mensaje al destinatario y guardar el mensaje en la carpeta Elementos enviados.</span><span class="sxs-lookup"><span data-stu-id="99039-187">Using the [EmailMessage.SendAndSaveCopy](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.emailmessage.sendandsavecopy%28v=exchg.80%29.aspx) method to send the message to the recipient and save the message in the Sent Items folder.</span></span> 
    
<span data-ttu-id="99039-188">En este ejemplo se da por supuesto que **servicio** es un objeto [ExchangeService](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) válido y que se ha autenticado el usuario a un servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="99039-188">This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and that the user has been authenticated to an Exchange server.</span></span> 
  
```cs
public static void CreateEmailWithInlineAttachment(ExchangeService service)
{
    // Create the HTML body with the content identifier of the attachment.
    string html = @"<html>
                        <head>
                        </head>
                        <body>
                        <img width=100 height=100 id=""1"" src=""cid:Party.jpg"">
                        </body>
                        </html>";
         
    // Create the email message.
    EmailMessage message = new EmailMessage(service);
    message.Subject = "Inline Attachment";
    message.Body = new MessageBody(BodyType.HTML, html);
    message.ToRecipients.Add("sadie@contoso.com");
    // Add the attachment to the local copy of the email message.
    string file = @"C:\Temp\Party.jpg";
    message.Attachments.AddFileAttachment("Party.jpg", file);
    message.Attachments[0].IsInline = true;
    message.Attachments[0].ContentId = "Party.jpg";
         
    // Send the mail and save a copy in the Sent Items folder.
    // This method results in a CreateItem and SendItem call to EWS.
    message.SendAndSaveCopy();
}
```

## <a name="create-an-email-with-an-inline-attachment-by-using-ews"></a><span data-ttu-id="99039-189">Crear un correo electrónico con datos adjuntos en línea mediante el uso de EWS</span><span class="sxs-lookup"><span data-stu-id="99039-189">Create an email with an inline attachment by using EWS</span></span>
<span data-ttu-id="99039-190"><a name="bk_createinlineattachewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="99039-190"></span></span>

<span data-ttu-id="99039-191">En el ejemplo de código siguiente se muestra cómo usar la operación [CreateItem](http://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) para crear un mensaje de correo electrónico con datos adjuntos del archivo en línea.</span><span class="sxs-lookup"><span data-stu-id="99039-191">The following code example shows how to use the [CreateItem](http://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) operation to create an email message with an inline file attachment.</span></span> <span data-ttu-id="99039-192">El atributo **BodyType** del elemento [Body](http://msdn.microsoft.com/library/7851ea9b-9f87-4adc-a26f-7a27df4a9bca%28Office.15%29.aspx) indica que el contenido está en formato HTML y que incluye el origen de la imagen.</span><span class="sxs-lookup"><span data-stu-id="99039-192">The **BodyType** attribute of the [Body](http://msdn.microsoft.com/library/7851ea9b-9f87-4adc-a26f-7a27df4a9bca%28Office.15%29.aspx) element indicates that the content is in HTML format and includes the image source.</span></span> <span data-ttu-id="99039-193">También es una de las solicitudes XML que la API administrada de EWS envía al usar la API administrada de EWS para [crear un correo electrónico con datos adjuntos en línea](#bk_createinlineattachewsma).</span><span class="sxs-lookup"><span data-stu-id="99039-193">This is also one of the XML requests that the EWS Managed API sends when you use the EWS Managed API to [create an email with an inline attachment](#bk_createinlineattachewsma).</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2010" />
  </soap:Header>
  <soap:Body>
    <m:CreateItem MessageDisposition="SaveOnly">
      <m:Items>
        <t:Message>
          <t:Subject>Inline Attachment</t:Subject>
          <t:Body BodyType="HTML">
            &amp;lt;html&amp;gt;
            &amp;lt;head&amp;gt;
            &amp;lt;/head&amp;gt;
            &amp;lt;body&amp;gt;
            &amp;lt;img width=100 height=100 id="1" src="cid:Party.jpg"&amp;gt;
            &amp;lt;/body&amp;gt;
            &amp;lt;/html&amp;gt;
          </t:Body>
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

<span data-ttu-id="99039-194">El servidor responde a la solicitud **CreateItem** con un mensaje de [CreateItemResponse](http://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) que incluye un valor [ResponseCode](http://msdn.microsoft.com/es-es/library/aa580757%28v=exchg.150%29.aspx) **NoError**, lo que indica que el correo electrónico se ha creado correctamente y la [ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) de la recientemente mensaje de creación.</span><span class="sxs-lookup"><span data-stu-id="99039-194">The server responds to the **CreateItem** request with a [CreateItemResponse](http://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/es-es/library/aa580757%28v=exchg.150%29.aspx) value of **NoError**, which indicates that the email was created successfully, and the [ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) of the newly created message.</span></span> 
  
<span data-ttu-id="99039-195">Para [enviar el recién creado mensaje](how-to-send-email-messages-by-using-ews-in-exchange.md), llame a la operación de [SendItem](http://msdn.microsoft.com/library/337b89ef-e1b7-45ed-92f3-8abe4200e4c7%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="99039-195">To [send this newly created message](how-to-send-email-messages-by-using-ews-in-exchange.md), call the [SendItem](http://msdn.microsoft.com/library/337b89ef-e1b7-45ed-92f3-8abe4200e4c7%28Office.15%29.aspx) operation.</span></span> 
  
## <a name="add-an-attachment-to-an-existing-email-by-using-the-ews-managed-api"></a><span data-ttu-id="99039-196">Agregar datos adjuntos a un correo electrónico existente mediante el uso de la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="99039-196">Add an attachment to an existing email by using the EWS Managed API</span></span>
<span data-ttu-id="99039-197"><a name="bk_createinlineattachewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="99039-197"></span></span>

<span data-ttu-id="99039-198">En el ejemplo de código siguiente se muestra cómo agregar datos adjuntos a un correo electrónico existente por:</span><span class="sxs-lookup"><span data-stu-id="99039-198">The following code example shows how to add an attachment to an existing email by:</span></span> 
  
1. <span data-ttu-id="99039-199">Utilizar el método [EmailMessage.Bind](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) para enlazar a un mensaje de correo electrónico existente.</span><span class="sxs-lookup"><span data-stu-id="99039-199">Using the [EmailMessage.Bind](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) method to bind to an existing email message.</span></span> 
    
2. <span data-ttu-id="99039-200">Adición de un archivo adjunto al mensaje mediante el método **AddFileAttachment** .</span><span class="sxs-lookup"><span data-stu-id="99039-200">Adding a file attachment to the message by using the **AddFileAttachment** method.</span></span> 
    
3. <span data-ttu-id="99039-201">Guardar las actualizaciones llamando al método [EmailMessage.Update](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.emailmessage.update%28v=exchg.80%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="99039-201">Saving the updates by calling the [EmailMessage.Update](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.emailmessage.update%28v=exchg.80%29.aspx) method.</span></span> 
    
<span data-ttu-id="99039-202">En este ejemplo se da por supuesto que **servicio** es un objeto [ExchangeService](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) válido y que se ha autenticado el usuario a un servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="99039-202">This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and that the user has been authenticated to an Exchange server.</span></span> 
  
```XML
public static void AddAttachmentToExisting(ExchangeService service, ItemId itemId)
{
    // This method results in a GetItem call to EWS.
    EmailMessage message = EmailMessage.Bind(service, itemId);
    message.Attachments.AddFileAttachment("C:\\temp\\FileAttachment.txt");
    // This method results in a CreateAttachment call to EWS.
    message.Update(ConflictResolutionMode.AlwaysOverwrite);
}
```

## <a name="add-an-attachment-to-an-existing-email-by-using-ews"></a><span data-ttu-id="99039-203">Agregar datos adjuntos a un correo electrónico existente mediante el uso de EWS</span><span class="sxs-lookup"><span data-stu-id="99039-203">Add an attachment to an existing email by using EWS</span></span>
<span data-ttu-id="99039-204"><a name="bk_createinlineattachewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="99039-204"></span></span>

<span data-ttu-id="99039-205">En el ejemplo de código siguiente se muestra cómo usar la operación [CreateAttachment](http://msdn.microsoft.com/library/e066db95-6963-4507-a8d0-8efad287f550%28Office.15%29.aspx) para agregar un archivo adjunto a un mensaje de correo electrónico existente.</span><span class="sxs-lookup"><span data-stu-id="99039-205">The following code example shows how to use the [CreateAttachment](http://msdn.microsoft.com/library/e066db95-6963-4507-a8d0-8efad287f550%28Office.15%29.aspx) operation to add a file attachment to an existing email message.</span></span> <span data-ttu-id="99039-206">También es una de las solicitudes XML que la API administrada de EWS envía al usar la API administrada de EWS para [Agregar datos adjuntos a un correo electrónico existente](#bk_createinlineattachewsma).</span><span class="sxs-lookup"><span data-stu-id="99039-206">This is also one of the XML requests that the EWS Managed API sends when you use the EWS Managed API to [add an attachment to an existing email](#bk_createinlineattachewsma).</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
    <t:TimeZoneContext>
      <t:TimeZoneDefinition Id="Central Standard Time" />
    </t:TimeZoneContext>
  </soap:Header>
  <soap:Body>
    <m:CreateAttachment>
      <m:ParentItemId Id="uqE2AAA=" />
      <m:Attachments>
        <t:FileAttachment>
          <t:Name>FileAttachment.txt</t:Name>
          <t:Content>VGhpcyBpcyBhIGZpbGUgYXR0YWNobWVudC4=</t:Content>
        </t:FileAttachment>
      </m:Attachments>
    </m:CreateAttachment>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="99039-207">El servidor responde a la solicitud de **CreateAttachment** con un mensaje de [CreateAttachmentResponse](http://msdn.microsoft.com/library/cf6bd8bb-5317-4a03-bd75-297dd359b5da%28Office.15%29.aspx) que incluye un valor [ResponseCode](http://msdn.microsoft.com/es-es/library/aa580757%28v=exchg.150%29.aspx) **NoError**, lo que indica que los datos adjuntos se crean correctamente y el [ AttachmentId](http://msdn.microsoft.com/library/55a5fd77-60d1-40fa-8144-770600cedc6a%28Office.15%29.aspx) de los datos adjuntos recién creado.</span><span class="sxs-lookup"><span data-stu-id="99039-207">The server responds to the **CreateAttachment** request with a [CreateAttachmentResponse](http://msdn.microsoft.com/library/cf6bd8bb-5317-4a03-bd75-297dd359b5da%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/es-es/library/aa580757%28v=exchg.150%29.aspx) value of **NoError**, which indicates that the attachment was created successfully, and the [AttachmentId](http://msdn.microsoft.com/library/55a5fd77-60d1-40fa-8144-770600cedc6a%28Office.15%29.aspx) of the newly created attachment.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="939"
                         MinorBuildNumber="12"
                         Version="V2_11"
                         xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:CreateAttachmentResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
                                xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:CreateAttachmentResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Attachments>
            <t:FileAttachment>
              <t:AttachmentId Id="yRLhCh8="
                              RootItemId="uqE2AAA="
                              RootItemChangeKey="CQAAABYAAAAFI5DJmZv+TLtyLOLIF1S5AAAXulcf" />
            </t:FileAttachment>
          </m:Attachments>
        </m:CreateAttachmentResponseMessage>
      </m:ResponseMessages>
    </m:CreateAttachmentResponse>
  </s:Body>
</s:Envelope>
```

## <a name="see-also"></a><span data-ttu-id="99039-208">Vea también</span><span class="sxs-lookup"><span data-stu-id="99039-208">See also</span></span>


- [<span data-ttu-id="99039-209">Los datos adjuntos y EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="99039-209">Attachments and EWS in Exchange</span></span>](attachments-and-ews-in-exchange.md)
    
- [<span data-ttu-id="99039-210">Agregar datos adjuntos mediante el uso de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="99039-210">Add attachments by using EWS in Exchange</span></span>](how-to-add-attachments-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="99039-211">Eliminar los datos adjuntos mediante el uso de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="99039-211">Delete attachments by using EWS in Exchange</span></span>](how-to-delete-attachments-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="99039-212">Obtener datos adjuntos mediante el uso de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="99039-212">Get attachments by using EWS in Exchange</span></span>](how-to-get-attachments-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="99039-213">Enviar mensajes de correo electrónico mediante el uso de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="99039-213">Send email messages by using EWS in Exchange</span></span>](how-to-send-email-messages-by-using-ews-in-exchange.md)
    

