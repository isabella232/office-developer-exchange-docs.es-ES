---
title: Offset
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
description: El elemento offset describe el desplazamiento desde BaseOffset. Junto con el elemento BaseOffset, el elemento offset identifica si la hora es estándar o de horario de verano.
ms.openlocfilehash: 74ad87026c2cb89f3b0c35218c91f81380029963
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459759"
---
# <a name="offset"></a>Offset

El elemento **offset** describe el desplazamiento desde [BaseOffset](baseoffset.md). Junto con el elemento **BaseOffset** , el elemento **offset** identifica si la hora es estándar o de horario de verano. 
  
```xml
<Offset/>
```

 **duration**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Horario](daylight.md) <br/> |Representa la fecha y la hora en que cambia el horario de verano a la hora estándar.  <br/> |
|[Estándar](standard.md) <br/> |Representa la fecha y la hora en que cambia el horario de verano a la hora estándar.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto representa el desplazamiento de hora universal coordinada (UTC).
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también



- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)

