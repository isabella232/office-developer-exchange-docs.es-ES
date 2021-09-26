---
title: PermissionSet (PermissionSetType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PermissionSet
api_type:
- schema
ms.assetid: 6ac1bd17-a089-46bb-b9e6-f5b1dfe1076d
description: El elemento PermissionSet contiene todos los permisos configurados para una carpeta.
ms.openlocfilehash: b18fef33d3be6cb8c525f731a264860c3a83afdc
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59543145"
---
# <a name="permissionset-permissionsettype"></a>PermissionSet (PermissionSetType)

El **elemento PermissionSet** contiene todos los permisos configurados para una carpeta. 
  
```XML
<PermissionSet>
   <Permissions/>
   <UnknownEntries/>
</PermissionSet>
```

 **PermissionSetType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Permisos](permissions.md) <br/> |Contiene la colección de permisos de una carpeta. Este elemento se introdujo en Exchange 2007 SP1.  <br/> |
|[UnknownEntries](unknownentries.md) <br/> |Contiene una matriz de entradas desconocidas que no se pueden resolver en el servicio de directorio de Active Directory. Este elemento se introdujo en Exchange 2007 SP1.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Folder](folder.md) <br/> |Define una carpeta para crear, obtener, buscar, sincronizar o actualizar.  <br/> |
|[SearchFolder](searchfolder.md) <br/> |Representa una carpeta de búsqueda que se encuentra en un buzón.  <br/> |
|[ContactsFolder](contactsfolder.md) <br/> |Representa una carpeta de contactos que se encuentra en un buzón.  <br/> |
|[TasksFolder](tasksfolder.md) <br/> |Representa una carpeta de tareas que se encuentra en un buzón.  <br/> |
   
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
   
## <a name="see-also"></a>Consulte también



- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)


[Configuración Folder-Level permisos](https://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)

