---
title: SortOrder (ConversationNodeSortOrder)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f9c4295c-8089-4533-b92f-2051eae9afeb
description: El elemento SortOrder especifica el criterio de ordenación usado para el resultado de una solicitud GetConversationItems.
ms.openlocfilehash: 69d362b9f769749bcc9692825b64ff486e8b60a0
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530968"
---
# <a name="sortorder-conversationnodesortorder"></a>SortOrder (ConversationNodeSortOrder)

El elemento **SortOrder** especifica el criterio de ordenación usado para el resultado de una solicitud **GetConversationItems** . 
  
```XML
<SortOrder>TreeOrderAscending | TreeOrderDescending | DateOrderAscending | DateOrderDescending</SortOrder>
```

 **ConversationNodeSortOrder**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

[GetConversationItems](getconversationitems.md)
  
## <a name="text-value"></a>Valor de texto

El valor de texto del elemento **SortOrder** es el orden en el que se ordenan las conversaciones. Un valor de texto de **TreeOrderAscending** indica que las conversaciones se ordenan de acuerdo con el árbol de conversaciones en orden ascendente. Un valor de texto de **TreeOrderDescending** indica que las conversaciones se ordenan de acuerdo con el árbol de conversación en orden descendente. Un valor de texto de **DateOrderAscending** indica que las conversaciones se ordenan en función de la fecha de la conversación en orden ascendente. Un valor de texto de **DateOrderDescending** indica que las conversaciones se ordenan según la fecha de la conversación en orden descendente. 
  
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages. xsd  <br/> |
|Puede estar vacío  <br/> ||
   

