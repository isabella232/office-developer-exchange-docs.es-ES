---
title: SearchExpression
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SearchExpression
api_type:
- schema
ms.assetid: daa179b6-8c7f-4268-a312-c2acc67fa7c3
description: El elemento SearchExpression es un elemento abstracto que representa el elemento sustituido dentro de una restricción. Todas las expresiones de búsqueda se derivan de este tipo de base. Este elemento no se usa en un documento de instancia XML.
ms.openlocfilehash: 8e0d09aec079280816cd9dfe2c1a55c88bb959a7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19837286"
---
# <a name="searchexpression"></a><span data-ttu-id="c7484-105">SearchExpression</span><span class="sxs-lookup"><span data-stu-id="c7484-105">SearchExpression</span></span>

<span data-ttu-id="c7484-106">El elemento **SearchExpression** es un elemento abstracto que representa el elemento sustituido dentro de una restricción.</span><span class="sxs-lookup"><span data-stu-id="c7484-106">The **SearchExpression** element is an abstract element that represents the substituted element within a restriction.</span></span> <span data-ttu-id="c7484-107">Todas las expresiones de búsqueda se derivan de este tipo de base.</span><span class="sxs-lookup"><span data-stu-id="c7484-107">All search expressions derive from this base type.</span></span> <span data-ttu-id="c7484-108">Este elemento no se usa en un documento de instancia XML.</span><span class="sxs-lookup"><span data-stu-id="c7484-108">This element is not used in an XML instance document.</span></span> 
  
```xml
<SearchExpression/>
```

 <span data-ttu-id="c7484-109">**SearchExpressionType**</span><span class="sxs-lookup"><span data-stu-id="c7484-109">**SearchExpressionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c7484-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="c7484-110">Attributes and elements</span></span>

<span data-ttu-id="c7484-111">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="c7484-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c7484-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="c7484-112">Attributes</span></span>

<span data-ttu-id="c7484-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="c7484-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c7484-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c7484-114">Child elements</span></span>

<span data-ttu-id="c7484-115">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="c7484-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="c7484-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="c7484-116">Parent elements</span></span>

|<span data-ttu-id="c7484-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="c7484-117">**Element**</span></span>|<span data-ttu-id="c7484-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c7484-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c7484-119">Restriction</span><span class="sxs-lookup"><span data-stu-id="c7484-119">Restriction</span></span>](restriction.md) <br/> |<span data-ttu-id="c7484-120">Representa la restricción o la consulta que se usa para filtrar los elementos o carpetas en las operaciones de carpeta FindItem/FindFolder y búsqueda.</span><span class="sxs-lookup"><span data-stu-id="c7484-120">Represents the restriction or query that is used to filter items or folders in FindItem/FindFolder and search folder operations.</span></span>  <br/> |
|[<span data-ttu-id="c7484-121">No</span><span class="sxs-lookup"><span data-stu-id="c7484-121">Not</span></span>](not.md) <br/> |<span data-ttu-id="c7484-122">Representa una expresión de búsqueda que niega el valor booleano de la expresión de búsqueda que contiene.</span><span class="sxs-lookup"><span data-stu-id="c7484-122">Represents a search expression that negates the Boolean value of the search expression that it contains.</span></span>  <br/> |
|[<span data-ttu-id="c7484-123">And</span><span class="sxs-lookup"><span data-stu-id="c7484-123">And</span></span>](and.md) <br/> |<span data-ttu-id="c7484-124">Representa una expresión de búsqueda que le permite realizar una operación de tipo Boolean **y** entre dos o más expresiones de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="c7484-124">Represents a search expression that allows you to perform a Boolean **AND** operation between two or more search expressions.</span></span> <span data-ttu-id="c7484-125">El resultado de la operación **AND** es **true** si se **cumplen**todas las expresiones de búsqueda incluidas dentro del elemento **y** .</span><span class="sxs-lookup"><span data-stu-id="c7484-125">The result of the **AND** operation is **true** if all the search expressions contained within the **And** element are **true**.</span></span>  <br/> |
|[<span data-ttu-id="c7484-126">Or</span><span class="sxs-lookup"><span data-stu-id="c7484-126">Or</span></span>](or.md) <br/> |<span data-ttu-id="c7484-127">Representa una expresión de búsqueda que se realiza una operación de **OR** lógica en la expresión de búsqueda que contiene.</span><span class="sxs-lookup"><span data-stu-id="c7484-127">Represents a search expression that performs a logical **OR** operation on the search expression that it contains.</span></span> <span data-ttu-id="c7484-128">**O** devolverá **true** si cualquiera de sus elementos secundarios devuelven **true**.</span><span class="sxs-lookup"><span data-stu-id="c7484-128">**Or** will return **true** if any of its children return **true**.</span></span> <span data-ttu-id="c7484-129">**O** debe tener dos o más elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="c7484-129">**Or** must have two or more children.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c7484-130">Notas</span><span class="sxs-lookup"><span data-stu-id="c7484-130">Remarks</span></span>

