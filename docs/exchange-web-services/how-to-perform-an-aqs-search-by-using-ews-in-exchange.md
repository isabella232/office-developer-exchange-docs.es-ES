---
title: Realizar una búsqueda AQS con EWS en Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: c136901a-313e-4adf-a223-1d090d16917a
description: Descubra cómo buscar con cadenas de consulta y AQS en la API administrada de EWS o en la aplicación EWS.
localization_priority: Priority
ms.openlocfilehash: 9f611a8d90c6baf0f307897735c6366c82bb63c8
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44455719"
---
# <a name="perform-an-aqs-search-by-using-ews-in-exchange"></a><span data-ttu-id="d5413-103">Realizar una búsqueda AQS con EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="d5413-103">Perform an AQS search by using EWS in Exchange</span></span>

<span data-ttu-id="d5413-104">Descubra cómo buscar con cadenas de consulta y AQS en la API administrada de EWS o en la aplicación EWS.</span><span class="sxs-lookup"><span data-stu-id="d5413-104">Find out how to search with query strings and AQS in your EWS Managed API or EWS application.</span></span>
  
<span data-ttu-id="d5413-105">Las cadenas de consulta proporcionan una alternativa a los [filtros de búsqueda](how-to-use-search-filters-with-ews-in-exchange.md) para expresar criterios de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="d5413-105">Query strings provide an alternative to [search filters](how-to-use-search-filters-with-ews-in-exchange.md) for expressing search criteria.</span></span> <span data-ttu-id="d5413-106">La mayor ventaja de usar las cadenas de consulta es que no es necesario especificar una única propiedad para buscar.</span><span class="sxs-lookup"><span data-stu-id="d5413-106">The biggest advantage to using query strings is that you are not required to specify a single property to search.</span></span> <span data-ttu-id="d5413-107">Solo puede proporcionar un valor y la búsqueda se aplicará a todos los campos de los elementos que se usen con frecuencia.</span><span class="sxs-lookup"><span data-stu-id="d5413-107">You can just provide a value, and the search will apply to all commonly used fields on the items.</span></span> <span data-ttu-id="d5413-108">También puede refinar la búsqueda con la sintaxis de consulta avanzada (AQS) en lugar de un valor sencillo.</span><span class="sxs-lookup"><span data-stu-id="d5413-108">You can also refine your search by using Advanced Query Syntax (AQS) instead of a simple value.</span></span> <span data-ttu-id="d5413-109">Sin embargo, las cadenas de consulta tienen las siguientes limitaciones que debe tener en cuenta antes de agregarlas al cuadro de herramientas:</span><span class="sxs-lookup"><span data-stu-id="d5413-109">However, query strings have the following limitations that you should be aware of before you add them to your toolbox:</span></span> 
  
- <span data-ttu-id="d5413-110">**Capacidad limitada para buscar propiedades específicas.**</span><span class="sxs-lookup"><span data-stu-id="d5413-110">**Limited ability to search specific properties.**</span></span> <span data-ttu-id="d5413-111">Cuando se realiza una búsqueda con un valor simple en una cadena de consulta, la búsqueda se realiza en todas las propiedades indizadas.</span><span class="sxs-lookup"><span data-stu-id="d5413-111">When you search with a simple value in a query string, the search is performed against all indexed properties.</span></span> <span data-ttu-id="d5413-112">Puede restringir la búsqueda a propiedades específicas, pero las propiedades disponibles para usarlas en una cadena AQS son limitadas.</span><span class="sxs-lookup"><span data-stu-id="d5413-112">You can refine your search to specific properties, but the properties available to use in an AQS string are limited.</span></span> <span data-ttu-id="d5413-113">Si la propiedad que quieres buscar no es una de las propiedades que están disponibles para AQS, considera la posibilidad de usar un filtro de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="d5413-113">If the property you want to search isn't one of the properties that are available for AQS, consider using a search filter.</span></span> 
    
- <span data-ttu-id="d5413-114">**Las propiedades personalizadas no se buscan.**</span><span class="sxs-lookup"><span data-stu-id="d5413-114">**Custom properties aren't searched.**</span></span> <span data-ttu-id="d5413-115">Las búsquedas de cadenas de consulta se realizan en un índice, y las propiedades personalizadas no se incluyen en ese índice.</span><span class="sxs-lookup"><span data-stu-id="d5413-115">Query string searches are performed against an index, and custom properties are not included in that index.</span></span> <span data-ttu-id="d5413-116">Si necesita buscar propiedades personalizadas, use un filtro de búsqueda en su lugar.</span><span class="sxs-lookup"><span data-stu-id="d5413-116">If you need to search custom properties, use a search filter instead.</span></span> 
    
- <span data-ttu-id="d5413-117">**Control limitado para las búsquedas de cadena.**</span><span class="sxs-lookup"><span data-stu-id="d5413-117">**Limited control for string searches.**</span></span> <span data-ttu-id="d5413-118">Las búsquedas de cadenas de consulta siempre omiten mayúsculas y minúsculas y son siempre búsquedas de subcadenas.</span><span class="sxs-lookup"><span data-stu-id="d5413-118">Query string searches always ignore case, and are always substring searches.</span></span> <span data-ttu-id="d5413-119">Si desea realizar búsquedas con distinción de mayúsculas y minúsculas, prefijos o de coincidencia exacta, use un filtro de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="d5413-119">If you want to do case-sensitive, prefix, or exact match searches, use a search filter.</span></span> 
    
