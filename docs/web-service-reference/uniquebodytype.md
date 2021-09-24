---
title: UniqueBodyType
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 8f7276aa-e354-40e4-b9cb-950fad46ac93
description: El elemento UniqueBodyType especifica si el cuerpo único se devuelve en formato HTML o texto.
ms.openlocfilehash: a0149e41da24646fdf38a465434bfad3557ece22
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59520272"
---
# <a name="uniquebodytype"></a>UniqueBodyType

El **elemento UniqueBodyType** especifica si el cuerpo único se devuelve en formato HTML o texto. 
  
```XML
<UniqueBodyType> Best | HTML | Text </UniqueBodyType>
```

 **BodyTypeResponseType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

[ItemShape](itemshape.md)
  
## <a name="text-value"></a>Valor de texto

El valor de texto del **elemento UniqueBodyType** indica el formato en el que se devuelve el cuerpo único. En la tabla siguiente se enumeran los valores posibles para este elemento. 
  
****

|**Valor**|**Descripción**|
|:-----|:-----|
|Procedimientos  <br/> |La respuesta devolverá el contenido más completo disponible del texto del cuerpo. Esto es útil si se desconoce si el contenido es texto o HTML.  <br/> El cuerpo devuelto será texto si el cuerpo almacenado es texto sin formato. De lo contrario, la respuesta devolverá HTML si el cuerpo almacenado está en formato HTML o RTF.  <br/> Este es el valor predeterminado.  <br/> |
|HTML  <br/> |La respuesta devolverá un cuerpo único como HTML.  <br/> |
|Texto  <br/> |La respuesta devolverá un cuerpo único como texto sin formato.  <br/> |
   
## <a name="remarks"></a>Comentarios

Este elemento se incorporó en Exchange Server 2013 Service Pack 1 (SP1).
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Verdadero  <br/> |
   
## <a name="see-also"></a>Ver también



[ItemShape](itemshape.md)


- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

