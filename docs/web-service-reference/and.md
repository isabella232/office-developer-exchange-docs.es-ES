---
title: Y
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- And
api_type:
- schema
ms.assetid: 790246c2-37ad-49a8-91b9-6186d743b011
description: El elemento y representa una expresión de búsqueda que le permite realizar una operación de tipo Boolean y entre dos o más expresiones de búsqueda. Es true si se cumplen todas las expresiones de búsqueda incluidas dentro del elemento y el resultado de la operación AND.
ms.openlocfilehash: d287d57d68aeca7127325dc8fb65fd0190e5b5eb
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763439"
---
# <a name="and"></a><span data-ttu-id="918a3-104">Y</span><span class="sxs-lookup"><span data-stu-id="918a3-104">And</span></span>

<span data-ttu-id="918a3-105">El elemento **y** representa una expresión de búsqueda que le permite realizar una operación de tipo Boolean **y** entre dos o más expresiones de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="918a3-105">The **And** element represents a search expression that allows you to perform a Boolean **AND** operation between two or more search expressions.</span></span> <span data-ttu-id="918a3-106">El resultado de la operación **AND** es **true** si se **cumplen**todas las expresiones de búsqueda incluidas dentro del elemento **y** .</span><span class="sxs-lookup"><span data-stu-id="918a3-106">The result of the **AND** operation is **true** if all the search expressions contained within the **And** element are **true**.</span></span>
  
```xml
<And>
   <SearchExpression/>
   <SearchExpression/>
</And>
```

 <span data-ttu-id="918a3-107">**AndType**</span><span class="sxs-lookup"><span data-stu-id="918a3-107">**AndType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="918a3-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="918a3-108">Attributes and elements</span></span>

<span data-ttu-id="918a3-109">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="918a3-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="918a3-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="918a3-110">Attributes</span></span>

<span data-ttu-id="918a3-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="918a3-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="918a3-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="918a3-112">Child elements</span></span>

|<span data-ttu-id="918a3-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="918a3-113">**Element**</span></span>|<span data-ttu-id="918a3-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="918a3-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="918a3-115">SearchExpression</span><span class="sxs-lookup"><span data-stu-id="918a3-115">SearchExpression</span></span>](searchexpression.md) <br/> | <span data-ttu-id="918a3-116">Representa la clase base para expresiones dentro de una restricción.</span><span class="sxs-lookup"><span data-stu-id="918a3-116">Represents the base class for expressions within a restriction.</span></span> <span data-ttu-id="918a3-117">Debe haber dos o más expresiones de búsqueda en una operación de And.</span><span class="sxs-lookup"><span data-stu-id="918a3-117">There must be two or more search expressions in an And operation.</span></span><br/><br/>  <span data-ttu-id="918a3-118">Uno de los siguientes elementos debe ser sustituido para el elemento **SearchExpression** :</span><span class="sxs-lookup"><span data-stu-id="918a3-118">One of the following elements must be substituted for the **SearchExpression** element:</span></span><ul><li> [<span data-ttu-id="918a3-119">Existe</span><span class="sxs-lookup"><span data-stu-id="918a3-119">Exists</span></span>](exists.md)</li><li>[<span data-ttu-id="918a3-120">Excluye</span><span class="sxs-lookup"><span data-stu-id="918a3-120">Excludes</span></span>](excludes.md)</li><li>[<span data-ttu-id="918a3-121">IsEqualTo</span><span class="sxs-lookup"><span data-stu-id="918a3-121">IsEqualTo</span></span>](isequalto.md)</li><li>[<span data-ttu-id="918a3-122">IsNotEqualTo</span><span class="sxs-lookup"><span data-stu-id="918a3-122">IsNotEqualTo</span></span>](isnotequalto.md)</li><li>[<span data-ttu-id="918a3-123">IsGreaterThan</span><span class="sxs-lookup"><span data-stu-id="918a3-123">IsGreaterThan</span></span>](isgreaterthan.md)</li><li>[<span data-ttu-id="918a3-124">IsGreaterThanOrEqualTo</span><span class="sxs-lookup"><span data-stu-id="918a3-124">IsGreaterThanOrEqualTo</span></span>](isgreaterthanorequalto.md)</li><li>[<span data-ttu-id="918a3-125">IsLessThan</span><span class="sxs-lookup"><span data-stu-id="918a3-125">IsLessThan</span></span>](islessthan.md)</li><li>[<span data-ttu-id="918a3-126">IsLessThanOrEqualTo</span><span class="sxs-lookup"><span data-stu-id="918a3-126">IsLessThanOrEqualTo</span></span>](islessthanorequalto.md)</li><li>[<span data-ttu-id="918a3-127">Incluye</span><span class="sxs-lookup"><span data-stu-id="918a3-127">Contains</span></span>](contains.md)</li><li>[<span data-ttu-id="918a3-128">No</span><span class="sxs-lookup"><span data-stu-id="918a3-128">Not</span></span>](not.md)</li><li><span data-ttu-id="918a3-129">**And**</span><span class="sxs-lookup"><span data-stu-id="918a3-129">**And**</span></span></li><li>[<span data-ttu-id="918a3-130">Or</span><span class="sxs-lookup"><span data-stu-id="918a3-130">Or</span></span>](or.md) </li></ul> |
   
