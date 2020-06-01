---
title: Sesgo
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Bias
api_type:
- schema
ms.assetid: ae10aa44-e6d3-483d-a3e6-bb9c45966810
description: El elemento bias representa el desplazamiento del desplazamiento de la hora universal coordinada (UTC) identificado por el elemento Bias (UTC) para el horario estándar y el horario de verano. Este valor está en minutos.
ms.openlocfilehash: 6c9dce88f3eece9c793fb018114f07a85c7cb89b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460242"
---
# <a name="bias"></a>Sesgo

El elemento **Bias** representa el desplazamiento del desplazamiento de la hora universal coordinada (UTC) identificado por el elemento [Bias (UTC)](bias-utc.md) para el horario estándar y el horario de verano. Este valor está en minutos. 
  
```xml
<Bias>...</Bias>
```

**int**

## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Standardtime Element](standardtime.md) <br/> | Representa un desplazamiento del tiempo relativo a la hora UTC representado por el elemento [Bias (UTC)](bias-utc.md) . Este elemento también contiene información sobre la transición a la hora estándar del horario de verano en regiones en las que se observa el horario de verano.<br/><br/>Las siguientes son las expresiones XPath para el elemento [standardtime Element](standardtime.md) :<br/><br/>   `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/TimeZone/StandardTime` <br/><br/> `/GetUserAvailabilityRequest/TimeZone/StandardTime` <br/> |
|[DaylightTime](daylighttime.md) <br/> | Representa un desplazamiento del tiempo relativo a la hora UTC representado por el elemento [Bias (UTC)](bias-utc.md) en las regiones en las que se observa el horario de verano. Este elemento también contiene información sobre cuándo se produce la transición al horario de verano desde la hora estándar.  <br/><br/>Las siguientes son las expresiones XPath para el elemento [DaylightTime](daylighttime.md) :<br/><br/> `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/TimeZone/DaylightTime` <br/><br/> `/GetUserAvailabilityRequest/TimeZone/DaylightTime` <br/> |
   
## <a name="text-value"></a>Valor de texto

Se requiere un valor de texto. El valor de texto representa un número entero.
  
## <a name="remarks"></a>Comentarios

El desplazamiento que se usa para determinar la hora local solo puede ser proporcionado por uno de los elementos **Bias** . La suma de los valores del elemento bias proporcionado por el elemento [DaylightTime](daylighttime.md) o el elemento [standardtime Element](standardtime.md) más el elemento [Bias (UTC)](bias-utc.md) identifica la hora local. 
  
## <a name="example"></a>Ejemplo

En el ejemplo siguiente se muestra parte de una solicitud XML que identifica a un usuario que observa el horario de verano mediante el ajuste del desplazamiento con respecto a la hora UTC de-60 minutos. Esto hace que la diferencia sea de 420 minutos respecto a la hora UTC.
  
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
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también

- [Operación GetUserAvailability](getuseravailability-operation.md)
- [Obtener disponibilidad del usuario](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

