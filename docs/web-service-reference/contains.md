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
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763816"
---
# <a name="contains"></a><span data-ttu-id="2b332-103">Contains</span><span class="sxs-lookup"><span data-stu-id="2b332-103">Contains</span></span>

<span data-ttu-id="2b332-104">El elemento **contiene** representa una expresión de búsqueda que determina si una propiedad determinada contiene el valor de cadena constante proporcionada.</span><span class="sxs-lookup"><span data-stu-id="2b332-104">The **Contains** element represents a search expression that determines whether a given property contains the supplied constant string value.</span></span> 
  
```xml
<Contains ContainmentMode="" ContainmentComparison="">
   <FieldURI/>
   <Constant/>
</Contains>
```

 <span data-ttu-id="2b332-105">**ContainsExpressionType**</span><span class="sxs-lookup"><span data-stu-id="2b332-105">**ContainsExpressionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2b332-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="2b332-106">Attributes and elements</span></span>

<span data-ttu-id="2b332-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="2b332-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2b332-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="2b332-108">Attributes</span></span>

|<span data-ttu-id="2b332-109">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="2b332-109">**Attribute**</span></span>|<span data-ttu-id="2b332-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2b332-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2b332-111">**ContainmentMode**</span><span class="sxs-lookup"><span data-stu-id="2b332-111">**ContainmentMode**</span></span> <br/> |<span data-ttu-id="2b332-112">Identifica los límites de una búsqueda.</span><span class="sxs-lookup"><span data-stu-id="2b332-112">Identifies the boundaries of a search.</span></span>  <br/> |
|<span data-ttu-id="2b332-113">**ContainmentComparison**</span><span class="sxs-lookup"><span data-stu-id="2b332-113">**ContainmentComparison**</span></span> <br/> |<span data-ttu-id="2b332-114">Determina si la búsqueda omite los casos y espacios.</span><span class="sxs-lookup"><span data-stu-id="2b332-114">Determines whether the search ignores cases and spaces.</span></span>  <br/> |
   
#### <a name="containmentmode-attribute-values"></a><span data-ttu-id="2b332-115">Valores de atributo de ContainmentMode</span><span class="sxs-lookup"><span data-stu-id="2b332-115">ContainmentMode attribute values</span></span>

|<span data-ttu-id="2b332-116">**Valor**</span><span class="sxs-lookup"><span data-stu-id="2b332-116">**Value**</span></span>|<span data-ttu-id="2b332-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2b332-117">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2b332-118">FullString</span><span class="sxs-lookup"><span data-stu-id="2b332-118">FullString</span></span>  <br/> |<span data-ttu-id="2b332-119">Es la comparación entre la cadena completa y la constante.</span><span class="sxs-lookup"><span data-stu-id="2b332-119">The comparison is between the full string and the constant.</span></span> <span data-ttu-id="2b332-120">El valor de la propiedad y la constante suministrada están exactamente el mismo.</span><span class="sxs-lookup"><span data-stu-id="2b332-120">The property value and the supplied constant are precisely the same.</span></span>  <br/> |
|<span data-ttu-id="2b332-121">El prefijo</span><span class="sxs-lookup"><span data-stu-id="2b332-121">Prefixed</span></span>  <br/> |<span data-ttu-id="2b332-122">La comparación es entre el prefijo de la cadena y la constante.</span><span class="sxs-lookup"><span data-stu-id="2b332-122">The comparison is between the string prefix and the constant.</span></span>  <br/> |
|<span data-ttu-id="2b332-123">Subcadena</span><span class="sxs-lookup"><span data-stu-id="2b332-123">Substring</span></span>  <br/> |<span data-ttu-id="2b332-124">La comparación es entre una subcadena de la cadena y la constante.</span><span class="sxs-lookup"><span data-stu-id="2b332-124">The comparison is between a substring of the string and the constant.</span></span>  <br/> |
|<span data-ttu-id="2b332-125">PrefixOnWords</span><span class="sxs-lookup"><span data-stu-id="2b332-125">PrefixOnWords</span></span>  <br/> |<span data-ttu-id="2b332-126">La comparación es entre un prefijo en palabras individuales en la cadena y la constante.</span><span class="sxs-lookup"><span data-stu-id="2b332-126">The comparison is between a prefix on individual words in the string and the constant.</span></span>  <br/> |
|<span data-ttu-id="2b332-127">ExactPhrase</span><span class="sxs-lookup"><span data-stu-id="2b332-127">ExactPhrase</span></span>  <br/> |<span data-ttu-id="2b332-128">La comparación es entre una frase exacta en la cadena y la constante.</span><span class="sxs-lookup"><span data-stu-id="2b332-128">The comparison is between an exact phrase in the string and the constant.</span></span>  <br/> |
   
