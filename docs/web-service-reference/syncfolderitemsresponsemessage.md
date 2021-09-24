---
title: SyncFolderItemsResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- SyncFolderItemsResponseMessage
api_type:
- schema
ms.assetid: f58e773f-94a7-4729-90f0-ac4c71b4ba59
description: El elemento SyncFolderItemsResponseMessage contiene el estado y el resultado de una única solicitud de operación SyncFolderItems.
ms.openlocfilehash: c11f896c2d9f0dec498a4e2048aa78d17da33d0e
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59531442"
---
# <a name="syncfolderitemsresponsemessage"></a>SyncFolderItemsResponseMessage

El **elemento SyncFolderItemsResponseMessage** contiene el estado y el resultado de una única [solicitud de operación SyncFolderItems.](syncfolderitems-operation.md) 
  
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
|**ResponseClass** <br/> | Describe el estado de una respuesta de [operación SyncFolderItems.](syncfolderitems-operation.md) <br/><br/>Los siguientes valores son válidos para este atributo: <br/> <br/>- Éxito  <br/>- Advertencia  <br/>- Error  <br/> |
   
#### <a name="responseclass-attribute"></a>Atributo ResponseClass

|**Valor**|**Descripción**|
|:-----|:-----|
|**Success** <br/> |Describe una solicitud que se ha cumplido.  <br/> |
|**Advertencia** <br/> | Describe una solicitud que no se ha procesado. Se puede devolver una advertencia si se produjo un error al procesar un elemento en la solicitud y los elementos posteriores no se pueden procesar. <br/><br/>A continuación se muestran ejemplos de orígenes de advertencias:  <br/><br/>- El Exchange está sin conexión durante el lote.  <br/>- Servicios de dominio de Active Directory (AD DS) está sin conexión.  <br/>- Los buzones se movieron.  <br/>- La base de datos de mensajes (MDB) está sin conexión.  <br/>- Una contraseña ha expirado.  <br/>- Se superó una cuota.  <br/> |
|**Error** <br/> | Describe una solicitud que no se puede cumplir. <br/><br/>A continuación se muestran ejemplos de orígenes de errores:  <br/><br/>- Atributos o elementos no válidos  <br/>- Atributos o elementos que están fuera del intervalo  <br/>- Una etiqueta desconocida  <br/>- Un atributo o elemento que no es válido en el contexto  <br/>- Cualquier intento de acceso no autorizado por cualquier cliente  <br/>- Cualquier error del lado servidor en respuesta a una llamada válida del lado cliente  <br/>  <br/>Encontrará información sobre el error en los [elementos ResponseCode](responsecode.md) y [MessageText.](messagetext.md)  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[MessageText](messagetext.md) <br/> |Proporciona una descripción de texto del estado de la respuesta.  <br/> |
|[ResponseCode](responsecode.md) <br/> |Proporciona un código de error que identifica el error específico que encontró la solicitud.  <br/> |
|[DescriptiveLinkKey](descriptivelinkkey.md) <br/> |Actualmente no se usa y está reservado para su uso futuro. Contiene el valor de 0.  <br/> |
|[MessageXml](messagexml.md) <br/> |Proporciona información adicional de respuesta a errores.  <br/> |
|[SyncState](syncstate-ex15websvcsotherref.md) <br/> |Contiene una forma codificada en base64 de los datos de sincronización que se actualizan después de cada solicitud correcta. Esto se usa para identificar el estado de sincronización.  <br/> |
|[IncludesLastItemInRange](includeslastiteminrange.md) <br/> |Indica si el último elemento que se va a sincronizar se ha incluido en la respuesta.  <br/> |
|[Changes (Items)](changes-items.md) <br/> |Contiene una matriz de secuencias de tipos de cambio que representan los tipos de diferencias entre los elementos del cliente y los elementos del Exchange servidor.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[ResponseMessages](responsemessages.md) <br/> |Contiene los mensajes de respuesta de una Exchange de servicios web.  <br/> |
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor Acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también

- [Operación SyncFolderItems](syncfolderitems-operation.md)
- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

