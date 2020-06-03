---
title: OccurrenceItemId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- OccurrenceItemId
api_type:
- schema
ms.assetid: 4a15bbc3-5b93-4193-b9ec-da32f0a9a552
description: El elemento OccurrenceItemId identifica una única ocurrencia de un elemento periódico.
ms.openlocfilehash: 37c3a2442afb3302bca88ef0301e98013ff0319b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468379"
---
# <a name="occurrenceitemid"></a>OccurrenceItemId

El elemento **OccurrenceItemId** identifica una única ocurrencia de un elemento periódico. 
  
```XML
<OccurrenceItemId RecurringMasterId="" ChangeKey="" InstanceIndex=""/>
```

**OccurrenceItemIdType**

## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Descripción**|
|:-----|:-----|
|**RecurringMasterId** <br/> |Identifica el maestro recurrente de un elemento periódico. Este atributo es obligatorio.  <br/> |
|**ChangeKey** <br/> |Identifica una versión específica del maestro periódico o de una ocurrencia del elemento. Si el patrón recurrente o cualquiera de sus repeticiones cambia, el **changekey** cambia. El **changekey** es el mismo para el maestro periódico y todas las repeticiones.  <br/> |
|**InstanceIndex** <br/> |Identifica el índice de la ocurrencia del elemento. Este atributo es obligatorio. Este valor representa un número entero.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[GlobalItemIds](globalitemids.md) <br/> |Contiene la colección de identificadores de elemento para todos los elementos de conversación en un buzón.  <br/> |
|[ItemIds](itemids.md) <br/> | Contiene las identidades únicas de los elementos, los elementos de ocurrencia y los elementos maestros periódicos que se usan para eliminar, enviar, obtener, mover o copiar elementos en el almacén de Exchange. <br/><br/>Las siguientes son las expresiones XPath de este elemento: <br/><br/>  `/DeleteItem/ItemIds` <br/>  `/SendItem/ItemIds` <br/>  `/GetItem/ItemIds` <br/><br/>**Nota**: las operaciones [MoveItem](moveitem-operation.md) y [CopyItem](copyitem-operation.md) solo funcionan con elementos de calendario únicos y elementos de patrón periódicos. Las repeticiones de elementos no son válidas con estas operaciones.           |
|[ItemChange](itemchange.md) <br/> |Contiene un identificador de elemento y las actualizaciones que se aplican al elemento.<br/><br/> La siguiente es la expresión XPath a este elemento:  <br/>  `/UpdateItem/ItemChanges/ItemChange[i]` <br/> |
   
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="example"></a>Ejemplo

En el ejemplo siguiente se identifica la cuarta ocurrencia de un elemento periódico que tiene la identidad 34vswe4.
  
```XML
<OccurrenceItemId RecurringMasterId="34vswe4" InstanceIndex="4" />
```

## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también

- [RecurringMasterItemId](recurringmasteritemid.md)
- [Operación FindConversation](findconversation-operation.md)
- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)

