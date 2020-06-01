---
title: SearchFilter
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1a7ee364-b7da-4197-aab2-57134537109a
description: El elemento SearchFilter contiene la cadena de consulta para filtrar los buzones que se van a devolver desde una solicitud GetSearchableMailboxes.
ms.openlocfilehash: 5bc7389ecc54dd6d1c97debdb97e6fce42517ef4
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467434"
---
# <a name="searchfilter"></a>SearchFilter

El elemento **SearchFilter** contiene la cadena de consulta para filtrar los buzones que se van a devolver desde una solicitud **GetSearchableMailboxes** . 
  
```XML
<SearchFilter></SearchFilter>
```

 **string**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

[GetSearchableMailboxes](getsearchablemailboxes.md)
  
## <a name="text-value"></a>Valor de texto

El valor de texto del elemento **SearchFilter** es una cadena de consulta para filtrar buzones para la búsqueda de detección. 
  
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
   

