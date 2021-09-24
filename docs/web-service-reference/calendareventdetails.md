---
title: CalendarEventDetails
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- CalendarEventDetails
api_type:
- schema
ms.assetid: 2dca0192-b91b-4154-aa09-84da74e875e9
description: El elemento CalendarEventDetails proporciona información adicional sobre un evento de calendario.
ms.openlocfilehash: c332d17b1bb630b9635e64c484b4c5fd989f9845
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59516093"
---
# <a name="calendareventdetails"></a>CalendarEventDetails

El **elemento CalendarEventDetails** proporciona información adicional sobre un evento de calendario. 
  
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

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Id.](id.md) <br/> |Representa el identificador de entrada del elemento de calendario.  <br/> |
|[Subject (CalendarEventDetails)](subject-calendareventdetails.md) <br/> |Representa el asunto del elemento de calendario.  <br/> |
|[Location (CalendarEventDetails)](location-calendareventdetails.md) <br/> |Representa el campo de ubicación del elemento de calendario.  <br/> |
|[IsMeeting (CalendarEventDetails)](ismeeting-calendareventdetails.md) <br/> |Indica si el evento del calendario es una reunión o una cita.  <br/> |
|[IsRecurring (CalendarEventDetails)](isrecurring-calendareventdetails.md) <br/> |Indica si el evento de calendario es una instancia de un elemento de calendario periódico o un único elemento de calendario.  <br/> |
|[IsException](isexception.md) <br/> |Indica si se cambia una instancia de un elemento de calendario periódico desde el patrón.  <br/> |
|[IsReminderSet](isreminderset.md) <br/> |Indica si se ha establecido un aviso para el evento de calendario.  <br/> |
|[IsPrivate](isprivate.md) <br/> |Indica si el elemento de calendario es privado.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[CalendarEvent](calendarevent.md) <br/> |Representa una repetición de elemento de calendario única.  <br/> A continuación se muestra la expresión XPath 2.0 para este elemento:  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/CalendarEventArray/CalendarEvent[i]` <br/> |
   
## <a name="remarks"></a>Comentarios

Todos los elementos secundarios se enumeran en la secuencia en la que se producen. 
  
Si el [elemento IsPrivate](isprivate.md) es **true**, todos los demás elementos del elemento [CalendarEventDetails](calendareventdetails.md) no se devuelven en la respuesta. 
  
La operación GetUserAvailability no devuelve información detallada del autor de la llamada a menos que el autor de la llamada tenga acceso de lectura en el calendario del usuario de destino. Puede establecer permisos de acceso mediante el Shell Exchange administración.
  
El esquema que describe este elemento se encuentra en el directorio virtual EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor Acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también



[Operación GetUserAvailability](getuseravailability-operation.md)
  
[GetUserAvailabilityResponse](getuseravailabilityresponse.md)


[Obtener disponibilidad del usuario](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

