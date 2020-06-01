---
title: TaskSuggestion
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ade9ea3b-bdf1-4999-ac7d-44c6452cef36
description: El elemento TaskSuggestion contiene una sugerencia de tarea que resulta de una entidad extraída de un elemento.
ms.openlocfilehash: 49564c246596dabbf7fbacf2924eeb877698ea1a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/01/2020
ms.locfileid: "44468127"
---
# <a name="tasksuggestion"></a>TaskSuggestion

El elemento **TaskSuggestion** contiene una sugerencia de tarea que resulta de una entidad extraída de un elemento. 
  
```XML
<TaskSuggestion>
   <Position/>
   <TaskString/>
   <Assignees/>
</TaskSuggestion>
```

**TaskSuggestionType**

## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

[Posición](position.md)  |  [TaskString](taskstring.md)  |  Usuarios [asignados](assignees.md)
  
### <a name="parent-elements"></a>Elementos principales

[TaskSuggestions](tasksuggestions.md)
  
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> ||
   

