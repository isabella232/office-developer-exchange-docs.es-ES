---
title: Folder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Folder
api_type:
- schema
ms.assetid: 812948d8-c7db-45ce-bb3a-77233a53a974
description: El elemento Folder define una carpeta para crear, obtener, buscar, sincronizar o actualizar.
ms.openlocfilehash: 5b6b8eb1d53c84bc3d0484d1c868470137db492d
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59530384"
---
# <a name="folder"></a>Folder

El **elemento Folder** define una carpeta para crear, obtener, buscar, sincronizar o actualizar. 
  
```xml
<Folder>
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
</Folder>
```

 **FolderType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[FolderId](folderid.md) <br/> |Contiene el identificador y la clave de cambio de una carpeta.  <br/> |
|[ParentFolderId](parentfolderid.md) <br/> |Representa el identificador de la carpeta principal que contiene la carpeta.  <br/> |
|[FolderClass](folderclass.md) <br/> |Representa la clase de carpeta de una carpeta determinada.  <br/> |
|[DisplayName (cadena)](displayname-string.md) <br/> |Contiene el nombre para mostrar de una carpeta.  <br/> |
|[TotalCount](totalcount.md) <br/> |Representa el recuento total de elementos dentro de una carpeta determinada.  <br/> |
|[ChildFolderCount](childfoldercount.md) <br/> |Representa el número de carpetas secundarias que se encuentran dentro de una carpeta. Esta propiedad es de sólo lectura.  <br/> |
|[ExtendedProperty](extendedproperty.md) <br/> |Identifica las propiedades extendidas de las carpetas.  <br/> |
|[ManagedFolderInformation](managedfolderinformation.md) <br/> |Contiene información sobre una carpeta administrada.  <br/> |
|[UnreadCount](unreadcount.md) <br/> |Representa el recuento de elementos no leídos dentro de una carpeta determinada.  <br/> |
|[PermissionSet (PermissionSetType)](permissionset-permissionsettype.md) <br/> |Contiene todos los permisos configurados para una carpeta. Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).  <br/> |
|[EffectiveRights](effectiverights.md) <br/> |Contiene los derechos del cliente en función de la configuración de permisos del elemento o carpeta. Este elemento es de solo lectura. Este elemento se introdujo en Exchange 2007 SP1.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[AppendToFolderField](appendtofolderfield.md) <br/> |Especifica los datos que se anexarán a una propiedad folder durante una [operación UpdateFolder](updatefolder-operation.md).  <br/> |
|[Create (FolderSync)](create-foldersync.md) <br/> |Identifica una sola carpeta para crear en el almacén de cliente local.  <br/> |
|[SetFolderField](setfolderfield.md) <br/> |Representa una actualización de una sola propiedad de una carpeta en una [operación UpdateFolder](updatefolder-operation.md).  <br/> |
|[Update (FolderSync)](update-foldersync.md) <br/> |Identifica una sola carpeta que se actualizará en el almacén de cliente local.  <br/> |
|[Folders](folders-ex15websvcsotherref.md) <br/> |Contiene una matriz de carpetas que se usan en las operaciones de carpeta.  <br/> |
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual EWS del equipo que ejecuta Exchange 2007 que tiene instalado el rol de servidor Acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también



[Operación SyncFolderItems](syncfolderitems-operation.md)


- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

