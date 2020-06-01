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
description: El elemento ItemChange contiene un identificador de elemento y las actualizaciones que se aplican al elemento.
ms.openlocfilehash: 916ef1ba2c7a709ec1fd80ababd72999506773c4
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459920"
---
# <a name="itemchange"></a>ItemChange

El elemento **ItemChange** contiene un identificador de elemento y las actualizaciones que se aplican al elemento. 
  
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

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[ItemId](itemid.md) <br/> |Contiene el identificador único y la clave de cambio de un elemento en el almacén de Exchange. Este elemento es obligatorio si no se usa el elemento [OccurrenceItemId](occurrenceitemid.md) o [RecurringMasterItemId](recurringmasteritemid.md) .  <br/> |
|[OccurrenceItemId](occurrenceitemid.md) <br/> |Identifica una única ocurrencia de un elemento periódico. Este elemento es obligatorio si se usa. Este elemento es obligatorio si no se usa el elemento [RecurringMasterItemId](recurringmasteritemid.md) o [Itemid](itemid.md) .  <br/> |
|[RecurringMasterItemId](recurringmasteritemid.md) <br/> |Identifica un elemento principal de periodicidad mediante la identificación de uno de los identificadores de elementos de ocurrencia relacionados. Este elemento es obligatorio si se usa. Este elemento es obligatorio si no se usa el elemento [OccurrenceItemId](occurrenceitemid.md) o [Itemid](itemid.md) .  <br/> |
|[Actualizaciones (elemento)](updates-item.md) <br/> |Contiene una matriz que define los cambios de anexión, establecimiento y eliminación en las propiedades de elemento. Se requiere este elemento.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[ItemChanges](itemchanges.md) <br/> |Contiene una matriz de elementos [ItemChange](itemchange.md) que identifican los elementos y las actualizaciones que se aplican a los elementos.  <br/> La siguiente es la expresión XPath a este elemento:  <br/>  `/UpdateItem/ItemChanges` <br/> |
   
## <a name="remarks"></a>Comentarios

Solo se puede usar un elemento [Itemid](itemid.md), [OccurrenceItemId](occurrenceitemid.md)o [RecurringMasterItemId](recurringmasteritemid.md) en un elemento **ItemChange** . 
  
El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también

- [Operación UpdateItem](updateitem-operation.md)

