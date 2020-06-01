---
title: FolderId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FolderId
api_type:
- schema
ms.assetid: 00d14e3e-4365-4f21-8f88-eaeea73b9bf7
description: El elemento FolderId contiene el identificador y la clave de cambio de una carpeta.
ms.openlocfilehash: 7aa5070fa7a2c51303c7159de04fe277f909a874
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461390"
---
# <a name="folderid"></a>FolderId

El elemento **FolderId** contiene el identificador y la clave de cambio de una carpeta. 
  
```XML
<FolderId Id="" ChangeKey="" />
```

 **FolderIdType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Descripción**|
|:-----|:-----|
|Id  <br/> |Contiene una cadena que identifica una carpeta en el almacén de Exchange. Este atributo es obligatorio.  <br/> |
|ChangeKey  <br/> |Contiene una cadena que identifica una versión de una carpeta identificada por el atributo id. Este atributo es opcional. Use este atributo para asegurarse de que se usa la versión correcta de una carpeta.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[ContextFolderId](contextfolderid.md) <br/> |Indica la carpeta que está destinada a las acciones que usan carpetas.  <br/> |
|[CopiedEvent](copiedevent.md) <br/> |Representa un evento en el que se copia un elemento o una carpeta.  <br/> |
|[DestinationFolderId](destinationfolderid.md) <br/> |Indica la carpeta de destino para las acciones de copiar y mover.  <br/> |
|[ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) <br/> | Identifica la carpeta en la que se crea una nueva carpeta o elemento.  <br/><br/>  Las siguientes son las expresiones XPath de este elemento:<br/>  <br/> `/CreateItem/ParentFolderId` <br/><br/>  `/CreateFolder/ParentFolderId` <br/> |
|[BaseFolderIds](basefolderids.md) <br/> |Representa la colección de carpetas que se extendrán para determinar el contenido de una carpeta de búsqueda.  <br/> |
|[Eliminar (FolderSync)](delete-foldersync.md) <br/> |Identifica una única carpeta que se va a eliminar en el almacén de cliente local.  <br/> |
|[Folder](folder.md) <br/> |Representa una carpeta en un buzón.  <br/> |
|[Hubiera](calendarfolder.md) <br/> |Representa una carpeta de calendario en un buzón.  <br/> |
|[FolderChange](folderchange.md) <br/> |Representa una colección de cambios que se van a realizar en una sola carpeta.  <br/> La siguiente es la expresión XPath a este elemento:`/UpdateFolder/FolderChanges/FolderChange` <br/> |
|[Hubiera](contactsfolder.md) <br/> |Representa una carpeta de contactos en un buzón.  <br/> |
|[SearchFolder](searchfolder.md) <br/> |Representa una carpeta de búsqueda en un buzón.  <br/> |
|[Hubiera](tasksfolder.md) <br/> |Representa una carpeta de tareas en un buzón.  <br/> |
|[ToFolderId](tofolderid.md) <br/> | Representa la carpeta de destino de un elemento o carpeta que se ha copiado o movido. <br/> <br/>  Las siguientes son las expresiones XPath de este elemento: <br/> <br/>  `/MoveFolder/ToFolderId` <br/> <br/> `/CopyFolder/ToFolderId` <br/> <br/> `/MoveItem/ToFolderId`<br/> <br/>  `/CopyItem/ToFolderId` <br/> |
|[SavedItemFolderId](saveditemfolderid.md) <br/> | Identifica la carpeta de destino para las operaciones que actualizan, envían y crean elementos en el almacén de Exchange.  <br/><br/>  Las siguientes son las expresiones XPath de este elemento: <br/> <br/>  `/CreateItem/SavedItemFolderId` <br/><br/>  `/UpdateItem/SavedItemFolderId` <br/><br/>  `/SendItem/SavedItemFolderId` <br/> |
|[SyncFolderId](syncfolderid.md) <br/> |Representa la carpeta que contiene los elementos que se van a sincronizar.  <br/> |
|[UserConfigurationName](userconfigurationname.md) <br/> |Representa el nombre de un objeto de configuración de usuario. El nombre del objeto de configuración de usuario es el identificador de un objeto de configuración de usuario.  <br/> |
|[CopyToFolder](copytofolder.md) <br/> |Identifica el identificador de la carpeta en la que se copiarán los elementos de correo electrónico.  <br/> |
|[MoveToFolder](movetofolder.md) <br/> |Identifica el identificador de la carpeta a la que se moverán los elementos de correo electrónico.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="remarks"></a>Comentarios

Todos los elementos **FolderId** son del tipo **FolderIdType** . El elemento **FolderId** es necesario en todos los casos, excepto en elementos cuyo tipo extiende la **BaseFolderType** o donde el elemento **FolderId** forma parte de una opción. Revise el esquema para obtener más información. 
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también

- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)
- [Creación de carpetas (servicios Web de Exchange)](https://msdn.microsoft.com/library/3b15b0ec-8691-45ed-9a24-a91ff732d6cf%28Office.15%29.aspx)

