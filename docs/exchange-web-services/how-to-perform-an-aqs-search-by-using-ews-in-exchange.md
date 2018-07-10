---
title: Realizar una búsqueda AQS mediante EWS en Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: c136901a-313e-4adf-a223-1d090d16917a
description: Averigüe cómo buscar con cadenas de consulta y AQS en la API administrada de EWS o aplicación de EWS.
ms.openlocfilehash: dc859e24fa80cd5627477182979c9cc9527818d6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763171"
---
# <a name="perform-an-aqs-search-by-using-ews-in-exchange"></a><span data-ttu-id="239a4-103">Realizar una búsqueda AQS mediante EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="239a4-103">Perform an AQS search by using EWS in Exchange</span></span>

<span data-ttu-id="239a4-104">Averigüe cómo buscar con cadenas de consulta y AQS en la API administrada de EWS o aplicación de EWS.</span><span class="sxs-lookup"><span data-stu-id="239a4-104">Find out how to search with query strings and AQS in your EWS Managed API or EWS application.</span></span>
  
<span data-ttu-id="239a4-105">Cadenas de consulta proporcionan una alternativa a los [filtros de búsqueda](how-to-use-search-filters-with-ews-in-exchange.md) para expresar los criterios de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="239a4-105">Query strings provide an alternative to [search filters](how-to-use-search-filters-with-ews-in-exchange.md) for expressing search criteria.</span></span> <span data-ttu-id="239a4-106">La mayor ventaja de usar cadenas de consulta es que no es necesario especificar una sola propiedad para buscar.</span><span class="sxs-lookup"><span data-stu-id="239a4-106">The biggest advantage to using query strings is that you are not required to specify a single property to search.</span></span> <span data-ttu-id="239a4-107">Sólo puede proporcionar un valor, y la búsqueda se aplicará a todos los campos usados con más frecuencia en los elementos.</span><span class="sxs-lookup"><span data-stu-id="239a4-107">You can just provide a value, and the search will apply to all commonly used fields on the items.</span></span> <span data-ttu-id="239a4-108">También puede restringir la búsqueda mediante el uso de sintaxis de consulta avanzada (AQS) en lugar de un valor simple.</span><span class="sxs-lookup"><span data-stu-id="239a4-108">You can also refine your search by using Advanced Query Syntax (AQS) instead of a simple value.</span></span> <span data-ttu-id="239a4-109">Sin embargo, las cadenas de consulta tienen las siguientes limitaciones que deben tenerse en cuenta antes de agregar al cuadro de herramientas:</span><span class="sxs-lookup"><span data-stu-id="239a4-109">However, query strings have the following limitations that you should be aware of before you add them to your toolbox:</span></span> 
  
- <span data-ttu-id="239a4-110">**Capacidad limitada para buscar propiedades específicas.**</span><span class="sxs-lookup"><span data-stu-id="239a4-110">**Limited ability to search specific properties.**</span></span> <span data-ttu-id="239a4-111">Al buscar con un valor simple en una cadena de consulta, la búsqueda se realiza en todas las propiedades indizadas.</span><span class="sxs-lookup"><span data-stu-id="239a4-111">When you search with a simple value in a query string, the search is performed against all indexed properties.</span></span> <span data-ttu-id="239a4-112">Puede restringir la búsqueda a propiedades específicas, pero las propiedades disponibles para su uso en una cadena AQS están limitadas.</span><span class="sxs-lookup"><span data-stu-id="239a4-112">You can refine your search to specific properties, but the properties available to use in an AQS string are limited.</span></span> <span data-ttu-id="239a4-113">Si la propiedad que desea buscar no es una de las propiedades que están disponibles para AQS, considere el uso de un filtro de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="239a4-113">If the property you want to search isn't one of the properties that are available for AQS, consider using a search filter.</span></span> 
    
- <span data-ttu-id="239a4-114">**No se buscan en las propiedades personalizadas.**</span><span class="sxs-lookup"><span data-stu-id="239a4-114">**Custom properties aren't searched.**</span></span> <span data-ttu-id="239a4-115">Las búsquedas de cadena de consulta se llevan a cabo con un índice, y las propiedades personalizadas no se incluyen en ese índice.</span><span class="sxs-lookup"><span data-stu-id="239a4-115">Query string searches are performed against an index, and custom properties are not included in that index.</span></span> <span data-ttu-id="239a4-116">Si necesita las propiedades personalizadas de búsqueda, utilice en su lugar un filtro de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="239a4-116">If you need to search custom properties, use a search filter instead.</span></span> 
    
- <span data-ttu-id="239a4-117">**Busca un control limitado de cadena.**</span><span class="sxs-lookup"><span data-stu-id="239a4-117">**Limited control for string searches.**</span></span> <span data-ttu-id="239a4-118">Búsquedas de cadenas de consulta siempre entre mayúsculas y minúsculas y siempre son búsquedas de subcadenas.</span><span class="sxs-lookup"><span data-stu-id="239a4-118">Query string searches always ignore case, and are always substring searches.</span></span> <span data-ttu-id="239a4-119">Si desea hacer entre mayúsculas y minúsculas, prefijo o las búsquedas de coincidencia exacta, utilice un filtro de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="239a4-119">If you want to do case-sensitive, prefix, or exact match searches, use a search filter.</span></span> 
    
