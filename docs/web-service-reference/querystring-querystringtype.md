---
title: QueryString (QueryStringType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- QueryString
api_type:
- schema
ms.assetid: cadbf9a5-b87e-4d7f-b488-b76fb0ee7150
description: El elemento de cadena de consulta contiene una cadena de consulta de buzón de correo basada en la sintaxis de consulta avanzada (AQS).
ms.openlocfilehash: 410405638b3f8628dc589049873cfea1f153310c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836943"
---
# <a name="querystring-querystringtype"></a><span data-ttu-id="5836a-103">QueryString (QueryStringType)</span><span class="sxs-lookup"><span data-stu-id="5836a-103">QueryString (QueryStringType)</span></span>

<span data-ttu-id="5836a-104">El elemento de **cadena de consulta** contiene una cadena de consulta de buzón de correo basada en la sintaxis de consulta avanzada (AQS).</span><span class="sxs-lookup"><span data-stu-id="5836a-104">The **QueryString** element contains a mailbox query string based on Advanced Query Syntax (AQS).</span></span> 
  
```XML
<QueryString/>
```

 <span data-ttu-id="5836a-105">**QueryStringType**</span><span class="sxs-lookup"><span data-stu-id="5836a-105">**QueryStringType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="5836a-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="5836a-106">Attributes and elements</span></span>

<span data-ttu-id="5836a-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="5836a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5836a-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="5836a-108">Attributes</span></span>

|<span data-ttu-id="5836a-109">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="5836a-109">**Attribute**</span></span>|<span data-ttu-id="5836a-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5836a-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5836a-111">ResetCache</span><span class="sxs-lookup"><span data-stu-id="5836a-111">ResetCache</span></span>  <br/> |<span data-ttu-id="5836a-112">Indica que se debe restablecer la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="5836a-112">Indicates that the cache should be reset.</span></span>  <br/> |
|<span data-ttu-id="5836a-113">ReturnDeletedItems</span><span class="sxs-lookup"><span data-stu-id="5836a-113">ReturnDeletedItems</span></span>  <br/> |<span data-ttu-id="5836a-114">Indica que se deben devolver los elementos eliminados.</span><span class="sxs-lookup"><span data-stu-id="5836a-114">Indicates that deleted items should be returned.</span></span>  <br/> |
|<span data-ttu-id="5836a-115">ReturnHighlightTerms</span><span class="sxs-lookup"><span data-stu-id="5836a-115">ReturnHighlightTerms</span></span>  <br/> |<span data-ttu-id="5836a-116">Indica que se deben devolver el resaltado términos.</span><span class="sxs-lookup"><span data-stu-id="5836a-116">Indicates that highlighted terms should be returned.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="5836a-117">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="5836a-117">Child elements</span></span>

<span data-ttu-id="5836a-118">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="5836a-118">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="5836a-119">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="5836a-119">Parent elements</span></span>

|<span data-ttu-id="5836a-120">**Element**</span><span class="sxs-lookup"><span data-stu-id="5836a-120">**Element**</span></span>|<span data-ttu-id="5836a-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5836a-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5836a-122">FindItem</span><span class="sxs-lookup"><span data-stu-id="5836a-122">FindItem</span></span>](finditem.md) <br/> |<span data-ttu-id="5836a-123">Define una solicitud para buscar elementos en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="5836a-123">Defines a request to find items in a mailbox.</span></span>  <br/> <span data-ttu-id="5836a-124">La siguiente es la expresión de XPath para este elemento: /FindItem.</span><span class="sxs-lookup"><span data-stu-id="5836a-124">The following is the XPath expression to this element: /FindItem.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="5836a-125">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="5836a-125">Text value</span></span>

