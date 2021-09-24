---
title: MailboxScope
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: c9778823-f290-4827-ba19-5f391ed4f877
description: El elemento MailboxScope identifica si una búsqueda o captura de una conversación debe abarcar el buzón principal, el buzón de archivo o el buzón principal y el buzón de archivo.
ms.openlocfilehash: 705c72ae2aefbb16599f392eb712d080668490b0
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59522883"
---
# <a name="mailboxscope"></a>MailboxScope

El **elemento MailboxScope** identifica si una búsqueda o captura de una conversación debe abarcar el buzón principal, el buzón de archivo o el buzón principal y el buzón de archivo. 
  
```XML
<MailboxScope> PrimaryOnly | ArchiveOnly | All </MailboxScope>
```

**MailboxSearchLocationType**

## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

[FindConversation](findconversation.md)  |  [GetConversationItems](getconversationitems.md)  |  [Conversación (ConversationType)](conversation-conversationtype.md)
  
## <a name="text-value"></a>Valor de texto

El valor de texto del **elemento MailboxScope** es el ámbito para buscar o obtener elementos en una conversación en buzones principales, buzones de archivo o buzones de correo principales y de archivo. Un valor de texto **de PrimaryOnly** indica un ámbito que está dirigido al buzón principal de un usuario. Un valor de texto **de ArchiveOnly** indica un ámbito que está dirigido al buzón de archivo de un usuario. Un valor de texto de **All** indica un ámbito dirigido tanto al buzón principal como al buzón de archivo. 
  
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre del esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |false  <br/> |
   

