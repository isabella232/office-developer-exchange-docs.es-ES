---
title: FreeBusyView
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FreeBusyView
api_type:
- schema
ms.assetid: cb18434f-5f41-4e05-a5ce-d921b2721a8c
description: El elemento FreeBusyView contiene la información de disponibilidad para un usuario específico.
ms.openlocfilehash: d0d603f18642a94e841a1a6bb8e8849aa6b5b273
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764718"
---
# <a name="freebusyview"></a>FreeBusyView

El elemento **FreeBusyView** contiene la información de disponibilidad para un usuario específico. 
  
[GetUserAvailabilityResponse](getuseravailabilityresponse.md)
  
[FreeBusyResponseArray](freebusyresponsearray.md)
  
[FreeBusyResponse](freebusyresponse.md)
  
[FreeBusyView](freebusyview.md)
  
```xml
<FreeBusyView>
   <FreeBusyViewType>...</FreeBusyViewType>
   <MergedFreeBusy>...</MergedFreeBusy>
   <CalendarEventArray>...</CalendarEventArray>
   <WorkingHours>...</WorkingHours>
</FreeBusyView>
```

 **FreeBusyView**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[FreeBusyViewType](freebusyviewtype.md) <br/> |Representa el tipo de información de disponibilidad solicitada devuelto en la respuesta.  <br/> |
|[MergedFreeBusy](mergedfreebusy.md) <br/> |Contiene la secuencia de libre/ocupado combinada de datos.  <br/> |
|[CalendarEventArray](calendareventarray.md) <br/> |Contiene un conjunto de repeticiones de elemento de calendario únicos que representan la disponibilidad del usuario solicitado.  <br/> |
|[WorkingHours](workinghours-ex15websvcsotherref.md) <br/> |Representa la configuración de zona horaria y horario laboral para el usuario del buzón solicitado.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[FreeBusyResponse](freebusyresponse.md) <br/> |Contiene la información de disponibilidad para un usuario de buzón único.  <br/> La siguiente es la expresión de XPath para este elemento:  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse` <br/> |
   
## <a name="remarks"></a>Notas

Todos los elementos secundarios se enumeran en la secuencia en la que se producen. El nivel de detalle proporcionado por este elemento depende de los permisos concedidos para el solicitante.
  
El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Ver también



[Operación GetUserAvailability](getuseravailability-operation.md)
  
[GetUserAvailabilityResponse](getuseravailabilityresponse.md)


[Obtención de disponibilidad del usuario](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

