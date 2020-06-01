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
ms.openlocfilehash: e5d968673403eba24a68c67175e3ebcbb35eca39
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462664"
---
# <a name="normalizedbodytype"></a>NormalizedBodyType

El elemento **NormalizedBodyType** especifica si el cuerpo normalizado se devuelve en formato de texto o HTML. 
  
```XML
<NormalizedBodyType> Best | HTML | Text </NormalizedBodyType>
```

 **BodyTypeResponseType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

[ItemShape](itemshape.md)
  
## <a name="text-value"></a>Valor de texto

El valor de texto del elemento **NormalizedBodyType** indica el formato en el que se devuelve el cuerpo normalizado. En la siguiente tabla se enumeran los valores posibles para este elemento. 
  
****

|**Valor**|**Descripción**|
|:-----|:-----|
|Procedimientos  <br/> |La respuesta devolverá el contenido más enriquecido disponible del texto del cuerpo. Esto es útil si es desconocido si el contenido es de texto o HTML.  <br/> El cuerpo devuelto será Text si el cuerpo almacenado es texto sin formato. De lo contrario, la respuesta devolverá HTML si el cuerpo almacenado está en formato HTML o RTF.  <br/> Este es el valor predeterminado.  <br/> |
|HTML  <br/> |La respuesta devolverá un cuerpo normalizado como HTML.  <br/> |
|Texto  <br/> |La respuesta devolverá un cuerpo normalizado como texto sin formato.  <br/> |
   
## <a name="remarks"></a>Comentarios

Este elemento se incorporó en Exchange Server 2013 Service Pack 1 (SP1).
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> |Verdadero  <br/> |
   
## <a name="see-also"></a>Vea también



[ItemShape](itemshape.md)


- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)

