---
title: Acción (ConversationActionTypeType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Action
api_type:
- schema
ms.assetid: 8bbc12f2-76c5-4fda-828f-56b2086a0454
description: El elemento de acción contiene la acción para llevar a cabo en la conversación especificada por el elemento ConversationId.
ms.openlocfilehash: b468eeaf0c2509bfa53cbd83f497f0bae20a7f68
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763381"
---
# <a name="action-conversationactiontypetype"></a>Acción (ConversationActionTypeType)

El elemento de **acción** contiene la acción para llevar a cabo en la conversación especificada por el elemento [ConversationId](conversationid.md) . 
  
- [ApplyConversationAction](applyconversationaction.md)
  
- [ConversationActions](conversationactions.md)
  
- [ConversationAction](conversationaction.md)
  
- [Acción (ConversationActionTypeType)](action-conversationactiontypetype.md)
  
```XML
<Action> AlwaysCategorize | AlwaysDelete | AlwaysMove | Delete | Move | Copy | SetReadState </Action>
```

 **ConversationActionTypeType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[ConversationAction](conversationaction.md) <br/> |Contiene una única acción que se aplicará a una conversación único.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto del elemento **Action** indica la acción que se realizará en una conversación. Los siguientes son los valores de texto posibles y las acciones correspondientes: 
  
- **AlwaysCategorize** - los elementos actuales y los elementos nuevos en la conversación se establecerá automáticamente con las categorías identificadas en el elemento de [categorías](categories-ex15websvcsotherref.md) . 
    
- **AlwaysDelete** - los elementos actuales y los elementos nuevos en la conversación se eliminarán automáticamente. El modo de eliminación está establecido por el elemento [DeleteType](deletetype.md) . 
    
- **AlwaysMove** - los elementos actuales y los elementos nuevos en la conversación se moverán automáticamente a la carpeta identificada por el elemento [DestinationFolderId](destinationfolderid.md) . 
    
- **Eliminar** - los elementos de la conversación actuales se eliminará. No se eliminarán los elementos subsiguientes de la conversación. El modo de eliminación está establecido por el elemento [DeleteType](deletetype.md) . 
    
- **Mover** - los elementos actualmente en la conversación se moverán a la carpeta identificada por el elemento [DestinationFolderId](destinationfolderid.md) . No se moverán los elementos subsiguientes de la conversación. 
    
- **Copia** : los elementos de la conversación actuales se copiarán a la carpeta identificada por el elemento [DestinationFolderId](destinationfolderid.md) . No se copiarán los elementos subsiguientes de la conversación. 
    
- **SetReadState** - los elementos de la conversación actuales tendrán a su estado de lectura a establecer. El estado de lectura está establecido por el elemento [estáleído](isread.md) . 
    
- **Marca** - los elementos de la conversación actuales tendrá una marca establecida como definidas por el elemento de [marca](flag.md) . 
    
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda Exchange Web Services.This elemento fue introdujo en Exchange Server 2010 Service Pack 1 (SP1).
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Vea también

- [Operación ApplyConversationAction](applyconversationaction-operation.md)
- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

