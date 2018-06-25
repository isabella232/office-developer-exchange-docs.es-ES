---
title: UserConfigurationName
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UserConfigurationName
api_type:
- schema
ms.assetid: 6947dd03-9727-4379-9b9d-42373fa120c7
description: El elemento UserConfigurationName representa el nombre de un objeto de configuración de usuario. El nombre del objeto de configuración de usuario es el identificador de un objeto de configuración de usuario.
ms.openlocfilehash: 40580343e92493c3d39b090371708269ec3274b9
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19840900"
---
# <a name="userconfigurationname"></a>UserConfigurationName

El elemento **UserConfigurationName** representa el nombre de un objeto de configuración de usuario. El nombre del objeto de configuración de usuario es el identificador de un objeto de configuración de usuario. 
  
```XML
<UserConfigurationName Name="">
   <FolderId/>
</UserConfigurationName>
```

 **UserConfigurationNameType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Attribute**|**Descripción**|
|:-----|:-----|
|**Name** <br/> |Contiene un valor de tipo string que representa el nombre de un objeto de configuración de usuario. Este atributo es necesario.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[FolderId](folderid.md) <br/> |Representa el identificador de la carpeta de la carpeta que contiene el objeto de configuración de usuario.  <br/> |
|[DistinguishedFolderId](distinguishedfolderid.md) <br/> |Representa un nombre distintivo (DN) de carpeta de la carpeta que contiene el objeto de configuración de usuario.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[DeleteUserConfiguration](deleteuserconfiguration.md) <br/> |Representa una solicitud para eliminar un objeto de configuración de usuario.  <br/> |
|[GetUserConfiguration](getuserconfiguration.md) <br/> |Representa una solicitud para obtener un objeto de configuración de usuario.  <br/> |
|[UserConfiguration](userconfiguration.md) <br/> |Define un objeto de configuración de usuario único.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Vea también



- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

