---
title: Excluye
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Excludes
api_type:
- schema
ms.assetid: bbaeddf6-9a67-4ee0-af99-7a7a5bbdc0e1
description: El elemento excluye realiza una máscara de bit a bit de la propiedad especificada y un valor suministrado.
ms.openlocfilehash: 73e4eb782a4f54c113ea9a9b67fcf185a9028153
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764481"
---
# <a name="excludes"></a>Excluye

El elemento **excluye** realiza una máscara de bit a bit de la propiedad especificada y un valor suministrado. 
  
```xml
<Excludes>
   <FieldURI/>
   <Bitmask/>
</Excludes>
```

 **ExcludesType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[FieldURI](fielduri.md) <br/> |Identifica las propiedades con frecuencia que se hace referencia mediante un identificador URI.  <br/> |
|[IndexedFieldURI](indexedfielduri.md) <br/> |Identifica a los miembros individuales de un diccionario.  <br/> |
|[ExtendedFieldURI](extendedfielduri.md) <br/> |Identifica las propiedades MAPI.  <br/> |
|[Máscara de bits](bitmask.md) <br/> |Representa una máscara de hexadecimal o decimal que se utilizará durante una operación de restricción [excluye](excludes.md) . Si la máscara de bits representa un número hexadecimal, deben ir precedido por 0 x o 0 X. De lo contrario, se considerará un número decimal.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[Restriction](restriction.md) <br/> |Representa la restricción o la consulta que se usa para filtrar los elementos o carpetas en las operaciones de carpeta FindItem/FindFolder y búsqueda.  <br/> |
|[No](not.md) <br/> |Representa una expresión de búsqueda que niega el valor booleano de la expresión de búsqueda que contiene.  <br/> |
|[And](and.md) <br/> |Representa una expresión de búsqueda que le permite realizar una operación de tipo Boolean y entre dos o más expresiones de búsqueda. El resultado de la operación And es **true** si se **cumplen**todas las expresiones de búsqueda incluidas en el y.  <br/> |
|[Or](or.md) <br/> |Representa una expresión de búsqueda que se realiza una operación OR lógica en la expresión de búsqueda que contiene. El elemento [o](or.md) devolverá **true** si cualquiera de sus elementos secundarios que devuelva **true**.  <br/> |
   
## <a name="remarks"></a>Notas

 **Excluye** se puede resolver en **true** si y realizada una operación en la siguiente se resuelve en 0: 
  
1. El valor de la propiedad bit a bit
    
2. El valor de máscara de bits para la propiedad
    
 **Excluye** solo se puede aplicar a una propiedad que tiene un valor entero. Si el tipo de propiedad no es un entero, se devuelve un código de error de **ErrorUnsupportedPathForQuery** en la respuesta. 
  
Puede realizar la operación inversa mediante una llamada a Not(Excludes).
  
El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Ver también



- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

