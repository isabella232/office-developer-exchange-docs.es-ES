---
title: SearchItemKind
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 89513c26-b751-4619-a300-0ed8f55b0102
description: El elemento SearchItemKind indica el tipo de elementos que se buscan para una operación de FindMailboxStatisticsByKeyword.
ms.openlocfilehash: 1c099fc49ec882c1672b265ff0e3aa2c71c5f95b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19837298"
---
# <a name="searchitemkind"></a>SearchItemKind

El elemento **SearchItemKind** indica el tipo de elementos que se buscan para una operación de **FindMailboxStatisticsByKeyword** . 
  
```XML
<SearchItemKind>Email | Meetings | Tasks | Notes | Docs | Journals | Contacts | Im | Voicemail | Faxes | Posts | Rssfeeds</SearchItemKind>
```

 **SearchItemKindType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

[MessageTypes](messagetypes.md)
  
## <a name="text-value"></a>Valor de texto

El valor de texto del elemento **SearchItemKind** es el tipo de elemento que se va a buscar palabras clave. En la lista siguiente contiene los valores de texto que se pueden usar en el elemento **SearchItemKind** . 
  
- **Correo electrónico** - indica que los mensajes de correo electrónico se buscan las palabras clave. 
    
- **Las reuniones** , indica que las reuniones se buscan las palabras clave. 
    
- **Tareas** - indica que las tareas se buscan las palabras clave. 
    
- **Notas** - indica que se buscarán palabras clave. 
    
- **Documentos** - indica que se buscan documentos para palabras clave. 
    
- **Diarios** - indica que se buscan diarios para palabras clave. 
    
- **Contactos** - indica que los contactos se buscan las palabras clave. 
    
- **Mensajería instantánea** - indica que los mensajes instantáneos se buscan las palabras clave. 
    
- **Correo de voz** - indica que los correos de voz se buscan las palabras clave. 
    
- **Faxes** - indica que los faxes se buscan las palabras clave. 
    
- **Entradas de** - indica que se desea buscar entradas de palabras clave. 
    
- **Rssfeeds** - indica que se buscan las fuentes RSS para palabras clave. 
    
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
   

