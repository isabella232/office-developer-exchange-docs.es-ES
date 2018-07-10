---
title: Crear eventos de día completo mediante el uso de EWS en Exchange
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 0fcb484b-4ffc-41a5-aeed-8c797766b70c
description: Obtenga información sobre cómo crear eventos de día completo mediante la API administrada de EWS o EWS en Exchange.
ms.openlocfilehash: 0547fdf0ca92ba0648caeb5de6940d90d2a8ff46
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763047"
---
# <a name="create-all-day-events-by-using-ews-in-exchange"></a><span data-ttu-id="f8742-103">Crear eventos de día completo mediante el uso de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="f8742-103">Create all-day events by using EWS in Exchange</span></span>

<span data-ttu-id="f8742-104">Obtenga información sobre cómo crear eventos de día completo mediante la API administrada de EWS o EWS en Exchange.</span><span class="sxs-lookup"><span data-stu-id="f8742-104">Learn how to create all-day events by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="f8742-105">Eventos de todo el día proporcionan una forma de representar algo que sucede para todo un día o varios días, por ejemplo, un día festivo o días de vacaciones.</span><span class="sxs-lookup"><span data-stu-id="f8742-105">All-day events provide a way to represent something that happens for an entire day or multiple days—for example, a holiday, or vacation days.</span></span> <span data-ttu-id="f8742-106">Crear eventos de día completo con la API administrada de EWS o EWS es un complemento.</span><span class="sxs-lookup"><span data-stu-id="f8742-106">Creating all-day events with the EWS Managed API or EWS is a snap.</span></span> <span data-ttu-id="f8742-107">Es igual que [crear citas](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md), pero con unos pequeños cambios.</span><span class="sxs-lookup"><span data-stu-id="f8742-107">It's just like [creating appointments](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md), but with a few small changes.</span></span>
  
## <a name="setting-start-and-end-times"></a><span data-ttu-id="f8742-108">Configuración de horas de inicio y finalización</span><span class="sxs-lookup"><span data-stu-id="f8742-108">Setting start and end times</span></span>

<span data-ttu-id="f8742-109">Por definición, inician eventos de día completo en la medianoche en un día específico y end 24 horas (o un múltiplo de 24 horas) más adelante.</span><span class="sxs-lookup"><span data-stu-id="f8742-109">By definition, all-day events start at midnight on a specific day, and end 24 hours (or a multiple of 24 hours) later.</span></span> <span data-ttu-id="f8742-110">Sin embargo, la API administrada de EWS y EWS permite especificar las horas que no sean medianoche al crear todos los eventos de día.</span><span class="sxs-lookup"><span data-stu-id="f8742-110">However, the EWS Managed API and EWS allow you to specify times other than midnight when creating all day events.</span></span> <span data-ttu-id="f8742-111">Esto puede provocar un comportamiento imprevisto si no tener en cuenta cómo traducir estos tiempos en el servidor.</span><span class="sxs-lookup"><span data-stu-id="f8742-111">This can lead to unintended behavior if you're not aware of how these times get translated on the server.</span></span>
  
<span data-ttu-id="f8742-112">Cuando se recibe una solicitud para crear un nuevo evento de día completo con los que no sean medianoche (en la [zona horaria de la solicitud o cita](time-zones-and-ews-in-exchange.md)) inicio o finalización, esas horas se ajustan a medianoche en la zona horaria adecuada según las reglas siguientes:</span><span class="sxs-lookup"><span data-stu-id="f8742-112">When a request is received to create a new all-day event with non-midnight (in the [time zone of the request or appointment](time-zones-and-ews-in-exchange.md)) start and/or end times, those times get adjusted to midnight in the appropriate time zone according to the following rules:</span></span>
  
- <span data-ttu-id="f8742-113">Horas de inicio de la medianoche de no se ajustan a la medianoche antes de la hora especificada.</span><span class="sxs-lookup"><span data-stu-id="f8742-113">Non-midnight start times are adjusted to the midnight prior to the time specified.</span></span> <span data-ttu-id="f8742-114">Por ejemplo, 1:00 P.M. en 6 de junio obtiene ajustados a las 12:00 A.M. en 6 de junio.</span><span class="sxs-lookup"><span data-stu-id="f8742-114">For example, 1:00 PM on June 6 gets adjusted to 12:00 AM on June 6.</span></span>
    
- <span data-ttu-id="f8742-115">Hora de finalización de la medianoche de no se ajusta a la medianoche después de la hora especificada.</span><span class="sxs-lookup"><span data-stu-id="f8742-115">Non-midnight end times are adjusted to the midnight after the time specified.</span></span> <span data-ttu-id="f8742-116">Por ejemplo, 1:00 P.M. en 6 de junio obtiene ajustados a las 12:00 A.M. en 7 de junio.</span><span class="sxs-lookup"><span data-stu-id="f8742-116">For example, 1:00 PM on June 6 gets adjusted to 12:00 AM on June 7.</span></span>
    
