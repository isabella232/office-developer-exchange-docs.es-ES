---
title: ConversationAction
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ConversationAction
api_type:
- schema
ms.assetid: 9ecea41a-3860-4569-8e9b-284b451fc4e0
description: El elemento ConversationAction contiene una sola acción que se aplicará a una sola conversación.
ms.openlocfilehash: 04af68b4ad8442160792fd3aa9f3259058a0f3a4
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59531109"
---
# <a name="conversationaction"></a>ConversationAction

El **elemento ConversationAction** contiene una sola acción que se aplicará a una sola conversación. 
  
[ApplyConversationAction](applyconversationaction.md)
  
[ConversationActions](conversationactions.md)
  
[ConversationAction](conversationaction.md)
  
```XML
<ConversationAction>
   <Action/>
   <ConversationId/>
   <ContextFolderId/>
   <ConversationLastSyncTime/>
   <ProcessRightAway/>
   <DestinationFolderId/>
   <Categories/>
   <EnableAlwaysDelete/>
   <IsRead/>
   <DeleteType/>
</ConversationAction>
```

 **ConversationActionType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Action (ConversationActionTypeType)](action-conversationactiontypetype.md) <br/> |Contiene la acción que se debe realizar en la conversación especificada por el [elemento ConversationId.](conversationid.md) Este elemento debe estar presente.  <br/> |
|[ConversationId](conversationid.md) <br/> |Contiene el identificador de la conversación que tendrá la acción especificada por el elemento [Action (ConversationActionTypeType)](action-conversationactiontypetype.md) aplicado a los elementos de la conversación. Este elemento debe estar presente.  <br/> |
|[ContextFolderId](contextfolderid.md) <br/> |Indica la carpeta destinada a las acciones que usan carpetas. Este elemento debe estar presente al copiar, eliminar, mover y establecer el estado de lectura en los elementos de conversación de una carpeta de destino.  <br/> |
|[ConversationLastSyncTime](conversationlastsynctime.md) <br/> |Contiene la fecha y hora en que se sincronice por última vez una conversación. Este elemento debe estar presente al intentar eliminar todos los elementos de una conversación que se recibieron hasta la hora especificada.  <br/> |
|[ProcessRightAway](processrightaway.md) <br/> |Indica si la respuesta se envía tan pronto como la acción comienza a procesarse en el servidor o si la respuesta se envía una vez completada la acción. Este elemento debe estar presente para que la respuesta se envíe asincrónica a la acción solicitada.  <br/> |
|[DestinationFolderId](destinationfolderid.md) <br/> |Indica la carpeta de destino para las acciones de copia y movimiento.  <br/> |
|[Categories](categories-ex15websvcsotherref.md) <br/> |Contiene una colección de cadenas que identifican las categorías a las que pertenecen los elementos de una conversación.  <br/> |
|[EnableAlwaysDelete](enablealwaysdelete.md) <br/> |Especifica una marca que habilita la eliminación de todos los elementos nuevos de una conversación.  <br/> |
|[IsRead](isread.md) <br/> |Indica si se ha leído un mensaje.  <br/> |
|[DeleteType](deletetype.md) <br/> |Indica cómo se eliminan los elementos de una conversación.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[ConversationActions](conversationactions.md) <br/> |Contiene una colección de conversaciones y las acciones que se deben aplicar a ellas.  <br/> |
   
## <a name="text-value"></a>Valor de texto

**Valores de texto del elemento ConversationAction**

|**Valor**|**Descripción**|
|:-----|:-----|
|AlwaysCategorize  <br/> |Clasificar siempre la conversación.  <br/> |
|AlwaysDelete  <br/> |Elimine siempre la conversación.  <br/> |
|AlwaysMove  <br/> |Mueva siempre la conversación.  <br/> |
|Eliminar  <br/> |Elimine la conversación.  <br/> |
|Mover  <br/> |Mueva la conversación.  <br/> |
|Copiar  <br/> |Copie la conversación.  <br/> |
|SetReadState  <br/> |Establece el estado de lectura de la conversación.  <br/> |
|SetRetentionPolicy  <br/> |Establezca la directiva de retención de la conversación.  <br/> |
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual de IIS que hospeda Exchange Web Services.Este elemento se introdujo en Exchange Server 2010 Service Pack 1 (SP1).
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también



[Operación ApplyConversationAction](applyconversationaction-operation.md)


- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

