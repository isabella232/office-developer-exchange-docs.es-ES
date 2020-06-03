---
title: Operación GetUserAvailability
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetUserAvailability
api_type:
- schema
ms.assetid: 8da17226-5d3a-4525-9ffa-d83730f47bb1
description: Buscar información sobre la operación de EWS de GetUserAvailability.
ms.openlocfilehash: b6d03c7da65e3f30f093b7e41448abcca2330a84
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458225"
---
# <a name="getuseravailability-operation"></a>Operación GetUserAvailability

Buscar información sobre la operación de EWS de **GetUserAvailability** . 
  
La operación **GetUserAvailability** proporciona información detallada sobre la disponibilidad de un conjunto de usuarios, salones y recursos en un período de tiempo especificado. 
  
## <a name="using-the-getuseravailability-operation"></a>Uso de la operación GetUserAvailability

La operación **GetUserAvailability** proporciona información actual sobre la disponibilidad del usuario en un nivel de detalle especificado. Las aplicaciones cliente como Outlook, Outlook Web Access, Outlook Mobile Access y otras usan direcciones SMTP para identificar la información de usuario solicitada. 
  
El servicio de disponibilidad expande las listas de distribución para recuperar el estado de disponibilidad de cada miembro de la lista, siempre que el número de buzones de la lista de distribución sea inferior a 100, que es el número máximo de identidades que la operación **GetUserAvailability** puede solicitar. Los Estados de disponibilidad de los miembros de la lista de distribución se combinan en un solo Estado de disponibilidad para toda la lista de distribución. 
  
Las solicitudes de aplicación de cliente especifican el período de tiempo de la consulta de disponibilidad. El período de tiempo predeterminado para la información solicitada es de 42 días. Si el calendario del usuario contiene citas o reuniones que están dentro y fuera del período de tiempo definido para la consulta, se devuelve la cita. 
  
Las horas de citas y reuniones que se devuelven se encuentran en la misma zona horaria que la aplicación cliente que solicita la reunión.
  
El servicio de disponibilidad procesa la solicitud para cada cliente. El servicio expande todas las citas periódicas y devuelve el número máximo de detalles del calendario que el cliente solicitante tiene permiso para recibir.
  
> [!NOTE]
> Si el buzón de destino no está disponible o no se encuentra, se produce una excepción **MailRecipientNotFoundException** . El cliente recibe un mensaje de error que indica que el destinatario de correo no se encuentra en el servicio de directorio Active Directory o en los servicios de dominio de Active Directory (AD DS). 
  
### <a name="getuseravailability-operation-soap-headers"></a>Encabezados SOAP de operación GetUserAvailability

La operación **GetUserAvailability** puede usar los encabezados SOAP que se enumeran en la tabla siguiente. 
  
|**Header**|**Elemento**|**Descripción**|
|:-----|:-----|:-----|
|**Suplantación** <br/> |[ExchangeImpersonation](exchangeimpersonation.md) <br/> |Identifica al usuario que el cliente está suplantando. Este encabezado se aplica a una solicitud.  <br/> |
|**RequestVersion** <br/> |[RequestServerVersion](requestserverversion.md) <br/> |Identifica la versión del esquema para la solicitud de operación. Este encabezado se aplica a una solicitud.  <br/> |
|**ServerVersion** <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |Identifica la versión del servidor que respondió a la solicitud. Este encabezado se aplica a una respuesta.  <br/> |
|**TimeZoneContext** <br/> |[TimeZoneContext](timezonecontext.md) <br/> |Especifica un encabezado SOAP que identifica la zona horaria que se va a usar para todas las respuestas del servidor. Todas las horas que se devuelven del servidor se convertirán en la zona horaria especificada. Este encabezado se aplica a una respuesta.  <br/> |
   
## <a name="getuseravailability-request-example-get-availability-information"></a>Ejemplo de solicitud GetUserAvailability: obtener información de disponibilidad

