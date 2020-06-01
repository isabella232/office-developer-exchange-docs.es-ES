---
title: FindItem
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FindItem
api_type:
- schema
ms.assetid: f7624f5c-c390-4563-ab9a-08f1024fb914
description: El elemento FindItem define una solicitud para buscar elementos en un buzón.
ms.openlocfilehash: 3aeda1cffc03292734a91bc3fff3289d51c9b445
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460998"
---
# <a name="finditem"></a>FindItem

El elemento **FindItem** define una solicitud para buscar elementos en un buzón. 
  
```xml
<FindItem Traversal="">
   <ItemShape/>
   <IndexedPageItemView/>
   <GroupBy/>
   <Restriction/>
   <SortOrder/>
   <ParentFolderIds/>
   <QueryString/>
</FindItem>
```

```xml
<FindItem Traversal="">
   <ItemShape/>
   <IndexedPageItemView/>
   <DistinguishedGroupBy/>
   <Restriction/>
   <SortOrder/>
   <ParentFolderIds/>
   <QueryString/>
</FindItem>
```

```xml
<FindItem Traversal="">
   <ItemShape/>
   <ContactsView/>
   <GroupBy/>
   <Restriction/>
   <SortOrder/>
   <ParentFolderIds/>
   <QueryString/>
</FindItem>
```

```xml
<FindItem Traversal="">
   <ItemShape/>
   <ContactsView/> 
   <DistinguishedGroupBy/>
   <Restriction/>
   <SortOrder/>
   <ParentFolderIds/>
   <QueryString/>
</FindItem>
```

```xml
<FindItem Traversal="">
   <ItemShape/>
   <CalendarView/>
   <GroupBy/>
   <Restriction/>
   <SortOrder/>
   <ParentFolderIds/>
   <QueryString/>
</FindItem>
```

```xml
<FindItem Traversal="">
   <ItemShape/>
   <FractionalPageItemView/>
   <GroupBy/>
   <Restriction/>
   <SortOrder/>
   <ParentFolderIds/>
   <QueryString/>
</FindItem>
```

```xml
<FindItem Traversal="">
   <ItemShape/>
   <FractionalPageItemView/>
   <DistinguishedGroupBy/>
   <Restriction/>
   <SortOrder/>
   <ParentFolderIds/>
   <QueryString/>
</FindItem>
```


**FindItemType**

## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Descripción**|
|:-----|:-----|
|**Transversal** <br/> |Define si la búsqueda encuentra elementos en las carpetas o en los supercontenedores de las carpetas. Este atributo es obligatorio.  <br/> |
   
#### <a name="traversal-attribute-values"></a>Valores de atributo de recorrido

|**Valor**|**Descripción**|
|:-----|:-----|
|Profunda  <br/> |Devuelve solo las identidades de los elementos de la carpeta.  <br/> |
|SoftDeleted  <br/> |Devuelve solo las identidades de los elementos que están en el contenedor de una carpeta. Tenga en cuenta que un recorrido de eliminación temporal combinado con una restricción de búsqueda dará como resultado la devolución de elementos cero, incluso si hay elementos que coinciden con los criterios de búsqueda.  <br/> |
|Están  <br/> |Devuelve solo las identidades de los elementos asociados de la carpeta.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[ItemShape](itemshape.md) <br/> |Identifica las propiedades del elemento y el contenido que se deben incluir en una respuesta de la [operación FindItem](finditem-operation.md) .  <br/> |
|[IndexedPageItemView](indexedpageitemview.md) <br/> |Describe cómo se devuelve la información de elementos paginados para una solicitud **FindItem** . Este elemento es opcional.  <br/> |
|[FractionalPageItemView](fractionalpageitemview.md) <br/> |Describe dónde se inicia la vista paginada y el número máximo de elementos devueltos en una solicitud **FindItem** . El desplazamiento de la vista paginada desde el principio del conjunto de elementos encontrados se describe mediante una fracción. Este elemento es opcional.  <br/> |
|[CalendarView](calendarview.md) <br/> |Proporciona límites de tiempo para definir una búsqueda para los elementos de calendario. Este elemento es opcional.  <br/> |
|[ContactsView](contactsview.md) <br/> |Define una búsqueda para los elementos de contacto basándose en los nombres para mostrar alfabéticos. Este elemento es opcional.  <br/> |
|[GroupBy](groupby.md) <br/> |Especifica agrupaciones arbitrarias para consultas **FindItem** . Este elemento es opcional.  <br/> |
|[DistinguishedGroupBy](distinguishedgroupby.md) <br/> |Proporciona agrupaciones estándar para las consultas **FindItem** . Este elemento es opcional.  <br/> |
|[Restriction](restriction.md) <br/> |Define la restricción o consulta que se usa para filtrar elementos o carpetas **FindItem**en /  las operaciones de carpeta de**FindFolder** y de búsqueda de la FindItem. Este elemento es opcional.  <br/> |
|[SortOrder](sortorder.md) <br/> |Define cómo se ordenan los elementos en una solicitud FindItem. Este elemento es opcional.  <br/> |
|[ParentFolderIds](parentfolderids.md) <br/> |Identifica las carpetas para buscar las operaciones FindItem y FindFolder.  <br/> |
|[QueryString (QueryStringType)](querystring-querystringtype.md) <br/> |Contiene una cadena de consulta de buzón basada en la sintaxis de consulta avanzada (AQS).  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

Ninguno.
  
## <a name="remarks"></a>Comentarios

Solo se puede incluir uno de los elementos [IndexedPageItemView](indexedpageitemview.md), [FractionalPageItemView](fractionalpageitemview.md), [CalendarView](calendarview.md)o [ContactsView](contactsview.md) en una solicitud **FindItem** . Solo se puede incluir uno de los elementos [GroupBy](groupby.md) o [DistinguishedGroupBy](distinguishedgroupby.md) en una solicitud **FindItem** . 
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también

- [Operación FindItem](finditem-operation.md)
- [Buscar elementos](https://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

