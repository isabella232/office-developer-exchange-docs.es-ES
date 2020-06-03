---
title: BlockExternalImages
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5c754dfc-a9e9-4272-9b5f-5fe3db537e62
description: El elemento BlockExternalImages especifica si las imágenes externas están bloqueadas en cuerpos de texto HTML.
ms.openlocfilehash: 73342316024ebe476a0e35f14157befc80edcf83
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44527407"
---
# <a name="blockexternalimages"></a>BlockExternalImages

El elemento **BlockExternalImages** especifica si las imágenes externas están bloqueadas en cuerpos de texto HTML. 
  
```XML
<BlockExternalImages> true | false </BlockExternalImages>
```

 **Boolean**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[FolderShape](foldershape.md) <br/> |Identifica las propiedades de carpeta que se incluirán en la respuesta GetFolder, FindFolder o SyncFolderHierarchy.  <br/> |
|[ItemShape](itemshape.md) <br/> |Identifica el contenido y las propiedades de los elementos que se van a incluir en una respuesta GetItem, FindItem o SyncFolderItems.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Un valor de texto de **true** para el elemento **BlockExternalImages** indica que las imágenes externas están bloqueadas en cuerpos HTML. Un valor de **false** indica que se permiten las imágenes externas. 
  
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipo  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> ||
   
## <a name="see-also"></a>Vea también



- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)