El siguiente ejemplo de una solicitud de operación de **GetUserAvailability** muestra cómo obtener información detallada de disponibilidad para dos usuarios en la zona horaria del Pacífico. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <GetUserAvailabilityRequest xmlns="https://schemas.microsoft.com/exchange/services/2006/messages"
                xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <t:TimeZone xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
        <Bias>480</Bias>
        <StandardTime>
          <Bias>0</Bias>
          <Time>02:00:00</Time>
          <DayOrder>5</DayOrder>
          <Month>10</Month>
          <DayOfWeek>Sunday</DayOfWeek>
        </StandardTime>
        <DaylightTime>
          <Bias>-60</Bias>
          <Time>02:00:00</Time>
          <DayOrder>1</DayOrder>
          <Month>4</Month>
          <DayOfWeek>Sunday</DayOfWeek>
        </DaylightTime>
      </t:TimeZone>
      <MailboxDataArray>
        <t:MailboxData>
          <t:Email>
            <t:Address>user1@example.com</t:Address>
          </t:Email>
          <t:AttendeeType>Required</t:AttendeeType>
          <t:ExcludeConflicts>false</t:ExcludeConflicts>
        </t:MailboxData>
        <t:MailboxData>
          <t:Email>
            <t:Address>user2@example.com</t:Address>
          </t:Email>
          <t:AttendeeType>Required</t:AttendeeType>
          <t:ExcludeConflicts>false</t:ExcludeConflicts>
        </t:MailboxData>
      </MailboxDataArray>
      <t:FreeBusyViewOptions>
        <t:TimeWindow>
          <t:StartTime>2006-10-16T00:00:00</t:StartTime>
          <t:EndTime>2006-10-16T23:59:59</t:EndTime>
        </t:TimeWindow>
        <t:MergedFreeBusyIntervalInMinutes>60</t:MergedFreeBusyIntervalInMinutes>
        <t:RequestedView>DetailedMerged</t:RequestedView>
      </t:FreeBusyViewOptions>
    </GetUserAvailabilityRequest>
  </soap:Body>