#### <a name="containmentcomparison-attribute-values"></a><span data-ttu-id="2b332-129">Valores de atributo de ContainmentComparison</span><span class="sxs-lookup"><span data-stu-id="2b332-129">ContainmentComparison attribute values</span></span>

|<span data-ttu-id="2b332-130">**Valor**</span><span class="sxs-lookup"><span data-stu-id="2b332-130">**Value**</span></span>|<span data-ttu-id="2b332-131">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2b332-131">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2b332-132">Exact</span><span class="sxs-lookup"><span data-stu-id="2b332-132">Exact</span></span>  <br/> |<span data-ttu-id="2b332-133">La comparación debe ser exacta.</span><span class="sxs-lookup"><span data-stu-id="2b332-133">The comparison must be exact.</span></span>  <br/> |
|<span data-ttu-id="2b332-134">IgnoreCase</span><span class="sxs-lookup"><span data-stu-id="2b332-134">IgnoreCase</span></span>  <br/> |<span data-ttu-id="2b332-135">La comparación pasa por alto las mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="2b332-135">The comparison ignores casing.</span></span>  <br/> |
|<span data-ttu-id="2b332-136">IgnoreNonSpacingCharacters</span><span class="sxs-lookup"><span data-stu-id="2b332-136">IgnoreNonSpacingCharacters</span></span>  <br/> |<span data-ttu-id="2b332-137">La comparación pasa por alto caracteres sin espacios.</span><span class="sxs-lookup"><span data-stu-id="2b332-137">The comparison ignores non-spacing characters.</span></span>  <br/> |
|<span data-ttu-id="2b332-138">Separada</span><span class="sxs-lookup"><span data-stu-id="2b332-138">Loose</span></span>  <br/> |<span data-ttu-id="2b332-139">Va a quitar.</span><span class="sxs-lookup"><span data-stu-id="2b332-139">To be removed.</span></span>  <br/> |
|<span data-ttu-id="2b332-140">IgnoreCaseAndNonSpacingCharacters</span><span class="sxs-lookup"><span data-stu-id="2b332-140">IgnoreCaseAndNonSpacingCharacters</span></span>  <br/> |<span data-ttu-id="2b332-141">La comparación omite mayúsculas y que no sean de espaciado entre caracteres.</span><span class="sxs-lookup"><span data-stu-id="2b332-141">The comparison ignores casing and non-spacing characters.</span></span>  <br/> |
|<span data-ttu-id="2b332-142">LooseAndIgnoreCase</span><span class="sxs-lookup"><span data-stu-id="2b332-142">LooseAndIgnoreCase</span></span>  <br/> |<span data-ttu-id="2b332-143">Va a quitar.</span><span class="sxs-lookup"><span data-stu-id="2b332-143">To be removed.</span></span>  <br/> |
|<span data-ttu-id="2b332-144">LooseAndIgnoreNonSpace</span><span class="sxs-lookup"><span data-stu-id="2b332-144">LooseAndIgnoreNonSpace</span></span>  <br/> |<span data-ttu-id="2b332-145">Va a quitar.</span><span class="sxs-lookup"><span data-stu-id="2b332-145">To be removed.</span></span>  <br/> |
|<span data-ttu-id="2b332-146">LooseAndIgnoreCaseAndIgnoreNonSpace</span><span class="sxs-lookup"><span data-stu-id="2b332-146">LooseAndIgnoreCaseAndIgnoreNonSpace</span></span>  <br/> |<span data-ttu-id="2b332-147">Va a quitar.</span><span class="sxs-lookup"><span data-stu-id="2b332-147">To be removed.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="2b332-148">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="2b332-148">Child elements</span></span>

|<span data-ttu-id="2b332-149">**Element**</span><span class="sxs-lookup"><span data-stu-id="2b332-149">**Element**</span></span>|<span data-ttu-id="2b332-150">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2b332-150">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2b332-151">FieldURI</span><span class="sxs-lookup"><span data-stu-id="2b332-151">FieldURI</span></span>](fielduri.md) <br/> |<span data-ttu-id="2b332-152">Identifica las propiedades con frecuencia que se hace referencia mediante un identificador URI.</span><span class="sxs-lookup"><span data-stu-id="2b332-152">Identifies frequently referenced properties by URI.</span></span>  <br/> |
|[<span data-ttu-id="2b332-153">IndexedFieldURI</span><span class="sxs-lookup"><span data-stu-id="2b332-153">IndexedFieldURI</span></span>](indexedfielduri.md) <br/> |<span data-ttu-id="2b332-154">Identifica a los miembros individuales de un diccionario.</span><span class="sxs-lookup"><span data-stu-id="2b332-154">Identifies individual members of a dictionary.</span></span>  <br/> |
|[<span data-ttu-id="2b332-155">ExtendedFieldURI</span><span class="sxs-lookup"><span data-stu-id="2b332-155">ExtendedFieldURI</span></span>](extendedfielduri.md) <br/> |<span data-ttu-id="2b332-156">Identifica las propiedades MAPI.</span><span class="sxs-lookup"><span data-stu-id="2b332-156">Identifies MAPI properties.</span></span>  <br/> |
|[<span data-ttu-id="2b332-157">Constante</span><span class="sxs-lookup"><span data-stu-id="2b332-157">Constant</span></span>](constant.md) <br/> |<span data-ttu-id="2b332-158">Identifica un valor constante en una restricción.</span><span class="sxs-lookup"><span data-stu-id="2b332-158">Identifies a constant value in a restriction.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="2b332-159">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="2b332-159">Parent elements</span></span>

