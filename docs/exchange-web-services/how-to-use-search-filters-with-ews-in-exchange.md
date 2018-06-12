---
title: Use los filtros de búsqueda con EWS en Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 20fc6d2d-41c2-4490-98b8-c52513977fef
description: Descubra cómo usar filtros de búsqueda con la API administrada de EWS o EWS en Exchange.
ms.openlocfilehash: 0652c36fd610c2f9dfe22b55323b368997137e0c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763197"
---
# <a name="use-search-filters-with-ews-in-exchange"></a>Use los filtros de búsqueda con EWS en Exchange

Descubra cómo usar filtros de búsqueda con la API administrada de EWS o EWS en Exchange.
  
Filtros de búsqueda es la principal herramienta para expresar los criterios de búsqueda en la API administrada de EWS o aplicación de EWS. Se recomienda que utilice filtros de búsqueda, a diferencia de [las cadenas de consulta](how-to-perform-an-aqs-search-by-using-ews-in-exchange.md), para hacer lo siguiente:
  
- Buscar en una propiedad concreta o un conjunto de propiedades.  
- La búsqueda con varios criterios de búsqueda.
    
Filtros de búsqueda es la única opción si está realizando una de las siguientes:
  
- Búsqueda de propiedades personalizadas.  
- Busca en la realización de cadena entre mayúsculas y minúsculas.  
- Busca en la realización de prefijo o cadena de coincidencia exacta. 
- Busca en la realización de máscara de bits.
- Busca los elementos que tienen una propiedad concreta se establece, independientemente del valor.
- Búsqueda de carpetas.
- Creación de las carpetas de búsqueda.
    
## <a name="determine-what-type-of-search-filter-you-need"></a>Determinar qué tipo de filtro de búsqueda necesita
<a name="bk_SelectFilter"> </a>

