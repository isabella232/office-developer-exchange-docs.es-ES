---
title: Obtener acceso a un calendario como delegado mediante EWS en Exchange
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.assetid: d7db4a1e-9ed6-41da-8529-a73ca285cdf2
description: Obtenga información sobre cómo obtener acceso a un calendario como delegado mediante la API administrada de EWS o EWS en Exchange.
localization_priority: Priority
ms.openlocfilehash: 20ec294ddc4ccf014f0b2148c786c8c3ef8a6069
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44528296"
---
#  <a name="access-a-calendar-as-a-delegate-by-using-ews-in-exchange"></a><span data-ttu-id="a61d2-103">Obtener acceso a un calendario como delegado mediante EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="a61d2-103">Access a calendar as a delegate by using EWS in Exchange</span></span>

<span data-ttu-id="a61d2-104">Obtenga información sobre cómo obtener acceso a un calendario como delegado mediante la API administrada de EWS o EWS en Exchange.</span><span class="sxs-lookup"><span data-stu-id="a61d2-104">Learn how to access a calendar as a delegate by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="a61d2-105">Puede usar la API administrada de EWS o EWS para conceder a un usuario acceso delegado a la carpeta de calendario de un propietario del buzón.</span><span class="sxs-lookup"><span data-stu-id="a61d2-105">You can use the EWS Managed API or EWS to give a user delegate access to a mailbox owner's Calendar folder.</span></span> <span data-ttu-id="a61d2-106">A continuación, el delegado puede crear convocatorias de reunión en nombre del propietario del buzón, crear citas, responder a convocatorias de reunión y recuperar, actualizar y eliminar reuniones de la carpeta calendario del propietario del buzón, en función de sus permisos.</span><span class="sxs-lookup"><span data-stu-id="a61d2-106">The delegate can then create meeting requests on behalf of the mailbox owner, create appointments, respond to meeting requests, and retrieve, update, and delete meetings from the mailbox owner's Calendar folder, depending on their permissions.</span></span>
  
<span data-ttu-id="a61d2-107">Como delegado, se usan los mismos métodos y operaciones para tener acceso a la carpeta Calendario de un propietario del buzón que se usa para tener acceso a su propia carpeta calendario.</span><span class="sxs-lookup"><span data-stu-id="a61d2-107">As a delegate, you use the same methods and operations to access a mailbox owner's Calendar folder that you use to access your own Calendar folder.</span></span> <span data-ttu-id="a61d2-108">La principal diferencia es que tiene que usar el [acceso explícito](delegate-access-and-ews-in-exchange.md#bk_explicit) para buscar o crear un elemento de calendario o una subcarpeta de calendario y, después, después de identificar el identificador de elemento o la carpeta, puede usar el [acceso implícito](delegate-access-and-ews-in-exchange.md#bk_implicit) para obtener, actualizar o eliminar el elemento.</span><span class="sxs-lookup"><span data-stu-id="a61d2-108">The main difference is that you have to use [explicit access](delegate-access-and-ews-in-exchange.md#bk_explicit) to find or create a calendar item or calendar subfolder, and then after you identify the item ID or folder ID, you can use [implicit access](delegate-access-and-ews-in-exchange.md#bk_implicit) to get, update, or delete the item.</span></span> 
  
<span data-ttu-id="a61d2-109">**Tabla 1. Métodos de la API administrada de EWS y operaciones EWS para tener acceso a un calendario como delegado**</span><span class="sxs-lookup"><span data-stu-id="a61d2-109">**Table 1. EWS Managed API methods and EWS operations for accessing a calendar as a delegate**</span></span>

