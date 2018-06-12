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
description: El elemento de FolderId contiene el identificador y cambiar la clave de una carpeta.
ms.openlocfilehash: 5764a164d5af183b8f313955ace5274dc6023a6a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764683"
---
# <a name="folderid"></a>FolderId

El elemento de **FolderId** contiene el identificador y cambiar la clave de una carpeta. 
  
```XML
<FolderId Id="" ChangeKey="" />
```

 **FolderIdType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Attribute**|**Descripción**|
|:-----|:-----|
|Id  <br/> |Contiene una cadena que identifica una carpeta en el almacén de Exchange. Este atributo es necesario.  <br/> |
|ChangeKey  <br/> |Contiene una cadena que identifica una versión de una carpeta que se identifica con el atributo Id. Este atributo es opcional. Use este atributo para asegurarse de que se usa la versión correcta de una carpeta.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[ContextFolderId](contextfolderid.md) <br/> |Indica la carpeta que está destinada a las acciones que utilizan carpetas.  <br/> |
|[CopiedEvent](copiedevent.md) <br/> |Representa un evento en el que se copia un elemento o carpeta.  <br/> |
|[DestinationFolderId](destinationfolderid.md) <br/> |Indica la carpeta de destino para copiar y mover las acciones.  <br/> |
|[ID (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) <br/> | Identifica la carpeta donde se crea una nueva carpeta o elemento.  <br/><br/>  Los siguientes son las expresiones de XPath para este elemento:<br/>  <br/> `/CreateItem/ParentFolderId` <br/><br/>  `/CreateFolder/ParentFolderId` <br/> |
|[BaseFolderIds](basefolderids.md) <br/> |Representa la colección de carpetas que se extraídos para determinar el contenido de una carpeta de búsqueda.  <br/> |
|[Eliminar (FolderSync)](delete-foldersync.md) <br/> |Identifica una sola carpeta para eliminar en el almacén de cliente local.  <br/> |
|[Folder](folder.md) <br/> |Representa una carpeta en un buzón de correo.  <br/> |
|[CalendarFolder](calendarfolder.md) <br/> |Representa una carpeta del calendario en un buzón de correo.  <br/> |
|[FolderChange](folderchange.md) <br/> |Representa una colección de los cambios que se debe realizar en una sola carpeta.  <br/> La siguiente es la expresión de XPath para este elemento:`/UpdateFolder/FolderChanges/FolderChange` <br/> |
|[ContactsFolder](contactsfolder.md) <br/> |Representa una carpeta de contactos en un buzón de correo.  <br/> |
|[SearchFolder](searchfolder.md) <br/> |Representa una carpeta de búsqueda en un buzón de correo.  <br/> |
|[TasksFolder](tasksfolder.md) <br/> |Representa una carpeta de tareas en un buzón de correo.  <br/> |
|[ToFolderId](tofolderid.md) <br/> | Representa la carpeta de destino para un elemento que se ha movido o copiado o una carpeta. <br/> <br/>  Los siguientes son las expresiones de XPath para este elemento: <br/> <br/>  `/MoveFolder/ToFolderId` <br/> <br/> `/CopyFolder/ToFolderId` <br/> <br/> `/MoveItem/ToFolderId`<br/> <br/>  `/CopyItem/ToFolderId` <br/> |
|[SavedItemFolderId](saveditemfolderid.md) <br/> | Identifica la carpeta de destino para las operaciones que actualizar, enviar y crear elementos en el almacén de Exchange.  <br/><br/>  Los siguientes son las expresiones de XPath para este elemento: <br/> <br/>  `/CreateItem/SavedItemFolderId` <br/><br/>  `/UpdateItem/SavedItemFolderId` <br/><br/>  `/SendItem/SavedItemFolderId` <br/> |
|[SyncFolderId](syncfolderid.md) <br/> |Representa la carpeta que contiene los elementos para sincronizar.  <br/> |
|[UserConfigurationName](userconfigurationname.md) <br/> |Representa el nombre de un objeto de configuración de usuario. El nombre del objeto de configuración de usuario es el identificador de un objeto de configuración de usuario.  <br/> |
|[CopyToFolder](copytofolder.md) <br/> |Identifica el identificador de la carpeta que se copiarán los elementos de correo electrónico a.  <br/> |
|[MoveToFolder](movetofolder.md) <br/> |Identifica el identificador de la carpeta que se moverán los elementos de correo electrónico a.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="remarks"></a>Observaciones

Todos los elementos de **FolderId** son del tipo **FolderIdType** . Se requiere el elemento **FolderId** en todos los casos, excepto en los elementos cuyo tipo extiende el **BaseFolderType** o donde el elemento **FolderId** es una parte de una opción. Revise el esquema para obtener más información. 
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Ver también

- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)
- [Creación de carpetas (servicios Web de Exchange)](http://msdn.microsoft.com/library/3b15b0ec-8691-45ed-9a24-a91ff732d6cf%28Office.15%29.aspx)

