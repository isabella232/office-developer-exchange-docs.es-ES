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
description: El elemento ItemIds contiene las identidades únicas de los elementos, los elementos de ocurrencia y los elementos maestros periódicos que se usan para eliminar, enviar, obtener, mover o copiar elementos en el almacén de Exchange.
ms.openlocfilehash: bbd594ce2610bd625b0e16a0383fda552ee9eb19
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44460606"
---
# <a name="itemids"></a>ItemIds
  
El elemento **ItemIds** contiene las identidades únicas de los elementos, los elementos de ocurrencia y los elementos maestros periódicos que se usan para eliminar, enviar, obtener, mover o copiar elementos en el almacén de Exchange.
  
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

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[ItemId](itemid.md) <br/> |Contiene el identificador único y la clave de cambio de un elemento en el almacén de Exchange.  <br/> |
|[OccurrenceItemId](occurrenceitemid.md) <br/> |Identifica una única ocurrencia de un elemento periódico.  <br/> |
|[RecurringMasterItemId](recurringmasteritemid.md) <br/> |Identifica un elemento principal de periodicidad mediante la identificación de uno de los identificadores de elementos de ocurrencia relacionados.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Conversación (ConversationType)](conversation-conversationtype.md) <br/> |Representa una sola conversación.  <br/> |
|[DeleteItem](deleteitem.md) <br/> |Define una solicitud para eliminar elementos en el almacén de Exchange.  <br/> La siguiente es la expresión XPath a este elemento:  <br/>  `/DeleteItem` <br/> |
|[SendItem](senditem.md) <br/> |El elemento raíz que define una solicitud para enviar elementos en el almacén de Exchange.  <br/> La siguiente es la expresión XPath a este elemento:  <br/>  `/SendItem` <br/> |
|[GetItem](getitem.md) <br/> |Define una solicitud para obtener elementos del almacén de Exchange.  <br/> La siguiente es la expresión XPath a este elemento:  <br/>  `/GetItem` <br/> |
|[MoveItem](moveitem.md) <br/> |Define una solicitud para mover elementos en el almacén de Exchange.  <br/> La siguiente es la expresión XPath a este elemento:  <br/>  `/MoveItem` <br/> |
|[CopyItem](copyitem.md) <br/> |Define una solicitud para copiar elementos en el almacén de Exchange.  <br/> La siguiente es la expresión XPath a este elemento:  <br/>  `/CopyItem` <br/> |
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también

- [Operación DeleteItem](deleteitem-operation.md)
- [Operación SendItem](senditem-operation.md) 
- [Operación GetItem](getitem-operation.md)
- [Operación MoveItem](moveitem-operation.md)
- [Operación CopyItem](copyitem-operation.md)
- [Operación FindConversation](findconversation-operation.md)

