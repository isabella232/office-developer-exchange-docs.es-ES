---
title: Mover y copiar los mensajes de correo electrónico mediante el uso de EWS en Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4771668f-5623-4397-a5c0-b75a7ba01698
description: Obtenga información sobre cómo mover y copiar los mensajes de correo electrónico mediante el uso de la API administrada de EWS o EWS en Exchange.
ms.openlocfilehash: 44d5834176b55ad041befbad2230b8b507a12ecc
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/28/2018
ms.locfileid: "21353472"
---
# <a name="move-and-copy-email-messages-by-using-ews-in-exchange"></a><span data-ttu-id="ab1e3-103">Mover y copiar los mensajes de correo electrónico mediante el uso de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="ab1e3-103">Move and copy email messages by using EWS in Exchange</span></span>

<span data-ttu-id="ab1e3-104">Obtenga información sobre cómo mover y copiar los mensajes de correo electrónico mediante el uso de la API administrada de EWS o EWS en Exchange.</span><span class="sxs-lookup"><span data-stu-id="ab1e3-104">Learn how to move and copy email messages by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="ab1e3-105">Puede usar la API administrada de EWS o EWS para mover y copiar los mensajes en un buzón de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="ab1e3-105">You can use the EWS Managed API or EWS to move and copy email messages in a mailbox.</span></span>
  
<span data-ttu-id="ab1e3-106">**La tabla 1. Métodos de la API administrada de EWS y las operaciones de EWS para mover y copiar mensajes de correo electrónico**</span><span class="sxs-lookup"><span data-stu-id="ab1e3-106">**Table 1. EWS Managed API methods and EWS operations for moving and copying email messages**</span></span>

|<span data-ttu-id="ab1e3-107">**Tarea**</span><span class="sxs-lookup"><span data-stu-id="ab1e3-107">**Task**</span></span>|<span data-ttu-id="ab1e3-108">**Método de la API administrada de EWS**</span><span class="sxs-lookup"><span data-stu-id="ab1e3-108">**EWS Managed API method**</span></span>|<span data-ttu-id="ab1e3-109">**Operación de EWS**</span><span class="sxs-lookup"><span data-stu-id="ab1e3-109">**EWS operation**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ab1e3-110">Mover un mensaje de correo electrónico</span><span class="sxs-lookup"><span data-stu-id="ab1e3-110">Move an email message</span></span>  <br/> |[<span data-ttu-id="ab1e3-111">EmailMessage.Move</span><span class="sxs-lookup"><span data-stu-id="ab1e3-111">EmailMessage.Move</span></span>](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.emailmessage.move%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="ab1e3-112">MoveItem</span><span class="sxs-lookup"><span data-stu-id="ab1e3-112">MoveItem</span></span>](http://msdn.microsoft.com/library/dcf40fa7-7796-4a5c-bf5b-7a509a18d208%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="ab1e3-113">Copiar un mensaje de correo electrónico</span><span class="sxs-lookup"><span data-stu-id="ab1e3-113">Copy an email message</span></span>  <br/> |[<span data-ttu-id="ab1e3-114">EmailMessage.Copy</span><span class="sxs-lookup"><span data-stu-id="ab1e3-114">EmailMessage.Copy</span></span>](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.emailmessage.copy%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="ab1e3-115">CopyItem</span><span class="sxs-lookup"><span data-stu-id="ab1e3-115">CopyItem</span></span>](http://msdn.microsoft.com/library/bcc68f9e-d511-4c29-bba6-ed535524624a%28Office.15%29.aspx) <br/> |
   
