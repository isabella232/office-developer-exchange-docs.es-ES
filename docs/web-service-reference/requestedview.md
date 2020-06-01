---
title: RequestedView
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RequestedView
api_type:
- schema
ms.assetid: e2b4cf8c-5d43-4cd8-b86d-cc27a5d2f095
description: El elemento RequestedView define el tipo de información de calendario que solicita un cliente.
ms.openlocfilehash: bc4f863841fc5a7d1d23f0bd4c7c2895d2593a2d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459163"
---
# <a name="requestedview"></a>RequestedView

El elemento **RequestedView** define el tipo de información de calendario que solicita un cliente. 
  
[GetUserAvailabilityRequest](getuseravailabilityrequest.md)
  
[FreeBusyViewOptions](freebusyviewoptions.md)
  
[RequestedView](requestedview.md)
  
```xml
<RequestedView>None or MergedOnly or FreeBusy or FreeBusyMerged or Detailed or DetailedMerged</RequestedView>
```

 **FreeBusyViewType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[FreeBusyViewOptions](freebusyviewoptions.md) <br/> |Especifica el tipo de información de disponibilidad devuelta en la respuesta.  <br/> A continuación se encuentra la expresión XPath de este elemento:  <br/>  `/GetUserAvailabilityRequest/FreeBusyViewOptions` <br/> |
   
## <a name="text-value"></a>Valor de texto

Se requiere un valor de texto. En la siguiente tabla se enumeran los valores posibles para este elemento.
  
|**Valor**|**Descripción**|
|:-----|:-----|
|Ninguno  <br/> |Este valor no es válido para las solicitudes. Este valor es válido para las respuestas.  <br/> |
|MergedOnly  <br/> |Representa una secuencia de disponibilidad agregada. En escenarios entre bosques en los que el usuario de destino de un bosque no tiene un servicio de disponibilidad configurado, el servicio de disponibilidad del solicitante recupera la información de disponibilidad del usuario de destino de la carpeta pública de disponibilidad. Como las carpetas públicas solo almacenan la información de disponibilidad en formulario combinado, **MergedOnly** es la única información disponible.  <br/> |
|FreeBusy  <br/> |Representa la información de estado heredada: libre, ocupado, provisional y OOF. Esto también incluye las horas de inicio y finalización de las citas. Esta vista es más rica que la vista disponibilidad heredada porque se proporcionan horas de inicio y finalización de una reunión individual, en lugar de una secuencia de disponibilidad agregada.  <br/> |
|FreeBusyMerged  <br/> |Representa todas las propiedades de **FreeBusy** con una secuencia de información de disponibilidad combinada.  <br/> |
|Detallada  <br/> |Representa la información de estado heredada: libre, ocupado, provisional y OOF; las horas de inicio y finalización de las citas; y diversas propiedades de la cita, como el asunto, la ubicación y la importancia. Esta vista solicitada devolverá la cantidad máxima de información que el usuario solicitante tiene privilegio. Si la información de disponibilidad combinada solo está disponible, al igual que con la solicitud de información para los usuarios en un bosque de Microsoft Exchange Server 2003, se devolverá **MergedOnly** . De lo contrario, se devolverá **FreeBusy** o **Detailed** .  <br/> |
|DetailedMerged  <br/> |Representa todas las propiedades en **detalle** con una secuencia de información de disponibilidad combinada. Si la información de disponibilidad combinada solo está disponible, se devolverá **MergedOnly** . De lo contrario, se devolverá **FreeBusyMerged** o **DetailedMerged** .  <br/> |
   
## <a name="remarks"></a>Comentarios

El valor establecido por este elemento se devuelve con el elemento [FreeBusyViewType](freebusyviewtype.md) en la respuesta. 
  
En la siguiente tabla se muestran los elementos que se devuelven para los distintos tipos de vista y la propiedad MAPI correspondiente. Cada tipo de vista se basa en el tipo de vista anterior.
  
|**Tipo de vista de disponibilidad**|**Propiedades**|**Propiedad Calendar de MAPI**|
|:-----|:-----|:-----|
|**MergedOnly** <br/> |MergedFreeBusyStream  <br/> ||
|**FreeBusy** <br/> |Estado clásico  <br/> |PropTag (0x80860003)  <br/> |
|**FreeBusy** <br/> |Horas laborables  <br/> ||
|**FreeBusy** <br/> |Hora de inicio  <br/> |PR_START_DATE  <br/> |
|**FreeBusy** <br/> |Hora de finalización  <br/> |PR_END_DATE  <br/> |
|**FreeBusyMerged** <br/> |Estado clásico  <br/> |PropTag (0x80860003)  <br/> |
|**FreeBusyMerged** <br/> |Horas laborables  <br/> ||
|**FreeBusyMerged** <br/> |Hora de inicio  <br/> |PR_START_DATE  <br/> |
|**FreeBusyMerged** <br/> |Hora de finalización  <br/> |PR_END_DATE  <br/> |
|**FreeBusyMerged** <br/> |MergedFreeBusyStream  <br/> ||
|**Detallada** <br/> |Estado clásico  <br/> |PropTag (0x80860003)  <br/> |
|**Detallada** <br/> |Horas laborables  <br/> ||
|**Detallada** <br/> |Hora de inicio  <br/> |PR_START_DATE  <br/> |
|**Detallada** <br/> |Hora de finalización  <br/> |PR_END_DATE  <br/> |
|**Detallada** <br/> |Subject  <br/> |PR_SUBJECT  <br/> |
|**Detallada** <br/> |Ubicación  <br/> |PR_LOCATION  <br/> |
|**Detallada** <br/> |Identificador de entrada (a menos que sea privado)  <br/> ||
|**Detallada** <br/> |Marca privada  <br/> ||
|**Detallada** <br/> |IsMeeting  <br/> ||
|**Detallada** <br/> |IsRecurring  <br/> ||
|**Detallada** <br/> |IsException  <br/> ||
|**Detallada** <br/> |IsReminderSet  <br/> ||
|**DetailedMerged** <br/> |Estado clásico  <br/> |PropTag (0x80860003)  <br/> |
|**DetailedMerged** <br/> |Horas laborables  <br/> ||
|**DetailedMerged** <br/> |Hora de inicio  <br/> |PR_START_DATE  <br/> |
|**DetailedMerged** <br/> |Hora de finalización  <br/> |PR_END_DATE  <br/> |
|**DetailedMerged** <br/> |Subject  <br/> |PR_SUBJECT  <br/> |
|**DetailedMerged** <br/> |Ubicación  <br/> |PR_LOCATION  <br/> |
|**DetailedMerged** <br/> |Identificador de entrada (a menos que sea privado)  <br/> ||
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
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también



[Operación GetUserAvailability](getuseravailability-operation.md)


[Obtener disponibilidad del usuario](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

