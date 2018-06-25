---
title: Restricción
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
description: El elemento Restriction representa la restricción o la consulta que se usa para filtrar los elementos o carpetas en las operaciones de carpeta FindItem/FindFolder y búsqueda.
ms.openlocfilehash: 6b5702696db29910ae476a370bf362fe6a036ae7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19837213"
---
# <a name="restriction"></a><span data-ttu-id="45f70-103">Restricción</span><span class="sxs-lookup"><span data-stu-id="45f70-103">Restriction</span></span>

<span data-ttu-id="45f70-104">El elemento **Restriction** representa la restricción o la consulta que se usa para filtrar los elementos o carpetas en las operaciones de carpeta FindItem/FindFolder y búsqueda.</span><span class="sxs-lookup"><span data-stu-id="45f70-104">The **Restriction** element represents the restriction or query that is used to filter items or folders in FindItem/FindFolder and search folder operations.</span></span> 
  
```xml
<Restriction>
   <SearchExpression/>
</Restriction>
```

 <span data-ttu-id="45f70-105">**RestrictionType**</span><span class="sxs-lookup"><span data-stu-id="45f70-105">**RestrictionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="45f70-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="45f70-106">Attributes and elements</span></span>

<span data-ttu-id="45f70-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="45f70-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="45f70-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="45f70-108">Attributes</span></span>

<span data-ttu-id="45f70-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="45f70-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="45f70-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="45f70-110">Child elements</span></span>

|<span data-ttu-id="45f70-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="45f70-111">**Element**</span></span>|<span data-ttu-id="45f70-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="45f70-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="45f70-113">And</span><span class="sxs-lookup"><span data-stu-id="45f70-113">And</span></span>](and.md) <br/> |<span data-ttu-id="45f70-114">Representa una expresión de búsqueda que permite realizar una operación de tipo Boolean **y** entre dos o más expresiones de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="45f70-114">Represents a search expression that enables you to perform a Boolean **AND** operation between two or more search expressions.</span></span>  <br/> |
|[<span data-ttu-id="45f70-115">Incluye</span><span class="sxs-lookup"><span data-stu-id="45f70-115">Contains</span></span>](contains.md) <br/> |<span data-ttu-id="45f70-116">Representa una expresión de búsqueda que determina si una propiedad determinada contiene el valor de cadena constante proporcionada.</span><span class="sxs-lookup"><span data-stu-id="45f70-116">Represents a search expression that determines whether a given property contains the supplied constant string value.</span></span>  <br/> |
|[<span data-ttu-id="45f70-117">Excluye</span><span class="sxs-lookup"><span data-stu-id="45f70-117">Excludes</span></span>](excludes.md) <br/> |<span data-ttu-id="45f70-118">Realiza una máscara de bit a bit de las propiedades.</span><span class="sxs-lookup"><span data-stu-id="45f70-118">Performs a bitwise mask of the properties.</span></span>  <br/> |
|[<span data-ttu-id="45f70-119">Existe</span><span class="sxs-lookup"><span data-stu-id="45f70-119">Exists</span></span>](exists.md) <br/> |<span data-ttu-id="45f70-120">Representa una expresión de búsqueda que devuelve **true** si existe la propiedad proporcionada en un elemento.</span><span class="sxs-lookup"><span data-stu-id="45f70-120">Represents a search expression that returns **true** if the supplied property exists on an item.</span></span>  <br/> |
|[<span data-ttu-id="45f70-121">IsEqualTo</span><span class="sxs-lookup"><span data-stu-id="45f70-121">IsEqualTo</span></span>](isequalto.md) <br/> |<span data-ttu-id="45f70-122">Representa una expresión de búsqueda que compara una propiedad con un valor constante u otra propiedad y se evalúa como **true** si son iguales.</span><span class="sxs-lookup"><span data-stu-id="45f70-122">Represents a search expression that compares a property with either a constant value or another property and evaluates to **true** if they are equal.</span></span>  <br/> |
|[<span data-ttu-id="45f70-123">IsGreaterThan</span><span class="sxs-lookup"><span data-stu-id="45f70-123">IsGreaterThan</span></span>](isgreaterthan.md) <br/> |<span data-ttu-id="45f70-124">Representa una expresión de búsqueda que se compara una propiedad con un valor constante o de otra propiedad y devuelve **true** si la primera propiedad es mayor que el valor o la propiedad.</span><span class="sxs-lookup"><span data-stu-id="45f70-124">Represents a search expression that compares a property with either a constant value or another property and returns **true** if the first property is greater than the value or property.</span></span>  <br/> |
|[<span data-ttu-id="45f70-125">IsGreaterThanOrEqualTo</span><span class="sxs-lookup"><span data-stu-id="45f70-125">IsGreaterThanOrEqualTo</span></span>](isgreaterthanorequalto.md) <br/> |<span data-ttu-id="45f70-126">Representa una expresión de búsqueda que compara una propiedad con un valor constante o de otra propiedad y devuelve **true** si la primera propiedad es mayor que o igual que el valor o la propiedad.</span><span class="sxs-lookup"><span data-stu-id="45f70-126">Represents a search expression that compares a property with either a constant value or another property and returns **true** if the first property is greater than or equal to the value or property.</span></span>  <br/> |
|[<span data-ttu-id="45f70-127">IsLessThan</span><span class="sxs-lookup"><span data-stu-id="45f70-127">IsLessThan</span></span>](islessthan.md) <br/> |<span data-ttu-id="45f70-128">Representa una expresión de búsqueda que se compara una propiedad con un valor constante o de otra propiedad y devuelve **true** si la primera propiedad es menor que el valor o la propiedad.</span><span class="sxs-lookup"><span data-stu-id="45f70-128">Represents a search expression that compares a property with either a constant value or another property and returns **true** if the first property is less than the value or property.</span></span>  <br/> |
|[<span data-ttu-id="45f70-129">IsLessThanOrEqualTo</span><span class="sxs-lookup"><span data-stu-id="45f70-129">IsLessThanOrEqualTo</span></span>](islessthanorequalto.md) <br/> |<span data-ttu-id="45f70-130">Representa una expresión de búsqueda que compara una propiedad con un valor constante o de otra propiedad y devuelve **true** si la primera propiedad es menor o igual al valor o propiedad.</span><span class="sxs-lookup"><span data-stu-id="45f70-130">Represents a search expression that compares a property with either a constant value or another property and returns **true** if the first property is less than or equal to the value or property.</span></span>  <br/> |
|[<span data-ttu-id="45f70-131">IsNotEqualTo</span><span class="sxs-lookup"><span data-stu-id="45f70-131">IsNotEqualTo</span></span>](isnotequalto.md) <br/> |<span data-ttu-id="45f70-132">Representa una expresión de búsqueda que se compara una propiedad con un valor constante o de otra propiedad y devuelve **true** si los valores no son los mismos.</span><span class="sxs-lookup"><span data-stu-id="45f70-132">Represents a search expression that compares a property with either a constant value or another property and returns **true** if the values are not the same.</span></span>  <br/> |
|[<span data-ttu-id="45f70-133">No</span><span class="sxs-lookup"><span data-stu-id="45f70-133">Not</span></span>](not.md) <br/> |<span data-ttu-id="45f70-134">Representa una expresión de búsqueda que niega el valor booleano de la expresión de búsqueda que contiene.</span><span class="sxs-lookup"><span data-stu-id="45f70-134">Represents a search expression that negates the Boolean value of the search expression it contains.</span></span>  <br/> |
|[<span data-ttu-id="45f70-135">Or</span><span class="sxs-lookup"><span data-stu-id="45f70-135">Or</span></span>](or.md) <br/> |<span data-ttu-id="45f70-136">Representa una expresión de búsqueda que se realiza una operación de **OR** lógica en la expresión de búsqueda que contiene.</span><span class="sxs-lookup"><span data-stu-id="45f70-136">Represents a search expression that performs a logical **OR** operation on the search expression it contains.</span></span> <span data-ttu-id="45f70-137">El elemento **o** devolverá **true** si cualquiera de sus elementos secundarios que devuelva **true**.</span><span class="sxs-lookup"><span data-stu-id="45f70-137">The **Or** element will return **true** if any of its children return **true**.</span></span>  <br/> |
|[<span data-ttu-id="45f70-138">SearchExpression</span><span class="sxs-lookup"><span data-stu-id="45f70-138">SearchExpression</span></span>](searchexpression.md) <br/> |<span data-ttu-id="45f70-139">Representa el elemento sustituido dentro de una restricción.</span><span class="sxs-lookup"><span data-stu-id="45f70-139">Represents the substituted element within a restriction.</span></span> <span data-ttu-id="45f70-140">Este elemento no se usa en un documento de instancia XML.</span><span class="sxs-lookup"><span data-stu-id="45f70-140">This element is not used in an XML instance document.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="45f70-141">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="45f70-141">Parent elements</span></span>

