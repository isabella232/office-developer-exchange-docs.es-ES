---
title: Obtener acceso a una serie periódica mediante el uso de EWS en Exchange
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 196a5671-2836-4696-b734-d5ecfdbf8962
description: Obtenga información sobre cómo obtener acceso a los elementos del calendario en una serie periódica mediante el uso de la API administrada de EWS o EWS en Exchange.
ms.openlocfilehash: 9f78ef5b51766a69d23fce3f36c55fbb9422fb16
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763016"
---
# <a name="access-a-recurring-series-by-using-ews-in-exchange"></a><span data-ttu-id="a4d26-103">Obtener acceso a una serie periódica mediante el uso de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="a4d26-103">Access a recurring series by using EWS in Exchange</span></span>

<span data-ttu-id="a4d26-104">Obtenga información sobre cómo obtener acceso a los elementos del calendario en una serie periódica mediante el uso de la API administrada de EWS o EWS en Exchange.</span><span class="sxs-lookup"><span data-stu-id="a4d26-104">Learn how to access calendar items in a recurring series by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="a4d26-105">Una serie de citas o reuniones periódicas se compone de un patrón periódico, un número de repeticiones de una serie que se repiten según un patrón de conjunto y, opcionalmente, conjuntos de repeticiones que se han cambiado y que se han eliminado.</span><span class="sxs-lookup"><span data-stu-id="a4d26-105">A recurring series of appointments or meetings is made up of a recurring master, a number of occurrences in a series that repeat according to a set pattern, and, optionally, sets of occurrences that were changed and that were deleted.</span></span> <span data-ttu-id="a4d26-106">Puede usar la API administrada de EWS o EWS para obtener acceso a los elementos del calendario en una serie periódica.</span><span class="sxs-lookup"><span data-stu-id="a4d26-106">You can use the EWS Managed API or EWS to access calendar items in a recurring series.</span></span> <span data-ttu-id="a4d26-107">Esto le permite:</span><span class="sxs-lookup"><span data-stu-id="a4d26-107">This enables you to:</span></span>
  
- <span data-ttu-id="a4d26-108">Comprobar si un elemento de calendario asociado con un identificador de elemento es un maestro periódico, una ocurrencia en una serie, o una excepción a una serie.</span><span class="sxs-lookup"><span data-stu-id="a4d26-108">Check to see if a calendar item associated with an item ID is a recurring master, an occurrence in a series, or an exception to a series.</span></span>
    
- <span data-ttu-id="a4d26-109">Busque la carpeta de calendario para las citas de periodicidad.</span><span class="sxs-lookup"><span data-stu-id="a4d26-109">Search your calendar folder for recurrence appointments.</span></span>
    
- <span data-ttu-id="a4d26-110">Obtener elementos de calendario de periodicidad relacionado</span><span class="sxs-lookup"><span data-stu-id="a4d26-110">Get related recurrence calendar items</span></span>
    
- <span data-ttu-id="a4d26-111">Realice una iteración por repeticiones en una serie, excepciones de aparición o eliminaciones de repetición.</span><span class="sxs-lookup"><span data-stu-id="a4d26-111">Iterate through occurrences in a series, occurrence exceptions, or occurrence deletions.</span></span>
    
## <a name="get-a-collection-of-recurring-calendar-items-by-using-the-ews-managed-api"></a><span data-ttu-id="a4d26-112">Obtener una colección de elementos de calendario periódicos mediante el uso de la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="a4d26-112">Get a collection of recurring calendar items by using the EWS Managed API</span></span>