- <span data-ttu-id="d5413-120">**No disponible para carpetas o carpetas de búsqueda.**</span><span class="sxs-lookup"><span data-stu-id="d5413-120">**Not available for folders or search folders.**</span></span> <span data-ttu-id="d5413-121">Las operaciones de EWS para buscar carpetas no admiten el uso de una cadena de consulta.</span><span class="sxs-lookup"><span data-stu-id="d5413-121">The EWS operations for searching for folders don't support using a query string.</span></span> <span data-ttu-id="d5413-122">Además, las carpetas de búsqueda no admiten cadenas de consulta.</span><span class="sxs-lookup"><span data-stu-id="d5413-122">Additionally, search folders don't support query strings.</span></span> <span data-ttu-id="d5413-123">En ambos casos, un filtro de búsqueda es la única opción.</span><span class="sxs-lookup"><span data-stu-id="d5413-123">In both cases, a search filter is your only option.</span></span> 
    
## <a name="creating-a-query-string"></a><span data-ttu-id="d5413-124">Creación de una cadena de consulta</span><span class="sxs-lookup"><span data-stu-id="d5413-124">Creating a query string</span></span>
<span data-ttu-id="d5413-125"><a name="bk_CreateQueryString"> </a></span><span class="sxs-lookup"><span data-stu-id="d5413-125"><a name="bk_CreateQueryString"> </a></span></span>

<span data-ttu-id="d5413-126">Las cadenas de consulta en la API administrada de EWS y EWS se interpretan como un subconjunto de la sintaxis de AQS.</span><span class="sxs-lookup"><span data-stu-id="d5413-126">Query strings in the EWS Managed API and EWS are interpreted as a subset of AQS syntax.</span></span> <span data-ttu-id="d5413-127">Las cadenas AQS se componen de valores o pares de palabra clave y valor, separados por dos puntos (:).</span><span class="sxs-lookup"><span data-stu-id="d5413-127">AQS strings are composed of either values or keyword/value pairs, separated by a colon (:).</span></span>
  
`keyword:value`

<span data-ttu-id="d5413-128">Cuando se especifica un valor sin una palabra clave, se busca el valor en todas las propiedades indizadas.</span><span class="sxs-lookup"><span data-stu-id="d5413-128">When a value is specified without a keyword, all indexed properties are searched for the value.</span></span> <span data-ttu-id="d5413-129">Si una palabra clave está emparejada con un valor, la palabra clave especifica una propiedad para buscar el valor correspondiente.</span><span class="sxs-lookup"><span data-stu-id="d5413-129">If a keyword is paired with a value, the keyword specifies a property to search for the corresponding value.</span></span>
  
<span data-ttu-id="d5413-130">**Tabla 1. Palabras clave de AQS admitidas**</span><span class="sxs-lookup"><span data-stu-id="d5413-130">**Table 1. Supported AQS keywords**</span></span>

