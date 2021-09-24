---
title: GetFolderResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- GetFolderResponseMessage
api_type:
- schema
ms.assetid: 51359863-d110-4c12-b89f-aba5e3e40c1d
description: El elemento GetFolderResponseMessage contiene el estado y el resultado de una única solicitud de operación GetFolder.
ms.openlocfilehash: 29d982ef5cde6344cefb6cb5050c29f567defffe
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59520559"
---
# <a name="getfolderresponsemessage"></a>GetFolderResponseMessage

El **elemento GetFolderResponseMessage** contiene el estado y el resultado de una única [solicitud de operación GetFolder.](getfolder-operation.md) 
  
- [GetFolderResponse](getfolderresponse.md) 
- [ResponseMessages](responsemessages.md)
- [GetFolderResponseMessage](getfolderresponsemessage.md)
  
```xml
<GetFolderResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <Folders/>
</GetFolderResponseMessage>
```

 **FolderInfoResponseMessageType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Descripción**|
|:-----|:-----|
|**ResponseClass** <br/> | Describe el estado de una respuesta de [operación GetFolder.](getfolder-operation.md) <br/><br/>Los siguientes valores son válidos para este atributo:<br/>  <br/>- Éxito  <br/>- Advertencia  <br/>- Error  <br/> |
   
#### <a name="responseclass-attribute"></a>Atributo ResponseClass

|**Valor**|**Descripción**|
|:-----|:-----|
|**Success** <br/> |Describe una solicitud que se ha cumplido.  <br/> |
|**Advertencia** <br/> | Describe una solicitud que no se ha procesado. Se puede devolver una advertencia si se produjo un error mientras se procesaba un elemento de la solicitud y no se pudieron procesar los elementos posteriores. <br/><br/>A continuación se muestran ejemplos de orígenes de advertencias:  <br/><br/>- El Exchange está sin conexión durante el lote.  <br/>- Servicios de dominio de Active Directory (AD DS) está sin conexión.  <br/>- Los buzones se mueven.  <br/>- La base de datos de mensajes (MDB) está sin conexión.  <br/>- Una contraseña ha expirado.  <br/>- Se supera una cuota.  <br/> |
|**Error** <br/> | Describe una solicitud que no se puede cumplir. <br/><br/>A continuación se muestran ejemplos de orígenes de errores:  <br/><br/>- Atributos o elementos no válidos  <br/>- Atributos o elementos fuera del intervalo  <br/>- Etiqueta desconocida  <br/>- Atributo o elemento no válido en el contexto  <br/>- Intento de acceso no autorizado por cualquier cliente  <br/>- Error del lado servidor en respuesta a una llamada válida del lado cliente  <br/><br/>  Encontrará información sobre el error en los [elementos ResponseCode](responsecode.md) y [MessageText.](messagetext.md)  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[MessageText](messagetext.md) <br/> |Proporciona una descripción de texto del estado de la respuesta.  <br/> |
|[ResponseCode](responsecode.md) <br/> |Proporciona un código de error que identifica el error específico que encontró la solicitud.  <br/> |
|[DescriptiveLinkKey](descriptivelinkkey.md) <br/> |Actualmente no se usa y está reservado para su uso futuro. Contiene un valor de 0.  <br/> |
|[MessageXml](messagexml.md) <br/> |Proporciona información adicional de respuesta a errores.  <br/> |
|[Folders](folders-ex15websvcsotherref.md) <br/> |Contiene una matriz de carpetas que se usan en las operaciones de carpeta.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[ResponseMessages](responsemessages.md) <br/> |Contiene los mensajes de respuesta de una Exchange de servicios web.  <br/> |
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual EWS del equipo que ejecuta Microsoft Exchange Server 2010 que tiene instalado el rol de servidor Acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también

- [GetFolder](getfolder.md)
- [GetFolderResponse](getfolderresponse.md) 
- [Operación GetFolder](getfolder-operation.md)

