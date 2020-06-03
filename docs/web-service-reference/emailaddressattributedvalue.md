---
title: EmailAddressAttributedValue
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ebdf224d-3796-4179-aa0a-87942e7585ff
description: El elemento EmailAddressAttributedValue especifica una instancia de una matriz de direcciones de correo electrónico y sus atribuciones asociadas.
ms.openlocfilehash: 09fdd5921cef3d70a6da4b6d4d38f08834c5d482
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530694"
---
# <a name="emailaddressattributedvalue"></a>EmailAddressAttributedValue

El elemento **EmailAddressAttributedValue** especifica una instancia de una matriz de direcciones de correo electrónico y sus atribuciones asociadas. 
  
```XML
<EmailAddressAttributedValue>
    <Value></Value>
    <Attributions></Attributions>
<EmailAddressAttributedValue>
```

 **EmailAddressAttributedValueType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Valor (EmailAddressType)](value-emailaddresstype.md) <br/> |Especifica el valor de una **EmailAddress** asociada a una matriz de atribuciones.  <br/> |
|[Atribuciones (ArrayOfValueAttributionsType)](attributions-arrayofvalueattributionstype.md) <br/> |Especifica una matriz de atribuciones para su elemento de **valor** asociado.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Emails1](emails1.md) <br/> |Especifica una matriz de valores de correo electrónico y los identificadores de sus atribuciones de origen para el rol asociado.  <br/> |
|[Emails2](emails2.md) <br/> |Especifica una matriz de valores de correo electrónico y los identificadores de sus atribuciones de origen para el rol asociado.  <br/> |
|[Emails3](emails3.md) <br/> |Especifica una matriz de valores de correo electrónico y los identificadores de sus atribuciones de origen para el rol asociado.  <br/> |
   
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipo  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> ||
   
## <a name="see-also"></a>Vea también



- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)

