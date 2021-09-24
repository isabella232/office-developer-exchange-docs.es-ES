---
title: HasChanged
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 15ff513d-f39e-44ed-a13f-ab3f86fa37e1
description: El elemento HasChanged indica si la foto de un usuario ha cambiado.
ms.openlocfilehash: 456660272815aac27ea99919eb92a02f754fb4ff
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59516793"
---
# <a name="haschanged"></a>HasChanged

El **elemento HasChanged** indica si la foto de un usuario ha cambiado. 
  
```XML
<HasChanged> true | false </HasChanged>
```

 ****
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

[GetUserPhotoResponse](getuserphotoresponse.md)
  
## <a name="text-value"></a>Valor de texto

Un valor de texto **de true** para el **elemento HasChanged** indica que la foto ha cambiado desde la última vez que se devolvió. Un valor de **false** indica que la foto no ha cambiado desde la última vez que se devolvió. 
  
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre del esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> ||
   

