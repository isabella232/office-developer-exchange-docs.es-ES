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
description: El elemento Contains representa una expresión de búsqueda que determina si una propiedad determinada contiene el valor de cadena constante proporcionado.
ms.openlocfilehash: 79529bd752bcbce954ae3c8b0085c203b4eb8777
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44527120"
---
# <a name="contains"></a><span data-ttu-id="a7afe-103">Contains</span><span class="sxs-lookup"><span data-stu-id="a7afe-103">Contains</span></span>

<span data-ttu-id="a7afe-104">El elemento **Contains** representa una expresión de búsqueda que determina si una propiedad determinada contiene el valor de cadena constante proporcionado.</span><span class="sxs-lookup"><span data-stu-id="a7afe-104">The **Contains** element represents a search expression that determines whether a given property contains the supplied constant string value.</span></span> 
  
```xml
<Contains ContainmentMode="" ContainmentComparison="">
   <FieldURI/>
   <Constant/>
</Contains>
```

```xml
<Contains ContainmentMode="" ContainmentComparison="">
   <ExtendedFieldURI/>
   <Constant/>
</Contains>
```

```xml
<Contains ContainmentMode="" ContainmentComparison="">
   <IndexedFieldURI/>
   <Constant/>
</Contains>
```


<span data-ttu-id="a7afe-105">**ContainsExpressionType**</span><span class="sxs-lookup"><span data-stu-id="a7afe-105">**ContainsExpressionType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="a7afe-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="a7afe-106">Attributes and elements</span></span>

<span data-ttu-id="a7afe-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="a7afe-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a7afe-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="a7afe-108">Attributes</span></span>

|<span data-ttu-id="a7afe-109">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="a7afe-109">**Attribute**</span></span>|<span data-ttu-id="a7afe-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a7afe-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a7afe-111">**ContainmentMode**</span><span class="sxs-lookup"><span data-stu-id="a7afe-111">**ContainmentMode**</span></span> <br/> |<span data-ttu-id="a7afe-112">Identifica los límites de una búsqueda.</span><span class="sxs-lookup"><span data-stu-id="a7afe-112">Identifies the boundaries of a search.</span></span>  <br/> |
|<span data-ttu-id="a7afe-113">**ContainmentComparison**</span><span class="sxs-lookup"><span data-stu-id="a7afe-113">**ContainmentComparison**</span></span> <br/> |<span data-ttu-id="a7afe-114">Determina si la búsqueda omite los casos y los espacios.</span><span class="sxs-lookup"><span data-stu-id="a7afe-114">Determines whether the search ignores cases and spaces.</span></span>  <br/> |
   
#### <a name="containmentmode-attribute-values"></a><span data-ttu-id="a7afe-115">Valores del atributo ContainmentMode</span><span class="sxs-lookup"><span data-stu-id="a7afe-115">ContainmentMode attribute values</span></span>

|<span data-ttu-id="a7afe-116">**Valor**</span><span class="sxs-lookup"><span data-stu-id="a7afe-116">**Value**</span></span>|<span data-ttu-id="a7afe-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a7afe-117">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a7afe-118">FullString</span><span class="sxs-lookup"><span data-stu-id="a7afe-118">FullString</span></span>  <br/> |<span data-ttu-id="a7afe-119">La comparación se encuentra entre la cadena completa y la constante.</span><span class="sxs-lookup"><span data-stu-id="a7afe-119">The comparison is between the full string and the constant.</span></span> <span data-ttu-id="a7afe-120">El valor de la propiedad y la constante proporcionada son exactamente iguales.</span><span class="sxs-lookup"><span data-stu-id="a7afe-120">The property value and the supplied constant are precisely the same.</span></span>  <br/> |
|<span data-ttu-id="a7afe-121">Prefijo</span><span class="sxs-lookup"><span data-stu-id="a7afe-121">Prefixed</span></span>  <br/> |<span data-ttu-id="a7afe-122">La comparación se encuentra entre el prefijo de cadena y la constante.</span><span class="sxs-lookup"><span data-stu-id="a7afe-122">The comparison is between the string prefix and the constant.</span></span>  <br/> |
|<span data-ttu-id="a7afe-123">Subcadena</span><span class="sxs-lookup"><span data-stu-id="a7afe-123">Substring</span></span>  <br/> |<span data-ttu-id="a7afe-124">La comparación se encuentra entre una subcadena de la cadena y la constante.</span><span class="sxs-lookup"><span data-stu-id="a7afe-124">The comparison is between a substring of the string and the constant.</span></span>  <br/> |
|<span data-ttu-id="a7afe-125">PrefixOnWords</span><span class="sxs-lookup"><span data-stu-id="a7afe-125">PrefixOnWords</span></span>  <br/> |<span data-ttu-id="a7afe-126">La comparación se encuentra entre un prefijo de palabras individuales en la cadena y la constante.</span><span class="sxs-lookup"><span data-stu-id="a7afe-126">The comparison is between a prefix on individual words in the string and the constant.</span></span>  <br/> |
|<span data-ttu-id="a7afe-127">ExactPhrase</span><span class="sxs-lookup"><span data-stu-id="a7afe-127">ExactPhrase</span></span>  <br/> |<span data-ttu-id="a7afe-128">La comparación se encuentra entre una frase exacta en la cadena y la constante.</span><span class="sxs-lookup"><span data-stu-id="a7afe-128">The comparison is between an exact phrase in the string and the constant.</span></span>  <br/> |
   
