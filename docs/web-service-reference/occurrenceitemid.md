---
title: OccurrenceItemId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- OccurrenceItemId
api_type:
- schema
ms.assetid: 4a15bbc3-5b93-4193-b9ec-da32f0a9a552
description: El elemento OccurrenceItemId identifica una única aparición de un elemento periódico.
ms.openlocfilehash: ac6fc081e67f3897880ad30fcc1b62fe2e844459
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59515421"
---
# <a name="occurrenceitemid"></a>OccurrenceItemId

El **elemento OccurrenceItemId** identifica una única aparición de un elemento periódico. 
  
```XML
<OccurrenceItemId RecurringMasterId="" ChangeKey="" InstanceIndex=""/>
```

**OccurrenceItemIdType**

## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Descripción**|
|:-----|:-----|
|**RecurringMasterId** <br/> |Identifica el patrón periódico de un elemento periódico. Este atributo es obligatorio.  <br/> |
|**ChangeKey** <br/> |Identifica una versión específica del patrón periódico o una aparición de elementos. Si el patrón periódico o cualquiera de sus apariciones cambian, **cambia ChangeKey.** **ChangeKey** es el mismo para el patrón periódico y todas las repeticiones.  <br/> |
|**InstanceIndex** <br/> |Identifica el índice de la aparición del elemento. Este atributo es obligatorio. Este valor representa un entero.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[GlobalItemIds](globalitemids.md) <br/> |Contiene la colección de identificadores de elementos para todos los elementos de conversación de un buzón.  <br/> |
|[ItemIds](itemids.md) <br/> | Contiene las identidades únicas de los elementos, los elementos de repetición y los elementos maestros periódicos que se usan para eliminar, enviar, obtener, mover o copiar elementos en el Exchange almacén. <br/><br/>Las siguientes son las expresiones XPath de este elemento: <br/><br/>  `/DeleteItem/ItemIds` <br/>  `/SendItem/ItemIds` <br/>  `/GetItem/ItemIds` <br/><br/>**NOTA:** [La operación MoveItem y](moveitem-operation.md) la operación [CopyItem](copyitem-operation.md) solo funcionan con elementos de calendario único y elementos maestros periódicos. Las repeticiones de elementos no son válidas con estas operaciones.           |
|[ItemChange](itemchange.md) <br/> |Contiene un identificador de elemento y las actualizaciones que se aplicarán al elemento.<br/><br/> A continuación se muestra la expresión XPath de este elemento:  <br/>  `/UpdateItem/ItemChanges/ItemChange[i]` <br/> |
   
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="example"></a>Ejemplo

En el ejemplo siguiente se identifica la cuarta aparición de un elemento periódico que tiene la identidad 34vswe4.
  
```XML
<OccurrenceItemId RecurringMasterId="34vswe4" InstanceIndex="4" />
```

## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también

- [RecurringMasterItemId](recurringmasteritemid.md)
- [Operación FindConversation](findconversation-operation.md)
- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

