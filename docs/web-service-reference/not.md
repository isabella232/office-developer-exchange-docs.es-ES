---
title: No
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Not
api_type:
- schema
ms.assetid: 1aa16318-7e90-4b19-bce8-dd1a20a66223
description: El elemento no representa una expresión de búsqueda que niega el valor booleano de la expresión de búsqueda que contiene.
ms.openlocfilehash: f5bc709d8b1e77a13b3598905651ac1750436f03
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836553"
---
# <a name="not"></a><span data-ttu-id="e8242-103">No</span><span class="sxs-lookup"><span data-stu-id="e8242-103">Not</span></span>

<span data-ttu-id="e8242-104">El elemento **no** representa una expresión de búsqueda que niega el valor booleano de la expresión de búsqueda que contiene.</span><span class="sxs-lookup"><span data-stu-id="e8242-104">The **Not** element represents a search expression that negates the Boolean value of the search expression that it contains.</span></span> 
  
```xml
<Not>
   <SearchExpression/>
</Not>
```

 <span data-ttu-id="e8242-105">**NotType**</span><span class="sxs-lookup"><span data-stu-id="e8242-105">**NotType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e8242-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="e8242-106">Attributes and elements</span></span>

<span data-ttu-id="e8242-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="e8242-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e8242-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="e8242-108">Attributes</span></span>

<span data-ttu-id="e8242-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="e8242-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e8242-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="e8242-110">Child elements</span></span>

|<span data-ttu-id="e8242-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="e8242-111">**Element**</span></span>|<span data-ttu-id="e8242-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e8242-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e8242-113">SearchExpression</span><span class="sxs-lookup"><span data-stu-id="e8242-113">SearchExpression</span></span>](searchexpression.md) <br/> | <span data-ttu-id="e8242-114">Representa la clase base para expresiones dentro de una restricción.</span><span class="sxs-lookup"><span data-stu-id="e8242-114">Represents the base class for expressions within a restriction.</span></span> <br/><br/><span data-ttu-id="e8242-115">Uno de los siguientes elementos debe ser sustituido para el elemento **SearchExpression** :</span><span class="sxs-lookup"><span data-stu-id="e8242-115">One of the following elements must be substituted for the **SearchExpression** element:</span></span> <br/> <br/><span data-ttu-id="e8242-116">- [Existe](exists.md)</span><span class="sxs-lookup"><span data-stu-id="e8242-116">- [Exists](exists.md)</span></span> <br/><span data-ttu-id="e8242-117">- [Excluye](excludes.md)</span><span class="sxs-lookup"><span data-stu-id="e8242-117">- [Excludes](excludes.md)</span></span> <br/><span data-ttu-id="e8242-118">- [IsEqualTo](isequalto.md)</span><span class="sxs-lookup"><span data-stu-id="e8242-118">- [IsEqualTo](isequalto.md)</span></span> <br/><span data-ttu-id="e8242-119">- [IsNotEqualTo](isnotequalto.md)</span><span class="sxs-lookup"><span data-stu-id="e8242-119">- [IsNotEqualTo](isnotequalto.md)</span></span> <br/><span data-ttu-id="e8242-120">- [IsGreaterThan](isgreaterthan.md)</span><span class="sxs-lookup"><span data-stu-id="e8242-120">- [IsGreaterThan](isgreaterthan.md)</span></span> <br/><span data-ttu-id="e8242-121">- [IsGreaterThanOrEqualTo](isgreaterthanorequalto.md)</span><span class="sxs-lookup"><span data-stu-id="e8242-121">- [IsGreaterThanOrEqualTo](isgreaterthanorequalto.md)</span></span> <br/><span data-ttu-id="e8242-122">- [IsLessThan](islessthan.md)</span><span class="sxs-lookup"><span data-stu-id="e8242-122">- [IsLessThan](islessthan.md)</span></span> <br/><span data-ttu-id="e8242-123">- [IsLessThanOrEqualTo](islessthanorequalto.md)</span><span class="sxs-lookup"><span data-stu-id="e8242-123">- [IsLessThanOrEqualTo](islessthanorequalto.md)</span></span> <br/><span data-ttu-id="e8242-124">- [Contiene](contains.md)</span><span class="sxs-lookup"><span data-stu-id="e8242-124">- [Contains](contains.md)</span></span> <br/><span data-ttu-id="e8242-125">- **No**</span><span class="sxs-lookup"><span data-stu-id="e8242-125">- **Not**</span></span> <br/><span data-ttu-id="e8242-126">- [Y](and.md)</span><span class="sxs-lookup"><span data-stu-id="e8242-126">- [And](and.md)</span></span> <br/><span data-ttu-id="e8242-127">- [O](or.md)</span><span class="sxs-lookup"><span data-stu-id="e8242-127">- [Or](or.md)</span></span> <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="e8242-128">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="e8242-128">Parent elements</span></span>

