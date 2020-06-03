---
title: CreateManagedFolder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CreateManagedFolder
api_type:
- schema
ms.assetid: cfdf01a9-0191-47c7-a7ad-5254d8bdee4a
description: El elemento CreateManagedFolder define una solicitud para agregar carpetas administradas personalizadas a un buzón de correo.
ms.openlocfilehash: 01fe8b7341c38ad33089c56271434ad3f9a4e5f0
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458365"
---
# <a name="createmanagedfolder"></a>CreateManagedFolder

El elemento **CreateManagedFolder** define una solicitud para agregar carpetas administradas personalizadas a un buzón de correo. 
  
```xml
<CreateManagedFolder>
   <FolderNames/>
   <Mailbox/>
</CreateManagedFolder>
```

 **CreateManagedFolderRequestType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[FolderNames](foldernames.md) <br/> |Contiene una matriz de carpetas administradas con nombre para agregar a un buzón de correo.  <br/> |
|[Buzón](mailbox.md) <br/> |Identifica un objeto de servicio de directorio de Active Directory habilitado para correo.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

Ninguno.
  
## <a name="remarks"></a>Comentarios

La cuenta de la persona que realiza la solicitud debe tener permisos FullAccess en el buzón de correo en el que se crean las carpetas administradas. Puede usar el parámetro _-AccessRights _ con el cmdlet **Add-MailboxPermission** del shell de administración de Exchange para asignar el permiso FullAccess. 
  
Aunque puede usar los servicios Web de Exchange para agregar carpetas administradas a un buzón de correo, no puede usar los servicios web Exchange para tener acceso a la lista de carpetas administradas que están disponibles. Para obtener una lista de las carpetas administradas disponibles, use el cmdlet **Get-managedfolder de** Shell de administración de Exchange. La lista que devuelve el **cmdlet Get-managedfolder** contendrá tanto las carpetas personalizadas administradas como las carpetas predeterminadas administradas. Solo se pueden agregar carpetas de tipo **managedcustomfolder** al buzón mediante la operación CreateManagedFolder. 
  
> [!NOTE]
> También puede obtener una lista de carpetas administradas mediante la API de DirectoryServices de Microsoft .NET Framework. 
  
Puede usar la [operación FindFolder](findfolder-operation.md) para buscar carpetas administradas en un buzón. Las carpetas administradas se pueden distinguir estableciendo el elemento [BaseShape](baseshape.md) en AllProperties en la solicitud. La respuesta contendrá un elemento [ManagedFolderInformation](managedfolderinformation.md) para distinguir las carpetas administradas de las carpetas de almacén de Exchange. Las carpetas administradas se pueden eliminar de la misma manera que se eliminan otros tipos de carpetas. 
  
El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también



[Operación CreateManagedFolder](createmanagedfolder-operation.md)
  
[Operación FindFolder](findfolder-operation.md)


[Buscar carpetas](https://msdn.microsoft.com/library/9124d868-017a-43f0-b915-5c0082cacec9%28Office.15%29.aspx)
  
[Adición de carpetas administradas](https://msdn.microsoft.com/library/846658c6-7043-40fb-8439-19f97c2a967f%28Office.15%29.aspx)

