---
title: Hora
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Time
api_type:
- schema
ms.assetid: c4b98be7-141c-4ba8-97ef-9ad1ed19f61f
description: El elemento de tiempo representa el tiempo de transición del día a y desde el horario estándar y del horario de verano.
ms.openlocfilehash: 716487fb7ed64dbaa6fa97caf1ea608e4673d2ef
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19840652"
---
# <a name="time"></a>Time

El elemento de **tiempo** representa el tiempo de transición del día a y desde el horario estándar y del horario de verano. 
  
```xml
<Time>...</Time>
```

 **string**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[StandardTime](standardtime.md) <br/> | Representa un desplazamiento desde el momento en relación con hora Universal coordinada (UTC), representado por el elemento [Bias (UTC)](bias-utc.md) . Este elemento también contiene información sobre la transición a la hora estándar de horario de verano en regiones donde se observa el horario de verano.  <br/><br/>  Los siguientes son las expresiones de XPath para el elemento [StandardTime](standardtime.md) : <br/> <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/TimeZone/StandardTime`<br/> <br/>  `/GetUserAvailabilityRequest/TimeZone/StandardTime` <br/> |
|[DaylightTime](daylighttime.md) <br/> | Representa un desplazamiento de la hora con respecto a UTC representada por el elemento [Bias (UTC)](bias-utc.md) en las regiones donde se observa el horario de verano. Este elemento también contiene información acerca de cuándo se produce la transición al horario de verano de tiempo estándar.  <br/><br/>  Los siguientes son las expresiones de XPath para el elemento [DaylightTime](daylighttime.md) :  <br/><br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/TimeZone/DaylightTime` <br/><br/>  `/GetUserAvailabilityRequest/TimeZone/DaylightTime` <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto representa horas, minutos y segundos en el siguiente formato: ss.
  
## <a name="remarks"></a>Notas

Cuando se produce el elemento de **tiempo** en el elemento [DaylightTime](daylighttime.md) , representa la hora del día en que se produce la transición desde el horario de verano a la hora estándar. Cuando se produce el elemento de [tiempo](time.md) en el elemento [StandardTime](standardtime.md) , que representa la hora del día en que se produce la transición desde el horario estándar al horario de verano. 
  
Este elemento tiene una repetición mínima de cero y una máxima aparición de uno.
  
## <a name="example"></a>Ejemplo

La siguiente parte de una solicitud representa un tiempo de transición de 2 A.M. desde el horario estándar al horario de verano.
  
```xml
<StandardTime>
   <Bias>0</Bias>
   <Time>02:00:00</Time>
   <DayOrder>5</DayOrder>
   <Month>10</Month>
   <DayOfWeek>Sunday</DayOfWeek>
</StandardTime
```

## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Ver también

- [Operación GetUserAvailability](getuseravailability-operation.md)
- [Obtención de disponibilidad del usuario](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

