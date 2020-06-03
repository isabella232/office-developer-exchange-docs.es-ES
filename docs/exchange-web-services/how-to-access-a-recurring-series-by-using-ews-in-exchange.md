---
title: Obtener acceso a una serie periódica mediante EWS en Exchange
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 196a5671-2836-4696-b734-d5ecfdbf8962
description: Obtenga información sobre cómo acceder a los elementos de calendario en una serie periódica mediante la API administrada de EWS o EWS en Exchange.
ms.openlocfilehash: dca41472b3b2f775f420b6654d7e43ef456b0583
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44456895"
---
# <a name="access-a-recurring-series-by-using-ews-in-exchange"></a><span data-ttu-id="16d4d-103">Obtener acceso a una serie periódica mediante EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="16d4d-103">Access a recurring series by using EWS in Exchange</span></span>

<span data-ttu-id="16d4d-104">Obtenga información sobre cómo acceder a los elementos de calendario en una serie periódica mediante la API administrada de EWS o EWS en Exchange.</span><span class="sxs-lookup"><span data-stu-id="16d4d-104">Learn how to access calendar items in a recurring series by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="16d4d-105">Una serie periódica de citas o reuniones está formada por un maestro recurrente, un número de repeticiones en una serie que se repiten según un patrón establecido y, opcionalmente, conjuntos de ocurrencias que se han cambiado y que se han eliminado.</span><span class="sxs-lookup"><span data-stu-id="16d4d-105">A recurring series of appointments or meetings is made up of a recurring master, a number of occurrences in a series that repeat according to a set pattern, and, optionally, sets of occurrences that were changed and that were deleted.</span></span> <span data-ttu-id="16d4d-106">Puede usar la API administrada de EWS o EWS para tener acceso a los elementos de calendario en una serie periódica.</span><span class="sxs-lookup"><span data-stu-id="16d4d-106">You can use the EWS Managed API or EWS to access calendar items in a recurring series.</span></span> <span data-ttu-id="16d4d-107">Esto le permite:</span><span class="sxs-lookup"><span data-stu-id="16d4d-107">This enables you to:</span></span>
  
- <span data-ttu-id="16d4d-108">Compruebe si un elemento de calendario asociado con un identificador de elemento es un patrón periódico, una ocurrencia en una serie o una excepción a una serie.</span><span class="sxs-lookup"><span data-stu-id="16d4d-108">Check to see if a calendar item associated with an item ID is a recurring master, an occurrence in a series, or an exception to a series.</span></span>
    
- <span data-ttu-id="16d4d-109">Busque citas periódicas en su carpeta de calendario.</span><span class="sxs-lookup"><span data-stu-id="16d4d-109">Search your calendar folder for recurrence appointments.</span></span>
    
- <span data-ttu-id="16d4d-110">Obtener elementos de calendario de periodicidad relacionados</span><span class="sxs-lookup"><span data-stu-id="16d4d-110">Get related recurrence calendar items</span></span>
    
- <span data-ttu-id="16d4d-111">Recorrer en iteración las ocurrencias de una serie, excepciones de ocurrencia o eliminaciones de ocurrencia.</span><span class="sxs-lookup"><span data-stu-id="16d4d-111">Iterate through occurrences in a series, occurrence exceptions, or occurrence deletions.</span></span>
    
## <a name="get-a-collection-of-recurring-calendar-items-by-using-the-ews-managed-api"></a><span data-ttu-id="16d4d-112">Obtener una colección de elementos de calendario periódicos mediante la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="16d4d-112">Get a collection of recurring calendar items by using the EWS Managed API</span></span>

<span data-ttu-id="16d4d-113">Si desea recuperar una colección de citas, puede usar el método [ExchangeService. FindAppointments](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice.findappointments%28v=exchg.80%29.aspx) para recuperar todas las citas entre una fecha de inicio y una fecha de finalización determinada y, a continuación, agregar todos los elementos del calendario con un tipo de cita **ocurrencia** o una **excepción** a una colección, como se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="16d4d-113">If you want to retrieve a collection of appointments, you can use the [ExchangeService.FindAppointments](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice.findappointments%28v=exchg.80%29.aspx) method to retrieve all appointments between a given start and end date, and then add all calendar items with an appointment type of **Occurrence** or **Exception** to a collection, as shown in the following example.</span></span> 
  
