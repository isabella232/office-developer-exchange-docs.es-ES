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
description: El elemento contiene representa una expresión de búsqueda que determina si una propiedad determinada contiene el valor de cadena constante proporcionada.
ms.openlocfilehash: 083efdf32cd32bea6964361b5b558480aa937280
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763816"
---
# <a name="contains"></a><span data-ttu-id="9181d-103">Contains</span><span class="sxs-lookup"><span data-stu-id="9181d-103">Contains</span></span>

<span data-ttu-id="9181d-104">El elemento **contiene** representa una expresión de búsqueda que determina si una propiedad determinada contiene el valor de cadena constante proporcionada.</span><span class="sxs-lookup"><span data-stu-id="9181d-104">The **Contains** element represents a search expression that determines whether a given property contains the supplied constant string value.</span></span> 
  
```xml
<Contains ContainmentMode="" ContainmentComparison="">
   <FieldURI/>
   <Constant/>
</Contains>
```

 <span data-ttu-id="9181d-105">**ContainsExpressionType**</span><span class="sxs-lookup"><span data-stu-id="9181d-105">**ContainsExpressionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9181d-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="9181d-106">Attributes and elements</span></span>

<span data-ttu-id="9181d-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="9181d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9181d-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="9181d-108">Attributes</span></span>

|<span data-ttu-id="9181d-109">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="9181d-109">**Attribute**</span></span>|<span data-ttu-id="9181d-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9181d-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9181d-111">**ContainmentMode**</span><span class="sxs-lookup"><span data-stu-id="9181d-111">**ContainmentMode**</span></span> <br/> |<span data-ttu-id="9181d-112">Identifica los límites de una búsqueda.</span><span class="sxs-lookup"><span data-stu-id="9181d-112">Identifies the boundaries of a search.</span></span>  <br/> |
|<span data-ttu-id="9181d-113">**ContainmentComparison**</span><span class="sxs-lookup"><span data-stu-id="9181d-113">**ContainmentComparison**</span></span> <br/> |<span data-ttu-id="9181d-114">Determina si la búsqueda omite los casos y espacios.</span><span class="sxs-lookup"><span data-stu-id="9181d-114">Determines whether the search ignores cases and spaces.</span></span>  <br/> |
   
#### <a name="containmentmode-attribute-values"></a><span data-ttu-id="9181d-115">Valores de atributo de ContainmentMode</span><span class="sxs-lookup"><span data-stu-id="9181d-115">ContainmentMode attribute values</span></span>

|<span data-ttu-id="9181d-116">**Valor**</span><span class="sxs-lookup"><span data-stu-id="9181d-116">**Value**</span></span>|<span data-ttu-id="9181d-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9181d-117">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9181d-118">FullString</span><span class="sxs-lookup"><span data-stu-id="9181d-118">FullString</span></span>  <br/> |<span data-ttu-id="9181d-119">Es la comparación entre la cadena completa y la constante.</span><span class="sxs-lookup"><span data-stu-id="9181d-119">The comparison is between the full string and the constant.</span></span> <span data-ttu-id="9181d-120">El valor de la propiedad y la constante suministrada están exactamente el mismo.</span><span class="sxs-lookup"><span data-stu-id="9181d-120">The property value and the supplied constant are precisely the same.</span></span>  <br/> |
|<span data-ttu-id="9181d-121">El prefijo</span><span class="sxs-lookup"><span data-stu-id="9181d-121">Prefixed</span></span>  <br/> |<span data-ttu-id="9181d-122">La comparación es entre el prefijo de la cadena y la constante.</span><span class="sxs-lookup"><span data-stu-id="9181d-122">The comparison is between the string prefix and the constant.</span></span>  <br/> |
|<span data-ttu-id="9181d-123">Subcadena</span><span class="sxs-lookup"><span data-stu-id="9181d-123">Substring</span></span>  <br/> |<span data-ttu-id="9181d-124">La comparación es entre una subcadena de la cadena y la constante.</span><span class="sxs-lookup"><span data-stu-id="9181d-124">The comparison is between a substring of the string and the constant.</span></span>  <br/> |
|<span data-ttu-id="9181d-125">PrefixOnWords</span><span class="sxs-lookup"><span data-stu-id="9181d-125">PrefixOnWords</span></span>  <br/> |<span data-ttu-id="9181d-126">La comparación es entre un prefijo en palabras individuales en la cadena y la constante.</span><span class="sxs-lookup"><span data-stu-id="9181d-126">The comparison is between a prefix on individual words in the string and the constant.</span></span>  <br/> |
|<span data-ttu-id="9181d-127">ExactPhrase</span><span class="sxs-lookup"><span data-stu-id="9181d-127">ExactPhrase</span></span>  <br/> |<span data-ttu-id="9181d-128">La comparación es entre una frase exacta en la cadena y la constante.</span><span class="sxs-lookup"><span data-stu-id="9181d-128">The comparison is between an exact phrase in the string and the constant.</span></span>  <br/> |
   
