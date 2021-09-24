---
title: Mes
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Month
api_type:
- schema
ms.assetid: b12ac64f-b230-4573-be05-c86a428c4965
description: El elemento Month representa el mes de transición del año a y desde la hora estándar y el horario de verano.
ms.openlocfilehash: aca81faf2767e17dab956db9a208245fbd0b7d83
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59520433"
---
# <a name="month"></a>Mes

El **elemento Month** representa el mes de transición del año a y desde la hora estándar y el horario de verano. 
  
```xml
<Month>...</Month>
```

 **Short**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[StandardTime](standardtime.md) <br/> | Representa un desplazamiento respecto a la hora universal coordinada (UTC) representada por el [elemento Bias (UTC).](bias-utc.md) Este elemento también contiene información sobre la transición a la hora estándar desde el horario de verano en las regiones donde se observa el horario de verano. <br/> <br/>  Las siguientes son las expresiones XPath del [elemento StandardTime:](standardtime.md) <br/> <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/TimeZone/StandardTime` <br/><br/>  `/GetUserAvailabilityRequest/TimeZone/StandardTime` <br/> |
|[DaylightTime](daylighttime.md) <br/> | Representa un desplazamiento respecto a la hora UTC representada por el elemento [Bias (UTC)](bias-utc.md) en las regiones donde se observa el horario de verano. Este elemento también contiene información sobre cuándo se produce la transición al horario de verano desde el horario estándar.  <br/><br/>  Las siguientes son las expresiones XPath del [elemento DaylightTime:](daylighttime.md)  <br/> <br/> `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/TimeZone/DaylightTime` <br/><br/>  `/GetUserAvailabilityRequest/TimeZone/DaylightTime` <br/> |
   
## <a name="text-value"></a>Valor de texto

Se requiere un valor de texto. El valor representa la clasificación ordinal del mes por repetición y debe ser un número entre 1 y 12. Se trata de un tipo de datos enteros corto.
  
## <a name="remarks"></a>Comentarios

Un [elemento StandardTime](standardtime.md) que contiene un elemento [DayOrder](dayorder.md) que tiene un valor de 5, un elemento **Month** que tiene un valor de 10 y un [elemento DayOfWeek (TimeZone)](dayofweek-timezone.md) que tiene un valor de Sunday significa que la transición de la hora estándar al horario de verano se produce el quinto domingo del décimo mes. 
  
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