<span data-ttu-id="f8742-117">Por lo que es el evento de día completo que se crea siempre incluidos la hora de inicio y finalización que especifique, pero es posible que el tiempo adicional de notificación en el usuario del calendario de vencimiento para el cambio a partir de la medianoche.</span><span class="sxs-lookup"><span data-stu-id="f8742-117">So the all-day event that you create is always inclusive of the start and end time that you specify, but might claim additional time on the user's calendar due to the shift to midnight.</span></span> <span data-ttu-id="f8742-118">Debido a que el servidor va a ajustar la hora de inicio y final a partir de la medianoche, se recomienda que especifique la hora de inicio y final en la medianoche para evitar los cambios no deseados en los tiempos de.</span><span class="sxs-lookup"><span data-stu-id="f8742-118">Because the server will adjust the start and end time to midnight, we recommend that you specify your start and end time at midnight to avoid any unintended changes to the times.</span></span>
  
<span data-ttu-id="f8742-119">También es importante tener en cuenta las zonas horarias al crear eventos de día completo.</span><span class="sxs-lookup"><span data-stu-id="f8742-119">It's also important to consider time zones when creating all-day events.</span></span> <span data-ttu-id="f8742-120">Debido a que el Exchange server impone una medianoche inicio y hora en la zona horaria de la cita o la solicitud de finalización, la visualización de ese evento de día completo en un cliente configurado para una zona horaria diferente puede producir resultados inesperados.</span><span class="sxs-lookup"><span data-stu-id="f8742-120">Because the Exchange server enforces a midnight start and end time in the time zone of the request or appointment, viewing that all-day event in a client configured for a different time zone can yield unexpected results.</span></span> <span data-ttu-id="f8742-121">Dependiendo del cliente, puede aparecer como un evento de día completo con días adicionales que no tenía intención de incluir o no puede aparecer como un evento de día completo totalmente.</span><span class="sxs-lookup"><span data-stu-id="f8742-121">Depending on the client, it might appear as an all-day event with extra days that you did not intend to include, or it might not appear as an all-day event altogether.</span></span> <span data-ttu-id="f8742-122">Por este motivo, se recomienda usar el preferido zona horaria del usuario siempre que sea posible crear eventos de día completo.</span><span class="sxs-lookup"><span data-stu-id="f8742-122">Because of this, we recommend that you use the user's preferred time zone whenever possible when you create all-day events.</span></span>
  
## <a name="create-an-all-day-event-by-using-the-ews-managed-api"></a><span data-ttu-id="f8742-123">Crear un evento de día completo mediante el uso de la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="f8742-123">Create an all-day event by using the EWS Managed API</span></span>

