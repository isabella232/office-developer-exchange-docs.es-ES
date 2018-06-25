---
title: FindConversation
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FindConversation
api_type:
- schema
ms.assetid: 94b7083c-60cf-478b-a9af-a88f7acb30fb
description: El elemento FindConversation define una solicitud para buscar las conversaciones en un buzón de correo.
ms.openlocfilehash: 990e15f468f836d51977329c524acb439014da95
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764613"
---
# <a name="findconversation"></a>FindConversation

El elemento **FindConversation** define una solicitud para buscar las conversaciones en un buzón de correo. 
  
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

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

****

|**Attribute**|**Descripción**|
|:-----|:-----|
|Cruce seguro del  <br/> |Identifica los tipos de cruce del subárbol. Este atributo es opcional.  <br/> |
|DinámicaFiltrar  <br/> |Identifica los filtros de vista de tipos. Este atributo es opcional.  <br/> |
   
#### <a name="traversal-attribute-values"></a>Valores de atributo recorrido

****

|**Valor**|**Descripción**|
|:-----|:-----|
|Superficial  <br/> |Indica un recorrido superficial.  <br/> |
|Profunda  <br/> |Indica un recorrido profundo.  <br/> |
   
#### <a name="viewfilter-attribute-values"></a>Valores de atributo de dinámicaFiltrar

****

|**Valor**|**Descripción**|
|:-----|:-----|
|Todos  <br/> |Buscar todas las conversaciones.  <br/> |
|Marca  <br/> |Buscar conversaciones marcas.  <br/> |
|HasAttachment  <br/> |Buscar conversaciones con datos adjuntos.  <br/> |
|ToOrCcMe  <br/> |Buscar conversaciones dirigidas o cc sería a mí.  <br/> |
|Unread  <br/> |Buscar conversaciones no leídas.  <br/> |
|TaskActive  <br/> |Aquí encontrará las tareas activas.  <br/> |
|TaskOverdue  <br/> |Aquí encontrará las tareas vencidas.  <br/> |
|TaskCompleted  <br/> |Aquí encontrará las tareas completadas.  <br/> |
|NoClutter  <br/> |Solo para uso interno.  <br/> |
|Desorden  <br/> |Solo para uso interno.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[IndexedPageItemView](indexedpageitemview.md) <br/> |Describe cómo paginada conversación se devuelve información.  <br/> |
|[SeekToConditionPageItemView](seektoconditionpageitemview.md) <br/> |Especifica la condición que se usa para identificar el final de una búsqueda, el índice de inicio de una búsqueda, las entradas máximas para devolver y las instrucciones de búsqueda para una búsqueda **FindItem** o **FindConversation** .  <br/> |
|[SortOrder](sortorder.md) <br/> |Define cómo se ordenan los elementos en una solicitud de [operación FindConversation](findconversation-operation.md) . La propiedad de **Conversación: LastDeliveryTime** es la única propiedad que se admite para la ordenación cuando se usa la operación **FindConversation** .  <br/> |
|[ID (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) <br/> |Identifica la carpeta de búsqueda para las conversaciones.  <br/> |
|[MailboxScope](mailboxscope.md) <br/> |Especifica si debe abarcar el buzón principal, buzón de archivo o ambos la principal y archivar el buzón de correo, una búsqueda u obtención de una conversación.  <br/> |
|[QueryString (QueryStringType)](querystring-querystringtype.md) <br/> |Especifica una cadena de consulta de buzón de correo basada en la sintaxis de consulta avanzada (AQS).  <br/> |
|[ConversationShape](conversationshape.md) <br/> |Identifica la propiedad establecida para devolver en una respuesta de la [operación de FindConversation](findconversation-operation.md) .  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

Ninguno.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda Exchange Web Services.This elemento fue introdujo en Exchange Server 2010 Service Pack 1 (SP1).
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Vea también



[Operación de FindConversation](findconversation-operation.md)


- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)


[Conversaciones de EWS](http://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)

