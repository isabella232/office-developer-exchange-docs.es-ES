---
title: Offset
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Offset
api_type:
- schema
ms.assetid: dcbb9d85-d90c-4363-b4c9-d081ad03f407
description: El elemento Offset describe el desplazamiento del BaseOffset. Junto con el elemento BaseOffset, el elemento Offset identifica si la hora es estándar o el horario de verano.
ms.openlocfilehash: af9a2f7a94ae0cd736a4fe6f11b8a5a77673bbe3
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59515393"
---
# <a name="offset"></a>Offset

El **elemento Offset** describe el desplazamiento de [BaseOffset](baseoffset.md). Junto con el **elemento BaseOffset,** el **elemento Offset** identifica si la hora es estándar o el horario de verano. 
  
```xml
<Offset/>
```

 **duration**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Daylight](daylight.md) <br/> |Representa la fecha y hora en que la hora cambia del horario de verano a la hora estándar.  <br/> |
|[Estándar](standard.md) <br/> |Representa la fecha y hora en que la hora cambia del horario de verano a la hora estándar.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto representa el desplazamiento de la hora universal coordinada (UTC).
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor Acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también



- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

