---
title: ArchiveSourceFolderId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d5b6a099-3b87-44ef-a197-8198730ff72d
description: El elemento ArchiveSourceFolderId especifica el identificador de la carpeta de origen para el elemento de archivo.
ms.openlocfilehash: 403f40cb4529cf72f07b8a04c0803d757c24e470
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463387"
---
# <a name="archivesourcefolderid"></a>ArchiveSourceFolderId

El elemento **ArchiveSourceFolderId** especifica el identificador de la carpeta de origen para el elemento de archivo. 
  
```XML
<ArchiveSourceFolderId>
   <FolderId/>
   <DistinguishedFolderId/>
   <AddressListId/>
</ArchiveSourceFolderId>
```

 **TargetFolderIdType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

[FolderId](folderid.md)  |  [DistinguishedFolderId](distinguishedfolderid.md)  |  [AddressListId](addresslistid.md)
  
### <a name="parent-elements"></a>Elementos principales

[ArchiveItem](archiveitem.md)
  
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |messages. xsd  <br/> |
|Puede estar vacío  <br/> |false  <br/> |
   

