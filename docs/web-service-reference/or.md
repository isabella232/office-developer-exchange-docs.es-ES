---
title: O
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Or
api_type:
- schema
ms.assetid: 4876d83a-73a3-4953-9d95-3048e6b76ccb
description: El elemento Or representa una expresión de búsqueda que se realiza una operación OR lógica en la expresión de búsqueda que contiene. O bien, devuelve true si cualquiera de sus elementos secundarios devuelven true. O bien, debe tener dos o más elementos secundarios.
ms.openlocfilehash: 46cf031047aeb09e05a385150ab7587968aef345
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836661"
---
# <a name="or"></a><span data-ttu-id="85bc7-105">O</span><span class="sxs-lookup"><span data-stu-id="85bc7-105">Or</span></span>

<span data-ttu-id="85bc7-106">El elemento **o** representa una expresión de búsqueda que lleva a cabo una lógica **o** en la expresión de búsqueda que contiene.</span><span class="sxs-lookup"><span data-stu-id="85bc7-106">The **Or** element represents a search expression that performs a logical **OR** on the search expression that it contains.</span></span> <span data-ttu-id="85bc7-107">**O** devolverá **true** si cualquiera de sus elementos secundarios devuelven **true**.</span><span class="sxs-lookup"><span data-stu-id="85bc7-107">**Or** will return **true** if any of its children return **true**.</span></span> <span data-ttu-id="85bc7-108">**O** debe tener dos o más elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="85bc7-108">**Or** must have two or more children.</span></span> 
  
```xml
<Or>
   <SearchExpression/>
   <SearchExpression/>
</Or>
```

 <span data-ttu-id="85bc7-109">**OrType**</span><span class="sxs-lookup"><span data-stu-id="85bc7-109">**OrType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="85bc7-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="85bc7-110">Attributes and elements</span></span>

<span data-ttu-id="85bc7-111">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="85bc7-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="85bc7-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="85bc7-112">Attributes</span></span>

<span data-ttu-id="85bc7-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="85bc7-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="85bc7-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="85bc7-114">Child elements</span></span>

|<span data-ttu-id="85bc7-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="85bc7-115">**Element**</span></span>|<span data-ttu-id="85bc7-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="85bc7-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="85bc7-117">SearchExpression</span><span class="sxs-lookup"><span data-stu-id="85bc7-117">SearchExpression</span></span>](searchexpression.md) <br/> | <span data-ttu-id="85bc7-118">Representa la clase base para expresiones dentro de una restricción.</span><span class="sxs-lookup"><span data-stu-id="85bc7-118">Represents the base class for expressions within a restriction.</span></span> <br/><br/><span data-ttu-id="85bc7-119">Uno de los siguientes elementos debe ser sustituido para el elemento **SearchExpression** :</span><span class="sxs-lookup"><span data-stu-id="85bc7-119">One of the following elements must be substituted for the **SearchExpression** element:</span></span> <br/> <br/><span data-ttu-id="85bc7-120">- [Existe](exists.md)</span><span class="sxs-lookup"><span data-stu-id="85bc7-120">- [Exists](exists.md)</span></span> <br/><span data-ttu-id="85bc7-121">- [Excluye](excludes.md)</span><span class="sxs-lookup"><span data-stu-id="85bc7-121">- [Excludes](excludes.md)</span></span> <br/><span data-ttu-id="85bc7-122">- [IsEqualTo](isequalto.md)</span><span class="sxs-lookup"><span data-stu-id="85bc7-122">- [IsEqualTo](isequalto.md)</span></span> <br/><span data-ttu-id="85bc7-123">- [IsNotEqualTo](isnotequalto.md)</span><span class="sxs-lookup"><span data-stu-id="85bc7-123">- [IsNotEqualTo](isnotequalto.md)</span></span> <br/><span data-ttu-id="85bc7-124">- [IsGreaterThan](isgreaterthan.md)</span><span class="sxs-lookup"><span data-stu-id="85bc7-124">- [IsGreaterThan](isgreaterthan.md)</span></span> <br/><span data-ttu-id="85bc7-125">- [IsGreaterThanOrEqualTo](isgreaterthanorequalto.md)</span><span class="sxs-lookup"><span data-stu-id="85bc7-125">- [IsGreaterThanOrEqualTo](isgreaterthanorequalto.md)</span></span> <br/><span data-ttu-id="85bc7-126">- [IsLessThan](islessthan.md)</span><span class="sxs-lookup"><span data-stu-id="85bc7-126">- [IsLessThan](islessthan.md)</span></span> <br/><span data-ttu-id="85bc7-127">- [IsLessThanOrEqualTo](islessthanorequalto.md)</span><span class="sxs-lookup"><span data-stu-id="85bc7-127">- [IsLessThanOrEqualTo](islessthanorequalto.md)</span></span> <br/><span data-ttu-id="85bc7-128">- [Contiene](contains.md)</span><span class="sxs-lookup"><span data-stu-id="85bc7-128">- [Contains](contains.md)</span></span> <br/><span data-ttu-id="85bc7-129">- [No](not.md)</span><span class="sxs-lookup"><span data-stu-id="85bc7-129">- [Not](not.md)</span></span> <br/><span data-ttu-id="85bc7-130">- [Y](and.md)</span><span class="sxs-lookup"><span data-stu-id="85bc7-130">- [And](and.md)</span></span> <br/><span data-ttu-id="85bc7-131">- **O**</span><span class="sxs-lookup"><span data-stu-id="85bc7-131">- **Or**</span></span> <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="85bc7-132">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="85bc7-132">Parent elements</span></span>

