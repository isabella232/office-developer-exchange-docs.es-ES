---
title: Crear citas y reuniones mediante EWS en Exchange 2013
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: fdea70a4-9267-4e5d-9152-b749e2acc3b0
description: Obtenga información sobre cómo crear citas y reuniones mediante la API administrada de EWS o EWS en Exchange.
localization_priority: Priority
ms.openlocfilehash: b617519b839fb5ad310fbcaf6fae065f71f0f165
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44528233"
---
# <a name="create-appointments-and-meetings-by-using-ews-in-exchange-2013"></a>Crear citas y reuniones mediante EWS en Exchange 2013

Obtenga información sobre cómo crear citas y reuniones mediante la API administrada de EWS o EWS en Exchange.
  
La diferencia fundamental entre las reuniones y las citas es que las reuniones tienen asistentes y las citas no. Las citas y las reuniones pueden ser únicas o formar parte de una serie periódica, pero debido a que las citas no incluyen asistentes, salones o recursos, no necesitan que se envíe un mensaje. Internamente, Exchange usa el mismo objeto para las reuniones y las citas. Use la [clase de cita](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) de API administrada EWS o el elemento [CalendarItem](https://msdn.microsoft.com/library/Title Topic ID Project Name Writer Editor Publish Preview.aspx) de EWS para trabajar con reuniones y citas. 
  
**Tabla 1. Métodos de API administrada de EWS y operaciones de EWS para trabajar con citas y reuniones**

|**Método de la API administrada de EWS**|**Operación de EWS**|
|:-----|:-----|
|[Appointment. Save](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.save%28v=exchg.80%29.aspx) <br/> |[Operación CreateItem (elemento de calendario)](https://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) <br/> |
|[Item. bind](https://msdn.microsoft.com/library/dd634410%28v=exchg.80%29.aspx) <br/> |[Operación GetItem (elemento de calendario)](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) <br/> |
   
## <a name="create-an-appointment-by-using-the-ews-managed-api"></a>Crear una cita mediante la API administrada de EWS
<a name="bk_CreateApptEWSMA"> </a>

En el siguiente ejemplo de código se muestra cómo usar el [objeto appointment](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) para crear una cita, el método [Save](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.save%28v=exchg.80%29.aspx) para guardarlo en la carpeta del calendario y el método [Item. bind](https://msdn.microsoft.com/library/dd634410%28v=exchg.80%29.aspx) para comprobar que la cita se ha creado. 
  
En este ejemplo se supone que se ha autenticado en un servidor de Exchange y que se ha adquirido un objeto [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) denominado **Service**. 
  
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

Después de establecer las propiedades del objeto appointment, guarde la cita en la carpeta calendario mediante el método [Save](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.save%28v=exchg.80%29.aspx) del objeto appointment. 
  
Tenga en cuenta que en el paso de comprobación, use el [identificador](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) de elemento asociado a la cita para comprobar que la cita se encuentra en la carpeta calendario. Como práctica recomendada, limite las propiedades devueltas por el servidor solo a lo que necesita, en este caso, el asunto de la cita. 
  
## <a name="create-an-appointment-by-using-ews"></a>Crear una cita mediante EWS
<a name="bk_CreateApptEWS"> </a>

El XML de solicitud y respuesta de los ejemplos siguientes corresponden a las llamadas realizadas por el código de la API administrada de EWS en [crear una cita mediante la API administrada de EWS](#bk_CreateApptEWSMA). El XML de solicitud y respuesta que comprueba que los elementos de cita están en la carpeta calendario también se muestran.
  
En el ejemplo siguiente se muestra el XML de la solicitud cuando se utiliza la operación [CreateItem](https://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) para crear una cita. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
       xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
       xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
       xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
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

 En el ejemplo siguiente se muestra el XML de respuesta que devuelve la operación **CreateItem** . 
  
> [!NOTE]
> Los atributos **Itemid** y **changekey** se han abreviado para facilitar su lectura. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="775" MinorBuildNumber="7" Version="V2_4" 
 xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
 xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
 xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
 xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:CreateItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
  xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
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

En el ejemplo siguiente se muestra el XML de la solicitud que se genera al usar la operación [GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) para comprobar que la cita se ha creado. 
  
> [!NOTE]
> Los atributos **Itemid** y **changekey** se han abreviado para facilitar su lectura. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
       xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
       xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
       xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
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

 En el ejemplo siguiente se muestra el XML de respuesta que devuelve la operación **GetItem** . 
  
> [!NOTE]
> Los atributos **Itemid** y **changekey** se han abreviado para facilitar su lectura. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="775" MinorBuildNumber="7" Version="V2_4" 
 xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
 xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
 xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
 xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
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

## <a name="create-a-meeting-by-using-the-ews-managed-api"></a>Crear una reunión mediante la API administrada de EWS
<a name="bk_CreateMtgEWSMA"> </a>

Al crear una reunión, además de guardar un elemento en la carpeta calendario, también suele ser conveniente enviar las convocatorias de reunión a los asistentes. En el ejemplo de código siguiente se muestra cómo crear una reunión y enviar convocatorias de reunión.
  
En este ejemplo se supone que se ha autenticado en un servidor de Exchange y que se ha adquirido un objeto [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) denominado **Service**. 
  
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

Después de establecer las propiedades del objeto [appointment](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) , guarde la reunión en la carpeta calendario mediante el método [Save](https://msdn.microsoft.com/library/dd635394%28v=exchg.80%29.aspx) . Cuando se establece el valor de enumeración [SendInvitationsMode](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.sendinvitationsmode%28v=exchg.80%29.aspx) en **SendOnlyToAll** o **SendToAllAndSaveCopy**, se envían invitaciones a los asistentes.
  
Use el [identificador](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) de elemento asociado a la reunión para comprobar que se ha guardado en la carpeta calendario. Como práctica recomendada, limite las propiedades devueltas por el servidor solo a lo que necesita, en este caso, el asunto de la reunión. 
  
## <a name="create-a-meeting-by-using-ews"></a>Crear una reunión con EWS
<a name="bk_CreateMtgEWS"> </a>

El XML de solicitud y respuesta de los ejemplos siguientes corresponden a las llamadas realizadas por el código de la API administrada de EWS en [crear una reunión mediante la API administrada de EWS](#bk_CreateMtgEWSMA). El XML de solicitud y respuesta que comprueba que los elementos de la reunión están en la carpeta calendario también se muestran.
  
En el ejemplo siguiente se muestra el XML de la solicitud cuando se utiliza la operación [CreateItem](https://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) para crear una reunión. 
  
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

En el ejemplo siguiente se muestra el XML de respuesta que devuelve la operación **CreateItem** . 
  
> [!NOTE]
> Los atributos **Itemid** y **changekey** se han abreviado para facilitar su lectura. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="775" MinorBuildNumber="7" Version="V2_4" 
 xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
 xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
 xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:CreateItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
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

En el ejemplo siguiente se muestra el XML de la solicitud que genera la operación [GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) al comprobar que la reunión se ha creado. 
  
> [!NOTE]
> Los atributos **Itemid** y **changekey** se han abreviado para facilitar su lectura. 
  
```xml
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

En el ejemplo siguiente se muestra el XML de respuesta que devuelve la operación **GetItem** . 
  
> [!NOTE]
> Los atributos **Itemid** y **changekey** se han abreviado para facilitar su lectura. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="775" MinorBuildNumber="7" Version="V2_4" 
 xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
 xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
 xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
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

## <a name="see-also"></a>Vea también

- [Calendarios y EWS en Exchange](calendars-and-ews-in-exchange.md)  
- [Obtener citas y reuniones mediante EWS en Exchange](how-to-get-appointments-and-meetings-by-using-ews-in-exchange.md)  
- [Actualizar citas y reuniones mediante EWS en Exchange](how-to-update-appointments-and-meetings-by-using-ews-in-exchange.md) 
- [Eliminar citas y cancelar reuniones mediante EWS en Exchange](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md) 
- [Proponer una nueva hora de reunión mediante EWS en Exchange](how-to-propose-a-new-meeting-time-by-using-ews-in-exchange.md)
    

