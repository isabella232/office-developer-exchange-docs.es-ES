---
title: Crear eventos de día completo mediante el uso de EWS en Exchange
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 0fcb484b-4ffc-41a5-aeed-8c797766b70c
description: Obtenga información sobre cómo crear eventos de día completo mediante la API administrada de EWS o EWS en Exchange.
ms.openlocfilehash: 0547fdf0ca92ba0648caeb5de6940d90d2a8ff46
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763047"
---
# <a name="create-all-day-events-by-using-ews-in-exchange"></a>Crear eventos de día completo mediante el uso de EWS en Exchange

Obtenga información sobre cómo crear eventos de día completo mediante la API administrada de EWS o EWS en Exchange.
  
Eventos de todo el día proporcionan una forma de representar algo que sucede para todo un día o varios días, por ejemplo, un día festivo o días de vacaciones. Crear eventos de día completo con la API administrada de EWS o EWS es un complemento. Es igual que [crear citas](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md), pero con unos pequeños cambios.
  
## <a name="setting-start-and-end-times"></a>Configuración de horas de inicio y finalización

Por definición, inician eventos de día completo en la medianoche en un día específico y end 24 horas (o un múltiplo de 24 horas) más adelante. Sin embargo, la API administrada de EWS y EWS permite especificar las horas que no sean medianoche al crear todos los eventos de día. Esto puede provocar un comportamiento imprevisto si no tener en cuenta cómo traducir estos tiempos en el servidor.
  
Cuando se recibe una solicitud para crear un nuevo evento de día completo con los que no sean medianoche (en la [zona horaria de la solicitud o cita](time-zones-and-ews-in-exchange.md)) inicio o finalización, esas horas se ajustan a medianoche en la zona horaria adecuada según las reglas siguientes:
  
- Horas de inicio de la medianoche de no se ajustan a la medianoche antes de la hora especificada. Por ejemplo, 1:00 P.M. en 6 de junio obtiene ajustados a las 12:00 A.M. en 6 de junio.
    
- Hora de finalización de la medianoche de no se ajusta a la medianoche después de la hora especificada. Por ejemplo, 1:00 P.M. en 6 de junio obtiene ajustados a las 12:00 A.M. en 7 de junio.
    
Por lo que es el evento de día completo que se crea siempre incluidos la hora de inicio y finalización que especifique, pero es posible que el tiempo adicional de notificación en el usuario del calendario de vencimiento para el cambio a partir de la medianoche. Debido a que el servidor va a ajustar la hora de inicio y final a partir de la medianoche, se recomienda que especifique la hora de inicio y final en la medianoche para evitar los cambios no deseados en los tiempos de.
  
También es importante tener en cuenta las zonas horarias al crear eventos de día completo. Debido a que el Exchange server impone una medianoche inicio y hora en la zona horaria de la cita o la solicitud de finalización, la visualización de ese evento de día completo en un cliente configurado para una zona horaria diferente puede producir resultados inesperados. Dependiendo del cliente, puede aparecer como un evento de día completo con días adicionales que no tenía intención de incluir o no puede aparecer como un evento de día completo totalmente. Por este motivo, se recomienda usar el preferido zona horaria del usuario siempre que sea posible crear eventos de día completo.
  
## <a name="create-an-all-day-event-by-using-the-ews-managed-api"></a>Crear un evento de día completo mediante el uso de la API administrada de EWS

En el ejemplo siguiente se muestra cómo usar la API administrada de EWS para crear un evento de día completo, comenzando en la fecha especificada por el parámetro _startDate_ y una duración para el número de días especificado por el parámetro _numDays_ . Tenga en cuenta que se creará la cita en la zona horaria especificada por la propiedad [ExchangeService.TimeZone](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.timezone%28v=exchg.80%29.aspx) . En este ejemplo se da por supuesto que se ha inicializado el objeto [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) pasado en el parámetro de _servicio_ con los valores válidos para las propiedades de [las credenciales](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservicebase.credentials%28v=exchg.80%29.aspx) y [dirección Url](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.url%28v=exchg.80%29.aspx) . 
  
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

## <a name="create-an-all-day-event-by-using-ews"></a>Crear un evento de día completo mediante el uso de EWS

En el ejemplo siguiente se muestra una solicitud de EWS [operación CreateItem](http://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) para crear un evento de día completo. La cita se crea en la zona hora oriental, como se indica en el elemento [TimeZoneContext](http://msdn.microsoft.com/library/573c462b-aa1d-4ba0-8852-e3f48b26873b%28Office.15%29.aspx) . Tenga en cuenta que la parte de los valores de los elementos de [Inicio](http://msdn.microsoft.com/library/7cfe9979-c893-4f9b-b3a1-8f9e17515a4b%28Office.15%29.aspx) y [fin de](http://msdn.microsoft.com/library/72329821-32ff-495d-b6e5-fdc011003c2e%28Office.15%29.aspx) la hora son ambos 04:00Z, que se convierte a partir de la medianoche en la zona hora oriental durante el horario de verano. 
  
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
    
- [Crear citas y reuniones mediante el uso de EWS en Exchange 2013](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md)
    
- [Zonas horarias y EWS en Exchange](time-zones-and-ews-in-exchange.md)
    

