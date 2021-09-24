---
title: Búsqueda y EWS en Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 9fa5b836-857e-401d-9450-51e7dbc69104
description: Descubra cómo buscar elementos en Exchange mediante la API administrada ews o EWS.
ms.openlocfilehash: f78f4625880480e4f0d1ebb683c6e7c2c7fa83e0
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59524437"
---
# <a name="search-and-ews-in-exchange"></a>Búsqueda y EWS en Exchange

Descubra cómo buscar elementos en Exchange mediante la API administrada ews o EWS.

¿Hace a esto les resulta familiar? Por fin está iniciando el proyecto que ha estado a punto de finalizar durante semanas y necesita información sobre el proyecto que su administrador le envió por correo electrónico semanas atrás. La Bandeja de entrada tiene cientos o quizás miles de mensajes. ¿A qué te dedicas? ¿Se desplaza por el correo electrónico analizando cada asunto y remitente hasta encontrarlo? ¿O usa la característica de búsqueda en su cliente de correo electrónico favorito para cero rápidamente en lo que necesita?

La búsqueda es posiblemente una característica imprescindible para cualquier cliente de correo electrónico. Pero la búsqueda puede usarse para mucho más que permitir a los usuarios buscar en su buzón. ¿La aplicación necesita procesar citas que se encuentran dentro de ventanas de tiempo específico? Quizás necesite informar sobre todos los elementos de tarea con un estado específico o mover todos los contactos con un nombre de empresa específico a una carpeta diferente. La búsqueda puede ayudar con todos estos requisitos.

## <a name="search-basics"></a>Conceptos básicos de búsqueda
<a name="bk_SearchBasics"> </a>

La API administrada ews y EWS ofrecen dos métodos básicos para especificar una búsqueda. Puede usar un filtro [de búsqueda o](how-to-use-search-filters-with-ews-in-exchange.md) una cadena de [consulta](how-to-perform-an-aqs-search-by-using-ews-in-exchange.md). El método que use depende de la intención detrás de la búsqueda.

**Tabla 1. Escenarios para filtros de búsqueda y consultas de búsqueda**

|**Si quiere...**|**Use un...**|**Notas**|
|:-----|:-----|:-----|
|Limitar la búsqueda a una propiedad o conjunto de propiedades específicos  <br/> |Filtro de búsqueda  <br/> |Los filtros de búsqueda proporcionan el mejor nivel de control sobre qué propiedades se buscan. Aunque las cadenas de consulta pueden tener como destino un conjunto limitado de propiedades mediante la sintaxis de consulta avanzada (AQS), los filtros de búsqueda pueden tener como destino cualquier propiedad.  <br/> |
|Crear búsquedas con varios criterios  <br/> |Filtro de búsqueda  <br/> |Con los filtros de búsqueda, se pueden unir varios criterios de búsqueda con AND lógicos o OR, lo que permite búsquedas como "asunto contiene 'Notas de reunión' Y el remitente es igual a 'Sadie Daniels'". Aunque las cadenas de consulta también pueden unirse a varios criterios de búsqueda, se limitan al conjunto de propiedades admitidas por cadenas de consulta.  <br/> |
|Buscar propiedades personalizadas  <br/> |Filtro de búsqueda  <br/> |Los filtros de búsqueda pueden dirigirse a propiedades personalizadas. Las cadenas de consulta no buscan propiedades personalizadas.  <br/> |
|Realizar una búsqueda entre mayúsculas y minúsculas de propiedades de cadena  <br/> |Filtro de búsqueda  <br/> |Las búsquedas de cadenas de consulta no distinguen mayúsculas de minúsculas.  <br/> |
|Controlar el modo de contención al buscar propiedades de cadena  <br/> |Filtro de búsqueda  <br/> |Las búsquedas de cadenas de consulta siempre son búsquedas de subcadenas. Si necesita buscar prefijos específicos o requerir coincidencias exactas, un filtro de búsqueda es la mejor opción.  <br/> |
|Buscar carpetas  <br/> |Filtro de búsqueda  <br/> |EWS no admite la búsqueda de carpetas con una cadena de consulta.  <br/> |
|Crear una carpeta de búsqueda  <br/> |Filtro de búsqueda  <br/> |EWS no admite la creación de carpetas de búsqueda con una cadena de consulta.  <br/> |
|Buscar en todas las propiedades usadas habitualmente  <br/> |Cadena de consulta  <br/> |Las cadenas de consulta que no contienen AQS buscarán en todas las propiedades usadas habitualmente. Por ejemplo, un valor de cadena de consulta de "Mack Chaves" devolverá todos los mensajes enviados por Mack Chaves, así como los mensajes que tengan "Mack Chaves" en el cuerpo o el asunto.  <br/> |
|Construir una búsqueda basada en la entrada sencilla del usuario  <br/> |Cadena de consulta  <br/> |Una cadena de consulta es una excelente opción para permitir que un usuario final realice una búsqueda rápida escribiendo una cadena sencilla. Dado que una búsqueda de cadena de consulta incluye todas las propiedades usadas habitualmente, los resultados contendrán los elementos que contengan los términos de búsqueda del usuario.  <br/> |

