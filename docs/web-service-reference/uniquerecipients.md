---
title: UniqueRecipients
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- UniqueRecipients
api_type:
- schema
ms.assetid: 9f46ed05-5370-46ee-80f5-83f97224c76e
description: El elemento UniqueRecipients contiene la lista de destinatarios de una conversación en una carpeta determinada. Este elemento es de solo lectura.
ms.openlocfilehash: d611efa7d632a07e14740bd211c4bfa796173a68
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59510795"
---
# <a name="uniquerecipients"></a>UniqueRecipients

El **elemento UniqueRecipients** contiene la lista de destinatarios de una conversación en una carpeta determinada. Este elemento es de solo lectura. 
  
[FindConversationResponse](findconversationresponse.md)
  
[Conversaciones](conversations-ex15websvcsotherref.md)
  
[Conversation (ConversationType)](conversation-conversationtype.md)
  
[UniqueRecipients](uniquerecipients.md)
  
```XML
<UniqueRecpients>
   <String/>
</UniqueRecpients>
```

 **ArrayOfStringsType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[String](string.md) <br/> |Representa un destinatario único de una conversación. Este elemento es de solo lectura.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Conversation (ConversationType)](conversation-conversationtype.md) <br/> |Representa una sola conversación.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual de IIS que hospeda Exchange Web Services.Este elemento se introdujo en Exchange Server 2010 Service Pack 1 (SP1).
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre del esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también



[Operación FindConversation](findconversation-operation.md)


[Conversaciones en EWS](https://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)

