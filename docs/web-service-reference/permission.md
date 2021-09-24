---
title: Permiso
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Permission
api_type:
- schema
ms.assetid: b8d0429a-0e58-4480-9847-4901970c7033
description: El elemento Permission define el acceso que un usuario tiene a una carpeta.
ms.openlocfilehash: bc3e140aaf7bd9ea7f1a4993c9bea1dcad8d39fa
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59512670"
---
# <a name="permission"></a>Permiso

El **elemento Permission** define el acceso que un usuario tiene a una carpeta. 
  
```XML
<Permission>
   <CanCreateItems/>
   <CanCreateSubfolders/>
   <IsFolderOwner/>
   <IsFolderVisible/>
   <IsFolderContact/>
   <EditItems/>
   <DeleteItems/>
   <PermissionLevel/>
   <ReadItems/>
   <UserId/>
</Permission>
```

 **PermissionType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[CanCreateItems](cancreateitems.md) <br/> |Indica si un usuario tiene permiso para crear elementos en una carpeta. Este elemento se introdujo en Exchange 2007 SP1.  <br/> |
|[CanCreateSubFolders](cancreatesubfolders.md) <br/> |Indica si un usuario tiene permiso para crear subcarpetas en una carpeta. Este elemento se introdujo en Exchange 2007 SP1.  <br/> |
|[DeleteItems](deleteitems.md) <br/> |Indica si un usuario tiene permiso para eliminar elementos de una carpeta. Este elemento se introdujo en Exchange 2007 SP1.  <br/> |
|[EditItems](edititems.md) <br/> |Indica si un usuario tiene permiso para editar elementos de una carpeta. Este elemento se introdujo en Exchange 2007 SP1.  <br/> |
|[IsFolderContact](isfoldercontact.md) <br/> |Indica si un usuario es un contacto de una carpeta. Este elemento se introdujo en Exchange 2007 SP1.  <br/> |
|[IsFolderOwner](isfolderowner.md) <br/> |Indica si un usuario es el propietario de una carpeta. Este elemento se introdujo en Exchange 2007 SP1.  <br/> |
|[IsFolderVisible](isfoldervisible.md) <br/> |Indica si un usuario puede ver una carpeta. Este elemento se introdujo en Exchange 2007 SP1.  <br/> |
|[PermissionLevel](permissionlevel.md) <br/> |Representa la combinación de permisos que un usuario tiene en una carpeta. Este elemento se introdujo en Exchange 2007 SP1.  <br/> |
|[ReadItems (PermissionType)](readitems-permissiontype.md) <br/> |Indica si un usuario tiene permiso para leer elementos dentro de una carpeta. Este elemento se introdujo en Exchange 2007 SP1.  <br/> |
|[UserId](userid.md) <br/> |Identifica un usuario delegado o un usuario que tiene permisos de acceso a carpetas. Este elemento se introdujo en Exchange 2007 SP1.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Permisos](permissions.md) <br/> |Contiene todos los permisos configurados para una carpeta. Este elemento se introdujo en Exchange 2007 SP1.  <br/> |
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
Este elemento se introdujo en Exchange Server 2007 Service Pack 1 (SP1).
  
### <a name="version-differences"></a>Diferencias de versión

Para las aplicaciones de destino Exchange Online, Exchange Online como parte de Office 365 o una versión local de Exchange a partir de Exchange 2013, los permisos de carpeta no se devuelven cuando el elemento [BaseShape](baseshape.md) tiene un valor de **AllProperties** en [GetFolder](getfolder-operation.md) solicitud de operación. Para recuperar los permisos de carpeta, agregue el [elemento PermissionSet (PermissionSetType)](permissionset-permissionsettype.md) al [elemento AdditionalProperties](additionalproperties.md) en la **solicitud GetFolder.** 
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también



- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)


[Configuración Folder-Level permisos](https://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)

