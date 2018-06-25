---
title: TasksFolder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- TasksFolder
api_type:
- schema
ms.assetid: 5a9a4612-8064-4986-b467-c44f268c64df
description: El elemento TasksFolder representa una carpeta de tareas que se encuentra en un buzón de correo.
ms.openlocfilehash: b2151c68519a6ff15fbc74b48fc93a7e06af9e76
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19840626"
---
# <a name="tasksfolder"></a>TasksFolder

El elemento **TasksFolder** representa una carpeta de tareas que se encuentra en un buzón de correo. 
  
```xml
<TasksFolder>
   <FolderId/>
   <ParentFolderId/>
   <FolderClass/>
   <DisplayName/>
   <TotalCount/>
   <ChildFolderCount/>
   <ExtendedProperty/>
   <ManagedFolderInformation/>
   <UnreadCount/>
   <PermissionSet/>
      <EffectiveRights/>
</TasksFolder>
```

**TasksFolderType**

## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[FolderId](folderid.md) <br/> |Contiene el identificador y cambiar la clave de una carpeta tareas.  <br/> |
|[Id](parentfolderid.md) <br/> |Representa el identificador de la carpeta primaria que contiene la carpeta tareas.  <br/> |
|[FolderClass](folderclass.md) <br/> |Representa la clase de carpeta para una carpeta de tareas.  <br/> |
|[DisplayName (cadena)](displayname-string.md) <br/> |Contiene el nombre para mostrar de una carpeta tareas.  <br/> |
|[TotalCount](totalcount.md) <br/> |Representa el recuento total de elementos dentro de una carpeta tareas.  <br/> |
|[ChildFolderCount](childfoldercount.md) <br/> |Representa el número de carpetas secundarias contenidas en una carpeta de tareas. Esta propiedad es de sólo lectura.  <br/> |
|[ExtendedProperty](extendedproperty.md) <br/> |Identifica las propiedades extendidas en una carpeta de tareas.  <br/> |
|[ManagedFolderInformation](managedfolderinformation.md) <br/> |Contiene información acerca de una carpeta administrada.  <br/> |
|[UnreadCount](unreadcount.md) <br/> |Representa el recuento de elementos no leídos dentro de una carpeta tareas.  <br/> |
|[PermissionSet (PermissionSetType)](permissionset-permissionsettype.md) <br/> |Contiene todos los permisos configurados para una carpeta. Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).  <br/> |
|[EffectiveRights](effectiverights.md) <br/> |Contiene los derechos del cliente en función de la configuración de permisos para el elemento o la carpeta. Este elemento es de sólo lectura. Este elemento se introdujo en Microsoft Exchange 2007 SP1.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[AppendToFolderField](appendtofolderfield.md) <br/> |Especifica los datos que se anexará a una propiedad de la carpeta durante una [operación de UpdateFolder](updatefolder-operation.md).  <br/> |
|[Crear (FolderSync)](create-foldersync.md) <br/> |Identifica una sola carpeta para crear en el almacén de cliente local.  <br/> |
|[SetFolderField](setfolderfield.md) <br/> |Representa una actualización a una propiedad única en una carpeta en una [operación de UpdateFolder](updatefolder-operation.md).  <br/> |
|[Actualización (FolderSync)](update-foldersync.md) <br/> |Identifica una sola carpeta para actualizar en el almacén de cliente local.  <br/> |
|[Carpetas](folders-ex15websvcsotherref.md) <br/> |Contiene una matriz de las carpetas que se usan en las operaciones de la carpeta.  <br/> |
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Vea también

- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

