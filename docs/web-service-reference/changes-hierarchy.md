---
title: Cambios (jerarquía)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Changes
api_type:
- schema
ms.assetid: 918a0d1f-90a5-4eef-9592-07e15bef94e6
description: El elemento Changes contiene una matriz secuenciada de tipos de cambio que representan el tipo de diferencias entre las carpetas en el cliente y las carpetas en el equipo que ejecuta Microsoft Exchange Server 2007.
ms.openlocfilehash: a296d87f23e85d42b4c8c858e92eddfb586a8324
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463275"
---
# <a name="changes-hierarchy"></a>Cambios (jerarquía)

El elemento **Changes** contiene una matriz secuenciada de tipos de cambio que representan el tipo de diferencias entre las carpetas en el cliente y las carpetas en el equipo que ejecuta Microsoft Exchange Server 2007. 
  
[SyncFolderHierarchyResponse](syncfolderhierarchyresponse.md)
  
[ResponseMessages](responsemessages.md)
  
[SyncFolderHierarchyResponseMessage](syncfolderhierarchyresponsemessage.md)
  
[Cambios (jerarquía)](changes-hierarchy.md)
  
```xml
<Changes>
   <Create/>
   <Update/>
   <Delete/>
</Changes>
```

 **SyncFolderHierarchyChangesType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Crear (FolderSync)](create-foldersync.md) <br/> |Identifica una única carpeta que se va a crear en el almacén de cliente local.  <br/> |
|[Actualización (FolderSync)](update-foldersync.md) <br/> |Identifica una única carpeta para actualizar en el almacén de cliente local.  <br/> |
|[Eliminar (FolderSync)](delete-foldersync.md) <br/> |Identifica una única carpeta que se va a eliminar en el almacén de cliente local.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[SyncFolderHierarchyResponseMessage](syncfolderhierarchyresponsemessage.md) <br/> |Contiene el estado y el resultado de una solicitud SyncFolderHierarchy.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Se requiere un valor de texto que representa un valor booleano.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo de Exchange 2007 que tiene instalado el rol de servidor acceso de clientes.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también



[Operación SyncFolderHierarchy](syncfolderhierarchy-operation.md)


[Referencia EWS para Exchange](ews-reference-for-exchange.md)
  
- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)

