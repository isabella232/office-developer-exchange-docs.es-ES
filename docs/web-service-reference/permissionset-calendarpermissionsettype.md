---
title: PermissionSet (CalendarPermissionSetType)
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
ms.assetid: 75f20033-85eb-4627-b4f8-be85e4889e96
description: El elemento PermissionSet contiene todos los permisos configurados para una carpeta de calendario.
ms.openlocfilehash: 26351be8fd9fbe56ea5abb2dd346cb9c9458c463
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59539159"
---
# <a name="permissionset-calendarpermissionsettype"></a>PermissionSet (CalendarPermissionSetType)

El **elemento PermissionSet** contiene todos los permisos configurados para una carpeta de calendario. 
  
```XML
<PermissionSet>
   <CalendarPermissions/>
   <UnknownEntries/>
</PermissionSet>
```

 **CalendarPermissonSetType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[CalendarPermissions](calendarpermissions.md) <br/> |Contiene una matriz de permisos de calendario para una carpeta. Este elemento se introdujo en Exchange 2007 SP1.  <br/> |
|[UnknownEntries](unknownentries.md) <br/> |Contiene una matriz de entradas desconocidas que no se pueden resolver en el servicio de directorio de Active Directory. Este elemento se introdujo en Exchange 2007 SP1.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[CalendarFolder](calendarfolder.md) <br/> |Representa una carpeta que contiene principalmente elementos de calendario.  <br/> |
   
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