<span data-ttu-id="16d4d-114">En este ejemplo se supone que se ha autenticado en un servidor de Exchange y que se ha adquirido un objeto [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) denominado **Service**.</span><span class="sxs-lookup"><span data-stu-id="16d4d-114">This example assumes that you have authenticated to an Exchange server and have acquired an [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object named **service**.</span></span> 
  
```cs
public static Collection<Appointment> FindRecurringCalendarItems(ExchangeService service, 
                                                                    DateTime startSearchDate, 
                                                                    DateTime endSearchDate)
{
    // Instantiate a collection to hold occurrences and exception calendar items.
    Collection<Appointment> foundAppointments = new Collection<Appointment>();
    // Create a calendar view to search the calendar folder and specify the properties to return.
    CalendarView calView = new CalendarView(startSearchDate, endSearchDate);
    calView.PropertySet = new PropertySet(BasePropertySet.IdOnly, 
                                            AppointmentSchema.Subject, 
                                            AppointmentSchema.Start, 
                                            AppointmentSchema.IsRecurring, 
                                            AppointmentSchema.AppointmentType);
    // Retrieve a collection of calendar items.
    FindItemsResults<Appointment> findResults = service.FindAppointments(WellKnownFolderName.Calendar, calView);
    // Add all calendar items in your view that are occurrences or exceptions to your collection.
    foreach (Appointment appt in findResults.Items)
    {
        if (appt.AppointmentType == AppointmentType.Occurrence || appt.AppointmentType == AppointmentType.Exception)
        {
            foundAppointments.Add(appt);
        }
        else
        {
            Console.WriteLine("Discarding calendar item of type {0}.", appt.AppointmentType);
        }
    }
    return foundAppointments;
}

```

<span data-ttu-id="16d4d-115">Tenga en cuenta que los elementos de calendario maestro periódicos no se devuelven en una llamada a **FindAppointments**.</span><span class="sxs-lookup"><span data-stu-id="16d4d-115">Note that recurring master calendar items aren't returned in a call to **FindAppointments**.</span></span> <span data-ttu-id="16d4d-116">Si desea recuperar los patrones recurrentes o si desea un enfoque más general para recuperar elementos de calendario, debe usar [ExchangeService. FindItems](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="16d4d-116">If you want to retrieve recurring masters, or you want a more general approach to retrieving calendar items, you need to use [ExchangeService.FindItems](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx).</span></span> <span data-ttu-id="16d4d-117">A continuación, puede usar un filtro de búsqueda para recuperar sólo los elementos con una fecha de comienzo mayor o igual que la fecha elegida, así como una vista de elemento para limitar el número de elementos que se van a devolver.</span><span class="sxs-lookup"><span data-stu-id="16d4d-117">You can then use a search filter to retrieve only items with a start date greater than or equal to a date you choose, and an item view to limit the number of items to return.</span></span> <span data-ttu-id="16d4d-118">Tenga en cuenta que no se encontrará un patrón recurrente con una fecha de inicio anterior a la fecha de inicio de la búsqueda, aunque se produzcan repeticiones en este intervalo.</span><span class="sxs-lookup"><span data-stu-id="16d4d-118">Note that a recurring master with a start date earlier than the start date in your search will not be found, even if occurrences occur in this range.</span></span>
  
<span data-ttu-id="16d4d-119">En este ejemplo se supone que se ha autenticado en un servidor de Exchange y que se ha adquirido un objeto [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) denominado **Service**.</span><span class="sxs-lookup"><span data-stu-id="16d4d-119">This example assumes that you have authenticated to an Exchange server and have acquired an [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object named **service**.</span></span> 
  
```cs
public static Collection<Appointment> FindCalendarItemsByAppointmentType(ExchangeService service, 
                                                                         AppointmentType myAppointmentType, 
                                                                         DateTime startSearchDate)
{
    Collection<Appointment> foundAppointments = new Collection<Appointment>();
    // Create a search filter based on the start search date.
    SearchFilter.SearchFilterCollection searchFilter = new SearchFilter.SearchFilterCollection();
    searchFilter.Add(new SearchFilter.IsGreaterThanOrEqualTo(AppointmentSchema.Start, startSearchDate));
    // Create an item view to specify which properties to return.
    ItemView view = new ItemView(20);
    view.PropertySet = new PropertySet(BasePropertySet.IdOnly, 
                                       AppointmentSchema.Subject, 
                                       AppointmentSchema.Start, 
                                       AppointmentSchema.AppointmentType,
                                       AppointmentSchema.IsRecurring);
    // Get the appointment items from the server with the properties we specified.
    FindItemsResults<Item> findResults = service.FindItems(WellKnownFolderName.Calendar, searchFilter, view);
    // Add each of the appointments of the type you want to the collection.
    foreach (Item item in findResults.Items)
    {
        Appointment appt = item as Appointment;
        if (appt.AppointmentType == myAppointmentType)
        {
            foundAppointments.Add(appt);
        }
    }
    return foundAppointments;
}

```

## <a name="get-related-recurrence-calendar-items-by-using-the-ews-managed-api"></a><span data-ttu-id="16d4d-120">Obtener elementos de calendario de periodicidad relacionados mediante la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="16d4d-120">Get related recurrence calendar items by using the EWS Managed API</span></span>

<span data-ttu-id="16d4d-121">A veces tiene una pieza del rompecabezas, pero para solucionarlo necesita el resto de las piezas.</span><span class="sxs-lookup"><span data-stu-id="16d4d-121">Sometimes you have one piece of the puzzle, but to solve it you need the rest of the pieces.</span></span> <span data-ttu-id="16d4d-122">Si tiene el identificador de elemento para un elemento de calendario de periodicidad, puede obtener las otras partes que necesita mediante uno de varios métodos o propiedades de la API administrada de EWS.</span><span class="sxs-lookup"><span data-stu-id="16d4d-122">If you have the item ID for a recurrence calendar item, you can get the other pieces you need by using one of several EWS Managed API properties or methods.</span></span>
  
<span data-ttu-id="16d4d-123">**Tabla 1. Método o propiedad de la API administrada EWS que se va a usar para obtener los elementos de calendario de periodicidad relacionados**</span><span class="sxs-lookup"><span data-stu-id="16d4d-123">**Table 1. EWS Managed API property or method to use to get related recurrence calendar items**</span></span>

|<span data-ttu-id="16d4d-124">**Si tiene el identificador de elemento para...**</span><span class="sxs-lookup"><span data-stu-id="16d4d-124">**If you have the item ID for…**</span></span>|<span data-ttu-id="16d4d-125">**Puede obtener...**</span><span class="sxs-lookup"><span data-stu-id="16d4d-125">**You can get…**</span></span>|<span data-ttu-id="16d4d-126">**Mediante el uso del...**</span><span class="sxs-lookup"><span data-stu-id="16d4d-126">**By using the…**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="16d4d-127">El elemento de calendario maestro periódico</span><span class="sxs-lookup"><span data-stu-id="16d4d-127">The recurring master calendar item</span></span>  <br/> | <span data-ttu-id="16d4d-128">La primera aparición en una serie</span><span class="sxs-lookup"><span data-stu-id="16d4d-128">The first occurrence in a series</span></span>  <br/>  <span data-ttu-id="16d4d-129">La última aparición en una serie</span><span class="sxs-lookup"><span data-stu-id="16d4d-129">The last occurrence in a series</span></span>  <br/>  <span data-ttu-id="16d4d-130">Las excepciones a una serie</span><span class="sxs-lookup"><span data-stu-id="16d4d-130">The exceptions to a series</span></span>  <br/>  <span data-ttu-id="16d4d-131">Las citas eliminadas en una serie</span><span class="sxs-lookup"><span data-stu-id="16d4d-131">The deleted appointments in a series</span></span>  <br/>  <span data-ttu-id="16d4d-132">Cualquier aparición (según su índice)</span><span class="sxs-lookup"><span data-stu-id="16d4d-132">Any occurrence (given its index)</span></span>  <br/> |<span data-ttu-id="16d4d-133">Propiedad [appointment. FirstOccurrence](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.firstoccurrence%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="16d4d-133">[Appointment.FirstOccurrence](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.firstoccurrence%28v=exchg.80%29.aspx) property</span></span>  <br/> <span data-ttu-id="16d4d-134">Propiedad [appointment. LastOccurrence](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.lastoccurrence%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="16d4d-134">[Appointment.LastOccurrence](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.lastoccurrence%28v=exchg.80%29.aspx) property</span></span>  <br/> <span data-ttu-id="16d4d-135">Propiedad [appointment. ModifiedOccurrences](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.modifiedoccurrences%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="16d4d-135">[Appointment.ModifiedOccurrences](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.modifiedoccurrences%28v=exchg.80%29.aspx) property</span></span>  <br/> <span data-ttu-id="16d4d-136">Propiedad [appointment. DeletedOccurrences](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.deletedoccurrences%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="16d4d-136">[Appointment.DeletedOccurrences](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.deletedoccurrences%28v=exchg.80%29.aspx) property</span></span>  <br/> <span data-ttu-id="16d4d-137">Método [appointment. BindToOccurrence](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.appointment.bindtooccurrence%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="16d4d-137">[Appointment.BindToOccurrence](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.appointment.bindtooccurrence%28v=exchg.80%29.aspx) method</span></span>  <br/> |
|<span data-ttu-id="16d4d-138">Una sola ocurrencia en una serie</span><span class="sxs-lookup"><span data-stu-id="16d4d-138">A single occurrence in a series</span></span>  <br/> |<span data-ttu-id="16d4d-139">El patrón recurrente</span><span class="sxs-lookup"><span data-stu-id="16d4d-139">The recurring master</span></span>  <br/> |<span data-ttu-id="16d4d-140">Método [appointment. BindToRecurringMaster](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.appointment.bindtorecurringmaster%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="16d4d-140">[Appointment.BindToRecurringMaster](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.appointment.bindtorecurringmaster%28v=exchg.80%29.aspx) method</span></span>  <br/> |
|<span data-ttu-id="16d4d-141">Cualquier elemento de calendario (un objeto de [cita](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) )</span><span class="sxs-lookup"><span data-stu-id="16d4d-141">Any calendar item (an [Appointment](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) object)</span></span>  <br/> |<span data-ttu-id="16d4d-142">El valor de enumeración de [tipo de cita](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.appointmenttype%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="16d4d-142">The [appointment type](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.appointmenttype%28v=exchg.80%29.aspx) enumeration value</span></span>  <br/> |<span data-ttu-id="16d4d-143">Propiedad [appointment. AppointmentType](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.appointment.appointmenttype%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="16d4d-143">[Appointment.AppointmentType](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.appointment.appointmenttype%28v=exchg.80%29.aspx) property</span></span>  <br/> |
   
<span data-ttu-id="16d4d-144">En el ejemplo de código siguiente se muestra cómo obtener un patrón recurrente, la primera o la última aparición en una serie o una ocurrencia dada su índice.</span><span class="sxs-lookup"><span data-stu-id="16d4d-144">The following code example shows how to get a recurring master, the first or last occurrence in a series, or an occurrence given its index.</span></span>
  
<span data-ttu-id="16d4d-145">En este ejemplo se supone que se ha autenticado en un servidor de Exchange y que se ha adquirido un objeto [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) denominado **Service**.</span><span class="sxs-lookup"><span data-stu-id="16d4d-145">This example assumes that you have authenticated to an Exchange server and have acquired an [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object named **service**.</span></span> 
  
```cs
public static void GetRelatedRecurrenceCalendarItems(ExchangeService service, ItemId itemId)
{
    Appointment calendarItem = Appointment.Bind(service, itemId, new PropertySet(AppointmentSchema.AppointmentType));
    Appointment recurrMaster = new Appointment(service);
    PropertySet props = new PropertySet(AppointmentSchema.AppointmentType,
                                        AppointmentSchema.Subject,
                                        AppointmentSchema.FirstOccurrence,
                                        AppointmentSchema.LastOccurrence,
                                        AppointmentSchema.ModifiedOccurrences,
                                        AppointmentSchema.DeletedOccurrences);
    // If the item ID is not for a recurring master, retrieve the recurring master for the series.
    switch (calendarItem.AppointmentType)
    {
        // Calendar item is a recurring master so use Appointment.Bind
        case AppointmentType.RecurringMaster:
            recurrMaster = Appointment.Bind(service, itemId, props);
            break;
        // The calendar item is a single instance meeting, so there are no instances to modify or delete.
        case AppointmentType.Single:
            Console.WriteLine("Item id must reference a calendar item that is part of a recurring series.");
            return;
        // The calendar item is an occurrence in the series, so use BindToRecurringMaster.
        case AppointmentType.Occurrence:
            recurrMaster = Appointment.BindToRecurringMaster(service, itemId, props);
            break;
        // The calendar item is an exception to the series, so use BindToRecurringMaster.                
        case AppointmentType.Exception:
            recurrMaster = Appointment.BindToRecurringMaster(service, itemId, props);
            break;
    }
    // View the first occurrence, last occurrence, and number of modified and deleted occurrences associated with the recurring master.
    Console.WriteLine("Information for the {0} recurring series:", recurrMaster.Subject);
    Console.WriteLine("The start time for the first appointment with id \t{0} was on \t{1}.", 
                        recurrMaster.FirstOccurrence.ItemId.ToString().Substring(144), 
                        recurrMaster.FirstOccurrence.Start.ToString());
    Console.WriteLine("The start time for the last appointment with id \t{0} will be on \t{1}.", 
                        recurrMaster.LastOccurrence.ItemId.ToString().Substring(144), 
                        recurrMaster.LastOccurrence.Start.ToString());
    Console.WriteLine("There are {0} modified occurrences and {1} deleted occurrences.", 
                        recurrMaster.ModifiedOccurrences == null ? "no" : recurrMaster.ModifiedOccurrences.Count.ToString(), 
                        recurrMaster.DeletedOccurrences == null ? "no" : recurrMaster.DeletedOccurrences.Count.ToString());
    // Bind to the first occurrence of a series by using its index.
    Appointment firstOccurrence = Appointment.BindToOccurrence(service, 
                                                                recurrMaster.Id, 
                                                                1, // Index of first item is 1, not 0.
                                                                new PropertySet(AppointmentSchema.AppointmentType,
                                                                                AppointmentSchema.Start));
    Console.WriteLine("Compare the start times for a recurring master's first occurrence " + 
                        "and the occurrence found at index 1 using the BindToOccurrence method:");
    Console.WriteLine("The appointment at index 1 has a start time of\t\t\t\t {0}\n" +
                        "Which matches that of the first occurrence on the recurring master: \t {1}",
                        firstOccurrence.Start.ToString(),
                        recurrMaster.FirstOccurrence.Start.ToString());
}

```

## <a name="access-calendar-items-in-a-recurring-series-by-using-ews"></a><span data-ttu-id="16d4d-146">Obtener acceso a los elementos de calendario de una serie periódica mediante EWS</span><span class="sxs-lookup"><span data-stu-id="16d4d-146">Access calendar items in a recurring series by using EWS</span></span>

<span data-ttu-id="16d4d-147">Obtener acceso a los elementos de calendario en una serie periódica es muy similar a tener acceso a instancias únicas de elementos de calendario.</span><span class="sxs-lookup"><span data-stu-id="16d4d-147">Accessing calendar items in a recurring series is very similar to accessing single instances of calendar items.</span></span> <span data-ttu-id="16d4d-148">Use una solicitud de operación [GetItem](https://msdn.microsoft.com/library/769df8eb-9c72-48b5-a49f-82c6b86bc5fc%28Office.15%29.aspx) , especificando las propiedades que desee, con el [OccurrenceItemId](https://msdn.microsoft.com/library/4a15bbc3-5b93-4193-b9ec-da32f0a9a552%28Office.15%29.aspx) de la instancia de la cita que necesite.</span><span class="sxs-lookup"><span data-stu-id="16d4d-148">You use a [GetItem](https://msdn.microsoft.com/library/769df8eb-9c72-48b5-a49f-82c6b86bc5fc%28Office.15%29.aspx) operation request, specifying the properties you want, with the [OccurrenceItemId](https://msdn.microsoft.com/library/4a15bbc3-5b93-4193-b9ec-da32f0a9a552%28Office.15%29.aspx) of the appointment instance you need.</span></span> <span data-ttu-id="16d4d-149">[OccurrenceItemId](https://msdn.microsoft.com/library/4a15bbc3-5b93-4193-b9ec-da32f0a9a552%28Office.15%29.aspx) contiene el valor de **Itemid** del maestro recurrente de la ocurrencia, así como su valor de índice en la serie.</span><span class="sxs-lookup"><span data-stu-id="16d4d-149">The [OccurrenceItemId](https://msdn.microsoft.com/library/4a15bbc3-5b93-4193-b9ec-da32f0a9a552%28Office.15%29.aspx) contains the **ItemID** of the occurrence's recurring master, as well as its index value in the series.</span></span> 
  
<span data-ttu-id="16d4d-150">El siguiente XML muestra la solicitud [GetItem](https://msdn.microsoft.com/library/769df8eb-9c72-48b5-a49f-82c6b86bc5fc%28Office.15%29.aspx) usada para devolver una ocurrencia en una serie especificada por su índice.</span><span class="sxs-lookup"><span data-stu-id="16d4d-150">The following XML shows the [GetItem](https://msdn.microsoft.com/library/769df8eb-9c72-48b5-a49f-82c6b86bc5fc%28Office.15%29.aspx) request used to return an occurrence in a series specified by its index.</span></span> <span data-ttu-id="16d4d-151">Tenga en cuenta que el **Itemid** del patrón recurrente se ha abreviado para facilitar su lectura.</span><span class="sxs-lookup"><span data-stu-id="16d4d-151">Note that the **ItemID** of the recurring master has been shortened for readability.</span></span> 
  
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
          <t:FieldURI FieldURI="calendar:CalendarItemType" />
          <t:FieldURI FieldURI="calendar:Start" />
        </t:AdditionalProperties>
      </m:ItemShape>
      <m:ItemIds>
        <t:OccurrenceItemId RecurringMasterId="AAMkA" InstanceIndex="1" />
      </m:ItemIds>
    </m:GetItem>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="16d4d-152">El servidor responde a la solicitud **GetItem** con un mensaje [GetItemResponse](https://msdn.microsoft.com/library/8b66de1b-26a6-476c-9585-a96059125716%28Office.15%29.aspx) que incluye un valor [ResponseCode](https://msdn.microsoft.com/library/aa580757%28v=exchg.150%29.aspx) de **NoError**, que indica que el correo electrónico se ha creado correctamente y el [Itemid](https://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) del mensaje recién creado.</span><span class="sxs-lookup"><span data-stu-id="16d4d-152">The server responds to the **GetItem** request with a [GetItemResponse](https://msdn.microsoft.com/library/8b66de1b-26a6-476c-9585-a96059125716%28Office.15%29.aspx) message that includes a [ResponseCode](https://msdn.microsoft.com/library/aa580757%28v=exchg.150%29.aspx) value of **NoError**, which indicates that the email was created successfully, and the [ItemId](https://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) of the newly created message.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="16d4d-153">Vea también</span><span class="sxs-lookup"><span data-stu-id="16d4d-153">See also</span></span>


- [<span data-ttu-id="16d4d-154">Calendarios y EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="16d4d-154">Calendars and EWS in Exchange</span></span>](calendars-and-ews-in-exchange.md)
- [<span data-ttu-id="16d4d-155">Obtener citas y reuniones mediante EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="16d4d-155">Get appointments and meetings by using EWS in Exchange</span></span>](how-to-get-appointments-and-meetings-by-using-ews-in-exchange.md)
    