- <span data-ttu-id="239a4-120">**No está disponible para las carpetas o las carpetas de búsqueda.**</span><span class="sxs-lookup"><span data-stu-id="239a4-120">**Not available for folders or search folders.**</span></span> <span data-ttu-id="239a4-121">Las operaciones de EWS para la búsqueda de las carpetas no admiten el uso de una cadena de consulta.</span><span class="sxs-lookup"><span data-stu-id="239a4-121">The EWS operations for searching for folders don't support using a query string.</span></span> <span data-ttu-id="239a4-122">Además, las carpetas de búsqueda no admiten cadenas de consulta.</span><span class="sxs-lookup"><span data-stu-id="239a4-122">Additionally, search folders don't support query strings.</span></span> <span data-ttu-id="239a4-123">En ambos casos, un filtro de búsqueda es la única opción.</span><span class="sxs-lookup"><span data-stu-id="239a4-123">In both cases, a search filter is your only option.</span></span> 
    
## <a name="creating-a-query-string"></a><span data-ttu-id="239a4-124">Creación de una cadena de consulta</span><span class="sxs-lookup"><span data-stu-id="239a4-124">Creating a query string</span></span>
<span data-ttu-id="239a4-125"><a name="bk_CreateQueryString"> </a></span><span class="sxs-lookup"><span data-stu-id="239a4-125"></span></span>

<span data-ttu-id="239a4-126">Cadenas de consulta en la API administrada de EWS y EWS se interpretan como un subconjunto de la sintaxis AQS.</span><span class="sxs-lookup"><span data-stu-id="239a4-126">Query strings in the EWS Managed API and EWS are interpreted as a subset of AQS syntax.</span></span> <span data-ttu-id="239a4-127">Cadenas AQS se componen de los valores o los pares de palabra clave y valor, separados por un carácter de dos puntos (:).</span><span class="sxs-lookup"><span data-stu-id="239a4-127">AQS strings are composed of either values or keyword/value pairs, separated by a colon (:).</span></span>
  
`keyword:value`

<span data-ttu-id="239a4-128">Cuando se especifica un valor sin una palabra clave, se buscan todas las propiedades indizadas para el valor.</span><span class="sxs-lookup"><span data-stu-id="239a4-128">When a value is specified without a keyword, all indexed properties are searched for the value.</span></span> <span data-ttu-id="239a4-129">Si una palabra clave se corresponde con un valor, la palabra clave especifica una propiedad para buscar el valor correspondiente.</span><span class="sxs-lookup"><span data-stu-id="239a4-129">If a keyword is paired with a value, the keyword specifies a property to search for the corresponding value.</span></span>
  
<span data-ttu-id="239a4-130">**La tabla 1. Palabras clave AQS compatibles**</span><span class="sxs-lookup"><span data-stu-id="239a4-130">**Table 1. Supported AQS keywords**</span></span>

