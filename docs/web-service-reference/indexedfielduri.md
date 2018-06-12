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
ms.openlocfilehash: 6a75e8855ecabf15ca31bb1e05d569c258a43b0b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19835909"
---
# <a name="indexedfielduri"></a>IndexedFieldURI

El elemento **IndexedFieldURI** identifica a los miembros individuales de un diccionario. 
  
```xml
<IndexedFieldURI FieldURI="" FieldIndex="" />
```

 **PathToIndexedFieldType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Attribute**|**Descripción**|
|:-----|:-----|
|**FieldURI** <br/> |Identifica el diccionario que contiene el miembro para devolver. Este atributo es necesario.  <br/> |
|**FieldIndex** <br/> |Identifica el miembro del diccionario para devolver. Este atributo es necesario.  <br/> |
   
#### <a name="fielduri-attribute"></a>Atributo FieldURI

|**Valor**|**Descripción**|
|:-----|:-----|
|elemento: InternetMessageHeader  <br/> |Representa el encabezado del mensaje de un elemento.  <br/> |
|contactos: ImAddress  <br/> |Representa la dirección de un contacto de mensajería instantánea.  <br/> |
|contactos: PhysicalAddress:Street  <br/> |Representa la dirección de un contacto.  <br/> |
|contactos: PhysicalAddress:City  <br/> |Representa la ciudad de un contacto.  <br/> |
|contactos: PhysicalAddress:State  <br/> |Representa el estado de un contacto.  <br/> |
|contactos: PhysicalAddress:Country  <br/> |Representa el país o región de un contacto.  <br/> |
|contactos: PhysicalAddress:PostalCode  <br/> |Representa el código postal de un contacto.  <br/> |
|contactos: PhoneNumber  <br/> |Representa el número de teléfono de un contacto.  <br/> |
|contactos: EmailAddress  <br/> |Representa la dirección de correo electrónico de un contacto.  <br/> |
|DistributionList:members:Member  <br/> |Representa a un miembro de una lista de distribución.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[AdditionalProperties](additionalproperties.md) <br/> |Identifica las propiedades adicionales para obtener, establecer o crear.  <br/> |
|[AggregateOn](aggregateon.md) <br/> |Representa la propiedad que se utiliza para determinar el orden de elementos agrupados en un conjunto de resultados FindItem agrupado.  <br/> |
|[GroupBy](groupby.md) <br/> |Especifica un agrupamiento arbitrario para consultas FindItem.  <br/> |
   
## <a name="remarks"></a>Notas

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Ver también



- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

