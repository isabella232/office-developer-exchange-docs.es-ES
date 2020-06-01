---
title: UniqueUnreadSenders
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UniqueUnreadSenders
api_type:
- schema
ms.assetid: eb7d1274-ce2e-4ef8-b47f-e911174aab0c
description: El elemento UniqueUnreadSenders contiene una lista de todas las personas que han enviado mensajes que actualmente no están leídos en esta conversación en la carpeta actual. Este elemento es de sólo lectura.
ms.openlocfilehash: 0e45362e88be4930b8bc2f641c1fb00cc63c0605
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458855"
---
# <a name="uniqueunreadsenders"></a>UniqueUnreadSenders

El elemento **UniqueUnreadSenders** contiene una lista de todas las personas que han enviado mensajes que actualmente no están leídos en esta conversación en la carpeta actual. Este elemento es de sólo lectura. 
  
[FindConversationResponse](findconversationresponse.md)
  
[Conversaciones](conversations-ex15websvcsotherref.md)
  
[Conversación (ConversationType)](conversation-conversationtype.md)
  
[UniqueUnreadSenders](uniqueunreadsenders.md)
  
```XML
<UniqueUnreadSenders>
   <String/>
</UniqueUnreadSenders>
```

 **ArrayOfStringsType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[String](string.md) <br/> |Contiene un remitente de una sola conversación.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Conversación (ConversationType)](conversation-conversationtype.md) <br/> |Representa una sola conversación.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Ninguno.
  
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

