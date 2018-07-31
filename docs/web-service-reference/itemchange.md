---
title: ItemChange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ItemChange
api_type:
- schema
ms.assetid: 5cb43b02-d444-4d9c-9075-cdc5a4427daf
description: El elemento ItemChange contiene un identificador de elemento y las actualizaciones que se debe aplicar al elemento.
ms.openlocfilehash: 42484c8deecb106e05023215342af3c7d996d852
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/28/2018
ms.locfileid: "21353514"
---
# <a name="itemchange"></a>ItemChange

El elemento **ItemChange** contiene un identificador de elemento y las actualizaciones que se debe aplicar al elemento. 
  
- [UpdateItem](updateitem.md) 
- [ItemChanges](itemchanges.md)
- [ItemChange](itemchange.md)
  
```xml
<ItemChange>
   <ItemId/>
   <Updates>...</Updates>
</ItemChange>
```

```xml
<ItemChange>
   <OccurrenceItemId>...</OccurrenceItemId>
   <Updates>...</Updates>
</ItemChange>
```

```xml
<ItemChange>
   <RecurringMasterItemId>...</RecurringMasterItemId>
   <Updates>...</Updates>
</ItemChange>
```

**ItemChangeType**

## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[ItemId](itemid.md) <br/> |Contiene el único identificador y cambiar la clave de un elemento en el almacén de Exchange. Este elemento es necesario si no se usa el elemento [OccurrenceItemId](occurrenceitemid.md) o [RecurringMasterItemId](recurringmasteritemid.md) .  <br/> |
|[OccurrenceItemId](occurrenceitemid.md) <br/> |Identifica una sola aparición de un elemento periódico. Este elemento es necesario si utiliza. Este elemento es necesario si no se usa el elemento [RecurringMasterItemId](recurringmasteritemid.md) o [ItemId](itemid.md) .  <br/> |
|[RecurringMasterItemId](recurringmasteritemid.md) <br/> |Identifica un elemento de patrón de periodicidad mediante la identificación de uno de los identificadores de los elementos de su aparición relacionados. Este elemento es necesario si utiliza. Este elemento es necesario si no se usa el elemento [OccurrenceItemId](occurrenceitemid.md) o [ItemId](itemid.md) .  <br/> |
|[Updates (Elemento)](updates-item.md) <br/> |Contiene una matriz que define append, establecer y eliminar los cambios realizados en las propiedades de elementos. Se requiere este elemento.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[ItemChanges](itemchanges.md) <br/> |Contiene una matriz de elementos de [ItemChange](itemchange.md) que identifican los elementos y las actualizaciones que se debe aplicar a los elementos.  <br/> La siguiente es la expresión de XPath para este elemento:  <br/>  `/UpdateItem/ItemChanges` <br/> |
   
## <a name="remarks"></a>Comentarios

Sólo un elemento [ItemId](itemid.md), [OccurrenceItemId](occurrenceitemid.md)o [RecurringMasterItemId](recurringmasteritemid.md) único puede usarse en un elemento **ItemChange** . 
  
El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Vea también

- [Operación UpdateItem](updateitem-operation.md)

