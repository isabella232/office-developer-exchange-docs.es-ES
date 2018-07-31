---
title: IsNotEqualTo
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsNotEqualTo
api_type:
- schema
ms.assetid: e2eff26c-3403-45cd-bb74-1eb98c7dbfcd
description: El elemento IsNotEqualTo representa una expresión de búsqueda que compara una propiedad con un valor constante u otra propiedad y devuelve true si los valores no son los mismos.
ms.openlocfilehash: 75b580d97fbadbf3aa28c29159973f53768df624
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/28/2018
ms.locfileid: "21353255"
---
# <a name="isnotequalto"></a><span data-ttu-id="dd4ae-103">IsNotEqualTo</span><span class="sxs-lookup"><span data-stu-id="dd4ae-103">IsNotEqualTo</span></span>

<span data-ttu-id="dd4ae-104">El elemento **IsNotEqualTo** representa una expresión de búsqueda que se compara una propiedad con un valor constante o de otra propiedad y devuelve **true** si los valores no son los mismos.</span><span class="sxs-lookup"><span data-stu-id="dd4ae-104">The **IsNotEqualTo** element represents a search expression that compares a property with either a constant value or another property and returns **true** if the values are not the same.</span></span> 
  
```xml
<IsNotEqualTo>
   <FieldURI/>
   <FieldURIOrConstant/>
</IsNotEqualTo>
```

```xml
<IsNotEqualTo>
   <ExtendedFieldURI/> 
   <FieldURIOrConstant/>
</IsNotEqualTo>
```

```xml
<IsNotEqualTo>
   <IndexedFieldURI/>
   <FieldURIOrConstant/>
</IsNotEqualTo>
```

<span data-ttu-id="dd4ae-105">**IsNotEqualToType**</span><span class="sxs-lookup"><span data-stu-id="dd4ae-105">**IsNotEqualToType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="dd4ae-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="dd4ae-106">Attributes and elements</span></span>

<span data-ttu-id="dd4ae-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="dd4ae-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="dd4ae-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="dd4ae-108">Attributes</span></span>

<span data-ttu-id="dd4ae-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="dd4ae-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="dd4ae-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="dd4ae-110">Child elements</span></span>

|<span data-ttu-id="dd4ae-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="dd4ae-111">**Element**</span></span>|<span data-ttu-id="dd4ae-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="dd4ae-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="dd4ae-113">FieldURI</span><span class="sxs-lookup"><span data-stu-id="dd4ae-113">FieldURI</span></span>](fielduri.md) <br/> |<span data-ttu-id="dd4ae-114">Identifica las propiedades con frecuencia que se hace referencia mediante un identificador URI.</span><span class="sxs-lookup"><span data-stu-id="dd4ae-114">Identifies frequently referenced properties by URI.</span></span>  <br/> |
|[<span data-ttu-id="dd4ae-115">IndexedFieldURI</span><span class="sxs-lookup"><span data-stu-id="dd4ae-115">IndexedFieldURI</span></span>](indexedfielduri.md) <br/> |<span data-ttu-id="dd4ae-116">Identifica a los miembros individuales de un diccionario.</span><span class="sxs-lookup"><span data-stu-id="dd4ae-116">Identifies individual members of a dictionary.</span></span>  <br/> |
|[<span data-ttu-id="dd4ae-117">ExtendedFieldURI</span><span class="sxs-lookup"><span data-stu-id="dd4ae-117">ExtendedFieldURI</span></span>](extendedfielduri.md) <br/> |<span data-ttu-id="dd4ae-118">Identifica las propiedades MAPI.</span><span class="sxs-lookup"><span data-stu-id="dd4ae-118">Identifies MAPI properties.</span></span>  <br/> |
|[<span data-ttu-id="dd4ae-119">FieldURIOrConstant</span><span class="sxs-lookup"><span data-stu-id="dd4ae-119">FieldURIOrConstant</span></span>](fielduriorconstant.md) <br/> |<span data-ttu-id="dd4ae-120">Representa una propiedad o un valor constante que se usará cuando se comparan con otra propiedad.</span><span class="sxs-lookup"><span data-stu-id="dd4ae-120">Represents either a property or a constant value to be used when comparing with another property.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="dd4ae-121">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="dd4ae-121">Parent elements</span></span>