#### <a name="containmentcomparison-attribute-values"></a><span data-ttu-id="9181d-129">Valores de atributo de ContainmentComparison</span><span class="sxs-lookup"><span data-stu-id="9181d-129">ContainmentComparison attribute values</span></span>

|<span data-ttu-id="9181d-130">**Valor**</span><span class="sxs-lookup"><span data-stu-id="9181d-130">**Value**</span></span>|<span data-ttu-id="9181d-131">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9181d-131">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9181d-132">Exact</span><span class="sxs-lookup"><span data-stu-id="9181d-132">Exact</span></span>  <br/> |<span data-ttu-id="9181d-133">La comparación debe ser exacta.</span><span class="sxs-lookup"><span data-stu-id="9181d-133">The comparison must be exact.</span></span>  <br/> |
|<span data-ttu-id="9181d-134">IgnoreCase</span><span class="sxs-lookup"><span data-stu-id="9181d-134">IgnoreCase</span></span>  <br/> |<span data-ttu-id="9181d-135">La comparación pasa por alto las mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="9181d-135">The comparison ignores casing.</span></span>  <br/> |
|<span data-ttu-id="9181d-136">IgnoreNonSpacingCharacters</span><span class="sxs-lookup"><span data-stu-id="9181d-136">IgnoreNonSpacingCharacters</span></span>  <br/> |<span data-ttu-id="9181d-137">La comparación pasa por alto caracteres sin espacios.</span><span class="sxs-lookup"><span data-stu-id="9181d-137">The comparison ignores non-spacing characters.</span></span>  <br/> |
|<span data-ttu-id="9181d-138">Separada</span><span class="sxs-lookup"><span data-stu-id="9181d-138">Loose</span></span>  <br/> |<span data-ttu-id="9181d-139">Va a quitar.</span><span class="sxs-lookup"><span data-stu-id="9181d-139">To be removed.</span></span>  <br/> |
|<span data-ttu-id="9181d-140">IgnoreCaseAndNonSpacingCharacters</span><span class="sxs-lookup"><span data-stu-id="9181d-140">IgnoreCaseAndNonSpacingCharacters</span></span>  <br/> |<span data-ttu-id="9181d-141">La comparación omite mayúsculas y que no sean de espaciado entre caracteres.</span><span class="sxs-lookup"><span data-stu-id="9181d-141">The comparison ignores casing and non-spacing characters.</span></span>  <br/> |
|<span data-ttu-id="9181d-142">LooseAndIgnoreCase</span><span class="sxs-lookup"><span data-stu-id="9181d-142">LooseAndIgnoreCase</span></span>  <br/> |<span data-ttu-id="9181d-143">Va a quitar.</span><span class="sxs-lookup"><span data-stu-id="9181d-143">To be removed.</span></span>  <br/> |
|<span data-ttu-id="9181d-144">LooseAndIgnoreNonSpace</span><span class="sxs-lookup"><span data-stu-id="9181d-144">LooseAndIgnoreNonSpace</span></span>  <br/> |<span data-ttu-id="9181d-145">Va a quitar.</span><span class="sxs-lookup"><span data-stu-id="9181d-145">To be removed.</span></span>  <br/> |
|<span data-ttu-id="9181d-146">LooseAndIgnoreCaseAndIgnoreNonSpace</span><span class="sxs-lookup"><span data-stu-id="9181d-146">LooseAndIgnoreCaseAndIgnoreNonSpace</span></span>  <br/> |<span data-ttu-id="9181d-147">Va a quitar.</span><span class="sxs-lookup"><span data-stu-id="9181d-147">To be removed.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="9181d-148">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="9181d-148">Child elements</span></span>

|<span data-ttu-id="9181d-149">**Element**</span><span class="sxs-lookup"><span data-stu-id="9181d-149">**Element**</span></span>|<span data-ttu-id="9181d-150">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9181d-150">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9181d-151">FieldURI</span><span class="sxs-lookup"><span data-stu-id="9181d-151">FieldURI</span></span>](fielduri.md) <br/> |<span data-ttu-id="9181d-152">Identifica las propiedades con frecuencia que se hace referencia mediante un identificador URI.</span><span class="sxs-lookup"><span data-stu-id="9181d-152">Identifies frequently referenced properties by URI.</span></span>  <br/> |
|[<span data-ttu-id="9181d-153">IndexedFieldURI</span><span class="sxs-lookup"><span data-stu-id="9181d-153">IndexedFieldURI</span></span>](indexedfielduri.md) <br/> |<span data-ttu-id="9181d-154">Identifica a los miembros individuales de un diccionario.</span><span class="sxs-lookup"><span data-stu-id="9181d-154">Identifies individual members of a dictionary.</span></span>  <br/> |
|[<span data-ttu-id="9181d-155">ExtendedFieldURI</span><span class="sxs-lookup"><span data-stu-id="9181d-155">ExtendedFieldURI</span></span>](extendedfielduri.md) <br/> |<span data-ttu-id="9181d-156">Identifica las propiedades MAPI.</span><span class="sxs-lookup"><span data-stu-id="9181d-156">Identifies MAPI properties.</span></span>  <br/> |
|[<span data-ttu-id="9181d-157">Constante</span><span class="sxs-lookup"><span data-stu-id="9181d-157">Constant</span></span>](constant.md) <br/> |<span data-ttu-id="9181d-158">Identifica un valor constante en una restricción.</span><span class="sxs-lookup"><span data-stu-id="9181d-158">Identifies a constant value in a restriction.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="9181d-159">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="9181d-159">Parent elements</span></span>

