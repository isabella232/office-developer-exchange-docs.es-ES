---
title: MinimumSize
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 841d229c-140c-48bd-b3a7-21478fcea2fb
description: El elemento MinimumSize representa el tamaño mínimo que un mensaje debe estar en orden para la condición o la excepción que se debe aplicar.
ms.openlocfilehash: 4f80bac3b9226019ec3d726cd2d6430e02cac423
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836480"
---
# <a name="minimumsize"></a>MinimumSize

El elemento **MinimumSize** representa el tamaño mínimo que un mensaje debe estar en orden para la condición o la excepción que se debe aplicar. 
  
```XML
<MinimumSize/>
```

 **int**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[WithinSizeRange](withinsizerange.md) <br/> |Especifica los tamaños máximos y mínimos que deben ser los mensajes entrantes en orden para la condición o la excepción que se debe aplicar.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto es un entero que identifica el tamaño mínimo del mensaje en bytes.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Verdadero  <br/> |
   
## <a name="see-also"></a>Vea también



[MaximumSize](maximumsize.md)


- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

