---
title: Contains
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Contains
api_type:
- schema
ms.assetid: 476d059d-c243-43e9-b475-319fc413ade2
description: El elemento contiene representa una expresión de búsqueda que determina si una propiedad determinada contiene el valor de cadena constante proporcionada.
ms.openlocfilehash: 083efdf32cd32bea6964361b5b558480aa937280
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763816"
---
# <a name="contains"></a>Contains

El elemento **contiene** representa una expresión de búsqueda que determina si una propiedad determinada contiene el valor de cadena constante proporcionada. 
  
```xml
<Contains ContainmentMode="" ContainmentComparison="">
   <FieldURI/>
   <Constant/>
</Contains>
```

 **ContainsExpressionType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Attribute**|**Descripción**|
|:-----|:-----|
|**ContainmentMode** <br/> |Identifica los límites de una búsqueda.  <br/> |
|**ContainmentComparison** <br/> |Determina si la búsqueda omite los casos y espacios.  <br/> |
   
#### <a name="containmentmode-attribute-values"></a>Valores de atributo de ContainmentMode

|**Valor**|**Descripción**|
|:-----|:-----|
|FullString  <br/> |Es la comparación entre la cadena completa y la constante. El valor de la propiedad y la constante suministrada están exactamente el mismo.  <br/> |
|El prefijo  <br/> |La comparación es entre el prefijo de la cadena y la constante.  <br/> |
|Subcadena  <br/> |La comparación es entre una subcadena de la cadena y la constante.  <br/> |
|PrefixOnWords  <br/> |La comparación es entre un prefijo en palabras individuales en la cadena y la constante.  <br/> |
|ExactPhrase  <br/> |La comparación es entre una frase exacta en la cadena y la constante.  <br/> |
   
#### <a name="containmentcomparison-attribute-values"></a>Valores de atributo de ContainmentComparison

|**Valor**|**Descripción**|
|:-----|:-----|
|Exact  <br/> |La comparación debe ser exacta.  <br/> |
|IgnoreCase  <br/> |La comparación pasa por alto las mayúsculas y minúsculas.  <br/> |
|IgnoreNonSpacingCharacters  <br/> |La comparación pasa por alto caracteres sin espacios.  <br/> |
|Separada  <br/> |Va a quitar.  <br/> |
|IgnoreCaseAndNonSpacingCharacters  <br/> |La comparación omite mayúsculas y que no sean de espaciado entre caracteres.  <br/> |
|LooseAndIgnoreCase  <br/> |Va a quitar.  <br/> |
|LooseAndIgnoreNonSpace  <br/> |Va a quitar.  <br/> |
|LooseAndIgnoreCaseAndIgnoreNonSpace  <br/> |Va a quitar.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[FieldURI](fielduri.md) <br/> |Identifica las propiedades con frecuencia que se hace referencia mediante un identificador URI.  <br/> |
|[IndexedFieldURI](indexedfielduri.md) <br/> |Identifica a los miembros individuales de un diccionario.  <br/> |
|[ExtendedFieldURI](extendedfielduri.md) <br/> |Identifica las propiedades MAPI.  <br/> |
|[Constante](constant.md) <br/> |Identifica un valor constante en una restricción.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[Restriction](restriction.md) <br/> |Representa la restricción o la consulta que se usa para filtrar los elementos o carpetas en las operaciones de carpeta FindItem/FindFolder y búsqueda.  <br/> |
|[No](not.md) <br/> |Representa una expresión de búsqueda que niega el valor booleano de la expresión de búsqueda que contiene.  <br/> |
|[And](and.md) <br/> |Representa una expresión de búsqueda que le permite realizar una operación de tipo Boolean y entre dos o más expresiones de búsqueda. El resultado de la operación And es **true** si se **cumplen**todas las expresiones de búsqueda incluidas en el y.  <br/> |
|[Or](or.md) <br/> |Representa una expresión de búsqueda que se realiza una operación OR lógica en la expresión de búsqueda que contiene. El elemento [o](or.md) devolverá **true** si cualquiera de sus elementos secundarios que devuelva **true**.  <br/> |
   
## <a name="remarks"></a>Comentarios

Los atributos se utilizan para determinar cómo se comparan los elementos.
  
El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Vea también



- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

