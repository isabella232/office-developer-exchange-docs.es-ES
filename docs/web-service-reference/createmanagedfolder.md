---
title: CreateManagedFolder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- CreateManagedFolder
api_type:
- schema
ms.assetid: cfdf01a9-0191-47c7-a7ad-5254d8bdee4a
description: El elemento CreateManagedFolder define una solicitud para agregar carpetas personalizadas administradas a un buzón.
ms.openlocfilehash: ca6850cfdc8a37bf0480db0c040b035591a59ce6
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59536376"
---
# <a name="createmanagedfolder"></a>CreateManagedFolder

El **elemento CreateManagedFolder** define una solicitud para agregar carpetas personalizadas administradas a un buzón. 
  
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

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[FolderNames](foldernames.md) <br/> |Contiene una matriz de carpetas administradas con nombre para agregar a un buzón.  <br/> |
|[Buzón](mailbox.md) <br/> |Identifica un objeto de servicio de directorio de Active Directory habilitado para correo.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

Ninguno.
  
## <a name="remarks"></a>Comentarios

La cuenta de la persona que realiza la solicitud debe tener permisos FullAccess en el buzón donde se crean las carpetas administradas. Puede usar el parámetro _ -AccessRights _ con el cmdlet **Add-MailboxPermission** del Shell de administración de Exchange para asignar el permiso FullAccess. 
  
Aunque puede usar Exchange Web Services para agregar carpetas administradas a un buzón, no puede usar Exchange Web Services para obtener acceso a la lista de carpetas administradas que están disponibles. Para obtener una lista de carpetas administradas disponibles, use el **cmdlet get-managedfolder** Exchange Shell de administración. La lista que devuelve el **cmdlet get-managedfolder** contendrá carpetas personalizadas administradas y carpetas predeterminadas administradas. Solo puede agregar carpetas de tipo **managedcustomfolder** al buzón mediante la operación CreateManagedFolder. 
  
> [!NOTE]
> También puede obtener una lista de carpetas administradas mediante la API DirectoryServices de Microsoft .NET Framework. 
  
Puede usar la operación [FindFolder para](findfolder-operation.md) buscar carpetas administradas en un buzón. Las carpetas administradas se pueden distinguir estableciendo el [elemento BaseShape](baseshape.md) en AllProperties en la solicitud. La respuesta contendrá un [elemento ManagedFolderInformation](managedfolderinformation.md) para distinguir las carpetas administradas de las Exchange almacén. Puede eliminar carpetas administradas de la misma manera que elimina otros tipos de carpetas. 
  
El esquema que describe este elemento se encuentra en el directorio virtual EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor Acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también



[Operación CreateManagedFolder](createmanagedfolder-operation.md)
  
[Operación FindFolder](findfolder-operation.md)


[Buscar carpetas](https://msdn.microsoft.com/library/9124d868-017a-43f0-b915-5c0082cacec9%28Office.15%29.aspx)
  
[Agregar carpetas administradas](https://msdn.microsoft.com/library/846658c6-7043-40fb-8439-19f97c2a967f%28Office.15%29.aspx)

