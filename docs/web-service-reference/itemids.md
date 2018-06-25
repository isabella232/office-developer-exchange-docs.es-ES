---
title: ItemIds
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ItemIds
api_type:
- schema
ms.assetid: 6b82122b-5544-4adf-91b7-ef2db7d5046f
description: El elemento de ItemId contiene las identidades únicas de los elementos, elementos de aparición y elementos maestros periódicos que se usan para eliminar, enviar, obtener, mover o copiar elementos en el almacén de Exchange.
ms.openlocfilehash: 1bd4d6f4593a7c3b418561269d8b29707cc6030c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836155"
---
# <a name="itemids"></a>ItemIds
  
El elemento de **ItemID** contiene las identidades únicas de los elementos, elementos de aparición y elementos maestros periódicos que se usan para eliminar, enviar, obtener, mover o copiar elementos en el almacén de Exchange.
  
```xml
<ItemIds>
   <ItemId/>
   <OccurrenceItemId/>
   <RecurringMasterItemId/>
</ItemIds>
```

**NonEmptyArrayOfBaseItemIdsType**

## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios. 
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[ItemId](itemid.md) <br/> |Contiene el único identificador y cambiar la clave de un elemento en el almacén de Exchange.  <br/> |
|[OccurrenceItemId](occurrenceitemid.md) <br/> |Identifica una sola aparición de un elemento periódico.  <br/> |
|[RecurringMasterItemId](recurringmasteritemid.md) <br/> |Identifica un elemento de patrón de periodicidad mediante la identificación de uno de los identificadores de los elementos de su aparición relacionados.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[Conversación (ConversationType)](conversation-conversationtype.md) <br/> |Representa una sola conversación.  <br/> |
|[DeleteItem](deleteitem.md) <br/> |Define una solicitud para eliminar los elementos en el almacén de Exchange.  <br/> La siguiente es la expresión de XPath para este elemento:  <br/>  `/DeleteItem` <br/> |
|[SendItem](senditem.md) <br/> |El elemento raíz que define una solicitud de envío de elementos en el almacén de Exchange.  <br/> La siguiente es la expresión de XPath para este elemento:  <br/>  `/SendItem` <br/> |
|[GetItem](getitem.md) <br/> |Define una solicitud para obtener los elementos desde el almacén de Exchange.  <br/> La siguiente es la expresión de XPath para este elemento:  <br/>  `/GetItem` <br/> |
|[MoveItem](moveitem.md) <br/> |Define una solicitud para mover los elementos en el almacén de Exchange.  <br/> La siguiente es la expresión de XPath para este elemento:  <br/>  `/MoveItem` <br/> |
|[CopyItem](copyitem.md) <br/> |Define una solicitud para copiar elementos en el almacén de Exchange.  <br/> La siguiente es la expresión de XPath para este elemento:  <br/>  `/CopyItem` <br/> |
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Vea también

- [Operación DeleteItem](deleteitem-operation.md)
- [Operación SendItem](senditem-operation.md) 
- [Operación GetItem](getitem-operation.md)
- [Operación MoveItem](moveitem-operation.md)
- [Operación CopyItem](copyitem-operation.md)
- [Operación de FindConversation](findconversation-operation.md)