<span data-ttu-id="ab1e3-116">Es importante tener en cuenta que al mover o copiar un mensaje de correo electrónico en una carpeta diferente, se crea un nuevo elemento en la nueva carpeta con un identificador de elemento único, y se elimina el mensaje original.</span><span class="sxs-lookup"><span data-stu-id="ab1e3-116">It's important to note that when you move or copy an email message into a different folder, a new item is created in the new folder with a unique item ID, and the original message is deleted.</span></span> <span data-ttu-id="ab1e3-117">Si está mover o copiar un mensaje de correo electrónico entre dos carpetas en el mismo buzón, se devuelve el nuevo elemento en la respuesta, que le proporciona acceso para el nuevo identificador de elemento.</span><span class="sxs-lookup"><span data-stu-id="ab1e3-117">If you're moving or copying an email message between two folders in the same mailbox, the new item is returned in the response, which gives you access to the new item ID.</span></span> <span data-ttu-id="ab1e3-118">Sin embargo, si va a mover o copiar un mensaje de correo electrónico entre dos buzones o entre un buzón de correo y una carpeta pública, el nuevo elemento no se devuelve en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ab1e3-118">However, if you're moving or copying an email message between two mailboxes or between a mailbox and a public folder, the new item is not returned in the response.</span></span> <span data-ttu-id="ab1e3-119">Para obtener acceso a los mensajes que se ha movido en esa situación, utilice el método de la API administrada de EWS [FindItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) u operación de EWS [FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) , [crear una definición de propiedad extendida](properties-and-extended-properties-in-ews-in-exchange.md) para la propiedad [PidTagSearchKey](http://msdn.microsoft.com/en-us/library/cc839918.aspx) (0x300B0102), o crear y establecer un ampliado personalizado (propiedad) y, a continuación, busque la propiedad extendida personalizada en la nueva carpeta.</span><span class="sxs-lookup"><span data-stu-id="ab1e3-119">To access the moved message in that scenario, use the EWS Managed API [FindItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) method or EWS [FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) operation, [create an extended property definition](properties-and-extended-properties-in-ews-in-exchange.md) for the [PidTagSearchKey](http://msdn.microsoft.com/en-us/library/cc839918.aspx) (0x300B0102) property, or create and set a custom extended property and then search for the custom extended property in the new folder.</span></span> 
  
