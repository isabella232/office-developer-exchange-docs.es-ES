---
title: GlobalLastDeliveryTime
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GlobalLastDeliveryTime
api_type:
- schema
ms.assetid: a88dada9-c527-43a7-b2d3-31aad330def9
description: El elemento GlobalLastDeliveryTime contiene la hora de entrega del mensaje que se recibió por última vez en esta conversación en todas las carpetas del buzón.
ms.openlocfilehash: b6d4d7c1d51c206e44973a717d25df4066845ada
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459415"
---
# <a name="globallastdeliverytime"></a>GlobalLastDeliveryTime

El elemento **GlobalLastDeliveryTime** contiene la hora de entrega del mensaje que se recibió por última vez en esta conversación en todas las carpetas del buzón. 
  
[FindConversationResponse](findconversationresponse.md)
  
[Conversaciones](conversations-ex15websvcsotherref.md)
  
[Conversación (ConversationType)](conversation-conversationtype.md)
  
[GlobalLastDeliveryTime](globallastdeliverytime.md)
  
```XML
<GlobalLastDeliveryTime/>
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
|[Conversación (ConversationType)](conversation-conversationtype.md) <br/> |Representa una sola conversación.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto del elemento **GlobalLastDeliveryTime** es la fecha y la hora del mensaje que se recibió por última vez en esta conversación en todas las carpetas del buzón. 
  
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2010 Service Pack 1 (SP1). El esquema que describe este elemento se encuentra en el directorio virtual de IIS que hospeda los servicios Web de Exchange.
  
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

