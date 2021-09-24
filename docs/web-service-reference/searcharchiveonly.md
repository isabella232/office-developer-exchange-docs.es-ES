---
title: SearchArchiveOnly
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: cce5344c-b622-44d4-bc14-a0de346c9335
description: El elemento SearchArchiveOnly indica si solo se busca en el buzón de archivo elementos no indizables.
ms.openlocfilehash: a4766e101394bb83a0dcebdfe5b92f576f4a4160
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59521685"
---
# <a name="searcharchiveonly"></a>SearchArchiveOnly

El **elemento SearchArchiveOnly** indica si solo se busca en el buzón de archivo elementos no indizables. 
  
```xml
<SearchArchiveOnly>true | false</SearchArchiveOnly>
```

 **Boolean**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

[GetNonIndexableItemStatistics](getnonindexableitemstatistics.md) → [GetNonIndexableItemDetails](getnonindexableitemdetails.md)
  
## <a name="text-value"></a>Valor de texto

Un valor de texto **de true** para el **elemento SearchArchiveOnly** indica que la búsqueda de elementos no indizables solo se realiza en el buzón de archivo. Un valor de texto de **false** indica que la búsqueda se realiza en el buzón principal y el buzón de archivo. 
  
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre del esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> ||
   

