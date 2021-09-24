---
title: Actualice la zona horaria de una cita mediante EWS en Exchange
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: dc2240c1-5500-4d5c-97d5-09d63ffd30d5
description: Obtenga información sobre cómo actualizar la zona horaria de una cita o reunión existente mediante la API administrada ews o EWS en Exchange.
ms.openlocfilehash: 525feb1c7e37914ef4105312e89af8f1a8cf856b
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59521088"
---
# <a name="update-the-time-zone-for-an-appointment-by-using-ews-in-exchange"></a>Actualice la zona horaria de una cita mediante EWS en Exchange

Obtenga información sobre cómo actualizar la zona horaria de una cita o reunión existente mediante la API administrada ews o EWS en Exchange.
  
Cuando se crea una cita o reunión en un calendario Exchange, la zona horaria usada para especificar las horas de inicio y finalización se guarda como zona horaria de creación para la cita. Puede cambiar esa zona horaria mediante la API administrada ews o EWS. Sin embargo, cambiar la zona horaria de una cita tiene otros efectos en la hora de inicio y finalización de la cita.
  
Los valores de hora se almacenan en el servidor Exchange en la hora universal de coordenadas (UTC). Por lo tanto, si una cita está configurada para iniciarse a las 13:00 (13:00) en la zona horaria oriental (UTC-05:00), ese valor se almacena como 6:00 p.m. (18:00) en el servidor, suponiendo que la zona horaria se encuentra en su fase horaria estándar. Cuando esa cita se ve en otras zonas horarias, se agrega o resta el número adecuado de horas del valor UTC para determinar la hora específica de la zona horaria. Por ejemplo, si una cita tiene una hora de inicio a la 1:00 p.m. del este (6:00 PM UTC) y se ve desde un cliente en la zona horaria del Pacífico (UTC-08:00), la hora de inicio específica de la zona horaria para ese cliente sería de 10:00 a.m. (18:00 - 08:00).
  
Al actualizar la zona horaria de la cita sin actualizar la hora de inicio y finalización, el servidor actualiza los valores UTC almacenados en el servidor para mantener la hora de inicio y finalización como las mismas horas específicas de la zona horaria. Por ejemplo, considere la cita oriental de las 1:00 p.m. La hora se almacena como 18:00 UTC en el servidor. Si la zona horaria de la cita se cambia a la zona horaria del Pacífico, el servidor cambia la hora de inicio a 1:00 PM Pacífico (21:00 UTC).
  
Puede cambiar este comportamiento estableciendo explícitamente las horas de inicio y finalización.
  
## <a name="updating-the-time-zone-on-an-existing-appointment-by-using-the-ews-managed-api"></a>Actualizar la zona horaria en una cita existente mediante la API administrada de EWS

En el siguiente ejemplo, la API administrada ews se usa para actualizar la zona horaria de una cita existente a la zona horaria central actualizando las propiedades **Appointment.StartTimeZone** y **Appointment.EndTimeZone.** Si el  _parámetro shiftAppointnment_ se establece en **true,** el código no establece explícitamente las horas de inicio y finalización de la cita. En este caso, el servidor desplazará las horas de inicio y finalización para mantenerlas a la misma hora relativa a la zona horaria en la nueva zona horaria. Si se establece en **false,** el código convierte explícitamente las horas de inicio y finalización para mantener la cita al mismo tiempo en UTC. 

En este ejemplo se asume que el objeto **ExchangeService** se ha inicializado con valores válidos en las propiedades [Credentials](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.credentials%28v=exchg.80%29.aspx) y [Url](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.url%28v=exchg.80%29.aspx). 
  
