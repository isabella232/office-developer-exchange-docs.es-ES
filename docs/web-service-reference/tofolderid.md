---
title: ToFolderId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ToFolderId
api_type:
- schema
ms.assetid: bd6a4265-ad40-43f6-bcc4-0bf5df4e984c
description: El elemento ToFolderId representa la carpeta de destino de un elemento o carpeta copiados o movidos.
ms.openlocfilehash: b58192aa4d1ffe609da78dfdf1b5c86522fc45c8
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59515169"
---
# <a name="tofolderid"></a>ToFolderId

El **elemento ToFolderId** representa la carpeta de destino de un elemento o carpeta copiados o movidos. 
  
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

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[FolderId](folderid.md) <br/> |Contiene el identificador de una carpeta de destino para un elemento o carpeta copiados o movidos.  <br/> |
|[DistinguishedFolderId](distinguishedfolderid.md) <br/> |Identifica una carpeta de destino con nombre para un elemento o carpeta copiados o movidos.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[MoveFolder](movefolder.md) <br/> |Define una solicitud para mover una carpeta en el Exchange almacén.  <br/> A continuación se muestra la expresión XPath de este elemento:  <br/>  `/MoveFolder` <br/> |
|[CopyFolder](copyfolder.md) <br/> |Define una solicitud para copiar una carpeta en el Exchange almacén.  <br/> A continuación se muestra la expresión XPath de este elemento:  <br/>  `/CopyFolder` <br/> |
|[MoveItem](moveitem.md) <br/> |Define una solicitud para mover un elemento en el Exchange almacén.  <br/> A continuación se muestra la expresión XPath de este elemento:  <br/>  `/MoveItem` <br/> |
|[CopyItem](copyitem.md) <br/> |Define una solicitud para copiar un elemento en el Exchange almacén.  <br/> A continuación se muestra la expresión XPath de este elemento:  <br/>  `/CopyItem` <br/> |
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor Acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también

- [Operación MoveFolder](movefolder-operation.md)  
- [Operación CopyFolder](copyfolder-operation.md) 
- [Operación MoveItem](moveitem-operation.md) 
- [Operación CopyItem](copyitem-operation.md)

