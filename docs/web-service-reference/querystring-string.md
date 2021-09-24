---
title: QueryString (Cadena)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: f81b1b3d-9fe4-4ab3-b517-42e4207fa596
description: El elemento QueryString especifica un conjunto de valores que se devolverán que coinciden con la cadena de consulta en una solicitud de operación FindPeople. Una búsqueda sin queryString especificada devuelve todos los elementos de la carpeta especificada.
ms.openlocfilehash: 6dfd4b5552511e2551baf5ce645f82d4f74e5499
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59523737"
---
# <a name="querystring-string"></a>QueryString (Cadena)

El **elemento QueryString** especifica un conjunto de valores que se devolverán que coinciden con la cadena de consulta en una [solicitud de operación FindPeople.](findpeople-operation.md) Una búsqueda sin **queryString** especificada devuelve todos los elementos de la carpeta especificada. 
  
```XML
<QueryString/> 
```

 **string**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[FindPeople](findpeople.md) <br/> |Contiene los argumentos de una [búsqueda de operación FindPeople.](findpeople-operation.md)  <br/> |
   
## <a name="text-value"></a>Valor de texto

El **valor de texto QueryString** representa una consulta de buzón realizada mediante un subconjunto de sintaxis de consulta avanzada [(AQS).](https://msdn.microsoft.com/library/aa965711%28VS.85%29.aspx) Para obtener información acerca de la sintaxis de este elemento, vea [QueryString (QueryStringType).](querystring-querystringtype.md)
  
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre del esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también



[Operación FindPeople](findpeople-operation.md)


- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