#### <a name="containmentcomparison-attribute-values"></a><span data-ttu-id="a7afe-129">Valores del atributo ContainmentComparison</span><span class="sxs-lookup"><span data-stu-id="a7afe-129">ContainmentComparison attribute values</span></span>

|<span data-ttu-id="a7afe-130">**Valor**</span><span class="sxs-lookup"><span data-stu-id="a7afe-130">**Value**</span></span>|<span data-ttu-id="a7afe-131">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a7afe-131">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a7afe-132">Motiva</span><span class="sxs-lookup"><span data-stu-id="a7afe-132">Exact</span></span>  <br/> |<span data-ttu-id="a7afe-133">La comparación debe ser exacta.</span><span class="sxs-lookup"><span data-stu-id="a7afe-133">The comparison must be exact.</span></span>  <br/> |
|<span data-ttu-id="a7afe-134">IgnoreCase</span><span class="sxs-lookup"><span data-stu-id="a7afe-134">IgnoreCase</span></span>  <br/> |<span data-ttu-id="a7afe-135">La comparación omite el uso de mayúsculas.</span><span class="sxs-lookup"><span data-stu-id="a7afe-135">The comparison ignores casing.</span></span>  <br/> |
|<span data-ttu-id="a7afe-136">IgnoreNonSpacingCharacters</span><span class="sxs-lookup"><span data-stu-id="a7afe-136">IgnoreNonSpacingCharacters</span></span>  <br/> |<span data-ttu-id="a7afe-137">La comparación omite los caracteres que no son de espacio.</span><span class="sxs-lookup"><span data-stu-id="a7afe-137">The comparison ignores non-spacing characters.</span></span>  <br/> |
|<span data-ttu-id="a7afe-138">Separada</span><span class="sxs-lookup"><span data-stu-id="a7afe-138">Loose</span></span>  <br/> |<span data-ttu-id="a7afe-139">Que se va a quitar.</span><span class="sxs-lookup"><span data-stu-id="a7afe-139">To be removed.</span></span>  <br/> |
|<span data-ttu-id="a7afe-140">IgnoreCaseAndNonSpacingCharacters</span><span class="sxs-lookup"><span data-stu-id="a7afe-140">IgnoreCaseAndNonSpacingCharacters</span></span>  <br/> |<span data-ttu-id="a7afe-141">La comparación no tiene en cuenta las mayúsculas y minúsculas y los caracteres sin espacio.</span><span class="sxs-lookup"><span data-stu-id="a7afe-141">The comparison ignores casing and non-spacing characters.</span></span>  <br/> |
|<span data-ttu-id="a7afe-142">LooseAndIgnoreCase</span><span class="sxs-lookup"><span data-stu-id="a7afe-142">LooseAndIgnoreCase</span></span>  <br/> |<span data-ttu-id="a7afe-143">Que se va a quitar.</span><span class="sxs-lookup"><span data-stu-id="a7afe-143">To be removed.</span></span>  <br/> |
|<span data-ttu-id="a7afe-144">LooseAndIgnoreNonSpace</span><span class="sxs-lookup"><span data-stu-id="a7afe-144">LooseAndIgnoreNonSpace</span></span>  <br/> |<span data-ttu-id="a7afe-145">Que se va a quitar.</span><span class="sxs-lookup"><span data-stu-id="a7afe-145">To be removed.</span></span>  <br/> |
|<span data-ttu-id="a7afe-146">LooseAndIgnoreCaseAndIgnoreNonSpace</span><span class="sxs-lookup"><span data-stu-id="a7afe-146">LooseAndIgnoreCaseAndIgnoreNonSpace</span></span>  <br/> |<span data-ttu-id="a7afe-147">Que se va a quitar.</span><span class="sxs-lookup"><span data-stu-id="a7afe-147">To be removed.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="a7afe-148">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="a7afe-148">Child elements</span></span>

