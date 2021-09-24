---
title: MeetingWorkspaceUrl
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MeetingWorkspaceUrl
api_type:
- schema
ms.assetid: 0ca942fe-8f57-4065-93ad-65790f9a04c3
description: El elemento MeetingWorkspaceUrl contiene la dirección URL del área de trabajo de reunión que se incluye en el elemento de calendario. Un área de trabajo de reunión es un sitio web compartido para planear la reunión y realizar un seguimiento de los resultados.
ms.openlocfilehash: c3d051d3529e9de9288c5ecaec2d601b317e2b0b
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59540800"
---
# <a name="meetingworkspaceurl"></a>MeetingWorkspaceUrl

El **elemento MeetingWorkspaceUrl** contiene la dirección URL del área de trabajo de reunión que se incluye en el elemento de calendario. Un área de trabajo de reunión es un sitio web compartido para planear la reunión y realizar un seguimiento de los resultados. 
  
```xml
<MeetingWorkspaceUrl/>
```

 **string**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[MeetingRequest](meetingrequest.md) <br/> |Representa una reunión en el Exchange almacén.  <br/> |
|[CalendarItem](calendaritem.md) <br/> |Representa un Exchange de calendario.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Si se usa este elemento, se requiere un valor de texto que represente una dirección URL.
  
## <a name="remarks"></a>Comentarios

La propiedad MeetingWorkspaceUrl se puede leer para el elemento de calendario del organizador. Es de solo lectura para las solicitudes de reunión y para los elementos del calendario de los asistentes.
  
El esquema que describe este elemento se encuentra en el directorio virtual EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor Acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre del esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también



- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