</soap:Envelope>
```

Para obtener más información sobre cómo recuperar reuniones sugeridas mediante el elemento [SuggestionsViewOptions](suggestionsviewoptions.md) , vea el esquema en el directorio virtual EWS. 
  
El cuerpo SOAP de la solicitud contiene los siguientes elementos:
  
- [GetUserAvailabilityRequest](getuseravailabilityrequest.md)
    
- [Zona horaria (disponibilidad)](timezone-availability.md)
    
- [Bias (UTC)](bias-utc.md)
    
- [Standardtime Element](standardtime.md)
    
- [Sesgo](bias.md)
    
- [Time](time.md)
    
- [DayOrder](dayorder.md)
    
- [Month](month.md)
    
- [DayOfWeek (TimeZone)](dayofweek-timezone.md)
    
- [DaylightTime](daylighttime.md)
    
- [MailboxDataArray](mailboxdataarray.md)
    
- [MailboxData](mailboxdata.md)
    
- [Correo electrónico (EmailAddressType)](email-emailaddresstype.md)
    
- [Address (cadena)](address-string.md)
    
- [AttendeeType](attendeetype.md)
    
- [ExcludeConflicts](excludeconflicts.md)
    
- [FreeBusyViewOptions](freebusyviewoptions.md)
    
- [TimeWindow](timewindow.md)
    
- [StartTime](starttime.md)
    
- [EndTime](endtime.md)
    
## <a name="successful-getuseravailability-operation-response"></a>Respuesta de operación GetUserAvailability correcta

En el ejemplo siguiente se muestra una respuesta correcta a la solicitud de operación **GetUserAvailability** . 
  
> [!NOTE]
> Los identificadores de eventos de calendario se han reducido para preservar la legibilidad. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="665" MinorBuildNumber="7" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <GetUserAvailabilityResponse xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <FreeBusyResponseArray>
        <FreeBusyResponse>
          <ResponseMessage ResponseClass="Success">
            <ResponseCode>NoError</ResponseCode>
          </ResponseMessage>
          <FreeBusyView>
            <FreeBusyViewType xmlns="https://schemas.microsoft.com/exchange/services/2006/types">DetailedMerged</FreeBusyViewType>
            <MergedFreeBusy xmlns="https://schemas.microsoft.com/exchange/services/2006/types">000002220220000000000000</MergedFreeBusy>
            <CalendarEventArray xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
              <CalendarEvent>
                <StartTime>2006-10-16T06:00:00-07:00</StartTime>
                <EndTime>2006-10-16T06:30:00-07:00</EndTime>
                <BusyType>Busy</BusyType>
                <CalendarEventDetails>
                  <ID>14B6414B0</ID>
                  <Subject>Meet with Contoso Account Executives</Subject>
                  <Location />
                  <IsMeeting>false</IsMeeting>
                  <IsRecurring>false</IsRecurring>
                  <IsException>false</IsException>
                  <IsReminderSet>false</IsReminderSet>
                  <IsPrivate>false</IsPrivate>
                </CalendarEventDetails>
              </CalendarEvent>
              <CalendarEvent>
                <StartTime>2006-10-16T07:00:00-07:00</StartTime>
                <EndTime>2006-10-16T08:00:00-07:00</EndTime>
                <BusyType>Busy</BusyType>
                <CalendarEventDetails>
                  <ID>E14B6414B0B</ID>
                  <Subject>Pick up my groceries</Subject>
                  <Location />
                  <IsMeeting>false</IsMeeting>
                  <IsRecurring>false</IsRecurring>
                  <IsException>false</IsException>
                  <IsReminderSet>false</IsReminderSet>
                  <IsPrivate>false</IsPrivate>
                </CalendarEventDetails>
              </CalendarEvent>
              <CalendarEvent>
                <StartTime>2006-10-16T09:40:00-07:00</StartTime>
                <EndTime>2006-10-16T10:10:00-07:00</EndTime>
                <BusyType>Busy</BusyType>
                <CalendarEventDetails>
                  <ID>14B6414B0B1</ID>
                  <Subject>Meet with doctor</Subject>
                  <Location>Kirkland</Location>
                  <IsMeeting>false</IsMeeting>
                  <IsRecurring>false</IsRecurring>
                  <IsException>false</IsException>
                  <IsReminderSet>false</IsReminderSet>
                  <IsPrivate>false</IsPrivate>
                </CalendarEventDetails>
              </CalendarEvent>
            </CalendarEventArray>
            <WorkingHours xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
              <TimeZone>
                <Bias>480</Bias>
                <StandardTime>
                  <Bias>0</Bias>
                  <Time>02:00:00</Time>
                  <DayOrder>5</DayOrder>
                  <Month>10</Month>
                  <DayOfWeek>Sunday</DayOfWeek>
                </StandardTime>
                <DaylightTime>
                  <Bias>-60</Bias>
                  <Time>02:00:00</Time>
                  <DayOrder>1</DayOrder>
                  <Month>4</Month>
                  <DayOfWeek>Sunday</DayOfWeek>
                </DaylightTime>
              </TimeZone>
              <WorkingPeriodArray>
                <WorkingPeriod>
                  <DayOfWeek>Monday Tuesday Wednesday Thursday Friday</DayOfWeek>
                  <StartTimeInMinutes>480</StartTimeInMinutes>
                  <EndTimeInMinutes>1020</EndTimeInMinutes>
                </WorkingPeriod>
              </WorkingPeriodArray>
            </WorkingHours>
          </FreeBusyView>
        </FreeBusyResponse>
        <FreeBusyResponse>
          <ResponseMessage ResponseClass="Success">
            <ResponseCode>NoError</ResponseCode>
          </ResponseMessage>
          <FreeBusyView>
            <FreeBusyViewType xmlns="https://schemas.microsoft.com/exchange/services/2006/types">FreeBusyMerged</FreeBusyViewType>
            <MergedFreeBusy xmlns="https://schemas.microsoft.com/exchange/services/2006/types">000000001100000000000000</MergedFreeBusy>
            <CalendarEventArray xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
              <CalendarEvent>
                <StartTime>2006-10-16T09:00:00-07:00</StartTime>
                <EndTime>2006-10-16T10:00:00-07:00</EndTime>
                <BusyType>Tentative</BusyType>
              </CalendarEvent>
            </CalendarEventArray>
            <WorkingHours xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
              <TimeZone>
                <Bias>480</Bias>
                <StandardTime>
                  <Bias>0</Bias>
                  <Time>02:00:00</Time>
                  <DayOrder>5</DayOrder>
                  <Month>10</Month>
                  <DayOfWeek>Sunday</DayOfWeek>
                </StandardTime>
                <DaylightTime>
                  <Bias>-60</Bias>
                  <Time>02:00:00</Time>
                  <DayOrder>1</DayOrder>
                  <Month>4</Month>
                  <DayOfWeek>Sunday</DayOfWeek>
                </DaylightTime>
              </TimeZone>
              <WorkingPeriodArray>
                <WorkingPeriod>
                  <DayOfWeek>Monday Tuesday Wednesday Thursday Friday</DayOfWeek>
                  <StartTimeInMinutes>480</StartTimeInMinutes>
                  <EndTimeInMinutes>1020</EndTimeInMinutes>
                </WorkingPeriod>
              </WorkingPeriodArray>
            </WorkingHours>
          </FreeBusyView>
        </FreeBusyResponse>
      </FreeBusyResponseArray>
    </GetUserAvailabilityResponse>
  </soap:Body>
</soap:Envelope>
```

