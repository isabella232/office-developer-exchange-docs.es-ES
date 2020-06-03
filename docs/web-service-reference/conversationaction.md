---
title: ConversationAction
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ConversationAction
api_type:
- schema
ms.assetid: 9ecea41a-3860-4569-8e9b-284b451fc4e0
description: El elemento ConversationAction contiene una sola acción que se aplicará a una única conversación.
ms.openlocfilehash: cb7d874f787b105d5185749dfaf1e940d2411d89
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529255"
---
# <a name="conversationaction"></a>ConversationAction

El elemento **ConversationAction** contiene una sola acción que se aplicará a una única conversación. 
  
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

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Acción (ConversationActionTypeType)](action-conversationactiontypetype.md) <br/> |Contiene la acción que se realizará en la conversación especificada por el elemento [ConversationId](conversationid.md) . Este elemento debe estar presente.  <br/> |
|[ConversationId](conversationid.md) <br/> |Contiene el identificador de la conversación que tendrá la acción especificada por el elemento [Action (ConversationActionTypeType)](action-conversationactiontypetype.md) aplicado a los elementos de la conversación. Este elemento debe estar presente.  <br/> |
|[ContextFolderId](contextfolderid.md) <br/> |Indica la carpeta que está destinada a las acciones que usan carpetas. Este elemento debe estar presente al copiar, eliminar, mover y establecer el estado de lectura en los elementos de la conversación de una carpeta de destino.  <br/> |
|[ConversationLastSyncTime](conversationlastsynctime.md) <br/> |Contiene la fecha y la hora en que una conversación se sincronizó por última vez. Este elemento debe estar presente cuando se intenta eliminar todos los elementos de una conversación que se recibieron hasta la hora especificada.  <br/> |
|[ProcessRightAway](processrightaway.md) <br/> |Indica si la respuesta se envía en cuanto la acción comienza a procesarse en el servidor o si la respuesta se envía una vez completada la acción. Este elemento debe estar presente para que la respuesta se envíe asincrónica a la acción solicitada.  <br/> |
|[DestinationFolderId](destinationfolderid.md) <br/> |Indica la carpeta de destino para las acciones de copiar y mover.  <br/> |
|[Categorías](categories-ex15websvcsotherref.md) <br/> |Contiene una colección de cadenas que identifican las categorías a las que pertenecen los elementos de una conversación.  <br/> |
|[EnableAlwaysDelete](enablealwaysdelete.md) <br/> |Especifica una marca que permite la eliminación para todos los elementos nuevos de una conversación.  <br/> |
|[IsRead](isread.md) <br/> |Indica si se ha leído un mensaje.  <br/> |
|[DeleteType](deletetype.md) <br/> |Indica cómo se eliminan los elementos de una conversación.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[ConversationActions](conversationactions.md) <br/> |Contiene una colección de conversaciones y las acciones que se aplican a ellas.  <br/> |
   
## <a name="text-value"></a>Valor de texto

**Valores de texto del elemento ConversationAction**

|**Valor**|**Descripción**|
|:-----|:-----|
|AlwaysCategorize  <br/> |Clasificar siempre la conversación.  <br/> |
|AlwaysDelete  <br/> |Elimine siempre la conversación.  <br/> |
|AlwaysMove  <br/> |Mueva siempre la conversación.  <br/> |
|Eliminar  <br/> |Elimine la conversación.  <br/> |
|Mover  <br/> |Mover la conversación.  <br/> |
|Copiar  <br/> |Copiar la conversación.  <br/> |
|SetReadState  <br/> |Establezca el estado de lectura de la conversación.  <br/> |
|SetRetentionPolicy  <br/> |Establezca la Directiva de retención para la conversación.  <br/> |
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual de IIS que hospeda los servicios Web de Exchange. este elemento se introdujo en Exchange Server 2010 Service Pack 1 (SP1).
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también



[Operación ApplyConversationAction](applyconversationaction-operation.md)


- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)

