---
title: ParentFolderIds
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ParentFolderIds
api_type:
- schema
ms.assetid: e7998023-e5e0-465c-91fa-2aa6d1559f64
description: El elemento ParentFolderIds identifica las carpetas de las operaciones FindItem y FindFolder que se buscarán.
ms.openlocfilehash: e9e0f14651b205ad64be04dbe1d0707a109f3edc
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59512920"
---
# <a name="parentfolderids"></a>ParentFolderIds

El **elemento ParentFolderIds** identifica las carpetas de las operaciones FindItem y FindFolder que se buscarán. 
  
```xml
<ParentFolderIds>
   <DistinguishedFolderId/>
<ParentFolderIds>
```

```xml
<ParentFolderIds>
   <FolderId/> 
<ParentFolderIds>
```

**NonEmptyArrayOfBaseFolderIdsType**

## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[FolderId](folderid.md) <br/> |Contiene el identificador y la clave de cambio de una carpeta. El **elemento ParentFolderIds** debe usar este elemento o [el elemento DistinguishedFolderId.](distinguishedfolderid.md)  <br/> |
|[DistinguishedFolderId](distinguishedfolderid.md) <br/> |Identifica Microsoft Exchange Server carpetas de 2007 a las que se puede hacer referencia por su nombre. El **elemento ParentFolderIds** debe usar este elemento o [el elemento FolderId.](folderid.md)  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[FindFolder](findfolder.md) <br/> |Define una solicitud para identificar carpetas de un buzón.  <br/> |
|[FindItem](finditem.md) <br/> |Define una solicitud para buscar elementos en un buzón.  <br/> |
|[ResolveNames](resolvenames.md) <br/> |Define una solicitud para resolver nombres ambiguos.  <br/> |
   
## <a name="remarks"></a>Comentarios

El **elemento ParentFolderIds** debe usar el [elemento FolderId](folderid.md) o [distinguishedFolderId.](distinguishedfolderid.md) Se puede definir un número ilimitado de carpetas para la búsqueda. 
  
## <a name="example"></a>Ejemplo

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <FindFolder Traversal="Shallow" xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <FolderShape>
        <t:BaseShape>Default</t:BaseShape>
      </FolderShape>
      <ParentFolderIds>
        <t:DistinguishedFolderId Id="inbox"/>
      </ParentFolderIds>
    </FindFolder>
  </soap:Body>
</soap:Envelope>
```

## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también

- [Operación FindFolder](findfolder-operation.md)  
- [Operación FindItem](finditem-operation.md) 
- [Operación ResolveNames](resolvenames-operation.md)

