---
title: GetConversationItems
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 4f7bcd0f-140c-4cbc-a5ed-daeffded1df1
description: El elemento GetConversationItems define una solicitud para obtener un conjunto de elementos que están relacionados por la que se está en la misma conversación.
ms.openlocfilehash: 9be300318a07173e4a8e11e5a6ca78b885de1199
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764780"
---
# <a name="getconversationitems"></a>GetConversationItems

El elemento **GetConversationItems** define una solicitud para obtener un conjunto de elementos que están relacionados por la que se está en la misma conversación. 
  
```XML
<GetConversationItems>
   <ItemShape/>
   <FoldersToIgnore/>
   <MaxItemsToReturn/>
   <SortOrder/>
   <MailboxScope/>
   <Conversations/>
</GetConversationItems>
```

 **GetConversationItemsType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

[ItemShape](itemshape.md) | [FoldersToIgnore](folderstoignore.md) | [MaxItemsToReturn](maxitemstoreturn.md) | [SortOrder (ConversationNodeSortOrder)](sortorder-conversationnodesortorder.md) | [MailboxScope](mailboxscope.md) | [conversaciones](conversations-ex15websvcsotherref.md)
  
### <a name="parent-elements"></a>Elementos principales

Ninguno.
  
## <a name="remarks"></a>Observaciones

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |falso  <br/> |
   

