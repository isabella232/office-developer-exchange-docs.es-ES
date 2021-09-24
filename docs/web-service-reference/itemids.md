---
title: ItemIds
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ItemIds
api_type:
- schema
ms.assetid: 6b82122b-5544-4adf-91b7-ef2db7d5046f
description: El elemento ItemIds contiene las identidades únicas de los elementos, los elementos de repetición y los elementos maestros periódicos que se usan para eliminar, enviar, obtener, mover o copiar elementos del Exchange almacén.
ms.openlocfilehash: 7341b8214b4d61564bd87707a9d8c76fbca07628
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59522890"
---
# <a name="itemids"></a>ItemIds
  
El **elemento ItemIds** contiene las identidades únicas de los elementos, los elementos de repetición y los elementos maestros periódicos que se usan para eliminar, enviar, obtener, mover o copiar elementos del Exchange almacén.
  
```xml
<ItemIds>
   <ItemId/>
   <OccurrenceItemId/>
   <RecurringMasterItemId/>
</ItemIds>
```

**NonEmptyArrayOfBaseItemIdsType**

## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios. 
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[ItemId](itemid.md) <br/> |Contiene el identificador único y la clave de cambio de un elemento en el Exchange almacén.  <br/> |
|[OccurrenceItemId](occurrenceitemid.md) <br/> |Identifica una única aparición de un elemento periódico.  <br/> |
|[RecurringMasterItemId](recurringmasteritemid.md) <br/> |Identifica un elemento maestro de periodicidad identificando uno de los identificadores de los elementos de repetición relacionados.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Conversation (ConversationType)](conversation-conversationtype.md) <br/> |Representa una sola conversación.  <br/> |
|[DeleteItem](deleteitem.md) <br/> |Define una solicitud para eliminar elementos en el Exchange almacén.  <br/> A continuación se muestra la expresión XPath de este elemento:  <br/>  `/DeleteItem` <br/> |
|[SendItem](senditem.md) <br/> |Elemento raíz que define una solicitud para enviar elementos en el Exchange almacén.  <br/> A continuación se muestra la expresión XPath de este elemento:  <br/>  `/SendItem` <br/> |
|[GetItem](getitem.md) <br/> |Define una solicitud para obtener elementos del Exchange almacén.  <br/> A continuación se muestra la expresión XPath de este elemento:  <br/>  `/GetItem` <br/> |
|[MoveItem](moveitem.md) <br/> |Define una solicitud para mover elementos en el Exchange almacén.  <br/> A continuación se muestra la expresión XPath de este elemento:  <br/>  `/MoveItem` <br/> |
|[CopyItem](copyitem.md) <br/> |Define una solicitud para copiar elementos en el Exchange almacén.  <br/> A continuación se muestra la expresión XPath de este elemento:  <br/>  `/CopyItem` <br/> |
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también

- [Operación DeleteItem](deleteitem-operation.md)
- [Operación SendItem](senditem-operation.md) 
- [Operación GetItem](getitem-operation.md)
- [Operación MoveItem](moveitem-operation.md)
- [Operación CopyItem](copyitem-operation.md)
- [Operación FindConversation](findconversation-operation.md)

