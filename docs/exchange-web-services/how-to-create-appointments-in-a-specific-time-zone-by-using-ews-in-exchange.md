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
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763057"
---
# <a name="create-appointments-in-a-specific-time-zone-by-using-ews-in-exchange"></a><span data-ttu-id="6a2c9-103">Crear citas en una zona horaria concreta mediante el uso de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="6a2c9-103">Create appointments in a specific time zone by using EWS in Exchange</span></span>

<span data-ttu-id="6a2c9-104">Obtenga información sobre cómo crear citas en zonas horarias específicas mediante el uso de la API administrada de EWS o EWS en Exchange.</span><span class="sxs-lookup"><span data-stu-id="6a2c9-104">Learn how to create appointments in specific time zones by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="6a2c9-105">Cuando se crea una cita o reunión en un calendario de Exchange, la zona horaria que se usa para especificar las horas de inicio y final se guarda como la zona horaria de creación para la cita.</span><span class="sxs-lookup"><span data-stu-id="6a2c9-105">When an appointment or meeting is created on an Exchange calendar, the time zone used to specify the start and end times is saved as the creation time zone for the appointment.</span></span> <span data-ttu-id="6a2c9-106">Esa zona horaria también se utiliza para [interpretar los valores de fecha y hora en que no tienen una zona horaria explícita especificada](time-zones-and-ews-in-exchange.md), por lo que es importante comprender las opciones para especificar la zona horaria.</span><span class="sxs-lookup"><span data-stu-id="6a2c9-106">That time zone is also used to [interpret date and time values that do not have an explicit time zone specified](time-zones-and-ews-in-exchange.md), so it is important to understand your options to specify the time zone.</span></span>
  
## <a name="creating-appointments-in-different-time-zones-by-using-the-ews-managed-api"></a><span data-ttu-id="6a2c9-107">Crear citas en distintas zonas horarias mediante el uso de la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="6a2c9-107">Creating appointments in different time zones by using the EWS Managed API</span></span>

<span data-ttu-id="6a2c9-108">Al crear citas o reuniones mediante la API administrada de EWS, dispone de tres opciones para especificar la zona horaria:</span><span class="sxs-lookup"><span data-stu-id="6a2c9-108">When creating appointments or meetings using the EWS Managed API, you have three options for specifying the time zone:</span></span>
  
