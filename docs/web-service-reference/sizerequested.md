---
title: SizeRequested
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: e86f98b6-83b5-4530-80eb-dc5df42e2c62
description: El elemento SizeRequested contiene el tamaño de foto solicitado para una operación GetUserPhoto.
ms.openlocfilehash: 799869a85d7f72e79753a73f9c259388a2702bf5
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59545919"
---
# <a name="sizerequested"></a>SizeRequested

El **elemento SizeRequested** contiene el tamaño de foto solicitado para una **operación GetUserPhoto.** 
  
```XML
<SizeRequested>HR48x48 | HR64x64 | HR96X96 | HR120X120 | HR240X240 | HR360X360 | HR432X432 | HR504X504 | HR648X648</SizeRequested>
```

 **UserPhotoSizeType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

[GetUserPhoto](getuserphoto.md)
  
## <a name="text-value"></a>Valor de texto

El valor de texto del **elemento SizeRequested** es el tamaño de foto solicitado de una imagen digital devuelta desde el servidor. En la tabla siguiente se identifican los valores de texto del **elemento SizeRequested.** 
  
|**Valor**|**Significado**|
|:-----|:-----|
|HR48x48  <br/> |La imagen tiene 48 píxeles de alto y 48 píxeles de ancho.  <br/> |
|HR64x64  <br/> |La imagen tiene 64 píxeles de alto y 64 píxeles de ancho.  <br/> |
|HR96x96  <br/> |La imagen tiene 96 píxeles de alto y 96 píxeles de ancho.  <br/> |
|HR120x120  <br/> |La imagen tiene 120 píxeles de alto y 120 píxeles de ancho.  <br/> |
|HR240x240  <br/> |La imagen tiene 240 píxeles de alto y 240 píxeles de ancho.  <br/> |
|HR360x360  <br/> |La imagen tiene 360 píxeles de alto y 360 píxeles de ancho.  <br/> |
|HR432x432  <br/> |La imagen tiene 432 píxeles de alto y 432 píxeles de ancho.  <br/> |
|HR504x504  <br/> |La imagen tiene 504 píxeles de alto y 504 píxeles de ancho.  <br/> |
|HR648x648  <br/> |La imagen tiene 648 píxeles de alto y 648 píxeles de ancho.  <br/> |
   
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
   

