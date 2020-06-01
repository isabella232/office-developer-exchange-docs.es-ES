---
title: Actualizar la zona horaria de una cita mediante EWS en Exchange
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: dc2240c1-5500-4d5c-97d5-09d63ffd30d5
description: Obtenga información sobre cómo actualizar la zona horaria para una cita o reunión existente mediante el uso de la API administrada de EWS o EWS en Exchange.
ms.openlocfilehash: 064f99997b7c3d1197cb8d1ee6a24f8fb874f706
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44455845"
---
# <a name="update-the-time-zone-for-an-appointment-by-using-ews-in-exchange"></a><span data-ttu-id="46c7d-103">Actualizar la zona horaria de una cita mediante EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="46c7d-103">Update the time zone for an appointment by using EWS in Exchange</span></span>

<span data-ttu-id="46c7d-104">Obtenga información sobre cómo actualizar la zona horaria para una cita o reunión existente mediante el uso de la API administrada de EWS o EWS en Exchange.</span><span class="sxs-lookup"><span data-stu-id="46c7d-104">Learn how to update the time zone for an existing appointment or meeting by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="46c7d-105">Cuando se crea una cita o una reunión en un calendario de Exchange, la zona horaria utilizada para especificar las horas de inicio y finalización se guarda como zona horaria de creación para la cita.</span><span class="sxs-lookup"><span data-stu-id="46c7d-105">When an appointment or meeting is created on an Exchange calendar, the time zone used to specify the start and end times is saved as the creation time zone for the appointment.</span></span> <span data-ttu-id="46c7d-106">Puede cambiar esa zona horaria mediante la API administrada de EWS o EWS.</span><span class="sxs-lookup"><span data-stu-id="46c7d-106">You can change that time zone by using the EWS Managed API or EWS.</span></span> <span data-ttu-id="46c7d-107">Sin embargo, cambiar la zona horaria en una cita tiene otros efectos en la hora de inicio y finalización de la cita.</span><span class="sxs-lookup"><span data-stu-id="46c7d-107">However, changing the time zone on an appointment has other effects on the start and end time of the appointment.</span></span>
  
<span data-ttu-id="46c7d-108">Los valores de hora se almacenan en el servidor de Exchange en hora universal coordinada (UTC).</span><span class="sxs-lookup"><span data-stu-id="46c7d-108">Time values are stored on the Exchange server in Coordinate Universal Time (UTC).</span></span> <span data-ttu-id="46c7d-109">Por lo tanto, si se establece una cita para que empiece en 1:00 PM (13:00) en la zona horaria oriental (UTC-05:00), ese valor se almacena como 6:00 PM (18:00) en el servidor, siempre que la zona horaria esté en su fase de tiempo estándar.</span><span class="sxs-lookup"><span data-stu-id="46c7d-109">So if an appointment is set to start at 1:00 PM (13:00) in the Eastern time zone (UTC-05:00), that value is stored as 6:00 PM (18:00) on the server, assuming that the time zone is in its standard time phase.</span></span> <span data-ttu-id="46c7d-110">Cuando esa cita se ve en otras zonas horarias, se suma o resta el número correspondiente de horas del valor UTC para determinar la hora específica de la zona horaria.</span><span class="sxs-lookup"><span data-stu-id="46c7d-110">When that appointment is viewed in other time zones, the appropriate number of hours is added or subtracted from the UTC value to determine the time zone-specific time.</span></span> <span data-ttu-id="46c7d-111">Por ejemplo, si una cita tiene una hora de inicio de 1:00 PM oriental (6:00 P.M. UTC) y se ve desde un cliente en la zona horaria del Pacífico (UTC-08:00), la hora de inicio específica de la zona horaria de ese cliente sería 10:00 A.M. (18:00-08:00).</span><span class="sxs-lookup"><span data-stu-id="46c7d-111">For example, if an appointment has a start time at 1:00 PM Eastern (6:00 PM UTC), and is viewed from a client in the Pacific time zone (UTC-08:00), the time-zone specific start time for that client would be 10:00 AM (18:00 - 08:00).</span></span>
  
