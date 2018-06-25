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
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763197"
---
# <a name="use-search-filters-with-ews-in-exchange"></a><span data-ttu-id="4b0a3-103">Use los filtros de búsqueda con EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="4b0a3-103">Use search filters with EWS in Exchange</span></span>

<span data-ttu-id="4b0a3-104">Descubra cómo usar filtros de búsqueda con la API administrada de EWS o EWS en Exchange.</span><span class="sxs-lookup"><span data-stu-id="4b0a3-104">Find out how to use search filters with the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="4b0a3-105">Filtros de búsqueda es la principal herramienta para expresar los criterios de búsqueda en la API administrada de EWS o aplicación de EWS.</span><span class="sxs-lookup"><span data-stu-id="4b0a3-105">Search filters are the primary tool for expressing search criteria in your EWS Managed API or EWS application.</span></span> <span data-ttu-id="4b0a3-106">Se recomienda que utilice filtros de búsqueda, a diferencia de [las cadenas de consulta](how-to-perform-an-aqs-search-by-using-ews-in-exchange.md), para hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="4b0a3-106">We recommend that you use search filters, as opposed to [query strings](how-to-perform-an-aqs-search-by-using-ews-in-exchange.md), to do the following:</span></span>
  
- <span data-ttu-id="4b0a3-107">Buscar en una propiedad concreta o un conjunto de propiedades.</span><span class="sxs-lookup"><span data-stu-id="4b0a3-107">Search on a specific property or set of properties.</span></span>  
- <span data-ttu-id="4b0a3-108">La búsqueda con varios criterios de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="4b0a3-108">Search using multiple search criteria.</span></span>
    
<span data-ttu-id="4b0a3-109">Filtros de búsqueda es la única opción si está realizando una de las siguientes:</span><span class="sxs-lookup"><span data-stu-id="4b0a3-109">Search filters are your only option if you are doing any of the following:</span></span>
  
- <span data-ttu-id="4b0a3-110">Búsqueda de propiedades personalizadas.</span><span class="sxs-lookup"><span data-stu-id="4b0a3-110">Searching custom properties.</span></span>  
- <span data-ttu-id="4b0a3-111">Busca en la realización de cadena entre mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="4b0a3-111">Performing case-sensitive string searches.</span></span>  
- <span data-ttu-id="4b0a3-112">Busca en la realización de prefijo o cadena de coincidencia exacta.</span><span class="sxs-lookup"><span data-stu-id="4b0a3-112">Performing prefix or exact match string searches.</span></span> 
- <span data-ttu-id="4b0a3-113">Busca en la realización de máscara de bits.</span><span class="sxs-lookup"><span data-stu-id="4b0a3-113">Performing bitmask searches.</span></span>
- <span data-ttu-id="4b0a3-114">Busca los elementos que tienen una propiedad concreta se establece, independientemente del valor.</span><span class="sxs-lookup"><span data-stu-id="4b0a3-114">Searching for items that have a specific property set, regardless of value.</span></span>
- <span data-ttu-id="4b0a3-115">Búsqueda de carpetas.</span><span class="sxs-lookup"><span data-stu-id="4b0a3-115">Searching for folders.</span></span>
- <span data-ttu-id="4b0a3-116">Creación de las carpetas de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="4b0a3-116">Creating search folders.</span></span>
    
## <a name="determine-what-type-of-search-filter-you-need"></a><span data-ttu-id="4b0a3-117">Determinar qué tipo de filtro de búsqueda necesita</span><span class="sxs-lookup"><span data-stu-id="4b0a3-117">Determine what type of search filter you need</span></span>
<span data-ttu-id="4b0a3-118"><a name="bk_SelectFilter"> </a></span><span class="sxs-lookup"><span data-stu-id="4b0a3-118"></span></span>

