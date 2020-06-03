---
title: Patrones de periodicidad y EWS
manager: luken
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: fd9ef706-1e01-49fa-af6f-2f6d3e173c16
description: Obtenga información sobre los patrones de periodicidad y la serie periódica en Exchange.
ms.openlocfilehash: 681dfee7e0a66a483b8638810da5e4e0ac0f05ac
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459331"
---
# <a name="recurrence-patterns-and-ews"></a>Patrones de periodicidad y EWS

Obtenga información sobre los patrones de periodicidad y la serie periódica en Exchange.
  
Una serie periódica es una cita o reunión que se repite según un patrón definido. Una serie periódica puede tener un número específico de repeticiones o puede repetirse indefinidamente. Además, una serie periódica puede tener excepciones que no siguen el patrón del resto de las repeticiones y pueden tener ocurrencias que se han eliminado del patrón. Puede usar la API administrada de EWS y EWS para trabajar con la serie periódica y sus elementos de calendario asociados.
  
## <a name="recurring-calendar-items"></a>Elementos de calendario periódicos

Todos los elementos de calendario se dividen en una de las cuatro categorías siguientes:
  
- Elementos de calendario no periódicos
    
- Maestros periódicos
    
- Ocurrencias en una serie
    
- Instancias modificadas en una serie, conocidas como excepciones
    
En este artículo, analizaremos los tres tipos de elementos de calendario que forman parte de una serie periódica.
  
Es útil comprender cómo se implementan las series periódicas en el servidor Exchange. En lugar de crear un elemento diferente distinto para cada repetición en una serie periódica, el servidor crea solo un elemento real en el calendario, conocido como maestro periódico. El formato de un patrón recurrente es muy similar a una cita no recurrente, además de la información del patrón de periodicidad. A continuación, el servidor genera repeticiones según el patrón de periodicidad en respuesta a las solicitudes de información de la cita de los clientes, mediante un proceso denominado expansión. Estas ocurrencias generadas no se almacenan de forma permanente en el servidor. Esto es importante para comprender porque la forma en que se buscan los elementos del calendario determina la información que se recibe y si se produce la expansión.
  
## <a name="recurrence-patterns"></a>Patrones de periodicidad

La pieza clave para una serie periódica que hace que la expansión sea posible es el patrón de periodicidad. El patrón de periodicidad se encuentra en el patrón recurrente y describe un conjunto de criterios para calcular los repeticiones en función de la fecha y la hora del patrón recurrente.
  
**Tabla 1. Patrones de periodicidad disponibles**

