---
title: EmailAddressAttributedValue
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ebdf224d-3796-4179-aa0a-87942e7585ff
description: El elemento EmailAddressAttributedValue especifica una instancia de una matriz de direcciones de correo electrónico y sus atribuciones asociados.
ms.openlocfilehash: 3bcbb5c0a2bc9a2dc24516b5fc62e6e3363a360b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764349"
---
# <a name="emailaddressattributedvalue"></a>EmailAddressAttributedValue

El elemento **EmailAddressAttributedValue** especifica una instancia de una matriz de direcciones de correo electrónico y sus atribuciones asociados. 
  
```XML
<EmailAddressAttributedValue>
    <Value></Value>
    <Attributions></Attributions>
<EmailAddressAttributedValue>
```

 **EmailAddressAttributedValueType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[Valor (EmailAddressType)](value-emailaddresstype.md) <br/> |Especifica que el valor de un **EmailAddress** asociado con una matriz de atribuciones.  <br/> |
|[Atribuciones (ArrayOfValueAttributionsType)](attributions-arrayofvalueattributionstype.md) <br/> |Especifica una matriz de atribuciones para su elemento de **valor** asociado.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[Emails1](emails1.md) <br/> |Especifica una matriz de valores de correo electrónico y los identificadores de sus atribuciones de origen para el rol asociado.  <br/> |
|[Emails2](emails2.md) <br/> |Especifica una matriz de valores de correo electrónico y los identificadores de sus atribuciones de origen para el rol asociado.  <br/> |
|[Emails3](emails3.md) <br/> |Especifica una matriz de valores de correo electrónico y los identificadores de sus atribuciones de origen para el rol asociado.  <br/> |
   
## <a name="remarks"></a>Notas

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipo  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> ||
   
## <a name="see-also"></a>Ver también



- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

