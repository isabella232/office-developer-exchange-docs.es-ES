---
title: ItemChange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ItemChange
api_type:
- schema
ms.assetid: 5cb43b02-d444-4d9c-9075-cdc5a4427daf
description: El elemento ItemChange contiene un identificador de elemento y las actualizaciones que se aplicarán al elemento.
ms.openlocfilehash: 8ace3cf78eb902e48529a0534e39ce7d584bd164
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59537752"
---
# <a name="itemchange"></a>ItemChange

El **elemento ItemChange** contiene un identificador de elemento y las actualizaciones que se aplicarán al elemento. 
  
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

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[ItemId](itemid.md) <br/> |Contiene el identificador único y la clave de cambio de un elemento en el Exchange almacén. Este elemento es necesario si no se [usa el elemento OccurrenceItemId](occurrenceitemid.md) o [RecurringMasterItemId.](recurringmasteritemid.md)  <br/> |
|[OccurrenceItemId](occurrenceitemid.md) <br/> |Identifica una única aparición de un elemento periódico. Este elemento es necesario si se usa. Este elemento es necesario si no se [usa el elemento RecurringMasterItemId](recurringmasteritemid.md) o [ItemId.](itemid.md)  <br/> |
|[RecurringMasterItemId](recurringmasteritemid.md) <br/> |Identifica un elemento maestro de periodicidad identificando uno de los identificadores de los elementos de repetición relacionados. Este elemento es necesario si se usa. Este elemento es necesario si no se [usa el elemento OccurrenceItemId](occurrenceitemid.md) o [ItemId.](itemid.md)  <br/> |
|[Updates (Elemento)](updates-item.md) <br/> |Contiene una matriz que define los cambios de anexar, establecer y eliminar a las propiedades del elemento. Se requiere este elemento.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[ItemChanges](itemchanges.md) <br/> |Contiene una matriz de [elementos ItemChange](itemchange.md) que identifican los elementos y las actualizaciones que se deben aplicar a los elementos.  <br/> A continuación se muestra la expresión XPath de este elemento:  <br/>  `/UpdateItem/ItemChanges` <br/> |
   
## <a name="remarks"></a>Comentarios

Solo se [puede usar un elemento ItemId](itemid.md), [OccurrenceItemId](occurrenceitemid.md)o [RecurringMasterItemId](recurringmasteritemid.md) en un **elemento ItemChange.** 
  
El esquema que describe este elemento se encuentra en el directorio virtual EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor Acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también

- [Operación UpdateItem](updateitem-operation.md)

