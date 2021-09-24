---
title: Changes (Hierarchy)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Changes
api_type:
- schema
ms.assetid: 918a0d1f-90a5-4eef-9592-07e15bef94e6
description: El elemento Changes contiene una matriz secuenciada de tipos de cambio que representan el tipo de diferencias entre las carpetas del cliente y las carpetas del equipo que se ejecuta Microsoft Exchange Server 2007.
ms.openlocfilehash: 1ecb43e37258ad5d8e12619436f14992cc2f788b
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59512124"
---
# <a name="changes-hierarchy"></a>Changes (Hierarchy)

El **elemento Changes** contiene una matriz secuenciada de tipos de cambio que representan el tipo de diferencias entre las carpetas del cliente y las carpetas del equipo que se ejecuta Microsoft Exchange Server 2007. 
  
[SyncFolderHierarchyResponse](syncfolderhierarchyresponse.md)
  
[ResponseMessages](responsemessages.md)
  
[SyncFolderHierarchyResponseMessage](syncfolderhierarchyresponsemessage.md)
  
[Changes (Hierarchy)](changes-hierarchy.md)
  
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

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Create (FolderSync)](create-foldersync.md) <br/> |Identifica una sola carpeta para crear en el almacén de cliente local.  <br/> |
|[Update (FolderSync)](update-foldersync.md) <br/> |Identifica una sola carpeta que se actualizará en el almacén de cliente local.  <br/> |
|[Delete (FolderSync)](delete-foldersync.md) <br/> |Identifica una sola carpeta que se debe eliminar en el almacén de cliente local.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[SyncFolderHierarchyResponseMessage](syncfolderhierarchyresponsemessage.md) <br/> |Contiene el estado y el resultado de una solicitud SyncFolderHierarchy.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Se requiere un valor de texto que representa un valor booleano.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual EWS del equipo Exchange 2007 que tiene instalado el rol de servidor Acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre del esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también



[Operación SyncFolderHierarchy](syncfolderhierarchy-operation.md)


[Referencia EWS para Exchange](ews-reference-for-exchange.md)
  
- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