|<span data-ttu-id="d5413-131">**Palabra clave**</span><span class="sxs-lookup"><span data-stu-id="d5413-131">**Keyword**</span></span>|<span data-ttu-id="d5413-132">**Tipo de valor**</span><span class="sxs-lookup"><span data-stu-id="d5413-132">**Value type**</span></span>|<span data-ttu-id="d5413-133">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="d5413-133">**Example**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d5413-134">subject</span><span class="sxs-lookup"><span data-stu-id="d5413-134">subject</span></span>  <br/> |<span data-ttu-id="d5413-135">String</span><span class="sxs-lookup"><span data-stu-id="d5413-135">String</span></span>  <br/> |<span data-ttu-id="d5413-136">asunto: proyecto</span><span class="sxs-lookup"><span data-stu-id="d5413-136">subject:project</span></span>  <br/> |
|<span data-ttu-id="d5413-137">body</span><span class="sxs-lookup"><span data-stu-id="d5413-137">body</span></span>  <br/> |<span data-ttu-id="d5413-138">Cadena</span><span class="sxs-lookup"><span data-stu-id="d5413-138">String</span></span>  <br/> |<span data-ttu-id="d5413-139">cuerpo: cifras de ventas</span><span class="sxs-lookup"><span data-stu-id="d5413-139">body:sales figures</span></span>  <br/> |
|<span data-ttu-id="d5413-140">datos adjuntos</span><span class="sxs-lookup"><span data-stu-id="d5413-140">attachment</span></span>  <br/> |<span data-ttu-id="d5413-141">Cadena</span><span class="sxs-lookup"><span data-stu-id="d5413-141">String</span></span>  <br/> |<span data-ttu-id="d5413-142">datos adjuntos: informe</span><span class="sxs-lookup"><span data-stu-id="d5413-142">attachment:report</span></span>  <br/> |
|<span data-ttu-id="d5413-143">a</span><span class="sxs-lookup"><span data-stu-id="d5413-143">to</span></span>  <br/> |<span data-ttu-id="d5413-144">Cadena</span><span class="sxs-lookup"><span data-stu-id="d5413-144">String</span></span>  <br/> |<span data-ttu-id="d5413-145">para: "Sadie Daniels"</span><span class="sxs-lookup"><span data-stu-id="d5413-145">to:"Sadie Daniels"</span></span>  <br/> |
|<span data-ttu-id="d5413-146">from</span><span class="sxs-lookup"><span data-stu-id="d5413-146">from</span></span>  <br/> |<span data-ttu-id="d5413-147">Cadena</span><span class="sxs-lookup"><span data-stu-id="d5413-147">String</span></span>  <br/> |<span data-ttu-id="d5413-148">de: espero</span><span class="sxs-lookup"><span data-stu-id="d5413-148">from:hope</span></span>  <br/> |
|<span data-ttu-id="d5413-149">cc</span><span class="sxs-lookup"><span data-stu-id="d5413-149">cc</span></span>  <br/> |<span data-ttu-id="d5413-150">Cadena</span><span class="sxs-lookup"><span data-stu-id="d5413-150">String</span></span>  <br/> |<span data-ttu-id="d5413-151">CC: "Ronnie Sturgis"</span><span class="sxs-lookup"><span data-stu-id="d5413-151">cc:"Ronnie Sturgis"</span></span>  <br/> |
|<span data-ttu-id="d5413-152">cco</span><span class="sxs-lookup"><span data-stu-id="d5413-152">bcc</span></span>  <br/> |<span data-ttu-id="d5413-153">Cadena</span><span class="sxs-lookup"><span data-stu-id="d5413-153">String</span></span>  <br/> |<span data-ttu-id="d5413-154">CCO: Mack</span><span class="sxs-lookup"><span data-stu-id="d5413-154">bcc:mack</span></span>  <br/> |
|<span data-ttu-id="d5413-155">participants</span><span class="sxs-lookup"><span data-stu-id="d5413-155">participants</span></span>  <br/> |<span data-ttu-id="d5413-156">Cadena</span><span class="sxs-lookup"><span data-stu-id="d5413-156">String</span></span>  <br/> |<span data-ttu-id="d5413-157">participantes: Sadie</span><span class="sxs-lookup"><span data-stu-id="d5413-157">participants:sadie</span></span>  <br/> |
|<span data-ttu-id="d5413-158">categoría</span><span class="sxs-lookup"><span data-stu-id="d5413-158">category</span></span>  <br/> |<span data-ttu-id="d5413-159">Cadena</span><span class="sxs-lookup"><span data-stu-id="d5413-159">String</span></span>  <br/> |<span data-ttu-id="d5413-160">Categoría: proyecto</span><span class="sxs-lookup"><span data-stu-id="d5413-160">category:project</span></span>  <br/> |
|<span data-ttu-id="d5413-161">importance</span><span class="sxs-lookup"><span data-stu-id="d5413-161">importance</span></span>  <br/> |<span data-ttu-id="d5413-162">Cadena</span><span class="sxs-lookup"><span data-stu-id="d5413-162">String</span></span>  <br/> |<span data-ttu-id="d5413-163">importance:alta</span><span class="sxs-lookup"><span data-stu-id="d5413-163">importance:high</span></span>  <br/> |
|<span data-ttu-id="d5413-164">kind</span><span class="sxs-lookup"><span data-stu-id="d5413-164">kind</span></span>  <br/> |<span data-ttu-id="d5413-165">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="d5413-165">Item type</span></span>  <br/> |<span data-ttu-id="d5413-166">tipo: reuniones</span><span class="sxs-lookup"><span data-stu-id="d5413-166">kind:meetings</span></span>  <br/> |
|<span data-ttu-id="d5413-167">sent</span><span class="sxs-lookup"><span data-stu-id="d5413-167">sent</span></span>  <br/> |<span data-ttu-id="d5413-168">Fecha</span><span class="sxs-lookup"><span data-stu-id="d5413-168">Date</span></span>  <br/> |<span data-ttu-id="d5413-169">Enviado el: 12/10/2013</span><span class="sxs-lookup"><span data-stu-id="d5413-169">sent:12/10/2013</span></span>  <br/> |
|<span data-ttu-id="d5413-170">received</span><span class="sxs-lookup"><span data-stu-id="d5413-170">received</span></span>  <br/> |<span data-ttu-id="d5413-171">Fecha</span><span class="sxs-lookup"><span data-stu-id="d5413-171">Date</span></span>  <br/> |<span data-ttu-id="d5413-172">recibido: ayer</span><span class="sxs-lookup"><span data-stu-id="d5413-172">received:yesterday</span></span>  <br/> |
|<span data-ttu-id="d5413-173">hasattachment</span><span class="sxs-lookup"><span data-stu-id="d5413-173">hasattachment</span></span>  <br/> |<span data-ttu-id="d5413-174">Boolean</span><span class="sxs-lookup"><span data-stu-id="d5413-174">Boolean</span></span>  <br/> |<span data-ttu-id="d5413-175">Tiene datos adjuntos: true</span><span class="sxs-lookup"><span data-stu-id="d5413-175">Has attachment:true</span></span>  <br/> |
|<span data-ttu-id="d5413-176">isflagged</span><span class="sxs-lookup"><span data-stu-id="d5413-176">isflagged</span></span>  <br/> |<span data-ttu-id="d5413-177">Boolean</span><span class="sxs-lookup"><span data-stu-id="d5413-177">Boolean</span></span>  <br/> |<span data-ttu-id="d5413-178">isflagged: true</span><span class="sxs-lookup"><span data-stu-id="d5413-178">isflagged:true</span></span>  <br/> |
|<span data-ttu-id="d5413-179">isread</span><span class="sxs-lookup"><span data-stu-id="d5413-179">isread</span></span>  <br/> |<span data-ttu-id="d5413-180">Boolean</span><span class="sxs-lookup"><span data-stu-id="d5413-180">Boolean</span></span>  <br/> |<span data-ttu-id="d5413-181">isread: false</span><span class="sxs-lookup"><span data-stu-id="d5413-181">isread:false</span></span>  <br/> |
|<span data-ttu-id="d5413-182">size</span><span class="sxs-lookup"><span data-stu-id="d5413-182">size</span></span>  <br/> |<span data-ttu-id="d5413-183">Número</span><span class="sxs-lookup"><span data-stu-id="d5413-183">Number</span></span>  <br/> |<span data-ttu-id="d5413-184">tamaño: \> 5000</span><span class="sxs-lookup"><span data-stu-id="d5413-184">size:\>5000</span></span>  <br/> |
   
