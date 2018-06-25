---
title: DeleteType
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DeleteType
api_type:
- schema
ms.assetid: 6e3136cd-9cb4-493a-aa85-9678f719002d
description: El elemento DeleteType indica cómo se eliminan los elementos en una conversación.
ms.openlocfilehash: abaa0c3d8b7001b2f42a38d1c82475edba32d2c5
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764104"
---
# <a name="deletetype"></a>DeleteType

El elemento **DeleteType** indica cómo se eliminan los elementos en una conversación. 
  
- [ApplyConversationAction](applyconversationaction.md)  
- [ConversationActions](conversationactions.md)  
- [ConversationAction](conversationaction.md)  
- [DeleteType](deletetype.md)
  
```XML
<DeleteType> HardDelete | MoveToDeletedItems | SoftDelete </DeleteType>
```

 **DisposalType**
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

El valor de texto del elemento **DeleteType** indica cómo se eliminan los elementos en una conversación. Los siguientes son los valores de texto posibles: 
  
- HardDelete - indica que los elementos en una conversación se quitan permanentemente de la base de datos de buzón de correo.
    
- MoveToDeleteItems - indica que se mueven los elementos en una conversación a la carpeta Elementos eliminados.
    
- SoftDelete - indica que se mueven los elementos en una conversación para el volcado de archivos si el volcado de archivos está habilitado.
    
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

