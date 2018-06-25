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
description: El elemento OccurrenceItemId identifica una sola aparición de un elemento periódico.
ms.openlocfilehash: e3d7b6efc49775f54219ce0dc0ec39a34a95f8fd
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836639"
---
# <a name="occurrenceitemid"></a>OccurrenceItemId

El elemento **OccurrenceItemId** identifica una sola aparición de un elemento periódico. 
  
```XML
<OccurrenceItemId RecurringMasterId="" ChangeKey="" InstanceIndex=""/>
```

**OccurrenceItemIdType**

## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Attribute**|**Descripción**|
|:-----|:-----|
|**RecurringMasterId** <br/> |Identifica al patrón periódico de un elemento periódico. Este atributo es necesario.  <br/> |
|**ChangeKey** <br/> |Identifica una versión específica del patrón periódico o una ocurrencia del elemento. Si cambia el patrón periódico o cualquiera de sus apariciones, cambia el **ChangeKey** . El **ChangeKey** es el mismo para el patrón de periódico y todas las apariciones.  <br/> |
|**InstanceIndex** <br/> |Identifica el índice de la aparición de elemento. Este atributo es necesario. Este valor representa un número entero.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[GlobalItemIds](globalitemids.md) <br/> |Contiene la colección de identificadores de elemento para todos los elementos de la conversación en un buzón de correo.  <br/> |
|[ItemId](itemids.md) <br/> | Contiene las identidades únicas de los elementos, elementos de aparición y elementos maestros periódicos que se usan para eliminar, enviar, obtener, mover o copiar elementos en el almacén de Exchange. <br/><br/>Los siguientes son las expresiones de XPath para este elemento: <br/><br/>  `/DeleteItem/ItemIds` <br/>  `/SendItem/ItemIds` <br/>  `/GetItem/ItemIds` <br/><br/>**Nota**: [operación de MoveItem](moveitem-operation.md) y [CopyItem](copyitem-operation.md) sólo funcionan con elementos de calendario único y elementos maestros periódicos. Repeticiones de elemento no son válidas con estas operaciones.           |
|[ItemChange](itemchange.md) <br/> |Contiene un identificador de elemento y las actualizaciones que se debe aplicar al elemento.<br/><br/> La siguiente es la expresión de XPath para este elemento:  <br/>  `/UpdateItem/ItemChanges/ItemChange[i]` <br/> |
   
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="example"></a>Ejemplo

En el ejemplo siguiente se identifica la aparición de un elemento periódico que tiene la identidad 34vswe4 cuarto.
  
```XML
<OccurrenceItemId RecurringMasterId="34vswe4" InstanceIndex="4" />
```

## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Vea también

- [RecurringMasterItemId](recurringmasteritemid.md)
- [Operación de FindConversation](findconversation-operation.md)
- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

