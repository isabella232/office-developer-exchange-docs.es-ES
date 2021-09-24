---
title: CalendarEvent
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- CalendarEvent
api_type:
- schema
ms.assetid: 91958c01-1fcb-4ac0-8601-5e5b434c988a
description: El elemento CalendarEvent representa una aparición única del elemento de calendario.
ms.openlocfilehash: fd57517595659f2081c82fe9f4665ce2c39059fe
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59514826"
---
# <a name="calendarevent"></a>CalendarEvent

El **elemento CalendarEvent** representa una aparición única del elemento de calendario. 
  
[GetUserAvailabilityResponse](getuseravailabilityresponse.md)
  
[FreeBusyResponseArray](freebusyresponsearray.md)
  
[FreeBusyResponse](freebusyresponse.md)
  
[FreeBusyView](freebusyview.md)
  
[CalendarEventArray](calendareventarray.md)
  
[CalendarEvent](calendarevent.md)
  
```xml
<CalendarEvent>
   <StartTime>...</StartTime>
   <EndTime>...</EndTime>
   <BusyType>...</BusyType>
   <CalendarEventDetails>...</CalendarEventDetails>
</CalendarEvent>
```

 **CalendarEvent**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[StartTime](starttime.md) <br/> |Representa el inicio de un evento de calendario. Este es un elemento secundario obligatorio.  <br/> |
|[EndTime](endtime.md) <br/> |Representa el final de un evento de calendario. Este es un elemento secundario obligatorio.  <br/> |
|[BusyType](busytype.md) <br/> |Representa el conjunto de estado de disponibilidad de un evento de calendario. Este es un elemento secundario obligatorio.  <br/> |
|[CalendarEventDetails](calendareventdetails.md) <br/> |Proporciona información adicional para un evento de calendario. Se trata de un elemento secundario opcional.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[CalendarEventArray](calendareventarray.md) <br/> |Contiene un conjunto de repeticiones de elementos de calendario únicos que representan la disponibilidad del usuario solicitado.  <br/> A continuación se muestra la expresión XPath 2.0 para este elemento:  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/CalendarEventArray` <br/> |
   
## <a name="remarks"></a>Comentarios

La cita y las horas de reunión se devuelven en la zona horaria del cliente. Todos los elementos secundarios se enumeran en la secuencia en la que se producen. El nivel de detalle proporcionado por este elemento depende de los permisos concedidos al solicitante.
  
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

