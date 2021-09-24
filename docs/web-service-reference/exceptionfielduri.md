---
title: ExceptionFieldURI
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ExceptionFieldURI
api_type:
- schema
ms.assetid: 7afda93a-0f8c-4c9e-8e09-f1b0bfc928bf
description: El elemento ExceptionFieldURI identifica errores concretos en una solicitud. Este elemento solo se usa como parte de una respuesta de error en el nodo MessageXml.
ms.openlocfilehash: 7368fd51e8eca2081b1fd50c86bce9ffa469c6b1
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59524332"
---
# <a name="exceptionfielduri"></a>ExceptionFieldURI

El **elemento ExceptionFieldURI** identifica errores concretos en una solicitud. Este elemento solo se usa como parte de una respuesta de error en el [nodo MessageXml.](messagexml.md) 
  
```xml
<ExceptionFieldURI FieldURI="" />
```

 **ExceptionPropertyURIType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Descripción**|
|:-----|:-----|
|**FieldURI** <br/> |Identifica una propiedad de una aparición de un elemento periódico. Este atributo es obligatorio.  <br/> |
   
#### <a name="fielduri-attribute"></a>Atributo FieldURI

|**Valor**|**Descripción**|
|:-----|:-----|
|attachment:Name  <br/> |Identifica el nombre de los datos adjuntos como que contiene un error.  <br/> |
|attachment:ContentType  <br/> |Identifica el tipo de contenido como que contiene un error.  <br/> |
|attachment:Content  <br/> |Identifica el contenido como que contiene un error.  <br/> |
|recurrence:Month  <br/> |Identifica el campo de mes como que contiene un error.  <br/> |
|recurrence:DayOfWeekIndex  <br/> |Identifica el índice del día de la semana como que contiene un error.  <br/> |
|recurrence:DaysOfWeek  <br/> |Identifica la propiedad DaysOfWeek como que contiene un error.  <br/> |
|recurrence:DayOfMonth  <br/> |Identifica el DayOfMonth como que contiene un error.  <br/> |
|recurrence:Interval  <br/> |Identifica el intervalo como que contiene un error.  <br/> |
|recurrence:NumberOfOccurrences  <br/> |Identifica el número de repeticiones como que contienen un error.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[MessageXml](messagexml.md) <br/> |Proporciona información adicional de respuesta a errores.  <br/> |
   
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

