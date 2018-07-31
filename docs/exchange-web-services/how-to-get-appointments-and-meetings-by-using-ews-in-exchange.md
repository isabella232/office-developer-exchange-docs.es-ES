---
title: Obtener las citas y reuniones con EWS en Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 1bae582a-8cb3-4e77-be2a-7e107fad26fe
description: Obtenga información sobre cómo obtener las citas y reuniones con la API administrada de EWS o EWS en Exchange.
ms.openlocfilehash: c78d70ca2266bd192b82f644d902ad8c958d2d4a
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/28/2018
ms.locfileid: "21353696"
---
# <a name="get-appointments-and-meetings-by-using-ews-in-exchange"></a>Obtener las citas y reuniones con EWS en Exchange

Obtenga información sobre cómo obtener las citas y reuniones con la API administrada de EWS o EWS en Exchange.
  
Puede recuperar las citas y reuniones desde una carpeta Calendario mediante el método de la API administrada de EWS [CalendarFolder.FindAppointments](http://msdn.microsoft.com/en-us/library/dd636179%28v=exchg.80%29.aspx) o la operación de EWS [FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) . 
  
## <a name="get-appointments-by-using-the-ews-managed-api"></a>Obtener las citas mediante el uso de la API administrada de EWS
<a name="bk_retrieveappsEWSMA"> </a>

En el ejemplo de código siguiente se muestra cómo usar la API administrada de EWS para recuperar las citas de un usuario que se dividen entre un inicio especificada y la hora de finalización.
  
```cs
       // Initialize values for the start and end times, and the number of appointments to retrieve.
            DateTime startDate = DateTime.Now;
            DateTime endDate = startDate.AddDays(30);
            const int NUM_APPTS = 5;
            // Initialize the calendar folder object with only the folder ID. 
            CalendarFolder calendar = CalendarFolder.Bind(service, WellKnownFolderName.Calendar, new PropertySet());
            // Set the start and end time and number of appointments to retrieve.
            CalendarView cView = new CalendarView(startDate, endDate, NUM_APPTS);
            // Limit the properties returned to the appointment's subject, start time, and end time.
            cView.PropertySet = new PropertySet(AppointmentSchema.Subject, AppointmentSchema.Start, AppointmentSchema.End);
            // Retrieve a collection of appointments by using the calendar view.
            FindItemsResults<Appointment> appointments = calendar.FindAppointments(cView);
            Console.WriteLine("\nThe first " + NUM_APPTS + " appointments on your calendar from " + startDate.Date.ToShortDateString() + 
                              " to " + endDate.Date.ToShortDateString() + " are: \n");
            
            foreach (Appointment a in appointments)
            {
                Console.Write("Subject: " + a.Subject.ToString() + " ");
                Console.Write("Start: " + a.Start.ToString() + " ");
                Console.Write("End: " + a.End.ToString());
                Console.WriteLine();
            }

```

<br/>

El siguiente es el resultado del ejemplo de código.
  
```text
The first five appointments on your calendar from 8/21/2013 to 9/20/2013 are: 
  
Subject: Contoso devs team meeting Start: 8/21/2013 12:30:00 PM End: 8/21/2013 1:00:00 PM
  
Subject: Daily status meeting Start: 8/21/2013 1:00:00 PM End: 8/21/2013 2:00:00 PM
  
Subject: Lunch with sales team Start: 8/21/2013 2:30:00 PM End: 8/21/2013 3:30:00 PM
  
Subject: Tennis at the club Start: 8/22/2013 11:00:00 AM End: 8/22/2013 12:00:00 PM
  
Subject: Online training webcast: 8/22/2013 2:00:00 PM End: 8/22/2013 3:00:00 PM
```

## <a name="get-appointments-by-using-ews"></a>Obtener las citas mediante el uso de EWS
<a name="bk_xml"> </a>

El siguiente código XML muestra una solicitud de operación [GetFolder](http://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) para devolver un identificador de la carpeta para la operación [FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) . 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
       xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
       xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
       xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
  </soap:Header>
  <soap:Body>
    <m:GetFolder>
      <m:FolderShape>
        <t:BaseShape>IdOnly</t:BaseShape>
      </m:FolderShape>
      <m:FolderIds>
        <t:DistinguishedFolderId Id="calendar" />
      </m:FolderIds>
    </m:GetFolder>
  </soap:Body>
</soap:Envelope>
```

<br/>

El siguiente código XML muestra la respuesta **GetFolder** . Tenga en cuenta que los atributos **FolderID** y **ChangeKey** son más cortos para mejorar la legibilidad. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="731" MinorBuildNumber="10" Version="V2_3" 
 xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
 xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
 xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetFolderResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
 xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:GetFolderResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Folders>
            <t:CalendarFolder>
              <t:FolderId Id="AAMk" ChangeKey="AgAA" />
            </t:CalendarFolder>
          </m:Folders>
        </m:GetFolderResponseMessage>
      </m:ResponseMessages>
    </m:GetFolderResponse>
  </s:Body>
</s:Envelope>
```

<br/>

El siguiente código XML muestra la solicitud **FindItem** que se usa para devolver las citas solicitadas. Tenga en cuenta que los atributos **FolderID** y **ChangeKey** son más cortos para mejorar la legibilidad. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
       xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
       xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
       xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
  </soap:Header>
  <soap:Body>
    <m:FindItem Traversal="Shallow">
      <m:ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="item:Subject" />
          <t:FieldURI FieldURI="calendar:Start" />
          <t:FieldURI FieldURI="calendar:End" />
        </t:AdditionalProperties>
      </m:ItemShape>
      <m:CalendarView MaxEntriesReturned="5" StartDate="2013-08-21T17:30:24.127Z" EndDate="2013-09-20T17:30:24.127Z" />
      <m:ParentFolderIds>
        <t:FolderId Id="AAMk" ChangeKey="AgAA" />
      </m:ParentFolderIds>
    </m:FindItem>
  </soap:Body>
</soap:Envelope>
```

<br/>

El siguiente código XML muestra la respuesta **FindItem** . Tenga en cuenta que los atributos **ItemID** y **ChangeKey** son más cortos para mejorar la legibilidad. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="731" MinorBuildNumber="10" Version="V2_3" 
 xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
 xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
 xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
 xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:FindItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:FindItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:RootFolder TotalItemsInView="33" IncludesLastItemInRange="false">
            <t:Items>
              <t:CalendarItem>
                <t:ItemId Id="AAMk" ChangeKey="DwAA" />
                <t:Subject>Contoso devs team meeting</t:Subject>
                <t:Start>2013-08-21T19:30:00Z</t:Start>
                <t:End>2013-08-21T20:00:00Z</t:End>
              </t:CalendarItem>
              <t:CalendarItem>
                <t:ItemId Id="AAMk" ChangeKey="DwAA" />
                <t:Subject>Daily status meeting</t:Subject>
                <t:Start>2013-08-21T20:00:00Z</t:Start>
                <t:End>2013-08-21T21:00:00Z</t:End>
              </t:CalendarItem>
              <t:CalendarItem>
                <t:ItemId Id="AAMk" ChangeKey="DwAA" />
                <t:Subject>Lunch with sales team</t:Subject>
                <t:Start>2013-08-21T21:30:00Z</t:Start>
                <t:End>2013-08-21T22:30:00Z</t:End>
              </t:CalendarItem>
              <t:CalendarItem>
                <t:ItemId Id="AAMk" ChangeKey="DwAA" />
                <t:Subject>Tennis at the club</t:Subject>
                <t:Start>2013-08-22T18:00:00Z</t:Start>
                <t:End>2013-08-22T19:00:00Z</t:End>
              </t:CalendarItem>
              <t:CalendarItem>
                <t:ItemId Id="AAMkA" ChangeKey="DwAA" />
                <t:Subject>Online training webcast</t:Subject>
                <t:Start>2013-08-22T21:00:00Z</t:Start>
                <t:End>2013-08-22T22:00:00Z</t:End>
              </t:CalendarItem>
            </t:Items>
          </m:RootFolder>
        </m:FindItemResponseMessage>
      </m:ResponseMessages>
    </m:FindItemResponse>
  </s:Body>
</s:Envelope>
```

## <a name="recurring-meetings-and-the-calendar-view"></a>Reuniones periódicas y la vista de calendario
<a name="bk_recurring"> </a>

La carpeta de calendario es un poco diferente de otras carpetas en un buzón debido a que no son elementos real en el buzón de repeticiones en una serie periódica y las excepciones de una serie periódica, pero en su lugar se almacenan internamente como datos adjuntos a un maestro periódico. Esto significa, si bien puede crear una solicitud de EWS devuelve valores entre un conjunto de **start** y **end** valores mediante el uso de uno de la API administrada de EWS **FindItems** sobrecargan métodos, como [ExchangeService.FindItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) o la [EWS FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) operación, EWS no tendría un aspecto a través de la tabla de datos adjuntos de todos los elementos de calendario para buscar excepciones y repeticiones. 
  
En su lugar, ¿qué desea hacer en realidad es algo parecido a la aplicación de una *Dataview* en una unión de dos tablas SQL, con un objeto [CalendarView](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.calendarview%28v=exchg.80%29.aspx) . Tenga en cuenta que por motivos de rendimiento, se recomienda que utilice la propiedad [PropertySet](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.propertyset%28v=exchg.80%29.aspx) para limitar el tamaño de la respuesta de forma que indica el número de citas o reuniones que desea devolver, así como las propiedades específicas que desee. 
  
## <a name="see-also"></a>Vea también
<a name="bk_additional"> </a>

- [Calendarios y EWS en Exchange](calendars-and-ews-in-exchange.md)   
- [Crear citas y reuniones mediante el uso de EWS en Exchange 2013](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md)  
- [Actualizar las citas y reuniones con EWS en Exchange](how-to-update-appointments-and-meetings-by-using-ews-in-exchange.md)  
- [Eliminar las citas y cancelar reuniones mediante el uso de EWS en Exchange](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md) 
- [Desarrollo de clientes de servicios web de Exchange](develop-web-service-clients-for-exchange.md)
    

