---
title: GlobalHasAttachments
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GlobalHasAttachments
api_type:
- schema
ms.assetid: 3d075e93-14bc-479d-957f-9b7873d1db39
description: El elemento GlobalHasAttachments contiene un valor que indica si al menos un elemento de conversación de un buzón tiene datos adjuntos.
ms.openlocfilehash: e314e8e5c06ca7d7820b910c05b381765e88911f
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459479"
---
# <a name="globalhasattachments"></a>GlobalHasAttachments

El elemento **GlobalHasAttachments** contiene un valor que indica si al menos un elemento de conversación de un buzón tiene datos adjuntos. 
  
[FindConversationResponse](findconversationresponse.md)
  
[Conversaciones](conversations-ex15websvcsotherref.md)
  
[Conversación (ConversationType)](conversation-conversationtype.md)
  
[GlobalHasAttachments](globalhasattachments.md)
  
```XML
<GlobalHasAttachments/>
```

 **Boolean**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Conversación (ConversationType)](conversation-conversationtype.md) <br/> |Representa una sola conversación.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor del elemento **GlobalHasAttachments** indica si al menos un elemento de la conversación de un buzón tiene datos adjuntos. Se requiere un valor de texto que representa un valor booleano. Un valor de **true** significa que la conversación tiene al menos un archivo de datos adjuntos visible. Un valor de **false** significa que la conversación no tiene datos adjuntos o solo tiene datos adjuntos ocultos. 
  
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



[Operación FindConversation](findconversation-operation.md)
  
[Operación ApplyConversationAction](applyconversationaction-operation.md)


[Conversaciones en EWS](https://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)

