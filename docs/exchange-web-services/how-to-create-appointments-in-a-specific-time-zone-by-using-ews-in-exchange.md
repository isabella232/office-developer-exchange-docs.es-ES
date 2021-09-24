---
title: Crear citas en una zona horaria específica mediante EWS en Exchange
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: e68aaa27-250e-4170-b099-077a979c127c
description: Obtenga información sobre cómo crear citas en zonas horarias específicas mediante la API administrada ews o EWS en Exchange.
ms.openlocfilehash: 589c72982fdda568170468c376b8a6d9f598aa36
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59521147"
---
# <a name="create-appointments-in-a-specific-time-zone-by-using-ews-in-exchange"></a>Crear citas en una zona horaria específica mediante EWS en Exchange

Obtenga información sobre cómo crear citas en zonas horarias específicas mediante la API administrada ews o EWS en Exchange.
  
Cuando se crea una cita o reunión en un calendario Exchange, la zona horaria usada para especificar las horas de inicio y finalización se guarda como zona horaria de creación para la cita. Esa zona horaria también se usa para interpretar valores de fecha y hora que no tienen una zona horaria explícita [especificada,](time-zones-and-ews-in-exchange.md)por lo que es importante comprender las opciones para especificar la zona horaria.
  
## <a name="creating-appointments-in-different-time-zones-by-using-the-ews-managed-api"></a>Crear citas en distintas zonas horarias mediante la API administrada ews

Al crear citas o reuniones con la API administrada ews, tiene tres opciones para especificar la zona horaria:
  
- Para usar la zona horaria del equipo donde se ejecuta la API administrada ews, no especifique una zona horaria al crear el [objeto ExchangeService.](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) 
    
- Para usar una zona horaria específica para todas las propiedades de fecha y hora, incluidas las propiedades al crear una nueva cita o reunión, especifique una zona horaria en el constructor para el **objeto ExchangeService.** 
    
- Para usar una zona horaria diferente a la especificada en la propiedad [ExchangeService.TimeZone,](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.timezone%28v=exchg.80%29.aspx) use las propiedades [Appointment.StartTimeZone](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.starttimezone%28v=exchg.80%29.aspx) y [Appointment.EndTimeZone.](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.endtimezone%28v=exchg.80%29.aspx) 
    
    > [!NOTE]
    > La **propiedad EndTimeZone** solo está disponible cuando la propiedad [ExchangeService.RequestedServerVersion](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.requestedserverversion%28v=exchg.80%29.aspx) está establecida en **Exchange2010** o posterior. Si no está disponible, la configuración de **StartTimeZone** se aplica tanto a las horas de inicio como de finalización de la cita. 
  
En el siguiente ejemplo, se usa la API administrada ews para crear tres citas. Cada cita está configurada para comenzar a la 1:00 p.m. dentro de dos días, en una zona horaria no especificada y finalizar una hora más tarde. La primera cita se crea en la zona horaria del equipo cliente mediante el comportamiento predeterminado de la API administrada ews. El segundo se crea en la zona horaria central mediante las **propiedades Appointment.StartTimeZone** y **Appointment.EndTimeZone.** El tercero se crea en la zona horaria de montaña mediante la **propiedad ExchangeService.TimeZone.** 
  
