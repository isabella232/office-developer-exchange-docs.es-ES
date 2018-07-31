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
ms.openlocfilehash: 9d2fd6c177711cfe3a5d3415320440259e2f5289
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/28/2018
ms.locfileid: "21353661"
---
# <a name="tofolderid"></a>ToFolderId

El elemento **ToFolderId** representa la carpeta de destino para un elemento que se ha movido o copiado o una carpeta. 
  
```xml
<ToFolderId>
   <FolderId/>
</ToFolderId>
```

```xml
<ToFolderId>
   <DistinguishedFolderId/>
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
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Vea también

- [Operación MoveFolder](movefolder-operation.md)  
- [Operación CopyFolder](copyfolder-operation.md) 
- [Operación MoveItem](moveitem-operation.md) 
- [Operación CopyItem](copyitem-operation.md)

