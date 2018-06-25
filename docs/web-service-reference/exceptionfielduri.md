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
description: El elemento ExceptionFieldURI identifica errores particulares en una solicitud. Este elemento solo se usa como parte de una respuesta de error en el nodo MessageXml.
ms.openlocfilehash: 79909405179cec0d0b86ad12bf52031e1daeb790
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764466"
---
# <a name="exceptionfielduri"></a>ExceptionFieldURI

El elemento **ExceptionFieldURI** identifica errores particulares en una solicitud. Este elemento solo se usa como parte de una respuesta de error en el nodo [MessageXml](messagexml.md) . 
  
```xml
<ExceptionFieldURI FieldURI="" />
```

 **ExceptionPropertyURIType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Attribute**|**Descripción**|
|:-----|:-----|
|**FieldURI** <br/> |Identifica una propiedad de una ocurrencia de un elemento periódico. Este atributo es necesario.  <br/> |
   
#### <a name="fielduri-attribute"></a>Atributo FieldURI

|**Valor**|**Descripción**|
|:-----|:-----|
|Nombre del archivo adjunto:  <br/> |Identifica el nombre de datos adjuntos como que contiene un error.  <br/> |
|datos adjuntos: ContentType  <br/> |Identifica el tipo de contenido como que contiene un error.  <br/> |
|datos adjuntos: contenido  <br/> |Identifica el contenido como que contiene un error.  <br/> |
|Mes de periodicidad:  <br/> |Identifica el campo mes como que contiene un error.  <br/> |
|Periodicidad: DayOfWeekIndex  <br/> |Identifica el día de índice de la semana como que contiene un error.  <br/> |
|Periodicidad: DaysOfWeek  <br/> |Identifica la propiedad DaysOfWeek como que contiene un error.  <br/> |
|Periodicidad: DayOfMonth  <br/> |Identifica el DayOfMonth como que contiene un error.  <br/> |
|Intervalo de periodicidad:  <br/> |Identifica el intervalo como que contiene un error.  <br/> |
|Periodicidad: NumberOfOccurrences  <br/> |Identifica el número de repeticiones como que contiene un error.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[MessageXml](messagexml.md) <br/> |Proporciona información de la respuesta de error adicionales.  <br/> |
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Vea también



- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

