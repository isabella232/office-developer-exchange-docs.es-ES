---
title: SyncFolderItemsResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SyncFolderItemsResponseMessage
api_type:
- schema
ms.assetid: f58e773f-94a7-4729-90f0-ac4c71b4ba59
description: El elemento SyncFolderItemsResponseMessage contiene el estado y el resultado de una única solicitud de operación SyncFolderItems.
ms.openlocfilehash: 87de1b679fad4affa29a6dfdea72f5312b9191d5
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463044"
---
# <a name="syncfolderitemsresponsemessage"></a>SyncFolderItemsResponseMessage

El elemento **SyncFolderItemsResponseMessage** contiene el estado y el resultado de una única solicitud de [operación SyncFolderItems](syncfolderitems-operation.md) . 
  
- [SyncFolderItemsResponse](syncfolderitemsresponse.md) 
- [ResponseMessages](responsemessages.md)
- [SyncFolderItemsResponseMessage](syncfolderitemsresponsemessage.md)
  
```xml
<SyncFolderItemsResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <SyncState/>
   <IncludesLastItemInRange/>
   <Changes/>
</SyncFolderItemsResponseMessage>
```

 **SyncFolderItemsResponseMessageType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Descripción**|
|:-----|:-----|
|**ResponseClass** <br/> | Describe el estado de una respuesta de [operación de SyncFolderItems](syncfolderitems-operation.md) . <br/><br/>Los siguientes valores son válidos para este atributo: <br/> <br/>-Correcto  <br/>-ADVERTENCIA  <br/>-Error  <br/> |
   
#### <a name="responseclass-attribute"></a>Atributo ResponseClass

|**Valor**|**Descripción**|
|:-----|:-----|
|**Success** <br/> |Describe una solicitud que se ha completado.  <br/> |
|**Advertencia** <br/> | Describe una solicitud que no se ha procesado. Se puede devolver una advertencia si se produjo un error al procesar un elemento en la solicitud y no se pueden procesar los elementos siguientes. <br/><br/>Los siguientes son ejemplos de fuentes de advertencias:  <br/><br/>-El almacén de Exchange está sin conexión durante el lote.  <br/>-Los servicios de dominio de Active Directory (AD DS) están sin conexión.  <br/>-Se movieron los buzones.  <br/>-La base de datos de mensajes (MDB) está sin conexión.  <br/>-Una contraseña ha expirado.  <br/>-Se ha superado la cuota.  <br/> |
|**Error** <br/> | Describe una solicitud que no se puede cumplir. <br/><br/>Los siguientes son ejemplos de orígenes de errores:  <br/><br/>-Atributos o elementos no válidos  <br/>-Atributos o elementos que están fuera del intervalo  <br/>-Una etiqueta desconocida  <br/>-Un atributo o elemento que no es válido en el contexto  <br/>-Cualquier intento de acceso no autorizado por parte de cualquier cliente  <br/>-Cualquier error del servidor en respuesta a una llamada válida del lado cliente  <br/>  <br/>La información sobre el error se puede encontrar en los elementos [ResponseCode](responsecode.md) y [MessageText](messagetext.md) .  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[MessageText](messagetext.md) <br/> |Proporciona una descripción de texto del estado de la respuesta.  <br/> |
|[ResponseCode](responsecode.md) <br/> |Proporciona un código de error que identifica el error específico que ha encontrado la solicitud.  <br/> |
|[DescriptiveLinkKey](descriptivelinkkey.md) <br/> |Actualmente no se usa y está reservado para su uso en el futuro. Contiene el valor de 0.  <br/> |
|[MessageXml](messagexml.md) <br/> |Proporciona información de respuesta de error adicional.  <br/> |
|[SyncState](syncstate-ex15websvcsotherref.md) <br/> |Contiene una forma codificada en Base64 de los datos de sincronización que se actualizan después de cada solicitud correcta. Se usa para identificar el estado de sincronización.  <br/> |
|[IncludesLastItemInRange](includeslastiteminrange.md) <br/> |Indica si se ha incluido en la respuesta el último elemento que se va a sincronizar.  <br/> |
|[Cambios (elementos)](changes-items.md) <br/> |Contiene una matriz de secuencias de tipos de cambio que representan los tipos de diferencias entre los elementos en el cliente y los elementos en el servidor de Exchange.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[ResponseMessages](responsemessages.md) <br/> |Contiene los mensajes de respuesta de una solicitud de servicios web Exchange.  <br/> |
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también

- [Operación SyncFolderItems](syncfolderitems-operation.md)
- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)

