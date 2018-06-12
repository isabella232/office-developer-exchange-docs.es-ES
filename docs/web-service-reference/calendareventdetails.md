---
title: CalendarEventDetails
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CalendarEventDetails
api_type:
- schema
ms.assetid: 2dca0192-b91b-4154-aa09-84da74e875e9
description: El elemento CalendarEventDetails proporciona información adicional acerca de un evento de calendario.
ms.openlocfilehash: 8df4f3ed4f66c7dcba00e1f0c5b0c383075da0a0
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763697"
---
# <a name="calendareventdetails"></a>CalendarEventDetails

El elemento **CalendarEventDetails** proporciona información adicional acerca de un evento de calendario. 
  
[GetUserAvailabilityResponse](getuseravailabilityresponse.md)
  
[FreeBusyResponseArray](freebusyresponsearray.md)
  
[FreeBusyResponse](freebusyresponse.md)
  
[FreeBusyView](freebusyview.md)
  
[CalendarEventArray](calendareventarray.md)
  
[CalendarEvent](calendarevent.md)
  
[CalendarEventDetails](calendareventdetails.md)
  
```xml
<CalendarEventDetails>
   <ID/>
   <Subject/>
   <Location/>
   <IsMeeting/>
   <IsRecurring/>
   <IsException/>
   <IsReminderSet/>
   <IsPrivate/>
</CalendarEventDetails>
```

 **CalendarEventDetails**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[ID](id.md) <br/> |Representa el identificador de entrada del elemento de calendario.  <br/> |
|[Asunto (CalendarEventDetails)](subject-calendareventdetails.md) <br/> |Representa al asunto del elemento de calendario.  <br/> |
|[Ubicación (CalendarEventDetails)](location-calendareventdetails.md) <br/> |Representa el campo de ubicación del elemento de calendario.  <br/> |
|[IsMeeting (CalendarEventDetails)](ismeeting-calendareventdetails.md) <br/> |Indica si el evento de calendario es una reunión o una cita.  <br/> |
|[IsRecurring (CalendarEventDetails)](isrecurring-calendareventdetails.md) <br/> |Indica si el evento de calendario es una instancia de un elemento periódico del calendario o un elemento de calendario único.  <br/> |
|[IsException](isexception.md) <br/> |Indica si se cambia una instancia de un elemento periódico del calendario desde el maestro.  <br/> |
|[IsReminderSet](isreminderset.md) <br/> |Indica si se ha establecido un aviso para el evento de calendario.  <br/> |
|[IsPrivate](isprivate.md) <br/> |Indica si el elemento de calendario es privado.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[CalendarEvent](calendarevent.md) <br/> |Representa una repetición del elemento de calendario único.  <br/> La siguiente es la expresión de XPath 2.0 para este elemento:  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/CalendarEventArray/CalendarEvent[i]` <br/> |
   
## <a name="remarks"></a>Notas

Todos los elementos secundarios se enumeran en la secuencia en la que se producen. 
  
Si el elemento [IsPrivate](isprivate.md) es **true**, todos los demás elementos en el elemento [CalendarEventDetails](calendareventdetails.md) no se devuelven en la respuesta. 
  
La operación GetUserAvailability no devuelve información detallada autor de la llamada a menos que el autor de la llamada tiene acceso de lectura en el calendario del usuario de destino. Puede establecer permisos de acceso mediante el Shell de administración de Exchange.
  
El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Ver también



[Operación GetUserAvailability](getuseravailability-operation.md)
  
[GetUserAvailabilityResponse](getuseravailabilityresponse.md)


[Obtención de disponibilidad del usuario](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

