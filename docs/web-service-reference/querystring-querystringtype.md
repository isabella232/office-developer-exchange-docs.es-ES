---
title: QueryString (QueryStringType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
api_name:
- QueryString
api_type:
- schema
ms.assetid: cadbf9a5-b87e-4d7f-b488-b76fb0ee7150
description: El elemento QueryString contiene una cadena de consulta de buzón basada en la sintaxis de consulta avanzada (AQS).
localization_priority: Priority
ms.openlocfilehash: eafbbab6de8d191197fb4b80e2b8e3cea80ab800
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459191"
---
# <a name="querystring-querystringtype"></a><span data-ttu-id="b0581-103">QueryString (QueryStringType)</span><span class="sxs-lookup"><span data-stu-id="b0581-103">QueryString (QueryStringType)</span></span>

<span data-ttu-id="b0581-104">El elemento **QueryString** contiene una cadena de consulta de buzón basada en la sintaxis de consulta avanzada (AQS).</span><span class="sxs-lookup"><span data-stu-id="b0581-104">The **QueryString** element contains a mailbox query string based on Advanced Query Syntax (AQS).</span></span> 
  
```XML
<QueryString/>
```

 <span data-ttu-id="b0581-105">**QueryStringType**</span><span class="sxs-lookup"><span data-stu-id="b0581-105">**QueryStringType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b0581-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="b0581-106">Attributes and elements</span></span>

<span data-ttu-id="b0581-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="b0581-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b0581-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="b0581-108">Attributes</span></span>

|<span data-ttu-id="b0581-109">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="b0581-109">**Attribute**</span></span>|<span data-ttu-id="b0581-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b0581-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b0581-111">ResetCache</span><span class="sxs-lookup"><span data-stu-id="b0581-111">ResetCache</span></span>  <br/> |<span data-ttu-id="b0581-112">Indica que se debe restablecer la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="b0581-112">Indicates that the cache should be reset.</span></span>  <br/> |
|<span data-ttu-id="b0581-113">ReturnDeletedItems</span><span class="sxs-lookup"><span data-stu-id="b0581-113">ReturnDeletedItems</span></span>  <br/> |<span data-ttu-id="b0581-114">Indica que se deben devolver los elementos eliminados.</span><span class="sxs-lookup"><span data-stu-id="b0581-114">Indicates that deleted items should be returned.</span></span>  <br/> |
|<span data-ttu-id="b0581-115">ReturnHighlightTerms</span><span class="sxs-lookup"><span data-stu-id="b0581-115">ReturnHighlightTerms</span></span>  <br/> |<span data-ttu-id="b0581-116">Indica que deben devolverse los términos resaltados.</span><span class="sxs-lookup"><span data-stu-id="b0581-116">Indicates that highlighted terms should be returned.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="b0581-117">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b0581-117">Child elements</span></span>

<span data-ttu-id="b0581-118">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="b0581-118">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="b0581-119">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="b0581-119">Parent elements</span></span>

|<span data-ttu-id="b0581-120">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="b0581-120">**Element**</span></span>|<span data-ttu-id="b0581-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b0581-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b0581-122">FindItem</span><span class="sxs-lookup"><span data-stu-id="b0581-122">FindItem</span></span>](finditem.md) <br/> |<span data-ttu-id="b0581-123">Define una solicitud para buscar elementos en un buzón.</span><span class="sxs-lookup"><span data-stu-id="b0581-123">Defines a request to find items in a mailbox.</span></span>  <br/> <span data-ttu-id="b0581-124">La siguiente es la expresión XPath a este elemento:/FindItem.</span><span class="sxs-lookup"><span data-stu-id="b0581-124">The following is the XPath expression to this element: /FindItem.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="b0581-125">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="b0581-125">Text value</span></span>

