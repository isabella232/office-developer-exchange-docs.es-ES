---
title: Búsqueda y EWS en Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9fa5b836-857e-401d-9450-51e7dbc69104
description: Descubra cómo buscar elementos en Exchange mediante la API administrada de EWS o EWS.
ms.openlocfilehash: d35cc74ab2fa79530ac09256e315a780023d833b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463840"
---
# <a name="search-and-ews-in-exchange"></a>Búsqueda y EWS en Exchange

Descubra cómo buscar elementos en Exchange mediante la API administrada de EWS o EWS.

¿Hace a esto les resulta familiar? Por último, comenzará el proyecto que se ha estado descargando durante semanas y necesitará información sobre el proyecto que su jefe le envió en un correo electrónico hace semanas. En la bandeja de entrada hay cientos de mensajes o incluso miles de ellos. ¿A qué te dedicas? ¿Se desplaza a través del análisis de correo electrónico a cada asunto y remitente hasta que lo encuentra? O bien, puede usar la característica de búsqueda de su cliente de correo electrónico favorito a fin de llegar rápidamente a lo que necesita?

La búsqueda es una característica que debe tener para cualquier cliente de correo electrónico. Pero la búsqueda puede usarse mucho más que solo permitir que los usuarios busquen en su buzón. ¿Su aplicación tiene que procesar citas que se encuentran dentro de ventanas de tiempo específicas? Es posible que necesite informar sobre todos los elementos de tareas con un estado específico o mover todos los contactos con un nombre de empresa específico a una carpeta diferente. La búsqueda puede ayudar con todos estos requisitos.

## <a name="search-basics"></a>Conceptos básicos de la búsqueda
<a name="bk_SearchBasics"> </a>

La API administrada de EWS y EWS ofrecen dos métodos básicos para especificar una búsqueda. Puede usar un [filtro de búsqueda](how-to-use-search-filters-with-ews-in-exchange.md) o una [cadena de consulta](how-to-perform-an-aqs-search-by-using-ews-in-exchange.md). El método que use dependerá de la intención de la búsqueda.

**Tabla 1. Escenarios para filtros de búsqueda y consultas de búsqueda**

|**Si quiere...**|**Usar un...**|**Notas**|
|:-----|:-----|:-----|
|Limitar la búsqueda a una propiedad específica o a un conjunto de propiedades  <br/> |Filtro de búsqueda  <br/> |Los filtros de búsqueda proporcionan el mejor nivel de control sobre las propiedades que se buscan. Aunque las cadenas de consulta pueden dirigir un conjunto limitado de propiedades mediante la sintaxis de consulta avanzada (AQS), los filtros de búsqueda pueden dirigirse a cualquier propiedad.  <br/> |
|Crear búsquedas con varios criterios  <br/> |Filtro de búsqueda  <br/> |Con los filtros de búsqueda, se pueden combinar varios criterios de búsqueda con mezclar lógicos o ORs, lo que permite búsquedas como "asunto contiene ' notas de la reunión" y Sender es igual a ' Sadie Daniels ' ". Aunque las cadenas de consulta también pueden unirse a varios criterios de búsqueda, se limitan al conjunto de propiedades admitidas por las cadenas de consulta.  <br/> |
|Buscar propiedades personalizadas  <br/> |Filtro de búsqueda  <br/> |Los filtros de búsqueda pueden tener como objetivo propiedades personalizadas. Las cadenas de consulta no buscan propiedades personalizadas.  <br/> |
|Realizar una búsqueda de propiedades de cadena con distinción de mayúsculas y minúsculas  <br/> |Filtro de búsqueda  <br/> |Las búsquedas de cadenas de consulta no distinguen mayúsculas de minúsculas.  <br/> |
|Controlar el modo de contención al buscar propiedades de cadena  <br/> |Filtro de búsqueda  <br/> |Las búsquedas de cadenas de consulta siempre son búsquedas de subcadenas. Si necesita buscar prefijos específicos o requerir coincidencias exactas, el filtro de búsqueda es la mejor opción.  <br/> |
|Buscar carpetas  <br/> |Filtro de búsqueda  <br/> |EWS no admite la búsqueda de carpetas con una cadena de consulta.  <br/> |
|Crear una carpeta de búsqueda  <br/> |Filtro de búsqueda  <br/> |EWS no admite la creación de carpetas de búsqueda con una cadena de consulta.  <br/> |
|Buscar en todas las propiedades de uso frecuente  <br/> |Cadena de consulta  <br/> |Las cadenas de consulta que no contienen AQS buscarán en todas las propiedades que se usan con más frecuencia. Por ejemplo, un valor de cadena de consulta "Mack Chaves" devolverá todos los mensajes enviados por Mack Chaves, así como cualquier mensaje que contenga "Mack Chaves" en el cuerpo o el asunto.  <br/> |
|Crear una búsqueda basada en una entrada de usuario simple  <br/> |Cadena de consulta  <br/> |Una cadena de consulta es una buena opción para permitir que un usuario final realice una búsqueda rápida escribiendo en una cadena simple. Como una búsqueda de cadena de consulta incluye todas las propiedades que se usan con frecuencia, los resultados contendrán los elementos que contengan los términos de búsqueda del usuario.  <br/> |

