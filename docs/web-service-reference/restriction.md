---
title: Restriction
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Restriction
api_type:
- schema
ms.assetid: 77f19014-d112-4999-8e83-ecc32a117a73
description: El elemento Restriction representa la restricción o consulta que se usa para filtrar elementos o carpetas en FindItem/FindFolder y operaciones de carpeta de búsqueda.
ms.openlocfilehash: 6037ba15417d67d393ca70f3edf2248749c396e1
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465292"
---
# <a name="restriction"></a><span data-ttu-id="530b2-103">Restriction</span><span class="sxs-lookup"><span data-stu-id="530b2-103">Restriction</span></span>

<span data-ttu-id="530b2-104">El elemento **Restriction** representa la restricción o consulta que se usa para filtrar elementos o carpetas en FindItem/FindFolder y operaciones de carpeta de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="530b2-104">The **Restriction** element represents the restriction or query that is used to filter items or folders in FindItem/FindFolder and search folder operations.</span></span> 
  
```xml
<Restriction>
   <SearchExpression/>
</Restriction>
```

 <span data-ttu-id="530b2-105">**RestrictionType**</span><span class="sxs-lookup"><span data-stu-id="530b2-105">**RestrictionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="530b2-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="530b2-106">Attributes and elements</span></span>

<span data-ttu-id="530b2-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="530b2-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="530b2-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="530b2-108">Attributes</span></span>

<span data-ttu-id="530b2-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="530b2-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="530b2-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="530b2-110">Child elements</span></span>

|<span data-ttu-id="530b2-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="530b2-111">**Element**</span></span>|<span data-ttu-id="530b2-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="530b2-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="530b2-113">And</span><span class="sxs-lookup"><span data-stu-id="530b2-113">And</span></span>](and.md) <br/> |<span data-ttu-id="530b2-114">Representa una expresión de búsqueda que permite realizar una operación **and** booleana entre dos o más expresiones de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="530b2-114">Represents a search expression that enables you to perform a Boolean **AND** operation between two or more search expressions.</span></span>  <br/> |
|[<span data-ttu-id="530b2-115">Contains</span><span class="sxs-lookup"><span data-stu-id="530b2-115">Contains</span></span>](contains.md) <br/> |<span data-ttu-id="530b2-116">Representa una expresión de búsqueda que determina si una propiedad determinada contiene el valor de cadena constante proporcionado.</span><span class="sxs-lookup"><span data-stu-id="530b2-116">Represents a search expression that determines whether a given property contains the supplied constant string value.</span></span>  <br/> |
|[<span data-ttu-id="530b2-117">Excluye</span><span class="sxs-lookup"><span data-stu-id="530b2-117">Excludes</span></span>](excludes.md) <br/> |<span data-ttu-id="530b2-118">Realiza una máscara bit a bit de las propiedades.</span><span class="sxs-lookup"><span data-stu-id="530b2-118">Performs a bitwise mask of the properties.</span></span>  <br/> |
|[<span data-ttu-id="530b2-119">Exists</span><span class="sxs-lookup"><span data-stu-id="530b2-119">Exists</span></span>](exists.md) <br/> |<span data-ttu-id="530b2-120">Representa una expresión de búsqueda que devuelve **true** si la propiedad proporcionada existe en un elemento.</span><span class="sxs-lookup"><span data-stu-id="530b2-120">Represents a search expression that returns **true** if the supplied property exists on an item.</span></span>  <br/> |
|[<span data-ttu-id="530b2-121">IsEqualTo</span><span class="sxs-lookup"><span data-stu-id="530b2-121">IsEqualTo</span></span>](isequalto.md) <br/> |<span data-ttu-id="530b2-122">Representa una expresión de búsqueda que compara una propiedad con un valor constante u otra propiedad y evalúa en **true** si son iguales.</span><span class="sxs-lookup"><span data-stu-id="530b2-122">Represents a search expression that compares a property with either a constant value or another property and evaluates to **true** if they are equal.</span></span>  <br/> |
|[<span data-ttu-id="530b2-123">IsGreaterThan</span><span class="sxs-lookup"><span data-stu-id="530b2-123">IsGreaterThan</span></span>](isgreaterthan.md) <br/> |<span data-ttu-id="530b2-124">Representa una expresión de búsqueda que compara una propiedad con un valor constante u otra propiedad y devuelve **true** si la primera propiedad es mayor que el valor o la propiedad.</span><span class="sxs-lookup"><span data-stu-id="530b2-124">Represents a search expression that compares a property with either a constant value or another property and returns **true** if the first property is greater than the value or property.</span></span>  <br/> |
|[<span data-ttu-id="530b2-125">IsGreaterThanOrEqualTo</span><span class="sxs-lookup"><span data-stu-id="530b2-125">IsGreaterThanOrEqualTo</span></span>](isgreaterthanorequalto.md) <br/> |<span data-ttu-id="530b2-126">Representa una expresión de búsqueda que compara una propiedad con un valor constante u otra propiedad y devuelve **true** si la primera propiedad es mayor o igual que el valor o la propiedad.</span><span class="sxs-lookup"><span data-stu-id="530b2-126">Represents a search expression that compares a property with either a constant value or another property and returns **true** if the first property is greater than or equal to the value or property.</span></span>  <br/> |
|[<span data-ttu-id="530b2-127">IsLessThan</span><span class="sxs-lookup"><span data-stu-id="530b2-127">IsLessThan</span></span>](islessthan.md) <br/> |<span data-ttu-id="530b2-128">Representa una expresión de búsqueda que compara una propiedad con un valor constante u otra propiedad y devuelve **true** si la primera propiedad es menor que el valor o la propiedad.</span><span class="sxs-lookup"><span data-stu-id="530b2-128">Represents a search expression that compares a property with either a constant value or another property and returns **true** if the first property is less than the value or property.</span></span>  <br/> |
|[<span data-ttu-id="530b2-129">IsLessThanOrEqualTo</span><span class="sxs-lookup"><span data-stu-id="530b2-129">IsLessThanOrEqualTo</span></span>](islessthanorequalto.md) <br/> |<span data-ttu-id="530b2-130">Representa una expresión de búsqueda que compara una propiedad con un valor constante u otra propiedad y devuelve **true** si la primera propiedad es menor o igual que el valor o la propiedad.</span><span class="sxs-lookup"><span data-stu-id="530b2-130">Represents a search expression that compares a property with either a constant value or another property and returns **true** if the first property is less than or equal to the value or property.</span></span>  <br/> |
|[<span data-ttu-id="530b2-131">IsNotEqualTo</span><span class="sxs-lookup"><span data-stu-id="530b2-131">IsNotEqualTo</span></span>](isnotequalto.md) <br/> |<span data-ttu-id="530b2-132">Representa una expresión de búsqueda que compara una propiedad con un valor constante u otra propiedad y devuelve **true** si los valores no son los mismos.</span><span class="sxs-lookup"><span data-stu-id="530b2-132">Represents a search expression that compares a property with either a constant value or another property and returns **true** if the values are not the same.</span></span>  <br/> |
|[<span data-ttu-id="530b2-133">Not</span><span class="sxs-lookup"><span data-stu-id="530b2-133">Not</span></span>](not.md) <br/> |<span data-ttu-id="530b2-134">Representa una expresión de búsqueda que niega el valor booleano de la expresión de búsqueda que contiene.</span><span class="sxs-lookup"><span data-stu-id="530b2-134">Represents a search expression that negates the Boolean value of the search expression it contains.</span></span>  <br/> |
|[<span data-ttu-id="530b2-135">Or</span><span class="sxs-lookup"><span data-stu-id="530b2-135">Or</span></span>](or.md) <br/> |<span data-ttu-id="530b2-136">Representa una expresión de búsqueda que realiza una operación **or** lógica en la expresión de búsqueda que contiene.</span><span class="sxs-lookup"><span data-stu-id="530b2-136">Represents a search expression that performs a logical **OR** operation on the search expression it contains.</span></span> <span data-ttu-id="530b2-137">El elemento **o** devolverá **true** si cualquiera de sus secundarios devuelve **true**.</span><span class="sxs-lookup"><span data-stu-id="530b2-137">The **Or** element will return **true** if any of its children return **true**.</span></span>  <br/> |
|[<span data-ttu-id="530b2-138">SearchExpression</span><span class="sxs-lookup"><span data-stu-id="530b2-138">SearchExpression</span></span>](searchexpression.md) <br/> |<span data-ttu-id="530b2-139">Representa el elemento sustituido dentro de una restricción.</span><span class="sxs-lookup"><span data-stu-id="530b2-139">Represents the substituted element within a restriction.</span></span> <span data-ttu-id="530b2-140">Este elemento no se usa en un documento de instancia XML.</span><span class="sxs-lookup"><span data-stu-id="530b2-140">This element is not used in an XML instance document.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="530b2-141">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="530b2-141">Parent elements</span></span>

