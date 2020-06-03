---
title: Crear una serie periódica mediante EWS en Exchange
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 88ed6e87-25f7-4a54-83fa-d757a0ff2528
description: Obtenga información sobre cómo crear reuniones periódicas mediante la API administrada de EWS o EWS en Exchange.
ms.openlocfilehash: 1d04bd48c56a1a0e94eb1368166f776b3dfeb23a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44456874"
---
# <a name="create-a-recurring-series-by-using-ews-in-exchange"></a><span data-ttu-id="aa4a9-103">Crear una serie periódica mediante EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="aa4a9-103">Create a recurring series by using EWS in Exchange</span></span>

<span data-ttu-id="aa4a9-104">Obtenga información sobre cómo crear reuniones periódicas mediante la API administrada de EWS o EWS en Exchange.</span><span class="sxs-lookup"><span data-stu-id="aa4a9-104">Learn how to create recurring meetings by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="aa4a9-105">La creación de una cita o reunión periódica no es tan grande como la creación de [una reunión o cita de instancia única](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md).</span><span class="sxs-lookup"><span data-stu-id="aa4a9-105">Creating a recurring appointment or meeting isn't all that much different than creating [a single instance appointment or meeting](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md).</span></span> <span data-ttu-id="aa4a9-106">Solo tiene que asignar valores a algunas propiedades adicionales relacionadas con la periodicidad.</span><span class="sxs-lookup"><span data-stu-id="aa4a9-106">You just need to assign values to a few additional recurrence-related properties.</span></span> <span data-ttu-id="aa4a9-107">Se establecen en el objeto de [periodicidad](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.recurrence%28v=exchg.80%29.aspx) de un objeto [ExchangeService. appointment](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) (si está usando la API administrada de EWS) o en el elemento secundario de [periodicidad](https://msdn.microsoft.com/library/5f164e5b-47b6-4242-b6b9-8d650090a831%28Office.15%29.aspx) de un elemento [CalendarItem](https://msdn.microsoft.com/library/b0c1fd27-b6da-46e5-88b8-88f00c71ba80%28Office.15%29.aspx) (si está usando EWS).</span><span class="sxs-lookup"><span data-stu-id="aa4a9-107">These are set on an [ExchangeService.Appointment](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) object's [Recurrence](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.recurrence%28v=exchg.80%29.aspx) object (if you're using the EWS Managed API), or the [Recurrence](https://msdn.microsoft.com/library/5f164e5b-47b6-4242-b6b9-8d650090a831%28Office.15%29.aspx) child element of a [CalendarItem](https://msdn.microsoft.com/library/b0c1fd27-b6da-46e5-88b8-88f00c71ba80%28Office.15%29.aspx) element (if you're using EWS).</span></span> <span data-ttu-id="aa4a9-108">Un aspecto que se debe tener en cuenta al crear una reunión periódica, en lugar de una única instancia, es que el elemento de calendario que se crea es el maestro periódico de una serie.</span><span class="sxs-lookup"><span data-stu-id="aa4a9-108">One thing to consider when you create a recurring, rather than a single-instance meeting, is that the calendar item you create is the recurring master for a series.</span></span> <span data-ttu-id="aa4a9-109">Una serie de propiedades se establecen sólo en un patrón recurrente; Estas propiedades pueden ayudarle a buscar, modificar o eliminar instancias individuales de una serie.</span><span class="sxs-lookup"><span data-stu-id="aa4a9-109">A number of properties are set only on a recurring master; these properties can help you find, modify, or delete individual instances in a series.</span></span> <span data-ttu-id="aa4a9-110">Por este motivo, puede resultar útil realizar un seguimiento del identificador de la página maestra recurrente cuando se crea una serie periódica.</span><span class="sxs-lookup"><span data-stu-id="aa4a9-110">For this reason, it might be useful to keep track of the ID of the recurring master when you create a recurring series.</span></span> 
  
<span data-ttu-id="aa4a9-111">**Tabla 1. Propiedades establecidas en los elementos de calendario maestro periódico**</span><span class="sxs-lookup"><span data-stu-id="aa4a9-111">**Table 1. Properties set on recurring master calendar items**</span></span>

