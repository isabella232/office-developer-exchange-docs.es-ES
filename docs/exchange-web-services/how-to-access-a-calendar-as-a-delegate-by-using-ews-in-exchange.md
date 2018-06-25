---
title: Obtener acceso a un calendario como delegado mediante el uso de EWS en Exchange
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: d7db4a1e-9ed6-41da-8529-a73ca285cdf2
description: Obtenga información sobre cómo obtener acceso a un calendario como delegado mediante la API administrada de EWS o EWS en Exchange.
ms.openlocfilehash: 24327c28f58e728807fc5581b480d3c01d3b7208
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763032"
---
#  <a name="access-a-calendar-as-a-delegate-by-using-ews-in-exchange"></a><span data-ttu-id="f24a3-103">Obtener acceso a un calendario como delegado mediante el uso de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="f24a3-103">Access a calendar as a delegate by using EWS in Exchange</span></span>

<span data-ttu-id="f24a3-104">Obtenga información sobre cómo obtener acceso a un calendario como delegado mediante la API administrada de EWS o EWS en Exchange.</span><span class="sxs-lookup"><span data-stu-id="f24a3-104">Learn how to access a calendar as a delegate by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="f24a3-105">Puede usar la API administrada de EWS o EWS para dar a un usuario delegar el acceso a la carpeta del calendario del propietario del buzón.</span><span class="sxs-lookup"><span data-stu-id="f24a3-105">You can use the EWS Managed API or EWS to give a user delegate access to a mailbox owner's Calendar folder.</span></span> <span data-ttu-id="f24a3-106">El delegado puede, a continuación, crear convocatorias de reunión en nombre del propietario del buzón de correo, crear citas, responder a las convocatorias de reunión y recuperar, actualizar y eliminar las reuniones de la carpeta del calendario del propietario del buzón, en función de sus permisos.</span><span class="sxs-lookup"><span data-stu-id="f24a3-106">The delegate can then create meeting requests on behalf of the mailbox owner, create appointments, respond to meeting requests, and retrieve, update, and delete meetings from the mailbox owner's Calendar folder, depending on their permissions.</span></span>
  
<span data-ttu-id="f24a3-107">Como delegado, use los mismos métodos y operaciones para tener acceso a la carpeta de calendario de un propietario buzón de correo que use para tener acceso a su propia carpeta de calendario.</span><span class="sxs-lookup"><span data-stu-id="f24a3-107">As a delegate, you use the same methods and operations to access a mailbox owner's Calendar folder that you use to access your own Calendar folder.</span></span> <span data-ttu-id="f24a3-108">La diferencia principal es que se debe usar [acceso explícito](delegate-access-and-ews-in-exchange.md#bk_explicit) para buscar o crear un elemento de calendario o una subcarpeta de calendario y, a continuación, después de identificar el identificador de elemento o carpeta, puede usar [acceso implícito](delegate-access-and-ews-in-exchange.md#bk_implicit) para obtener, actualizar o eliminar el elemento.</span><span class="sxs-lookup"><span data-stu-id="f24a3-108">The main difference is that you have to use [explicit access](delegate-access-and-ews-in-exchange.md#bk_explicit) to find or create a calendar item or calendar subfolder, and then after you identify the item ID or folder ID, you can use [implicit access](delegate-access-and-ews-in-exchange.md#bk_implicit) to get, update, or delete the item.</span></span> 
  
<span data-ttu-id="f24a3-109">**La tabla 1. Métodos de la API administrada de EWS y las operaciones de EWS para obtener acceso a un calendario como delegado**</span><span class="sxs-lookup"><span data-stu-id="f24a3-109">**Table 1. EWS Managed API methods and EWS operations for accessing a calendar as a delegate**</span></span>

