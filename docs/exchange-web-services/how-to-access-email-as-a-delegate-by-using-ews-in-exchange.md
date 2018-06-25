---
title: Correo electrónico de acceso como delegado mediante el uso de EWS en Exchange
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: a8123604-c7c0-405d-a0ed-7a9b4a431bfd
description: Obtenga información sobre cómo obtener acceso a correo electrónico como un delegado mediante la API administrada de EWS o EWS en Exchange.
ms.openlocfilehash: 8331f337136426913347cf6941d64b4611922d74
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763030"
---
# <a name="access-email-as-a-delegate-by-using-ews-in-exchange"></a><span data-ttu-id="1a3f6-103">Correo electrónico de acceso como delegado mediante el uso de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="1a3f6-103">Access email as a delegate by using EWS in Exchange</span></span>

<span data-ttu-id="1a3f6-104">Obtenga información sobre cómo obtener acceso a correo electrónico como un delegado mediante la API administrada de EWS o EWS en Exchange.</span><span class="sxs-lookup"><span data-stu-id="1a3f6-104">Learn how to access email as a delegate by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="1a3f6-105">Puede usar la API administrada de EWS o EWS para dar a un usuario delegar el acceso a la carpeta Bandeja de entrada de un propietario buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="1a3f6-105">You can use the EWS Managed API or EWS to give a user delegate access to a mailbox owner's Inbox folder.</span></span> <span data-ttu-id="1a3f6-106">El delegado puede, a continuación, crear convocatorias de reunión en nombre del propietario del buzón de correo, de búsqueda para el correo electrónico y recuperar, actualizar y eliminar el correo electrónico desde bandeja del propietario buzón de correo de la de entrada, en función de sus permisos.</span><span class="sxs-lookup"><span data-stu-id="1a3f6-106">The delegate can then create meeting requests on behalf of the mailbox owner, search for email, and retrieve, update, and delete email from the mailbox owner's Inbox folder, depending on their permissions.</span></span>
  
<span data-ttu-id="1a3f6-107">Como delegado, use los mismos métodos y operaciones para tener acceso a la carpeta Bandeja de entrada de un propietario buzón de correo que usan para tener acceso a una carpeta Bandeja de entrada sin acceso delegado.</span><span class="sxs-lookup"><span data-stu-id="1a3f6-107">As a delegate, you use the same methods and operations to access a mailbox owner's Inbox folder that you use to access an Inbox folder without delegate access.</span></span> <span data-ttu-id="1a3f6-108">La diferencia principal es que se debe usar [acceso explícito](delegate-access-and-ews-in-exchange.md#bk_explicit) para buscar o crear un elemento de correo electrónico y, a continuación, después de identificar el identificador de elemento, puede usar [acceso implícito](delegate-access-and-ews-in-exchange.md#bk_implicit) para obtener, actualizar o eliminar el elemento.</span><span class="sxs-lookup"><span data-stu-id="1a3f6-108">The main difference is that you have to use [explicit access](delegate-access-and-ews-in-exchange.md#bk_explicit) to find or create an email item, and then after you identify the item ID, you can use [implicit access](delegate-access-and-ews-in-exchange.md#bk_implicit) to get, update, or delete the item.</span></span> 
  
<span data-ttu-id="1a3f6-109">**La tabla 1. Métodos de la API administrada de EWS y las operaciones de EWS para obtener acceso al correo electrónico como delegado**</span><span class="sxs-lookup"><span data-stu-id="1a3f6-109">**Table 1. EWS Managed API methods and EWS operations for accessing email as a delegate**</span></span>