|<span data-ttu-id="239a4-131">**Palabra clave**</span><span class="sxs-lookup"><span data-stu-id="239a4-131">**Keyword**</span></span>|<span data-ttu-id="239a4-132">**Tipo de valor**</span><span class="sxs-lookup"><span data-stu-id="239a4-132">**Value type**</span></span>|<span data-ttu-id="239a4-133">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="239a4-133">**Example**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="239a4-134">subject</span><span class="sxs-lookup"><span data-stu-id="239a4-134">subject</span></span>  <br/> |<span data-ttu-id="239a4-135">Cadena</span><span class="sxs-lookup"><span data-stu-id="239a4-135">String</span></span>  <br/> |<span data-ttu-id="239a4-136">Asunto: proyecto</span><span class="sxs-lookup"><span data-stu-id="239a4-136">subject:project</span></span>  <br/> |
|<span data-ttu-id="239a4-137">cuerpo</span><span class="sxs-lookup"><span data-stu-id="239a4-137">body</span></span>  <br/> |<span data-ttu-id="239a4-138">Cadena</span><span class="sxs-lookup"><span data-stu-id="239a4-138">String</span></span>  <br/> |<span data-ttu-id="239a4-139">cifras de ventas de cuerpo:</span><span class="sxs-lookup"><span data-stu-id="239a4-139">body:sales figures</span></span>  <br/> |
|<span data-ttu-id="239a4-140">datos adjuntos</span><span class="sxs-lookup"><span data-stu-id="239a4-140">attachment</span></span>  <br/> |<span data-ttu-id="239a4-141">Cadena</span><span class="sxs-lookup"><span data-stu-id="239a4-141">String</span></span>  <br/> |<span data-ttu-id="239a4-142">datos adjuntos: informe</span><span class="sxs-lookup"><span data-stu-id="239a4-142">attachment:report</span></span>  <br/> |
|<span data-ttu-id="239a4-143">a</span><span class="sxs-lookup"><span data-stu-id="239a4-143">to</span></span>  <br/> |<span data-ttu-id="239a4-144">Cadena</span><span class="sxs-lookup"><span data-stu-id="239a4-144">String</span></span>  <br/> |<span data-ttu-id="239a4-145">para: "Sadie Daniels"</span><span class="sxs-lookup"><span data-stu-id="239a4-145">to:"Sadie Daniels"</span></span>  <br/> |
|<span data-ttu-id="239a4-146">from</span><span class="sxs-lookup"><span data-stu-id="239a4-146">from</span></span>  <br/> |<span data-ttu-id="239a4-147">Cadena</span><span class="sxs-lookup"><span data-stu-id="239a4-147">String</span></span>  <br/> |<span data-ttu-id="239a4-148">desde: Esperamos</span><span class="sxs-lookup"><span data-stu-id="239a4-148">from:hope</span></span>  <br/> |
|<span data-ttu-id="239a4-149">cc</span><span class="sxs-lookup"><span data-stu-id="239a4-149">cc</span></span>  <br/> |<span data-ttu-id="239a4-150">Cadena</span><span class="sxs-lookup"><span data-stu-id="239a4-150">String</span></span>  <br/> |<span data-ttu-id="239a4-151">cc: "Ronnie Sturgis"</span><span class="sxs-lookup"><span data-stu-id="239a4-151">cc:"Ronnie Sturgis"</span></span>  <br/> |
|<span data-ttu-id="239a4-152">bcc</span><span class="sxs-lookup"><span data-stu-id="239a4-152">bcc</span></span>  <br/> |<span data-ttu-id="239a4-153">Cadena</span><span class="sxs-lookup"><span data-stu-id="239a4-153">String</span></span>  <br/> |<span data-ttu-id="239a4-154">BCC:Mack</span><span class="sxs-lookup"><span data-stu-id="239a4-154">bcc:mack</span></span>  <br/> |
|<span data-ttu-id="239a4-155">participants</span><span class="sxs-lookup"><span data-stu-id="239a4-155">participants</span></span>  <br/> |<span data-ttu-id="239a4-156">Cadena</span><span class="sxs-lookup"><span data-stu-id="239a4-156">String</span></span>  <br/> |<span data-ttu-id="239a4-157">los participantes: sadie</span><span class="sxs-lookup"><span data-stu-id="239a4-157">participants:sadie</span></span>  <br/> |
|<span data-ttu-id="239a4-158">.</span><span class="sxs-lookup"><span data-stu-id="239a4-158">category</span></span>  <br/> |<span data-ttu-id="239a4-159">String</span><span class="sxs-lookup"><span data-stu-id="239a4-159">String</span></span>  <br/> |<span data-ttu-id="239a4-160">categoría: proyecto</span><span class="sxs-lookup"><span data-stu-id="239a4-160">category:project</span></span>  <br/> |
|<span data-ttu-id="239a4-161">importance</span><span class="sxs-lookup"><span data-stu-id="239a4-161">importance</span></span>  <br/> |<span data-ttu-id="239a4-162">Cadena</span><span class="sxs-lookup"><span data-stu-id="239a4-162">String</span></span>  <br/> |<span data-ttu-id="239a4-163">importancia: alta</span><span class="sxs-lookup"><span data-stu-id="239a4-163">importance:high</span></span>  <br/> |
|<span data-ttu-id="239a4-164">tipo</span><span class="sxs-lookup"><span data-stu-id="239a4-164">kind</span></span>  <br/> |<span data-ttu-id="239a4-165">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="239a4-165">Item type</span></span>  <br/> |<span data-ttu-id="239a4-166">tipo: reuniones</span><span class="sxs-lookup"><span data-stu-id="239a4-166">kind:meetings</span></span>  <br/> |
|<span data-ttu-id="239a4-167">enviado</span><span class="sxs-lookup"><span data-stu-id="239a4-167">sent</span></span>  <br/> |<span data-ttu-id="239a4-168">Fecha</span><span class="sxs-lookup"><span data-stu-id="239a4-168">Date</span></span>  <br/> |<span data-ttu-id="239a4-169">enviado: 10/12/2013</span><span class="sxs-lookup"><span data-stu-id="239a4-169">sent:12/10/2013</span></span>  <br/> |
|<span data-ttu-id="239a4-170">recibido</span><span class="sxs-lookup"><span data-stu-id="239a4-170">received</span></span>  <br/> |<span data-ttu-id="239a4-171">Fecha</span><span class="sxs-lookup"><span data-stu-id="239a4-171">Date</span></span>  <br/> |<span data-ttu-id="239a4-172">recibido: ayer</span><span class="sxs-lookup"><span data-stu-id="239a4-172">received:yesterday</span></span>  <br/> |
|<span data-ttu-id="239a4-173">HasAttachment</span><span class="sxs-lookup"><span data-stu-id="239a4-173">hasattachment</span></span>  <br/> |<span data-ttu-id="239a4-174">Boolean</span><span class="sxs-lookup"><span data-stu-id="239a4-174">Boolean</span></span>  <br/> |<span data-ttu-id="239a4-175">Tiene datos adjuntos: true</span><span class="sxs-lookup"><span data-stu-id="239a4-175">Has attachment:true</span></span>  <br/> |
|<span data-ttu-id="239a4-176">estámarcado</span><span class="sxs-lookup"><span data-stu-id="239a4-176">isflagged</span></span>  <br/> |<span data-ttu-id="239a4-177">Boolean</span><span class="sxs-lookup"><span data-stu-id="239a4-177">Boolean</span></span>  <br/> |<span data-ttu-id="239a4-178">isflagged:true</span><span class="sxs-lookup"><span data-stu-id="239a4-178">isflagged:true</span></span>  <br/> |
|<span data-ttu-id="239a4-179">estáleído</span><span class="sxs-lookup"><span data-stu-id="239a4-179">isread</span></span>  <br/> |<span data-ttu-id="239a4-180">Boolean</span><span class="sxs-lookup"><span data-stu-id="239a4-180">Boolean</span></span>  <br/> |<span data-ttu-id="239a4-181">isread:False</span><span class="sxs-lookup"><span data-stu-id="239a4-181">isread:false</span></span>  <br/> |
|<span data-ttu-id="239a4-182">size</span><span class="sxs-lookup"><span data-stu-id="239a4-182">size</span></span>  <br/> |<span data-ttu-id="239a4-183">Número</span><span class="sxs-lookup"><span data-stu-id="239a4-183">Number</span></span>  <br/> |<span data-ttu-id="239a4-184">tamaño:\>5000</span><span class="sxs-lookup"><span data-stu-id="239a4-184">size:\>5000</span></span>  <br/> |
   
