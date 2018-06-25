---
title: GetUserAvailabilityResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetUserAvailabilityResponse
api_type:
- schema
ms.assetid: 6999510a-d60e-43da-8964-57b5fb3e9d11
description: El elemento GetUserAvailabilityResponse es el elemento raíz que contiene las propiedades que definen la información de disponibilidad del usuario o sugeridas información de tiempo de la reunión.
ms.openlocfilehash: 0a30dc8ebc11b1f818b2c27b0ea68fc135ec0925
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19835684"
---
# <a name="getuseravailabilityresponse"></a>GetUserAvailabilityResponse

El elemento **GetUserAvailabilityResponse** es el elemento raíz que contiene las propiedades que definen la información de disponibilidad del usuario o sugeridas información de tiempo de la reunión. 
  
```xml
<GetUserAvailabilityResponse>
   <FreeBusyResponseArray>...</FreeBusyResponseArray>
   <SuggestionsResponse>...</SuggestionsResponse>
</GetUserAvailabilityResponse>
```

 **GetUserAvailabilityResponseType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[FreeBusyResponseArray](freebusyresponsearray.md) <br/> |Contiene información sobre la disponibilidad de los usuarios solicitado y el estado de la respuesta.  <br/> |
|[SuggestionsResponse](suggestionsresponse.md) <br/> |Contiene datos de sugerencia y la información de estado de respuesta para solicitado sugerencias de reunión.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

Ninguno.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.
  
## <a name="example"></a>Ejemplo

El siguiente ejemplo de una respuesta GetUserAvailability muestra una respuesta a una solicitud de GetUserAvailability.
  
```
<?xml version="1.0" encoding="utf-8" ?>
<GetUserAvailabilityResponse xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
                             xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <FreeBusyResponseArray xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
    <FreeBusyResponse>
      <ResponseMessage ResponseClass="Success">
        <Path select="/m:GetUserAvailabilityRequest/MailboxDataArray[0]" />
      </ResponseMessage>
      <FreeBusyView>
        <FreeBusyViewType xmlns="http://schemas.microsoft.com/exchange/services/2006/types">Detailed</FreeBusyViewType>
        <CalendarEventArray xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
          <CalendarEvent>
            <StartTime>2006-02-28T19:00:00-08:00</StartTime>
            <EndTime>2006-02-28T23:30:00-08:00</EndTime>
            <BusyType>OOF</BusyType>
            <IsPrivate>false</IsPrivate>
            <CalendarEventDetails>
              <ID>00000</ID>
              <Subject>Exercise</Subject>
              <Location>the gym</Location>
              <IsMeeting>false</IsMeeting>
              <IsRecurring>false</IsRecurring>
              <IsException>false</IsException>
              <IsReminderSet>true</IsReminderSet>
            </CalendarEventDetails>
          </CalendarEvent>
        </CalendarEventArray>
        <WorkingHours xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
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
```

El contenido del [identificador de](id.md) elemento se ha más cortos para conservar la legibilidad. 
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Vea también



[GetUserAvailabilityRequest](getuseravailabilityrequest.md)


[Obtención de disponibilidad del usuario](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

