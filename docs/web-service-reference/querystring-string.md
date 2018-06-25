---
title: QueryString (cadena)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f81b1b3d-9fe4-4ab3-b517-42e4207fa596
description: El elemento de QueryString especifica un conjunto de valores que se devolverá que coinciden con la cadena de consulta en una solicitud de operación FindPeople. Una búsqueda con ninguna cadena de consulta especificada devuelve todos los elementos de la carpeta especificada.
ms.openlocfilehash: 9c5c733adcec1496e36986fd720b56b0a0274593
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836935"
---
# <a name="querystring-string"></a>QueryString (cadena)

El elemento de **QueryString** especifica un conjunto de valores que se devolverá que coinciden con la cadena de consulta en una solicitud de [operación FindPeople](findpeople-operation.md) . Una búsqueda con ninguna **cadena de consulta** especificada devuelve todos los elementos de la carpeta especificada. 
  
```XML
<QueryString/> 
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
|[FindPeople](findpeople.md) <br/> |Contiene los argumentos para una búsqueda de la [operación de FindPeople](findpeople-operation.md) .  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto de la **cadena de consulta** representa una consulta de buzón de correo realizada mediante un subconjunto de la [Sintaxis de consulta avanzada (AQS)](http://msdn.microsoft.com/en-us/library/aa965711%28VS.85%29.aspx). Para obtener información sobre la sintaxis de este elemento, vea [QueryString (QueryStringType)](querystring-querystringtype.md).
  
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Vea también



[Operación FindPeople](findpeople-operation.md)


- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