<span data-ttu-id="239a4-185">Vamos a echar un vistazo a cómo funcionan los tipos de valores diferentes.</span><span class="sxs-lookup"><span data-stu-id="239a4-185">Let's take a look at how the different value types work.</span></span>
  
### <a name="using-a-string-value-type"></a><span data-ttu-id="239a4-186">Uso de un tipo de valor de cadena</span><span class="sxs-lookup"><span data-stu-id="239a4-186">Using a string value type</span></span>

<span data-ttu-id="239a4-187">Tipos de valor de cadena son buscado como búsquedas de subcadenas de prefijo que no distinguen mayúsculas de minúsculas de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="239a4-187">String value types are by default searched as prefix substring searches that are not case-sensitive.</span></span> <span data-ttu-id="239a4-188">Eso significa que busca asunto: proyecto coincidirá con cualquiera de los siguientes temas:</span><span class="sxs-lookup"><span data-stu-id="239a4-188">That means that searching for subject:project would match any of the following subjects:</span></span> 
  
- <span data-ttu-id="239a4-189">Notas de las reuniones de proyecto</span><span class="sxs-lookup"><span data-stu-id="239a4-189">Project meeting notes</span></span>
    
- <span data-ttu-id="239a4-190">¿Tiene los planes del proyecto?</span><span class="sxs-lookup"><span data-stu-id="239a4-190">Do you have the project plans?</span></span>
    
- <span data-ttu-id="239a4-191">Previsiones de ventas de diciembre</span><span class="sxs-lookup"><span data-stu-id="239a4-191">December sales projections</span></span>
    
<span data-ttu-id="239a4-192">Puede cambiar la búsqueda para exigir la palabra completa en lugar de coincidencia de prefijos por encerrar la cadena entre comillas.</span><span class="sxs-lookup"><span data-stu-id="239a4-192">You can change the search to require the whole word rather than matching prefixes by enclosing the string in quotation marks.</span></span> <span data-ttu-id="239a4-193">Buscar asunto: "proyecto" eliminaría el valor "Diciembre las previsiones de ventas" de la lista de coincidencias.</span><span class="sxs-lookup"><span data-stu-id="239a4-193">Searching for subject:"project" would eliminate the "December sales projections" value from the list of matches.</span></span> <span data-ttu-id="239a4-194">Tenga en cuenta que el valor sea aún no distingue mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="239a4-194">Note that the value is still not case-sensitive.</span></span> 
  
<span data-ttu-id="239a4-195">Si usa varias palabras en una cadena de consulta, se requiere una coincidencia que ambas palabras aparecen en los campos de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="239a4-195">If you use multiple words in a query string, a match requires that both words appear in the searched fields.</span></span> <span data-ttu-id="239a4-196">Por ejemplo, busca el plan del proyecto: asunto coincidirá con cualquiera de los siguientes temas:</span><span class="sxs-lookup"><span data-stu-id="239a4-196">For example, searching for subject:project plan would match any of the following subjects:</span></span> 
  
- <span data-ttu-id="239a4-197">Plan del proyecto</span><span class="sxs-lookup"><span data-stu-id="239a4-197">Project plan</span></span>
    
- <span data-ttu-id="239a4-198">¿Tiene los planes del proyecto?</span><span class="sxs-lookup"><span data-stu-id="239a4-198">Do you have the project plans?</span></span>
    
- <span data-ttu-id="239a4-199">Envíeme el plan para nuestro proyecto</span><span class="sxs-lookup"><span data-stu-id="239a4-199">Please send me the plan for our project</span></span>
    
- <span data-ttu-id="239a4-200">Planeación de los hitos del proyecto</span><span class="sxs-lookup"><span data-stu-id="239a4-200">Planning project milestones</span></span>
    
