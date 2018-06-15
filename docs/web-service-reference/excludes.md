---
title: Excluye
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Excludes
api_type:
- schema
ms.assetid: bbaeddf6-9a67-4ee0-af99-7a7a5bbdc0e1
description: El elemento excluye realiza una máscara de bit a bit de la propiedad especificada y un valor suministrado.
ms.openlocfilehash: 73e4eb782a4f54c113ea9a9b67fcf185a9028153
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764481"
---
# <a name="excludes"></a><span data-ttu-id="4f4ce-103">Excluye</span><span class="sxs-lookup"><span data-stu-id="4f4ce-103">Excludes</span></span>

<span data-ttu-id="4f4ce-104">El elemento **excluye** realiza una máscara de bit a bit de la propiedad especificada y un valor suministrado.</span><span class="sxs-lookup"><span data-stu-id="4f4ce-104">The **Excludes** element performs a bitwise mask of the specified property and a supplied value.</span></span> 
  
```xml
<Excludes>
   <FieldURI/>
   <Bitmask/>
</Excludes>
```

 <span data-ttu-id="4f4ce-105">**ExcludesType**</span><span class="sxs-lookup"><span data-stu-id="4f4ce-105">**ExcludesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4f4ce-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="4f4ce-106">Attributes and elements</span></span>

<span data-ttu-id="4f4ce-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="4f4ce-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4f4ce-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="4f4ce-108">Attributes</span></span>

<span data-ttu-id="4f4ce-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="4f4ce-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4f4ce-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="4f4ce-110">Child elements</span></span>

|<span data-ttu-id="4f4ce-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="4f4ce-111">**Element**</span></span>|<span data-ttu-id="4f4ce-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4f4ce-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4f4ce-113">FieldURI</span><span class="sxs-lookup"><span data-stu-id="4f4ce-113">FieldURI</span></span>](fielduri.md) <br/> |<span data-ttu-id="4f4ce-114">Identifica las propiedades con frecuencia que se hace referencia mediante un identificador URI.</span><span class="sxs-lookup"><span data-stu-id="4f4ce-114">Identifies frequently referenced properties by URI.</span></span>  <br/> |
|[<span data-ttu-id="4f4ce-115">IndexedFieldURI</span><span class="sxs-lookup"><span data-stu-id="4f4ce-115">IndexedFieldURI</span></span>](indexedfielduri.md) <br/> |<span data-ttu-id="4f4ce-116">Identifica a los miembros individuales de un diccionario.</span><span class="sxs-lookup"><span data-stu-id="4f4ce-116">Identifies individual members of a dictionary.</span></span>  <br/> |
|[<span data-ttu-id="4f4ce-117">ExtendedFieldURI</span><span class="sxs-lookup"><span data-stu-id="4f4ce-117">ExtendedFieldURI</span></span>](extendedfielduri.md) <br/> |<span data-ttu-id="4f4ce-118">Identifica las propiedades MAPI.</span><span class="sxs-lookup"><span data-stu-id="4f4ce-118">Identifies MAPI properties.</span></span>  <br/> |
|[<span data-ttu-id="4f4ce-119">Máscara de bits</span><span class="sxs-lookup"><span data-stu-id="4f4ce-119">Bitmask</span></span>](bitmask.md) <br/> |<span data-ttu-id="4f4ce-120">Representa una máscara de hexadecimal o decimal que se utilizará durante una operación de restricción [excluye](excludes.md) .</span><span class="sxs-lookup"><span data-stu-id="4f4ce-120">Represents a hexadecimal or decimal mask to be used during an [Excludes](excludes.md) restriction operation.</span></span> <span data-ttu-id="4f4ce-121">Si la máscara de bits representa un número hexadecimal, deben ir precedido por 0 x o 0 X.</span><span class="sxs-lookup"><span data-stu-id="4f4ce-121">If the bitmask represents a hexadecimal number, it must be prefixed by 0x or 0X.</span></span> <span data-ttu-id="4f4ce-122">De lo contrario, se considerará un número decimal.</span><span class="sxs-lookup"><span data-stu-id="4f4ce-122">Otherwise, it will be considered a decimal number.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="4f4ce-123">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="4f4ce-123">Parent elements</span></span>

