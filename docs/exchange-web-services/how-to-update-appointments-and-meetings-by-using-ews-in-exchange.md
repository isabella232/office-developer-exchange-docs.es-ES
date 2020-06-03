---
title: Actualizar citas y reuniones mediante EWS en Exchange
manager: sethgros
ms.date: 12/9/2015
ms.audience: Developer
ms.assetid: 13256625-083e-4a17-8fd1-2bed1f7cc14e
description: Obtenga información sobre cómo actualizar citas y reuniones mediante la API administrada de EWS o EWS en Exchange.
localization_priority: Priority
ms.openlocfilehash: 553f52e3d9c7119ee249e0e162d057e4acc993ff
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44527610"
---
# <a name="update-appointments-and-meetings-by-using-ews-in-exchange"></a><span data-ttu-id="25fe4-103">Actualizar citas y reuniones mediante EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="25fe4-103">Update appointments and meetings by using EWS in Exchange</span></span>

<span data-ttu-id="25fe4-104">Obtenga información sobre cómo actualizar citas y reuniones mediante la API administrada de EWS o EWS en Exchange.</span><span class="sxs-lookup"><span data-stu-id="25fe4-104">Learn how to update appointments and meetings by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="25fe4-105">La diferencia fundamental entre las reuniones y las citas es que las reuniones tienen asistentes y las citas no.</span><span class="sxs-lookup"><span data-stu-id="25fe4-105">The essential difference between meetings and appointments is that meetings have attendees, and appointments don't.</span></span> <span data-ttu-id="25fe4-106">Las citas y las reuniones pueden ser únicas o formar parte de una serie periódica, pero debido a que las citas no incluyen asistentes, salones o recursos, no necesitan que se envíe un mensaje.</span><span class="sxs-lookup"><span data-stu-id="25fe4-106">Both appointments and meetings can be single instances or part of a recurring series, but because appointments don't include attendees, rooms, or resources, they do not require a message to be sent.</span></span> <span data-ttu-id="25fe4-107">Internamente, Exchange usa el mismo objeto para las reuniones y las citas.</span><span class="sxs-lookup"><span data-stu-id="25fe4-107">Internally, Exchange uses the same object for both meetings and appointments.</span></span> <span data-ttu-id="25fe4-108">Use la [clase de cita](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) de API administrada EWS o el elemento [CalendarItem](https://msdn.microsoft.com/library/b0c1fd27-b6da-46e5-88b8-88f00c71ba80%28Office.15%29.aspx) de EWS para trabajar con reuniones y citas.</span><span class="sxs-lookup"><span data-stu-id="25fe4-108">You use the EWS Managed API [Appointment class](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) or the EWS [CalendarItem](https://msdn.microsoft.com/library/b0c1fd27-b6da-46e5-88b8-88f00c71ba80%28Office.15%29.aspx) element to work with meetings and appointments.</span></span> 
  
<span data-ttu-id="25fe4-109">**Tabla 1. Método de API administrada de EWS y operaciones de EWS para actualizar citas y reuniones**</span><span class="sxs-lookup"><span data-stu-id="25fe4-109">**Table 1. EWS Managed API method and EWS operations for updating appointments and meetings**</span></span>

|<span data-ttu-id="25fe4-110">**Método de la API administrada de EWS**</span><span class="sxs-lookup"><span data-stu-id="25fe4-110">**EWS Managed API method**</span></span>|<span data-ttu-id="25fe4-111">**Operaciones de EWS correspondientes**</span><span class="sxs-lookup"><span data-stu-id="25fe4-111">**Corresponding EWS operations**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="25fe4-112">Appointment. Update</span><span class="sxs-lookup"><span data-stu-id="25fe4-112">Appointment.Update</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.update%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="25fe4-113">UpdateItem</span><span class="sxs-lookup"><span data-stu-id="25fe4-113">UpdateItem</span></span>](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx)<br/><br/>          [<span data-ttu-id="25fe4-114">UpdateItemResponse</span><span class="sxs-lookup"><span data-stu-id="25fe4-114">UpdateItemResponse</span></span>](https://msdn.microsoft.com/library/023b79b4-c675-4669-9112-d85499ec4fc4%28Office.15%29.aspx) <br/> |
   
## <a name="update-an-appointment-by-using-the-ews-managed-api"></a><span data-ttu-id="25fe4-115">Actualizar una cita mediante la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="25fe4-115">Update an appointment by using the EWS Managed API</span></span>
<span data-ttu-id="25fe4-116"><a name="bk_UpdateApptEWSMA"> </a></span><span class="sxs-lookup"><span data-stu-id="25fe4-116"><a name="bk_UpdateApptEWSMA"> </a></span></span>

<span data-ttu-id="25fe4-117">En el ejemplo de código siguiente se muestra cómo usar el [objeto appointment](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) para actualizar las propiedades asociadas a una cita y el método [Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.update%28v=exchg.80%29.aspx) para guardar la cita en la carpeta del calendario.</span><span class="sxs-lookup"><span data-stu-id="25fe4-117">The following code example shows how to use the [Appointment object](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) to update properties associated with an appointment and the [Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.update%28v=exchg.80%29.aspx) method to save the appointment to your calendar folder.</span></span> 
  
<span data-ttu-id="25fe4-118">En este ejemplo se supone que se ha autenticado en un servidor de Exchange y que se ha adquirido un objeto [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) denominado **Service**.</span><span class="sxs-lookup"><span data-stu-id="25fe4-118">This example assumes that you have authenticated to an Exchange server and have acquired an [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object named **service**.</span></span> <span data-ttu-id="25fe4-119">La variable local `appointmentId` es un identificador asociado con una cita existente.</span><span class="sxs-lookup"><span data-stu-id="25fe4-119">The local variable  `appointmentId` is an identifier associated with an existing appointment.</span></span> 
  
```cs
// Instantiate an appointment object by binding to it by using the ItemId.
// As a best practice, limit the properties returned to only the ones you need.
Appointment appointment = Appointment.Bind(service, appointmentId, new PropertySet(AppointmentSchema.Subject, AppointmentSchema.Start, AppointmentSchema.End));
string oldSubject = appointment.Subject;
// Update properties on the appointment with a new subject, start time, and end time.
appointment.Subject = appointment.Subject + " moved one hour later and to the day after " + appointment.Start.DayOfWeek + "!";
appointment.Start.AddHours(25);
appointment.End.AddHours(25);
// Unless explicitly specified, the default is to use SendToAllAndSaveCopy.
// This can convert an appointment into a meeting. To avoid this,
// explicitly set SendToNone on non-meetings.
SendInvitationsOrCancellationsMode mode = appointment.IsMeeting ? 
    SendInvitationsOrCancellationsMode.SendToAllAndSaveCopy : SendInvitationsOrCancellationsMode.SendToNone;
// Send the update request to the Exchange server.
appointment.Update(ConflictResolutionMode.AlwaysOverwrite, mode);
// Verify the update.
Console.WriteLine("Subject for the appointment was \"" + oldSubject + "\". The new subject is \"" + appointment.Subject + "\"");

```

## <a name="update-an-appointment-by-using-ews"></a><span data-ttu-id="25fe4-120">Actualizar una cita mediante EWS</span><span class="sxs-lookup"><span data-stu-id="25fe4-120">Update an appointment by using EWS</span></span>
<span data-ttu-id="25fe4-121"><a name="bk_UpdateApptEWS"> </a></span><span class="sxs-lookup"><span data-stu-id="25fe4-121"><a name="bk_UpdateApptEWS"> </a></span></span>

<span data-ttu-id="25fe4-122">El XML de solicitud y respuesta de los ejemplos siguientes corresponden a las llamadas realizadas por el código de la API administrada de EWS en [actualizar una cita mediante la API administrada de EWS](#bk_UpdateApptEWSMA).</span><span class="sxs-lookup"><span data-stu-id="25fe4-122">The request and response XML in the following examples correspond to calls made by the EWS Managed API code in [Update an appointment by using the EWS Managed API](#bk_UpdateApptEWSMA).</span></span>
  
<span data-ttu-id="25fe4-123">En el ejemplo siguiente se muestra el XML de la solicitud cuando se usa la operación [UpdateItem](https://msdn.microsoft.com/library/34643d58-2743-45b0-a08d-bff6dc1da61d%28Office.15%29.aspx) para actualizar una cita.</span><span class="sxs-lookup"><span data-stu-id="25fe4-123">The following example shows the request XML when you use the [UpdateItem](https://msdn.microsoft.com/library/34643d58-2743-45b0-a08d-bff6dc1da61d%28Office.15%29.aspx) operation to update an appointment.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
       xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
    <t:TimeZoneContext>
      <t:TimeZoneDefinition Id="Pacific Standard Time" />
    </t:TimeZoneContext>
  </soap:Header>
  <soap:Body>
    <m:UpdateItem MessageDisposition="SaveOnly" ConflictResolution="AlwaysOverwrite" SendMeetingInvitationsOrCancellations="SendToNone">
      <m:ItemChanges>
        <t:ItemChange>
          <t:ItemId Id="AAMkA" ChangeKey="DwAAAB" />
          <t:Updates>
            <t:SetItemField>
              <t:FieldURI FieldURI="item:Subject" />
              <t:CalendarItem>
                <t:Subject>Tennis Lesson moved one hour later and to the day after Wednesday!</t:Subject>
              </t:CalendarItem>
            </t:SetItemField>
          </t:Updates>
        </t:ItemChange>
      </m:ItemChanges>
    </m:UpdateItem>
  </soap:Body>
</soap:Envelope>

```

<span data-ttu-id="25fe4-124">En el ejemplo siguiente se muestra el XML que se devuelve en respuesta a una solicitud [UpdateItem](https://msdn.microsoft.com/library/34643d58-2743-45b0-a08d-bff6dc1da61d%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="25fe4-124">The following example shows the XML that is returned in response to an [UpdateItem](https://msdn.microsoft.com/library/34643d58-2743-45b0-a08d-bff6dc1da61d%28Office.15%29.aspx) request.</span></span> <span data-ttu-id="25fe4-125">Los atributos **Itemid** y **changekey** se han abreviado para facilitar su lectura.</span><span class="sxs-lookup"><span data-stu-id="25fe4-125">The **ItemId** and **ChangeKey** attributes have been shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="815" MinorBuildNumber="6" Version="V2_7" 
 xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
 xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:UpdateItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="https://schemas.microsoft.com/exc
hange/services/2006/types">
      <m:ResponseMessages>
        <m:UpdateItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Items>
            <t:CalendarItem>
              <t:ItemId Id="AAMkA" ChangeKey="DwAAAB" />
            </t:CalendarItem>
          </m:Items>
          <m:ConflictResults>
            <t:Count>0</t:Count>
          </m:ConflictResults>
        </m:UpdateItemResponseMessage>
      </m:ResponseMessages>
    </m:UpdateItemResponse>
  </s:Body>
</s:Envelope>

```

## <a name="update-a-meeting-by-using-the-ews-managed-api"></a><span data-ttu-id="25fe4-126">Actualizar una reunión mediante la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="25fe4-126">Update a meeting by using the EWS Managed API</span></span>
<span data-ttu-id="25fe4-127"><a name="bk_UpdateMtgEWSMA"> </a></span><span class="sxs-lookup"><span data-stu-id="25fe4-127"><a name="bk_UpdateMtgEWSMA"> </a></span></span>

<span data-ttu-id="25fe4-128">Al actualizar una reunión, además de guardar el elemento de cita modificado en la carpeta del calendario, también suele ser conveniente enviar las convocatorias de reunión actualizadas a los asistentes.</span><span class="sxs-lookup"><span data-stu-id="25fe4-128">When you update a meeting, in addition to saving the modified appointment item to the calendar folder, you also typically want to send updated meeting requests to attendees.</span></span> <span data-ttu-id="25fe4-129">En el ejemplo de código siguiente se muestra cómo actualizar una reunión y enviar convocatorias de reunión.</span><span class="sxs-lookup"><span data-stu-id="25fe4-129">The following code example shows how to update a meeting and send meeting requests.</span></span>
  
<span data-ttu-id="25fe4-130">En este ejemplo se supone que se ha autenticado en un servidor de Exchange y que se ha adquirido un objeto [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) denominado **Service**.</span><span class="sxs-lookup"><span data-stu-id="25fe4-130">This example assumes that you have authenticated to an Exchange server and have acquired an [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object named **service**.</span></span> <span data-ttu-id="25fe4-131">La variable local `meetingId` es un identificador asociado con una cita existente.</span><span class="sxs-lookup"><span data-stu-id="25fe4-131">The local variable  `meetingId` is an identifier that is associated with an existing appointment.</span></span> 
  
```cs
// Instantiate an appointment object by binding to it using the ItemId.
// As a best practice, limit the properties returned to only the Appointment ID.
Appointment meeting = Appointment.Bind(service, meetingId, new PropertySet(AppointmentSchema.Subject, 
                                                                           AppointmentSchema.Location, 
                                                                           AppointmentSchema.RequiredAttendees, 
                                                                           AppointmentSchema.Resources));
string oldSubject = meeting.Subject;
// Update properties on the appointment with a new subject, location, an additional required attendee, and a resource.
meeting.Subject = "Team building exercise has moved!";
meeting.Location = "4567 Contoso Way, Redmond, OH 33333, USA";
meeting.RequiredAttendees.Add("alisa@contoso.com");
meeting.Resources.Add("dlpprojector@contoso.com");
// Send the update request to the Exchange server.
meeting.Update(ConflictResolutionMode.AlwaysOverwrite, SendInvitationsOrCancellationsMode.SendToAllAndSaveCopy);
// Verify the update.
Console.WriteLine("Subject for the meeting was \"" + oldSubject + "\". The new subject is \"" + meeting.Subject + "\"");

```

<span data-ttu-id="25fe4-132">Después de establecer las propiedades del objeto [appointment](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) , guarde la reunión en la carpeta del calendario y envíe las convocatorias de reunión actualizadas mediante el método [Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.update%28v=exchg.80%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="25fe4-132">After setting the properties on the [Appointment](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) object, save the meeting to your calendar folder and send updated meeting requests by using the [Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.update%28v=exchg.80%29.aspx) method.</span></span> 
  
<span data-ttu-id="25fe4-133">Puede pasar uno de dos valores de enumeración como parámetros al llamar al método [Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.update%28v=exchg.80%29.aspx) :</span><span class="sxs-lookup"><span data-stu-id="25fe4-133">You can pass in one of two enumeration values as parameters when you call the [Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.update%28v=exchg.80%29.aspx) method:</span></span> 
  
- <span data-ttu-id="25fe4-134">[Enumeración ConflictResolutionMode](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.conflictresolutionmode%28v=exchg.80%29.aspx) : determina cómo se administran los Estados conflictivos entre el cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="25fe4-134">[ConflictResolutionMode enumeration](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.conflictresolutionmode%28v=exchg.80%29.aspx) — Determines how conflicting states between client and server are handled.</span></span> 
    
- <span data-ttu-id="25fe4-135">[Enumeración SendInvitationsOrCancellationsMode](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.sendinvitationsorcancellationsmode%28v=exchg.80%29.aspx) : afecta al envío y al guardado de solicitudes de actualización de reuniones.</span><span class="sxs-lookup"><span data-stu-id="25fe4-135">[SendInvitationsOrCancellationsMode enumeration](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.sendinvitationsorcancellationsmode%28v=exchg.80%29.aspx) — Affects the sending and saving of meeting update requests.</span></span> 
    
<span data-ttu-id="25fe4-136">Cuando establece el valor de enumeración [ConflictResolutionMode](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.conflictresolutionmode%28v=exchg.80%29.aspx) en **AlwaysOverwrite**, la versión de la reunión siempre se guardará en la carpeta calendario.</span><span class="sxs-lookup"><span data-stu-id="25fe4-136">When you set the [ConflictResolutionMode](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.conflictresolutionmode%28v=exchg.80%29.aspx) enumeration value to **AlwaysOverwrite**, your version of the meeting will always be saved to the calendar folder.</span></span>
  
## <a name="update-a-meeting-by-using-ews"></a><span data-ttu-id="25fe4-137">Actualizar una reunión con EWS</span><span class="sxs-lookup"><span data-stu-id="25fe4-137">Update a meeting by using EWS</span></span>
<span data-ttu-id="25fe4-138"><a name="bk_UpdateMtgEWS"> </a></span><span class="sxs-lookup"><span data-stu-id="25fe4-138"><a name="bk_UpdateMtgEWS"> </a></span></span>

<span data-ttu-id="25fe4-139">El XML de solicitud y respuesta de los ejemplos siguientes corresponden a las llamadas realizadas por el código de la API administrada de EWS en [actualizar una reunión mediante la API administrada de EWS](#bk_UpdateMtgEWSMA).</span><span class="sxs-lookup"><span data-stu-id="25fe4-139">The request and response XML in the following examples correspond to calls made by the EWS Managed API code in [Update a meeting by using the EWS Managed API](#bk_UpdateMtgEWSMA).</span></span> 
  
<span data-ttu-id="25fe4-140">En el ejemplo siguiente se muestra el XML de la solicitud cuando se usa la operación [UpdateItem](https://msdn.microsoft.com/library/34643d58-2743-45b0-a08d-bff6dc1da61d%28Office.15%29.aspx) para actualizar una reunión.</span><span class="sxs-lookup"><span data-stu-id="25fe4-140">The following example shows the request XML when you use the [UpdateItem](https://msdn.microsoft.com/library/34643d58-2743-45b0-a08d-bff6dc1da61d%28Office.15%29.aspx) operation to update a meeting.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
    <t:TimeZoneContext>
      <t:TimeZoneDefinition Id="Pacific Standard Time" />
    </t:TimeZoneContext>
  </soap:Header>
  <soap:Body>
    <m:UpdateItem MessageDisposition="SaveOnly" ConflictResolution="AlwaysOverwrite" SendMeetingInvitationsOrCancellations="SendToAllAndSaveCopy">
      <m:ItemChanges>
        <t:ItemChange>
          <t:ItemId Id="AAMkA" ChangeKey="DwAAA" />
          <t:Updates>
            <t:SetItemField>
              <t:FieldURI FieldURI="item:Subject" />
              <t:CalendarItem>
                <t:Subject>Team building exercise has moved!</t:Subject>
              </t:CalendarItem>
            </t:SetItemField>
            <t:SetItemField>
              <t:FieldURI FieldURI="calendar:Location" />
              <t:CalendarItem>
                <t:Location>4567 Contoso Way, Redmond, OH 33333, USA</t:Location>
              </t:CalendarItem>
            </t:SetItemField>
            <t:SetItemField>
              <t:FieldURI FieldURI="calendar:RequiredAttendees" />
              <t:CalendarItem>
                <t:RequiredAttendees>
                  <t:Attendee>
                    <t:Mailbox>
                      <t:Name>Mack.Chaves@contoso.com</t:Name>
                      <t:EmailAddress>Mack.Chaves@contoso.com</t:EmailAddress>
                      <t:RoutingType>SMTP</t:RoutingType>
                    </t:Mailbox>
                  </t:Attendee>
                  <t:Attendee>
                    <t:Mailbox>
                      <t:Name>Sadie.Daniels@contoso.com</t:Name>
                      <t:EmailAddress>Sadie.Daniels@contoso.com</t:EmailAddress>
                      <t:RoutingType>SMTP</t:RoutingType>
                    </t:Mailbox>
                  </t:Attendee>
                  <t:Attendee>
                    <t:Mailbox>
                      <t:EmailAddress>alisa@contoso.com</t:EmailAddress>
                    </t:Mailbox>
                  </t:Attendee>
                </t:RequiredAttendees>
              </t:CalendarItem>
            </t:SetItemField>
            <t:SetItemField>
              <t:FieldURI FieldURI="calendar:Resources" />
              <t:CalendarItem>
                <t:Resources>
                  <t:Attendee>
                    <t:Mailbox>
                      <t:EmailAddress>dlpprojector@contoso.com</t:EmailAddress>
                    </t:Mailbox>
                  </t:Attendee>
                </t:Resources>
              </t:CalendarItem>
            </t:SetItemField>
          </t:Updates>
        </t:ItemChange>
      </m:ItemChanges>
    </m:UpdateItem>
  </soap:Body>
</soap:Envelope>
```

 <span data-ttu-id="25fe4-141">En el ejemplo siguiente se muestra el XML que se devuelve en respuesta a una solicitud [UpdateItem](https://msdn.microsoft.com/library/34643d58-2743-45b0-a08d-bff6dc1da61d%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="25fe4-141">The following example shows the XML that is returned in response to an [UpdateItem](https://msdn.microsoft.com/library/34643d58-2743-45b0-a08d-bff6dc1da61d%28Office.15%29.aspx) request.</span></span> <span data-ttu-id="25fe4-142">Los atributos **changekey** y **Itemid** se han abreviado para facilitar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="25fe4-142">The **ChangeKey** and **ItemId** attributes have been shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="815" MinorBuildNumber="6" Version="V2_7" 
 xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
 xmlns="https://schemas.microsoft.com/exchange/services/2006/types" xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
 xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:UpdateItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:UpdateItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Items>
            <t:CalendarItem>
              <t:ItemId Id="AAMkA" ChangeKey="DwAAA" />
            </t:CalendarItem>
          </m:Items>
          <m:ConflictResults>
            <t:Count>0</t:Count>
          </m:ConflictResults>
        </m:UpdateItemResponseMessage>
      </m:ResponseMessages>
    </m:UpdateItemResponse>
  </s:Body>
</s:Envelope>
```

## <a name="see-also"></a><span data-ttu-id="25fe4-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="25fe4-143">See also</span></span>

- [<span data-ttu-id="25fe4-144">Calendarios y EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="25fe4-144">Calendars and EWS in Exchange</span></span>](calendars-and-ews-in-exchange.md)   
- [<span data-ttu-id="25fe4-145">Crear citas y reuniones mediante EWS en Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="25fe4-145">Create appointments and meetings by using EWS in Exchange 2013</span></span>](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md)   
- [<span data-ttu-id="25fe4-146">Obtener citas y reuniones mediante EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="25fe4-146">Get appointments and meetings by using EWS in Exchange</span></span>](how-to-get-appointments-and-meetings-by-using-ews-in-exchange.md)  
- [<span data-ttu-id="25fe4-147">Eliminar citas y cancelar reuniones mediante EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="25fe4-147">Delete appointments and cancel meetings by using EWS in Exchange</span></span>](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md)  
- [<span data-ttu-id="25fe4-148">Proponer una nueva hora de reunión mediante EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="25fe4-148">Propose a new meeting time by using EWS in Exchange</span></span>](how-to-propose-a-new-meeting-time-by-using-ews-in-exchange.md)
    

