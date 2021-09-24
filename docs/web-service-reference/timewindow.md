---
title: TimeWindow
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- TimeWindow
api_type:
- schema
ms.assetid: 49c79266-353a-4036-a8e2-8a4660d0d8ea
description: El elemento TimeWindow identifica el intervalo de tiempo que se consulta para la información de disponibilidad del usuario.
ms.openlocfilehash: 93a486a5bc2306cfa61b74de82d795a711dbbceb
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59531347"
---
# <a name="timewindow"></a>TimeWindow

El **elemento TimeWindow** identifica el intervalo de tiempo que se consulta para la información de disponibilidad del usuario. 
  
[GetUserAvailabilityRequest](getuseravailabilityrequest.md)
  
[FreeBusyViewOptions](freebusyviewoptions.md)
  
[TimeWindow](timewindow.md)
  
```xml
<TimeWindow>
   <StartTime>dateTime</StartTime>
   <EndTime>dateTime</EndTime>
</TimeWindow>
```

 **Duration**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[StartTime](starttime.md) <br/> |Representa el inicio de un intervalo de tiempo que se consulta para la información de disponibilidad del usuario.  <br/> |
|[EndTime](endtime.md) <br/> |Representa el final de un intervalo de tiempo que se consulta para la información de disponibilidad del usuario.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[FreeBusyViewOptions](freebusyviewoptions.md) <br/> |Especifica el tipo de información de disponibilidad devuelta en la respuesta.  <br/> A continuación se muestra XPath a este elemento:  <br/>  `/GetUserAvailabilityRequest/FreeBusyViewOptions` <br/> |
   
## <a name="remarks"></a>Comentarios

El valor máximo para este período de tiempo es de 42 días. Este valor máximo se puede modificar. Cualquier solicitud de información de disponibilidad del usuario que supere el valor máximo devolverá un error. Si alguna cita se encuentra parcialmente en el intervalo de tiempo definido por los elementos [StartTime](starttime.md) y [EndTime,](endtime.md) esa cita se incluye en su totalidad. 
  
> [!NOTE]
> El esquema que describe este elemento se encuentra en el directorio /EWS/ del equipo que ejecuta Microsoft® Exchange Server 2007 que tiene instalado el rol de servidor Acceso de cliente. 
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también



[Operación GetUserAvailability](getuseravailability-operation.md)


[Obtener disponibilidad del usuario](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

