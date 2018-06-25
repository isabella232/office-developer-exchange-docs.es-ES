---
title: HasChanged
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 15ff513d-f39e-44ed-a13f-ab3f86fa37e1
description: El elemento HasChanged indica si ha cambiado la foto de un usuario.
ms.openlocfilehash: b0129e3d3acb43ada16a824e3d21706999d7053c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19835802"
---
# <a name="haschanged"></a>HasChanged

El elemento **HasChanged** indica si ha cambiado la foto de un usuario. 
  
```XML
<HasChanged> true | false </HasChanged>
```

 ****
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

[GetUserPhotoResponse](getuserphotoresponse.md)
  
## <a name="text-value"></a>Valor de texto

Un valor de texto de **true** para el elemento **HasChanged** indica que la foto ha cambiado desde la última vez que se ha devuelto. Un valor de **false** indica que la foto no ha cambiado desde la última vez que se ha devuelto. 
  
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> ||
   

