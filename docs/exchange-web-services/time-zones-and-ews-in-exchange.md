---
title: Zonas horarias y EWS en Exchange
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.assetid: 0e0a666c-0541-414b-a7fb-297d94f692e6
description: Descubra cómo funcionan las zonas horarias con la API administrada de EWS y EWS en Exchange.
localization_priority: Priority
ms.openlocfilehash: 8435087d7709b77e7562e2b9d50ece58377dd8db
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463751"
---
# <a name="time-zones-and-ews-in-exchange"></a>Zonas horarias y EWS en Exchange

Descubra cómo funcionan las zonas horarias con la API administrada de EWS y EWS en Exchange.
  
Las zonas horarias no son algo que la mayoría de las personas le consideran muy reflexionadas. Sin embargo, son un concepto importante a la hora de especificar fechas y horas con la API administrada de EWS o EWS. Las zonas horarias en mal manejo en una API administrada de EWS o en una aplicación de EWS pueden producir resultados inesperados. La administración correcta de las zonas horarias es sencilla, siempre que se sepa cómo hacerlo.
  
## <a name="handling-time-zones-in-the-ews-managed-api"></a>Administración de zonas horarias en la API administrada de EWS

Si está usando la API administrada de EWS, las zonas horarias son, en su mayor parte, que se controlan automáticamente. Sin ninguna acción explícita en su parte, la API usa la zona horaria local del equipo cliente y administra todas las conversiones necesarias en segundo plano. Esto es estupendo cuando se trata del efecto deseado, pero tiene otras opciones.
  
