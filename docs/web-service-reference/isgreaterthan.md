---
title: IsGreaterThan
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsGreaterThan
api_type:
- schema
ms.assetid: a6e9d462-cfa7-40ec-903e-128c95050352
description: El elemento IsGreaterThan representa una expresión de búsqueda que compara una propiedad con un valor constante u otra propiedad y devuelve true si la primera propiedad es mayor.
ms.openlocfilehash: dfa7c221bb04e59f1ae12eeb5b9f2e1f09aea3ce
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/28/2018
ms.locfileid: "21353493"
---
# <a name="isgreaterthan"></a><span data-ttu-id="79f26-103">IsGreaterThan</span><span class="sxs-lookup"><span data-stu-id="79f26-103">IsGreaterThan</span></span>

<span data-ttu-id="79f26-104">El elemento **IsGreaterThan** representa una expresión de búsqueda que se compara una propiedad con un valor constante o de otra propiedad y devuelve **true** si la primera propiedad es mayor.</span><span class="sxs-lookup"><span data-stu-id="79f26-104">The **IsGreaterThan** element represents a search expression that compares a property with either a constant value or another property and returns **true** if the first property is greater.</span></span> 
  
```xml
<IsGreaterThan>
   <FieldURI/>
   <FieldURIOrConstant/>
</IsGreaterThan>
```

```xml
<IsGreaterThan>
   <IndexedFieldURI/> 
   <FieldURIOrConstant/>
</IsGreaterThan>
```

```xml
<IsGreaterThan>
   <ExtendedFieldURI/>
   <FieldURIOrConstant/>
</IsGreaterThan>
```

<span data-ttu-id="79f26-105">**IsGreaterThanType**</span><span class="sxs-lookup"><span data-stu-id="79f26-105">**IsGreaterThanType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="79f26-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="79f26-106">Attributes and elements</span></span>

<span data-ttu-id="79f26-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="79f26-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="79f26-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="79f26-108">Attributes</span></span>

<span data-ttu-id="79f26-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="79f26-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="79f26-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="79f26-110">Child elements</span></span>

|<span data-ttu-id="79f26-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="79f26-111">**Element**</span></span>|<span data-ttu-id="79f26-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="79f26-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="79f26-113">FieldURI</span><span class="sxs-lookup"><span data-stu-id="79f26-113">FieldURI</span></span>](fielduri.md) <br/> |<span data-ttu-id="79f26-114">Identifica las propiedades con frecuencia que se hace referencia mediante un identificador URI.</span><span class="sxs-lookup"><span data-stu-id="79f26-114">Identifies frequently referenced properties by URI.</span></span>  <br/> |
|[<span data-ttu-id="79f26-115">IndexedFieldURI</span><span class="sxs-lookup"><span data-stu-id="79f26-115">IndexedFieldURI</span></span>](indexedfielduri.md) <br/> |<span data-ttu-id="79f26-116">Identifica a los miembros individuales de un diccionario.</span><span class="sxs-lookup"><span data-stu-id="79f26-116">Identifies individual members of a dictionary.</span></span>  <br/> |
|[<span data-ttu-id="79f26-117">ExtendedFieldURI</span><span class="sxs-lookup"><span data-stu-id="79f26-117">ExtendedFieldURI</span></span>](extendedfielduri.md) <br/> |<span data-ttu-id="79f26-118">Identifica las propiedades MAPI.</span><span class="sxs-lookup"><span data-stu-id="79f26-118">Identifies MAPI properties.</span></span>  <br/> |
|[<span data-ttu-id="79f26-119">FieldURIOrConstant</span><span class="sxs-lookup"><span data-stu-id="79f26-119">FieldURIOrConstant</span></span>](fielduriorconstant.md) <br/> |<span data-ttu-id="79f26-120">Representa una propiedad o un valor constante que se usará cuando se comparan con otra propiedad.</span><span class="sxs-lookup"><span data-stu-id="79f26-120">Represents either a property or a constant value to be used when comparing with another property.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="79f26-121">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="79f26-121">Parent elements</span></span>

|<span data-ttu-id="79f26-122">**Element**</span><span class="sxs-lookup"><span data-stu-id="79f26-122">**Element**</span></span>|<span data-ttu-id="79f26-123">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="79f26-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="79f26-124">Restriction</span><span class="sxs-lookup"><span data-stu-id="79f26-124">Restriction</span></span>](restriction.md) <br/> |<span data-ttu-id="79f26-125">Representa la restricción o la consulta que se usa para filtrar los elementos o carpetas en las operaciones de carpeta FindItem/FindFolder y búsqueda.</span><span class="sxs-lookup"><span data-stu-id="79f26-125">Represents the restriction or query that is used to filter items or folders in FindItem/FindFolder and search folder operations.</span></span>  <br/> |
|[<span data-ttu-id="79f26-126">No</span><span class="sxs-lookup"><span data-stu-id="79f26-126">Not</span></span>](not.md) <br/> |<span data-ttu-id="79f26-127">Representa una expresión de búsqueda que niega el valor booleano de la expresión de búsqueda que contiene.</span><span class="sxs-lookup"><span data-stu-id="79f26-127">Represents a search expression that negates the Boolean value of the search expression that it contains.</span></span>  <br/> |
|[<span data-ttu-id="79f26-128">And</span><span class="sxs-lookup"><span data-stu-id="79f26-128">And</span></span>](and.md) <br/> |<span data-ttu-id="79f26-129">Representa una expresión de búsqueda que le permite realizar una operación de tipo Boolean y entre dos o más expresiones de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="79f26-129">Represents a search expression that enables you to perform a Boolean And operation between two or more search expressions.</span></span> <span data-ttu-id="79f26-130">El resultado de la operación And es **true** si se **cumplen**todas las expresiones de búsqueda incluidas en el y.</span><span class="sxs-lookup"><span data-stu-id="79f26-130">The result of the And operation is **true** if all the search expressions contained within the And are **true**.</span></span>  <br/> |
|[<span data-ttu-id="79f26-131">Or</span><span class="sxs-lookup"><span data-stu-id="79f26-131">Or</span></span>](or.md) <br/> |<span data-ttu-id="79f26-132">Representa una expresión de búsqueda que se realiza una operación OR lógica en la expresión de búsqueda que contiene.</span><span class="sxs-lookup"><span data-stu-id="79f26-132">Represents a search expression that performs a logical OR on the search expression it contains.</span></span> <span data-ttu-id="79f26-133">[O](or.md) devolverá **true** si cualquiera de sus elementos secundarios devuelven **true**.</span><span class="sxs-lookup"><span data-stu-id="79f26-133">[Or](or.md) will return **true** if any of its children return **true**.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="79f26-134">Comentarios</span><span class="sxs-lookup"><span data-stu-id="79f26-134">Remarks</span></span>

<span data-ttu-id="79f26-135">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="79f26-135">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="79f26-136">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="79f26-136">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="79f26-137">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="79f26-137">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="79f26-138">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="79f26-138">Schema Name</span></span>  <br/> |<span data-ttu-id="79f26-139">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="79f26-139">Types schema</span></span>  <br/> |
|<span data-ttu-id="79f26-140">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="79f26-140">Validation File</span></span>  <br/> |<span data-ttu-id="79f26-141">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="79f26-141">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="79f26-142">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="79f26-142">Can be Empty</span></span>  <br/> |<span data-ttu-id="79f26-143">False</span><span class="sxs-lookup"><span data-stu-id="79f26-143">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="79f26-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="79f26-144">See also</span></span>

- [<span data-ttu-id="79f26-145">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="79f26-145">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

