---
title: DayOrder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- DayOrder
api_type:
- schema
ms.assetid: 3022f839-12a2-42a9-820e-3ea585ce8657
description: El elemento DayOrder representa la enésima aparición del día especificado en el elemento DayOfWeek (TimeZone) que representa la fecha de transición desde y hasta la hora estándar y el horario de verano.
ms.openlocfilehash: bc216984a92fef58ac6f46dc4646a0deca837563
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59543446"
---
# <a name="dayorder"></a>DayOrder

El **elemento DayOrder** representa la _n_th del día especificado en el [elemento DayOfWeek (TimeZone)](dayofweek-timezone.md) que representa la fecha de transición desde y hacia la hora estándar y el horario de verano. 
  
```xml
<DayOrder>...</DayOrder>
```

**short**

## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[StandardTime](standardtime.md) <br/> | Representa un desplazamiento respecto a la hora universal coordinada (UTC) representada por el [elemento Bias (UTC).](bias-utc.md)<br/><br/>Este elemento también contiene información sobre la transición a la hora estándar desde el horario de verano en las regiones donde se observa el horario de verano.<br/><br/>Las siguientes son las expresiones XPath del [elemento StandardTime:](standardtime.md)<br/><br/>`/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/TimeZone/StandardTime`<br/><br/>`/GetUserAvailabilityRequest/TimeZone/StandardTime` <br/> |
|[DaylightTime](daylighttime.md) <br/> | Representa un desplazamiento respecto a la hora UTC representada por el elemento [Bias (UTC)](bias-utc.md) en las regiones donde se observa el horario de verano.<br/><br/>Este elemento también contiene información sobre cuándo se produce la transición al horario de verano desde el horario estándar.<br/><br/>Las siguientes son las expresiones XPath del [elemento DaylightTime:](daylighttime.md)<br/><br/>`/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/TimeZone/DaylightTime`<br/><br/>`/GetUserAvailabilityRequest/TimeZone/DaylightTime` <br/> |
   
## <a name="text-value"></a>Valor de texto

Se requiere un valor de texto. El valor del **elemento DayOrder** puede ser del 1 al 5. El valor máximo de este elemento puede ser 4 o 5, según el mes y el año. 
  
## <a name="remarks"></a>Comentarios

Un [elemento StandardTime](standardtime.md) que contiene un elemento **DayOrder** que tiene un valor de 5, un elemento [Month](month.md) que tiene un valor de 10 y un [elemento DayOfWeek (TimeZone)](dayofweek-timezone.md) que tiene un valor de Sunday significa que la transición de la hora estándar al horario de verano se produce el quinto domingo del décimo mes. 
  
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

