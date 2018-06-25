---
title: PermissionSet (PermissionSetType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PermissionSet
api_type:
- schema
ms.assetid: 6ac1bd17-a089-46bb-b9e6-f5b1dfe1076d
description: El elemento PermissionSet contiene todos los permisos que están configurados para una carpeta.
ms.openlocfilehash: 0fa0ac78a0db2bf382ad413cbb8bd072aa88c6fb
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836732"
---
# <a name="permissionset-permissionsettype"></a>PermissionSet (PermissionSetType)

El elemento **PermissionSet** contiene todos los permisos que están configurados para una carpeta. 
  
```XML
<PermissionSet>
   <Permissions/>
   <UnknownEntries/>
</PermissionSet>
```

 **PermissionSetType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[Permisos](permissions.md) <br/> |Contiene la colección de permisos para una carpeta. Este elemento se introdujo en Exchange 2007 SP1.  <br/> |
|[UnknownEntries](unknownentries.md) <br/> |Contiene una matriz de las entradas desconocidas que no se puede resolver con el servicio de directorio de Active Directory. Este elemento se introdujo en Exchange 2007 SP1.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[Folder](folder.md) <br/> |Define una carpeta para crear, obtener, buscar, sincronizar o actualizar.  <br/> |
|[SearchFolder](searchfolder.md) <br/> |Representa una carpeta de búsqueda que se encuentra en un buzón de correo.  <br/> |
|[ContactsFolder](contactsfolder.md) <br/> |Representa una carpeta de contactos que se encuentra en un buzón de correo.  <br/> |
|[TasksFolder](tasksfolder.md) <br/> |Representa una carpeta de tareas que se encuentra en un buzón de correo.  <br/> |
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
Este elemento se introdujo en Exchange Server 2007 Service Pack 1 (SP1).
  
### <a name="version-differences"></a>Diferencias de versión

Para las aplicaciones de ese destino Exchange Online, Exchange Online como parte de Office 365 o una versión local de Exchange a partir de Exchange 2013, los permisos de carpetas no se devuelven cuando el elemento [BaseShape](baseshape.md) tiene un valor de **AllProperties** en la solicitud de operación [GetFolder](getfolder-operation.md) . Para recuperar los permisos de carpeta, agregue el elemento [PermissionSet (PermissionSetType)](permissionset-permissionsettype.md) al elemento [AdditionalProperties](additionalproperties.md) en la solicitud de **GetFolder** . 
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Vea también



- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)


[Establecimiento de permisos de nivel de carpeta](http://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)

