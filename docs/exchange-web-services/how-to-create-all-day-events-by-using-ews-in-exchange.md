---
title: Crear eventos de todo el día mediante EWS en Exchange
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 0fcb484b-4ffc-41a5-aeed-8c797766b70c
description: Obtenga información sobre cómo crear eventos de todo el día mediante la API administrada ews o EWS en Exchange.
ms.openlocfilehash: 8769999907df46f519355a36fdf409f9ad347330
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59521224"
---
# <a name="create-all-day-events-by-using-ews-in-exchange"></a>Crear eventos de todo el día mediante EWS en Exchange

Obtenga información sobre cómo crear eventos de todo el día mediante la API administrada ews o EWS en Exchange.
  
Los eventos de todo el día proporcionan una forma de representar algo que sucede durante todo un día o varios días, por ejemplo, días festivos o de vacaciones. Crear eventos durante todo el día con la API administrada ews o EWS es un complemento. Es como crear [citas,](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md)pero con algunos cambios pequeños.
  
## <a name="setting-start-and-end-times"></a>Establecer las horas de inicio y finalización

Por definición, los eventos de todo el día comienzan a medianoche en un día específico y terminan 24 horas (o un múltiplo de 24 horas) más tarde. Sin embargo, la API administrada ews y EWS permiten especificar horas que no son medianoche al crear eventos de todo el día. Esto puede provocar un comportamiento no intencionado si no sabe cómo se traducen estas veces en el servidor.
  
Cuando se recibe una solicitud para crear un nuevo evento [](time-zones-and-ews-in-exchange.md)de todo el día con horas de inicio y finalización que no son medianoche (en la zona horaria de la solicitud o cita), esas horas se ajustan a medianoche en la zona horaria adecuada de acuerdo con las siguientes reglas:
  
- Las horas de inicio que no son de medianoche se ajustan a la medianoche anterior a la hora especificada. Por ejemplo, a la 1:00 p.m. del 6 de junio se ajusta a las 12:00 a.m. del 6 de junio.
    
- Las horas de finalización que no son de medianoche se ajustan a la medianoche después de la hora especificada. Por ejemplo, a la 1:00 p.m. del 6 de junio se ajusta a las 12:00 a.m. del 7 de junio.
    
Por lo tanto, el evento de todo el día que cree siempre incluye la hora de inicio y finalización que especifique, pero puede reclamar tiempo adicional en el calendario del usuario debido al cambio a medianoche. Dado que el servidor ajustará la hora de inicio y finalización a medianoche, se recomienda especificar la hora de inicio y finalización a medianoche para evitar cualquier cambio no intencionado en las horas.
  
También es importante tener en cuenta las zonas horarias al crear eventos de todo el día. Dado que el servidor Exchange aplica una hora de inicio y finalización de medianoche en la zona horaria de la solicitud o cita, ver que el evento de todo el día en un cliente configurado para una zona horaria diferente puede producir resultados inesperados. Según el cliente, puede aparecer como un evento de todo el día con días adicionales que no tenía intención de incluir, o puede que no aparezca como un evento de todo el día por completo. Debido a esto, se recomienda usar la zona horaria preferida del usuario siempre que sea posible al crear eventos de todo el día.
  
## <a name="create-an-all-day-event-by-using-the-ews-managed-api"></a>Crear un evento de todo el día mediante la API administrada de EWS

En el ejemplo siguiente se muestra cómo usar la API administrada de EWS para crear un evento de todo el día, a partir de la fecha especificada por el parámetro _startDate_ y que dura el número de días especificado por el _parámetro numDays._ Tenga en cuenta que la cita se creará en la zona horaria especificada por la [propiedad ExchangeService.TimeZone.](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.timezone%28v=exchg.80%29.aspx) En este ejemplo se supone que el objeto [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) pasado en el parámetro _service_ se ha inicializado con valores válidos para las [propiedades Credentials](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.credentials%28v=exchg.80%29.aspx) y [Url.](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.url%28v=exchg.80%29.aspx) 
  
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

## <a name="create-an-all-day-event-by-using-ews"></a>Crear un evento de todo el día mediante EWS

En el ejemplo siguiente se muestra una solicitud de operación [CreateItem](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) de EWS para crear un evento de todo el día. La cita se crea en la zona horaria oriental, tal como se indica en el [elemento TimeZoneContext.](https://msdn.microsoft.com/library/573c462b-aa1d-4ba0-8852-e3f48b26873b%28Office.15%29.aspx) Observe que la parte de hora de los valores de los elementos [Start](https://msdn.microsoft.com/library/7cfe9979-c893-4f9b-b3a1-8f9e17515a4b%28Office.15%29.aspx) y [End](https://msdn.microsoft.com/library/72329821-32ff-495d-b6e5-fdc011003c2e%28Office.15%29.aspx) es a las 04:00Z, que se convierte a medianoche en la zona horaria oriental durante el horario de verano. 
  
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

## <a name="see-also"></a>Ver también


- [Calendarios y EWS en Exchange](calendars-and-ews-in-exchange.md)
    
- [Crear citas y reuniones mediante EWS en Exchange 2013](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md)
    
- [Zonas horarias y EWS en Exchange](time-zones-and-ews-in-exchange.md)
    

