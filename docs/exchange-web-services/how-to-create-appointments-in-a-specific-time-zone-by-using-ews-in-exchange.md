---
title: Crear citas en una zona horaria concreta mediante el uso de EWS en Exchange
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: e68aaa27-250e-4170-b099-077a979c127c
description: Obtenga información sobre cómo crear citas en zonas horarias específicas mediante el uso de la API administrada de EWS o EWS en Exchange.
ms.openlocfilehash: 1725498847f89a417b62a06fb8a3109af5c4deb0
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763057"
---
# <a name="create-appointments-in-a-specific-time-zone-by-using-ews-in-exchange"></a>Crear citas en una zona horaria concreta mediante el uso de EWS en Exchange

Obtenga información sobre cómo crear citas en zonas horarias específicas mediante el uso de la API administrada de EWS o EWS en Exchange.
  
Cuando se crea una cita o reunión en un calendario de Exchange, la zona horaria que se usa para especificar las horas de inicio y final se guarda como la zona horaria de creación para la cita. Esa zona horaria también se utiliza para [interpretar los valores de fecha y hora en que no tienen una zona horaria explícita especificada](time-zones-and-ews-in-exchange.md), por lo que es importante comprender las opciones para especificar la zona horaria.
  
## <a name="creating-appointments-in-different-time-zones-by-using-the-ews-managed-api"></a>Crear citas en distintas zonas horarias mediante el uso de la API administrada de EWS

Al crear citas o reuniones mediante la API administrada de EWS, dispone de tres opciones para especificar la zona horaria:
  
- Para usar la zona horaria del equipo donde se ejecuta la API administrada de EWS, no especifique una zona horaria al crear el objeto [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) . 
    
- Para usar una zona horaria concreta para todas las propiedades de fecha y hora, incluidas las propiedades al crear una nueva cita o reunión, especifique una zona horaria en el constructor para el objeto **ExchangeService** . 
    
- Para usar una zona horaria diferente que no sea el especificado en la propiedad [ExchangeService.TimeZone](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.timezone%28v=exchg.80%29.aspx) , use las propiedades [Appointment.StartTimeZone](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.starttimezone%28v=exchg.80%29.aspx) y [Appointment.EndTimeZone](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.endtimezone%28v=exchg.80%29.aspx) . 
    
    > [!NOTE]
    > La propiedad **EndTimeZone** sólo está disponible cuando se establece la propiedad [ExchangeService.RequestedServerVersion](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservicebase.requestedserverversion%28v=exchg.80%29.aspx) a **Exchange2010** o posterior. Si no está disponible, la **StartTimeZone** se aplican a veces el inicio y el final de la cita. 
  
En el siguiente ejemplo, se usa la API administrada de EWS para crear tres citas. Cada cita está configurado para iniciarse a la 1:00 P.M. dos días a partir de ahora, en una zona horaria no especificada y el final de una hora más tarde. Se crea la primera cita en la zona horaria del equipo cliente mediante el uso de comportamiento predeterminado de la API administrada de EWS. El segundo se crea en la zona horaria Central mediante el uso de las propiedades **Appointment.StartTimeZone** y **Appointment.EndTimeZone** . La tercera se crea en la zona horaria de montaña mediante el uso de la propiedad **ExchangeService.TimeZone** . 
  
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

Cuando en este ejemplo, se ejecuta en un equipo cliente configurado en la zona hora oriental y se ven las tres citas que se creen desde un cliente configurado en la zona hora oriental, que aparecen a la 1:00 P.M., 2:00 P.M. y 3:00 P.M., respectivamente.
  
## <a name="creating-appointments-in-different-time-zones-by-using-ews"></a>Crear citas en distintas zonas horarias mediante el uso de EWS

Al crear citas o reuniones mediante EWS, dispone de tres opciones para especificar la zona horaria:
  
