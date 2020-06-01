---
title: SearchFolder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SearchFolder
api_type:
- schema
ms.assetid: 1a7d408b-2e98-4391-8834-085ed6d5757c
description: El elemento SearchFolder representa una carpeta de búsqueda que está contenida en un buzón.
ms.openlocfilehash: e1d5893e00f3b199451622061785e2566c6f32e5
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44464010"
---
# <a name="searchfolder"></a>SearchFolder

El elemento **SearchFolder** representa una carpeta de búsqueda que está contenida en un buzón. 
  
```xml
<SearchFolder>
   <FolderId/>
   <ParentFolderId/>
   <FolderClass/>
   <DisplayName/>
   <TotalCount/>
   <ChildFolderCount/>
   <ExtendedProperty/>
   <ManagedFolderInformation/>
   <UnreadCount/>
   <SearchParameters/>
   <PermissionSet/>
      <EffectiveRights/>
</SearchFolder>
```

 **SearchFolderType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[FolderId](folderid.md) <br/> |Contiene el identificador y la clave de cambio de una carpeta.  <br/> |
|[ParentFolderId](parentfolderid.md) <br/> |Representa el identificador de la carpeta principal que contiene la carpeta.  <br/> |
|[FolderClass](folderclass.md) <br/> |Representa la clase de carpeta de una carpeta determinada.  <br/> |
|[DisplayName (cadena)](displayname-string.md) <br/> |Contiene el nombre para mostrar de una carpeta.  <br/> |
|[TotalCount](totalcount.md) <br/> |Representa el número total de elementos dentro de una carpeta determinada.  <br/> |
|[ChildFolderCount](childfoldercount.md) <br/> |Representa el número de carpetas secundarias contenidas dentro de una carpeta. Esta propiedad es de sólo lectura.  <br/> |
|[Las extendedproperty](extendedproperty.md) <br/> |Identifica las propiedades extendidas de las carpetas.  <br/> |
|[ManagedFolderInformation](managedfolderinformation.md) <br/> |Contiene información acerca de una carpeta administrada.  <br/> |
|[UnreadCount](unreadcount.md) <br/> |Representa el número de elementos no leídos dentro de una carpeta determinada.  <br/> |
|[SearchParameters](searchparameters.md) <br/> |Contiene los parámetros que definen una carpeta de búsqueda.  <br/> |
|[PermissionSet (PermissionSetType)](permissionset-permissionsettype.md) <br/> |Contiene todos los permisos configurados para una carpeta. Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).  <br/> |
|[EffectiveRights](effectiverights.md) <br/> |Contiene los derechos del cliente en función de la configuración de los permisos del elemento o carpeta. Este elemento es de sólo lectura. Este elemento se introdujo en Exchange 2007 SP1.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[AppendToFolderField](appendtofolderfield.md) <br/> |Especifica los datos que se van a anexar a una propiedad de carpeta durante una [operación UpdateFolder](updatefolder-operation.md).  <br/> |
|[Crear (FolderSync)](create-foldersync.md) <br/> |Identifica una única carpeta que se va a crear en el almacén de cliente local.  <br/> |
|[SetFolderField](setfolderfield.md) <br/> |Representa una actualización de una propiedad única de una carpeta en una [operación UpdateFolder](updatefolder-operation.md).  <br/> |
|[Actualización (FolderSync)](update-foldersync.md) <br/> |Identifica una única carpeta para actualizar en el almacén de cliente local.  <br/> |
|[Folders](folders-ex15websvcsotherref.md) <br/> |Contiene una matriz de carpetas que se usan en las operaciones de carpeta.  <br/> |
   
## <a name="remarks"></a>Comentarios

 **SearchFolder** se utiliza tanto para las carpetas de búsqueda normales como para las carpetas de búsqueda de MicrosoftOfficeOutlook y Outlook Web Access visibles. Para que una carpeta de búsqueda esté visible en Outlook y Outlook Web Access, la carpeta debe crearse en la carpeta distintiva SearchFolders. 
  
El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también



- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)

