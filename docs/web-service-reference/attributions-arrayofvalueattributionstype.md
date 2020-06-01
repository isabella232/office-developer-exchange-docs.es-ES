---
title: Atribuciones (ArrayOfValueAttributionsType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 7f36b6ee-8ecf-48c9-8cb6-dfb2da0ce2a2
description: El elemento atribuciones especifica una matriz de atribuciones para su elemento de valor asociado.
ms.openlocfilehash: 9fd552670c529009838125063869f65e130c1e63
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463996"
---
# <a name="attributions-arrayofvalueattributionstype"></a>Atribuciones (ArrayOfValueAttributionsType)

El elemento **atribuciones** especifica una matriz de atribuciones para su elemento de **valor** asociado. 
  
```XML
<Attributions>
    <Attribution></Attribution>
</Attribution>
```

 **ArrayOfValueAttributionsType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Atribución (cadena)](attribution-string.md) <br/> |Especifica una cadena que se usa para identificar un atributo.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[BodyContentAttributedValue](bodycontentattributedvalue.md) <br/> |Especifica el contenido del cuerpo de un elemento.  <br/> |
|[EmailAddressAttributedValue](emailaddressattributedvalue.md) <br/> |Especifica una instancia de una matriz de direcciones de correo electrónico y sus atribuciones asociadas.  <br/> |
|[ExtendedPropertyAttributedValue](extendedpropertyattributedvalue.md) <br/> |Especifica las propiedades extendidas de un rol.  <br/> |
|[PhoneNumberAttributedValue](phonenumberattributedvalue.md) <br/> |Especifica una instancia de una matriz de números de teléfono y sus atribuciones asociadas.  <br/> |
|[PostalAddressAttributedValue](postaladdressattributedvalue.md) <br/> |Especifica una instancia de una matriz de direcciones postales y sus atribuciones asociadas.  <br/> |
|[StringArrayAttributedValue](stringarrayattributedvalue.md) <br/> |Especifica una instancia de una matriz de datos de cadena para un elemento de rol.  <br/> |
|[StringAttributedValue](stringattributedvalue.md) <br/> |Especifica una instancia de una matriz de atributos asociada a un elemento de rol.  <br/> |
   
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

