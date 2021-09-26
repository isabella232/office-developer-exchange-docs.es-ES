---
title: Contains
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Contains
api_type:
- schema
ms.assetid: 476d059d-c243-43e9-b475-319fc413ade2
description: El elemento Contains representa una expresión de búsqueda que determina si una propiedad determinada contiene el valor de cadena constante proporcionado.
ms.openlocfilehash: 6e36ede6a10c64a4aa53e68721d9edf7893c4c05
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59547550"
---
# <a name="contains"></a>Contains

El **elemento Contains** representa una expresión de búsqueda que determina si una propiedad determinada contiene el valor de cadena constante proporcionado. 
  
```xml
<Contains ContainmentMode="" ContainmentComparison="">
   <FieldURI/>
   <Constant/>
</Contains>
```

```xml
<Contains ContainmentMode="" ContainmentComparison="">
   <ExtendedFieldURI/>
   <Constant/>
</Contains>
```

```xml
<Contains ContainmentMode="" ContainmentComparison="">
   <IndexedFieldURI/>
   <Constant/>
</Contains>
```


**ContainsExpressionType**

## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Descripción**|
|:-----|:-----|
|**ContainmentMode** <br/> |Identifica los límites de una búsqueda.  <br/> |
|**ContainmentComparison** <br/> |Determina si la búsqueda omite casos y espacios.  <br/> |
   
#### <a name="containmentmode-attribute-values"></a>Valores de atributo ContainmentMode

|**Valor**|**Descripción**|
|:-----|:-----|
|FullString  <br/> |La comparación es entre la cadena completa y la constante. El valor de la propiedad y la constante suministrada son exactamente los mismos.  <br/> |
|Con prefijo  <br/> |La comparación es entre el prefijo de cadena y la constante.  <br/> |
|Subcadena  <br/> |La comparación es entre una subcadena de la cadena y la constante.  <br/> |
|PrefixOnWords  <br/> |La comparación es entre un prefijo de palabras individuales de la cadena y la constante.  <br/> |
|ExactPhrase  <br/> |La comparación es entre una frase exacta en la cadena y la constante.  <br/> |
   
#### <a name="containmentcomparison-attribute-values"></a>Valores de atributo ContainmentComparison

|**Valor**|**Descripción**|
|:-----|:-----|
|Exacto  <br/> |La comparación debe ser exacta.  <br/> |
|IgnoreCase  <br/> |La comparación omite mayúsculas de minúsculas.  <br/> |
|IgnoreNonSpacingCharacters  <br/> |La comparación omite los caracteres que no están espaciados.  <br/> |
|Separada  <br/> |Que se va a quitar.  <br/> |
|IgnoreCaseAndNonSpacingCharacters  <br/> |La comparación omite los caracteres de mayúsculas y minúsculas.  <br/> |
|LooseAndIgnoreCase  <br/> |Que se va a quitar.  <br/> |
|LooseAndIgnoreNonSpace  <br/> |Que se va a quitar.  <br/> |
|LooseAndIgnoreCaseAndIgnoreNonSpace  <br/> |Que se va a quitar.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[FieldURI](fielduri.md) <br/> |Identifica las propiedades a las que se hace referencia con frecuencia mediante URI.  <br/> |
|[IndexedFieldURI](indexedfielduri.md) <br/> |Identifica miembros individuales de un diccionario.  <br/> |
|[ExtendedFieldURI](extendedfielduri.md) <br/> |Identifica las propiedades MAPI.  <br/> |
|[Constante](constant.md) <br/> |Identifica un valor constante en una restricción.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Restriction](restriction.md) <br/> |Representa la restricción o consulta que se usa para filtrar elementos o carpetas en las operaciones FindItem/FindFolder y carpeta de búsqueda.  <br/> |
|[Not](not.md) <br/> |Representa una expresión de búsqueda que niega el valor booleano de la expresión de búsqueda que contiene.  <br/> |
|[And](and.md) <br/> |Representa una expresión de búsqueda que permite realizar una operación Boolean And entre dos o más expresiones de búsqueda. El resultado de la operación And es **true** si todas las expresiones de búsqueda contenidas en and son **true**.  <br/> |
|[Or](or.md) <br/> |Representa una expresión de búsqueda que realiza un or lógico en la expresión de búsqueda que contiene. El [elemento Or](or.md) devolverá **true** si alguno de sus elementos secundarios devuelve **true**.  <br/> |
   
## <a name="remarks"></a>Comentarios

Los atributos se usan para determinar cómo coinciden los elementos.
  
El esquema que describe este elemento se encuentra en el directorio virtual EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor Acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Consulte también

- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

