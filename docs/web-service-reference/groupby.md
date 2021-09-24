---
title: GroupBy
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- GroupBy
api_type:
- schema
ms.assetid: 9728619b-4674-4b9d-9f6c-e75c6165966c
description: El elemento GroupBy especifica una agrupación arbitraria para las consultas FindItem.
ms.openlocfilehash: 15e2d818ceae81f08ad0c52d9bdc881f7c3e2579
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59539805"
---
# <a name="groupby"></a>GroupBy

El **elemento GroupBy** especifica una agrupación arbitraria para las consultas FindItem. 
  
- [FindItem](finditem.md)
- [GroupBy](groupby.md)
  
```xml
<GroupBy Order="">
   <FieldURI/>
   <AggregateOn/>
</GroupBy>
```

```xml
<GroupBy Order="">
   <ExtendededFieldURI/>
   <AggregateOn/>
</GroupBy>
```

```xml
<GroupBy Order="">
   <IndexedFieldURI/>
   <AggregateOn/>
</GroupBy>
```

**GroupByType**

## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Descripción**|
|:-----|:-----|
|**Order** <br/> | Determina el orden de los grupos en la matriz de elementos agrupados que se devuelve en la respuesta. Este atributo es de tipo SortDirectionType.  <br/> |
   
#### <a name="order-attribute-values"></a>Valores de atributo Order

|**Valor**|**Descripción**|
|:-----|:-----|
|Ascendente  <br/> |Los grupos se ordenan en orden ascendente.  <br/> |
|Descendente  <br/> |Los grupos se ordenan en orden descendente.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[FieldURI](fielduri.md) <br/> |Identifica las propiedades a las que se hace referencia con frecuencia mediante URI.  <br/> |
|[IndexedFieldURI](indexedfielduri.md) <br/> |Identifica miembros individuales de un diccionario.  <br/> |
|[ExtendedFieldURI](extendedfielduri.md) <br/> |Identifica las propiedades MAPI extendidas para obtener, establecer o crear.  <br/> |
|[AggregateOn](aggregateon.md) <br/> |Representa el campo que se usa para determinar el orden de los grupos en una respuesta.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[FindItem](finditem.md) <br/> |Define una solicitud para buscar elementos en un buzón.  <br/><br/> A continuación se muestra la expresión XPath de este elemento:  `/FindItem` <br/> |
   
## <a name="remarks"></a>Comentarios

La respuesta FindItem contendrá una colección de grupos. Cada grupo contendrá todos los elementos que tenían valores que coinciden con la **propiedad GroupBy.** La propiedad que determina la agrupación se identifica en el [elemento FieldURI](fielduri.md), [IndexedFieldURI](indexedfielduri.md)o [ExtendedFieldURI.](extendedfielduri.md) 
  
El esquema que describe este elemento se encuentra en el directorio virtual EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor Acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también

- [Operación FindItem](finditem-operation.md)
- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)
- [Buscar elementos](https://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

