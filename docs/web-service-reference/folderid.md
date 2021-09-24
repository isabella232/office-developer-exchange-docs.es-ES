---
title: FolderId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- FolderId
api_type:
- schema
ms.assetid: 00d14e3e-4365-4f21-8f88-eaeea73b9bf7
description: El elemento FolderId contiene el identificador y la clave de cambio de una carpeta.
ms.openlocfilehash: 7348fb7342bf33d487591a9daf93a9570f7552f4
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59513685"
---
# <a name="folderid"></a>FolderId

El **elemento FolderId** contiene el identificador y la clave de cambio de una carpeta. 
  
```XML
<FolderId Id="" ChangeKey="" />
```

 **FolderIdType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Descripción**|
|:-----|:-----|
|Id  <br/> |Contiene una cadena que identifica una carpeta en el Exchange almacén. Este atributo es obligatorio.  <br/> |
|ChangeKey  <br/> |Contiene una cadena que identifica una versión de una carpeta identificada por el atributo Id. Este atributo es opcional. Use este atributo para asegurarse de que se usa la versión correcta de una carpeta.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[ContextFolderId](contextfolderid.md) <br/> |Indica la carpeta destinada a las acciones que usan carpetas.  <br/> |
|[CopiedEvent](copiedevent.md) <br/> |Representa un evento en el que se copia un elemento o carpeta.  <br/> |
|[DestinationFolderId](destinationfolderid.md) <br/> |Indica la carpeta de destino para las acciones de copia y movimiento.  <br/> |
|[ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) <br/> | Identifica la carpeta donde se crea una nueva carpeta o elemento.  <br/><br/>  Las siguientes son las expresiones XPath de este elemento:<br/>  <br/> `/CreateItem/ParentFolderId` <br/><br/>  `/CreateFolder/ParentFolderId` <br/> |
|[BaseFolderIds](basefolderids.md) <br/> |Representa la colección de carpetas que se extrairán para determinar el contenido de una carpeta de búsqueda.  <br/> |
|[Delete (FolderSync)](delete-foldersync.md) <br/> |Identifica una sola carpeta que se debe eliminar en el almacén de cliente local.  <br/> |
|[Folder](folder.md) <br/> |Representa una carpeta de un buzón.  <br/> |
|[CalendarFolder](calendarfolder.md) <br/> |Representa una carpeta de calendario en un buzón.  <br/> |
|[FolderChange](folderchange.md) <br/> |Representa una colección de cambios que se deben realizar en una sola carpeta.  <br/> A continuación se muestra la expresión XPath de este elemento:  `/UpdateFolder/FolderChanges/FolderChange` <br/> |
|[ContactsFolder](contactsfolder.md) <br/> |Representa una carpeta de contacto en un buzón.  <br/> |
|[SearchFolder](searchfolder.md) <br/> |Representa una carpeta de búsqueda en un buzón.  <br/> |
|[TasksFolder](tasksfolder.md) <br/> |Representa una carpeta de tareas en un buzón.  <br/> |
|[ToFolderId](tofolderid.md) <br/> | Representa la carpeta de destino de un elemento o carpeta copiados o movidos. <br/> <br/>  Las siguientes son las expresiones XPath de este elemento: <br/> <br/>  `/MoveFolder/ToFolderId` <br/> <br/> `/CopyFolder/ToFolderId` <br/> <br/> `/MoveItem/ToFolderId`<br/> <br/>  `/CopyItem/ToFolderId` <br/> |
|[SavedItemFolderId](saveditemfolderid.md) <br/> | Identifica la carpeta de destino para las operaciones que actualizan, envían y crean elementos en el Exchange almacén.  <br/><br/>  Las siguientes son las expresiones XPath de este elemento: <br/> <br/>  `/CreateItem/SavedItemFolderId` <br/><br/>  `/UpdateItem/SavedItemFolderId` <br/><br/>  `/SendItem/SavedItemFolderId` <br/> |
|[SyncFolderId](syncfolderid.md) <br/> |Representa la carpeta que contiene los elementos que se deben sincronizar.  <br/> |
|[UserConfigurationName](userconfigurationname.md) <br/> |Representa el nombre de un objeto de configuración de usuario. El nombre del objeto de configuración de usuario es el identificador de un objeto de configuración de usuario.  <br/> |
|[CopyToFolder](copytofolder.md) <br/> |Identifica el identificador de la carpeta a la que se copiarán los elementos de correo electrónico.  <br/> |
|[MoveToFolder](movetofolder.md) <br/> |Identifica el identificador de la carpeta a la que se van a mover los elementos de correo electrónico.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="remarks"></a>Comentarios

Todos **los elementos FolderId** son del **tipo FolderIdType.** El **elemento FolderId** es necesario en todos los casos, excepto en los elementos cuyo tipo extiende **el BaseFolderType** o donde **el elemento FolderId** forma parte de una opción. Revise el esquema para obtener más información. 
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también

- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)
- [Creación de carpetas (Exchange Web Services)](https://msdn.microsoft.com/library/3b15b0ec-8691-45ed-9a24-a91ff732d6cf%28Office.15%29.aspx)

