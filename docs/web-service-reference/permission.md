---
title: Permiso
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Permission
api_type:
- schema
ms.assetid: b8d0429a-0e58-4480-9847-4901970c7033
description: El elemento Permission define el acceso que tiene un usuario a una carpeta.
ms.openlocfilehash: 0f7515dbb06f8423f8d4d95e1391496e8ac73653
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459261"
---
# <a name="permission"></a>Permiso

El elemento **Permission** define el acceso que tiene un usuario a una carpeta. 
  
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

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[CanCreateItems](cancreateitems.md) <br/> |Indica si un usuario tiene permiso para crear elementos en una carpeta. Este elemento se introdujo en Exchange 2007 SP1.  <br/> |
|[CanCreateSubFolders](cancreatesubfolders.md) <br/> |Indica si un usuario tiene permiso para crear subcarpetas en una carpeta. Este elemento se introdujo en Exchange 2007 SP1.  <br/> |
|[DeleteItems](deleteitems.md) <br/> |Indica si un usuario tiene permiso para eliminar elementos de una carpeta. Este elemento se introdujo en Exchange 2007 SP1.  <br/> |
|[EditItems](edititems.md) <br/> |Indica si un usuario tiene permiso para editar los elementos de una carpeta. Este elemento se introdujo en Exchange 2007 SP1.  <br/> |
|[IsFolderContact](isfoldercontact.md) <br/> |Indica si un usuario es un contacto de una carpeta. Este elemento se introdujo en Exchange 2007 SP1.  <br/> |
|[IsFolderOwner](isfolderowner.md) <br/> |Indica si un usuario es el propietario de una carpeta. Este elemento se introdujo en Exchange 2007 SP1.  <br/> |
|[IsFolderVisible](isfoldervisible.md) <br/> |Indica si un usuario puede ver una carpeta. Este elemento se introdujo en Exchange 2007 SP1.  <br/> |
|[PermissionLevel](permissionlevel.md) <br/> |Representa la combinación de permisos que tiene un usuario en una carpeta. Este elemento se introdujo en Exchange 2007 SP1.  <br/> |
|[ReadItems (PermissionType)](readitems-permissiontype.md) <br/> |Indica si un usuario tiene permiso para leer elementos dentro de una carpeta. Este elemento se introdujo en Exchange 2007 SP1.  <br/> |
|[UserId](userid.md) <br/> |Identifica un usuario delegado o un usuario que tiene permisos de acceso a la carpeta. Este elemento se introdujo en Exchange 2007 SP1.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Permisos](permissions.md) <br/> |Contiene todos los permisos configurados para una carpeta. Este elemento se introdujo en Exchange 2007 SP1.  <br/> |
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
Este elemento se introdujo en Exchange Server 2007 Service Pack 1 (SP1).
  
### <a name="version-differences"></a>Diferencias de versión

Para las aplicaciones dirigidas a Exchange Online, Exchange online como parte de Office 365 o a una versión local de Exchange a partir de Exchange 2013, no se devuelven permisos de carpeta cuando el elemento [BaseShape](baseshape.md) tiene un valor de **AllProperties** en la solicitud de operación [GetFolder](getfolder-operation.md) . Para recuperar los permisos de carpeta, agregue el elemento [PermissionSet (PermissionSetType)](permissionset-permissionsettype.md) al elemento [AdditionalProperties](additionalproperties.md) en la solicitud **GetFolder** . 
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también



- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)


[Configuración de permisos de nivel de carpeta](https://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)

