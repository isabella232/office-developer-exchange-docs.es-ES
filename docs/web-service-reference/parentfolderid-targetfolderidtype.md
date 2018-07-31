---
title: ParentFolderId (TargetFolderIdType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ParentFolderId
api_type:
- schema
ms.assetid: 0e3e6e5f-06d0-499b-8ca4-d36036521658
description: El elemento ID identifica la carpeta en que se crea una nueva carpeta o la carpeta que se va a buscar la operación FindConversation.
ms.openlocfilehash: 8e80b9b342274a8b2004838ebd16f8425a2d3fa3
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/28/2018
ms.locfileid: "21353829"
---
# <a name="parentfolderid-targetfolderidtype"></a>ParentFolderId (TargetFolderIdType)

El elemento **ID** identifica la carpeta en que se crea una nueva carpeta o la carpeta que se va a buscar la [operación FindConversation](findconversation-operation.md).
  
```xml
<ParentFolderId>
   <DistinguishedFolderId/>
</ParentFolderId>
```

```xml
<ParentFolderId>
   <FolderId/> 
</ParentFolderId>
```

**TargetFolderIdType**

## <a name="attributes-and-elements"></a>Atributos y elementos

El elemento **ID** contiene dos elementos secundarios. Los elementos secundarios son mutuamente excluyentes en el esquema. 
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[FolderId](folderid.md) <br/> |Contiene el identificador requerido y la clave de cambio opcional de una carpeta en la que se crea una nueva carpeta o la carpeta que se va a buscar la [operación FindConversation](findconversation-operation.md). Uso de este elemento excluye el uso del elemento [DistinguishedFolderId](distinguishedfolderid.md) .  <br/> |
|[DistinguishedFolderId](distinguishedfolderid.md) <br/> |Identifica las carpetas predeterminadas de Microsoft Exchange Server 2007. Uso de este elemento excluye el uso del elemento [FolderId](folderid.md) .  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[CreateFolder](createfolder.md) <br/> |Define una solicitud para crear una carpeta en la base de datos de Exchange.  <br/> La siguiente es la expresión de XPath para este elemento:`/CreateFolder` <br/> |
|[FindConversation](findconversation.md) <br/> |Define una solicitud para buscar las conversaciones en un buzón de correo.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="remarks"></a>Comentarios

Los dos elementos secundarios se usan para definir la carpeta que contendrá la nueva carpeta. Debe seleccionar el [FolderId](folderid.md) o el elemento [DistinguishedFolderId](distinguishedfolderid.md) para identificar la carpeta principal de la nueva carpeta. No puede utilizar ambos elementos al mismo tiempo. Este elemento es necesario crear carpetas. 
  
El elemento [ID](parentfolderid.md) describe la ubicación de los elementos y las carpetas existentes. 
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensaje  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Vea también

- [Operación CreateFolder](createfolder-operation.md)
- [Operación FindConversation](findconversation-operation.md)
- [Creación de carpetas (servicios Web de Exchange)](http://msdn.microsoft.com/library/3b15b0ec-8691-45ed-9a24-a91ff732d6cf%28Office.15%29.aspx)

