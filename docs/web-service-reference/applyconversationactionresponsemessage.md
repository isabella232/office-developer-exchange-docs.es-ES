---
title: ApplyConversationActionResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ApplyConversationActionResponseMessage
api_type:
- schema
ms.assetid: a09edc89-7f2f-4846-a3a5-06694c97b9f6
description: El elemento ApplyConversationActionResponseMessage contiene el estado y los resultados de una solicitud de operación ApplyConversationAction.
ms.openlocfilehash: 81378c822a473d969035f46f34ffca8939d7059d
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59522050"
---
# <a name="applyconversationactionresponsemessage"></a>ApplyConversationActionResponseMessage

El **elemento ApplyConversationActionResponseMessage** contiene el estado y los resultados de una solicitud de [operación ApplyConversationAction.](applyconversationaction-operation.md)  
  
- [ApplyConversationActionResponse](applyconversationactionresponse.md)
- [ResponseMessages](responsemessages.md)
- [ApplyConversationActionResponseMessage](applyconversationactionresponsemessage.md)
  
```XML
<ApplyConversationActionResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
</ApplyConversationActionResponseMessage>
```

 **ApplyConversationActionResponseMessageType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Descripción**|
|:-----|:-----|
|**ResponseClass** <br/> | Describe el estado de la respuesta.<br/><br/>Los siguientes valores son válidos para este atributo:<ul><li>Correcto</li><li>Advertencia</li><li>Error</li></ul> |
   
#### <a name="responseclass-attribute-values"></a>Valores de atributo ResponseClass

|**Valor**|**Descripción**|
|:-----|:-----|
|**Success** <br/> |Describe una solicitud que se ha cumplido.  <br/> |
|**Advertencia** <br/> | Describe una solicitud que no se ha procesado. Se puede devolver una advertencia si se produjo un error mientras se procesaba un elemento de la solicitud y no se pudieron procesar los elementos posteriores.<br/><br/>A continuación se muestran ejemplos de orígenes de advertencias:<ul><li>El Exchange está sin conexión durante el lote.</li><li>Servicios de dominio de Active Directory (AD DS) está sin conexión.</li><li>Los buzones se movieron.</li><li>La base de datos de mensajes (MDB) está sin conexión.</li><li>Una contraseña ha expirado.</li><li>Se ha excedido una cuota.</li></ul> |
|**Error** <br/> | Describe una solicitud que no se puede cumplir.<br/><br/>A continuación se muestran ejemplos de orígenes de errores:  <ul><li>Atributos o elementos no válidos</li><li>Atributos o elementos que están fuera del intervalo</li><li>Una etiqueta desconocida  </li><li>Un atributo o elemento que no es válido en el contexto</li><li>Un intento de acceso no autorizado por cualquier cliente</li><li>Un error del lado servidor en respuesta a una llamada válida del lado cliente</li></ul>Encontrará información sobre el error en los [elementos ResponseCode](responsecode.md) y [MessageText.](messagetext.md)  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[MessageText](messagetext.md) <br/> |Proporciona una descripción de texto del estado de la respuesta.  <br/> |
|[ResponseCode](responsecode.md) <br/> |Proporciona un código de error que identifica el error específico que encontró la solicitud.  <br/> |
|[DescriptiveLinkKey](descriptivelinkkey.md) <br/> |Actualmente no se usa y está reservado para uso futuro. Este elemento contiene un valor de 0.  <br/> |
|[MessageXml](messagexml.md) <br/> |Proporciona información adicional de respuesta a errores.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[ResponseMessages](responsemessages.md) <br/> |Contiene los mensajes de respuesta de una Exchange de servicios web.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual de IIS que hospeda Exchange Web Services.Este elemento se introdujo en Exchange Server 2010 Service Pack 1 (SP1).
  
### <a name="version-differences"></a>Diferencias de versión

En versiones de Exchange a partir de la compilación 15.00.0986.00, el elemento **ApplyConversationActionResponseMessage** es del tipo **ApplyConversationActionResponseMessageType**. En versiones anteriores, el elemento es de tipo **ResponseMessageType**.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensaje  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también

- [Operación ApplyConversationAction](applyconversationaction-operation.md)
- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

