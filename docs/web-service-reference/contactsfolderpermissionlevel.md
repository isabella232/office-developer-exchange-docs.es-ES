---
title: ContactsFolderPermissionLevel
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ContactsFolderPermissionLevel
api_type:
- schema
ms.assetid: 805f05e7-b320-436a-9965-ba1ee235ac41
description: El elemento ContactsFolderPermissionLevel contiene los permisos para la carpeta de contactos predeterminada. Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).
ms.openlocfilehash: 8d76e00ab63714e220bd3205b10c8b72d15a4788
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44527127"
---
# <a name="contactsfolderpermissionlevel"></a>ContactsFolderPermissionLevel

El elemento **ContactsFolderPermissionLevel** contiene los permisos para la carpeta de contactos predeterminada. Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1). 
  
```xml
<ContactsFolderPermissionLevel>
   None or Editor or Reviewer or Author or Custom
</ContactsFolderPermissionLevel>
```

 **DelegateFolderPermissionLevelType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[DelegatePermissions](delegatepermissions.md) <br/> |Contiene la configuración del nivel de permisos de delegado de un usuario. Este elemento se introdujo en Exchange 2007 SP1.  <br/> |
   
## <a name="text-value"></a>Valor de texto

En la siguiente tabla se enumeran los valores de texto que representan los niveles de permisos.
  
**Valores de texto de nivel de permisos**

|**Nivel de permisos**|**Descripción**|
|:-----|:-----|
|Ninguno  <br/> |El usuario delegado no tiene permisos de acceso a la carpeta contactos.  <br/> |
|Reviewer  <br/> |El usuario delegado puede leer los elementos de la carpeta de contactos.  <br/> |
|Autor  <br/> |El usuario delegado puede leer y crear elementos en la carpeta de contactos.  <br/> |
|Editor  <br/> |El usuario delegado puede leer, crear y modificar los elementos de la carpeta de contactos.  <br/> |
|Personalizado  <br/> |El usuario delegado tiene permisos de acceso personalizados a la carpeta contactos.  <br/> |
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también



[Operación AddDelegate](adddelegate-operation.md)
  
[Operación UpdateDelegate](updatedelegate-operation.md)


- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)


[Adición de delegados](https://msdn.microsoft.com/library/3a744150-66a3-4a13-9433-793603ba5038%28Office.15%29.aspx)

