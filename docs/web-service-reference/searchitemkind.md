---
title: SearchItemKind
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 89513c26-b751-4619-a300-0ed8f55b0102
description: El elemento SearchItemKind indica el tipo de elementos que se buscan en una operación de FindMailboxStatisticsByKeyword.
ms.openlocfilehash: e0625ac169c3083702494c094da15d38d220fe67
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44464003"
---
# <a name="searchitemkind"></a>SearchItemKind

El elemento **SearchItemKind** indica el tipo de elementos que se buscan en una operación de **FindMailboxStatisticsByKeyword** . 
  
```XML
<SearchItemKind>Email | Meetings | Tasks | Notes | Docs | Journals | Contacts | Im | Voicemail | Faxes | Posts | Rssfeeds</SearchItemKind>
```

 **SearchItemKindType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

[MessageTypes](messagetypes.md)
  
## <a name="text-value"></a>Valor de texto

El valor de texto del elemento **SearchItemKind** es el tipo de elemento en el que se buscan palabras clave. La lista siguiente contiene los valores de texto que se pueden usar en el elemento **SearchItemKind** . 
  
- **Email** -indica que se buscan palabras clave en los mensajes de correo electrónico. 
    
- **Reuniones** : indica que se buscan palabras clave en las reuniones. 
    
- **Tareas** : indica que se buscan palabras clave en las tareas. 
    
- **Notas** : indica que se buscan palabras clave en las notas. 
    
- **Docs** : indica que se buscan palabras clave en los documentos. 
    
- **Diarios** : indica que se buscan palabras clave en los diarios. 
    
- **Contacts** : indica que se buscan palabras clave en los contactos. 
    
- **Mi** : indica que se buscan palabras clave en los mensajes instantáneos. 
    
- Correo **de voz: indica** que se buscan palabras clave en los correos de voz. 
    
- **Faxes** : indica que se buscan palabras clave en los faxes. 
    
- **Postes** : indica que se buscan palabras clave en las publicaciones. 
    
- **RSSFeeds** : indica que se buscan palabras clave en las fuentes RSS. 
    
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
   

