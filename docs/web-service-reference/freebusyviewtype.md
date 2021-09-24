---
title: FreeBusyViewType
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- FreeBusyViewType
api_type:
- schema
ms.assetid: 7c7f82ba-fa52-4a3e-bec7-39d373c66fc7
description: El elemento FreeBusyViewType representa el tipo de información de disponibilidad devuelta en la respuesta.
ms.openlocfilehash: 6eec490b39ccb9c02e7a16c8da7cfdd57f9b92c5
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59509934"
---
# <a name="freebusyviewtype"></a>FreeBusyViewType

El **elemento FreeBusyViewType** representa el tipo de información de disponibilidad devuelta en la respuesta. 
  
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

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[FreeBusyView](freebusyview.md) <br/> |Contiene información de disponibilidad para un usuario específico.  <br/> A continuación se muestra la expresión XPath de este elemento:  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView` <br/> |
   
## <a name="text-value"></a>Valor de texto

Se requiere un valor de texto. En la tabla siguiente se enumeran los valores posibles para este elemento.
  
|**Valor**|**Descripción**|
|:-----|:-----|
|Ninguno  <br/> |Este valor no es válido para las solicitudes. Este valor es válido para las respuestas.  <br/> |
|MergedOnly  <br/> |Representa una secuencia de disponibilidad agregada. En escenarios entre bosques en los que el usuario de destino de un bosque no tiene configurado un servicio de disponibilidad, el servicio de disponibilidad del solicitante recupera la información de disponibilidad del usuario de destino de la carpeta pública de disponibilidad. Dado que las carpetas públicas solo almacenan información de disponibilidad en forma combinada, **MergedOnly** es la única información disponible.  <br/> |
|FreeBusy  <br/> |Representa la información de estado heredada: libre, ocupado, provisional y OOF. Esto también incluye las horas de inicio y finalización de las citas. Esta vista es más rica que la vista de disponibilidad heredada porque se proporcionan horas de inicio y finalización de reuniones individuales en lugar de una secuencia de disponibilidad agregada.  <br/> |
|FreeBusyMerged  <br/> |Representa todas las propiedades de **FreeBusy con** una secuencia de información de disponibilidad de disponibilidad combinada.  <br/> |
|Detallado  <br/> |Representa la información de estado heredada: libre, ocupado, provisional y OOF; las horas de inicio y finalización de las citas; y varias propiedades de la cita, como asunto, ubicación e importancia. Esta vista solicitada devolverá la cantidad máxima de información para la que el usuario solicitante tiene privilegios. Si la información de disponibilidad combinada solo está disponible, al igual que con la solicitud de información para los usuarios de un bosque de Microsoft Exchange Server 2003, se devolverá **MergedOnly.** De lo contrario, **se devolverá FreeBusy** o **Detailed.**  <br/> Si **se especifica Detailed** para una lista de distribución, se combina la información de disponibilidad de los miembros de la lista y se devuelve **MergedOnly.**  <br/> |
|DetailedMerged  <br/> |Representa todas las propiedades de **Detailed** con una secuencia de información de disponibilidad de disponibilidad combinada. Si solo está disponible la información de disponibilidad combinada, por ejemplo, si el buzón existe en un equipo que ejecuta Exchange 2003, se devolverá **MergedOnly.** De lo contrario, **se devolverá FreeBusyMerged** **o DetailedMerged.**  <br/> |
   
## <a name="remarks"></a>Comentarios

Este elemento es necesario si se usa el elemento [FreeBusyView.](freebusyview.md) El tipo de información de disponibilidad devuelta se designa en el [elemento RequestedView.](requestedview.md) El esquema que describe este elemento se encuentra en el directorio virtual EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor Acceso de cliente. 
  
En la tabla siguiente se muestra lo que se devuelve para los diferentes tipos de vista y la propiedad MAPI correspondiente. Cada tipo de vista se basa en el tipo de vista anterior.
  
|**FreeBusyViewType**|**Propiedades**|**Propiedad Calendar MAPI**|
|:-----|:-----|:-----|
|**MergedOnly** <br/> |MergedFreeBusyStream  <br/> ||
|**FreeBusy** <br/> |Estado clásico  <br/> |PropTag (0x80860003)  <br/> |
|**FreeBusy** <br/> |Horario laboral  <br/> ||
|**FreeBusy** <br/> |Hora de inicio  <br/> |PR_START_DATE  <br/> |
|**FreeBusy** <br/> |Hora de finalización  <br/> |PR_END_DATE  <br/> |
|**FreeBusyMerged** <br/> |Estado clásico  <br/> |PropTag (0x80860003)  <br/> |
|**FreeBusyMerged** <br/> |Horario laboral  <br/> ||
|**FreeBusyMerged** <br/> |Hora de inicio  <br/> |PR_START_DATE  <br/> |
|**FreeBusyMerged** <br/> |Hora de finalización  <br/> |PR_END_DATE  <br/> |
|**FreeBusyMerged** <br/> |MergedFreeBusyStream  <br/> ||
|**Detallado** <br/> |Estado clásico  <br/> |PropTag (0x80860003)  <br/> |
|**Detallado** <br/> |Horario laboral  <br/> ||
|**Detallado** <br/> |Hora de inicio  <br/> |PR_START_DATE  <br/> |
|**Detallado** <br/> |Hora de finalización  <br/> |PR_END_DATE  <br/> |
|**Detallado** <br/> |Subject  <br/> |PR_SUBJECT  <br/> |
|**Detallado** <br/> |Ubicación  <br/> |PR_LOCATION  <br/> |
|**Detallado** <br/> |Entry-Id(unless private)  <br/> ||
|**Detallado** <br/> |Marca privada  <br/> ||
|**Detallado** <br/> |IsMeeting  <br/> ||
|**Detallado** <br/> |IsRecurring  <br/> ||
|**Detallado** <br/> |IsException  <br/> ||
|**Detallado** <br/> |IsReminderSet  <br/> ||
|**Detallado** <br/> |Mensaje Office (si se solicita)  <br/> ||
|**DetailedMerged** <br/> |Estado clásico  <br/> |PropTag (0x80860003)  <br/> |
|**DetailedMerged** <br/> |Horario laboral  <br/> ||
|**DetailedMerged** <br/> |Hora de inicio  <br/> |PR_START_DATE  <br/> |
|**DetailedMerged** <br/> |Hora de finalización  <br/> |PR_END_DATE  <br/> |
|**DetailedMerged** <br/> |Subject  <br/> |PR_SUBJECT  <br/> |
|**DetailedMerged** <br/> |Ubicación  <br/> |PR_LOCATION  <br/> |
|**DetailedMerged** <br/> |Entry-Id(unless private)  <br/> ||
|**DetailedMerged** <br/> |Marca privada  <br/> ||
|**DetailedMerged** <br/> |MergedFreeBusyStream  <br/> ||
|**DetailedMerged** <br/> |IsMeeting  <br/> ||
|**DetailedMerged** <br/> |IsRecurring  <br/> ||
|**DetailedMerged** <br/> |IsException  <br/> ||
|**DetailedMerged** <br/> |IsReminderSet  <br/> ||
   
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

