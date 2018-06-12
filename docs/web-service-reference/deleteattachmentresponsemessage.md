---
title: DeleteAttachmentResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DeleteAttachmentResponseMessage
api_type:
- schema
ms.assetid: 1edb085f-1674-48e5-8ec3-42351adeac7d
description: El elemento DeleteAttachmentResponseMessage contiene el estado y el resultado de una única solicitud de operación DeleteAttachment.
ms.openlocfilehash: 387e998a393c23f416cc5ad8d6c4a7ad4c92ebc7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764087"
---
# <a name="deleteattachmentresponsemessage"></a>DeleteAttachmentResponseMessage

El elemento **DeleteAttachmentResponseMessage** contiene el estado y el resultado de una única solicitud de [operación DeleteAttachment](deleteattachment-operation.md) . 
  
- [DeleteAttachmentResponse](deleteattachmentresponse.md)  
- [ResponseMessages](responsemessages.md)  
- [DeleteAttachmentResponseMessage](deleteattachmentresponsemessage.md)
  
```xml
<DeleteAttachmentResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <RootItemId/>
</DeleteAttachmentResponseMessage>
```

**DeleteAttachmentResponseMessageType**

## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Attribute**|**Descripción**|
|:-----|:-----|
|**ResponseClass** <br/> | Describe el estado de una respuesta de [la operación DeleteAttachment](deleteattachment-operation.md) .<br/><br/>Los siguientes valores son válidos para este atributo:<br/><br/>-Éxito  <br/>-Advertencia  <br/>-Error  <br/> |
   
#### <a name="responseclass-attribute-values"></a>Valores de atributo de ResponseClass

|**Valor**|**Descripción**|
|:-----|:-----|
|**Operación correcta** <br/> |Describe una solicitud que se cumplen los requisitos.  <br/> |
|**Warning** <br/> | Describe una solicitud que no se procesó. Es posible que se devuelve una advertencia si se produjo un error mientras procesaba un elemento en la solicitud y no se podrían procesar los elementos subsiguientes.<br/><br/>Los siguientes son ejemplos de fuentes de advertencias:<br/><br/>-El almacén de Exchange está sin conexión durante el proceso por lotes.  <br/>-Los servicios de dominio de Active Directory (AD DS) está sin conexión.  <br/>-Se mueven los buzones de correo.  <br/>-La base de datos de mensajes (MDB) está sin conexión.  <br/>-Una contraseña ha expirado.  <br/>-Se ha excedido una cuota.  <br/> |
|**Error** <br/> | Describe una solicitud que no se cumplen los requisitos.<br/><br/>Los siguientes son ejemplos de orígenes de errores:<br/><br/>-No válida Atributos o elementos  <br/>-Los atributos o elementos fuera del intervalo  <br/>-Etiqueta desconocida  <br/>-De atributo o elemento no es válido en el contexto  <br/>-Intento de acceso no autorizado por parte de cualquier cliente  <br/>-Error server-side en respuesta a una llamada de cliente válida<br/><br/>  Puede encontrar información sobre el error en los elementos [ResponseCode](responsecode.md) y [MessageText](messagetext.md) .  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[MessageText](messagetext.md) <br/> |Proporciona una descripción de texto del estado de la respuesta.  <br/> |
|[ResponseCode](responsecode.md) <br/> |Proporciona un código de error que identifica el error específico que ha encontrado la solicitud.  <br/> |
|[DescriptiveLinkKey](descriptivelinkkey.md) <br/> |Actualmente no se utiliza y está reservado para uso futuro. Contiene un valor de 0.  <br/> |
|[MessageXml](messagexml.md) <br/> |Proporciona información de la respuesta de error adicionales.  <br/> |
|[RootItemId](rootitemid.md) <br/> |Identifica el elemento primario de un archivo adjunto eliminado.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[ResponseMessages](responsemessages.md) <br/> |Contiene los mensajes de respuesta para una solicitud de servicios Web de Exchange.  <br/> |
   
## <a name="remarks"></a>Notas

El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Exchange Server con la función de servidor de acceso de cliente instalada.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Ver también

- [DeleteAttachment](deleteattachment.md) 
- [Operación DeleteAttachment](deleteattachment-operation.md)
- [Referencia EWS para Exchange](ews-reference-for-exchange.md) 
- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

