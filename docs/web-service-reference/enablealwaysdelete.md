---
title: EnableAlwaysDelete
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- EnableAlwaysDelete
api_type:
- schema
ms.assetid: 7753aec5-3f93-4aeb-a28e-8b9b42ca7f9b
description: El elemento EnableAlwaysDelete especifica una marca que permite la eliminación de todos los elementos nuevos de una conversación.
ms.openlocfilehash: 7b0704ebd7187ac06293589277aefd53f6bceaaa
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59520727"
---
# <a name="enablealwaysdelete"></a>EnableAlwaysDelete

El **elemento EnableAlwaysDelete** especifica una marca que permite la eliminación de todos los elementos nuevos de una conversación. 
  
[ApplyConversationAction](applyconversationaction.md)
  
[ConversationActions](conversationactions.md)
  
[ConversationAction](conversationaction.md)
  
[EnableAlwaysDelete](enablealwaysdelete.md)
  
```XML
<EnableAlwaysDelete/>
```

 **xs:boolean**
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

El valor de texto del **elemento EnableAlwaysDelete** es **true** para habilitar la eliminación de todos los elementos de la conversación; de lo contrario, **false**.
  
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



[Operación ApplyConversationAction](applyconversationaction-operation.md)

