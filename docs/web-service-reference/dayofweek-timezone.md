---
title: DayOfWeek (TimeZone)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- DayOfWeek
api_type:
- schema
ms.assetid: 416e8892-ebb1-4fac-82cf-e27549a6c175
description: El elemento DayOfWeek representa el día de la semana en que se produce la transición de zona horaria.
ms.openlocfilehash: 5b51a3692a1836d2d2448df88b0ec07ccf1d79a5
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59519901"
---
# <a name="dayofweek-timezone"></a>DayOfWeek (TimeZone)

El **elemento DayOfWeek** representa el día de la semana en que se produce la transición de zona horaria. 
  
```xml
<DayOfWeek>...</DayOfWeek>
```

**DayOfWeekType**

## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[StandardTime](standardtime.md) <br/> | Representa un desplazamiento respecto a la hora universal coordinada (UTC) representada por el [elemento Bias (UTC).](bias-utc.md)<br/><br/>Este elemento también contiene información sobre la transición a la hora estándar desde el horario de verano en las regiones donde se observa el horario de verano.<br/><br/>Las siguientes son las expresiones XPath de este elemento:<br/><br/>`/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/TimeZone/StandardTime`<br/><br/>`/GetUserAvailabilityRequest/TimeZone/StandardTime` <br/> |
|[DaylightTime](daylighttime.md) <br/> | Representa un desplazamiento respecto a la hora UTC representada por el elemento [Bias (UTC)](bias-utc.md) en las regiones donde se observa el horario de verano.<br/><br/>Este elemento también contiene información sobre cuándo se produce la transición al horario de verano desde el horario estándar.<br/><br/>Las siguientes son las expresiones XPath de este elemento:<br/><br/>`/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/TimeZone/DaylightTime`<br/><br/>`/GetUserAvailabilityRequest/TimeZone/DaylightTime` <br/> |
|[RecurringDayTransition](recurringdaytransition.md) <br/> |Representa una transición de zona horaria que se produce el mismo día de cada año.  <br/> |
   
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

Un [elemento StandardTime](standardtime.md) que contiene un elemento [DayOrder](dayorder.md) que tiene un valor de 5, un elemento [Month](month.md) que tiene un valor de 10 y un elemento **DayOfWeek** que tiene un valor de Sunday significa que la transición de la hora estándar al horario de verano se produce el quinto domingo del décimo mes. 
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también

- [Operación GetUserAvailability](getuseravailability-operation.md)
- [Obtener disponibilidad del usuario](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

