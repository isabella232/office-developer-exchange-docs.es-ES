---
title: Mover y copiar mensajes de correo electrónico mediante EWS en Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: 4771668f-5623-4397-a5c0-b75a7ba01698
description: Obtenga información sobre cómo mover y copiar mensajes de correo electrónico mediante la API administrada de EWS o EWS en Exchange.
localization_priority: Priority
ms.openlocfilehash: d13e84648f194dd4f431cf128396daf016addb22
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44527939"
---
# <a name="move-and-copy-email-messages-by-using-ews-in-exchange"></a><span data-ttu-id="2439c-103">Mover y copiar mensajes de correo electrónico mediante EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="2439c-103">Move and copy email messages by using EWS in Exchange</span></span>

<span data-ttu-id="2439c-104">Obtenga información sobre cómo mover y copiar mensajes de correo electrónico mediante la API administrada de EWS o EWS en Exchange.</span><span class="sxs-lookup"><span data-stu-id="2439c-104">Learn how to move and copy email messages by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="2439c-105">Puede usar la API administrada de EWS o EWS para mover y copiar mensajes de correo electrónico en un buzón.</span><span class="sxs-lookup"><span data-stu-id="2439c-105">You can use the EWS Managed API or EWS to move and copy email messages in a mailbox.</span></span>
  
<span data-ttu-id="2439c-106">**Tabla 1. Métodos de API administrada de EWS y operaciones EWS para mover y copiar mensajes de correo electrónico**</span><span class="sxs-lookup"><span data-stu-id="2439c-106">**Table 1. EWS Managed API methods and EWS operations for moving and copying email messages**</span></span>