### <a name="using-a-search-filter"></a>Uso de un filtro de búsqueda

Los filtros de búsqueda le dan una amplia variedad de opciones de búsqueda y el mayor grado de control sobre cómo se realiza la búsqueda. Puede usar filtros de búsqueda para realizar búsquedas básicas de igualdad y comparación, pero también puede buscar dentro del contenido de las propiedades de cadena o realizar comparaciones de máscaras de bits.

Por ejemplo, puede buscar en el contenido del asunto de los elementos mediante la clase [SearchFilter.ContainsSubstring](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.searchfilter.containssubstring%28v=exchg.80%29.aspx) en la API administrada ews. En este ejemplo, se crea un filtro de búsqueda para buscar en el asunto la subcadena "notas de reunión", ignorando caso.

```cs
SearchFilter.ContainsSubstring subjectFilter = new SearchFilter.ContainsSubstring(ItemSchema.Subject,
    "meeting notes", ContainmentMode.Substring, ComparisonMode.IgnoreCase);
```

También puede buscar en propiedades personalizadas. En este ejemplo, se busca en la **propiedad personalizada ItemIndex** valores mayores que 3.

```cs
Guid MyAppGuid = new Guid("{AA3DF801-4FC7-401F-BBC1-7C93D6498C2E}");
ExtendedPropertyDefinition customPropDefinition =
    new ExtendedPropertyDefinition(MyAppGuid, "ItemIndex", MapiPropertyType.Integer);
SearchFilter.IsGreaterThan customPropFilter =
    new SearchFilter.IsGreaterThan(customPropDefinition, 3);
```

También puede combinar varios filtros de búsqueda para crear búsquedas más complejas. Por ejemplo, puede combinar los dos filtros anteriores con un AND lógico mediante la [clase SearchFilter.SearchFilterCollection.](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.searchfilter.searchfiltercollection%28v=exchg.80%29.aspx)

```cs
SearchFilter.SearchFilterCollection compoundFilter =
    new SearchFilter.SearchFilterCollection(LogicalOperator.And, subjectFilter, customPropFilter);
```

### <a name="using-a-query-string"></a>Uso de una cadena de consulta

Las cadenas de consulta proporcionan un enfoque diferente para la búsqueda. Tiene menos control sobre los campos que se buscan y cómo se realiza la búsqueda cuando se usa una búsqueda de cadena de consulta. No es que eso sea algo malo. En algunos casos, es posible que quieras convertir una red más ancha, por así decirlo.