<span data-ttu-id="d5413-185">Echemos un vistazo a cómo funcionan los distintos tipos de valor.</span><span class="sxs-lookup"><span data-stu-id="d5413-185">Let's take a look at how the different value types work.</span></span>
  
### <a name="using-a-string-value-type"></a><span data-ttu-id="d5413-186">Uso de un tipo de valor de cadena</span><span class="sxs-lookup"><span data-stu-id="d5413-186">Using a string value type</span></span>

<span data-ttu-id="d5413-187">De forma predeterminada, los tipos de valor de cadena se buscan como búsquedas de subcadena de prefijo que no distinguen mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="d5413-187">String value types are by default searched as prefix substring searches that are not case-sensitive.</span></span> <span data-ttu-id="d5413-188">Eso significa que la búsqueda de asunto: Project coincidirá con cualquiera de los siguientes asuntos:</span><span class="sxs-lookup"><span data-stu-id="d5413-188">That means that searching for subject:project would match any of the following subjects:</span></span> 
  
- <span data-ttu-id="d5413-189">Notas de la reunión del proyecto</span><span class="sxs-lookup"><span data-stu-id="d5413-189">Project meeting notes</span></span>
    
- <span data-ttu-id="d5413-190">¿Tiene planes de proyecto?</span><span class="sxs-lookup"><span data-stu-id="d5413-190">Do you have the project plans?</span></span>
    
- <span data-ttu-id="d5413-191">Proyecciones de ventas de diciembre</span><span class="sxs-lookup"><span data-stu-id="d5413-191">December sales projections</span></span>
    
<span data-ttu-id="d5413-192">Puede cambiar la búsqueda para que requiera la palabra completa en lugar de que los prefijos coincidan encerrando la cadena entre comillas.</span><span class="sxs-lookup"><span data-stu-id="d5413-192">You can change the search to require the whole word rather than matching prefixes by enclosing the string in quotation marks.</span></span> <span data-ttu-id="d5413-193">Buscar asunto: "Project" eliminará el valor "proyecto de ventas de diciembre" de la lista de coincidencias.</span><span class="sxs-lookup"><span data-stu-id="d5413-193">Searching for subject:"project" would eliminate the "December sales projections" value from the list of matches.</span></span> <span data-ttu-id="d5413-194">Tenga en cuenta que el valor todavía no distingue mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="d5413-194">Note that the value is still not case-sensitive.</span></span> 
  
<span data-ttu-id="d5413-195">Si usa varias palabras en una cadena de consulta, una coincidencia requiere que ambas palabras aparezcan en los campos buscados.</span><span class="sxs-lookup"><span data-stu-id="d5413-195">If you use multiple words in a query string, a match requires that both words appear in the searched fields.</span></span> <span data-ttu-id="d5413-196">Por ejemplo, la búsqueda de asunto: el plan del proyecto coincidiría con cualquiera de los siguientes asuntos:</span><span class="sxs-lookup"><span data-stu-id="d5413-196">For example, searching for subject:project plan would match any of the following subjects:</span></span> 
  
- <span data-ttu-id="d5413-197">Plan del proyecto</span><span class="sxs-lookup"><span data-stu-id="d5413-197">Project plan</span></span>
    
- <span data-ttu-id="d5413-198">¿Tiene planes de proyecto?</span><span class="sxs-lookup"><span data-stu-id="d5413-198">Do you have the project plans?</span></span>
    
- <span data-ttu-id="d5413-199">Envíeme el plan de nuestro proyecto.</span><span class="sxs-lookup"><span data-stu-id="d5413-199">Please send me the plan for our project</span></span>
    
- <span data-ttu-id="d5413-200">Planeación de hitos de proyecto</span><span class="sxs-lookup"><span data-stu-id="d5413-200">Planning project milestones</span></span>
    
<span data-ttu-id="d5413-201">Si escribe varias palabras entre comillas, se tratarán como una sola frase.</span><span class="sxs-lookup"><span data-stu-id="d5413-201">If you enclose multiple words in quotation marks, they are treated as a single phrase.</span></span> <span data-ttu-id="d5413-202">La búsqueda del asunto: "plan del proyecto" solo coincidirá con el asunto "plan del proyecto" de la lista anterior.</span><span class="sxs-lookup"><span data-stu-id="d5413-202">Searching for subject:"project plan" would only match the "Project plan" subject from the previous list.</span></span> 
  
### <a name="using-an-item-type-value-type"></a><span data-ttu-id="d5413-203">Usar un tipo de valor de tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="d5413-203">Using an item type value type</span></span>

<span data-ttu-id="d5413-204">Puede usar los siguientes valores de tipo de elemento con la palabra clave **Kind** para limitar los resultados de la búsqueda a un tipo específico de elemento, como correo electrónico o convocatorias de reunión:</span><span class="sxs-lookup"><span data-stu-id="d5413-204">You can use the following item type values with the **kind** keyword to limit your search results to only a specific type of item, such as email or meeting requests:</span></span> 
  
