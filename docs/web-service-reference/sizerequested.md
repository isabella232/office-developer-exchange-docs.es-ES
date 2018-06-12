---
title: SizeRequested
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: e86f98b6-83b5-4530-80eb-dc5df42e2c62
description: El elemento SizeRequested contiene el tamaño de la foto solicitado para una operación de GetUserPhoto.
ms.openlocfilehash: 43e422512b1e8f06e410e533e9ae1dc49283d5f6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19837504"
---
# <a name="sizerequested"></a>SizeRequested

El elemento **SizeRequested** contiene el tamaño de la foto solicitado para una operación de **GetUserPhoto** . 
  
```XML
<SizeRequested>HR48x48 | HR64x64 | HR96X96 | HR120X120 | HR240X240 | HR360X360 | HR432X432 | HR504X504 | HR648X648</SizeRequested>
```

 **UserPhotoSizeType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

[GetUserPhoto](getuserphoto.md)
  
## <a name="text-value"></a>Valor de texto

El valor de texto del elemento **SizeRequested** es el tamaño de la foto solicitado de una imagen digital devuelto desde el servidor. En la siguiente tabla identifica los valores de texto para el elemento **SizeRequested** . 
  
|**Valor**|**Significado**|
|:-----|:-----|
|HR48x48  <br/> |La imagen es 48 píxeles de alto y 48 píxeles de ancho.  <br/> |
|HR64x64  <br/> |La imagen es de 64 píxeles de alto y ancho de 64 píxeles.  <br/> |
|HR96x96  <br/> |La imagen es de 96 píxeles de alto y 96 píxeles de ancho.  <br/> |
|HR120x120  <br/> |La imagen es 120 píxeles de alto y 120 píxeles de ancho.  <br/> |
|HR240x240  <br/> |La imagen es 240 píxeles de alto y ancho de 240 píxeles.  <br/> |
|HR360x360  <br/> |La imagen es 360 píxeles de alto y 360 píxeles de ancho.  <br/> |
|HR432x432  <br/> |La imagen es 432 píxeles de alto y 432 píxeles de ancho.  <br/> |
|HR504x504  <br/> |La imagen es de 504 píxeles de alto y ancho de 504 píxeles.  <br/> |
|HR648x648  <br/> |La imagen es 648 píxeles de alto y 648 píxeles de ancho.  <br/> |
   
## <a name="remarks"></a>Notas

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> ||
   

