---
title: SearchItemKind
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 89513c26-b751-4619-a300-0ed8f55b0102
description: El elemento SearchItemKind indica el tipo de elementos que se buscan para una operación FindMailboxStatisticsByKeyword.
ms.openlocfilehash: 93803d181f32d88c30ab0fa9a72bb92f22907dde
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59510864"
---
# <a name="searchitemkind"></a>SearchItemKind

El **elemento SearchItemKind** indica el tipo de elementos que se buscan para una **operación FindMailboxStatisticsByKeyword.** 
  
```XML
<SearchItemKind>Email | Meetings | Tasks | Notes | Docs | Journals | Contacts | Im | Voicemail | Faxes | Posts | Rssfeeds</SearchItemKind>
```

 **SearchItemKindType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

[MessageTypes](messagetypes.md)
  
## <a name="text-value"></a>Valor de texto

El valor de texto del **elemento SearchItemKind** es el tipo de elemento en el que se buscan palabras clave. La siguiente lista contiene los valores de texto que se pueden usar en el **elemento SearchItemKind.** 
  
- **Correo** electrónico: indica que se buscan palabras clave en los mensajes de correo electrónico. 
    
- **Reuniones:** indica que se buscan palabras clave en las reuniones. 
    
- **Tareas:** indica que se buscan palabras clave en las tareas. 
    
- **Notas:** indica que se buscan palabras clave en las notas. 
    
- **Docs:** indica que se buscan palabras clave en los documentos. 
    
- **Diarios:** indica que se buscan palabras clave en los diarios. 
    
- **Contactos:** indica que se buscan palabras clave en los contactos. 
    
- **Im:** indica que se buscan palabras clave en los mensajes instantáneos. 
    
- **Correo** de voz: indica que se buscan palabras clave en los correos de voz. 
    
- **Faxes:** indica que se buscan palabras clave en los faxes. 
    
- **Posts:** indica que se buscan palabras clave en las publicaciones. 
    
- **Rssfeeds:** indica que se buscan palabras clave en fuentes RSS. 
    
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
   

