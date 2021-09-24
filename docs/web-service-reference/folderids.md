---
title: FolderIds
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- FolderIds
api_type:
- schema
ms.assetid: 3ff9d15a-7220-4785-ae6b-583a7eb82005
description: El elemento FolderIds contiene una matriz de identificadores de carpeta que se usan para identificar carpetas para copiar, mover, obtener, eliminar o supervisar las notificaciones de eventos.
ms.openlocfilehash: 7c0cf46d5fdaf35ec72cf3b5750b51edc5a8bfe0
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59518368"
---
# <a name="folderids"></a>FolderIds

El **elemento FolderIds** contiene una matriz de identificadores de carpeta que se usan para identificar carpetas para copiar, mover, obtener, eliminar o supervisar las notificaciones de eventos. 
  
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

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[FolderId](folderid.md) <br/> |Contiene el identificador y la clave de cambio de una carpeta.  <br/> |
|[DistinguishedFolderId](distinguishedfolderid.md) <br/> |Identifica Microsoft Exchange Server carpetas a las que se puede hacer referencia por su nombre.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[GetFolder](getfolder.md) <br/> |Define una solicitud para obtener una carpeta del Exchange almacén.  <br/> A continuación se muestra la expresión XPath de este elemento:  `/GetFolder` <br/> |
|[DeleteFolder](deletefolder.md) <br/> |Define una solicitud para eliminar carpetas del Exchange almacén.  <br/> A continuación se muestra la expresión XPath de este elemento:  `/DeleteFolder` <br/> |
|[EmptyFolder](emptyfolder.md) <br/> |Define una solicitud para eliminar carpetas del Exchange almacén.  <br/> A continuación se muestra la expresión XPath de este elemento:  `/EmptyFolder` <br/> |
|[MoveFolder](movefolder.md) <br/> |Define una solicitud para mover una carpeta en el Exchange almacén.  <br/> A continuación se muestra la expresión XPath de este elemento:  `/MoveFolder` <br/> |
|[CopyFolder](copyfolder.md) <br/> |Define una solicitud para copiar una carpeta en el Exchange almacén.  <br/> A continuación se muestra la expresión XPath de este elemento:  `/CopyFolder` <br/> |
|[PushSubscriptionRequest](pushsubscriptionrequest.md) <br/> |Representa una suscripción a una suscripción de notificación de eventos basada en inserción.  <br/> |
|[PullSubscriptionRequest](pullsubscriptionrequest.md) <br/> |Representa una suscripción a una suscripción de notificación de eventos basada en extracción.  <br/> |
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual EWS del equipo que ejecuta Microsoft Exchange Server que tiene instalado el rol de servidor Acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages y https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes; Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Messages.xsd; Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también



[Operación GetFolder](getfolder-operation.md)
  
[Operación DeleteFolder](deletefolder-operation.md)
  
[Operación MoveFolder](movefolder-operation.md)
  
[Operación CopyFolder](copyfolder-operation.md)
  
[Operación de suscripción](subscribe-operation.md)

