---
title: Zonas horarias y EWS en Exchange
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 0e0a666c-0541-414b-a7fb-297d94f692e6
description: Obtenga información acerca de cómo las zonas horarias trabajar con la API administrada de EWS y EWS en Exchange.
ms.openlocfilehash: fcc8b00acf2b63de04718e13b82191de95bbf2b7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763311"
---
# <a name="time-zones-and-ews-in-exchange"></a>Zonas horarias y EWS en Exchange

Obtenga información acerca de cómo las zonas horarias trabajar con la API administrada de EWS y EWS en Exchange.
  
Zonas horarias no son algo que dar la mayoría de las personas de manera considerar a. Sin embargo, son un concepto importante al especificar las fechas y horas con la API administrada de EWS o EWS. Manejo incorrecto zonas horarias en una API administrada de EWS o EWS aplicación puede producir resultados inesperados. Controlar zonas horarias correctamente es fácil, siempre y cuando sabe cómo.
  
## <a name="handling-time-zones-in-the-ews-managed-api"></a>Controlar zonas horarias en la API administrada de EWS

Si se usa la API administrada de EWS, zonas horarias se, la mayor parte controlan por usted automáticamente. Sin ninguna acción explícita por su parte, la API usa la zona horaria local del equipo cliente y administra todas las conversiones necesarias en segundo plano. Esto es excelente cuando es el efecto que desee, pero tiene otras opciones.
  
