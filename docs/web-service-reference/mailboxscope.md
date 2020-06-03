---
title: MailboxScope
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c9778823-f290-4827-ba19-5f391ed4f877
description: El elemento MailboxScope identifica si una búsqueda o búsqueda para una conversación debe abarcar el buzón principal, el buzón de archivo o bien el buzón de archivo y el principal.
ms.openlocfilehash: 92823c06d4fe186917c3cfb532eda821bd6a95a7
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44455376"
---
# <a name="mailboxscope"></a>MailboxScope

El elemento **MailboxScope** identifica si una búsqueda o búsqueda para una conversación debe abarcar el buzón principal, el buzón de archivo o bien el buzón de archivo y el principal. 
  
```XML
<MailboxScope> PrimaryOnly | ArchiveOnly | All </MailboxScope>
```

**MailboxSearchLocationType**

## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

[FindConversation](findconversation.md)  |  [GetConversationItems](getconversationitems.md)  |  [Conversación (ConversationType)](conversation-conversationtype.md)
  
## <a name="text-value"></a>Valor de texto

El valor de texto del elemento **MailboxScope** es el ámbito para buscar u obtener elementos en una conversación en buzones de correo principales, buzones de correo de archivo o tanto en buzones de correo principales como de archivo. Un valor de texto de **PrimaryOnly** indica un ámbito que tiene como destino el buzón principal de un usuario. Un valor de texto de **ArchiveOnly** indica un ámbito que tiene como destino el buzón de archivo de un usuario. Un valor de texto de **All** indica un ámbito que tiene como destino el buzón principal y el buzón de archivo. 
  
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages. xsd  <br/> |
|Puede estar vacío  <br/> |false  <br/> |
   