|<span data-ttu-id="f24a3-110">**Si quiere...**</span><span class="sxs-lookup"><span data-stu-id="f24a3-110">**If you want to…**</span></span>|<span data-ttu-id="f24a3-111">**Use este método de la API administrada de EWS...**</span><span class="sxs-lookup"><span data-stu-id="f24a3-111">**Use this EWS Managed API method…**</span></span>|<span data-ttu-id="f24a3-112">**Use esta operación de EWS...**</span><span class="sxs-lookup"><span data-stu-id="f24a3-112">**Use this EWS operation…**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f24a3-113">Crear una reunión o cita como delegado</span><span class="sxs-lookup"><span data-stu-id="f24a3-113">Create a meeting or appointment as a delegate</span></span>  <br/> |<span data-ttu-id="f24a3-114">[Appointment.Save](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.save%28v=exchg.80%29.aspx) donde el parámetro [FolderId](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) proporciona [acceso explícito](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) a la carpeta del calendario del propietario del buzón</span><span class="sxs-lookup"><span data-stu-id="f24a3-114">[Appointment.Save](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.save%28v=exchg.80%29.aspx) where the [FolderId](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) parameter provides [explicit access](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) to the mailbox owner's Calendar folder</span></span>  <br/> |<span data-ttu-id="f24a3-115">[CreateItem](http://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) donde el elemento de [buzón de correo](http://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) especifica la [EmailAddress](http://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) del propietario del buzón</span><span class="sxs-lookup"><span data-stu-id="f24a3-115">[CreateItem](http://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) where the [Mailbox](http://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) element specifies the [EmailAddress](http://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) of the mailbox owner</span></span>  <br/> |
|<span data-ttu-id="f24a3-116">Crear varias reuniones o citas como delegado</span><span class="sxs-lookup"><span data-stu-id="f24a3-116">Create multiple meetings or appointments as a delegate</span></span>  <br/> |<span data-ttu-id="f24a3-117">[ExchangeService.CreateItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.createitems%28v=exchg.80%29.aspx) donde el parámetro **FolderId** proporciona [acceso explícito](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) a la carpeta del calendario del propietario del buzón</span><span class="sxs-lookup"><span data-stu-id="f24a3-117">[ExchangeService.CreateItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.createitems%28v=exchg.80%29.aspx) where the **FolderId** parameter provides [explicit access](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) to the mailbox owner's Calendar folder</span></span>  <br/> |<span data-ttu-id="f24a3-118">[CreateItem](http://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) donde el elemento de [buzón de correo](http://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) especifica la [EmailAddress](http://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) del propietario del buzón</span><span class="sxs-lookup"><span data-stu-id="f24a3-118">[CreateItem](http://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) where the [Mailbox](http://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) element specifies the [EmailAddress](http://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) of the mailbox owner</span></span>  <br/> |
|<span data-ttu-id="f24a3-119">Buscar o buscar una cita o reunión como delegado</span><span class="sxs-lookup"><span data-stu-id="f24a3-119">Search for or find an appointment or meeting as a delegate</span></span>  <br/> |<span data-ttu-id="f24a3-120">[ExchangeService.FindItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) donde el parámetro **FolderId** proporciona [acceso explícito](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) a la carpeta del calendario del propietario del buzón</span><span class="sxs-lookup"><span data-stu-id="f24a3-120">[ExchangeService.FindItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) where the **FolderId** parameter provides [explicit access](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) to the mailbox owner's Calendar folder</span></span>  <br/> |<span data-ttu-id="f24a3-121">[FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) donde el elemento de [buzón de correo](http://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) especifica la [EmailAddress](http://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) del propietario del buzón</span><span class="sxs-lookup"><span data-stu-id="f24a3-121">[FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) where the [Mailbox](http://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) element specifies the [EmailAddress](http://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) of the mailbox owner</span></span>  <br/> |
|<span data-ttu-id="f24a3-122">Obtener una cita o reunión como delegado</span><span class="sxs-lookup"><span data-stu-id="f24a3-122">Get an appointment or meeting as a delegate</span></span>  <br/> |[<span data-ttu-id="f24a3-123">Appointment.Bind</span><span class="sxs-lookup"><span data-stu-id="f24a3-123">Appointment.Bind</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="f24a3-124">GetItem</span><span class="sxs-lookup"><span data-stu-id="f24a3-124">GetItem</span></span>](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="f24a3-125">Actualización de una cita o reunión como delegado</span><span class="sxs-lookup"><span data-stu-id="f24a3-125">Update an appointment or meeting as a delegate</span></span>  <br/> |<span data-ttu-id="f24a3-126">[Appointment.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) seguido de [Appointment.Update](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.update%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f24a3-126">[Appointment.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) followed by [Appointment.Update](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.update%28v=exchg.80%29.aspx)</span></span> <br/> |<span data-ttu-id="f24a3-127">[GetItem](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) seguido [UpdateItem](http://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f24a3-127">[GetItem](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) followed by [UpdateItem](http://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx)</span></span> <br/> |
|<span data-ttu-id="f24a3-128">Eliminación de una cita o reunión como delegado</span><span class="sxs-lookup"><span data-stu-id="f24a3-128">Delete an appointment or meeting as a delegate</span></span>  <br/> |<span data-ttu-id="f24a3-129">[Appointment.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) seguido de [Appointment.Delete](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.delete%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f24a3-129">[Appointment.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) followed by [Appointment.Delete](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.delete%28v=exchg.80%29.aspx)</span></span> <br/> |<span data-ttu-id="f24a3-130">[GetItem](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) seguido [DeleteItem](http://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f24a3-130">[GetItem](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) followed by [DeleteItem](http://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx)</span></span> <br/> |
   
> [!NOTE]
> <span data-ttu-id="f24a3-131">En los ejemplos de código de este artículo, primary@contoso.com es el propietario del buzón.</span><span class="sxs-lookup"><span data-stu-id="f24a3-131">In the code examples in this article, primary@contoso.com is the mailbox owner.</span></span> 
  
## <a name="prerequisite-tasks"></a><span data-ttu-id="f24a3-132">Tareas de requisitos previos</span><span class="sxs-lookup"><span data-stu-id="f24a3-132">Prerequisite tasks</span></span>
<span data-ttu-id="f24a3-133"><a name="bk_prereq"> </a></span><span class="sxs-lookup"><span data-stu-id="f24a3-133"></span></span>

<span data-ttu-id="f24a3-134">Antes de que un usuario puede obtener acceso a la carpeta de calendario de un propietario buzón de correo como delegado, el usuario debe ser [agregado como delegado con permisos](how-to-add-and-remove-delegates-by-using-ews-in-exchange.md) para la carpeta del calendario del propietario del buzón.</span><span class="sxs-lookup"><span data-stu-id="f24a3-134">Before a user can access a mailbox owner's Calendar folder as a delegate, the user must be [added as a delegate with permissions](how-to-add-and-remove-delegates-by-using-ews-in-exchange.md) to the mailbox owner's Calendar folder.</span></span> 
  
<span data-ttu-id="f24a3-135">Un delegado debe tener un buzón vinculado a su cuenta para actualizar el calendario de un propietario del buzón.</span><span class="sxs-lookup"><span data-stu-id="f24a3-135">A delegate must have a mailbox attached to their account to update the calendar of a mailbox owner.</span></span>
  
<span data-ttu-id="f24a3-136">Si un delegado necesita para trabajar con convocatorias de reunión y las respuestas sólo, se puede agregar al delegado a la carpeta Calendario y usar el valor de enumeración de API administrada de EWS de [MeetingRequestsDeliveryScope.DelegatesAndSendInformationToMe](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.meetingrequestsdeliveryscope%28v=exchg.80%29.aspx) predeterminado o la [ DeliverMeetingRequests](http://msdn.microsoft.com/library/04b999af-0b27-4e6d-a8b1-400955a1afaa%28Office.15%29.aspx) valor de elemento EWS de **DelegatesAndSendInformationToMe** para enviar las solicitudes al delegado y los mensajes informativos al propietario del buzón.</span><span class="sxs-lookup"><span data-stu-id="f24a3-136">If a delegate needs to work with meeting requests and responses only, you can add the delegate to the Calendar folder, and use the default [MeetingRequestsDeliveryScope.DelegatesAndSendInformationToMe](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.meetingrequestsdeliveryscope%28v=exchg.80%29.aspx) EWS Managed API enumeration value or the [DeliverMeetingRequests](http://msdn.microsoft.com/library/04b999af-0b27-4e6d-a8b1-400955a1afaa%28Office.15%29.aspx) EWS element value of **DelegatesAndSendInformationToMe** to send the requests to the delegate and informational messages to the mailbox owner.</span></span> <span data-ttu-id="f24a3-137">A continuación, el delegado no necesita tener acceso a la carpeta de bandeja de entrada del propietario del buzón.</span><span class="sxs-lookup"><span data-stu-id="f24a3-137">The delegate then does not need to be given access to the mailbox owner's Inbox folder.</span></span> 
  
## <a name="create-a-meeting-or-appointment-as-a-delegate-by-using-the-ews-managed-api"></a><span data-ttu-id="f24a3-138">Crear una reunión o cita como delegado mediante el uso de la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="f24a3-138">Create a meeting or appointment as a delegate by using the EWS Managed API</span></span>
<span data-ttu-id="f24a3-139"><a name="bk_createewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="f24a3-139"></span></span>

<span data-ttu-id="f24a3-140">La API administrada de EWS le permite usar el objeto de servicio para el usuario delegado para crear elementos de calendario para el propietario del buzón.</span><span class="sxs-lookup"><span data-stu-id="f24a3-140">The EWS Managed API enables you to use the service object for the delegate user to create calendar items for the mailbox owner.</span></span> <span data-ttu-id="f24a3-141">En este ejemplo se muestra cómo utilizar el método [Save](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.save%28v=exchg.80%29.aspx) para crear una reunión y enviar convocatorias de reunión a los asistentes.</span><span class="sxs-lookup"><span data-stu-id="f24a3-141">This example shows how to use the [Save](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.save%28v=exchg.80%29.aspx) method to create a meeting and send meeting requests to the attendees.</span></span> 
  
<span data-ttu-id="f24a3-142">En este ejemplo se da por supuesto que **servicio** es un objeto [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) válido para el delegado y que el delegado se ha concedido los permisos adecuados para la carpeta del calendario del propietario del buzón.</span><span class="sxs-lookup"><span data-stu-id="f24a3-142">This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object for the delegate and that the delegate has been granted the appropriate permissions for the mailbox owner's Calendar folder.</span></span> 
  
```cs
private static void DelegateAccessCreateMeeting(ExchangeService service)
{
    Appointment meeting = new Appointment(service);
    // Set the properties on the meeting object to create the meeting.
    meeting.Subject = "Team building exercise";
    meeting.Body = "Let's learn to really work as a team and then have lunch!";
    meeting.Start = DateTime.Now.AddDays(2);
    meeting.End = meeting.Start.AddHours(4);
    meeting.Location = "Conference Room 12";
    meeting.RequiredAttendees.Add("sadie@contoso.com");
    meeting.ReminderMinutesBeforeStart = 60;
    // Save the meeting to the Calendar folder for 
    // the mailbox owner and send the meeting request.
    // This method call results in a CreateItem call to EWS.
    meeting.Save(new FolderId(WellKnownFolderName.Calendar, 
        "primary@contoso.com"), 
        SendInvitationsMode.SendToAllAndSaveCopy);
    // Verify that the meeting was created.
    Item item = Item.Bind(service, meeting.Id, new PropertySet(ItemSchema.Subject));
    Console.WriteLine("\nMeeting created: " + item.Subject + "\n");
}
```

<span data-ttu-id="f24a3-143">Tenga en cuenta que cuando se guarda el elemento, la llamada al método [Save](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.save%28v=exchg.80%29.aspx) debe identificar carpeta del calendario del propietario del buzón.</span><span class="sxs-lookup"><span data-stu-id="f24a3-143">Note that when you save the item, the [Save](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.save%28v=exchg.80%29.aspx) method call must identify the mailbox owner's Calendar folder.</span></span> <span data-ttu-id="f24a3-144">Si no se especifica la carpeta del calendario del propietario del buzón, la convocatoria de reunión obtiene guardan en el calendario del delegado y no la carpeta de calendario del propietario del buzón.</span><span class="sxs-lookup"><span data-stu-id="f24a3-144">If the mailbox owner's Calendar folder is not specified, the meeting request gets saved to the delegate's calendar and not the mailbox owner's Calendar folder.</span></span> <span data-ttu-id="f24a3-145">Puede incluir la carpeta del calendario del propietario del buzón en la llamada al método **Guardar** de dos maneras.</span><span class="sxs-lookup"><span data-stu-id="f24a3-145">You can include the mailbox owner's Calendar folder in the **Save** method call in two ways.</span></span> <span data-ttu-id="f24a3-146">Se recomienda que se cree una instancia de una nueva instancia del objeto [FolderId](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) mediante el uso de la [WellKnownFolderName](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.wellknownfoldername%28v=exchg.80%29.aspx) y la dirección SMTP del propietario del buzón.</span><span class="sxs-lookup"><span data-stu-id="f24a3-146">We recommend that you instantiate a new instance of the [FolderId](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) object by using the [WellKnownFolderName](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.wellknownfoldername%28v=exchg.80%29.aspx) and the SMTP address of the mailbox owner.</span></span> 
  
```cs
meeting.Save(new FolderId(WellKnownFolderName.Calendar,
    "primary@contoso.com"), SendInvitationsMode.SendToAllAndSaveCopy);
```

<span data-ttu-id="f24a3-147">Sin embargo, también puede [enlazar](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) a la carpeta Calendario en primer lugar y, a continuación, use el identificador de la carpeta en la llamada al método **Save** .</span><span class="sxs-lookup"><span data-stu-id="f24a3-147">However, you can also [Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) to the Calendar folder first, and then use the ID of the folder in the **Save** method call.</span></span> <span data-ttu-id="f24a3-148">Tenga en cuenta, sin embargo, esto crea una llamada EWS adicional.</span><span class="sxs-lookup"><span data-stu-id="f24a3-148">Be aware, however, that this creates an extra EWS call.</span></span> 
  
```cs
    // Identify the mailbox owner's SMTP address
    // and bind to their Calendar folder.
    Mailbox primary = new Mailbox("primary@contoso.com"); 
    Folder primaryCalendar = Folder.Bind(service, 
        new FolderId(WellKnownFolderName.Calendar, primary)); 
…
    // Save the meeting to the Calendar folder for the mailbox owner and send the meeting request.
    meeting.Save(primaryCalendar.Id, 
        SendInvitationsMode.SendToAllAndSaveCopy);
```

## <a name="create-a-meeting-or-appointment-as-a-delegate-by-using-ews"></a><span data-ttu-id="f24a3-149">Crear una reunión o cita como delegado mediante el uso de EWS</span><span class="sxs-lookup"><span data-stu-id="f24a3-149">Create a meeting or appointment as a delegate by using EWS</span></span>
<span data-ttu-id="f24a3-150"><a name="bk_createews"> </a></span><span class="sxs-lookup"><span data-stu-id="f24a3-150"></span></span>

<span data-ttu-id="f24a3-151">EWS le permite usar el objeto de servicio para el usuario delegado para crear elementos de calendario para el propietario del buzón.</span><span class="sxs-lookup"><span data-stu-id="f24a3-151">EWS enables you to use the service object for the delegate user to create calendar items for the mailbox owner.</span></span> <span data-ttu-id="f24a3-152">En este ejemplo se muestra cómo usar la operación [CreateItem](http://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) para crear una reunión y enviar convocatorias de reunión a los asistentes.</span><span class="sxs-lookup"><span data-stu-id="f24a3-152">This example shows how to use the [CreateItem](http://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) operation to create a meeting and send meeting requests to the attendees.</span></span> 
  
<span data-ttu-id="f24a3-153">También es la solicitud XML que la API administrada de EWS envía cuando se utiliza el método **Save** para [crear una reunión o cita como delegado](#bk_createewsma).</span><span class="sxs-lookup"><span data-stu-id="f24a3-153">This is also the XML request that the EWS Managed API sends when you use the **Save** method to [create a meeting or appointment as a delegate](#bk_createewsma).</span></span>
  
<span data-ttu-id="f24a3-154">El encabezado SOAP se ha quitado el siguiente ejemplo para mayor brevedad.</span><span class="sxs-lookup"><span data-stu-id="f24a3-154">The SOAP header has been removed from the following example for brevity.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
         xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
         xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
…
  <soap:Body>
    <m:CreateItem SendMeetingInvitations="SendToAllAndSaveCopy">
      <m:SavedItemFolderId>
        <t:DistinguishedFolderId Id="calendar">
          <t:Mailbox>
            <t:EmailAddress>primary@contoso.com</t:EmailAddress>
          </t:Mailbox>
        </t:DistinguishedFolderId>
      </m:SavedItemFolderId>
      <m:Items>
        <t:CalendarItem>
          <t:Subject>Team building exercise</t:Subject>
          <t:Body BodyType="HTML">Let's learn to really work as a 
              team and then have lunch!</t:Body>
          <t:ReminderMinutesBeforeStart>60</t:ReminderMinutesBeforeStart>
          <t:Start>2014-03-09T23:26:33.756-05:00</t:Start>
          <t:End>2014-03-10T03:26:33.756-05:00</t:End>
          <t:Location>Conference Room 12</t:Location>
          <t:RequiredAttendees>
            <t:Attendee>
              <t:Mailbox>
                <t:EmailAddress>sadie@contoso.com</t:EmailAddress>
              </t:Mailbox>
            </t:Attendee>
          </t:RequiredAttendees>
        </t:CalendarItem>
      </m:Items>
    </m:CreateItem>
  </soap:Body>
</soap:Envelope>

```

<span data-ttu-id="f24a3-155">El servidor responde a la solicitud **CreateItem** con un mensaje de [CreateItemResponse](http://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) que incluye un valor de elemento [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) de **NoError**, lo que indica que la reunión se ha creado correctamente.</span><span class="sxs-lookup"><span data-stu-id="f24a3-155">The server responds to the **CreateItem** request with a [CreateItemResponse](http://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) element value of **NoError**, which indicates that the meeting was created successfully.</span></span> <span data-ttu-id="f24a3-156">La respuesta también contiene el identificador de elemento de la reunión recién creado.</span><span class="sxs-lookup"><span data-stu-id="f24a3-156">The response also contains the item ID of the newly created meeting.</span></span>
  
## <a name="search-for-a-meeting-or-appointment-as-a-delegate-by-using-the-ews-managed-api"></a><span data-ttu-id="f24a3-157">Búsqueda de una reunión o cita como delegado mediante el uso de la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="f24a3-157">Search for a meeting or appointment as a delegate by using the EWS Managed API</span></span>
<span data-ttu-id="f24a3-158"><a name="bk_searchewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="f24a3-158"></span></span>

<span data-ttu-id="f24a3-159">Para buscar una reunión, debe usar uno de los métodos de [ExchangeService.FindItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) que incluya un parámetro [FolderId](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) , por lo que puede especificar la carpeta del calendario del propietario del buzón.</span><span class="sxs-lookup"><span data-stu-id="f24a3-159">To search for a meeting, you must use one of the [ExchangeService.FindItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) methods that includes a [FolderId](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) parameter, so that you can specify the mailbox owner's Calendar folder.</span></span> 
  
```cs
static void DelegateAccessSearchWithFilter
    (ExchangeService service, SearchFilter filter)
{
    // Limit the result set to 10 items.
    ItemView view = new ItemView(10);
    view.PropertySet = new PropertySet(ItemSchema.Subject,
                                       ItemSchema.DateTimeReceived,
                                       EmailMessageSchema.IsRead);
    // Item searches do not support deep traversal.
    view.Traversal = ItemTraversal.Shallow;
    // Define the sort order.
    view.OrderBy.Add(ItemSchema.DateTimeReceived, SortDirection.Descending);
    try
    {
        // Call FindItems to find matching calendar items. 
        // The FindItems parameters must denote the mailbox owner,
        // mailbox, and Calendar folder.
        // This method call results in a FindItem call to EWS.
        FindItemsResults<Item> results = service.FindItems(
        new FolderId(WellKnownFolderName.Calendar, 
            "primary@contoso.com"), 
            filter, 
            view);
        foreach (Item item in results.Items)
        {
            Console.WriteLine("Subject: {0}", item.Subject);
            Console.WriteLine("Id: {0}", item.Id.ToString());
        }
    }
    catch (Exception ex)
    {
        Console.WriteLine("Exception while 
            enumerating results: {0}", ex.Message);
    }
}
```

<span data-ttu-id="f24a3-160">Después de la llamada **FindItems** devuelve una respuesta con el identificador, puede obtener, actualizar o eliminar dicha reunión mediante el identificador y el [acceso implícito](delegate-access-and-ews-in-exchange.md#bk_implicit) , y no es necesario especificar la dirección de SMTP del propietario del buzón.</span><span class="sxs-lookup"><span data-stu-id="f24a3-160">After the **FindItems** call returns a response with an ID, you can get, update or delete that meeting by using the ID and [implicit access](delegate-access-and-ews-in-exchange.md#bk_implicit) — and you do not need to specify the mailbox owner's SMTP address.</span></span> 
  
## <a name="search-for-a-meeting-or-appointment-as-a-delegate-by-using-ews"></a><span data-ttu-id="f24a3-161">Búsqueda de una reunión o cita como delegado mediante el uso de EWS</span><span class="sxs-lookup"><span data-stu-id="f24a3-161">Search for a meeting or appointment as a delegate by using EWS</span></span>
<span data-ttu-id="f24a3-162"><a name="bk_searchews"> </a></span><span class="sxs-lookup"><span data-stu-id="f24a3-162"></span></span>

<span data-ttu-id="f24a3-163">EWS le permite usar el objeto de servicio para el usuario delegado para buscar las citas y reuniones que cumplen un conjunto de criterios de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="f24a3-163">EWS enables you to use the service object for the delegate user to search for appointments and meetings that meet a set of search criteria.</span></span> <span data-ttu-id="f24a3-164">En este ejemplo se muestra cómo usar la operación [FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) para buscar las reuniones en la carpeta del calendario del propietario del buzón que contengan la palabra "building" en el asunto.</span><span class="sxs-lookup"><span data-stu-id="f24a3-164">This example shows how to use the [FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) operation to find meetings in the mailbox owner's Calendar folder that contain the word "building" in the subject.</span></span> 
  
<span data-ttu-id="f24a3-165">También es la solicitud XML que la API administrada de EWS envía cuando se utiliza el método **FindItem** a la [búsqueda de una reunión o cita como delegado](#bk_searchewsma).</span><span class="sxs-lookup"><span data-stu-id="f24a3-165">This is also the XML request that the EWS Managed API sends when you use the **FindItem** method to [search for a meeting or appointment as a delegate](#bk_searchewsma).</span></span>
  
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
          <t:Constant Value="building" />
        </t:Contains>
      </m:Restriction>
      <m:SortOrder>
        <t:FieldOrder Order="Descending">
          <t:FieldURI FieldURI="item:DateTimeReceived" />
        </t:FieldOrder>
      </m:SortOrder>
      <m:ParentFolderIds>
        <t:DistinguishedFolderId Id="calendar">
          <t:Mailbox>
            <t:EmailAddress>primary@contoso.com</t:EmailAddress>
          </t:Mailbox>
        </t:DistinguishedFolderId>
      </m:ParentFolderIds>
    </m:FindItem>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="f24a3-166">El servidor responde a la solicitud de **FindItem** con un mensaje de [FindItemResponse](http://msdn.microsoft.com/library/c8b316df-d4ab-49b8-96d4-8e9a016730ef%28Office.15%29.aspx) que incluye un valor de elemento [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) de **NoError**, lo que indica que la búsqueda que se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="f24a3-166">The server responds to the **FindItem** request with a [FindItemResponse](http://msdn.microsoft.com/library/c8b316df-d4ab-49b8-96d4-8e9a016730ef%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) element value of **NoError**, which indicates that the search completed successfully.</span></span> <span data-ttu-id="f24a3-167">La respuesta contiene un [CalendarItem](http://msdn.microsoft.com/library/b0c1fd27-b6da-46e5-88b8-88f00c71ba80%28Office.15%29.aspx) para cualquier citas o reuniones que cumplen los criterios de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="f24a3-167">The response contains a [CalendarItem](http://msdn.microsoft.com/library/b0c1fd27-b6da-46e5-88b8-88f00c71ba80%28Office.15%29.aspx) for any appointments or meetings that met the search criteria.</span></span> <span data-ttu-id="f24a3-168">En este caso, se ha encontrado sólo una de las reuniones.</span><span class="sxs-lookup"><span data-stu-id="f24a3-168">In this case, only one meeting is found.</span></span> 
  
<span data-ttu-id="f24a3-169">El valor del elemento [ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) se ha acortado para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="f24a3-169">The value of the [ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) element has been shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="893"
                         MinorBuildNumber="10"
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
              <t:CalendarItem>
                <t:ItemId Id="IJpUAAA="
                          ChangeKey="DwAAABYAAADOilbYa8KaT7ZgMoTz2P+hAAAAIKhS" />
                <t:Subject>Team building exercise</t:Subject>
                <t:DateTimeReceived>2014-03-04T21:27:22Z</t:DateTimeReceived>
              </t:CalendarItem>
            </t:Items>
          </m:RootFolder>
        </m:FindItemResponseMessage>
      </m:ResponseMessages>
    </m:FindItemResponse>
  </s:Body>
</s:Envelope>
```

<span data-ttu-id="f24a3-170">Ahora que tiene la **ItemId** para la reunión que cumpla los criterios, obtener, actualizar o eliminar dicha reunión mediante el [acceso implícito](delegate-access-and-ews-in-exchange.md#bk_implicit) y **ItemId** , y no es necesario especificar la dirección de SMTP del propietario del buzón.</span><span class="sxs-lookup"><span data-stu-id="f24a3-170">Now that you have the **ItemId** for the meeting that meets your criteria, you can get, update, or delete that meeting by using the **ItemId** and [implicit access](delegate-access-and-ews-in-exchange.md#bk_implicit) — and you do not need to specify the mailbox owner's SMTP address.</span></span> 
  
## <a name="get-update-or-delete-calendar-items-as-a-delegate-by-using-the-ews-managed-api"></a><span data-ttu-id="f24a3-171">Obtener, actualizar o eliminar elementos de calendario como delegado mediante el uso de la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="f24a3-171">Get, update, or delete calendar items as a delegate by using the EWS Managed API</span></span>
<span data-ttu-id="f24a3-172"><a name="bk_geteswma"> </a></span><span class="sxs-lookup"><span data-stu-id="f24a3-172"></span></span>

<span data-ttu-id="f24a3-173">Puede usar la API administrada de EWS para obtener, actualizar o eliminar una reunión o una cita de la misma manera que se realizan estas acciones cuando no está utilizando acceso delegado.</span><span class="sxs-lookup"><span data-stu-id="f24a3-173">You can use the EWS Managed API to get, update, or delete a meeting or appointment in the same way that you perform these actions when you're not using delegate access.</span></span> <span data-ttu-id="f24a3-174">La única diferencia es que el objeto de servicio para el usuario delegado.</span><span class="sxs-lookup"><span data-stu-id="f24a3-174">The only difference is that the service object is for the delegate user.</span></span> <span data-ttu-id="f24a3-175">El identificador de elemento incluido en la llamada al método **enlazar** de forma única identifica el elemento en el almacén de buzón de correo, en la carpeta del calendario del propietario del buzón.</span><span class="sxs-lookup"><span data-stu-id="f24a3-175">The item ID included in the **Bind** method call uniquely identifies the item in the mailbox store, in the mailbox owner's Calendar folder.</span></span> 
  
<span data-ttu-id="f24a3-176">**Tabla 2. Métodos de la API administrada de EWS para trabajar con las citas y reuniones como delegado**</span><span class="sxs-lookup"><span data-stu-id="f24a3-176">**Table 2. EWS Managed API methods for working with appointments and meetings as a delegate**</span></span>

|<span data-ttu-id="f24a3-177">**Tarea**</span><span class="sxs-lookup"><span data-stu-id="f24a3-177">**Task**</span></span>|<span data-ttu-id="f24a3-178">**Método de la API administrada de EWS**</span><span class="sxs-lookup"><span data-stu-id="f24a3-178">**EWS Managed API method**</span></span>|<span data-ttu-id="f24a3-179">**Ejemplo de código**</span><span class="sxs-lookup"><span data-stu-id="f24a3-179">**Code example**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f24a3-180">Obtener una cita o reunión</span><span class="sxs-lookup"><span data-stu-id="f24a3-180">Get an appointment or meeting</span></span>  <br/> |[<span data-ttu-id="f24a3-181">Enlazar</span><span class="sxs-lookup"><span data-stu-id="f24a3-181">Bind</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="f24a3-182">Obtener un elemento mediante el uso de la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="f24a3-182">Get an item by using the EWS Managed API</span></span>](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_getewsma) <br/> |
|<span data-ttu-id="f24a3-183">Actualización de una cita o reunión</span><span class="sxs-lookup"><span data-stu-id="f24a3-183">Update an appointment or meeting</span></span>  <br/> |<span data-ttu-id="f24a3-184">[Enlazar](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) seguido de [actualización](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.update%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f24a3-184">[Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) followed by [Update](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.update%28v=exchg.80%29.aspx)</span></span> <br/> |[<span data-ttu-id="f24a3-185">Actualización de una reunión mediante el uso de la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="f24a3-185">Update a meeting by using the EWS Managed API</span></span>](how-to-update-appointments-and-meetings-by-using-ews-in-exchange.md#bk_UpdateMtgEWSMA) <br/> |
|<span data-ttu-id="f24a3-186">Eliminar una reunión o cita</span><span class="sxs-lookup"><span data-stu-id="f24a3-186">Delete an appointment or meeting</span></span>  <br/> |<span data-ttu-id="f24a3-187">[Enlazar](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) seguido de [Eliminar](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.delete%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f24a3-187">[Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) followed by [Delete](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.delete%28v=exchg.80%29.aspx)</span></span> <br/> |[<span data-ttu-id="f24a3-188">Eliminar una reunión mediante el uso de la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="f24a3-188">Delete a meeting by using the EWS Managed API</span></span>](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md#bk_DeleteMtgEWSMA) <br/> |
   
## <a name="get-update-or-delete-calendar-items-as-a-delegate-by-using-ews"></a><span data-ttu-id="f24a3-189">Obtener, actualizar o eliminar elementos de calendario como delegado mediante el uso de EWS</span><span class="sxs-lookup"><span data-stu-id="f24a3-189">Get, update, or delete calendar items as a delegate by using EWS</span></span>
<span data-ttu-id="f24a3-190"><a name="bk_getews"> </a></span><span class="sxs-lookup"><span data-stu-id="f24a3-190"></span></span>

<span data-ttu-id="f24a3-191">Puede usar EWS para obtener, actualizar o eliminar una reunión o una cita de la misma manera que se realizan estas acciones cuando no está utilizando acceso delegado.</span><span class="sxs-lookup"><span data-stu-id="f24a3-191">You can use EWS to get, update, or delete a meeting or appointment in the same way that you perform these actions when you're not using delegate access.</span></span> <span data-ttu-id="f24a3-192">La única diferencia es que el objeto de servicio para el usuario delegado.</span><span class="sxs-lookup"><span data-stu-id="f24a3-192">The only difference is that the service object is for the delegate user.</span></span> <span data-ttu-id="f24a3-193">El identificador de elemento incluido en la llamada al método [GetItem](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) identifica de forma exclusiva identifica el elemento en el almacén de buzón de correo, en la carpeta del calendario del propietario del buzón.</span><span class="sxs-lookup"><span data-stu-id="f24a3-193">The item ID included in the [GetItem](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) method call uniquely identifies the item in the mailbox store, in the mailbox owner's Calendar folder.</span></span> 
  
<span data-ttu-id="f24a3-194">**Tabla 3. Operaciones de EWS para trabajar con las citas y reuniones como delegado**</span><span class="sxs-lookup"><span data-stu-id="f24a3-194">**Table 3. EWS operations for working with appointments and meetings as a delegate**</span></span>

|<span data-ttu-id="f24a3-195">**Tarea**</span><span class="sxs-lookup"><span data-stu-id="f24a3-195">**Task**</span></span>|<span data-ttu-id="f24a3-196">**Operación de EWS**</span><span class="sxs-lookup"><span data-stu-id="f24a3-196">**EWS operation**</span></span>|<span data-ttu-id="f24a3-197">**Ejemplo de código**</span><span class="sxs-lookup"><span data-stu-id="f24a3-197">**Code example**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f24a3-198">Obtener una cita o reunión</span><span class="sxs-lookup"><span data-stu-id="f24a3-198">Get an appointment or meeting</span></span>  <br/> |[<span data-ttu-id="f24a3-199">GetItem</span><span class="sxs-lookup"><span data-stu-id="f24a3-199">GetItem</span></span>](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) <br/> |[<span data-ttu-id="f24a3-200">Obtener un elemento mediante el uso de EWS</span><span class="sxs-lookup"><span data-stu-id="f24a3-200">Get an item by using EWS</span></span>](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_getews) <br/> |
|<span data-ttu-id="f24a3-201">Actualización de una cita o reunión</span><span class="sxs-lookup"><span data-stu-id="f24a3-201">Update an appointment or meeting</span></span>  <br/> |<span data-ttu-id="f24a3-202">[GetItem](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) seguido [UpdateItem](http://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f24a3-202">[GetItem](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) followed by [UpdateItem](http://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx)</span></span> <br/> |[<span data-ttu-id="f24a3-203">Actualización de una reunión mediante el uso de EWS</span><span class="sxs-lookup"><span data-stu-id="f24a3-203">Update a meeting by using EWS</span></span>](how-to-update-appointments-and-meetings-by-using-ews-in-exchange.md#bk_UpdateMtgEWS) <br/> |
|<span data-ttu-id="f24a3-204">Eliminar una reunión o cita</span><span class="sxs-lookup"><span data-stu-id="f24a3-204">Delete an appointment or meeting</span></span>  <br/> |<span data-ttu-id="f24a3-205">[GetItem](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) seguido [DeleteItem](http://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f24a3-205">[GetItem](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) followed by [DeleteItem](http://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx)</span></span> <br/> |[](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md#bk_DeleteMtgEWSMA) <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f24a3-206">Vea también</span><span class="sxs-lookup"><span data-stu-id="f24a3-206">See also</span></span>

- [<span data-ttu-id="f24a3-207">Acceso delegado y EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="f24a3-207">Delegate access and EWS in Exchange</span></span>](delegate-access-and-ews-in-exchange.md)   
- [<span data-ttu-id="f24a3-208">Agregar y quitar delegados mediante EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="f24a3-208">Add and remove delegates by using EWS in Exchange</span></span>](how-to-add-and-remove-delegates-by-using-ews-in-exchange.md)
- [<span data-ttu-id="f24a3-209">Establecer permisos de carpeta de otro usuario mediante el uso de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="f24a3-209">Set folder permissions for another user by using EWS in Exchange</span></span>](how-to-set-folder-permissions-for-another-user-by-using-ews-in-exchange.md) 
- [<span data-ttu-id="f24a3-210">Calendarios y EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="f24a3-210">Calendars and EWS in Exchange</span></span>](calendars-and-ews-in-exchange.md)
    