|<span data-ttu-id="aa4a9-112">**Clase o propiedad de la API administrada de EWS**</span><span class="sxs-lookup"><span data-stu-id="aa4a9-112">**EWS Managed API class or property**</span></span>|<span data-ttu-id="aa4a9-113">**Elemento XML EWS**</span><span class="sxs-lookup"><span data-stu-id="aa4a9-113">**EWS XML element**</span></span>|<span data-ttu-id="aa4a9-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="aa4a9-114">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="aa4a9-115">Clase recurrence</span><span class="sxs-lookup"><span data-stu-id="aa4a9-115">Recurrence class</span></span>](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.recurrence%28v=exchg.80%29.aspx) <br/> <span data-ttu-id="aa4a9-116">La clase **recurrence** es la clase base para una clase de patrón derivada, ya sea [IntervalPattern](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.recurrence.intervalpattern%28v=exchg.80%29.aspx), [RelativeYearlyPattern](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.recurrence.relativeyearlypattern%28v=exchg.80%29.aspx)o [YearlyPattern](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.recurrence.yearlypattern%28v=exchg.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="aa4a9-116">The **Recurrence** class is the base class for a derived pattern class, either [IntervalPattern](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.recurrence.intervalpattern%28v=exchg.80%29.aspx), [RelativeYearlyPattern](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.recurrence.relativeyearlypattern%28v=exchg.80%29.aspx), or [YearlyPattern](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.recurrence.yearlypattern%28v=exchg.80%29.aspx).</span></span>  <br/> |[<span data-ttu-id="aa4a9-117">Recurrence (RecurrenceType)</span><span class="sxs-lookup"><span data-stu-id="aa4a9-117">Recurrence (RecurrenceType)</span></span>](https://msdn.microsoft.com/library/3d1c2c1c-4103-47ce-ad3c-ad16ec6e9b12%28Office.15%29.aspx) <br/> |<span data-ttu-id="aa4a9-118">Contiene información relacionada con la periodicidad, incluido el patrón de periodicidad (diario, semanal, mensual, etc.), la fecha de inicio y de finalización, el número de repeticiones, etc.</span><span class="sxs-lookup"><span data-stu-id="aa4a9-118">Contains recurrence-related information, including the recurrence pattern (daily, weekly, monthly, and so on), start and end date, number of occurrences, and so on.</span></span>  <br/> |
|[<span data-ttu-id="aa4a9-119">Propiedad FirstOccurrence</span><span class="sxs-lookup"><span data-stu-id="aa4a9-119">FirstOccurrence property</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.firstoccurrence%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="aa4a9-120">FirstOccurrence</span><span class="sxs-lookup"><span data-stu-id="aa4a9-120">FirstOccurrence</span></span>](https://msdn.microsoft.com/library/d6748860-ce0d-4d2e-b7e4-9ed834f1e45a%28Office.15%29.aspx) <br/> |<span data-ttu-id="aa4a9-121">Contiene las horas de inicio y finalización, y el identificador de elemento de la primera reunión de una serie.</span><span class="sxs-lookup"><span data-stu-id="aa4a9-121">Contains the start and end times and the item ID for the first meeting in a series.</span></span>  <br/> |
|[<span data-ttu-id="aa4a9-122">Propiedad LastOccurrence</span><span class="sxs-lookup"><span data-stu-id="aa4a9-122">LastOccurrence property</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.lastoccurrence%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="aa4a9-123">LastOccurrence</span><span class="sxs-lookup"><span data-stu-id="aa4a9-123">LastOccurrence</span></span>](https://msdn.microsoft.com/library/c9ef0fcb-4265-4e60-9986-fff0f211d00b%28Office.15%29.aspx) <br/> |<span data-ttu-id="aa4a9-124">Contiene las horas de inicio y finalización, y el identificador de elemento de la última reunión de una serie.</span><span class="sxs-lookup"><span data-stu-id="aa4a9-124">Contains the start and end times and the item ID for the last meeting in a series.</span></span>  <br/> |
|[<span data-ttu-id="aa4a9-125">Propiedad ModifiedOccurrences</span><span class="sxs-lookup"><span data-stu-id="aa4a9-125">ModifiedOccurrences property</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.modifiedoccurrences%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="aa4a9-126">ModifiedOccurrences</span><span class="sxs-lookup"><span data-stu-id="aa4a9-126">ModifiedOccurrences</span></span>](https://msdn.microsoft.com/library/552932fc-b3b4-486e-8d73-32c0bb10bd68%28Office.15%29.aspx) <br/> |<span data-ttu-id="aa4a9-127">Contiene el conjunto de todas las reuniones de la serie que se han modificado desde el patrón de periodicidad original.</span><span class="sxs-lookup"><span data-stu-id="aa4a9-127">Contains the set of all meetings in the series that have been modified from the original recurrence pattern.</span></span>  <br/> |
|[<span data-ttu-id="aa4a9-128">Propiedad DeletedOccurrences</span><span class="sxs-lookup"><span data-stu-id="aa4a9-128">DeletedOccurrences property</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.deletedoccurrences%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="aa4a9-129">DeletedOccurrences</span><span class="sxs-lookup"><span data-stu-id="aa4a9-129">DeletedOccurrences</span></span>](https://msdn.microsoft.com/library/736fb305-9528-4be8-ad37-65d7556edbf2%28Office.15%29.aspx) <br/> |<span data-ttu-id="aa4a9-130">Contiene el conjunto de todas las reuniones de la serie que se han eliminado del patrón de periodicidad original.</span><span class="sxs-lookup"><span data-stu-id="aa4a9-130">Contains the set of all meetings in the series that have been deleted from the original recurrence pattern.</span></span>  <br/> |
   
<span data-ttu-id="aa4a9-131">Como las reuniones son esencialmente citas que incluyen asistentes, los ejemplos de código de este artículo muestran cómo crear reuniones periódicas.</span><span class="sxs-lookup"><span data-stu-id="aa4a9-131">Because meetings are essentially appointments that include attendees, the code examples in this article show how to create recurring meetings.</span></span> <span data-ttu-id="aa4a9-132">Si desea crear una cita periódica, puede modificar los ejemplos quitando el código relacionado con los asistentes.</span><span class="sxs-lookup"><span data-stu-id="aa4a9-132">If you want to create a recurring appointment, you can modify the examples by removing code related to attendees.</span></span>
  
## <a name="create-a-recurring-meeting-by-using-the-ews-managed-api"></a><span data-ttu-id="aa4a9-133">Crear una reunión periódica mediante la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="aa4a9-133">Create a recurring meeting by using the EWS Managed API</span></span>
<span data-ttu-id="aa4a9-134"><a name="bk_CreateMtgEWSMA"> </a></span><span class="sxs-lookup"><span data-stu-id="aa4a9-134"><a name="bk_CreateMtgEWSMA"> </a></span></span>

<span data-ttu-id="aa4a9-135">En el ejemplo de código siguiente se muestra cómo crear una reunión periódica.</span><span class="sxs-lookup"><span data-stu-id="aa4a9-135">The following code example shows how to create a recurring meeting.</span></span> <span data-ttu-id="aa4a9-136">En primer lugar, asigne valores a las propiedades de un [objeto de cita](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) que se usa para crear una reunión y, a continuación, utilice el método [Save](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.save%28v=exchg.80%29.aspx) para guardar la serie periódica en la carpeta del calendario y enviar las convocatorias de reunión a los asistentes.</span><span class="sxs-lookup"><span data-stu-id="aa4a9-136">First, assign values to the properties of an [Appointment object](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) used to create a meeting, then use the [Save](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.save%28v=exchg.80%29.aspx) method to save the recurring series to your calendar folder, and send meeting requests to your attendees.</span></span> <span data-ttu-id="aa4a9-137">Por último, use el método [appointment. bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) para ver los valores establecidos en el maestro periódico de la serie periódica que acaba de crear.</span><span class="sxs-lookup"><span data-stu-id="aa4a9-137">Finally, use the [Appointment.Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) method to look at the values set on the recurring master for the recurring series you just created.</span></span> 
  
<span data-ttu-id="aa4a9-138">En este ejemplo se supone que se ha autenticado en un servidor de Exchange y que se ha adquirido un objeto [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) denominado **Service**.</span><span class="sxs-lookup"><span data-stu-id="aa4a9-138">This example assumes that you have authenticated to an Exchange server and have acquired an [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object named **service**.</span></span> <span data-ttu-id="aa4a9-139">El método de este ejemplo devuelve el [identificador de elemento](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) de la serie periódica "maestro periódico.</span><span class="sxs-lookup"><span data-stu-id="aa4a9-139">The method in this example returns the [item ID](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) of the recurring series' recurring master.</span></span> 
  
```cs
public static ItemId CreateARecurringMeeting(ExchangeService service)
{        Appointment recurrMeeting = new Appointment(service);
        // Set the properties you need to create a meeting.
        recurrMeeting.Subject = "Weekly Update Meeting";
        recurrMeeting.Body = "Come hear about how the project is coming along!";
        recurrMeeting.Start = DateTime.Now.AddDays(1);
        recurrMeeting.End = recurrMeeting.Start.AddHours(1);
        recurrMeeting.Location = "Contoso Main Gallery";
        recurrMeeting.RequiredAttendees.Add("Mack@contoso.com");
        recurrMeeting.RequiredAttendees.Add("Sadie@contoso.com");
        recurrMeeting.RequiredAttendees.Add("Magdalena@contoso.com"); recurrMeeting.ReminderMinutesBeforeStart = 30;
             
        DayOfTheWeek[] dow = new DayOfTheWeek[] { (DayOfTheWeek)recurrMeeting.Start.DayOfWeek };
        // The following are the recurrence-specific properties for the meeting.
        recurrMeeting.Recurrence = new Recurrence.WeeklyPattern(recurrMeeting.Start.Date, 1, dow);
        recurrMeeting.Recurrence.StartDate = recurrMeeting.Start.Date;
        recurrMeeting.Recurrence.NumberOfOccurrences = 10;
        // This method results in in a CreateItem call to EWS.
        recurrMeeting.Save(SendInvitationsMode.SendToAllAndSaveCopy);
        // Retrieve the meeting subject and the properties that are set on a recurring master when a recurring series is created.
        recurrMeeting = Appointment.Bind(service, recurrMeeting.Id, new PropertySet(AppointmentSchema.Subject,
                                                                                    AppointmentSchema.AppointmentType, 
                                                                                    AppointmentSchema.Recurrence, 
                                                                                    AppointmentSchema.FirstOccurrence,
                                                                                    AppointmentSchema.LastOccurrence,
                                                                                    AppointmentSchema.ModifiedOccurrences,
                                                                                    AppointmentSchema.DeletedOccurrences));
        // Print out the recurring master properties.
        Console.WriteLine("\nAppointment created: " + recurrMeeting.Subject);
        Console.WriteLine("Appointment Type: {0}\n", recurrMeeting.AppointmentType);
        Console.WriteLine("These property values are always null unless the item is a recurring master:\n");
        Console.WriteLine("\tRecurrence pattern: {0}", recurrMeeting.Recurrence.ToString());
        Console.WriteLine("\tRecurring series start Date: {0}", recurrMeeting.Recurrence.StartDate.ToString());
        Console.WriteLine("\tRecurring series end Date: {0}", 
                        recurrMeeting.Recurrence.EndDate == null ? "Null" : recurrMeeting.Recurrence.EndDate.ToString());
        Console.WriteLine("\tHas end: {0}", recurrMeeting.Recurrence.HasEnd.ToString());
        Console.WriteLine("\tNumber of occurrances: {0}", recurrMeeting.Recurrence.NumberOfOccurrences);
        Console.WriteLine("\tLast 24 characters of the first occurrence's item ID:\t {0}", 
                        recurrMeeting.FirstOccurrence.ItemId.ToString().Substring(144));
        Console.WriteLine("\tLast 24 characters of the last occurrence's item ID:\t {0}", 
                        recurrMeeting.LastOccurrence.ItemId.ToString().Substring(144)); 
        Console.WriteLine("\tModified Occurrences: {0}", 
                        (recurrMeeting.ModifiedOccurrences == null ? "Null" : recurrMeeting.ModifiedOccurrences.Count.ToString()));
        Console.WriteLine("\tDeleted Occurrences: {0}", 
                        recurrMeeting.DeletedOccurrences == null ? "Null" : recurrMeeting.ModifiedOccurrences.Count.ToString());
        // Return the ID of the recurring master.
        return recurrMeeting.Id;
}

```

## <a name="create-a-recurring-meeting-by-using-ews"></a><span data-ttu-id="aa4a9-140">Crear una reunión periódica con EWS</span><span class="sxs-lookup"><span data-stu-id="aa4a9-140">Create a recurring meeting by using EWS</span></span>
<span data-ttu-id="aa4a9-141"><a name="bk_CreateMtgEWS"> </a></span><span class="sxs-lookup"><span data-stu-id="aa4a9-141"><a name="bk_CreateMtgEWS"> </a></span></span>

<span data-ttu-id="aa4a9-142">El XML de solicitud y respuesta de los ejemplos siguientes corresponden a las llamadas realizadas para [crear una reunión periódica mediante la API administrada de EWS](#bk_CreateMtgEWSMA).</span><span class="sxs-lookup"><span data-stu-id="aa4a9-142">The request and response XML in the following examples correspond to calls made to [create a recurring meeting by using the EWS Managed API](#bk_CreateMtgEWSMA).</span></span> <span data-ttu-id="aa4a9-143">Tenga en cuenta que, además de establecer valores específicos de periodicidad en el elemento de [periodicidad](https://msdn.microsoft.com/library/5f164e5b-47b6-4242-b6b9-8d650090a831%28Office.15%29.aspx) , la solicitud es esencialmente la misma que la que se usaría para crear una cita de instancia única.</span><span class="sxs-lookup"><span data-stu-id="aa4a9-143">Note that other than setting recurrence-specific values on the [Recurrence](https://msdn.microsoft.com/library/5f164e5b-47b6-4242-b6b9-8d650090a831%28Office.15%29.aspx) element, the request is essentially the same as one you would use to create a single-instance appointment.</span></span> <span data-ttu-id="aa4a9-144">En el ejemplo siguiente se muestra el XML de la solicitud cuando se utiliza la operación [CreateItem](https://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) para crear una reunión.</span><span class="sxs-lookup"><span data-stu-id="aa4a9-144">The following example shows the request XML when you use the [CreateItem](https://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) operation to create a meeting.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2010" />
    <t:TimeZoneContext>
      <t:TimeZoneDefinition Name="(UTC-08:00) Pacific Time (US &amp;amp; Canada)" Id="Pacific Standard Time">
        <t:Periods>
          <t:Period Bias="P0DT8H0M0.0S" Name="Standard" Id="Std" />
          <t:Period Bias="P0DT7H0M0.0S" Name="Daylight" Id="Dlt/1" />
          <t:Period Bias="P0DT7H0M0.0S" Name="Daylight" Id="Dlt/2007" />
        </t:Periods>
        <t:TransitionsGroups>
          <t:TransitionsGroup Id="0">
            <t:RecurringDayTransition>
              <t:To Kind="Period">Dlt/1</t:To>
              <t:TimeOffset>P0DT2H0M0.0S</t:TimeOffset>
              <t:Month>4</t:Month>
              <t:DayOfWeek>Sunday</t:DayOfWeek>
              <t:Occurrence>1</t:Occurrence>
            </t:RecurringDayTransition>
            <t:RecurringDayTransition>
              <t:To Kind="Period">Std</t:To>
              <t:TimeOffset>P0DT2H0M0.0S</t:TimeOffset>
              <t:Month>10</t:Month>
              <t:DayOfWeek>Sunday</t:DayOfWeek>
              <t:Occurrence>-1</t:Occurrence>
            </t:RecurringDayTransition>
          </t:TransitionsGroup>
          <t:TransitionsGroup Id="1">
            <t:RecurringDayTransition>
              <t:To Kind="Period">Dlt/2007</t:To>
              <t:TimeOffset>P0DT2H0M0.0S</t:TimeOffset>
              <t:Month>3</t:Month>
              <t:DayOfWeek>Sunday</t:DayOfWeek>
              <t:Occurrence>2</t:Occurrence>
            </t:RecurringDayTransition>
            <t:RecurringDayTransition>
              <t:To Kind="Period">Std</t:To>
              <t:TimeOffset>P0DT2H0M0.0S</t:TimeOffset>
              <t:Month>11</t:Month>
              <t:DayOfWeek>Sunday</t:DayOfWeek>
              <t:Occurrence>1</t:Occurrence>
            </t:RecurringDayTransition>
          </t:TransitionsGroup>
        </t:TransitionsGroups>
        <t:Transitions>
          <t:Transition>
            <t:To Kind="Group">0</t:To>
          </t:Transition>
          <t:AbsoluteDateTransition>
            <t:To Kind="Group">1</t:To>
            <t:DateTime>2007-01-01T08:00:00.000Z</t:DateTime>
          </t:AbsoluteDateTransition>
        </t:Transitions>
      </t:TimeZoneDefinition>
    </t:TimeZoneContext>
  </soap:Header>
  <soap:Body>
    <m:CreateItem SendMeetingInvitations="SendToAllAndSaveCopy">
      <m:Items>
        <t:CalendarItem>
          <t:Subject>Weekly Update Meeting</t:Subject>
          <t:Body BodyType="HTML">Come hear about how the Organized Observational Paradigm SkyNet project is coming along!</t:Body>
          <t:ReminderMinutesBeforeStart>30</t:ReminderMinutesBeforeStart>
          <t:Start>2014-03-08T13:21:32.868-08:00</t:Start>
          <t:End>2014-03-08T14:21:32.868-08:00</t:End>
          <t:Location>Contoso Main Gallery</t:Location>
          <t:RequiredAttendees>
            <t:Attendee>
              <t:Mailbox>
                <t:EmailAddress>Mack@contoso.com</t:EmailAddress>
              </t:Mailbox>
            </t:Attendee>
            <t:Attendee>
              <t:Mailbox>
                <t:EmailAddress>Sadie@contoso.com</t:EmailAddress>
              </t:Mailbox>
            </t:Attendee>
            <t:Attendee>
              <t:Mailbox>
                <t:EmailAddress>Magdalena@contoso.com</t:EmailAddress>
              </t:Mailbox>
            </t:Attendee>
          </t:RequiredAttendees>
          <t:Recurrence>
            <t:WeeklyRecurrence>
              <t:Interval>1</t:Interval>
              <t:DaysOfWeek>Saturday</t:DaysOfWeek>
            </t:WeeklyRecurrence>
            <t:NumberedRecurrence>
              <t:StartDate>2014-03-08-08:00</t:StartDate>
              <t:NumberOfOccurrences>10</t:NumberOfOccurrences>
            </t:NumberedRecurrence>
          </t:Recurrence>
        </t:CalendarItem>
      </m:Items>
    </m:CreateItem>
  </soap:Body>
</soap:Envelope>

```

 <span data-ttu-id="aa4a9-145">En el ejemplo siguiente se muestra el XML de respuesta que devuelve la operación **CreateItem** .</span><span class="sxs-lookup"><span data-stu-id="aa4a9-145">The following example shows the response XML that is returned by the **CreateItem** operation.</span></span> 
  
<span data-ttu-id="aa4a9-146">Los atributos **Itemid** y **changekey** se acortan para facilitar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="aa4a9-146">The **ItemId** and **ChangeKey** attributes are shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="893" MinorBuildNumber="10" 
                         Version="V2_10" xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:CreateItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:CreateItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Items>
            <t:CalendarItem>
              <t:ItemId Id="AAMkAD" ChangeKey="DwAAAB" />
            </t:CalendarItem>
          </m:Items>
        </m:CreateItemResponseMessage>
      </m:ResponseMessages>
    </m:CreateItemResponse>
  </s:Body>
</s:Envelope>

```

<span data-ttu-id="aa4a9-147">En el ejemplo siguiente se muestra el XML de la solicitud que se genera cuando se usa la operación [GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) y la **Itemid** para la serie que ha creado, y las propiedades de solicitud solo se establecen en un patrón recurrente para confirmar que el **Itemid** devuelto por el servidor al crear una serie periódica es para un maestro recurrente.</span><span class="sxs-lookup"><span data-stu-id="aa4a9-147">The following example shows the request XML that is generated when you use the [GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) operation and the **ItemId** for the series you created, and request properties only set on a recurring master to confirm that the **ItemId** returned by the server when creating a recurring series is for a recurring master.</span></span> 
  
<span data-ttu-id="aa4a9-148">Los atributos **Itemid** y **changekey** se acortan para facilitar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="aa4a9-148">The **ItemId** and **ChangeKey** attributes are shortened for readability.</span></span> 
  
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
    <m:GetItem>
      <m:ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="item:Subject" />
          <t:FieldURI FieldURI="calendar:CalendarItemType" />
          <t:FieldURI FieldURI="calendar:Recurrence" />
          <t:FieldURI FieldURI="calendar:FirstOccurrence" />
          <t:FieldURI FieldURI="calendar:LastOccurrence" />
          <t:FieldURI FieldURI="calendar:ModifiedOccurrences" />
          <t:FieldURI FieldURI="calendar:DeletedOccurrences" />
        </t:AdditionalProperties>
      </m:ItemShape>
      <m:ItemIds>
        <t:ItemId Id="AAMkAD" ChangeKey="DwAAAB" />
      </m:ItemIds>
    </m:GetItem>
  </soap:Body>
</soap:Envelope>

```

 <span data-ttu-id="aa4a9-149">En el ejemplo siguiente se muestra el XML de respuesta que devuelve la operación **GetItem** .</span><span class="sxs-lookup"><span data-stu-id="aa4a9-149">The following example shows the response XML that is returned by the **GetItem** operation.</span></span> 
  
<span data-ttu-id="aa4a9-150">Los atributos **Itemid** y **changekey** se acortan para facilitar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="aa4a9-150">The **ItemId** and **ChangeKey** attributes are shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="893" MinorBuildNumber="10" 
                         Version="V2_10" xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                       xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:GetItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Items>
            <t:CalendarItem>
              <t:ItemId Id="AAMkAD" ChangeKey="DwAAAB" />
              <t:Subject>Weekly Update Meeting</t:Subject>
              <t:CalendarItemType>RecurringMaster</t:CalendarItemType>
              <t:Recurrence>
                <t:WeeklyRecurrence>
                  <t:Interval>1</t:Interval>
                  <t:DaysOfWeek>Saturday</t:DaysOfWeek>
                </t:WeeklyRecurrence>
                <t:NumberedRecurrence>
                  <t:StartDate>2014-03-08-08:00</t:StartDate>
                  <t:NumberOfOccurrences>10</t:NumberOfOccurrences>
                </t:NumberedRecurrence>
              </t:Recurrence>
              <t:FirstOccurrence>
                <t:ItemId Id="AAMkAD" ChangeKey="DwAAABY" />
                <t:Start>2014-03-08T21:21:00Z</t:Start>
                <t:End>2014-03-08T22:21:00Z</t:End>
                <t:OriginalStart>2014-03-08T21:21:00Z</t:OriginalStart>
              </t:FirstOccurrence>
              <t:LastOccurrence>
                <t:ItemId Id="AAMkAD" ChangeKey="DwAAABY" />
                <t:Start>2014-05-10T20:21:00Z</t:Start>
                <t:End>2014-05-10T21:21:00Z</t:End>
                <t:OriginalStart>2014-05-10T20:21:00Z</t:OriginalStart>
              </t:LastOccurrence>
            </t:CalendarItem>
          </m:Items>
        </m:GetItemResponseMessage>
      </m:ResponseMessages>
    </m:GetItemResponse>
  </s:Body>
</s:Envelope>

```

## <a name="see-also"></a><span data-ttu-id="aa4a9-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="aa4a9-151">See also</span></span>


- [<span data-ttu-id="aa4a9-152">Calendarios y EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="aa4a9-152">Calendars and EWS in Exchange</span></span>](calendars-and-ews-in-exchange.md)
    
- [<span data-ttu-id="aa4a9-153">Crear citas y reuniones mediante EWS en Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="aa4a9-153">Create appointments and meetings by using EWS in Exchange 2013</span></span>](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md)
    
- [<span data-ttu-id="aa4a9-154">Patrones de periodicidad y EWS</span><span class="sxs-lookup"><span data-stu-id="aa4a9-154">Recurrence patterns and EWS</span></span>](recurrence-patterns-and-ews.md)
    
- [<span data-ttu-id="aa4a9-155">Obtener acceso a una serie periódica mediante EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="aa4a9-155">Access a recurring series by using EWS in Exchange</span></span>](how-to-access-a-recurring-series-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="aa4a9-156">Eliminar citas en una serie periódica mediante EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="aa4a9-156">Delete appointments in a recurring series by using EWS in Exchange</span></span>](how-to-delete-appointments-in-a-recurring-series-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="aa4a9-157">Actualizar una serie periódica mediante EWS</span><span class="sxs-lookup"><span data-stu-id="aa4a9-157">Update a recurring series by using EWS</span></span>](how-to-update-a-recurring-series-by-using-ews.md)
    
- [<span data-ttu-id="aa4a9-158">Actualizar una serie periódica mediante EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="aa4a9-158">Update a recurring series by using EWS in Exchange</span></span>](how-to-update-a-recurring-series-by-using-ews-in-exchange.md)
    