### <a name="using-a-search-filter"></a>Uso de un filtro de búsqueda

Los filtros de búsqueda proporcionan una amplia variedad de opciones de búsqueda y el mayor grado de control sobre la forma en que se realiza la búsqueda. Puede usar filtros de búsqueda para realizar búsquedas básicas de igualdad y comparación, pero también puede buscar en el contenido de las propiedades de cadena o realizar comparaciones de máscara de la máscara.

Por ejemplo, puede buscar el contenido del asunto de los elementos mediante la clase [SearchFilter. ContainsSubstring](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.searchfilter.containssubstring%28v=exchg.80%29.aspx) en la API administrada de EWS. En este ejemplo, se crea un filtro de búsqueda para buscar el asunto de la subcadena "Notas de la reunión", pero se omite la distinción entre mayúsculas y minúsculas.

```cs
SearchFilter.ContainsSubstring subjectFilter = new SearchFilter.ContainsSubstring(ItemSchema.Subject,
    "meeting notes", ContainmentMode.Substring, ComparisonMode.IgnoreCase);
```

También puede buscar en propiedades personalizadas. En este ejemplo, se busca en la propiedad personalizada **itemIndex** los valores mayores que 3.

```cs
Guid MyAppGuid = new Guid("{AA3DF801-4FC7-401F-BBC1-7C93D6498C2E}");
ExtendedPropertyDefinition customPropDefinition =
    new ExtendedPropertyDefinition(MyAppGuid, "ItemIndex", MapiPropertyType.Integer);
SearchFilter.IsGreaterThan customPropFilter =
    new SearchFilter.IsGreaterThan(customPropDefinition, 3);
```

También puede combinar varios filtros de búsqueda para crear búsquedas más complejas. Por ejemplo, puede combinar los dos filtros anteriores con un AND lógico mediante la clase [SearchFilter. SearchFilterCollection](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.searchfilter.searchfiltercollection%28v=exchg.80%29.aspx) .

```cs
SearchFilter.SearchFilterCollection compoundFilter =
    new SearchFilter.SearchFilterCollection(LogicalOperator.And, subjectFilter, customPropFilter);
```

### <a name="using-a-query-string"></a>Uso de una cadena de consulta

Las cadenas de consulta proporcionan un enfoque diferente para la búsqueda. Tiene menos control sobre los campos que se buscan y cómo se realiza la búsqueda cuando se usa una búsqueda de cadena de consulta. No es eso lo malo. En algunos casos, es posible que quiera convertir una red más ancha para hablar.

