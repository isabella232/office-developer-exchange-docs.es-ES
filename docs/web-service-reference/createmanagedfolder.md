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
description: El elemento CreateManagedFolder define una solicitud para agregar carpetas personalizadas administradas a un buzón de correo.
ms.openlocfilehash: 4acc931de2a8665db092c3b309d914f0a3c67558
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763966"
---
# <a name="createmanagedfolder"></a>CreateManagedFolder

El elemento **CreateManagedFolder** define una solicitud para agregar carpetas personalizadas administradas a un buzón de correo. 
  
```xml
<CreateManagedFolder>
   <FolderNames/>
   <Mailbox/>
</CreateManagedFolder>
```

 **CreateManagedFolderRequestType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[Nombres de carpetas](foldernames.md) <br/> |Contiene una matriz de las carpetas administradas con nombre para agregar a un buzón de correo.  <br/> |
|[Buzón de correo](mailbox.md) <br/> |Identifica un objeto de servicio de directorio de Active Directory habilitados para correo.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

Ninguno.
  
## <a name="remarks"></a>Observaciones

La cuenta de la persona que realiza la solicitud debe tener permisos de FullAccess en el buzón de correo donde se crean las carpetas administradas. Puede usar el parámetro de _ _ - AccessRights con el cmdlet **Add-MailboxPermission** de Shell de administración de Exchange para asignar el permiso FullAccess. 
  
Aunque puede usar servicios Web de Exchange para agregar las carpetas administradas a un buzón de correo, no puede usar servicios Web de Exchange para tener acceso a la lista de carpetas administradas que están disponibles. Para obtener una lista de las carpetas administradas disponibles, use el cmdlet del Shell de administración de Exchange de **get-carpeta administrada** . La lista que es devuelto por el **cmdlet get-carpeta administrada** contiene carpetas personalizadas administradas y carpetas predeterminadas administradas. Sólo puede agregar carpetas de tipo **managedcustomfolder** para el buzón de correo mediante el uso de la operación CreateManagedFolder. 
  
> [!NOTE]
> También puede obtener una lista de las carpetas administradas mediante el uso de la API de DirectoryServices de Microsoft .NET Framework. 
  
Puede usar la [operación FindFolder](findfolder-operation.md) para buscar las carpetas administradas en un buzón de correo. Las carpetas administradas se pueden distinguir estableciendo el elemento [BaseShape](baseshape.md) en AllProperties en la solicitud. La respuesta contendrá un elemento [ManagedFolderInformation](managedfolderinformation.md) para distinguir las carpetas administradas de las carpetas del almacén de Exchange. Puede eliminar las carpetas administradas de la misma forma que eliminar otros tipos de carpetas. 
  
El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Ver también



[Operación CreateManagedFolder](createmanagedfolder-operation.md)
  
[Operación FindFolder](findfolder-operation.md)


[Buscar carpetas](http://msdn.microsoft.com/library/9124d868-017a-43f0-b915-5c0082cacec9%28Office.15%29.aspx)
  
[Adición de las carpetas administradas](http://msdn.microsoft.com/library/846658c6-7043-40fb-8439-19f97c2a967f%28Office.15%29.aspx)

