---
title: ParentFolderIds
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ParentFolderIds
api_type:
- schema
ms.assetid: e7998023-e5e0-465c-91fa-2aa6d1559f64
description: El elemento ParentFolderIds identifica las carpetas para las operaciones FindItem y FindFolder buscar.
ms.openlocfilehash: 4dd23b45dcc397e29e67fc08b29dd773e50f0db1
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836688"
---
# <a name="parentfolderids"></a>ParentFolderIds

El elemento **ParentFolderIds** identifica las carpetas para las operaciones FindItem y FindFolder buscar. 
  
```xml
<ParentFolderIds>
   <DistinguishedFolderId/>
<ParentFolderIds>
```

**NonEmptyArrayOfBaseFolderIdsType**

## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[FolderId](folderid.md) <br/> |Contiene el identificador y cambiar la clave de una carpeta. El elemento **ParentFolderIds** debe usar este elemento o el elemento [DistinguishedFolderId](distinguishedfolderid.md) .  <br/> |
|[DistinguishedFolderId](distinguishedfolderid.md) <br/> |Identifica las carpetas de Microsoft Exchange Server 2007 que se pueden hacer referencia por su nombre. El elemento **ParentFolderIds** debe usar este elemento o el elemento [FolderId](folderid.md) .  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[FindFolder](findfolder.md) <br/> |Define una solicitud para identificar las carpetas de un buzón de correo.  <br/> |
|[FindItem](finditem.md) <br/> |Define una solicitud para buscar elementos en un buzón de correo.  <br/> |
|[ResolveNames](resolvenames.md) <br/> |Define una solicitud para resolver nombres ambiguos.  <br/> |
   
## <a name="remarks"></a>Comentarios

El elemento **ParentFolderIds** debe usar el [FolderId](folderid.md) o el elemento [DistinguishedFolderId](distinguishedfolderid.md) . Puede definirse un número ilimitado de carpetas para la búsqueda. 
  
## <a name="example"></a>Ejemplo

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <FindFolder Traversal="Shallow" xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Vea también

- [Operación FindFolder](findfolder-operation.md)  
- [Operación FindItem](finditem-operation.md) 
- [Operación ResolveNames](resolvenames-operation.md)

