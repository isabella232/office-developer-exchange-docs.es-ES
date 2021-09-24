---
title: ContextFolderId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ContextFolderId
api_type:
- schema
ms.assetid: 48de92aa-e124-42b5-89bc-cdce5e93d78b
description: El elemento ContextFolderId indica la carpeta destinada a las acciones que usan carpetas. Este elemento debe estar presente al copiar, eliminar, mover y establecer el estado de lectura en los elementos de conversación de una carpeta de destino.
ms.openlocfilehash: f9b1a5d140bbdaf91b2feee724101be3884f6c99
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59518676"
---
# <a name="contextfolderid"></a>ContextFolderId

El **elemento ContextFolderId** indica la carpeta destinada a las acciones que usan carpetas. Este elemento debe estar presente al copiar, eliminar, mover y establecer el estado de lectura en los elementos de conversación de una carpeta de destino. 
  
- [ApplyConversationAction](applyconversationaction.md) 
- [ConversationActions](conversationactions.md)
- [ConversationAction](conversationaction.md)
- [ContextFolderId](contextfolderid.md)
  
```XML
<ContextFolderId>
   <FolderId/>
</ContextFolderId>
```

```XML
<ContextFolderId>
   <DistinguishedFolderId/>
</ContextFolderId>
```


**TargetFolderIdType**

## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[FolderId](folderid.md) <br/> |Contiene el identificador y la clave de cambio de la carpeta de contexto.  <br/> |
|[DistinguishedFolderId](distinguishedfolderid.md) <br/> |Identifica las carpetas a las que se puede hacer referencia por su nombre.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[ConversationAction](conversationaction.md) <br/> |Contiene una sola acción que se aplicará a una sola conversación.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual de IIS que hospeda Exchange Web Services.Este elemento se introdujo en Exchange Server 2010 Service Pack 1 (SP1).
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también

- [Operación ApplyConversationAction](applyconversationaction-operation.md)

