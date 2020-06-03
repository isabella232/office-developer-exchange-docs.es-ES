---
title: Usar filtros de búsqueda con EWS en Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: 20fc6d2d-41c2-4490-98b8-c52513977fef
description: Descubra cómo usar filtros de búsqueda con la API administrada de EWS o EWS en Exchange.
localization_priority: Priority
ms.openlocfilehash: 04a74ec92d4bced8abd58d164a1c186d6405e679
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44455838"
---
# <a name="use-search-filters-with-ews-in-exchange"></a>Usar filtros de búsqueda con EWS en Exchange

Descubra cómo usar filtros de búsqueda con la API administrada de EWS o EWS en Exchange.
  
Los filtros de búsqueda son la herramienta principal para expresar los criterios de búsqueda en la API administrada de EWS o en la aplicación de EWS. Se recomienda usar filtros de búsqueda, en lugar de [cadenas de consulta](how-to-perform-an-aqs-search-by-using-ews-in-exchange.md), para hacer lo siguiente:
  
- Busca en una propiedad específica o un conjunto de propiedades.  
- Buscar con varios criterios de búsqueda.
    
Los filtros de búsqueda son la única opción si está realizando alguna de las siguientes acciones:
  
- Buscar propiedades personalizadas.  
- Realizar búsquedas de cadenas con distinción entre mayúsculas y minúsculas.  
- Realizar búsquedas de cadena de coincidencia exacta o prefijo. 
- Realizar búsquedas de máscara de la máscara.
- Buscar elementos que tienen un conjunto específico de propiedades, independientemente de su valor.
- Buscar carpetas.
- Crear carpetas de búsqueda.
    
## <a name="determine-what-type-of-search-filter-you-need"></a>Determinación del tipo de filtro de búsqueda que se necesita
<a name="bk_SelectFilter"> </a>

