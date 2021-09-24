---
title: DelegatePermissions
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- DelegatePermissions
api_type:
- schema
ms.assetid: 292badc7-bab3-4368-9d7c-9a8b7edb279b
description: El elemento DelegatePermissions contiene la configuración de nivel de permiso de delegado para un usuario. Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).
ms.openlocfilehash: a8c7e06ae0ad4e1d12d06b559ad7d9f9468c4ade
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59528995"
---
# <a name="delegatepermissions"></a>DelegatePermissions

El **elemento DelegatePermissions** contiene la configuración de nivel de permiso de delegado para un usuario. Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1). 
  
```xml
<DelegatePermissions>
   <CalendarFolderPermissionLevel/>
   <TasksFolderPermissionLevel/>
   <InboxFolderPermissionLevel/>
   <ContactsFolderPermissionLevel/>
   <NotesFolderPermissionLevel/>
   <JournalFolderPermissionLevel/>
</DelegatePermissions>
```

**DelegatePermissionsType**

## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[CalendarFolderPermissionLevel](calendarfolderpermissionlevel.md) <br/> |Contiene los permisos de la carpeta Calendar predeterminada. Este elemento se introdujo en Exchange 2007 SP1.  <br/> |
|[TasksFolderPermissionLevel](tasksfolderpermissionlevel.md) <br/> |Contiene los permisos de la carpeta task predeterminada. Este elemento se introdujo en Exchange 2007 SP1.  <br/> |
|[InboxFolderPermissionLevel](inboxfolderpermissionlevel.md) <br/> |Contiene los permisos de la carpeta Bandeja de entrada predeterminada. Este elemento se introdujo en Exchange 2007 SP1.  <br/> |
|[ContactsFolderPermissionLevel](contactsfolderpermissionlevel.md) <br/> |Contiene los permisos de la carpeta Contactos predeterminada. Este elemento se introdujo en Exchange 2007 SP1.  <br/> |
|[NotesFolderPermissionLevel](notesfolderpermissionlevel.md) <br/> |Contiene los permisos de la carpeta notes predeterminada. Este elemento se introdujo en Exchange 2007 SP1.  <br/> |
|[JournalFolderPermissionLevel](journalfolderpermissionlevel.md) <br/> |Contiene los permisos de la carpeta Journal predeterminada. Este elemento se introdujo en Exchange 2007 SP1.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[DelegateUser](delegateuser.md) <br/> |Identifica un único delegado para agregar o actualizar en un buzón. Este elemento se introdujo en Exchange 2007 SP1.  <br/> |
   
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

- [Operación AddDelegate](adddelegate-operation.md) 
- [Operación UpdateDelegate](updatedelegate-operation.md)
- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)
- [Agregar delegados](https://msdn.microsoft.com/library/3a744150-66a3-4a13-9433-793603ba5038%28Office.15%29.aspx)

