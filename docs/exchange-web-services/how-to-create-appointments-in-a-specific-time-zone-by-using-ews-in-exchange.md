---
title: Crear citas en una zona horaria específica mediante EWS en Exchange
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: e68aaa27-250e-4170-b099-077a979c127c
description: Obtenga información sobre cómo crear citas en zonas horarias específicas usando la API administrada de EWS o EWS en Exchange.
ms.openlocfilehash: 9b1160a9d62ab092d1b60265eba1ad953be0032b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44456860"
---
# <a name="create-appointments-in-a-specific-time-zone-by-using-ews-in-exchange"></a><span data-ttu-id="4d63e-103">Crear citas en una zona horaria específica mediante EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="4d63e-103">Create appointments in a specific time zone by using EWS in Exchange</span></span>

<span data-ttu-id="4d63e-104">Obtenga información sobre cómo crear citas en zonas horarias específicas usando la API administrada de EWS o EWS en Exchange.</span><span class="sxs-lookup"><span data-stu-id="4d63e-104">Learn how to create appointments in specific time zones by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="4d63e-105">Cuando se crea una cita o una reunión en un calendario de Exchange, la zona horaria utilizada para especificar las horas de inicio y finalización se guarda como zona horaria de creación para la cita.</span><span class="sxs-lookup"><span data-stu-id="4d63e-105">When an appointment or meeting is created on an Exchange calendar, the time zone used to specify the start and end times is saved as the creation time zone for the appointment.</span></span> <span data-ttu-id="4d63e-106">Esa zona horaria también se usa para [interpretar los valores de fecha y hora que no tienen una zona horaria explícita especificada](time-zones-and-ews-in-exchange.md), por lo que es importante comprender las opciones para especificar la zona horaria.</span><span class="sxs-lookup"><span data-stu-id="4d63e-106">That time zone is also used to [interpret date and time values that do not have an explicit time zone specified](time-zones-and-ews-in-exchange.md), so it is important to understand your options to specify the time zone.</span></span>
  
## <a name="creating-appointments-in-different-time-zones-by-using-the-ews-managed-api"></a><span data-ttu-id="4d63e-107">Crear citas en distintas zonas horarias mediante la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="4d63e-107">Creating appointments in different time zones by using the EWS Managed API</span></span>

<span data-ttu-id="4d63e-108">Al crear citas o reuniones mediante la API administrada de EWS, tiene tres opciones para especificar la zona horaria:</span><span class="sxs-lookup"><span data-stu-id="4d63e-108">When creating appointments or meetings using the EWS Managed API, you have three options for specifying the time zone:</span></span>
  