```cs
using Microsoft.Exchange.WebServices.Data;
using System.Security;
static void CreateAppointments(string userEmail, SecureString userPass)
{
    // *****************************************************
    // Create an appointment using the client computer's time zone.
    // *****************************************************
    // Do not specify a time zone when creating the ExchangeService.
    ExchangeService clientTZService = new ExchangeService(ExchangeVersion.Exchange2010);
    clientTZService.Credentials = new NetworkCredential(userEmail, userPass);
    clientTZService.AutodiscoverUrl(userEmail, redirectionCallback);
    // Create the appointment.
    Appointment clientTZAppt = new Appointment(clientTZService);
    clientTZAppt.Subject = "Appointment created using client time zone";
    clientTZAppt.Body = new MessageBody(string.Format("Time zone: {0}", clientTZService.TimeZone.DisplayName));
    // Set the start time to 1:00 PM two days from today.
    DateTime startTime = new DateTime(DateTime.Now.Year, DateTime.Now.Month, DateTime.Now.Day + 2);
    startTime = startTime.AddHours(13);
    clientTZAppt.Start = startTime;
    // Set the end time to 2:00 PM on that same day.
    DateTime endTime = startTime.AddHours(1);
    clientTZAppt.End = endTime;
    // Save the appointment to the default calendar.
    try
    {
        // This method results in a call to EWS.
        clientTZAppt.Save(SendInvitationsMode.SendToNone);
    }
    catch (Exception ex)
    {
        Console.WriteLine("Error saving appointment: {0}", ex.Message);
    }
    // *****************************************************
    // Create an appointment in the Central time zone by
    // using the StartTimeZone property.
    // *****************************************************
    // Retrieve the Central time zone.
    TimeZoneInfo centralTZ = TimeZoneInfo.FindSystemTimeZoneById("Central Standard Time");
    // Create the appointment.
    Appointment centralTZAppt = new Appointment(clientTZService);
    centralTZAppt.Subject = "Appointment created using Central time zone";
    centralTZAppt.Body = new MessageBody(string.Format("Time zone: {0}", centralTZ.DisplayName));
    // Set the time zone on the appointment.
    centralTZAppt.StartTimeZone = centralTZ;
    centralTZAppt.EndTimeZone = centralTZ;
    // Set the start time to 1:00 PM two days from today.
    centralTZAppt.Start = startTime;
    // Set the end time to 2:00 PM on that same day.
    centralTZAppt.End = endTime;
    // Save the appointment to the default calendar.
    try
    {
        // This method results in a call to EWS.
        centralTZAppt.Save(SendInvitationsMode.SendToNone);
    }
    catch (Exception ex)
    {
        Console.WriteLine("Error saving appointment: {0}", ex.Message);
    }
    // *****************************************************
    // Create an appointment in the Mountain time zone by
    // using the ExchangeService.TimeZone property.
    // *****************************************************
    // Specify the Mountain time zone when creating the ExchangeService.
    TimeZoneInfo mountainTZ = TimeZoneInfo.FindSystemTimeZoneById("Mountain Standard Time");
    ExchangeService mountainTZService = new ExchangeService(ExchangeVersion.Exchange2010, mountainTZ);
    mountainTZService.Credentials = new NetworkCredential(userEmail, userPass);
    mountainTZService.AutodiscoverUrl(userEmail, redirectionCallback);
    // Create the appointment.
    Appointment mountainTZAppt = new Appointment(mountainTZService);
    mountainTZAppt.Subject = "Appointment created using Mountain time zone";
    mountainTZAppt.Body = new MessageBody(string.Format("Time zone: {0}", mountainTZService.TimeZone.DisplayName));
    // Set the start time to 1:00 PM two days from today.
    mountainTZAppt.Start = startTime;
    // Set the end time to 2:00 PM on that same day.
    mountainTZAppt.End = endTime;
    // Save the appointment to the default calendar.
    try
    {
        // This method results in a call to EWS.
        mountainTZAppt.Save(SendInvitationsMode.SendToNone);
    }
    catch (Exception ex)
    {
        Console.WriteLine("Error saving appointment: {0}", ex.Message);
    }
}
```

Cuando este ejemplo se ejecuta en un equipo cliente configurado en la zona horaria oriental y las tres citas que crea se ven desde un cliente configurado en la zona horaria oriental, aparecen a la 1:00 PM, 2:00 PM y 3:00 PM, respectivamente.
  
## <a name="creating-appointments-in-different-time-zones-by-using-ews"></a>Crear citas en distintas zonas horarias mediante EWS

Al crear citas o reuniones con EWS, tiene tres opciones para especificar la zona horaria:
  
