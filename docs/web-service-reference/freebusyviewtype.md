---
title: FreeBusyViewType
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FreeBusyViewType
api_type:
- schema
ms.assetid: 7c7f82ba-fa52-4a3e-bec7-39d373c66fc7
description: El elemento FreeBusyViewType representa el tipo de información de libre/ocupado devuelto en la respuesta.
ms.openlocfilehash: fe965d062f72d99dff7148f4d00b12fd8c4e1366
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764733"
---
# <a name="freebusyviewtype"></a>FreeBusyViewType

El elemento **FreeBusyViewType** representa el tipo de información de libre/ocupado devuelto en la respuesta. 
  
[GetUserAvailabilityResponse](getuseravailabilityresponse.md)
  
[FreeBusyResponseArray](freebusyresponsearray.md)
  
[FreeBusyResponse](freebusyresponse.md)
  
[FreeBusyView](freebusyview.md)
  
[FreeBusyViewType](freebusyviewtype.md)
  
```xml
<FreeBusyViewType>None or MergedOnly or FreeBusy or FreeBusyMerged or Detailed or DetailedMerged</FreeBusyViewType>
```

 **FreeBusyViewType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[FreeBusyView](freebusyview.md) <br/> |Contiene la información de disponibilidad para un usuario específico.  <br/> La siguiente es la expresión de XPath para este elemento:  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView` <br/> |
   
## <a name="text-value"></a>Valor de texto

Se requiere un valor de texto. En la siguiente tabla se enumera los valores posibles para este elemento.
  
|**Valor**|**Descripción**|
|:-----|:-----|
|None  <br/> |Este valor no es válido para las solicitudes. Este valor es válido para las respuestas.  <br/> |
|MergedOnly  <br/> |Representa una secuencia de libre/ocupado agregada. En los escenarios entre bosques en la que el usuario de destino en un bosque no tiene configurado un servicio de disponibilidad, el servicio de disponibilidad del solicitante recupera información de disponibilidad del usuario de destino de la carpeta pública de disponibilidad. Dado que las carpetas públicas sólo almacenan información de disponibilidad en formulario combinado, **MergedOnly** es la información sólo está disponible.  <br/> |
|FreeBusy  <br/> |Representa la información de estado heredado: libre, ocupado, provisional y fuera de la oficina. Esto también incluye las horas de inicio y finalización de las citas. Esta vista es más completa de la libre/ocupado heredado ver porque individuales de la reunión de inicio y finalización veces se proporcionan en lugar de una secuencia de libre/ocupado agregada.  <br/> |
|FreeBusyMerged  <br/> |Representa todas las propiedades en **FreeBusy** con una secuencia de información de disponibilidad de libre/ocupado combinadas.  <br/> |
|Detallada  <br/> |Representa la información de estado heredado: libre, ocupado, provisional y fuera de la oficina; las horas de inicio y finalización de las citas; y varias propiedades de la cita, como el asunto, ubicación y su importancia. Esta vista solicitada devolverá la cantidad máxima de información para la que el usuario solicitante tiene privilegios. Si la información de libre/ocupado combinada sólo está disponible, como con la información que solicita a los usuarios de un bosque de Microsoft Exchange Server 2003, **MergedOnly** se devolverán. De lo contrario, se devolverán **FreeBusy** o **detallado** .  <br/> Si se especifica **Detailed** para obtener una lista de distribución, se combina la información de libre/ocupado para los miembros de la lista y se devuelve **MergedOnly** .  <br/> |
|DetailedMerged  <br/> |Representa todas las propiedades en **Detailed** con una secuencia de información de disponibilidad de libre/ocupado combinadas. Si sólo hay información de libre/ocupado combinada está disponible, por ejemplo, si existe el buzón de correo en un equipo que ejecuta Exchange 2003, se devolverán **MergedOnly** . De lo contrario, se devolverán **FreeBusyMerged** o **DetailedMerged** .  <br/> |
   
## <a name="remarks"></a>Notas

Este elemento es necesario si se usa el elemento [FreeBusyView](freebusyview.md) . El tipo de información de disponibilidad devuelta se designa en el elemento [RequestedView](requestedview.md) . El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente. 
  
En la siguiente tabla se muestra lo que se devuelve para los tipos de vista diferentes y la propiedad correspondiente de MAPI. Cada tipo de vista se basa en el tipo de vista anterior.
  
|**FreeBusyViewType**|**Properties**|**Calendario MAPI (propiedad)**|
|:-----|:-----|:-----|
|**MergedOnly** <br/> |MergedFreeBusyStream  <br/> ||
|**FreeBusy** <br/> |Estado clásica  <br/> |PropTag (0x80860003)  <br/> |
|**FreeBusy** <br/> |Horario laboral  <br/> ||
|**FreeBusy** <br/> |Hora de inicio  <br/> |PR_START_DATE  <br/> |
|**FreeBusy** <br/> |Hora de finalización  <br/> |PR_END_DATE  <br/> |
|**FreeBusyMerged** <br/> |Estado clásica  <br/> |PropTag (0x80860003)  <br/> |
|**FreeBusyMerged** <br/> |Horario laboral  <br/> ||
|**FreeBusyMerged** <br/> |Hora de inicio  <br/> |PR_START_DATE  <br/> |
|**FreeBusyMerged** <br/> |Hora de finalización  <br/> |PR_END_DATE  <br/> |
|**FreeBusyMerged** <br/> |MergedFreeBusyStream  <br/> ||
|**Detallada** <br/> |Estado clásica  <br/> |PropTag (0x80860003)  <br/> |
|**Detallada** <br/> |Horario laboral  <br/> ||
|**Detallada** <br/> |Hora de inicio  <br/> |PR_START_DATE  <br/> |
|**Detallada** <br/> |Hora de finalización  <br/> |PR_END_DATE  <br/> |
|**Detallada** <br/> |Subject  <br/> |PR_SUBJECT  <br/> |
|**Detallada** <br/> |Ubicación  <br/> |PR_LOCATION  <br/> |
|**Detallada** <br/> |Entrada Id(unless private)  <br/> ||
|**Detallada** <br/> |Marca privada  <br/> ||
|**Detallada** <br/> |IsMeeting  <br/> ||
|**Detallada** <br/> |IsRecurring  <br/> ||
|**Detallada** <br/> |IsException  <br/> ||
|**Detallada** <br/> |IsReminderSet  <br/> ||
|**Detallada** <br/> |Fuera del mensaje de Office (si se solicita)  <br/> ||
|**DetailedMerged** <br/> |Estado clásica  <br/> |PropTag (0x80860003)  <br/> |
|**DetailedMerged** <br/> |Horario laboral  <br/> ||
|**DetailedMerged** <br/> |Hora de inicio  <br/> |PR_START_DATE  <br/> |
|**DetailedMerged** <br/> |Hora de finalización  <br/> |PR_END_DATE  <br/> |
|**DetailedMerged** <br/> |Subject  <br/> |PR_SUBJECT  <br/> |
|**DetailedMerged** <br/> |Ubicación  <br/> |PR_LOCATION  <br/> |
|**DetailedMerged** <br/> |Entrada Id(unless private)  <br/> ||
|**DetailedMerged** <br/> |Marca privada  <br/> ||
|**DetailedMerged** <br/> |MergedFreeBusyStream  <br/> ||
|**DetailedMerged** <br/> |IsMeeting  <br/> ||
|**DetailedMerged** <br/> |IsRecurring  <br/> ||
|**DetailedMerged** <br/> |IsException  <br/> ||
|**DetailedMerged** <br/> |IsReminderSet  <br/> ||
   
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

