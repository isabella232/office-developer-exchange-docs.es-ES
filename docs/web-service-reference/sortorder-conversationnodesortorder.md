---
title: SortOrder (ConversationNodeSortOrder)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: f9c4295c-8089-4533-b92f-2051eae9afeb
description: El elemento SortOrder especifica el criterio de ordenación usado para el resultado de una solicitud GetConversationItems.
ms.openlocfilehash: 0091968f1359b0cf744525139b5c6a8cf1687d81
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59544678"
---
# <a name="sortorder-conversationnodesortorder"></a>SortOrder (ConversationNodeSortOrder)

El **elemento SortOrder** especifica el criterio de ordenación usado para el resultado de una **solicitud GetConversationItems.** 
  
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

El valor de texto del **elemento SortOrder** es el orden en que se ordenaron las conversaciones. Un valor de texto **de TreeOrderAscending** indica que las conversaciones se ordenan según el árbol de conversación en orden ascendente. Un valor de texto **de TreeOrderDescending** indica que las conversaciones se ordenan según el árbol de conversación en orden descendente. Un valor de texto **de DateOrderAscending** indica que las conversaciones se ordenan según la fecha de conversación en orden ascendente. Un valor de texto **de DateOrderDescending** indica que las conversaciones se ordenan según la fecha de conversación en orden descendente. 
  
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre del esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> ||
   

