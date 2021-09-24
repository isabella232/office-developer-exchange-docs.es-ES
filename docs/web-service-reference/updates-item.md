---
title: Updates (Elemento)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Updates
api_type:
- schema
ms.assetid: 5c1a855e-390d-4713-9d10-6e86ca392814
description: El elemento Updates contiene un conjunto de elementos que definen los cambios de anexar, establecer y eliminar a las propiedades del elemento.
ms.openlocfilehash: b4a343d941d29e9b25ebedfbf25894c7ec9b22d7
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59517409"
---
# <a name="updates-item"></a>Updates (Elemento)

El **elemento Updates** contiene un conjunto de elementos que definen los cambios de anexar, establecer y eliminar a las propiedades del elemento. 
  
- [UpdateItem](updateitem.md)
  
- [ItemChanges](itemchanges.md)
  
- [ItemChange](itemchange.md)
  
- [Updates (Elemento)](updates-item.md)
  
```xml
<Updates>
   <AppendToItemField/>
   <SetItemField/>
   <DeleteItemField/>
</Updates>
```

**NonEmptyArrayOfItemChangeDescriptionsType**

## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[AppendToItemField](appendtoitemfield.md) <br/> |Representa los datos para anexar a una sola propiedad de un elemento durante una [operación UpdateItem](updateitem-operation.md).  <br/> |
|[SetItemField](setitemfield.md) <br/> |Representa una actualización de una sola propiedad de un elemento en una [operación UpdateItem](updateitem-operation.md).  <br/> |
|[DeleteItemField](deleteitemfield.md) <br/> |Representa una operación para eliminar una propiedad determinada de un elemento durante una [operación UpdateItem](updateitem-operation.md).  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[ItemChange](itemchange.md) <br/> |Contiene un identificador de elemento y las actualizaciones que se aplicarán al elemento.  <br/> A continuación se muestra la expresión XPath de este elemento:  `/UpdateItem/ItemChanges/ItemChange[i]` <br/> |
   
## <a name="remarks"></a>Comentarios

Las actualizaciones definidas por este elemento se realizan en el elemento identificado por los [elementos ItemId](itemid.md), [OccurrenceItemId](occurrenceitemid.md)o [RecurringMasterItemId.](recurringmasteritemid.md) 
  
El esquema que describe este elemento se encuentra en el directorio virtual EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor Acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también

- [Operación UpdateItem](updateitem-operation.md)
- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

