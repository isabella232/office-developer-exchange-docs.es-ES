---
title: Actualización (FolderSync)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Update
api_type:
- schema
ms.assetid: 47ed8edb-2a94-471b-b965-93f91456252e
description: El elemento Update identifica una única carpeta para actualizar en el almacén de cliente local.
ms.openlocfilehash: 5c1b5b1fd87e4651125293eac431c56f732c6c02
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/01/2020
ms.locfileid: "44467140"
---
# <a name="update-foldersync"></a>Actualización (FolderSync)

El elemento **Update** identifica una única carpeta para actualizar en el almacén de cliente local. 
  
- [SyncFolderHierarchyResponse](syncfolderhierarchyresponse.md) 
- [ResponseMessages](responsemessages.md) 
- [SyncFolderHierarchyResponseMessage](syncfolderhierarchyresponsemessage.md)  
- [Cambios (jerarquía)](changes-hierarchy.md) 
- [Actualización (FolderSync)](update-foldersync.md)
  
```xml
<Update>
   <Folder/>
</Update>
```

```xml
<Update>
   <CalendarFolder/>
</Update>
```

```xml
<Update>
   <ContactsFolder/>
</Update>
```

```xml
<Update>
   <TasksFolder/>
</Update>
```

```xml
<Update>
   <SearchFolder/>
</Update>
```

**SyncFolderHierarchyCreateOrUpdateType**

## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Folder](folder.md) <br/> |Define la carpeta que se va a crear, obtener, buscar, sincronizar o actualizar.  <br/> |
|[Hubiera](calendarfolder.md) <br/> |Representa una carpeta que contiene principalmente elementos de calendario.  <br/> |
|[Hubiera](contactsfolder.md) <br/> |Representa una carpeta de contactos en un buzón.  <br/> |
|[SearchFolder](searchfolder.md) <br/> |Representa una carpeta de búsqueda contenida en un buzón.  <br/> |
|[Hubiera](tasksfolder.md) <br/> |Representa una carpeta de tareas t es thcontained en un buzón.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Cambios (jerarquía)](changes-hierarchy.md) <br/> |Contiene una matriz secuenciada de tipos de cambio que representan el tipo de diferencias entre las carpetas en el cliente y las carpetas en el servidor de Exchange.  <br/> |
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también

- [Operación SyncFolderItems](syncfolderitems-operation.md)
- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)

