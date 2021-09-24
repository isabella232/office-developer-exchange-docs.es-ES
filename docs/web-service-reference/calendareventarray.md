---
title: CalendarEventArray
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- CalendarEventArray
api_type:
- schema
ms.assetid: a00f7f56-d7f1-429d-ae02-97043718c864
description: El elemento CalendarEventArray contiene un conjunto de repeticiones de elementos de calendario únicos que representan la disponibilidad del usuario solicitado.
ms.openlocfilehash: 6faf9d85139ce99a6a60da5a05f171a229843b92
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59526837"
---
# <a name="calendareventarray"></a>CalendarEventArray

El **elemento CalendarEventArray** contiene un conjunto de repeticiones de elementos de calendario únicos que representan la disponibilidad del usuario solicitado. 
  
[GetUserAvailabilityResponse](getuseravailabilityresponse.md)
  
[FreeBusyResponseArray](freebusyresponsearray.md)
  
[FreeBusyResponse](freebusyresponse.md)
  
[FreeBusyView](freebusyview.md)
  
[CalendarEventArray](calendareventarray.md)
  
```xml
<CalendarEventArray>
   <CalendarEvent>...</CalendarEvent>
</CalendarEventArray>
```

 **ArrayOfCalendarEvent**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[CalendarEvent](calendarevent.md) <br/> |Representa una repetición de elemento de calendario única.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[FreeBusyView](freebusyview.md) <br/> |Contiene información de disponibilidad para un usuario específico.  <br/> A continuación se muestra la expresión XPath 2.0 para este elemento:  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView` <br/> |
   
## <a name="remarks"></a>Comentarios

El nivel de detalle proporcionado por este elemento depende de los permisos concedidos al solicitante. Este elemento se incluye cuando el [elemento FreeBusyViewType](freebusyviewtype.md) se establece en **FreeBusy**, **FreeBusyMerged,** **Detailed** o **DetailedMerged**. Este elemento no incluye ningún elemento secundario si no hay elementos de calendario presentes en la ventana de hora solicitada. 
  
El esquema que describe este elemento se encuentra en el directorio virtual EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor Acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también



[Operación GetUserAvailability](getuseravailability-operation.md)
  
[GetUserAvailabilityResponse](getuseravailabilityresponse.md)


[Obtener disponibilidad del usuario](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