- Para usar la hora Universal coordinada (UTC), no incluya un elemento [TimeZoneContext](http://msdn.microsoft.com/library/573c462b-aa1d-4ba0-8852-e3f48b26873b%28Office.15%29.aspx) , elemento [MeetingTimeZone](http://msdn.microsoft.com/library/413b47d9-8126-462c-9a4f-4e771a5e8889%28Office.15%29.aspx) (sólo en Exchange 2007,) o [StartTimeZone](http://msdn.microsoft.com/library/d38c4dc1-4ecb-42a1-8d57-a451b16a2de2%28Office.15%29.aspx) y elementos [EndTimeZone](http://msdn.microsoft.com/library/6c53c337-be60-4d22-9e9e-a0c140c5e913%28Office.15%29.aspx) (Exchange 2010 y versiones posterior) en el [ Operación CreateItem](http://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) solicitud. 
    
- Para usar una zona horaria concreta para todas las propiedades de fecha y hora, incluidas las propiedades al crear una nueva cita o reunión, especifique una zona horaria en el elemento [TimeZoneContext](http://msdn.microsoft.com/library/573c462b-aa1d-4ba0-8852-e3f48b26873b%28Office.15%29.aspx) en la solicitud de [operación CreateItem](http://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) . 
    
- Para usar una zona horaria diferente que el especificado en el elemento [TimeZoneContext](http://msdn.microsoft.com/library/573c462b-aa1d-4ba0-8852-e3f48b26873b%28Office.15%29.aspx) , incluir un elemento [TimeZoneContext](http://msdn.microsoft.com/library/573c462b-aa1d-4ba0-8852-e3f48b26873b%28Office.15%29.aspx) , elemento [MeetingTimeZone](http://msdn.microsoft.com/library/413b47d9-8126-462c-9a4f-4e771a5e8889%28Office.15%29.aspx) (sólo en Exchange 2007) o [StartTimeZone](http://msdn.microsoft.com/library/d38c4dc1-4ecb-42a1-8d57-a451b16a2de2%28Office.15%29.aspx) y [EndTimeZone](http://msdn.microsoft.com/library/6c53c337-be60-4d22-9e9e-a0c140c5e913%28Office.15%29.aspx) (de elementos Exchange 2010 y versiones posterior) en la solicitud de [operación CreateItem](http://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) . 
    
El siguiente ejemplo de solicitud de [operación CreateItem](http://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) crea una cita usando la hora UTC. Tenga en cuenta que el elemento **TimeZoneContext** , el elemento **StartTimeZone** y el elemento **EndTimeZone** están ausentes. Los valores del elemento **Start** y **End** se expresan en UTC. 
  
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

El siguiente ejemplo de solicitud [CreateItem operation](http://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) usa los elementos **StartTimeZone** y **EndTimeZone** para especificar la zona horaria Central para la cita. Tenga en cuenta que el elemento **TimeZoneContext** está ausente. Sin embargo, si estuviera presente, los valores de los elementos **StartTimeZone** y **EndTimeZone** haría reemplazar su valor. Una vez más, los valores del elemento **Start** y **End** se expresan en UTC. 
  
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

La siguiente solicitud [CreateItem operation](http://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) de ejemplo, Establece el elemento de **TimeZoneContext** a la zona horaria de montaña. Tenga en cuenta que los elementos **StartTimeZone** y **EndTimeZone** son ausentes. Una vez más, los valores del elemento **Start** y **End** se expresan en UTC. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
    xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
    xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
    xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
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

Cuando se ven las tres citas creadas por el ejemplo anterior de EWS solicitudes desde un cliente configurado en la zona hora oriental, que aparecen a la 1:00 P.M., 2:00 P.M. y 3:00 P.M., respectivamente.
  
## 

Ahora que sabe cómo crear citas en zonas horarias específicas, es posible que desee para [actualizar las zonas horarias en las citas existentes](how-to-update-the-time-zone-for-an-appointment-by-using-ews-in-exchange.md) a otro. 
  
## <a name="see-also"></a>Ver también


- [Zonas horarias y EWS en Exchange](time-zones-and-ews-in-exchange.md)
    
- [Actualización de la zona horaria para una cita mediante EWS en Exchange](how-to-update-the-time-zone-for-an-appointment-by-using-ews-in-exchange.md)
    
- [Crear citas y reuniones mediante el uso de EWS en Exchange 2013](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md)
    