|<span data-ttu-id="2439c-107">**Tarea**</span><span class="sxs-lookup"><span data-stu-id="2439c-107">**Task**</span></span>|<span data-ttu-id="2439c-108">**Método de la API administrada de EWS**</span><span class="sxs-lookup"><span data-stu-id="2439c-108">**EWS Managed API method**</span></span>|<span data-ttu-id="2439c-109">**Operación de EWS**</span><span class="sxs-lookup"><span data-stu-id="2439c-109">**EWS operation**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="2439c-110">Mover un mensaje de correo electrónico</span><span class="sxs-lookup"><span data-stu-id="2439c-110">Move an email message</span></span>  <br/> |[<span data-ttu-id="2439c-111">EmailMessage. Move</span><span class="sxs-lookup"><span data-stu-id="2439c-111">EmailMessage.Move</span></span>](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.emailmessage.move%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="2439c-112">MoveItem</span><span class="sxs-lookup"><span data-stu-id="2439c-112">MoveItem</span></span>](https://msdn.microsoft.com/library/dcf40fa7-7796-4a5c-bf5b-7a509a18d208%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="2439c-113">Copiar un mensaje de correo electrónico</span><span class="sxs-lookup"><span data-stu-id="2439c-113">Copy an email message</span></span>  <br/> |[<span data-ttu-id="2439c-114">EmailMessage. Copy</span><span class="sxs-lookup"><span data-stu-id="2439c-114">EmailMessage.Copy</span></span>](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.emailmessage.copy%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="2439c-115">CopyItem</span><span class="sxs-lookup"><span data-stu-id="2439c-115">CopyItem</span></span>](https://msdn.microsoft.com/library/bcc68f9e-d511-4c29-bba6-ed535524624a%28Office.15%29.aspx) <br/> |
   
<span data-ttu-id="2439c-116">Es importante tener en cuenta que cuando se mueve o se copia un mensaje de correo electrónico en una carpeta diferente, se crea un nuevo elemento en la nueva carpeta con un identificador de elemento único y se elimina el mensaje original.</span><span class="sxs-lookup"><span data-stu-id="2439c-116">It's important to note that when you move or copy an email message into a different folder, a new item is created in the new folder with a unique item ID, and the original message is deleted.</span></span> <span data-ttu-id="2439c-117">Si está moviendo o copiando un mensaje de correo electrónico entre dos carpetas en el mismo buzón, el nuevo elemento se devuelve en la respuesta, lo que proporciona acceso al nuevo identificador de elemento.</span><span class="sxs-lookup"><span data-stu-id="2439c-117">If you're moving or copying an email message between two folders in the same mailbox, the new item is returned in the response, which gives you access to the new item ID.</span></span> <span data-ttu-id="2439c-118">Sin embargo, si está moviendo o copiando un mensaje de correo electrónico entre dos buzones o entre un buzón y una carpeta pública, el nuevo elemento no se devolverá en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2439c-118">However, if you're moving or copying an email message between two mailboxes or between a mailbox and a public folder, the new item is not returned in the response.</span></span> <span data-ttu-id="2439c-119">Para obtener acceso al mensaje movido en ese escenario, use el método [FindItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) de la API administrada EWS o la operación de [FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) de EWS, [cree una definición de propiedad](properties-and-extended-properties-in-ews-in-exchange.md) extendida para la propiedad [PidTagSearchKey](https://msdn.microsoft.com/library/cc839918.aspx) (0x300B0102) o cree y establezca una propiedad extendida personalizada y, a continuación, busque la propiedad extendida personalizada en la nueva carpeta.</span><span class="sxs-lookup"><span data-stu-id="2439c-119">To access the moved message in that scenario, use the EWS Managed API [FindItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) method or EWS [FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) operation, [create an extended property definition](properties-and-extended-properties-in-ews-in-exchange.md) for the [PidTagSearchKey](https://msdn.microsoft.com/library/cc839918.aspx) (0x300B0102) property, or create and set a custom extended property and then search for the custom extended property in the new folder.</span></span> 
  
<span data-ttu-id="2439c-120">La eliminación de un mensaje de correo electrónico es diferente de mover un elemento a la carpeta elementos eliminados.</span><span class="sxs-lookup"><span data-stu-id="2439c-120">Deleting an email message is different than moving an item to the Deleted Items folder.</span></span> <span data-ttu-id="2439c-121">Si usa el método [Item. Delete](https://msdn.microsoft.com/library/office/dd635072%28v=exchg.80%29.aspx) de la API administrada EWS o la operación de la aplicación [DeleteItem](../web-service-reference/deleteitem-operation.md) de EWS, el elemento especificado en la solicitud se quita de la carpeta original y se coloca una copia en la carpeta elementos ELIMINAdos con un identificador de elemento nuevo.</span><span class="sxs-lookup"><span data-stu-id="2439c-121">If you use the EWS Managed API [Item.Delete](https://msdn.microsoft.com/library/office/dd635072%28v=exchg.80%29.aspx) method or the EWS [DeleteItem](../web-service-reference/deleteitem-operation.md) operation, the item specified in the request is removed from the original folder, and a copy is placed in the Deleted Items folder with a new item ID.</span></span> <span data-ttu-id="2439c-122">A diferencia de cuando se mueve o se copia un elemento, el nuevo elemento no se devuelve en el método **Delete** o la respuesta de la operación **DeleteItem** .</span><span class="sxs-lookup"><span data-stu-id="2439c-122">Unlike when you move or copy any item, the new item is not returned in the **Delete** method or the **DeleteItem** operation response.</span></span> <span data-ttu-id="2439c-123">Los pasos necesarios para [eliminar un correo electrónico mediante la API administrada de EWS](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_deleteewsma) o [EWS](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_deleteews) son los mismos que para eliminar cualquier elemento genérico del almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="2439c-123">The steps involved in [deleting an email by using the EWS Managed API](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_deleteewsma) or [EWS](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_deleteews) are the same as those for deleting any generic item from the Exchange store.</span></span> 
  
## <a name="move-an-email-message-by-using-the-ews-managed-api"></a><span data-ttu-id="2439c-124">Mover un mensaje de correo electrónico mediante la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="2439c-124">Move an email message by using the EWS Managed API</span></span>
<span data-ttu-id="2439c-125"><a name="bk_moveewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="2439c-125"><a name="bk_moveewsma"> </a></span></span>

<span data-ttu-id="2439c-126">En el ejemplo de código siguiente se muestra cómo usar el método [EmailMessage. Move](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.emailmessage.move%28v=exchg.80%29.aspx) para mover un mensaje de correo electrónico existente de una carpeta a otra.</span><span class="sxs-lookup"><span data-stu-id="2439c-126">The following code example shows how to use the [EmailMessage.Move](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.emailmessage.move%28v=exchg.80%29.aspx) method to move an existing email message from one folder to another.</span></span> 
  
<span data-ttu-id="2439c-127">En este ejemplo se supone que el **servicio** es un objeto [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) válido y que **Itemid** es el [identificador](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) del mensaje de correo electrónico que se va a mover o copiar.</span><span class="sxs-lookup"><span data-stu-id="2439c-127">This example assumes that **service** is a valid [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object, and that **ItemId** is the [Id](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) of the email message to move or copy.</span></span> 
  
```cs
// As a best practice, limit the properties returned by the Bind method to only those that are required.
PropertySet propSet = new PropertySet(BasePropertySet.IdOnly, EmailMessageSchema.Subject, EmailMessageSchema.ParentFolderId);
// Bind to the existing item by using the ItemId.
// This method call results in a GetItem call to EWS.
EmailMessage beforeMessage = EmailMessage.Bind(service, ItemId, propSet);
// Move the specified mail to the JunkEmail folder and store the returned item.
Item item = beforeMessage.Move(WellKnownFolderName.JunkEmail);
// Check that the item was moved by binding to the moved email message 
// and retrieving the new ParentFolderId.
// This method call results in a GetItem call to EWS.
EmailMessage movedMessage = EmailMessage.Bind(service, item.Id, propSet);
Console.WriteLine("An email message with the subject '" + beforeMessage.Subject + "' has been moved from the '" + beforeMessage.ParentFolderId + "' folder to the '" + movedMessage.ParentFolderId + "' folder.");
```

## <a name="move-an-email-message-by-using-ews"></a><span data-ttu-id="2439c-128">Mover un mensaje de correo electrónico mediante EWS</span><span class="sxs-lookup"><span data-stu-id="2439c-128">Move an email message by using EWS</span></span>
<span data-ttu-id="2439c-129"><a name="bk_moveews"> </a></span><span class="sxs-lookup"><span data-stu-id="2439c-129"><a name="bk_moveews"> </a></span></span>

<span data-ttu-id="2439c-130">En el siguiente ejemplo de código se muestra cómo usar la operación [MoveItem](https://msdn.microsoft.com/library/dcf40fa7-7796-4a5c-bf5b-7a509a18d208%28Office.15%29.aspx) para mover un mensaje de correo electrónico a la carpeta de correo electrónico no deseado.</span><span class="sxs-lookup"><span data-stu-id="2439c-130">The following code example shows how to use the [MoveItem](https://msdn.microsoft.com/library/dcf40fa7-7796-4a5c-bf5b-7a509a18d208%28Office.15%29.aspx) operation to move an email message to the Junk Email folder.</span></span> 
  
<span data-ttu-id="2439c-131">Esta es también la solicitud XML que la API administrada de EWS envía al llamar al método [Move](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.emailmessage.move%28v=exchg.80%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="2439c-131">This is also the XML request that is sent by the EWS Managed API when calling the [Move](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.emailmessage.move%28v=exchg.80%29.aspx) method.</span></span> <span data-ttu-id="2439c-132">Los valores de algunos atributos y elementos se han abreviado para facilitar su lectura.</span><span class="sxs-lookup"><span data-stu-id="2439c-132">The values of some attributes and elements have been shortened for readability.</span></span> 
  
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
    <m:MoveItem>
      <m:ToFolderId>
        <t:DistinguishedFolderId Id="junkemail" />
      </m:ToFolderId>
      <m:ItemIds>
        <t:ItemId Id="AfwDoAAA="
                  ChangeKey="CQAAABYAAAApjGm7TnMWQ5TzjbhziLL0AAF25sM1" />
      </m:ItemIds>
    </m:MoveItem>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="2439c-133">El servidor responde a la solicitud **MoveItem** con un mensaje [MoveItemResponse](https://msdn.microsoft.com/library/77be5104-1e09-4d50-abec-4fadb3a230e5%28Office.15%29.aspx) que incluye un valor [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) de **NoError**, que indica que el mensaje de correo electrónico se ha movido correctamente.</span><span class="sxs-lookup"><span data-stu-id="2439c-133">The server responds to the **MoveItem** request with a [MoveItemResponse](https://msdn.microsoft.com/library/77be5104-1e09-4d50-abec-4fadb3a230e5%28Office.15%29.aspx) message that includes a [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) value of **NoError**, which indicates that the email message was moved successfully.</span></span> <span data-ttu-id="2439c-134">La respuesta también incluye el **Itemid** del mensaje de correo electrónico en la nueva carpeta, que es importante almacenar porque **Itemid** es diferente en la nueva carpeta.</span><span class="sxs-lookup"><span data-stu-id="2439c-134">The response also includes the **ItemId** for the email message in the new folder, which is important to store because the **ItemId** is different in the new folder.</span></span> 
  
## <a name="copy-an-email-message-by-using-the-ews-managed-api"></a><span data-ttu-id="2439c-135">Copiar un mensaje de correo electrónico mediante la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="2439c-135">Copy an email message by using the EWS Managed API</span></span>
<span data-ttu-id="2439c-136"><a name="bk_copyewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="2439c-136"><a name="bk_copyewsma"> </a></span></span>

<span data-ttu-id="2439c-137">En el siguiente ejemplo de código se muestra cómo usar el método [EmailMessage. Copy](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.emailmessage.copy%28v=exchg.80%29.aspx) para copiar un mensaje de correo electrónico existente de una carpeta a otra.</span><span class="sxs-lookup"><span data-stu-id="2439c-137">The following code example shows how to use the [EmailMessage.Copy](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.emailmessage.copy%28v=exchg.80%29.aspx) method to copy an existing email message from one folder to another.</span></span> 
  
<span data-ttu-id="2439c-138">En este ejemplo se supone que el **servicio** es un objeto [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) válido y que **Itemid** es el [identificador](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) del mensaje de correo electrónico que se va a copiar.</span><span class="sxs-lookup"><span data-stu-id="2439c-138">This example assumes that **service** is a valid [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object, and that **ItemId** is the [Id](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) of the email message to copy.</span></span> <span data-ttu-id="2439c-139">Los valores de algunos parámetros se han abreviado para facilitar su lectura.</span><span class="sxs-lookup"><span data-stu-id="2439c-139">The values of some parameters have been shortened for readability.</span></span> 
  
```cs
// As a best practice, limit the properties returned by the Bind method to only those that are required.
PropertySet propSet = new PropertySet(BasePropertySet.IdOnly, EmailMessageSchema.Subject, EmailMessageSchema.ParentFolderId);
// Bind to the existing item by using the ItemId.
// This method call results in a GetItem call to EWS.
EmailMessage originalMessage = EmailMessage.Bind(service, ItemId, propSet);
// Copy the orignal message into another folder in the mailbox and store the returned item.
Item item = originalMessage.Copy("epQ/3AAA=");
// Check that the item was copied by binding to the copied email message 
// and retrieving the new ParentFolderId.
// This method call results in a GetItem call to EWS.
EmailMessage copiedMessage = EmailMessage.Bind(service, item.Id, propSet);
Console.WriteLine("An email message with the subject '" + originalMessage.Subject + "' has been copied from the '" + originalMessage.ParentFolderId + "' folder to the '" + copiedMessage.ParentFolderId + "' folder.");
```

## <a name="copy-an-email-message-by-using-ews"></a><span data-ttu-id="2439c-140">Copiar un mensaje de correo electrónico mediante EWS</span><span class="sxs-lookup"><span data-stu-id="2439c-140">Copy an email message by using EWS</span></span>
<span data-ttu-id="2439c-141"><a name="bk_copyews"> </a></span><span class="sxs-lookup"><span data-stu-id="2439c-141"><a name="bk_copyews"> </a></span></span>

<span data-ttu-id="2439c-142">En el siguiente ejemplo de código se muestra cómo usar la operación [CopyItem](https://msdn.microsoft.com/library/bcc68f9e-d511-4c29-bba6-ed535524624a%28Office.15%29.aspx) para copiar un mensaje de correo electrónico en una carpeta diferente del mismo buzón enviando el elemento [Itemid](https://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) del mensaje de correo electrónico que se va a mover y especificando la carpeta de destino en el elemento [ToFolderId](https://msdn.microsoft.com/library/bd6a4265-ad40-43f6-bcc4-0bf5df4e984c%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="2439c-142">The following code example shows how to use the [CopyItem](https://msdn.microsoft.com/library/bcc68f9e-d511-4c29-bba6-ed535524624a%28Office.15%29.aspx) operation to copy an email message to different folder in the same mailbox by sending the [ItemId](https://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) of the email message to move, and specifying the destination folder in the [ToFolderId](https://msdn.microsoft.com/library/bd6a4265-ad40-43f6-bcc4-0bf5df4e984c%28Office.15%29.aspx) element.</span></span> 
  
<span data-ttu-id="2439c-143">Esta es también la solicitud XML que la API administrada de EWS envía al llamar al método [Copy](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.emailmessage.copy%28v=exchg.80%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="2439c-143">This is also the XML request that is sent by the EWS Managed API when calling the [Copy](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.emailmessage.copy%28v=exchg.80%29.aspx) method.</span></span> <span data-ttu-id="2439c-144">Los valores de algunos atributos y elementos se han abreviado para facilitar su lectura.</span><span class="sxs-lookup"><span data-stu-id="2439c-144">The values of some attributes and elements have been shortened for readability.</span></span> 
  
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
    <m:CopyItem>
      <m:ToFolderId>
        <t:FolderId Id="pQ/3AAA=" />
      </m:ToFolderId>
      <m:ItemIds>
        <t:ItemId Id="2TSeSAAA="
                  ChangeKey="CQAAABYAAAApjGm7TnMWQ5TzjbhziLL0AAF2d+3+" />
      </m:ItemIds>
    </m:CopyItem>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="2439c-145">El servidor responde a la solicitud **CopyItem** con un mensaje [CopyItemResponse](https://msdn.microsoft.com/library/ae402bc1-4589-45e0-a929-f368c916a7e4%28Office.15%29.aspx) que incluye un valor [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) de **NoError**, que indica que el mensaje de correo electrónico se ha copiado correctamente.</span><span class="sxs-lookup"><span data-stu-id="2439c-145">The server responds to the **CopyItem** request with a [CopyItemResponse](https://msdn.microsoft.com/library/ae402bc1-4589-45e0-a929-f368c916a7e4%28Office.15%29.aspx) message that includes a [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) value of **NoError**, which indicates that the email message was copied successfully.</span></span> <span data-ttu-id="2439c-146">La respuesta también incluye el **Itemid** del mensaje de correo electrónico en la nueva carpeta, que es importante almacenar porque **Itemid** es diferente en la nueva carpeta.</span><span class="sxs-lookup"><span data-stu-id="2439c-146">The response also includes the **ItemId** for the email message in the new folder, which is important to store because the **ItemId** is different in the new folder.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2439c-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="2439c-147">See also</span></span>


- [<span data-ttu-id="2439c-148">Correo electrónico y EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="2439c-148">Email and EWS in Exchange</span></span>](email-and-ews-in-exchange.md)
    
- [<span data-ttu-id="2439c-149">Enviar mensajes de correo electrónico mediante EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="2439c-149">Send email messages by using EWS in Exchange</span></span>](how-to-send-email-messages-by-using-ews-in-exchange.md)
    

