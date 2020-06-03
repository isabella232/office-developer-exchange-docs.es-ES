---
title: SavedItemFolderId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SavedItemFolderId
api_type:
- schema
ms.assetid: 4b8b475c-9ca5-48c9-acb0-8848b53be1ce
description: El elemento SavedItemFolderId identifica la carpeta de destino para las operaciones que actualizan, envían y crean elementos en un buzón.
ms.openlocfilehash: 8e18b8863a54aa4e9d6e65f7a54e20904f5a9599
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465278"
---
# <a name="saveditemfolderid"></a>SavedItemFolderId

El elemento **SavedItemFolderId** identifica la carpeta de destino para las operaciones que actualizan, envían y crean elementos en un buzón. 
  
```xml
<SavedItemFolderId>
   <FolderId/>
</SavedItemFolderId>
```

```xml
<SavedItemFolderId>
   <DistinguishedFolderId/>
</SavedItemFolderId>
```

**TargetFolderIdType**

## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[FolderId](folderid.md) <br/> |Contiene el identificador y la clave de cambio de una carpeta de destino para las operaciones que actualizan, envían y crean elementos en el almacén de Exchange.  <br/> |
|[DistinguishedFolderId](distinguishedfolderid.md) <br/> |Identifica una carpeta de destino mediante un identificador con nombre para las operaciones que actualizan, envían y crean elementos en el almacén de Exchange.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[CreateItem](createitem.md) <br/> |Define una solicitud para crear un elemento en el almacén de Exchange.  <br/> La siguiente es la expresión XPath a este elemento:  <br/>  `/CreateItem` <br/> |
|[UpdateItem](updateitem.md) <br/> |Define una solicitud para actualizar un elemento en el almacén de Exchange.  <br/> La siguiente es la expresión XPath a este elemento:  <br/>  `/UpdateItem` <br/> |
|[SendItem](senditem.md) <br/> |Define una solicitud para enviar un elemento en el almacén de Exchange.  <br/> La siguiente es la expresión XPath a este elemento:  <br/>  `/SendItem` <br/> |
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   

