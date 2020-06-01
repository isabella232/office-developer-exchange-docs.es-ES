---
title: SortBy
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3dc4ab23-26b0-42b3-8930-f1c7eefecdeb
description: El elemento SortBy contiene una propiedad de elemento usada para ordenar los resultados de búsqueda.
ms.openlocfilehash: cf2b1e633bc66e526028078833afade363e4c5e0
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44468400"
---
# <a name="sortby"></a>SortBy

El elemento **sortBy** contiene una propiedad de elemento usada para ordenar los resultados de búsqueda. 
  
```XML
<SortBy Order="">
   <FieldURI/>
   <IndexedFieldURI/>
</SortBy>
```

 **FieldOrderType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Descripción**|
|:-----|:-----|
|Order  <br/> |El valor de texto del atributo **Order** es el criterio de ordenación. Un valor de texto **ascendente** indica que los resultados están en orden ascendente. Un valor de texto **descendente** indica que los resultados están en orden descendente.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

[FieldURI](fielduri.md)  |  [IndexedFieldURI](indexedfielduri.md)
  
### <a name="parent-elements"></a>Elementos principales

[SearchMailboxes](searchmailboxes.md)
  
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages. xsd  <br/> |
|Puede estar vacío  <br/> ||
   

