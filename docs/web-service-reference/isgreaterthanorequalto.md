---
title: IsGreaterThanOrEqualTo
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsGreaterThanOrEqualTo
api_type:
- schema
ms.assetid: 373cc954-314d-40e2-be03-cc08aefc0d5b
description: El elemento IsGreaterThanOrEqualTo representa una expresión de búsqueda que se compara una propiedad con un valor constante u otra propiedad y devuelve true si la primera propiedad es mayor que o igual que el segundo.
ms.openlocfilehash: c469f2535ab717e7bc09b6317e01f0f8b3be8170
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/28/2018
ms.locfileid: "21354375"
---
# <a name="isgreaterthanorequalto"></a><span data-ttu-id="c7674-103">IsGreaterThanOrEqualTo</span><span class="sxs-lookup"><span data-stu-id="c7674-103">IsGreaterThanOrEqualTo</span></span>

<span data-ttu-id="c7674-104">El elemento **IsGreaterThanOrEqualTo** representa una expresión de búsqueda que compara una propiedad con un valor constante o de otra propiedad y devuelve **true** si la primera propiedad es mayor o igual que el segundo.</span><span class="sxs-lookup"><span data-stu-id="c7674-104">The **IsGreaterThanOrEqualTo** element represents a search expression that compares a property with either a constant value or another property and returns **true** if the first property is greater than or equal to the second.</span></span> 
  
```xml
<IsGreaterThanOrEqualTo>
   <FieldURI/>
   <FieldURIOrConstant/>
</IsGreaterThanOrEqualTo>
```

```xml
<IsGreaterThanOrEqualTo>
   <IndexedFieldURI/>
   <FieldURIOrConstant/>
</IsGreaterThanOrEqualTo>
```

```xml
<IsGreaterThanOrEqualTo>
   <ExtendedFieldURI/> 
   <FieldURIOrConstant/>
</IsGreaterThanOrEqualTo>
```

<span data-ttu-id="c7674-105">**IsGreaterThanOrEqualToType**</span><span class="sxs-lookup"><span data-stu-id="c7674-105">**IsGreaterThanOrEqualToType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="c7674-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="c7674-106">Attributes and elements</span></span>

<span data-ttu-id="c7674-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="c7674-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c7674-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="c7674-108">Attributes</span></span>

<span data-ttu-id="c7674-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="c7674-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c7674-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c7674-110">Child elements</span></span>

|<span data-ttu-id="c7674-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="c7674-111">**Element**</span></span>|<span data-ttu-id="c7674-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c7674-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c7674-113">FieldURI</span><span class="sxs-lookup"><span data-stu-id="c7674-113">FieldURI</span></span>](fielduri.md) <br/> |<span data-ttu-id="c7674-114">Identifica las propiedades con frecuencia que se hace referencia mediante un identificador URI.</span><span class="sxs-lookup"><span data-stu-id="c7674-114">Identifies frequently referenced properties by URI.</span></span>  <br/> |
|[<span data-ttu-id="c7674-115">IndexedFieldURI</span><span class="sxs-lookup"><span data-stu-id="c7674-115">IndexedFieldURI</span></span>](indexedfielduri.md) <br/> |<span data-ttu-id="c7674-116">Identifica a los miembros individuales de un diccionario.</span><span class="sxs-lookup"><span data-stu-id="c7674-116">Identifies individual members of a dictionary.</span></span>  <br/> |
|[<span data-ttu-id="c7674-117">ExtendedFieldURI</span><span class="sxs-lookup"><span data-stu-id="c7674-117">ExtendedFieldURI</span></span>](extendedfielduri.md) <br/> |<span data-ttu-id="c7674-118">Identifica las propiedades MAPI.</span><span class="sxs-lookup"><span data-stu-id="c7674-118">Identifies MAPI properties.</span></span>  <br/> |
|[<span data-ttu-id="c7674-119">FieldURIOrConstant</span><span class="sxs-lookup"><span data-stu-id="c7674-119">FieldURIOrConstant</span></span>](fielduriorconstant.md) <br/> |<span data-ttu-id="c7674-120">Representa una propiedad o un valor constante que se usará cuando se comparan con otra propiedad.</span><span class="sxs-lookup"><span data-stu-id="c7674-120">Represents either a property or a constant value to be used when comparing with another property.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="c7674-121">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="c7674-121">Parent elements</span></span>

