---
title: NotesFolderPermissionLevel
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- NotesFolderPermissionLevel
api_type:
- schema
ms.assetid: 76a2520c-f453-4fd7-b3eb-1c5f4666680a
description: El elemento NotesFolderPermissionLevel contiene los permisos de la carpeta Notes predeterminada. Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).
ms.openlocfilehash: c7dbcbad6213c9ceccbcdf03b8e684c8523627e2
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59539265"
---
# <a name="notesfolderpermissionlevel"></a>NotesFolderPermissionLevel

El **elemento NotesFolderPermissionLevel** contiene los permisos de la carpeta Notes predeterminada. Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1). 
  
```xml
<NotesFolderPermissionLevel>
   None or Editor or Reviewer or Author or Custom
</NotesFolderPermissionLevel>
```

 **DelegateFolderPermissionLevelType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[DelegatePermissions](delegatepermissions.md) <br/> |Contiene la configuración del nivel de permiso delegado para un usuario. Este elemento se introdujo en Exchange 2007 SP1.  <br/> |
   
## <a name="text-value"></a>Valor de texto

En la tabla siguiente se enumeran los valores de texto que representan los niveles de permisos.
  
**Valores de texto de nivel de permiso**

|**Nivel de permisos**|**Descripción**|
|:-----|:-----|
|Ninguno  <br/> |El usuario delegado no tiene permisos de acceso a la carpeta Notas.  <br/> |
|Reviewer  <br/> |El usuario delegado puede leer elementos en la carpeta Notas.  <br/> |
|Autor  <br/> |El usuario delegado puede leer y crear elementos en la carpeta Notas.  <br/> |
|Editor  <br/> |El usuario delegado puede leer, crear y modificar elementos de la carpeta Notas.  <br/> |
|Personalizado  <br/> |El usuario delegado tiene permisos de acceso personalizados a la carpeta Notas.  <br/> |
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor Acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también



[Operación AddDelegate](adddelegate-operation.md)
  
[Operación UpdateDelegate](updatedelegate-operation.md)


- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)


[Agregar delegados](https://msdn.microsoft.com/library/3a744150-66a3-4a13-9433-793603ba5038%28Office.15%29.aspx)