<span data-ttu-id="ab1e3-120">Eliminación de un mensaje de correo electrónico es diferente de mover un elemento a la carpeta Elementos eliminados.</span><span class="sxs-lookup"><span data-stu-id="ab1e3-120">Deleting an email message is different than moving an item to the Deleted Items folder.</span></span> <span data-ttu-id="ab1e3-121">Si usa el método de la API administrada de EWS [Item.Delete](http://msdn.microsoft.com/en-us/library/office/dd635072%28v=exchg.80%29.aspx) o la operación de EWS [DeleteItem](../web-service-reference/deleteitem-operation.md) , se quita el elemento especificado en la solicitud de la carpeta original y se coloca una copia en la carpeta Elementos eliminados con un nuevo identificador de elemento.</span><span class="sxs-lookup"><span data-stu-id="ab1e3-121">If you use the EWS Managed API [Item.Delete](http://msdn.microsoft.com/en-us/library/office/dd635072%28v=exchg.80%29.aspx) method or the EWS [DeleteItem](../web-service-reference/deleteitem-operation.md) operation, the item specified in the request is removed from the original folder, and a copy is placed in the Deleted Items folder with a new item ID.</span></span> <span data-ttu-id="ab1e3-122">A diferencia de al mover o copiar cualquier elemento, el nuevo elemento no se devuelve en la respuesta de la operación **DeleteItem** o en el método **Delete** .</span><span class="sxs-lookup"><span data-stu-id="ab1e3-122">Unlike when you move or copy any item, the new item is not returned in the **Delete** method or the **DeleteItem** operation response.</span></span> <span data-ttu-id="ab1e3-123">Los pasos implicados en la [eliminación de un correo electrónico mediante el uso de la API administrada de EWS](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_deleteewsma) o [EWS](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_deleteews) son los mismos que los para eliminar cualquier elemento genérico desde el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="ab1e3-123">The steps involved in [deleting an email by using the EWS Managed API](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_deleteewsma) or [EWS](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_deleteews) are the same as those for deleting any generic item from the Exchange store.</span></span> 
  
## <a name="move-an-email-message-by-using-the-ews-managed-api"></a><span data-ttu-id="ab1e3-124">Mover un mensaje de correo electrónico mediante el uso de la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="ab1e3-124">Move an email message by using the EWS Managed API</span></span>
<span data-ttu-id="ab1e3-125"><a name="bk_moveewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="ab1e3-125"></span></span>

<span data-ttu-id="ab1e3-126">En el ejemplo de código siguiente se muestra cómo utilizar el método [EmailMessage.Move](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.emailmessage.move%28v=exchg.80%29.aspx) para mover un mensaje de correo electrónico existente de una carpeta a otra.</span><span class="sxs-lookup"><span data-stu-id="ab1e3-126">The following code example shows how to use the [EmailMessage.Move](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.emailmessage.move%28v=exchg.80%29.aspx) method to move an existing email message from one folder to another.</span></span> 
  
<span data-ttu-id="ab1e3-127">En este ejemplo se supone que **servicio** es un objeto [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) válido, y ese **ItemId** es el [identificador](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) de mensaje de correo electrónico para mover o copiar.</span><span class="sxs-lookup"><span data-stu-id="ab1e3-127">This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object, and that **ItemId** is the [Id](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) of the email message to move or copy.</span></span> 
  
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

## <a name="move-an-email-message-by-using-ews"></a><span data-ttu-id="ab1e3-128">Mover un mensaje de correo electrónico mediante el uso de EWS</span><span class="sxs-lookup"><span data-stu-id="ab1e3-128">Move an email message by using EWS</span></span>
<span data-ttu-id="ab1e3-129"><a name="bk_moveews"> </a></span><span class="sxs-lookup"><span data-stu-id="ab1e3-129"></span></span>

<span data-ttu-id="ab1e3-130">En el ejemplo de código siguiente se muestra cómo usar la operación [MoveItem](http://msdn.microsoft.com/library/dcf40fa7-7796-4a5c-bf5b-7a509a18d208%28Office.15%29.aspx) para mover un mensaje de correo electrónico a la carpeta correo electrónico no deseado.</span><span class="sxs-lookup"><span data-stu-id="ab1e3-130">The following code example shows how to use the [MoveItem](http://msdn.microsoft.com/library/dcf40fa7-7796-4a5c-bf5b-7a509a18d208%28Office.15%29.aspx) operation to move an email message to the Junk Email folder.</span></span> 
  
<span data-ttu-id="ab1e3-131">También es la solicitud XML que se envía por la API administrada de EWS al llamar al método [mover](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.emailmessage.move%28v=exchg.80%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="ab1e3-131">This is also the XML request that is sent by the EWS Managed API when calling the [Move](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.emailmessage.move%28v=exchg.80%29.aspx) method.</span></span> <span data-ttu-id="ab1e3-132">Los valores de algunos elementos y atributos se han abreviado para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="ab1e3-132">The values of some attributes and elements have been shortened for readability.</span></span> 
  
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

<span data-ttu-id="ab1e3-133">El servidor responde a la solicitud de **MoveItem** con un mensaje de [MoveItemResponse](http://msdn.microsoft.com/library/77be5104-1e09-4d50-abec-4fadb3a230e5%28Office.15%29.aspx) que incluye un valor [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) de **NoError**, que indica que el mensaje de correo electrónico se ha movido correctamente.</span><span class="sxs-lookup"><span data-stu-id="ab1e3-133">The server responds to the **MoveItem** request with a [MoveItemResponse](http://msdn.microsoft.com/library/77be5104-1e09-4d50-abec-4fadb3a230e5%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) value of **NoError**, which indicates that the email message was moved successfully.</span></span> <span data-ttu-id="ab1e3-134">La respuesta incluye también la **ItemId** para el mensaje de correo electrónico en la nueva carpeta, lo que es importante para almacenar porque la **ItemId** es distinto en la nueva carpeta.</span><span class="sxs-lookup"><span data-stu-id="ab1e3-134">The response also includes the **ItemId** for the email message in the new folder, which is important to store because the **ItemId** is different in the new folder.</span></span> 
  
## <a name="copy-an-email-message-by-using-the-ews-managed-api"></a><span data-ttu-id="ab1e3-135">Copiar un mensaje de correo electrónico mediante el uso de la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="ab1e3-135">Copy an email message by using the EWS Managed API</span></span>
<span data-ttu-id="ab1e3-136"><a name="bk_copyewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="ab1e3-136"></span></span>

<span data-ttu-id="ab1e3-137">En el ejemplo de código siguiente se muestra cómo utilizar el método [EmailMessage.Copy](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.emailmessage.copy%28v=exchg.80%29.aspx) para copiar un mensaje de correo electrónico existente de una carpeta a otra.</span><span class="sxs-lookup"><span data-stu-id="ab1e3-137">The following code example shows how to use the [EmailMessage.Copy](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.emailmessage.copy%28v=exchg.80%29.aspx) method to copy an existing email message from one folder to another.</span></span> 
  
<span data-ttu-id="ab1e3-138">En este ejemplo se supone que **servicio** es un objeto [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) válido, y ese **ItemId** es el [identificador](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) de mensaje de correo electrónico para copiar.</span><span class="sxs-lookup"><span data-stu-id="ab1e3-138">This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object, and that **ItemId** is the [Id](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) of the email message to copy.</span></span> <span data-ttu-id="ab1e3-139">Los valores de algunos parámetros se han abreviado para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="ab1e3-139">The values of some parameters have been shortened for readability.</span></span> 
  
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

## <a name="copy-an-email-message-by-using-ews"></a><span data-ttu-id="ab1e3-140">Copiar un mensaje de correo electrónico mediante el uso de EWS</span><span class="sxs-lookup"><span data-stu-id="ab1e3-140">Copy an email message by using EWS</span></span>
<span data-ttu-id="ab1e3-141"><a name="bk_copyews"> </a></span><span class="sxs-lookup"><span data-stu-id="ab1e3-141"></span></span>

<span data-ttu-id="ab1e3-142">En el ejemplo de código siguiente se muestra cómo utilizar la operación [CopyItem](http://msdn.microsoft.com/library/bcc68f9e-d511-4c29-bba6-ed535524624a%28Office.15%29.aspx) para copiar un mensaje de correo electrónico a una carpeta diferente en el mismo buzón mediante el envío del [ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) del mensaje de correo electrónico para mover y especificar la carpeta de destino en la [ToFolderId ](http://msdn.microsoft.com/library/bd6a4265-ad40-43f6-bcc4-0bf5df4e984c%28Office.15%29.aspx)elemento.</span><span class="sxs-lookup"><span data-stu-id="ab1e3-142">The following code example shows how to use the [CopyItem](http://msdn.microsoft.com/library/bcc68f9e-d511-4c29-bba6-ed535524624a%28Office.15%29.aspx) operation to copy an email message to different folder in the same mailbox by sending the [ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) of the email message to move, and specifying the destination folder in the [ToFolderId](http://msdn.microsoft.com/library/bd6a4265-ad40-43f6-bcc4-0bf5df4e984c%28Office.15%29.aspx) element.</span></span> 
  
<span data-ttu-id="ab1e3-143">También es la solicitud XML que se envía por la API administrada de EWS al llamar al método de [copia](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.emailmessage.copy%28v=exchg.80%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="ab1e3-143">This is also the XML request that is sent by the EWS Managed API when calling the [Copy](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.emailmessage.copy%28v=exchg.80%29.aspx) method.</span></span> <span data-ttu-id="ab1e3-144">Los valores de algunos elementos y atributos se han abreviado para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="ab1e3-144">The values of some attributes and elements have been shortened for readability.</span></span> 
  
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

<span data-ttu-id="ab1e3-145">El servidor responde a la solicitud de **CopyItem** con un mensaje de [CopyItemResponse](http://msdn.microsoft.com/library/ae402bc1-4589-45e0-a929-f368c916a7e4%28Office.15%29.aspx) que incluye un valor [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) de **NoError**, lo que indica que el mensaje de correo electrónico se ha copiado correctamente.</span><span class="sxs-lookup"><span data-stu-id="ab1e3-145">The server responds to the **CopyItem** request with a [CopyItemResponse](http://msdn.microsoft.com/library/ae402bc1-4589-45e0-a929-f368c916a7e4%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) value of **NoError**, which indicates that the email message was copied successfully.</span></span> <span data-ttu-id="ab1e3-146">La respuesta incluye también la **ItemId** para el mensaje de correo electrónico en la nueva carpeta, lo que es importante para almacenar porque la **ItemId** es distinto en la nueva carpeta.</span><span class="sxs-lookup"><span data-stu-id="ab1e3-146">The response also includes the **ItemId** for the email message in the new folder, which is important to store because the **ItemId** is different in the new folder.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ab1e3-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="ab1e3-147">See also</span></span>


- [<span data-ttu-id="ab1e3-148">Correo electrónico y EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="ab1e3-148">Email and EWS in Exchange</span></span>](email-and-ews-in-exchange.md)
    
- [<span data-ttu-id="ab1e3-149">Enviar mensajes de correo electrónico mediante el uso de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="ab1e3-149">Send email messages by using EWS in Exchange</span></span>](how-to-send-email-messages-by-using-ews-in-exchange.md)
    

