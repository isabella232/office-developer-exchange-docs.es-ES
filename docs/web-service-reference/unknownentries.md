---
title: UnknownEntries
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UnknownEntries
api_type:
- schema
ms.assetid: 107ec73e-083a-4956-9d37-33d4734cc157
description: El elemento UnknownEntries contiene una matriz de entradas de permisos desconocidos que no se pueden resolver contra el servicio de directorio de Active Directory. Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).
ms.openlocfilehash: 68cb2518b895ca0a74e6b9ed649ee92b7502ab05
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459422"
---
# <a name="unknownentries"></a>UnknownEntries

El elemento **UnknownEntries** contiene una matriz de entradas de permisos desconocidos que no se pueden resolver contra el servicio de directorio de Active Directory. Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1). 
  
```xml
<UnknownEntries>
   <UnknownEntry/>
</UnknownEntries>
```

 **ArrayOfUnknownEntriesType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[UnknownEntry](unknownentry.md) <br/> |Representa una sola entrada de permiso desconocida que no se puede resolver en Active Directory. Este elemento se introdujo en Exchange 2007 SP1.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[PermissionSet (PermissionSetType)](permissionset-permissionsettype.md) <br/> |Contiene todos los permisos que se configuran para una carpeta. Este elemento se introdujo en Exchange 2007 SP1.  <br/> |
|[PermissionSet (CalendarPermissionSetType)](permissionset-calendarpermissionsettype.md) <br/> |Contiene todos los permisos que se configuran para una carpeta de calendario. Este elemento se introdujo en Exchange 2007 SP1.  <br/> |
   
## <a name="remarks"></a>Comentarios

Puede eliminar entradas desconocidas de una carpeta mediante la operación UpdateFolder con el elemento [SetFolderField](setfolderfield.md) . Las entradas desconocidas se eliminan al restablecer el PermissionSet mediante la opción SetFolderField de la operación UpdateFolder. Los servicios web Exchange no admiten la eliminación de entradas individuales. 
  
El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también



[Operación UpdateFolder](updatefolder-operation.md)


- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)


[Configuración de permisos de nivel de carpeta](https://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)

