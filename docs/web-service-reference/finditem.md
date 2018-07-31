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
description: El elemento FindItem define una solicitud para buscar elementos en un buzón de correo.
ms.openlocfilehash: 6664cd91007f1d39db7e8d446e0135f47d5ab932
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/28/2018
ms.locfileid: "21353927"
---
# <a name="finditem"></a>FindItem

El elemento **FindItem** define una solicitud para buscar elementos en un buzón de correo. 
  
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

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Attribute**|**Descripción**|
|:-----|:-----|
|**Cruce seguro del** <br/> |Define si la búsqueda busca elementos en las carpetas o dumpsters de las carpetas. Este atributo es necesario.  <br/> |
   
#### <a name="traversal-attribute-values"></a>Valores de atributo recorrido

|**Valor**|**Descripción**|
|:-----|:-----|
|Superficial  <br/> |Devuelve sólo las identidades de los elementos de la carpeta.  <br/> |
|SoftDeleted  <br/> |Devuelve sólo las identidades de los elementos que se encuentran en una carpeta volcado de archivos. Tenga en cuenta que dará como resultado un recorrido eliminado temporalmente combinado con una restricción de la búsqueda en cero los elementos devueltos incluso si hay elementos que coincidan con los criterios de búsqueda.  <br/> |
|Asociado  <br/> |Devuelve sólo las identidades de elementos asociados en la carpeta.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[ItemShape](itemshape.md) <br/> |Identifica las propiedades de elemento y el contenido que desea incluir en una respuesta de [la operación FindItem](finditem-operation.md) .  <br/> |
|[IndexedPageItemView](indexedpageitemview.md) <br/> |Describe cómo paginada elemento de información se devuelve para una solicitud de **FindItem** . Este elemento es opcional.  <br/> |
|[FractionalPageItemView](fractionalpageitemview.md) <br/> |Describe donde se inicia la vista de página y el número máximo de elementos devueltos en una solicitud de **FindItem** . Se describe el desplazamiento de la vista de página desde el principio del conjunto de elementos encontrados por una fracción. Este elemento es opcional.  <br/> |
|[CalendarView](calendarview.md) <br/> |Proporciona tiempo abarcar límites para definir una búsqueda de elementos de calendario. Este elemento es opcional.  <br/> |
|[ContactsView](contactsview.md) <br/> |Define una búsqueda de elementos de contacto basándose en los nombres para mostrar alfabético. Este elemento es opcional.  <br/> |
|[GroupBy](groupby.md) <br/> |Especifica los grupos arbitrarios para las consultas de **FindItem** . Este elemento es opcional.  <br/> |
|[DistinguishedGroupBy](distinguishedgroupby.md) <br/> |Proporciona agrupaciones estándares para las consultas de **FindItem** . Este elemento es opcional.  <br/> |
|[Restriction](restriction.md) <br/> |Define la restricción o la consulta que se usa para filtrar los elementos o carpetas en **FindItem**/ operaciones de carpeta**FindFolder** y búsqueda. Este elemento es opcional.  <br/> |
|[SortOrder](sortorder.md) <br/> |Define cómo se ordenan los elementos en una solicitud FindItem. Este elemento es opcional.  <br/> |
|[ParentFolderIds](parentfolderids.md) <br/> |Identifica las carpetas para buscar las operaciones FindItem y FindFolder.  <br/> |
|[QueryString (QueryStringType)](querystring-querystringtype.md) <br/> |Contiene una cadena de consulta de buzón de correo basada en la sintaxis de consulta avanzada (AQS).  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

Ninguno.
  
## <a name="remarks"></a>Comentarios

Solo uno de los [IndexedPageItemView](indexedpageitemview.md), [FractionalPageItemView](fractionalpageitemview.md), [CalendarView](calendarview.md)o elementos de [contactos](contactsview.md) puede incluir en una solicitud **FindItem** . Solo uno de los elementos [GroupBy](groupby.md) o [DistinguishedGroupBy](distinguishedgroupby.md) puede incluirse en una solicitud **FindItem** . 
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Vea también

- [Operación FindItem](finditem-operation.md)
- [Buscar elementos](http://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

