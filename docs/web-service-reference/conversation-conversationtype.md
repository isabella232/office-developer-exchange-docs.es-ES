---
title: Conversación (ConversationType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Conversation
api_type:
- schema
ms.assetid: 59d014cd-5886-49ea-8d36-ba5de7e675de
description: El elemento de conversación representa una sola conversación.
ms.openlocfilehash: e1ae055d6a77fc5a9b483341830b978e0c1a5b5a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763870"
---
# <a name="conversation-conversationtype"></a>Conversación (ConversationType)

El elemento de **conversación** representa una sola conversación. 
  
[FindConversationResponse](findconversationresponse.md)
  
[Conversaciones](conversations-ex15websvcsotherref.md)
  
[Conversación (ConversationType)](conversation-conversationtype.md)
  
```XML
<Conversation>
   <ConversationId/>
   <ConversationTopic/>
   <UniqueRecipients/>
   <GlobalUniqueRecipients/>
   <UniqueUnreadSenders/>
   <GlobalUniqueUnreadSenders/>
   <UniqueSenders/>
   <GlobalUniqueSenders/>
   <LastDeliveryTime/>
   <GlobalLastDeliveryTime/>
   <Categories/>
   <GlobalCategories/>
   <FlagStatus/>
   <GlobalFlagStatus/>
   <HasAttachments/>
   <GlobalHasAttachments/>
   <MessageCount/>
   <GlobalMessageCount/>
   <UnreadCount/>
   <GlobalUnreadCount/>
   <Size/>   <GlobalSize/>
   <ItemClasses/>
   <GlobalItemClasses/>
   <Importance/>
   <GlobalImportance/>
   <ItemIds/>
   <GlobalItemIds/>
</Conversation>
```

 **ConversationType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[ConversationId](conversationid.md) <br/> |Representa el identificador de una conversación.  <br/> |
|[ConversationTopic](conversationtopic.md) <br/> |Representa el tema de conversación. Este elemento es de sólo lectura.  <br/> |
|[UniqueRecipients](uniquerecipients.md) <br/> |Contiene la lista de destinatarios de una conversación de agregados de una carpeta determinada. Este elemento es de sólo lectura.  <br/> |
|[GlobalUniqueRecipients](globaluniquerecipients.md) <br/> |Contiene la lista de destinatarios de una conversación agregada a través de un buzón de correo. Este elemento es de sólo lectura.  <br/> |
|[UniqueUnreadSenders](uniqueunreadsenders.md) <br/> |Contiene una lista de todas las personas que han enviado los mensajes que están actualmente no leídos en esta conversación en la carpeta actual. Este elemento es de sólo lectura.  <br/> |
|[GlobalUniqueUnreadSenders](globaluniqueunreadsenders.md) <br/> |Contiene una lista de todas las personas que han enviado los mensajes que están actualmente no leídos en esta conversación a través de todas las carpetas del buzón de correo.  <br/> |
|[UniqueSenders](uniquesenders.md) <br/> |Contiene una lista de todos los remitentes de los elementos de una conversación en la carpeta actual. Este elemento es de sólo lectura.  <br/> |
|[GlobalUniqueSenders](globaluniquesenders.md) <br/> |Contiene una lista de todos los remitentes de los elementos de la conversación en el buzón de correo.  <br/> |
|[LastDeliveryTime](lastdeliverytime.md) <br/> |Contiene la hora de entrega del mensaje que se recibió por última vez en esta conversación en la carpeta actual.  <br/> |
|[GlobalLastDeliveryTime](globallastdeliverytime.md) <br/> |Contiene la hora de entrega del mensaje que se recibió por última vez en esta conversación a través de todas las carpetas del buzón de correo.  <br/> |
|[Categories](categories-ex15websvcsotherref.md) <br/> |Contiene una colección de cadenas que identifican las categorías que se aplican a todos los elementos de una conversación en la carpeta actual.  <br/> |
|[GlobalCategories](globalcategories.md) <br/> |Contiene la lista de categorías para todos los elementos de la conversación en un buzón de correo.  <br/> |
|[FlagStatus](flagstatus.md) <br/> |Contiene el estado del indicador agregados por los elementos de conversación en la carpeta actual.  <br/> |
|[GlobalFlagStatus](globalflagstatus.md) <br/> |Contiene el estado del indicador agregada para todos los elementos de la conversación en un buzón de correo.  <br/> |
|[HasAttachments](hasattachments.md) <br/> |Contiene un valor que indica si el elemento de al menos una conversación en la carpeta actual tiene datos adjuntos.  <br/> |
|[GlobalHasAttachments](globalhasattachments.md) <br/> |Contiene un valor que indica si el elemento de al menos una conversación en un buzón tiene datos adjuntos.  <br/> |
|[MessageCount](messagecount.md) <br/> |Contiene el número total de elementos de una conversación en la carpeta actual.  <br/> |
|[GlobalMessageCount](globalmessagecount.md) <br/> |Contiene el número total de elementos de la conversación en el buzón de correo.  <br/> |
|[UnreadCount](unreadcount.md) <br/> |Contiene el recuento de elementos no leídos conversación dentro de una carpeta.  <br/> |
|[GlobalUnreadCount](globalunreadcount.md) <br/> |Contiene un recuento de todos los elementos no leídos de conversación en el buzón de correo.  <br/> |
|[Size](size.md) <br/> |Contiene el tamaño de conversación que se calcula a partir del tamaño de todos los elementos de una conversación en la carpeta actual.  <br/> |
|[GlobalSize](globalsize.md) <br/> |Contiene el tamaño de la conversación que se calcula a partir del tamaño de todos los elementos de la conversación en el buzón de correo.  <br/> |
|[ItemClasses (ArrayOfItemClassType)](itemclasses-arrayofitemclasstype.md) <br/> |Contiene una lista de las clases de elementos que representa todas las clases de elemento de los elementos de conversación en la carpeta actual.  <br/> |
|[GlobalItemClasses](globalitemclasses.md) <br/> |Contiene una lista de las clases de elementos que representa todas las clases de elemento de los elementos de la conversación en un buzón de correo.  <br/> |
|[Importancia](importance.md) <br/> |Contiene la importancia agregada para todos los elementos de una conversación en la carpeta actual.  <br/> |
|[GlobalImportance](globalimportance.md) <br/> |Contiene la importancia agregada para todos los elementos de la conversación en un buzón de correo.  <br/> |
|[ItemId](itemids.md) <br/> |Contiene la colección de identificadores de elemento para todos los elementos de una conversación en la carpeta actual.  <br/> |
|[GlobalItemIds](globalitemids.md) <br/> |Contiene la colección de identificadores de elemento para todos los elementos de la conversación en un buzón de correo.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[Conversaciones](conversations-ex15websvcsotherref.md) <br/> |Contiene una matriz de las conversaciones que se devuelven en la respuesta de **FindConversation** .  <br/> |
   
## <a name="text-value"></a>Valor de texto

Ninguno.
  
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



[Operación de FindConversation](findconversation-operation.md)
  
[Operación ApplyConversationAction](applyconversationaction-operation.md)


[Conversaciones de EWS](http://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)

