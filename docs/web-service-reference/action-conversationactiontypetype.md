---
title: Action (ConversationActionTypeType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Action
api_type:
- schema
ms.assetid: 8bbc12f2-76c5-4fda-828f-56b2086a0454
description: El elemento Action contiene la acción que se debe realizar en la conversación especificada por el elemento ConversationId.
ms.openlocfilehash: e75d9d5df75894d1de9831b0022269e7ace4fa63
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59514896"
---
# <a name="action-conversationactiontypetype"></a>Action (ConversationActionTypeType)

El **elemento Action** contiene la acción que se debe realizar en la conversación especificada por el elemento [ConversationId.](conversationid.md) 
  
- [ApplyConversationAction](applyconversationaction.md)
  
- [ConversationActions](conversationactions.md)
  
- [ConversationAction](conversationaction.md)
  
- [Action (ConversationActionTypeType)](action-conversationactiontypetype.md)
  
```XML
<Action> AlwaysCategorize | AlwaysDelete | AlwaysMove | Delete | Move | Copy | SetReadState </Action>
```

 **ConversationActionTypeType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[ConversationAction](conversationaction.md) <br/> |Contiene una sola acción que se aplicará a una sola conversación.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto del **elemento Action** indica qué acción se realizará en una conversación. Los siguientes son los valores de texto posibles y las acciones correspondientes: 
  
- **AlwaysCategorize:** los elementos actuales y los nuevos elementos de la conversación se establecerán automáticamente con las categorías identificadas en el [elemento Categories.](categories-ex15websvcsotherref.md) 
    
- **AlwaysDelete:** los elementos actuales y los nuevos elementos de la conversación se eliminarán automáticamente. El modo de eliminación se establece mediante [el elemento DeleteType.](deletetype.md) 
    
- **AlwaysMove:** los elementos actuales y los nuevos elementos de la conversación se moverán automáticamente a la carpeta identificada por el [elemento DestinationFolderId.](destinationfolderid.md) 
    
- **Eliminar:** se eliminarán los elementos actuales de la conversación. Los elementos posteriores de la conversación no se eliminarán. El modo de eliminación se establece mediante [el elemento DeleteType.](deletetype.md) 
    
- **Move:** los elementos actuales de la conversación se moverán a la carpeta identificada por el [elemento DestinationFolderId.](destinationfolderid.md) Los elementos posteriores de la conversación no se mueven. 
    
- **Copiar:** los elementos actuales de la conversación se copiarán en la carpeta identificada por el [elemento DestinationFolderId.](destinationfolderid.md) Los elementos posteriores de la conversación no se copiarán. 
    
- **SetReadState:** los elementos actuales de la conversación tendrán su estado de lectura establecido. El estado de lectura se establece mediante el [elemento IsRead.](isread.md) 
    
- **Flag:** los elementos actuales de la conversación tendrán una marca definida por el [elemento Flag.](flag.md) 
    
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
- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

