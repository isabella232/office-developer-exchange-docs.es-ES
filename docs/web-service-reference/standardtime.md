---
title: StandardTime
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- StandardTime
api_type:
- schema
ms.assetid: 13084726-ab24-4009-be99-c4a4273c9e05
description: El elemento StandardTime representa un desplazamiento de la hora con respecto a la hora universal coordinada (UTC) representada por el elemento Bias (UTC). Este elemento también contiene información sobre la transición a la hora estándar desde el horario de verano en las regiones donde se observa el horario de verano.
ms.openlocfilehash: ceddc511bf1883078c88dee240fc308d02024220
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59544664"
---
# <a name="standardtime"></a>StandardTime

El **elemento StandardTime** representa un desplazamiento de la hora con respecto a la hora universal coordinada (UTC) representada por el elemento [Bias (UTC).](bias-utc.md) Este elemento también contiene información sobre la transición a la hora estándar desde el horario de verano en las regiones donde se observa el horario de verano. 
  
- [TimeZone (Availability)](timezone-availability.md)
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

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Sesgo](bias.md) <br/> |Representa el desplazamiento del desplazamiento UTC que identifica el elemento [Bias (UTC)](bias-utc.md) para el horario estándar y el horario de verano. Este valor está en minutos.  <br/> |
|[Time](time.md) <br/> |Representa la hora de transición del día a y desde la hora estándar y el horario de verano.  <br/> |
|[DayOrder](dayorder.md) <br/> |Representa la _n_th del día que se especifica en el elemento [DayOfWeek (TimeZone)](dayofweek-timezone.md) que representa la fecha de transición desde y hasta la hora estándar y el horario de verano.  <br/> |
|[Month](month.md) <br/> |Representa el mes de transición del año a y desde la hora estándar y el horario de verano.  <br/> |
|[DayOfWeek (TimeZone)](dayofweek-timezone.md) <br/> |Representa el día de la semana en que se produce la transición a y desde la hora estándar y el horario de verano.  <br/> |
|[Year](year.md) <br/> |Define una zona horaria que cambia según el año. Este elemento es opcional. Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[TimeZone (Availability)](timezone-availability.md) <br/> | Contiene elementos que identifican la información de zona horaria. Este elemento también contiene información sobre la transición entre la hora estándar y el horario de verano. <br/><br/>Las siguientes son las expresiones XPath de este elemento: <br/> <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/TimeZone` <br/> <br/> `/GetUserAvailabilityRequest/TimeZone` <br/> |
   
## <a name="remarks"></a>Comentarios

El **elemento StandardTime** representa un tiempo de desplazamiento representado por el [elemento Bias (UTC).](bias-utc.md) Cuando el elemento [bias](bias.md) secundario es igual a 0, el tiempo estándar es igual al desplazamiento de sesgo de UTC que está representado por el elemento [Bias (UTC).](bias-utc.md) 
  
## <a name="example"></a>Ejemplo

En el ejemplo siguiente se muestra una región donde se observa el horario de verano. La transición del horario de verano al horario estándar se observa a las 2 a. m. el quinto domingo del décimo mes.
  
```xml
<TimeZone xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
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
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Consulte también

- [Operación GetUserAvailability](getuseravailability-operation.md)
- [Obtener disponibilidad del usuario](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