La información de disponibilidad de cada usuario aparece en un elemento [FreeBusyResponse](freebusyresponse.md) único. El orden de los usuarios en la solicitud de operación **GetUserAvailability** determina el orden de los datos de disponibilidad para cada usuario en la respuesta. 
  
Se devolverá un error al cliente si el número de citas en el período de tiempo definido en la consulta es mayor que el número máximo especificado por el administrador. El número máximo predeterminado de citas es 10.000 instancias únicas y elementos de periodicidad ampliada. Solo un administrador puede configurar esta propiedad.
  
En la respuesta se usan los siguientes elementos:
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [GetUserAvailabilityResponse](getuseravailabilityresponse.md)
    
- [FreeBusyResponseArray](freebusyresponsearray.md)
    
- [FreeBusyResponse](freebusyresponse.md)
    
- [ResponseMessage](responsemessage.md)
    
- [ResponseCode](responsecode.md)
    
- [FreeBusyView](freebusyview.md)
    
- [FreeBusyViewType](freebusyviewtype.md)
    
- [MergedFreeBusy](mergedfreebusy.md)
    
- [CalendarEventArray](calendareventarray.md)
    
- [CalendarEvent](calendarevent.md)
    
- [StartTime](starttime.md)
    
- [EndTime](endtime.md)
    
- [BusyType](busytype.md)
    
- [CalendarEventDetails](calendareventdetails.md)
    
- [Id.](id.md)
    
- [Asunto (CalendarEventDetails)](subject-calendareventdetails.md)
    
- [Ubicación (CalendarEventDetails)](location-calendareventdetails.md)
    
- [IsMeeting (CalendarEventDetails)](ismeeting-calendareventdetails.md)
    
- [IsRecurring (CalendarEventDetails)](isrecurring-calendareventdetails.md)
    
- [IsException](isexception.md)
    
- [IsReminderSet](isreminderset.md)
    
- [IsPrivate](isprivate.md)
    
- [WorkingHours](workinghours-ex15websvcsotherref.md)
    
- [Zona horaria (disponibilidad)](timezone-availability.md)
    
- [Bias (UTC)](bias-utc.md)
    
- [Standardtime Element](standardtime.md)
    
- [Sesgo](bias.md)
    
- [Time](time.md)
    
- [DayOrder](dayorder.md)
    
- [Month](month.md)
    
- [DayOfWeek (TimeZone)](dayofweek-timezone.md)
    
- [DaylightTime](daylighttime.md)
    
- [WorkingPeriodArray](workingperiodarray.md)
    
- [WorkingPeriod](workingperiod.md)
    
- [DayOfWeek (WorkingPeriod)](dayofweek-workingperiod.md)
    
- [StartTimeInMinutes](starttimeinminutes.md)
    
- [EndTimeInMinutes](endtimeinminutes.md)
    
## <a name="see-also"></a>Vea también

- [Operaciones de EWS en Exchange](ews-operations-in-exchange.md)
    
- [Obtener disponibilidad del usuario](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)
    