|<span data-ttu-id="45f70-142">**Element**</span><span class="sxs-lookup"><span data-stu-id="45f70-142">**Element**</span></span>|<span data-ttu-id="45f70-143">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="45f70-143">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="45f70-144">FindFolder</span><span class="sxs-lookup"><span data-stu-id="45f70-144">FindFolder</span></span>](findfolder.md) <br/> |<span data-ttu-id="45f70-145">Define una solicitud para identificar las carpetas de un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="45f70-145">Defines a request to identify folders in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="45f70-146">FindItem</span><span class="sxs-lookup"><span data-stu-id="45f70-146">FindItem</span></span>](finditem.md) <br/> |<span data-ttu-id="45f70-147">Define una solicitud para buscar elementos en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="45f70-147">Defines a request to find items in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="45f70-148">SearchParameters</span><span class="sxs-lookup"><span data-stu-id="45f70-148">SearchParameters</span></span>](searchparameters.md) <br/> |<span data-ttu-id="45f70-149">Representa los parámetros que definen una carpeta de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="45f70-149">Represents the parameters that define a search folder.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="45f70-150">Comentarios</span><span class="sxs-lookup"><span data-stu-id="45f70-150">Remarks</span></span>

<span data-ttu-id="45f70-151">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="45f70-151">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="45f70-152">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="45f70-152">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="45f70-153">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="45f70-153">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="45f70-154">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="45f70-154">Schema Name</span></span>  <br/> |<span data-ttu-id="45f70-155">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="45f70-155">Types schema</span></span>  <br/> |
|<span data-ttu-id="45f70-156">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="45f70-156">Validation File</span></span>  <br/> |<span data-ttu-id="45f70-157">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="45f70-157">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="45f70-158">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="45f70-158">Can be Empty</span></span>  <br/> |<span data-ttu-id="45f70-159">False</span><span class="sxs-lookup"><span data-stu-id="45f70-159">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="45f70-160">Vea también</span><span class="sxs-lookup"><span data-stu-id="45f70-160">See also</span></span>



- [<span data-ttu-id="45f70-161">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="45f70-161">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

