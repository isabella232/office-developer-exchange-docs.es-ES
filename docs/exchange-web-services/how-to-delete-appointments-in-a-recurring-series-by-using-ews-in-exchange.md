---
title: Eliminar citas en una serie periódica mediante EWS en Exchange
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: a9d5244a-bc4a-4e9c-9c6c-ff361e04cbf8
description: Obtenga información sobre cómo eliminar citas en una serie periódica mediante la API administrada ews o EWS en Exchange.
ms.openlocfilehash: 8a68b6655c98f290d569a14dc0ac518c5d875cbe
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59513195"
---
# <a name="delete-appointments-in-a-recurring-series-by-using-ews-in-exchange"></a>Eliminar citas en una serie periódica mediante EWS en Exchange

Obtenga información sobre cómo eliminar citas en una serie periódica mediante la API administrada ews o EWS en Exchange.
  
Puede usar la API administrada ews o EWS para eliminar una serie de citas o reuniones, o solo una instancia de la serie. El proceso que se usa para eliminar una serie completa es esencialmente el mismo que el que se usa para eliminar una sola repetición. Se usan los mismos métodos de LA API administrada ews u operaciones EWS que se usan para eliminar una única cita [o reunión de instancia.](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md) La diferencia está en el identificador de elemento que se incluye en el método u operación. Empecemos por ver cómo ambos escenarios son los mismos. 
  
Para eliminar una serie periódica o una sola repetición en una serie periódica, debe buscar la repetición o serie que desea eliminar y, a continuación, llamar al método u operación adecuado para quitarla. Aunque simplemente puede eliminar cualquier tipo de cita, se recomienda mantener actualizados a los asistentes o al organizador y cancelar las reuniones que el usuario ha organizado y rechazar las reuniones que el usuario no organizó.
  
Entonces, ¿en qué se diferencian los escenarios? Todo se trata del objeto [Appointment](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) usado para invocar el método (para la API administrada ews) o el identificador de elemento incluido en la solicitud de operación (para EWS). Para eliminar una serie completa, necesita el **objeto Appointment** o el identificador de elemento para el patrón periódico. Para eliminar una sola repetición, necesita el **objeto Appointment** o el identificador de elemento para la repetición. 
  
## <a name="delete-a-recurring-appointment-by-using-the-ews-managed-api"></a>Eliminar una cita periódica mediante la API administrada de EWS

En este ejemplo se supone que se ha autenticado en un servidor Exchange y que ha adquirido un objeto [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) denominado **service**. El  _parámetro recurringItem_ es un **objeto Appointment** para el patrón periódico o una única repetición. El  _parámetro deleteEntireSeries_ indica si se va a eliminar toda la serie de la que  _el objeto recurringItem_ forma parte. 
  
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

Para usar este ejemplo, debe enlazar a una repetición o al patrón periódico [y](how-to-access-a-recurring-series-by-using-ews-in-exchange.md)pasar el objeto **Appointment** resultante al método. Tenga en cuenta que si accede a las citas mediante una clase [CalendarView,](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.calendarview%28v=exchg.80%29.aspx) los elementos resultantes son todas repeticiones únicas. Por el contrario, si usa la [clase ItemView,](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.itemview%28v=exchg.80%29.aspx) los elementos resultantes son patrones periódicos. 
  
## <a name="delete-a-recurring-appointment-by-using-ews"></a>Eliminar una cita periódica mediante EWS

Eliminar una serie periódica mediante EWS es lo mismo que eliminar una [reunión de instancia única.](how-to-delete-appointments-in-a-recurring-series-by-using-ews-in-exchange.md) De hecho, las solicitudes SOAP tienen el mismo formato. De nuevo, la clave es el identificador de elemento usado en la solicitud. Si el identificador del elemento corresponde al patrón periódico, se eliminará toda la serie. Si el identificador del elemento corresponde a una única repetición, solo se eliminará esa repetición.
  
> [!NOTE]
> En los ejemplos de código siguientes, los **atributos ItemId,** **ChangeKey** y **RecurringMasterId** se acortan para mejorar la legibilidad. 
  
En este ejemplo se usa [la operación CreateItem](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) con un [elemento CancelCalendarItem](https://msdn.microsoft.com/library/a2046402-a176-44d5-b4b3-adb696581935%28Office.15%29.aspx) para cancelar una reunión para la que el usuario es el organizador. El valor del [elemento ReferenceItemId](https://msdn.microsoft.com/library/8fd4bb12-a94b-43f5-be3b-f435684e311d%28Office.15%29.aspx) indica el elemento que se va a cancelar y puede ser el identificador de elemento de un patrón periódico o una única repetición. 
  
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

En este ejemplo se usa **la operación CreateItem** con [un elemento DeclineItem](https://msdn.microsoft.com/library/2d8d2389-924e-4d03-a324-35d56cf0d6b1%28Office.15%29.aspx) para rechazar una reunión para la que el usuario no es el organizador. Al igual que en el ejemplo anterior, el valor del elemento **ReferenceItemId** indica el elemento que se va a rechazar y puede ser el identificador de elemento de un patrón periódico o una sola repetición. 
  
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

En este ejemplo se usa [la operación DeleteItem](https://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx) para eliminar una sola repetición de una cita sin asistentes. La repetición que se va a eliminar se especifica mediante el elemento [OccurrenceItemId,](https://msdn.microsoft.com/library/4a15bbc3-5b93-4193-b9ec-da32f0a9a552%28Office.15%29.aspx) que se construye a partir del identificador de elemento del patrón periódico y el índice de la repetición. 
  
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

Tenga en cuenta que puede obtener el mismo resultado reemplazando el elemento **OccurrenceItemId** por un [elemento ItemId](https://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) que contiene el identificador de elemento de la repetición, como se muestra. 
  
```XML
<m:ItemIds>
  <t:ItemId Id="AAMkADA7..." ChangeKey="DwAAABYA..." />
</m:ItemIds>

```

## <a name="see-also"></a>Ver también


- [Patrones de periodicidad y EWS](recurrence-patterns-and-ews.md)
    
- [Obtener acceso a una serie periódica mediante EWS en Exchange](how-to-access-a-recurring-series-by-using-ews-in-exchange.md)
    
- [Crear una serie periódica mediante EWS en Exchange](how-to-create-a-recurring-series-by-using-ews-in-exchange.md)
    
- [Actualizar una serie periódica mediante EWS](how-to-update-a-recurring-series-by-using-ews.md)
    
- [Actualice una serie periódica mediante EWS en Exchange](how-to-update-a-recurring-series-by-using-ews-in-exchange.md)
    
- [Calendarios y EWS en Exchange](calendars-and-ews-in-exchange.md)
    
- [Crear citas y reuniones mediante EWS en Exchange 2013](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md)
    
- [Eliminar citas y cancelar reuniones mediante EWS en Exchange](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md)
    

