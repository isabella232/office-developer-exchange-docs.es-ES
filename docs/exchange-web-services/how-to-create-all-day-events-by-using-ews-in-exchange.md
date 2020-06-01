---
title: Crear eventos de día completo mediante EWS en Exchange
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 0fcb484b-4ffc-41a5-aeed-8c797766b70c
description: Obtenga información sobre cómo crear eventos de todo el día mediante la API administrada de EWS o EWS en Exchange.
ms.openlocfilehash: 6be638c17cc0e0c86fa6b4217169aa7259dfd4aa
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44456867"
---
# <a name="create-all-day-events-by-using-ews-in-exchange"></a><span data-ttu-id="0e9f7-103">Crear eventos de día completo mediante EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="0e9f7-103">Create all-day events by using EWS in Exchange</span></span>

<span data-ttu-id="0e9f7-104">Obtenga información sobre cómo crear eventos de todo el día mediante la API administrada de EWS o EWS en Exchange.</span><span class="sxs-lookup"><span data-stu-id="0e9f7-104">Learn how to create all-day events by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="0e9f7-105">Los eventos de todo el día proporcionan una forma de representar algo que ocurre en un solo día o en varios días (por ejemplo, un día festivo o días de vacaciones).</span><span class="sxs-lookup"><span data-stu-id="0e9f7-105">All-day events provide a way to represent something that happens for an entire day or multiple days—for example, a holiday, or vacation days.</span></span> <span data-ttu-id="0e9f7-106">La creación de eventos de todo el día con la API administrada de EWS o EWS es un complemento.</span><span class="sxs-lookup"><span data-stu-id="0e9f7-106">Creating all-day events with the EWS Managed API or EWS is a snap.</span></span> <span data-ttu-id="0e9f7-107">Es igual que [crear citas](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md), pero con algunos pequeños cambios.</span><span class="sxs-lookup"><span data-stu-id="0e9f7-107">It's just like [creating appointments](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md), but with a few small changes.</span></span>
  
## <a name="setting-start-and-end-times"></a><span data-ttu-id="0e9f7-108">Establecer las horas de inicio y finalización</span><span class="sxs-lookup"><span data-stu-id="0e9f7-108">Setting start and end times</span></span>

<span data-ttu-id="0e9f7-109">Por definición, los eventos de todos los días comienzan a medianoche en un día específico y finalizan 24 horas (o un múltiplo de 24 horas) más adelante.</span><span class="sxs-lookup"><span data-stu-id="0e9f7-109">By definition, all-day events start at midnight on a specific day, and end 24 hours (or a multiple of 24 hours) later.</span></span> <span data-ttu-id="0e9f7-110">Sin embargo, la API administrada de EWS y EWS le permiten especificar horas distintas de medianoche al crear eventos de día completo.</span><span class="sxs-lookup"><span data-stu-id="0e9f7-110">However, the EWS Managed API and EWS allow you to specify times other than midnight when creating all day events.</span></span> <span data-ttu-id="0e9f7-111">Esto puede llevar a un comportamiento imprevisto si no tiene constancia de cómo estas horas se traducen en el servidor.</span><span class="sxs-lookup"><span data-stu-id="0e9f7-111">This can lead to unintended behavior if you're not aware of how these times get translated on the server.</span></span>
  
<span data-ttu-id="0e9f7-112">Cuando se recibe una solicitud para crear un nuevo evento de día completo con una hora distinta de la medianoche (en la [zona horaria de la solicitud o la cita](time-zones-and-ews-in-exchange.md)), esas horas se ajustan a la medianoche en la zona horaria adecuada según las siguientes reglas:</span><span class="sxs-lookup"><span data-stu-id="0e9f7-112">When a request is received to create a new all-day event with non-midnight (in the [time zone of the request or appointment](time-zones-and-ews-in-exchange.md)) start and/or end times, those times get adjusted to midnight in the appropriate time zone according to the following rules:</span></span>
  
