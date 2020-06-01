---
title: CreateAttachmentResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CreateAttachmentResponseMessage
api_type:
- schema
ms.assetid: b326e616-3ce0-4dcb-ba75-4ce4b9867211
description: El elemento CreateAttachmentResponseMessage contiene el estado y el resultado de una única solicitud de operación CreateAttachment.
ms.openlocfilehash: 14d8d1936b3cfd52bdb816343c86606cb8ccf76f
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458925"
---
# <a name="createattachmentresponsemessage"></a>CreateAttachmentResponseMessage

El elemento **CreateAttachmentResponseMessage** contiene el estado y el resultado de una única solicitud de [operación CreateAttachment](createattachment-operation.md) . 
  
- [CreateAttachmentResponse](createattachmentresponse.md)
- [ResponseMessages](responsemessages.md)
- [CreateAttachmentResponseMessage](createattachmentresponsemessage.md)
  
```xml
<CreateAttachmentResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <Attachments/>
</CreateAttachmentResponseMessage>
```

**AttachmentInfoResponseMessageType**

## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Descripción**|
|:-----|:-----|
|**ResponseClass** <br/> | Describe el estado de una respuesta de [operación de CreateAttachment](createattachment-operation.md) . <br/><br/>Los siguientes valores son válidos para este atributo:<br/><br/>-Correcto  <br/>-ADVERTENCIA  <br/>-Error  <br/> |
   
#### <a name="responseclass-attribute-values"></a>Valores del atributo ResponseClass

|**Valor**|**Descripción**|
|:-----|:-----|
|**Success** <br/> |Describe una solicitud que se ha completado.  <br/> |
|**Advertencia** <br/> | Describe una solicitud que no se ha procesado. Se puede devolver una advertencia si se produjo un error al procesar un elemento de la solicitud y no se pudieron procesar los siguientes elementos.<br/><br/>Los siguientes son ejemplos de fuentes de advertencias:<br/><br/>-El almacén de Exchange está sin conexión durante el lote.  <br/>-Los servicios de dominio de Active Directory (AD DS) están sin conexión.  <br/>-Se mueven los buzones.  <br/>-La base de datos de mensajes (MDB) está sin conexión.  <br/>-Una contraseña ha expirado.  <br/>-Se ha superado la cuota.  <br/> |
|**Error** <br/> | Describe una solicitud que no se puede cumplir.<br/><br/>Los siguientes son ejemplos de orígenes de errores:  <br/><br/>-Atributos o elementos no válidos  <br/>-Atributos o elementos fuera del intervalo  <br/>-Etiqueta desconocida  <br/>-Atributo o elemento no válido en el contexto  <br/>-Intento de acceso no autorizado por parte de un cliente  <br/>-Error del servidor en respuesta a una llamada válida del lado cliente<br/><br/>  La información sobre el error se puede encontrar en los elementos [ResponseCode](responsecode.md) y [MessageText](messagetext.md) .  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[MessageText](messagetext.md) <br/> |Proporciona una descripción de texto del estado de la respuesta.  <br/> |
|[ResponseCode](responsecode.md) <br/> |Proporciona un código de error que identifica el error específico que ha encontrado la solicitud.  <br/> |
|[DescriptiveLinkKey](descriptivelinkkey.md) <br/> |Actualmente no se usa y está reservado para su uso en el futuro. Contiene un valor de 0.  <br/> |
|[MessageXml](messagexml.md) <br/> |Proporciona información de respuesta de error adicional.  <br/> |
|[Datos adjuntos](attachments-ex15websvcsotherref.md) <br/> |Contiene los elementos o archivos adjuntos a un elemento en el almacén de Exchange.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[ResponseMessages](responsemessages.md) <br/> |Contiene los mensajes de respuesta de una solicitud de servicios web Exchange.  <br/> |
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2010 que tiene instalado el rol de servidor acceso de clientes.
  
> [!NOTE]
> Si se adjuntan varios datos adjuntos a un elemento en una sola acción de ida y vuelta, el atributo **RootItemChangeKey** del último mensaje de respuesta es el que representa la nueva clave de cambio del elemento que tiene los datos adjuntos. 
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también

- [Operación CreateAttachment](createattachment-operation.md) 
- [CreateAttachment](createattachment.md)
- [Referencia EWS para Exchange](ews-reference-for-exchange.md) 
- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)

