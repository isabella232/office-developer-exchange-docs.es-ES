---
title: MinimumSize
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 841d229c-140c-48bd-b3a7-21478fcea2fb
description: El elemento MinimumSize representa el tamaño mínimo que debe tener un mensaje para que se aplique la condición o excepción.
ms.openlocfilehash: c3f1284a5a82731093863b0a621bcf2f7f55cf22
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59540653"
---
# <a name="minimumsize"></a>MinimumSize

El **elemento MinimumSize** representa el tamaño mínimo que debe tener un mensaje para que se aplique la condición o excepción. 
  
```XML
<MinimumSize/>
```

 **int**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[WithinSizeRange](withinsizerange.md) <br/> |Especifica los tamaños mínimos y máximos que deben tener los mensajes entrantes para que se aplique la condición o excepción.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto es un entero que identifica el tamaño mínimo del mensaje en bytes.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Verdadero  <br/> |
   
## <a name="see-also"></a>Ver también



[MaximumSize](maximumsize.md)


- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

