---
title: Desplazamiento
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Offset
api_type:
- schema
ms.assetid: dcbb9d85-d90c-4363-b4c9-d081ad03f407
description: El elemento de desplazamiento describe el desplazamiento desde el BaseOffset. Junto con el elemento BaseOffset, el elemento de desplazamiento identifica si el tiempo es estándar o el horario de verano.
ms.openlocfilehash: d85fef0d67633733f6aa1943d70413ea70a528d6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836642"
---
# <a name="offset"></a>Desplazamiento

El elemento de **desplazamiento** describe el desplazamiento desde el [BaseOffset](baseoffset.md). Junto con el elemento **BaseOffset** , el elemento de **desplazamiento** identifica si el tiempo es estándar o el horario de verano. 
  
```xml
<Offset/>
```

 **duration**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[Horario de verano](daylight.md) <br/> |Representa la fecha y hora cuando se cambia la hora del horario de verano a la hora estándar.  <br/> |
|[Standard](standard.md) <br/> |Representa la fecha y hora cuando se cambia la hora del horario de verano a la hora estándar.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto representa el desplazamiento de hora Universal coordinada (UTC).
  
## <a name="remarks"></a>Notas

El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Ver también



- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