<span data-ttu-id="239a4-201">Si escriba varias palabras entre comillas, se tratan como una sola frase.</span><span class="sxs-lookup"><span data-stu-id="239a4-201">If you enclose multiple words in quotation marks, they are treated as a single phrase.</span></span> <span data-ttu-id="239a4-202">Buscar asunto: "plan del proyecto" sólo coincidirá con el asunto "Plan del proyecto" de la lista anterior.</span><span class="sxs-lookup"><span data-stu-id="239a4-202">Searching for subject:"project plan" would only match the "Project plan" subject from the previous list.</span></span> 
  
### <a name="using-an-item-type-value-type"></a><span data-ttu-id="239a4-203">Uso de un tipo de valor de tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="239a4-203">Using an item type value type</span></span>

<span data-ttu-id="239a4-204">Puede usar los siguientes valores de tipo de elemento con la palabra clave de **tipo** para limitar los resultados de búsqueda a solo un tipo específico de elemento, como correo electrónico o las convocatorias de reunión:</span><span class="sxs-lookup"><span data-stu-id="239a4-204">You can use the following item type values with the **kind** keyword to limit your search results to only a specific type of item, such as email or meeting requests:</span></span> 
  
- <span data-ttu-id="239a4-205">contactos</span><span class="sxs-lookup"><span data-stu-id="239a4-205">contacts</span></span>    
- <span data-ttu-id="239a4-206">documentos</span><span class="sxs-lookup"><span data-stu-id="239a4-206">docs</span></span>    
- <span data-ttu-id="239a4-207">email</span><span class="sxs-lookup"><span data-stu-id="239a4-207">email</span></span>    
- <span data-ttu-id="239a4-208">faxes</span><span class="sxs-lookup"><span data-stu-id="239a4-208">faxes</span></span>    
- <span data-ttu-id="239a4-209">mensajería instantánea (corresponde a los mensajes instantáneos)</span><span class="sxs-lookup"><span data-stu-id="239a4-209">im (corresponds to instant messages)</span></span>    
- <span data-ttu-id="239a4-210">diarios</span><span class="sxs-lookup"><span data-stu-id="239a4-210">journals</span></span>    
- <span data-ttu-id="239a4-211">las reuniones (corresponde a las citas y convocatorias de reunión)</span><span class="sxs-lookup"><span data-stu-id="239a4-211">meetings (corresponds to appointments and meeting requests)</span></span>    
- <span data-ttu-id="239a4-212">notas</span><span class="sxs-lookup"><span data-stu-id="239a4-212">notes</span></span>    
- <span data-ttu-id="239a4-213">posts</span><span class="sxs-lookup"><span data-stu-id="239a4-213">posts</span></span>    
- <span data-ttu-id="239a4-214">rssfeeds</span><span class="sxs-lookup"><span data-stu-id="239a4-214">rssfeeds</span></span>    
- <span data-ttu-id="239a4-215">tasks</span><span class="sxs-lookup"><span data-stu-id="239a4-215">tasks</span></span>    
- <span data-ttu-id="239a4-216">correo de voz</span><span class="sxs-lookup"><span data-stu-id="239a4-216">voicemail</span></span>
    
### <a name="using-a-date-value-type"></a><span data-ttu-id="239a4-217">Uso de un tipo de valor de fecha</span><span class="sxs-lookup"><span data-stu-id="239a4-217">Using a date value type</span></span>

<span data-ttu-id="239a4-218">Puede buscar los tipos de valor de fecha en un número de formas diferentes.</span><span class="sxs-lookup"><span data-stu-id="239a4-218">You can search date value types in a number of different ways.</span></span> <span data-ttu-id="239a4-219">Es el más simple buscar una fecha específica.</span><span class="sxs-lookup"><span data-stu-id="239a4-219">The simplest is to search for a specific date.</span></span> <span data-ttu-id="239a4-220">Buscar con recibido: 11/12/2013 devolverá todos los elementos recibidos en el 11 de diciembre de 2013.</span><span class="sxs-lookup"><span data-stu-id="239a4-220">Searching with received:12/11/2013 will return all items received on December 11, 2013.</span></span> <span data-ttu-id="239a4-221">Sin embargo, también puede ser menos específico.</span><span class="sxs-lookup"><span data-stu-id="239a4-221">However, you can also be less specific.</span></span> <span data-ttu-id="239a4-222">Buscar con recibido: 12/11 devolverá todos los elementos que se recibe en el 11 de diciembre del año actual.</span><span class="sxs-lookup"><span data-stu-id="239a4-222">Searching with received:12/11 will return all items received on December 11 of the current year.</span></span> 
  
<span data-ttu-id="239a4-223">Otra opción consiste en usar los nombres de mes.</span><span class="sxs-lookup"><span data-stu-id="239a4-223">Another option is to use the month names.</span></span> <span data-ttu-id="239a4-224">Puede buscar con recibido: 11 de diciembre de 2013 o el 11 de diciembre para obtener los mismos resultados recibidos: 11/12/2013 y recibido: 12/11, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="239a4-224">You can search with received:December 11, 2013 or December 11 to get the same results as received:12/11/2013 and received:12/11, respectively.</span></span> <span data-ttu-id="239a4-225">También puede buscar con recibido: diciembre para obtener todos los elementos recibidos en el mes de diciembre, en el año actual.</span><span class="sxs-lookup"><span data-stu-id="239a4-225">You can also search with received:December to get all items received in the month of December, in the current year.</span></span> 
  
