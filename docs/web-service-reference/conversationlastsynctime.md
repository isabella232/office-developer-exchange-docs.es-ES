---
title: ConversationLastSyncTime
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ConversationLastSyncTime
api_type:
- schema
ms.assetid: 90f8f9e3-5fc6-4a6a-bdfb-fc91fa51f8a2
description: El elemento ConversationLastSyncTime contiene la fecha y la hora en que una conversación se sincronizó por última vez. Este elemento debe estar presente cuando se intenta eliminar todos los elementos de una conversación que se recibieron hasta la hora especificada.
ms.openlocfilehash: f7cc6e205ab9936685d7b8c1f34129b799a53021
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461432"
---
# <a name="conversationlastsynctime"></a>ConversationLastSyncTime

El elemento **ConversationLastSyncTime** contiene la fecha y la hora en que una conversación se sincronizó por última vez. Este elemento debe estar presente cuando se intenta eliminar todos los elementos de una conversación que se recibieron hasta la hora especificada. 
  
[ApplyConversationAction](applyconversationaction.md)
  
[ConversationActions](conversationactions.md)
  
[ConversationAction](conversationaction.md)
  
[ConversationLastSyncTime](conversationlastsynctime.md)
  
```XML
<ConversationLastSyncTime/>
```

 **XS: dateTime**
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

El valor de texto de **ConversationLastSyncTime** indica la última vez que se sincronizó la conversación. 
  
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



[Operación ApplyConversationAction](applyconversationaction-operation.md)


- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)

