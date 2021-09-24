---
title: IndexedFieldURI
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IndexedFieldURI
api_type:
- schema
ms.assetid: 5c9cd0b5-7eca-480a-8730-fe98b1779afa
description: El elemento IndexedFieldURI identifica miembros individuales de un diccionario.
ms.openlocfilehash: 851d0d4296e926ab21e5bd1b842d5a215c27308a
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59539629"
---
# <a name="indexedfielduri"></a>IndexedFieldURI

El **elemento IndexedFieldURI** identifica miembros individuales de un diccionario. 
  
```xml
<IndexedFieldURI FieldURI="" FieldIndex="" />
```

 **PathToIndexedFieldType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Descripción**|
|:-----|:-----|
|**FieldURI** <br/> |Identifica el diccionario que contiene el miembro que se devolverá. Este atributo es obligatorio.  <br/> |
|**FieldIndex** <br/> |Identifica el miembro del diccionario que se devolverá. Este atributo es obligatorio.  <br/> |
   
#### <a name="fielduri-attribute"></a>Atributo FieldURI

|**Valor**|**Descripción**|
|:-----|:-----|
|item:InternetMessageHeader  <br/> |Representa el encabezado del mensaje de un elemento.  <br/> |
|contacts:ImAddress  <br/> |Representa la dirección de mensajería instantánea de un contacto.  <br/> |
|contacts:PhysicalAddress:Street  <br/> |Representa la dirección de calle de un contacto.  <br/> |
|contacts:PhysicalAddress:City  <br/> |Representa la ciudad de un contacto.  <br/> |
|contacts:PhysicalAddress:State  <br/> |Representa el estado de un contacto.  <br/> |
|contacts:PhysicalAddress:Country  <br/> |Representa el país o región de un contacto.  <br/> |
|contacts:PhysicalAddress:PostalCode  <br/> |Representa el código postal de un contacto.  <br/> |
|contacts:PhoneNumber  <br/> |Representa el número de teléfono de un contacto.  <br/> |
|contacts:EmailAddress  <br/> |Representa la dirección de correo electrónico de un contacto.  <br/> |
|distributionlist:Members:Member  <br/> |Representa un miembro de una lista de distribución.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[AdditionalProperties](additionalproperties.md) <br/> |Identifica propiedades adicionales para obtener, establecer o crear.  <br/> |
|[AggregateOn](aggregateon.md) <br/> |Representa la propiedad que se usa para determinar el orden de los elementos agrupados para un conjunto de resultados FindItem agrupado.  <br/> |
|[GroupBy](groupby.md) <br/> |Especifica una agrupación arbitraria para las consultas FindItem.  <br/> |
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también



- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

