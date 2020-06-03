---
title: ExceptionFieldURI
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ExceptionFieldURI
api_type:
- schema
ms.assetid: 7afda93a-0f8c-4c9e-8e09-f1b0bfc928bf
description: El elemento ExceptionFieldURI identifica errores concretos en una solicitud. Este elemento solo se usa como parte de una respuesta de error en el nodo MessageXml.
ms.openlocfilehash: a47d44098f85d8bacb1e7a2c48a33e478e56c7ac
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44454347"
---
# <a name="exceptionfielduri"></a>ExceptionFieldURI

El elemento **ExceptionFieldURI** identifica errores concretos en una solicitud. Este elemento solo se usa como parte de una respuesta de error en el nodo [MessageXml](messagexml.md) . 
  
```xml
<ExceptionFieldURI FieldURI="" />
```

 **ExceptionPropertyURIType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Descripción**|
|:-----|:-----|
|**FieldURI** <br/> |Identifica una propiedad de una ocurrencia de un elemento periódico. Este atributo es obligatorio.  <br/> |
   
#### <a name="fielduri-attribute"></a>Atributo FieldURI

|**Valor**|**Descripción**|
|:-----|:-----|
|datos adjuntos: nombre  <br/> |Identifica el nombre de datos adjuntos que contiene un error.  <br/> |
|datos adjuntos: ContentType  <br/> |Identifica el tipo de contenido que contiene un error.  <br/> |
|datos adjuntos: contenido  <br/> |Identifica el contenido como que contiene un error.  <br/> |
|periodicidad: mes  <br/> |Identifica el campo month con un error.  <br/> |
|periodicidad: DayOfWeekIndex  <br/> |Identifica el índice del día de la semana que contiene un error.  <br/> |
|periodicidad: DaysOfWeek  <br/> |Identifica la propiedad DaysOfWeek que contiene un error.  <br/> |
|periodicidad: DayOfMonth  <br/> |Identifica el DayOfMonth que contiene un error.  <br/> |
|periodicidad: intervalo  <br/> |Identifica el intervalo como que contiene un error.  <br/> |
|periodicidad: NumberOfOccurrences  <br/> |Identifica el número de repeticiones que contienen un error.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[MessageXml](messagexml.md) <br/> |Proporciona información de respuesta de error adicional.  <br/> |
   
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