<span data-ttu-id="239a4-226">También es una opción con los nombres de los días de la semana.</span><span class="sxs-lookup"><span data-stu-id="239a4-226">Using the names of the days of the week is also an option.</span></span> <span data-ttu-id="239a4-227">Buscar con recibido: el martes devolverá todos los elementos recibidos el martes de la semana actual.</span><span class="sxs-lookup"><span data-stu-id="239a4-227">Searching with received:Tuesday will return all items received on Tuesday of the current week.</span></span> 
  
<span data-ttu-id="239a4-228">Tipos de valor de fecha también admiten un conjunto de palabras clave para las búsquedas con respecto a la hora actual.</span><span class="sxs-lookup"><span data-stu-id="239a4-228">Date value types also support a set of keywords for searches relative to the current time.</span></span> <span data-ttu-id="239a4-229">Se admiten las siguientes palabras clave:</span><span class="sxs-lookup"><span data-stu-id="239a4-229">The following keywords are supported:</span></span>
  
- <span data-ttu-id="239a4-230">hoy</span><span class="sxs-lookup"><span data-stu-id="239a4-230">today</span></span>  
- <span data-ttu-id="239a4-231">tomorrow</span><span class="sxs-lookup"><span data-stu-id="239a4-231">tomorrow</span></span>
- <span data-ttu-id="239a4-232">yesterday</span><span class="sxs-lookup"><span data-stu-id="239a4-232">yesterday</span></span>
- <span data-ttu-id="239a4-233">this week</span><span class="sxs-lookup"><span data-stu-id="239a4-233">this week</span></span>    
- <span data-ttu-id="239a4-234">La semana pasada</span><span class="sxs-lookup"><span data-stu-id="239a4-234">last week</span></span>    
- <span data-ttu-id="239a4-235">próximo mes</span><span class="sxs-lookup"><span data-stu-id="239a4-235">next month</span></span>    
- <span data-ttu-id="239a4-236">mes pasado</span><span class="sxs-lookup"><span data-stu-id="239a4-236">past month</span></span>    
- <span data-ttu-id="239a4-237">año siguiente</span><span class="sxs-lookup"><span data-stu-id="239a4-237">coming year</span></span>
    
<span data-ttu-id="239a4-238">Tipos de valor de fecha también se pueden comparar con operadores relacionales como mayor o menor que, o se ha especificado como un rango con el operador de intervalo **.**. Por ejemplo, recibido:\>30/11/2013, envía:\>= ayer, y received:12/1/2013..today son todas las cadenas de consulta válida.</span><span class="sxs-lookup"><span data-stu-id="239a4-238">Date value types can also be compared with relational operators like greater than or less than, or specified as a range with the range operator **..**. For example, received:\>11/30/2013, sent:\>=yesterday, and received:12/1/2013..today are all valid query strings.</span></span> 
  
### <a name="using-a-boolean-value-type"></a><span data-ttu-id="239a4-239">Uso de un tipo de valor booleano</span><span class="sxs-lookup"><span data-stu-id="239a4-239">Using a Boolean value type</span></span>

<span data-ttu-id="239a4-240">Tipos de valor de tipo Boolean pueden ser "true" o "false".</span><span class="sxs-lookup"><span data-stu-id="239a4-240">Boolean value types can be "true" or "false".</span></span> <span data-ttu-id="239a4-241">Los valores no distinguen mayúsculas de minúsculas, por lo que isread:false generarán los mismos resultados que isread:FALSE.</span><span class="sxs-lookup"><span data-stu-id="239a4-241">The values are not case-sensitive, so isread:false will produce the same results as isread:FALSE.</span></span>
  
### <a name="using-a-number-value-type"></a><span data-ttu-id="239a4-242">Uso de un tipo de valor numérico</span><span class="sxs-lookup"><span data-stu-id="239a4-242">Using a number value type</span></span>

<span data-ttu-id="239a4-243">Se pueden buscar en los tipos de valor numéricos como coincidencias exactas, pero también se pueden buscar con operadores relacionales como mayor o menor que.</span><span class="sxs-lookup"><span data-stu-id="239a4-243">Number value types can be searched as exact matches, but they can also be searched using relational operators like greater than or less than.</span></span> <span data-ttu-id="239a4-244">Por ejemplo, tamaño: 10000 devolverá sólo los elementos que tienen un tamaño de exactamente 10000 bytes, pero tamaño:\>= 10000 devolverá los elementos que tienen un tamaño mayor o igual a 10000 bytes.</span><span class="sxs-lookup"><span data-stu-id="239a4-244">For example, size:10000 will return only items that have a size of exactly 10000 bytes, but size:\>=10000 will return items that have a size greater than or equal to 10000 bytes.</span></span> <span data-ttu-id="239a4-245">También puede especificar un intervalo mediante el operador de rango ( **.**).</span><span class="sxs-lookup"><span data-stu-id="239a4-245">You can also specify a range by using the range operator ( **..**).</span></span> <span data-ttu-id="239a4-246">Por ejemplo, tamaño: 7000..8000 devolverá los elementos que tienen un tamaño de entre 7000 y 8000.</span><span class="sxs-lookup"><span data-stu-id="239a4-246">For example, size:7000..8000 will return items that have a size between 7000 and 8000.</span></span> 
  
