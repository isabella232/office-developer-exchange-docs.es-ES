---
title: Eliminar los datos adjuntos mediante el uso de EWS en Exchange
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 71871ac7-ee1a-4f93-9e81-77f312d432f4
description: Obtenga información sobre cómo eliminar los datos adjuntos de elementos mediante el uso de la API administrada de EWS o EWS en Exchange.
ms.openlocfilehash: 458331f81493283efc20d24c7e2bebe0e74bbdbd
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763062"
---
# <a name="delete-attachments-by-using-ews-in-exchange"></a><span data-ttu-id="aa00b-103">Eliminar los datos adjuntos mediante el uso de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="aa00b-103">Delete attachments by using EWS in Exchange</span></span>

<span data-ttu-id="aa00b-104">Obtenga información sobre cómo eliminar los datos adjuntos de elementos mediante el uso de la API administrada de EWS o EWS en Exchange.</span><span class="sxs-lookup"><span data-stu-id="aa00b-104">Learn how to delete attachments from items by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="aa00b-105">Tiene un número de opciones de lo que respecta al eliminar el archivo y los datos adjuntos de elemento de elementos mediante el uso de la API administrada de EWS.</span><span class="sxs-lookup"><span data-stu-id="aa00b-105">You have a number of options when it comes to deleting file and item attachments from items by using the EWS Managed API.</span></span> <span data-ttu-id="aa00b-106">Puede eliminar todos los datos adjuntos del mensaje, para eliminar un nombre de archivo o eliminar por posición en la colección.</span><span class="sxs-lookup"><span data-stu-id="aa00b-106">You can delete all the attachments from the message, delete by a file name, or delete by position in the collection.</span></span> <span data-ttu-id="aa00b-107">Para cada una de estas opciones, hay un método [AttachmentCollection](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.attachmentcollection%28v=exchg.80%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="aa00b-107">For each of these options, there is an [AttachmentCollection](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.attachmentcollection%28v=exchg.80%29.aspx) method.</span></span> 
  
<span data-ttu-id="aa00b-108">Por el contrario, con la dirección URL de EWS, independientemente de si está eliminando todos los datos adjuntos de un elemento o sólo uno, la secuencia de operaciones es el misma.</span><span class="sxs-lookup"><span data-stu-id="aa00b-108">Conversely, with EWS, no matter whether you're deleting all attachments from an item or just one, the sequence of operations is same.</span></span> <span data-ttu-id="aa00b-109">A diferencia de la API administrada de EWS, EWS no incluye operaciones independientes para eliminar basándose en el nombre o la posición de la matriz de datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="aa00b-109">Unlike the EWS Managed API, EWS does not include separate operations to delete based on name or position in the attachments array.</span></span>
  
<span data-ttu-id="aa00b-110">**La tabla 1. Métodos de la API administrada de EWS y las operaciones de EWS para eliminar los datos adjuntos**</span><span class="sxs-lookup"><span data-stu-id="aa00b-110">**Table 1. EWS Managed API methods and EWS operations for deleting attachments**</span></span>

|<span data-ttu-id="aa00b-111">**Tarea**</span><span class="sxs-lookup"><span data-stu-id="aa00b-111">**Task**</span></span>|<span data-ttu-id="aa00b-112">**Método de la API administrada de EWS**</span><span class="sxs-lookup"><span data-stu-id="aa00b-112">**EWS Managed API method**</span></span>|<span data-ttu-id="aa00b-113">**Operación de EWS**</span><span class="sxs-lookup"><span data-stu-id="aa00b-113">**EWS operation**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="aa00b-114">Eliminar todos los datos adjuntos de un elemento.</span><span class="sxs-lookup"><span data-stu-id="aa00b-114">Delete all attachments from an item.</span></span>  <br/> |<span data-ttu-id="aa00b-115">[Item.Bind](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx), seguido de [AttachmentCollection.Clear](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.attachmentcollection.clear%28v=exchg.80%29.aspx), seguido de [EmailMessage.Update](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.emailmessage.update%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="aa00b-115">[Item.Bind](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx), followed by [AttachmentCollection.Clear](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.attachmentcollection.clear%28v=exchg.80%29.aspx), followed by [EmailMessage.Update](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.emailmessage.update%28v=exchg.80%29.aspx)</span></span> <br/> |<span data-ttu-id="aa00b-116">[GetItem](http://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) seguido [DeleteAttachment](http://msdn.microsoft.com/library/43d0c1cb-92ca-4399-9b3a-acb2b5c22624%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="aa00b-116">[GetItem](http://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) followed by [DeleteAttachment](http://msdn.microsoft.com/library/43d0c1cb-92ca-4399-9b3a-acb2b5c22624%28Office.15%29.aspx)</span></span> <br/> |
|<span data-ttu-id="aa00b-117">Eliminar datos adjuntos de un elemento por su nombre.</span><span class="sxs-lookup"><span data-stu-id="aa00b-117">Delete an attachment from an item by name.</span></span>  <br/> |<span data-ttu-id="aa00b-118">[Item.Bind](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx), seguido de [AttachmentCollection.Remove](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.attachmentcollection.remove%28v=exchg.80%29.aspx), seguido de [EmailMessage.Update](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.emailmessage.update%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="aa00b-118">[Item.Bind](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx), followed by [AttachmentCollection.Remove](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.attachmentcollection.remove%28v=exchg.80%29.aspx), followed by [EmailMessage.Update](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.emailmessage.update%28v=exchg.80%29.aspx)</span></span> <br/> |<span data-ttu-id="aa00b-119">[GetItem](http://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) seguido [DeleteAttachment](http://msdn.microsoft.com/library/43d0c1cb-92ca-4399-9b3a-acb2b5c22624%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="aa00b-119">[GetItem](http://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) followed by [DeleteAttachment](http://msdn.microsoft.com/library/43d0c1cb-92ca-4399-9b3a-acb2b5c22624%28Office.15%29.aspx)</span></span> <br/> |
|<span data-ttu-id="aa00b-120">Eliminar datos adjuntos de un elemento por su posición en la colección.</span><span class="sxs-lookup"><span data-stu-id="aa00b-120">Delete an attachment from an item by position in the collection.</span></span>  <br/> |<span data-ttu-id="aa00b-121">[Item.Bind](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx), seguido de [AttachmentCollection.RemoveAt](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.attachmentcollection.removeat%28v=exchg.80%29.aspx), seguido de [EmailMessage.Update](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.emailmessage.update%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="aa00b-121">[Item.Bind](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx), followed by [AttachmentCollection.RemoveAt](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.attachmentcollection.removeat%28v=exchg.80%29.aspx), followed by [EmailMessage.Update](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.emailmessage.update%28v=exchg.80%29.aspx)</span></span> <br/> |<span data-ttu-id="aa00b-122">[GetItem](http://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) seguido [DeleteAttachment](http://msdn.microsoft.com/library/43d0c1cb-92ca-4399-9b3a-acb2b5c22624%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="aa00b-122">[GetItem](http://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) followed by [DeleteAttachment](http://msdn.microsoft.com/library/43d0c1cb-92ca-4399-9b3a-acb2b5c22624%28Office.15%29.aspx)</span></span> <br/> |
   
## <a name="delete-all-attachments-from-an-email-by-using-the-ews-managed-api"></a><span data-ttu-id="aa00b-123">Eliminar todos los datos adjuntos de un correo electrónico mediante el uso de la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="aa00b-123">Delete all attachments from an email by using the EWS Managed API</span></span>
<span data-ttu-id="aa00b-124"><a name="bk_deleteattachewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="aa00b-124"></span></span>

<span data-ttu-id="aa00b-125">En el ejemplo de código siguiente se muestra cómo eliminar todos los datos adjuntos de un correo electrónico por:</span><span class="sxs-lookup"><span data-stu-id="aa00b-125">The following code example shows how to delete all attachments from an email by:</span></span>
  
1. <span data-ttu-id="aa00b-126">Con el método [EmailMessage.Bind](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) para enlazar a un mensaje de correo electrónico existente y recuperar la colección de [datos adjuntos](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.item.attachments%28v=exchg.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="aa00b-126">Using the [EmailMessage.Bind](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) method to bind to an existing email message and retrieve the collection of [Attachments](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.item.attachments%28v=exchg.80%29.aspx).</span></span>
    
2. <span data-ttu-id="aa00b-127">Con el método [AttachmentCollection.Clear](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.attachmentcollection.clear%28v=exchg.80%29.aspx) para eliminar todos los datos adjuntos de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="aa00b-127">Using the [AttachmentCollection.Clear](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.attachmentcollection.clear%28v=exchg.80%29.aspx) method to delete all the attachments from the email.</span></span> 
    
3. <span data-ttu-id="aa00b-128">Con el método [EmailMessage.Update](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.emailmessage.update%28v=exchg.80%29.aspx) para guardar los cambios.</span><span class="sxs-lookup"><span data-stu-id="aa00b-128">Using the [EmailMessage.Update](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.emailmessage.update%28v=exchg.80%29.aspx) method to save the changes.</span></span> 
    
<span data-ttu-id="aa00b-129">En este ejemplo se da por supuesto que el **servicio** es un objeto [ExchangeService](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) válido, **itemId** es el [ItemId](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.itemid%28v=exchg.80%29.aspx) del mensaje desde el que se eliminarán los datos adjuntos, y que se ha autenticado el usuario a un servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="aa00b-129">This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object, **itemId** is the [ItemId](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.itemid%28v=exchg.80%29.aspx) of the message from which attachments will be deleted, and that the user has been authenticated to an Exchange server.</span></span> 
  
```cs
public static void DeleteAllAttachments(ExchangeService service, ItemId itemId)
{
    // Bind to an existing message by using its item ID and requesting its attachments collection.
    // This method results in a GetItem call to EWS.
    EmailMessage message = EmailMessage.Bind(service, itemId, new PropertySet(ItemSchema.Attachments));
    // Delete all attachments from the message.
    message.Attachments.Clear();
    // Save the updated message.
    // This method results in an DeleteAttachment call to EWS.
    message.Update(ConflictResolutionMode.AlwaysOverwrite);
}
```

## <a name="delete-an-attachment-by-name-from-an-email-by-using-the-ews-managed-api"></a><span data-ttu-id="aa00b-130">Eliminar un archivo adjunto por su nombre desde un correo electrónico mediante el uso de la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="aa00b-130">Delete an attachment by name from an email by using the EWS Managed API</span></span>
<span data-ttu-id="aa00b-131"><a name="bk_deleteattachewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="aa00b-131"></span></span>

<span data-ttu-id="aa00b-132">El ejemplo de código siguiente se muestra cómo elimina un archivo adjunto por su nombre por:</span><span class="sxs-lookup"><span data-stu-id="aa00b-132">The following code example shows how delete an attachment by name by:</span></span>
  
1. <span data-ttu-id="aa00b-133">Con el método [EmailMessage.Bind](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) para enlazar a un mensaje de correo electrónico existente y recuperar la colección de [datos adjuntos](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.item.attachments%28v=exchg.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="aa00b-133">Using the [EmailMessage.Bind](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) method to bind to an existing email message and retrieve the collection of [Attachments](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.item.attachments%28v=exchg.80%29.aspx).</span></span>
    
2. <span data-ttu-id="aa00b-134">Con el método [AttachmentCollection.Remove](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.attachmentcollection.remove%28v=exchg.80%29.aspx) para eliminar un archivo adjunto denominado FileAttachment.txt.</span><span class="sxs-lookup"><span data-stu-id="aa00b-134">Using the [AttachmentCollection.Remove](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.attachmentcollection.remove%28v=exchg.80%29.aspx) method to delete an attachment named FileAttachment.txt.</span></span> 
    
3. <span data-ttu-id="aa00b-135">Con el método [EmailMessage.Update](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.emailmessage.update%28v=exchg.80%29.aspx) para guardar los cambios.</span><span class="sxs-lookup"><span data-stu-id="aa00b-135">Using the [EmailMessage.Update](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.emailmessage.update%28v=exchg.80%29.aspx) method to save the changes.</span></span> 
    
<span data-ttu-id="aa00b-136">En este ejemplo se da por supuesto que el **servicio** es un objeto [ExchangeService](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) válido, **itemId** es el [ItemId](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.itemid%28v=exchg.80%29.aspx) del mensaje desde el que se eliminarán los datos adjuntos, y que se ha autenticado el usuario a un servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="aa00b-136">This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object, **itemId** is the [ItemId](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.itemid%28v=exchg.80%29.aspx) of the message from which the attachment will be deleted, and that the user has been authenticated to an Exchange server.</span></span> 
  
```cs
public static void DeleteNamedAttachments(ExchangeService service, ItemId itemId)
{
    // Bind to an existing message by using its item ID and requesting its attachments collection.
    // This method results in a GetItem call to EWS.
    EmailMessage message = EmailMessage.Bind(service, itemId, new PropertySet(ItemSchema.Attachments));
    // Iterate through the attachments collection and delete the attachment named "FileAttachment.txt," if it exists.
    foreach (Attachment attachment in message.Attachments)
    {
        if (attachment.Name == "FileAttachment.txt")
        {
            message.Attachments.Remove(attachment);
            break;
        }
    }
    // Save the updated message.
    // This method results in an DeleteAttachment call to EWS.
    message.Update(ConflictResolutionMode.AlwaysOverwrite);
}
```

## <a name="delete-attachments-by-position-by-using-the-ews-managed-api"></a><span data-ttu-id="aa00b-137">Eliminar los datos adjuntos por posición mediante el uso de la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="aa00b-137">Delete attachments by position by using the EWS Managed API</span></span>
<span data-ttu-id="aa00b-138"><a name="bk_deleteattachewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="aa00b-138"></span></span>

<span data-ttu-id="aa00b-139">En el ejemplo de código siguiente se muestra cómo eliminar un archivo adjunto por posición por:</span><span class="sxs-lookup"><span data-stu-id="aa00b-139">The following code example shows how to delete an attachment by position by:</span></span>
  
1. <span data-ttu-id="aa00b-140">Con el método [EmailMessage.Bind](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) para enlazar a un mensaje de correo electrónico existente y recuperar la colección de [datos adjuntos](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.item.attachments%28v=exchg.80%29.aspx) y la propiedad [EmailMessage.HasAttachments](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.item.hasattachments%28v=exchg.80%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="aa00b-140">Using the [EmailMessage.Bind](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) method to bind to an existing email message and retrieve the collection of [Attachments](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.item.attachments%28v=exchg.80%29.aspx) and the [EmailMessage.HasAttachments](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.item.hasattachments%28v=exchg.80%29.aspx) property.</span></span> 
    
2. <span data-ttu-id="aa00b-141">Con el método [AttachmentCollection.Remove](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.attachmentcollection.remove%28v=exchg.80%29.aspx) para eliminar los primeros datos adjuntos en la colección.</span><span class="sxs-lookup"><span data-stu-id="aa00b-141">Using the [AttachmentCollection.Remove](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.attachmentcollection.remove%28v=exchg.80%29.aspx) method to delete the first attachment in the collection.</span></span> 
    
3. <span data-ttu-id="aa00b-142">Con el método [EmailMessage.Update](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.emailmessage.update%28v=exchg.80%29.aspx) para guardar los cambios.</span><span class="sxs-lookup"><span data-stu-id="aa00b-142">Using the [EmailMessage.Update](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.emailmessage.update%28v=exchg.80%29.aspx) method to save the changes.</span></span> 
    
<span data-ttu-id="aa00b-143">En este ejemplo se da por supuesto que el **servicio** es un objeto [ExchangeService](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) válido, **itemId** es el [ItemId](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.itemid%28v=exchg.80%29.aspx) del mensaje desde el que se eliminarán los datos adjuntos, y que se ha autenticado el usuario a un servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="aa00b-143">This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object, **itemId** is the [ItemId](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.itemid%28v=exchg.80%29.aspx) of the message from which the attachment will be deleted, and that the user has been authenticated to an Exchange server.</span></span> 
  
```cs
public static void DeleteAttachmentByPosition(ExchangeService service, ItemId itemId)
{
    // Bind to an existing message by using its item ID and requesting the HasAttachments property and the attachments collection.
    // This method results in a GetItem call to EWS.
    EmailMessage message = EmailMessage.Bind(service, itemId, new PropertySet(EmailMessageSchema.HasAttachments, ItemSchema.Attachments));
    // Remove attachments using the zero-based index position of the attachment in the attachments collection.
    if (message.HasAttachments)
    {
        message.Attachments.RemoveAt(0);
    }
    // Save the updated message.
    // This method results in an DeleteAttachment call to EWS.
    message.Update(ConflictResolutionMode.AlwaysOverwrite);
}
```

## <a name="delete-attachments-from-an-item-by-using-ews"></a><span data-ttu-id="aa00b-144">Eliminar los datos adjuntos de un elemento mediante el uso de EWS</span><span class="sxs-lookup"><span data-stu-id="aa00b-144">Delete attachments from an item by using EWS</span></span>
<span data-ttu-id="aa00b-145"><a name="bk_deleteattachewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="aa00b-145"></span></span>

<span data-ttu-id="aa00b-146">Para eliminar los datos adjuntos mediante el uso de EWS, primero debe recuperar el mensaje y la colección de datos adjuntos para determinar la [AttachmentId (GetAttachment y DeleteAttachment)](http://msdn.microsoft.com/library/4bea1cb5-0a0f-4e14-9b09-f91af8cf9899%28Office.15%29.aspx) de los datos adjuntos para eliminar.</span><span class="sxs-lookup"><span data-stu-id="aa00b-146">To delete attachments by using EWS, you first need to retrieve the message and the attachment collection to determine the [AttachmentId (GetAttachment and DeleteAttachment)](http://msdn.microsoft.com/library/4bea1cb5-0a0f-4e14-9b09-f91af8cf9899%28Office.15%29.aspx) of the attachment to delete.</span></span> <span data-ttu-id="aa00b-147">Una vez que tenga uno o más valores de **AttachmentId** para eliminar, llame a la operación [DeleteAttachment](http://msdn.microsoft.com/library/4d48e595-b98c-48e7-bbeb-cacf91d12a78%28Office.15%29.aspx) para quitar los datos adjuntos especificados desde el mensaje.</span><span class="sxs-lookup"><span data-stu-id="aa00b-147">After you have one or more **AttachmentId** values to delete, call the [DeleteAttachment](http://msdn.microsoft.com/library/4d48e595-b98c-48e7-bbeb-cacf91d12a78%28Office.15%29.aspx) operation to remove the specified attachments from the message.</span></span> 
  
<span data-ttu-id="aa00b-148">En el ejemplo de código siguiente se muestra cómo usar la operación [GetItem](http://msdn.microsoft.com/library/e8492e3b-1c8d-4b14-8070-9530f8306edd%28Office.15%29.aspx) para obtener un mensaje de correo electrónico y la colección de datos adjuntos en el mensaje.</span><span class="sxs-lookup"><span data-stu-id="aa00b-148">The following code example shows how to use the [GetItem](http://msdn.microsoft.com/library/e8492e3b-1c8d-4b14-8070-9530f8306edd%28Office.15%29.aspx) operation to get an email message and the collection of attachments on the message.</span></span> <span data-ttu-id="aa00b-149">También es la primera solicitud XML que la API administrada de EWS envía al usar la API administrada de EWS para [Eliminar todos los datos adjuntos de un correo electrónico](#bk_deleteattachewsma).</span><span class="sxs-lookup"><span data-stu-id="aa00b-149">This is also the first XML request that the EWS Managed API sends when you use the EWS Managed API to [delete all attachments from an email](#bk_deleteattachewsma).</span></span> <span data-ttu-id="aa00b-150">Los valores de algunos atributos son más cortos para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="aa00b-150">The values of some attributes are shortened for readability.</span></span>
  
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
    <m:GetItem>
      <m:ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="item:Attachments" />
        </t:AdditionalProperties>
      </m:ItemShape>
      <m:ItemIds>
        <t:ItemId Id="uqE1AAA=" />
      </m:ItemIds>
    </m:GetItem>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="aa00b-151">El servidor responde a la solicitud de **GetItem** con un mensaje de [GetItemResponse](http://msdn.microsoft.com/library/8b66de1b-26a6-476c-9585-a96059125716%28Office.15%29.aspx) que incluye un valor de [ResponseCode](http://msdn.microsoft.com/es-es/library/aa580757%28v=exchg.150%29.aspx) de **NoError**, lo que indica que se ha recuperado el correo electrónico y los valores de [AttachmentId](http://msdn.microsoft.com/library/55a5fd77-60d1-40fa-8144-770600cedc6a%28Office.15%29.aspx) de los datos adjuntos existentes.</span><span class="sxs-lookup"><span data-stu-id="aa00b-151">The server responds to the **GetItem** request with a [GetItemResponse](http://msdn.microsoft.com/library/8b66de1b-26a6-476c-9585-a96059125716%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/es-es/library/aa580757%28v=exchg.150%29.aspx) value of **NoError**, which indicates that the email was retrieved successfully, and the [AttachmentId](http://msdn.microsoft.com/library/55a5fd77-60d1-40fa-8144-770600cedc6a%28Office.15%29.aspx) values of the existing attachments.</span></span> 
  
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
    <m:GetItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
                       xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:GetItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Items>
            <t:Message>
              <t:ItemId Id="uqE1AAA="
                        ChangeKey="CQAAABYAAAAFI5DJmZv+TLtyLOLIF1S5AAAXulcd" />
              <t:Attachments>
                <t:FileAttachment>
                  <t:AttachmentId Id="IpHLObE=" />
                  <t:Name>FileAttachment.txt</t:Name>
                </t:FileAttachment>
                <t:FileAttachment>
                  <t:AttachmentId Id="QuHSSmY=" />
                  <t:Name>SecondAttachment.txt</t:Name>
                </t:FileAttachment>
                <t:FileAttachment>
                  <t:AttachmentId Id="qf2KoPo=" />
                  <t:Name>ThirdAttachment.jpg</t:Name>
                </t:FileAttachment>
                <t:FileAttachment>
                  <t:AttachmentId Id="NFQMnMc=" />
                  <t:Name>FourthAttachment.txt</t:Name>
                </t:FileAttachment>
                <t:ItemAttachment>
                  <t:AttachmentId Id="jJvbLXQ=" />
                  <t:Name>Attached Message Item</t:Name>
                </t:ItemAttachment>
              </t:Attachments>
            </t:Message>
          </m:Items>
        </m:GetItemResponseMessage>
      </m:ResponseMessages>
    </m:GetItemResponse>
  </s:Body>
</s:Envelope>
```

<span data-ttu-id="aa00b-152">Después de determinar qué datos adjuntos para eliminar, llamar a la operación [DeleteAttachment](http://msdn.microsoft.com/library/4d48e595-b98c-48e7-bbeb-cacf91d12a78%28Office.15%29.aspx) e incluir los valores de **AttachmentId** de los datos adjuntos para eliminar.</span><span class="sxs-lookup"><span data-stu-id="aa00b-152">After you determine which attachment to delete, call the [DeleteAttachment](http://msdn.microsoft.com/library/4d48e595-b98c-48e7-bbeb-cacf91d12a78%28Office.15%29.aspx) operation and include the **AttachmentId** values of the attachments to delete.</span></span> 
  
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
    <m:DeleteAttachment>
      <m:AttachmentIds>
        <t:AttachmentId Id="IpHLObE=" />
        <t:AttachmentId Id="QuHSSmY=" />
        <t:AttachmentId Id="qf2KoPo=" />
        <t:AttachmentId Id="NFQMnMc=" />
        <t:AttachmentId Id="jJvbLXQ=" />
      </m:AttachmentIds>
    </m:DeleteAttachment>
  </soap:Body>
</soap:Envelope>
```

El servidor responde a la solicitud de **DeleteAttachment** con un mensaje de [DeleteAttachmentResponse](http://msdn.microsoft.com/library/24099a88-4ab6-4bf3-8ed5-efec8e07b9b9%28Office.15%29.aspx) que incluye un valor [ResponseCode](http://msdn.microsoft.com/es-es/library/aa580757%28v=exchg.150%29.aspx) de **NoError** para cada [DeleteAttachmentResponseMessage](http://msdn.microsoft.com/library/1edb085f-1674-48e5-8ec3-42351adeac7d%28Office.15%29.aspx), lo que indica que cada dato adjunto se ha eliminado correctamente. <span data-ttu-id="aa00b-154">Los valores de algunos atributos son más cortos para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="aa00b-154">The values of some attributes are shortened for readability.</span></span>
  
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
    <m:DeleteAttachmentResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
                                xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:DeleteAttachmentResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:RootItemId RootItemId="uqE1AAA=" RootItemChangeKey="AAAXulck" />
        </m:DeleteAttachmentResponseMessage>
        <m:DeleteAttachmentResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:RootItemId RootItemId="uqE1AAA=" RootItemChangeKey="AAAXulck" />
        </m:DeleteAttachmentResponseMessage>
        <m:DeleteAttachmentResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:RootItemId RootItemId="uqE1AAA=" RootItemChangeKey="AAAXulck" />
        </m:DeleteAttachmentResponseMessage>
        <m:DeleteAttachmentResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:RootItemId RootItemId="uqE1AAA=" RootItemChangeKey="AAAXulck" />
        </m:DeleteAttachmentResponseMessage>
        <m:DeleteAttachmentResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:RootItemId RootItemId="uqE1AAA=" RootItemChangeKey="AAAXulck" />
        </m:DeleteAttachmentResponseMessage>
      </m:ResponseMessages>
    </m:DeleteAttachmentResponse>
  </s:Body>
</s:Envelope>
```

## <a name="see-also"></a><span data-ttu-id="aa00b-155">Vea también</span><span class="sxs-lookup"><span data-stu-id="aa00b-155">See also</span></span>


- [<span data-ttu-id="aa00b-156">Los datos adjuntos y EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="aa00b-156">Attachments and EWS in Exchange</span></span>](attachments-and-ews-in-exchange.md)
    
- [<span data-ttu-id="aa00b-157">Agregar datos adjuntos mediante el uso de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="aa00b-157">Add attachments by using EWS in Exchange</span></span>](how-to-add-attachments-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="aa00b-158">Obtener datos adjuntos mediante el uso de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="aa00b-158">Get attachments by using EWS in Exchange</span></span>](how-to-get-attachments-by-using-ews-in-exchange.md)
    