```cs
static void UpdateAppointmentTimeZone(ExchangeService service, ItemId apptId, bool shiftAppointment)
{
    PropertySet includeTimeZones = new PropertySet(AppointmentSchema.Subject,
                                                   AppointmentSchema.Start,
                                                   AppointmentSchema.ReminderDueBy,
                                                   AppointmentSchema.End,
                                                   AppointmentSchema.StartTimeZone,
                                                   AppointmentSchema.EndTimeZone);
    Appointment apptToUpdate;
    // Load the existing appointment.
    // This will result in a call to EWS.
    try
    {
        apptToUpdate = Appointment.Bind(service, apptId, includeTimeZones);
    }
    catch (Exception ex)
    {
        Console.WriteLine("Error retrieving existing appointment: {0}", ex.Message);
        return;
    }
    Console.WriteLine("Before update:");
    // Output the current start, reminder, end, and time zones.
    Console.WriteLine("  Start: {0}", apptToUpdate.Start);
    Console.WriteLine("  Start time zone: {0}", apptToUpdate.StartTimeZone.DisplayName);
    Console.WriteLine("  Reminder: {0}", apptToUpdate.ReminderDueBy);
    Console.WriteLine("  End: {0}", apptToUpdate.End);
    Console.WriteLine("  End time zone: {0}", apptToUpdate.EndTimeZone.DisplayName);
    // Retrieve the Central time zone.
    TimeZoneInfo centralTZ = TimeZoneInfo.FindSystemTimeZoneById("Central Standard Time");
    // Update the time zones on the appointment.
    apptToUpdate.StartTimeZone = centralTZ;
    apptToUpdate.EndTimeZone = centralTZ;
    if (!shiftAppointment)
    {
        // Set the start and end times explicitly so that the appointment
        // will start and end at the same UTC time.
        // Convert the times to then Central time zone. This
        // will keep them at the same time in UTC.
        // For example, 1:00 PM Eastern becomes 12:00 PM Central.
        DateTime newStartTime = TimeZoneInfo.ConvertTime(
            apptToUpdate.Start, centralTZ);
        DateTime newEndTime = TimeZoneInfo.ConvertTime(
            apptToUpdate.End, centralTZ);
        apptToUpdate.Start = newStartTime;
        apptToUpdate.End = newEndTime;
    }
    try
    {
        // Save the changes. This will result in a call to EWS.
        apptToUpdate.Update(ConflictResolutionMode.AlwaysOverwrite, 
            SendInvitationsOrCancellationsMode.SendToNone);
    }
    catch (Exception ex)
    {
        Console.WriteLine("Error updating appointment: {0}", ex.Message);
        return;
    }
    // Now rebind to the appointment to get the new values.
    Appointment apptAfterUpdate;
    
    try
    {
        // This will result in a call to EWS.
        apptAfterUpdate = Appointment.Bind(service, apptId, includeTimeZones);
    }
    catch (Exception ex)
    {
        Console.WriteLine("Error retrieving existing appointment: {0}", ex.Message);
        return;
    }
    Console.WriteLine("After update:");
    // Output the current start, reminder, end, and time zones.
    Console.WriteLine("  Start: {0}", apptAfterUpdate.Start);
    Console.WriteLine("  Start time zone: {0}", apptAfterUpdate.StartTimeZone.DisplayName);
    Console.WriteLine("  Reminder: {0}", apptAfterUpdate.ReminderDueBy);
    Console.WriteLine("  End: {0}", apptAfterUpdate.End);
    Console.WriteLine("  End time zone: {0}", apptAfterUpdate.EndTimeZone.DisplayName);
}
```

Cuando se usa el ejemplo para actualizar una cita que comienza a la 1:00 p. m. del este y termina a las 2:00 p. m. del este, con el parámetro  _shiftAppointment_ establecido en true y la propiedad [ExchangeService.TimeZone](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.timezone%28v=exchg.80%29.aspx) establecida en la zona horaria oriental, el resultado es similar al siguiente. 
  
```MS-DOS
Before update:
  Start: 6/20/2014 1:00:00 PM
  Start time zone: (UTC-05:00) Eastern Time (US &amp; Canada)
  Reminder: 6/20/2014 1:00:00 PM
  End: 6/20/2014 2:00:00 PM
  End time zone: (UTC-05:00) Eastern Time (US &amp; Canada)
After update:
  Start: 6/20/2014 2:00:00 PM
  Start time zone: (UTC-06:00) Central Time (US &amp; Canada)
  Reminder: 6/20/2014 2:00:00 PM
  End: 6/20/2014 3:00:00 PM
  End time zone: (UTC-06:00) Central Time (US &amp; Canada)
```

Cuando se usa el ejemplo para actualizar la misma cita con el parámetro  _shiftAppointment_ establecido en false y con la propiedad **TimeZone** nuevamente establecida en la zona horaria oriental, el resultado tiene un aspecto un poco diferente. 
  
```MS-DOS
Before update:
  Start: 6/20/2014 1:00:00 PM
  Start time zone: (UTC-05:00) Eastern Time (US &amp; Canada)
  Reminder: 6/20/2014 1:00:00 PM
  End: 6/20/2014 2:00:00 PM
  End time zone: (UTC-05:00) Eastern Time (US &amp; Canada)
After update:
  Start: 6/20/2014 1:00:00 PM
  Start time zone: (UTC-06:00) Central Time (US &amp; Canada)
  Reminder: 6/20/2014 1:00:00 PM
  End: 6/20/2014 2:00:00 PM
  End time zone: (UTC-06:00) Central Time (US &amp; Canada)
```