|**Clase de API administrada de EWS**|**Elemento EWS**|**Ejemplos**|
|:-----|:-----|:-----|
|[Recurrence. DailyPattern](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.recurrence.dailypattern%28v=exchg.80%29.aspx) <br/> |[DailyRecurrence](https://msdn.microsoft.com/library/0aaf265d-b723-49c6-8e9c-9ba60141e9ab%28Office.15%29.aspx) <br/> |Repita todos los días.  <br/> Repetir cada dos días.  <br/> |
|[Recurrence. MonthlyPattern](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.recurrence.monthlypattern%28v=exchg.80%29.aspx) <br/> |[AbsoluteMonthlyRecurrence](https://msdn.microsoft.com/library/178fa0ae-9dfc-417f-933c-d657d31c2161%28Office.15%29.aspx) <br/> |Repetir cada mes el décimo día del mes.  <br/> Repita cada dos meses en el vigésimo primer día del mes.  <br/> |
|[Recurrence. RelativeMonthlyPattern](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.recurrence.relativemonthlypattern%28v=exchg.80%29.aspx) <br/> |[RelativeMonthlyRecurrence](https://msdn.microsoft.com/library/a76595db-7460-44ac-ac2a-53241caa33a7%28Office.15%29.aspx) <br/> |Repetir el segundo martes de cada mes.  <br/> Repita el tercer jueves del mes cada tres meses.  <br/> |
|[Recurrence. RelativeYearlyPattern](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.recurrence.relativeyearlypattern%28v=exchg.80%29.aspx) <br/> |[RelativeYearlyRecurrence](https://msdn.microsoft.com/library/25b67876-9979-4a30-a637-357ea10a93b8%28Office.15%29.aspx) <br/> |Repetir el primer lunes de agosto de cada año.  <br/> |
|[Recurrence. WeeklyPattern](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.recurrence.weeklypattern%28v=exchg.80%29.aspx) <br/> |[WeeklyRecurrence](https://msdn.microsoft.com/library/69c41dd5-597c-45bc-be3f-e2f2b5615aa3%28Office.15%29.aspx) <br/> |Repita cada lunes.  <br/> Repita cada martes y jueves cada dos semanas.  <br/> |
|[Recurrence. YearlyPattern](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.recurrence.yearlypattern%28v=exchg.80%29.aspx) <br/> |[AbsoluteYearlyRecurrence](https://msdn.microsoft.com/library/96f53e2c-3893-4f6e-a78a-ac179f45c5db%28Office.15%29.aspx) <br/> |Repetir el 1 de septiembre de cada año.  <br/> |
   
La otra información importante para un patrón de periodicidad es cuando finaliza la periodicidad. Esto puede expresarse como un número establecido de repeticiones, como una fecha de finalización o como sin fin.
  
**Tabla 2. Opciones para el final de una serie periódica**

|**Método o propiedad de la API administrada de EWS**|**Elemento EWS**|**Descripción**|
|:-----|:-----|:-----|
|[Recurrence. NumberOfOccurrences](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.recurrence.numberofoccurrences%28v=exchg.80%29.aspx) <br/> |[NumberedRecurrence](https://msdn.microsoft.com/library/53746909-ef21-4764-8715-a7769b943cca%28Office.15%29.aspx) <br/> |El valor de esta propiedad o elemento especifica el número de repeticiones.  <br/> |
|[Recurrence. EndDate](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.recurrence.enddate%28v=exchg.80%29.aspx) <br/> |[EndDateRecurrence](https://msdn.microsoft.com/library/a5ee2504-db84-49ee-870c-cca9269f2e26%28Office.15%29.aspx) <br/> |La última aparición en la serie cae en o antes de la fecha especificada por esta propiedad o elemento.  <br/> |
|[Recurrence. HasEnd](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.recurrence.hasend%28v=exchg.80%29.aspx) <br/> [Recurrence. NeverEnds](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.recurrence.neverends%28v=exchg.80%29.aspx) <br/> |[NoEndRecurrence](https://msdn.microsoft.com/library/ab2ebd9c-388e-45f1-abf9-56e293ef123b%28Office.15%29.aspx) <br/> |La serie no tiene fin.  <br/> |
   
## <a name="expanded-vs-non-expanded-views"></a>Vistas expandidas frente a vistas no expandidas

El uso del método **FindAppointments** en la API administrada de EWS (o la operación **FindItem** con un elemento **CalendarView** en EWS) invoca el proceso de expansión. De esta forma, se ocultan las citas maestras periódicas del conjunto de resultados y, en su lugar, se presenta una vista expandida de esa serie periódica. Las repeticiones y excepciones al patrón periódico que se encuentran dentro de los parámetros de la vista de calendario se incluyen en el conjunto de resultados. Por el contrario, si se usa el método **FindItems** en la API administrada de EWS (o la operación **FindItem** con un elemento **IndexedPageItemView** o **FractionalPageItemView** en EWS), no se invoca el proceso de expansión y no se incluyen las repeticiones ni las excepciones. Veamos un ejemplo de comparación de los dos métodos. 
  
**Tabla 3. Métodos y operaciones para buscar citas**

|**Método de la API administrada de EWS**|**Operación de EWS**|**¿Expande la serie?**|**Elementos incluidos en los resultados**|
|:-----|:-----|:-----|:-----|
|[ExchangeService. FindAppointments](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.findappointments%28v=exchg.80%29.aspx) <br/> |[Operación FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) con un elemento [CalendarView](https://msdn.microsoft.com/library/a4a953b8-0710-416c-95ef-59e51eba9982%28Office.15%29.aspx)  <br/> |Sí  <br/> |Citas no periódicas, ocurrencias únicas de una serie periódica y excepciones a la serie periódica  <br/> |
|[ExchangeService. FindItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) <br/> |[Operación FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) con un elemento [IndexedPageItemView](https://msdn.microsoft.com/library/6d1b0b04-cc35-4a57-bd7a-824136d14fda%28Office.15%29.aspx) o un elemento [FractionalPageItemView](https://msdn.microsoft.com/library/4111afec-35e7-4c6f-b291-9bbba603f633%28Office.15%29.aspx)  <br/> |No  <br/> |Citas no periódicas y citas maestras periódicas  <br/> |
   
Sadie acaba de firmar su hijo para el equipo de natación. El equipo se ha practicado cada miércoles por la mañana a las 8:30 A.M., a partir del 2 de julio, con la última práctica de 6 de agosto. Si no desea olvidarse de la práctica, Sadie agrega una cita periódica a su calendario para recordarla.
  
**Tabla 4. Cita periódica de Sadie**

|**Campo de cita**|**Valor**|
|:-----|:-----|
|Subject  <br/> |Práctica del equipo de nadar  <br/> |
|Iniciar  <br/> |2 de julio de 2014 8:30 A.M.  <br/> |
|End  <br/> |2 de julio de 2014 10:00 A.M.  <br/> |
|Repetitivo  <br/> |Todos los miércoles  <br/> |
|Última ocurrencia  <br/> |6 de agosto de 2014 8:30 A.M.  <br/> |
   
Un vistazo rápido a un calendario muestra que el equipo tendrá un total de seis prácticas. Sin embargo, no hay seis elementos de cita distintos en el calendario. En su lugar, solo hay una cita de patrón recurrente que representa la serie.
  
Veamos ahora cómo buscar citas en el calendario de Sadie que se produzcan dentro del mes de julio. El siguiente ejemplo de código usa el método **FindItems** en la API administrada de Exchange para generar una vista no expandida del calendario de Sadie. 
  
```cs
PropertySet propSet = new PropertySet(AppointmentSchema.Subject,
                                      AppointmentSchema.Location,
                                      AppointmentSchema.Start, 
                                      AppointmentSchema.End,
                                      AppointmentSchema.AppointmentType);
#region FindItems + ItemView method
ItemView itemView = new ItemView(100);
itemView.PropertySet = propSet;
List<SearchFilter> filterList = new List<SearchFilter>();
// Find appointments that start after midnight on July 1, 2014.
SearchFilter.IsGreaterThan startFilter = new SearchFilter.IsGreaterThan(AppointmentSchema.Start,
    new DateTime(2014, 7, 1));
// Find appointments that end before midnight on July 31, 2014
SearchFilter.IsLessThan endFilter = new SearchFilter.IsLessThan(AppointmentSchema.End,
    new DateTime(2014, 7, 31));
filterList.Add(startFilter);
filterList.Add(endFilter);
SearchFilter.SearchFilterCollection calendarFilter = new SearchFilter.SearchFilterCollection(LogicalOperator.And, filterList);
// This results in a call to EWS.
FindItemsResults<Item> results = service.FindItems(WellKnownFolderName.Calendar, calendarFilter, itemView);
foreach(Item appt in results.Items)
{
    Console.WriteLine(appt.Subject);
}
```

El código da como resultado la siguiente solicitud de [operación FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) con un elemento [IndexedPageItemView](https://msdn.microsoft.com/library/6d1b0b04-cc35-4a57-bd7a-824136d14fda%28Office.15%29.aspx) . 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
    xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
    xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
    xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
    <t:TimeZoneContext>
      <t:TimeZoneDefinition Id="Pacific Standard Time" />
    </t:TimeZoneContext>
  </soap:Header>
  <soap:Body>
    <m:FindItem Traversal="Shallow">
      <m:ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="item:Subject" />
          <t:FieldURI FieldURI="calendar:Location" />
          <t:FieldURI FieldURI="calendar:Start" />
          <t:FieldURI FieldURI="calendar:End" />
          <t:FieldURI FieldURI="calendar:CalendarItemType" />
        </t:AdditionalProperties>
      </m:ItemShape>
      <m:IndexedPageItemView MaxEntriesReturned="100" Offset="0" BasePoint="Beginning" />
      <m:Restriction>
        <t:And>
          <t:IsGreaterThan>
            <t:FieldURI FieldURI="calendar:Start" />
            <t:FieldURIOrConstant>
              <t:Constant Value="2014-07-01T07:00:00.000Z" />
            </t:FieldURIOrConstant>
          </t:IsGreaterThan>
          <t:IsLessThan>
            <t:FieldURI FieldURI="calendar:End" />
            <t:FieldURIOrConstant>
              <t:Constant Value="2014-07-31T07:00:00.000Z" />
            </t:FieldURIOrConstant>
          </t:IsLessThan>
        </t:And>
      </m:Restriction>
      <m:ParentFolderIds>
        <t:DistinguishedFolderId Id="calendar" />
      </m:ParentFolderIds>
    </m:FindItem>
  </soap:Body>
</soap:Envelope>
```

La respuesta del servidor incluye solo un elemento único, el patrón recurrente, indicado por el valor del elemento [CalendarItemType](https://msdn.microsoft.com/library/1feb0788-adf7-4a7c-830c-005214ad930f%28Office.15%29.aspx) de **RecurringMaster**. El valor del elemento [Itemid](https://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) se ha abreviado para facilitar su lectura. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="939" MinorBuildNumber="16" Version="V2_11" 
        xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
        xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:FindItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
        xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:FindItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:RootFolder IndexedPagingOffset="1" TotalItemsInView="1" IncludesLastItemInRange="true">
            <t:Items>
              <t:CalendarItem>
                <t:ItemId Id="AAMkADA5..." ChangeKey="DwAAABYA..." />
                <t:Subject>Swim Team Practice</t:Subject>
                <t:Start>2014-07-02T15:30:00Z</t:Start>
                <t:End>2014-07-02T17:00:00Z</t:End>
                <t:Location>Neighborhood Swimming Pool</t:Location>
                <t:CalendarItemType>RecurringMaster</t:CalendarItemType>
              </t:CalendarItem>
            </t:Items>
          </m:RootFolder>
        </m:FindItemResponseMessage>
      </m:ResponseMessages>
    </m:FindItemResponse>
  </s:Body>
</s:Envelope>
```

Ahora, vamos a comparar con una vista expandida. El siguiente ejemplo de código usa el método **FindAppointments** en la API administrada de EWS para crear una vista expandida del calendario de Sadie. 
  
```cs
PropertySet propSet = new PropertySet(AppointmentSchema.Subject,
                                      AppointmentSchema.Location,
                                      AppointmentSchema.Start, 
                                      AppointmentSchema.End,
                                      AppointmentSchema.AppointmentType);
CalendarView calView = new CalendarView(new DateTime(2014, 7, 1),
    new DateTime(2014, 7, 31));
calView.PropertySet = propSet;
FindItemsResults<Appointment> results = service.FindAppointments(WellKnownFolderName.Calendar, calView);
foreach(Appointment appt in results.Items)
{
    Console.WriteLine(appt.Subject);
}
```

Este código da como resultado la siguiente solicitud de [operación FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) con un elemento [CalendarView](https://msdn.microsoft.com/library/a4a953b8-0710-416c-95ef-59e51eba9982%28Office.15%29.aspx) . 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
    xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
    xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
    xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
    <t:TimeZoneContext>
      <t:TimeZoneDefinition Id="Pacific Standard Time" />
    </t:TimeZoneContext>
  </soap:Header>
  <soap:Body>
    <m:FindItem Traversal="Shallow">
      <m:ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="item:Subject" />
          <t:FieldURI FieldURI="calendar:Location" />
          <t:FieldURI FieldURI="calendar:Start" />
          <t:FieldURI FieldURI="calendar:End" />
          <t:FieldURI FieldURI="calendar:CalendarItemType" />
        </t:AdditionalProperties>
      </m:ItemShape>
      <m:CalendarView StartDate="2014-07-01T07:00:00.000Z" EndDate="2014-07-31T07:00:00.000Z" />
      <m:ParentFolderIds>
        <t:DistinguishedFolderId Id="calendar" />
      </m:ParentFolderIds>
    </m:FindItem>
  </soap:Body>
</soap:Envelope>
```

Esta vez, la respuesta del servidor incluye cinco repeticiones, una para cada miércoles en julio. Todos los elementos [CalendarItemType](https://msdn.microsoft.com/library/1feb0788-adf7-4a7c-830c-005214ad930f%28Office.15%29.aspx) de estos elementos tienen un valor de **ocurrencia**. Tenga en cuenta que el patrón recurrente no está presente en la respuesta. Los valores de los elementos [Itemid](https://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) se han abreviado para facilitar su lectura. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="939" MinorBuildNumber="16" Version="V2_11" 
        xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
        xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:FindItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
        xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:FindItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:RootFolder TotalItemsInView="5" IncludesLastItemInRange="true">
            <t:Items>
              <t:CalendarItem>
                <t:ItemId Id="AAMkADA6..." ChangeKey="DwAAABYA..." />
                <t:Subject>Swim Team Practice</t:Subject>
                <t:Start>2014-07-02T15:30:00Z</t:Start>
                <t:End>2014-07-02T17:00:00Z</t:End>
                <t:Location>Neighborhood Swimming Pool</t:Location>
                <t:CalendarItemType>Occurrence</t:CalendarItemType>
              </t:CalendarItem>
              <t:CalendarItem>
                <t:ItemId Id="AAMkADA7..." ChangeKey="DwAAABYA..." />
                <t:Subject>Swim Team Practice</t:Subject>
                <t:Start>2014-07-09T15:30:00Z</t:Start>
                <t:End>2014-07-09T17:00:00Z</t:End>
                <t:Location>Neighborhood Swimming Pool</t:Location>
                <t:CalendarItemType>Occurrence</t:CalendarItemType>
              </t:CalendarItem>
              <t:CalendarItem>
                <t:ItemId Id="AAMkADA8..." ChangeKey="DwAAABYA..." />
                <t:Subject>Swim Team Practice</t:Subject>
                <t:Start>2014-07-16T15:30:00Z</t:Start>
                <t:End>2014-07-16T17:00:00Z</t:End>
                <t:Location>Neighborhood Swimming Pool</t:Location>
                <t:CalendarItemType>Occurrence</t:CalendarItemType>
              </t:CalendarItem>
              <t:CalendarItem>
                <t:ItemId Id="AAMkADA9..." ChangeKey="DwAAABYA..." />
                <t:Subject>Swim Team Practice</t:Subject>
                <t:Start>2014-07-23T15:30:00Z</t:Start>
                <t:End>2014-07-23T17:00:00Z</t:End>
                <t:Location>Neighborhood Swimming Pool</t:Location>
                <t:CalendarItemType>Occurrence</t:CalendarItemType>
              </t:CalendarItem>
              <t:CalendarItem>
                <t:ItemId Id="AAMkADAA..." ChangeKey="DwAAABYA..." />
                <t:Subject>Swim Team Practice</t:Subject>
                <t:Start>2014-07-30T15:30:00Z</t:Start>
                <t:End>2014-07-30T17:00:00Z</t:End>
                <t:Location>Neighborhood Swimming Pool</t:Location>
                <t:CalendarItemType>Occurrence</t:CalendarItemType>
              </t:CalendarItem>
            </t:Items>
          </m:RootFolder>
        </m:FindItemResponseMessage>
      </m:ResponseMessages>
    </m:FindItemResponse>
  </s:Body>
</s:Envelope>
```

Una vez que tenga un patrón recurrente, una ocurrencia o una excepción, siempre podrá [recuperar los demás elementos relacionados](how-to-access-a-recurring-series-by-using-ews-in-exchange.md). Una vez transcurrida o excepción, puede recuperar el patrón recurrente y viceversa.
  
## <a name="working-with-recurring-calendar-items"></a>Trabajar con elementos de calendario periódicos

Use los mismos métodos y operaciones para trabajar con series periódicas mientras usa para trabajar con elementos de calendario no periódicos. La diferencia estriba en que, en función del elemento que se use para invocar dichos métodos u operaciones, las acciones que se realicen se pueden aplicar a toda la serie o solo a una única incidencia. Las [acciones realizadas en el maestro periódico](how-to-update-a-recurring-series-by-using-ews-in-exchange.md) se aplicarán a todas las repeticiones de la serie, mientras que [las acciones realizadas en una sola ocurrencia o excepción](how-to-update-a-recurring-series-by-using-ews.md) solo se aplicarán a esa ocurrencia o excepción. 
  
## <a name="in-this-section"></a>En esta sección

- [Obtener acceso a una serie periódica mediante EWS en Exchange](how-to-access-a-recurring-series-by-using-ews-in-exchange.md)
    
- [Crear una serie periódica mediante EWS en Exchange](how-to-create-a-recurring-series-by-using-ews-in-exchange.md)
    
- [Eliminar citas en una serie periódica mediante EWS en Exchange](how-to-delete-appointments-in-a-recurring-series-by-using-ews-in-exchange.md)
    
- [Actualizar una serie periódica mediante EWS](how-to-update-a-recurring-series-by-using-ews.md)
    
- [Actualizar una serie periódica mediante EWS en Exchange](how-to-update-a-recurring-series-by-using-ews-in-exchange.md)
    
## <a name="see-also"></a>Vea también


- [Calendarios y EWS en Exchange](calendars-and-ews-in-exchange.md)
    
- [Desarrollo de clientes de servicios web de Exchange](develop-web-service-clients-for-exchange.md)
    
- [Obtener citas y reuniones mediante EWS en Exchange](how-to-get-appointments-and-meetings-by-using-ews-in-exchange.md)
    

