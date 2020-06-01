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
ms.openlocfilehash: 3e1dbba00bce4a1fdc53f3330527764c516890ab
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459072"
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

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Id.](id.md) <br/> |Representa el identificador de entrada del elemento de calendario.  <br/> |
|[Asunto (CalendarEventDetails)](subject-calendareventdetails.md) <br/> |Representa el asunto del elemento de calendario.  <br/> |
|[Ubicación (CalendarEventDetails)](location-calendareventdetails.md) <br/> |Representa el campo Ubicación del elemento de calendario.  <br/> |
|[IsMeeting (CalendarEventDetails)](ismeeting-calendareventdetails.md) <br/> |Indica si el evento de calendario es una reunión o una cita.  <br/> |
|[IsRecurring (CalendarEventDetails)](isrecurring-calendareventdetails.md) <br/> |Indica si el evento de calendario es una instancia de un elemento de calendario periódico o un solo elemento de calendario.  <br/> |
|[IsException](isexception.md) <br/> |Indica si se cambia la instancia de un elemento de calendario periódico desde el patrón.  <br/> |
|[IsReminderSet](isreminderset.md) <br/> |Indica si se ha establecido un aviso para el evento de calendario.  <br/> |
|[IsPrivate](isprivate.md) <br/> |Indica si el elemento de calendario es privado.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[CalendarEvent](calendarevent.md) <br/> |Representa una ocurrencia única del elemento de calendario.  <br/> La siguiente es la expresión XPath 2,0 a este elemento:  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/CalendarEventArray/CalendarEvent[i]` <br/> |
   
## <a name="remarks"></a>Comentarios

Todos los elementos secundarios se enumeran en la secuencia en que se producen. 
  
Si el elemento [IsPrivate](isprivate.md) es **true**, el resto de los elementos del elemento [CalendarEventDetails](calendareventdetails.md) no se devuelven en la respuesta. 
  
La operación GetUserAvailability no devuelve información detallada del autor de la llamada a menos que el autor de la llamada tenga acceso de lectura en el calendario del usuario de destino. Puede establecer permisos de acceso mediante el shell de administración de Exchange.
  
El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también



[Operación GetUserAvailability](getuseravailability-operation.md)
  
[GetUserAvailabilityResponse](getuseravailabilityresponse.md)


[Obtener disponibilidad del usuario](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