|<span data-ttu-id="85bc7-133">**Element**</span><span class="sxs-lookup"><span data-stu-id="85bc7-133">**Element**</span></span>|<span data-ttu-id="85bc7-134">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="85bc7-134">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="85bc7-135">Restriction</span><span class="sxs-lookup"><span data-stu-id="85bc7-135">Restriction</span></span>](restriction.md) <br/> |<span data-ttu-id="85bc7-136">Representa la restricción o la consulta que se usa para filtrar los elementos o carpetas en las operaciones de carpeta FindItem/FindFolder y búsqueda.</span><span class="sxs-lookup"><span data-stu-id="85bc7-136">Represents the restriction or query that is used to filter items or folders in FindItem/FindFolder and search folder operations.</span></span>  <br/> |
|[<span data-ttu-id="85bc7-137">No</span><span class="sxs-lookup"><span data-stu-id="85bc7-137">Not</span></span>](not.md) <br/> |<span data-ttu-id="85bc7-138">Representa una expresión de búsqueda que niega el valor booleano de la expresión de búsqueda que contiene.</span><span class="sxs-lookup"><span data-stu-id="85bc7-138">Represents a search expression that negates the Boolean value of the search expression that it contains.</span></span>  <br/> |
|[<span data-ttu-id="85bc7-139">And</span><span class="sxs-lookup"><span data-stu-id="85bc7-139">And</span></span>](and.md) <br/> |<span data-ttu-id="85bc7-140">Representa una expresión de búsqueda que le permite realizar una operación de tipo Boolean **y** entre dos o más expresiones de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="85bc7-140">Represents a search expression that allows you to perform a Boolean **AND** operation between two or more search expressions.</span></span> <span data-ttu-id="85bc7-141">El resultado de la operación **AND** es **true** si se **cumplen**todas las expresiones de búsqueda incluidas dentro del elemento **y** .</span><span class="sxs-lookup"><span data-stu-id="85bc7-141">The result of the **AND** operation is **true** if all the search expressions contained within the **And** element are **true**.</span></span>  <br/> |
|<span data-ttu-id="85bc7-142">**Or**</span><span class="sxs-lookup"><span data-stu-id="85bc7-142">**Or**</span></span> <br/> |<span data-ttu-id="85bc7-143">Representa una expresión de búsqueda que se realiza una operación de **OR** lógica en la expresión de búsqueda que contiene.</span><span class="sxs-lookup"><span data-stu-id="85bc7-143">Represents a search expression that performs a logical **OR** operation on the search expression that it contains.</span></span> <span data-ttu-id="85bc7-144">**O** devolverá **true** si cualquiera de sus elementos secundarios devuelven **true**.</span><span class="sxs-lookup"><span data-stu-id="85bc7-144">**Or** will return **true** if any of its children return **true**.</span></span> <span data-ttu-id="85bc7-145">**O** debe tener dos o más elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="85bc7-145">**Or** must have two or more children.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="85bc7-146">Comentarios</span><span class="sxs-lookup"><span data-stu-id="85bc7-146">Remarks</span></span>

<span data-ttu-id="85bc7-147">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="85bc7-147">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="85bc7-148">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="85bc7-148">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="85bc7-149">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="85bc7-149">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="85bc7-150">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="85bc7-150">Schema Name</span></span>  <br/> |<span data-ttu-id="85bc7-151">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="85bc7-151">Types schema</span></span>  <br/> |
|<span data-ttu-id="85bc7-152">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="85bc7-152">Validation File</span></span>  <br/> |<span data-ttu-id="85bc7-153">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="85bc7-153">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="85bc7-154">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="85bc7-154">Can be Empty</span></span>  <br/> |<span data-ttu-id="85bc7-155">False</span><span class="sxs-lookup"><span data-stu-id="85bc7-155">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="85bc7-156">Vea también</span><span class="sxs-lookup"><span data-stu-id="85bc7-156">See also</span></span>

- [<span data-ttu-id="85bc7-157">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="85bc7-157">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

