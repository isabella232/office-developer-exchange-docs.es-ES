---
title: PermissionLevel
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PermissionLevel
api_type:
- schema
ms.assetid: 87978600-3523-451e-a725-ef092c543e2a
description: El elemento PermissionLevel representa el nivel de permisos que un usuario tiene en una carpeta. Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).
ms.openlocfilehash: 7cc734f5807fe039467065315c220341f47d3fb4
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836730"
---
# <a name="permissionlevel"></a>PermissionLevel

El elemento **PermissionLevel** representa el nivel de permisos que un usuario tiene en una carpeta. Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1). 
  
```xml
<PermissionLevel>None or Owner or PublishingEditor or Editor or PublishingAuthor or Author or NoneditingAuthor or Reviewer or Contributor or Custom</PermissionLevel>
```

 **PermissionLevelType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[Permission](permission.md) <br/> |Define el acceso que tiene un usuario a una carpeta. Este elemento se introdujo en Exchange 2007 SP1.  <br/> |
   
## <a name="text-value"></a>Valor de texto

En la siguiente tabla se enumera los valores posibles para el elemento **PermissionLevel** . 
  
**Valores de texto de elemento PermissionLevel**

|**Valor**|**Descripción**|
|:-----|:-----|
|None  <br/> |Indica que el usuario no tiene permisos en la carpeta.  <br/> |
|Owner  <br/> |Indica que el usuario puede crear, leer, modificar y eliminar todos los elementos de la carpeta y crear subcarpetas. El usuario es el propietario de la carpeta y el contacto de la carpeta.  <br/> |
|PublishingEditor  <br/> |Indica que el usuario puede crear, leer, modificar y eliminar todos los elementos de la carpeta y crear subcarpetas.  <br/> |
|Editor  <br/> |Indica que el usuario puede crear, leer, editar y eliminar todos los elementos de la carpeta.  <br/> |
|PublishingAuthor  <br/> |Indica que el usuario puede crear y leer todos los elementos en la carpeta, editar y eliminar sólo los elementos que crea el usuario y crear subcarpetas.  <br/> |
|Autor  <br/> |Indica que el usuario puede crear y leer todos los elementos en la carpeta y editar y eliminar sólo los elementos que crea el usuario.  <br/> |
|NoneditingAuthor  <br/> |Indica que el usuario puede crear y leer todos los elementos en la carpeta y eliminar sólo los elementos que crea el usuario.  <br/> |
|Reviewer  <br/> |Indica que el usuario puede leer todos los elementos de la carpeta.  <br/> |
|Colaborador  <br/> |Indica que el usuario puede crear elementos en la carpeta. El contenido de la carpeta no aparecen.  <br/> |
|Personalizado  <br/> |Indica que el usuario tiene permisos de acceso personalizados en la carpeta.  <br/> |
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.
  
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

