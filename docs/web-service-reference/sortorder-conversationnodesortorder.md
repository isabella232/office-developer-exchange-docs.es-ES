---
title: SortOrder (ConversationNodeSortOrder)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f9c4295c-8089-4533-b92f-2051eae9afeb
description: El elemento SortOrder especifica el criterio de ordenación que se usan en el resultado de una solicitud de GetConversationItems.
ms.openlocfilehash: 397aead62d32e72f991af783bff02e79a6e4b0fb
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19837520"
---
# <a name="sortorder-conversationnodesortorder"></a>SortOrder (ConversationNodeSortOrder)

El elemento **SortOrder** especifica el criterio de ordenación que se usan en el resultado de una solicitud de **GetConversationItems** . 
  
```XML
<SortOrder>TreeOrderAscending | TreeOrderDescending | DateOrderAscending | DateOrderDescending</SortOrder>
```

 **ConversationNodeSortOrder**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

[GetConversationItems](getconversationitems.md)
  
## <a name="text-value"></a>Valor de texto

El valor de texto del elemento **SortOrder** es el orden en que se ordenan las conversaciones. Un valor de texto de **TreeOrderAscending** indica que las conversaciones se ordenan según el árbol de la conversación en orden ascendente. Un valor de texto de **TreeOrderDescending** indica que las conversaciones se ordenan según el árbol de la conversación en orden descendente. Un valor de texto de **DateOrderAscending** indica que las conversaciones se ordenan según la fecha de conversación en orden ascendente. Un valor de texto de **DateOrderDescending** indica que las conversaciones se ordenan según la fecha de conversación en orden descendente. 
  
## <a name="remarks"></a>Notas

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> ||
   

