---
title: IndexedFieldURI
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IndexedFieldURI
api_type:
- schema
ms.assetid: 5c9cd0b5-7eca-480a-8730-fe98b1779afa
description: El elemento IndexedFieldURI identifica a los miembros individuales de un diccionario.
ms.openlocfilehash: f794d9970590417d916925f7258b28d4f0920d0e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467021"
---
# <a name="indexedfielduri"></a>IndexedFieldURI

El elemento **IndexedFieldURI** identifica a los miembros individuales de un diccionario. 
  
```xml
<IndexedFieldURI FieldURI="" FieldIndex="" />
```

 **PathToIndexedFieldType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Descripción**|
|:-----|:-----|
|**FieldURI** <br/> |Identifica el diccionario que contiene el miembro que se va a devolver. Este atributo es obligatorio.  <br/> |
|**FieldIndex** <br/> |Identifica al miembro del diccionario que se debe devolver. Este atributo es obligatorio.  <br/> |
   
#### <a name="fielduri-attribute"></a>Atributo FieldURI

|**Valor**|**Descripción**|
|:-----|:-----|
|elemento: InternetMessageHeader  <br/> |Representa el encabezado del mensaje de un elemento.  <br/> |
|contactos: direcciones  <br/> |Representa la dirección de mensajería instantánea de un contacto.  <br/> |
|contactos: PhysicalAddress: calle  <br/> |Representa la dirección postal de un contacto.  <br/> |
|contactos: PhysicalAddress: ciudad  <br/> |Representa la ciudad de un contacto.  <br/> |
|contactos: PhysicalAddress: estado  <br/> |Representa el estado de un contacto.  <br/> |
|contactos: PhysicalAddress: país  <br/> |Representa el país o la región de un contacto.  <br/> |
|contactos: PhysicalAddress: CódigoPostal  <br/> |Representa el código postal de un contacto.  <br/> |
|contactos: PhoneNumber  <br/> |Representa el número de teléfono de un contacto.  <br/> |
|contactos: EmailAddress  <br/> |Representa la dirección de correo electrónico de un contacto.  <br/> |
|DistributionList: miembros: miembro  <br/> |Representa un miembro de una lista de distribución.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[AdditionalProperties](additionalproperties.md) <br/> |Identifica las propiedades adicionales que se van a obtener, establecer o crear.  <br/> |
|[AggregateOn](aggregateon.md) <br/> |Representa la propiedad que se usa para determinar el orden de los elementos agrupados para un conjunto de resultados FindItem agrupados.  <br/> |
|[GroupBy](groupby.md) <br/> |Especifica una agrupación arbitraria para consultas FindItem.  <br/> |
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también



- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)

