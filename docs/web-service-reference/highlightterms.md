---
title: HighlightTerms
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: ce4a2978-fd0c-41a4-ae65-aa6f5dc9a0f9
description: El elemento HighlightTerms identifica los términos resaltados devueltos en una operación FindItem y una respuesta de operación FindConversation.
ms.openlocfilehash: 058c283ab4114f14b5bbffe20c6e953bd877f1e0
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59511547"
---
# <a name="highlightterms"></a>HighlightTerms

El **elemento HighlightTerms** identifica los términos resaltados devueltos en una **operación FindItem** y una respuesta de operación **FindConversation.** 
  
```XML
<HighlightTerms>
   <Term/>
</HighlightTerms>
```

 **ArrayOfHighlightTermsType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Término
  
### <a name="parent-elements"></a>Elementos principales

[FindConversationResponse](findconversationresponse.md)  |  [FindItemResponseMessage](finditemresponsemessage.md)
  
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
   

