---
title: Correo electrónico y EWS en Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4d7bdb37-f7f1-409f-9749-f8bcde7dc52a
description: Obtenga información acerca de cómo trabajar con mensajes de correo electrónico, incluido cómo crear un correo electrónico y cómo realizar otras tareas relacionadas con el correo electrónico mediante el uso de la API administrada de EWS o EWS en Exchange.
ms.openlocfilehash: d222be7409a3c3f4613a2be39b83b977fabb09e8
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763002"
---
# <a name="email-and-ews-in-exchange"></a><span data-ttu-id="ebb2b-103">Correo electrónico y EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="ebb2b-103">Email and EWS in Exchange</span></span>

<span data-ttu-id="ebb2b-104">Obtenga información acerca de cómo trabajar con mensajes de correo electrónico, incluido cómo crear un correo electrónico y cómo realizar otras tareas relacionadas con el correo electrónico mediante el uso de la API administrada de EWS o EWS en Exchange.</span><span class="sxs-lookup"><span data-stu-id="ebb2b-104">Find out how to work with email messages, including how to create an email and how to perform other email-related tasks by using the EWS Managed API or EWS in Exchange.</span></span>
  

  
<span data-ttu-id="ebb2b-105">En esencia, Exchange es acerca del correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="ebb2b-105">At its core, Exchange is about email.</span></span> <span data-ttu-id="ebb2b-106">Pero ¿qué hace un correo electrónico de un correo electrónico?</span><span class="sxs-lookup"><span data-stu-id="ebb2b-106">But what makes an email an email?</span></span> <span data-ttu-id="ebb2b-107">Bueno, mensajes de correo electrónico están uno de [los elementos con establecimiento inflexible de tipos](folders-and-items-in-ews-in-exchange.md#bk_item) en Exchange, lo que significa que contienen un determinado [conjunto de propiedades](email-properties-and-elements-in-ews-in-exchange.md), incluso antes de que se envían.</span><span class="sxs-lookup"><span data-stu-id="ebb2b-107">Well, email messages are one of the [strongly typed items](folders-and-items-in-ews-in-exchange.md#bk_item) in Exchange, which means that they contain a particular [set of properties](email-properties-and-elements-in-ews-in-exchange.md), even before they're sent.</span></span> <span data-ttu-id="ebb2b-108">Mensajes de correo electrónico están representados por la clase [EmailMessage](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx) en la API administrada de EWS y en el elemento de [mensaje](http://msdn.microsoft.com/library/2400b33c-43b2-4fc2-b6fb-275a99e0e810%28Office.15%29.aspx) y sus elementos secundarios en EWS.</span><span class="sxs-lookup"><span data-stu-id="ebb2b-108">Email messages are represented by the [EmailMessage](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx) class in the EWS Managed API and by the [Message](http://msdn.microsoft.com/library/2400b33c-43b2-4fc2-b6fb-275a99e0e810%28Office.15%29.aspx) element and its child elements in EWS.</span></span> 
  
<span data-ttu-id="ebb2b-109">En la API administrada de EWS, el objeto **EmailMessage** se deriva el objeto de [elemento](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item%28v=exchg.80%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="ebb2b-109">In the EWS Managed API, the **EmailMessage** object derives from the [Item](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item%28v=exchg.80%29.aspx) object.</span></span> <span data-ttu-id="ebb2b-110">La clase **EmailMessage** extiende la clase de **elemento** proporcionando propiedades adicionales como [EmailMessage.Sender](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.sender%28v=exchg.80%29.aspx) y [EmailMessage.IsRead](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.emailmessage.isread%28v=exchg.80%29.aspx), que ahora son comunes a casi todos los escenarios de mensajería.</span><span class="sxs-lookup"><span data-stu-id="ebb2b-110">The **EmailMessage** class extends the **Item** class by providing additional properties like [EmailMessage.Sender](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.sender%28v=exchg.80%29.aspx) and [EmailMessage.IsRead](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.emailmessage.isread%28v=exchg.80%29.aspx), which are now common to nearly all messaging scenarios.</span></span> <span data-ttu-id="ebb2b-111">Al obtener, actualizar o eliminar un mensaje de correo electrónico, en la mayoría de los casos que puede hacerlo mediante el objeto **EmailMessage** o el objeto de **elemento** base, en función de si las propiedades que se está trabajando con están en la [EmailMessageSchema](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessageschema%28v=exchg.80%29.aspx) o la [ ItemSchema](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.itemschema%28v=exchg.80%29.aspx) clase.</span><span class="sxs-lookup"><span data-stu-id="ebb2b-111">When you get, update, or delete an email message, in most cases you can do that by using the **EmailMessage** object or the base **Item** object, depending on whether the properties you're working with are in the [EmailMessageSchema](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessageschema%28v=exchg.80%29.aspx) or the [ItemSchema](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.itemschema%28v=exchg.80%29.aspx) class.</span></span> <span data-ttu-id="ebb2b-112">Creación de elemento es diferente porque la clase de **elemento** no tiene un constructor, por lo que si se está creando un correo electrónico, se usará el [constructor EmailMessage](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.emailmessage.emailmessage%28v=exchg.80%29.aspx) para crear y el [EmailMessage.Save](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.save%28v=exchg.80%29.aspx) o [EmailMessage.SendAndSaveCopy ](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.sendandsavecopy%28v=exchg.80%29.aspx)métodos para guardarlo, o enviarlo y vuelva a guardarla.</span><span class="sxs-lookup"><span data-stu-id="ebb2b-112">Item creation is different because the **Item** class does not have a constructor, so when you're creating an email, you'll use the [EmailMessage constructor](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.emailmessage.emailmessage%28v=exchg.80%29.aspx) to create it and the [EmailMessage.Save](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.save%28v=exchg.80%29.aspx) or [EmailMessage.SendAndSaveCopy](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.sendandsavecopy%28v=exchg.80%29.aspx) methods to save it, or send it and save it.</span></span> 
  
<span data-ttu-id="ebb2b-113">De forma similar, en EWS, use la operación [CreateItem](http://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) con el elemento de [mensaje](http://msdn.microsoft.com/library/2400b33c-43b2-4fc2-b6fb-275a99e0e810%28Office.15%29.aspx) para crear un mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="ebb2b-113">Similarly, in EWS, use the [CreateItem](http://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) operation with the [Message](http://msdn.microsoft.com/library/2400b33c-43b2-4fc2-b6fb-275a99e0e810%28Office.15%29.aspx) element to create an email message.</span></span> <span data-ttu-id="ebb2b-114">Para obtener, actualizar o eliminar mensajes de correo electrónico mediante el uso de EWS, el hecho de que el elemento que se modifica es un mensaje de correo electrónico no es importante, aparte del hecho de que las propiedades adicionales están disponibles en los mensajes de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="ebb2b-114">To get, update, or delete emails by using EWS, the fact that the item being modified is an email message is not important, aside from the fact that additional properties are available on email messages.</span></span> <span data-ttu-id="ebb2b-115">También se usan las mismas operaciones que se usan para otros elementos fuertemente tipados para mensajes de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="ebb2b-115">The same operations that are used for other strongly typed items are also used for email messages.</span></span> 
  
|<span data-ttu-id="ebb2b-116">**Tarea**</span><span class="sxs-lookup"><span data-stu-id="ebb2b-116">**Task**</span></span>|<span data-ttu-id="ebb2b-117">**Método de la API administrada de EWS**</span><span class="sxs-lookup"><span data-stu-id="ebb2b-117">**EWS Managed API method**</span></span>|<span data-ttu-id="ebb2b-118">**Operación de EWS**</span><span class="sxs-lookup"><span data-stu-id="ebb2b-118">**EWS operation**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ebb2b-119">Crear</span><span class="sxs-lookup"><span data-stu-id="ebb2b-119">Create</span></span>  <br/> |[<span data-ttu-id="ebb2b-120">EmailMessage.Save</span><span class="sxs-lookup"><span data-stu-id="ebb2b-120">EmailMessage.Save</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.save%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="ebb2b-121">CreateItem</span><span class="sxs-lookup"><span data-stu-id="ebb2b-121">CreateItem</span></span>](http://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="ebb2b-122">Obtener</span><span class="sxs-lookup"><span data-stu-id="ebb2b-122">Get</span></span>  <br/> |[<span data-ttu-id="ebb2b-123">EmailMessage.Bind</span><span class="sxs-lookup"><span data-stu-id="ebb2b-123">EmailMessage.Bind</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="ebb2b-124">GetItem</span><span class="sxs-lookup"><span data-stu-id="ebb2b-124">GetItem</span></span>](http://msdn.microsoft.com/library/e8492e3b-1c8d-4b14-8070-9530f8306edd%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="ebb2b-125">Actualizar</span><span class="sxs-lookup"><span data-stu-id="ebb2b-125">Update</span></span>  <br/> |[<span data-ttu-id="ebb2b-126">Item.Update</span><span class="sxs-lookup"><span data-stu-id="ebb2b-126">Item.Update</span></span>](http://msdn.microsoft.com/en-us/library/dd635915%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="ebb2b-127">UpdateItem</span><span class="sxs-lookup"><span data-stu-id="ebb2b-127">UpdateItem</span></span>](http://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="ebb2b-128">Eliminar</span><span class="sxs-lookup"><span data-stu-id="ebb2b-128">Delete</span></span>  <br/> |[<span data-ttu-id="ebb2b-129">Item.Delete</span><span class="sxs-lookup"><span data-stu-id="ebb2b-129">Item.Delete</span></span>](http://msdn.microsoft.com/en-us/library/dd635072%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="ebb2b-130">DeleteItem</span><span class="sxs-lookup"><span data-stu-id="ebb2b-130">DeleteItem</span></span>](http://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx) <br/> |
   
<span data-ttu-id="ebb2b-131">Debido a que los mensajes de correo electrónico son simplemente [elementos con establecimiento inflexible de tipos](folders-and-items-in-ews-in-exchange.md#bk_item), en algunos casos trabaja con ellos de la misma manera que [trabajar con los elementos genéricos](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="ebb2b-131">Because email messages are simply [strongly typed items](folders-and-items-in-ews-in-exchange.md#bk_item), in some cases you work with them in the same way that you [work with generic items](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md).</span></span> 
  
## <a name="create-an-email-message-by-using-the-ews-managed-api"></a><span data-ttu-id="ebb2b-132">Crear un mensaje de correo electrónico mediante el uso de la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="ebb2b-132">Create an email message by using the EWS Managed API</span></span>
<span data-ttu-id="ebb2b-133"><a name="bk_createewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="ebb2b-133"></span></span>

<span data-ttu-id="ebb2b-134">Puede crear un mensaje de correo electrónico mediante el método API administrada de EWS [Guardar](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.save%28v=exchg.80%29.aspx) , tal como se muestra en el código en el siguiente ejemplo.</span><span class="sxs-lookup"><span data-stu-id="ebb2b-134">You can create an email message by using the EWS Managed API [Save](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.save%28v=exchg.80%29.aspx) method, as shown in the code in the following example.</span></span> <span data-ttu-id="ebb2b-135">Tenga en cuenta que sólo en el ejemplo se guarda el mensaje en la carpeta Borradores, no envía el mensaje.</span><span class="sxs-lookup"><span data-stu-id="ebb2b-135">Note that the example only saves the message in the Drafts folder, it does not send the message.</span></span> <span data-ttu-id="ebb2b-136">Para obtener información acerca de cómo enviar el mensaje o crear y enviar el mensaje en un solo paso, consulte [enviar mensajes de correo electrónico mediante el uso de EWS en Exchange](how-to-send-email-messages-by-using-ews-in-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="ebb2b-136">For information about how to send the message or create and send the message in one step, see [Send email messages by using EWS in Exchange](how-to-send-email-messages-by-using-ews-in-exchange.md).</span></span>
  
<span data-ttu-id="ebb2b-137">En este ejemplo se da por supuesto que **servicio** es un objeto [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) válido y que se ha autenticado el usuario a un servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="ebb2b-137">This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and that the user has been authenticated to an Exchange server.</span></span> 
  
```cs
// Create a new email message.
EmailMessage message = new EmailMessage(service);
// Set properties on the email message.
message.ToRecipients.Add("mack@contoso.com");
message.Subject = "Project priorities";
message.Body = "(1) Buy pizza, (2) Eat pizza";
// Save the email message to the Drafts folder (where it can be retrieved, updated, and sent at a later time).
// This method call results in a CreateItem call to EWS.
message.Save(WellKnownFolderName.Drafts);
Console.WriteLine("A draft email message with the subject '" + message.Subject + "' has been saved to the Drafts folder.");
```

## <a name="create-an-email-message-by-using-ews"></a><span data-ttu-id="ebb2b-138">Crear un mensaje de correo electrónico mediante el uso de EWS</span><span class="sxs-lookup"><span data-stu-id="ebb2b-138">Create an email message by using EWS</span></span>
<span data-ttu-id="ebb2b-139"><a name="bk_createews"> </a></span><span class="sxs-lookup"><span data-stu-id="ebb2b-139"></span></span>

<span data-ttu-id="ebb2b-140">Puede crear un mensaje de correo electrónico mediante el uso de la operación EWS [CreateItem](http://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) , tal como se muestra en el siguiente ejemplo.</span><span class="sxs-lookup"><span data-stu-id="ebb2b-140">You can create an email message by using the EWS [CreateItem](http://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) operation, as shown in the following example.</span></span> <span data-ttu-id="ebb2b-141">Esto también es la solicitud XML que la API administrada de EWS envía al [crear un mensaje de correo electrónico](#bk_createewsma).</span><span class="sxs-lookup"><span data-stu-id="ebb2b-141">This is also the XML request that the EWS Managed API sends when you [create an email message](#bk_createewsma).</span></span> <span data-ttu-id="ebb2b-142">Tenga en cuenta que sólo en el ejemplo siguiente se guarda el mensaje en la carpeta Borradores, no envía el mensaje.</span><span class="sxs-lookup"><span data-stu-id="ebb2b-142">Note that the following example only saves the message in the Drafts folder, it does not send the message.</span></span> <span data-ttu-id="ebb2b-143">Para obtener información acerca de cómo enviar el mensaje o crear y enviar el mensaje en uno ste, vea [enviar mensajes de correo electrónico mediante el uso de EWS en Exchange](how-to-send-email-messages-by-using-ews-in-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="ebb2b-143">For information about how to send the message or create and send the message in one ste, see [Send email messages by using EWS in Exchange](how-to-send-email-messages-by-using-ews-in-exchange.md).</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2010_SP2" />
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
              <t:EmailAddress>mack@contoso.com</t:EmailAddress>
            </t:Mailbox>
          </t:ToRecipients>
        </t:Message>
      </m:Items>
    </m:CreateItem>
  </soap:Body>
</soap:Envelope>

```

<span data-ttu-id="ebb2b-144">El servidor responde a la solicitud **CreateItem** con un mensaje de [CreateItemResponse](http://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) que incluye un valor [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) **NoError**, lo que indica que el correo electrónico se ha creado correctamente y la [ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) de la recientemente mensaje de creación.</span><span class="sxs-lookup"><span data-stu-id="ebb2b-144">The server responds to the **CreateItem** request with a [CreateItemResponse](http://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) value of **NoError**, which indicates that the email was created successfully, and the [ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) of the newly created message.</span></span> 
  
## <a name="get-update-and-delete-an-email-message-by-using-the-ews-managed-api"></a><span data-ttu-id="ebb2b-145">Obtener, actualizar y eliminar un mensaje de correo electrónico mediante el uso de la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="ebb2b-145">Get, update, and delete an email message by using the EWS Managed API</span></span>
<span data-ttu-id="ebb2b-146"><a name="bk_getewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="ebb2b-146"></span></span>

<span data-ttu-id="ebb2b-147">Puede usar la API administrada de EWS para obtener, actualizar o eliminar un mensaje de correo electrónico de la misma manera que se realizan estas acciones con cualquier elemento genérico desde el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="ebb2b-147">You can use the EWS Managed API to get, update, or delete an email message in the same way that you perform these actions on any generic item from the Exchange store.</span></span> <span data-ttu-id="ebb2b-148">Para obtener más información, vea [trabajar con elementos de buzón de correo de Exchange mediante el uso de EWS en Exchange](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="ebb2b-148">For more information, see [Work with Exchange mailbox items by using EWS in Exchange](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md).</span></span>
  
<span data-ttu-id="ebb2b-149">Si está actualizando un mensaje de correo electrónico, vea [de correo electrónico las propiedades y los elementos de EWS en Exchange](email-properties-and-elements-in-ews-in-exchange.md) para obtener una lista de propiedades del mensaje de correo electrónico puede escribir.</span><span class="sxs-lookup"><span data-stu-id="ebb2b-149">If you're updating an email message, see [Email properties and elements in EWS in Exchange](email-properties-and-elements-in-ews-in-exchange.md) for a list of writable email message properties.</span></span> <span data-ttu-id="ebb2b-150">Para enviar un borrador de mensaje después de que lo haya actualizado, vea [Enviar un borrador de mensaje de correo electrónico mediante el uso de la API administrada de EWS](how-to-send-email-messages-by-using-ews-in-exchange.md#bk_senddraftewsma).</span><span class="sxs-lookup"><span data-stu-id="ebb2b-150">To send a draft message after you've updated it, see [Send a draft email message by using the EWS Managed API](how-to-send-email-messages-by-using-ews-in-exchange.md#bk_senddraftewsma).</span></span>
  
## <a name="get-update-and-delete-an-email-message-by-using-ews"></a><span data-ttu-id="ebb2b-151">Obtener, actualizar y eliminar un mensaje de correo electrónico mediante el uso de EWS</span><span class="sxs-lookup"><span data-stu-id="ebb2b-151">Get, update, and delete an email message by using EWS</span></span>
<span data-ttu-id="ebb2b-152"><a name="bk_getews"> </a></span><span class="sxs-lookup"><span data-stu-id="ebb2b-152"></span></span>

<span data-ttu-id="ebb2b-153">Puede usar EWS para obtener, actualizar y eliminar un mensaje de correo electrónico de la misma manera que se realizan estas acciones con cualquier elemento genérico desde el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="ebb2b-153">You can use EWS to get, update, and delete an email message in the same way that you perform these actions on any generic item from the Exchange store.</span></span> <span data-ttu-id="ebb2b-154">Para obtener más información, vea [trabajar con elementos de buzón de correo de Exchange mediante el uso de EWS en Exchange](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="ebb2b-154">For more information, see [Work with Exchange mailbox items by using EWS in Exchange](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md).</span></span>
  
<span data-ttu-id="ebb2b-155">Si está actualizando un mensaje de correo electrónico, vea [de correo electrónico las propiedades y los elementos de EWS en Exchange](email-properties-and-elements-in-ews-in-exchange.md) para obtener una lista de propiedades del mensaje de correo electrónico puede escribir.</span><span class="sxs-lookup"><span data-stu-id="ebb2b-155">If you're updating an email message, see [Email properties and elements in EWS in Exchange](email-properties-and-elements-in-ews-in-exchange.md) for a list of writable email message properties.</span></span> <span data-ttu-id="ebb2b-156">Para enviar un borrador de mensaje después de que lo haya actualizado, vea [Enviar un borrador de mensaje de correo electrónico mediante el uso de EWS](how-to-send-email-messages-by-using-ews-in-exchange.md#bk_senddraftews).</span><span class="sxs-lookup"><span data-stu-id="ebb2b-156">To send a draft message after you've updated it, see [Send a draft email message by using EWS](how-to-send-email-messages-by-using-ews-in-exchange.md#bk_senddraftews).</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="ebb2b-157">En esta sección</span><span class="sxs-lookup"><span data-stu-id="ebb2b-157">In this section</span></span>
<span data-ttu-id="ebb2b-158"><a name="bk_inthissection"> </a></span><span class="sxs-lookup"><span data-stu-id="ebb2b-158"></span></span>

- [<span data-ttu-id="ebb2b-159">Correo electrónico de las propiedades y los elementos de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="ebb2b-159">Email properties and elements in EWS in Exchange</span></span>](email-properties-and-elements-in-ews-in-exchange.md)
    
- [<span data-ttu-id="ebb2b-160">Enviar mensajes de correo electrónico mediante el uso de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="ebb2b-160">Send email messages by using EWS in Exchange</span></span>](how-to-send-email-messages-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="ebb2b-161">Responder a mensajes de correo electrónico mediante el uso de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="ebb2b-161">Respond to email messages by using EWS in Exchange</span></span>](how-to-respond-to-email-messages-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="ebb2b-162">Mover y copiar los mensajes de correo electrónico mediante el uso de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="ebb2b-162">Move and copy email messages by using EWS in Exchange</span></span>](how-to-move-and-copy-email-messages-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="ebb2b-163">Trabajar con las conversaciones con EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="ebb2b-163">Work with conversations by using EWS in Exchange</span></span>](how-to-work-with-conversations-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="ebb2b-164">Extraer una entidad de un mensaje de correo electrónico mediante el uso de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="ebb2b-164">Extract an entity from an email message by using EWS in Exchange</span></span>](how-to-extract-an-entity-from-an-email-message-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="ebb2b-165">Mensajes de correo electrónico de proceso por lotes mediante el uso de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="ebb2b-165">Process email messages in batches by using EWS in Exchange</span></span>](how-to-process-email-messages-in-batches-by-using-ews-in-exchange.md)
    
## <a name="see-also"></a><span data-ttu-id="ebb2b-166">Vea también</span><span class="sxs-lookup"><span data-stu-id="ebb2b-166">See also</span></span>


- [<span data-ttu-id="ebb2b-167">Desarrollo de clientes de servicios web de Exchange</span><span class="sxs-lookup"><span data-stu-id="ebb2b-167">Develop web service clients for Exchange</span></span>](develop-web-service-clients-for-exchange.md)
    
- [<span data-ttu-id="ebb2b-168">Las carpetas y elementos de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="ebb2b-168">Folders and items in EWS in Exchange</span></span>](folders-and-items-in-ews-in-exchange.md)
    