|<span data-ttu-id="4f4ce-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="4f4ce-124">**Element**</span></span>|<span data-ttu-id="4f4ce-125">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4f4ce-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4f4ce-126">Restriction</span><span class="sxs-lookup"><span data-stu-id="4f4ce-126">Restriction</span></span>](restriction.md) <br/> |<span data-ttu-id="4f4ce-127">Representa la restricción o la consulta que se usa para filtrar los elementos o carpetas en las operaciones de carpeta FindItem/FindFolder y búsqueda.</span><span class="sxs-lookup"><span data-stu-id="4f4ce-127">Represents the restriction or query that is used to filter items or folders in FindItem/FindFolder and search folder operations.</span></span>  <br/> |
|[<span data-ttu-id="4f4ce-128">No</span><span class="sxs-lookup"><span data-stu-id="4f4ce-128">Not</span></span>](not.md) <br/> |<span data-ttu-id="4f4ce-129">Representa una expresión de búsqueda que niega el valor booleano de la expresión de búsqueda que contiene.</span><span class="sxs-lookup"><span data-stu-id="4f4ce-129">Represents a search expression that negates the Boolean value of the search expression that it contains.</span></span>  <br/> |
|[<span data-ttu-id="4f4ce-130">And</span><span class="sxs-lookup"><span data-stu-id="4f4ce-130">And</span></span>](and.md) <br/> |<span data-ttu-id="4f4ce-131">Representa una expresión de búsqueda que le permite realizar una operación de tipo Boolean y entre dos o más expresiones de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="4f4ce-131">Represents a search expression that allows you to perform a Boolean And operation between two or more search expressions.</span></span> <span data-ttu-id="4f4ce-132">El resultado de la operación And es **true** si se **cumplen**todas las expresiones de búsqueda incluidas en el y.</span><span class="sxs-lookup"><span data-stu-id="4f4ce-132">The result of the And operation is **true** if all of the search expressions contained within the And are **true**.</span></span>  <br/> |
|[<span data-ttu-id="4f4ce-133">Or</span><span class="sxs-lookup"><span data-stu-id="4f4ce-133">Or</span></span>](or.md) <br/> |<span data-ttu-id="4f4ce-134">Representa una expresión de búsqueda que se realiza una operación OR lógica en la expresión de búsqueda que contiene.</span><span class="sxs-lookup"><span data-stu-id="4f4ce-134">Represents a search expression that performs a logical OR on the search expression it contains.</span></span> <span data-ttu-id="4f4ce-135">El elemento [o](or.md) devolverá **true** si cualquiera de sus elementos secundarios que devuelva **true**.</span><span class="sxs-lookup"><span data-stu-id="4f4ce-135">The [Or](or.md) element will return **true** if any of its children return **true**.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4f4ce-136">Notas</span><span class="sxs-lookup"><span data-stu-id="4f4ce-136">Remarks</span></span>

 <span data-ttu-id="4f4ce-137">**Excluye** se puede resolver en **true** si y realizada una operación en la siguiente se resuelve en 0:</span><span class="sxs-lookup"><span data-stu-id="4f4ce-137">**Excludes** will resolve to **true** if an AND operation performed on the following resolves to 0:</span></span> 
  
1. <span data-ttu-id="4f4ce-138">El valor de la propiedad bit a bit</span><span class="sxs-lookup"><span data-stu-id="4f4ce-138">The bitwise value for the property</span></span>
    
2. <span data-ttu-id="4f4ce-139">El valor de máscara de bits para la propiedad</span><span class="sxs-lookup"><span data-stu-id="4f4ce-139">The bitmask value for the property</span></span>
    
 <span data-ttu-id="4f4ce-140">**Excluye** solo se puede aplicar a una propiedad que tiene un valor entero.</span><span class="sxs-lookup"><span data-stu-id="4f4ce-140">**Excludes** can only be applied to a property that has an integer value.</span></span> <span data-ttu-id="4f4ce-141">Si el tipo de propiedad no es un entero, se devuelve un código de error de **ErrorUnsupportedPathForQuery** en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4f4ce-141">If the property type is anything other than an integer, an error code of **ErrorUnsupportedPathForQuery** is returned in the response.</span></span> 
  
<span data-ttu-id="4f4ce-142">Puede realizar la operación inversa mediante una llamada a Not(Excludes).</span><span class="sxs-lookup"><span data-stu-id="4f4ce-142">You can perform the reverse operation by calling Not(Excludes).</span></span>
  
<span data-ttu-id="4f4ce-143">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="4f4ce-143">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4f4ce-144">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="4f4ce-144">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4f4ce-145">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="4f4ce-145">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="4f4ce-146">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="4f4ce-146">Schema Name</span></span>  <br/> |<span data-ttu-id="4f4ce-147">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="4f4ce-147">Types schema</span></span>  <br/> |
|<span data-ttu-id="4f4ce-148">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="4f4ce-148">Validation File</span></span>  <br/> |<span data-ttu-id="4f4ce-149">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="4f4ce-149">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="4f4ce-150">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="4f4ce-150">Can be Empty</span></span>  <br/> |<span data-ttu-id="4f4ce-151">False</span><span class="sxs-lookup"><span data-stu-id="4f4ce-151">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4f4ce-152">Ver también</span><span class="sxs-lookup"><span data-stu-id="4f4ce-152">See also</span></span>



- [<span data-ttu-id="4f4ce-153">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="4f4ce-153">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
