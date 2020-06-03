---
title: DayOrder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DayOrder
api_type:
- schema
ms.assetid: 3022f839-12a2-42a9-820e-3ea585ce8657
description: El elemento DayOrder representa el número n de ocurrencias del día especificado en el elemento DayOfWeek (TimeZone) que representa la fecha de transición desde y hasta el horario estándar y el horario de verano.
ms.openlocfilehash: 53a8cb979bdb7aefead5623b4680f4c1a4ef5509
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526966"
---
# <a name="dayorder"></a>DayOrder

El elemento **DayOrder** representa la _n_th aparición del día especificado en el elemento [DayOfWeek (TimeZone)](dayofweek-timezone.md) que representa la fecha de transición desde y hasta el horario estándar y el horario de verano. 
  
```xml
<DayOrder>...</DayOrder>
```

**Short**

## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Standardtime Element](standardtime.md) <br/> | Representa un desplazamiento del tiempo con respecto a la hora universal coordinada (UTC) representada por el elemento [Bias (UTC)](bias-utc.md) .<br/><br/>Este elemento también contiene información sobre la transición a la hora estándar del horario de verano en regiones en las que se observa el horario de verano.<br/><br/>Las siguientes son las expresiones XPath para el elemento [standardtime Element](standardtime.md) :<br/><br/>`/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/TimeZone/StandardTime`<br/><br/>`/GetUserAvailabilityRequest/TimeZone/StandardTime` <br/> |
|[DaylightTime](daylighttime.md) <br/> | Representa un desplazamiento del tiempo relativo a la hora UTC representado por el elemento [Bias (UTC)](bias-utc.md) en las regiones en las que se observa el horario de verano.<br/><br/>Este elemento también contiene información sobre cuándo se produce la transición al horario de verano desde la hora estándar.<br/><br/>Las siguientes son las expresiones XPath para el elemento [DaylightTime](daylighttime.md) :<br/><br/>`/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/TimeZone/DaylightTime`<br/><br/>`/GetUserAvailabilityRequest/TimeZone/DaylightTime` <br/> |
   
## <a name="text-value"></a>Valor de texto

Se requiere un valor de texto. El valor del elemento **DayOrder** puede estar comprendido entre 1 y 5. El valor máximo para este elemento puede ser 4 o 5, según el mes y el año. 
  
## <a name="remarks"></a>Comentarios

Un elemento [standardtime Element](standardtime.md) que contiene un elemento **DayOrder** que tiene un valor de 5, un elemento [Month](month.md) que tiene un valor de 10, y un elemento [DayOfWeek (TimeZone)](dayofweek-timezone.md) que tiene un valor de domingo, significa que la transición de la hora estándar al horario de verano se produce el quinto domingo del décimo mes. 
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también

- [Operación GetUserAvailability](getuseravailability-operation.md)
- [Obtener disponibilidad del usuario](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