- <span data-ttu-id="0e9f7-113">Las horas de inicio que no sean de medianoche se ajustan a la medianoche antes de la hora especificada.</span><span class="sxs-lookup"><span data-stu-id="0e9f7-113">Non-midnight start times are adjusted to the midnight prior to the time specified.</span></span> <span data-ttu-id="0e9f7-114">Por ejemplo, 1:00 PM el 6 de junio se ajusta a 12:00 AM el 6 de junio.</span><span class="sxs-lookup"><span data-stu-id="0e9f7-114">For example, 1:00 PM on June 6 gets adjusted to 12:00 AM on June 6.</span></span>
    
- <span data-ttu-id="0e9f7-115">Las horas de finalización que no sean de medianoche se ajustan a la medianoche después de la hora especificada.</span><span class="sxs-lookup"><span data-stu-id="0e9f7-115">Non-midnight end times are adjusted to the midnight after the time specified.</span></span> <span data-ttu-id="0e9f7-116">Por ejemplo, 1:00 PM el 6 de junio se ajusta a 12:00 AM el 7 de junio.</span><span class="sxs-lookup"><span data-stu-id="0e9f7-116">For example, 1:00 PM on June 6 gets adjusted to 12:00 AM on June 7.</span></span>
    
<span data-ttu-id="0e9f7-117">Por lo tanto, el evento de todo el día que se crea siempre está incluido en las horas de inicio y finalización especificadas, pero puede reclamar más tiempo en el calendario del usuario debido al cambio a medianoche.</span><span class="sxs-lookup"><span data-stu-id="0e9f7-117">So the all-day event that you create is always inclusive of the start and end time that you specify, but might claim additional time on the user's calendar due to the shift to midnight.</span></span> <span data-ttu-id="0e9f7-118">Como el servidor ajustará la hora de inicio y de finalización a medianoche, se recomienda especificar la hora de inicio y de finalización a medianoche para evitar cambios no deseados en las horas.</span><span class="sxs-lookup"><span data-stu-id="0e9f7-118">Because the server will adjust the start and end time to midnight, we recommend that you specify your start and end time at midnight to avoid any unintended changes to the times.</span></span>
  
<span data-ttu-id="0e9f7-119">También es importante tener en cuenta las zonas horarias al crear eventos de día completo.</span><span class="sxs-lookup"><span data-stu-id="0e9f7-119">It's also important to consider time zones when creating all-day events.</span></span> <span data-ttu-id="0e9f7-120">Debido a que el servidor de Exchange aplica una hora de inicio y finalización de la medianoche en la zona horaria de la solicitud o cita, ver el evento de todo el día en un cliente configurado para una zona horaria diferente puede producir resultados inesperados.</span><span class="sxs-lookup"><span data-stu-id="0e9f7-120">Because the Exchange server enforces a midnight start and end time in the time zone of the request or appointment, viewing that all-day event in a client configured for a different time zone can yield unexpected results.</span></span> <span data-ttu-id="0e9f7-121">Según el cliente, es posible que aparezca como un evento de todo el día con días adicionales que no pretendía incluir, o puede que no aparezca como un evento de todo el día al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="0e9f7-121">Depending on the client, it might appear as an all-day event with extra days that you did not intend to include, or it might not appear as an all-day event altogether.</span></span> <span data-ttu-id="0e9f7-122">Por este motivo, se recomienda usar la zona horaria preferida del usuario siempre que sea posible al crear eventos de todo el día.</span><span class="sxs-lookup"><span data-stu-id="0e9f7-122">Because of this, we recommend that you use the user's preferred time zone whenever possible when you create all-day events.</span></span>
  
## <a name="create-an-all-day-event-by-using-the-ews-managed-api"></a><span data-ttu-id="0e9f7-123">Crear un evento de todo el día mediante la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="0e9f7-123">Create an all-day event by using the EWS Managed API</span></span>