- <span data-ttu-id="d5413-205">contactos</span><span class="sxs-lookup"><span data-stu-id="d5413-205">contacts</span></span>    
- <span data-ttu-id="d5413-206">documentos</span><span class="sxs-lookup"><span data-stu-id="d5413-206">docs</span></span>    
- <span data-ttu-id="d5413-207">correo electrónico</span><span class="sxs-lookup"><span data-stu-id="d5413-207">email</span></span>    
- <span data-ttu-id="d5413-208">faxes</span><span class="sxs-lookup"><span data-stu-id="d5413-208">faxes</span></span>    
- <span data-ttu-id="d5413-209">mi (corresponde a mensajes instantáneos)</span><span class="sxs-lookup"><span data-stu-id="d5413-209">im (corresponds to instant messages)</span></span>    
- <span data-ttu-id="d5413-210">diarios</span><span class="sxs-lookup"><span data-stu-id="d5413-210">journals</span></span>    
- <span data-ttu-id="d5413-211">reuniones (corresponde a citas y convocatorias de reunión)</span><span class="sxs-lookup"><span data-stu-id="d5413-211">meetings (corresponds to appointments and meeting requests)</span></span>    
- <span data-ttu-id="d5413-212">notas</span><span class="sxs-lookup"><span data-stu-id="d5413-212">notes</span></span>    
- <span data-ttu-id="d5413-213">entradas</span><span class="sxs-lookup"><span data-stu-id="d5413-213">posts</span></span>    
- <span data-ttu-id="d5413-214">fuentes rss</span><span class="sxs-lookup"><span data-stu-id="d5413-214">rssfeeds</span></span>    
- <span data-ttu-id="d5413-215">tareas</span><span class="sxs-lookup"><span data-stu-id="d5413-215">tasks</span></span>    
- <span data-ttu-id="d5413-216">correo de voz</span><span class="sxs-lookup"><span data-stu-id="d5413-216">voicemail</span></span>
    
### <a name="using-a-date-value-type"></a><span data-ttu-id="d5413-217">Uso de un tipo de valor de fecha</span><span class="sxs-lookup"><span data-stu-id="d5413-217">Using a date value type</span></span>

<span data-ttu-id="d5413-218">Los tipos de valores de fecha se pueden buscar de varias formas.</span><span class="sxs-lookup"><span data-stu-id="d5413-218">You can search date value types in a number of different ways.</span></span> <span data-ttu-id="d5413-219">La más sencilla es buscar una fecha específica.</span><span class="sxs-lookup"><span data-stu-id="d5413-219">The simplest is to search for a specific date.</span></span> <span data-ttu-id="d5413-220">La búsqueda con Received: 12/11/2013 devolverá todos los elementos recibidos el 11 de diciembre de 2013.</span><span class="sxs-lookup"><span data-stu-id="d5413-220">Searching with received:12/11/2013 will return all items received on December 11, 2013.</span></span> <span data-ttu-id="d5413-221">Sin embargo, también puede ser menos específico.</span><span class="sxs-lookup"><span data-stu-id="d5413-221">However, you can also be less specific.</span></span> <span data-ttu-id="d5413-222">La búsqueda con Received: 12/11 devolverá todos los elementos que se hayan recibido el 11 de diciembre del año actual.</span><span class="sxs-lookup"><span data-stu-id="d5413-222">Searching with received:12/11 will return all items received on December 11 of the current year.</span></span> 
  
<span data-ttu-id="d5413-223">Otra opción es usar los nombres de los meses.</span><span class="sxs-lookup"><span data-stu-id="d5413-223">Another option is to use the month names.</span></span> <span data-ttu-id="d5413-224">Puede buscar con Received: 11 de diciembre de 2013 o 11 de diciembre para obtener los mismos resultados que los recibidos: 12/11/2013 y recibidos: 12/11, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="d5413-224">You can search with received:December 11, 2013 or December 11 to get the same results as received:12/11/2013 and received:12/11, respectively.</span></span> <span data-ttu-id="d5413-225">También puede buscar con Received: December para obtener todos los elementos recibidos en el mes de diciembre en el año actual.</span><span class="sxs-lookup"><span data-stu-id="d5413-225">You can also search with received:December to get all items received in the month of December, in the current year.</span></span> 
  
<span data-ttu-id="d5413-226">El uso de los nombres de los días de la semana también es una opción.</span><span class="sxs-lookup"><span data-stu-id="d5413-226">Using the names of the days of the week is also an option.</span></span> <span data-ttu-id="d5413-227">La búsqueda con Received: Tuesday devolverá todos los elementos que se reciben el martes de la semana actual.</span><span class="sxs-lookup"><span data-stu-id="d5413-227">Searching with received:Tuesday will return all items received on Tuesday of the current week.</span></span> 
  
<span data-ttu-id="d5413-228">Los tipos de valores de fecha también admiten un conjunto de palabras clave para las búsquedas relativas a la hora actual.</span><span class="sxs-lookup"><span data-stu-id="d5413-228">Date value types also support a set of keywords for searches relative to the current time.</span></span> <span data-ttu-id="d5413-229">Se admiten las siguientes palabras clave:</span><span class="sxs-lookup"><span data-stu-id="d5413-229">The following keywords are supported:</span></span>
  
