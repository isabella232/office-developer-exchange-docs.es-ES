---
title: Actualizar una serie periódica mediante EWS en Exchange
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: c922072f-ce33-4bff-97b0-1c1d0f9b880d
description: Obtenga información sobre cómo actualizar una serie completa a la vez mediante la API administrada de EWS o EWS en Exchange.
ms.openlocfilehash: 253bc7da176a954480db97e303393fecdda54892
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44527617"
---
# <a name="update-a-recurring-series-by-using-ews-in-exchange"></a>Actualizar una serie periódica mediante EWS en Exchange

Obtenga información sobre cómo actualizar una serie completa a la vez mediante la API administrada de EWS o EWS en Exchange.
  
Puede usar la API administrada de EWS o EWS para actualizar una serie periódica actualizando la serie completa o [actualizando una sola ocurrencia](how-to-update-a-recurring-series-by-using-ews.md). En este artículo se explica cómo actualizar toda la serie a la vez.
  
En general, la actualización de una serie periódica es muy similar a [la modificación de una sola cita](how-to-update-appointments-and-meetings-by-using-ews-in-exchange.md). Se usan los mismos métodos y operaciones, pero se usa el identificador de elemento de la serie maestro periódico. En algunos casos, es posible que no comience con el maestro periódico y que necesite [Buscar el identificador de elemento del maestro recurrente](how-to-access-a-recurring-series-by-using-ews-in-exchange.md).
  
Sin embargo, hay una diferencia clave que hay que tener en cuenta al actualizar una serie periódica: actualizar el patrón de periodicidad. La actualización del patrón de periodicidad solo es posible con el patrón recurrente, y los cambios en el patrón pueden agregar o quitar repeticiones. Por ejemplo, si se modifica la propiedad [recurrence. EndDate](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.recurrence.enddate%28v=exchg.80%29.aspx) a una fecha posterior a su valor actual, se vuelve a evaluar el patrón de periodicidad y se pueden agregar repeticiones adicionales. 
  
## <a name="modify-all-occurrences-in-a-series-by-using-the-ews-managed-api"></a>Modificar todas las repeticiones de una serie mediante la API administrada de EWS

Para modificar todas las ocurrencias de una serie:
  
1. Enlazar con el patrón periódico de la serie mediante el método [appointment. BindToRecurringMaster](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.appointment.bindtorecurringmaster%28v=exchg.80%29.aspx) o [appointment. bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) en un patrón recurrente. 
    
2. Actualice las propiedades en el objeto periódico maestro de [citas](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) . 
    
3. Guarde los cambios en el patrón periódico mediante el método [appointment. Save](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.appointment.save%28v=exchg.80%29.aspx) . 
    
En el siguiente ejemplo se actualiza una serie periódica para cambiar la ubicación, agregar un asistente y modificar el patrón de periodicidad. En este ejemplo se supone que el objeto [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) pasado en el parámetro _Service_ se ha inicializado con valores válidos en las propiedades [Credentials](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.credentials%28v=exchg.80%29.aspx) y [URL](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.url%28v=exchg.80%29.aspx) . El parámetro _recurringAppointment_ es un objeto **appointment** enlazado a una ocurrencia o al patrón recurrente para que se actualice la serie. 
  
```cs
using Microsoft.Exchange.WebServices.Data;
public static bool UpdateRecurringSeries(ExchangeService service, Appointment recurringAppointment)
{
    Appointment recurringMaster = null;
    // If the item is a single appointment, fail.
    if (recurringAppointment.AppointmentType == AppointmentType.Single)
    {
        Console.WriteLine("ERROR: The item to delete is not part of a recurring series.");
        return false;
    }
    // Check the Appointment that was passed. Is it
    // an occurrence or the recurring master?
    if (recurringAppointment.AppointmentType != AppointmentType.RecurringMaster)
    {
        // If an occurrence was passed in, bind to the master.
        try
        {
            // This method results in a call to EWS.
            recurringMaster = Appointment.BindToRecurringMaster(service, recurringAppointment.Id);
        }
        catch (Exception ex)
        {
            Console.WriteLine("Couldn't bind to master: {0}", ex.Message);
            return false;
        }
    }
    else
    {
        // Bind to the appointment to load all properties.
        // This method results in a call to EWS.
        recurringMaster = Appointment.Bind(service, recurringAppointment.Id);
    }
    // Basic updates. These kinds of updates are the same
    // as if you were updating a single appointment.
    // Update the location. All occurrences will update to this new location.
    recurringMaster.Location = "Conference Room 2";
    // Add an attendee.
    Attendee newAttendee = new Attendee("sadie@contoso.com");
    recurringMaster.RequiredAttendees.Add(newAttendee);
    // Changes to the recurrence. This is only applicable to a recurring
    // master.
    // If the series has an end date, extend the series to add two more occurrences.
    if (recurringMaster.Recurrence.HasEnd)
    {
        // NumberOfOccurrences is only set if the user created the
        // appointment with a set number of occurrences.
        // Otherwise, there's a start and end date.
        if (recurringMaster.Recurrence.NumberOfOccurrences != null)
        {
            recurringMaster.Recurrence.NumberOfOccurrences += 2;
        }
        else
        {
            // This is a bit more complicated if you want to add two more
            // occurrences. You need to calculate a new end date.
            Type recurrenceType = recurringMaster.Recurrence.GetType();
            switch (recurrenceType.Name)
            {
                case "DailyPattern":
                    recurringMaster.Recurrence.EndDate =
                        recurringMaster.Recurrence.EndDate.Value.AddDays(2);
                    break;
                case "WeeklyPattern":
                    recurringMaster.Recurrence.EndDate =
                        recurringMaster.Recurrence.EndDate.Value.AddDays(14);
                    break;
                case "YearlyPattern":
                    recurringMaster.Recurrence.EndDate =
                        recurringMaster.Recurrence.EndDate.Value.AddYears(2);
                    break;
                default:
                    // Do nothing here. There are other recurrence
                    // types but for simplicity, these aren't covered.
                    break;
            }
        }
    }
    else
    {
        // If it has no end, set an end date to 2 weeks from today.
        recurringMaster.Recurrence.EndDate = DateTime.Now.AddDays(14);
    }
    // Update the series.
    try
    {
        // This method results in a call to EWS.
        recurringMaster.Update(ConflictResolutionMode.AutoResolve);
    }
    catch (Exception ex)
    {
        Console.WriteLine("Error updating series: {0}", ex.Message);
        return false;
    }
    return true;
}
```

