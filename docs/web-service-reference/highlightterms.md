---
title: HighlightTerms
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ce4a2978-fd0c-41a4-ae65-aa6f5dc9a0f9
description: El elemento HighlightTerms identifica los términos resaltados que se devuelven en una operación FindItem y una respuesta de operación FindConversation.
ms.openlocfilehash: c55ffc010dc0cfb09403433aaf8a0809a26f71a3
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457637"
---
# <a name="highlightterms"></a>HighlightTerms

El elemento **HighlightTerms** identifica los términos resaltados que se devuelven en una operación **FindItem** y una respuesta de operación **FindConversation** . 
  
```XML
<HighlightTerms>
   <Term/>
</HighlightTerms>
```

 **ArrayOfHighlightTermsType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Term
  
### <a name="parent-elements"></a>Elementos principales

[FindConversationResponse](findconversationresponse.md)  |  [FindItemResponseMessage](finditemresponsemessage.md)
  
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
   