|<span data-ttu-id="c7674-122">**Element**</span><span class="sxs-lookup"><span data-stu-id="c7674-122">**Element**</span></span>|<span data-ttu-id="c7674-123">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c7674-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c7674-124">Restriction</span><span class="sxs-lookup"><span data-stu-id="c7674-124">Restriction</span></span>](restriction.md) <br/> |<span data-ttu-id="c7674-125">Representa la restricción o la consulta que se usa para filtrar los elementos o carpetas en las operaciones de carpeta FindItem/FindFolder y búsqueda.</span><span class="sxs-lookup"><span data-stu-id="c7674-125">Represents the restriction or query that is used to filter items or folders in FindItem/FindFolder and search folder operations.</span></span>  <br/> |
|[<span data-ttu-id="c7674-126">No</span><span class="sxs-lookup"><span data-stu-id="c7674-126">Not</span></span>](not.md) <br/> |<span data-ttu-id="c7674-127">Representa una expresión de búsqueda que niega el valor booleano de la expresión de búsqueda que contiene.</span><span class="sxs-lookup"><span data-stu-id="c7674-127">Represents a search expression that negates the Boolean value of the search expression it contains.</span></span>  <br/> |
|[<span data-ttu-id="c7674-128">And</span><span class="sxs-lookup"><span data-stu-id="c7674-128">And</span></span>](and.md) <br/> |<span data-ttu-id="c7674-129">Representa una expresión de búsqueda que le permite realizar una operación de tipo Boolean y entre dos o más expresiones de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="c7674-129">Represents a search expression that enables you to perform a Boolean And operation between two or more search expressions.</span></span> <span data-ttu-id="c7674-130">El resultado de la operación And es **true** si se **cumplen**todas las expresiones de búsqueda incluidas en el y.</span><span class="sxs-lookup"><span data-stu-id="c7674-130">The result of the And operation is **true** if all of the search expressions contained within the And are **true**.</span></span>  <br/> |
|[<span data-ttu-id="c7674-131">Or</span><span class="sxs-lookup"><span data-stu-id="c7674-131">Or</span></span>](or.md) <br/> |<span data-ttu-id="c7674-132">Representa una expresión de búsqueda que se realiza una operación OR lógica en la expresión de búsqueda que contiene.</span><span class="sxs-lookup"><span data-stu-id="c7674-132">Represents a search expression that performs a logical OR on the search expression it contains.</span></span> <span data-ttu-id="c7674-133">Devuelve true si cualquiera de sus elementos secundarios que devuelva true [o](or.md) .</span><span class="sxs-lookup"><span data-stu-id="c7674-133">[Or](or.md) will return true if any of its children return true.</span></span> <span data-ttu-id="c7674-134">[O](or.md) debe tener dos o más elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="c7674-134">[Or](or.md) must have two or more children.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c7674-135">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c7674-135">Remarks</span></span>

<span data-ttu-id="c7674-136">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="c7674-136">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c7674-137">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="c7674-137">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c7674-138">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c7674-138">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c7674-139">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="c7674-139">Schema Name</span></span>  <br/> |<span data-ttu-id="c7674-140">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="c7674-140">Types schema</span></span>  <br/> |
|<span data-ttu-id="c7674-141">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="c7674-141">Validation File</span></span>  <br/> |<span data-ttu-id="c7674-142">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="c7674-142">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="c7674-143">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="c7674-143">Can be Empty</span></span>  <br/> |<span data-ttu-id="c7674-144">False</span><span class="sxs-lookup"><span data-stu-id="c7674-144">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c7674-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="c7674-145">See also</span></span>

- [<span data-ttu-id="c7674-146">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="c7674-146">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