Por ejemplo, puede buscar "notas de reunión" mediante el método de api administrada EWS [ExchangeService.FindItems.](https://msdn.microsoft.com/library/jj223808%28v=exchg.80%29.aspx)

```cs
FindItemsResults<Item> results = service.FindItems(folder, "meeting notes", view);
```

Si compara los resultados de esta búsqueda con los resultados del ejemplo de búsqueda **SearchFilter.ContainsSubstring** anterior, esta búsqueda contendrá más resultados. La búsqueda de filtro de búsqueda devolverá solo los elementos que tengan "notas de reunión" en el asunto, mientras que esta búsqueda devolverá elementos que tengan "notas de reunión" en el asunto, el cuerpo y otros campos.

Echemos un vistazo a cómo puede refinar la cadena de consulta para acercarse a los resultados que ve en el filtro de búsqueda. Con AQS, puede limitar la búsqueda al asunto.

```cs
FindItemsResults<Item> results = service.FindItems(folder, "subject:meeting notes", view);
```

Esto está más cerca, pero los resultados siguen sin ser exactamente los mismos. Cuando se usa una cadena de consulta con varias palabras, se obtienen coincidencias incluso si las palabras no están en el orden especificado, o incluso si no están adyacentes entre sí. Con la cadena de consulta "subject:meeting notes", se obtienen coincidencias para "notas de reunión", "notas de la reunión", y así sucesivamente. Para refinar aún más, puede ajustar los términos de búsqueda entre comillas dobles para indicar que solo desea esa frase.

```cs
FindItemsResults<Item> results = service.FindItems(folder, "subject:\"meeting notes\"", view);
```

## <a name="requesting-specific-properties-in-search-results"></a>Solicitar propiedades específicas en los resultados de búsqueda
<a name="bk_RequestSpecific"> </a>

De forma predeterminada, los resultados de la búsqueda contendrán todas las propiedades de los elementos que coincidan con la búsqueda. En algunos casos, esto puede ser lo que desea, pero en la mayoría de los casos la aplicación solo requiere un conjunto discreto de propiedades. En este caso, debe limitar el conjunto de propiedades que se devuelven solo a las propiedades que necesita la aplicación. En el ejemplo siguiente, se usa [la clase ItemView](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.itemview%28v=exchg.80%29.aspx) para limitar las propiedades devueltas al asunto, la fecha y hora recibidas y el identificador de los elementos.

```cs
ItemView view = new ItemView(10);
// Creating a new PropertySet with this constructor includes
// ItemSchema.Id.
view.PropertySet = new PropertySet(ItemSchema.Subject, ItemSchema.DateTimeReceived);
```

## <a name="controlling-search-depth"></a>Controlar la profundidad de búsqueda
<a name="bk_SearchDepth"> </a>

Al establecer el recorrido en la vista, se controla la profundidad y el ámbito de la búsqueda.

**Tabla 2. Valores de recorrido de búsqueda**

|**Valor de traversal**|**Se aplica a**|**Descripción**|
|:-----|:-----|:-----|
|Superficial  <br/> |Elementos y carpetas  <br/> |Las búsquedas superficiales se limitan a los secundarios directos de la carpeta que se está buscando.  <br/> |
|Deep  <br/> |Elementos (solo con carpetas de búsqueda) y Carpetas  <br/> |Las búsquedas profundas buscan de forma recursiva la carpeta que se está buscando y las subcarpetas.  <br/> |
|Asociado  <br/> |Elementos  <br/> |Las búsquedas asociadas solo incluyen elementos asociados de la carpeta que se está buscando. Los elementos asociados son elementos ocultos dentro de la carpeta.  <br/> |
|SoftDeleted  <br/> |Elementos y carpetas  <br/> |Este tipo de recorrido está en desuso. Las búsquedas de SoftDeleted solo incluyen elementos que están en el contenedor. El contenedor ha sido [](https://docs.microsoft.com/exchange/policy-and-compliance/recoverable-items-folder/recoverable-items-folder) reemplazado por la carpeta Elementos recuperables en Exchange Online, Exchange Online como parte de Office 365 y versiones de Exchange a partir de Exchange 2010.  <br/> |

## <a name="managing-search-results"></a>Administración de resultados de búsqueda
<a name="bk_ManageSearchResults"> </a>

La API administrada ews y EWS también permiten cambiar la forma en que se devuelven los resultados de la búsqueda. Puede usar vistas para especificar qué propiedades se incluyen en los resultados, ordenar los resultados y paginar los resultados para obtener solo un número establecido de resultados por respuesta. También puede agrupar los resultados por valores de campo específicos y controlar la profundidad de una búsqueda especificando un tipo de recorrido. Por último, puede usar carpetas de búsqueda para crear búsquedas persistentes que se actualizan dinámicamente a medida que llegan nuevos elementos.

### <a name="sorting"></a>Ordenación

Puede obtener que el servidor devuelva resultados ordenados, lo que puede facilitar la visualización o el proceso de elementos en orden. En este ejemplo, los resultados se ordenarán por la fecha y hora recibidas, siendo los elementos más nuevos los primeros.

```cs
view.OrderBy.Add(ItemSchema.DateTimeReceived, SortDirection.Descending);
```

### <a name="paging"></a>Paginación

Cuando se envía una solicitud de búsqueda mediante la API administrada ews o EWS, se especifica un tamaño de vista, que controla el número máximo de elementos devueltos. Sin embargo, el número de elementos del servidor que coinciden con la búsqueda puede ser mayor que el tamaño de la vista. En este caso, el servidor indica que hay más elementos disponibles. Puede usar [la paginación para repetir la búsqueda](how-to-perform-paged-searches-by-using-ews-in-exchange.md) y obtener el siguiente conjunto de resultados.

Por ejemplo, puede enviar una solicitud de búsqueda con un tamaño de vista de 10. Puede haber 15 elementos en el servidor que coincidan con la búsqueda, pero solo recuperará los primeros 10, junto con un indicador [(FindItemsResults \<TItem\> . Propiedad MoreAvailable](https://msdn.microsoft.com/library/dd635477%28v=exchg.80%29.aspx) si usa la API administrada ews) que hay más resultados en el servidor. A continuación, puede enviar la misma búsqueda con un desplazamiento de 10 para solicitar los siguientes 10 elementos que coincidan con la búsqueda. El servidor devolverá los cinco elementos restantes.

**Figura 1. Ejemplo de búsqueda paginada**

![Ilustración que muestra una búsqueda paginada. Se envía una solicitud inicial de 10 elementos. Se envía una segunda solicitud de los 10 elementos siguientes.](media/Ex15_Search_PagedSearch.png)

### <a name="grouping"></a>Agrupación

 Exchange permite agrupar los resultados de búsqueda por un campo específico. Esto puede ayudar a dividir los resultados de la búsqueda en conjuntos más manejables. Por ejemplo, puede buscar "notas de reunión" y agrupar los resultados por remitente. Como se muestra en la figura siguiente, los elementos devueltos se separarán en grupos, con todos los elementos que coincidan con los criterios del mismo remitente en un grupo, todos los elementos que coincidan de otro remitente de otro grupo, y así sucesivamente.

**Figura 2. Resultados de búsqueda agrupados por remitente**

![Ilustración que muestra los resultados de búsqueda agrupados por remitente.](media/Ex15_Search_GroupedResults.png)

## <a name="search-folders"></a>Carpetas de búsqueda
<a name="bk_SearchFolders"> </a>

Con una búsqueda regular, la búsqueda se ejecuta, los resultados se devuelven a la aplicación para su procesamiento y la búsqueda deja de existir. Las carpetas de búsqueda proporcionan una forma de hacer que una búsqueda sea persistente. Esta es una excelente opción para las búsquedas que sabes que querrás ejecutar varias veces. En lugar de ejecutar la misma búsqueda repetidamente, lo que hace que el servidor evalúe la búsqueda desde cero cada vez, una carpeta de búsqueda realiza una búsqueda siempre activa, lo que permite al servidor actualizar el conjunto de resultados existente a medida que se agregan o quitan elementos del ámbito de búsqueda. Las carpetas de búsqueda actúan como carpetas normales, ya que aparecen como carpetas que tienen elementos en ellas. La diferencia es que los únicos elementos contenidos en la carpeta son aquellos que coinciden con los criterios de búsqueda asociados a la carpeta. Después de crear una carpeta de búsqueda, la aplicación puede obtener los resultados actualizados de la búsqueda comprobando el contenido de la carpeta.

La creación de una carpeta de búsqueda es sencilla cuando se ha masterado la creación de filtros de búsqueda. En el ejemplo siguiente, se crea una carpeta de búsqueda para mostrar todo el correo electrónico con un asunto que contiene "notas de reunión".

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

- [Realizar una búsqueda de AQS mediante EWS en Exchange](how-to-perform-an-aqs-search-by-using-ews-in-exchange.md)

- [Realizar búsquedas paginadas utilizando EWS en Exchange](how-to-perform-paged-searches-by-using-ews-in-exchange.md)

- [Realizar búsquedas agrupadas mediante EWS en Exchange](how-to-perform-grouped-searches-by-using-ews-in-exchange.md)

- [Trabajar con carpetas de búsqueda mediante EWS en Exchange](how-to-work-with-search-folders-by-using-ews-in-exchange.md)

## <a name="see-also"></a>Vea también


- [Desarrollo de clientes de servicios web de Exchange](develop-web-service-clients-for-exchange.md)

- [Carpeta Elementos recuperables](https://docs.microsoft.com/exchange/policy-and-compliance/recoverable-items-folder/recoverable-items-folder)

- [ExchangeService.FindItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx)

- [Parámetros de directiva de limitación que afectan a las operaciones de búsqueda de EWS](ews-throttling-in-exchange.md#throttling-policy-parameters-that-affect-ews-search-operations)
