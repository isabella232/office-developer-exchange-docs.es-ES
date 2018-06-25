---
title: CalendarFolderPermissionLevel
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CalendarFolderPermissionLevel
api_type:
- schema
ms.assetid: 2a5c9381-dc2c-4fc6-b9b5-893477d0970e
description: El elemento CalendarFolderPermissionLevel contiene los permisos para la carpeta Calendario predeterminada. Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).
ms.openlocfilehash: 5d51fea522656910d8417e7f75214214e2c162c6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763702"
---
# <a name="calendarfolderpermissionlevel"></a>CalendarFolderPermissionLevel

El elemento **CalendarFolderPermissionLevel** contiene los permisos para la carpeta Calendario predeterminada. Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1). 
  
```xml
<CalendarFolderPermissionLevel>
   None or Editor or Reviewer or Author or Custom
</CalendarFolderPermissionLevel>
```

 **DelegateFolderPermissionLevelType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[DelegatePermissions](delegatepermissions.md) <br/> |Contiene la configuración de nivel de permisos de delegado de un usuario. Este elemento se introdujo en Exchange 2007 SP1.  <br/> |
   
## <a name="text-value"></a>Valor de texto

En la siguiente tabla se enumera los valores de texto que representan los niveles de permisos.
  
**Valores de texto de nivel de permisos**

|**Nivel de permisos**|**Descripción**|
|:-----|:-----|
|None  <br/> |El usuario delegado no tiene ningún permiso de acceso a la carpeta Calendario.  <br/> |
|Reviewer  <br/> |El usuario delegado puede leer los elementos de la carpeta del calendario.  <br/> |
|Autor  <br/> |El usuario delegado puede leer y crear elementos en la carpeta del calendario.  <br/> |
|Editor  <br/> |El usuario delegado puede leer, crear y modificar elementos en la carpeta Calendario.  <br/> |
|Personalizado  <br/> |El usuario delegado tiene permisos de acceso personalizados a la carpeta Calendario.  <br/> |
   
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



[Operación AddDelegate](adddelegate-operation.md)
  
[Operación UpdateDelegate](updatedelegate-operation.md)


- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)


[Adición de delegados](http://msdn.microsoft.com/library/3a744150-66a3-4a13-9433-793603ba5038%28Office.15%29.aspx)

