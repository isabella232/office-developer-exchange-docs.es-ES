---
title: Cambios (elementos)
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
description: El elemento de cambios contiene una matriz de secuencia de tipos de cambio que representan los tipos de las diferencias entre los elementos en el cliente y los elementos en el servidor de Exchange.
ms.openlocfilehash: 8e38597276e3e3051a5c1494619d3220280e401f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763735"
---
# <a name="changes-items"></a>Cambios (elementos)

El elemento de **cambios** contiene una matriz de secuencia de tipos de cambio que representan los tipos de las diferencias entre los elementos en el cliente y los elementos en el servidor de Exchange. 
  
[SyncFolderItemsResponse](syncfolderitemsresponse.md)
  
[ResponseMessages](responsemessages.md)
  
[SyncFolderItemsResponseMessage](syncfolderitemsresponsemessage.md)
  
[Cambios (elementos)](changes-items.md)
  
```xml
<Changes>
   <Create/>
   <Update/>
   <Delete/>
</Changes>
```

 **SyncFolderItemsChangesType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[Crear (ItemSync)](create-itemsync.md) <br/> |Identifica un solo elemento para crear en el almacén de cliente local.  <br/> |
|[Actualización (ItemSync)](update-itemsync.md) <br/> |Identifica un solo elemento que se debe actualizar en el almacén de cliente local.  <br/> |
|[Eliminar (ItemSync)](delete-itemsync.md) <br/> |Identifica un solo elemento para eliminar en el almacén de cliente local.  <br/> |
|[ReadFlagChange](readflagchange.md) <br/> |Se devuelven en las respuestas de [operación SyncFolderItems](syncfolderitems-operation.md) cuando se leyó un elemento. Esta propiedad es de sólo lectura.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[SyncFolderItemsResponseMessage](syncfolderitemsresponsemessage.md) <br/> |Contiene el estado y el resultado de una solicitud de [operación SyncFolderItems](syncfolderitems-operation.md) .  <br/> |
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2010 que tenga instalado el rol de servidor de acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Vea también



[Operación SyncFolderItems](syncfolderitems-operation.md)


- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