|<span data-ttu-id="dd4ae-122">**Element**</span><span class="sxs-lookup"><span data-stu-id="dd4ae-122">**Element**</span></span>|<span data-ttu-id="dd4ae-123">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="dd4ae-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="dd4ae-124">Restriction</span><span class="sxs-lookup"><span data-stu-id="dd4ae-124">Restriction</span></span>](restriction.md) <br/> |<span data-ttu-id="dd4ae-125">Representa la restricción o la consulta que se usa para filtrar los elementos o carpetas en las operaciones de carpeta FindItem/FindFolder y búsqueda.</span><span class="sxs-lookup"><span data-stu-id="dd4ae-125">Represents the restriction or query that is used to filter items or folders in FindItem/FindFolder and search folder operations.</span></span>  <br/> |
|[<span data-ttu-id="dd4ae-126">No</span><span class="sxs-lookup"><span data-stu-id="dd4ae-126">Not</span></span>](not.md) <br/> |<span data-ttu-id="dd4ae-127">Representa una expresión de búsqueda que niega el valor booleano de la expresión de búsqueda que contiene.</span><span class="sxs-lookup"><span data-stu-id="dd4ae-127">Represents a search expression that negates the Boolean value of the search expression that it contains.</span></span>  <br/> |
|[<span data-ttu-id="dd4ae-128">And</span><span class="sxs-lookup"><span data-stu-id="dd4ae-128">And</span></span>](and.md) <br/> |<span data-ttu-id="dd4ae-129">Representa una expresión de búsqueda que le permite realizar una operación de tipo Boolean y entre dos o más expresiones de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="dd4ae-129">Represents a search expression that allows you to perform a Boolean And operation between two or more search expressions.</span></span> <span data-ttu-id="dd4ae-130">El resultado de la operación And es **true** si se **cumplen**todas las expresiones de búsqueda incluidas en el y.</span><span class="sxs-lookup"><span data-stu-id="dd4ae-130">The result of the And operation is **true** if all of the search expressions contained within the And are **true**.</span></span>  <br/> |
|[<span data-ttu-id="dd4ae-131">Or</span><span class="sxs-lookup"><span data-stu-id="dd4ae-131">Or</span></span>](or.md) <br/> |<span data-ttu-id="dd4ae-132">Representa una expresión de búsqueda que se realiza una operación OR lógica en la expresión de búsqueda que contiene.</span><span class="sxs-lookup"><span data-stu-id="dd4ae-132">Represents a search expression that performs a logical OR on the search expression that it contains.</span></span> <span data-ttu-id="dd4ae-133">[O](or.md) devolverá **true** si cualquiera de sus elementos secundarios devuelven **true**.</span><span class="sxs-lookup"><span data-stu-id="dd4ae-133">[Or](or.md) will return **true** if any of its children return **true**.</span></span> <span data-ttu-id="dd4ae-134">**O** debe tener dos o más elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="dd4ae-134">**Or** must have two or more children.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dd4ae-135">Comentarios</span><span class="sxs-lookup"><span data-stu-id="dd4ae-135">Remarks</span></span>

<span data-ttu-id="dd4ae-136">Para realizar comparaciones de cadenas, considere el uso del elemento [Contains](contains.md) , ya que proporciona opciones para los parámetros coincidentes como caso y espacio en blanco.</span><span class="sxs-lookup"><span data-stu-id="dd4ae-136">To perform string comparisons, consider using the [Contains](contains.md) element, as it provides options for matching parameters such as case and white space.</span></span> <span data-ttu-id="dd4ae-137">Use el elemento [no](not.md) junto con el elemento [contiene](contains.md) para negar el resultado.</span><span class="sxs-lookup"><span data-stu-id="dd4ae-137">Use the [Not](not.md) element in conjunction with the [Contains](contains.md) element to negate the result.</span></span> 
  
<span data-ttu-id="dd4ae-138">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="dd4ae-138">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="dd4ae-139">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="dd4ae-139">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="dd4ae-140">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="dd4ae-140">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="dd4ae-141">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="dd4ae-141">Schema Name</span></span>  <br/> |<span data-ttu-id="dd4ae-142">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="dd4ae-142">Types schema</span></span>  <br/> |
|<span data-ttu-id="dd4ae-143">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="dd4ae-143">Validation File</span></span>  <br/> |<span data-ttu-id="dd4ae-144">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="dd4ae-144">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="dd4ae-145">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="dd4ae-145">Can be Empty</span></span>  <br/> |<span data-ttu-id="dd4ae-146">False</span><span class="sxs-lookup"><span data-stu-id="dd4ae-146">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="dd4ae-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="dd4ae-147">See also</span></span>

- [<span data-ttu-id="dd4ae-148">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="dd4ae-148">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

