---
title: Término
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 1a796535-7e83-4aa8-850a-d217059050f8
description: El elemento Term especifica un término resaltado en una respuesta FindConversation o FindItem.
ms.openlocfilehash: 12aba499ebfcad392a4e72b29a8cb3522a4f964f
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59522541"
---
# <a name="term"></a>Término

El **elemento Term** especifica un término resaltado en una respuesta **FindConversation** o **FindItem.** 
  
```XML
<Term>
   <Scope/>
   <Value/>
</Term>
```

 **HighlightTermType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

[Ámbito (HighlightTermType)](scope-highlighttermtype.md)  |  [Valor](value.md)
  
### <a name="parent-elements"></a>Elementos principales

[HighlightTerms](highlightterms.md)
  
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre del esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> ||
   

