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
ms.openlocfilehash: 5754ea7540fa6daac8cd725386ca213d5bf05c8e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764615"
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

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Attribute**|**Descripción**|
|:-----|:-----|
|**ResponseClass** <br/> | Describe el estado de una respuesta de [la operación FindConversation](findconversation-operation.md) . <br/><br/>Los siguientes valores son válidos para este atributo:<br/>  <br/>-Éxito  <br/>-Advertencia  <br/>-Error  <br/> |
   
#### <a name="responseclass-attribute-values"></a>Valores de atributo de ResponseClass

|**Valor**|**Descripción**|
|:-----|:-----|
|**Operación correcta** <br/> |Describe una solicitud que se cumplen los requisitos.  <br/> |
|**Warning** <br/> | Describe una solicitud que no se procesó. Es posible que se devuelve una advertencia si se produjo un error mientras procesaba un elemento en la solicitud y no se podrían procesar los elementos subsiguientes.<br/><br/> Los siguientes son ejemplos de fuentes de advertencias:  <br/><br/>-El almacén de Exchange está sin conexión durante el proceso por lotes.  <br/>-Los servicios de dominio de Active Directory (AD DS) está sin conexión.  <br/>-Buzones se han movido.  <br/>-La base de datos de mensajes (MDB) está sin conexión.  <br/>-Una contraseña ha expirado.  <br/>-Se superó una cuota.  <br/> |
|**Error** <br/> | Describe una solicitud que no se cumplen los requisitos. <br/><br/>Los siguientes son ejemplos de orígenes de errores:  <br/><br/>-No válida Atributos o elementos  <br/>-Los atributos o elementos que están fuera del intervalo  <br/>-Una etiqueta desconocida  <br/>-Un atributo o un elemento que no es válido en el contexto  <br/>-Un intento de acceso no autorizado por cualquier cliente  <br/>-Un error del lado del servidor en respuesta a una llamada de cliente válida  <br/><br/>  Puede encontrar información sobre el error en los elementos [ResponseCode](responsecode.md) y [MessageText](messagetext.md) .  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[Conversaciones](conversations-ex15websvcsotherref.md) <br/> |Contiene una matriz de las conversaciones.  <br/> |
|[MessageText](messagetext.md) <br/> |Proporciona una descripción de texto del estado de la respuesta.  <br/> |
|[ResponseCode](responsecode.md) <br/> |Proporciona un código de error que identifica el error específico que ha encontrado la solicitud.  <br/> |
|[DescriptiveLinkKey](descriptivelinkkey.md) <br/> |Actualmente no se utiliza y está reservado para uso futuro. Contiene un valor de 0.  <br/> |
|[MessageXml](messagexml.md) <br/> |Proporciona información de la respuesta de error adicionales.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

Ninguno.
  
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda Exchange Web Services.This elemento fue introdujo en Exchange Server 2010 Service Pack 1 (SP1).
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Vea también

- [Operación de FindConversation](findconversation-operation.md)
- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)
- [Conversaciones de EWS](http://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)

