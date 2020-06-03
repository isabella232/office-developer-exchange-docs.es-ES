---
title: MeetingWorkspaceUrl
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MeetingWorkspaceUrl
api_type:
- schema
ms.assetid: 0ca942fe-8f57-4065-93ad-65790f9a04c3
description: El elemento MeetingWorkspaceUrl contiene la dirección URL del área de reuniones que se incluye en el elemento de calendario. Un área de reuniones es un sitio web compartido para planear la reunión y realizar un seguimiento de los resultados.
ms.openlocfilehash: cd4396e590ab1471278bd44b9a4e0009fe326eaf
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466286"
---
# <a name="meetingworkspaceurl"></a>MeetingWorkspaceUrl

El elemento **MeetingWorkspaceUrl** contiene la dirección URL del área de reuniones que se incluye en el elemento de calendario. Un área de reuniones es un sitio web compartido para planear la reunión y realizar un seguimiento de los resultados. 
  
```xml
<MeetingWorkspaceUrl/>
```

 **string**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[MeetingRequest](meetingrequest.md) <br/> |Representa una reunión en el almacén de Exchange.  <br/> |
|[CalendarItem](calendaritem.md) <br/> |Representa un elemento de calendario de Exchange.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Si se usa este elemento, es necesario un valor de texto que represente una dirección URL.
  
## <a name="remarks"></a>Comentarios

La propiedad MeetingWorkspaceUrl es de lectura y escritura para el elemento de calendario del organizador. Es de solo lectura para las convocatorias de reunión y para los elementos de calendario de los asistentes.
  
El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también



- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)