## <a name="modify-all-occurrences-in-a-series-by-using-ews"></a>Modificar todas las repeticiones de una serie mediante EWS

Para modificar todas las repeticiones de una serie, debe usar la [operación UpdateItem](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) con el identificador de elemento del patrón recurrente en el elemento [Itemid](https://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) de la solicitud. La estructura de la solicitud es la misma que una solicitud para actualizar una única cita. 
  
En el siguiente ejemplo se actualiza la serie periódica de las siguientes maneras:
  
- Actualiza la ubicación de la serie estableciendo el elemento [Location](https://msdn.microsoft.com/library/3fcf7133-ae1c-47b4-a187-660045f71df0%28Office.15%29.aspx) . 
    
- Actualiza los asistentes estableciendo el elemento [RequiredAttendees](https://msdn.microsoft.com/library/422f8d44-b0eb-49ca-af0f-0e22b54c78d2%28Office.15%29.aspx) . 
    
- Actualiza la periodicidad estableciendo el elemento [recurrence (RecurrenceType)](https://msdn.microsoft.com/library/3d1c2c1c-4103-47ce-ad3c-ad16ec6e9b12%28Office.15%29.aspx) . 
    
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
    <m:UpdateItem MessageDisposition="SaveOnly" ConflictResolution="AutoResolve" SendMeetingInvitationsOrCancellations="SendToAllAndSaveCopy">
      <m:ItemChanges>
        <t:ItemChange>
          <t:ItemId Id="AAMkADA5..." ChangeKey="DwAAABYA..." />
          <t:Updates>
            <t:SetItemField>
              <t:FieldURI FieldURI="calendar:Location" />
              <t:CalendarItem>
                <t:Location>Conference Room 2</t:Location>
              </t:CalendarItem>
            </t:SetItemField>
            <t:SetItemField>
              <t:FieldURI FieldURI="calendar:RequiredAttendees" />
              <t:CalendarItem>
                <t:RequiredAttendees>
                  <t:Attendee>
                    <t:Mailbox>
                      <t:Name>Mack Chaves</t:Name>
                      <t:EmailAddress>mack@contoso.com</t:EmailAddress>
                      <t:RoutingType>SMTP</t:RoutingType>
                    </t:Mailbox>
                  </t:Attendee>
                  <t:Attendee>
                    <t:Mailbox>
                      <t:Name>Sadie Daniels</t:Name>
                      <t:EmailAddress>sadie@contoso.com</t:EmailAddress>
                      <t:RoutingType>SMTP</t:RoutingType>
                    </t:Mailbox>
                  </t:Attendee>
                </t:RequiredAttendees>
              </t:CalendarItem>
            </t:SetItemField>
            <t:SetItemField>
              <t:FieldURI FieldURI="calendar:Recurrence" />
              <t:CalendarItem>
                <t:Recurrence>
                  <t:WeeklyRecurrence>
                    <t:Interval>1</t:Interval>
                    <t:DaysOfWeek>Tuesday</t:DaysOfWeek>
                  </t:WeeklyRecurrence>
                  <t:EndDateRecurrence>
                    <t:StartDate>2014-05-06</t:StartDate>
                    <t:EndDate>2014-06-22-04:00</t:EndDate>
                  </t:EndDateRecurrence>
                </t:Recurrence>
              </t:CalendarItem>
            </t:SetItemField>
            <t:SetItemField>
              <t:FieldURI FieldURI="calendar:MeetingTimeZone" />
              <t:CalendarItem>
                <t:MeetingTimeZone TimeZoneName="Pacific Standard Time" />
              </t:CalendarItem>
            </t:SetItemField>
          </t:Updates>
        </t:ItemChange>
      </m:ItemChanges>
    </m:UpdateItem>
  </soap:Body>
</soap:Envelope>
```

El servidor responde con un elemento [UpdateItemResponse](https://msdn.microsoft.com/library/023b79b4-c675-4669-9112-d85499ec4fc4%28Office.15%29.aspx) que incluye un elemento [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) con un valor de **NoError**, que indica que la actualización se realizó correctamente.
  
## <a name="see-also"></a>Vea también


- [Calendarios y EWS en Exchange](calendars-and-ews-in-exchange.md)
    
- [Patrones de periodicidad y EWS](recurrence-patterns-and-ews.md)
    
- [Actualizar citas y reuniones mediante EWS en Exchange](how-to-update-appointments-and-meetings-by-using-ews-in-exchange.md)
    
- [Actualizar una serie periódica mediante EWS](how-to-update-a-recurring-series-by-using-ews.md)
    
- [Obtener acceso a una serie periódica mediante EWS en Exchange](how-to-access-a-recurring-series-by-using-ews-in-exchange.md)
    

