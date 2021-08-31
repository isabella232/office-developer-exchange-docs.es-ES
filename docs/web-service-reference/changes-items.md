---
title: Changes (Items)
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
ms.assetid: d3139fef-0455-4b89-babd-5d6783b50a58
description: El elemento Changes contiene una matriz de secuencias de tipos de cambio que representan los tipos de diferencias entre los elementos del cliente y los elementos del Exchange servidor.
ms.openlocfilehash: ede81d8ecae9751c477ae05cbd13f914fedf8e0f
ms.sourcegitcommit: 357b882a02e37b380a23b8a45b15f9c006a40b02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/31/2021
ms.locfileid: "58764633"
---
# <a name="changes-items"></a>Changes (Items)

El **elemento Changes** contiene una matriz de secuencias de tipos de cambio que representan los tipos de diferencias entre los elementos del cliente y los elementos del Exchange servidor. 
  
[SyncFolderItemsResponse](syncfolderitemsresponse.md)
  
[ResponseMessages](responsemessages.md)
  
[SyncFolderItemsResponseMessage](syncfolderitemsresponsemessage.md)
  
[Changes (Items)](changes-items.md)
  
```xml
<Changes>
   <Create/>
   <Update/>
   <Delete/>
   <ReadFlagChange/>
</Changes>
```

 **SyncFolderItemsChangesType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Create (ItemSync)](create-itemsync.md) <br/> |Identifica un solo elemento para crear en el almacén de cliente local.  <br/> |
|[Update (ItemSync)](update-itemsync.md) <br/> |Identifica un solo elemento para actualizar en el almacén de cliente local.  <br/> |
|[Delete (ItemSync)](delete-itemsync.md) <br/> |Identifica un único elemento que se debe eliminar en el almacén de cliente local.  <br/> |
|[ReadFlagChange](readflagchange.md) <br/> |Se devuelve en las respuestas de la operación [SyncFolderItems](syncfolderitems-operation.md) cuando se ha leído un elemento. Esta propiedad es de sólo lectura.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[SyncFolderItemsResponseMessage](syncfolderitemsresponsemessage.md) <br/> |Contiene el estado y el resultado de una [solicitud de operación SyncFolderItems.](syncfolderitems-operation.md)  <br/> |
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual EWS del equipo que ejecuta Microsoft Exchange Server 2010 que tiene instalado el rol de servidor Acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre del esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también



[Operación SyncFolderItems](syncfolderitems-operation.md)


- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

