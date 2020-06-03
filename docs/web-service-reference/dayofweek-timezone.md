---
title: DayOfWeek (TimeZone)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DayOfWeek
api_type:
- schema
ms.assetid: 416e8892-ebb1-4fac-82cf-e27549a6c175
description: El elemento DayOfWeek representa el día de la semana en el que se produce la transición de zona horaria.
ms.openlocfilehash: 7bc05f417268ccfb20adae12e2694d8360023ab2
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457847"
---
# <a name="dayofweek-timezone"></a>DayOfWeek (TimeZone)

El elemento **DayOfWeek** representa el día de la semana en el que se produce la transición de zona horaria. 
  
```xml
<DayOfWeek>...</DayOfWeek>
```

**DayOfWeekType**

## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Standardtime Element](standardtime.md) <br/> | Representa un desplazamiento del tiempo con respecto a la hora universal coordinada (UTC) representada por el elemento [Bias (UTC)](bias-utc.md) .<br/><br/>Este elemento también contiene información sobre la transición a la hora estándar del horario de verano en regiones en las que se observa el horario de verano.<br/><br/>Las siguientes son las expresiones XPath de este elemento:<br/><br/>`/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/TimeZone/StandardTime`<br/><br/>`/GetUserAvailabilityRequest/TimeZone/StandardTime` <br/> |
|[DaylightTime](daylighttime.md) <br/> | Representa un desplazamiento del tiempo relativo a la hora UTC representado por el elemento [Bias (UTC)](bias-utc.md) en las regiones en las que se observa el horario de verano.<br/><br/>Este elemento también contiene información sobre cuándo se produce la transición al horario de verano desde la hora estándar.<br/><br/>Las siguientes son las expresiones XPath de este elemento:<br/><br/>`/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/TimeZone/DaylightTime`<br/><br/>`/GetUserAvailabilityRequest/TimeZone/DaylightTime` <br/> |
|[RecurringDayTransition](recurringdaytransition.md) <br/> |Representa una transición de zona horaria que se produce el mismo día cada año.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Se requiere un valor de texto. El valor de texto se representa mediante una enumeración que tiene los siguientes valores posibles:
  
- Domingo    
- lunes    
- martes    
- miércoles    
- jueves    
- viernes    
- Sábado    
- Day    
- Día de la semana   
- WeekendDay
    
## <a name="remarks"></a>Comentarios

Un elemento [standardtime Element](standardtime.md) que contiene un elemento [DayOrder](dayorder.md) que tiene un valor de 5, un elemento [Month](month.md) que tiene un valor de 10 y un elemento **DayOfWeek** que tiene un valor de domingo, significa que la transición de la hora estándar al horario de verano se produce el quinto domingo del décimo mes. 
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
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