|<span data-ttu-id="2b332-160">**Element**</span><span class="sxs-lookup"><span data-stu-id="2b332-160">**Element**</span></span>|<span data-ttu-id="2b332-161">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2b332-161">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2b332-162">Restriction</span><span class="sxs-lookup"><span data-stu-id="2b332-162">Restriction</span></span>](restriction.md) <br/> |<span data-ttu-id="2b332-163">Representa la restricción o la consulta que se usa para filtrar los elementos o carpetas en las operaciones de carpeta FindItem/FindFolder y búsqueda.</span><span class="sxs-lookup"><span data-stu-id="2b332-163">Represents the restriction or query that is used to filter items or folders in FindItem/FindFolder and search folder operations.</span></span>  <br/> |
|[<span data-ttu-id="2b332-164">No</span><span class="sxs-lookup"><span data-stu-id="2b332-164">Not</span></span>](not.md) <br/> |<span data-ttu-id="2b332-165">Representa una expresión de búsqueda que niega el valor booleano de la expresión de búsqueda que contiene.</span><span class="sxs-lookup"><span data-stu-id="2b332-165">Represents a search expression that negates the Boolean value of the search expression it contains.</span></span>  <br/> |
|[<span data-ttu-id="2b332-166">And</span><span class="sxs-lookup"><span data-stu-id="2b332-166">And</span></span>](and.md) <br/> |<span data-ttu-id="2b332-167">Representa una expresión de búsqueda que le permite realizar una operación de tipo Boolean y entre dos o más expresiones de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="2b332-167">Represents a search expression that allows you to perform a Boolean And operation between two or more search expressions.</span></span> <span data-ttu-id="2b332-168">El resultado de la operación And es **true** si se **cumplen**todas las expresiones de búsqueda incluidas en el y.</span><span class="sxs-lookup"><span data-stu-id="2b332-168">The result of the And operation is **true** if all of the search expressions contained within the And are **true**.</span></span>  <br/> |
|[<span data-ttu-id="2b332-169">Or</span><span class="sxs-lookup"><span data-stu-id="2b332-169">Or</span></span>](or.md) <br/> |<span data-ttu-id="2b332-170">Representa una expresión de búsqueda que se realiza una operación OR lógica en la expresión de búsqueda que contiene.</span><span class="sxs-lookup"><span data-stu-id="2b332-170">Represents a search expression that performs a logical OR on the search expression it contains.</span></span> <span data-ttu-id="2b332-171">El elemento [o](or.md) devolverá **true** si cualquiera de sus elementos secundarios que devuelva **true**.</span><span class="sxs-lookup"><span data-stu-id="2b332-171">The [Or](or.md) element will return **true** if any of its children return **true**.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2b332-172">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2b332-172">Remarks</span></span>

<span data-ttu-id="2b332-173">Los atributos se utilizan para determinar cómo se comparan los elementos.</span><span class="sxs-lookup"><span data-stu-id="2b332-173">The attributes are used to determine how the elements are matched.</span></span>
  
<span data-ttu-id="2b332-174">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="2b332-174">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2b332-175">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="2b332-175">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2b332-176">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="2b332-176">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="2b332-177">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="2b332-177">Schema Name</span></span>  <br/> |<span data-ttu-id="2b332-178">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="2b332-178">Types schema</span></span>  <br/> |
|<span data-ttu-id="2b332-179">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="2b332-179">Validation File</span></span>  <br/> |<span data-ttu-id="2b332-180">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="2b332-180">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="2b332-181">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="2b332-181">Can be Empty</span></span>  <br/> |<span data-ttu-id="2b332-182">False</span><span class="sxs-lookup"><span data-stu-id="2b332-182">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2b332-183">Vea también</span><span class="sxs-lookup"><span data-stu-id="2b332-183">See also</span></span>



- [<span data-ttu-id="2b332-184">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="2b332-184">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