Una opción es establecer la propiedad [ExchangeService. TimeZone](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.timezone%28v=exchg.80%29.aspx) . Esta propiedad controla la zona horaria de todas las solicitudes ejecutadas por la API administrada de EWS. Esta propiedad es de sólo lectura; la única forma de establecerla es mediante el constructor de clase. Si usa el constructor [ExchangeService (System. TimeZoneInfo)](https://msdn.microsoft.com/library/dd635875%28v=exchg.80%29.aspx) o [ExchangeService (ExchangeVersion, System. TimeZoneInfo)](https://msdn.microsoft.com/library/dd636248%28v=exchg.80%29.aspx) , puede especificar una zona horaria determinada como un objeto [System. TimeZoneInfo](https://msdn.microsoft.com/library/system.timezoneinfo%28v=vs.110%29.aspx) . Si usa uno de los otros constructores que no toman un objeto **TimeZoneInfo** como parámetro, la clase **ExchangeService** establece la propiedad **TimeZone** en la zona horaria actual del equipo cliente. 
  
Tanto si establece una zona horaria específica como si la deja como la zona horaria del equipo cliente, todas las fechas y horas se expresan en la zona horaria representada por la propiedad **TimeZone** . La API administrada de EWS expone todas las propiedades de fecha y hora como estructuras [System. DateTime](https://msdn.microsoft.com/library/system.datetime%28v=vs.110%29.aspx) . Por lo tanto, si establece propiedades de fecha y hora, tenga en cuenta que el tiempo que especifique se interpretará de acuerdo con el valor de la propiedad [DateTime. Kind](https://msdn.microsoft.com/library/system.datetime.kind%28v=vs.110%29.aspx) en el objeto **DateTime** . Si el valor de la propiedad **Kind** se establece en **sin especificar**, el valor de **DateTime** se interpreta como si estuviera en la zona horaria especificada por la propiedad **TimeZone** . Si está leyendo propiedades de fecha y hora, todas las propiedades **DateTime** se expresan en esa zona horaria. 
  
Si va a [crear citas o reuniones nuevas](how-to-create-appointments-in-a-specific-time-zone-by-using-ews-in-exchange.md) o [actualizar las citas o reuniones existentes](how-to-update-the-time-zone-for-an-appointment-by-using-ews-in-exchange.md), tiene la posibilidad de reemplazar la zona horaria especificada en la zona **horaria** para los nuevos objetos de [cita](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) . Sin embargo, el contenido exacto que puede invalidar depende de la [versión del esquema EWS](ews-schema-versions-in-exchange.md) de destino. Para todos los valores de la propiedad [ExchangeService. RequestedServerVersion](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.requestedserverversion%28v=exchg.80%29.aspx) , puede establecer [appointment. StartTimeZone](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.starttimezone%28v=exchg.80%29.aspx) para usar una zona horaria específica para dicha cita o reunión. Si está usando un valor para la propiedad **ExchangeService. RequestedServerVersion** mayor que **Exchange2007_SP1**, también puede establecer la propiedad [appointment. EndTimeZone](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.endtimezone%28v=exchg.80%29.aspx) , lo que le permite especificar una zona horaria para la propiedad [appointment. end](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.end%28v=exchg.80%29.aspx) . Sin embargo, tenga en cuenta que estas propiedades solo afectan a la interpretación de la fecha y la hora para la solicitud de creación. Si recupera la cita, las horas de inicio y finalización seguirán siendo expresadas en la zona horaria especificada por la propiedad **TimeZone** . 
  
Si actualiza citas o reuniones existentes, puede cambiar la zona horaria de un objeto **appointment** estableciendo la propiedad **StartTimeZone** y la propiedad **EndTimeZone** . Si lo hace, se producirá el cambio de horario aplicable en consecuencia. Si ha establecido **ExchangeService. RequestedServerVersion** en **Exchange2007_SP1**, no puede establecer la propiedad **EndTimeZone** ; se usará el valor de la propiedad **StartTimeZone** en su posición. 
  
**Tabla 1. Propiedades de zona horaria en la API administrada de EWS**

|**Propiedad Time Zone**|**Versión mínima de solicitud de servidor**|**Descripción**|
|:-----|:-----|:-----|
|[TimeZone](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.timezone%28v=exchg.80%29.aspx) <br/> |**Exchange2007_SP1** <br/> |Si no se establece a través del constructor de la clase **ExchangeService** , esta propiedad se establece en la zona horaria del equipo cliente. Todas las propiedades de **fecha** y hora al crear elementos y al recuperar los elementos existentes se expresan en esta zona horaria. Esta zona horaria puede invalidarse en crear solicitudes de citas y reuniones estableciendo la propiedad **appointment. StartTimeZone** y la propiedad **appointment. EndTimeZone** . Si no se reemplaza por la propiedad **appointment. StartTimeZone** , esta zona horaria se considera la zona horaria de creación para las citas y reuniones.  <br/> |
|[StartTimeZone](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.starttimezone%28v=exchg.80%29.aspx) <br/> |**Exchange2007_SP1** <br/> |Si se establece en nuevos objetos de **cita** , esta zona horaria se usa para interpretar las propiedades [appointment. Start](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.start%28v=exchg.80%29.aspx) y [appointment. ReminderDueBy](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.reminderdueby%28v=exchg.80%29.aspx) . Esta zona horaria también se considera la zona horaria de creación del objeto de **cita** .  <br/> Al recuperar elementos existentes, esta propiedad es solo informativa. Los valores de las propiedades **DateTime** de una cita existente siempre se expresan en la zona horaria especificada por la propiedad **ExchangeService. TimeZone** .  <br/> |
|[EndTimeZone](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.endtimezone%28v=exchg.80%29.aspx) <br/> |**Exchange2010** <br/> |Si se establece en nuevos objetos de **cita** , esta zona horaria se usa para interpretar la propiedad [appointment. end](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.end%28v=exchg.80%29.aspx) .  <br/> Al recuperar elementos existentes, esta propiedad es solo informativa. Los valores de las propiedades **DateTime** de una cita existente siempre se expresan en la zona horaria especificada por la propiedad **ExchangeService. TimeZone** .  <br/> |
   
## <a name="handling-time-zones-in-ews"></a>Administración de zonas horarias en EWS

Si está usando EWS, las zonas horarias no se administran automáticamente y las cosas son un poco más complicadas. Cómo el impacto de las zonas horarias en las solicitudes y respuestas de EWS depende de varios factores:
  
- La versión de Exchange especificada en el elemento [RequestServerVersion](https://msdn.microsoft.com/library/af4032d5-42b3-463e-9d0a-8236d78e5b75%28Office.15%29.aspx) 
    
- La zona horaria especificada en el elemento [TimeZoneContext](https://msdn.microsoft.com/library/573c462b-aa1d-4ba0-8852-e3f48b26873b%28Office.15%29.aspx) (si está presente) 
    
- La zona horaria especificada en los elementos [MeetingTimeZone](https://msdn.microsoft.com/library/413b47d9-8126-462c-9a4f-4e771a5e8889%28Office.15%29.aspx), [StartTimeZone](https://msdn.microsoft.com/library/d38c4dc1-4ecb-42a1-8d57-a451b16a2de2%28Office.15%29.aspx)o [EndTimeZone](https://msdn.microsoft.com/library/6c53c337-be60-4d22-9e9e-a0c140c5e913%28Office.15%29.aspx) (si está presente en citas o reuniones) 
    
- La zona horaria especificada en los elementos XML de **fecha y** hora (si corresponde) 
    
La zona horaria especificada en el valor de los elementos **DateTime** puede tener tres formas. Puede leer todos los detalles en el [esquema XML parte 2: Datatypes Second Edition](http://www.w3.org/TR/xmlschema-2/#dateTime), pero en Paraphrase:
  
- **Hora universal coordinada (UTC):** Especificado por "Z". Por ejemplo,  `2014-06-06T19:00:00.000Z`
    
- **Zona horaria específica:** Especificado por "+" o "-" seguido de horas y minutos. Por ejemplo,  `2014-06-06T19:00:00.000-08:00`
    
- **Sin zona horaria:** Especificada por la ausencia de ninguna zona horaria. Por ejemplo,  `2014-06-06T19:00:00.000`
    
Si hay una zona horaria presente en un valor de **fecha y** hora (ya sea la hora UTC o una zona horaria específica), ese valor siempre se interpreta como esa zona horaria. Si no hay una zona horaria presente, la interpretación del valor depende de la combinación específica de los otros elementos relacionados con la zona horaria. 
  
**Tabla 2. Elementos de zona horaria en EWS y sus efectos**

|**RequestServerVersion**|**¿Está presente TimeZoneContext?**|**MeetingTimeZone, StartTimeZone o EndTimeZone presente (solo CalendarItem y MeetingRequest)?**|**Fecha y hora en UTC**|**dateTime en una zona horaria específica**|**Fecha y hora sin zona horaria**|**Zona horaria de creación de citas y reuniones**|
|:-----|:-----|:-----|:-----|:-----|:-----|:-----|
|**Exchange2007_SP1** <br/> |Sí  <br/> |Sí ( **MeetingTimeZone** )  <br/> |Interpretar como UTC  <br/> |Se interpreta como la zona horaria indicada en el valor  <br/> |Los elementos de los elementos [CalendarItem](https://msdn.microsoft.com/library/b0c1fd27-b6da-46e5-88b8-88f00c71ba80%28Office.15%29.aspx) o [MeetingRequest](https://msdn.microsoft.com/library/c44f8804-a355-473d-a837-48cc91617251%28Office.15%29.aspx) que contienen el elemento **MeetingTimeZone** se interpretan como la zona horaria en el elemento **MeetingTimeZone** , todos los demás se interpretan como UTC.  <br/> |Zona horaria en el elemento **MeetingTimeZone**  <br/> |
|**Exchange2007_SP1** <br/> |Sí  <br/> |No  <br/> |Interpretar como UTC  <br/> |Se interpreta como la zona horaria indicada en el valor  <br/> |Interpretar como UTC  <br/> |UTC  <br/> |
|**Exchange2007_SP1** <br/> |No  <br/> |Sí ( **MeetingTimeZone** )  <br/> |Interpretar como UTC  <br/> |Se interpreta como la zona horaria indicada en el valor  <br/> |Los elementos de los elementos [CalendarItem](https://msdn.microsoft.com/library/b0c1fd27-b6da-46e5-88b8-88f00c71ba80%28Office.15%29.aspx) o [MeetingRequest](https://msdn.microsoft.com/library/c44f8804-a355-473d-a837-48cc91617251%28Office.15%29.aspx) que contienen el elemento **MeetingTimeZone** se interpretan como la zona horaria en el elemento **MeetingTimeZone** , todos los demás se interpretan como UTC.  <br/> |Zona horaria en el elemento **MeetingTimeZone**  <br/> |
|**Exchange2007_SP1** <br/> |No  <br/> |No  <br/> |Interpretar como UTC  <br/> |Se interpreta como la zona horaria indicada en el valor  <br/> |Interpretar como UTC  <br/> |UTC  <br/> |
|**Exchange2010** y versiones posteriores  <br/> |Sí  <br/> |Sí ( **StartTimeZone** y **EndTimeZone** )  <br/> |Interpretar como UTC  <br/> |Se interpreta como la zona horaria indicada en el valor  <br/> |Si el elemento **StartTimeZone** está presente, el valor de los elementos [Start](https://msdn.microsoft.com/library/7cfe9979-c893-4f9b-b3a1-8f9e17515a4b%28Office.15%29.aspx) y [ReminderDueBy](https://msdn.microsoft.com/library/e28a0485-86af-4a4e-a2ba-3ad2d4ebff6f%28Office.15%29.aspx) se interpreta como la zona horaria en el elemento **StartTimeZone** . De lo contrario, el valor de esos elementos se interpreta como la zona horaria en el elemento **TimeZoneContext** .  <br/> Si el elemento **EndTimeZone** está presente, el valor del elemento [Start](https://msdn.microsoft.com/library/7cfe9979-c893-4f9b-b3a1-8f9e17515a4b%28Office.15%29.aspx) se interpreta como la zona horaria en el elemento **EndTimeZone** . De lo contrario, el valor del elemento **final** se interpreta como la zona horaria en el elemento **TimeZoneContext** .  <br/> Los elementos fuera de [CalendarItem](https://msdn.microsoft.com/library/b0c1fd27-b6da-46e5-88b8-88f00c71ba80%28Office.15%29.aspx) o [MeetingRequest](https://msdn.microsoft.com/library/c44f8804-a355-473d-a837-48cc91617251%28Office.15%29.aspx) se interpretan como la zona horaria en el elemento **TimeZoneContext** .  <br/> |Zona horaria en el elemento **StartTimeZone** si está presente, zona horaria en el elemento **TimeZoneContext** si no lo está  <br/> |
|**Exchange2010** y versiones posteriores  <br/> |Sí  <br/> |No  <br/> |Interpretar como UTC  <br/> |Se interpreta como la zona horaria indicada en el valor  <br/> |Se interpreta como la zona horaria en el elemento **TimeZoneContext**  <br/> |Zona horaria en el elemento **TimeZoneContext**  <br/> |
|**Exchange2010** y versiones posteriores  <br/> |No  <br/> |Sí ( **StartTimeZone** y **EndTimeZone** )  <br/> |Interpretar como UTC  <br/> |Se interpreta como la zona horaria indicada en el valor  <br/> |Si el elemento **StartTimeZone** está presente, el valor de los elementos [Start](https://msdn.microsoft.com/library/7cfe9979-c893-4f9b-b3a1-8f9e17515a4b%28Office.15%29.aspx) y [ReminderDueBy](https://msdn.microsoft.com/library/e28a0485-86af-4a4e-a2ba-3ad2d4ebff6f%28Office.15%29.aspx) se interpreta como la zona horaria en el elemento **StartTimeZone** . De lo contrario, el valor de esos elementos se interpreta como UTC.  <br/> Si el elemento **EndTimeZone** está presente, el valor del elemento [Start](https://msdn.microsoft.com/library/7cfe9979-c893-4f9b-b3a1-8f9e17515a4b%28Office.15%29.aspx) se interpreta como la zona horaria en el elemento **EndTimeZone** . De lo contrario, el valor del elemento **final** se interpreta como UTC.  <br/> Los elementos fuera de [CalendarItem](https://msdn.microsoft.com/library/b0c1fd27-b6da-46e5-88b8-88f00c71ba80%28Office.15%29.aspx) o [MeetingRequest](https://msdn.microsoft.com/library/c44f8804-a355-473d-a837-48cc91617251%28Office.15%29.aspx) se interpretan como UTC.  <br/> |Zona horaria en el elemento **StartTimeZone** si está presente, UTC Si no  <br/> |
|**Exchange2010** y versiones posteriores  <br/> |No  <br/> |No  <br/> |Interpretar como UTC  <br/> |Se interpreta como la zona horaria indicada en el valor  <br/> |Interpretar como UTC  <br/> |UTC  <br/> |
   
Al interpretar las respuestas del servidor, siempre debe comprobar el valor de cada elemento e interpretar el valor en consecuencia. Exchange siempre incluirá una zona horaria (ya sea UTC o una zona horaria específica) en el valor.
  
## <a name="additional-time-zone-considerations-when-creating-appointments-and-meetings"></a>Consideraciones adicionales sobre zonas horarias al crear citas y reuniones

Cuando se crea una cita o una reunión, la zona horaria que se aplica a la hora de inicio se considera la zona horaria de creación de la cita. Además de controlar cómo se interpreta la fecha y la hora cuando se crea una cita o una reunión, la zona horaria de creación tiene los siguientes efectos en el elemento:
  
- Si el elemento es un evento de todo el día, es posible que se muestre de forma inesperada si se visualiza desde un cliente que usa una zona horaria distinta de la zona horaria de creación. Esto se debe a que, [cuando se crea un evento de todo el día](how-to-create-all-day-events-by-using-ews-in-exchange.md), la hora de inicio y finalización de los eventos de todo el día se ajustan a la medianoche de la zona horaria de creación. Esa hora se mostrará como una hora distinta a la medianoche en una zona horaria diferente, por lo que el elemento puede que parezca abarcar días adicionales. Por este motivo, se recomienda usar la zona horaria configurada para el cliente de calendario principal del usuario para crear eventos de todo el día cuando sea posible.
    
- Si el elemento es una reunión, la zona horaria de creación se mostrará en la barra de información de Outlook en las convocatorias de reunión que los asistentes hayan recibido, si esa zona horaria difiere de la zona horaria de su cliente.
    
## <a name="in-this-section"></a>En esta sección

- [Crear citas en una zona horaria específica mediante EWS en Exchange](how-to-create-appointments-in-a-specific-time-zone-by-using-ews-in-exchange.md)
    
- [Actualizar la zona horaria de una cita mediante EWS en Exchange](how-to-update-the-time-zone-for-an-appointment-by-using-ews-in-exchange.md)
    
## <a name="see-also"></a>Vea también


- [Desarrollar clientes de servicios web de Exchange](develop-web-service-clients-for-exchange.md)
    
- [Versiones del esquema EWS en Exchange](ews-schema-versions-in-exchange.md)
    
- [Crear citas y reuniones mediante EWS en Exchange 2013](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md)
    
- [Actualizar citas y reuniones mediante EWS en Exchange](how-to-update-appointments-and-meetings-by-using-ews-in-exchange.md)
    
- [Crear eventos de día completo mediante EWS en Exchange](how-to-create-all-day-events-by-using-ews-in-exchange.md)
    
- [Estructura DateTime](https://msdn.microsoft.com/library/system.datetime%28v=vs.110%29.aspx)
    
- [Clase TimeZoneInfo](https://msdn.microsoft.com/library/system.timezoneinfo%28v=vs.110%29.aspx)
    

