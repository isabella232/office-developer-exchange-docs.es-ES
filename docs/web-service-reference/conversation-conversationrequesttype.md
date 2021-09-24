---
title: Conversation (ConversationRequestType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 0308b71c-d4ff-44a8-b9ca-d5965291ee1d
description: El elemento Conversation representa una sola conversación devuelta en una respuesta GetConversationItems.
ms.openlocfilehash: 9c7faf9c06c1476bca688e831f452e711a89f10f
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59533896"
---
# <a name="conversation-conversationrequesttype"></a>Conversation (ConversationRequestType)

El **elemento Conversation** representa una sola conversación devuelta en una respuesta **GetConversationItems.** 
  
```XML
<Conversation>
   <ConversationId/>
   <SyncState/>
</Conversation>
```

 ****
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

[ConversationId](conversationid.md)  |  [SyncState (base64Binary)](syncstate-base64binary.md)
  
### <a name="parent-elements"></a>Elementos principales

[Conversaciones](conversations-ex15websvcsotherref.md)
  
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre del esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |types.xsd  <br/> |
|Puede estar vacío  <br/> |false  <br/> |
   