<span data-ttu-id="4b0a3-119">Antes de crear un filtro de búsqueda, en primer lugar determine qué tipo de filtro que necesita.</span><span class="sxs-lookup"><span data-stu-id="4b0a3-119">Before you create a search filter, first determine which type of filter you need.</span></span> <span data-ttu-id="4b0a3-120">Los tipos de filtro se implementan como clases descendientes de la clase [SearchFilter](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.searchfilter%28v=exchg.80%29.aspx) en la API administrada de EWS y como elementos secundarios del elemento de [restricción](http://msdn.microsoft.com/library/77f19014-d112-4999-8e83-ecc32a117a73%28Office.15%29.aspx) de EWS.</span><span class="sxs-lookup"><span data-stu-id="4b0a3-120">The filter types are implemented as descendant classes of the [SearchFilter](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.searchfilter%28v=exchg.80%29.aspx) class in the EWS Managed API, and as child elements of the [Restriction](http://msdn.microsoft.com/library/77f19014-d112-4999-8e83-ecc32a117a73%28Office.15%29.aspx) element in EWS.</span></span> 
  
<span data-ttu-id="4b0a3-121">**La tabla 1. Tipos de filtros de búsqueda**</span><span class="sxs-lookup"><span data-stu-id="4b0a3-121">**Table 1. Types of search filters**</span></span>

|<span data-ttu-id="4b0a3-122">**Tipo de filtro**</span><span class="sxs-lookup"><span data-stu-id="4b0a3-122">**Filter type**</span></span>|<span data-ttu-id="4b0a3-123">**Clase de la API administrada de EWS**</span><span class="sxs-lookup"><span data-stu-id="4b0a3-123">**EWS Managed API class**</span></span>|<span data-ttu-id="4b0a3-124">**Elemento EWS**</span><span class="sxs-lookup"><span data-stu-id="4b0a3-124">**EWS element**</span></span>|<span data-ttu-id="4b0a3-125">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4b0a3-125">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="4b0a3-126">Contiene el filtro</span><span class="sxs-lookup"><span data-stu-id="4b0a3-126">Contains filter</span></span>  <br/> |[<span data-ttu-id="4b0a3-127">ContainsSubstring</span><span class="sxs-lookup"><span data-stu-id="4b0a3-127">ContainsSubstring</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.searchfilter.containssubstring%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="4b0a3-128">Incluye</span><span class="sxs-lookup"><span data-stu-id="4b0a3-128">Contains</span></span>](http://msdn.microsoft.com/library/476d059d-c243-43e9-b475-319fc413ade2%28Office.15%29.aspx) <br/> |<span data-ttu-id="4b0a3-129">El mejor tipo de filtro que se usará para las comparaciones de cadenas.</span><span class="sxs-lookup"><span data-stu-id="4b0a3-129">The best filter type to use for string comparisons.</span></span> <span data-ttu-id="4b0a3-130">Permite controlar la distinción de mayúsculas y, si se debe omitir espacios en blanco y establecer el modo de contención.</span><span class="sxs-lookup"><span data-stu-id="4b0a3-130">It allows you to control case sensitivity, whether to ignore whitespace, and set the containment mode.</span></span>  <br/> |
|<span data-ttu-id="4b0a3-131">Filtro de máscara de bits</span><span class="sxs-lookup"><span data-stu-id="4b0a3-131">Bitmask filter</span></span>  <br/> |[<span data-ttu-id="4b0a3-132">ExcludesBitmask</span><span class="sxs-lookup"><span data-stu-id="4b0a3-132">ExcludesBitmask</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.searchfilter.excludesbitmask%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="4b0a3-133">Excluye</span><span class="sxs-lookup"><span data-stu-id="4b0a3-133">Excludes</span></span>](http://msdn.microsoft.com/library/bbaeddf6-9a67-4ee0-af99-7a7a5bbdc0e1%28Office.15%29.aspx) <br/> |<span data-ttu-id="4b0a3-134">Permite buscar propiedades de entero como máscaras de bits y sólo devolverá los resultados que tienen bits correspondiente a la máscara de bits especificado no establecido.</span><span class="sxs-lookup"><span data-stu-id="4b0a3-134">Allows you to search integer properties as bitmasks and only return results that have bits corresponding to the specified bitmask unset.</span></span>  <br/> |
|<span data-ttu-id="4b0a3-135">Existe filtro</span><span class="sxs-lookup"><span data-stu-id="4b0a3-135">Exists filter</span></span>  <br/> |[<span data-ttu-id="4b0a3-136">Existe</span><span class="sxs-lookup"><span data-stu-id="4b0a3-136">Exists</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.searchfilter.exists%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="4b0a3-137">Existe</span><span class="sxs-lookup"><span data-stu-id="4b0a3-137">Exists</span></span>](http://msdn.microsoft.com/library/55d568bd-8dbc-4d50-b9d7-54b74a54d4b5%28Office.15%29.aspx) <br/> |<span data-ttu-id="4b0a3-138">Devuelve todos los elementos que tienen la propiedad especificada está presente, independientemente del valor.</span><span class="sxs-lookup"><span data-stu-id="4b0a3-138">Returns all items that have the specified property present, regardless of value.</span></span>  <br/> |
|<span data-ttu-id="4b0a3-139">Filtro de igualdad</span><span class="sxs-lookup"><span data-stu-id="4b0a3-139">Equality filter</span></span>  <br/> |[<span data-ttu-id="4b0a3-140">IsEqualTo</span><span class="sxs-lookup"><span data-stu-id="4b0a3-140">IsEqualTo</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.searchfilter.isequalto%28v=exchg.80%29.aspx) <br/> [<span data-ttu-id="4b0a3-141">IsNotEqualTo</span><span class="sxs-lookup"><span data-stu-id="4b0a3-141">IsNotEqualTo</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.searchfilter.isnotequalto%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="4b0a3-142">IsEqualTo</span><span class="sxs-lookup"><span data-stu-id="4b0a3-142">IsEqualTo</span></span>](http://msdn.microsoft.com/library/48e7e067-049c-4184-8026-071e6f558e8a%28Office.15%29.aspx) <br/> [<span data-ttu-id="4b0a3-143">IsNotEqualTo</span><span class="sxs-lookup"><span data-stu-id="4b0a3-143">IsNotEqualTo</span></span>](http://msdn.microsoft.com/library/e2eff26c-3403-45cd-bb74-1eb98c7dbfcd%28Office.15%29.aspx) <br/> |<span data-ttu-id="4b0a3-144">Compara el valor de la propiedad especificada con un valor constante especificado o el valor de otra propiedad y devolver todos los elementos que tienen un valor igual (en el caso de un filtro **IsEqualTo** ) o un valor que no sean igual (en el caso de un **IsNotEqualTo **filtro).</span><span class="sxs-lookup"><span data-stu-id="4b0a3-144">Compares the value of the specified property with either a specified constant value or the value of another property and return all items that have an equal value (in the case of an **IsEqualTo** filter) or a non-equal value (in the case of an **IsNotEqualTo** filter).</span></span>  <br/> |
|<span data-ttu-id="4b0a3-145">Filtro de prueba relacional</span><span class="sxs-lookup"><span data-stu-id="4b0a3-145">Relational testing filter</span></span>  <br/> |[<span data-ttu-id="4b0a3-146">IsGreaterThan</span><span class="sxs-lookup"><span data-stu-id="4b0a3-146">IsGreaterThan</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.searchfilter.isgreaterthan%28v=exchg.80%29.aspx) <br/> [<span data-ttu-id="4b0a3-147">IsGreaterThanOrEqualTo</span><span class="sxs-lookup"><span data-stu-id="4b0a3-147">IsGreaterThanOrEqualTo</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.searchfilter.isgreaterthanorequalto%28v=exchg.80%29.aspx) <br/> [<span data-ttu-id="4b0a3-148">IsLessThan</span><span class="sxs-lookup"><span data-stu-id="4b0a3-148">IsLessThan</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.searchfilter.islessthan%28v=exchg.80%29.aspx) <br/> [<span data-ttu-id="4b0a3-149">IsLessThanOrEqualTo</span><span class="sxs-lookup"><span data-stu-id="4b0a3-149">IsLessThanOrEqualTo</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.searchfilter.islessthanorequalto%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="4b0a3-150">IsGreaterThan</span><span class="sxs-lookup"><span data-stu-id="4b0a3-150">IsGreaterThan</span></span>](http://msdn.microsoft.com/library/a6e9d462-cfa7-40ec-903e-128c95050352%28Office.15%29.aspx) <br/> [<span data-ttu-id="4b0a3-151">IsGreaterThanOrEqualTo</span><span class="sxs-lookup"><span data-stu-id="4b0a3-151">IsGreaterThanOrEqualTo</span></span>](http://msdn.microsoft.com/library/373cc954-314d-40e2-be03-cc08aefc0d5b%28Office.15%29.aspx) <br/> [<span data-ttu-id="4b0a3-152">IsLessThan</span><span class="sxs-lookup"><span data-stu-id="4b0a3-152">IsLessThan</span></span>](http://msdn.microsoft.com/library/2550469b-6e5d-45a5-9ecc-090d1b409296%28Office.15%29.aspx) <br/> [<span data-ttu-id="4b0a3-153">IsLessThanOrEqualTo</span><span class="sxs-lookup"><span data-stu-id="4b0a3-153">IsLessThanOrEqualTo</span></span>](http://msdn.microsoft.com/library/b5d85eb2-5e15-4d01-ad49-6289e735ad8a%28Office.15%29.aspx) <br/> |<span data-ttu-id="4b0a3-154">Devuelve todos los elementos que tienen un valor para la propiedad especificada en la relación correspondiente a un valor constante especificado u otra propiedad.</span><span class="sxs-lookup"><span data-stu-id="4b0a3-154">Returns all items that have a value for the specified property in the appropriate relation to either a specified constant value or another property.</span></span> <span data-ttu-id="4b0a3-155">Por ejemplo, un filtro **IsGreaterThan** devuelve todos los elementos que tienen un valor que es mayor que el valor especificado en la propiedad especificada.</span><span class="sxs-lookup"><span data-stu-id="4b0a3-155">For example, an **IsGreaterThan** filter returns all items that have a value that is greater than the specified value in the specified property.</span></span>  <br/> |
|<span data-ttu-id="4b0a3-156">Filtro de negación</span><span class="sxs-lookup"><span data-stu-id="4b0a3-156">Negating filter</span></span>  <br/> |[<span data-ttu-id="4b0a3-157">No</span><span class="sxs-lookup"><span data-stu-id="4b0a3-157">Not</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.searchfilter.not%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="4b0a3-158">No</span><span class="sxs-lookup"><span data-stu-id="4b0a3-158">Not</span></span>](http://msdn.microsoft.com/library/1aa16318-7e90-4b19-bce8-dd1a20a66223%28Office.15%29.aspx) <br/> |<span data-ttu-id="4b0a3-159">Niega el resultado de los otros filtros.</span><span class="sxs-lookup"><span data-stu-id="4b0a3-159">Negates the result of the other filters.</span></span>  <br/> |
|<span data-ttu-id="4b0a3-160">Filtro de compuestos</span><span class="sxs-lookup"><span data-stu-id="4b0a3-160">Compound filter</span></span>  <br/> |[<span data-ttu-id="4b0a3-161">SearchFilterCollection</span><span class="sxs-lookup"><span data-stu-id="4b0a3-161">SearchFilterCollection</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.searchfilter.searchfiltercollection%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="4b0a3-162">And</span><span class="sxs-lookup"><span data-stu-id="4b0a3-162">And</span></span>](http://msdn.microsoft.com/library/790246c2-37ad-49a8-91b9-6186d743b011%28Office.15%29.aspx) <br/> [<span data-ttu-id="4b0a3-163">Or</span><span class="sxs-lookup"><span data-stu-id="4b0a3-163">Or</span></span>](http://msdn.microsoft.com/library/4876d83a-73a3-4953-9d95-3048e6b76ccb%28Office.15%29.aspx) <br/> |<span data-ttu-id="4b0a3-164">Combina varios filtros, lo que permite los criterios de búsqueda más complejos.</span><span class="sxs-lookup"><span data-stu-id="4b0a3-164">Combines multiple filters, allowing for more complex search criteria.</span></span>  <br/> |
   
### <a name="contains-filter"></a><span data-ttu-id="4b0a3-165">Contiene el filtro</span><span class="sxs-lookup"><span data-stu-id="4b0a3-165">Contains filter</span></span>

<span data-ttu-id="4b0a3-166">Contiene un filtro es la mejor opción para la búsqueda de propiedades de cadena.</span><span class="sxs-lookup"><span data-stu-id="4b0a3-166">A contains filter is the best choice for searching string properties.</span></span> <span data-ttu-id="4b0a3-167">Con un contiene filtro, puede controlar aspectos de coincidencia de cadena, como entre mayúsculas y minúsculas y cómo se tratan los espacios en blanco, estableciendo el modo de contención y el modo de comparación.</span><span class="sxs-lookup"><span data-stu-id="4b0a3-167">With a contains filter, you can control aspects of string matching, like case sensitivity and how whitespace is treated, by setting the containment mode and the comparison mode.</span></span>
  
#### <a name="contains-filter-in-the-ews-managed-api"></a><span data-ttu-id="4b0a3-168">Contiene el filtro en la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="4b0a3-168">Contains filter in the EWS Managed API</span></span>
<span data-ttu-id="4b0a3-169"><a name="bk_ContainsEWSMA"> </a></span><span class="sxs-lookup"><span data-stu-id="4b0a3-169"></span></span>

<span data-ttu-id="4b0a3-170">Si se usa la API administrada de EWS, establezca el modo de contención mediante el uso de la propiedad [ContainmentMode](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.searchfilter.containssubstring.containmentmode%28v=exchg.80%29.aspx) de la clase [ContainsSubstring](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.searchfilter.containssubstring%28v=exchg.80%29.aspx) y establecer el modo de comparación mediante el uso de la propiedad [ComparisonMode](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.searchfilter.containssubstring.comparisonmode%28v=exchg.80%29.aspx) de la ** ContainsSubstring** clase.</span><span class="sxs-lookup"><span data-stu-id="4b0a3-170">If you're using the EWS Managed API, you set the containment mode by using the [ContainmentMode](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.searchfilter.containssubstring.containmentmode%28v=exchg.80%29.aspx) property of the [ContainsSubstring](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.searchfilter.containssubstring%28v=exchg.80%29.aspx) class, and you set the comparison mode by using the [ComparisonMode](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.searchfilter.containssubstring.comparisonmode%28v=exchg.80%29.aspx) property of the **ContainsSubstring** class.</span></span> <span data-ttu-id="4b0a3-171">En el ejemplo siguiente se muestra cómo crear un filtro de búsqueda que busca en el campo Asunto de los elementos de la subcadena "notas de la reunión".</span><span class="sxs-lookup"><span data-stu-id="4b0a3-171">The following example shows you how to create a search filter that searches the subject field of items for the substring "meeting notes".</span></span> <span data-ttu-id="4b0a3-172">En este ejemplo se omite el caso, pero no omite el espacio en blanco.</span><span class="sxs-lookup"><span data-stu-id="4b0a3-172">This example ignores case, but does not ignore whitespace.</span></span> 
  
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

#### <a name="contains-filter-in-ews"></a><span data-ttu-id="4b0a3-173">Contiene el filtro de EWS</span><span class="sxs-lookup"><span data-stu-id="4b0a3-173">Contains filter in EWS</span></span>
<span data-ttu-id="4b0a3-174"><a name="bk_ContainsEWSMA"> </a></span><span class="sxs-lookup"><span data-stu-id="4b0a3-174"></span></span>

<span data-ttu-id="4b0a3-175">En EWS, se establece el modo de contención mediante el atributo **ContainmentMode** en el elemento [Contains](http://msdn.microsoft.com/library/476d059d-c243-43e9-b475-319fc413ade2%28Office.15%29.aspx) y establecer el modo de comparación mediante el atributo **ContainmentComparison** en el elemento **contiene** .</span><span class="sxs-lookup"><span data-stu-id="4b0a3-175">In EWS, you set the containment mode by using the **ContainmentMode** attribute on the [Contains](http://msdn.microsoft.com/library/476d059d-c243-43e9-b475-319fc413ade2%28Office.15%29.aspx) element, and you set the comparison mode by using the **ContainmentComparison** attribute on the **Contains** element.</span></span> <span data-ttu-id="4b0a3-176">En el ejemplo siguiente se muestra cómo crear un filtro de búsqueda para buscar en el campo Asunto de los elementos de la subcadena "notas de la reunión".</span><span class="sxs-lookup"><span data-stu-id="4b0a3-176">The following example shows you how to create a search filter to search the subject field of items for the substring "meeting notes".</span></span> <span data-ttu-id="4b0a3-177">En este ejemplo se omite el caso, pero no omite el espacio en blanco.</span><span class="sxs-lookup"><span data-stu-id="4b0a3-177">This example ignores case, but does not ignore whitespace.</span></span> 
  
```XML
<t:Contains ContainmentMode="Substring" ContainmentComparison="IgnoreCase">
  <t:FieldURI FieldURI="item:Subject" />
  <t:Constant Value="meeting notes" />
</t:Contains>
```

### <a name="bitmask-filter"></a><span data-ttu-id="4b0a3-178">Filtro de máscara de bits</span><span class="sxs-lookup"><span data-stu-id="4b0a3-178">Bitmask filter</span></span>

<span data-ttu-id="4b0a3-179">Un filtro de máscara de bits permite buscar propiedades de entero como máscaras de bits y devolver resultados donde bits específicos no se establecen en el valor de la propiedad especificada.</span><span class="sxs-lookup"><span data-stu-id="4b0a3-179">A bitmask filter enables you to search integer properties as bitmasks, and return results where specific bits are not set in the value of the specified property.</span></span>
  
#### <a name="bitmask-filter-in-the-ews-managed-api"></a><span data-ttu-id="4b0a3-180">Filtro de máscara de bits en la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="4b0a3-180">Bitmask filter in the EWS Managed API</span></span>

<span data-ttu-id="4b0a3-181">En el ejemplo siguiente se muestra cómo usar la API administrada de EWS para crear un filtro de búsqueda para devolver todos los elementos que tienen un valor en la propiedad personalizada **ItemIndex** (definido en la [ejemplo: buscar elementos mediante el uso de un filtro de búsqueda y la API administrada de EWS](#bk_ExampleEWSMA) sección de este artículo) que no tienen el segundo bit (10 en binario) establecer.</span><span class="sxs-lookup"><span data-stu-id="4b0a3-181">The following example shows you how to use the EWS Managed API to create a search filter to return all items that have a value in the **ItemIndex** custom property (defined in the [Example: Find items by using a search filter and the EWS Managed API](#bk_ExampleEWSMA) section of this article) that do not have the second bit (10 in binary) set.</span></span> 
  
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

#### <a name="bitmask-filter-in-ews"></a><span data-ttu-id="4b0a3-182">Filtro de máscara de bits de EWS</span><span class="sxs-lookup"><span data-stu-id="4b0a3-182">Bitmask filter in EWS</span></span>

<span data-ttu-id="4b0a3-183">En el ejemplo siguiente se muestra cómo usar EWS para crear un filtro de búsqueda para devolver todos los elementos que tienen un valor en la propiedad personalizada **ItemIndex** (definido en la [ejemplo: buscar elementos mediante el uso de un filtro de búsqueda y la API administrada de EWS](#bk_ExampleEWSMA) sección de este artículo) que no tienen el segundo bit (10 en binario) establecer.</span><span class="sxs-lookup"><span data-stu-id="4b0a3-183">The following example shows you how to use EWS to create a search filter to return all items that have a value in the **ItemIndex** custom property (defined in the [Example: Find items by using a search filter and the EWS Managed API](#bk_ExampleEWSMA) section of this article) that do not have the second bit (10 in binary) set.</span></span> 
  
```XML
<t:Excludes>
  <t:ExtendedFieldURI PropertySetId="aa3df801-4fc7-401f-bbc1-7c93d6498c2e" PropertyName="ItemIndex" PropertyType="Integer" />
  <t:Bitmask Value="2" />
</t:Excludes>
```

### <a name="exists-filter"></a><span data-ttu-id="4b0a3-184">Existe filtro</span><span class="sxs-lookup"><span data-stu-id="4b0a3-184">Exists filter</span></span>

<span data-ttu-id="4b0a3-185">Un existe filtro le permite buscar los elementos que tienen una propiedad concreta que se establezca en ellos, independientemente del valor.</span><span class="sxs-lookup"><span data-stu-id="4b0a3-185">An exists filter enables you to search for items that have a specific property set on them, regardless of the value.</span></span>
  
#### <a name="exists-filter-in-the-ews-managed-api"></a><span data-ttu-id="4b0a3-186">Existe el filtro en la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="4b0a3-186">Exists filter in the EWS Managed API</span></span>

<span data-ttu-id="4b0a3-187">En el ejemplo siguiente se muestra cómo crear un filtro de búsqueda para devolver todos los elementos que tienen establecida la propiedad **ItemIndex** personalizada.</span><span class="sxs-lookup"><span data-stu-id="4b0a3-187">The following example shows you how to create a search filter to return all items that have the **ItemIndex** custom property set.</span></span> 
  
```cs
// Find all items that have the custom property set.
SearchFilter.Exists customPropSetFilter =
    new SearchFilter.Exists(customPropDefinition);
```

#### <a name="exists-filter-in-ews"></a><span data-ttu-id="4b0a3-188">Existe el filtro de EWS</span><span class="sxs-lookup"><span data-stu-id="4b0a3-188">Exists filter in EWS</span></span>

<span data-ttu-id="4b0a3-189">En el ejemplo siguiente se muestra cómo crear un filtro de búsqueda para devolver todos los elementos que tienen establecida la propiedad **ItemIndex** personalizada.</span><span class="sxs-lookup"><span data-stu-id="4b0a3-189">The following example shows you how to create a search filter to return all items that have the **ItemIndex** custom property set.</span></span> 
  
```XML
<t:Exists>
  <t:ExtendedFieldURI PropertySetId="aa3df801-4fc7-401f-bbc1-7c93d6498c2e" PropertyName="ItemIndex" PropertyType="Integer" />
</t:Exists>
```

### <a name="equality-filter"></a><span data-ttu-id="4b0a3-190">Filtro de igualdad</span><span class="sxs-lookup"><span data-stu-id="4b0a3-190">Equality filter</span></span>

<span data-ttu-id="4b0a3-191">Filtros de igualdad permiten buscar todos los elementos que tienen un valor para la propiedad especificada que es igual a un valor específico o que no es igual a un valor específico.</span><span class="sxs-lookup"><span data-stu-id="4b0a3-191">Equality filters enable you to search for all items that have a value for the specified property that either equals a specific value or does not equal a specific value.</span></span> <span data-ttu-id="4b0a3-192">El valor se va a comparar con puede ser un valor constante o el valor de otra propiedad en cada elemento.</span><span class="sxs-lookup"><span data-stu-id="4b0a3-192">The value to compare with can be either a constant value or the value of another property on each item.</span></span>
  
#### <a name="equality-filter-in-the-ews-managed-api"></a><span data-ttu-id="4b0a3-193">Filtro de igualdad en la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="4b0a3-193">Equality filter in the EWS Managed API</span></span>

<span data-ttu-id="4b0a3-194">En el ejemplo siguiente se muestra cómo usar la API administrada de EWS para crear un filtro de búsqueda para devolver todos los elementos que no se han leído.</span><span class="sxs-lookup"><span data-stu-id="4b0a3-194">The following example shows you how to use the EWS Managed API to create a search filter to return all items that have not been read.</span></span>
  
```cs
// Find all items that are not marked as read.
SearchFilter.IsEqualTo unreadFilter =
    new SearchFilter.IsEqualTo(EmailMessageSchema.IsRead, false);
```

<span data-ttu-id="4b0a3-195">En el ejemplo siguiente se muestra cómo crear un filtro de búsqueda para devolver todos los elementos que tienen un valor en la propiedad **ItemIndex** que no es igual que el tamaño del elemento.</span><span class="sxs-lookup"><span data-stu-id="4b0a3-195">The following example shows you how to create a search filter to return all items that have a value in the **ItemIndex** property that is not equal to the size of the item.</span></span> 
  
```cs
// Find all items that are marked as read.
SearchFilter.IsNotEqualTo indexNotEqualToSizeFilter =
    new SearchFilter.IsNotEqualTo(customPropDefinition, ItemSchema.Size);
```

#### <a name="equality-filter-in-ews"></a><span data-ttu-id="4b0a3-196">Filtro de igualdad en EWS</span><span class="sxs-lookup"><span data-stu-id="4b0a3-196">Equality filter in EWS</span></span>

<span data-ttu-id="4b0a3-197">En el ejemplo siguiente se muestra cómo usar EWS para crear un filtro de búsqueda para devolver todos los elementos que no se han leído.</span><span class="sxs-lookup"><span data-stu-id="4b0a3-197">The following example shows you how to use EWS to create a search filter to return all items that have not been read.</span></span>
  
```XML
<t:IsEqualTo>
  <t:FieldURI FieldURI="message:IsRead" />
  <t:FieldURIOrConstant>
    <t:Constant Value="false" />
  </t:FieldURIOrConstant>
</t:IsEqualTo>
```

<span data-ttu-id="4b0a3-198">En el ejemplo siguiente se muestra cómo crear un filtro de búsqueda para devolver todos los elementos que tienen un valor en la propiedad **ItemIndex** que no es igual que el tamaño del elemento.</span><span class="sxs-lookup"><span data-stu-id="4b0a3-198">The following example shows you how to create a search filter to return all items that have a value in the **ItemIndex** property that is not equal to the size of the item.</span></span> 
  
```XML
<t:IsNotEqualTo>
  <t:ExtendedFieldURI PropertySetId="aa3df801-4fc7-401f-bbc1-7c93d6498c2e" PropertyName="ItemIndex" PropertyType="Integer" />
  <t:FieldURIOrConstant>
    <t:FieldURI FieldURI="item:Size" />
  </t:FieldURIOrConstant>
</t:IsNotEqualTo>
```

### <a name="relational-testing-filter"></a><span data-ttu-id="4b0a3-199">Filtro de prueba relacional</span><span class="sxs-lookup"><span data-stu-id="4b0a3-199">Relational testing filter</span></span>

<span data-ttu-id="4b0a3-200">Filtros pruebas relacionales permiten buscar todos los elementos que tienen un valor en la propiedad especificada que es mayor que (\>), mayor o igual que (\>=), menor que (\<), o menor o igual que (\<=) un valor especificado.</span><span class="sxs-lookup"><span data-stu-id="4b0a3-200">Relational testing filters enable you to search for all items that have a value in the specified property that is either greater than (\>), greater than or equal to (\>=), less than (\<), or less than or equal to (\<=) a specified value.</span></span> <span data-ttu-id="4b0a3-201">El valor se va a comparar con puede ser un valor constante o el valor de otra propiedad en cada elemento.</span><span class="sxs-lookup"><span data-stu-id="4b0a3-201">The value to compare with can be either a constant value or the value of another property on each item.</span></span>
  
#### <a name="relational-testing-filter-in-the-ews-managed-api"></a><span data-ttu-id="4b0a3-202">Filtro de prueba relacional en la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="4b0a3-202">Relational testing filter in the EWS Managed API</span></span>

<span data-ttu-id="4b0a3-203">En el ejemplo siguiente se muestra cómo usar la API administrada de EWS para crear filtros de búsqueda para devolver todos los elementos con un valor de la propiedad **ItemIndex** que tiene la relación especificada con el valor constante 3.</span><span class="sxs-lookup"><span data-stu-id="4b0a3-203">The following example shows you how to use the EWS Managed API to create search filters to return all items with a value in the **ItemIndex** property that has the specified relationship to the constant value 3.</span></span> 
  
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

#### <a name="relational-testing-filter-in-ews"></a><span data-ttu-id="4b0a3-204">Filtro de prueba relacional de EWS</span><span class="sxs-lookup"><span data-stu-id="4b0a3-204">Relational testing filter in EWS</span></span>

<span data-ttu-id="4b0a3-205">En el ejemplo siguiente se muestra cómo usar EWS para crear un filtro de búsqueda para devolver todos los elementos con un valor de la propiedad **ItemIndex** que es mayor que el valor constante 3.</span><span class="sxs-lookup"><span data-stu-id="4b0a3-205">The following example shows you how to use EWS to create a search filter to return all items with a value in the **ItemIndex** property that is greater than the constant value 3.</span></span> 
  
```XML
<t:IsGreaterThan>
  <t:ExtendedFieldURI PropertySetId="aa3df801-4fc7-401f-bbc1-7c93d6498c2e" PropertyName="ItemIndex" PropertyType="Integer" />
  <t:FieldURIOrConstant>
    <t:Constant Value="3" />
  </t:FieldURIOrConstant>
</t:IsGreaterThan>
```

<span data-ttu-id="4b0a3-206">En el ejemplo siguiente se muestra cómo crear un filtro de búsqueda para devolver todos los elementos con un valor de la propiedad **ItemIndex** que es mayor o igual que el valor constante 3.</span><span class="sxs-lookup"><span data-stu-id="4b0a3-206">The following example shows you how to create a search filter to return all items with a value in the **ItemIndex** property that is greater than or equal to the constant value 3.</span></span> 
  
```XML
<t:IsGreaterThanOrEqualTo>
  <t:ExtendedFieldURI PropertySetId="aa3df801-4fc7-401f-bbc1-7c93d6498c2e" PropertyName="ItemIndex" PropertyType="Integer" />
  <t:FieldURIOrConstant>
    <t:Constant Value="3" />
  </t:FieldURIOrConstant>
</t:IsGreaterThanOrEqualTo>
```

<span data-ttu-id="4b0a3-207">En el ejemplo siguiente se muestra cómo crear un filtro de búsqueda para devolver todos los elementos con un valor de la propiedad **ItemIndex** que es menor que el valor constante 3.</span><span class="sxs-lookup"><span data-stu-id="4b0a3-207">The following example shows you how to create a search filter to return all items with a value in the **ItemIndex** property that is less than the constant value 3.</span></span> 
  
```XML
<t:IsLessThan>
  <t:ExtendedFieldURI PropertySetId="aa3df801-4fc7-401f-bbc1-7c93d6498c2e" PropertyName="ItemIndex" PropertyType="Integer" />
  <t:FieldURIOrConstant>
    <t:Constant Value="3" />
  </t:FieldURIOrConstant>
</t:IsLessThan>
```

<span data-ttu-id="4b0a3-208">En el ejemplo siguiente se muestra cómo crear un filtro de búsqueda para devolver todos los elementos con un valor de la propiedad **ItemIndex** que es menor o igual que el valor constante 3.</span><span class="sxs-lookup"><span data-stu-id="4b0a3-208">The following example shows you how to create a search filter to return all items with a value in the **ItemIndex** property that is less than or equal to the constant value 3.</span></span> 
  
```XML
<t:IsLessThanOrEqualTo>
  <t:ExtendedFieldURI PropertySetId="aa3df801-4fc7-401f-bbc1-7c93d6498c2e" PropertyName="ItemIndex" PropertyType="Integer" />
  <t:FieldURIOrConstant>
    <t:Constant Value="3" />
  </t:FieldURIOrConstant>
</t:IsLessThanOrEqualTo>
```

### <a name="negating-filter"></a><span data-ttu-id="4b0a3-209">Filtro de negación</span><span class="sxs-lookup"><span data-stu-id="4b0a3-209">Negating filter</span></span>

<span data-ttu-id="4b0a3-210">Un filtro negating permite negar otro filtro y obtener los resultados de búsqueda opuesto.</span><span class="sxs-lookup"><span data-stu-id="4b0a3-210">A negating filter enables you to negate another filter and get the opposite search results.</span></span> <span data-ttu-id="4b0a3-211">Mientras que otros filtros devuelven resultados que coincidan con criterios específicos, un filtro negating devuelve resultados que no coinciden con los criterios especificados por el filtro se aplica a.</span><span class="sxs-lookup"><span data-stu-id="4b0a3-211">While other filters return results that match specific criteria, a negating filter returns results that do not match the criteria specified by the filter it is applied to.</span></span>
  
#### <a name="negating-filter-in-the-ews-managed-api"></a><span data-ttu-id="4b0a3-212">Negación filtro en la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="4b0a3-212">Negating filter in the EWS Managed API</span></span>

<span data-ttu-id="4b0a3-213">En el ejemplo siguiente se muestra cómo usar la API administrada de EWS para crear un filtro de búsqueda para devolver todos los elementos que no tienen la subcadena "notas de la reunión" en el asunto.</span><span class="sxs-lookup"><span data-stu-id="4b0a3-213">The following example shows you how to use the EWS Managed API to create a search filter to return all items that do not have the substring "meeting notes" in the subject.</span></span>
  
```cs
SearchFilter.ContainsSubstring subjectFilter = new SearchFilter.ContainsSubstring(ItemSchema.Subject,
    "meeting notes", ContainmentMode.Substring, ComparisonMode.IgnoreCase);
SearchFilter.Not subjectNotFilter =
    new SearchFilter.Not(subjectFilter);
```

#### <a name="negating-filter-in-ews"></a><span data-ttu-id="4b0a3-214">Filtro de negación de EWS</span><span class="sxs-lookup"><span data-stu-id="4b0a3-214">Negating filter in EWS</span></span>

<span data-ttu-id="4b0a3-215">En el ejemplo siguiente se muestra cómo crear un filtro de búsqueda para devolver todos los elementos que no tienen la subcadena "notas de la reunión" en el asunto.</span><span class="sxs-lookup"><span data-stu-id="4b0a3-215">The following example shows you how to create a search filter to return all items that do not have the substring "meeting notes" in the subject.</span></span>
  
```XML
<t:Not>
  <t:Contains ContainmentMode="ExactPhrase" ContainmentComparison="IgnoreCase">
    <t:FieldURI FieldURI="item:Subject" />
    <t:Constant Value="meeting notes" />
  </t:Contains>
</t:Not>
```

### <a name="compound-filter"></a><span data-ttu-id="4b0a3-216">Filtro de compuestos</span><span class="sxs-lookup"><span data-stu-id="4b0a3-216">Compound filter</span></span>

<span data-ttu-id="4b0a3-217">Un filtro de compuestos permite combinar varios filtros para crear criterios de búsqueda más complejos.</span><span class="sxs-lookup"><span data-stu-id="4b0a3-217">A compound filter enables you to combine multiple filters to create more complex search criteria.</span></span> <span data-ttu-id="4b0a3-218">Puede combinar los criterios mediante el uso de los operadores lógicos y o OR.</span><span class="sxs-lookup"><span data-stu-id="4b0a3-218">You can combine criteria by using the logical operators AND or OR.</span></span> <span data-ttu-id="4b0a3-219">De este modo, puede realizar búsquedas al igual que "todo el correo de Sadie Daniels que contiene 'notas de la reunión' en el asunto".</span><span class="sxs-lookup"><span data-stu-id="4b0a3-219">In this way, you can perform searches like "all mail from Sadie Daniels that contains 'meeting notes' in the subject".</span></span>
  
#### <a name="compound-filter-in-the-ews-managed-api"></a><span data-ttu-id="4b0a3-220">Filtro de compuestos en la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="4b0a3-220">Compound filter in the EWS Managed API</span></span>

<span data-ttu-id="4b0a3-221">En el ejemplo siguiente se muestra cómo usar la API administrada de EWS para crear un filtro de búsqueda que devuelve todos los elementos que se envían desde Sadie Daniels y contienen "notas de la reunión" en el asunto.</span><span class="sxs-lookup"><span data-stu-id="4b0a3-221">The following example shows you how to use the EWS Managed API to create a search filter that returns all items that are sent from Sadie Daniels and contain "meeting notes" in the subject.</span></span>
  
```cs
SearchFilter.ContainsSubstring subjectFilter = new SearchFilter.ContainsSubstring(ItemSchema.Subject,
    "meeting notes", ContainmentMode.Substring, ComparisonMode.IgnoreCase);
EmailAddress manager = new EmailAddress("sadie@contoso.com");
SearchFilter.IsEqualTo fromManagerFilter =
    new SearchFilter.IsEqualTo(EmailMessageSchema.Sender, manager);
SearchFilter.SearchFilterCollection compoundFilter =
    new SearchFilter.SearchFilterCollection(LogicalOperator.And, subjectFilter, fromManagerFilter);
```

#### <a name="compound-filter-in-ews"></a><span data-ttu-id="4b0a3-222">Filtro de compuestos en EWS</span><span class="sxs-lookup"><span data-stu-id="4b0a3-222">Compound filter in EWS</span></span>

<span data-ttu-id="4b0a3-223">En el ejemplo siguiente se muestra cómo usar EWS para crear un filtro de búsqueda que devuelve todos los elementos que se envían desde Sadie Daniels y contienen "notas de la reunión" en el asunto.</span><span class="sxs-lookup"><span data-stu-id="4b0a3-223">The following example shows you how to use EWS to create a search filter that returns all items that are sent from Sadie Daniels and contain "meeting notes" in the subject.</span></span>
  
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

## <a name="example-find-items-by-using-a-search-filter-and-the-ews-managed-api"></a><span data-ttu-id="4b0a3-224">Ejemplo: Buscar elementos mediante el uso de un filtro de búsqueda y la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="4b0a3-224">Example: Find items by using a search filter and the EWS Managed API</span></span>
<span data-ttu-id="4b0a3-225"><a name="bk_ExampleEWSMA"> </a></span><span class="sxs-lookup"><span data-stu-id="4b0a3-225"></span></span>

<span data-ttu-id="4b0a3-226">Los siguientes métodos de la API administrada de EWS utilizar filtros de búsqueda:</span><span class="sxs-lookup"><span data-stu-id="4b0a3-226">The following EWS Managed API methods use search filters:</span></span>
  
- [<span data-ttu-id="4b0a3-227">ExchangeService.FindItems</span><span class="sxs-lookup"><span data-stu-id="4b0a3-227">ExchangeService.FindItems</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx)
- [<span data-ttu-id="4b0a3-228">ExchangeService.FindFolders</span><span class="sxs-lookup"><span data-stu-id="4b0a3-228">ExchangeService.FindFolders</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.findfolders%28v=exchg.80%29.aspx)
- [<span data-ttu-id="4b0a3-229">Folder.FindFolders</span><span class="sxs-lookup"><span data-stu-id="4b0a3-229">Folder.FindFolders</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.findfolders%28v=exchg.80%29.aspx)
- [<span data-ttu-id="4b0a3-230">Folder.FindItems</span><span class="sxs-lookup"><span data-stu-id="4b0a3-230">Folder.FindItems</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.finditems%28v=exchg.80%29.aspx)
    
<span data-ttu-id="4b0a3-231">En el ejemplo siguiente se utiliza el método **ExchangeService.FindItems** ; Sin embargo, las mismas reglas y los conceptos se aplican a todos los métodos.</span><span class="sxs-lookup"><span data-stu-id="4b0a3-231">The following example uses the **ExchangeService.FindItems** method; however, the same rules and concepts apply to all the methods.</span></span> <span data-ttu-id="4b0a3-232">En este ejemplo, se define un método denominado **SearchWithFilter** .</span><span class="sxs-lookup"><span data-stu-id="4b0a3-232">In this example, a method called **SearchWithFilter** is defined.</span></span> <span data-ttu-id="4b0a3-233">Toma un objetos [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) , [WellKnownFolderName](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.wellknownfoldername%28v=exchg.80%29.aspx) y [SearchFilter](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.searchfilter%28v=exchg.80%29.aspx) como parámetros.</span><span class="sxs-lookup"><span data-stu-id="4b0a3-233">It takes an [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object, a [WellKnownFolderName](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.wellknownfoldername%28v=exchg.80%29.aspx) object, and a [SearchFilter](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.searchfilter%28v=exchg.80%29.aspx) object as parameters.</span></span> <span data-ttu-id="4b0a3-234">En este ejemplo se da por supuesto que se ha inicializado el objeto **ExchangeService** con valores válidos en las propiedades de [las credenciales](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservicebase.credentials%28v=exchg.80%29.aspx) y [dirección Url](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.url%28v=exchg.80%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="4b0a3-234">This example assumes that the **ExchangeService** object has been initialized with valid values in the [Credentials](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservicebase.credentials%28v=exchg.80%29.aspx) and [Url](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.url%28v=exchg.80%29.aspx) properties.</span></span> <span data-ttu-id="4b0a3-235">La clase **SearchFilter** es la clase base para todos los filtros de búsqueda diferentes.</span><span class="sxs-lookup"><span data-stu-id="4b0a3-235">The **SearchFilter** class is the base class for all the different search filters.</span></span> 
  
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

<span data-ttu-id="4b0a3-236">Puede usar esta función con cualquiera de los filtros de búsqueda que se muestra en los ejemplos de este artículo.</span><span class="sxs-lookup"><span data-stu-id="4b0a3-236">You can use this function with any of the search filters shown in the examples in this article.</span></span> <span data-ttu-id="4b0a3-237">En este ejemplo se usa un filtro de compuestos para devolver todos los elementos de la Bandeja de entrada de Sadie Daniels con "notas de la reunión" en el asunto.</span><span class="sxs-lookup"><span data-stu-id="4b0a3-237">This example uses a compound filter to return all items in the Inbox from Sadie Daniels with "meeting notes" in the subject.</span></span>
  
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

## <a name="example-find-an-item-by-using-a-search-filter-and-ews"></a><span data-ttu-id="4b0a3-238">Ejemplo: Buscar un elemento mediante el uso de un filtro de búsqueda y EWS</span><span class="sxs-lookup"><span data-stu-id="4b0a3-238">Example: Find an item by using a search filter and EWS</span></span>
<span data-ttu-id="4b0a3-239"><a name="bk_ExampleEWS"> </a></span><span class="sxs-lookup"><span data-stu-id="4b0a3-239"></span></span>

<span data-ttu-id="4b0a3-240">Las siguientes operaciones de EWS usar filtros de búsqueda:</span><span class="sxs-lookup"><span data-stu-id="4b0a3-240">The following EWS operations use search filters:</span></span>
  
- [<span data-ttu-id="4b0a3-241">FindFolder</span><span class="sxs-lookup"><span data-stu-id="4b0a3-241">FindFolder</span></span>](http://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx)
- [<span data-ttu-id="4b0a3-242">FindItem</span><span class="sxs-lookup"><span data-stu-id="4b0a3-242">FindItem</span></span>](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)
    
<span data-ttu-id="4b0a3-243">En el ejemplo siguiente se utiliza la operación **FindItem** ; Sin embargo, las mismas reglas y los conceptos se aplican a ambas operaciones.</span><span class="sxs-lookup"><span data-stu-id="4b0a3-243">The following example uses the **FindItem** operation; however, the same rules and concepts apply to both operations.</span></span> <span data-ttu-id="4b0a3-244">Filtros de búsqueda se encuentran en el elemento de [restricción](http://msdn.microsoft.com/library/77f19014-d112-4999-8e83-ecc32a117a73%28Office.15%29.aspx) en las solicitudes SOAP.</span><span class="sxs-lookup"><span data-stu-id="4b0a3-244">Search filters are contained in the [Restriction](http://msdn.microsoft.com/library/77f19014-d112-4999-8e83-ecc32a117a73%28Office.15%29.aspx) element in SOAP requests.</span></span> <span data-ttu-id="4b0a3-245">En este ejemplo se envía una solicitud SOAP que es equivalente a la búsqueda que se muestra en el ejemplo anterior de la API administrada de EWS.</span><span class="sxs-lookup"><span data-stu-id="4b0a3-245">This example sends a SOAP request that is equivalent to the search that is shown in the preceding EWS Managed API example.</span></span> 
  
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

<span data-ttu-id="4b0a3-246">En el ejemplo siguiente se muestra la respuesta del servidor, incluidos los resultados de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="4b0a3-246">The following example shows the response from the server, including the search results.</span></span>
  
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

## <a name="next-steps"></a><span data-ttu-id="4b0a3-247">Siguientes pasos</span><span class="sxs-lookup"><span data-stu-id="4b0a3-247">Next steps</span></span>
<span data-ttu-id="4b0a3-248"><a name="bk_ExampleEWS"> </a></span><span class="sxs-lookup"><span data-stu-id="4b0a3-248"></span></span>

<span data-ttu-id="4b0a3-249">Ahora que está familiarizado con el uso de filtros de búsqueda en las búsquedas básicas, puede mover a técnicas más avanzadas de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="4b0a3-249">Now that you're familiar with using search filters in basic searches, you can move on to more advanced search techniques.</span></span>
  
- [<span data-ttu-id="4b0a3-250">Realizar búsquedas agrupadas mediante EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="4b0a3-250">Perform grouped searches by using EWS in Exchange</span></span>](how-to-perform-grouped-searches-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="4b0a3-251">Realizar búsquedas paginadas mediante EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="4b0a3-251">Perform paged searches by using EWS in Exchange</span></span>](how-to-perform-paged-searches-by-using-ews-in-exchange.md)
    
## <a name="see-also"></a><span data-ttu-id="4b0a3-252">Vea también</span><span class="sxs-lookup"><span data-stu-id="4b0a3-252">See also</span></span>

- [<span data-ttu-id="4b0a3-253">Búsqueda y EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="4b0a3-253">Search and EWS in Exchange</span></span>](search-and-ews-in-exchange.md)    
- [<span data-ttu-id="4b0a3-254">Realizar una búsqueda AQS mediante EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="4b0a3-254">Perform an AQS search by using EWS in Exchange</span></span>](how-to-perform-an-aqs-search-by-using-ews-in-exchange.md)   
- [<span data-ttu-id="4b0a3-255">ExchangeService.FindItems</span><span class="sxs-lookup"><span data-stu-id="4b0a3-255">ExchangeService.FindItems</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx)    
- [<span data-ttu-id="4b0a3-256">ExchangeService.FindFolders</span><span class="sxs-lookup"><span data-stu-id="4b0a3-256">ExchangeService.FindFolders</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.findfolders%28v=exchg.80%29.aspx)    
- [<span data-ttu-id="4b0a3-257">Folder.FindFolders</span><span class="sxs-lookup"><span data-stu-id="4b0a3-257">Folder.FindFolders</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.findfolders%28v=exchg.80%29.aspx)    
- [<span data-ttu-id="4b0a3-258">Folder.FindItems</span><span class="sxs-lookup"><span data-stu-id="4b0a3-258">Folder.FindItems</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.finditems%28v=exchg.80%29.aspx)    
- [<span data-ttu-id="4b0a3-259">Operación FindFolder</span><span class="sxs-lookup"><span data-stu-id="4b0a3-259">FindFolder operation</span></span>](http://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx)   
- [<span data-ttu-id="4b0a3-260">Operación FindItem</span><span class="sxs-lookup"><span data-stu-id="4b0a3-260">FindItem operation</span></span>](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)
    

