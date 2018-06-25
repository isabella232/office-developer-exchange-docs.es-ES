---
title: NormalizedBodyType
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c6973aee-ec7b-44c1-b328-f2204d9de5d1
description: El elemento NormalizedBodyType especifica si el cuerpo normalizado se devuelve en formato de texto o HTML.
ms.openlocfilehash: 33575594b22f972a9eb762dfac884fa91459f04a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836554"
---
# <a name="normalizedbodytype"></a>NormalizedBodyType

El elemento **NormalizedBodyType** especifica si el cuerpo normalizado se devuelve en formato de texto o HTML. 
  
```XML
<NormalizedBodyType> Best | HTML | Text </NormalizedBodyType>
```

 **BodyTypeResponseType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

[ItemShape](itemshape.md)
  
## <a name="text-value"></a>Valor de texto

El valor de texto del elemento **NormalizedBodyType** indica el formato del cuerpo normalizado se devuelve en. En la siguiente tabla se enumera los valores posibles para este elemento. 
  
****

|**Valor**|**Descripción**|
|:-----|:-----|
|Mejor  <br/> |La respuesta devolverá el contenido disponible más completa del texto del cuerpo. Esto es útil si se desconoce si el contenido es texto o HTML.  <br/> El cuerpo devuelto será texto si el cuerpo almacenado es texto sin formato. De lo contrario, la respuesta devolverá HTML si se encuentra el cuerpo almacenado en formato HTML o RTF.  <br/> Éste es el valor predeterminado.  <br/> |
|HTML  <br/> |La respuesta devolverá un cuerpo normalizado como HTML.  <br/> |
|Texto  <br/> |La respuesta devolverá un cuerpo normalizado como texto sin formato.  <br/> |
   
## <a name="remarks"></a>Comentarios

Este elemento se incorporó en Exchange Server 2013 Service Pack 1 (SP1).
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Verdadero  <br/> |
   
## <a name="see-also"></a>Vea también



[ItemShape](itemshape.md)


- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

