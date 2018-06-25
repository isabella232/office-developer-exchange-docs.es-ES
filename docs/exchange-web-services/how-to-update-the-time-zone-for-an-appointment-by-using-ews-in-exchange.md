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
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763184"
---
# <a name="update-the-time-zone-for-an-appointment-by-using-ews-in-exchange"></a><span data-ttu-id="1e43c-103">Actualización de la zona horaria para una cita mediante EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="1e43c-103">Update the time zone for an appointment by using EWS in Exchange</span></span>

<span data-ttu-id="1e43c-104">Obtenga información sobre cómo actualizar la zona horaria para una cita o una reunión existente mediante la API administrada de EWS o EWS en Exchange.</span><span class="sxs-lookup"><span data-stu-id="1e43c-104">Learn how to update the time zone for an existing appointment or meeting by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="1e43c-105">Cuando se crea una cita o reunión en un calendario de Exchange, la zona horaria que se usa para especificar las horas de inicio y final se guarda como la zona horaria de creación para la cita.</span><span class="sxs-lookup"><span data-stu-id="1e43c-105">When an appointment or meeting is created on an Exchange calendar, the time zone used to specify the start and end times is saved as the creation time zone for the appointment.</span></span> <span data-ttu-id="1e43c-106">Puede cambiar esa zona horaria mediante el uso de la API administrada de EWS o EWS.</span><span class="sxs-lookup"><span data-stu-id="1e43c-106">You can change that time zone by using the EWS Managed API or EWS.</span></span> <span data-ttu-id="1e43c-107">Sin embargo, cambiar la zona horaria en una cita tiene otros efectos en la hora de inicio y finalización de la cita.</span><span class="sxs-lookup"><span data-stu-id="1e43c-107">However, changing the time zone on an appointment has other effects on the start and end time of the appointment.</span></span>
  
<span data-ttu-id="1e43c-108">Los valores de tiempo se almacenan en el servidor de Exchange en hora Universal coordinado (UTC).</span><span class="sxs-lookup"><span data-stu-id="1e43c-108">Time values are stored on the Exchange server in Coordinate Universal Time (UTC).</span></span> <span data-ttu-id="1e43c-109">Por tanto, si se establece una cita para iniciar a la 1:00 P.M. (13:00) en la zona hora oriental (UTC-05:00), que el valor se almacena como 6:00 P.M. (18:00) en el servidor, suponiendo que la zona horaria está en fase de tiempo estándar.</span><span class="sxs-lookup"><span data-stu-id="1e43c-109">So if an appointment is set to start at 1:00 PM (13:00) in the Eastern time zone (UTC-05:00), that value is stored as 6:00 PM (18:00) on the server, assuming that the time zone is in its standard time phase.</span></span> <span data-ttu-id="1e43c-110">Cuando esa cita se ve en otras zonas horarias, el número adecuado de horas se agrega o resta del valor UTC para determinar el tiempo de zona horaria específica.</span><span class="sxs-lookup"><span data-stu-id="1e43c-110">When that appointment is viewed in other time zones, the appropriate number of hours is added or subtracted from the UTC value to determine the time zone-specific time.</span></span> <span data-ttu-id="1e43c-111">Por ejemplo, si una cita tiene una hora de inicio a la 1:00 P.M. oriental (UTC 6:00 P.M.) y se ve desde un cliente en la zona hora del Pacífico (UTC-08:00), hora de inicio de la zona horaria específica para que el cliente sería 10:00 A.M. (18:00-08:00).</span><span class="sxs-lookup"><span data-stu-id="1e43c-111">For example, if an appointment has a start time at 1:00 PM Eastern (6:00 PM UTC), and is viewed from a client in the Pacific time zone (UTC-08:00), the time-zone specific start time for that client would be 10:00 AM (18:00 - 08:00).</span></span>
  
