---
title: Carpetas
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Folders
api_type:
- schema
ms.assetid: 8e71cb44-1df6-444a-add7-0c1363863f65
description: El elemento de las carpetas contiene una matriz de las carpetas que se usan en las operaciones de la carpeta.
ms.openlocfilehash: 34372f2480825c7a9977eeae8e730c201307f36b
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/28/2018
ms.locfileid: "21353591"
---
# <a name="folders"></a>Carpetas

El elemento de **las carpetas** contiene una matriz de las carpetas que se usan en las operaciones de la carpeta. 
  
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

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[Folder](folder.md) <br/> |Identifica una carpeta para crear, obtener, buscar, sincronizar o actualizar.  <br/> |
|[CalendarFolder](calendarfolder.md) <br/> |Representa una carpeta que principalmente contiene los elementos del calendario.  <br/> |
|[ContactsFolder](contactsfolder.md) <br/> |Representa una carpeta de contactos en un buzón de correo.  <br/> |
|[SearchFolder](searchfolder.md) <br/> |Representa una carpeta de búsqueda incluida en un buzón de correo.  <br/> |
|[TasksFolder](tasksfolder.md) <br/> |Representa una carpeta de tareas en un buzón de correo.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[CopyFolderResponseMessage](copyfolderresponsemessage.md) <br/> |Contiene el estado y el resultado de una única solicitud de [operación CopyFolder](copyfolder-operation.md) .  <br/> |
|[CreateFolder](createfolder.md) <br/> |Define una solicitud para crear una carpeta en el almacén de Exchange.  <br/> |
|[CreateFolderResponseMessage](createfolderresponsemessage.md) <br/> |Contiene el estado y el resultado de una única solicitud de [operación CreateFolder](createfolder-operation.md) .  <br/> |
|[CreateManagedFolderResponseMessage](createmanagedfolderresponsemessage.md) <br/> |Contiene el estado y el resultado de una única solicitud de [operación CreateManagedFolder](createmanagedfolder-operation.md) .  <br/> |
|[GetFolderResponseMessage](getfolderresponsemessage.md) <br/> |Contiene el estado y el resultado de una solicitud de [operación GetFolder](getfolder-operation.md) .  <br/> |
|[MoveFolderResponseMessage](movefolderresponsemessage.md) <br/> |Contiene el estado y el resultado de una solicitud de [operación MoveFolder](movefolder-operation.md) .  <br/> |
|[ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) <br/> |Identifica la carpeta donde se crea una nueva carpeta.  <br/> |
|[RootFolder (FindFolderResponseMessage)](rootfolder-findfolderresponsemessage.md) <br/> |Contiene los resultados de búsqueda de una sola carpeta raíz durante una [operación de FindFolder](findfolder-operation.md).  <br/> |
|[UpdateFolderResponseMessage](updatefolderresponsemessage.md) <br/> |Contiene el estado y el resultado de una única solicitud de [operación UpdateFolder](updatefolder-operation.md) .  <br/> |
   
## <a name="remarks"></a>Comentarios

Este elemento es un elemento secundario necesario del elemento [ID (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) . 
  
El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2010 que tenga instalado el rol de servidor de acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Vea también

- [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md)

