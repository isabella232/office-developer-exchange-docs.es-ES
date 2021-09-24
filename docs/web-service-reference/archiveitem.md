---
title: ArchiveItem
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: c2172e61-876a-4f76-bc9c-263c8be11429
description: El elemento ArchiveItem contiene el identificador de carpeta de origen y una matriz de identificadores de elemento para el elemento de archivo asociado.
ms.openlocfilehash: 876c86321c688e20fc3b5539c542bc46e67ba343
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59525298"
---
# <a name="archiveitem"></a>ArchiveItem

El **elemento ArchiveItem** contiene el identificador de carpeta de origen y una matriz de identificadores de elemento para el elemento de archivo asociado. 
  
```XML
<ArchiveItem>
   <ArchiveSourceFolderId/>
   <ItemIds/>
</ArchiveItem>
```

 **ArchiveItemType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

[ArchiveSourceFolderId](archivesourcefolderid.md)  |  [ItemIds](itemids.md)
  
### <a name="parent-elements"></a>Elementos principales

Ninguno.
  
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre del esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |messages.xsd  <br/> |
|Puede estar vacío  <br/> |false  <br/> |
   

