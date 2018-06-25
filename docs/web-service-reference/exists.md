---
title: Exists
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Exists
api_type:
- schema
ms.assetid: 55d568bd-8dbc-4d50-b9d7-54b74a54d4b5
description: El elemento Exists representa una expresión de búsqueda que devuelve true si existe la propiedad proporcionada en un elemento.
ms.openlocfilehash: d30f4b505afcac32afbfeaf2289c964ba145668e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764484"
---
# <a name="exists"></a><span data-ttu-id="2833c-103">Exists</span><span class="sxs-lookup"><span data-stu-id="2833c-103">Exists</span></span>

<span data-ttu-id="2833c-104">El elemento **Exists** representa una expresión de búsqueda que devuelve **true** si existe la propiedad proporcionada en un elemento.</span><span class="sxs-lookup"><span data-stu-id="2833c-104">The **Exists** element represents a search expression that returns **true** if the supplied property exists on an item.</span></span> 
  
```xml
<Exists>
   <Path/>
</Exists>
```

 <span data-ttu-id="2833c-105">**ExistsType**</span><span class="sxs-lookup"><span data-stu-id="2833c-105">**ExistsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2833c-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="2833c-106">Attributes and elements</span></span>

<span data-ttu-id="2833c-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="2833c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2833c-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="2833c-108">Attributes</span></span>

<span data-ttu-id="2833c-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="2833c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2833c-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="2833c-110">Child elements</span></span>

|<span data-ttu-id="2833c-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="2833c-111">**Element**</span></span>|<span data-ttu-id="2833c-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2833c-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2833c-113">FieldURI</span><span class="sxs-lookup"><span data-stu-id="2833c-113">FieldURI</span></span>](fielduri.md) <br/> |<span data-ttu-id="2833c-114">Identifica las propiedades con frecuencia que se hace referencia mediante un identificador URI.</span><span class="sxs-lookup"><span data-stu-id="2833c-114">Identifies frequently referenced properties by URI.</span></span>  <br/> |
|[<span data-ttu-id="2833c-115">IndexedFieldURI</span><span class="sxs-lookup"><span data-stu-id="2833c-115">IndexedFieldURI</span></span>](indexedfielduri.md) <br/> |<span data-ttu-id="2833c-116">Identifica a los miembros individuales de un diccionario.</span><span class="sxs-lookup"><span data-stu-id="2833c-116">Identifies individual members of a dictionary.</span></span>  <br/> |
|[<span data-ttu-id="2833c-117">ExtendedFieldURI</span><span class="sxs-lookup"><span data-stu-id="2833c-117">ExtendedFieldURI</span></span>](extendedfielduri.md) <br/> |<span data-ttu-id="2833c-118">Identifica las propiedades MAPI.</span><span class="sxs-lookup"><span data-stu-id="2833c-118">Identifies MAPI properties.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="2833c-119">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="2833c-119">Parent elements</span></span>

|<span data-ttu-id="2833c-120">**Element**</span><span class="sxs-lookup"><span data-stu-id="2833c-120">**Element**</span></span>|<span data-ttu-id="2833c-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2833c-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2833c-122">Restriction</span><span class="sxs-lookup"><span data-stu-id="2833c-122">Restriction</span></span>](restriction.md) <br/> |<span data-ttu-id="2833c-123">Representa la restricción o la consulta que se usa para filtrar los elementos o carpetas en las operaciones de carpeta FindItem/FindFolder y búsqueda.</span><span class="sxs-lookup"><span data-stu-id="2833c-123">Represents the restriction or query that is used to filter items or folders in FindItem/FindFolder and search folder operations.</span></span>  <br/> |
|[<span data-ttu-id="2833c-124">No</span><span class="sxs-lookup"><span data-stu-id="2833c-124">Not</span></span>](not.md) <br/> |<span data-ttu-id="2833c-125">Representa una expresión de búsqueda que niega el valor booleano de la expresión de búsqueda que contiene.</span><span class="sxs-lookup"><span data-stu-id="2833c-125">Represents a search expression that negates the Boolean value of the search expression that it contains.</span></span>  <br/> |
|[<span data-ttu-id="2833c-126">And</span><span class="sxs-lookup"><span data-stu-id="2833c-126">And</span></span>](and.md) <br/> |<span data-ttu-id="2833c-127">Representa una expresión de búsqueda que le permite realizar una operación de tipo Boolean y entre dos o más expresiones de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="2833c-127">Represents a search expression that enables you to perform a Boolean And operation between two or more search expressions.</span></span> <span data-ttu-id="2833c-128">El resultado de la operación And es **true** si se **cumplen**todas las expresiones de búsqueda incluidas en el y.</span><span class="sxs-lookup"><span data-stu-id="2833c-128">The result of the And operation is **true** if all the search expressions contained within the And are **true**.</span></span>  <br/> |
|[<span data-ttu-id="2833c-129">Or</span><span class="sxs-lookup"><span data-stu-id="2833c-129">Or</span></span>](or.md) <br/> |<span data-ttu-id="2833c-130">Representa una expresión de búsqueda que se realiza una operación OR lógica en la expresión de búsqueda que contiene.</span><span class="sxs-lookup"><span data-stu-id="2833c-130">Represents a search expression that performs a logical OR on the search expression that it contains.</span></span> <span data-ttu-id="2833c-131">[O](or.md) devolverá **true** si cualquiera de sus elementos secundarios devuelven **true**.</span><span class="sxs-lookup"><span data-stu-id="2833c-131">[Or](or.md) will return **true** if any of its children return **true**.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2833c-132">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2833c-132">Remarks</span></span>

<span data-ttu-id="2833c-133">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="2833c-133">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2833c-134">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="2833c-134">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2833c-135">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="2833c-135">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="2833c-136">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="2833c-136">Schema Name</span></span>  <br/> |<span data-ttu-id="2833c-137">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="2833c-137">Types schema</span></span>  <br/> |
|<span data-ttu-id="2833c-138">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="2833c-138">Validation File</span></span>  <br/> |<span data-ttu-id="2833c-139">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="2833c-139">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="2833c-140">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="2833c-140">Can be Empty</span></span>  <br/> |<span data-ttu-id="2833c-141">False</span><span class="sxs-lookup"><span data-stu-id="2833c-141">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2833c-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="2833c-142">See also</span></span>



- [<span data-ttu-id="2833c-143">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="2833c-143">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

