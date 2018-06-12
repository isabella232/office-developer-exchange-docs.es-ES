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
ms.openlocfilehash: f36ad646e6c2d415d14d4311a9971a56a85a3121
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836031"
---
# <a name="isgreaterthan"></a><span data-ttu-id="b39ae-103">IsGreaterThan</span><span class="sxs-lookup"><span data-stu-id="b39ae-103">IsGreaterThan</span></span>

<span data-ttu-id="b39ae-104">El elemento **IsGreaterThan** representa una expresión de búsqueda que se compara una propiedad con un valor constante o de otra propiedad y devuelve **true** si la primera propiedad es mayor.</span><span class="sxs-lookup"><span data-stu-id="b39ae-104">The **IsGreaterThan** element represents a search expression that compares a property with either a constant value or another property and returns **true** if the first property is greater.</span></span> 
  
```xml
<IsGreaterThan>
   <FieldURI/>
   <FieldURIOrConstant/>
</IsGreaterThan>
```

 <span data-ttu-id="b39ae-105">**IsGreaterThanType**</span><span class="sxs-lookup"><span data-stu-id="b39ae-105">**IsGreaterThanType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b39ae-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="b39ae-106">Attributes and elements</span></span>

<span data-ttu-id="b39ae-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="b39ae-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b39ae-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="b39ae-108">Attributes</span></span>

<span data-ttu-id="b39ae-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="b39ae-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b39ae-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b39ae-110">Child elements</span></span>

|<span data-ttu-id="b39ae-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="b39ae-111">**Element**</span></span>|<span data-ttu-id="b39ae-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b39ae-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b39ae-113">FieldURI</span><span class="sxs-lookup"><span data-stu-id="b39ae-113">FieldURI</span></span>](fielduri.md) <br/> |<span data-ttu-id="b39ae-114">Identifica las propiedades con frecuencia que se hace referencia mediante un identificador URI.</span><span class="sxs-lookup"><span data-stu-id="b39ae-114">Identifies frequently referenced properties by URI.</span></span>  <br/> |
|[<span data-ttu-id="b39ae-115">IndexedFieldURI</span><span class="sxs-lookup"><span data-stu-id="b39ae-115">IndexedFieldURI</span></span>](indexedfielduri.md) <br/> |<span data-ttu-id="b39ae-116">Identifica a los miembros individuales de un diccionario.</span><span class="sxs-lookup"><span data-stu-id="b39ae-116">Identifies individual members of a dictionary.</span></span>  <br/> |
|[<span data-ttu-id="b39ae-117">ExtendedFieldURI</span><span class="sxs-lookup"><span data-stu-id="b39ae-117">ExtendedFieldURI</span></span>](extendedfielduri.md) <br/> |<span data-ttu-id="b39ae-118">Identifica las propiedades MAPI.</span><span class="sxs-lookup"><span data-stu-id="b39ae-118">Identifies MAPI properties.</span></span>  <br/> |
|[<span data-ttu-id="b39ae-119">FieldURIOrConstant</span><span class="sxs-lookup"><span data-stu-id="b39ae-119">FieldURIOrConstant</span></span>](fielduriorconstant.md) <br/> |<span data-ttu-id="b39ae-120">Representa una propiedad o un valor constante que se usará cuando se comparan con otra propiedad.</span><span class="sxs-lookup"><span data-stu-id="b39ae-120">Represents either a property or a constant value to be used when comparing with another property.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="b39ae-121">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="b39ae-121">Parent elements</span></span>

|<span data-ttu-id="b39ae-122">**Element**</span><span class="sxs-lookup"><span data-stu-id="b39ae-122">**Element**</span></span>|<span data-ttu-id="b39ae-123">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b39ae-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b39ae-124">Restriction</span><span class="sxs-lookup"><span data-stu-id="b39ae-124">Restriction</span></span>](restriction.md) <br/> |<span data-ttu-id="b39ae-125">Representa la restricción o la consulta que se usa para filtrar los elementos o carpetas en las operaciones de carpeta FindItem/FindFolder y búsqueda.</span><span class="sxs-lookup"><span data-stu-id="b39ae-125">Represents the restriction or query that is used to filter items or folders in FindItem/FindFolder and search folder operations.</span></span>  <br/> |
|[<span data-ttu-id="b39ae-126">No</span><span class="sxs-lookup"><span data-stu-id="b39ae-126">Not</span></span>](not.md) <br/> |<span data-ttu-id="b39ae-127">Representa una expresión de búsqueda que niega el valor booleano de la expresión de búsqueda que contiene.</span><span class="sxs-lookup"><span data-stu-id="b39ae-127">Represents a search expression that negates the Boolean value of the search expression that it contains.</span></span>  <br/> |
|[<span data-ttu-id="b39ae-128">And</span><span class="sxs-lookup"><span data-stu-id="b39ae-128">And</span></span>](and.md) <br/> |<span data-ttu-id="b39ae-129">Representa una expresión de búsqueda que le permite realizar una operación de tipo Boolean y entre dos o más expresiones de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="b39ae-129">Represents a search expression that enables you to perform a Boolean And operation between two or more search expressions.</span></span> <span data-ttu-id="b39ae-130">El resultado de la operación And es **true** si se **cumplen**todas las expresiones de búsqueda incluidas en el y.</span><span class="sxs-lookup"><span data-stu-id="b39ae-130">The result of the And operation is **true** if all the search expressions contained within the And are **true**.</span></span>  <br/> |
|[<span data-ttu-id="b39ae-131">Or</span><span class="sxs-lookup"><span data-stu-id="b39ae-131">Or</span></span>](or.md) <br/> |<span data-ttu-id="b39ae-132">Representa una expresión de búsqueda que se realiza una operación OR lógica en la expresión de búsqueda que contiene.</span><span class="sxs-lookup"><span data-stu-id="b39ae-132">Represents a search expression that performs a logical OR on the search expression it contains.</span></span> <span data-ttu-id="b39ae-133">[O](or.md) devolverá **true** si cualquiera de sus elementos secundarios devuelven **true**.</span><span class="sxs-lookup"><span data-stu-id="b39ae-133">[Or](or.md) will return **true** if any of its children return **true**.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b39ae-134">Notas</span><span class="sxs-lookup"><span data-stu-id="b39ae-134">Remarks</span></span>

<span data-ttu-id="b39ae-135">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="b39ae-135">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b39ae-136">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="b39ae-136">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b39ae-137">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b39ae-137">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="b39ae-138">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="b39ae-138">Schema Name</span></span>  <br/> |<span data-ttu-id="b39ae-139">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="b39ae-139">Types schema</span></span>  <br/> |
|<span data-ttu-id="b39ae-140">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="b39ae-140">Validation File</span></span>  <br/> |<span data-ttu-id="b39ae-141">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="b39ae-141">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="b39ae-142">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="b39ae-142">Can be Empty</span></span>  <br/> |<span data-ttu-id="b39ae-143">False</span><span class="sxs-lookup"><span data-stu-id="b39ae-143">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b39ae-144">Ver también</span><span class="sxs-lookup"><span data-stu-id="b39ae-144">See also</span></span>



- [<span data-ttu-id="b39ae-145">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="b39ae-145">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