Antes de crear un filtro de búsqueda, determine primero qué tipo de filtro necesita. Los tipos de filtro se implementan como clases descendientes de la clase [SearchFilter](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.searchfilter%28v=exchg.80%29.aspx) en la API administrada de EWS y como elementos secundarios del elemento [Restriction](https://msdn.microsoft.com/library/77f19014-d112-4999-8e83-ecc32a117a73%28Office.15%29.aspx) en EWS. 
  
**Tabla 1. Tipos de filtros de búsqueda**

|**Tipo de filtro**|**Clase de API administrada de EWS**|**Elemento EWS**|**Descripción**|
|:-----|:-----|:-----|:-----|
|Contiene el filtro  <br/> |[ContainsSubstring](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.searchfilter.containssubstring%28v=exchg.80%29.aspx) <br/> |[Contains](https://msdn.microsoft.com/library/476d059d-c243-43e9-b475-319fc413ade2%28Office.15%29.aspx) <br/> |El mejor tipo de filtro que se debe usar para las comparaciones de cadenas. Permite controlar la distinción entre mayúsculas y minúsculas, si se debe omitir el espacio en blanco y establecer el modo de contención.  <br/> |
|Filtro de máscara de máscara  <br/> |[ExcludesBitmask](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.searchfilter.excludesbitmask%28v=exchg.80%29.aspx) <br/> |[Excluye](https://msdn.microsoft.com/library/bbaeddf6-9a67-4ee0-af99-7a7a5bbdc0e1%28Office.15%29.aspx) <br/> |Permite buscar propiedades enteras como máscaras de bits y devolver solo los resultados que tienen bits correspondientes a la máscara de bits especificada sin establecer.  <br/> |
|Filtro EXISTS  <br/> |[Exists](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.searchfilter.exists%28v=exchg.80%29.aspx) <br/> |[Exists](https://msdn.microsoft.com/library/55d568bd-8dbc-4d50-b9d7-54b74a54d4b5%28Office.15%29.aspx) <br/> |Devuelve todos los elementos que tienen la propiedad especificada presente, independientemente de Value.  <br/> |
|Filtro de igualdad  <br/> |[IsEqualTo](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.searchfilter.isequalto%28v=exchg.80%29.aspx) <br/> [IsNotEqualTo](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.searchfilter.isnotequalto%28v=exchg.80%29.aspx) <br/> |[IsEqualTo](https://msdn.microsoft.com/library/48e7e067-049c-4184-8026-071e6f558e8a%28Office.15%29.aspx) <br/> [IsNotEqualTo](https://msdn.microsoft.com/library/e2eff26c-3403-45cd-bb74-1eb98c7dbfcd%28Office.15%29.aspx) <br/> |Compara el valor de la propiedad especificada con un valor constante especificado o el valor de otra propiedad y devuelve todos los elementos que tienen un valor igual (en el caso de un filtro **IsEqualTo** ) o un valor no igual (en el caso de un filtro **IsNotEqualTo** ).  <br/> |
|Filtro de pruebas relacionales  <br/> |[IsGreaterThan](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.searchfilter.isgreaterthan%28v=exchg.80%29.aspx) <br/> [IsGreaterThanOrEqualTo](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.searchfilter.isgreaterthanorequalto%28v=exchg.80%29.aspx) <br/> [IsLessThan](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.searchfilter.islessthan%28v=exchg.80%29.aspx) <br/> [IsLessThanOrEqualTo](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.searchfilter.islessthanorequalto%28v=exchg.80%29.aspx) <br/> |[IsGreaterThan](https://msdn.microsoft.com/library/a6e9d462-cfa7-40ec-903e-128c95050352%28Office.15%29.aspx) <br/> [IsGreaterThanOrEqualTo](https://msdn.microsoft.com/library/373cc954-314d-40e2-be03-cc08aefc0d5b%28Office.15%29.aspx) <br/> [IsLessThan](https://msdn.microsoft.com/library/2550469b-6e5d-45a5-9ecc-090d1b409296%28Office.15%29.aspx) <br/> [IsLessThanOrEqualTo](https://msdn.microsoft.com/library/b5d85eb2-5e15-4d01-ad49-6289e735ad8a%28Office.15%29.aspx) <br/> |Devuelve todos los elementos que tienen un valor para la propiedad especificada en la relación correspondiente a un valor constante especificado u otra propiedad. Por ejemplo, un filtro **IsGreaterThan** devuelve todos los elementos que tienen un valor mayor que el valor especificado en la propiedad especificada.  <br/> |
|Niega el filtro  <br/> |[Not](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.searchfilter.not%28v=exchg.80%29.aspx) <br/> |[Not](https://msdn.microsoft.com/library/1aa16318-7e90-4b19-bce8-dd1a20a66223%28Office.15%29.aspx) <br/> |Niega el resultado de los otros filtros.  <br/> |
|Filtro compuesto  <br/> |[SearchFilterCollection](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.searchfilter.searchfiltercollection%28v=exchg.80%29.aspx) <br/> |[And](https://msdn.microsoft.com/library/790246c2-37ad-49a8-91b9-6186d743b011%28Office.15%29.aspx) <br/> [Or](https://msdn.microsoft.com/library/4876d83a-73a3-4953-9d95-3048e6b76ccb%28Office.15%29.aspx) <br/> |Combina varios filtros, lo que permite criterios de búsqueda más complejos.  <br/> |
   
### <a name="contains-filter"></a>Contiene el filtro

Un filtro Contains es la mejor opción para buscar propiedades de cadena. Con un filtro Contains, puede controlar aspectos de coincidencia de cadenas, como la distinción entre mayúsculas y minúsculas y el tratamiento del espacio en blanco, estableciendo el modo de contención y el modo de comparación.
  
#### <a name="contains-filter-in-the-ews-managed-api"></a>Contiene un filtro en la API administrada de EWS
<a name="bk_ContainsEWSMA"> </a>

Si está usando la API administrada de EWS, establezca el modo de contención mediante la propiedad [ContainmentMode](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.searchfilter.containssubstring.containmentmode%28v=exchg.80%29.aspx) de la clase [ContainsSubstring](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.searchfilter.containssubstring%28v=exchg.80%29.aspx) y establezca el modo de comparación mediante la propiedad [ComparisonMode](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.searchfilter.containssubstring.comparisonmode%28v=exchg.80%29.aspx) de la clase **ContainsSubstring** . En el ejemplo siguiente se muestra cómo crear un filtro de búsqueda que busque en el campo Subject de los elementos la subcadena "Notas de la reunión". En este ejemplo se omite la distinción entre mayúsculas y minúsculas, pero no se omite el espacio. 
  
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

#### <a name="contains-filter-in-ews"></a>Contiene un filtro en EWS
<a name="bk_ContainsEWSMA"> </a>

En EWS, se establece el modo de contención mediante el atributo **ContainmentMode** en el elemento [Contains](https://msdn.microsoft.com/library/476d059d-c243-43e9-b475-319fc413ade2%28Office.15%29.aspx) y se establece el modo de comparación usando el atributo **ContainmentComparison** en el elemento **Contains** . En el ejemplo siguiente se muestra cómo crear un filtro de búsqueda para buscar en el campo de asunto de los elementos de la subcadena "Notas de la reunión". En este ejemplo se omite la distinción entre mayúsculas y minúsculas, pero no se omite el espacio. 
  
```XML
<t:Contains ContainmentMode="Substring" ContainmentComparison="IgnoreCase">
  <t:FieldURI FieldURI="item:Subject" />
  <t:Constant Value="meeting notes" />
</t:Contains>
```

### <a name="bitmask-filter"></a>Filtro de máscara de máscara

Un filtro de máscara de bits permite buscar propiedades de enteros como máscaras de bits y devolver resultados en los que no se establecen bits específicos en el valor de la propiedad especificada.
  
#### <a name="bitmask-filter-in-the-ews-managed-api"></a>Filtro de máscara de máscara en la API administrada de EWS

El siguiente ejemplo muestra cómo usar la API administrada de EWS para crear un filtro de búsqueda para devolver todos los elementos que tienen un valor en la propiedad personalizada **itemIndex** (definida en el [ejemplo: buscar elementos mediante un filtro de búsqueda y la sección API administrada de EWS](#bk_ExampleEWSMA) de este artículo) que no tienen el segundo bit (10 en binario) establecido. 
  
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

#### <a name="bitmask-filter-in-ews"></a>Filtro de máscara de máscara en EWS

El siguiente ejemplo muestra cómo usar EWS para crear un filtro de búsqueda para devolver todos los elementos que tienen un valor en la propiedad personalizada **itemIndex** (definida en el [ejemplo: buscar elementos mediante un filtro de búsqueda y la sección API administrada de EWS](#bk_ExampleEWSMA) de este artículo) que no tienen el segundo bit (10 en binario) establecido. 
  
```XML
<t:Excludes>
  <t:ExtendedFieldURI PropertySetId="aa3df801-4fc7-401f-bbc1-7c93d6498c2e" PropertyName="ItemIndex" PropertyType="Integer" />
  <t:Bitmask Value="2" />
</t:Excludes>
```

### <a name="exists-filter"></a>Filtro EXISTS

Un filtro EXISTS permite buscar elementos que tienen una propiedad específica establecida en ellos, independientemente del valor.
  
#### <a name="exists-filter-in-the-ews-managed-api"></a>Filtro EXISTS en la API administrada de EWS

En el ejemplo siguiente se muestra cómo crear un filtro de búsqueda para devolver todos los elementos que tienen el conjunto de propiedades personalizadas **itemIndex** . 
  
```cs
// Find all items that have the custom property set.
SearchFilter.Exists customPropSetFilter =
    new SearchFilter.Exists(customPropDefinition);
```

#### <a name="exists-filter-in-ews"></a>Filtro EXISTS en EWS

En el ejemplo siguiente se muestra cómo crear un filtro de búsqueda para devolver todos los elementos que tienen el conjunto de propiedades personalizadas **itemIndex** . 
  
```XML
<t:Exists>
  <t:ExtendedFieldURI PropertySetId="aa3df801-4fc7-401f-bbc1-7c93d6498c2e" PropertyName="ItemIndex" PropertyType="Integer" />
</t:Exists>
```

### <a name="equality-filter"></a>Filtro de igualdad

Los filtros de igualdad permiten buscar todos los elementos que tienen un valor para la propiedad especificada que sea igual a un valor específico o que no sea igual a un valor específico. El valor con el que se va a comparar puede ser un valor constante o el valor de otra propiedad en cada elemento.
  
#### <a name="equality-filter-in-the-ews-managed-api"></a>Filtro de igualdad en la API administrada de EWS

En el ejemplo siguiente se muestra cómo usar la API administrada de EWS para crear un filtro de búsqueda para devolver todos los elementos que no se han leído.
  
```cs
// Find all items that are not marked as read.
SearchFilter.IsEqualTo unreadFilter =
    new SearchFilter.IsEqualTo(EmailMessageSchema.IsRead, false);
```

En el ejemplo siguiente se muestra cómo crear un filtro de búsqueda para devolver todos los elementos que tienen un valor en la propiedad **itemIndex** que no es igual al tamaño del elemento. 
  
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

En el ejemplo siguiente se muestra cómo crear un filtro de búsqueda para devolver todos los elementos que tienen un valor en la propiedad **itemIndex** que no es igual al tamaño del elemento. 
  
```XML
<t:IsNotEqualTo>
  <t:ExtendedFieldURI PropertySetId="aa3df801-4fc7-401f-bbc1-7c93d6498c2e" PropertyName="ItemIndex" PropertyType="Integer" />
  <t:FieldURIOrConstant>
    <t:FieldURI FieldURI="item:Size" />
  </t:FieldURIOrConstant>
</t:IsNotEqualTo>
```

### <a name="relational-testing-filter"></a>Filtro de pruebas relacionales

Los filtros de pruebas relacionales permiten buscar todos los elementos que tienen un valor en la propiedad especificada que sea mayor que ( \> ), mayor o igual que ( \> =), menor que ( \< ) o menor o igual que ( \< =) un valor especificado. El valor con el que se va a comparar puede ser un valor constante o el valor de otra propiedad en cada elemento.
  
#### <a name="relational-testing-filter-in-the-ews-managed-api"></a>Filtro de pruebas relacionales en la API administrada de EWS

En el ejemplo siguiente se muestra cómo usar la API administrada de EWS para crear filtros de búsqueda para devolver todos los elementos con un valor en la propiedad **itemIndex** que tiene la relación especificada con el valor constante 3. 
  
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

#### <a name="relational-testing-filter-in-ews"></a>Filtro de pruebas relacionales en EWS

En el ejemplo siguiente se muestra cómo usar EWS para crear un filtro de búsqueda para devolver todos los elementos con un valor en la propiedad **itemIndex** que sea mayor que el valor constante 3. 
  
```XML
<t:IsGreaterThan>
  <t:ExtendedFieldURI PropertySetId="aa3df801-4fc7-401f-bbc1-7c93d6498c2e" PropertyName="ItemIndex" PropertyType="Integer" />
  <t:FieldURIOrConstant>
    <t:Constant Value="3" />
  </t:FieldURIOrConstant>
</t:IsGreaterThan>
```

En el ejemplo siguiente se muestra cómo crear un filtro de búsqueda para devolver todos los elementos con un valor en la propiedad **itemIndex** que sea mayor o igual que el valor constante 3. 
  
```XML
<t:IsGreaterThanOrEqualTo>
  <t:ExtendedFieldURI PropertySetId="aa3df801-4fc7-401f-bbc1-7c93d6498c2e" PropertyName="ItemIndex" PropertyType="Integer" />
  <t:FieldURIOrConstant>
    <t:Constant Value="3" />
  </t:FieldURIOrConstant>
</t:IsGreaterThanOrEqualTo>
```

En el ejemplo siguiente se muestra cómo crear un filtro de búsqueda para devolver todos los elementos con un valor en la propiedad **itemIndex** que sea menor que el valor constante 3. 
  
```XML
<t:IsLessThan>
  <t:ExtendedFieldURI PropertySetId="aa3df801-4fc7-401f-bbc1-7c93d6498c2e" PropertyName="ItemIndex" PropertyType="Integer" />
  <t:FieldURIOrConstant>
    <t:Constant Value="3" />
  </t:FieldURIOrConstant>
</t:IsLessThan>
```

En el ejemplo siguiente se muestra cómo crear un filtro de búsqueda para devolver todos los elementos con un valor de la propiedad **itemIndex** que sea menor o igual que el valor constante 3. 
  
```XML
<t:IsLessThanOrEqualTo>
  <t:ExtendedFieldURI PropertySetId="aa3df801-4fc7-401f-bbc1-7c93d6498c2e" PropertyName="ItemIndex" PropertyType="Integer" />
  <t:FieldURIOrConstant>
    <t:Constant Value="3" />
  </t:FieldURIOrConstant>
</t:IsLessThanOrEqualTo>
```

### <a name="negating-filter"></a>Niega el filtro

Un filtro de negación permite negar otro filtro y obtener los resultados de búsqueda opuestos. Mientras que otros filtros devuelven resultados que coinciden con criterios específicos, un filtro de negación devuelve resultados que no coinciden con los criterios especificados por el filtro al que se aplica.
  
#### <a name="negating-filter-in-the-ews-managed-api"></a>Niega el filtro en la API administrada de EWS

El siguiente ejemplo muestra cómo usar la API administrada de EWS para crear un filtro de búsqueda para devolver todos los elementos que no tienen la subcadena "Notas de la reunión" en el asunto.
  
```cs
SearchFilter.ContainsSubstring subjectFilter = new SearchFilter.ContainsSubstring(ItemSchema.Subject,
    "meeting notes", ContainmentMode.Substring, ComparisonMode.IgnoreCase);
SearchFilter.Not subjectNotFilter =
    new SearchFilter.Not(subjectFilter);
```

#### <a name="negating-filter-in-ews"></a>Niega el filtro en EWS

En el ejemplo siguiente se muestra cómo crear un filtro de búsqueda para devolver todos los elementos que no tienen la subcadena "Notas de la reunión" en el asunto.
  
```XML
<t:Not>
  <t:Contains ContainmentMode="ExactPhrase" ContainmentComparison="IgnoreCase">
    <t:FieldURI FieldURI="item:Subject" />
    <t:Constant Value="meeting notes" />
  </t:Contains>
</t:Not>
```

### <a name="compound-filter"></a>Filtro compuesto

Un filtro compuesto permite combinar varios filtros para crear criterios de búsqueda más complejos. Puede combinar criterios usando los operadores lógicos AND u OR. De este modo, puede realizar búsquedas como "todo el correo de Sadie Daniels que contiene" Notas de la reunión "en el asunto".
  
#### <a name="compound-filter-in-the-ews-managed-api"></a>Filtro compuesto en la API administrada de EWS

El siguiente ejemplo muestra cómo usar la API administrada de EWS para crear un filtro de búsqueda que devuelve todos los elementos que se envían desde Sadie Daniels y contienen "Notas de la reunión" en el asunto.
  
```cs
SearchFilter.ContainsSubstring subjectFilter = new SearchFilter.ContainsSubstring(ItemSchema.Subject,
    "meeting notes", ContainmentMode.Substring, ComparisonMode.IgnoreCase);
EmailAddress manager = new EmailAddress("sadie@contoso.com");
SearchFilter.IsEqualTo fromManagerFilter =
    new SearchFilter.IsEqualTo(EmailMessageSchema.Sender, manager);
SearchFilter.SearchFilterCollection compoundFilter =
    new SearchFilter.SearchFilterCollection(LogicalOperator.And, subjectFilter, fromManagerFilter);
```

#### <a name="compound-filter-in-ews"></a>Filtro compuesto en EWS

En el ejemplo siguiente se muestra cómo usar EWS para crear un filtro de búsqueda que devuelve todos los elementos que se envían desde Sadie Daniels y contienen "Notas de la reunión" en el asunto.
  
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

## <a name="example-find-items-by-using-a-search-filter-and-the-ews-managed-api"></a>Ejemplo: buscar elementos mediante un filtro de búsqueda y la API administrada EWS
<a name="bk_ExampleEWSMA"> </a>

Los siguientes métodos de la API administrada de EWS usan filtros de búsqueda:
  
- [ExchangeService. FindItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx)
- [ExchangeService. FindFolders](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.findfolders%28v=exchg.80%29.aspx)
- [Folder. FindFolders](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.findfolders%28v=exchg.80%29.aspx)
- [Folder. FindItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.finditems%28v=exchg.80%29.aspx)
    
En el ejemplo siguiente se usa el método **ExchangeService. FindItems** ; sin embargo, las mismas reglas y conceptos se aplican a todos los métodos. En este ejemplo, se define un método denominado **SearchWithFilter** . Toma un objeto [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) , un objeto [WellKnownFolderName](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.wellknownfoldername%28v=exchg.80%29.aspx) y un objeto [SearchFilter](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.searchfilter%28v=exchg.80%29.aspx) como parámetros. En este ejemplo se supone que el objeto **ExchangeService** se ha inicializado con valores válidos en las propiedades [Credentials](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.credentials%28v=exchg.80%29.aspx) y [URL](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.url%28v=exchg.80%29.aspx) . La clase **SearchFilter** es la clase base para todos los distintos filtros de búsqueda. 
  
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

Puede usar esta función con cualquiera de los filtros de búsqueda que se muestran en los ejemplos de este artículo. En este ejemplo se usa un filtro compuesto para devolver todos los elementos de la bandeja de entrada de Sadie Daniels con "Notas de la reunión" en el asunto.
  
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

## <a name="example-find-an-item-by-using-a-search-filter-and-ews"></a>Ejemplo: buscar un elemento mediante un filtro de búsqueda y EWS
<a name="bk_ExampleEWS"> </a>

Las siguientes operaciones de EWS usan filtros de búsqueda:
  
- [FindFolder](https://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx)
- [FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)
    
En el siguiente ejemplo, se usa la operación **FindItem** ; sin embargo, se aplican las mismas reglas y conceptos a ambas operaciones. Los filtros de búsqueda están incluidos en el elemento [Restriction](https://msdn.microsoft.com/library/77f19014-d112-4999-8e83-ecc32a117a73%28Office.15%29.aspx) de las solicitudes SOAP. En este ejemplo se envía una solicitud SOAP que es equivalente a la búsqueda que se muestra en el ejemplo anterior de la API administrada de EWS. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
    xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
    xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
    xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
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

En el ejemplo siguiente se muestra la respuesta del servidor, incluidos los resultados de la búsqueda.
  
```XML
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="712" MinorBuildNumber="22" Version="V2_3" 
        xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
        xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:FindItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
        xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
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

Ahora que está familiarizado con el uso de filtros de búsqueda en las búsquedas básicas, puede pasar a técnicas de búsqueda más avanzadas.
  
- [Realizar búsquedas agrupadas mediante EWS en Exchange](how-to-perform-grouped-searches-by-using-ews-in-exchange.md)
    
- [Realizar búsquedas paginadas mediante EWS en Exchange](how-to-perform-paged-searches-by-using-ews-in-exchange.md)
    
## <a name="see-also"></a>Vea también

- [Búsqueda y EWS en Exchange](search-and-ews-in-exchange.md)    
- [Realizar una búsqueda AQS con EWS en Exchange](how-to-perform-an-aqs-search-by-using-ews-in-exchange.md)   
- [ExchangeService. FindItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx)    
- [ExchangeService. FindFolders](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.findfolders%28v=exchg.80%29.aspx)    
- [Folder. FindFolders](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.findfolders%28v=exchg.80%29.aspx)    
- [Folder. FindItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.finditems%28v=exchg.80%29.aspx)    
- [Operación FindFolder](https://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx)   
- [Operación FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)
    

