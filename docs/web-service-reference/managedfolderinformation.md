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
description: El elemento ManagedFolderInformation contiene información acerca de una carpeta personalizada administrada.
ms.openlocfilehash: ef46e2e0db440de2a8acae8316ce98d11bd6710e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836341"
---
# <a name="managedfolderinformation"></a>ManagedFolderInformation

El elemento **ManagedFolderInformation** contiene información acerca de una carpeta personalizada administrada. 
  
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

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[CanDelete](candelete.md) <br/> |Indica si se puede eliminar una carpeta administrada por un cliente.  <br/> |
|[CanRenameOrMove](canrenameormove.md) <br/> |Indica si una determinada carpeta administrada se puede cambiar el nombre o movida por el cliente.  <br/> |
|[MustDisplayComment](mustdisplaycomment.md) <br/> |Indica si se debe mostrar el comentario de la carpeta administrada.  <br/> |
|[HasQuota](hasquota.md) <br/> |Indica si la carpeta administrada tiene una cuota.  <br/> |
|[IsManagedFoldersRoot](ismanagedfoldersroot.md) <br/> |Indica si la carpeta administrada es la raíz de todas las carpetas administradas.  <br/> |
|[ManagedFolderId](managedfolderid.md) <br/> |Contiene el identificador de la carpeta de la carpeta administrada.  <br/> |
|[Comment](comment.md) <br/> |Contiene el comentario que está asociado a una carpeta administrada.  <br/> |
|[StorageQuota](storagequota.md) <br/> |Describe la cuota de almacenamiento para la carpeta administrada.  <br/> |
|[FolderSize](foldersize.md) <br/> |Describe el tamaño total de todo el contenido de una carpeta administrada.  <br/> |
|[Página principal](homepage.md) <br/> |Especifica la dirección URL que será la página principal predeterminada para la carpeta administrada.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[Folder](folder.md) <br/> |Representa una carpeta en el almacén de Exchange. Las carpetas personalizadas administradas sólo pueden ser las subcarpetas de la carpeta denominada **Carpetas administradas**.  <br/> |
|[CalendarFolder](calendarfolder.md) <br/> |No es aplicable.  <br/> |
|[ContactsFolder](contactsfolder.md) <br/> |No es aplicable.  <br/> |
|[SearchFolder](searchfolder.md) <br/> |No es aplicable.  <br/> |
|[TasksFolder](tasksfolder.md) <br/> |No procede.  <br/> |
   
## <a name="remarks"></a>Notas

El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Ver también



[Operación CreateManagedFolder](createmanagedfolder-operation.md)


- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)


[Adición de las carpetas administradas](http://msdn.microsoft.com/library/846658c6-7043-40fb-8439-19f97c2a967f%28Office.15%29.aspx)

