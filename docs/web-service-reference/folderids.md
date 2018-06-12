---
title: FolderIds
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FolderIds
api_type:
- schema
ms.assetid: 3ff9d15a-7220-4785-ae6b-583a7eb82005
description: El elemento FolderIds contiene una matriz de identificadores de carpeta que se usa para identificar las carpetas para copiar, mover, obtener, eliminar o supervisar para las notificaciones de eventos.
ms.openlocfilehash: 911a74ca778ee988c270c16c67620a40656d82d8
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764681"
---
# <a name="folderids"></a>FolderIds

El elemento **FolderIds** contiene una matriz de identificadores de carpeta que se usa para identificar las carpetas para copiar, mover, obtener, eliminar o supervisar para las notificaciones de eventos. 
  
```xml
<FolderIds>
   <FolderId/>
   <DistinguishedFolderId/>
</FolderIds>
```

 **NonEmptyArrayOfBaseFolderIdsType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[FolderId](folderid.md) <br/> |Contiene el identificador y cambiar la clave de una carpeta.  <br/> |
|[DistinguishedFolderId](distinguishedfolderid.md) <br/> |Identifica las carpetas de Microsoft Exchange Server que se pueden hacer referencia por su nombre.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[GetFolder](getfolder.md) <br/> |Define una solicitud para obtener una carpeta desde el almacén de Exchange.  <br/> La siguiente es la expresión de XPath para este elemento:`/GetFolder` <br/> |
|[DeleteFolder](deletefolder.md) <br/> |Define una solicitud para eliminar las carpetas del almacén de Exchange.  <br/> La siguiente es la expresión de XPath para este elemento:`/DeleteFolder` <br/> |
|[EmptyFolder](emptyfolder.md) <br/> |Define una solicitud para eliminar las carpetas del almacén de Exchange.  <br/> La siguiente es la expresión de XPath para este elemento:`/EmptyFolder` <br/> |
|[MoveFolder](movefolder.md) <br/> |Define una solicitud para mover una carpeta en el almacén de Exchange.  <br/> La siguiente es la expresión de XPath para este elemento:`/MoveFolder` <br/> |
|[CopyFolder](copyfolder.md) <br/> |Define una solicitud para copiar una carpeta en el almacén de Exchange.  <br/> La siguiente es la expresión de XPath para este elemento:`/CopyFolder` <br/> |
|[PushSubscriptionRequest](pushsubscriptionrequest.md) <br/> |Representa una suscripción a una suscripción de notificación de evento basada en inserción.  <br/> |
|[PullSubscriptionRequest](pullsubscriptionrequest.md) <br/> |Representa una suscripción a una suscripción de notificación de eventos basado en la extracción.  <br/> |
   
## <a name="remarks"></a>Notas

El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server que tiene instalada la función del servidor acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages y http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de los mensajes; Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Messages.xsd; Types.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Ver también



[Operación GetFolder](getfolder-operation.md)
  
[Operación DeleteFolder](deletefolder-operation.md)
  
[Operación MoveFolder](movefolder-operation.md)
  
[Operación CopyFolder](copyfolder-operation.md)
  
[Operación de suscripción](subscribe-operation.md)