- <span data-ttu-id="d5413-230">hoy</span><span class="sxs-lookup"><span data-stu-id="d5413-230">today</span></span>  
- <span data-ttu-id="d5413-231">tomorrow</span><span class="sxs-lookup"><span data-stu-id="d5413-231">tomorrow</span></span>
- <span data-ttu-id="d5413-232">yesterday</span><span class="sxs-lookup"><span data-stu-id="d5413-232">yesterday</span></span>
- <span data-ttu-id="d5413-233">this week</span><span class="sxs-lookup"><span data-stu-id="d5413-233">this week</span></span>    
- <span data-ttu-id="d5413-234">La semana pasada</span><span class="sxs-lookup"><span data-stu-id="d5413-234">last week</span></span>    
- <span data-ttu-id="d5413-235">próximo mes</span><span class="sxs-lookup"><span data-stu-id="d5413-235">next month</span></span>    
- <span data-ttu-id="d5413-236">último mes</span><span class="sxs-lookup"><span data-stu-id="d5413-236">past month</span></span>    
- <span data-ttu-id="d5413-237">año próximo</span><span class="sxs-lookup"><span data-stu-id="d5413-237">coming year</span></span>
    
<span data-ttu-id="d5413-238">Los tipos de valores de fecha también se pueden comparar con operadores relacionales como mayor o menor que, o especificarse como un rango con el operador de rango **..**. Por ejemplo, Received: \> 11/30/2013, Sent: \> = ayer y Received: 12/1/2013.. hoy son cadenas de consulta válidas.</span><span class="sxs-lookup"><span data-stu-id="d5413-238">Date value types can also be compared with relational operators like greater than or less than, or specified as a range with the range operator **..**. For example, received:\>11/30/2013, sent:\>=yesterday, and received:12/1/2013..today are all valid query strings.</span></span> 
  
### <a name="using-a-boolean-value-type"></a><span data-ttu-id="d5413-239">Uso de un tipo de valor booleano</span><span class="sxs-lookup"><span data-stu-id="d5413-239">Using a Boolean value type</span></span>

<span data-ttu-id="d5413-240">Los tipos de valores booleanos pueden ser "true" o "false".</span><span class="sxs-lookup"><span data-stu-id="d5413-240">Boolean value types can be "true" or "false".</span></span> <span data-ttu-id="d5413-241">Los valores no distinguen entre mayúsculas y minúsculas, por lo que isread: false generarán los mismos resultados que isread: FALSE.</span><span class="sxs-lookup"><span data-stu-id="d5413-241">The values are not case-sensitive, so isread:false will produce the same results as isread:FALSE.</span></span>
  
### <a name="using-a-number-value-type"></a><span data-ttu-id="d5413-242">Uso de un tipo de valor de número</span><span class="sxs-lookup"><span data-stu-id="d5413-242">Using a number value type</span></span>

<span data-ttu-id="d5413-243">Los tipos de valores de número se pueden buscar como coincidencias exactas, pero también se pueden buscar mediante operadores relacionales como mayor o menor que.</span><span class="sxs-lookup"><span data-stu-id="d5413-243">Number value types can be searched as exact matches, but they can also be searched using relational operators like greater than or less than.</span></span> <span data-ttu-id="d5413-244">Por ejemplo, size: 10000 devolverá solo los elementos que tengan un tamaño exacto de 10000 bytes, pero Size: \> = 10000 devolverá los elementos que tengan un tamaño mayor o igual que 10000 bytes.</span><span class="sxs-lookup"><span data-stu-id="d5413-244">For example, size:10000 will return only items that have a size of exactly 10000 bytes, but size:\>=10000 will return items that have a size greater than or equal to 10000 bytes.</span></span> <span data-ttu-id="d5413-245">También puede especificar un intervalo mediante el operador de intervalo ( **..**).</span><span class="sxs-lookup"><span data-stu-id="d5413-245">You can also specify a range by using the range operator ( **..**).</span></span> <span data-ttu-id="d5413-246">Por ejemplo, size: 7000.. 8000 devolverá los elementos que tengan un tamaño entre 7000 y 8000.</span><span class="sxs-lookup"><span data-stu-id="d5413-246">For example, size:7000..8000 will return items that have a size between 7000 and 8000.</span></span> 
  
### <a name="using-logical-operators"></a><span data-ttu-id="d5413-247">Uso de operadores lógicos</span><span class="sxs-lookup"><span data-stu-id="d5413-247">Using logical operators</span></span>

<span data-ttu-id="d5413-248">Las cadenas de consulta admiten los siguientes operadores lógicos.</span><span class="sxs-lookup"><span data-stu-id="d5413-248">Query strings support the following logical operators.</span></span>
  
<span data-ttu-id="d5413-249">**Tabla 2. Operadores lógicos admitidos**</span><span class="sxs-lookup"><span data-stu-id="d5413-249">**Table 2. Supported logical operators**</span></span>

|<span data-ttu-id="d5413-250">**Operator**</span><span class="sxs-lookup"><span data-stu-id="d5413-250">**Operator**</span></span>|<span data-ttu-id="d5413-251">**Ejemplos**</span><span class="sxs-lookup"><span data-stu-id="d5413-251">**Examples**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d5413-252">Y</span><span class="sxs-lookup"><span data-stu-id="d5413-252">AND</span></span>  <br/> |<span data-ttu-id="d5413-253">Project y de: "Sadie Daniels"</span><span class="sxs-lookup"><span data-stu-id="d5413-253">project AND from:"Sadie Daniels"</span></span>  <br/> <span data-ttu-id="d5413-254">asunto: (proyecto y plan)</span><span class="sxs-lookup"><span data-stu-id="d5413-254">subject:(project AND plan)</span></span>  <br/> |
|<span data-ttu-id="d5413-255">O</span><span class="sxs-lookup"><span data-stu-id="d5413-255">OR</span></span>  <br/> |<span data-ttu-id="d5413-256">asunto: reunión o de: "Esperamos bruta"</span><span class="sxs-lookup"><span data-stu-id="d5413-256">subject:meeting OR from:"Hope Gross"</span></span>  <br/> <span data-ttu-id="d5413-257">From:("Sadie Daniels" o "esperanza bruto")</span><span class="sxs-lookup"><span data-stu-id="d5413-257">from:("Sadie Daniels" OR "Hope Gross")</span></span>  <br/> |
|<span data-ttu-id="d5413-258">NO</span><span class="sxs-lookup"><span data-stu-id="d5413-258">NOT</span></span>  <br/> |<span data-ttu-id="d5413-259">NO de: "Ronnie Sturgis"</span><span class="sxs-lookup"><span data-stu-id="d5413-259">NOT from:"Ronnie Sturgis"</span></span>  <br/> <span data-ttu-id="d5413-260">recibido: no hoy</span><span class="sxs-lookup"><span data-stu-id="d5413-260">received:NOT today</span></span>  <br/> |
   