<span data-ttu-id="0e9f7-124">En el ejemplo siguiente se muestra cómo usar la API administrada de EWS para crear un evento de todo el día, a partir de la fecha especificada por el parámetro _startDate_ y que dura durante el número de días especificado por el parámetro _numDays_ .</span><span class="sxs-lookup"><span data-stu-id="0e9f7-124">The following example shows how to use the EWS Managed API to create an all-day event, starting on the date specified by the  _startDate_ parameter and lasting for the number of days specified by the  _numDays_ parameter.</span></span> <span data-ttu-id="0e9f7-125">Tenga en cuenta que la cita se creará en la zona horaria especificada por la propiedad [ExchangeService. TimeZone](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.timezone%28v=exchg.80%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="0e9f7-125">Note that the appointment will be created in the time zone specified by the [ExchangeService.TimeZone](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.timezone%28v=exchg.80%29.aspx) property.</span></span> <span data-ttu-id="0e9f7-126">En este ejemplo se supone que el objeto [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) pasado en el parámetro _Service_ se ha inicializado con valores válidos para las [credenciales](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.credentials%28v=exchg.80%29.aspx) y las propiedades de [dirección URL](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.url%28v=exchg.80%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="0e9f7-126">This example assumes that the [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object passed in the  _service_ parameter has been initialized with valid values for the [Credentials](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.credentials%28v=exchg.80%29.aspx) and [Url](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.url%28v=exchg.80%29.aspx) properties.</span></span> 
  
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

## <a name="create-an-all-day-event-by-using-ews"></a><span data-ttu-id="0e9f7-127">Crear un evento de todo el día mediante EWS</span><span class="sxs-lookup"><span data-stu-id="0e9f7-127">Create an all-day event by using EWS</span></span>

<span data-ttu-id="0e9f7-128">En el ejemplo siguiente se muestra una solicitud de operación de EWS [CreateItem](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) para crear un evento de todo el día.</span><span class="sxs-lookup"><span data-stu-id="0e9f7-128">The following example shows an EWS [CreateItem operation](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) request to create an all-day event.</span></span> <span data-ttu-id="0e9f7-129">La cita se crea en la zona horaria oriental, como se indica en el elemento [TimeZoneContext](https://msdn.microsoft.com/library/573c462b-aa1d-4ba0-8852-e3f48b26873b%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="0e9f7-129">The appointment is created in the Eastern time zone, as indicated by the [TimeZoneContext](https://msdn.microsoft.com/library/573c462b-aa1d-4ba0-8852-e3f48b26873b%28Office.15%29.aspx) element.</span></span> <span data-ttu-id="0e9f7-130">Observe que la parte de hora de los valores de los elementos [Start](https://msdn.microsoft.com/library/7cfe9979-c893-4f9b-b3a1-8f9e17515a4b%28Office.15%29.aspx) y [End](https://msdn.microsoft.com/library/72329821-32ff-495d-b6e5-fdc011003c2e%28Office.15%29.aspx) son tanto 04:00Z, que se convierte en la medianoche de la zona horaria Oriental durante el horario de verano.</span><span class="sxs-lookup"><span data-stu-id="0e9f7-130">Notice that the time portion of the values of the [Start](https://msdn.microsoft.com/library/7cfe9979-c893-4f9b-b3a1-8f9e17515a4b%28Office.15%29.aspx) and [End](https://msdn.microsoft.com/library/72329821-32ff-495d-b6e5-fdc011003c2e%28Office.15%29.aspx) elements are both 04:00Z, which converts to midnight in the Eastern time zone during daylight saving time.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
    xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
    xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
    xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
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

## <a name="see-also"></a><span data-ttu-id="0e9f7-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="0e9f7-131">See also</span></span>


- [<span data-ttu-id="0e9f7-132">Calendarios y EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="0e9f7-132">Calendars and EWS in Exchange</span></span>](calendars-and-ews-in-exchange.md)
    
- [<span data-ttu-id="0e9f7-133">Crear citas y reuniones mediante EWS en Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="0e9f7-133">Create appointments and meetings by using EWS in Exchange 2013</span></span>](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md)
    
- [<span data-ttu-id="0e9f7-134">Zonas horarias y EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="0e9f7-134">Time zones and EWS in Exchange</span></span>](time-zones-and-ews-in-exchange.md)
    

