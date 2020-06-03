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
# <a name="delete-appointments-in-a-recurring-series-by-using-ews-in-exchange"></a>Eliminar citas en una serie periódica mediante EWS en Exchange

Obtenga información sobre cómo eliminar citas en una serie periódica mediante la API administrada de EWS o EWS en Exchange.
  
Puede usar la API administrada de EWS o EWS para eliminar una serie de citas o reuniones, o solo una instancia de la serie. El proceso que se usa para eliminar una serie completa es esencialmente el mismo que el proceso que se usa para eliminar una sola ocurrencia. Use los mismos métodos de API administrada de EWS o las operaciones de EWS que usa para [eliminar una reunión o cita de instancia única](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md). La diferencia se encuentra en el identificador de elemento que se incluye en el método o en la operación. Comencemos observando el funcionamiento de ambos escenarios. 
  
Para eliminar una serie periódica o una sola repetición en una serie periódica, debe buscar la ocurrencia o la serie que desea eliminar y, a continuación, llamar al método o la operación apropiados para quitarla. Aunque simplemente puede eliminar cualquier tipo de cita, le recomendamos que mantenga a los asistentes o al organizador al día y que cancele las reuniones que el usuario haya organizado y declinando las reuniones que el usuario no haya organizado.
  
¿En qué se diferencian los escenarios? Todo el objeto [appointment](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) se usa para invocar el método (para la API administrada EWS) o el identificador de elemento incluido en la solicitud de operación (para EWS). Para eliminar una serie completa, necesitará el objeto de **cita** o el identificador de elemento del patrón recurrente. Para eliminar una sola repetición, necesitará el objeto de **cita** o identificador de elemento para la ocurrencia. 
  
## <a name="delete-a-recurring-appointment-by-using-the-ews-managed-api"></a>Eliminar una cita periódica mediante la API administrada de EWS

En este ejemplo se supone que se ha autenticado en un servidor de Exchange y que se ha adquirido un objeto [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) denominado **Service**. El parámetro _recurringItem_ es un objeto de **cita** para el patrón periódico o una sola ocurrencia. El parámetro _deleteEntireSeries_ indica si se va a eliminar la serie completa de la que forma parte _recurringItem_ . 
  
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

Para usar este ejemplo, debe [enlazar a una ocurrencia o a un patrón recurrente](how-to-access-a-recurring-series-by-using-ews-in-exchange.md), y pasar el objeto **appointment** resultante al método. Tenga en cuenta que si tiene acceso a las citas mediante una clase [CalendarView](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.calendarview%28v=exchg.80%29.aspx) , los elementos resultantes son todas las ocurrencias únicas. Por el contrario, si usa la clase [ItemView](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.itemview%28v=exchg.80%29.aspx) , los elementos resultantes son todos los maestros periódicos. 
  
## <a name="delete-a-recurring-appointment-by-using-ews"></a>Eliminar una cita periódica mediante EWS

Eliminar una serie periódica mediante EWS es lo mismo que [eliminar una reunión de instancia única](how-to-delete-appointments-in-a-recurring-series-by-using-ews-in-exchange.md). De hecho, las solicitudes SOAP tienen el mismo formato. Una vez más, la clave es el identificador de elemento usado en la solicitud. Si el identificador de elemento corresponde al patrón recurrente, se eliminará toda la serie. Si el identificador de elemento corresponde a una sola ocurrencia, solo se eliminará esa repetición.
  
> [!NOTE]
> En los ejemplos de código siguientes, los atributos **Itemid**, **changekey**y **RecurringMasterId** se acortan para facilitar su lectura. 
  
En este ejemplo, se usa la [operación CreateItem](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) con un elemento [CancelCalendarItem](https://msdn.microsoft.com/library/a2046402-a176-44d5-b4b3-adb696581935%28Office.15%29.aspx) para cancelar una reunión para la que el usuario es el organizador. El valor del elemento [ReferenceItemId](https://msdn.microsoft.com/library/8fd4bb12-a94b-43f5-be3b-f435684e311d%28Office.15%29.aspx) indica el elemento que se va a cancelar, y puede ser el identificador de elemento de un patrón recurrente o una sola ocurrencia. 
  
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

En este ejemplo se utiliza la **operación CreateItem** con un elemento [DeclineItem](https://msdn.microsoft.com/library/2d8d2389-924e-4d03-a324-35d56cf0d6b1%28Office.15%29.aspx) para rechazar una reunión para la que el usuario no es el organizador. Como en el ejemplo anterior, el valor del elemento **ReferenceItemId** indica el elemento que se va a rechazar, y puede ser el identificador de elemento de un patrón recurrente o una sola ocurrencia. 
  
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

En este ejemplo se usa la [operación DeleteItem](https://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx) para eliminar una única ocurrencia de una cita sin asistentes. La repetición que se va a eliminar se especifica mediante el elemento [OccurrenceItemId](https://msdn.microsoft.com/library/4a15bbc3-5b93-4193-b9ec-da32f0a9a552%28Office.15%29.aspx) , que se crea a partir del identificador de elemento del patrón recurrente y el índice de la ocurrencia. 
  
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

Tenga en cuenta que puede obtener el mismo resultado si reemplaza el elemento **OccurrenceItemId** con un elemento [Itemid](https://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) que contenga el identificador de elemento de la ocurrencia, tal como se muestra. 
  
```XML
<m:ItemIds>
  <t:ItemId Id="AAMkADA7..." ChangeKey="DwAAABYA..." />
</m:ItemIds>

```

## <a name="see-also"></a>Vea también


- [Patrones de periodicidad y EWS](recurrence-patterns-and-ews.md)
    
- [Obtener acceso a una serie periódica mediante EWS en Exchange](how-to-access-a-recurring-series-by-using-ews-in-exchange.md)
    
- [Crear una serie periódica mediante EWS en Exchange](how-to-create-a-recurring-series-by-using-ews-in-exchange.md)
    
- [Actualizar una serie periódica mediante EWS](how-to-update-a-recurring-series-by-using-ews.md)
    
- [Actualizar una serie periódica mediante EWS en Exchange](how-to-update-a-recurring-series-by-using-ews-in-exchange.md)
    
- [Calendarios y EWS en Exchange](calendars-and-ews-in-exchange.md)
    
- [Crear citas y reuniones mediante EWS en Exchange 2013](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md)
    
- [Eliminar citas y cancelar reuniones mediante EWS en Exchange](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md)
    

