---
title: FoldersToIgnore
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: b5d18516-a617-4daf-8baf-c7ce29c76f6b
description: El elemento FoldersToIgnore identifica una lista de carpetas que se omiten al obtener elementos en una conversación. Todos los elementos de conversación de las carpetas ignoradas no se devuelven en una respuesta GetConversationItems.
ms.openlocfilehash: c0102d12b24df2cadd5e307e80c5acda9a3c0589
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59528668"
---
# <a name="folderstoignore"></a>FoldersToIgnore

El **elemento FoldersToIgnore** identifica una lista de carpetas que se omiten al obtener elementos en una conversación. Todos los elementos de conversación de las carpetas ignoradas no se devuelven en una **respuesta GetConversationItems.** 
  
```XML
<FoldersToIgnore>
   <FolderId/>
   <DistinguishedFolderId/>
</FoldersToIgnore>
```

 **NonEmptyArrayOfBaseFolderIdsType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

[FolderId](folderid.md)  |  [DistinguishedFolderId](distinguishedfolderid.md)
  
### <a name="parent-elements"></a>Elementos principales

[GetConversationItems](getconversationitems.md)
  
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre del esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |false  <br/> |
   

