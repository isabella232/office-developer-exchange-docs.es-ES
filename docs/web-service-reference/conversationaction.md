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
description: El elemento ConversationAction contiene una sola acción que se aplicará a una conversación único.
ms.openlocfilehash: 45cd6df3aba94062bd5aa0ddf9367e8cf118dc6b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763869"
---
# <a name="conversationaction"></a>ConversationAction

El elemento **ConversationAction** contiene una sola acción que se aplicará a una conversación único. 
  
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

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[Acción (ConversationActionTypeType)](action-conversationactiontypetype.md) <br/> |Contiene la acción para llevar a cabo en la conversación especificada por el elemento [ConversationId](conversationid.md) . Este elemento debe estar presente.  <br/> |
|[ConversationId](conversationid.md) <br/> |Contiene el identificador de la conversación que se va a tener la acción especificada por el elemento de [acción (ConversationActionTypeType)](action-conversationactiontypetype.md) aplicado a los elementos de la conversación. Este elemento debe estar presente.  <br/> |
|[ContextFolderId](contextfolderid.md) <br/> |Indica la carpeta que está destinada a las acciones que utilizan carpetas. Este elemento debe estar presente al copiar, eliminar, mover y establecer el estado de lectura en los elementos de una conversación en una carpeta de destino.  <br/> |
|[ConversationLastSyncTime](conversationlastsynctime.md) <br/> |Contiene la fecha y hora en que se sincronizaron por última vez una conversación. Este elemento debe estar presente al intentar eliminar todos los elementos de una conversación que se han recibido hasta el momento especificado.  <br/> |
|[ProcessRightAway](processrightaway.md) <br/> |Indica si la respuesta se envía tan pronto como la acción inicia el procesamiento en el servidor o si la respuesta se ha enviado una vez completada la acción. Este elemento debe estar presente para la respuesta que se envíen asincrónica a la acción solicitada.  <br/> |
|[DestinationFolderId](destinationfolderid.md) <br/> |Indica la carpeta de destino para copiar y mover las acciones.  <br/> |
|[Categories](categories-ex15websvcsotherref.md) <br/> |Contiene una colección de cadenas que identifican las categorías a la que pertenecen los elementos en una conversación.  <br/> |
|[EnableAlwaysDelete](enablealwaysdelete.md) <br/> |Especifica una marca que habilita la eliminación de todos los elementos nuevos en una conversación.  <br/> |
|[Estáleído](isread.md) <br/> |Indica si se ha leído un mensaje.  <br/> |
|[DeleteType](deletetype.md) <br/> |Indica cómo se eliminan los elementos en una conversación.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[ConversationActions](conversationactions.md) <br/> |Contiene una colección de las conversaciones y las acciones que se debe aplicar a ellos.  <br/> |
   
## <a name="text-value"></a>Valor de texto

**Valores de texto de elemento ConversationAction**

|**Valor**|**Descripción**|
|:-----|:-----|
|AlwaysCategorize  <br/> |Clasificar siempre la conversación.  <br/> |
|AlwaysDelete  <br/> |Eliminar siempre la conversación.  <br/> |
|AlwaysMove  <br/> |Mover siempre la conversación.  <br/> |
|Eliminar  <br/> |Eliminación de la conversación.  <br/> |
|Mover  <br/> |Mover la conversación.  <br/> |
|Copiar  <br/> |Copie la conversación.  <br/> |
|SetReadState  <br/> |Establecer el estado de la conversación.  <br/> |
|SetRetentionPolicy  <br/> |Establecer la directiva de retención para la conversación.  <br/> |
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda Exchange Web Services.This elemento fue introdujo en Exchange Server 2010 Service Pack 1 (SP1).
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Vea también



[Operación ApplyConversationAction](applyconversationaction-operation.md)


- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