<span data-ttu-id="b0581-126">El valor de texto del elemento **QueryString** representa una consulta de buzón que se realiza mediante un subconjunto de la [Sintaxis de consulta avanzada (AQS)](https://msdn.microsoft.com/library/aa965711%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="b0581-126">The **QueryString** element text value represents a mailbox query that is made by using a subset of [Advanced Query Syntax (AQS)](https://msdn.microsoft.com/library/aa965711%28VS.85%29.aspx).</span></span> <span data-ttu-id="b0581-127">Vea la sección Comentarios para obtener información sobre las opciones de sintaxis admitidas para las cadenas de consulta.</span><span class="sxs-lookup"><span data-stu-id="b0581-127">See the remarks section for information about the supported syntax options for query strings.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b0581-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b0581-128">Remarks</span></span>

<span data-ttu-id="b0581-129">En Exchange Server 2010, este elemento es un tipo de cadena de esquema XML.</span><span class="sxs-lookup"><span data-stu-id="b0581-129">In Exchange Server 2010, this element is an XML schema string type.</span></span> <span data-ttu-id="b0581-130">En las versiones de Exchange a partir de Exchange Server 2013, incluido Exchange Online, el tipo de este elemento es **QueryStringType**.</span><span class="sxs-lookup"><span data-stu-id="b0581-130">In versions of Exchange starting with Exchange Server 2013, including Exchange Online, the type for this element is **QueryStringType**.</span></span> <span data-ttu-id="b0581-131">Este cambio no rompe los clientes existentes porque agrega tres nuevos atributos opcionales.</span><span class="sxs-lookup"><span data-stu-id="b0581-131">This change does not break any existing clients because it adds three new optional attributes.</span></span> 
  
<span data-ttu-id="b0581-132">El elemento **QueryString** excluye el uso de restricciones de EWS.</span><span class="sxs-lookup"><span data-stu-id="b0581-132">The **QueryString** element excludes the use of EWS restrictions.</span></span> <span data-ttu-id="b0581-133">AQS en EWS admite tres tipos de restricciones: restricción de fase de Word, restricción de intervalo de fechas y restricción de tipo de mensaje.</span><span class="sxs-lookup"><span data-stu-id="b0581-133">AQS in EWS supports three types of restrictions: word phase restriction, date range restriction, and message type restriction.</span></span> <span data-ttu-id="b0581-134">En las tablas siguientes se enumeran las propiedades de búsqueda admitidas para cada tipo de restricción.</span><span class="sxs-lookup"><span data-stu-id="b0581-134">The following tables list the supported search properties for each restriction type.</span></span> 
  
<span data-ttu-id="b0581-135">**Restricción de fase de Word**</span><span class="sxs-lookup"><span data-stu-id="b0581-135">**Word phase restriction**</span></span>

|<span data-ttu-id="b0581-136">**Propiedad**</span><span class="sxs-lookup"><span data-stu-id="b0581-136">**Property**</span></span>|<span data-ttu-id="b0581-137">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="b0581-137">**Example**</span></span>|<span data-ttu-id="b0581-138">**Función**</span><span class="sxs-lookup"><span data-stu-id="b0581-138">**Function**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b0581-139">from</span><span class="sxs-lookup"><span data-stu-id="b0581-139">from</span></span>  <br/> |<span data-ttu-id="b0581-140">De: Dean</span><span class="sxs-lookup"><span data-stu-id="b0581-140">From:Dean</span></span>  <br/> <span data-ttu-id="b0581-141">De: "Dean Halstead"</span><span class="sxs-lookup"><span data-stu-id="b0581-141">From:"Dean Halstead"</span></span>  <br/> |<span data-ttu-id="b0581-142">Buscar elementos enviados desde Dean.</span><span class="sxs-lookup"><span data-stu-id="b0581-142">Search items sent from Dean.</span></span>  <br/> <span data-ttu-id="b0581-143">Buscar elementos enviados desde Dean Halstead.</span><span class="sxs-lookup"><span data-stu-id="b0581-143">Search items sent from Dean Halstead.</span></span> <span data-ttu-id="b0581-144">El remitente debe ser exactamente "Dean Halstead".</span><span class="sxs-lookup"><span data-stu-id="b0581-144">The sender must be exactly "Dean Halstead".</span></span>  <br/> |
|<span data-ttu-id="b0581-145">a</span><span class="sxs-lookup"><span data-stu-id="b0581-145">to</span></span>  <br/> |<span data-ttu-id="b0581-146">Para: Dean</span><span class="sxs-lookup"><span data-stu-id="b0581-146">To:Dean</span></span>  <br/> |<span data-ttu-id="b0581-147">Buscar elementos enviados a Dean.</span><span class="sxs-lookup"><span data-stu-id="b0581-147">Search items sent to Dean.</span></span>  <br/> |
|<span data-ttu-id="b0581-148">cc</span><span class="sxs-lookup"><span data-stu-id="b0581-148">cc</span></span>  <br/> |<span data-ttu-id="b0581-149">CC: Dean</span><span class="sxs-lookup"><span data-stu-id="b0581-149">Cc:Dean</span></span>  <br/> |<span data-ttu-id="b0581-150">Busque los elementos con Dean en la línea CC.</span><span class="sxs-lookup"><span data-stu-id="b0581-150">Search for items with Dean on the Cc line.</span></span>  <br/> |
|<span data-ttu-id="b0581-151">cco</span><span class="sxs-lookup"><span data-stu-id="b0581-151">bcc</span></span>  <br/> |<span data-ttu-id="b0581-152">CCO: Dean</span><span class="sxs-lookup"><span data-stu-id="b0581-152">Bcc:Dean</span></span>  <br/> |<span data-ttu-id="b0581-153">Busque los elementos con Dean en la línea CCO.</span><span class="sxs-lookup"><span data-stu-id="b0581-153">Search for items with Dean on the Bcc line.</span></span>  <br/> |
|<span data-ttu-id="b0581-154">Participantes</span><span class="sxs-lookup"><span data-stu-id="b0581-154">Participants</span></span>  <br/> |<span data-ttu-id="b0581-155">Participantes: Dean</span><span class="sxs-lookup"><span data-stu-id="b0581-155">Participants:Dean</span></span>  <br/> |<span data-ttu-id="b0581-156">Busca elementos con Dean en los campos to, CC o BCC.</span><span class="sxs-lookup"><span data-stu-id="b0581-156">Search for items with Dean in the To, Cc, or Bcc fields.</span></span>  <br/> |
|<span data-ttu-id="b0581-157">Subject</span><span class="sxs-lookup"><span data-stu-id="b0581-157">Subject</span></span>  <br/> |<span data-ttu-id="b0581-158">Asunto: producto</span><span class="sxs-lookup"><span data-stu-id="b0581-158">Subject:product</span></span>  <br/> <span data-ttu-id="b0581-159">Asunto: (desarrollo de producto)</span><span class="sxs-lookup"><span data-stu-id="b0581-159">Subject:(product development)</span></span>  <br/> <span data-ttu-id="b0581-160">Asunto: "desarrollo de producto"</span><span class="sxs-lookup"><span data-stu-id="b0581-160">Subject:"product development"</span></span>  <br/> |<span data-ttu-id="b0581-161">Busca elementos con producto en el asunto.</span><span class="sxs-lookup"><span data-stu-id="b0581-161">Search for items with product in the subject.</span></span>  <br/> <span data-ttu-id="b0581-162">Busca elementos con producto y desarrollo en el asunto.</span><span class="sxs-lookup"><span data-stu-id="b0581-162">Search for items with product and development in the subject.</span></span>  <br/> |
|<span data-ttu-id="b0581-163">Cuerpo</span><span class="sxs-lookup"><span data-stu-id="b0581-163">Body</span></span>  <br/> <span data-ttu-id="b0581-164">Contenido</span><span class="sxs-lookup"><span data-stu-id="b0581-164">Content</span></span>  <br/> |<span data-ttu-id="b0581-165">Cuerpo: progreso</span><span class="sxs-lookup"><span data-stu-id="b0581-165">Body:progress</span></span>  <br/> <span data-ttu-id="b0581-166">Contenido: progreso</span><span class="sxs-lookup"><span data-stu-id="b0581-166">Content:progress</span></span>  <br/> |<span data-ttu-id="b0581-167">Busca elementos con progreso en el cuerpo.</span><span class="sxs-lookup"><span data-stu-id="b0581-167">Search for items with progress in the body.</span></span>  <br/> |
|<span data-ttu-id="b0581-168">Datos adjuntos</span><span class="sxs-lookup"><span data-stu-id="b0581-168">Attachment</span></span>  <br/> |<span data-ttu-id="b0581-169">Datos adjuntos: informe</span><span class="sxs-lookup"><span data-stu-id="b0581-169">Attachment:report</span></span>  <br/> |<span data-ttu-id="b0581-170">Busca elementos con informe en el nombre del archivo adjunto o en el cuerpo del archivo.</span><span class="sxs-lookup"><span data-stu-id="b0581-170">Search for items with report in the attachment file name or file body.</span></span>  <br/> |
|<span data-ttu-id="b0581-171">(no se especifica la propiedad)</span><span class="sxs-lookup"><span data-stu-id="b0581-171">(property is not specified)</span></span>  <br/> |<span data-ttu-id="b0581-172">Desarrollo de productos</span><span class="sxs-lookup"><span data-stu-id="b0581-172">Product Development</span></span>  <br/> |<span data-ttu-id="b0581-173">Busque elementos que contengan el producto y el desarrollo en todas las propiedades de la fase de Word.</span><span class="sxs-lookup"><span data-stu-id="b0581-173">Search for items that contain both product and development in all word phase properties.</span></span>  <br/> |
   
<span data-ttu-id="b0581-174">La coincidencia de restricción de fase de Word siempre no distingue mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="b0581-174">Word phase restriction match is always case insensitive.</span></span> <span data-ttu-id="b0581-175">La restricción de fase de Word admite dos tipos de coincidencia: coincidencia de prefijo o coincidencia exacta.</span><span class="sxs-lookup"><span data-stu-id="b0581-175">Word phase restriction supports two match types: prefix match or exact match.</span></span> <span data-ttu-id="b0581-176">La coincidencia de prefijo es el comportamiento predeterminado de la coincidencia.</span><span class="sxs-lookup"><span data-stu-id="b0581-176">Prefix match is the default match behavior.</span></span> <span data-ttu-id="b0581-177">Si desea que la coincidencia sea exacta, use comillas dobles.</span><span class="sxs-lookup"><span data-stu-id="b0581-177">If you want exact match, use double quotes.</span></span> <span data-ttu-id="b0581-178">Por ejemplo, asunto: "Product" coincide con "Product", pero no con "Production" en el asunto.</span><span class="sxs-lookup"><span data-stu-id="b0581-178">For example, subject:"product" matches 'product' but not 'production' in the subject.</span></span> <span data-ttu-id="b0581-179">Varias palabras en comillas dobles restringen ambas fases de Word y su orden.</span><span class="sxs-lookup"><span data-stu-id="b0581-179">Multiple words in double quotes restrict both word phases and their order.</span></span> <span data-ttu-id="b0581-180">Por ejemplo, "el producto de" gana "coincide solamente con" producto Win ", no con" Win95 Product "ni" Product of Win ".</span><span class="sxs-lookup"><span data-stu-id="b0581-180">For example "win product" matches only 'win product', not 'win95 product' or 'product of win'.</span></span> <span data-ttu-id="b0581-181">Puede usar un asterisco ( \* ) para definir una coincidencia de prefijo con Order Restricted.</span><span class="sxs-lookup"><span data-stu-id="b0581-181">You can use an asterisk (\*) to define a prefix match with order restricted.</span></span> <span data-ttu-id="b0581-182">Por ejemplo, "producto Win" \* coincide con "Win95 Product", "Windows Production line" pero no con "Windows New Product" ni "Product of Win".</span><span class="sxs-lookup"><span data-stu-id="b0581-182">For example, "win product"\* matches 'win95 product', 'windows production line' but not 'windows new product' or 'product of win'.</span></span> <span data-ttu-id="b0581-183">Puede buscar en todos los mensajes enviados desde o hacia un dominio.</span><span class="sxs-lookup"><span data-stu-id="b0581-183">You can search all messages sent from or to a domain.</span></span> <span data-ttu-id="b0581-184">Por ejemplo, from: "@hotmail. com" devuelve todos los mensajes enviados desde hotmail.com.</span><span class="sxs-lookup"><span data-stu-id="b0581-184">For example, from:"@hotmail.com" returns all messages sent from hotmail.com.</span></span>
  
<span data-ttu-id="b0581-185">En la tabla siguiente se describen las restricciones del intervalo de fechas.</span><span class="sxs-lookup"><span data-stu-id="b0581-185">The following table describes date range restrictions.</span></span>
  
<span data-ttu-id="b0581-186">**Restricción de intervalo de fechas**</span><span class="sxs-lookup"><span data-stu-id="b0581-186">**Date range restriction**</span></span>

|<span data-ttu-id="b0581-187">**Propiedad**</span><span class="sxs-lookup"><span data-stu-id="b0581-187">**Property**</span></span>|<span data-ttu-id="b0581-188">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="b0581-188">**Example**</span></span>|<span data-ttu-id="b0581-189">**Función**</span><span class="sxs-lookup"><span data-stu-id="b0581-189">**Function**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b0581-190">Sent</span><span class="sxs-lookup"><span data-stu-id="b0581-190">Sent</span></span>  <br/> |<span data-ttu-id="b0581-191">Enviado: última semana</span><span class="sxs-lookup"><span data-stu-id="b0581-191">Sent:last week</span></span>  <br/> <span data-ttu-id="b0581-192">Enviado el: 01/01/2001</span><span class="sxs-lookup"><span data-stu-id="b0581-192">Sent:01/01/2001</span></span>  <br/> <span data-ttu-id="b0581-193">Enviado el: 01/01/2001.. 01/15/2001</span><span class="sxs-lookup"><span data-stu-id="b0581-193">Sent:01/01/2001..01/15/2001</span></span>  <br/> |<span data-ttu-id="b0581-194">Elementos de búsqueda enviados la semana pasada.</span><span class="sxs-lookup"><span data-stu-id="b0581-194">Search items sent last week.</span></span>  <br/> <span data-ttu-id="b0581-195">Buscar los elementos enviados el 1 de enero de 2001.</span><span class="sxs-lookup"><span data-stu-id="b0581-195">Search items sent on January 1st, 2001.</span></span>  <br/> <span data-ttu-id="b0581-196">Buscar los elementos enviados entre el 1 de enero de 2001 y el 15 de enero de 2001.</span><span class="sxs-lookup"><span data-stu-id="b0581-196">Search items sent between January 1st, 2001 and January 15th, 2001.</span></span>  <br/> |
|<span data-ttu-id="b0581-197">Cantidad.Recibida</span><span class="sxs-lookup"><span data-stu-id="b0581-197">Received</span></span>  <br/> |<span data-ttu-id="b0581-198">Recibido: hoy</span><span class="sxs-lookup"><span data-stu-id="b0581-198">Received:today</span></span>  <br/> <span data-ttu-id="b0581-199">Recibido: 01/01/2001</span><span class="sxs-lookup"><span data-stu-id="b0581-199">Received:01/01/2001</span></span>  <br/> |<span data-ttu-id="b0581-200">Elementos de búsqueda recibidos hoy.</span><span class="sxs-lookup"><span data-stu-id="b0581-200">Search items received today.</span></span>  <br/> <span data-ttu-id="b0581-201">Buscar los elementos recibidos el 1 de enero de 2001.</span><span class="sxs-lookup"><span data-stu-id="b0581-201">Search items received on January 1st, 2001.</span></span>  <br/> |
   
<span data-ttu-id="b0581-202">Los dos puntos (..) es un operador de rango.</span><span class="sxs-lookup"><span data-stu-id="b0581-202">The two dots (..) is a range operator.</span></span> <span data-ttu-id="b0581-203">Se puede usar para definir un intervalo con una fecha de inicio y una fecha de finalización.</span><span class="sxs-lookup"><span data-stu-id="b0581-203">It can be used to define a range with a start and an end date.</span></span> <span data-ttu-id="b0581-204">Para especificar una fecha, puede usar fechas relativas.</span><span class="sxs-lookup"><span data-stu-id="b0581-204">To specify a date, you can use relative dates.</span></span> <span data-ttu-id="b0581-205">Se admiten las siguientes fechas relativas:</span><span class="sxs-lookup"><span data-stu-id="b0581-205">The following relative dates are supported:</span></span>
  
- <span data-ttu-id="b0581-206">Fechas relativas: hoy, mañana, ayer</span><span class="sxs-lookup"><span data-stu-id="b0581-206">Relative dates: Today, tomorrow, yesterday</span></span>
    
- <span data-ttu-id="b0581-207">Fechas relativas a multiword: esta semana, mes próximo, semana pasada, mes pasado o año próximo</span><span class="sxs-lookup"><span data-stu-id="b0581-207">Multiword relative dates: This week, next month, last week, past month, or coming year</span></span>
    
- <span data-ttu-id="b0581-208">Días: Domingo, lunes, martes, miércoles, jueves, viernes, sábado</span><span class="sxs-lookup"><span data-stu-id="b0581-208">Days: Sunday, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday</span></span>
    
- <span data-ttu-id="b0581-209">Enero, febrero, marzo, abril, mayo, junio, julio, agosto, septiembre, octubre, noviembre, diciembre</span><span class="sxs-lookup"><span data-stu-id="b0581-209">January, February, March, April, May, June, July, August, September, October, November, December</span></span>
    
<span data-ttu-id="b0581-210">En la tabla siguiente se describen las restricciones de tipo de mensaje.</span><span class="sxs-lookup"><span data-stu-id="b0581-210">The following table describes message type restrictions.</span></span> 
  
<span data-ttu-id="b0581-211">**Restricción de tipo de mensaje**</span><span class="sxs-lookup"><span data-stu-id="b0581-211">**Message type restriction**</span></span>

|<span data-ttu-id="b0581-212">**Propiedad**</span><span class="sxs-lookup"><span data-stu-id="b0581-212">**Property**</span></span>|<span data-ttu-id="b0581-213">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="b0581-213">**Example**</span></span>|<span data-ttu-id="b0581-214">**Función**</span><span class="sxs-lookup"><span data-stu-id="b0581-214">**Function**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b0581-215">Tipo</span><span class="sxs-lookup"><span data-stu-id="b0581-215">Kind</span></span>  <br/> |<span data-ttu-id="b0581-216">Tipo: tareas</span><span class="sxs-lookup"><span data-stu-id="b0581-216">Kind:tasks</span></span>  <br/> |<span data-ttu-id="b0581-217">Buscar en todos los elementos de tarea.</span><span class="sxs-lookup"><span data-stu-id="b0581-217">Search all task items.</span></span>  <br/> |
   
<span data-ttu-id="b0581-218">AQS en EWS usa la propiedad **Kind** para especificar el tipo de mensaje.</span><span class="sxs-lookup"><span data-stu-id="b0581-218">AQS in EWS uses the **Kind** property to specify the message type.</span></span> <span data-ttu-id="b0581-219">La propiedad Kind se puede usar con los siguientes tipos de elemento:</span><span class="sxs-lookup"><span data-stu-id="b0581-219">The Kind property can be used with the following item types:</span></span> 
  
- <span data-ttu-id="b0581-220">email</span><span class="sxs-lookup"><span data-stu-id="b0581-220">email</span></span>
    
- <span data-ttu-id="b0581-221">reuniones</span><span class="sxs-lookup"><span data-stu-id="b0581-221">meetings</span></span>
    
- <span data-ttu-id="b0581-222">tasks</span><span class="sxs-lookup"><span data-stu-id="b0581-222">tasks</span></span>
    
- <span data-ttu-id="b0581-223">notas</span><span class="sxs-lookup"><span data-stu-id="b0581-223">notes</span></span>
    
- <span data-ttu-id="b0581-224">documentos</span><span class="sxs-lookup"><span data-stu-id="b0581-224">docs</span></span>
    
- <span data-ttu-id="b0581-225">diarios</span><span class="sxs-lookup"><span data-stu-id="b0581-225">journals</span></span>
    
- <span data-ttu-id="b0581-226">contacts</span><span class="sxs-lookup"><span data-stu-id="b0581-226">contacts</span></span>
    
- <span data-ttu-id="b0581-227">mensajería instantánea</span><span class="sxs-lookup"><span data-stu-id="b0581-227">im</span></span>
    
<span data-ttu-id="b0581-228">En la siguiente tabla se describen los conectores lógicos de agrupación.</span><span class="sxs-lookup"><span data-stu-id="b0581-228">The following table describes grouping logical connectors.</span></span>
  
<span data-ttu-id="b0581-229">**Agrupación de conectores lógicos**</span><span class="sxs-lookup"><span data-stu-id="b0581-229">**Grouping logical connectors**</span></span>

|<span data-ttu-id="b0581-230">**Connector**</span><span class="sxs-lookup"><span data-stu-id="b0581-230">**Connector**</span></span>|<span data-ttu-id="b0581-231">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="b0581-231">**Example**</span></span>|<span data-ttu-id="b0581-232">**Función**</span><span class="sxs-lookup"><span data-stu-id="b0581-232">**Function**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b0581-233">Y</span><span class="sxs-lookup"><span data-stu-id="b0581-233">AND</span></span>  <br/> |<span data-ttu-id="b0581-234">Asunto: producto y asunto: desarrollo</span><span class="sxs-lookup"><span data-stu-id="b0581-234">Subject:product AND subject:development</span></span>  <br/> <span data-ttu-id="b0581-235">Asunto: (Product y Development)</span><span class="sxs-lookup"><span data-stu-id="b0581-235">Subject:(product AND development)</span></span>  <br/> <span data-ttu-id="b0581-236">Asunto: (desarrollo de producto)</span><span class="sxs-lookup"><span data-stu-id="b0581-236">Subject:(product development)</span></span>  <br/> |<span data-ttu-id="b0581-237">Buscar elementos con el producto y el desarrollo en el asunto.</span><span class="sxs-lookup"><span data-stu-id="b0581-237">Search items with both product and development in the subject.</span></span>  <br/> |
|<span data-ttu-id="b0581-238">O</span><span class="sxs-lookup"><span data-stu-id="b0581-238">OR</span></span>  <br/> |<span data-ttu-id="b0581-239">Cuerpo: proyecto o cuerpo: propuesta</span><span class="sxs-lookup"><span data-stu-id="b0581-239">Body:project OR body:proposal</span></span>  <br/> <span data-ttu-id="b0581-240">Cuerpo: (proyecto o propuesta)</span><span class="sxs-lookup"><span data-stu-id="b0581-240">Body:(project OR proposal)</span></span>  <br/> |<span data-ttu-id="b0581-241">Buscar elementos con el producto o el desarrollo en el cuerpo.</span><span class="sxs-lookup"><span data-stu-id="b0581-241">Search items with either product or development in the body.</span></span>  <br/> |
|<span data-ttu-id="b0581-242">NO</span><span class="sxs-lookup"><span data-stu-id="b0581-242">NOT</span></span>  <br/> |<span data-ttu-id="b0581-243">NO cuerpo: propuesta</span><span class="sxs-lookup"><span data-stu-id="b0581-243">NOT body:proposal</span></span>  <br/> <span data-ttu-id="b0581-244">Cuerpo: (no propuesta)</span><span class="sxs-lookup"><span data-stu-id="b0581-244">Body:(NOT proposal)</span></span>  <br/> |<span data-ttu-id="b0581-245">Buscar mensajes sin propuestas en el cuerpo.</span><span class="sxs-lookup"><span data-stu-id="b0581-245">Search messages without proposal in the body.</span></span>  <br/> |
   
<span data-ttu-id="b0581-246">Y siempre es el conector predeterminado.</span><span class="sxs-lookup"><span data-stu-id="b0581-246">AND is always the default connector.</span></span> <span data-ttu-id="b0581-247">Por ejemplo, asunto: proyecto y cuerpo: la propuesta es la misma que el asunto: cuerpo del proyecto: propuesta.</span><span class="sxs-lookup"><span data-stu-id="b0581-247">For example, subject:project AND body:proposal is the same as subject:project body:proposal.</span></span> <span data-ttu-id="b0581-248">Los conectores lógicos distinguen mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="b0581-248">Logical connectors are case sensitive.</span></span> <span data-ttu-id="b0581-249">Por ejemplo, Body: (proyecto o propuesta) busca los mensajes con "Project", "o", y "proposar" en el cuerpo en lugar de "Project" o "proposar".</span><span class="sxs-lookup"><span data-stu-id="b0581-249">For example, body:(project Or proposal) searches messages with 'project', 'or', and 'proposal' in the body instead of 'project' or 'proposal'.</span></span> <span data-ttu-id="b0581-250">El símbolo más (+) equivale a y.</span><span class="sxs-lookup"><span data-stu-id="b0581-250">The plus symbol (+) is equivalent to AND.</span></span> <span data-ttu-id="b0581-251">El símbolo de guión (-) equivale a no.</span><span class="sxs-lookup"><span data-stu-id="b0581-251">The hyphen symbol (-) is equivalent to NOT.</span></span> <span data-ttu-id="b0581-252">Por ejemplo, Body: (Project-Proposal) busca los mensajes con ' Project ' pero sin ' proposar ' en el cuerpo.</span><span class="sxs-lookup"><span data-stu-id="b0581-252">For example, body:(project - proposal) searches messages with 'project' but without 'proposal' in the body.</span></span> 
  
<span data-ttu-id="b0581-253">La cadena de consulta también puede contener propiedades no indizadas para la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="b0581-253">The query string can also contain nonindexed properties for search.</span></span> <span data-ttu-id="b0581-254">Si la cadena de consulta contiene propiedades no indizadas, la búsqueda puede realizar una búsqueda de Exchange en las propiedades indizadas y una búsqueda de almacén en las propiedades no indizadas.</span><span class="sxs-lookup"><span data-stu-id="b0581-254">If the query string contains nonindexed properties, the search might perform an Exchange search on the indexed properties and a store search on the nonindexed properties.</span></span> 
  
<span data-ttu-id="b0581-255">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="b0581-255">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="example"></a><span data-ttu-id="b0581-256">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b0581-256">Example</span></span>

<span data-ttu-id="b0581-257">En el siguiente ejemplo se muestra una solicitud para buscar mensajes en la bandeja de entrada con la detección automática en el asunto.</span><span class="sxs-lookup"><span data-stu-id="b0581-257">The following example shows a request to search for messages in the Inbox with Autodiscover in the subject.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2010" />
  </soap:Header>
  <soap:Body>
    <m:FindItem Traversal="Shallow">
      <m:ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="item:Subject" />
        </t:AdditionalProperties>
      </m:ItemShape>
      <m:IndexedPageItemView MaxEntriesReturned="1" Offset="0" BasePoint="Beginning" />
      <m:ParentFolderIds>
        <t:DistinguishedFolderId Id="inbox" />
      </m:ParentFolderIds>
      <m:QueryString>subject:Autodiscover</m:QueryString>
    </m:FindItem>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="b0581-258">En el ejemplo siguiente se muestra una respuesta correcta a la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b0581-258">The following example shows a successful response to the request.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="14" 
                         MinorVersion="0" 
                         MajorBuildNumber="639" 
                         MinorBuildNumber="20" 
                         Version="Exchange2010" 
                         xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:FindItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:FindItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:RootFolder IndexedPagingOffset="1" 
                        TotalItemsInView="5" 
                        IncludesLastItemInRange="false">
            <t:Items>
              <t:Message>
                <t:ItemId Id="AAMkADEzOTExYjJkLTYx" ChangeKey="CQAAABY" />
                <t:Subject>How to use Autodiscover</t:Subject>
              </t:Message>
            </t:Items>
          </m:RootFolder>
        </m:FindItemResponseMessage>
      </m:ResponseMessages>
    </m:FindItemResponse>
  </s:Body>
</s:Envelope>

```

## <a name="element-information"></a><span data-ttu-id="b0581-259">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="b0581-259">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b0581-260">Namespace</span><span class="sxs-lookup"><span data-stu-id="b0581-260">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="b0581-261">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="b0581-261">Schema name</span></span>  <br/> |<span data-ttu-id="b0581-262">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="b0581-262">Messages schema</span></span>  <br/> |
|<span data-ttu-id="b0581-263">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="b0581-263">Validation file</span></span>  <br/> |<span data-ttu-id="b0581-264">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="b0581-264">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="b0581-265">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="b0581-265">Can be empty</span></span>  <br/> |<span data-ttu-id="b0581-266">Falso</span><span class="sxs-lookup"><span data-stu-id="b0581-266">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b0581-267">Vea también</span><span class="sxs-lookup"><span data-stu-id="b0581-267">See also</span></span>



[<span data-ttu-id="b0581-268">Operación FindItem</span><span class="sxs-lookup"><span data-stu-id="b0581-268">FindItem operation</span></span>](finditem-operation.md)
  
[<span data-ttu-id="b0581-269">Operación FindConversation</span><span class="sxs-lookup"><span data-stu-id="b0581-269">FindConversation operation</span></span>](findconversation-operation.md)


- [<span data-ttu-id="b0581-270">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="b0581-270">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