Por ejemplo, puede buscar "Notas de la reunión" mediante el método de la API administrada de EWS [ExchangeService. FindItems](https://msdn.microsoft.com/library/jj223808%28v=exchg.80%29.aspx) .

```cs
FindItemsResults<Item> results = service.FindItems(folder, "meeting notes", view);
```

Si compara los resultados de esta búsqueda con los resultados del ejemplo de búsqueda **SearchFilter. ContainsSubstring** anterior, esta búsqueda contendrá más resultados. La búsqueda del filtro de búsqueda devolverá solo los elementos que contengan "Notas de la reunión" en el asunto, mientras que esta búsqueda devolverá los elementos que contengan "Notas de la reunión" en los campos asunto, cuerpo y otros.

Echemos un vistazo a cómo se puede refinar la cadena de consulta para que se acerque a los resultados que se ven en el filtro de búsqueda. Con AQS, puede limitar la búsqueda al asunto.

```cs
FindItemsResults<Item> results = service.FindItems(folder, "subject:meeting notes", view);
```

Esto está más cerca, pero los resultados todavía no son iguales. Si usa una cadena de consulta con varias palabras, obtendrá coincidencias incluso si las palabras no están en el orden especificado o incluso si no son adyacentes. Con la cadena de consulta "Subject: notas de la reunión" obtendrá resultados para "Notas de la reunión", "Notas de la reunión" y así sucesivamente. Para refinar aún más, puede ajustar los términos de búsqueda entre comillas dobles para indicar que solo desea esa frase.

```cs
FindItemsResults<Item> results = service.FindItems(folder, "subject:\"meeting notes\"", view);
```

## <a name="requesting-specific-properties-in-search-results"></a>Solicitar propiedades específicas en los resultados de búsqueda
<a name="bk_RequestSpecific"> </a>

De forma predeterminada, los resultados de la búsqueda contendrán todas las propiedades de los elementos que coinciden con la búsqueda. En algunos casos, esto puede ser lo que se desea, pero en la mayoría de los casos la aplicación solo requiere un conjunto discreto de propiedades. En este caso, debe limitar el conjunto de propiedades que se devuelven a las propiedades que necesita la aplicación. En el siguiente ejemplo, se usa la clase [ItemView](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.itemview%28v=exchg.80%29.aspx) para limitar las propiedades devueltas al asunto, la fecha y la hora de recepción y el identificador de los elementos.

```cs
ItemView view = new ItemView(10);
// Creating a new PropertySet with this constructor includes
// ItemSchema.Id.
view.PropertySet = new PropertySet(ItemSchema.Subject, ItemSchema.DateTimeReceived);
```

## <a name="controlling-search-depth"></a>Controlar la profundidad de búsqueda
<a name="bk_SearchDepth"> </a>

Al establecer el recorrido en la vista, se controla la profundidad y el ámbito de la búsqueda.

**Tabla 2. Buscar valores de recorrido**

|**Valor de recorrido**|**Se aplica a**|**Descripción**|
|:-----|:-----|:-----|
|Profunda  <br/> |Elementos y carpetas  <br/> |Las búsquedas rasas se limitan a elementos secundarios de la carpeta en la que se busca.  <br/> |
|Gran  <br/> |Elementos (solo con carpetas de búsqueda) y carpetas  <br/> |Las búsquedas en profundidad buscan en la carpeta que se busca y en las subcarpetas de forma recursiva.  <br/> |
|Están  <br/> |Elementos  <br/> |Las búsquedas asociadas solo incluyen elementos asociados de la carpeta en la que se busca. Los elementos asociados son elementos ocultos dentro de la carpeta.  <br/> |
|SoftDeleted  <br/> |Elementos y carpetas  <br/> |Este tipo de recorrido está en desuso. Las búsquedas de SoftDeleted solo incluyen elementos que están en el contenedor. El contenedor se ha reemplazado por la [carpeta elementos recuperables](https://docs.microsoft.com/exchange/policy-and-compliance/recoverable-items-folder/recoverable-items-folder) de Exchange Online, Exchange online como parte de Office 365 y las versiones de Exchange que comienzan con Exchange 2010.  <br/> |

## <a name="managing-search-results"></a>Administración de los resultados de búsqueda
<a name="bk_ManageSearchResults"> </a>

La API administrada de EWS y EWS también permiten cambiar la forma en que se devuelven los resultados de la búsqueda. Puede usar vistas para especificar qué propiedades se incluyen en los resultados, ordenar los resultados y paginar los resultados para obtener solo un número determinado de resultados por respuesta. También puede agrupar los resultados por valores de campo específicos y controlar la profundidad de una búsqueda especificando un tipo de recorrido. Por último, puede usar carpetas de búsqueda para crear búsquedas persistentes que se actualizan dinámicamente a medida que se reciben nuevos elementos.

### <a name="sorting"></a>Ordenación

Puede conseguir que el servidor devuelva resultados ordenados, lo que puede facilitar la visualización o el procesamiento de elementos en orden. En este ejemplo, los resultados se ordenarán por la fecha y hora de recepción, con los elementos más recientes en primer lugar.

```cs
view.OrderBy.Add(ItemSchema.DateTimeReceived, SortDirection.Descending);
```

### <a name="paging"></a>Paginación

Cuando se envía una solicitud de búsqueda mediante la API administrada de EWS o EWS, se especifica un tamaño de vista, que controla el número máximo de elementos devueltos. Sin embargo, el número de elementos del servidor que coinciden con la búsqueda puede ser mayor que el tamaño de la vista. En este caso, el servidor indica que hay más elementos disponibles. Puede [usar la paginación para repetir la búsqueda](how-to-perform-paged-searches-by-using-ews-in-exchange.md) y obtener el siguiente conjunto de resultados.

Por ejemplo, puede enviar una solicitud de búsqueda con un tamaño de vista de 10. Puede haber 15 elementos en el servidor que coinciden con la búsqueda, pero solo recibirá los 10 primeros, junto con un indicador (el [FindItemsResults \<TItem\> . Propiedad MoreAvailable](https://msdn.microsoft.com/library/dd635477%28v=exchg.80%29.aspx) si está usando la API administrada de EWS), hay más resultados en el servidor. A continuación, puede enviar la misma búsqueda con un desplazamiento de 10 para solicitar los 10 elementos siguientes que coincidan con la búsqueda. El servidor devolverá los cinco elementos restantes.

**Figura 1. Ejemplo de búsqueda paginada**

![Ilustración que muestra una búsqueda paginada. Se envía una solicitud inicial de 10 elementos. Se envía una segunda solicitud de los 10 elementos siguientes.](media/Ex15_Search_PagedSearch.png)

### <a name="grouping"></a>Agrupación

 Exchange permite agrupar los resultados de la búsqueda por un campo específico. Esto puede ayudar a dividir los resultados de la búsqueda en conjuntos más fáciles de administrar. Por ejemplo, puede buscar "Notas de la reunión" y agrupar los resultados por remitente. Como se muestra en la siguiente figura, los elementos devueltos se separan en grupos, con todos los elementos que coinciden con los criterios del mismo remitente en un grupo: todos los elementos coincidentes de otro remitente en otro grupo, y así sucesivamente.

**Figura 2. Resultados de la búsqueda agrupados por remitente**

![Ilustración que muestra los resultados de búsqueda agrupados por remitente.](media/Ex15_Search_GroupedResults.png)

## <a name="search-folders"></a>Carpetas de búsqueda
<a name="bk_SearchFolders"> </a>

Con una búsqueda normal, la búsqueda se ejecuta, los resultados se devuelven a la aplicación para su procesamiento y la búsqueda deja de existir. Las carpetas de búsqueda proporcionan una forma de hacer que una búsqueda sea persistente. Esta es una buena opción para las búsquedas que sabe que querrá ejecutar varias veces. En lugar de ejecutar la misma búsqueda repetidamente, lo que hace que el servidor evalúe la búsqueda desde cero cada vez, una carpeta de búsqueda activa siempre la búsqueda, lo que permite al servidor actualizar el conjunto de resultados existente a medida que se agregan o quitan elementos del ámbito de búsqueda. Las carpetas de búsqueda actúan como carpetas normales, en que aparecen como carpetas que contienen elementos. La diferencia es que los únicos elementos contenidos en la carpeta son los que coinciden con los criterios de búsqueda asociados a la carpeta. Una vez que se crea una carpeta de búsqueda, la aplicación puede obtener resultados actualizados de la búsqueda con solo comprobar el contenido de la carpeta.

La creación de una carpeta de búsqueda es sencilla cuando se domina la creación de filtros de búsqueda. En el siguiente ejemplo, se crea una carpeta de búsqueda para mostrar todos los mensajes de correo electrónico con un asunto que contenga "Notas de la reunión".

```cs
static void CreateSearchFolder(ExchangeService service)
{
    SearchFilter.ContainsSubstring subjectFilter = new SearchFilter.ContainsSubstring(ItemSchema.Subject,
        "meeting notes", ContainmentMode.Substring, ComparisonMode.IgnoreCase);
    SearchFolder searchFolder = new SearchFolder(service);
    searchFolder.DisplayName = "Meeting Notes";
    searchFolder.SearchParameters.RootFolderIds.Add(WellKnownFolderName.Inbox);
    searchFolder.SearchParameters.Traversal = SearchFolderTraversal.Deep;
    searchFolder.SearchParameters.SearchFilter = subjectFilter;
    searchFolder.Save(WellKnownFolderName.SearchFolders);
}
```

## <a name="in-this-section"></a>En esta sección
<a name="bk_InThisSection"> </a>

- [Usar filtros de búsqueda con EWS en Exchange](how-to-use-search-filters-with-ews-in-exchange.md)

- [Realizar una búsqueda AQS con EWS en Exchange](how-to-perform-an-aqs-search-by-using-ews-in-exchange.md)

- [Realizar búsquedas paginadas mediante EWS en Exchange](how-to-perform-paged-searches-by-using-ews-in-exchange.md)

- [Realizar búsquedas agrupadas mediante EWS en Exchange](how-to-perform-grouped-searches-by-using-ews-in-exchange.md)

- [Trabajar con carpetas de búsqueda mediante EWS en Exchange](how-to-work-with-search-folders-by-using-ews-in-exchange.md)

## <a name="see-also"></a>Vea también


- [Desarrollar clientes de servicios web de Exchange](develop-web-service-clients-for-exchange.md)

- [Carpeta elementos recuperables](https://docs.microsoft.com/exchange/policy-and-compliance/recoverable-items-folder/recoverable-items-folder)

- [ExchangeService. FindItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx)

- [Parámetros de directivas de limitación que afectan a las operaciones de búsqueda de EWS](ews-throttling-in-exchange.md#throttling-policy-parameters-that-affect-ews-search-operations)