<span data-ttu-id="46c7d-112">Al actualizar la zona horaria de la cita sin actualizar la hora de inicio y finalización, el servidor actualiza los valores UTC almacenados en el servidor para mantener la hora de inicio y de finalización como las mismas horas específicas de la zona horaria.</span><span class="sxs-lookup"><span data-stu-id="46c7d-112">When you update the time zone of the appointment without updating the start and end time, the server updates the UTC values stored on the server to keep the start and end time as the same time zone-specific times.</span></span> <span data-ttu-id="46c7d-113">Por ejemplo, considere la cita 1:00 PM oriental.</span><span class="sxs-lookup"><span data-stu-id="46c7d-113">For example, consider the 1:00 PM Eastern appointment.</span></span> <span data-ttu-id="46c7d-114">La hora se almacena como 18:00 UTC en el servidor.</span><span class="sxs-lookup"><span data-stu-id="46c7d-114">The time is stored as 18:00 UTC on the server.</span></span> <span data-ttu-id="46c7d-115">Si la zona horaria de la cita se cambia a la zona horaria del Pacífico, el servidor cambia la hora de inicio a 1:00 PM hora del Pacífico (21:00 UTC).</span><span class="sxs-lookup"><span data-stu-id="46c7d-115">If the time zone of the appointment is changed to the Pacific time zone, the server shifts the start time to 1:00 PM Pacific (21:00 UTC).</span></span>
  
<span data-ttu-id="46c7d-116">Puede cambiar este comportamiento estableciendo explícitamente las horas de inicio y finalización.</span><span class="sxs-lookup"><span data-stu-id="46c7d-116">You can change this behavior by explicitly setting the start and end times.</span></span>
  
## <a name="updating-the-time-zone-on-an-existing-appointment-by-using-the-ews-managed-api"></a><span data-ttu-id="46c7d-117">Actualización de la zona horaria en una cita existente mediante la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="46c7d-117">Updating the time zone on an existing appointment by using the EWS Managed API</span></span>

<span data-ttu-id="46c7d-118">En el siguiente ejemplo, se usa la API administrada de EWS para actualizar la zona horaria de una cita existente a la zona horaria central mediante la actualización de las propiedades **appointment. StartTimeZone** y **appointment. EndTimeZone** .</span><span class="sxs-lookup"><span data-stu-id="46c7d-118">In the following example, the EWS Managed API is used to update the time zone on an existing appointment to the Central time zone by updating the **Appointment.StartTimeZone** and **Appointment.EndTimeZone** properties.</span></span> <span data-ttu-id="46c7d-119">Si el parámetro _shiftAppointnment_ está establecido en **true**, el código no establece explícitamente las horas de inicio y finalización de la cita.</span><span class="sxs-lookup"><span data-stu-id="46c7d-119">If the  _shiftAppointnment_ parameter is set to **true**, the code does not explicitly set the start and end times on the appointment.</span></span> <span data-ttu-id="46c7d-120">En este caso, el servidor cambiará las horas de inicio y finalización para mantenerlas en las mismas horas relativas a la zona horaria de la nueva zona horaria.</span><span class="sxs-lookup"><span data-stu-id="46c7d-120">In this case, the server will shift the start and end times to keep them at the same time zone-relative times in the new time zone.</span></span> <span data-ttu-id="46c7d-121">Si se establece en **false**, el código convierte las horas de inicio y finalización de forma explícita para mantener la cita a la vez en UTC.</span><span class="sxs-lookup"><span data-stu-id="46c7d-121">If set to **false**, the code converts the start and end times explicitly to keep the appointment at the same time in UTC.</span></span> 

