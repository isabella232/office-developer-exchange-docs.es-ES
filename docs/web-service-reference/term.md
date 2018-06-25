---
title: Término
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1a796535-7e83-4aa8-850a-d217059050f8
description: El elemento de términos especifica un término resaltado en una respuesta FindConversation o FindItem.
ms.openlocfilehash: cef2ecd7c51b61ccff2c7261a7a612095047956c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19840641"
---
# <a name="term"></a>Término

El elemento de **términos** especifica un término resaltado en una respuesta **FindConversation** o **FindItem** . 
  
```XML
<Term>
   <Scope/>
   <Value/>
</Term>
```

 **HighlightTermType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

[Ámbito (HighlightTermType)](scope-highlighttermtype.md) | [valor](value.md)
  
### <a name="parent-elements"></a>Elementos principales

[HighlightTerms](highlightterms.md)
  
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> ||
   