- <span data-ttu-id="6a2c9-109">Para usar la zona horaria del equipo donde se ejecuta la API administrada de EWS, no especifique una zona horaria al crear el objeto [ExchangeService](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="6a2c9-109">To use the time zone of the computer where your EWS Managed API is executing, do not specify a time zone when creating the [ExchangeService](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object.</span></span> 
    
- <span data-ttu-id="6a2c9-110">Para usar una zona horaria concreta para todas las propiedades de fecha y hora, incluidas las propiedades al crear una nueva cita o reunión, especifique una zona horaria en el constructor para el objeto **ExchangeService** .</span><span class="sxs-lookup"><span data-stu-id="6a2c9-110">To use a specific time zone for all date/time properties, including properties when creating a new appointment or meeting, specify a time zone in the constructor for the **ExchangeService** object.</span></span> 
    
- <span data-ttu-id="6a2c9-111">Para usar una zona horaria diferente que no sea el especificado en la propiedad [ExchangeService.TimeZone](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.exchangeservice.timezone%28v=exchg.80%29.aspx) , use las propiedades [Appointment.StartTimeZone](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.appointment.starttimezone%28v=exchg.80%29.aspx) y [Appointment.EndTimeZone](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.appointment.endtimezone%28v=exchg.80%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="6a2c9-111">To use a different time zone than the one specified in the [ExchangeService.TimeZone](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.exchangeservice.timezone%28v=exchg.80%29.aspx) property, use the [Appointment.StartTimeZone](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.appointment.starttimezone%28v=exchg.80%29.aspx) and [Appointment.EndTimeZone](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.appointment.endtimezone%28v=exchg.80%29.aspx) properties.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="6a2c9-112">La propiedad **EndTimeZone** sólo está disponible cuando se establece la propiedad [ExchangeService.RequestedServerVersion](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.exchangeservicebase.requestedserverversion%28v=exchg.80%29.aspx) a **Exchange2010** o posterior.</span><span class="sxs-lookup"><span data-stu-id="6a2c9-112">The **EndTimeZone** property is only available when the [ExchangeService.RequestedServerVersion](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.exchangeservicebase.requestedserverversion%28v=exchg.80%29.aspx) property is set to **Exchange2010** or later.</span></span> <span data-ttu-id="6a2c9-113">Si no está disponible, la **StartTimeZone** se aplican a veces el inicio y el final de la cita.</span><span class="sxs-lookup"><span data-stu-id="6a2c9-113">If it is not available, setting the **StartTimeZone** applies to both the start and end times of the appointment.</span></span> 
  
<span data-ttu-id="6a2c9-114">En el siguiente ejemplo, se usa la API administrada de EWS para crear tres citas.</span><span class="sxs-lookup"><span data-stu-id="6a2c9-114">In the following example, the EWS Managed API is used to create three appointments.</span></span> <span data-ttu-id="6a2c9-115">Cada cita está configurado para iniciarse a la 1:00 P.M. dos días a partir de ahora, en una zona horaria no especificada y el final de una hora más tarde.</span><span class="sxs-lookup"><span data-stu-id="6a2c9-115">Each appointment is set to start at 1:00 PM two days from now, in an unspecified time zone, and end one hour later.</span></span> <span data-ttu-id="6a2c9-116">Se crea la primera cita en la zona horaria del equipo cliente mediante el uso de comportamiento predeterminado de la API administrada de EWS.</span><span class="sxs-lookup"><span data-stu-id="6a2c9-116">The first appointment is created in the client computer's time zone by using default EWS Managed API behavior.</span></span> <span data-ttu-id="6a2c9-117">El segundo se crea en la zona horaria Central mediante el uso de las propiedades **Appointment.StartTimeZone** y **Appointment.EndTimeZone** .</span><span class="sxs-lookup"><span data-stu-id="6a2c9-117">The second is created in the Central time zone by using the **Appointment.StartTimeZone** and **Appointment.EndTimeZone** properties.</span></span> <span data-ttu-id="6a2c9-118">La tercera se crea en la zona horaria de montaña mediante el uso de la propiedad **ExchangeService.TimeZone** .</span><span class="sxs-lookup"><span data-stu-id="6a2c9-118">The third is created in the Mountain time zone by using the **ExchangeService.TimeZone** property.</span></span> 
  
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

<span data-ttu-id="6a2c9-119">Cuando en este ejemplo, se ejecuta en un equipo cliente configurado en la zona hora oriental y se ven las tres citas que se creen desde un cliente configurado en la zona hora oriental, que aparecen a la 1:00 P.M., 2:00 P.M. y 3:00 P.M., respectivamente.</span><span class="sxs-lookup"><span data-stu-id="6a2c9-119">When this example is executed on a client computer configured in the Eastern time zone, and the three appointments it creates are viewed from a client configured in the Eastern time zone, they appear at 1:00 PM, 2:00 PM, and 3:00 PM, respectively.</span></span>
  
## <a name="creating-appointments-in-different-time-zones-by-using-ews"></a><span data-ttu-id="6a2c9-120">Crear citas en distintas zonas horarias mediante el uso de EWS</span><span class="sxs-lookup"><span data-stu-id="6a2c9-120">Creating appointments in different time zones by using EWS</span></span>

<span data-ttu-id="6a2c9-121">Al crear citas o reuniones mediante EWS, dispone de tres opciones para especificar la zona horaria:</span><span class="sxs-lookup"><span data-stu-id="6a2c9-121">When creating appointments or meetings using EWS, you have three options for specifying the time zone:</span></span>
  
- <span data-ttu-id="6a2c9-122">Para usar la hora Universal coordinada (UTC), no incluya un elemento [TimeZoneContext](http://msdn.microsoft.com/library/573c462b-aa1d-4ba0-8852-e3f48b26873b%28Office.15%29.aspx) , elemento [MeetingTimeZone](http://msdn.microsoft.com/library/413b47d9-8126-462c-9a4f-4e771a5e8889%28Office.15%29.aspx) (sólo en Exchange 2007,) o [StartTimeZone](http://msdn.microsoft.com/library/d38c4dc1-4ecb-42a1-8d57-a451b16a2de2%28Office.15%29.aspx) y elementos [EndTimeZone](http://msdn.microsoft.com/library/6c53c337-be60-4d22-9e9e-a0c140c5e913%28Office.15%29.aspx) (Exchange 2010 y versiones posterior) en el [ Operación CreateItem](http://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) solicitud.</span><span class="sxs-lookup"><span data-stu-id="6a2c9-122">To use Coordinated Universal Time (UTC), do not include a [TimeZoneContext](http://msdn.microsoft.com/library/573c462b-aa1d-4ba0-8852-e3f48b26873b%28Office.15%29.aspx) element, [MeetingTimeZone](http://msdn.microsoft.com/library/413b47d9-8126-462c-9a4f-4e771a5e8889%28Office.15%29.aspx) element (Exchange 2007 only), or [StartTimeZone](http://msdn.microsoft.com/library/d38c4dc1-4ecb-42a1-8d57-a451b16a2de2%28Office.15%29.aspx) and [EndTimeZone](http://msdn.microsoft.com/library/6c53c337-be60-4d22-9e9e-a0c140c5e913%28Office.15%29.aspx) elements (Exchange 2010 and later) in the [CreateItem operation](http://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) request.</span></span> 
    
- <span data-ttu-id="6a2c9-123">Para usar una zona horaria concreta para todas las propiedades de fecha y hora, incluidas las propiedades al crear una nueva cita o reunión, especifique una zona horaria en el elemento [TimeZoneContext](http://msdn.microsoft.com/library/573c462b-aa1d-4ba0-8852-e3f48b26873b%28Office.15%29.aspx) en la solicitud de [operación CreateItem](http://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="6a2c9-123">To use a specific time zone for all date/time properties, including properties when creating a new appointment or meeting, specify a time zone in the [TimeZoneContext](http://msdn.microsoft.com/library/573c462b-aa1d-4ba0-8852-e3f48b26873b%28Office.15%29.aspx) element in the [CreateItem operation](http://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) request.</span></span> 
    
- <span data-ttu-id="6a2c9-124">Para usar una zona horaria diferente que el especificado en el elemento [TimeZoneContext](http://msdn.microsoft.com/library/573c462b-aa1d-4ba0-8852-e3f48b26873b%28Office.15%29.aspx) , incluir un elemento [TimeZoneContext](http://msdn.microsoft.com/library/573c462b-aa1d-4ba0-8852-e3f48b26873b%28Office.15%29.aspx) , elemento [MeetingTimeZone](http://msdn.microsoft.com/library/413b47d9-8126-462c-9a4f-4e771a5e8889%28Office.15%29.aspx) (sólo en Exchange 2007) o [StartTimeZone](http://msdn.microsoft.com/library/d38c4dc1-4ecb-42a1-8d57-a451b16a2de2%28Office.15%29.aspx) y [EndTimeZone](http://msdn.microsoft.com/library/6c53c337-be60-4d22-9e9e-a0c140c5e913%28Office.15%29.aspx) (de elementos Exchange 2010 y versiones posterior) en la solicitud de [operación CreateItem](http://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="6a2c9-124">To use a different time zone than the one specified in the [TimeZoneContext](http://msdn.microsoft.com/library/573c462b-aa1d-4ba0-8852-e3f48b26873b%28Office.15%29.aspx) element, include a [TimeZoneContext](http://msdn.microsoft.com/library/573c462b-aa1d-4ba0-8852-e3f48b26873b%28Office.15%29.aspx) element, [MeetingTimeZone](http://msdn.microsoft.com/library/413b47d9-8126-462c-9a4f-4e771a5e8889%28Office.15%29.aspx) element (Exchange 2007 only), or [StartTimeZone](http://msdn.microsoft.com/library/d38c4dc1-4ecb-42a1-8d57-a451b16a2de2%28Office.15%29.aspx) and [EndTimeZone](http://msdn.microsoft.com/library/6c53c337-be60-4d22-9e9e-a0c140c5e913%28Office.15%29.aspx) elements (Exchange 2010 and later) in the [CreateItem operation](http://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) request.</span></span> 
    
<span data-ttu-id="6a2c9-125">El siguiente ejemplo de solicitud de [operación CreateItem](http://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) crea una cita usando la hora UTC.</span><span class="sxs-lookup"><span data-stu-id="6a2c9-125">The following example [CreateItem operation](http://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) request creates an appointment using UTC.</span></span> <span data-ttu-id="6a2c9-126">Tenga en cuenta que el elemento **TimeZoneContext** , el elemento **StartTimeZone** y el elemento **EndTimeZone** están ausentes.</span><span class="sxs-lookup"><span data-stu-id="6a2c9-126">Notice that the **TimeZoneContext** element, the **StartTimeZone** element, and the **EndTimeZone** element are absent.</span></span> <span data-ttu-id="6a2c9-127">Los valores del elemento **Start** y **End** se expresan en UTC.</span><span class="sxs-lookup"><span data-stu-id="6a2c9-127">The **Start** and **End** element values are expressed in UTC.</span></span> 
  
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

<span data-ttu-id="6a2c9-128">El siguiente ejemplo de solicitud [CreateItem operation](http://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) usa los elementos **StartTimeZone** y **EndTimeZone** para especificar la zona horaria Central para la cita.</span><span class="sxs-lookup"><span data-stu-id="6a2c9-128">The following example [CreateItem operation](http://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) request uses the **StartTimeZone** and **EndTimeZone** elements to specify the Central time zone for the appointment.</span></span> <span data-ttu-id="6a2c9-129">Tenga en cuenta que el elemento **TimeZoneContext** está ausente.</span><span class="sxs-lookup"><span data-stu-id="6a2c9-129">Notice that the **TimeZoneContext** element is absent.</span></span> <span data-ttu-id="6a2c9-130">Sin embargo, si estuviera presente, los valores de los elementos **StartTimeZone** y **EndTimeZone** haría reemplazar su valor.</span><span class="sxs-lookup"><span data-stu-id="6a2c9-130">However, if it were present, the values of the **StartTimeZone** and **EndTimeZone** elements would override its value.</span></span> <span data-ttu-id="6a2c9-131">Una vez más, los valores del elemento **Start** y **End** se expresan en UTC.</span><span class="sxs-lookup"><span data-stu-id="6a2c9-131">Again, the **Start** and **End** element values are expressed in UTC.</span></span> 
  
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

<span data-ttu-id="6a2c9-132">La siguiente solicitud [CreateItem operation](http://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) de ejemplo, Establece el elemento de **TimeZoneContext** a la zona horaria de montaña.</span><span class="sxs-lookup"><span data-stu-id="6a2c9-132">The following example [CreateItem operation](http://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) request sets the **TimeZoneContext** element to the Mountain time zone.</span></span> <span data-ttu-id="6a2c9-133">Tenga en cuenta que los elementos **StartTimeZone** y **EndTimeZone** son ausentes.</span><span class="sxs-lookup"><span data-stu-id="6a2c9-133">Notice that the **StartTimeZone** and **EndTimeZone** elements are absent.</span></span> <span data-ttu-id="6a2c9-134">Una vez más, los valores del elemento **Start** y **End** se expresan en UTC.</span><span class="sxs-lookup"><span data-stu-id="6a2c9-134">Again, the **Start** and **End** element values are expressed in UTC.</span></span> 
  
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

<span data-ttu-id="6a2c9-135">Cuando se ven las tres citas creadas por el ejemplo anterior de EWS solicitudes desde un cliente configurado en la zona hora oriental, que aparecen a la 1:00 P.M., 2:00 P.M. y 3:00 P.M., respectivamente.</span><span class="sxs-lookup"><span data-stu-id="6a2c9-135">When the three appointments created by the previous EWS example requests are viewed from a client configured in the Eastern time zone, they appear at 1:00 PM, 2:00 PM, and 3:00 PM, respectively.</span></span>
  
## 

<span data-ttu-id="6a2c9-136">Ahora que sabe cómo crear citas en zonas horarias específicas, es posible que desee para [actualizar las zonas horarias en las citas existentes](how-to-update-the-time-zone-for-an-appointment-by-using-ews-in-exchange.md) a otro.</span><span class="sxs-lookup"><span data-stu-id="6a2c9-136">Now that you know how to create appointments in specific time zones, you might want to [update the time zones on existing appointments](how-to-update-the-time-zone-for-an-appointment-by-using-ews-in-exchange.md) to a different one.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6a2c9-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="6a2c9-137">See also</span></span>


- [<span data-ttu-id="6a2c9-138">Zonas horarias y EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="6a2c9-138">Time zones and EWS in Exchange</span></span>](time-zones-and-ews-in-exchange.md)
    
- [<span data-ttu-id="6a2c9-139">Actualización de la zona horaria para una cita mediante EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="6a2c9-139">Update the time zone for an appointment by using EWS in Exchange</span></span>](how-to-update-the-time-zone-for-an-appointment-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="6a2c9-140">Crear citas y reuniones mediante el uso de EWS en Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="6a2c9-140">Create appointments and meetings by using EWS in Exchange 2013</span></span>](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md)
    

