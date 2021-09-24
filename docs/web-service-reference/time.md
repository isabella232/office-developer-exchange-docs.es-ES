---
title: Hora
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Time
api_type:
- schema
ms.assetid: c4b98be7-141c-4ba8-97ef-9ad1ed19f61f
description: El elemento Time representa la hora de transición del día a y desde la hora estándar y el horario de verano.
ms.openlocfilehash: d9cd83a7dcb0a296693e3daa1874b12294de5857
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59513272"
---
# <a name="time"></a>Hora

El **elemento Time** representa la hora de transición del día a y desde la hora estándar y el horario de verano. 
  
```xml
<Time>...</Time>
```

 **string**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[StandardTime](standardtime.md) <br/> | Representa un desplazamiento respecto a la hora universal coordinada (UTC) representada por el [elemento Bias (UTC).](bias-utc.md) Este elemento también contiene información sobre la transición a la hora estándar desde el horario de verano en las regiones donde se observa el horario de verano.  <br/><br/>  Las siguientes son las expresiones XPath del [elemento StandardTime:](standardtime.md) <br/> <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/TimeZone/StandardTime`<br/> <br/>  `/GetUserAvailabilityRequest/TimeZone/StandardTime` <br/> |
|[DaylightTime](daylighttime.md) <br/> | Representa un desplazamiento respecto a la hora UTC representada por el elemento [Bias (UTC)](bias-utc.md) en las regiones donde se observa el horario de verano. Este elemento también contiene información sobre cuándo se produce la transición al horario de verano desde el horario estándar.  <br/><br/>  Las siguientes son las expresiones XPath del [elemento DaylightTime:](daylighttime.md)  <br/><br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/TimeZone/DaylightTime` <br/><br/>  `/GetUserAvailabilityRequest/TimeZone/DaylightTime` <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto representa horas, minutos y segundos en el siguiente formato: hh:mm:ss.
  
## <a name="remarks"></a>Comentarios

Cuando el **elemento Time** se produce en el elemento [DaylightTime,](daylighttime.md) representa la hora del día en la que se produce la transición del horario de verano al horario estándar. Cuando el [elemento Time](time.md) se produce en el [elemento StandardTime,](standardtime.md) representa la hora del día en la que se produce la transición de la hora estándar al horario de verano. 
  
Este elemento tiene una ocurrencia mínima de cero y una repetición máxima de uno.
  
## <a name="example"></a>Ejemplo

La siguiente parte de una solicitud representa un tiempo de transición de 2 a. m. desde la hora estándar hasta el horario de verano.
  
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
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también

- [Operación GetUserAvailability](getuseravailability-operation.md)
- [Obtener disponibilidad del usuario](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