<span data-ttu-id="c7484-131">Cualquier elemento de filtro que forma parte del grupo de sustitución SearchExpression puede aparecer en lugar del elemento SearchExpression.</span><span class="sxs-lookup"><span data-stu-id="c7484-131">Any filter element that is part of the SearchExpression substitution group can appear in place of the SearchExpression element.</span></span>
  
> [!NOTE]
> <span data-ttu-id="c7484-132">Este elemento no se producirá nunca directamente dentro de un documento de instancia.</span><span class="sxs-lookup"><span data-stu-id="c7484-132">This element will never occur directly within an instance document.</span></span> 
  
<span data-ttu-id="c7484-133">Los siguientes elementos son miembros del grupo de sustitución SearchExpression:</span><span class="sxs-lookup"><span data-stu-id="c7484-133">The following elements are members of the SearchExpression substitution group:</span></span>
  
- [<span data-ttu-id="c7484-134">Existe</span><span class="sxs-lookup"><span data-stu-id="c7484-134">Exists</span></span>](exists.md)
    
- [<span data-ttu-id="c7484-135">Excluye</span><span class="sxs-lookup"><span data-stu-id="c7484-135">Excludes</span></span>](excludes.md)
    
- [<span data-ttu-id="c7484-136">IsEqualTo</span><span class="sxs-lookup"><span data-stu-id="c7484-136">IsEqualTo</span></span>](isequalto.md)
    
- [<span data-ttu-id="c7484-137">IsNotEqualTo</span><span class="sxs-lookup"><span data-stu-id="c7484-137">IsNotEqualTo</span></span>](isnotequalto.md)
    
- [<span data-ttu-id="c7484-138">IsGreaterThan</span><span class="sxs-lookup"><span data-stu-id="c7484-138">IsGreaterThan</span></span>](isgreaterthan.md)
    
- [<span data-ttu-id="c7484-139">IsGreaterThanOrEqualTo</span><span class="sxs-lookup"><span data-stu-id="c7484-139">IsGreaterThanOrEqualTo</span></span>](isgreaterthanorequalto.md)
    
- [<span data-ttu-id="c7484-140">IsLessThan</span><span class="sxs-lookup"><span data-stu-id="c7484-140">IsLessThan</span></span>](islessthan.md)
    
- [<span data-ttu-id="c7484-141">IsLessThanOrEqualTo</span><span class="sxs-lookup"><span data-stu-id="c7484-141">IsLessThanOrEqualTo</span></span>](islessthanorequalto.md)
    
- [<span data-ttu-id="c7484-142">Incluye</span><span class="sxs-lookup"><span data-stu-id="c7484-142">Contains</span></span>](contains.md)
    
- [<span data-ttu-id="c7484-143">No</span><span class="sxs-lookup"><span data-stu-id="c7484-143">Not</span></span>](not.md)
    
- [<span data-ttu-id="c7484-144">And</span><span class="sxs-lookup"><span data-stu-id="c7484-144">And</span></span>](and.md)
    
- [<span data-ttu-id="c7484-145">Or</span><span class="sxs-lookup"><span data-stu-id="c7484-145">Or</span></span>](or.md)
    
<span data-ttu-id="c7484-146">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="c7484-146">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c7484-147">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="c7484-147">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c7484-148">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c7484-148">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c7484-149">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="c7484-149">Schema Name</span></span>  <br/> |<span data-ttu-id="c7484-150">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="c7484-150">Types schema</span></span>  <br/> |
|<span data-ttu-id="c7484-151">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="c7484-151">Validation File</span></span>  <br/> |<span data-ttu-id="c7484-152">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="c7484-152">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="c7484-153">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="c7484-153">Can be Empty</span></span>  <br/> |<span data-ttu-id="c7484-154">False</span><span class="sxs-lookup"><span data-stu-id="c7484-154">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c7484-155">Ver también</span><span class="sxs-lookup"><span data-stu-id="c7484-155">See also</span></span>



- [<span data-ttu-id="c7484-156">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="c7484-156">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