|<span data-ttu-id="a7afe-149">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="a7afe-149">**Element**</span></span>|<span data-ttu-id="a7afe-150">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a7afe-150">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a7afe-151">FieldURI</span><span class="sxs-lookup"><span data-stu-id="a7afe-151">FieldURI</span></span>](fielduri.md) <br/> |<span data-ttu-id="a7afe-152">Identifica las propiedades a las que se hace referencia con frecuencia mediante el URI.</span><span class="sxs-lookup"><span data-stu-id="a7afe-152">Identifies frequently referenced properties by URI.</span></span>  <br/> |
|[<span data-ttu-id="a7afe-153">IndexedFieldURI</span><span class="sxs-lookup"><span data-stu-id="a7afe-153">IndexedFieldURI</span></span>](indexedfielduri.md) <br/> |<span data-ttu-id="a7afe-154">Identifica a los miembros individuales de un diccionario.</span><span class="sxs-lookup"><span data-stu-id="a7afe-154">Identifies individual members of a dictionary.</span></span>  <br/> |
|[<span data-ttu-id="a7afe-155">ExtendedFieldURI</span><span class="sxs-lookup"><span data-stu-id="a7afe-155">ExtendedFieldURI</span></span>](extendedfielduri.md) <br/> |<span data-ttu-id="a7afe-156">Identifica las propiedades MAPI.</span><span class="sxs-lookup"><span data-stu-id="a7afe-156">Identifies MAPI properties.</span></span>  <br/> |
|[<span data-ttu-id="a7afe-157">Constante</span><span class="sxs-lookup"><span data-stu-id="a7afe-157">Constant</span></span>](constant.md) <br/> |<span data-ttu-id="a7afe-158">Identifica un valor constante en una restricción.</span><span class="sxs-lookup"><span data-stu-id="a7afe-158">Identifies a constant value in a restriction.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="a7afe-159">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="a7afe-159">Parent elements</span></span>

|<span data-ttu-id="a7afe-160">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="a7afe-160">**Element**</span></span>|<span data-ttu-id="a7afe-161">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a7afe-161">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a7afe-162">Restriction</span><span class="sxs-lookup"><span data-stu-id="a7afe-162">Restriction</span></span>](restriction.md) <br/> |<span data-ttu-id="a7afe-163">Representa la restricción o consulta que se usa para filtrar elementos o carpetas en las operaciones de carpeta de búsqueda FindItem/FindFolder.</span><span class="sxs-lookup"><span data-stu-id="a7afe-163">Represents the restriction or query that is used to filter items or folders in FindItem/FindFolder and search folder operations.</span></span>  <br/> |
|[<span data-ttu-id="a7afe-164">Not</span><span class="sxs-lookup"><span data-stu-id="a7afe-164">Not</span></span>](not.md) <br/> |<span data-ttu-id="a7afe-165">Representa una expresión de búsqueda que niega el valor booleano de la expresión de búsqueda que contiene.</span><span class="sxs-lookup"><span data-stu-id="a7afe-165">Represents a search expression that negates the Boolean value of the search expression it contains.</span></span>  <br/> |
|[<span data-ttu-id="a7afe-166">And</span><span class="sxs-lookup"><span data-stu-id="a7afe-166">And</span></span>](and.md) <br/> |<span data-ttu-id="a7afe-167">Representa una expresión de búsqueda que permite realizar una operación and booleana entre dos o más expresiones de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="a7afe-167">Represents a search expression that allows you to perform a Boolean And operation between two or more search expressions.</span></span> <span data-ttu-id="a7afe-168">El resultado de la operación and es **true** si todas las expresiones de búsqueda incluidas en el y son **true**.</span><span class="sxs-lookup"><span data-stu-id="a7afe-168">The result of the And operation is **true** if all of the search expressions contained within the And are **true**.</span></span>  <br/> |
|[<span data-ttu-id="a7afe-169">Or</span><span class="sxs-lookup"><span data-stu-id="a7afe-169">Or</span></span>](or.md) <br/> |<span data-ttu-id="a7afe-170">Representa una expresión de búsqueda que realiza una operación lógica OR en la expresión de búsqueda que contiene.</span><span class="sxs-lookup"><span data-stu-id="a7afe-170">Represents a search expression that performs a logical OR on the search expression it contains.</span></span> <span data-ttu-id="a7afe-171">El elemento [o](or.md) devolverá **true** si cualquiera de sus secundarios devuelve **true**.</span><span class="sxs-lookup"><span data-stu-id="a7afe-171">The [Or](or.md) element will return **true** if any of its children return **true**.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a7afe-172">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a7afe-172">Remarks</span></span>

<span data-ttu-id="a7afe-173">Los atributos se usan para determinar cómo coinciden los elementos.</span><span class="sxs-lookup"><span data-stu-id="a7afe-173">The attributes are used to determine how the elements are matched.</span></span>
  
<span data-ttu-id="a7afe-174">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="a7afe-174">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a7afe-175">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="a7afe-175">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a7afe-176">Namespace</span><span class="sxs-lookup"><span data-stu-id="a7afe-176">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a7afe-177">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="a7afe-177">Schema Name</span></span>  <br/> |<span data-ttu-id="a7afe-178">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="a7afe-178">Types schema</span></span>  <br/> |
|<span data-ttu-id="a7afe-179">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="a7afe-179">Validation File</span></span>  <br/> |<span data-ttu-id="a7afe-180">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="a7afe-180">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="a7afe-181">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="a7afe-181">Can be Empty</span></span>  <br/> |<span data-ttu-id="a7afe-182">Falso</span><span class="sxs-lookup"><span data-stu-id="a7afe-182">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a7afe-183">Vea también</span><span class="sxs-lookup"><span data-stu-id="a7afe-183">See also</span></span>

- [<span data-ttu-id="a7afe-184">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="a7afe-184">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