- <span data-ttu-id="4d63e-109">Para usar la zona horaria del equipo en el que se ejecuta la API administrada de EWS, no especifique una zona horaria al crear el objeto [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="4d63e-109">To use the time zone of the computer where your EWS Managed API is executing, do not specify a time zone when creating the [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object.</span></span> 
    
- <span data-ttu-id="4d63e-110">Para usar una zona horaria específica para todas las propiedades de fecha y hora, incluidas las propiedades al crear una nueva cita o reunión, especifique una zona horaria en el constructor para el objeto **ExchangeService** .</span><span class="sxs-lookup"><span data-stu-id="4d63e-110">To use a specific time zone for all date/time properties, including properties when creating a new appointment or meeting, specify a time zone in the constructor for the **ExchangeService** object.</span></span> 
    
- <span data-ttu-id="4d63e-111">Para usar una zona horaria diferente a la especificada en la propiedad [ExchangeService. TimeZone](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.timezone%28v=exchg.80%29.aspx) , use las propiedades [appointment. StartTimeZone](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.starttimezone%28v=exchg.80%29.aspx) y [appointment. EndTimeZone](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.endtimezone%28v=exchg.80%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="4d63e-111">To use a different time zone than the one specified in the [ExchangeService.TimeZone](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.timezone%28v=exchg.80%29.aspx) property, use the [Appointment.StartTimeZone](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.starttimezone%28v=exchg.80%29.aspx) and [Appointment.EndTimeZone](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.endtimezone%28v=exchg.80%29.aspx) properties.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="4d63e-112">La propiedad **EndTimeZone** solo está disponible cuando la propiedad [ExchangeService. RequestedServerVersion](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.requestedserverversion%28v=exchg.80%29.aspx) se establece en **Exchange2010** o posterior.</span><span class="sxs-lookup"><span data-stu-id="4d63e-112">The **EndTimeZone** property is only available when the [ExchangeService.RequestedServerVersion](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.requestedserverversion%28v=exchg.80%29.aspx) property is set to **Exchange2010** or later.</span></span> <span data-ttu-id="4d63e-113">Si no está disponible, el establecimiento de **StartTimeZone** se aplica a las horas de inicio y finalización de la cita.</span><span class="sxs-lookup"><span data-stu-id="4d63e-113">If it is not available, setting the **StartTimeZone** applies to both the start and end times of the appointment.</span></span> 
  
<span data-ttu-id="4d63e-114">En el siguiente ejemplo, se usa la API administrada de EWS para crear tres citas.</span><span class="sxs-lookup"><span data-stu-id="4d63e-114">In the following example, the EWS Managed API is used to create three appointments.</span></span> <span data-ttu-id="4d63e-115">Cada cita está configurada para iniciarse a las 1:00 PM dos días a partir de ahora, en una zona horaria no especificada y finalizar una hora más tarde.</span><span class="sxs-lookup"><span data-stu-id="4d63e-115">Each appointment is set to start at 1:00 PM two days from now, in an unspecified time zone, and end one hour later.</span></span> <span data-ttu-id="4d63e-116">La primera cita se crea en la zona horaria del equipo cliente mediante el comportamiento predeterminado de la API administrada de EWS.</span><span class="sxs-lookup"><span data-stu-id="4d63e-116">The first appointment is created in the client computer's time zone by using default EWS Managed API behavior.</span></span> <span data-ttu-id="4d63e-117">El segundo se crea en la zona horaria central mediante las propiedades **appointment. StartTimeZone** y **appointment. EndTimeZone** .</span><span class="sxs-lookup"><span data-stu-id="4d63e-117">The second is created in the Central time zone by using the **Appointment.StartTimeZone** and **Appointment.EndTimeZone** properties.</span></span> <span data-ttu-id="4d63e-118">El tercero se crea en la zona horaria de las montañas rocosas mediante la propiedad **ExchangeService. TimeZone** .</span><span class="sxs-lookup"><span data-stu-id="4d63e-118">The third is created in the Mountain time zone by using the **ExchangeService.TimeZone** property.</span></span> 
  
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

<span data-ttu-id="4d63e-119">Cuando este ejemplo se ejecuta en un equipo cliente configurado en la zona horaria oriental y las tres citas que crea se ven desde un cliente configurado en la zona horaria oriental, aparecen en 1:00 PM, 2:00 PM y 3:00 PM, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="4d63e-119">When this example is executed on a client computer configured in the Eastern time zone, and the three appointments it creates are viewed from a client configured in the Eastern time zone, they appear at 1:00 PM, 2:00 PM, and 3:00 PM, respectively.</span></span>
  
## <a name="creating-appointments-in-different-time-zones-by-using-ews"></a><span data-ttu-id="4d63e-120">Creación de citas en distintas zonas horarias mediante EWS</span><span class="sxs-lookup"><span data-stu-id="4d63e-120">Creating appointments in different time zones by using EWS</span></span>

<span data-ttu-id="4d63e-121">Al crear citas o reuniones con EWS, tiene tres opciones para especificar la zona horaria:</span><span class="sxs-lookup"><span data-stu-id="4d63e-121">When creating appointments or meetings using EWS, you have three options for specifying the time zone:</span></span>
  
- <span data-ttu-id="4d63e-122">Para usar la hora universal coordinada (UTC), no incluya un elemento [TimeZoneContext](https://msdn.microsoft.com/library/573c462b-aa1d-4ba0-8852-e3f48b26873b%28Office.15%29.aspx) , el elemento [MeetingTimeZone](https://msdn.microsoft.com/library/413b47d9-8126-462c-9a4f-4e771a5e8889%28Office.15%29.aspx) (solo Exchange 2007) o los elementos [StartTimeZone](https://msdn.microsoft.com/library/d38c4dc1-4ecb-42a1-8d57-a451b16a2de2%28Office.15%29.aspx) y [EndTimeZone](https://msdn.microsoft.com/library/6c53c337-be60-4d22-9e9e-a0c140c5e913%28Office.15%29.aspx) (Exchange 2010 o posterior) en la solicitud de [operación CreateItem](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="4d63e-122">To use Coordinated Universal Time (UTC), do not include a [TimeZoneContext](https://msdn.microsoft.com/library/573c462b-aa1d-4ba0-8852-e3f48b26873b%28Office.15%29.aspx) element, [MeetingTimeZone](https://msdn.microsoft.com/library/413b47d9-8126-462c-9a4f-4e771a5e8889%28Office.15%29.aspx) element (Exchange 2007 only), or [StartTimeZone](https://msdn.microsoft.com/library/d38c4dc1-4ecb-42a1-8d57-a451b16a2de2%28Office.15%29.aspx) and [EndTimeZone](https://msdn.microsoft.com/library/6c53c337-be60-4d22-9e9e-a0c140c5e913%28Office.15%29.aspx) elements (Exchange 2010 and later) in the [CreateItem operation](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) request.</span></span> 
    
- <span data-ttu-id="4d63e-123">Para usar una zona horaria específica para todas las propiedades de fecha y hora, incluidas las propiedades al crear una nueva cita o reunión, especifique una zona horaria en el elemento [TimeZoneContext](https://msdn.microsoft.com/library/573c462b-aa1d-4ba0-8852-e3f48b26873b%28Office.15%29.aspx) de la solicitud de [operación CreateItem](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="4d63e-123">To use a specific time zone for all date/time properties, including properties when creating a new appointment or meeting, specify a time zone in the [TimeZoneContext](https://msdn.microsoft.com/library/573c462b-aa1d-4ba0-8852-e3f48b26873b%28Office.15%29.aspx) element in the [CreateItem operation](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) request.</span></span> 
    
- <span data-ttu-id="4d63e-124">Para usar una zona horaria diferente a la especificada en el elemento [TimeZoneContext](https://msdn.microsoft.com/library/573c462b-aa1d-4ba0-8852-e3f48b26873b%28Office.15%29.aspx) , incluya un elemento [TimeZoneContext](https://msdn.microsoft.com/library/573c462b-aa1d-4ba0-8852-e3f48b26873b%28Office.15%29.aspx) , elemento [MeetingTimeZone](https://msdn.microsoft.com/library/413b47d9-8126-462c-9a4f-4e771a5e8889%28Office.15%29.aspx) (solo Exchange 2007) o [StartTimeZone](https://msdn.microsoft.com/library/d38c4dc1-4ecb-42a1-8d57-a451b16a2de2%28Office.15%29.aspx) y [EndTimeZone](https://msdn.microsoft.com/library/6c53c337-be60-4d22-9e9e-a0c140c5e913%28Office.15%29.aspx) (Exchange 2010 o posterior) en la solicitud de [operación CreateItem](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="4d63e-124">To use a different time zone than the one specified in the [TimeZoneContext](https://msdn.microsoft.com/library/573c462b-aa1d-4ba0-8852-e3f48b26873b%28Office.15%29.aspx) element, include a [TimeZoneContext](https://msdn.microsoft.com/library/573c462b-aa1d-4ba0-8852-e3f48b26873b%28Office.15%29.aspx) element, [MeetingTimeZone](https://msdn.microsoft.com/library/413b47d9-8126-462c-9a4f-4e771a5e8889%28Office.15%29.aspx) element (Exchange 2007 only), or [StartTimeZone](https://msdn.microsoft.com/library/d38c4dc1-4ecb-42a1-8d57-a451b16a2de2%28Office.15%29.aspx) and [EndTimeZone](https://msdn.microsoft.com/library/6c53c337-be60-4d22-9e9e-a0c140c5e913%28Office.15%29.aspx) elements (Exchange 2010 and later) in the [CreateItem operation](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) request.</span></span> 
    
<span data-ttu-id="4d63e-125">El siguiente ejemplo de solicitud de [operación del CreateItem](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) crea una cita con UTC.</span><span class="sxs-lookup"><span data-stu-id="4d63e-125">The following example [CreateItem operation](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) request creates an appointment using UTC.</span></span> <span data-ttu-id="4d63e-126">Observe que el elemento **TimeZoneContext** , el elemento **StartTimeZone** y el elemento **EndTimeZone** están ausentes.</span><span class="sxs-lookup"><span data-stu-id="4d63e-126">Notice that the **TimeZoneContext** element, the **StartTimeZone** element, and the **EndTimeZone** element are absent.</span></span> <span data-ttu-id="4d63e-127">Los valores de los elementos **Start** y **End** se expresan en UTC.</span><span class="sxs-lookup"><span data-stu-id="4d63e-127">The **Start** and **End** element values are expressed in UTC.</span></span> 
  
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

<span data-ttu-id="4d63e-128">En el siguiente ejemplo, la solicitud de [operación CreateItem](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) usa los elementos **StartTimeZone** y **EndTimeZone** para especificar la zona horaria central de la cita.</span><span class="sxs-lookup"><span data-stu-id="4d63e-128">The following example [CreateItem operation](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) request uses the **StartTimeZone** and **EndTimeZone** elements to specify the Central time zone for the appointment.</span></span> <span data-ttu-id="4d63e-129">Observe que el elemento **TimeZoneContext** está ausente.</span><span class="sxs-lookup"><span data-stu-id="4d63e-129">Notice that the **TimeZoneContext** element is absent.</span></span> <span data-ttu-id="4d63e-130">Sin embargo, si está presente, los valores de los elementos **StartTimeZone** y **EndTimeZone** invalidarían su valor.</span><span class="sxs-lookup"><span data-stu-id="4d63e-130">However, if it were present, the values of the **StartTimeZone** and **EndTimeZone** elements would override its value.</span></span> <span data-ttu-id="4d63e-131">De nuevo, los valores de los elementos **Start** y **End** se expresan en UTC.</span><span class="sxs-lookup"><span data-stu-id="4d63e-131">Again, the **Start** and **End** element values are expressed in UTC.</span></span> 
  
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

<span data-ttu-id="4d63e-132">El siguiente ejemplo de solicitud de la [operación CreateItem](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) establece el elemento **TimeZoneContext** en la zona horaria de las montañas rocosas.</span><span class="sxs-lookup"><span data-stu-id="4d63e-132">The following example [CreateItem operation](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) request sets the **TimeZoneContext** element to the Mountain time zone.</span></span> <span data-ttu-id="4d63e-133">Observe que los elementos **StartTimeZone** y **EndTimeZone** están ausentes.</span><span class="sxs-lookup"><span data-stu-id="4d63e-133">Notice that the **StartTimeZone** and **EndTimeZone** elements are absent.</span></span> <span data-ttu-id="4d63e-134">De nuevo, los valores de los elementos **Start** y **End** se expresan en UTC.</span><span class="sxs-lookup"><span data-stu-id="4d63e-134">Again, the **Start** and **End** element values are expressed in UTC.</span></span> 
  
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

<span data-ttu-id="4d63e-135">Cuando las tres citas creadas por las solicitudes de ejemplo anteriores de EWS se ven desde un cliente configurado en la zona horaria oriental, aparecen en 1:00 PM, 2:00 PM y 3:00 PM, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="4d63e-135">When the three appointments created by the previous EWS example requests are viewed from a client configured in the Eastern time zone, they appear at 1:00 PM, 2:00 PM, and 3:00 PM, respectively.</span></span>
  
## 

<span data-ttu-id="4d63e-136">Ahora que sabe cómo crear citas en zonas horarias específicas, es posible que desee [actualizar las zonas horarias de las citas existentes](how-to-update-the-time-zone-for-an-appointment-by-using-ews-in-exchange.md) a una diferente.</span><span class="sxs-lookup"><span data-stu-id="4d63e-136">Now that you know how to create appointments in specific time zones, you might want to [update the time zones on existing appointments](how-to-update-the-time-zone-for-an-appointment-by-using-ews-in-exchange.md) to a different one.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4d63e-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="4d63e-137">See also</span></span>


- [<span data-ttu-id="4d63e-138">Zonas horarias y EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="4d63e-138">Time zones and EWS in Exchange</span></span>](time-zones-and-ews-in-exchange.md)
    
- [<span data-ttu-id="4d63e-139">Actualizar la zona horaria de una cita mediante EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="4d63e-139">Update the time zone for an appointment by using EWS in Exchange</span></span>](how-to-update-the-time-zone-for-an-appointment-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="4d63e-140">Crear citas y reuniones mediante EWS en Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="4d63e-140">Create appointments and meetings by using EWS in Exchange 2013</span></span>](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md)
    