- Para usar la hora universal coordinada (UTC), no incluya un elemento [TimeZoneContext,](https://msdn.microsoft.com/library/573c462b-aa1d-4ba0-8852-e3f48b26873b%28Office.15%29.aspx) un elemento [MeetingTimeZone](https://msdn.microsoft.com/library/413b47d9-8126-462c-9a4f-4e771a5e8889%28Office.15%29.aspx) (solo Exchange 2007) ni los elementos [StartTimeZone](https://msdn.microsoft.com/library/d38c4dc1-4ecb-42a1-8d57-a451b16a2de2%28Office.15%29.aspx) y [EndTimeZone](https://msdn.microsoft.com/library/6c53c337-be60-4d22-9e9e-a0c140c5e913%28Office.15%29.aspx) (Exchange 2010 y versiones posteriores) en la solicitud de operación [CreateItem.](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) 
    
- Para usar una zona horaria específica para todas las propiedades de fecha y hora, incluidas las propiedades al crear una nueva cita o reunión, especifique una zona horaria en el elemento [TimeZoneContext](https://msdn.microsoft.com/library/573c462b-aa1d-4ba0-8852-e3f48b26873b%28Office.15%29.aspx) en la solicitud de [operación CreateItem.](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) 
    
- Para usar una zona horaria diferente a la especificada en el elemento [TimeZoneContext,](https://msdn.microsoft.com/library/573c462b-aa1d-4ba0-8852-e3f48b26873b%28Office.15%29.aspx) incluya un elemento [TimeZoneContext,](https://msdn.microsoft.com/library/573c462b-aa1d-4ba0-8852-e3f48b26873b%28Office.15%29.aspx) un elemento [MeetingTimeZone](https://msdn.microsoft.com/library/413b47d9-8126-462c-9a4f-4e771a5e8889%28Office.15%29.aspx) (solo Exchange 2007) o los elementos [StartTimeZone](https://msdn.microsoft.com/library/d38c4dc1-4ecb-42a1-8d57-a451b16a2de2%28Office.15%29.aspx) y [EndTimeZone](https://msdn.microsoft.com/library/6c53c337-be60-4d22-9e9e-a0c140c5e913%28Office.15%29.aspx) (Exchange 2010 y posteriores) en la solicitud de operación [CreateItem.](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) 
    
En el siguiente [ejemplo, la solicitud de operación CreateItem](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) crea una cita con UTC. Observe que el **elemento TimeZoneContext,** **el elemento StartTimeZone** y el elemento **EndTimeZone** no están presentes. Los **valores de** los elementos Start y **End** se expresan en UTC. 
  
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
    <m:CreateItem SendMeetingInvitations="SendToNone">
      <m:Items>
        <t:CalendarItem>
          <t:Subject>Appointment created using UTC</t:Subject>
          <t:Body BodyType="HTML">Time zone: UTC</t:Body>
          <t:Start>2014-06-07T17:00:00.000Z</t:Start>
          <t:End>2014-06-07T18:00:00.000Z</t:End>
        </t:CalendarItem>
      </m:Items>
    </m:CreateItem>
  </soap:Body>
</soap:Envelope>
```

En el siguiente [ejemplo, la solicitud de](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) operación CreateItem usa los elementos **StartTimeZone** y **EndTimeZone** para especificar la zona horaria central para la cita. Observe que el **elemento TimeZoneContext** no está presente. Sin embargo, si estuviera presente, los valores de los **elementos StartTimeZone** y **EndTimeZone** invalidarían su valor. De nuevo, **los valores de** los elementos Start y **End** se expresan en UTC. 
  
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
    <m:CreateItem SendMeetingInvitations="SendToNone">
      <m:Items>
        <t:CalendarItem>
          <t:Subject>Appointment created using Central time zone</t:Subject>
          <t:Body BodyType="HTML">Time zone: (UTC-06:00) Central Time (US &amp;amp; Canada)</t:Body>
          <t:Start>2014-06-07T18:00:00.000Z</t:Start>
          <t:End>2014-06-07T19:00:00.000Z</t:End>
          <t:StartTimeZone Id="Central Standard Time" />
          <t:EndTimeZone Id="Central Standard Time" />
        </t:CalendarItem>
      </m:Items>
    </m:CreateItem>
  </soap:Body>
</soap:Envelope>
```

En el siguiente [ejemplo, la solicitud de operación CreateItem](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) establece el **elemento TimeZoneContext** en la zona horaria mountain. Observe que los **elementos StartTimeZone** **y EndTimeZone** no están presentes. De nuevo, **los valores de** los elementos Start y **End** se expresan en UTC. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
    xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
    xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
    xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2010" />
    <t:TimeZoneContext>
      <t:TimeZoneDefinition Id="Mountain Standard Time" />
    </t:TimeZoneContext>
  </soap:Header>
  <soap:Body>
    <m:CreateItem SendMeetingInvitations="SendToNone">
      <m:Items>
        <t:CalendarItem>
          <t:Subject>Appointment created using Mountain time zone</t:Subject>
          <t:Body BodyType="HTML">Time zone: (UTC-07:00) Mountain Time (US &amp;amp; Canada)</t:Body>
          <t:Start>2014-06-07T19:00:00.000Z</t:Start>
          <t:End>2014-06-07T20:00:00.000Z</t:End>
        </t:CalendarItem>
      </m:Items>
    </m:CreateItem>
  </soap:Body>
</soap:Envelope>
```

Cuando las tres citas creadas por las solicitudes de ejemplo de EWS anteriores se ven desde un cliente configurado en la zona horaria oriental, aparecen a la 1:00 PM, 2:00 PM y 3:00 PM, respectivamente.
  
## 

Ahora que sabe cómo crear citas en zonas horarias específicas, es posible que desee actualizar las zonas horarias de las citas [existentes](how-to-update-the-time-zone-for-an-appointment-by-using-ews-in-exchange.md) a una diferente. 
  
## <a name="see-also"></a>Ver también


- [Zonas horarias y EWS en Exchange](time-zones-and-ews-in-exchange.md)
    
- [Actualice la zona horaria de una cita mediante EWS en Exchange](how-to-update-the-time-zone-for-an-appointment-by-using-ews-in-exchange.md)
    
- [Crear citas y reuniones mediante EWS en Exchange 2013](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md)
    

