---
title: TimeWindow
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- TimeWindow
api_type:
- schema
ms.assetid: 49c79266-353a-4036-a8e2-8a4660d0d8ea
description: El elemento TimeWindow identifica el intervalo de tiempo consultado para la información de disponibilidad del usuario.
ms.openlocfilehash: 5c66614520f9d616687d67ad609b3d55d9cf6571
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458932"
---
# <a name="timewindow"></a>TimeWindow

El elemento **TimeWindow** identifica el intervalo de tiempo consultado para la información de disponibilidad del usuario. 
  
[GetUserAvailabilityRequest](getuseravailabilityrequest.md)
  
[FreeBusyViewOptions](freebusyviewoptions.md)
  
[TimeWindow](timewindow.md)
  
```xml
<TimeWindow>
   <StartTime>dateTime</StartTime>
   <EndTime>dateTime</EndTime>
</TimeWindow>
```

 **Duración**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[StartTime](starttime.md) <br/> |Representa el inicio de un intervalo de tiempo consultado para obtener la información de disponibilidad del usuario.  <br/> |
|[EndTime](endtime.md) <br/> |Representa el final de un intervalo de tiempo consultado para obtener la información de disponibilidad del usuario.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[FreeBusyViewOptions](freebusyviewoptions.md) <br/> |Especifica el tipo de información de disponibilidad devuelta en la respuesta.  <br/> A continuación se encuentra la expresión XPath de este elemento:  <br/>  `/GetUserAvailabilityRequest/FreeBusyViewOptions` <br/> |
   
## <a name="remarks"></a>Comentarios

El valor máximo para este período de tiempo es de 42 días. Este valor máximo se puede modificar. Cualquier solicitud de información de disponibilidad del usuario que no supere el valor máximo devolverá un error. Si alguna de las citas se encuentra parcialmente en el intervalo de tiempo definido por los elementos [startTime](starttime.md) y [EndTime](endtime.md) , la cita se incluirá en su totalidad. 
  
> [!NOTE]
> El esquema que describe este elemento se encuentra en el directorio/EWS/del equipo que ejecuta Microsoft® Exchange Server 2007 que tenga instalado el rol de servidor acceso de clientes. 
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también



[Operación GetUserAvailability](getuseravailability-operation.md)


[Obtener disponibilidad del usuario](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