Observe que las horas de inicio y finalización no cambiaron. Esto se debe a que los tiempos se interpretan en la zona horaria oriental (porque la propiedad **TimeZone** está establecida en la zona horaria oriental) y los valores de hora se actualizaron para evitar que la cita cambie. 
  
## <a name="updating-the-time-zone-on-an-existing-appointment-by-using-ews"></a>Actualizar la zona horaria en una cita existente mediante EWS

En el siguiente ejemplo, la [solicitud de operación UpdateItem](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) de EWS actualiza la zona horaria en una cita. En este ejemplo solo se actualiza los elementos [StartTimeZone](https://msdn.microsoft.com/library/d38c4dc1-4ecb-42a1-8d57-a451b16a2de2%28Office.15%29.aspx) y [EndTimeZone,](https://msdn.microsoft.com/library/6c53c337-be60-4d22-9e9e-a0c140c5e913%28Office.15%29.aspx) por lo que el servidor desplazará las horas de inicio y finalización de la cita para mantenerla a la misma hora relativa a la zona horaria en la nueva zona horaria. El valor del **elemento ItemId** se acorta para que sea legible. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
    xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
    xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
    xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2010" />
  </soap:Header>
  <soap:Body>
    <m:UpdateItem ConflictResolution="AlwaysOverwrite" SendMeetingInvitationsOrCancellations="SendToNone">
      <m:ItemChanges>
        <t:ItemChange>
          <t:ItemId Id="AAMkADA5..." ChangeKey="DwAAABYA..." />
          <t:Updates>
            <t:SetItemField>
              <t:FieldURI FieldURI="calendar:StartTimeZone" />
              <t:CalendarItem>
                <t:StartTimeZone Id="Central Standard Time" />
              </t:CalendarItem>
            </t:SetItemField>
            <t:SetItemField>
              <t:FieldURI FieldURI="calendar:EndTimeZone" />
              <t:CalendarItem>
                <t:EndTimeZone Id="Central Standard Time" />
              </t:CalendarItem>
            </t:SetItemField>
          </t:Updates>
        </t:ItemChange>
      </m:ItemChanges>
    </m:UpdateItem>
  </soap:Body>
</soap:Envelope>
```

En el siguiente ejemplo, la solicitud actualiza la zona horaria de la cita y también actualiza las horas de inicio y finalización estableciendo explícitamente los **elementos Start** y **End.** El valor del **elemento ItemId** se acorta para que sea legible. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
    xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
    xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
    xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2010" />
  </soap:Header>
  <soap:Body>
    <m:UpdateItem ConflictResolution="AlwaysOverwrite" SendMeetingInvitationsOrCancellations="SendToNone">
      <m:ItemChanges>
        <t:ItemChange>
          <t:ItemId Id="AAMkADA5..." ChangeKey="DwAAABYA..." />
          <t:Updates>
            <t:SetItemField>
              <t:FieldURI FieldURI="calendar:StartTimeZone" />
              <t:CalendarItem>
                <t:StartTimeZone Id="Central Standard Time" />
              </t:CalendarItem>
            </t:SetItemField>
            <t:SetItemField>
              <t:FieldURI FieldURI="calendar:EndTimeZone" />
              <t:CalendarItem>
                <t:EndTimeZone Id="Central Standard Time" />
              </t:CalendarItem>
            </t:SetItemField>
            <t:SetItemField>
              <t:FieldURI FieldURI="calendar:Start" />
              <t:CalendarItem>
                <t:Start>2014-06-20T17:00:00.000Z</t:Start>
              </t:CalendarItem>
            </t:SetItemField>
            <t:SetItemField>
              <t:FieldURI FieldURI="calendar:End" />
              <t:CalendarItem>
                <t:End>2014-06-20T18:00:00.000Z</t:End>
              </t:CalendarItem>
            </t:SetItemField>
          </t:Updates>
        </t:ItemChange>
      </m:ItemChanges>
    </m:UpdateItem>
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a>Ver también

- [Zonas horarias y EWS en Exchange](time-zones-and-ews-in-exchange.md)   
- [Crear citas en una zona horaria específica mediante EWS en Exchange](how-to-create-appointments-in-a-specific-time-zone-by-using-ews-in-exchange.md)   
- [Actualice las citas y reuniones mediante EWS en Exchange](how-to-update-appointments-and-meetings-by-using-ews-in-exchange.md)
    