|<span data-ttu-id="1a3f6-110">**Si quiere...**</span><span class="sxs-lookup"><span data-stu-id="1a3f6-110">**If you want to…**</span></span>|<span data-ttu-id="1a3f6-111">**Use este método de la API administrada de EWS...**</span><span class="sxs-lookup"><span data-stu-id="1a3f6-111">**Use this EWS Managed API method…**</span></span>|<span data-ttu-id="1a3f6-112">**Use esta operación de EWS...**</span><span class="sxs-lookup"><span data-stu-id="1a3f6-112">**Use this EWS operation…**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1a3f6-113">Crear y enviar un correo electrónico como delegado</span><span class="sxs-lookup"><span data-stu-id="1a3f6-113">Create and send an email as a delegate</span></span>  <br/> |<span data-ttu-id="1a3f6-114">[EmailMessage.Save](http://msdn.microsoft.com/en-us/library/dd635209%28v=exchg.80%29.aspx) donde el parámetro [FolderId](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) proporciona [acceso explícito](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) a la carpeta de borradores del propietario del buzón</span><span class="sxs-lookup"><span data-stu-id="1a3f6-114">[EmailMessage.Save](http://msdn.microsoft.com/en-us/library/dd635209%28v=exchg.80%29.aspx) where the [FolderId](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) parameter provides [explicit access](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) to the mailbox owner's Drafts folder</span></span>  <br/> <span data-ttu-id="1a3f6-115">[EmailMessage.SendAndSaveCopy](http://msdn.microsoft.com/en-us/library/dd634248%28v=exchg.80%29.aspx) donde el parámetro [FolderId](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) proporciona [acceso explícito](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) a la carpeta de elementos enviados del propietario del buzón</span><span class="sxs-lookup"><span data-stu-id="1a3f6-115">[EmailMessage.SendAndSaveCopy](http://msdn.microsoft.com/en-us/library/dd634248%28v=exchg.80%29.aspx) where the [FolderId](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) parameter provides [explicit access](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) to the mailbox owner's Sent Items folder</span></span>  <br/> |<span data-ttu-id="1a3f6-116">[CreateItem](http://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) donde el elemento de [buzón de correo](http://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) especifica la [EmailAddress](http://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) del propietario del buzón</span><span class="sxs-lookup"><span data-stu-id="1a3f6-116">[CreateItem](http://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) where the [Mailbox](http://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) element specifies the [EmailAddress](http://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) of the mailbox owner</span></span>  <br/> <span data-ttu-id="1a3f6-117">[SendItem](http://msdn.microsoft.com/library/a966da19-b05a-4504-ac98-91acc1667b9a%28Office.15%29.aspx) donde el elemento de [buzón de correo](http://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) especifica la [EmailAddress](http://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) del propietario del buzón</span><span class="sxs-lookup"><span data-stu-id="1a3f6-117">[SendItem](http://msdn.microsoft.com/library/a966da19-b05a-4504-ac98-91acc1667b9a%28Office.15%29.aspx) where the [Mailbox](http://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) element specifies the [EmailAddress](http://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) of the mailbox owner</span></span>  <br/> |
|<span data-ttu-id="1a3f6-118">Crear varios mensajes de correo electrónico como delegado</span><span class="sxs-lookup"><span data-stu-id="1a3f6-118">Create multiple email messages as a delegate</span></span>  <br/> |<span data-ttu-id="1a3f6-119">[ExchangeService.CreateItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.createitems%28v=exchg.80%29.aspx) donde el parámetro **FolderId** proporciona [acceso explícito](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) a la carpeta de bandeja de entrada del propietario del buzón</span><span class="sxs-lookup"><span data-stu-id="1a3f6-119">[ExchangeService.CreateItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.createitems%28v=exchg.80%29.aspx) where the **FolderId** parameter provides [explicit access](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) to the mailbox owner's Inbox folder</span></span>  <br/> |<span data-ttu-id="1a3f6-120">[CreateItem](http://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) donde el elemento de [buzón de correo](http://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) especifica la [EmailAddress](http://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) del propietario del buzón</span><span class="sxs-lookup"><span data-stu-id="1a3f6-120">[CreateItem](http://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) where the [Mailbox](http://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) element specifies the [EmailAddress](http://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) of the mailbox owner</span></span>  <br/> |
|<span data-ttu-id="1a3f6-121">Buscar o buscar un correo electrónico como delegado</span><span class="sxs-lookup"><span data-stu-id="1a3f6-121">Search for or find an email as a delegate</span></span>  <br/> |<span data-ttu-id="1a3f6-122">[ExchangeService.FindItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) donde el parámetro **FolderId** proporciona [acceso explícito](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) a la carpeta de bandeja de entrada del propietario del buzón</span><span class="sxs-lookup"><span data-stu-id="1a3f6-122">[ExchangeService.FindItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) where the **FolderId** parameter provides [explicit access](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) to the mailbox owner's Inbox folder</span></span>  <br/> |<span data-ttu-id="1a3f6-123">[FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) donde el elemento de [buzón de correo](http://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) especifica la [EmailAddress](http://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) del propietario del buzón</span><span class="sxs-lookup"><span data-stu-id="1a3f6-123">[FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) where the [Mailbox](http://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) element specifies the [EmailAddress](http://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) of the mailbox owner</span></span>  <br/> |
|<span data-ttu-id="1a3f6-124">Obtener un correo electrónico como delegado</span><span class="sxs-lookup"><span data-stu-id="1a3f6-124">Get an email as a delegate</span></span>  <br/> |[<span data-ttu-id="1a3f6-125">EmailMessage.Bind</span><span class="sxs-lookup"><span data-stu-id="1a3f6-125">EmailMessage.Bind</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="1a3f6-126">GetItem</span><span class="sxs-lookup"><span data-stu-id="1a3f6-126">GetItem</span></span>](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="1a3f6-127">Actualizar un correo electrónico como delegado</span><span class="sxs-lookup"><span data-stu-id="1a3f6-127">Update an email as a delegate</span></span>  <br/> |<span data-ttu-id="1a3f6-128">[EmailMessage.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) seguido de [EmailMessage.Update](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.update%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1a3f6-128">[EmailMessage.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) followed by [EmailMessage.Update](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.update%28v=exchg.80%29.aspx)</span></span> <br/> |<span data-ttu-id="1a3f6-129">[GetItem](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) seguido [UpdateItem](http://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1a3f6-129">[GetItem](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) followed by [UpdateItem](http://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx)</span></span> <br/> |
|<span data-ttu-id="1a3f6-130">Eliminar un correo electrónico como delegado</span><span class="sxs-lookup"><span data-stu-id="1a3f6-130">Delete an email as a delegate</span></span>  <br/> |<span data-ttu-id="1a3f6-131">[EmailMessage.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) seguido de [EmailMessage.Delete](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.delete%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1a3f6-131">[EmailMessage.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) followed by [EmailMessage.Delete](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.delete%28v=exchg.80%29.aspx)</span></span> <br/> |<span data-ttu-id="1a3f6-132">[GetItem](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) seguido [DeleteItem](http://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1a3f6-132">[GetItem](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) followed by [DeleteItem](http://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx)</span></span> <br/> |
   
<span data-ttu-id="1a3f6-133">Cuando se trabaja con mensajes de correo electrónico como delegado, tenga en cuenta lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="1a3f6-133">Keep the following things in mind when working with emails as a delegate:</span></span>
  
- <span data-ttu-id="1a3f6-134">Si sólo necesita un delegado trabajar con convocatorias de reunión y respuestas, el delegado no necesitan tener acceso a la carpeta Bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="1a3f6-134">If a delegate only needs to work with meeting requests and responses, the delegate does not need access to the Inbox folder.</span></span> <span data-ttu-id="1a3f6-135">Para obtener más información, vea [tareas de requisitos previos para obtener acceso a calendarios como delegado](how-to-access-a-calendar-as-a-delegate-by-using-ews-in-exchange.md#bk_prereq).</span><span class="sxs-lookup"><span data-stu-id="1a3f6-135">For more information, see [prerequisite tasks for accessing calendars as a delegate](how-to-access-a-calendar-as-a-delegate-by-using-ews-in-exchange.md#bk_prereq).</span></span>
    
- <span data-ttu-id="1a3f6-136">Cuando un destinatario recibe un mensaje que se ha enviado en nombre de un propietario del buzón, el remitente aparece como " *delegado* en nombre *del propietario del buzón* ".</span><span class="sxs-lookup"><span data-stu-id="1a3f6-136">When a recipient receives a message that was sent on behalf of a mailbox owner, the sender appears as " *Delegate*  on behalf of  *mailbox owner*  ."</span></span> 
    
> [!NOTE]
> <span data-ttu-id="1a3f6-137">En los ejemplos de código de este artículo, primary@contoso.com es el propietario del buzón.</span><span class="sxs-lookup"><span data-stu-id="1a3f6-137">In the code examples in this article, primary@contoso.com is the mailbox owner.</span></span> 
  
## <a name="prerequisite-tasks"></a><span data-ttu-id="1a3f6-138">Tareas de requisitos previos</span><span class="sxs-lookup"><span data-stu-id="1a3f6-138">Prerequisite tasks</span></span>
<span data-ttu-id="1a3f6-139"><a name="bk_prereq"> </a></span><span class="sxs-lookup"><span data-stu-id="1a3f6-139"></span></span>

<span data-ttu-id="1a3f6-140">Antes de que un usuario puede obtener acceso a la carpeta de bandeja de entrada del propietario del buzón como delegado, el usuario debe ser [agregado como delegado con permisos de](how-to-add-and-remove-delegates-by-using-ews-in-exchange.md) carpeta de bandeja de entrada del propietario del buzón.</span><span class="sxs-lookup"><span data-stu-id="1a3f6-140">Before a user can access the mailbox owner's Inbox folder as a delegate, the user must be [added as a delegate with permissions](how-to-add-and-remove-delegates-by-using-ews-in-exchange.md) to the mailbox owner's Inbox folder.</span></span> 
  
## <a name="create-and-send-an-email-as-a-delegate-by-using-the-ews-managed-api"></a><span data-ttu-id="1a3f6-141">Crear y enviar un correo electrónico como delegado mediante el uso de la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="1a3f6-141">Create and send an email as a delegate by using the EWS Managed API</span></span>
<span data-ttu-id="1a3f6-142"><a name="bk_createewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="1a3f6-142"></span></span>

<span data-ttu-id="1a3f6-143">La API administrada de EWS le permite usar el objeto de servicio para el usuario delegado para crear y enviar correo electrónico en nombre del propietario del buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="1a3f6-143">The EWS Managed API enables you to use the service object for the delegate user to create and send email on behalf of the mailbox owner.</span></span> <span data-ttu-id="1a3f6-144">En este ejemplo se muestra cómo utilizar el método [Save](http://msdn.microsoft.com/en-us/library/dd635209%28v=exchg.80%29.aspx) para guardar el mensaje en la carpeta de borradores del propietario del buzón y, a continuación, el método [SendAndSaveCopy](http://msdn.microsoft.com/en-us/library/dd634248%28v=exchg.80%29.aspx) para enviar el correo y guardar el mensaje en la carpeta de elementos enviados del propietario del buzón.</span><span class="sxs-lookup"><span data-stu-id="1a3f6-144">This example shows how to use the [Save](http://msdn.microsoft.com/en-us/library/dd635209%28v=exchg.80%29.aspx) method to save the message in the mailbox owner's Drafts folder, and then the [SendAndSaveCopy](http://msdn.microsoft.com/en-us/library/dd634248%28v=exchg.80%29.aspx) method to send the mail and save the message in the mailbox owner's Sent Items folder.</span></span> 
  
<span data-ttu-id="1a3f6-145">En este ejemplo se da por supuesto que **servicio** es un objeto [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) válido para el delegado y que el delegado se ha concedido los [permisos adecuados para la carpeta de bandeja de entrada, borradores y elementos enviados del propietario del buzón](how-to-set-folder-permissions-for-another-user-by-using-ews-in-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="1a3f6-145">This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object for the delegate and that the delegate has been granted the [appropriate permissions for the mailbox owner's Inbox, Drafts, and Sent Items folder](how-to-set-folder-permissions-for-another-user-by-using-ews-in-exchange.md).</span></span>
  
```cs
public static void DelegateAccessCreateEmail(ExchangeService service)
{
    // Create an email message and provide it with connection 
    // configuration information by using an ExchangeService 
    // object named service.
    EmailMessage message = new EmailMessage(service);
    // Set properties on the email message.
    message.Subject = "Company Soccer Team";
    message.Body = "Are you interested in joining?";
    message.ToRecipients.Add("sadie@contoso.com");
    // Save the email to the mailbox owner's Drafts folder.
    // This method call results in a CreateItem call to EWS.
    // The FolderId parameter contains the context for the 
    // mailbox owner's Inbox folder. Any additional actions 
    // taken on this message will be performed in the mailbox 
    // owner's mailbox. 
    message.Save(new FolderId(WellKnownFolderName.Drafts, new Mailbox("primary@contoso.com")));
    // Send the email and save the message in the mailbox owner's 
    // Sent Items folder.
    // This method call results in a SendItem call to EWS.
    message.SendAndSaveCopy(new FolderId(WellKnownFolderName.SentItems, new Mailbox("primary@contoso.com")));
    Console.WriteLine("An email with the subject '" + message.Subject + "' has been sent to '" 
    + message.ToRecipients[0] + "' and saved in the Sent Items folder of the mailbox owner.");
}
```

## <a name="create-and-send-an-email-as-a-delegate-by-using-ews"></a><span data-ttu-id="1a3f6-146">Crear y enviar un correo electrónico como delegado mediante el uso de EWS</span><span class="sxs-lookup"><span data-stu-id="1a3f6-146">Create and send an email as a delegate by using EWS</span></span>
<span data-ttu-id="1a3f6-147"><a name="bk_createews"> </a></span><span class="sxs-lookup"><span data-stu-id="1a3f6-147"></span></span>

<span data-ttu-id="1a3f6-148">EWS le permite usar el objeto de servicio para el usuario delegado para crear y enviar correo electrónico en nombre del propietario del buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="1a3f6-148">EWS enables you to use the service object for the delegate user to create and send email on behalf of the mailbox owner.</span></span> <span data-ttu-id="1a3f6-149">En este ejemplo se muestra cómo usar la operación [CreateItem](http://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) para crear un correo electrónico y la operación de [SendItem](http://msdn.microsoft.com/library/337b89ef-e1b7-45ed-92f3-8abe4200e4c7%28Office.15%29.aspx) para enviar el tiempo y vuelva a guardarla en la carpeta de elementos enviados del propietario del buzón.</span><span class="sxs-lookup"><span data-stu-id="1a3f6-149">This example shows how to use the [CreateItem](http://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) operation to create an email and the [SendItem](http://msdn.microsoft.com/library/337b89ef-e1b7-45ed-92f3-8abe4200e4c7%28Office.15%29.aspx) operation to send the time and save it in the mailbox owner's Sent Items folder.</span></span> 
  
<span data-ttu-id="1a3f6-150">También es la primera solicitud XML que la API administrada de EWS envía cuando se utiliza el método **Save** para [crear y enviar un correo electrónico](#bk_createewsma).</span><span class="sxs-lookup"><span data-stu-id="1a3f6-150">This is also the first XML request that the EWS Managed API sends when you use the **Save** method to [create and send an email](#bk_createewsma).</span></span>
  
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
    <m:CreateItem MessageDisposition="SaveOnly">
      <m:SavedItemFolderId>
        <t:DistinguishedFolderId Id="drafts">
          <t:Mailbox>
            <t:EmailAddress>primary@contoso.com</t:EmailAddress>
          </t:Mailbox>
        </t:DistinguishedFolderId>
      </m:SavedItemFolderId>
      <m:Items>
        <t:Message>
          <t:Subject>Company Soccer Team</t:Subject>
          <t:Body BodyType="HTML">Are you interested in joining?</t:Body>
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

<span data-ttu-id="1a3f6-151">El servidor responde a la solicitud **CreateItem** con un mensaje de [CreateItemResponse](http://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) que incluye un valor de elemento [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) de **NoError**, lo que indica que el correo electrónico se ha creado y guardado correctamente.</span><span class="sxs-lookup"><span data-stu-id="1a3f6-151">The server responds to the **CreateItem** request with a [CreateItemResponse](http://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) element value of **NoError**, which indicates that the email was created and saved successfully.</span></span> <span data-ttu-id="1a3f6-152">La respuesta también contiene el identificador de elemento de correo electrónico recién creado.</span><span class="sxs-lookup"><span data-stu-id="1a3f6-152">The response also contains the item ID of the newly created email.</span></span>
  
<span data-ttu-id="1a3f6-153">El valor de **ItemId** se ha acortado para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="1a3f6-153">The **ItemId** value has been shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="893"
                         MinorBuildNumber="17"
                         Version="V2_10"
                         xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body>
    <m:CreateItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
                          xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:CreateItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Items>
            <t:Message>
              <t:ItemId Id="iNRaAAA="
                        ChangeKey="CQAAABYAAADOilbYa8KaT7ZgMoTz2P+hAAABiQPU" />
            </t:Message>
          </m:Items>
        </m:CreateItemResponseMessage>
      </m:ResponseMessages>
    </m:CreateItemResponse>
  </s:Body>
</s:Envelope>
```

<span data-ttu-id="1a3f6-154">A continuación, use la operación de **SendItem** para enviar el mensaje en nombre del propietario del buzón de correo y vuelva a guardarla en la carpeta de elementos enviados del propietario del buzón.</span><span class="sxs-lookup"><span data-stu-id="1a3f6-154">Next, use the **SendItem** operation to send the message on behalf of the mailbox owner and save it in the mailbox owner's Sent Items folder.</span></span> 
  
<span data-ttu-id="1a3f6-155">El valor de **ItemId** se ha acortado para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="1a3f6-155">The **ItemId** value has been shortened for readability.</span></span> 
  
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
    <m:SendItem SaveItemToFolder="true">
      <m:ItemIds>
        <t:ItemId Id="iNRaAAA="
                  ChangeKey="CQAAABYAAADOilbYa8KaT7ZgMoTz2P+hAAABiQPU" />
      </m:ItemIds>
      <m:SavedItemFolderId>
        <t:DistinguishedFolderId Id="sentitems">
          <t:Mailbox>
            <t:EmailAddress>primary@contoso.com</t:EmailAddress>
          </t:Mailbox>
        </t:DistinguishedFolderId>
      </m:SavedItemFolderId>
    </m:SendItem>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="1a3f6-156">El servidor responde a la solicitud de **SendItem** con un mensaje de [SendItemResponse](http://msdn.microsoft.com/library/26ac41c7-57d9-473e-ab7a-bae93e1d2aba%28Office.15%29.aspx) que incluye un valor de elemento [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) de **NoError**, lo que indica que se envió el correo electrónico y se guardan en la carpeta de elementos enviados del propietario del buzón correctamente.</span><span class="sxs-lookup"><span data-stu-id="1a3f6-156">The server responds to the **SendItem** request with a [SendItemResponse](http://msdn.microsoft.com/library/26ac41c7-57d9-473e-ab7a-bae93e1d2aba%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) element value of **NoError**, which indicates that the email was sent and saved to the mailbox owner's Sent Items folder successfully.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="893"
                         MinorBuildNumber="17"
                         Version="V2_10"
                         xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body>
    <m:SendItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
                        xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:SendItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
        </m:SendItemResponseMessage>
      </m:ResponseMessages>
    </m:SendItemResponse>
  </s:Body>
</s:Envelope>
```

## <a name="search-for-an-email-as-a-delegate-by-using-the-ews-managed-api"></a><span data-ttu-id="1a3f6-157">Buscar un correo electrónico como delegado mediante el uso de la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="1a3f6-157">Search for an email as a delegate by using the EWS Managed API</span></span>
<span data-ttu-id="1a3f6-158"><a name="bk_searchewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="1a3f6-158"></span></span>

<span data-ttu-id="1a3f6-159">Para buscar un correo electrónico, debe usar uno de los métodos de [ExchangeService.FindItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) que incluya un parámetro [FolderId](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) , por lo que puede especificar la carpeta de bandeja de entrada del propietario del buzón.</span><span class="sxs-lookup"><span data-stu-id="1a3f6-159">To search for an email, you must use one of the [ExchangeService.FindItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) methods that includes a [FolderId](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) parameter, so that you can specify the mailbox owner's Inbox folder.</span></span> 
  
```cs
static void DelegateAccessSearchEmailWithFilter(ExchangeService service)
{
    // Limit the result set to 10 items.
    ItemView view = new ItemView(10);
    // Define the search filter.
    SearchFilter.ContainsSubstring filter = new SearchFilter.ContainsSubstring(ItemSchema.Subject, 
        "soccer", ContainmentMode.Substring, ComparisonMode.IgnoreCase);
    view.PropertySet = new PropertySet(ItemSchema.Subject,
                                       ItemSchema.DateTimeReceived,
                                       EmailMessageSchema.IsRead);
    // Item searches do not support deep traversal.
    view.Traversal = ItemTraversal.Shallow;
    // Sorting.
    view.OrderBy.Add(ItemSchema.DateTimeReceived, SortDirection.Descending);
    try
    {
        // Call FindItems to find matching Inbox items. 
        // The parameters of FindItems must denote the mailbox owner,
        // mailbox, and Inbox folder.
        // This call results in a FindItem call to EWS.
        FindItemsResults<Item> results = service.FindItems(new 
            FolderId(WellKnownFolderName.Inbox, "primary@contoso.com"), 
            filter, view);
        foreach (Item item in results.Items)
        {
            Console.WriteLine("Subject: {0}", item.Subject);
            Console.WriteLine("Id: {0}", item.Id.ToString());
            if (item is EmailMessage)
            {
                EmailMessage message = item as EmailMessage;
                Console.WriteLine("Read: {0}", message.IsRead.ToString());
            }
        }
    }
    catch (Exception ex)
    {
        Console.WriteLine("Exception while enumerating results: {0}", ex.Message);
    }
}
```

<span data-ttu-id="1a3f6-160">Después de la llamada **FindItems** devuelve una respuesta con el identificador, puede obtener, update o delete que de correo electrónico mediante el identificador y [acceso implícito](delegate-access-and-ews-in-exchange.md#bk_implicit) - y no es necesario especificar la dirección de SMTP del propietario del buzón.</span><span class="sxs-lookup"><span data-stu-id="1a3f6-160">After the **FindItems** call returns a response with an ID, you can get, update or delete that email by using the ID and [implicit access](delegate-access-and-ews-in-exchange.md#bk_implicit) - and you do not need to specify the mailbox owner's SMTP address.</span></span> 
  
## <a name="search-for-an-email-as-a-delegate-by-using-ews"></a><span data-ttu-id="1a3f6-161">Buscar un correo electrónico como delegado mediante el uso de EWS</span><span class="sxs-lookup"><span data-stu-id="1a3f6-161">Search for an email as a delegate by using EWS</span></span>
<span data-ttu-id="1a3f6-162"><a name="bk_searchews"> </a></span><span class="sxs-lookup"><span data-stu-id="1a3f6-162"></span></span>

<span data-ttu-id="1a3f6-163">EWS le permite usar el objeto de servicio para el usuario delegado para buscar mensajes de correo electrónico que cumplen un conjunto de criterios de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="1a3f6-163">EWS enables you to use the service object for the delegate user to search for emails that meet a set of search criteria.</span></span> <span data-ttu-id="1a3f6-164">En este ejemplo se muestra cómo usar la operación [FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) para buscar mensajes en la carpeta del propietario Bandeja de entrada que contienen la palabra "fútbol" en el asunto.</span><span class="sxs-lookup"><span data-stu-id="1a3f6-164">This example shows how to use the [FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) operation to find messages in the owner's Inbox folder that contain the word "soccer" in the subject.</span></span> 
  
<span data-ttu-id="1a3f6-165">Esto también es la solicitud XML que la API administrada de EWS envía cuando [busca un correo electrónico](#bk_searchewsma).</span><span class="sxs-lookup"><span data-stu-id="1a3f6-165">This is also the XML request that the EWS Managed API sends when you [search for an email](#bk_searchewsma).</span></span>
  
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
    <m:FindItem Traversal="Shallow">
      <m:ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="item:Subject" />
          <t:FieldURI FieldURI="item:DateTimeReceived" />
          <t:FieldURI FieldURI="message:IsRead" />
        </t:AdditionalProperties>
      </m:ItemShape>
      <m:IndexedPageItemView MaxEntriesReturned="10"
                             Offset="0"
                             BasePoint="Beginning" />
      <m:Restriction>
        <t:Contains ContainmentMode="Substring"
                    ContainmentComparison="IgnoreCase">
          <t:FieldURI FieldURI="item:Subject" />
          <t:Constant Value="soccer" />
        </t:Contains>
      </m:Restriction>
      <m:SortOrder>
        <t:FieldOrder Order="Descending">
          <t:FieldURI FieldURI="item:DateTimeReceived" />
        </t:FieldOrder>
      </m:SortOrder>
      <m:ParentFolderIds>
        <t:DistinguishedFolderId Id="inbox">
          <t:Mailbox>
            <t:EmailAddress>primary@contoso.com</t:EmailAddress>
          </t:Mailbox>
        </t:DistinguishedFolderId>
      </m:ParentFolderIds>
    </m:FindItem>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="1a3f6-166">El servidor responde a la solicitud de **FindItem** con un mensaje de [FindItemResponse](http://msdn.microsoft.com/library/c8b316df-d4ab-49b8-96d4-8e9a016730ef%28Office.15%29.aspx) que incluye un valor de elemento [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) de **NoError**, lo que indica que la búsqueda que se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="1a3f6-166">The server responds to the **FindItem** request with a [FindItemResponse](http://msdn.microsoft.com/library/c8b316df-d4ab-49b8-96d4-8e9a016730ef%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) element value of **NoError**, which indicates that the search completed successfully.</span></span> <span data-ttu-id="1a3f6-167">La respuesta contiene un elemento de [mensaje](http://msdn.microsoft.com/library/2400b33c-43b2-4fc2-b6fb-275a99e0e810%28Office.15%29.aspx) para los mensajes de correo electrónico que cumplen los criterios de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="1a3f6-167">The response contains a [Message](http://msdn.microsoft.com/library/2400b33c-43b2-4fc2-b6fb-275a99e0e810%28Office.15%29.aspx) element for any emails that met the search criteria.</span></span> <span data-ttu-id="1a3f6-168">En este caso, se ha encontrado un solo de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="1a3f6-168">In this case, only one email is found.</span></span> 
  
<span data-ttu-id="1a3f6-169">El valor del elemento [ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) se ha acortado para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="1a3f6-169">The value of the [ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) element has been shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="893"
                         MinorBuildNumber="17"
                         Version="V2_10"
                         xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body>
    <m:FindItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
                        xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:FindItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:RootFolder IndexedPagingOffset="1"
                        TotalItemsInView="1"
                        IncludesLastItemInRange="true">
            <t:Items>
              <t:Message>
                <t:ItemId Id="iNwoAAA="
                          ChangeKey="CQAAABYAAADOilbYa8KaT7ZgMoTz2P+hAAABiQuu" />
                <t:Subject>Soccer team</t:Subject>
                <t:DateTimeReceived>2014-03-10T06:16:55Z</t:DateTimeReceived>
                <t:IsRead>false</t:IsRead>
              </t:Message>
            </t:Items>
          </m:RootFolder>
        </m:FindItemResponseMessage>
      </m:ResponseMessages>
    </m:FindItemResponse>
  </s:Body>
</s:Envelope>
```

<span data-ttu-id="1a3f6-170">Ahora que tiene la **ItemId** para el correo electrónico que cumple los criterios, puede obtener, update o delete que de correo electrónico mediante el uso de la **ItemId** y [acceso implícito](delegate-access-and-ews-in-exchange.md#bk_implicit) - y no es necesario especificar la dirección de SMTP del propietario del buzón.</span><span class="sxs-lookup"><span data-stu-id="1a3f6-170">Now that you have the **ItemId** for the email that meets your criteria, you can get, update, or delete that email by using the **ItemId** and [implicit access](delegate-access-and-ews-in-exchange.md#bk_implicit) - and you do not need to specify the mailbox owner's SMTP address.</span></span> 
  
## <a name="get-update-or-delete-email-items-as-a-delegate-by-using-the-ews-managed-api"></a><span data-ttu-id="1a3f6-171">Obtener, actualizar o eliminar elementos de correo electrónico como delegado mediante el uso de la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="1a3f6-171">Get, update, or delete email items as a delegate by using the EWS Managed API</span></span>
<span data-ttu-id="1a3f6-172"><a name="bk_geteswma"> </a></span><span class="sxs-lookup"><span data-stu-id="1a3f6-172"></span></span>

<span data-ttu-id="1a3f6-173">Puede usar la API administrada de EWS para obtener, actualizar o eliminar un correo electrónico de la misma manera que se realizan estas acciones cuando no está utilizando acceso delegado.</span><span class="sxs-lookup"><span data-stu-id="1a3f6-173">You can use the EWS Managed API to get, update, or delete an email in the same way that you perform these actions when you're not using delegate access.</span></span> <span data-ttu-id="1a3f6-174">La única diferencia es que el objeto **ExchangeService** es para el usuario delegado.</span><span class="sxs-lookup"><span data-stu-id="1a3f6-174">The only difference is that the **ExchangeService** object is for the delegate user.</span></span> <span data-ttu-id="1a3f6-175">El identificador de elemento incluido en la llamada al método **enlazar** de forma única identifica el elemento en el almacén de buzón de correo, en del propietario buzón de correo de la Bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="1a3f6-175">The item ID included in the **Bind** method call uniquely identifies the item in the mailbox store, in the mailbox owner's Inbox folder.</span></span> 
  
<span data-ttu-id="1a3f6-176">**Tabla 2. Métodos de API administrada de EWS trabajar con correo electrónico como delegado**</span><span class="sxs-lookup"><span data-stu-id="1a3f6-176">**Table 2. EWS Managed API methods working with email as a delegate**</span></span>

|<span data-ttu-id="1a3f6-177">**Tarea**</span><span class="sxs-lookup"><span data-stu-id="1a3f6-177">**Task**</span></span>|<span data-ttu-id="1a3f6-178">**Método de la API administrada de EWS**</span><span class="sxs-lookup"><span data-stu-id="1a3f6-178">**EWS Managed API method**</span></span>|<span data-ttu-id="1a3f6-179">**Ejemplo de código**</span><span class="sxs-lookup"><span data-stu-id="1a3f6-179">**Code example**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1a3f6-180">Obtener un correo electrónico</span><span class="sxs-lookup"><span data-stu-id="1a3f6-180">Get an email</span></span>  <br/> |[<span data-ttu-id="1a3f6-181">Enlazar</span><span class="sxs-lookup"><span data-stu-id="1a3f6-181">Bind</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="1a3f6-182">Obtener un elemento mediante el uso de la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="1a3f6-182">Get an item by using the EWS Managed API</span></span>](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_getewsma) <br/> |
|<span data-ttu-id="1a3f6-183">Actualización de un correo electrónico</span><span class="sxs-lookup"><span data-stu-id="1a3f6-183">Update an email</span></span>  <br/> |<span data-ttu-id="1a3f6-184">[Enlazar](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) seguido de [actualización](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.update%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1a3f6-184">[Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) followed by [Update](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.update%28v=exchg.80%29.aspx)</span></span> <br/> |[<span data-ttu-id="1a3f6-185">Actualizar un elemento mediante el uso de la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="1a3f6-185">Update an item by using the EWS Managed API</span></span>](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_updateewsma) <br/> |
|<span data-ttu-id="1a3f6-186">Eliminar un correo electrónico</span><span class="sxs-lookup"><span data-stu-id="1a3f6-186">Delete an email</span></span>  <br/> |<span data-ttu-id="1a3f6-187">[Enlazar](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) seguido de [Eliminar](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.delete%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1a3f6-187">[Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) followed by [Delete](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.delete%28v=exchg.80%29.aspx)</span></span> <br/> |[<span data-ttu-id="1a3f6-188">Eliminar un elemento mediante el uso de la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="1a3f6-188">Delete an item by using the EWS Managed API</span></span>](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_deleteewsma) <br/> |
   
## <a name="get-update-or-delete-email-items-as-a-delegate-by-using-ews"></a><span data-ttu-id="1a3f6-189">Obtener, actualizar o eliminar elementos de correo electrónico como delegado mediante el uso de EWS</span><span class="sxs-lookup"><span data-stu-id="1a3f6-189">Get, update, or delete email items as a delegate by using EWS</span></span>
<span data-ttu-id="1a3f6-190"><a name="bk_getews"> </a></span><span class="sxs-lookup"><span data-stu-id="1a3f6-190"></span></span>

<span data-ttu-id="1a3f6-191">Puede usar la API administrada de EWS para obtener, actualizar o eliminar un correo electrónico de la misma manera que se realizan estas acciones cuando no está utilizando acceso delegado.</span><span class="sxs-lookup"><span data-stu-id="1a3f6-191">You can use the EWS Managed API to get, update, or delete an email in the same way that you perform these actions when you're not using delegate access.</span></span> <span data-ttu-id="1a3f6-192">La única diferencia es que el objeto de servicio para el usuario delegado.</span><span class="sxs-lookup"><span data-stu-id="1a3f6-192">The only difference is that the service object is for the delegate user.</span></span> <span data-ttu-id="1a3f6-193">El identificador de elemento incluido en la solicitud de **GetItem** identifica de forma exclusiva identifica el elemento en el almacén de buzón de correo, en del propietario buzón de correo de la Bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="1a3f6-193">The item ID included in the **GetItem** request uniquely identifies the item in the mailbox store, in the mailbox owner's Inbox folder.</span></span> 
  
<span data-ttu-id="1a3f6-194">**Tabla 3. Operaciones de EWS para trabajar con correo electrónico como delegado**</span><span class="sxs-lookup"><span data-stu-id="1a3f6-194">**Table 3. EWS operations for working with email as a delegate**</span></span>

|<span data-ttu-id="1a3f6-195">**Tarea**</span><span class="sxs-lookup"><span data-stu-id="1a3f6-195">**Task**</span></span>|<span data-ttu-id="1a3f6-196">**Operación de EWS**</span><span class="sxs-lookup"><span data-stu-id="1a3f6-196">**EWS operation**</span></span>|<span data-ttu-id="1a3f6-197">**Ejemplo de código**</span><span class="sxs-lookup"><span data-stu-id="1a3f6-197">**Code example**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1a3f6-198">Obtener un correo electrónico</span><span class="sxs-lookup"><span data-stu-id="1a3f6-198">Get an email</span></span>  <br/> |[<span data-ttu-id="1a3f6-199">GetItem</span><span class="sxs-lookup"><span data-stu-id="1a3f6-199">GetItem</span></span>](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) <br/> |[<span data-ttu-id="1a3f6-200">Obtener un elemento mediante el uso de EWS</span><span class="sxs-lookup"><span data-stu-id="1a3f6-200">Get an item by using EWS</span></span>](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_getews) <br/> |
|<span data-ttu-id="1a3f6-201">Actualización de un correo electrónico</span><span class="sxs-lookup"><span data-stu-id="1a3f6-201">Update an email</span></span>  <br/> |<span data-ttu-id="1a3f6-202">[GetItem](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) seguido [UpdateItem](http://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1a3f6-202">[GetItem](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) followed by [UpdateItem](http://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx)</span></span> <br/> |[<span data-ttu-id="1a3f6-203">Actualizar un elemento mediante el uso de EWS</span><span class="sxs-lookup"><span data-stu-id="1a3f6-203">Update an item by using EWS</span></span>](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_updateews) <br/> |
|<span data-ttu-id="1a3f6-204">Eliminar un correo electrónico</span><span class="sxs-lookup"><span data-stu-id="1a3f6-204">Delete an email</span></span>  <br/> |<span data-ttu-id="1a3f6-205">[GetItem](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) seguido [DeleteItem](http://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1a3f6-205">[GetItem](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) followed by [DeleteItem](http://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx)</span></span> <br/> |[<span data-ttu-id="1a3f6-206">Eliminar un elemento mediante el uso de EWS</span><span class="sxs-lookup"><span data-stu-id="1a3f6-206">Delete an item by using EWS</span></span>](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_deleteews) <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1a3f6-207">Vea también</span><span class="sxs-lookup"><span data-stu-id="1a3f6-207">See also</span></span>

- [<span data-ttu-id="1a3f6-208">Acceso delegado y EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="1a3f6-208">Delegate access and EWS in Exchange</span></span>](delegate-access-and-ews-in-exchange.md)    
- [<span data-ttu-id="1a3f6-209">Agregar y quitar delegados mediante EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="1a3f6-209">Add and remove delegates by using EWS in Exchange</span></span>](how-to-add-and-remove-delegates-by-using-ews-in-exchange.md)    
- [<span data-ttu-id="1a3f6-210">Establecer permisos de carpeta de otro usuario mediante el uso de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="1a3f6-210">Set folder permissions for another user by using EWS in Exchange</span></span>](how-to-set-folder-permissions-for-another-user-by-using-ews-in-exchange.md)    
- [<span data-ttu-id="1a3f6-211">Calendarios y EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="1a3f6-211">Calendars and EWS in Exchange</span></span>](calendars-and-ews-in-exchange.md)
    

