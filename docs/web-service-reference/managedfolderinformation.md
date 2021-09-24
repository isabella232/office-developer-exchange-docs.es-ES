---
title: ManagedFolderInformation
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ManagedFolderInformation
api_type:
- schema
ms.assetid: dea980eb-8303-47fe-a380-20a8efc9ead6
description: El elemento ManagedFolderInformation contiene información sobre una carpeta personalizada administrada.
ms.openlocfilehash: f25daeff82b4a30574a627f290c2fcd336a38a6c
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59524801"
---
# <a name="managedfolderinformation"></a>ManagedFolderInformation

El **elemento ManagedFolderInformation** contiene información sobre una carpeta personalizada administrada. 
  
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

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[CanDelete](candelete.md) <br/> |Indica si un cliente puede eliminar una carpeta administrada.  <br/> |
|[CanRenameOrMove](canrenameormove.md) <br/> |Indica si el cliente puede cambiar el nombre o mover una carpeta administrada determinada.  <br/> |
|[MustDisplayComment](mustdisplaycomment.md) <br/> |Indica si se debe mostrar el comentario de carpeta administrada.  <br/> |
|[HasQuota](hasquota.md) <br/> |Indica si la carpeta administrada tiene una cuota.  <br/> |
|[IsManagedFoldersRoot](ismanagedfoldersroot.md) <br/> |Indica si la carpeta administrada es la raíz de todas las carpetas administradas.  <br/> |
|[ManagedFolderId](managedfolderid.md) <br/> |Contiene el identificador de carpeta de la carpeta administrada.  <br/> |
|[Comment](comment.md) <br/> |Contiene el comentario asociado a una carpeta administrada.  <br/> |
|[StorageQuota](storagequota.md) <br/> |Describe la cuota de almacenamiento de la carpeta administrada.  <br/> |
|[FolderSize](foldersize.md) <br/> |Describe el tamaño total de todo el contenido de una carpeta administrada.  <br/> |
|[HomePage](homepage.md) <br/> |Especifica la dirección URL que será la página principal predeterminada de la carpeta administrada.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Folder](folder.md) <br/> |Representa una carpeta en el Exchange almacén. Las carpetas personalizadas administradas solo pueden ser subcarpetas de la carpeta denominada **Carpetas administradas**.  <br/> |
|[CalendarFolder](calendarfolder.md) <br/> |No procede.  <br/> |
|[ContactsFolder](contactsfolder.md) <br/> |No procede.  <br/> |
|[SearchFolder](searchfolder.md) <br/> |No procede.  <br/> |
|[TasksFolder](tasksfolder.md) <br/> |No procede.  <br/> |
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor Acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre del esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también



[Operación CreateManagedFolder](createmanagedfolder-operation.md)


- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)


[Agregar carpetas administradas](https://msdn.microsoft.com/library/846658c6-7043-40fb-8439-19f97c2a967f%28Office.15%29.aspx)

