---
title: TimeZone (disponibilidad)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- TimeZone
api_type:
- schema
ms.assetid: d662ffae-1f93-4c08-85a4-c69de2f7c681
description: El elemento TimeZone contiene elementos que identifican la información de zona horaria. Este elemento también contiene información sobre la transición entre la hora estándar y el horario de verano.
ms.openlocfilehash: dc2466e8039819edc82294ff05f1746ada64cb43
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19840693"
---
# <a name="timezone-availability"></a>TimeZone (disponibilidad)

El elemento **TimeZone** contiene elementos que identifican la información de zona horaria. Este elemento también contiene información sobre la transición entre la hora estándar y el horario de verano. 
  
```xml
<TimeZone>
   <Bias/>
   <StandardTime/>
   <DaylightTime/>
</TimeZone>
```

 **SerializableTimeZone**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[Bias (UTC)](bias-utc.md) <br/> |Representa el desplazamiento general de la hora Universal coordinada (UTC). Este valor está en minutos.  <br/> |
|[StandardTime](standardtime.md) <br/> |Representa un desplazamiento de la hora con respecto a UTC representada por el elemento [Bias (UTC)](bias-utc.md) . Este elemento también contiene información sobre la transición a la hora estándar de horario de verano en regiones donde se observa el horario de verano.  <br/> |
|[DaylightTime](daylighttime.md) <br/> |Representa un desplazamiento de la hora con respecto a UTC representada por el elemento [Bias (UTC)](bias-utc.md) en las regiones donde se observa el horario de verano. Este elemento también contiene información acerca de cuándo se produce la transición al horario de verano de tiempo estándar.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[GetUserAvailabilityRequest](getuseravailabilityrequest.md) <br/> |Contiene los argumentos utilizados para obtener información de disponibilidad del usuario. Esto es un elemento raíz.  <br/> El elemento de la **zona horaria** en el mensaje GetUserAvailabilityRequest representa la zona horaria en la que se especifican los valores de fecha y hora de la solicitud. Los valores de fecha y hora devueltos por el servicio de disponibilidad también están en esta zona horaria.  <br/> La siguiente es la expresión de XPath para este elemento:  <br/>  `/GetUserAvailabilityRequest` <br/> |
|[WorkingHours](workinghours-ex15websvcsotherref.md) <br/> |Representa la configuración de zona horaria y horario laboral para el usuario del buzón solicitado.  <br/> El elemento de la **zona horaria** en el mensaje GetUserAvailabilityResponse representa la configuración de zona horaria del usuario de buzón solicitado.  <br/> La siguiente es la expresión de XPath para este elemento:  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours` <br/> |
   
## <a name="remarks"></a>Comentarios

Este elemento es necesario en el elemento [GetUserAvailabilityRequest](getuseravailabilityrequest.md) . Este elemento se produce como máximo una vez o al menos cero veces cuando el elemento primario es el elemento [WorkingHours](workinghours-ex15websvcsotherref.md) . 
  
## <a name="example"></a>Ejemplo

En el ejemplo siguiente se muestra parte de una solicitud XML que identifica un desplazamiento de la hora UTC de 8 horas en la aplicación cliente.
  
```XML
<TimeZone xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
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
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Vea también



[Operación GetUserAvailability](getuseravailability-operation.md)
  
[Bias](bias.md)


[Obtención de disponibilidad del usuario](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

