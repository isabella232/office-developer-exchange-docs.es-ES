---
title: ToFolderId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ToFolderId
api_type:
- schema
ms.assetid: bd6a4265-ad40-43f6-bcc4-0bf5df4e984c
description: El elemento ToFolderId representa la carpeta de destino para un elemento que se ha movido o copiado o una carpeta.
ms.openlocfilehash: a48309f0b7f5c9bf667fc2eb653a0502832bc996
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19840686"
---
# <a name="tofolderid"></a>ToFolderId

El elemento **ToFolderId** representa la carpeta de destino para un elemento que se ha movido o copiado o una carpeta. 
  
```xml
<ToFolderId>
   <FolderId/>
</ToFolderId>
```

 **TargetFolderIdType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[FolderId](folderid.md) <br/> |Contiene el identificador de una carpeta de destino para un elemento que se ha movido o copiado o una carpeta.  <br/> |
|[DistinguishedFolderId](distinguishedfolderid.md) <br/> |Identifica una carpeta de destino con nombre para un elemento que se ha movido o copiado o una carpeta.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[MoveFolder](movefolder.md) <br/> |Define una solicitud para mover una carpeta en el almacén de Exchange.  <br/> La siguiente es la expresión de XPath para este elemento:  <br/>  `/MoveFolder` <br/> |
|[CopyFolder](copyfolder.md) <br/> |Define una solicitud para copiar una carpeta en el almacén de Exchange.  <br/> La siguiente es la expresión de XPath para este elemento:  <br/>  `/CopyFolder` <br/> |
|[MoveItem](moveitem.md) <br/> |Define una solicitud para mover un elemento en el almacén de Exchange.  <br/> La siguiente es la expresión de XPath para este elemento:  <br/>  `/MoveItem` <br/> |
|[CopyItem](copyitem.md) <br/> |Define una solicitud para copiar un elemento en el almacén de Exchange.  <br/> La siguiente es la expresión de XPath para este elemento:  <br/>  `/CopyItem` <br/> |
   
## <a name="remarks"></a>Notas

El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Ver también



[Operación MoveFolder](movefolder-operation.md)
  
[Operación CopyFolder](copyfolder-operation.md)
  
[Operación MoveItem](moveitem-operation.md)
  
[Operación CopyItem](copyitem-operation.md)

