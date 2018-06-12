---
title: MailboxScope
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c9778823-f290-4827-ba19-5f391ed4f877
description: El elemento MailboxScope identifica si una búsqueda u obtención de una conversación debe abarcar el buzón principal, buzón de archivo o ambos la principal y archivar el buzón de correo.
ms.openlocfilehash: 89c9776079d686b114d6b744150f1c6df3711eab
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836293"
---
# <a name="mailboxscope"></a>MailboxScope

El elemento **MailboxScope** identifica si una búsqueda u obtención de una conversación debe abarcar el buzón principal, buzón de archivo o ambos la principal y archivar el buzón de correo. 
  
```XML
<MailboxScope> PrimaryOnly | ArchiveOnly | All </MailboxScope>
```

**MailboxSearchLocationType**

## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

[FindConversation](findconversation.md) | [GetConversationItems](getconversationitems.md) | [conversación (ConversationType)](conversation-conversationtype.md)
  
## <a name="text-value"></a>Valor de texto

El valor de texto del elemento **MailboxScope** es el ámbito de búsqueda u obtener elementos en una conversación entre ambos buzones de correo principales, archivar los buzones de correo, o ambos primaria y buzones de archivo. Un valor de texto de **PrimaryOnly** indica un ámbito que se dirige el buzón principal para un usuario. Un valor de texto de **ArchiveOnly** indica un ámbito que se dirige el buzón de archivo para un usuario. Un valor de texto de **todos los** indica un ámbito que se dirige el buzón principal y el buzón de archivo. 
  
## <a name="remarks"></a>Notas

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |falso  <br/> |
   

