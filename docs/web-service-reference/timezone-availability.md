---
title: TimeZone (Availability)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- TimeZone
api_type:
- schema
ms.assetid: d662ffae-1f93-4c08-85a4-c69de2f7c681
description: El elemento TimeZone contiene elementos que identifican la información de zona horaria. Este elemento también contiene información sobre la transición entre la hora estándar y el horario de verano.
ms.openlocfilehash: 7ca6f0f2d9950770055d19c04adab9b76b95c295
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59538845"
---
# <a name="timezone-availability"></a>TimeZone (Availability)

El **elemento TimeZone** contiene elementos que identifican la información de zona horaria. Este elemento también contiene información sobre la transición entre la hora estándar y el horario de verano. 
  
```xml
<TimeZone>
   <Bias/>
   <StandardTime/>
   <DaylightTime/>
</TimeZone>
```

 **SerializableTimeZone**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Bias (UTC)](bias-utc.md) <br/> |Representa el desplazamiento general de la hora universal coordinada (UTC). Este valor está en minutos.  <br/> |
|[StandardTime](standardtime.md) <br/> |Representa un desplazamiento respecto a la hora UTC representada por el [elemento Bias (UTC).](bias-utc.md) Este elemento también contiene información sobre la transición a la hora estándar desde el horario de verano en las regiones donde se observa el horario de verano.  <br/> |
|[DaylightTime](daylighttime.md) <br/> |Representa un desplazamiento respecto a la hora UTC representada por el elemento [Bias (UTC)](bias-utc.md) en las regiones donde se observa el horario de verano. Este elemento también contiene información sobre cuándo se produce la transición al horario de verano desde el horario estándar.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[GetUserAvailabilityRequest](getuseravailabilityrequest.md) <br/> |Contiene los argumentos usados para obtener información de disponibilidad del usuario. Se trata de un elemento raíz.  <br/> El **elemento TimeZone** del mensaje GetUserAvailabilityRequest representa la zona horaria en la que se especifican los valores DateTime de la solicitud. Los valores DateTime devueltos por el servicio de disponibilidad también se encuentran en esta zona horaria.  <br/> A continuación se muestra XPath a este elemento:  <br/>  `/GetUserAvailabilityRequest` <br/> |
|[WorkingHours](workinghours-ex15websvcsotherref.md) <br/> |Representa la configuración de zona horaria y el horario laboral del usuario del buzón solicitado.  <br/> El **elemento TimeZone** del mensaje GetUserAvailabilityResponse representa la configuración de zona horaria del usuario de buzón solicitado.  <br/> A continuación se muestra XPath a este elemento:  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours` <br/> |
   
## <a name="remarks"></a>Comentarios

Este elemento es necesario en el [elemento GetUserAvailabilityRequest.](getuseravailabilityrequest.md) Este elemento se produce como máximo una o al menos cero veces cuando el elemento primario es el [elemento WorkingHours.](workinghours-ex15websvcsotherref.md) 
  
## <a name="example"></a>Ejemplo

En el ejemplo siguiente se muestra parte de una solicitud XML que identifica un desplazamiento de UTC de 8 horas en la aplicación cliente.
  
```XML
<TimeZone xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
  <Bias>480</Bias>
  <StandardTime>
    <Bias>0</Bias>
    <Time>02:00:00</Time>
    <DayOrder>1</DayOrder>
    <Month>11</Month>
    <DayOfWeek>Sunday</DayOfWeek>
  </StandardTime>
  <DaylightTime>
    <Bias>-60</Bias>
    <Time>02:00:00</Time>
    <DayOrder>2</DayOrder>
    <Month>3</Month>
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
   
## <a name="see-also"></a>Ver también



[Operación GetUserAvailability](getuseravailability-operation.md)
  
[Sesgo](bias.md)


[Obtener disponibilidad del usuario](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

