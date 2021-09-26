---
title: CreateFolderPath
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 282576cb-a921-49f7-8748-64158fd50c41
description: El elemento CreateFolderPath se usa para crear una ruta de acceso de carpeta e incluye un identificador de carpeta principal y una ruta de carpeta relativa.
ms.openlocfilehash: 603bdd0d7a36c169dfe48db02c3db0591fbe253b
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59543437"
---
# <a name="createfolderpath"></a>CreateFolderPath

El **elemento CreateFolderPath** se usa para crear una ruta de acceso de carpeta e incluye un identificador de carpeta principal y una ruta de carpeta relativa. 
  
```XML
<CreateFolderPath>
   <ParentFolderId/>
   <RelativeFolderPath/>
</CreateFolderPath>
```

 **CreateFolderPathType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

[ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md)  |  [RelativeFolderPath](relativefolderpath.md)
  
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
   