|<span data-ttu-id="9181d-160">**Element**</span><span class="sxs-lookup"><span data-stu-id="9181d-160">**Element**</span></span>|<span data-ttu-id="9181d-161">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9181d-161">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9181d-162">Restriction</span><span class="sxs-lookup"><span data-stu-id="9181d-162">Restriction</span></span>](restriction.md) <br/> |<span data-ttu-id="9181d-163">Representa la restricción o la consulta que se usa para filtrar los elementos o carpetas en las operaciones de carpeta FindItem/FindFolder y búsqueda.</span><span class="sxs-lookup"><span data-stu-id="9181d-163">Represents the restriction or query that is used to filter items or folders in FindItem/FindFolder and search folder operations.</span></span>  <br/> |
|[<span data-ttu-id="9181d-164">No</span><span class="sxs-lookup"><span data-stu-id="9181d-164">Not</span></span>](not.md) <br/> |<span data-ttu-id="9181d-165">Representa una expresión de búsqueda que niega el valor booleano de la expresión de búsqueda que contiene.</span><span class="sxs-lookup"><span data-stu-id="9181d-165">Represents a search expression that negates the Boolean value of the search expression it contains.</span></span>  <br/> |
|[<span data-ttu-id="9181d-166">And</span><span class="sxs-lookup"><span data-stu-id="9181d-166">And</span></span>](and.md) <br/> |<span data-ttu-id="9181d-167">Representa una expresión de búsqueda que le permite realizar una operación de tipo Boolean y entre dos o más expresiones de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="9181d-167">Represents a search expression that allows you to perform a Boolean And operation between two or more search expressions.</span></span> <span data-ttu-id="9181d-168">El resultado de la operación And es **true** si se **cumplen**todas las expresiones de búsqueda incluidas en el y.</span><span class="sxs-lookup"><span data-stu-id="9181d-168">The result of the And operation is **true** if all of the search expressions contained within the And are **true**.</span></span>  <br/> |
|[<span data-ttu-id="9181d-169">Or</span><span class="sxs-lookup"><span data-stu-id="9181d-169">Or</span></span>](or.md) <br/> |<span data-ttu-id="9181d-170">Representa una expresión de búsqueda que se realiza una operación OR lógica en la expresión de búsqueda que contiene.</span><span class="sxs-lookup"><span data-stu-id="9181d-170">Represents a search expression that performs a logical OR on the search expression it contains.</span></span> <span data-ttu-id="9181d-171">El elemento [o](or.md) devolverá **true** si cualquiera de sus elementos secundarios que devuelva **true**.</span><span class="sxs-lookup"><span data-stu-id="9181d-171">The [Or](or.md) element will return **true** if any of its children return **true**.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9181d-172">Notas</span><span class="sxs-lookup"><span data-stu-id="9181d-172">Remarks</span></span>

<span data-ttu-id="9181d-173">Los atributos se utilizan para determinar cómo se comparan los elementos.</span><span class="sxs-lookup"><span data-stu-id="9181d-173">The attributes are used to determine how the elements are matched.</span></span>
  
<span data-ttu-id="9181d-174">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="9181d-174">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9181d-175">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="9181d-175">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9181d-176">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="9181d-176">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="9181d-177">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="9181d-177">Schema Name</span></span>  <br/> |<span data-ttu-id="9181d-178">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="9181d-178">Types schema</span></span>  <br/> |
|<span data-ttu-id="9181d-179">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="9181d-179">Validation File</span></span>  <br/> |<span data-ttu-id="9181d-180">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="9181d-180">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="9181d-181">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="9181d-181">Can be Empty</span></span>  <br/> |<span data-ttu-id="9181d-182">False</span><span class="sxs-lookup"><span data-stu-id="9181d-182">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9181d-183">Ver también</span><span class="sxs-lookup"><span data-stu-id="9181d-183">See also</span></span>



- [<span data-ttu-id="9181d-184">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="9181d-184">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

