---
title: ManagedFolderInformation
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ManagedFolderInformation
api_type:
- schema
ms.assetid: dea980eb-8303-47fe-a380-20a8efc9ead6
description: El elemento ManagedFolderInformation contiene información sobre una carpeta personalizada administrada.
ms.openlocfilehash: ce15dcb15cccdce253494beefd2f4a2a7a0c0ad8
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44450952"
---
# <a name="managedfolderinformation"></a>ManagedFolderInformation

El elemento **ManagedFolderInformation** contiene información sobre una carpeta personalizada administrada. 
  
```xml
<ManagedFolderInformation>
   <CanDelete/>
   <CanRenameOrMove/>
   <MustDisplayComment/>
   <HasQuota/>
   <IsManagedFoldersRoot/>
   <ManagedFolderId/>
   <Comment/>
   <StorageQuota/>
   <FolderSize/>
   <HomePage/>
</ManagedFolderInformation>
```

 **ManagedFolderInformationType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[CanDelete](candelete.md) <br/> |Indica si un cliente puede eliminar una carpeta administrada.  <br/> |
|[CanRenameOrMove](canrenameormove.md) <br/> |Indica si el cliente puede cambiar el nombre o mover una carpeta administrada determinada.  <br/> |
|[MustDisplayComment](mustdisplaycomment.md) <br/> |Indica si se debe mostrar el comentario de la carpeta administrada.  <br/> |
|[HasQuota](hasquota.md) <br/> |Indica si la carpeta administrada tiene una cuota.  <br/> |
|[IsManagedFoldersRoot](ismanagedfoldersroot.md) <br/> |Indica si la carpeta administrada es la raíz de todas las carpetas administradas.  <br/> |
|[ManagedFolderId](managedfolderid.md) <br/> |Contiene el identificador de carpeta de la carpeta administrada.  <br/> |
|[Comment](comment.md) <br/> |Contiene el comentario asociado con una carpeta administrada.  <br/> |
|[StorageQuota](storagequota.md) <br/> |Describe la cuota de almacenamiento de la carpeta administrada.  <br/> |
|[FolderSize](foldersize.md) <br/> |Describe el tamaño total de todo el contenido de una carpeta administrada.  <br/> |
|[HomePage](homepage.md) <br/> |Especifica la dirección URL que será la Página principal predeterminada para la carpeta administrada.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Folder](folder.md) <br/> |Representa una carpeta en el almacén de Exchange. Las carpetas personalizadas administradas solo pueden ser subcarpetas de la carpeta denominada **carpetas administradas**.  <br/> |
|[Hubiera](calendarfolder.md) <br/> |No procede.  <br/> |
|[Hubiera](contactsfolder.md) <br/> |No procede.  <br/> |
|[SearchFolder](searchfolder.md) <br/> |No procede.  <br/> |
|[Hubiera](tasksfolder.md) <br/> |No procede.  <br/> |
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también



[Operación CreateManagedFolder](createmanagedfolder-operation.md)


- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)


[Adición de carpetas administradas](https://msdn.microsoft.com/library/846658c6-7043-40fb-8439-19f97c2a967f%28Office.15%29.aspx)

