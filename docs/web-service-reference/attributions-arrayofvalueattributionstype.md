---
title: Attributions (ArrayOfValueAttributionsType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 7f36b6ee-8ecf-48c9-8cb6-dfb2da0ce2a2
description: El elemento Atribuciones especifica una matriz de atribuciones para su elemento Value asociado.
ms.openlocfilehash: e5483e8e7ef4745e8025106ae1f1c52e91987183
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59529331"
---
# <a name="attributions-arrayofvalueattributionstype"></a>Attributions (ArrayOfValueAttributionsType)

El **elemento Atribuciones** especifica una matriz de atribuciones para su elemento **Value** asociado. 
  
```XML
<Attributions>
    <Attribution></Attribution>
</Attribution>
```

 **ArrayOfValueAttributionsType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Attribution (cadena)](attribution-string.md) <br/> |Especifica una cadena usada para identificar un atributo.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[BodyContentAttributedValue](bodycontentattributedvalue.md) <br/> |Especifica el contenido del cuerpo de un elemento.  <br/> |
|[EmailAddressAttributedValue](emailaddressattributedvalue.md) <br/> |Especifica una instancia de una matriz de direcciones de correo electrónico y sus atribuciones asociadas.  <br/> |
|[ExtendedPropertyAttributedValue](extendedpropertyattributedvalue.md) <br/> |Especifica propiedades extendidas para una persona.  <br/> |
|[PhoneNumberAttributedValue](phonenumberattributedvalue.md) <br/> |Especifica una instancia de una matriz de números de teléfono y sus atribuciones asociadas.  <br/> |
|[PostalAddressAttributedValue](postaladdressattributedvalue.md) <br/> |Especifica una instancia de una matriz de direcciones postales y sus atribuciones asociadas.  <br/> |
|[StringArrayAttributedValue](stringarrayattributedvalue.md) <br/> |Especifica una instancia de una matriz de datos de cadena para un elemento persona.  <br/> |
|[StringAttributedValue](stringattributedvalue.md) <br/> |Especifica una instancia en una matriz de atributos asociados con un elemento persona.  <br/> |
   
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

