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
ms.openlocfilehash: e1b9e337f633dbf6fda159c28725d3fb8dcd55a6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764686"
---
# <a name="folders"></a>Carpetas

El elemento de **las carpetas** contiene una matriz de las carpetas que se usan en las operaciones de la carpeta. 
  
```xml
<Folders>
   <Folder/>
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
|[ID (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) <br/> |Identifica la carpeta donde se crea una nueva carpeta.  <br/> |
|[RootFolder (FindFolderResponseMessage)](rootfolder-findfolderresponsemessage.md) <br/> |Contiene los resultados de búsqueda de una sola carpeta raíz durante una [operación de FindFolder](findfolder-operation.md).  <br/> |
|[UpdateFolderResponseMessage](updatefolderresponsemessage.md) <br/> |Contiene el estado y el resultado de una única solicitud de [operación UpdateFolder](updatefolder-operation.md) .  <br/> |
   
## <a name="remarks"></a>Notas

Este elemento es un elemento secundario necesario del elemento [ID (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) . 
  
El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2010 que tenga instalado el rol de servidor de acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Ver también



[ID (TargetFolderIdType)](parentfolderid-targetfolderidtype.md)

