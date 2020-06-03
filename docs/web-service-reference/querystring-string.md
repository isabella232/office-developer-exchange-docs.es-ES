---
title: QueryString (cadena)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f81b1b3d-9fe4-4ab3-b517-42e4207fa596
description: El elemento QueryString especifica un conjunto de valores que se devolverán que coinciden con la cadena de consulta en una solicitud de operación FindPeople. Una búsqueda sin cadena de consulta especificada devuelve todos los elementos de la carpeta especificada.
ms.openlocfilehash: ec025f86d3e6fb74810e9c539eba102d05adbb93
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465327"
---
# <a name="querystring-string"></a>QueryString (cadena)

El elemento **QueryString** especifica un conjunto de valores que se devolverán que coinciden con la cadena de consulta en una solicitud de [operación FindPeople](findpeople-operation.md) . Una búsqueda sin **cadena** de consulta especificada devuelve todos los elementos de la carpeta especificada. 
  
```XML
<QueryString/> 
```

 **string**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[FindPeople](findpeople.md) <br/> |Contiene los argumentos para una búsqueda de [operación FindPeople](findpeople-operation.md) .  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto **QueryString** representa una consulta de buzón realizada mediante un subconjunto de [Sintaxis de consulta avanzada (AQS)](https://msdn.microsoft.com/library/aa965711%28VS.85%29.aspx). Para obtener información acerca de la sintaxis de este elemento, consulte [QueryString (QueryStringType)](querystring-querystringtype.md).
  
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también



[Operación FindPeople](findpeople-operation.md)


- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)

