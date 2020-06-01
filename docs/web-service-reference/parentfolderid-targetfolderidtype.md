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
description: El elemento ParentFolderId identifica la carpeta en la que se crea una nueva carpeta o la carpeta en la que se busca la operación FindConversation.
ms.openlocfilehash: 36e63266d10603c4d453a37e2b0d22e02599e516
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467805"
---
# <a name="parentfolderid-targetfolderidtype"></a>ParentFolderId (TargetFolderIdType)

El elemento **ParentFolderId** identifica la carpeta en la que se crea una nueva carpeta o la carpeta en la que se busca la [operación FindConversation](findconversation-operation.md).
  
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

El elemento **ParentFolderId** contiene dos elementos secundarios. Los elementos secundarios se excluyen mutuamente en el esquema. 
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[FolderId](folderid.md) <br/> |Contiene el identificador necesario y la clave de cambio opcional de una carpeta en la que se crea una nueva carpeta o la carpeta en la que se busca la [operación FindConversation](findconversation-operation.md). El uso de este elemento excluye el uso del elemento [DistinguishedFolderId](distinguishedfolderid.md) .  <br/> |
|[DistinguishedFolderId](distinguishedfolderid.md) <br/> |Identifica las carpetas predeterminadas de Microsoft Exchange Server 2007. El uso de este elemento excluye el uso del elemento [FolderId](folderid.md) .  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[CreateFolder](createfolder.md) <br/> |Define una solicitud para crear una carpeta en la base de datos de Exchange.  <br/> La siguiente es la expresión XPath a este elemento:`/CreateFolder` <br/> |
|[FindConversation](findconversation.md) <br/> |Define una solicitud para buscar conversaciones en un buzón.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="remarks"></a>Comentarios

Los dos elementos secundarios se usan para definir la carpeta que contendrá la nueva carpeta. Debe seleccionar el elemento [FolderId](folderid.md) o el elemento [DistinguishedFolderId](distinguishedfolderid.md) para identificar la carpeta principal de la nueva carpeta. No se pueden usar ambos elementos al mismo tiempo. Este elemento es necesario para crear carpetas. 
  
El elemento [ParentFolderId](parentfolderid.md) describe la ubicación de los elementos y las carpetas existentes. 
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también

- [Operación CreateFolder](createfolder-operation.md)
- [Operación FindConversation](findconversation-operation.md)
- [Creación de carpetas (servicios Web de Exchange)](https://msdn.microsoft.com/library/3b15b0ec-8691-45ed-9a24-a91ff732d6cf%28Office.15%29.aspx)