|<span data-ttu-id="e8242-129">**Element**</span><span class="sxs-lookup"><span data-stu-id="e8242-129">**Element**</span></span>|<span data-ttu-id="e8242-130">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e8242-130">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e8242-131">Restriction</span><span class="sxs-lookup"><span data-stu-id="e8242-131">Restriction</span></span>](restriction.md) <br/> |<span data-ttu-id="e8242-132">Representa la restricción o la consulta que se usa para filtrar los elementos o carpetas en las operaciones de carpeta FindItem/FindFolder y búsqueda.</span><span class="sxs-lookup"><span data-stu-id="e8242-132">Represents the restriction or query that is used to filter items or folders in FindItem/FindFolder and search folder operations.</span></span>  <br/> |
|<span data-ttu-id="e8242-133">**No**</span><span class="sxs-lookup"><span data-stu-id="e8242-133">**Not**</span></span> <br/> |<span data-ttu-id="e8242-134">Representa una expresión de búsqueda que niega el valor booleano de la expresión de búsqueda que contiene.</span><span class="sxs-lookup"><span data-stu-id="e8242-134">Represents a search expression that negates the Boolean value of the search expression that it contains.</span></span>  <br/> |
|[<span data-ttu-id="e8242-135">And</span><span class="sxs-lookup"><span data-stu-id="e8242-135">And</span></span>](and.md) <br/> |<span data-ttu-id="e8242-136">Representa una expresión de búsqueda que le permite realizar una operación de tipo Boolean **y** entre dos o más expresiones de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="e8242-136">Represents a search expression that allows you to perform a Boolean **AND** operation between two or more search expressions.</span></span> <span data-ttu-id="e8242-137">El resultado de la operación **AND** es **true** si se **cumplen**todas las expresiones de búsqueda incluidas dentro del elemento **y** .</span><span class="sxs-lookup"><span data-stu-id="e8242-137">The result of the **AND** operation is **true** if all the search expressions contained within the **And** element are **true**.</span></span>  <br/> |
|[<span data-ttu-id="e8242-138">Or</span><span class="sxs-lookup"><span data-stu-id="e8242-138">Or</span></span>](or.md) <br/> |<span data-ttu-id="e8242-139">Representa una expresión de búsqueda que se realiza una operación de **OR** lógica en la expresión de búsqueda que contiene.</span><span class="sxs-lookup"><span data-stu-id="e8242-139">Represents a search expression that performs a logical **OR** operation on the search expression that it contains.</span></span> <span data-ttu-id="e8242-140">**O** devolverá **true** si cualquiera de sus elementos secundarios devuelven **true**.</span><span class="sxs-lookup"><span data-stu-id="e8242-140">**Or** will return **true** if any of its children return **true**.</span></span> <span data-ttu-id="e8242-141">**O** debe tener dos o más elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="e8242-141">**Or** must have two or more children.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e8242-142">Notas</span><span class="sxs-lookup"><span data-stu-id="e8242-142">Remarks</span></span>

<span data-ttu-id="e8242-143">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="e8242-143">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e8242-144">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="e8242-144">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e8242-145">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e8242-145">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="e8242-146">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="e8242-146">Schema Name</span></span>  <br/> |<span data-ttu-id="e8242-147">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="e8242-147">Types schema</span></span>  <br/> |
|<span data-ttu-id="e8242-148">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="e8242-148">Validation File</span></span>  <br/> |<span data-ttu-id="e8242-149">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="e8242-149">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="e8242-150">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="e8242-150">Can be Empty</span></span>  <br/> |<span data-ttu-id="e8242-151">False</span><span class="sxs-lookup"><span data-stu-id="e8242-151">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e8242-152">Ver también</span><span class="sxs-lookup"><span data-stu-id="e8242-152">See also</span></span>

- [<span data-ttu-id="e8242-153">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="e8242-153">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