|<span data-ttu-id="530b2-142">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="530b2-142">**Element**</span></span>|<span data-ttu-id="530b2-143">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="530b2-143">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="530b2-144">FindFolder</span><span class="sxs-lookup"><span data-stu-id="530b2-144">FindFolder</span></span>](findfolder.md) <br/> |<span data-ttu-id="530b2-145">Define una solicitud para identificar las carpetas en un buzón.</span><span class="sxs-lookup"><span data-stu-id="530b2-145">Defines a request to identify folders in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="530b2-146">FindItem</span><span class="sxs-lookup"><span data-stu-id="530b2-146">FindItem</span></span>](finditem.md) <br/> |<span data-ttu-id="530b2-147">Define una solicitud para buscar elementos en un buzón.</span><span class="sxs-lookup"><span data-stu-id="530b2-147">Defines a request to find items in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="530b2-148">SearchParameters</span><span class="sxs-lookup"><span data-stu-id="530b2-148">SearchParameters</span></span>](searchparameters.md) <br/> |<span data-ttu-id="530b2-149">Representa los parámetros que definen una carpeta de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="530b2-149">Represents the parameters that define a search folder.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="530b2-150">Comentarios</span><span class="sxs-lookup"><span data-stu-id="530b2-150">Remarks</span></span>

<span data-ttu-id="530b2-151">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="530b2-151">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="530b2-152">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="530b2-152">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="530b2-153">Namespace</span><span class="sxs-lookup"><span data-stu-id="530b2-153">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="530b2-154">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="530b2-154">Schema Name</span></span>  <br/> |<span data-ttu-id="530b2-155">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="530b2-155">Types schema</span></span>  <br/> |
|<span data-ttu-id="530b2-156">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="530b2-156">Validation File</span></span>  <br/> |<span data-ttu-id="530b2-157">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="530b2-157">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="530b2-158">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="530b2-158">Can be Empty</span></span>  <br/> |<span data-ttu-id="530b2-159">Falso</span><span class="sxs-lookup"><span data-stu-id="530b2-159">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="530b2-160">Vea también</span><span class="sxs-lookup"><span data-stu-id="530b2-160">See also</span></span>



- [<span data-ttu-id="530b2-161">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="530b2-161">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