<span data-ttu-id="a4d26-113">Si desea recuperar una colección de citas, puede usar el método [ExchangeService.FindAppointments](http://msdn.microsoft.com/es-es/library/office/microsoft.exchange.webservices.data.exchangeservice.findappointments%28v=exchg.80%29.aspx) para recuperar todas las citas entre una fecha de inicio y finalización determinada y, a continuación, agregue todos los elementos de calendario con un tipo de cita de **aparición **o una **excepción** a una colección, tal como se muestra en el siguiente ejemplo.</span><span class="sxs-lookup"><span data-stu-id="a4d26-113">If you want to retrieve a collection of appointments, you can use the [ExchangeService.FindAppointments](http://msdn.microsoft.com/es-es/library/office/microsoft.exchange.webservices.data.exchangeservice.findappointments%28v=exchg.80%29.aspx) method to retrieve all appointments between a given start and end date, and then add all calendar items with an appointment type of **Occurrence** or **Exception** to a collection, as shown in the following example.</span></span> 
  
<span data-ttu-id="a4d26-114">En este ejemplo se supone que se han autenticado a un servidor de Exchange y ha adquirido un objeto [ExchangeService](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) con el nombre de **servicio**.</span><span class="sxs-lookup"><span data-stu-id="a4d26-114">This example assumes that you have authenticated to an Exchange server and have acquired an [ExchangeService](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object named **service**.</span></span> 
  
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

<span data-ttu-id="a4d26-115">Tenga en cuenta que no se devuelven elementos periódicos del calendario principal en una llamada a **FindAppointments**.</span><span class="sxs-lookup"><span data-stu-id="a4d26-115">Note that recurring master calendar items aren't returned in a call to **FindAppointments**.</span></span> <span data-ttu-id="a4d26-116">Si desea recuperar a los patrones periódicos o, si desea un enfoque más general para la recuperación de elementos de calendario, debe usar [ExchangeService.FindItems](http://msdn.microsoft.com/es-es/library/office/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="a4d26-116">If you want to retrieve recurring masters, or you want a more general approach to retrieving calendar items, you need to use [ExchangeService.FindItems](http://msdn.microsoft.com/es-es/library/office/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx).</span></span> <span data-ttu-id="a4d26-117">A continuación, puede usar un filtro de búsqueda para recuperar sólo los elementos con una fecha de inicio mayor o igual a la fecha que elija y una vista de elemento para limitar el número de elementos para devolver.</span><span class="sxs-lookup"><span data-stu-id="a4d26-117">You can then use a search filter to retrieve only items with a start date greater than or equal to a date you choose, and an item view to limit the number of items to return.</span></span> <span data-ttu-id="a4d26-118">Tenga en cuenta que un maestro periódico con un inicio de fecha anteriores a la fecha de inicio de la búsqueda no se encontrará, incluso si se producen las apariciones de este intervalo.</span><span class="sxs-lookup"><span data-stu-id="a4d26-118">Note that a recurring master with a start date earlier than the start date in your search will not be found, even if occurrences occur in this range.</span></span>
  
<span data-ttu-id="a4d26-119">En este ejemplo se supone que se han autenticado a un servidor de Exchange y ha adquirido un objeto [ExchangeService](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) con el nombre de **servicio**.</span><span class="sxs-lookup"><span data-stu-id="a4d26-119">This example assumes that you have authenticated to an Exchange server and have acquired an [ExchangeService](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object named **service**.</span></span> 
  
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

## <a name="get-related-recurrence-calendar-items-by-using-the-ews-managed-api"></a><span data-ttu-id="a4d26-120">Obtener elementos de calendario de periodicidad relacionado mediante el uso de la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="a4d26-120">Get related recurrence calendar items by using the EWS Managed API</span></span>

<span data-ttu-id="a4d26-121">A veces tiene una pieza del puzzle, pero para resolver necesita el resto de las piezas.</span><span class="sxs-lookup"><span data-stu-id="a4d26-121">Sometimes you have one piece of the puzzle, but to solve it you need the rest of the pieces.</span></span> <span data-ttu-id="a4d26-122">Si tiene el identificador de elemento para un elemento de calendario de periodicidad, puede obtener las otras partes que necesita mediante uno de varios métodos o propiedades de la API administrada de EWS.</span><span class="sxs-lookup"><span data-stu-id="a4d26-122">If you have the item ID for a recurrence calendar item, you can get the other pieces you need by using one of several EWS Managed API properties or methods.</span></span>
  
<span data-ttu-id="a4d26-123">**La tabla 1. API administrada de EWS propiedad o un método a usar para obtener los elementos de calendario de periodicidad relacionado**</span><span class="sxs-lookup"><span data-stu-id="a4d26-123">**Table 1. EWS Managed API property or method to use to get related recurrence calendar items**</span></span>

|<span data-ttu-id="a4d26-124">**Si tiene el identificador de elemento para...**</span><span class="sxs-lookup"><span data-stu-id="a4d26-124">**If you have the item ID for…**</span></span>|<span data-ttu-id="a4d26-125">**Puede obtener...**</span><span class="sxs-lookup"><span data-stu-id="a4d26-125">**You can get…**</span></span>|<span data-ttu-id="a4d26-126">**Mediante el uso de la...**</span><span class="sxs-lookup"><span data-stu-id="a4d26-126">**By using the…**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a4d26-127">El elemento periódico del calendario principal</span><span class="sxs-lookup"><span data-stu-id="a4d26-127">The recurring master calendar item</span></span>  <br/> | <span data-ttu-id="a4d26-128">La primera aparición de una serie</span><span class="sxs-lookup"><span data-stu-id="a4d26-128">The first occurrence in a series</span></span>  <br/>  <span data-ttu-id="a4d26-129">La última aparición de una serie</span><span class="sxs-lookup"><span data-stu-id="a4d26-129">The last occurrence in a series</span></span>  <br/>  <span data-ttu-id="a4d26-130">Las excepciones a una serie de</span><span class="sxs-lookup"><span data-stu-id="a4d26-130">The exceptions to a series</span></span>  <br/>  <span data-ttu-id="a4d26-131">Las citas eliminadas de una serie</span><span class="sxs-lookup"><span data-stu-id="a4d26-131">The deleted appointments in a series</span></span>  <br/>  <span data-ttu-id="a4d26-132">Cualquier aparición (dado su índice)</span><span class="sxs-lookup"><span data-stu-id="a4d26-132">Any occurrence (given its index)</span></span>  <br/> |<span data-ttu-id="a4d26-133">[Appointment.FirstOccurrence](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.appointment.firstoccurrence%28v=exchg.80%29.aspx) (propiedad)</span><span class="sxs-lookup"><span data-stu-id="a4d26-133">[Appointment.FirstOccurrence](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.appointment.firstoccurrence%28v=exchg.80%29.aspx) property</span></span>  <br/> <span data-ttu-id="a4d26-134">[Appointment.LastOccurrence](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.appointment.lastoccurrence%28v=exchg.80%29.aspx) (propiedad)</span><span class="sxs-lookup"><span data-stu-id="a4d26-134">[Appointment.LastOccurrence](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.appointment.lastoccurrence%28v=exchg.80%29.aspx) property</span></span>  <br/> <span data-ttu-id="a4d26-135">[Appointment.ModifiedOccurrences](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.appointment.modifiedoccurrences%28v=exchg.80%29.aspx) (propiedad)</span><span class="sxs-lookup"><span data-stu-id="a4d26-135">[Appointment.ModifiedOccurrences](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.appointment.modifiedoccurrences%28v=exchg.80%29.aspx) property</span></span>  <br/> <span data-ttu-id="a4d26-136">[Appointment.DeletedOccurrences](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.appointment.deletedoccurrences%28v=exchg.80%29.aspx) (propiedad)</span><span class="sxs-lookup"><span data-stu-id="a4d26-136">[Appointment.DeletedOccurrences](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.appointment.deletedoccurrences%28v=exchg.80%29.aspx) property</span></span>  <br/> <span data-ttu-id="a4d26-137">[Appointment.BindToOccurrence](http://msdn.microsoft.com/es-es/library/office/microsoft.exchange.webservices.data.appointment.bindtooccurrence%28v=exchg.80%29.aspx) (método)</span><span class="sxs-lookup"><span data-stu-id="a4d26-137">[Appointment.BindToOccurrence](http://msdn.microsoft.com/es-es/library/office/microsoft.exchange.webservices.data.appointment.bindtooccurrence%28v=exchg.80%29.aspx) method</span></span>  <br/> |
|<span data-ttu-id="a4d26-138">Una sola aparición de una serie</span><span class="sxs-lookup"><span data-stu-id="a4d26-138">A single occurrence in a series</span></span>  <br/> |<span data-ttu-id="a4d26-139">El patrón periódico</span><span class="sxs-lookup"><span data-stu-id="a4d26-139">The recurring master</span></span>  <br/> |<span data-ttu-id="a4d26-140">[Appointment.BindToRecurringMaster](http://msdn.microsoft.com/es-es/library/office/microsoft.exchange.webservices.data.appointment.bindtorecurringmaster%28v=exchg.80%29.aspx) (método)</span><span class="sxs-lookup"><span data-stu-id="a4d26-140">[Appointment.BindToRecurringMaster](http://msdn.microsoft.com/es-es/library/office/microsoft.exchange.webservices.data.appointment.bindtorecurringmaster%28v=exchg.80%29.aspx) method</span></span>  <br/> |
|<span data-ttu-id="a4d26-141">Cualquier elemento de calendario (un objeto [Appointment](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) )</span><span class="sxs-lookup"><span data-stu-id="a4d26-141">Any calendar item (an [Appointment](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) object)</span></span>  <br/> |<span data-ttu-id="a4d26-142">El valor de [tipo de cita](http://msdn.microsoft.com/es-es/library/office/microsoft.exchange.webservices.data.appointmenttype%28v=exchg.80%29.aspx) (enumeración)</span><span class="sxs-lookup"><span data-stu-id="a4d26-142">The [appointment type](http://msdn.microsoft.com/es-es/library/office/microsoft.exchange.webservices.data.appointmenttype%28v=exchg.80%29.aspx) enumeration value</span></span>  <br/> |<span data-ttu-id="a4d26-143">[Appointment.AppointmentType](http://msdn.microsoft.com/es-es/library/office/microsoft.exchange.webservices.data.appointment.appointmenttype%28v=exchg.80%29.aspx) (propiedad)</span><span class="sxs-lookup"><span data-stu-id="a4d26-143">[Appointment.AppointmentType](http://msdn.microsoft.com/es-es/library/office/microsoft.exchange.webservices.data.appointment.appointmenttype%28v=exchg.80%29.aspx) property</span></span>  <br/> |
   
<span data-ttu-id="a4d26-144">En el ejemplo de código siguiente se muestra cómo obtener una ocurrencia dado su índice, la primera o la última aparición de una serie o un patrón periódico.</span><span class="sxs-lookup"><span data-stu-id="a4d26-144">The following code example shows how to get a recurring master, the first or last occurrence in a series, or an occurrence given its index.</span></span>
  
<span data-ttu-id="a4d26-145">En este ejemplo se supone que se han autenticado a un servidor de Exchange y ha adquirido un objeto [ExchangeService](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) con el nombre de **servicio**.</span><span class="sxs-lookup"><span data-stu-id="a4d26-145">This example assumes that you have authenticated to an Exchange server and have acquired an [ExchangeService](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object named **service**.</span></span> 
  
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

## <a name="access-calendar-items-in-a-recurring-series-by-using-ews"></a><span data-ttu-id="a4d26-146">Elementos de calendario de Access en una serie periódica mediante el uso de EWS</span><span class="sxs-lookup"><span data-stu-id="a4d26-146">Access calendar items in a recurring series by using EWS</span></span>

<span data-ttu-id="a4d26-147">Obtener acceso a los elementos del calendario en una serie periódica es muy similar a obtener acceso a las instancias únicas de los elementos del calendario.</span><span class="sxs-lookup"><span data-stu-id="a4d26-147">Accessing calendar items in a recurring series is very similar to accessing single instances of calendar items.</span></span> <span data-ttu-id="a4d26-148">Use una solicitud de operación [GetItem](http://msdn.microsoft.com/library/769df8eb-9c72-48b5-a49f-82c6b86bc5fc%28Office.15%29.aspx) , que especifica las propiedades que desee, con el [OccurrenceItemId](http://msdn.microsoft.com/library/4a15bbc3-5b93-4193-b9ec-da32f0a9a552%28Office.15%29.aspx) de la instancia de una cita que necesita.</span><span class="sxs-lookup"><span data-stu-id="a4d26-148">You use a [GetItem](http://msdn.microsoft.com/library/769df8eb-9c72-48b5-a49f-82c6b86bc5fc%28Office.15%29.aspx) operation request, specifying the properties you want, with the [OccurrenceItemId](http://msdn.microsoft.com/library/4a15bbc3-5b93-4193-b9ec-da32f0a9a552%28Office.15%29.aspx) of the appointment instance you need.</span></span> <span data-ttu-id="a4d26-149">El [OccurrenceItemId](http://msdn.microsoft.com/library/4a15bbc3-5b93-4193-b9ec-da32f0a9a552%28Office.15%29.aspx) contiene el **ItemID** de maestro periódico de la aparición, así como su valor de índice de la serie.</span><span class="sxs-lookup"><span data-stu-id="a4d26-149">The [OccurrenceItemId](http://msdn.microsoft.com/library/4a15bbc3-5b93-4193-b9ec-da32f0a9a552%28Office.15%29.aspx) contains the **ItemID** of the occurrence's recurring master, as well as its index value in the series.</span></span> 
  
<span data-ttu-id="a4d26-150">El siguiente código XML muestra la solicitud [GetItem](http://msdn.microsoft.com/library/769df8eb-9c72-48b5-a49f-82c6b86bc5fc%28Office.15%29.aspx) que se usa para devolver una ocurrencia de una serie especificada por su índice.</span><span class="sxs-lookup"><span data-stu-id="a4d26-150">The following XML shows the [GetItem](http://msdn.microsoft.com/library/769df8eb-9c72-48b5-a49f-82c6b86bc5fc%28Office.15%29.aspx) request used to return an occurrence in a series specified by its index.</span></span> <span data-ttu-id="a4d26-151">Tenga en cuenta que se ha reducido la **ItemID** del patrón periódico para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="a4d26-151">Note that the **ItemID** of the recurring master has been shortened for readability.</span></span> 
  
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

<span data-ttu-id="a4d26-152">El servidor responde a la solicitud de **GetItem** con un mensaje de [GetItemResponse](http://msdn.microsoft.com/library/8b66de1b-26a6-476c-9585-a96059125716%28Office.15%29.aspx) que incluye un valor [ResponseCode](http://msdn.microsoft.com/es-es/library/aa580757%28v=exchg.150%29.aspx) **NoError**, lo que indica que el correo electrónico se ha creado correctamente y la [ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) de la recientemente mensaje de creación.</span><span class="sxs-lookup"><span data-stu-id="a4d26-152">The server responds to the **GetItem** request with a [GetItemResponse](http://msdn.microsoft.com/library/8b66de1b-26a6-476c-9585-a96059125716%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/es-es/library/aa580757%28v=exchg.150%29.aspx) value of **NoError**, which indicates that the email was created successfully, and the [ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) of the newly created message.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a4d26-153">Vea también</span><span class="sxs-lookup"><span data-stu-id="a4d26-153">See also</span></span>


- [<span data-ttu-id="a4d26-154">Calendarios y EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="a4d26-154">Calendars and EWS in Exchange</span></span>](calendars-and-ews-in-exchange.md)
- [<span data-ttu-id="a4d26-155">Obtener las citas y reuniones con EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="a4d26-155">Get appointments and meetings by using EWS in Exchange</span></span>](how-to-get-appointments-and-meetings-by-using-ews-in-exchange.md)
    

