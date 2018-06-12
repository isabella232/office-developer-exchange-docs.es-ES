---
title: StandardTime
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- StandardTime
api_type:
- schema
ms.assetid: 13084726-ab24-4009-be99-c4a4273c9e05
description: El elemento StandardTime representa un desplazamiento desde el momento en relación con hora Universal coordinada (UTC) que está representada por el elemento Bias (UTC). Este elemento también contiene información sobre la transición a la hora estándar de horario de verano en regiones donde se observa el horario de verano.
ms.openlocfilehash: 726c31ffba06c1c437711b88444ec5eba45b520d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19837546"
---
# <a name="standardtime"></a>StandardTime

El elemento **StandardTime** representa un desplazamiento desde el momento en relación con hora Universal coordinada (UTC) que está representada por el elemento [Bias (UTC)](bias-utc.md) . Este elemento también contiene información sobre la transición a la hora estándar de horario de verano en regiones donde se observa el horario de verano. 
  
- [TimeZone (disponibilidad)](timezone-availability.md)
- [StandardTime](standardtime.md)
  
```xml
<StandardTime>
   <Bias>int</Bias>
   <Time>string</Time>
   <DayOrder>short</DayOrder>
   <Month>short</Month>
   <DayOfWeek>Sunday or Monday or Tuesday or Wednesday or Thursday or Friday or Saturday</DayOfWeek>
   <Year>string</Year>
</StandardTime>
```

 **SerializableTimeZoneTime**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[Bias](bias.md) <br/> |Representa el desplazamiento desde el desplazamiento de UTC que se identifica con el elemento [Bias (UTC)](bias-utc.md) para la hora estándar y el horario de verano. Este valor está en minutos.  <br/> |
|[Time](time.md) <br/> |Representa el tiempo de transición del día a y desde el horario estándar y del horario de verano.  <br/> |
|[DayOrder](dayorder.md) <br/> |Representa la aparición de _n_th del día que se especifica en el elemento [DayOfWeek (TimeZone)](dayofweek-timezone.md) que representa la fecha de transición desde y a la hora estándar y el horario de verano.  <br/> |
|[Month](month.md) <br/> |Representa el mes de transición del año a y desde el horario estándar y del horario de verano.  <br/> |
|[DayOfWeek (TimeZone)](dayofweek-timezone.md) <br/> |Representa el día de la semana cuando se produce la transición a y desde el horario estándar y del horario de verano.  <br/> |
|[year](year.md) <br/> |Define una zona horaria que cambia según el año. Este elemento es opcional. Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[TimeZone (disponibilidad)](timezone-availability.md) <br/> | Contiene elementos que identifican la información de zona horaria. Este elemento también contiene información sobre la transición entre la hora estándar y el horario de verano. <br/><br/>Los siguientes son las expresiones de XPath para este elemento: <br/> <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/TimeZone` <br/> <br/> `/GetUserAvailabilityRequest/TimeZone` <br/> |
   
## <a name="remarks"></a>Notas

El elemento **StandardTime** representa un tiempo de desfase que está representado por el elemento [Bias (UTC)](bias-utc.md) . Cuando el elemento de [inclinación](bias.md) secundario es igual a 0, el tiempo estándar es igual que el desplazamiento de diferencia de la hora UTC que está representada por el elemento [Bias (UTC)](bias-utc.md) . 
  
## <a name="example"></a>Ejemplo

En el ejemplo siguiente se muestra un área donde se observa el horario de verano. Se observa la transición desde el horario de verano a la hora estándar a las 2 A.M. en el quinto domingo del décimo mes.
  
```xml
<TimeZone xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
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

