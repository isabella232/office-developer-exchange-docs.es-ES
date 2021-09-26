---
title: Carpetas
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Folders
api_type:
- schema
ms.assetid: 8e71cb44-1df6-444a-add7-0c1363863f65
description: El elemento Folders contiene una matriz de carpetas que se usan en las operaciones de carpeta.
ms.openlocfilehash: 77442965c9d372a2895404cf1c919be38e98abb5
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59546437"
---
# <a name="folders"></a>Folders

El **elemento Folders** contiene una matriz de carpetas que se usan en las operaciones de carpeta. 
  
```xml
<Folders>
   <Folder/>
</Folders>
```

```xml
<Folders>
   <ContactsFolder/> 
</Folders>
```

```xml
<Folders>
   <TasksFolder/>
</Folders>
```

```xml
<Folders>
   <CalendarFolder/>
</Folders>
```

```xml
<Folders>
   <SearchFolder/> 
</Folders>
```

**ArrayOfFoldersType** o **NonEmptyArrayOfFoldersType**

## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Folder](folder.md) <br/> |Identifica una carpeta para crear, obtener, buscar, sincronizar o actualizar.  <br/> |
|[CalendarFolder](calendarfolder.md) <br/> |Representa una carpeta que contiene principalmente elementos de calendario.  <br/> |
|[ContactsFolder](contactsfolder.md) <br/> |Representa una carpeta Contactos de un buzón.  <br/> |
|[SearchFolder](searchfolder.md) <br/> |Representa una carpeta de búsqueda contenida en un buzón.  <br/> |
|[TasksFolder](tasksfolder.md) <br/> |Representa una carpeta Tareas en un buzón.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[CopyFolderResponseMessage](copyfolderresponsemessage.md) <br/> |Contiene el estado y el resultado de una única [solicitud de operación CopyFolder.](copyfolder-operation.md)  <br/> |
|[CreateFolder](createfolder.md) <br/> |Define una solicitud para crear una carpeta en el Exchange almacén.  <br/> |
|[CreateFolderResponseMessage](createfolderresponsemessage.md) <br/> |Contiene el estado y el resultado de una única [solicitud de operación CreateFolder.](createfolder-operation.md)  <br/> |
|[CreateManagedFolderResponseMessage](createmanagedfolderresponsemessage.md) <br/> |Contiene el estado y el resultado de una única solicitud de [operación CreateManagedFolder.](createmanagedfolder-operation.md)  <br/> |
|[GetFolderResponseMessage](getfolderresponsemessage.md) <br/> |Contiene el estado y el resultado de una [solicitud de operación GetFolder.](getfolder-operation.md)  <br/> |
|[MoveFolderResponseMessage](movefolderresponsemessage.md) <br/> |Contiene el estado y el resultado de una [solicitud de operación MoveFolder.](movefolder-operation.md)  <br/> |
|[ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) <br/> |Identifica la carpeta donde se crea una nueva carpeta.  <br/> |
|[RootFolder (FindFolderResponseMessage)](rootfolder-findfolderresponsemessage.md) <br/> |Contiene los resultados de la búsqueda de una sola carpeta raíz durante una [operación FindFolder](findfolder-operation.md).  <br/> |
|[UpdateFolderResponseMessage](updatefolderresponsemessage.md) <br/> |Contiene el estado y el resultado de una única [solicitud de operación UpdateFolder.](updatefolder-operation.md)  <br/> |
   
## <a name="remarks"></a>Comentarios

Este elemento es un elemento secundario necesario del [elemento ParentFolderId (TargetFolderIdType).](parentfolderid-targetfolderidtype.md) 
  
El esquema que describe este elemento se encuentra en el directorio virtual EWS del equipo que ejecuta Microsoft Exchange Server 2010 que tiene instalado el rol de servidor Acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Consulte también

- [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md)

