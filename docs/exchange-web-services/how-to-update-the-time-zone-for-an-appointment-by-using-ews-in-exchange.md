---
title: Actualización de la zona horaria para una cita mediante EWS en Exchange
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: dc2240c1-5500-4d5c-97d5-09d63ffd30d5
description: Obtenga información sobre cómo actualizar la zona horaria para una cita o una reunión existente mediante la API administrada de EWS o EWS en Exchange.
ms.openlocfilehash: 535eb9f546d9a4353408579f3a24750f32237699
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763184"
---
# <a name="update-the-time-zone-for-an-appointment-by-using-ews-in-exchange"></a>Actualización de la zona horaria para una cita mediante EWS en Exchange

Obtenga información sobre cómo actualizar la zona horaria para una cita o una reunión existente mediante la API administrada de EWS o EWS en Exchange.
  
Cuando se crea una cita o reunión en un calendario de Exchange, la zona horaria que se usa para especificar las horas de inicio y final se guarda como la zona horaria de creación para la cita. Puede cambiar esa zona horaria mediante el uso de la API administrada de EWS o EWS. Sin embargo, cambiar la zona horaria en una cita tiene otros efectos en la hora de inicio y finalización de la cita.
  
Los valores de tiempo se almacenan en el servidor de Exchange en hora Universal coordinado (UTC). Por tanto, si se establece una cita para iniciar a la 1:00 P.M. (13:00) en la zona hora oriental (UTC-05:00), que el valor se almacena como 6:00 P.M. (18:00) en el servidor, suponiendo que la zona horaria está en fase de tiempo estándar. Cuando esa cita se ve en otras zonas horarias, el número adecuado de horas se agrega o resta del valor UTC para determinar el tiempo de zona horaria específica. Por ejemplo, si una cita tiene una hora de inicio a la 1:00 P.M. oriental (UTC 6:00 P.M.) y se ve desde un cliente en la zona hora del Pacífico (UTC-08:00), hora de inicio de la zona horaria específica para que el cliente sería 10:00 A.M. (18:00-08:00).
  
Al actualizar la zona horaria de la cita sin actualizar el tiempo de inicio y finalización, el servidor actualiza los valores de UTC almacenados en el servidor para mantener la hora de inicio y finalización del mismo veces específicos de la zona horaria. Por ejemplo, considere la posibilidad de la cita oriental 1:00 PM. La hora se almacenará como 18:00 UTC en el servidor. Si se cambia la zona horaria de la cita a la zona horaria del Pacífico, el servidor desplaza a la hora de inicio a la 1:00 P.M. Pacífico (21:00 UTC).
  
Puede cambiar este comportamiento estableciendo explícitamente las horas de inicio y finalización.
  
## <a name="updating-the-time-zone-on-an-existing-appointment-by-using-the-ews-managed-api"></a>Actualización de la zona horaria en una cita existente mediante el uso de la API administrada de EWS

En el siguiente ejemplo, se usa la API administrada de EWS para actualizar la zona horaria en una cita existente a la zona horaria Central mediante la actualización de las propiedades de **Appointment.EndTimeZone** y **Appointment.StartTimeZone** . Si el parámetro _shiftAppointnment_ se establece en **true**, el código no establecer explícitamente las horas de inicio y finalización de la cita. En este caso, el servidor se produce el desplazamiento de las horas de inicio y finalización para mantenerlos en el mismo momento relativa a la zona horaria en la nueva zona horaria. Si se establece en **false**, el código convierte los tiempos de inicio y finalización explícitamente para mantener la cita al mismo tiempo en UTC. 

En este ejemplo se da por supuesto que se ha inicializado el objeto **ExchangeService** con valores válidos en las propiedades de [las credenciales](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservicebase.credentials%28v=exchg.80%29.aspx) y [dirección Url](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.url%28v=exchg.80%29.aspx) . 
  
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

Cuando el ejemplo se utiliza para actualizar una cita que se inicia a la 1:00 P.M. oriental y finaliza a las 2:00 P.M. oriental, con el parámetro _shiftAppointment_ establecido en true y la propiedad [ExchangeService.TimeZone](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.timezone%28v=exchg.80%29.aspx) establecida en la zona hora oriental, el resultado tiene el aspecto como el siguiente. 
  
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

Cuando el ejemplo se utiliza para actualizar la misma cita con el parámetro _shiftAppointment_ establecido en false y con la propiedad **TimeZone** vuelva a establecer para la zona horaria oriental, el resultado tiene un aspecto un poco diferente. 
  
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

Tenga en cuenta que los tiempos de inicio y finalización no ha cambiado. Esto es debido a que el tiempo que se interpretará en la hora oriental de zona (debido a que la propiedad de **zona horaria** se establece en la zona hora oriental), y se han actualizado los valores de tiempo para evitar que la cita de un cambio. 
  
## <a name="updating-the-time-zone-on-an-existing-appointment-by-using-ews"></a>Actualización de la zona horaria en una cita existente mediante el uso de EWS

El siguiente ejemplo de solicitud de EWS [UpdateItem operación](http://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) actualiza la zona horaria en una cita. En este ejemplo se actualizan sólo los elementos [StartTimeZone](http://msdn.microsoft.com/library/d38c4dc1-4ecb-42a1-8d57-a451b16a2de2%28Office.15%29.aspx) y [EndTimeZone](http://msdn.microsoft.com/library/6c53c337-be60-4d22-9e9e-a0c140c5e913%28Office.15%29.aspx) , por lo que el servidor cambiará las horas de inicio y finalización de la cita para mantener al mismo tiempo relativa a la zona del tiempo en la nueva zona horaria. El valor del elemento **ItemId** se acorta para mejorar la legibilidad. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
    xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
    xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
    xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
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

El siguiente ejemplo de solicitud actualiza la zona horaria de la cita y también actualiza las horas de inicio y finalización estableciendo explícitamente los elementos de **Inicio** y **fin** . El valor del elemento **ItemId** se acorta para mejorar la legibilidad. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
    xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
    xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
    xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
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
- [Crear citas en una zona horaria concreta mediante el uso de EWS en Exchange](how-to-create-appointments-in-a-specific-time-zone-by-using-ews-in-exchange.md)   
- [Actualizar las citas y reuniones con EWS en Exchange](how-to-update-appointments-and-meetings-by-using-ews-in-exchange.md)
    

