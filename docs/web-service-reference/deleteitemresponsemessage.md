---
title: DeleteItemResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DeleteItemResponseMessage
api_type:
- schema
ms.assetid: c3d34c4d-8d83-4612-aa9e-66f9cc7314df
description: El elemento DeleteItemResponseMessage contiene el estado y el resultado de una única solicitud de operación DeleteItem.
ms.openlocfilehash: 1f0cc3d49bfa5fba6da32cf65df6b6718ccfbded
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764113"
---
# <a name="deleteitemresponsemessage"></a>DeleteItemResponseMessage

El elemento **DeleteItemResponseMessage** contiene el estado y el resultado de una única solicitud de [operación DeleteItem](deleteitem-operation.md) . 
  
- [DeleteItemResponse](deleteitemresponse.md) 
- [ResponseMessages](responsemessages.md)  
- [DeleteItemResponseMessage](deleteitemresponsemessage.md)
  
```xml
<DeleteItemResponseMessage>
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
</DeleteItemResponseMessage>
```

 **DeleteItemResponseMessageType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Attribute**|**Descripción**|
|:-----|:-----|
|**ResponseClass** <br/> | Describe el estado de una respuesta de [la operación DeleteItem](deleteitem-operation.md) .<br/><br/>Los siguientes valores son válidos para este atributo:<br/><br/>-Éxito  <br/>-Advertencia  <br/>-Error  <br/> |
   
#### <a name="responseclass-attribute"></a>Atributo ResponseClass

|**Valor**|**Descripción**|
|:-----|:-----|
|**Operación correcta** <br/> |Describe una solicitud que se cumplen los requisitos.  <br/> |
|**Warning** <br/> | Describe una solicitud que no se procesó. Es posible que se devuelve una advertencia si se produjo un error mientras procesaba un elemento en la solicitud y no se podrían procesar los elementos subsiguientes.<br/><br/>Los siguientes son ejemplos de fuentes de advertencias:<br/><br/>-El almacén de Exchange se desconecta durante el proceso por lotes.  <br/>-Los servicios de dominio de Active Directory (AD DS) se queda sin conexión.  <br/>-Se mueven los buzones de correo.  <br/>-La base de datos de mensajes (MDB) se queda sin conexión.  <br/>-Una contraseña ha expirado.  <br/>-Se ha excedido una cuota.  <br/> |
|**Error** <br/> | Describe una solicitud que no se cumplen los requisitos.<br/><br/>Los siguientes son ejemplos de orígenes de errores:<br/><br/>-No válida Atributos o elementos  <br/>-Los atributos o elementos fuera del intervalo  <br/>-Etiqueta desconocida  <br/>-De atributo o elemento no es válido en el contexto  <br/>-Un cliente intenta establecer el nivel de registro de error por encima del nivel máximo permitido por el administrador  <br/>-Un cliente intenta establecer el nivel de error de gravedad por debajo del nivel predeterminado que es especificado por el administrador  <br/>-Intento de acceso no autorizado por parte de cualquier cliente  <br/>-Error server-side en respuesta a una llamada de cliente válida<br/><br/>  Puede encontrar información sobre el error en los elementos [ResponseCode](responsecode.md) y [MessageText](messagetext.md) .  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[MessageText](messagetext.md) <br/> |Proporciona una descripción de texto del estado de la respuesta.  <br/> |
|[ResponseCode](responsecode.md) <br/> |Proporciona un código de error que identifica el error específico que ha encontrado la solicitud.  <br/> |
|[DescriptiveLinkKey](descriptivelinkkey.md) <br/> |Actualmente no se utiliza y está reservado para uso futuro. Contiene un valor de 0.  <br/> |
|[MessageXml](messagexml.md) <br/> |Proporciona información de la respuesta de error adicionales.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[ResponseMessages](responsemessages.md) <br/> |Contiene los mensajes de respuesta para una solicitud de servicios Web de Exchange.  <br/> |
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2010 que tenga instalado el rol de servidor de acceso de cliente.
  
### <a name="version-differences"></a>Diferencias de versión

En las versiones de Exchange a partir de compilación 15.00.0986.00, el elemento **DeleteItemResponseMessage** es del tipo **DeleteItemResponseMessageType**. En versiones anteriores, el elemento es de tipo **ResponseMessageType**.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Vea también

- [Operación DeleteItem](deleteitem-operation.md)
- [Referencia EWS para Exchange](ews-reference-for-exchange.md)
- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)
- [Eliminación de elementos (servicios Web de Exchange)](http://msdn.microsoft.com/library/9bfc39e6-d944-4eb6-8aee-cbaf1e37c67d%28Office.15%29.aspx)