<span data-ttu-id="46c7d-122">En este ejemplo se supone que el objeto **ExchangeService** se ha inicializado con valores válidos en las propiedades [Credentials](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.credentials%28v=exchg.80%29.aspx) y [URL](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.url%28v=exchg.80%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="46c7d-122">This example assumes that the **ExchangeService** object has been initialized with valid values in the [Credentials](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.credentials%28v=exchg.80%29.aspx) and [Url](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.url%28v=exchg.80%29.aspx) properties.</span></span> 
  
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

<span data-ttu-id="46c7d-123">Cuando se usa el ejemplo para actualizar una cita que empieza a 1:00 PM oriental y termina en 2:00 PM oriental, con el parámetro _shiftAppointment_ establecido en true y la propiedad [ExchangeService. TimeZone](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.timezone%28v=exchg.80%29.aspx) establecida en la zona horaria oriental, el resultado es similar al siguiente.</span><span class="sxs-lookup"><span data-stu-id="46c7d-123">When the example is used to update an appointment that starts at 1:00 PM Eastern and ends at 2:00 PM Eastern, with the  _shiftAppointment_ parameter set to true, and the [ExchangeService.TimeZone](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.timezone%28v=exchg.80%29.aspx) property set to the Eastern time zone, the output looks like the following.</span></span> 
  
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

<span data-ttu-id="46c7d-124">Cuando se usa el ejemplo para actualizar la misma cita con el parámetro _shiftAppointment_ establecido en false y la propiedad **TimeZone** se establece de nuevo en la zona horaria oriental, el resultado es un poco diferente.</span><span class="sxs-lookup"><span data-stu-id="46c7d-124">When the example is used to update the same appointment with the  _shiftAppointment_ parameter set to false, and with the **TimeZone** property again set to the Eastern time zone, the output looks a little different.</span></span> 
  
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

<span data-ttu-id="46c7d-125">Observe que las horas de inicio y finalización no han cambiado.</span><span class="sxs-lookup"><span data-stu-id="46c7d-125">Notice that the start and end times did not change.</span></span> <span data-ttu-id="46c7d-126">Esto se debe a que las horas se interpretan en la zona horaria oriental (porque la propiedad **TimeZone** se establece en la zona horaria oriental) y los valores de tiempo se actualizan para evitar que la cita se desplace.</span><span class="sxs-lookup"><span data-stu-id="46c7d-126">This is because the times are being interpreted in the Eastern time zone (because the **TimeZone** property is set to the Eastern time zone), and the time values were updated to prevent the appointment from shifting.</span></span> 
  
## <a name="updating-the-time-zone-on-an-existing-appointment-by-using-ews"></a><span data-ttu-id="46c7d-127">Actualización de la zona horaria en una cita existente mediante EWS</span><span class="sxs-lookup"><span data-stu-id="46c7d-127">Updating the time zone on an existing appointment by using EWS</span></span>

<span data-ttu-id="46c7d-128">El siguiente ejemplo de solicitud de [operación de UpdateItem](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) de EWS actualiza la zona horaria en una cita.</span><span class="sxs-lookup"><span data-stu-id="46c7d-128">The following example EWS [UpdateItem operation](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) request updates the time zone on an appointment.</span></span> <span data-ttu-id="46c7d-129">En este ejemplo solo se actualizan los elementos [StartTimeZone](https://msdn.microsoft.com/library/d38c4dc1-4ecb-42a1-8d57-a451b16a2de2%28Office.15%29.aspx) y [EndTimeZone](https://msdn.microsoft.com/library/6c53c337-be60-4d22-9e9e-a0c140c5e913%28Office.15%29.aspx) , por lo que el servidor cambiará las horas de inicio y finalización de la cita para mantenerla en el mismo tiempo relativo a la zona horaria en la nueva zona horaria.</span><span class="sxs-lookup"><span data-stu-id="46c7d-129">This example only updates the [StartTimeZone](https://msdn.microsoft.com/library/d38c4dc1-4ecb-42a1-8d57-a451b16a2de2%28Office.15%29.aspx) and [EndTimeZone](https://msdn.microsoft.com/library/6c53c337-be60-4d22-9e9e-a0c140c5e913%28Office.15%29.aspx) elements, so the server will shift the start and end times of the appointment to keep it at the same time-zone-relative time in the new time zone.</span></span> <span data-ttu-id="46c7d-130">El valor del elemento **Itemid** se acorta para facilitar su lectura.</span><span class="sxs-lookup"><span data-stu-id="46c7d-130">The value of the **ItemId** element is shortened for readability.</span></span> 
  
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

<span data-ttu-id="46c7d-131">La solicitud de ejemplo siguiente actualiza la zona horaria de la cita, y también actualiza las horas de inicio y finalización estableciendo explícitamente los elementos **Start** y **End** .</span><span class="sxs-lookup"><span data-stu-id="46c7d-131">The following example request updates the time zone of the appointment, and also updates the start and end times by explicitly setting the **Start** and **End** elements.</span></span> <span data-ttu-id="46c7d-132">El valor del elemento **Itemid** se acorta para facilitar su lectura.</span><span class="sxs-lookup"><span data-stu-id="46c7d-132">The value of the **ItemId** element is shortened for readability.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="46c7d-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="46c7d-133">See also</span></span>

- [<span data-ttu-id="46c7d-134">Zonas horarias y EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="46c7d-134">Time zones and EWS in Exchange</span></span>](time-zones-and-ews-in-exchange.md)   
- [<span data-ttu-id="46c7d-135">Crear citas en una zona horaria específica mediante EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="46c7d-135">Create appointments in a specific time zone by using EWS in Exchange</span></span>](how-to-create-appointments-in-a-specific-time-zone-by-using-ews-in-exchange.md)   
- [<span data-ttu-id="46c7d-136">Actualizar citas y reuniones mediante EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="46c7d-136">Update appointments and meetings by using EWS in Exchange</span></span>](how-to-update-appointments-and-meetings-by-using-ews-in-exchange.md)
    

