---
title: Crear citas y reuniones mediante el uso de EWS en Exchange 2013
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: fdea70a4-9267-4e5d-9152-b749e2acc3b0
description: Aprenda a crear las citas y reuniones mediante la API administrada de EWS o EWS en Exchange.
ms.openlocfilehash: 1c840fac2ecca9fb51a28044dfac6299cb4fc038
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763056"
---
# <a name="create-appointments-and-meetings-by-using-ews-in-exchange-2013"></a><span data-ttu-id="c6157-103">Crear citas y reuniones mediante el uso de EWS en Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="c6157-103">Create appointments and meetings by using EWS in Exchange 2013</span></span>

<span data-ttu-id="c6157-104">Aprenda a crear las citas y reuniones mediante la API administrada de EWS o EWS en Exchange.</span><span class="sxs-lookup"><span data-stu-id="c6157-104">Learn how to create appointments and meetings by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="c6157-105">La diferencia entre las reuniones y citas esencial es que las reuniones tienen asistentes, y no las citas.</span><span class="sxs-lookup"><span data-stu-id="c6157-105">The essential difference between meetings and appointments is that meetings have attendees, and appointments don't.</span></span> <span data-ttu-id="c6157-106">Las citas y reuniones pueden ser instancias únicas o parte de una serie periódica pero, debido a que las citas no incluyen los asistentes, salas o recursos, no requieren que se envíe un mensaje.</span><span class="sxs-lookup"><span data-stu-id="c6157-106">Both appointments and meetings can be single instances or part of a recurring series, but because appointments don't include attendees, rooms, or resources, they do not require a message to be sent.</span></span> <span data-ttu-id="c6157-107">Internamente, Exchange utiliza el mismo objeto para las reuniones y citas.</span><span class="sxs-lookup"><span data-stu-id="c6157-107">Internally, Exchange uses the same object for both meetings and appointments.</span></span> <span data-ttu-id="c6157-108">Usar la API administrada de EWS [clase de cita](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) o el elemento EWS [CalendarItem](http://msdn.microsoft.com/library/Title Topic ID Project Name Writer Editor Publish Preview.aspx) para trabajar con las reuniones y citas.</span><span class="sxs-lookup"><span data-stu-id="c6157-108">You use the EWS Managed API [Appointment class](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) or the EWS [CalendarItem](http://msdn.microsoft.com/library/Title Topic ID Project Name Writer Editor Publish Preview.aspx) element to work with meetings and appointments.</span></span> 
  
<span data-ttu-id="c6157-109">**La tabla 1. Métodos de la API administrada de EWS y las operaciones de EWS para trabajar con las citas y reuniones**</span><span class="sxs-lookup"><span data-stu-id="c6157-109">**Table 1. EWS Managed API methods and EWS operations for working with appointments and meetings**</span></span>

|<span data-ttu-id="c6157-110">**Método de la API administrada de EWS**</span><span class="sxs-lookup"><span data-stu-id="c6157-110">**EWS Managed API method**</span></span>|<span data-ttu-id="c6157-111">**Operación de EWS**</span><span class="sxs-lookup"><span data-stu-id="c6157-111">**EWS operation**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c6157-112">Appointment.Save</span><span class="sxs-lookup"><span data-stu-id="c6157-112">Appointment.Save</span></span>](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.appointment.save%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="c6157-113">Operación CreateItem (elemento de calendario)</span><span class="sxs-lookup"><span data-stu-id="c6157-113">CreateItem operation (calendar item)</span></span>](http://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) <br/> |
|[<span data-ttu-id="c6157-114">Item.Bind</span><span class="sxs-lookup"><span data-stu-id="c6157-114">Item.Bind</span></span>](http://msdn.microsoft.com/es-es/library/dd634410%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="c6157-115">Operación GetItem (elemento de calendario)</span><span class="sxs-lookup"><span data-stu-id="c6157-115">GetItem operation (calendar item)</span></span>](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) <br/> |
   
## <a name="create-an-appointment-by-using-the-ews-managed-api"></a><span data-ttu-id="c6157-116">Crear una cita mediante el uso de la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="c6157-116">Create an appointment by using the EWS Managed API</span></span>
<span data-ttu-id="c6157-117"><a name="bk_CreateApptEWSMA"> </a></span><span class="sxs-lookup"><span data-stu-id="c6157-117"></span></span>

<span data-ttu-id="c6157-118">En el ejemplo de código siguiente se muestra cómo usar el [objeto Appointment](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) para crear una cita, el método [Save](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.appointment.save%28v=exchg.80%29.aspx) para guardar en la carpeta Calendario y el método [Item.Bind](http://msdn.microsoft.com/es-es/library/dd634410%28v=exchg.80%29.aspx) para comprobar que se ha creado la cita.</span><span class="sxs-lookup"><span data-stu-id="c6157-118">The following code example shows how to use the [Appointment object](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) to create an appointment, the [Save](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.appointment.save%28v=exchg.80%29.aspx) method to save it to your calendar folder, and the [Item.Bind](http://msdn.microsoft.com/es-es/library/dd634410%28v=exchg.80%29.aspx) method to verify that the appointment was created.</span></span> 
  
<span data-ttu-id="c6157-119">En este ejemplo se supone que se han autenticado a un servidor de Exchange y ha adquirido un objeto [ExchangeService](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) con el nombre de **servicio**.</span><span class="sxs-lookup"><span data-stu-id="c6157-119">This example assumes that you have authenticated to an Exchange server and have acquired an [ExchangeService](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object named **service**.</span></span> 
  
```cs
Appointment appointment = new Appointment(service);
// Set the properties on the appointment object to create the appointment.
appointment.Subject = "Tennis lesson";
appointment.Body = "Focus on backhand this week.";
appointment.Start = DateTime.Now.AddDays(2);
appointment.End = appointment.Start.AddHours(1);
appointment.Location = "Tennis club";
appointment.ReminderDueBy = DateTime.Now;
// Save the appointment to your calendar.
appointment.Save(SendInvitationsMode.SendToNone);
// Verify that the appointment was created by using the appointment's item ID.
Item item = Item.Bind(service, appointment.Id, new PropertySet(ItemSchema.Subject));
Console.WriteLine("\nAppointment created: " + item.Subject + "\n");

```

<span data-ttu-id="c6157-120">Después de establecer las propiedades en el objeto de cita, guarde la cita a la carpeta Calendario mediante el método de [Guardar](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.appointment.save%28v=exchg.80%29.aspx) del objeto cita.</span><span class="sxs-lookup"><span data-stu-id="c6157-120">After setting the properties on the appointment object, you save the appointment to the calendar folder by using the appointment object's [Save](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.appointment.save%28v=exchg.80%29.aspx) method.</span></span> 
  
<span data-ttu-id="c6157-121">Tenga en cuenta que en el paso de comprobación, use el elemento de [identificador](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) asociado con la cita para comprobar que la cita se encuentra en la carpeta del calendario.</span><span class="sxs-lookup"><span data-stu-id="c6157-121">Note that in the verification step, you use the item [Id](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) associated with the appointment to verify that the appointment is in the calendar folder.</span></span> <span data-ttu-id="c6157-122">Como procedimiento recomendado, limitar las propiedades devueltas por el servidor para que sólo lo que necesita, en este caso, la cita del asunto.</span><span class="sxs-lookup"><span data-stu-id="c6157-122">As a best practice, limit the properties returned by the server to only what you need — in this case, the appointment's subject.</span></span> 
  
## <a name="create-an-appointment-by-using-ews"></a><span data-ttu-id="c6157-123">Crear una cita mediante el uso de EWS</span><span class="sxs-lookup"><span data-stu-id="c6157-123">Create an appointment by using EWS</span></span>
<span data-ttu-id="c6157-124"><a name="bk_CreateApptEWS"> </a></span><span class="sxs-lookup"><span data-stu-id="c6157-124"></span></span>

<span data-ttu-id="c6157-125">La solicitud y respuesta XML en los ejemplos siguientes corresponden a las llamadas realizadas por el código de la API administrada de EWS en [crear una cita mediante el uso de la API administrada de EWS](#bk_CreateApptEWSMA).</span><span class="sxs-lookup"><span data-stu-id="c6157-125">The request and response XML in the following examples correspond to calls made by the EWS Managed API code in [Create an appointment by using the EWS Managed API](#bk_CreateApptEWSMA).</span></span> <span data-ttu-id="c6157-126">Así, se muestran la solicitud y respuesta XML que comprueba que los elementos de cita se encuentran en la carpeta del calendario.</span><span class="sxs-lookup"><span data-stu-id="c6157-126">The request and response XML that verifies that the appointment items are in the calendar folder are shown as well.</span></span>
  
<span data-ttu-id="c6157-127">En el ejemplo siguiente se muestra la solicitud XML al usar la operación [CreateItem](http://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) para crear una cita.</span><span class="sxs-lookup"><span data-stu-id="c6157-127">The following example shows the request XML when you use the [CreateItem](http://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) operation to create an appointment.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
       xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
       xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
       xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
    <t:TimeZoneContext>
      <t:TimeZoneDefinition Id="Pacific Standard Time" />
    </t:TimeZoneContext>
  </soap:Header>
  <soap:Body>
    <m:CreateItem SendMeetingInvitations="SendToNone">
      <m:Items>
        <t:CalendarItem>
          <t:Subject>Tennis lesson</t:Subject>
          <t:Body BodyType="HTML">Focus on backhand this week.</t:Body>
          <t:ReminderDueBy>2013-09-19T14:37:10.732-07:00</t:ReminderDueBy>
          <t:Start>2013-09-21T19:00:00.000Z</t:Start>
          <t:End>2013-09-21T20:00:00.000Z</t:End>
          <t:Location>Tennis club</t:Location>
          <t:MeetingTimeZone TimeZoneName="Pacific Standard Time" />
        </t:CalendarItem>
      </m:Items>
    </m:CreateItem>
  </soap:Body>
</soap:Envelope>
```

 <span data-ttu-id="c6157-128">En el ejemplo siguiente se muestra la respuesta XML que es devuelto por la operación **CreateItem** .</span><span class="sxs-lookup"><span data-stu-id="c6157-128">The following example shows the response XML that is returned by the **CreateItem** operation.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="c6157-129">Los atributos **ItemId** y **ChangeKey** se han abreviado para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="c6157-129">The **ItemId** and **ChangeKey** attributes have been shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="775" MinorBuildNumber="7" Version="V2_4" 
 xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
 xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
 xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
 xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:CreateItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
  xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:CreateItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Items>
            <t:CalendarItem>
              <t:ItemId Id="AAMkA" ChangeKey="DwAAA" />
            </t:CalendarItem>
          </m:Items>
        </m:CreateItemResponseMessage>
      </m:ResponseMessages>
    </m:CreateItemResponse>
  </s:Body>
</s:Envelope>

```

<span data-ttu-id="c6157-130">En el ejemplo siguiente se muestra la solicitud de XML que se genera cuando se usa la operación [GetItem](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) para comprobar que la cita se creó.</span><span class="sxs-lookup"><span data-stu-id="c6157-130">The following example shows the request XML that is generated when you use the [GetItem](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) operation to verify that the appointment was created.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="c6157-131">Los atributos **ItemId** y **ChangeKey** se han abreviado para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="c6157-131">The **ItemId** and **ChangeKey** attributes have been shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
       xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
       xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
       xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
    <t:TimeZoneContext>
      <t:TimeZoneDefinition Id="Pacific Standard Time" />
    </t:TimeZoneContext>
  </soap:Header>
  <soap:Body>
    <m:GetItem>
      <m:ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="item:Subject" />
        </t:AdditionalProperties>
      </m:ItemShape>
      <m:ItemIds>
        <t:ItemId Id="AAMkA" ChangeKey="DwAAA" />
      </m:ItemIds>
    </m:GetItem>
  </soap:Body>
</soap:Envelope>

```

 <span data-ttu-id="c6157-132">En el ejemplo siguiente se muestra la respuesta XML que es devuelto por la operación **GetItem** .</span><span class="sxs-lookup"><span data-stu-id="c6157-132">The following example shows the response XML that is returned by the **GetItem** operation.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="c6157-133">Los atributos **ItemId** y **ChangeKey** se han abreviado para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="c6157-133">The **ItemId** and **ChangeKey** attributes have been shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="775" MinorBuildNumber="7" Version="V2_4" 
 xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
 xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
 xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
 xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:GetItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Items>
            <t:CalendarItem>
              <t:ItemId Id="AAMkA" ChangeKey="DwAAA" />
              <t:Subject>Tennis lesson</t:Subject>
            </t:CalendarItem>
          </m:Items>
        </m:GetItemResponseMessage>
      </m:ResponseMessages>
    </m:GetItemResponse>
  </s:Body>
</s:Envelope>
```

## <a name="create-a-meeting-by-using-the-ews-managed-api"></a><span data-ttu-id="c6157-134">Crear una reunión mediante el uso de la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="c6157-134">Create a meeting by using the EWS Managed API</span></span>
<span data-ttu-id="c6157-135"><a name="bk_CreateMtgEWSMA"> </a></span><span class="sxs-lookup"><span data-stu-id="c6157-135"></span></span>

<span data-ttu-id="c6157-136">Cuando se crea una reunión, además de guardar un elemento en la carpeta del calendario, normalmente también desea enviar convocatorias de reunión a los asistentes.</span><span class="sxs-lookup"><span data-stu-id="c6157-136">When you create a meeting, in addition to saving an item to the calendar folder, you also typically want to send meeting requests to attendees.</span></span> <span data-ttu-id="c6157-137">En el ejemplo de código siguiente se muestra cómo crear una reunión y enviar convocatorias de reunión.</span><span class="sxs-lookup"><span data-stu-id="c6157-137">The following code example shows how to create a meeting and send meeting requests.</span></span>
  
<span data-ttu-id="c6157-138">En este ejemplo se supone que se han autenticado a un servidor de Exchange y ha adquirido un objeto [ExchangeService](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) con el nombre de **servicio**.</span><span class="sxs-lookup"><span data-stu-id="c6157-138">This example assumes that you have authenticated to an Exchange server and have acquired an [ExchangeService](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object named **service**.</span></span> 
  
```cs
Appointment meeting = new Appointment(service);
// Set the properties on the meeting object to create the meeting.
meeting.Subject = "Team building exercise";
meeting.Body = "Let's learn to really work as a team and then have lunch!";
meeting.Start = DateTime.Now.AddDays(2);            
meeting.End = meeting.Start.AddHours(4);
meeting.Location = "Conference Room 12";
meeting.RequiredAttendees.Add("Mack@contoso.com");
meeting.RequiredAttendees.Add("Sadie@contoso.com");
meeting.OptionalAttendees.Add("Magdalena@contoso.com");
meeting.ReminderMinutesBeforeStart = 60;
// Save the meeting to the Calendar folder and send the meeting request.
meeting.Save(SendInvitationsMode.SendToAllAndSaveCopy);
// Verify that the meeting was created.
Item item = Item.Bind(service, meeting.Id, new PropertySet(ItemSchema.Subject));
Console.WriteLine("\nMeeting created: " + item.Subject + "\n");

```

<span data-ttu-id="c6157-139">Después de establecer las propiedades en el objeto de [cita](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) , guardar la reunión a la carpeta Calendario mediante el método [Save](http://msdn.microsoft.com/es-es/library/dd635394%28v=exchg.80%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="c6157-139">After setting the properties on the [Appointment](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) object, save the meeting to your calendar folder by using the [Save](http://msdn.microsoft.com/es-es/library/dd635394%28v=exchg.80%29.aspx) method.</span></span> <span data-ttu-id="c6157-140">Cuando se establece el valor de la enumeración [SendInvitationsMode](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.sendinvitationsmode%28v=exchg.80%29.aspx) a **SendOnlyToAll** o **SendToAllAndSaveCopy**, se envían invitaciones a los asistentes.</span><span class="sxs-lookup"><span data-stu-id="c6157-140">When you set the [SendInvitationsMode](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.sendinvitationsmode%28v=exchg.80%29.aspx) enumeration value to **SendOnlyToAll** or **SendToAllAndSaveCopy**, invitations are sent to attendees.</span></span>
  
<span data-ttu-id="c6157-141">Use el elemento de [identificador](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) asociado con la reunión para comprobar que se guardó en la carpeta Calendario.</span><span class="sxs-lookup"><span data-stu-id="c6157-141">Use the item [Id](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) associated with the meeting to verify that it was saved in the calendar folder.</span></span> <span data-ttu-id="c6157-142">Como procedimiento recomendado, limite las propiedades devueltas por el servidor a sólo lo que necesita - en este caso, el asunto de la reunión.</span><span class="sxs-lookup"><span data-stu-id="c6157-142">As a best practice, limit the properties returned by the server to only what you need - in this case, the meeting's subject.</span></span> 
  
## <a name="create-a-meeting-by-using-ews"></a><span data-ttu-id="c6157-143">Crear una reunión mediante el uso de EWS</span><span class="sxs-lookup"><span data-stu-id="c6157-143">Create a meeting by using EWS</span></span>
<span data-ttu-id="c6157-144"><a name="bk_CreateMtgEWS"> </a></span><span class="sxs-lookup"><span data-stu-id="c6157-144"></span></span>

<span data-ttu-id="c6157-145">La solicitud y respuesta XML en los ejemplos siguientes corresponden a las llamadas realizadas por el código de la API administrada de EWS en [crear una reunión mediante el uso de la API administrada de EWS](#bk_CreateMtgEWSMA).</span><span class="sxs-lookup"><span data-stu-id="c6157-145">The request and response XML in the following examples correspond to calls made by the EWS Managed API code in [Create a meeting by using the EWS Managed API](#bk_CreateMtgEWSMA).</span></span> <span data-ttu-id="c6157-146">Así, se muestran la solicitud y respuesta XML que comprueba que los elementos de reunión están en la carpeta del calendario.</span><span class="sxs-lookup"><span data-stu-id="c6157-146">The request and response XML that verifies that the meeting items are in the calendar folder are shown as well.</span></span>
  
<span data-ttu-id="c6157-147">En el ejemplo siguiente se muestra la solicitud XML al usar la operación [CreateItem](http://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) para crear una reunión.</span><span class="sxs-lookup"><span data-stu-id="c6157-147">The following example shows the request XML when you use the [CreateItem](http://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) operation to create a meeting.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
       xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
    <t:TimeZoneContext>
      <t:TimeZoneDefinition Id="Pacific Standard Time" />
    </t:TimeZoneContext>
  </soap:Header>
  <soap:Body>
    <m:CreateItem SendMeetingInvitations="SendToAllAndSaveCopy">
      <m:Items>
        <t:CalendarItem>
          <t:Subject>Team building exercise</t:Subject>
          <t:Body BodyType="HTML">Let's learn to really work as a team and then have lunch!</t:Body>
          <t:ReminderMinutesBeforeStart>60</t:ReminderMinutesBeforeStart>
          <t:Start>2013-09-21T16:00:00.000Z</t:Start>
          <t:End>2013-09-21T20:00:00.000Z</t:End>
          <t:Location>Conference Room 12</t:Location>
          <t:RequiredAttendees>
            <t:Attendee>
              <t:Mailbox>
                <t:EmailAddress>Mack.Chaves@contoso.com</t:EmailAddress>
              </t:Mailbox>
            </t:Attendee>
            <t:Attendee>
              <t:Mailbox>
                <t:EmailAddress>Sadie.Daniels@contoso.com</t:EmailAddress>
              </t:Mailbox>
            </t:Attendee>
          </t:RequiredAttendees>
          <t:OptionalAttendees>
            <t:Attendee>
              <t:Mailbox>
                <t:EmailAddress>Magdalena.Kemp@contoso.com</t:EmailAddress>
              </t:Mailbox>
            </t:Attendee>
          </t:OptionalAttendees>
          <t:MeetingTimeZone TimeZoneName="Pacific Standard Time" />
        </t:CalendarItem>
      </m:Items>
    </m:CreateItem>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="c6157-148">En el ejemplo siguiente se muestra la respuesta XML que es devuelto por la operación **CreateItem** .</span><span class="sxs-lookup"><span data-stu-id="c6157-148">The following example shows the response XML that is returned by the **CreateItem** operation.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="c6157-149">Los atributos **ItemId** y **ChangeKey** se han abreviado para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="c6157-149">The **ItemId** and **ChangeKey** attributes have been shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="775" MinorBuildNumber="7" Version="V2_4" 
 xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
 xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
 xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:CreateItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:CreateItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Items>
            <t:CalendarItem>
              <t:ItemId Id="AAMkA" ChangeKey="DwAAA" />
            </t:CalendarItem>
          </m:Items>
        </m:CreateItemResponseMessage>
      </m:ResponseMessages>
    </m:CreateItemResponse>
  </s:Body>
</s:Envelope>
```

<span data-ttu-id="c6157-150">En el ejemplo siguiente se muestra la solicitud XML generado por la operación [GetItem](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) cuando compruebe que se ha creado la reunión.</span><span class="sxs-lookup"><span data-stu-id="c6157-150">The following example shows the request XML that is generated by the [GetItem](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) operation when you verify that the meeting was created.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="c6157-151">Los atributos **ItemId** y **ChangeKey** se han abreviado para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="c6157-151">The **ItemId** and **ChangeKey** attributes have been shortened for readability.</span></span> 
  
```xml
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
       xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
    <t:TimeZoneContext>
      <t:TimeZoneDefinition Id="Pacific Standard Time" />
    </t:TimeZoneContext>
  </soap:Header>
  <soap:Body>
    <m:GetItem>
      <m:ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="item:Subject" />
        </t:AdditionalProperties>
      </m:ItemShape>
      <m:ItemIds>
        <t:ItemId Id="AAMkA" ChangeKey="DwAAA" />
      </m:ItemIds>
    </m:GetItem>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="c6157-152">En el ejemplo siguiente se muestra la respuesta XML que es devuelto por la operación **GetItem** .</span><span class="sxs-lookup"><span data-stu-id="c6157-152">The following example shows the response XML that is returned by the **GetItem** operation.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="c6157-153">Los atributos **ItemId** y **ChangeKey** se han abreviado para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="c6157-153">The **ItemId** and **ChangeKey** attributes have been shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="775" MinorBuildNumber="7" Version="V2_4" 
 xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
 xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
 xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:GetItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Items>
            <t:CalendarItem>
              <t:ItemId Id="AAMkA" ChangeKey="DwAAA" />
              <t:Subject>Team building exercise</t:Subject>
            </t:CalendarItem>
          </m:Items>
        </m:GetItemResponseMessage>
      </m:ResponseMessages>
    </m:GetItemResponse>
  </s:Body>
</s:Envelope>
```

## <a name="see-also"></a><span data-ttu-id="c6157-154">Vea también</span><span class="sxs-lookup"><span data-stu-id="c6157-154">See also</span></span>

- [<span data-ttu-id="c6157-155">Calendarios y EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="c6157-155">Calendars and EWS in Exchange</span></span>](calendars-and-ews-in-exchange.md)  
- [<span data-ttu-id="c6157-156">Obtener las citas y reuniones con EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="c6157-156">Get appointments and meetings by using EWS in Exchange</span></span>](how-to-get-appointments-and-meetings-by-using-ews-in-exchange.md)  
- [<span data-ttu-id="c6157-157">Actualizar las citas y reuniones con EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="c6157-157">Update appointments and meetings by using EWS in Exchange</span></span>](how-to-update-appointments-and-meetings-by-using-ews-in-exchange.md) 
- [<span data-ttu-id="c6157-158">Eliminar las citas y cancelar reuniones mediante el uso de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="c6157-158">Delete appointments and cancel meetings by using EWS in Exchange</span></span>](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md) 
- [<span data-ttu-id="c6157-159">Proponer una nueva hora de reunión mediante el uso de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="c6157-159">Propose a new meeting time by using EWS in Exchange</span></span>](how-to-propose-a-new-meeting-time-by-using-ews-in-exchange.md)
    

