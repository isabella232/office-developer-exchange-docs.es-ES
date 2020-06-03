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
description: El elemento Action contiene la acción que se realizará en la conversación especificada por el elemento ConversationId.
ms.openlocfilehash: f97b04b98cdc29bee9aff5fa1fc6f37400b8314c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44527547"
---
# <a name="action-conversationactiontypetype"></a>Acción (ConversationActionTypeType)

El elemento **Action** contiene la acción que se realizará en la conversación especificada por el elemento [ConversationId](conversationid.md) . 
  
- [ApplyConversationAction](applyconversationaction.md)
  
- [ConversationActions](conversationactions.md)
  
- [ConversationAction](conversationaction.md)
  
- [Acción (ConversationActionTypeType)](action-conversationactiontypetype.md)
  
```XML
<Action> AlwaysCategorize | AlwaysDelete | AlwaysMove | Delete | Move | Copy | SetReadState </Action>
```

 **ConversationActionTypeType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[ConversationAction](conversationaction.md) <br/> |Contiene una sola acción que se aplicará a una única conversación.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto del elemento **Action** indica la acción que se realizará en una conversación. A continuación se muestran los valores de texto posibles y las acciones correspondientes: 
  
- **AlwaysCategorize** : los elementos actuales y los nuevos elementos de la conversación se establecerán automáticamente con las categorías identificadas en el elemento [Categories](categories-ex15websvcsotherref.md) . 
    
- **AlwaysDelete** : los elementos actuales y los nuevos elementos de la conversación se eliminarán automáticamente. El elemento [DeleteType](deletetype.md) establece el modo de eliminación. 
    
- **AlwaysMove** : los elementos actuales y los nuevos elementos de la conversación se moverán automáticamente a la carpeta identificada por el elemento [DestinationFolderId](destinationfolderid.md) . 
    
- **Eliminar** : se eliminarán los elementos actuales de la conversación. Los siguientes elementos de la conversación no se eliminarán. El elemento [DeleteType](deletetype.md) establece el modo de eliminación. 
    
- **Move** : los elementos actuales de la conversación se moverán a la carpeta identificada por el elemento [DestinationFolderId](destinationfolderid.md) . Los siguientes elementos de la conversación no se moverán. 
    
- **Copy** : los elementos actuales de la conversación se copiarán en la carpeta identificada por el elemento [DestinationFolderId](destinationfolderid.md) . No se copiarán los siguientes elementos de la conversación. 
    
- **SetReadState** : los elementos actuales de la conversación tendrán establecido el estado de lectura. El estado de lectura se establece mediante el elemento [IsRead](isread.md) . 
    
- **Marca** : los elementos actuales de la conversación tendrán un indicador establecido como definido por el elemento [Flag](flag.md) . 
    
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual de IIS que hospeda los servicios Web de Exchange. este elemento se introdujo en Exchange Server 2010 Service Pack 1 (SP1).
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también

- [Operación ApplyConversationAction](applyconversationaction-operation.md)
- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)

