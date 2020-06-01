---
title: FindConversationResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FindConversationResponse
api_type:
- schema
ms.assetid: a689e29d-5f3d-4deb-81ee-8b6cc60f6dea
description: El elemento FindConversationResponse define una respuesta a una solicitud de operación FindConversation.
ms.openlocfilehash: 68acc42045b91ab4b574f32ba3fd622057863015
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462643"
---
# <a name="findconversationresponse"></a>FindConversationResponse

El elemento **FindConversationResponse** define una respuesta a una solicitud de [operación FindConversation](findconversation-operation.md) . 
  
[FindConversationResponse](findconversationresponse.md)
  
```XML
<FindConversationResponse ResponseClass="">
   <Conversations/>
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
</FindConversationResponse>

```

 **FindConversationResponseMessageType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Descripción**|
|:-----|:-----|
|**ResponseClass** <br/> | Describe el estado de una respuesta de [operación de FindConversation](findconversation-operation.md) . <br/><br/>Los siguientes valores son válidos para este atributo:<br/>  <br/>-Correcto  <br/>-ADVERTENCIA  <br/>-Error  <br/> |
   
#### <a name="responseclass-attribute-values"></a>Valores del atributo ResponseClass

|**Valor**|**Descripción**|
|:-----|:-----|
|**Success** <br/> |Describe una solicitud que se ha completado.  <br/> |
|**Advertencia** <br/> | Describe una solicitud que no se ha procesado. Se puede devolver una advertencia si se produjo un error al procesar un elemento de la solicitud y no se pudieron procesar los siguientes elementos.<br/><br/> Los siguientes son ejemplos de fuentes de advertencias:  <br/><br/>-El almacén de Exchange está sin conexión durante el lote.  <br/>-Los servicios de dominio de Active Directory (AD DS) están sin conexión.  <br/>-Se movieron los buzones.  <br/>-La base de datos de mensajes (MDB) está sin conexión.  <br/>-Una contraseña ha expirado.  <br/>-Se ha superado la cuota.  <br/> |
|**Error** <br/> | Describe una solicitud que no se puede cumplir. <br/><br/>Los siguientes son ejemplos de orígenes de errores:  <br/><br/>-Atributos o elementos no válidos  <br/>-Atributos o elementos que están fuera del intervalo  <br/>-Una etiqueta desconocida  <br/>-Un atributo o elemento que no es válido en el contexto  <br/>-Un intento de acceso no autorizado por parte de cualquier cliente  <br/>-Un error del servidor en respuesta a una llamada válida del lado cliente  <br/><br/>  La información sobre el error se puede encontrar en los elementos [ResponseCode](responsecode.md) y [MessageText](messagetext.md) .  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Conversaciones](conversations-ex15websvcsotherref.md) <br/> |Contiene una matriz de conversaciones.  <br/> |
|[MessageText](messagetext.md) <br/> |Proporciona una descripción de texto del estado de la respuesta.  <br/> |
|[ResponseCode](responsecode.md) <br/> |Proporciona un código de error que identifica el error específico que ha encontrado la solicitud.  <br/> |
|[DescriptiveLinkKey](descriptivelinkkey.md) <br/> |Actualmente no se usa y está reservado para su uso en el futuro. Contiene un valor de 0.  <br/> |
|[MessageXml](messagexml.md) <br/> |Proporciona información de respuesta de error adicional.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

Ninguna.
  
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual de IIS que hospeda los servicios Web de Exchange. este elemento se introdujo en Exchange Server 2010 Service Pack 1 (SP1).
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también

- [Operación FindConversation](findconversation-operation.md)
- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)
- [Conversaciones en EWS](https://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)