Una opción es establecer la propiedad [ExchangeService.TimeZone](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.timezone%28v=exchg.80%29.aspx) . Esta propiedad controla la zona horaria para todas las solicitudes que se ejecute por medio de la API administrada de EWS. Esta propiedad es de sólo lectura; es la única forma de establecerla mediante el constructor de clase. Si usa el [ExchangeService(System.TimeZoneInfo)](http://msdn.microsoft.com/en-us/library/dd635875%28v=exchg.80%29.aspx) o el constructor [ExchangeService (ExchangeVersion, System.TimeZoneInfo)](http://msdn.microsoft.com/en-us/library/dd636248%28v=exchg.80%29.aspx) , puede especificar una zona horaria concreta como un objeto [System.TimeZoneInfo](http://msdn.microsoft.com/en-us/library/system.timezoneinfo%28v=vs.110%29.aspx) . Si usa uno de los otros constructores que toman un objeto **TimeZoneInfo** como un parámetro, la clase **ExchangeService** establece la propiedad de **zona horaria** para la zona horaria actual del equipo cliente. 
  
Si establece una zona horaria concreta o dejarla como la zona horaria del cliente para equipo, todas las fechas y horas se expresan en la zona horaria representada por la propiedad de **zona horaria** . La API administrada de EWS expone todas las propiedades de fecha y hora como estructuras [System.DateTime](http://msdn.microsoft.com/en-us/library/system.datetime%28v=vs.110%29.aspx) . Por lo que si establece las propiedades de fecha y hora, tenga en cuenta que el tiempo que especifique se interpreta según el valor de la propiedad [DateTime.Kind](http://msdn.microsoft.com/en-us/library/system.datetime.kind%28v=vs.110%29.aspx) en el objeto de **fecha y hora** . Si el valor de la propiedad **Kind** se establece en **no especificada**, el valor de **fecha y hora** se interpreta como perteneciente a la zona horaria especificada por la propiedad de **zona horaria** . Si está leyendo las propiedades de fecha y hora, todas las propiedades de **fecha y hora** se expresan en esa zona horaria. 
  
Si está [creando nuevas citas o reuniones](how-to-create-appointments-in-a-specific-time-zone-by-using-ews-in-exchange.md) o [actualizar las citas o reuniones existentes](how-to-update-the-time-zone-for-an-appointment-by-using-ews-in-exchange.md), tiene la capacidad de invalidar la zona horaria especificada en la **zona horaria** para los nuevos objetos de [cita](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) . Sin embargo, exactamente lo que se puede invalidar depende de la [versión del esquema de EWS](ews-schema-versions-in-exchange.md) de destino se establece. Todos los valores de la propiedad [ExchangeService.RequestedServerVersion](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservicebase.requestedserverversion%28v=exchg.80%29.aspx) , puede establecer el [Appointment.StartTimeZone](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.starttimezone%28v=exchg.80%29.aspx) a usar una zona horaria concreta para que una cita o reunión. Si utiliza un valor para la propiedad **ExchangeService.RequestedServerVersion** mayor que **Exchange2007_SP1**, también puede establecer que la propiedad [Appointment.EndTimeZone](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.endtimezone%28v=exchg.80%29.aspx) , que le permite especificar una zona horaria para el [ Appointment.End](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.end%28v=exchg.80%29.aspx) (propiedad). Sin embargo, tenga en cuenta que estas propiedades sólo afectan a la interpretación de la fecha y hora de la solicitud de creación. Si recupera la cita, aún se expresarán las horas de inicio y finalización en la zona horaria especificada por la propiedad de **zona horaria** . 
  
Si va a actualizar las citas o reuniones existentes, puede cambiar la zona horaria para un objeto de **cita** estableciendo la propiedad **StartTimeZone** o la propiedad **EndTimeZone** . Al hacerlo, hará que los tiempos de aplicables a se modificarán en consecuencia. Si ha establecido la **ExchangeService.RequestedServerVersion** en **Exchange2007_SP1**, no se puede establecer la propiedad **EndTimeZone** ; el valor de la propiedad **StartTimeZone** se usará en su lugar. 
  
**La tabla 1. Propiedades de la zona horaria en la API administrada de EWS**

|**Zona horaria (propiedad)**|**Versión de la solicitud de servidor mínimo**|**Descripción**|
|:-----|:-----|:-----|
|[Zona horaria](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.timezone%28v=exchg.80%29.aspx) <br/> |**Exchange2007_SP1** <br/> |Si no se establece mediante el constructor para la clase **ExchangeService** , esta propiedad se establece en la zona horaria del equipo cliente. Todas las propiedades de **fecha y hora** al crear los elementos y recuperar los existentes cuando elementos se expresan en esta zona horaria. Este tiempo de zona se puede invalidar en crear solicitudes de citas y reuniones estableciendo la **Appointment.StartTimeZone** o la propiedad **Appointment.EndTimeZone** . Si no se reemplaza por la propiedad **Appointment.StartTimeZone** , esta zona horaria se considera la zona horaria de creación de citas y reuniones.  <br/> |
|[StartTimeZone](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.starttimezone%28v=exchg.80%29.aspx) <br/> |**Exchange2007_SP1** <br/> |Si se establece en objetos de **citas** de nuevo, esta zona horaria se utiliza para interpretar las propiedades [Appointment.Start](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.start%28v=exchg.80%29.aspx) y [Appointment.ReminderDueBy](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.reminderdueby%28v=exchg.80%29.aspx) . Esta zona horaria también se considera la zona horaria de creación para el objeto de **cita** .  <br/> Cuando se recuperan los elementos existentes, esta propiedad sólo es informativa. Los valores de propiedades de **fecha y hora** en una cita existente siempre se expresan en la zona horaria especificada por la propiedad **ExchangeService.TimeZone** .  <br/> |
|[EndTimeZone](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.endtimezone%28v=exchg.80%29.aspx) <br/> |**Exchange2010** <br/> |Si se establece en objetos de **citas** de nuevo, esta zona horaria se utiliza para interpretar la propiedad [Appointment.End](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.end%28v=exchg.80%29.aspx) .  <br/> Cuando se recuperan los elementos existentes, esta propiedad sólo es informativa. Los valores de propiedades de **fecha y hora** en una cita existente siempre se expresan en la zona horaria especificada por la propiedad **ExchangeService.TimeZone** .  <br/> |
   
## <a name="handling-time-zones-in-ews"></a>Controlar las zonas horarias de EWS

Si está usando EWS, zonas horarias no se controlan automáticamente para usted y las cosas son un poco más complicadas. Cómo influir en las zonas horarias EWS solicitudes y respuestas depende de una serie de factores:
  
- La versión de Exchange especificada en el elemento [RequestServerVersion](http://msdn.microsoft.com/library/af4032d5-42b3-463e-9d0a-8236d78e5b75%28Office.15%29.aspx) 
    
- La zona horaria especificada en el elemento [TimeZoneContext](http://msdn.microsoft.com/library/573c462b-aa1d-4ba0-8852-e3f48b26873b%28Office.15%29.aspx) (si está presente) 
    
- La zona horaria especificada en los elementos [MeetingTimeZone](http://msdn.microsoft.com/library/413b47d9-8126-462c-9a4f-4e771a5e8889%28Office.15%29.aspx), [StartTimeZone](http://msdn.microsoft.com/library/d38c4dc1-4ecb-42a1-8d57-a451b16a2de2%28Office.15%29.aspx)o [EndTimeZone](http://msdn.microsoft.com/library/6c53c337-be60-4d22-9e9e-a0c140c5e913%28Office.15%29.aspx) (si está presente en las citas o reuniones) 
    
- La zona horaria especificada en los elementos de **fecha y hora** XML (si hay alguno) 
    
La zona horaria especificada en el valor de **fecha y hora** elementos puede adoptar tres formatos. Pueden leer todos los detalles en [esquema XML parte 2: tipos de datos Second Edition](http://www.w3.org/TR/xmlschema-2/#dateTime), pero que se probaron:
  
- **Hora Universal coordinada (UTC):** Especificado por 'Z'. Por ejemplo,`2014-06-06T19:00:00.000Z`
    
- **Zona horaria específicos:** Especificado por '+' o '-' seguido de horas y minutos. Por ejemplo,`2014-06-06T19:00:00.000-08:00`
    
- **Ninguna zona horaria:** Especificado por la ausencia de cualquier zona horaria. Por ejemplo,`2014-06-06T19:00:00.000`
    
Si una zona horaria está presente en un valor de **fecha y hora** (UTC o una zona horaria concreta), ese valor siempre se interpreta como esa zona horaria. Si ninguna zona horaria está presente, a continuación, la interpretación del valor depende de la combinación de los demás elementos relacionados de zona horaria específica. 
  
**Tabla 2. Elementos de la zona horaria en EWS y sus efectos**

|**RequestServerVersion**|**¿TimeZoneContext presente?**|**¿MeetingTimeZone, StartTimeZone o EndTimeZone presentar (CalendarItem y sólo MeetingRequest)?**|**fecha y hora en UTC**|**fecha y hora en la zona horaria específicos**|**fecha y hora sin zona horaria**|**Zona de tiempo de creación de citas y reuniones**|
|:-----|:-----|:-----|:-----|:-----|:-----|:-----|
|**Exchange2007_SP1** <br/> |Sí  <br/> |Sí ( **MeetingTimeZone** )  <br/> |Interpreta como UTC  <br/> |Interpreta como la zona horaria que se indican en el valor  <br/> |Los elementos dentro del elemento [CalendarItem](http://msdn.microsoft.com/library/b0c1fd27-b6da-46e5-88b8-88f00c71ba80%28Office.15%29.aspx) o [MeetingRequest](http://msdn.microsoft.com/library/c44f8804-a355-473d-a837-48cc91617251%28Office.15%29.aspx) que contiene el elemento **MeetingTimeZone** se interpretan como la zona horaria en el elemento **MeetingTimeZone** , todos los demás interpreta como UTC  <br/> |Zona horaria en el elemento **MeetingTimeZone**  <br/> |
|**Exchange2007_SP1** <br/> |Sí  <br/> |No  <br/> |Interpreta como UTC  <br/> |Interpreta como la zona horaria que se indican en el valor  <br/> |Interpreta como UTC  <br/> |UTC  <br/> |
|**Exchange2007_SP1** <br/> |No  <br/> |Sí ( **MeetingTimeZone** )  <br/> |Interpreta como UTC  <br/> |Interpreta como la zona horaria que se indican en el valor  <br/> |Los elementos dentro del elemento [CalendarItem](http://msdn.microsoft.com/library/b0c1fd27-b6da-46e5-88b8-88f00c71ba80%28Office.15%29.aspx) o [MeetingRequest](http://msdn.microsoft.com/library/c44f8804-a355-473d-a837-48cc91617251%28Office.15%29.aspx) que contiene el elemento **MeetingTimeZone** se interpretan como la zona horaria en el elemento **MeetingTimeZone** , todos los demás interpreta como UTC  <br/> |Zona horaria en el elemento **MeetingTimeZone**  <br/> |
|**Exchange2007_SP1** <br/> |No  <br/> |No  <br/> |Interpreta como UTC  <br/> |Interpreta como la zona horaria que se indican en el valor  <br/> |Interpreta como UTC  <br/> |UTC  <br/> |
|**Exchange2010** y versiones posteriores  <br/> |Sí  <br/> |Sí ( **StartTimeZone** o **EndTimeZone** )  <br/> |Interpreta como UTC  <br/> |Interpreta como la zona horaria que se indican en el valor  <br/> |Si el elemento **StartTimeZone** está presente, el valor de [Start](http://msdn.microsoft.com/library/7cfe9979-c893-4f9b-b3a1-8f9e17515a4b%28Office.15%29.aspx) y elementos de [ReminderDueBy](http://msdn.microsoft.com/library/e28a0485-86af-4a4e-a2ba-3ad2d4ebff6f%28Office.15%29.aspx) se interpreta como la zona horaria en el elemento **StartTimeZone** . De lo contrario, el valor de esos elementos se interpreta como la zona horaria en el elemento **TimeZoneContext** .  <br/> Si el elemento **EndTimeZone** está presente, el valor del elemento de [Inicio](http://msdn.microsoft.com/library/7cfe9979-c893-4f9b-b3a1-8f9e17515a4b%28Office.15%29.aspx) se interpreta como la zona horaria en el elemento **EndTimeZone** . De lo contrario, el valor del elemento **final** se interpreta como la zona horaria en el elemento **TimeZoneContext** .  <br/> Elementos fuera del [CalendarItem](http://msdn.microsoft.com/library/b0c1fd27-b6da-46e5-88b8-88f00c71ba80%28Office.15%29.aspx) o [MeetingRequest](http://msdn.microsoft.com/library/c44f8804-a355-473d-a837-48cc91617251%28Office.15%29.aspx) se interpretan como la zona horaria en el elemento **TimeZoneContext** .  <br/> |Zona horaria en el elemento **StartTimeZone** si está presente, la zona horaria en el elemento de **TimeZoneContext** si no  <br/> |
|**Exchange2010** y versiones posteriores  <br/> |Sí  <br/> |No  <br/> |Interpreta como UTC  <br/> |Interpreta como la zona horaria que se indican en el valor  <br/> |Interpreta como la zona horaria en el elemento **TimeZoneContext**  <br/> |Zona horaria en el elemento **TimeZoneContext**  <br/> |
|**Exchange2010** y versiones posteriores  <br/> |No  <br/> |Sí ( **StartTimeZone** o **EndTimeZone** )  <br/> |Interpreta como UTC  <br/> |Interpreta como la zona horaria que se indican en el valor  <br/> |Si el elemento **StartTimeZone** está presente, el valor de [Start](http://msdn.microsoft.com/library/7cfe9979-c893-4f9b-b3a1-8f9e17515a4b%28Office.15%29.aspx) y elementos de [ReminderDueBy](http://msdn.microsoft.com/library/e28a0485-86af-4a4e-a2ba-3ad2d4ebff6f%28Office.15%29.aspx) se interpreta como la zona horaria en el elemento **StartTimeZone** . De lo contrario, el valor de esos elementos se interpreta como UTC.  <br/> Si el elemento **EndTimeZone** está presente, el valor del elemento de [Inicio](http://msdn.microsoft.com/library/7cfe9979-c893-4f9b-b3a1-8f9e17515a4b%28Office.15%29.aspx) se interpreta como la zona horaria en el elemento **EndTimeZone** . De lo contrario, el valor del elemento **final** se interpreta como UTC.  <br/> Elementos fuera del [CalendarItem](http://msdn.microsoft.com/library/b0c1fd27-b6da-46e5-88b8-88f00c71ba80%28Office.15%29.aspx) o [MeetingRequest](http://msdn.microsoft.com/library/c44f8804-a355-473d-a837-48cc91617251%28Office.15%29.aspx) se interpretan como UTC.  <br/> |Zona horaria en el elemento **StartTimeZone** si está presente, UTC si no  <br/> |
|**Exchange2010** y versiones posteriores  <br/> |No  <br/> |No  <br/> |Interpreta como UTC  <br/> |Interpreta como la zona horaria que se indican en el valor  <br/> |Interpreta como UTC  <br/> |UTC  <br/> |
   
Al interpretar las respuestas desde el servidor, siempre debe comprobar el valor de cada elemento e interpretar el valor según corresponda. Exchange siempre incluirá una zona horaria (UTC o una zona horaria concreta) en el valor.
  
## <a name="additional-time-zone-considerations-when-creating-appointments-and-meetings"></a>Consideraciones sobre la zona horaria adicional al crear las citas y reuniones

Cuando se crea una cita o una reunión, la zona horaria que se aplica a la hora de inicio se considera la zona horaria de creación para la cita. Además de controlar cómo se interpretan la date/times cuando se crea una cita o una reunión, la zona horaria de creación tiene los efectos siguientes en el elemento:
  
- Si el elemento es un evento de día completo, es posible que muestre de forma inesperada si ve desde un cliente que está usando una zona horaria diferente a la zona de tiempo de creación. Esto es debido a que el tiempo [cuando se crea un evento de día completo](how-to-create-all-day-events-by-using-ews-in-exchange.md), el inicio y el final de los eventos de día completo se ajustan a partir de la medianoche de la zona de hora de creación. Ese tiempo se mostrará como una hora distinta de la medianoche en una zona horaria diferente, por lo que es posible que aparezca el elemento abarcar días adicionales. Por este motivo, se recomienda que use la zona horaria configurada para cliente de calendario principal del usuario para crear eventos de día completo cuando sea posible.
    
- Si el elemento es una reunión, se mostrará la zona horaria de creación de la barra de información de Outlook en las convocatorias de reunión recibidas por los asistentes, si esa zona horaria difiere de la zona horaria de su cliente.
    
## <a name="in-this-section"></a>En esta sección

- [Crear citas en una zona horaria concreta mediante el uso de EWS en Exchange](how-to-create-appointments-in-a-specific-time-zone-by-using-ews-in-exchange.md)
    
- [Actualización de la zona horaria para una cita mediante EWS en Exchange](how-to-update-the-time-zone-for-an-appointment-by-using-ews-in-exchange.md)
    
## <a name="see-also"></a>Vea también


- [Desarrollo de clientes de servicios web de Exchange](develop-web-service-clients-for-exchange.md)
    
- [Versiones de esquema EWS en Exchange](ews-schema-versions-in-exchange.md)
    
- [Crear citas y reuniones mediante el uso de EWS en Exchange 2013](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md)
    
- [Actualizar las citas y reuniones con EWS en Exchange](how-to-update-appointments-and-meetings-by-using-ews-in-exchange.md)
    
- [Crear eventos de día completo mediante el uso de EWS en Exchange](how-to-create-all-day-events-by-using-ews-in-exchange.md)
    
- [Estructura DateTime](http://msdn.microsoft.com/en-us/library/system.datetime%28v=vs.110%29.aspx)
    
- [Clase TimeZoneInfo](http://msdn.microsoft.com/en-us/library/system.timezoneinfo%28v=vs.110%29.aspx)
    

