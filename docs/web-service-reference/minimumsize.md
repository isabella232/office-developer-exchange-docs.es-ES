---
title: MinimumSize
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 841d229c-140c-48bd-b3a7-21478fcea2fb
description: El elemento MinimumSize representa el tamaño mínimo que debe tener un mensaje para que se aplique la condición o excepción.
ms.openlocfilehash: b43a8b5916747c4e3e4ca9b66cf8b9d73f5f8942
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/01/2020
ms.locfileid: "44464206"
---
# <a name="minimumsize"></a>MinimumSize

El elemento **MinimumSize** representa el tamaño mínimo que debe tener un mensaje para que se aplique la condición o excepción. 
  
```XML
<MinimumSize/>
```

 **int**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[WithinSizeRange](withinsizerange.md) <br/> |Especifica los tamaños máximos y mínimos que los mensajes entrantes deben tener en orden para que se aplique la condición o excepción.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto es un número entero que identifica el tamaño mínimo del mensaje en bytes.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages. xsd  <br/> |
|Puede estar vacío  <br/> |Verdadero  <br/> |
   
## <a name="see-also"></a>Vea también



[Tamañomáximo](maximumsize.md)


- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)

