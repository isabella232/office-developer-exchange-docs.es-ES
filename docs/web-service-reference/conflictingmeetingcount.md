---
title: ConflictingMeetingCount
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ConflictingMeetingCount
api_type:
- schema
ms.assetid: 11f4d93a-b514-4a27-8d19-f4f0a35a185e
description: El elemento ConflictingMeetingCount representa el número de reuniones que entran en conflicto con el elemento de calendario.
ms.openlocfilehash: d53245e1b5d1f0182b28b15bf55ba9742bbb2a07
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463863"
---
# <a name="conflictingmeetingcount"></a>ConflictingMeetingCount

El elemento **ConflictingMeetingCount** representa el número de reuniones que entran en conflicto con el elemento de calendario. 
  
```xml
<ConflictingMeetingCount/>
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
|[MeetingRequest](meetingrequest.md) <br/> |Representa una reunión en el almacén de Exchange.  <br/> |
|[CalendarItem](calendaritem.md) <br/> |Representa un elemento de calendario de Exchange.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto representa un número entero. Esta propiedad es de sólo lectura.
  
## <a name="remarks"></a>Comentarios

Un elemento de calendario se considera conflictivo si se produce, al menos en parte, al mismo tiempo que otro elemento de calendario en la misma carpeta calendario. Si un elemento de calendario está en una carpeta que no es un calendario, se compara con los elementos del calendario de la carpeta calendario predeterminada. Las convocatorias de reunión se comparan con los elementos del calendario de la carpeta calendario predeterminada.
  
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

