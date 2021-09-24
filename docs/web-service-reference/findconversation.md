---
title: FindConversation
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- FindConversation
api_type:
- schema
ms.assetid: 94b7083c-60cf-478b-a9af-a88f7acb30fb
description: El elemento FindConversation define una solicitud para buscar conversaciones en un buzón.
ms.openlocfilehash: e48e0d9fd71dac12fe6848031b2c056ea9a913ce
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59535173"
---
# <a name="findconversation"></a>FindConversation

El **elemento FindConversation** define una solicitud para buscar conversaciones en un buzón. 
  
[FindConversation](findconversation.md)
  
```XML
<FindConversation Traversal="" ViewFilter="">
   <IndexedPageItemView/>
   <SeekToConditionPageItemView/>
   <SortOrder/>
   <ParentFolderId/>
   <MailboxScope/>
   <QueryString/>
   <ConversationShape/>
</FindConversation>
```

 **FindConversationType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

****

|**Atributo**|**Descripción**|
|:-----|:-----|
|Traversal  <br/> |Identifica los tipos de recorrido del subárdo. Este atributo es opcional.  <br/> |
|ViewFilter  <br/> |Identifica los filtros de vista de tipos. Este atributo es opcional.  <br/> |
   
#### <a name="traversal-attribute-values"></a>Valores de atributo Traversal

****

|**Valor**|**Descripción**|
|:-----|:-----|
|Superficial  <br/> |Indica un recorrido superficial.  <br/> |
|Deep  <br/> |Indica un recorrido profundo.  <br/> |
   
#### <a name="viewfilter-attribute-values"></a>Valores de atributo ViewFilter

****

|**Valor**|**Descripción**|
|:-----|:-----|
|Todo  <br/> |Buscar todas las conversaciones.  <br/> |
|Marcado  <br/> |Buscar conversaciones marcadas.  <br/> |
|HasAttachment  <br/> |Buscar conversaciones con datos adjuntos.  <br/> |
|ToOrCcMe  <br/> |Buscar conversaciones dirigidas o cc'd para mí.  <br/> |
|No leídos  <br/> |Buscar conversaciones no leídas.  <br/> |
|TaskActive  <br/> |Buscar tareas activas.  <br/> |
|TaskOverdue  <br/> |Buscar tareas vencidas.  <br/> |
|TaskCompleted  <br/> |Buscar tareas completadas.  <br/> |
|NoClutter  <br/> |Únicamente para uso interno.  <br/> |
|Otros correos  <br/> |Únicamente para uso interno.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[IndexedPageItemView](indexedpageitemview.md) <br/> |Describe cómo se devuelve la información de conversación paginada.  <br/> |
|[SeekToConditionPageItemView](seektoconditionpageitemview.md) <br/> |Especifica la condición que se usa para identificar el final de una búsqueda, el índice inicial de una búsqueda, las entradas máximas que se devolverán y las direcciones de búsqueda de una búsqueda **FindItem** o **FindConversation.**  <br/> |
|[SortOrder](sortorder.md) <br/> |Define cómo se ordenan los elementos en una [solicitud de operación FindConversation.](findconversation-operation.md) La **propiedad conversation:LastDeliveryTime** es la única que se admite para ordenar cuando se usa la operación **FindConversation.**  <br/> |
|[ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) <br/> |Identifica la carpeta para buscar conversaciones.  <br/> |
|[MailboxScope](mailboxscope.md) <br/> |Especifica si una búsqueda o captura de una conversación debe abarcar el buzón principal, el buzón de archivo o el buzón principal y el buzón de archivo.  <br/> |
|[QueryString (QueryStringType)](querystring-querystringtype.md) <br/> |Especifica una cadena de consulta de buzón de correo basada en la sintaxis de consulta avanzada (AQS).  <br/> |
|[ConversationShape](conversationshape.md) <br/> |Identifica la propiedad establecida para devolver en una respuesta de operación [FindConversation.](findconversation-operation.md)  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

Ninguno.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual de IIS que hospeda Exchange Web Services.Este elemento se introdujo en Exchange Server 2010 Service Pack 1 (SP1).
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también



[Operación FindConversation](findconversation-operation.md)


- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)


[Conversaciones en EWS](https://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)