|<span data-ttu-id="a61d2-110">**Si quiere...**</span><span class="sxs-lookup"><span data-stu-id="a61d2-110">**If you want to…**</span></span>|<span data-ttu-id="a61d2-111">**Use este método de API administrada de EWS...**</span><span class="sxs-lookup"><span data-stu-id="a61d2-111">**Use this EWS Managed API method…**</span></span>|<span data-ttu-id="a61d2-112">**Usar esta operación de EWS...**</span><span class="sxs-lookup"><span data-stu-id="a61d2-112">**Use this EWS operation…**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a61d2-113">Crear una reunión o una cita como delegado</span><span class="sxs-lookup"><span data-stu-id="a61d2-113">Create a meeting or appointment as a delegate</span></span>  <br/> |<span data-ttu-id="a61d2-114">[Appointment. Save](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.save%28v=exchg.80%29.aspx) donde el parámetro [FolderId](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) proporciona [acceso explícito](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) a la carpeta de calendario del propietario del buzón de correo</span><span class="sxs-lookup"><span data-stu-id="a61d2-114">[Appointment.Save](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.save%28v=exchg.80%29.aspx) where the [FolderId](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) parameter provides [explicit access](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) to the mailbox owner's Calendar folder</span></span>  <br/> |<span data-ttu-id="a61d2-115">[CreateItem](https://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) donde el elemento [Mailbox](https://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) especifica el [EmailAddress](https://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) del propietario del buzón de correo</span><span class="sxs-lookup"><span data-stu-id="a61d2-115">[CreateItem](https://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) where the [Mailbox](https://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) element specifies the [EmailAddress](https://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) of the mailbox owner</span></span>  <br/> |
|<span data-ttu-id="a61d2-116">Crear varias reuniones o citas como delegado</span><span class="sxs-lookup"><span data-stu-id="a61d2-116">Create multiple meetings or appointments as a delegate</span></span>  <br/> |<span data-ttu-id="a61d2-117">[ExchangeService. CreateItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.createitems%28v=exchg.80%29.aspx) donde el parámetro **FolderId** proporciona [acceso explícito](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) a la carpeta de calendario del propietario del buzón de correo</span><span class="sxs-lookup"><span data-stu-id="a61d2-117">[ExchangeService.CreateItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.createitems%28v=exchg.80%29.aspx) where the **FolderId** parameter provides [explicit access](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) to the mailbox owner's Calendar folder</span></span>  <br/> |<span data-ttu-id="a61d2-118">[CreateItem](https://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) donde el elemento [Mailbox](https://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) especifica el [EmailAddress](https://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) del propietario del buzón de correo</span><span class="sxs-lookup"><span data-stu-id="a61d2-118">[CreateItem](https://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) where the [Mailbox](https://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) element specifies the [EmailAddress](https://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) of the mailbox owner</span></span>  <br/> |
|<span data-ttu-id="a61d2-119">Buscar o buscar una cita o reunión como delegado</span><span class="sxs-lookup"><span data-stu-id="a61d2-119">Search for or find an appointment or meeting as a delegate</span></span>  <br/> |<span data-ttu-id="a61d2-120">[ExchangeService. FindItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) donde el parámetro **FolderId** proporciona [acceso explícito](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) a la carpeta de calendario del propietario del buzón de correo</span><span class="sxs-lookup"><span data-stu-id="a61d2-120">[ExchangeService.FindItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) where the **FolderId** parameter provides [explicit access](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) to the mailbox owner's Calendar folder</span></span>  <br/> |<span data-ttu-id="a61d2-121">[FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) donde el elemento [Mailbox](https://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) especifica el [EmailAddress](https://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) del propietario del buzón.</span><span class="sxs-lookup"><span data-stu-id="a61d2-121">[FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) where the [Mailbox](https://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) element specifies the [EmailAddress](https://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) of the mailbox owner</span></span>  <br/> |
|<span data-ttu-id="a61d2-122">Obtener una cita o reunión como delegado</span><span class="sxs-lookup"><span data-stu-id="a61d2-122">Get an appointment or meeting as a delegate</span></span>  <br/> |[<span data-ttu-id="a61d2-123">Appointment. bind</span><span class="sxs-lookup"><span data-stu-id="a61d2-123">Appointment.Bind</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="a61d2-124">GetItem</span><span class="sxs-lookup"><span data-stu-id="a61d2-124">GetItem</span></span>](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="a61d2-125">Actualizar una cita o una reunión como delegado</span><span class="sxs-lookup"><span data-stu-id="a61d2-125">Update an appointment or meeting as a delegate</span></span>  <br/> |<span data-ttu-id="a61d2-126">[Appointment. bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) seguido de [appointment. Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.update%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a61d2-126">[Appointment.Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) followed by [Appointment.Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.update%28v=exchg.80%29.aspx)</span></span> <br/> |<span data-ttu-id="a61d2-127">[GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) seguido de [UpdateItem](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a61d2-127">[GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) followed by [UpdateItem](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx)</span></span> <br/> |
|<span data-ttu-id="a61d2-128">Eliminar una cita o una reunión como delegado</span><span class="sxs-lookup"><span data-stu-id="a61d2-128">Delete an appointment or meeting as a delegate</span></span>  <br/> |<span data-ttu-id="a61d2-129">[Appointment. bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) seguido de [appointment. Delete](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.delete%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a61d2-129">[Appointment.Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) followed by [Appointment.Delete](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.delete%28v=exchg.80%29.aspx)</span></span> <br/> |<span data-ttu-id="a61d2-130">[GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) seguido de [DeleteItem](../web-service-reference/deleteitem-operation.md)</span><span class="sxs-lookup"><span data-stu-id="a61d2-130">[GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) followed by [DeleteItem](../web-service-reference/deleteitem-operation.md)</span></span> <br/> |
   
> [!NOTE]
> <span data-ttu-id="a61d2-131">En los ejemplos de código de este artículo, primary@contoso.com es el propietario del buzón.</span><span class="sxs-lookup"><span data-stu-id="a61d2-131">In the code examples in this article, primary@contoso.com is the mailbox owner.</span></span> 
  
## <a name="prerequisite-tasks"></a><span data-ttu-id="a61d2-132">Tareas de requisitos previos</span><span class="sxs-lookup"><span data-stu-id="a61d2-132">Prerequisite tasks</span></span>
<span data-ttu-id="a61d2-133"><a name="bk_prereq"> </a></span><span class="sxs-lookup"><span data-stu-id="a61d2-133"><a name="bk_prereq"> </a></span></span>

<span data-ttu-id="a61d2-134">Para que un usuario pueda tener acceso a la carpeta del calendario de un propietario del buzón como delegado, el usuario debe [agregarse como delegado con permisos](how-to-add-and-remove-delegates-by-using-ews-in-exchange.md) para la carpeta de calendario del propietario del buzón.</span><span class="sxs-lookup"><span data-stu-id="a61d2-134">Before a user can access a mailbox owner's Calendar folder as a delegate, the user must be [added as a delegate with permissions](how-to-add-and-remove-delegates-by-using-ews-in-exchange.md) to the mailbox owner's Calendar folder.</span></span> 
  
<span data-ttu-id="a61d2-135">Un delegado debe tener un buzón adjunto a su cuenta para actualizar el calendario de un propietario del buzón.</span><span class="sxs-lookup"><span data-stu-id="a61d2-135">A delegate must have a mailbox attached to their account to update the calendar of a mailbox owner.</span></span>
  
<span data-ttu-id="a61d2-136">Si un delegado solo tiene que trabajar con convocatorias de reunión y respuestas, puede Agregar el delegado a la carpeta calendario y usar el valor predeterminado [MeetingRequestsDeliveryScope. DelegatesAndSendInformationToMe](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.meetingrequestsdeliveryscope%28v=exchg.80%29.aspx) de la enumeración de API administrada EWS o el valor [DeliverMeetingRequests](https://msdn.microsoft.com/library/04b999af-0b27-4e6d-a8b1-400955a1afaa%28Office.15%29.aspx) del elemento EWS de **DelegatesAndSendInformationToMe** para enviar las solicitudes al delegado y los mensajes informativos al propietario del buzón.</span><span class="sxs-lookup"><span data-stu-id="a61d2-136">If a delegate needs to work with meeting requests and responses only, you can add the delegate to the Calendar folder, and use the default [MeetingRequestsDeliveryScope.DelegatesAndSendInformationToMe](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.meetingrequestsdeliveryscope%28v=exchg.80%29.aspx) EWS Managed API enumeration value or the [DeliverMeetingRequests](https://msdn.microsoft.com/library/04b999af-0b27-4e6d-a8b1-400955a1afaa%28Office.15%29.aspx) EWS element value of **DelegatesAndSendInformationToMe** to send the requests to the delegate and informational messages to the mailbox owner.</span></span> <span data-ttu-id="a61d2-137">A continuación, no es necesario dar acceso al delegado a la carpeta Bandeja de entrada del propietario del buzón.</span><span class="sxs-lookup"><span data-stu-id="a61d2-137">The delegate then does not need to be given access to the mailbox owner's Inbox folder.</span></span> 
  
## <a name="create-a-meeting-or-appointment-as-a-delegate-by-using-the-ews-managed-api"></a><span data-ttu-id="a61d2-138">Crear una reunión o una cita como delegado mediante la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="a61d2-138">Create a meeting or appointment as a delegate by using the EWS Managed API</span></span>
<span data-ttu-id="a61d2-139"><a name="bk_createewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="a61d2-139"><a name="bk_createewsma"> </a></span></span>

<span data-ttu-id="a61d2-140">La API administrada de EWS permite usar el objeto de servicio para que el usuario delegado cree elementos de calendario para el propietario del buzón.</span><span class="sxs-lookup"><span data-stu-id="a61d2-140">The EWS Managed API enables you to use the service object for the delegate user to create calendar items for the mailbox owner.</span></span> <span data-ttu-id="a61d2-141">En este ejemplo se muestra cómo usar el método [Save](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.save%28v=exchg.80%29.aspx) para crear una reunión y enviar las convocatorias de reunión a los asistentes.</span><span class="sxs-lookup"><span data-stu-id="a61d2-141">This example shows how to use the [Save](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.save%28v=exchg.80%29.aspx) method to create a meeting and send meeting requests to the attendees.</span></span> 
  
<span data-ttu-id="a61d2-142">En este ejemplo se supone que el **servicio** es un objeto [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) válido para el delegado y que se han concedido al delegado los permisos adecuados para la carpeta de calendario del propietario del buzón.</span><span class="sxs-lookup"><span data-stu-id="a61d2-142">This example assumes that **service** is a valid [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object for the delegate and that the delegate has been granted the appropriate permissions for the mailbox owner's Calendar folder.</span></span> 
  
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

<span data-ttu-id="a61d2-143">Tenga en cuenta que, al guardar el elemento, la llamada al método [Save](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.save%28v=exchg.80%29.aspx) debe identificar la carpeta de calendario del propietario del buzón.</span><span class="sxs-lookup"><span data-stu-id="a61d2-143">Note that when you save the item, the [Save](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.save%28v=exchg.80%29.aspx) method call must identify the mailbox owner's Calendar folder.</span></span> <span data-ttu-id="a61d2-144">Si no se especifica la carpeta calendario del propietario del buzón, la convocatoria de reunión se guarda en el calendario del delegado y no en la carpeta calendario del propietario del buzón.</span><span class="sxs-lookup"><span data-stu-id="a61d2-144">If the mailbox owner's Calendar folder is not specified, the meeting request gets saved to the delegate's calendar and not the mailbox owner's Calendar folder.</span></span> <span data-ttu-id="a61d2-145">Puede incluir la carpeta de calendario del propietario del buzón de correo en la llamada al método **Save** de dos maneras.</span><span class="sxs-lookup"><span data-stu-id="a61d2-145">You can include the mailbox owner's Calendar folder in the **Save** method call in two ways.</span></span> <span data-ttu-id="a61d2-146">Se recomienda crear una instancia de una nueva instancia del objeto [FolderId](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) con el [WellKnownFolderName](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.wellknownfoldername%28v=exchg.80%29.aspx) y la dirección SMTP del propietario del buzón.</span><span class="sxs-lookup"><span data-stu-id="a61d2-146">We recommend that you instantiate a new instance of the [FolderId](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) object by using the [WellKnownFolderName](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.wellknownfoldername%28v=exchg.80%29.aspx) and the SMTP address of the mailbox owner.</span></span> 
  
```cs
meeting.Save(new FolderId(WellKnownFolderName.Calendar,
    "primary@contoso.com"), SendInvitationsMode.SendToAllAndSaveCopy);
```

<span data-ttu-id="a61d2-147">Sin embargo, también puede [enlazar](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) a la carpeta de calendario y, a continuación, usar el identificador de la carpeta en la llamada al método **Save** .</span><span class="sxs-lookup"><span data-stu-id="a61d2-147">However, you can also [Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) to the Calendar folder first, and then use the ID of the folder in the **Save** method call.</span></span> <span data-ttu-id="a61d2-148">Sin embargo, tenga en cuenta que esto crea una llamada a EWS adicional.</span><span class="sxs-lookup"><span data-stu-id="a61d2-148">Be aware, however, that this creates an extra EWS call.</span></span> 
  
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

## <a name="create-a-meeting-or-appointment-as-a-delegate-by-using-ews"></a><span data-ttu-id="a61d2-149">Crear una reunión o una cita como delegado mediante EWS</span><span class="sxs-lookup"><span data-stu-id="a61d2-149">Create a meeting or appointment as a delegate by using EWS</span></span>
<span data-ttu-id="a61d2-150"><a name="bk_createews"> </a></span><span class="sxs-lookup"><span data-stu-id="a61d2-150"><a name="bk_createews"> </a></span></span>

<span data-ttu-id="a61d2-151">EWS permite usar el objeto de servicio para que el usuario delegado cree elementos de calendario para el propietario del buzón.</span><span class="sxs-lookup"><span data-stu-id="a61d2-151">EWS enables you to use the service object for the delegate user to create calendar items for the mailbox owner.</span></span> <span data-ttu-id="a61d2-152">En este ejemplo se muestra cómo usar la operación [CreateItem](https://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) para crear una reunión y enviar las convocatorias de reunión a los asistentes.</span><span class="sxs-lookup"><span data-stu-id="a61d2-152">This example shows how to use the [CreateItem](https://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) operation to create a meeting and send meeting requests to the attendees.</span></span> 
  
<span data-ttu-id="a61d2-153">También es la solicitud XML que la API administrada de EWS envía cuando se usa el método **Save** para [crear una reunión o cita como delegado](#bk_createewsma).</span><span class="sxs-lookup"><span data-stu-id="a61d2-153">This is also the XML request that the EWS Managed API sends when you use the **Save** method to [create a meeting or appointment as a delegate](#bk_createewsma).</span></span>
  
<span data-ttu-id="a61d2-154">El encabezado SOAP se ha quitado del ejemplo siguiente por motivos de brevedad.</span><span class="sxs-lookup"><span data-stu-id="a61d2-154">The SOAP header has been removed from the following example for brevity.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
         xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
         xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
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

<span data-ttu-id="a61d2-155">El servidor responde a la solicitud **CreateItem** con un mensaje [CreateItemResponse](https://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) que incluye un valor de elemento [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) de **NoError**, que indica que la reunión se ha creado correctamente.</span><span class="sxs-lookup"><span data-stu-id="a61d2-155">The server responds to the **CreateItem** request with a [CreateItemResponse](https://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) message that includes a [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) element value of **NoError**, which indicates that the meeting was created successfully.</span></span> <span data-ttu-id="a61d2-156">La respuesta también contiene el identificador de elemento de la reunión recién creada.</span><span class="sxs-lookup"><span data-stu-id="a61d2-156">The response also contains the item ID of the newly created meeting.</span></span>
  
## <a name="search-for-a-meeting-or-appointment-as-a-delegate-by-using-the-ews-managed-api"></a><span data-ttu-id="a61d2-157">Buscar una reunión o una cita como delegado mediante la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="a61d2-157">Search for a meeting or appointment as a delegate by using the EWS Managed API</span></span>
<span data-ttu-id="a61d2-158"><a name="bk_searchewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="a61d2-158"><a name="bk_searchewsma"> </a></span></span>

<span data-ttu-id="a61d2-159">Para buscar una reunión, debe usar uno de los métodos [ExchangeService. FindItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) que incluya un parámetro [FolderId](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) , de modo que pueda especificar la carpeta de calendario del propietario del buzón.</span><span class="sxs-lookup"><span data-stu-id="a61d2-159">To search for a meeting, you must use one of the [ExchangeService.FindItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) methods that includes a [FolderId](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) parameter, so that you can specify the mailbox owner's Calendar folder.</span></span> 
  
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

<span data-ttu-id="a61d2-160">Una vez que la llamada de **FindItems** devuelve una respuesta con un identificador, puede obtener, actualizar o eliminar esa reunión con el identificador y el [acceso implícito](delegate-access-and-ews-in-exchange.md#bk_implicit) , y no es necesario especificar la dirección SMTP del propietario del buzón.</span><span class="sxs-lookup"><span data-stu-id="a61d2-160">After the **FindItems** call returns a response with an ID, you can get, update or delete that meeting by using the ID and [implicit access](delegate-access-and-ews-in-exchange.md#bk_implicit) — and you do not need to specify the mailbox owner's SMTP address.</span></span> 
  
## <a name="search-for-a-meeting-or-appointment-as-a-delegate-by-using-ews"></a><span data-ttu-id="a61d2-161">Buscar una reunión o una cita como delegado mediante EWS</span><span class="sxs-lookup"><span data-stu-id="a61d2-161">Search for a meeting or appointment as a delegate by using EWS</span></span>
<span data-ttu-id="a61d2-162"><a name="bk_searchews"> </a></span><span class="sxs-lookup"><span data-stu-id="a61d2-162"><a name="bk_searchews"> </a></span></span>

<span data-ttu-id="a61d2-163">EWS permite usar el objeto de servicio para que el usuario delegado busque citas y reuniones que cumplan un conjunto de criterios de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="a61d2-163">EWS enables you to use the service object for the delegate user to search for appointments and meetings that meet a set of search criteria.</span></span> <span data-ttu-id="a61d2-164">En este ejemplo se muestra cómo usar la operación [FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) para buscar reuniones en la carpeta calendario del propietario del buzón que contengan la palabra "Building" en el asunto.</span><span class="sxs-lookup"><span data-stu-id="a61d2-164">This example shows how to use the [FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) operation to find meetings in the mailbox owner's Calendar folder that contain the word "building" in the subject.</span></span> 
  
<span data-ttu-id="a61d2-165">También es la solicitud XML que la API administrada de EWS envía cuando se usa el método **FindItem** para [buscar una reunión o cita como delegado](#bk_searchewsma).</span><span class="sxs-lookup"><span data-stu-id="a61d2-165">This is also the XML request that the EWS Managed API sends when you use the **FindItem** method to [search for a meeting or appointment as a delegate](#bk_searchewsma).</span></span>
  
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

<span data-ttu-id="a61d2-166">El servidor responde a la solicitud **FindItem** con un mensaje [FindItemResponse](https://msdn.microsoft.com/library/c8b316df-d4ab-49b8-96d4-8e9a016730ef%28Office.15%29.aspx) que incluye un valor de elemento [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) de **NoError**, lo que indica que la búsqueda se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="a61d2-166">The server responds to the **FindItem** request with a [FindItemResponse](https://msdn.microsoft.com/library/c8b316df-d4ab-49b8-96d4-8e9a016730ef%28Office.15%29.aspx) message that includes a [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) element value of **NoError**, which indicates that the search completed successfully.</span></span> <span data-ttu-id="a61d2-167">La respuesta contiene un [CalendarItem](https://msdn.microsoft.com/library/b0c1fd27-b6da-46e5-88b8-88f00c71ba80%28Office.15%29.aspx) para las citas o reuniones que cumplen los criterios de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="a61d2-167">The response contains a [CalendarItem](https://msdn.microsoft.com/library/b0c1fd27-b6da-46e5-88b8-88f00c71ba80%28Office.15%29.aspx) for any appointments or meetings that met the search criteria.</span></span> <span data-ttu-id="a61d2-168">En este caso, solo se encuentra una reunión.</span><span class="sxs-lookup"><span data-stu-id="a61d2-168">In this case, only one meeting is found.</span></span> 
  
<span data-ttu-id="a61d2-169">El valor del elemento [Itemid](https://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) se ha abreviado para facilitar su lectura.</span><span class="sxs-lookup"><span data-stu-id="a61d2-169">The value of the [ItemId](https://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) element has been shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="893"
                         MinorBuildNumber="10"
                         Version="V2_10"
                         xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body>
    <m:FindItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                        xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
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

<span data-ttu-id="a61d2-170">Ahora que tiene el **Itemid** para la reunión que cumple con los criterios, puede obtener, actualizar o eliminar esa reunión mediante el uso de **Itemid** y el [acceso implícito](delegate-access-and-ews-in-exchange.md#bk_implicit) , y no es necesario especificar la dirección SMTP del propietario del buzón.</span><span class="sxs-lookup"><span data-stu-id="a61d2-170">Now that you have the **ItemId** for the meeting that meets your criteria, you can get, update, or delete that meeting by using the **ItemId** and [implicit access](delegate-access-and-ews-in-exchange.md#bk_implicit) — and you do not need to specify the mailbox owner's SMTP address.</span></span> 
  
## <a name="get-update-or-delete-calendar-items-as-a-delegate-by-using-the-ews-managed-api"></a><span data-ttu-id="a61d2-171">Obtener, actualizar o eliminar elementos de calendario como delegado mediante la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="a61d2-171">Get, update, or delete calendar items as a delegate by using the EWS Managed API</span></span>
<span data-ttu-id="a61d2-172"><a name="bk_geteswma"> </a></span><span class="sxs-lookup"><span data-stu-id="a61d2-172"><a name="bk_geteswma"> </a></span></span>

<span data-ttu-id="a61d2-173">Puede usar la API administrada de EWS para obtener, actualizar o eliminar una reunión o cita de la misma manera en que realiza estas acciones cuando no usa el acceso de delegado.</span><span class="sxs-lookup"><span data-stu-id="a61d2-173">You can use the EWS Managed API to get, update, or delete a meeting or appointment in the same way that you perform these actions when you're not using delegate access.</span></span> <span data-ttu-id="a61d2-174">La única diferencia es que el objeto de servicio es para el usuario delegado.</span><span class="sxs-lookup"><span data-stu-id="a61d2-174">The only difference is that the service object is for the delegate user.</span></span> <span data-ttu-id="a61d2-175">El identificador de elemento incluido en la llamada al método **BIND** identifica de forma única el elemento en el almacén de buzones, en la carpeta calendario del propietario del buzón.</span><span class="sxs-lookup"><span data-stu-id="a61d2-175">The item ID included in the **Bind** method call uniquely identifies the item in the mailbox store, in the mailbox owner's Calendar folder.</span></span> 
  
<span data-ttu-id="a61d2-176">**Tabla 2. Métodos de la API administrada de EWS para trabajar con citas y reuniones como delegado**</span><span class="sxs-lookup"><span data-stu-id="a61d2-176">**Table 2. EWS Managed API methods for working with appointments and meetings as a delegate**</span></span>

|<span data-ttu-id="a61d2-177">**Tarea**</span><span class="sxs-lookup"><span data-stu-id="a61d2-177">**Task**</span></span>|<span data-ttu-id="a61d2-178">**Método de la API administrada de EWS**</span><span class="sxs-lookup"><span data-stu-id="a61d2-178">**EWS Managed API method**</span></span>|<span data-ttu-id="a61d2-179">**Ejemplo de código**</span><span class="sxs-lookup"><span data-stu-id="a61d2-179">**Code example**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a61d2-180">Obtener una cita o una reunión</span><span class="sxs-lookup"><span data-stu-id="a61d2-180">Get an appointment or meeting</span></span>  <br/> |[<span data-ttu-id="a61d2-181">BIND</span><span class="sxs-lookup"><span data-stu-id="a61d2-181">Bind</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="a61d2-182">Obtener un elemento mediante la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="a61d2-182">Get an item by using the EWS Managed API</span></span>](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_getewsma) <br/> |
|<span data-ttu-id="a61d2-183">Actualizar una cita o una reunión</span><span class="sxs-lookup"><span data-stu-id="a61d2-183">Update an appointment or meeting</span></span>  <br/> |<span data-ttu-id="a61d2-184">[Enlazar](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) seguido de [Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.update%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a61d2-184">[Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) followed by [Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.update%28v=exchg.80%29.aspx)</span></span> <br/> |[<span data-ttu-id="a61d2-185">Actualizar una reunión mediante la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="a61d2-185">Update a meeting by using the EWS Managed API</span></span>](how-to-update-appointments-and-meetings-by-using-ews-in-exchange.md#bk_UpdateMtgEWSMA) <br/> |
|<span data-ttu-id="a61d2-186">Eliminar una cita o una reunión</span><span class="sxs-lookup"><span data-stu-id="a61d2-186">Delete an appointment or meeting</span></span>  <br/> |<span data-ttu-id="a61d2-187">[Enlazar](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) seguida de [eliminar](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.delete%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a61d2-187">[Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) followed by [Delete](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.delete%28v=exchg.80%29.aspx)</span></span> <br/> |[<span data-ttu-id="a61d2-188">Eliminar una reunión mediante la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="a61d2-188">Delete a meeting by using the EWS Managed API</span></span>](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md#bk_DeleteMtgEWSMA) <br/> |
   
## <a name="get-update-or-delete-calendar-items-as-a-delegate-by-using-ews"></a><span data-ttu-id="a61d2-189">Obtener, actualizar o eliminar elementos de calendario como delegado mediante EWS</span><span class="sxs-lookup"><span data-stu-id="a61d2-189">Get, update, or delete calendar items as a delegate by using EWS</span></span>
<span data-ttu-id="a61d2-190"><a name="bk_getews"> </a></span><span class="sxs-lookup"><span data-stu-id="a61d2-190"><a name="bk_getews"> </a></span></span>

<span data-ttu-id="a61d2-191">Puede usar EWS para obtener, actualizar o eliminar una reunión o cita de la misma manera en que realiza estas acciones cuando no está usando acceso delegado.</span><span class="sxs-lookup"><span data-stu-id="a61d2-191">You can use EWS to get, update, or delete a meeting or appointment in the same way that you perform these actions when you're not using delegate access.</span></span> <span data-ttu-id="a61d2-192">La única diferencia es que el objeto de servicio es para el usuario delegado.</span><span class="sxs-lookup"><span data-stu-id="a61d2-192">The only difference is that the service object is for the delegate user.</span></span> <span data-ttu-id="a61d2-193">El identificador de elemento incluido en la llamada al método [GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) identifica de forma única el elemento en el almacén de buzones, en la carpeta calendario del propietario del buzón.</span><span class="sxs-lookup"><span data-stu-id="a61d2-193">The item ID included in the [GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) method call uniquely identifies the item in the mailbox store, in the mailbox owner's Calendar folder.</span></span> 
  
<span data-ttu-id="a61d2-194">**Tabla 3. Operaciones de EWS para trabajar con citas y reuniones como delegado**</span><span class="sxs-lookup"><span data-stu-id="a61d2-194">**Table 3. EWS operations for working with appointments and meetings as a delegate**</span></span>

|<span data-ttu-id="a61d2-195">**Tarea**</span><span class="sxs-lookup"><span data-stu-id="a61d2-195">**Task**</span></span>|<span data-ttu-id="a61d2-196">**Operación de EWS**</span><span class="sxs-lookup"><span data-stu-id="a61d2-196">**EWS operation**</span></span>|<span data-ttu-id="a61d2-197">**Ejemplo de código**</span><span class="sxs-lookup"><span data-stu-id="a61d2-197">**Code example**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a61d2-198">Obtener una cita o una reunión</span><span class="sxs-lookup"><span data-stu-id="a61d2-198">Get an appointment or meeting</span></span>  <br/> |[<span data-ttu-id="a61d2-199">GetItem</span><span class="sxs-lookup"><span data-stu-id="a61d2-199">GetItem</span></span>](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) <br/> |[<span data-ttu-id="a61d2-200">Obtener un elemento mediante EWS</span><span class="sxs-lookup"><span data-stu-id="a61d2-200">Get an item by using EWS</span></span>](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_getews) <br/> |
|<span data-ttu-id="a61d2-201">Actualizar una cita o una reunión</span><span class="sxs-lookup"><span data-stu-id="a61d2-201">Update an appointment or meeting</span></span>  <br/> |<span data-ttu-id="a61d2-202">[GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) seguido de [UpdateItem](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a61d2-202">[GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) followed by [UpdateItem](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx)</span></span> <br/> |[<span data-ttu-id="a61d2-203">Actualizar una reunión con EWS</span><span class="sxs-lookup"><span data-stu-id="a61d2-203">Update a meeting by using EWS</span></span>](how-to-update-appointments-and-meetings-by-using-ews-in-exchange.md#bk_UpdateMtgEWS) <br/> |
|<span data-ttu-id="a61d2-204">Eliminar una cita o una reunión</span><span class="sxs-lookup"><span data-stu-id="a61d2-204">Delete an appointment or meeting</span></span>  <br/> |<span data-ttu-id="a61d2-205">[GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) seguido de [DeleteItem](../web-service-reference/deleteitem-operation.md)</span><span class="sxs-lookup"><span data-stu-id="a61d2-205">[GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) followed by [DeleteItem](../web-service-reference/deleteitem-operation.md)</span></span> <br/> |[](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md#bk_DeleteMtgEWSMA) <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a61d2-206">Vea también</span><span class="sxs-lookup"><span data-stu-id="a61d2-206">See also</span></span>

- [<span data-ttu-id="a61d2-207">Acceso delegado y EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="a61d2-207">Delegate access and EWS in Exchange</span></span>](delegate-access-and-ews-in-exchange.md)   
- [<span data-ttu-id="a61d2-208">Agregar y quitar delegados mediante EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="a61d2-208">Add and remove delegates by using EWS in Exchange</span></span>](how-to-add-and-remove-delegates-by-using-ews-in-exchange.md)
- [<span data-ttu-id="a61d2-209">Establecer los permisos de carpeta para otro usuario mediante EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="a61d2-209">Set folder permissions for another user by using EWS in Exchange</span></span>](how-to-set-folder-permissions-for-another-user-by-using-ews-in-exchange.md) 
- [<span data-ttu-id="a61d2-210">Calendarios y EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="a61d2-210">Calendars and EWS in Exchange</span></span>](calendars-and-ews-in-exchange.md)
    