<span data-ttu-id="1e43c-112">Al actualizar la zona horaria de la cita sin actualizar el tiempo de inicio y finalización, el servidor actualiza los valores de UTC almacenados en el servidor para mantener la hora de inicio y finalización del mismo veces específicos de la zona horaria.</span><span class="sxs-lookup"><span data-stu-id="1e43c-112">When you update the time zone of the appointment without updating the start and end time, the server updates the UTC values stored on the server to keep the start and end time as the same time zone-specific times.</span></span> <span data-ttu-id="1e43c-113">Por ejemplo, considere la posibilidad de la cita oriental 1:00 PM.</span><span class="sxs-lookup"><span data-stu-id="1e43c-113">For example, consider the 1:00 PM Eastern appointment.</span></span> <span data-ttu-id="1e43c-114">La hora se almacenará como 18:00 UTC en el servidor.</span><span class="sxs-lookup"><span data-stu-id="1e43c-114">The time is stored as 18:00 UTC on the server.</span></span> <span data-ttu-id="1e43c-115">Si se cambia la zona horaria de la cita a la zona horaria del Pacífico, el servidor desplaza a la hora de inicio a la 1:00 P.M. Pacífico (21:00 UTC).</span><span class="sxs-lookup"><span data-stu-id="1e43c-115">If the time zone of the appointment is changed to the Pacific time zone, the server shifts the start time to 1:00 PM Pacific (21:00 UTC).</span></span>
  
<span data-ttu-id="1e43c-116">Puede cambiar este comportamiento estableciendo explícitamente las horas de inicio y finalización.</span><span class="sxs-lookup"><span data-stu-id="1e43c-116">You can change this behavior by explicitly setting the start and end times.</span></span>
  
## <a name="updating-the-time-zone-on-an-existing-appointment-by-using-the-ews-managed-api"></a><span data-ttu-id="1e43c-117">Actualización de la zona horaria en una cita existente mediante el uso de la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="1e43c-117">Updating the time zone on an existing appointment by using the EWS Managed API</span></span>

<span data-ttu-id="1e43c-118">En el siguiente ejemplo, se usa la API administrada de EWS para actualizar la zona horaria en una cita existente a la zona horaria Central mediante la actualización de las propiedades de **Appointment.EndTimeZone** y **Appointment.StartTimeZone** .</span><span class="sxs-lookup"><span data-stu-id="1e43c-118">In the following example, the EWS Managed API is used to update the time zone on an existing appointment to the Central time zone by updating the **Appointment.StartTimeZone** and **Appointment.EndTimeZone** properties.</span></span> <span data-ttu-id="1e43c-119">Si el parámetro _shiftAppointnment_ se establece en **true**, el código no establecer explícitamente las horas de inicio y finalización de la cita.</span><span class="sxs-lookup"><span data-stu-id="1e43c-119">If the  _shiftAppointnment_ parameter is set to **true**, the code does not explicitly set the start and end times on the appointment.</span></span> <span data-ttu-id="1e43c-120">En este caso, el servidor se produce el desplazamiento de las horas de inicio y finalización para mantenerlos en el mismo momento relativa a la zona horaria en la nueva zona horaria.</span><span class="sxs-lookup"><span data-stu-id="1e43c-120">In this case, the server will shift the start and end times to keep them at the same time zone-relative times in the new time zone.</span></span> <span data-ttu-id="1e43c-121">Si se establece en **false**, el código convierte los tiempos de inicio y finalización explícitamente para mantener la cita al mismo tiempo en UTC.</span><span class="sxs-lookup"><span data-stu-id="1e43c-121">If set to **false**, the code converts the start and end times explicitly to keep the appointment at the same time in UTC.</span></span> 