### <a name="using-logical-operators"></a><span data-ttu-id="239a4-247">Usar operadores lógicos</span><span class="sxs-lookup"><span data-stu-id="239a4-247">Using logical operators</span></span>

<span data-ttu-id="239a4-248">Cadenas de consulta admiten los siguientes operadores lógicos.</span><span class="sxs-lookup"><span data-stu-id="239a4-248">Query strings support the following logical operators.</span></span>
  
<span data-ttu-id="239a4-249">**Tabla 2. Operadores lógicos compatibles**</span><span class="sxs-lookup"><span data-stu-id="239a4-249">**Table 2. Supported logical operators**</span></span>

|<span data-ttu-id="239a4-250">**Operador**</span><span class="sxs-lookup"><span data-stu-id="239a4-250">**Operator**</span></span>|<span data-ttu-id="239a4-251">**Ejemplos**</span><span class="sxs-lookup"><span data-stu-id="239a4-251">**Examples**</span></span>|
|:-----|:-----|
|<span data-ttu-id="239a4-252">AND</span><span class="sxs-lookup"><span data-stu-id="239a4-252">AND</span></span>  <br/> |<span data-ttu-id="239a4-253">proyecto y desde: "Sadie Daniels"</span><span class="sxs-lookup"><span data-stu-id="239a4-253">project AND from:"Sadie Daniels"</span></span>  <br/> <span data-ttu-id="239a4-254">Asunto:(project AND plan)</span><span class="sxs-lookup"><span data-stu-id="239a4-254">subject:(project AND plan)</span></span>  <br/> |
|<span data-ttu-id="239a4-255">O</span><span class="sxs-lookup"><span data-stu-id="239a4-255">OR</span></span>  <br/> |<span data-ttu-id="239a4-256">Asunto: reunión o desde: "Espero bruto"</span><span class="sxs-lookup"><span data-stu-id="239a4-256">subject:meeting OR from:"Hope Gross"</span></span>  <br/> <span data-ttu-id="239a4-257">desde: ("Sadie Daniels" o "Espero bruto")</span><span class="sxs-lookup"><span data-stu-id="239a4-257">from:("Sadie Daniels" OR "Hope Gross")</span></span>  <br/> |
|<span data-ttu-id="239a4-258">NOT</span><span class="sxs-lookup"><span data-stu-id="239a4-258">NOT</span></span>  <br/> |<span data-ttu-id="239a4-259">NO desde: "Ronnie Sturgis"</span><span class="sxs-lookup"><span data-stu-id="239a4-259">NOT from:"Ronnie Sturgis"</span></span>  <br/> <span data-ttu-id="239a4-260">recibido: no hoy mismo</span><span class="sxs-lookup"><span data-stu-id="239a4-260">received:NOT today</span></span>  <br/> |
   
<span data-ttu-id="239a4-261">Tenga en cuenta que puede utilizar estos operadores para unir varios criterios o para unir varios valores dentro de un par de palabra clave y valor único.</span><span class="sxs-lookup"><span data-stu-id="239a4-261">Notice that you can use these operators to join multiple criteria together or to join multiple values within a single keyword/value pair together.</span></span> <span data-ttu-id="239a4-262">Sin embargo, al unirse a varios valores en un par de palabra clave y valor único, debe usar paréntesis para delimitar los valores de varios.</span><span class="sxs-lookup"><span data-stu-id="239a4-262">However, when joining multiple values in a single keyword/value pair, you should use parentheses to enclose the multiple values.</span></span> <span data-ttu-id="239a4-263">Para comprender por qué, considere la posibilidad de búsqueda con desde: "Sadie Daniels" o "Espero bruto".</span><span class="sxs-lookup"><span data-stu-id="239a4-263">To understand why, consider searching with from:"Sadie Daniels" OR "Hope Gross".</span></span> <span data-ttu-id="239a4-264">Esta búsqueda realmente se interpreta como los siguientes criterios:</span><span class="sxs-lookup"><span data-stu-id="239a4-264">This search actually is interpreted as the following criteria:</span></span>
  
- <span data-ttu-id="239a4-265">El elemento es de Sadie Daniels, OR</span><span class="sxs-lookup"><span data-stu-id="239a4-265">The item is from Sadie Daniels, OR</span></span>
    
- <span data-ttu-id="239a4-266">El elemento tiene la frase "Espero bruto" en cualquiera de sus propiedades indizadas.</span><span class="sxs-lookup"><span data-stu-id="239a4-266">The item has the phrase "Hope Gross" in any of its indexed properties.</span></span>
    
<span data-ttu-id="239a4-267">Por el contrario, desde: ("Sadie Daniels" o "Espero bruto") se interpreta como:</span><span class="sxs-lookup"><span data-stu-id="239a4-267">In contrast, from:("Sadie Daniels" OR "Hope Gross") is interpreted as:</span></span> 
  
- <span data-ttu-id="239a4-268">El elemento es de Sadie Daniels, OR</span><span class="sxs-lookup"><span data-stu-id="239a4-268">The item is from Sadie Daniels, OR</span></span>
    