### <a name="parent-elements"></a><span data-ttu-id="918a3-131">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="918a3-131">Parent elements</span></span>

|<span data-ttu-id="918a3-132">**Element**</span><span class="sxs-lookup"><span data-stu-id="918a3-132">**Element**</span></span>|<span data-ttu-id="918a3-133">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="918a3-133">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="918a3-134">Restriction</span><span class="sxs-lookup"><span data-stu-id="918a3-134">Restriction</span></span>](restriction.md) <br/> |<span data-ttu-id="918a3-135">Representa la restricción o la consulta que se usa para filtrar los elementos o carpetas en las operaciones de carpeta FindItem/FindFolder y búsqueda.</span><span class="sxs-lookup"><span data-stu-id="918a3-135">Represents the restriction or query that is used to filter items or folders in FindItem/FindFolder and search folder operations.</span></span>  <br/> |
|[<span data-ttu-id="918a3-136">No</span><span class="sxs-lookup"><span data-stu-id="918a3-136">Not</span></span>](not.md) <br/> |<span data-ttu-id="918a3-137">Representa una expresión de búsqueda que niega el valor booleano de la expresión de búsqueda que contiene.</span><span class="sxs-lookup"><span data-stu-id="918a3-137">Represents a search expression that negates the Boolean value of the search expression that it contains.</span></span>  <br/> |
|<span data-ttu-id="918a3-138">**And**</span><span class="sxs-lookup"><span data-stu-id="918a3-138">**And**</span></span> <br/> |<span data-ttu-id="918a3-139">Representa una expresión de búsqueda que le permite realizar una operación de tipo Boolean **y** entre dos o más expresiones de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="918a3-139">Represents a search expression that allows you to perform a Boolean **AND** operation between two or more search expressions.</span></span> <span data-ttu-id="918a3-140">El resultado de la operación **AND** es **true** si se **cumplen**todas las expresiones de búsqueda incluidas dentro del elemento **y** .</span><span class="sxs-lookup"><span data-stu-id="918a3-140">The result of the **AND** operation is **true** if all of the search expressions contained within the **And** element are **true**.</span></span>  <br/> |
|[<span data-ttu-id="918a3-141">Or</span><span class="sxs-lookup"><span data-stu-id="918a3-141">Or</span></span>](or.md) <br/> |<span data-ttu-id="918a3-142">Representa una expresión de búsqueda que se realiza una operación de **OR** lógica en la expresión de búsqueda que contiene.</span><span class="sxs-lookup"><span data-stu-id="918a3-142">Represents a search expression that performs a logical **OR** operation on the search expression that it contains.</span></span> <span data-ttu-id="918a3-143">**O** devolverá **true** si cualquiera de sus elementos secundarios devuelven **true**.</span><span class="sxs-lookup"><span data-stu-id="918a3-143">**Or** will return **true** if any of its children return **true**.</span></span> <span data-ttu-id="918a3-144">**O** debe tener dos o más elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="918a3-144">**Or** must have two or more children.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="918a3-145">Comentarios</span><span class="sxs-lookup"><span data-stu-id="918a3-145">Remarks</span></span>

<span data-ttu-id="918a3-146">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="918a3-146">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="918a3-147">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="918a3-147">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="918a3-148">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="918a3-148">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="918a3-149">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="918a3-149">Schema Name</span></span>  <br/> |<span data-ttu-id="918a3-150">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="918a3-150">Types schema</span></span>  <br/> |
|<span data-ttu-id="918a3-151">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="918a3-151">Validation File</span></span>  <br/> |<span data-ttu-id="918a3-152">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="918a3-152">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="918a3-153">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="918a3-153">Can be Empty</span></span>  <br/> |<span data-ttu-id="918a3-154">False</span><span class="sxs-lookup"><span data-stu-id="918a3-154">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="918a3-155">Vea también</span><span class="sxs-lookup"><span data-stu-id="918a3-155">See also</span></span>

- [<span data-ttu-id="918a3-156">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="918a3-156">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

