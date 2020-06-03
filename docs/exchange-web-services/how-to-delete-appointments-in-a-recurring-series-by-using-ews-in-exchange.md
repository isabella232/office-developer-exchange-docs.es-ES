---
title: Eliminar citas en una serie periódica mediante EWS en Exchange
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: a9d5244a-bc4a-4e9c-9c6c-ff361e04cbf8
description: Obtenga información sobre cómo eliminar citas en una serie periódica mediante la API administrada de EWS o EWS en Exchange.
ms.openlocfilehash: 5646a30d218ed4d795044aefe5efea1399d19a79
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44528128"
---
# <a name="delete-appointments-in-a-recurring-series-by-using-ews-in-exchange"></a><span data-ttu-id="c98a4-103">Eliminar citas en una serie periódica mediante EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="c98a4-103">Delete appointments in a recurring series by using EWS in Exchange</span></span>

<span data-ttu-id="c98a4-104">Obtenga información sobre cómo eliminar citas en una serie periódica mediante la API administrada de EWS o EWS en Exchange.</span><span class="sxs-lookup"><span data-stu-id="c98a4-104">Learn how to delete appointments in a recurring series by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="c98a4-105">Puede usar la API administrada de EWS o EWS para eliminar una serie de citas o reuniones, o solo una instancia de la serie.</span><span class="sxs-lookup"><span data-stu-id="c98a4-105">You can use the EWS Managed API or EWS to delete a series of appointments or meetings, or just one instance in the series.</span></span> <span data-ttu-id="c98a4-106">El proceso que se usa para eliminar una serie completa es esencialmente el mismo que el proceso que se usa para eliminar una sola ocurrencia.</span><span class="sxs-lookup"><span data-stu-id="c98a4-106">The process you use to delete an entire series is essentially the same as the process you use to delete just a single occurrence.</span></span> <span data-ttu-id="c98a4-107">Use los mismos métodos de API administrada de EWS o las operaciones de EWS que usa para [eliminar una reunión o cita de instancia única](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="c98a4-107">You use the same EWS Managed API methods or EWS operations that you use to [delete a single instance appointment or meeting](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md).</span></span> <span data-ttu-id="c98a4-108">La diferencia se encuentra en el identificador de elemento que se incluye en el método o en la operación.</span><span class="sxs-lookup"><span data-stu-id="c98a4-108">The difference is in the item ID that is included in the method or operation.</span></span> <span data-ttu-id="c98a4-109">Comencemos observando el funcionamiento de ambos escenarios.</span><span class="sxs-lookup"><span data-stu-id="c98a4-109">Let's start by looking at how both scenarios are the same.</span></span> 
  
<span data-ttu-id="c98a4-110">Para eliminar una serie periódica o una sola repetición en una serie periódica, debe buscar la ocurrencia o la serie que desea eliminar y, a continuación, llamar al método o la operación apropiados para quitarla.</span><span class="sxs-lookup"><span data-stu-id="c98a4-110">In order to delete a recurring series or a single occurrence in a recurring series, you need to find the occurrence or series that you want to delete, and then call the appropriate method or operation to remove it.</span></span> <span data-ttu-id="c98a4-111">Aunque simplemente puede eliminar cualquier tipo de cita, le recomendamos que mantenga a los asistentes o al organizador al día y que cancele las reuniones que el usuario haya organizado y declinando las reuniones que el usuario no haya organizado.</span><span class="sxs-lookup"><span data-stu-id="c98a4-111">While you can simply delete any type of appointment, we recommend that you keep any attendees or the organizer up to date and cancel meetings that the user has organized and decline meetings that the user did not organize.</span></span>
  
<span data-ttu-id="c98a4-112">¿En qué se diferencian los escenarios?</span><span class="sxs-lookup"><span data-stu-id="c98a4-112">So how are the scenarios different?</span></span> <span data-ttu-id="c98a4-113">Todo el objeto [appointment](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) se usa para invocar el método (para la API administrada EWS) o el identificador de elemento incluido en la solicitud de operación (para EWS).</span><span class="sxs-lookup"><span data-stu-id="c98a4-113">It's all about the [Appointment](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) object used to invoke the method (for the EWS Managed API) or the item ID included in the operation request (for EWS).</span></span> <span data-ttu-id="c98a4-114">Para eliminar una serie completa, necesitará el objeto de **cita** o el identificador de elemento del patrón recurrente.</span><span class="sxs-lookup"><span data-stu-id="c98a4-114">To delete an entire series, you need the **Appointment** object or item ID for the recurring master.</span></span> <span data-ttu-id="c98a4-115">Para eliminar una sola repetición, necesitará el objeto de **cita** o identificador de elemento para la ocurrencia.</span><span class="sxs-lookup"><span data-stu-id="c98a4-115">To delete a single occurrence, you need the **Appointment** object or item ID for the occurrence.</span></span> 
  
## <a name="delete-a-recurring-appointment-by-using-the-ews-managed-api"></a><span data-ttu-id="c98a4-116">Eliminar una cita periódica mediante la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="c98a4-116">Delete a recurring appointment by using the EWS Managed API</span></span>

<span data-ttu-id="c98a4-117">En este ejemplo se supone que se ha autenticado en un servidor de Exchange y que se ha adquirido un objeto [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) denominado **Service**.</span><span class="sxs-lookup"><span data-stu-id="c98a4-117">This example assumes that you have authenticated to an Exchange server and have acquired an [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object named **service**.</span></span> <span data-ttu-id="c98a4-118">El parámetro _recurringItem_ es un objeto de **cita** para el patrón periódico o una sola ocurrencia.</span><span class="sxs-lookup"><span data-stu-id="c98a4-118">The  _recurringItem_ parameter is an **Appointment** object for either the recurring master or a single occurrence.</span></span> <span data-ttu-id="c98a4-119">El parámetro _deleteEntireSeries_ indica si se va a eliminar la serie completa de la que forma parte _recurringItem_ .</span><span class="sxs-lookup"><span data-stu-id="c98a4-119">The  _deleteEntireSeries_ parameter indicates whether to delete the entire series that the  _recurringItem_ is a part of.</span></span> 
  
```cs
public static bool DeleteRecurringItem(ExchangeService service, Appointment recurringItem, bool deleteEntireSeries)
{
    Appointment appointmentToDelete = null;
    // If the item is a single appointment, fail.
    if (recurringItem.AppointmentType == AppointmentType.Single)
    {
        Console.WriteLine("ERROR: The item to delete is not part of a recurring series.");
        return false;
    }
    // Check the Appointment that was passed. Is it
    // an occurrence or the recurring master?
    if (recurringItem.AppointmentType == AppointmentType.RecurringMaster)
    {
        if (!deleteEntireSeries)
        {
            // The item is the recurring master, so deleting it will delete
            // the entire series. The caller indicated that the entire series
            // should not be deleted, so fail.
            Console.WriteLine("ERROR: The item to delete is the recurring master of the series. Deleting it will delete the entire series.");
            return false;
        }
        else
        {
            appointmentToDelete = recurringItem;
        }
    }
    else
    {
        if (deleteEntireSeries)
        {
            // The item passed is not the recurring master, but the caller
            // wants to delete the entire series. Bind to the recurring
            // master to delete it.
            try
            {
                appointmentToDelete = Appointment.BindToRecurringMaster(service, recurringItem.Id);
            }
            catch (Exception ex)
            {
                Console.WriteLine("ERROR: {0}", ex.Message);
                return false;
            }
        }
        else
        {
            // The item passed is not the recurring master, but the caller
            // only wants to delete the occurrence, so just
            // delete the passed item.
            appointmentToDelete = recurringItem;
        }
    }
    if (appointmentToDelete != null)
    {
        // Remove the item, depending on the scenario. 
        if (appointmentToDelete.IsMeeting)
        {
            CalendarActionResults results;
            // If it's a meeting and the user is the organizer, cancel it.
            // Determine this by testing the AppointmentState bitmask for 
            // the presence of the second bit. This bit indicates that the appointment
            // was received, which means that someone sent it to the user. Therefore,
            // they're not the organizer.
            int isReceived = 2;
            if ((appointmentToDelete.AppointmentState &amp; isReceived) == 0)
            {
                results = appointmentToDelete.CancelMeeting("Cancelling this meeting.");
                return true;
            }
            // If it's a meeting and the user is not the organizer, decline it.
            else
            {
                results = appointmentToDelete.Decline(true);
                return true;
            }
        }
        else
        {
            // The item isn't a meeting, so just delete it.
            appointmentToDelete.Delete(DeleteMode.MoveToDeletedItems);
            return true;
        }
    }
    return false;
}
```

<span data-ttu-id="c98a4-120">Para usar este ejemplo, debe [enlazar a una ocurrencia o a un patrón recurrente](how-to-access-a-recurring-series-by-using-ews-in-exchange.md), y pasar el objeto **appointment** resultante al método.</span><span class="sxs-lookup"><span data-stu-id="c98a4-120">In order to use this example, you need to [bind to either an occurrence or the recurring master](how-to-access-a-recurring-series-by-using-ews-in-exchange.md), and pass the resulting **Appointment** object to the method.</span></span> <span data-ttu-id="c98a4-121">Tenga en cuenta que si tiene acceso a las citas mediante una clase [CalendarView](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.calendarview%28v=exchg.80%29.aspx) , los elementos resultantes son todas las ocurrencias únicas.</span><span class="sxs-lookup"><span data-stu-id="c98a4-121">Keep in mind that if you access appointments by using a [CalendarView](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.calendarview%28v=exchg.80%29.aspx) class, the resulting items are all single occurrences.</span></span> <span data-ttu-id="c98a4-122">Por el contrario, si usa la clase [ItemView](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.itemview%28v=exchg.80%29.aspx) , los elementos resultantes son todos los maestros periódicos.</span><span class="sxs-lookup"><span data-stu-id="c98a4-122">Conversely, if you use the [ItemView](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.itemview%28v=exchg.80%29.aspx) class, the resulting items are all recurring masters.</span></span> 
  
## <a name="delete-a-recurring-appointment-by-using-ews"></a><span data-ttu-id="c98a4-123">Eliminar una cita periódica mediante EWS</span><span class="sxs-lookup"><span data-stu-id="c98a4-123">Delete a recurring appointment by using EWS</span></span>

<span data-ttu-id="c98a4-124">Eliminar una serie periódica mediante EWS es lo mismo que [eliminar una reunión de instancia única](how-to-delete-appointments-in-a-recurring-series-by-using-ews-in-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="c98a4-124">Deleting a recurring series by using EWS is the same as [deleting a single-instance meeting](how-to-delete-appointments-in-a-recurring-series-by-using-ews-in-exchange.md).</span></span> <span data-ttu-id="c98a4-125">De hecho, las solicitudes SOAP tienen el mismo formato.</span><span class="sxs-lookup"><span data-stu-id="c98a4-125">In fact, the SOAP requests take the same format.</span></span> <span data-ttu-id="c98a4-126">Una vez más, la clave es el identificador de elemento usado en la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c98a4-126">Again, the key is the item ID used in the request.</span></span> <span data-ttu-id="c98a4-127">Si el identificador de elemento corresponde al patrón recurrente, se eliminará toda la serie.</span><span class="sxs-lookup"><span data-stu-id="c98a4-127">If the item ID corresponds to the recurring master, the entire series will be deleted.</span></span> <span data-ttu-id="c98a4-128">Si el identificador de elemento corresponde a una sola ocurrencia, solo se eliminará esa repetición.</span><span class="sxs-lookup"><span data-stu-id="c98a4-128">If the item ID corresponds to a single occurrence, only that occurrence will be deleted.</span></span>
  
> [!NOTE]
> <span data-ttu-id="c98a4-129">En los ejemplos de código siguientes, los atributos **Itemid**, **changekey**y **RecurringMasterId** se acortan para facilitar su lectura.</span><span class="sxs-lookup"><span data-stu-id="c98a4-129">In the code examples that follow, the **ItemId**, **ChangeKey**, and **RecurringMasterId** attributes are shortened for readability.</span></span> 
  
<span data-ttu-id="c98a4-130">En este ejemplo, se usa la [operación CreateItem](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) con un elemento [CancelCalendarItem](https://msdn.microsoft.com/library/a2046402-a176-44d5-b4b3-adb696581935%28Office.15%29.aspx) para cancelar una reunión para la que el usuario es el organizador.</span><span class="sxs-lookup"><span data-stu-id="c98a4-130">This example uses the [CreateItem operation](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) with a [CancelCalendarItem](https://msdn.microsoft.com/library/a2046402-a176-44d5-b4b3-adb696581935%28Office.15%29.aspx) element to cancel a meeting for which the user is the organizer.</span></span> <span data-ttu-id="c98a4-131">El valor del elemento [ReferenceItemId](https://msdn.microsoft.com/library/8fd4bb12-a94b-43f5-be3b-f435684e311d%28Office.15%29.aspx) indica el elemento que se va a cancelar, y puede ser el identificador de elemento de un patrón recurrente o una sola ocurrencia.</span><span class="sxs-lookup"><span data-stu-id="c98a4-131">The value of the [ReferenceItemId](https://msdn.microsoft.com/library/8fd4bb12-a94b-43f5-be3b-f435684e311d%28Office.15%29.aspx) element indicates the item to cancel, and can be the item ID of a recurring master or a single occurrence.</span></span> 
  
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
    <m:CreateItem MessageDisposition="SendAndSaveCopy">
      <m:Items>
        <t:CancelCalendarItem>
          <t:ReferenceItemId Id="AAMkADA5..." ChangeKey="DwAAABYA..." />
          <t:NewBodyContent BodyType="HTML">Cancelling this meeting.</t:NewBodyContent>
        </t:CancelCalendarItem>
      </m:Items>
    </m:CreateItem>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="c98a4-132">En este ejemplo se utiliza la **operación CreateItem** con un elemento [DeclineItem](https://msdn.microsoft.com/library/2d8d2389-924e-4d03-a324-35d56cf0d6b1%28Office.15%29.aspx) para rechazar una reunión para la que el usuario no es el organizador.</span><span class="sxs-lookup"><span data-stu-id="c98a4-132">This example uses the **CreateItem operation** with a [DeclineItem](https://msdn.microsoft.com/library/2d8d2389-924e-4d03-a324-35d56cf0d6b1%28Office.15%29.aspx) element to decline a meeting for which the user is not the organizer.</span></span> <span data-ttu-id="c98a4-133">Como en el ejemplo anterior, el valor del elemento **ReferenceItemId** indica el elemento que se va a rechazar, y puede ser el identificador de elemento de un patrón recurrente o una sola ocurrencia.</span><span class="sxs-lookup"><span data-stu-id="c98a4-133">As in the previous example, the value of the **ReferenceItemId** element indicates the item to decline, and can be the item ID of a recurring master or a single occurrence.</span></span> 
  
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
    <m:CreateItem MessageDisposition="SendAndSaveCopy">
      <m:Items>
        <t:DeclineItem>
          <t:ReferenceItemId Id="AAMkADA6..." ChangeKey="DwAAABYA..." />
        </t:DeclineItem>
      </m:Items>
    </m:CreateItem>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="c98a4-134">En este ejemplo se usa la [operación DeleteItem](https://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx) para eliminar una única ocurrencia de una cita sin asistentes.</span><span class="sxs-lookup"><span data-stu-id="c98a4-134">This example uses the [DeleteItem operation](https://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx) to delete a single occurrence of an appointment with no attendees.</span></span> <span data-ttu-id="c98a4-135">La repetición que se va a eliminar se especifica mediante el elemento [OccurrenceItemId](https://msdn.microsoft.com/library/4a15bbc3-5b93-4193-b9ec-da32f0a9a552%28Office.15%29.aspx) , que se crea a partir del identificador de elemento del patrón recurrente y el índice de la ocurrencia.</span><span class="sxs-lookup"><span data-stu-id="c98a4-135">The occurrence to delete is specified by the [OccurrenceItemId](https://msdn.microsoft.com/library/4a15bbc3-5b93-4193-b9ec-da32f0a9a552%28Office.15%29.aspx) element, which is constructed from the item ID of the recurring master and the index of the occurrence.</span></span> 
  
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
    <m:DeleteItem DeleteType="MoveToDeletedItems" SendMeetingCancellations="SendToAllAndSaveCopy">
      <m:ItemIds>
        <t:OccurrenceItemId RecurringMasterId="AAMkADA8..." InstanceIndex="3" />
      </m:ItemIds>
    </m:DeleteItem>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="c98a4-136">Tenga en cuenta que puede obtener el mismo resultado si reemplaza el elemento **OccurrenceItemId** con un elemento [Itemid](https://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) que contenga el identificador de elemento de la ocurrencia, tal como se muestra.</span><span class="sxs-lookup"><span data-stu-id="c98a4-136">Note that you can get the same result by replacing the **OccurrenceItemId** element with an [ItemId](https://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) element that contains the item ID of the occurrence, as shown.</span></span> 
  
```XML
<m:ItemIds>
  <t:ItemId Id="AAMkADA7..." ChangeKey="DwAAABYA..." />
</m:ItemIds>

```

## <a name="see-also"></a><span data-ttu-id="c98a4-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="c98a4-137">See also</span></span>


- [<span data-ttu-id="c98a4-138">Patrones de periodicidad y EWS</span><span class="sxs-lookup"><span data-stu-id="c98a4-138">Recurrence patterns and EWS</span></span>](recurrence-patterns-and-ews.md)
    
- [<span data-ttu-id="c98a4-139">Obtener acceso a una serie periódica mediante EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="c98a4-139">Access a recurring series by using EWS in Exchange</span></span>](how-to-access-a-recurring-series-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="c98a4-140">Crear una serie periódica mediante EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="c98a4-140">Create a recurring series by using EWS in Exchange</span></span>](how-to-create-a-recurring-series-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="c98a4-141">Actualizar una serie periódica mediante EWS</span><span class="sxs-lookup"><span data-stu-id="c98a4-141">Update a recurring series by using EWS</span></span>](how-to-update-a-recurring-series-by-using-ews.md)
    
- [<span data-ttu-id="c98a4-142">Actualizar una serie periódica mediante EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="c98a4-142">Update a recurring series by using EWS in Exchange</span></span>](how-to-update-a-recurring-series-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="c98a4-143">Calendarios y EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="c98a4-143">Calendars and EWS in Exchange</span></span>](calendars-and-ews-in-exchange.md)
    
- [<span data-ttu-id="c98a4-144">Crear citas y reuniones mediante EWS en Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="c98a4-144">Create appointments and meetings by using EWS in Exchange 2013</span></span>](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md)
    
- [<span data-ttu-id="c98a4-145">Eliminar citas y cancelar reuniones mediante EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="c98a4-145">Delete appointments and cancel meetings by using EWS in Exchange</span></span>](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md)
    

