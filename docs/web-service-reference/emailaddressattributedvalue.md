---
title: EmailAddressAttributedValue
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: ebdf224d-3796-4179-aa0a-87942e7585ff
description: El elemento EmailAddressAttributedValue especifica una instancia de una matriz de direcciones de correo electrónico y sus atribuciones asociadas.
ms.openlocfilehash: 2b5e9b431b6a62c63e815bfee190c923f454c867
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59519768"
---
# <a name="emailaddressattributedvalue"></a>EmailAddressAttributedValue

El **elemento EmailAddressAttributedValue** especifica una instancia de una matriz de direcciones de correo electrónico y sus atribuciones asociadas. 
  
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

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Value (EmailAddressType)](value-emailaddresstype.md) <br/> |Especifica el valor de un **EmailAddress asociado** a una matriz de atribuciones.  <br/> |
|[Attributions (ArrayOfValueAttributionsType)](attributions-arrayofvalueattributionstype.md) <br/> |Especifica una matriz de atribuciones para su elemento **Value** asociado.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Emails1](emails1.md) <br/> |Especifica una matriz de valores de correo electrónico y los identificadores de sus atribuciones de origen para la persona asociada.  <br/> |
|[Emails2](emails2.md) <br/> |Especifica una matriz de valores de correo electrónico y los identificadores de sus atribuciones de origen para la persona asociada.  <br/> |
|[Emails3](emails3.md) <br/> |Especifica una matriz de valores de correo electrónico y los identificadores de sus atribuciones de origen para la persona asociada.  <br/> |
   
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipo  <br/> |
|Archivo de validación  <br/> |types.xsd  <br/> |
|Puede estar vacío  <br/> ||
   
## <a name="see-also"></a>Ver también



- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

