---
title: NetShowUrl
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- NetShowUrl
api_type:
- schema
ms.assetid: a5d48fc1-b141-422c-bcb0-05d0f9ba90dd
description: El elemento NetShowUrl especifica la dirección URL de una reunión en línea de Microsoft NetShow.
ms.openlocfilehash: 2440e6c1501331d715d0e5ceb31b3b928122f927
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836519"
---
# <a name="netshowurl"></a>NetShowUrl

El elemento **NetShowUrl** especifica la dirección URL de una reunión en línea de Microsoft NetShow. 
  
```xml
<NetShowUrl/>
```

 **string**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[MeetingRequest](meetingrequest.md) <br/> |Representa una reunión en el almacén de Exchange.  <br/> |
|[CalendarItem](calendaritem.md) <br/> |Representa un elemento de calendario de Exchange.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Si se usa este elemento, es necesario un valor de texto que representa una dirección URL.
  
## <a name="remarks"></a>Comentarios

Esta propiedad NetShowUrl es de lectura escritura para el elemento de calendario del organizador. Es de sólo lectura para las convocatorias de reunión y de los asistentes.
  
El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Vea también



- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

