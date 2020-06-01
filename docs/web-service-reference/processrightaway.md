---
title: ProcessRightAway
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ProcessRightAway
api_type:
- schema
ms.assetid: f6bba68b-ae4f-41c1-b3e7-c8a31cdb1b0c
description: El elemento ProcessRightAway indica si la respuesta se envía en cuanto la acción comienza a procesarse en el servidor o si la respuesta se envía una vez completada la acción. Este elemento debe estar presente para que la respuesta se envíe asincrónica a la acción solicitada.
ms.openlocfilehash: 58d2b926c48db5e7395df64e1f8ee9d6a8f0e73c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44434074"
---
# <a name="processrightaway"></a>ProcessRightAway

El elemento **ProcessRightAway** indica si la respuesta se envía en cuanto la acción comienza a procesarse en el servidor o si la respuesta se envía una vez completada la acción. Este elemento debe estar presente para que la respuesta se envíe asincrónica a la acción solicitada. 
  
[ApplyConversationAction](applyconversationaction.md)
  
[ConversationActions](conversationactions.md)
  
[ConversationAction](conversationaction.md)
  
[ProcessRightAway](processrightaway.md)
  
```XML
<ProcessRightAway/>
```

 **XS: Boolean**
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

Un valor de texto de **true** indica que la respuesta se envía en cuanto la acción comienza el procesamiento en el servidor. Un valor de texto de **false** indica que la respuesta se envía una vez completada la acción. 
  
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