<span data-ttu-id="5836a-126">El valor de texto del elemento de **cadena de consulta** representa una consulta de buzón de correo que se realiza mediante el uso de un subconjunto de la [Sintaxis de consulta avanzada (AQS)](http://msdn.microsoft.com/en-us/library/aa965711%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="5836a-126">The **QueryString** element text value represents a mailbox query that is made by using a subset of [Advanced Query Syntax (AQS)](http://msdn.microsoft.com/en-us/library/aa965711%28VS.85%29.aspx).</span></span> <span data-ttu-id="5836a-127">Vea la sección Comentarios para obtener información acerca de las opciones de sintaxis admitida para cadenas de consulta.</span><span class="sxs-lookup"><span data-stu-id="5836a-127">See the remarks section for information about the supported syntax options for query strings.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5836a-128">Notas</span><span class="sxs-lookup"><span data-stu-id="5836a-128">Remarks</span></span>

<span data-ttu-id="5836a-129">En Exchange Server 2010, este elemento es un tipo de cadena de esquema XML.</span><span class="sxs-lookup"><span data-stu-id="5836a-129">In Exchange Server 2010, this element is an XML schema string type.</span></span> <span data-ttu-id="5836a-130">En las versiones de Exchange Server 2013 a partir de Exchange, incluido Exchange Online, el tipo de este elemento es **QueryStringType**.</span><span class="sxs-lookup"><span data-stu-id="5836a-130">In versions of Exchange starting with Exchange Server 2013, including Exchange Online, the type for this element is **QueryStringType**.</span></span> <span data-ttu-id="5836a-131">Este cambio no interrumpen a los clientes existentes ya que agrega tres nuevos atributos opcionales.</span><span class="sxs-lookup"><span data-stu-id="5836a-131">This change does not break any existing clients because it adds three new optional attributes.</span></span> 
  
<span data-ttu-id="5836a-132">El elemento **QueryString** excluye el uso de restricciones de EWS.</span><span class="sxs-lookup"><span data-stu-id="5836a-132">The **QueryString** element excludes the use of EWS restrictions.</span></span> <span data-ttu-id="5836a-133">AQS en EWS admite tres tipos de restricciones: restricción de fase, restricción de intervalo de fecha y restricción de tipo de mensaje de word.</span><span class="sxs-lookup"><span data-stu-id="5836a-133">AQS in EWS supports three types of restrictions: word phase restriction, date range restriction, and message type restriction.</span></span> <span data-ttu-id="5836a-134">Las siguientes tablas enumeran las propiedades de búsqueda admitidos para cada tipo de restricción.</span><span class="sxs-lookup"><span data-stu-id="5836a-134">The following tables list the supported search properties for each restriction type.</span></span> 
  
<span data-ttu-id="5836a-135">**Restricción de la fase de Word**</span><span class="sxs-lookup"><span data-stu-id="5836a-135">**Word phase restriction**</span></span>

|<span data-ttu-id="5836a-136">**Propiedad**</span><span class="sxs-lookup"><span data-stu-id="5836a-136">**Property**</span></span>|<span data-ttu-id="5836a-137">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="5836a-137">**Example**</span></span>|<span data-ttu-id="5836a-138">**Funci�n**</span><span class="sxs-lookup"><span data-stu-id="5836a-138">**Function**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="5836a-139">from</span><span class="sxs-lookup"><span data-stu-id="5836a-139">from</span></span>  <br/> |<span data-ttu-id="5836a-140">Desde: Dean</span><span class="sxs-lookup"><span data-stu-id="5836a-140">From:Dean</span></span>  <br/> <span data-ttu-id="5836a-141">De: "Dean Halstead"</span><span class="sxs-lookup"><span data-stu-id="5836a-141">From:"Dean Halstead"</span></span>  <br/> |<span data-ttu-id="5836a-142">Buscar artículos enviados desde Dean.</span><span class="sxs-lookup"><span data-stu-id="5836a-142">Search items sent from Dean.</span></span>  <br/> <span data-ttu-id="5836a-143">Buscar artículos enviados desde Dean Halstead.</span><span class="sxs-lookup"><span data-stu-id="5836a-143">Search items sent from Dean Halstead.</span></span> <span data-ttu-id="5836a-144">El remitente debe ser exactamente "Dean Halstead".</span><span class="sxs-lookup"><span data-stu-id="5836a-144">The sender must be exactly "Dean Halstead".</span></span>  <br/> |
|<span data-ttu-id="5836a-145">a</span><span class="sxs-lookup"><span data-stu-id="5836a-145">to</span></span>  <br/> |<span data-ttu-id="5836a-146">Para: Dean</span><span class="sxs-lookup"><span data-stu-id="5836a-146">To:Dean</span></span>  <br/> |<span data-ttu-id="5836a-147">Buscar elementos enviados a Dean.</span><span class="sxs-lookup"><span data-stu-id="5836a-147">Search items sent to Dean.</span></span>  <br/> |
|<span data-ttu-id="5836a-148">cc</span><span class="sxs-lookup"><span data-stu-id="5836a-148">cc</span></span>  <br/> |<span data-ttu-id="5836a-149">Cc:Dean</span><span class="sxs-lookup"><span data-stu-id="5836a-149">Cc:Dean</span></span>  <br/> |<span data-ttu-id="5836a-150">Buscar elementos con Dean en la línea Cc.</span><span class="sxs-lookup"><span data-stu-id="5836a-150">Search for items with Dean on the Cc line.</span></span>  <br/> |
|<span data-ttu-id="5836a-151">bcc</span><span class="sxs-lookup"><span data-stu-id="5836a-151">bcc</span></span>  <br/> |<span data-ttu-id="5836a-152">BCC:Dean</span><span class="sxs-lookup"><span data-stu-id="5836a-152">Bcc:Dean</span></span>  <br/> |<span data-ttu-id="5836a-153">Buscar elementos con Dean en la línea CCO.</span><span class="sxs-lookup"><span data-stu-id="5836a-153">Search for items with Dean on the Bcc line.</span></span>  <br/> |
|<span data-ttu-id="5836a-154">Participantes</span><span class="sxs-lookup"><span data-stu-id="5836a-154">Participants</span></span>  <br/> |<span data-ttu-id="5836a-155">Los participantes: Dean</span><span class="sxs-lookup"><span data-stu-id="5836a-155">Participants:Dean</span></span>  <br/> |<span data-ttu-id="5836a-156">Buscar elementos con Dean en para, Cc o CCO campos.</span><span class="sxs-lookup"><span data-stu-id="5836a-156">Search for items with Dean in the To, Cc, or Bcc fields.</span></span>  <br/> |
|<span data-ttu-id="5836a-157">Subject</span><span class="sxs-lookup"><span data-stu-id="5836a-157">Subject</span></span>  <br/> |<span data-ttu-id="5836a-158">Asunto: producto</span><span class="sxs-lookup"><span data-stu-id="5836a-158">Subject:product</span></span>  <br/> <span data-ttu-id="5836a-159">Asunto:(product development)</span><span class="sxs-lookup"><span data-stu-id="5836a-159">Subject:(product development)</span></span>  <br/> <span data-ttu-id="5836a-160">Asunto: "desarrollo de productos"</span><span class="sxs-lookup"><span data-stu-id="5836a-160">Subject:"product development"</span></span>  <br/> |<span data-ttu-id="5836a-161">Buscar elementos con el producto en el asunto.</span><span class="sxs-lookup"><span data-stu-id="5836a-161">Search for items with product in the subject.</span></span>  <br/> <span data-ttu-id="5836a-162">Buscar elementos con productos y desarrollo en el asunto.</span><span class="sxs-lookup"><span data-stu-id="5836a-162">Search for items with product and development in the subject.</span></span>  <br/> |
|<span data-ttu-id="5836a-163">Cuerpo</span><span class="sxs-lookup"><span data-stu-id="5836a-163">Body</span></span>  <br/> <span data-ttu-id="5836a-164">Contenido</span><span class="sxs-lookup"><span data-stu-id="5836a-164">Content</span></span>  <br/> |<span data-ttu-id="5836a-165">Cuerpo: progreso</span><span class="sxs-lookup"><span data-stu-id="5836a-165">Body:progress</span></span>  <br/> <span data-ttu-id="5836a-166">Contenido: progreso</span><span class="sxs-lookup"><span data-stu-id="5836a-166">Content:progress</span></span>  <br/> |<span data-ttu-id="5836a-167">Buscar elementos con el progreso en el cuerpo.</span><span class="sxs-lookup"><span data-stu-id="5836a-167">Search for items with progress in the body.</span></span>  <br/> |
|<span data-ttu-id="5836a-168">Datos adjuntos</span><span class="sxs-lookup"><span data-stu-id="5836a-168">Attachment</span></span>  <br/> |<span data-ttu-id="5836a-169">Datos adjuntos: informe</span><span class="sxs-lookup"><span data-stu-id="5836a-169">Attachment:report</span></span>  <br/> |<span data-ttu-id="5836a-170">Buscar elementos con el informe en el cuerpo de archivo o nombre de archivo de datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="5836a-170">Search for items with report in the attachment file name or file body.</span></span>  <br/> |
|<span data-ttu-id="5836a-171">(no se especifica la propiedad)</span><span class="sxs-lookup"><span data-stu-id="5836a-171">(property is not specified)</span></span>  <br/> |<span data-ttu-id="5836a-172">Desarrollo de productos</span><span class="sxs-lookup"><span data-stu-id="5836a-172">Product Development</span></span>  <br/> |<span data-ttu-id="5836a-173">Buscar elementos que contienen productos y desarrollo en todas las propiedades de fase de word.</span><span class="sxs-lookup"><span data-stu-id="5836a-173">Search for items that contain both product and development in all word phase properties.</span></span>  <br/> |
   
<span data-ttu-id="5836a-174">Coincidencia de restricción de la fase de Word siempre distingue mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="5836a-174">Word phase restriction match is always case insensitive.</span></span> <span data-ttu-id="5836a-175">Restricción de la fase de Word admite dos tipos de coincidencia: coincidencia de prefijo o coincidencia exacta.</span><span class="sxs-lookup"><span data-stu-id="5836a-175">Word phase restriction supports two match types: prefix match or exact match.</span></span> <span data-ttu-id="5836a-176">Coincidencia de prefijo es el comportamiento predeterminado de coincidencia.</span><span class="sxs-lookup"><span data-stu-id="5836a-176">Prefix match is the default match behavior.</span></span> <span data-ttu-id="5836a-177">Si desea que la coincidencia exacta, utilice comillas dobles.</span><span class="sxs-lookup"><span data-stu-id="5836a-177">If you want exact match, use double quotes.</span></span> <span data-ttu-id="5836a-178">Por ejemplo, subject: "product" coincide con 'producto' pero no 'producción' en el asunto.</span><span class="sxs-lookup"><span data-stu-id="5836a-178">For example, subject:"product" matches 'product' but not 'production' in the subject.</span></span> <span data-ttu-id="5836a-179">Varias palabras dobles restringen las fases de word y su orden.</span><span class="sxs-lookup"><span data-stu-id="5836a-179">Multiple words in double quotes restrict both word phases and their order.</span></span> <span data-ttu-id="5836a-180">Por ejemplo "win del producto" coincide con sólo 'win del producto', no 'producto Windows 95' o 'producto de win'.</span><span class="sxs-lookup"><span data-stu-id="5836a-180">For example "win product" matches only 'win product', not 'win95 product' or 'product of win'.</span></span> <span data-ttu-id="5836a-181">Puede usar un asterisco (\*) para definir una coincidencia de prefijo con orden restringido.</span><span class="sxs-lookup"><span data-stu-id="5836a-181">You can use an asterisk (\*) to define a prefix match with order restricted.</span></span> <span data-ttu-id="5836a-182">Por ejemplo, "win del producto"\* coincide con 'producto Windows 95', 'línea de producción de windows' pero no 'nuevo producto de windows' o 'producto de win'.</span><span class="sxs-lookup"><span data-stu-id="5836a-182">For example, "win product"\* matches 'win95 product', 'windows production line' but not 'windows new product' or 'product of win'.</span></span> <span data-ttu-id="5836a-183">Puede buscar todos los mensajes enviados desde o a un dominio.</span><span class="sxs-lookup"><span data-stu-id="5836a-183">You can search all messages sent from or to a domain.</span></span> <span data-ttu-id="5836a-184">Por ejemplo, from:"@hotmail.com" devuelve todos los mensajes enviados desde hotmail.com.</span><span class="sxs-lookup"><span data-stu-id="5836a-184">For example, from:"@hotmail.com" returns all messages sent from hotmail.com.</span></span>
  
<span data-ttu-id="5836a-185">En la siguiente tabla se describe las restricciones de intervalo de fecha.</span><span class="sxs-lookup"><span data-stu-id="5836a-185">The following table describes date range restrictions.</span></span>
  
<span data-ttu-id="5836a-186">**Restricción de intervalo de fecha**</span><span class="sxs-lookup"><span data-stu-id="5836a-186">**Date range restriction**</span></span>

|<span data-ttu-id="5836a-187">**Propiedad**</span><span class="sxs-lookup"><span data-stu-id="5836a-187">**Property**</span></span>|<span data-ttu-id="5836a-188">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="5836a-188">**Example**</span></span>|<span data-ttu-id="5836a-189">**Funci�n**</span><span class="sxs-lookup"><span data-stu-id="5836a-189">**Function**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="5836a-190">Enviado</span><span class="sxs-lookup"><span data-stu-id="5836a-190">Sent</span></span>  <br/> |<span data-ttu-id="5836a-191">Enviado: última semana</span><span class="sxs-lookup"><span data-stu-id="5836a-191">Sent:last week</span></span>  <br/> <span data-ttu-id="5836a-192">Enviado: 01/01/2001</span><span class="sxs-lookup"><span data-stu-id="5836a-192">Sent:01/01/2001</span></span>  <br/> <span data-ttu-id="5836a-193">Sent:01/01/2001..01/15/2001</span><span class="sxs-lookup"><span data-stu-id="5836a-193">Sent:01/01/2001..01/15/2001</span></span>  <br/> |<span data-ttu-id="5836a-194">Buscar artículos envían última semana.</span><span class="sxs-lookup"><span data-stu-id="5836a-194">Search items sent last week.</span></span>  <br/> <span data-ttu-id="5836a-195">Buscar elementos enviados en 1 de enero de 2001.</span><span class="sxs-lookup"><span data-stu-id="5836a-195">Search items sent on January 1st, 2001.</span></span>  <br/> <span data-ttu-id="5836a-196">Buscar artículos enviados entre el 1 de enero de 2001 y el 15 de enero de 2001.</span><span class="sxs-lookup"><span data-stu-id="5836a-196">Search items sent between January 1st, 2001 and January 15th, 2001.</span></span>  <br/> |
|<span data-ttu-id="5836a-197">Cantidad.Recibida</span><span class="sxs-lookup"><span data-stu-id="5836a-197">Received</span></span>  <br/> |<span data-ttu-id="5836a-198">Recibido: hoy mismo</span><span class="sxs-lookup"><span data-stu-id="5836a-198">Received:today</span></span>  <br/> <span data-ttu-id="5836a-199">Recibido: 01/01/2001</span><span class="sxs-lookup"><span data-stu-id="5836a-199">Received:01/01/2001</span></span>  <br/> |<span data-ttu-id="5836a-200">Buscar elementos recibidos hoy.</span><span class="sxs-lookup"><span data-stu-id="5836a-200">Search items received today.</span></span>  <br/> <span data-ttu-id="5836a-201">Buscar elementos recibidos en 1 de enero de 2001.</span><span class="sxs-lookup"><span data-stu-id="5836a-201">Search items received on January 1st, 2001.</span></span>  <br/> |
   
<span data-ttu-id="5836a-202">Los dos puntos (.) es un operador de rango.</span><span class="sxs-lookup"><span data-stu-id="5836a-202">The two dots (..) is a range operator.</span></span> <span data-ttu-id="5836a-203">Se puede usar para definir un intervalo con un inicio y una fecha de finalización.</span><span class="sxs-lookup"><span data-stu-id="5836a-203">It can be used to define a range with a start and an end date.</span></span> <span data-ttu-id="5836a-204">Para especificar una fecha, puede usar fechas relativas.</span><span class="sxs-lookup"><span data-stu-id="5836a-204">To specify a date, you can use relative dates.</span></span> <span data-ttu-id="5836a-205">Se admiten las fechas relativas siguientes:</span><span class="sxs-lookup"><span data-stu-id="5836a-205">The following relative dates are supported:</span></span>
  
- <span data-ttu-id="5836a-206">Fechas relativas: hoy, mañana, ayer</span><span class="sxs-lookup"><span data-stu-id="5836a-206">Relative dates: Today, tomorrow, yesterday</span></span>
    
- <span data-ttu-id="5836a-207">Fechas relativas varias palabras: esta semana, mes siguiente, la última semana, más allá de mes o año siguiente</span><span class="sxs-lookup"><span data-stu-id="5836a-207">Multiword relative dates: This week, next month, last week, past month, or coming year</span></span>
    
- <span data-ttu-id="5836a-208">Días: Domingo, el lunes, el martes, el miércoles, el jueves, el viernes, sábado</span><span class="sxs-lookup"><span data-stu-id="5836a-208">Days: Sunday, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday</span></span>
    
- <span data-ttu-id="5836a-209">Enero, febrero, marzo, abril, mayo, junio, julio, agosto, septiembre, octubre, noviembre, diciembre</span><span class="sxs-lookup"><span data-stu-id="5836a-209">January, February, March, April, May, June, July, August, September, October, November, December</span></span>
    
<span data-ttu-id="5836a-210">En la siguiente tabla se describe las restricciones de tipo de mensaje.</span><span class="sxs-lookup"><span data-stu-id="5836a-210">The following table describes message type restrictions.</span></span> 
  
<span data-ttu-id="5836a-211">**Restricción del tipo de mensaje**</span><span class="sxs-lookup"><span data-stu-id="5836a-211">**Message type restriction**</span></span>

|<span data-ttu-id="5836a-212">**Propiedad**</span><span class="sxs-lookup"><span data-stu-id="5836a-212">**Property**</span></span>|<span data-ttu-id="5836a-213">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="5836a-213">**Example**</span></span>|<span data-ttu-id="5836a-214">**Funci�n**</span><span class="sxs-lookup"><span data-stu-id="5836a-214">**Function**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="5836a-215">Tipo</span><span class="sxs-lookup"><span data-stu-id="5836a-215">Kind</span></span>  <br/> |<span data-ttu-id="5836a-216">Tipo: tareas</span><span class="sxs-lookup"><span data-stu-id="5836a-216">Kind:tasks</span></span>  <br/> |<span data-ttu-id="5836a-217">Buscar todos los elementos de tarea.</span><span class="sxs-lookup"><span data-stu-id="5836a-217">Search all task items.</span></span>  <br/> |
   
<span data-ttu-id="5836a-218">AQS en EWS usa la propiedad **Kind** para especificar el tipo de mensaje.</span><span class="sxs-lookup"><span data-stu-id="5836a-218">AQS in EWS uses the **Kind** property to specify the message type.</span></span> <span data-ttu-id="5836a-219">La propiedad Kind se puede usar con los siguientes tipos de elemento:</span><span class="sxs-lookup"><span data-stu-id="5836a-219">The Kind property can be used with the following item types:</span></span> 
  
- <span data-ttu-id="5836a-220">email</span><span class="sxs-lookup"><span data-stu-id="5836a-220">email</span></span>
    
- <span data-ttu-id="5836a-221">reuniones</span><span class="sxs-lookup"><span data-stu-id="5836a-221">meetings</span></span>
    
- <span data-ttu-id="5836a-222">tasks</span><span class="sxs-lookup"><span data-stu-id="5836a-222">tasks</span></span>
    
- <span data-ttu-id="5836a-223">notas</span><span class="sxs-lookup"><span data-stu-id="5836a-223">notes</span></span>
    
- <span data-ttu-id="5836a-224">documentos</span><span class="sxs-lookup"><span data-stu-id="5836a-224">docs</span></span>
    
- <span data-ttu-id="5836a-225">diarios</span><span class="sxs-lookup"><span data-stu-id="5836a-225">journals</span></span>
    
- <span data-ttu-id="5836a-226">contactos</span><span class="sxs-lookup"><span data-stu-id="5836a-226">contacts</span></span>
    
- <span data-ttu-id="5836a-227">mensajería instantánea</span><span class="sxs-lookup"><span data-stu-id="5836a-227">im</span></span>
    
<span data-ttu-id="5836a-228">En la siguiente tabla se describe los conectores de la lógicos de agrupación.</span><span class="sxs-lookup"><span data-stu-id="5836a-228">The following table describes grouping logical connectors.</span></span>
  
<span data-ttu-id="5836a-229">**Conectores de agrupación lógicos**</span><span class="sxs-lookup"><span data-stu-id="5836a-229">**Grouping logical connectors**</span></span>

|<span data-ttu-id="5836a-230">**Connector**</span><span class="sxs-lookup"><span data-stu-id="5836a-230">**Connector**</span></span>|<span data-ttu-id="5836a-231">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="5836a-231">**Example**</span></span>|<span data-ttu-id="5836a-232">**Funci�n**</span><span class="sxs-lookup"><span data-stu-id="5836a-232">**Function**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="5836a-233">AND</span><span class="sxs-lookup"><span data-stu-id="5836a-233">AND</span></span>  <br/> |<span data-ttu-id="5836a-234">Asunto: producto y asunto: desarrollo</span><span class="sxs-lookup"><span data-stu-id="5836a-234">Subject:product AND subject:development</span></span>  <br/> <span data-ttu-id="5836a-235">Asunto:(product AND development)</span><span class="sxs-lookup"><span data-stu-id="5836a-235">Subject:(product AND development)</span></span>  <br/> <span data-ttu-id="5836a-236">Asunto:(product development)</span><span class="sxs-lookup"><span data-stu-id="5836a-236">Subject:(product development)</span></span>  <br/> |<span data-ttu-id="5836a-237">Buscar elementos con productos y desarrollo en el asunto.</span><span class="sxs-lookup"><span data-stu-id="5836a-237">Search items with both product and development in the subject.</span></span>  <br/> |
|<span data-ttu-id="5836a-238">O</span><span class="sxs-lookup"><span data-stu-id="5836a-238">OR</span></span>  <br/> |<span data-ttu-id="5836a-239">Cuerpo: proyecto o cuerpo: propuesta</span><span class="sxs-lookup"><span data-stu-id="5836a-239">Body:project OR body:proposal</span></span>  <br/> <span data-ttu-id="5836a-240">Cuerpo de:(project OR proposal)</span><span class="sxs-lookup"><span data-stu-id="5836a-240">Body:(project OR proposal)</span></span>  <br/> |<span data-ttu-id="5836a-241">Buscar elementos con el producto o desarrollo en el cuerpo.</span><span class="sxs-lookup"><span data-stu-id="5836a-241">Search items with either product or development in the body.</span></span>  <br/> |
|<span data-ttu-id="5836a-242">NOT</span><span class="sxs-lookup"><span data-stu-id="5836a-242">NOT</span></span>  <br/> |<span data-ttu-id="5836a-243">NO: propuesta de cuerpo</span><span class="sxs-lookup"><span data-stu-id="5836a-243">NOT body:proposal</span></span>  <br/> <span data-ttu-id="5836a-244">Cuerpo:(NOT proposal)</span><span class="sxs-lookup"><span data-stu-id="5836a-244">Body:(NOT proposal)</span></span>  <br/> |<span data-ttu-id="5836a-245">Buscar mensajes sin propuesta en el cuerpo.</span><span class="sxs-lookup"><span data-stu-id="5836a-245">Search messages without proposal in the body.</span></span>  <br/> |
   
<span data-ttu-id="5836a-246">Y siempre es el conector de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="5836a-246">AND is always the default connector.</span></span> <span data-ttu-id="5836a-247">Por ejemplo, asunto: project AND cuerpo: propuesta es el mismo que el cuerpo: propuesta de asunto: proyecto.</span><span class="sxs-lookup"><span data-stu-id="5836a-247">For example, subject:project AND body:proposal is the same as subject:project body:proposal.</span></span> <span data-ttu-id="5836a-248">Conectores lógicos distinguen mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="5836a-248">Logical connectors are case sensitive.</span></span> <span data-ttu-id="5836a-249">Por ejemplo, body:(project Or proposal) busca los mensajes con 'proyecto', 'o' y 'propuesta' en el cuerpo en lugar de 'proyecto' o 'propuesta'.</span><span class="sxs-lookup"><span data-stu-id="5836a-249">For example, body:(project Or proposal) searches messages with 'project', 'or', and 'proposal' in the body instead of 'project' or 'proposal'.</span></span> <span data-ttu-id="5836a-250">El signo más (+) es equivalente a and.</span><span class="sxs-lookup"><span data-stu-id="5836a-250">The plus symbol (+) is equivalent to AND.</span></span> <span data-ttu-id="5836a-251">El símbolo de guión (-) es equivalente a NOT.</span><span class="sxs-lookup"><span data-stu-id="5836a-251">The hyphen symbol (-) is equivalent to NOT.</span></span> <span data-ttu-id="5836a-252">Por ejemplo, body:(project-proposal) busca mensajes con 'project' pero sin 'propuesta' en el cuerpo.</span><span class="sxs-lookup"><span data-stu-id="5836a-252">For example, body:(project - proposal) searches messages with 'project' but without 'proposal' in the body.</span></span> 
  
<span data-ttu-id="5836a-253">La cadena de consulta también puede contener propiedades no indizadas para la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="5836a-253">The query string can also contain nonindexed properties for search.</span></span> <span data-ttu-id="5836a-254">Si la cadena de consulta contiene propiedades no indizadas, la búsqueda puede realizar una búsqueda de Exchange en las propiedades indizadas y una búsqueda de almacenamiento en las propiedades no indizadas.</span><span class="sxs-lookup"><span data-stu-id="5836a-254">If the query string contains nonindexed properties, the search might perform an Exchange search on the indexed properties and a store search on the nonindexed properties.</span></span> 
  
<span data-ttu-id="5836a-255">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="5836a-255">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="example"></a><span data-ttu-id="5836a-256">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5836a-256">Example</span></span>

<span data-ttu-id="5836a-257">En el ejemplo siguiente se muestra una solicitud para buscar mensajes en la Bandeja de entrada con detección automática en el asunto.</span><span class="sxs-lookup"><span data-stu-id="5836a-257">The following example shows a request to search for messages in the Inbox with Autodiscover in the subject.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
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

<span data-ttu-id="5836a-258">En el ejemplo siguiente se muestra una respuesta correcta a la solicitud.</span><span class="sxs-lookup"><span data-stu-id="5836a-258">The following example shows a successful response to the request.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="14" 
                         MinorVersion="0" 
                         MajorBuildNumber="639" 
                         MinorBuildNumber="20" 
                         Version="Exchange2010" 
                         xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:FindItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
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

## <a name="element-information"></a><span data-ttu-id="5836a-259">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="5836a-259">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5836a-260">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="5836a-260">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="5836a-261">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="5836a-261">Schema name</span></span>  <br/> |<span data-ttu-id="5836a-262">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="5836a-262">Messages schema</span></span>  <br/> |
|<span data-ttu-id="5836a-263">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="5836a-263">Validation file</span></span>  <br/> |<span data-ttu-id="5836a-264">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="5836a-264">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="5836a-265">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="5836a-265">Can be empty</span></span>  <br/> |<span data-ttu-id="5836a-266">False</span><span class="sxs-lookup"><span data-stu-id="5836a-266">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5836a-267">Ver también</span><span class="sxs-lookup"><span data-stu-id="5836a-267">See also</span></span>



[<span data-ttu-id="5836a-268">Operación FindItem</span><span class="sxs-lookup"><span data-stu-id="5836a-268">FindItem operation</span></span>](finditem-operation.md)
  
[<span data-ttu-id="5836a-269">Operación de FindConversation</span><span class="sxs-lookup"><span data-stu-id="5836a-269">FindConversation operation</span></span>](findconversation-operation.md)


- [<span data-ttu-id="5836a-270">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="5836a-270">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

