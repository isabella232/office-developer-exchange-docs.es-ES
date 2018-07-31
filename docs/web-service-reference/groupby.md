---
title: GroupBy
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GroupBy
api_type:
- schema
ms.assetid: 9728619b-4674-4b9d-9f6c-e75c6165966c
description: El elemento GroupBy especifica una agrupación para las consultas de FindItem arbitraria.
ms.openlocfilehash: cdf9b9906025bc91768bb4a14acb2573801c4e12
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/28/2018
ms.locfileid: "21353220"
---
# <a name="groupby"></a>GroupBy

El elemento **GroupBy** especifica una agrupación para las consultas de FindItem arbitraria. 
  
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

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Attribute**|**Descripción**|
|:-----|:-----|
|**Order** <br/> | Determina el orden de los grupos en la matriz de elemento agrupado que se devuelve en la respuesta. Este atributo es del tipo SortDirectionType.  <br/> |
   
#### <a name="order-attribute-values"></a>Valores de atributo de orden

|**Valor**|**Descripción**|
|:-----|:-----|
|Ascendente  <br/> |Los grupos se ordenan en orden ascendente.  <br/> |
|Descendente  <br/> |Los grupos se ordenan en orden descendente.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[FieldURI](fielduri.md) <br/> |Identifica las propiedades con frecuencia que se hace referencia mediante un identificador URI.  <br/> |
|[IndexedFieldURI](indexedfielduri.md) <br/> |Identifica a los miembros individuales de un diccionario.  <br/> |
|[ExtendedFieldURI](extendedfielduri.md) <br/> |Identifica las propiedades extendidas de MAPI para obtener, establecer o crear.  <br/> |
|[AggregateOn](aggregateon.md) <br/> |Representa el campo que se utiliza para determinar el orden de los grupos en una respuesta.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[FindItem](finditem.md) <br/> |Define una solicitud para buscar elementos en un buzón de correo.  <br/><br/> La siguiente es la expresión de XPath para este elemento:`/FindItem` <br/> |
   
## <a name="remarks"></a>Comentarios

La respuesta FindItem contendrá una colección de grupos. Cada grupo contendrá todos los elementos que han tenido que coincidan con los valores de la propiedad **GroupBy** . La propiedad que determina la agrupación se identifica en el elemento [FieldURI](fielduri.md), [IndexedFieldURI](indexedfielduri.md)o [ExtendedFieldURI](extendedfielduri.md) . 
  
El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Vea también

- [Operación FindItem](finditem-operation.md)
- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)
- [Buscar elementos](http://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