<span data-ttu-id="d5413-261">Tenga en cuenta que puede usar estos operadores para unir varios criterios de forma conjunta o para combinar varios valores en un solo par de palabra clave y valor.</span><span class="sxs-lookup"><span data-stu-id="d5413-261">Notice that you can use these operators to join multiple criteria together or to join multiple values within a single keyword/value pair together.</span></span> <span data-ttu-id="d5413-262">Sin embargo, al combinar varios valores en un par de palabra clave y valor único, debe usar paréntesis para incluir los varios valores.</span><span class="sxs-lookup"><span data-stu-id="d5413-262">However, when joining multiple values in a single keyword/value pair, you should use parentheses to enclose the multiple values.</span></span> <span data-ttu-id="d5413-263">Para comprender por qué, considere la posibilidad de buscar con from: "Sadie Daniels" o "esperanza bruta".</span><span class="sxs-lookup"><span data-stu-id="d5413-263">To understand why, consider searching with from:"Sadie Daniels" OR "Hope Gross".</span></span> <span data-ttu-id="d5413-264">En realidad, esta búsqueda se interpreta como los siguientes criterios:</span><span class="sxs-lookup"><span data-stu-id="d5413-264">This search actually is interpreted as the following criteria:</span></span>
  
- <span data-ttu-id="d5413-265">El elemento es de Sadie Daniels o</span><span class="sxs-lookup"><span data-stu-id="d5413-265">The item is from Sadie Daniels, OR</span></span>
    
- <span data-ttu-id="d5413-266">El elemento tiene la frase "Esperamos bruta" en cualquiera de sus propiedades indizadas.</span><span class="sxs-lookup"><span data-stu-id="d5413-266">The item has the phrase "Hope Gross" in any of its indexed properties.</span></span>
    
<span data-ttu-id="d5413-267">Por el contrario, del:("Sadie Daniels" o "esperanza bruto") se interpreta como:</span><span class="sxs-lookup"><span data-stu-id="d5413-267">In contrast, from:("Sadie Daniels" OR "Hope Gross") is interpreted as:</span></span> 
  
- <span data-ttu-id="d5413-268">El elemento es de Sadie Daniels o</span><span class="sxs-lookup"><span data-stu-id="d5413-268">The item is from Sadie Daniels, OR</span></span>
    
- <span data-ttu-id="d5413-269">El elemento es de esperanza bruta</span><span class="sxs-lookup"><span data-stu-id="d5413-269">The item is from Hope Gross</span></span>
    
<span data-ttu-id="d5413-270">El operador predeterminado cuando se especifican varios criterios, pero no se incluye ningún operador lógico y.</span><span class="sxs-lookup"><span data-stu-id="d5413-270">The default operator when multiple criteria are specified but no logical operator is included is AND.</span></span> <span data-ttu-id="d5413-271">Por ejemplo, tiene datos adjuntos: verdadero asunto: Project equivale a: Attachment: true y Subject: Project.</span><span class="sxs-lookup"><span data-stu-id="d5413-271">For example, has attachment:true subject:project is equivalent to has:attachment:true AND subject:project.</span></span>
  
## <a name="example-find-items-by-using-a-query-string-and-the-ews-managed-api"></a><span data-ttu-id="d5413-272">Ejemplo: buscar elementos mediante una cadena de consulta y la API administrada EWS</span><span class="sxs-lookup"><span data-stu-id="d5413-272">Example: Find items by using a query string and the EWS Managed API</span></span>
<span data-ttu-id="d5413-273"><a name="bk_ExampleEWSMA"> </a></span><span class="sxs-lookup"><span data-stu-id="d5413-273"><a name="bk_ExampleEWSMA"> </a></span></span>

