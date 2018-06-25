---
title: Atribuciones (ArrayOfValueAttributionsType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 7f36b6ee-8ecf-48c9-8cb6-dfb2da0ce2a2
description: El elemento de atribuciones especifica una matriz de atribuciones para su elemento de valor asociado.
ms.openlocfilehash: a64510cacb9923682418ca8a9b203c765a129bdd
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763587"
---
# <a name="attributions-arrayofvalueattributionstype"></a>Atribuciones (ArrayOfValueAttributionsType)

El elemento de **atribuciones** especifica una matriz de atribuciones para su elemento de **valor** asociado. 
  
```XML
<Attributions>
    <Attribution></Attribution>
</Attribution>
```

 **ArrayOfValueAttributionsType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[Atribución (cadena)](attribution-string.md) <br/> |Especifica una cadena que se usa para identificar un atributo.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[BodyContentAttributedValue](bodycontentattributedvalue.md) <br/> |Especifica el contenido del cuerpo de un elemento.  <br/> |
|[EmailAddressAttributedValue](emailaddressattributedvalue.md) <br/> |Especifica una instancia de una matriz de direcciones de correo electrónico y sus atribuciones asociados.  <br/> |
|[ExtendedPropertyAttributedValue](extendedpropertyattributedvalue.md) <br/> |Especifica las propiedades extendidas para un rol.  <br/> |
|[PhoneNumberAttributedValue](phonenumberattributedvalue.md) <br/> |Especifica una instancia de una matriz de números de teléfono y sus atribuciones asociados.  <br/> |
|[PostalAddressAttributedValue](postaladdressattributedvalue.md) <br/> |Especifica una instancia de una matriz de direcciones postales y sus atribuciones asociados.  <br/> |
|[StringArrayAttributedValue](stringarrayattributedvalue.md) <br/> |Especifica una instancia de una matriz de datos de cadena de un elemento de la persona.  <br/> |
|[StringAttributedValue](stringattributedvalue.md) <br/> |Especifica una instancia de una matriz de atributos asociados con un elemento de la persona.  <br/> |
   
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipo  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> ||
   
## <a name="see-also"></a>Vea también

- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