<span data-ttu-id="f8742-124">En el ejemplo siguiente se muestra cómo usar la API administrada de EWS para crear un evento de día completo, comenzando en la fecha especificada por el parámetro _startDate_ y una duración para el número de días especificado por el parámetro _numDays_ .</span><span class="sxs-lookup"><span data-stu-id="f8742-124">The following example shows how to use the EWS Managed API to create an all-day event, starting on the date specified by the  _startDate_ parameter and lasting for the number of days specified by the  _numDays_ parameter.</span></span> <span data-ttu-id="f8742-125">Tenga en cuenta que se creará la cita en la zona horaria especificada por la propiedad [ExchangeService.TimeZone](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.exchangeservice.timezone%28v=exchg.80%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="f8742-125">Note that the appointment will be created in the time zone specified by the [ExchangeService.TimeZone](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.exchangeservice.timezone%28v=exchg.80%29.aspx) property.</span></span> <span data-ttu-id="f8742-126">En este ejemplo se da por supuesto que se ha inicializado el objeto [ExchangeService](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) pasado en el parámetro de _servicio_ con los valores válidos para las propiedades de [las credenciales](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.exchangeservicebase.credentials%28v=exchg.80%29.aspx) y [dirección Url](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.exchangeservice.url%28v=exchg.80%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="f8742-126">This example assumes that the [ExchangeService](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object passed in the  _service_ parameter has been initialized with valid values for the [Credentials](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.exchangeservicebase.credentials%28v=exchg.80%29.aspx) and [Url](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.exchangeservice.url%28v=exchg.80%29.aspx) properties.</span></span> 
  
```cs
static void CreateAllDayAppointment(ExchangeService service, DateTime startDate, int numDays)
{
    // Best practice is to set the start date to midnight
    // on the first day of the all-day event.
    DateTime startDateMidnight = startDate.Date;
    // The end date should be midnight on the first day
    // after the event.
    DateTime endDateMidnight = startDateMidnight.AddDays(numDays);
    Appointment allDayEvent = new Appointment(service);
    // Set IsAllDayEvent to true.
    allDayEvent.IsAllDayEvent = true;
    // Set other properties.
    allDayEvent.Subject = "Vacation";
    allDayEvent.LegacyFreeBusyStatus = LegacyFreeBusyStatus.OOF;
    allDayEvent.Start = startDateMidnight;
    allDayEvent.End = endDateMidnight;
    // Save the appointment.
    try
    {
        allDayEvent.Save(WellKnownFolderName.Calendar, SendInvitationsMode.SendToNone);
        Console.WriteLine("All day event created.");
    }
    catch (Exception ex)
    {
        Console.WriteLine("Error saving all day event: {0}", ex.Message);
    }
}
```

## <a name="create-an-all-day-event-by-using-ews"></a><span data-ttu-id="f8742-127">Crear un evento de día completo mediante el uso de EWS</span><span class="sxs-lookup"><span data-stu-id="f8742-127">Create an all-day event by using EWS</span></span>

<span data-ttu-id="f8742-128">En el ejemplo siguiente se muestra una solicitud de EWS [operación CreateItem](http://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) para crear un evento de día completo.</span><span class="sxs-lookup"><span data-stu-id="f8742-128">The following example shows an EWS [CreateItem operation](http://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) request to create an all-day event.</span></span> <span data-ttu-id="f8742-129">La cita se crea en la zona hora oriental, como se indica en el elemento [TimeZoneContext](http://msdn.microsoft.com/library/573c462b-aa1d-4ba0-8852-e3f48b26873b%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="f8742-129">The appointment is created in the Eastern time zone, as indicated by the [TimeZoneContext](http://msdn.microsoft.com/library/573c462b-aa1d-4ba0-8852-e3f48b26873b%28Office.15%29.aspx) element.</span></span> <span data-ttu-id="f8742-130">Tenga en cuenta que la parte de los valores de los elementos de [Inicio](http://msdn.microsoft.com/library/7cfe9979-c893-4f9b-b3a1-8f9e17515a4b%28Office.15%29.aspx) y [fin de](http://msdn.microsoft.com/library/72329821-32ff-495d-b6e5-fdc011003c2e%28Office.15%29.aspx) la hora son ambos 04:00Z, que se convierte a partir de la medianoche en la zona hora oriental durante el horario de verano.</span><span class="sxs-lookup"><span data-stu-id="f8742-130">Notice that the time portion of the values of the [Start](http://msdn.microsoft.com/library/7cfe9979-c893-4f9b-b3a1-8f9e17515a4b%28Office.15%29.aspx) and [End](http://msdn.microsoft.com/library/72329821-32ff-495d-b6e5-fdc011003c2e%28Office.15%29.aspx) elements are both 04:00Z, which converts to midnight in the Eastern time zone during daylight saving time.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
    xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
    xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
    xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
    <t:TimeZoneContext>
      <t:TimeZoneDefinition Id="Eastern Standard Time" />
    </t:TimeZoneContext>
  </soap:Header>
  <soap:Body>
    <m:CreateItem SendMeetingInvitations="SendToNone">
      <m:SavedItemFolderId>
        <t:DistinguishedFolderId Id="calendar" />
      </m:SavedItemFolderId>
      <m:Items>
        <t:CalendarItem>
          <t:Subject>Vacation</t:Subject>
          <t:Start>2014-06-09T04:00:00.000Z</t:Start>
          <t:End>2014-06-10T04:00:00.000Z</t:End>
          <t:IsAllDayEvent>true</t:IsAllDayEvent>
          <t:LegacyFreeBusyStatus>OOF</t:LegacyFreeBusyStatus>
        </t:CalendarItem>
      </m:Items>
    </m:CreateItem>
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a><span data-ttu-id="f8742-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="f8742-131">See also</span></span>


- [<span data-ttu-id="f8742-132">Calendarios y EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="f8742-132">Calendars and EWS in Exchange</span></span>](calendars-and-ews-in-exchange.md)
    
- [<span data-ttu-id="f8742-133">Crear citas y reuniones mediante el uso de EWS en Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="f8742-133">Create appointments and meetings by using EWS in Exchange 2013</span></span>](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md)
    
- [<span data-ttu-id="f8742-134">Zonas horarias y EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="f8742-134">Time zones and EWS in Exchange</span></span>](time-zones-and-ews-in-exchange.md)
    