<span data-ttu-id="1e43c-122">En este ejemplo se da por supuesto que se ha inicializado el objeto **ExchangeService** con valores válidos en las propiedades de [las credenciales](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservicebase.credentials%28v=exchg.80%29.aspx) y [dirección Url](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.url%28v=exchg.80%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="1e43c-122">This example assumes that the **ExchangeService** object has been initialized with valid values in the [Credentials](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservicebase.credentials%28v=exchg.80%29.aspx) and [Url](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.url%28v=exchg.80%29.aspx) properties.</span></span> 
  
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

<span data-ttu-id="1e43c-123">Cuando el ejemplo se utiliza para actualizar una cita que se inicia a la 1:00 P.M. oriental y finaliza a las 2:00 P.M. oriental, con el parámetro _shiftAppointment_ establecido en true y la propiedad [ExchangeService.TimeZone](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.timezone%28v=exchg.80%29.aspx) establecida en la zona hora oriental, el resultado tiene el aspecto como el siguiente.</span><span class="sxs-lookup"><span data-stu-id="1e43c-123">When the example is used to update an appointment that starts at 1:00 PM Eastern and ends at 2:00 PM Eastern, with the  _shiftAppointment_ parameter set to true, and the [ExchangeService.TimeZone](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.timezone%28v=exchg.80%29.aspx) property set to the Eastern time zone, the output looks like the following.</span></span> 
  
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

<span data-ttu-id="1e43c-124">Cuando el ejemplo se utiliza para actualizar la misma cita con el parámetro _shiftAppointment_ establecido en false y con la propiedad **TimeZone** vuelva a establecer para la zona horaria oriental, el resultado tiene un aspecto un poco diferente.</span><span class="sxs-lookup"><span data-stu-id="1e43c-124">When the example is used to update the same appointment with the  _shiftAppointment_ parameter set to false, and with the **TimeZone** property again set to the Eastern time zone, the output looks a little different.</span></span> 
  
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

<span data-ttu-id="1e43c-125">Tenga en cuenta que los tiempos de inicio y finalización no ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="1e43c-125">Notice that the start and end times did not change.</span></span> <span data-ttu-id="1e43c-126">Esto es debido a que el tiempo que se interpretará en la hora oriental de zona (debido a que la propiedad de **zona horaria** se establece en la zona hora oriental), y se han actualizado los valores de tiempo para evitar que la cita de un cambio.</span><span class="sxs-lookup"><span data-stu-id="1e43c-126">This is because the times are being interpreted in the Eastern time zone (because the **TimeZone** property is set to the Eastern time zone), and the time values were updated to prevent the appointment from shifting.</span></span> 
  
## <a name="updating-the-time-zone-on-an-existing-appointment-by-using-ews"></a><span data-ttu-id="1e43c-127">Actualización de la zona horaria en una cita existente mediante el uso de EWS</span><span class="sxs-lookup"><span data-stu-id="1e43c-127">Updating the time zone on an existing appointment by using EWS</span></span>

<span data-ttu-id="1e43c-128">El siguiente ejemplo de solicitud de EWS [UpdateItem operación](http://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) actualiza la zona horaria en una cita.</span><span class="sxs-lookup"><span data-stu-id="1e43c-128">The following example EWS [UpdateItem operation](http://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) request updates the time zone on an appointment.</span></span> <span data-ttu-id="1e43c-129">En este ejemplo se actualizan sólo los elementos [StartTimeZone](http://msdn.microsoft.com/library/d38c4dc1-4ecb-42a1-8d57-a451b16a2de2%28Office.15%29.aspx) y [EndTimeZone](http://msdn.microsoft.com/library/6c53c337-be60-4d22-9e9e-a0c140c5e913%28Office.15%29.aspx) , por lo que el servidor cambiará las horas de inicio y finalización de la cita para mantener al mismo tiempo relativa a la zona del tiempo en la nueva zona horaria.</span><span class="sxs-lookup"><span data-stu-id="1e43c-129">This example only updates the [StartTimeZone](http://msdn.microsoft.com/library/d38c4dc1-4ecb-42a1-8d57-a451b16a2de2%28Office.15%29.aspx) and [EndTimeZone](http://msdn.microsoft.com/library/6c53c337-be60-4d22-9e9e-a0c140c5e913%28Office.15%29.aspx) elements, so the server will shift the start and end times of the appointment to keep it at the same time-zone-relative time in the new time zone.</span></span> <span data-ttu-id="1e43c-130">El valor del elemento **ItemId** se acorta para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="1e43c-130">The value of the **ItemId** element is shortened for readability.</span></span> 
  
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

<span data-ttu-id="1e43c-131">El siguiente ejemplo de solicitud actualiza la zona horaria de la cita y también actualiza las horas de inicio y finalización estableciendo explícitamente los elementos de **Inicio** y **fin** .</span><span class="sxs-lookup"><span data-stu-id="1e43c-131">The following example request updates the time zone of the appointment, and also updates the start and end times by explicitly setting the **Start** and **End** elements.</span></span> <span data-ttu-id="1e43c-132">El valor del elemento **ItemId** se acorta para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="1e43c-132">The value of the **ItemId** element is shortened for readability.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="1e43c-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="1e43c-133">See also</span></span>

- [<span data-ttu-id="1e43c-134">Zonas horarias y EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="1e43c-134">Time zones and EWS in Exchange</span></span>](time-zones-and-ews-in-exchange.md)   
- [<span data-ttu-id="1e43c-135">Crear citas en una zona horaria concreta mediante el uso de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="1e43c-135">Create appointments in a specific time zone by using EWS in Exchange</span></span>](how-to-create-appointments-in-a-specific-time-zone-by-using-ews-in-exchange.md)   
- [<span data-ttu-id="1e43c-136">Actualizar las citas y reuniones con EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="1e43c-136">Update appointments and meetings by using EWS in Exchange</span></span>](how-to-update-appointments-and-meetings-by-using-ews-in-exchange.md)
    

