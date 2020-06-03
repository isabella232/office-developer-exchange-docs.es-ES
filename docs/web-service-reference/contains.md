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
description: El elemento Contains representa una expresión de búsqueda que determina si una propiedad determinada contiene el valor de cadena constante proporcionado.
ms.openlocfilehash: 79529bd752bcbce954ae3c8b0085c203b4eb8777
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44527120"
---
# <a name="contains"></a>Contains

El elemento **Contains** representa una expresión de búsqueda que determina si una propiedad determinada contiene el valor de cadena constante proporcionado. 
  
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
|**ContainmentComparison** <br/> |Determina si la búsqueda omite los casos y los espacios.  <br/> |
   
#### <a name="containmentmode-attribute-values"></a>Valores del atributo ContainmentMode

|**Valor**|**Descripción**|
|:-----|:-----|
|FullString  <br/> |La comparación se encuentra entre la cadena completa y la constante. El valor de la propiedad y la constante proporcionada son exactamente iguales.  <br/> |
|Prefijo  <br/> |La comparación se encuentra entre el prefijo de cadena y la constante.  <br/> |
|Subcadena  <br/> |La comparación se encuentra entre una subcadena de la cadena y la constante.  <br/> |
|PrefixOnWords  <br/> |La comparación se encuentra entre un prefijo de palabras individuales en la cadena y la constante.  <br/> |
|ExactPhrase  <br/> |La comparación se encuentra entre una frase exacta en la cadena y la constante.  <br/> |
   
#### <a name="containmentcomparison-attribute-values"></a>Valores del atributo ContainmentComparison

|**Valor**|**Descripción**|
|:-----|:-----|
|Motiva  <br/> |La comparación debe ser exacta.  <br/> |
|IgnoreCase  <br/> |La comparación omite el uso de mayúsculas.  <br/> |
|IgnoreNonSpacingCharacters  <br/> |La comparación omite los caracteres que no son de espacio.  <br/> |
|Separada  <br/> |Que se va a quitar.  <br/> |
|IgnoreCaseAndNonSpacingCharacters  <br/> |La comparación no tiene en cuenta las mayúsculas y minúsculas y los caracteres sin espacio.  <br/> |
|LooseAndIgnoreCase  <br/> |Que se va a quitar.  <br/> |
|LooseAndIgnoreNonSpace  <br/> |Que se va a quitar.  <br/> |
|LooseAndIgnoreCaseAndIgnoreNonSpace  <br/> |Que se va a quitar.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[FieldURI](fielduri.md) <br/> |Identifica las propiedades a las que se hace referencia con frecuencia mediante el URI.  <br/> |
|[IndexedFieldURI](indexedfielduri.md) <br/> |Identifica a los miembros individuales de un diccionario.  <br/> |
|[ExtendedFieldURI](extendedfielduri.md) <br/> |Identifica las propiedades MAPI.  <br/> |
|[Constante](constant.md) <br/> |Identifica un valor constante en una restricción.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Restriction](restriction.md) <br/> |Representa la restricción o consulta que se usa para filtrar elementos o carpetas en las operaciones de carpeta de búsqueda FindItem/FindFolder.  <br/> |
|[Not](not.md) <br/> |Representa una expresión de búsqueda que niega el valor booleano de la expresión de búsqueda que contiene.  <br/> |
|[And](and.md) <br/> |Representa una expresión de búsqueda que permite realizar una operación and booleana entre dos o más expresiones de búsqueda. El resultado de la operación and es **true** si todas las expresiones de búsqueda incluidas en el y son **true**.  <br/> |
|[Or](or.md) <br/> |Representa una expresión de búsqueda que realiza una operación lógica OR en la expresión de búsqueda que contiene. El elemento [o](or.md) devolverá **true** si cualquiera de sus secundarios devuelve **true**.  <br/> |
   
## <a name="remarks"></a>Comentarios

Los atributos se usan para determinar cómo coinciden los elementos.
  
El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también

- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)

