---
title: IsPermanentFailure
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 18dc3a97-cc0a-4092-934e-a6e86f52e668
description: El elemento IsPermanentFailure indica si un intento anterior de índice del elemento se ha realizado correctamente.
ms.openlocfilehash: 39592c15394a57e1c6aa1183ed0ccedeb085e6ea
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836085"
---
# <a name="ispermanentfailure"></a>IsPermanentFailure

El elemento **IsPermanentFailure** indica si un intento anterior de índice del elemento se ha realizado correctamente. 
  
```XML
<IsPermanentFailure>true | false</IsPermanentFailure>
```

 **Boolean**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

[NonIndexableItemDetail](nonindexableitemdetail.md)
  
## <a name="text-value"></a>Valor de texto

Un valor de texto de **true** para el elemento **IsPermanentFailure** indica que un intento anterior de índice del elemento de buzón de correo ha podido realizar. Un valor de **false** indica que un intento anterior de índice del elemento de buzón de correo se realizó correctamente. 
  
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |falso  <br/> |
   

