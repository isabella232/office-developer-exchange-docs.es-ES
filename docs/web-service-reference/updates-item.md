---
title: Actualizaciones (elemento)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Updates
api_type:
- schema
ms.assetid: 5c1a855e-390d-4713-9d10-6e86ca392814
description: El elemento de actualizaciones contiene un conjunto de elementos que definen append, establecer y eliminar los cambios realizados en las propiedades de elementos.
ms.openlocfilehash: 13df458c783b942e1c868853c41b6247119cf123
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19840866"
---
# <a name="updates-item"></a>Actualizaciones (elemento)

El elemento de **actualizaciones** contiene un conjunto de elementos que definen append, establecer y eliminar los cambios realizados en las propiedades de elementos. 
  
- [UpdateItem](updateitem.md)
  
- [ItemChanges](itemchanges.md)
  
- [ItemChange](itemchange.md)
  
- [Actualizaciones (elemento)](updates-item.md)
  
```xml
<Updates>
   <AppendToItemField/>
   <SetItemField/>
   <DeleteItemField/>
</Updates>
```

**NonEmptyArrayOfItemChangeDescriptionsType**

## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[AppendToItemField](appendtoitemfield.md) <br/> |Representa los datos que se anexará a una sola propiedad de un elemento durante una [operación de UpdateItem](updateitem-operation.md).  <br/> |
|[SetItemField](setitemfield.md) <br/> |Representa una actualización para una única propiedad de un elemento en una [operación de UpdateItem](updateitem-operation.md).  <br/> |
|[DeleteItemField](deleteitemfield.md) <br/> |Representa una operación para eliminar una propiedad determinada de un elemento durante una [operación de UpdateItem](updateitem-operation.md).  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[ItemChange](itemchange.md) <br/> |Contiene un identificador de elemento y las actualizaciones que se debe aplicar al elemento.  <br/> La siguiente es la expresión de XPath para este elemento:`/UpdateItem/ItemChanges/ItemChange[i]` <br/> |
   
## <a name="remarks"></a>Notas

Las actualizaciones que se definen mediante este elemento se realizan en el elemento que se identifica con los elementos [ItemId](itemid.md), [OccurrenceItemId](occurrenceitemid.md)o [RecurringMasterItemId](recurringmasteritemid.md) . 
  
El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Ver también

- [Operación UpdateItem](updateitem-operation.md)
- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

