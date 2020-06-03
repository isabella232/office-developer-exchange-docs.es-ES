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
description: El elemento FolderIds contiene una matriz de identificadores de carpeta que se usan para identificar las carpetas que se van a copiar, mover, obtener, eliminar o supervisar las notificaciones de eventos.
ms.openlocfilehash: ff0476f72c7da088bd2b39f58ab560dcc82197e4
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530996"
---
# <a name="folderids"></a>FolderIds

El elemento **FolderIds** contiene una matriz de identificadores de carpeta que se usan para identificar las carpetas que se van a copiar, mover, obtener, eliminar o supervisar las notificaciones de eventos. 
  
```xml
<FolderIds>
   <FolderId/>
   <DistinguishedFolderId/>
</FolderIds>
```

 **NonEmptyArrayOfBaseFolderIdsType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[FolderId](folderid.md) <br/> |Contiene el identificador y la clave de cambio de una carpeta.  <br/> |
|[DistinguishedFolderId](distinguishedfolderid.md) <br/> |Identifica las carpetas de Microsoft Exchange Server a las que se puede hacer referencia por su nombre.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[GetFolder](getfolder.md) <br/> |Define una solicitud para obtener una carpeta del almacén de Exchange.  <br/> La siguiente es la expresión XPath a este elemento:`/GetFolder` <br/> |
|[DeleteFolder](deletefolder.md) <br/> |Define una solicitud para eliminar carpetas del almacén de Exchange.  <br/> La siguiente es la expresión XPath a este elemento:`/DeleteFolder` <br/> |
|[EmptyFolder](emptyfolder.md) <br/> |Define una solicitud para eliminar carpetas del almacén de Exchange.  <br/> La siguiente es la expresión XPath a este elemento:`/EmptyFolder` <br/> |
|[MoveFolder](movefolder.md) <br/> |Define una solicitud para mover una carpeta en el almacén de Exchange.  <br/> La siguiente es la expresión XPath a este elemento:`/MoveFolder` <br/> |
|[CopyFolder](copyfolder.md) <br/> |Define una solicitud para copiar una carpeta en el almacén de Exchange.  <br/> La siguiente es la expresión XPath a este elemento:`/CopyFolder` <br/> |
|[PushSubscriptionRequest](pushsubscriptionrequest.md) <br/> |Representa una suscripción a una suscripción de notificación de eventos basada en inserción.  <br/> |
|[PullSubscriptionRequest](pullsubscriptionrequest.md) <br/> |Representa una suscripción a una suscripción de notificación de eventos basada en extracción.  <br/> |
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server que tiene instalado el rol de servidor acceso de clientes.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages y https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes; Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Messages. xsd; Types. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también



[Operación GetFolder](getfolder-operation.md)
  
[Operación DeleteFolder](deletefolder-operation.md)
  
[Operación MoveFolder](movefolder-operation.md)
  
[Operación CopyFolder](copyfolder-operation.md)
  
[Operación subscribe](subscribe-operation.md)

