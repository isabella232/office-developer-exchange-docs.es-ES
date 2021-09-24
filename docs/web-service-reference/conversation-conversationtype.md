---
title: Conversation (ConversationType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Conversation
api_type:
- schema
ms.assetid: 59d014cd-5886-49ea-8d36-ba5de7e675de
description: El elemento Conversation representa una sola conversación.
ms.openlocfilehash: 7ce75fad17589f4d9a3ca52bcb2041eb1d1f4d2e
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59515960"
---
# <a name="conversation-conversationtype"></a>Conversation (ConversationType)

El **elemento Conversation** representa una sola conversación. 
  
[FindConversationResponse](findconversationresponse.md)
  
[Conversaciones](conversations-ex15websvcsotherref.md)
  
[Conversation (ConversationType)](conversation-conversationtype.md)
  
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

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[ConversationId](conversationid.md) <br/> |Representa el identificador de una conversación.  <br/> |
|[ConversationTopic](conversationtopic.md) <br/> |Representa el tema de conversación. Este elemento es de solo lectura.  <br/> |
|[UniqueRecipients](uniquerecipients.md) <br/> |Contiene la lista de destinatarios de una conversación agregada desde una carpeta determinada. Este elemento es de solo lectura.  <br/> |
|[GlobalUniqueRecipients](globaluniquerecipients.md) <br/> |Contiene la lista de destinatarios de una conversación agregada en un buzón. Este elemento es de solo lectura.  <br/> |
|[UniqueUnreadSenders](uniqueunreadsenders.md) <br/> |Contiene una lista de todas las personas que han enviado mensajes que actualmente no están leídos en esta conversación en la carpeta actual. Este elemento es de solo lectura.  <br/> |
|[GlobalUniqueUnreadSenders](globaluniqueunreadsenders.md) <br/> |Contiene una lista de todas las personas que han enviado mensajes que actualmente no están leídos en esta conversación en todas las carpetas del buzón.  <br/> |
|[UniqueSenders](uniquesenders.md) <br/> |Contiene una lista de todos los remitentes de elementos de conversación de la carpeta actual. Este elemento es de solo lectura.  <br/> |
|[GlobalUniqueSenders](globaluniquesenders.md) <br/> |Contiene una lista de todos los remitentes de elementos de conversación en el buzón.  <br/> |
|[LastDeliveryTime](lastdeliverytime.md) <br/> |Contiene la hora de entrega del mensaje que se recibió por última vez en esta conversación en la carpeta actual.  <br/> |
|[GlobalLastDeliveryTime](globallastdeliverytime.md) <br/> |Contiene el tiempo de entrega del mensaje que se recibió por última vez en esta conversación en todas las carpetas del buzón.  <br/> |
|[Categories](categories-ex15websvcsotherref.md) <br/> |Contiene una colección de cadenas que identifican las categorías que se aplican a todos los elementos de conversación de la carpeta actual.  <br/> |
|[GlobalCategories](globalcategories.md) <br/> |Contiene la lista de categorías de todos los elementos de conversación de un buzón.  <br/> |
|[FlagStatus](flagstatus.md) <br/> |Contiene el estado de la marca agregada para los elementos de conversación de la carpeta actual.  <br/> |
|[GlobalFlagStatus](globalflagstatus.md) <br/> |Contiene el estado de la marca agregada para todos los elementos de conversación de un buzón.  <br/> |
|[HasAttachments](hasattachments.md) <br/> |Contiene un valor que indica si al menos un elemento de conversación de la carpeta actual tiene datos adjuntos.  <br/> |
|[GlobalHasAttachments](globalhasattachments.md) <br/> |Contiene un valor que indica si al menos un elemento de conversación de un buzón tiene datos adjuntos.  <br/> |
|[MessageCount](messagecount.md) <br/> |Contiene el número total de elementos de conversación de la carpeta actual.  <br/> |
|[GlobalMessageCount](globalmessagecount.md) <br/> |Contiene el número total de elementos de conversación en el buzón.  <br/> |
|[UnreadCount](unreadcount.md) <br/> |Contiene el recuento de elementos de conversación no leídos dentro de una carpeta.  <br/> |
|[GlobalUnreadCount](globalunreadcount.md) <br/> |Contiene un recuento de todos los elementos de conversación no leídos en el buzón.  <br/> |
|[Tamaño](size.md) <br/> |Contiene el tamaño de conversación calculado a partir del tamaño de todos los elementos de conversación de la carpeta actual.  <br/> |
|[GlobalSize](globalsize.md) <br/> |Contiene el tamaño de la conversación calculada a partir del tamaño de todos los elementos de conversación del buzón.  <br/> |
|[ItemClasses (ArrayOfItemClassType)](itemclasses-arrayofitemclasstype.md) <br/> |Contiene una lista de clases de elementos que representa todas las clases de elementos de los elementos de conversación de la carpeta actual.  <br/> |
|[GlobalItemClasses](globalitemclasses.md) <br/> |Contiene una lista de clases de elementos que representa todas las clases de elementos de los elementos de conversación de un buzón.  <br/> |
|[Importance](importance.md) <br/> |Contiene la importancia agregada para todos los elementos de conversación de la carpeta actual.  <br/> |
|[GlobalImportance](globalimportance.md) <br/> |Contiene la importancia agregada para todos los elementos de conversación de un buzón.  <br/> |
|[ItemIds](itemids.md) <br/> |Contiene la colección de identificadores de elementos para todos los elementos de conversación de la carpeta actual.  <br/> |
|[GlobalItemIds](globalitemids.md) <br/> |Contiene la colección de identificadores de elementos para todos los elementos de conversación de un buzón.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Conversaciones](conversations-ex15websvcsotherref.md) <br/> |Contiene una matriz de conversaciones que se devuelven en la **respuesta FindConversation.**  <br/> |
   
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual de IIS que hospeda Exchange Web Services.Este elemento se introdujo en Exchange Server 2010 Service Pack 1 (SP1).
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre del esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también



[Operación FindConversation](findconversation-operation.md)
  
[Operación ApplyConversationAction](applyconversationaction-operation.md)


[Conversaciones en EWS](https://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)