- <span data-ttu-id="239a4-269">El elemento es de espero bruto</span><span class="sxs-lookup"><span data-stu-id="239a4-269">The item is from Hope Gross</span></span>
    
<span data-ttu-id="239a4-270">Es el operador de forma predeterminada cuando se especifican varios criterios, pero no se incluye ningún operador lógico AND.</span><span class="sxs-lookup"><span data-stu-id="239a4-270">The default operator when multiple criteria are specified but no logical operator is included is AND.</span></span> <span data-ttu-id="239a4-271">Por ejemplo, tiene datos adjuntos: true asunto: proyecto es equivalente a tiene: true: los datos adjuntos y asunto: project.</span><span class="sxs-lookup"><span data-stu-id="239a4-271">For example, has attachment:true subject:project is equivalent to has:attachment:true AND subject:project.</span></span>
  
## <a name="example-find-items-by-using-a-query-string-and-the-ews-managed-api"></a><span data-ttu-id="239a4-272">Ejemplo: Buscar elementos mediante el uso de una cadena de consulta y la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="239a4-272">Example: Find items by using a query string and the EWS Managed API</span></span>
<span data-ttu-id="239a4-273"><a name="bk_ExampleEWSMA"> </a></span><span class="sxs-lookup"><span data-stu-id="239a4-273"></span></span>

<span data-ttu-id="239a4-274">En este ejemplo, se define un método denominado **SearchWithQueryString** .</span><span class="sxs-lookup"><span data-stu-id="239a4-274">In this example, a method called **SearchWithQueryString** is defined.</span></span> <span data-ttu-id="239a4-275">Toma un objeto [ExchangeService](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) , un objeto [WellKnownFolderName](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.wellknownfoldername%28v=exchg.80%29.aspx) y un objeto **string** que representa la cadena de consulta como parámetros.</span><span class="sxs-lookup"><span data-stu-id="239a4-275">It takes an [ExchangeService](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object, a [WellKnownFolderName](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.wellknownfoldername%28v=exchg.80%29.aspx) object, and a **string** object that represents the query string as parameters.</span></span> <span data-ttu-id="239a4-276">En este ejemplo se da por supuesto que se ha inicializado el objeto **ExchangeService** con valores válidos en las propiedades de [las credenciales](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.exchangeservicebase.credentials%28v=exchg.80%29.aspx) y [dirección Url](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.exchangeservice.url%28v=exchg.80%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="239a4-276">This example assumes that the **ExchangeService** object has been initialized with valid values in the [Credentials](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.exchangeservicebase.credentials%28v=exchg.80%29.aspx) and [Url](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.exchangeservice.url%28v=exchg.80%29.aspx) properties.</span></span> 
  
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

<span data-ttu-id="239a4-277">Puede usar este método para buscar todos los elementos con la frase "plan del proyecto" en el asunto, tal como se muestra en este ejemplo.</span><span class="sxs-lookup"><span data-stu-id="239a4-277">You can use this method to search for all items with the phrase "project plan" in the subject, as shown in this example.</span></span>
  
```cs
string queryString = "subject:\"project plan\"";
SearchWithQueryString(service, WellKnownFolderName.Inbox, queryString);
```

## <a name="example-find-items-by-using-a-query-string-and-ews"></a><span data-ttu-id="239a4-278">Ejemplo: Buscar elementos mediante el uso de una cadena de consulta y EWS</span><span class="sxs-lookup"><span data-stu-id="239a4-278">Example: Find items by using a query string and EWS</span></span>
<span data-ttu-id="239a4-279"><a name="bk_ExampleEWS"> </a></span><span class="sxs-lookup"><span data-stu-id="239a4-279"></span></span>

<span data-ttu-id="239a4-280">En este ejemplo, una solicitud SOAP [FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) busca todos los elementos en la Bandeja de entrada con la frase "plan del proyecto" en el asunto.</span><span class="sxs-lookup"><span data-stu-id="239a4-280">In this example, a SOAP [FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) request finds all items in the Inbox with the phrase "project plan" in the subject.</span></span> 
  
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

<span data-ttu-id="239a4-281">En el ejemplo siguiente se muestra la respuesta del servidor con los resultados de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="239a4-281">The following example shows the response from the server with the search results.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="712" MinorBuildNumber="22" Version="V2_3" 
        xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
        xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:FindItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
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

## <a name="see-also"></a><span data-ttu-id="239a4-282">Vea también</span><span class="sxs-lookup"><span data-stu-id="239a4-282">See also</span></span>

- [<span data-ttu-id="239a4-283">Búsqueda y EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="239a4-283">Search and EWS in Exchange</span></span>](search-and-ews-in-exchange.md)    
- [<span data-ttu-id="239a4-284">Use los filtros de búsqueda con EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="239a4-284">Use search filters with EWS in Exchange</span></span>](how-to-use-search-filters-with-ews-in-exchange.md)    
- [<span data-ttu-id="239a4-285">ExchangeService.FindItems</span><span class="sxs-lookup"><span data-stu-id="239a4-285">ExchangeService.FindItems</span></span>](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx)    
- [<span data-ttu-id="239a4-286">Operación FindItem</span><span class="sxs-lookup"><span data-stu-id="239a4-286">FindItem operation</span></span>](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)
    

