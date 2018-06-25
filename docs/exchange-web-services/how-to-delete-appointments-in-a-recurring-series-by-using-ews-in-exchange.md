---
title: Eliminar las citas de una serie periódica mediante el uso de EWS en Exchange
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: a9d5244a-bc4a-4e9c-9c6c-ff361e04cbf8
description: Obtenga información sobre cómo eliminar las citas de una serie periódica mediante el uso de la API administrada de EWS o EWS en Exchange.
ms.openlocfilehash: 5e4d95058808adf8db159000bdf90c1f92945338
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763076"
---
# <a name="delete-appointments-in-a-recurring-series-by-using-ews-in-exchange"></a>Eliminar las citas de una serie periódica mediante el uso de EWS en Exchange

Obtenga información sobre cómo eliminar las citas de una serie periódica mediante el uso de la API administrada de EWS o EWS en Exchange.
  
Puede usar la API administrada de EWS o EWS para eliminar una serie de citas o reuniones, o de una sola instancia de la serie. El proceso que se utiliza para eliminar una serie completa es básicamente el mismo que el proceso que se utiliza para eliminar solo una sola aparición. Use los mismos métodos de API administrada de EWS u operaciones de EWS que se usa para [Eliminar una reunión o cita de una sola instancia](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md). La diferencia está en el identificador del elemento que se incluye en el método o la operación. Vamos a iniciar observando cómo ambos escenarios son los mismos. 
  
Para eliminar una serie periódica o una sola aparición de una serie periódica, necesita encontrar la aparición o la serie que desea eliminar y, a continuación, llamar al método apropiado u operación para quitarlo. Mientras que simplemente puede eliminar cualquier tipo de cita, se recomienda mantener actualizados de los asistentes o el organizador y cancelar las reuniones organizadas por el usuario y Rechazar convocatorias de reunión que el usuario no organizar.
  
¿Cómo los escenarios son diferentes? Todos los detalles sobre el objeto de [cita](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) que se usa para invocar el método (para la API administrada de EWS) o el identificador de elemento incluirlo en la solicitud de operación (de EWS). Para eliminar una serie completa, necesita el identificador de objeto o el elemento de **cita** para el patrón de periódico. Para eliminar una sola aparición, necesita el identificador de objeto o el elemento de **cita** para la repetición. 
  
## <a name="delete-a-recurring-appointment-by-using-the-ews-managed-api"></a>Eliminación de una cita periódica mediante el uso de la API administrada de EWS

En este ejemplo se supone que se han autenticado a un servidor de Exchange y ha adquirido un objeto [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) con el nombre de **servicio**. El parámetro _recurringItem_ es un objeto de **cita** para el patrón de periódico o una sola aparición. El parámetro _deleteEntireSeries_ indica si se debe eliminar toda la serie que forma parte de la _recurringItem_ . 
  
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

Para poder utilizar este ejemplo, necesita [enlazar a una ocurrencia o el patrón periódico](how-to-access-a-recurring-series-by-using-ews-in-exchange.md)y pase el objeto de **cita** resultante al método. Tenga en cuenta que si tiene acceso a las citas mediante el uso de una clase [CalendarView](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.calendarview%28v=exchg.80%29.aspx) , los elementos resultantes son todas las apariciones único. Por el contrario, si usa la clase [artículoVer](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.itemview%28v=exchg.80%29.aspx) , los elementos resultantes son todos los patrones periódicos. 
  
## <a name="delete-a-recurring-appointment-by-using-ews"></a>Eliminación de una cita periódica mediante el uso de EWS

Eliminación de una serie periódica mediante el uso de EWS es lo mismo que [Eliminar una reunión de instancia única](how-to-delete-appointments-in-a-recurring-series-by-using-ews-in-exchange.md). De hecho, las solicitudes SOAP tienen el mismo formato. Una vez más, la clave es el identificador de elemento utilizado en la solicitud. Si el identificador de elemento corresponde al patrón de periódica, se eliminará toda la serie. Si el identificador de elemento corresponde a una sola aparición, se eliminará la única aparición.
  
> [!NOTE]
> En los ejemplos de código siguientes, se acortan los atributos **ItemId**, **ChangeKey**y **RecurringMasterId** para mejorar la legibilidad. 
  
En este ejemplo se usa la [operación CreateItem](http://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) con un elemento de [CancelCalendarItem](http://msdn.microsoft.com/library/a2046402-a176-44d5-b4b3-adb696581935%28Office.15%29.aspx) para cancelar una reunión para la que el usuario es el organizador. El valor del elemento [ReferenceItemId](http://msdn.microsoft.com/library/8fd4bb12-a94b-43f5-be3b-f435684e311d%28Office.15%29.aspx) indica el elemento que se va a cancelar, y puede ser el identificador de elemento de un patrón periódico o una sola aparición. 
  
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

En este ejemplo se usa la **operación CreateItem** con un elemento de [DeclineItem](http://msdn.microsoft.com/library/2d8d2389-924e-4d03-a324-35d56cf0d6b1%28Office.15%29.aspx) para rechazar una reunión para la que el usuario no es el organizador. Como se muestra en el ejemplo anterior, el valor del elemento **ReferenceItemId** indica el elemento que se va a rechazar, y puede ser el identificador de elemento de un patrón periódico o una sola aparición. 
  
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

En este ejemplo se usa la [operación DeleteItem](http://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx) para eliminar una sola aparición de una cita sin asistentes. La aparición para eliminar se especifica mediante el elemento [OccurrenceItemId](http://msdn.microsoft.com/library/4a15bbc3-5b93-4193-b9ec-da32f0a9a552%28Office.15%29.aspx) , que se construye a partir del identificador de elemento del patrón periódico y el índice de la aparición. 
  
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
    <m:DeleteItem DeleteType="MoveToDeletedItems" SendMeetingCancellations="SendToAllAndSaveCopy">
      <m:ItemIds>
        <t:OccurrenceItemId RecurringMasterId="AAMkADA8..." InstanceIndex="3" />
      </m:ItemIds>
    </m:DeleteItem>
  </soap:Body>
</soap:Envelope>
```

Tenga en cuenta que puede obtener el mismo resultado mediante el reemplazo del elemento **OccurrenceItemId** con un elemento de [ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) que contiene el identificador de elemento de la aparición, tal como se muestra. 
  
```XML
<m:ItemIds>
  <t:ItemId Id="AAMkADA7..." ChangeKey="DwAAABYA..." />
</m:ItemIds>

```

## <a name="see-also"></a>Vea también


- [Patrones de periodicidad y EWS](recurrence-patterns-and-ews.md)
    
- [Obtener acceso a una serie periódica mediante el uso de EWS en Exchange](how-to-access-a-recurring-series-by-using-ews-in-exchange.md)
    
- [Creación de una serie periódica mediante EWS en Exchange](how-to-create-a-recurring-series-by-using-ews-in-exchange.md)
    
- [Actualización de una serie periódica mediante el uso de EWS](how-to-update-a-recurring-series-by-using-ews.md)
    
- [Actualización de una serie periódica mediante el uso de EWS en Exchange](how-to-update-a-recurring-series-by-using-ews-in-exchange.md)
    
- [Calendarios y EWS en Exchange](calendars-and-ews-in-exchange.md)
    
- [Crear citas y reuniones mediante el uso de EWS en Exchange 2013](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md)
    
- [Eliminar las citas y cancelar reuniones mediante el uso de EWS en Exchange](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md)
    