Antes de crear un filtro de búsqueda, en primer lugar determine qué tipo de filtro que necesita. Los tipos de filtro se implementan como clases descendientes de la clase [SearchFilter](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.searchfilter%28v=exchg.80%29.aspx) en la API administrada de EWS y como elementos secundarios del elemento de [restricción](http://msdn.microsoft.com/library/77f19014-d112-4999-8e83-ecc32a117a73%28Office.15%29.aspx) de EWS. 
  
**La tabla 1. Tipos de filtros de búsqueda**

|**Tipo de filtro**|**Clase de la API administrada de EWS**|**Elemento EWS**|**Descripción**|
|:-----|:-----|:-----|:-----|
|Contiene el filtro  <br/> |[ContainsSubstring](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.searchfilter.containssubstring%28v=exchg.80%29.aspx) <br/> |[Incluye](http://msdn.microsoft.com/library/476d059d-c243-43e9-b475-319fc413ade2%28Office.15%29.aspx) <br/> |El mejor tipo de filtro que se usará para las comparaciones de cadenas. Permite controlar la distinción de mayúsculas y, si se debe omitir espacios en blanco y establecer el modo de contención.  <br/> |
|Filtro de máscara de bits  <br/> |[ExcludesBitmask](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.searchfilter.excludesbitmask%28v=exchg.80%29.aspx) <br/> |[Excluye](http://msdn.microsoft.com/library/bbaeddf6-9a67-4ee0-af99-7a7a5bbdc0e1%28Office.15%29.aspx) <br/> |Permite buscar propiedades de entero como máscaras de bits y sólo devolverá los resultados que tienen bits correspondiente a la máscara de bits especificado no establecido.  <br/> |
|Existe filtro  <br/> |[Existe](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.searchfilter.exists%28v=exchg.80%29.aspx) <br/> |[Existe](http://msdn.microsoft.com/library/55d568bd-8dbc-4d50-b9d7-54b74a54d4b5%28Office.15%29.aspx) <br/> |Devuelve todos los elementos que tienen la propiedad especificada está presente, independientemente del valor.  <br/> |
|Filtro de igualdad  <br/> |[IsEqualTo](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.searchfilter.isequalto%28v=exchg.80%29.aspx) <br/> [IsNotEqualTo](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.searchfilter.isnotequalto%28v=exchg.80%29.aspx) <br/> |[IsEqualTo](http://msdn.microsoft.com/library/48e7e067-049c-4184-8026-071e6f558e8a%28Office.15%29.aspx) <br/> [IsNotEqualTo](http://msdn.microsoft.com/library/e2eff26c-3403-45cd-bb74-1eb98c7dbfcd%28Office.15%29.aspx) <br/> |Compara el valor de la propiedad especificada con un valor constante especificado o el valor de otra propiedad y devolver todos los elementos que tienen un valor igual (en el caso de un filtro **IsEqualTo** ) o un valor que no sean igual (en el caso de un **IsNotEqualTo **filtro).  <br/> |
|Filtro de prueba relacional  <br/> |[IsGreaterThan](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.searchfilter.isgreaterthan%28v=exchg.80%29.aspx) <br/> [IsGreaterThanOrEqualTo](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.searchfilter.isgreaterthanorequalto%28v=exchg.80%29.aspx) <br/> [IsLessThan](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.searchfilter.islessthan%28v=exchg.80%29.aspx) <br/> [IsLessThanOrEqualTo](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.searchfilter.islessthanorequalto%28v=exchg.80%29.aspx) <br/> |[IsGreaterThan](http://msdn.microsoft.com/library/a6e9d462-cfa7-40ec-903e-128c95050352%28Office.15%29.aspx) <br/> [IsGreaterThanOrEqualTo](http://msdn.microsoft.com/library/373cc954-314d-40e2-be03-cc08aefc0d5b%28Office.15%29.aspx) <br/> [IsLessThan](http://msdn.microsoft.com/library/2550469b-6e5d-45a5-9ecc-090d1b409296%28Office.15%29.aspx) <br/> [IsLessThanOrEqualTo](http://msdn.microsoft.com/library/b5d85eb2-5e15-4d01-ad49-6289e735ad8a%28Office.15%29.aspx) <br/> |Devuelve todos los elementos que tienen un valor para la propiedad especificada en la relación correspondiente a un valor constante especificado u otra propiedad. Por ejemplo, un filtro **IsGreaterThan** devuelve todos los elementos que tienen un valor que es mayor que el valor especificado en la propiedad especificada.  <br/> |
|Filtro de negación  <br/> |[No](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.searchfilter.not%28v=exchg.80%29.aspx) <br/> |[No](http://msdn.microsoft.com/library/1aa16318-7e90-4b19-bce8-dd1a20a66223%28Office.15%29.aspx) <br/> |Niega el resultado de los otros filtros.  <br/> |
|Filtro de compuestos  <br/> |[SearchFilterCollection](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.searchfilter.searchfiltercollection%28v=exchg.80%29.aspx) <br/> |[And](http://msdn.microsoft.com/library/790246c2-37ad-49a8-91b9-6186d743b011%28Office.15%29.aspx) <br/> [Or](http://msdn.microsoft.com/library/4876d83a-73a3-4953-9d95-3048e6b76ccb%28Office.15%29.aspx) <br/> |Combina varios filtros, lo que permite los criterios de búsqueda más complejos.  <br/> |
   
### <a name="contains-filter"></a>Contiene el filtro

Contiene un filtro es la mejor opción para la búsqueda de propiedades de cadena. Con un contiene filtro, puede controlar aspectos de coincidencia de cadena, como entre mayúsculas y minúsculas y cómo se tratan los espacios en blanco, estableciendo el modo de contención y el modo de comparación.
  
#### <a name="contains-filter-in-the-ews-managed-api"></a>Contiene el filtro en la API administrada de EWS
<a name="bk_ContainsEWSMA"> </a>

Si se usa la API administrada de EWS, establezca el modo de contención mediante el uso de la propiedad [ContainmentMode](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.searchfilter.containssubstring.containmentmode%28v=exchg.80%29.aspx) de la clase [ContainsSubstring](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.searchfilter.containssubstring%28v=exchg.80%29.aspx) y establecer el modo de comparación mediante el uso de la propiedad [ComparisonMode](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.searchfilter.containssubstring.comparisonmode%28v=exchg.80%29.aspx) de la ** ContainsSubstring** clase. En el ejemplo siguiente se muestra cómo crear un filtro de búsqueda que busca en el campo Asunto de los elementos de la subcadena "notas de la reunión". En este ejemplo se omite el caso, pero no omite el espacio en blanco. 
  
```cs
// Find all items with a subject that contain the substring
// "meeting notes", regardless of case.
// Matches include:
//   - meeting notes
//   - Meeting Notes
//   - Here are my meeting notes
SearchFilter.ContainsSubstring subjectFilter = new SearchFilter.ContainsSubstring(ItemSchema.Subject,
    "meeting notes", ContainmentMode.Substring, ComparisonMode.IgnoreCase);
```

#### <a name="contains-filter-in-ews"></a>Contiene el filtro de EWS
<a name="bk_ContainsEWSMA"> </a>

En EWS, se establece el modo de contención mediante el atributo **ContainmentMode** en el elemento [Contains](http://msdn.microsoft.com/library/476d059d-c243-43e9-b475-319fc413ade2%28Office.15%29.aspx) y establecer el modo de comparación mediante el atributo **ContainmentComparison** en el elemento **contiene** . En el ejemplo siguiente se muestra cómo crear un filtro de búsqueda para buscar en el campo Asunto de los elementos de la subcadena "notas de la reunión". En este ejemplo se omite el caso, pero no omite el espacio en blanco. 
  
```XML
<t:Contains ContainmentMode="Substring" ContainmentComparison="IgnoreCase">
  <t:FieldURI FieldURI="item:Subject" />
  <t:Constant Value="meeting notes" />
</t:Contains>
```

### <a name="bitmask-filter"></a>Filtro de máscara de bits

Un filtro de máscara de bits permite buscar propiedades de entero como máscaras de bits y devolver resultados donde bits específicos no se establecen en el valor de la propiedad especificada.
  
#### <a name="bitmask-filter-in-the-ews-managed-api"></a>Filtro de máscara de bits en la API administrada de EWS

En el ejemplo siguiente se muestra cómo usar la API administrada de EWS para crear un filtro de búsqueda para devolver todos los elementos que tienen un valor en la propiedad personalizada **ItemIndex** (definido en la [ejemplo: buscar elementos mediante el uso de un filtro de búsqueda y la API administrada de EWS](#bk_ExampleEWSMA) sección de este artículo) que no tienen el segundo bit (10 en binario) establecer. 
  
```cs
// Find all items with a value of the custom property that does not
// have the second bit (0010) set.
// Matches include:
//   - Property not set
//   - 1 (0001)
//   - 4 (0100)
//   - 5 (0101)
//   - 8 (1000)
SearchFilter.ExcludesBitmask bit2NotSetFilter = 
    new SearchFilter.ExcludesBitmask(customPropDefinition, 2);
```

#### <a name="bitmask-filter-in-ews"></a>Filtro de máscara de bits de EWS

En el ejemplo siguiente se muestra cómo usar EWS para crear un filtro de búsqueda para devolver todos los elementos que tienen un valor en la propiedad personalizada **ItemIndex** (definido en la [ejemplo: buscar elementos mediante el uso de un filtro de búsqueda y la API administrada de EWS](#bk_ExampleEWSMA) sección de este artículo) que no tienen el segundo bit (10 en binario) establecer. 
  
```XML
<t:Excludes>
  <t:ExtendedFieldURI PropertySetId="aa3df801-4fc7-401f-bbc1-7c93d6498c2e" PropertyName="ItemIndex" PropertyType="Integer" />
  <t:Bitmask Value="2" />
</t:Excludes>
```

### <a name="exists-filter"></a>Existe filtro

Un existe filtro le permite buscar los elementos que tienen una propiedad concreta que se establezca en ellos, independientemente del valor.
  
#### <a name="exists-filter-in-the-ews-managed-api"></a>Existe el filtro en la API administrada de EWS

En el ejemplo siguiente se muestra cómo crear un filtro de búsqueda para devolver todos los elementos que tienen establecida la propiedad **ItemIndex** personalizada. 
  
```cs
// Find all items that have the custom property set.
SearchFilter.Exists customPropSetFilter =
    new SearchFilter.Exists(customPropDefinition);
```

#### <a name="exists-filter-in-ews"></a>Existe el filtro de EWS

En el ejemplo siguiente se muestra cómo crear un filtro de búsqueda para devolver todos los elementos que tienen establecida la propiedad **ItemIndex** personalizada. 
  
```XML
<t:Exists>
  <t:ExtendedFieldURI PropertySetId="aa3df801-4fc7-401f-bbc1-7c93d6498c2e" PropertyName="ItemIndex" PropertyType="Integer" />
</t:Exists>
```

### <a name="equality-filter"></a>Filtro de igualdad

Filtros de igualdad permiten buscar todos los elementos que tienen un valor para la propiedad especificada que es igual a un valor específico o que no es igual a un valor específico. El valor se va a comparar con puede ser un valor constante o el valor de otra propiedad en cada elemento.
  
#### <a name="equality-filter-in-the-ews-managed-api"></a>Filtro de igualdad en la API administrada de EWS

En el ejemplo siguiente se muestra cómo usar la API administrada de EWS para crear un filtro de búsqueda para devolver todos los elementos que no se han leído.
  
```cs
// Find all items that are not marked as read.
SearchFilter.IsEqualTo unreadFilter =
    new SearchFilter.IsEqualTo(EmailMessageSchema.IsRead, false);
```

En el ejemplo siguiente se muestra cómo crear un filtro de búsqueda para devolver todos los elementos que tienen un valor en la propiedad **ItemIndex** que no es igual que el tamaño del elemento. 
  
```cs
// Find all items that are marked as read.
SearchFilter.IsNotEqualTo indexNotEqualToSizeFilter =
    new SearchFilter.IsNotEqualTo(customPropDefinition, ItemSchema.Size);
```

#### <a name="equality-filter-in-ews"></a>Filtro de igualdad en EWS

En el ejemplo siguiente se muestra cómo usar EWS para crear un filtro de búsqueda para devolver todos los elementos que no se han leído.
  
```XML
<t:IsEqualTo>
  <t:FieldURI FieldURI="message:IsRead" />
  <t:FieldURIOrConstant>
    <t:Constant Value="false" />
  </t:FieldURIOrConstant>
</t:IsEqualTo>
```

En el ejemplo siguiente se muestra cómo crear un filtro de búsqueda para devolver todos los elementos que tienen un valor en la propiedad **ItemIndex** que no es igual que el tamaño del elemento. 
  
```XML
<t:IsNotEqualTo>
  <t:ExtendedFieldURI PropertySetId="aa3df801-4fc7-401f-bbc1-7c93d6498c2e" PropertyName="ItemIndex" PropertyType="Integer" />
  <t:FieldURIOrConstant>
    <t:FieldURI FieldURI="item:Size" />
  </t:FieldURIOrConstant>
</t:IsNotEqualTo>
```

### <a name="relational-testing-filter"></a>Filtro de prueba relacional

Filtros pruebas relacionales permiten buscar todos los elementos que tienen un valor en la propiedad especificada que es mayor que (\>), mayor o igual que (\>=), menor que (\<), o menor o igual que (\<=) un valor especificado. El valor se va a comparar con puede ser un valor constante o el valor de otra propiedad en cada elemento.
  
#### <a name="relational-testing-filter-in-the-ews-managed-api"></a>Filtro de prueba relacional en la API administrada de EWS

En el ejemplo siguiente se muestra cómo usar la API administrada de EWS para crear filtros de búsqueda para devolver todos los elementos con un valor de la propiedad **ItemIndex** que tiene la relación especificada con el valor constante 3. 
  
```cs
// Find all items where the custom property value is > 3.
SearchFilter.IsGreaterThan greaterThanFilter =
    new SearchFilter.IsGreaterThan(customPropDefinition, 3);
// Find all items where the custom property value is >= 3.
SearchFilter.IsGreaterThanOrEqualTo greaterThanOrEqualFilter =
    new SearchFilter.IsGreaterThanOrEqualTo(customPropDefinition, ItemSchema.Size);
// Find all items where the custom property value is < 3.
SearchFilter.IsLessThan lessThanFilter =
    new SearchFilter.IsLessThan(customPropDefinition, 3);
// Find all items where the custom property value is <= 3.
SearchFilter.IsLessThanOrEqualTo lessThanOrEqualFilter =
    new SearchFilter.IsLessThanOrEqualTo(customPropDefinition, 3);
```

#### <a name="relational-testing-filter-in-ews"></a>Filtro de prueba relacional de EWS

En el ejemplo siguiente se muestra cómo usar EWS para crear un filtro de búsqueda para devolver todos los elementos con un valor de la propiedad **ItemIndex** que es mayor que el valor constante 3. 
  
```XML
<t:IsGreaterThan>
  <t:ExtendedFieldURI PropertySetId="aa3df801-4fc7-401f-bbc1-7c93d6498c2e" PropertyName="ItemIndex" PropertyType="Integer" />
  <t:FieldURIOrConstant>
    <t:Constant Value="3" />
  </t:FieldURIOrConstant>
</t:IsGreaterThan>
```

En el ejemplo siguiente se muestra cómo crear un filtro de búsqueda para devolver todos los elementos con un valor de la propiedad **ItemIndex** que es mayor o igual que el valor constante 3. 
  
```XML
<t:IsGreaterThanOrEqualTo>
  <t:ExtendedFieldURI PropertySetId="aa3df801-4fc7-401f-bbc1-7c93d6498c2e" PropertyName="ItemIndex" PropertyType="Integer" />
  <t:FieldURIOrConstant>
    <t:Constant Value="3" />
  </t:FieldURIOrConstant>
</t:IsGreaterThanOrEqualTo>
```

En el ejemplo siguiente se muestra cómo crear un filtro de búsqueda para devolver todos los elementos con un valor de la propiedad **ItemIndex** que es menor que el valor constante 3. 
  
```XML
<t:IsLessThan>
  <t:ExtendedFieldURI PropertySetId="aa3df801-4fc7-401f-bbc1-7c93d6498c2e" PropertyName="ItemIndex" PropertyType="Integer" />
  <t:FieldURIOrConstant>
    <t:Constant Value="3" />
  </t:FieldURIOrConstant>
</t:IsLessThan>
```

En el ejemplo siguiente se muestra cómo crear un filtro de búsqueda para devolver todos los elementos con un valor de la propiedad **ItemIndex** que es menor o igual que el valor constante 3. 
  
```XML
<t:IsLessThanOrEqualTo>
  <t:ExtendedFieldURI PropertySetId="aa3df801-4fc7-401f-bbc1-7c93d6498c2e" PropertyName="ItemIndex" PropertyType="Integer" />
  <t:FieldURIOrConstant>
    <t:Constant Value="3" />
  </t:FieldURIOrConstant>
</t:IsLessThanOrEqualTo>
```

### <a name="negating-filter"></a>Filtro de negación

Un filtro negating permite negar otro filtro y obtener los resultados de búsqueda opuesto. Mientras que otros filtros devuelven resultados que coincidan con criterios específicos, un filtro negating devuelve resultados que no coinciden con los criterios especificados por el filtro se aplica a.
  
#### <a name="negating-filter-in-the-ews-managed-api"></a>Negación filtro en la API administrada de EWS

En el ejemplo siguiente se muestra cómo usar la API administrada de EWS para crear un filtro de búsqueda para devolver todos los elementos que no tienen la subcadena "notas de la reunión" en el asunto.
  
```cs
SearchFilter.ContainsSubstring subjectFilter = new SearchFilter.ContainsSubstring(ItemSchema.Subject,
    "meeting notes", ContainmentMode.Substring, ComparisonMode.IgnoreCase);
SearchFilter.Not subjectNotFilter =
    new SearchFilter.Not(subjectFilter);
```

#### <a name="negating-filter-in-ews"></a>Filtro de negación de EWS

En el ejemplo siguiente se muestra cómo crear un filtro de búsqueda para devolver todos los elementos que no tienen la subcadena "notas de la reunión" en el asunto.
  
```XML
<t:Not>
  <t:Contains ContainmentMode="ExactPhrase" ContainmentComparison="IgnoreCase">
    <t:FieldURI FieldURI="item:Subject" />
    <t:Constant Value="meeting notes" />
  </t:Contains>
</t:Not>
```

### <a name="compound-filter"></a>Filtro de compuestos

Un filtro de compuestos permite combinar varios filtros para crear criterios de búsqueda más complejos. Puede combinar los criterios mediante el uso de los operadores lógicos y o OR. De este modo, puede realizar búsquedas al igual que "todo el correo de Sadie Daniels que contiene 'notas de la reunión' en el asunto".
  
#### <a name="compound-filter-in-the-ews-managed-api"></a>Filtro de compuestos en la API administrada de EWS

En el ejemplo siguiente se muestra cómo usar la API administrada de EWS para crear un filtro de búsqueda que devuelve todos los elementos que se envían desde Sadie Daniels y contienen "notas de la reunión" en el asunto.
  
```cs
SearchFilter.ContainsSubstring subjectFilter = new SearchFilter.ContainsSubstring(ItemSchema.Subject,
    "meeting notes", ContainmentMode.Substring, ComparisonMode.IgnoreCase);
EmailAddress manager = new EmailAddress("sadie@contoso.com");
SearchFilter.IsEqualTo fromManagerFilter =
    new SearchFilter.IsEqualTo(EmailMessageSchema.Sender, manager);
SearchFilter.SearchFilterCollection compoundFilter =
    new SearchFilter.SearchFilterCollection(LogicalOperator.And, subjectFilter, fromManagerFilter);
```

#### <a name="compound-filter-in-ews"></a>Filtro de compuestos en EWS

En el ejemplo siguiente se muestra cómo usar EWS para crear un filtro de búsqueda que devuelve todos los elementos que se envían desde Sadie Daniels y contienen "notas de la reunión" en el asunto.
  
```XML
<t:And>
  <t:Contains ContainmentMode="Substring" ContainmentComparison="IgnoreCase">
    <t:FieldURI FieldURI="item:Subject" />
    <t:Constant Value="meeting notes" />
  </t:Contains>
  <t:IsEqualTo>
    <t:FieldURI FieldURI="message:Sender" />
    <t:FieldURIOrConstant>
      <t:Constant Value="sadie@fourthcoffee.com" />
    </t:FieldURIOrConstant>
  </t:IsEqualTo>
</t:And>
```

## <a name="example-find-items-by-using-a-search-filter-and-the-ews-managed-api"></a>Ejemplo: Buscar elementos mediante el uso de un filtro de búsqueda y la API administrada de EWS
<a name="bk_ExampleEWSMA"> </a>

Los siguientes métodos de la API administrada de EWS utilizar filtros de búsqueda:
  
- [ExchangeService.FindItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx)
- [ExchangeService.FindFolders](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.findfolders%28v=exchg.80%29.aspx)
- [Folder.FindFolders](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.findfolders%28v=exchg.80%29.aspx)
- [Folder.FindItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.finditems%28v=exchg.80%29.aspx)
    
En el ejemplo siguiente se utiliza el método **ExchangeService.FindItems** ; Sin embargo, las mismas reglas y los conceptos se aplican a todos los métodos. En este ejemplo, se define un método denominado **SearchWithFilter** . Toma un objetos [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) , [WellKnownFolderName](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.wellknownfoldername%28v=exchg.80%29.aspx) y [SearchFilter](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.searchfilter%28v=exchg.80%29.aspx) como parámetros. En este ejemplo se da por supuesto que se ha inicializado el objeto **ExchangeService** con valores válidos en las propiedades de [las credenciales](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservicebase.credentials%28v=exchg.80%29.aspx) y [dirección Url](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.url%28v=exchg.80%29.aspx) . La clase **SearchFilter** es la clase base para todos los filtros de búsqueda diferentes. 
  
```cs
using Microsoft.Exchange.WebServices.Data
private static Guid SearchTestGUID = new Guid("{AA3DF801-4FC7-401F-BBC1-7C93D6498C2E}");
private static ExtendedPropertyDefinition customPropDefinition =
        new ExtendedPropertyDefinition(SearchTestGUID, "ItemIndex", MapiPropertyType.Integer);
static void SearchWithFilter(ExchangeService service, WellKnownFolderName folder, SearchFilter filter)
{
    // Limit the result set to 10 items.
    ItemView view = new ItemView(10);
    view.PropertySet = new PropertySet(ItemSchema.Subject, 
                                       ItemSchema.DateTimeReceived,
                                       EmailMessageSchema.IsRead,
                                       customPropDefinition);
    // Item searches do not support Deep traversal.
    view.Traversal = ItemTraversal.Shallow;
    // Sorting.
    view.OrderBy.Add(ItemSchema.DateTimeReceived, SortDirection.Descending);
    try
    {
        FindItemsResults<Item> results = service.FindItems(folder, filter, view);
        foreach (Item item in results.Items)
        {
            Console.WriteLine("Subject: {0}", item.Subject);
            Console.WriteLine("Id: {0}", item.Id.ToString());
            if (item.ExtendedProperties.Count > 0 &&
                 item.ExtendedProperties[0].PropertyDefinition == customPropDefinition)
            {
                Console.WriteLine("Search Index: {0}", item.ExtendedProperties[0].Value);
            }
            if (item is EmailMessage)
            {
                EmailMessage message = item as EmailMessage;
                Console.WriteLine("Read: {0}", message.IsRead.ToString());
            }
        }
    }
    catch (Exception ex)
    {
        Console.WriteLine("Exception while enumerating results: {0}", ex.Message);
    }
}
```

Puede usar esta función con cualquiera de los filtros de búsqueda que se muestra en los ejemplos de este artículo. En este ejemplo se usa un filtro de compuestos para devolver todos los elementos de la Bandeja de entrada de Sadie Daniels con "notas de la reunión" en el asunto.
  
```cs
SearchFilter.ContainsSubstring subjectFilter = new SearchFilter.ContainsSubstring(ItemSchema.Subject,
    "meeting notes", ContainmentMode.Substring, ComparisonMode.IgnoreCase);
EmailAddress manager = new EmailAddress("sadie@contoso.com");
SearchFilter.IsEqualTo fromManagerFilter =
    new SearchFilter.IsEqualTo(EmailMessageSchema.Sender, manager);
SearchFilter.SearchFilterCollection compoundFilter =
    new SearchFilter.SearchFilterCollection(LogicalOperator.And, subjectFilter, greaterThanFilter);
SearchWithFilter(service, WellKnownFolderName.Inbox, compoundFilter);
```

## <a name="example-find-an-item-by-using-a-search-filter-and-ews"></a>Ejemplo: Buscar un elemento mediante el uso de un filtro de búsqueda y EWS
<a name="bk_ExampleEWS"> </a>

Las siguientes operaciones de EWS usar filtros de búsqueda:
  
- [FindFolder](http://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx)
- [FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)
    
En el ejemplo siguiente se utiliza la operación **FindItem** ; Sin embargo, las mismas reglas y los conceptos se aplican a ambas operaciones. Filtros de búsqueda se encuentran en el elemento de [restricción](http://msdn.microsoft.com/library/77f19014-d112-4999-8e83-ecc32a117a73%28Office.15%29.aspx) en las solicitudes SOAP. En este ejemplo se envía una solicitud SOAP que es equivalente a la búsqueda que se muestra en el ejemplo anterior de la API administrada de EWS. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
    xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
    xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
    xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2013" />
  </soap:Header>
  <soap:Body>
    <m:FindItem Traversal="Shallow">
      <m:ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="item:Subject" />
          <t:FieldURI FieldURI="item:DateTimeReceived" />
          <t:FieldURI FieldURI="message:IsRead" />
          <t:ExtendedFieldURI PropertySetId="aa3df801-4fc7-401f-bbc1-7c93d6498c2e" PropertyName="ItemIndex" PropertyType="Integer" />
        </t:AdditionalProperties>
      </m:ItemShape>
      <m:IndexedPageItemView MaxEntriesReturned="10" Offset="0" BasePoint="Beginning" />
      <m:Restriction>
        <t:And>
          <t:Contains ContainmentMode="Substring" ContainmentComparison="IgnoreCase">
            <t:FieldURI FieldURI="item:Subject" />
            <t:Constant Value="meeting notes" />
          </t:Contains>
          <t:IsEqualTo>
            <t:FieldURI FieldURI="message:Sender" />
            <t:FieldURIOrConstant>
              <t:Constant Value="sadie@contoso.com" />
            </t:FieldURIOrConstant>
          </t:IsEqualTo>
        </t:And>
      </m:Restriction>
      <m:SortOrder>
        <t:FieldOrder Order="Descending">
          <t:FieldURI FieldURI="item:DateTimeReceived" />
        </t:FieldOrder>
      </m:SortOrder>
      <m:ParentFolderIds>
        <t:DistinguishedFolderId Id="inbox" />
      </m:ParentFolderIds>
    </m:FindItem>
  </soap:Body>
</soap:Envelope>
```

En el ejemplo siguiente se muestra la respuesta del servidor, incluidos los resultados de búsqueda.
  
```XML
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="712" MinorBuildNumber="22" Version="V2_3" 
        xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
        xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:FindItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
        xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:FindItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:RootFolder IndexedPagingOffset="3" TotalItemsInView="3" IncludesLastItemInRange="true">
            <t:Items>
              <t:Message>
                <t:ItemId Id="AAMkAGM2..." ChangeKey="CQAAABYA..." />
                <t:Subject>meeting notes</t:Subject>
                <t:DateTimeReceived>2013-11-20T21:18:51Z</t:DateTimeReceived>
                <t:ExtendedProperty>
                  <t:ExtendedFieldURI PropertySetId="aa3df801-4fc7-401f-bbc1-7c93d6498c2e" PropertyName="ItemIndex" PropertyType="Integer" />
                  <t:Value>5</t:Value>
                </t:ExtendedProperty>
                <t:IsRead>true</t:IsRead>
              </t:Message>
              <t:Message>
                <t:ItemId Id="AAMkAGM2..." ChangeKey="CQAAABYA..." />
                <t:Subject>Meeting Notes</t:Subject>
                <t:DateTimeReceived>2013-11-20T21:18:51Z</t:DateTimeReceived>
                <t:ExtendedProperty>
                  <t:ExtendedFieldURI PropertySetId="aa3df801-4fc7-401f-bbc1-7c93d6498c2e" PropertyName="ItemIndex" PropertyType="Integer" />
                  <t:Value>6</t:Value>
                </t:ExtendedProperty>
                <t:IsRead>true</t:IsRead>
              </t:Message>
              <t:Message>
                <t:ItemId Id="AAMkAGM2..." ChangeKey="CQAAABYA..." />
                <t:Subject>Meeting notes</t:Subject>
                <t:DateTimeReceived>2013-11-20T21:18:51Z</t:DateTimeReceived>
                <t:ExtendedProperty>
                  <t:ExtendedFieldURI PropertySetId="aa3df801-4fc7-401f-bbc1-7c93d6498c2e" PropertyName="ItemIndex" PropertyType="Integer" />
                  <t:Value>7</t:Value>
                </t:ExtendedProperty>
                <t:IsRead>true</t:IsRead>
              </t:Message>
            </t:Items>
          </m:RootFolder>
        </m:FindItemResponseMessage>
      </m:ResponseMessages>
    </m:FindItemResponse>
  </s:Body>
</s:Envelope>
```

## <a name="next-steps"></a>Siguientes pasos
<a name="bk_ExampleEWS"> </a>

Ahora que está familiarizado con el uso de filtros de búsqueda en las búsquedas básicas, puede mover a técnicas más avanzadas de búsqueda.
  
- [Realizar búsquedas agrupadas mediante EWS en Exchange](how-to-perform-grouped-searches-by-using-ews-in-exchange.md)
    
- [Realizar búsquedas paginadas mediante EWS en Exchange](how-to-perform-paged-searches-by-using-ews-in-exchange.md)
    
## <a name="see-also"></a>Ver también

- [Búsqueda y EWS en Exchange](search-and-ews-in-exchange.md)    
- [Realizar una búsqueda AQS mediante EWS en Exchange](how-to-perform-an-aqs-search-by-using-ews-in-exchange.md)   
- [ExchangeService.FindItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx)    
- [ExchangeService.FindFolders](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.findfolders%28v=exchg.80%29.aspx)    
- [Folder.FindFolders](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.findfolders%28v=exchg.80%29.aspx)    
- [Folder.FindItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.finditems%28v=exchg.80%29.aspx)    
- [Operación FindFolder](http://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx)   
- [Operación FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)
    

