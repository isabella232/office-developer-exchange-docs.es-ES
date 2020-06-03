---
title: ConvertHtmlCodePageToUTF8
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f02c8331-0a4e-4d01-adc2-2b93ed838a42
description: El elemento ConvertHtmlCodePageToUTF8 indica si el cuerpo HTML del elemento se convierte en UTF8.
ms.openlocfilehash: a714eacd8cc105146a1471f062ec35dc16730d61
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457595"
---
# <a name="converthtmlcodepagetoutf8"></a>ConvertHtmlCodePageToUTF8

El elemento **ConvertHtmlCodePageToUTF8** indica si el cuerpo HTML del elemento se convierte en UTF8. 
  
```XML
<ConvertHtmlCodePageToUTF8/>
```

 **XS: Boolean**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[ItemShape](itemshape.md) <br/> |Identifica un conjunto de propiedades que se devolverán en una respuesta.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Un valor de texto de **true** para el elemento **ConvertHtmlCodePageToUTF8** indica que el cuerpo HTML se convierte en UTF8. Un valor de texto de **false** indica que el cuerpo HTML no se convierte en UTF8. 
  
## <a name="remarks"></a>Comentarios

El valor predeterminado de **true** se usa si no se especifica el elemento **ConvertHtmlCodePageToUTF8** en una solicitud. 
  
El esquema que describe este elemento se encuentra en el directorio virtual de IIS que hospeda los servicios Web de Exchange. este elemento se introdujo en Exchange Server 2010 Service Pack 1 (SP1).
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también



- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)