<span data-ttu-id="d5413-274">En este ejemplo, se define un método denominado **SearchWithQueryString** .</span><span class="sxs-lookup"><span data-stu-id="d5413-274">In this example, a method called **SearchWithQueryString** is defined.</span></span> <span data-ttu-id="d5413-275">Toma un objeto [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) , un objeto [WellKnownFolderName](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.wellknownfoldername%28v=exchg.80%29.aspx) y un objeto **String** que representa la cadena de consulta como parámetros.</span><span class="sxs-lookup"><span data-stu-id="d5413-275">It takes an [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object, a [WellKnownFolderName](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.wellknownfoldername%28v=exchg.80%29.aspx) object, and a **string** object that represents the query string as parameters.</span></span> <span data-ttu-id="d5413-276">En este ejemplo se supone que el objeto **ExchangeService** se ha inicializado con valores válidos en las propiedades [Credentials](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.credentials%28v=exchg.80%29.aspx) y [URL](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.url%28v=exchg.80%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="d5413-276">This example assumes that the **ExchangeService** object has been initialized with valid values in the [Credentials](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.credentials%28v=exchg.80%29.aspx) and [Url](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.url%28v=exchg.80%29.aspx) properties.</span></span> 
  
```cs
using Microsoft.Exchange.WebServices.Data;
static void SearchWithQueryString(ExchangeService service, WellKnownFolderName folder, string queryString)
{
    // Limit the result set to 10 items.
    ItemView view = new ItemView(10);
    view.PropertySet = new PropertySet(ItemSchema.Subject,
                                       ItemSchema.DateTimeReceived,
                                       ItemSchema.Size,
                                       ItemSchema.Importance,
                                       EmailMessageSchema.IsRead);
    // Item searches do not support Deep traversal.
    view.Traversal = ItemTraversal.Shallow;
    // Sorting
    view.OrderBy.Add(ItemSchema.DateTimeReceived, SortDirection.Descending);
    try
    {
        // Execute the search based on the query string.
        // Example: "subject:project plan"
        FindItemsResults<Item> results = service.FindItems(folder, queryString, view);
        foreach (Item item in results.Items)
        {
            Console.WriteLine("Subject: {0}", item.Subject);
            Console.WriteLine("Received: {0}", item.DateTimeReceived.ToString());
            Console.WriteLine("Size: {0}", item.Size.ToString());
            Console.WriteLine("Importance: {0}", item.Importance.ToString());
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

<span data-ttu-id="d5413-277">Puede usar este método para buscar todos los elementos que contengan la frase "plan de proyecto" en el asunto, tal como se muestra en este ejemplo.</span><span class="sxs-lookup"><span data-stu-id="d5413-277">You can use this method to search for all items with the phrase "project plan" in the subject, as shown in this example.</span></span>
  
```cs
string queryString = "subject:\"project plan\"";
SearchWithQueryString(service, WellKnownFolderName.Inbox, queryString);
```

## <a name="example-find-items-by-using-a-query-string-and-ews"></a><span data-ttu-id="d5413-278">Ejemplo: buscar elementos mediante una cadena de consulta y EWS</span><span class="sxs-lookup"><span data-stu-id="d5413-278">Example: Find items by using a query string and EWS</span></span>
<span data-ttu-id="d5413-279"><a name="bk_ExampleEWS"> </a></span><span class="sxs-lookup"><span data-stu-id="d5413-279"><a name="bk_ExampleEWS"> </a></span></span>

<span data-ttu-id="d5413-280">En este ejemplo, una solicitud [FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) de SOAP busca todos los elementos de la bandeja de entrada con la frase "plan del proyecto" en el asunto.</span><span class="sxs-lookup"><span data-stu-id="d5413-280">In this example, a SOAP [FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) request finds all items in the Inbox with the phrase "project plan" in the subject.</span></span> 
  
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
          <t:FieldURI FieldURI="item:Size" />
          <t:FieldURI FieldURI="item:Importance" />
          <t:FieldURI FieldURI="message:IsRead" />
        </t:AdditionalProperties>
      </m:ItemShape>
      <m:IndexedPageItemView MaxEntriesReturned="10" Offset="0" BasePoint="Beginning" />
      <m:SortOrder>
        <t:FieldOrder Order="Descending">
          <t:FieldURI FieldURI="item:DateTimeReceived" />
        </t:FieldOrder>
      </m:SortOrder>
      <m:ParentFolderIds>
        <t:DistinguishedFolderId Id="inbox" />
      </m:ParentFolderIds>
      <m:QueryString>subject:"project plan"</m:QueryString>
    </m:FindItem>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="d5413-281">En el ejemplo siguiente se muestra la respuesta del servidor con los resultados de la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="d5413-281">The following example shows the response from the server with the search results.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="712" MinorBuildNumber="22" Version="V2_3" 
        xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
        xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:FindItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:FindItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:RootFolder IndexedPagingOffset="1" TotalItemsInView="1" IncludesLastItemInRange="true">
            <t:Items>
              <t:Message>
                <t:ItemId Id="AAMkAGM2..." ChangeKey="CQAAABYA..." />
                <t:Subject>project plan</t:Subject>
                <t:DateTimeReceived>2013-12-11T15:42:02Z</t:DateTimeReceived>
                <t:Size>7406</t:Size>
                <t:Importance>Normal</t:Importance>
                <t:IsRead>false</t:IsRead>
              </t:Message>
            </t:Items>
          </m:RootFolder>
        </m:FindItemResponseMessage>
      </m:ResponseMessages>
    </m:FindItemResponse>
  </s:Body>
</s:Envelope>
```

## <a name="see-also"></a><span data-ttu-id="d5413-282">Vea también</span><span class="sxs-lookup"><span data-stu-id="d5413-282">See also</span></span>

- [<span data-ttu-id="d5413-283">Búsqueda y EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="d5413-283">Search and EWS in Exchange</span></span>](search-and-ews-in-exchange.md)    
- [<span data-ttu-id="d5413-284">Usar filtros de búsqueda con EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="d5413-284">Use search filters with EWS in Exchange</span></span>](how-to-use-search-filters-with-ews-in-exchange.md)    
- [<span data-ttu-id="d5413-285">ExchangeService. FindItems</span><span class="sxs-lookup"><span data-stu-id="d5413-285">ExchangeService.FindItems</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx)    
- [<span data-ttu-id="d5413-286">Operación FindItem</span><span class="sxs-lookup"><span data-stu-id="d5413-286">FindItem operation</span></span>](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)
    

