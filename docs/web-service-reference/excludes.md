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
description: El elemento Excludes realiza una máscara bit a bit de la propiedad especificada y un valor proporcionado.
ms.openlocfilehash: d5fcd8b86b454aa731bd43974b5b7d674fe76ed6
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530617"
---
# <a name="excludes"></a><span data-ttu-id="7dd44-103">Excluye</span><span class="sxs-lookup"><span data-stu-id="7dd44-103">Excludes</span></span>

<span data-ttu-id="7dd44-104">El elemento **Excludes** realiza una máscara bit a bit de la propiedad especificada y un valor proporcionado.</span><span class="sxs-lookup"><span data-stu-id="7dd44-104">The **Excludes** element performs a bitwise mask of the specified property and a supplied value.</span></span> 
  
```xml
<Excludes>
   <FieldURI/>
   <Bitmask/>
</Excludes>
```

```xml
<Excludes>
   <ExtendedFieldURI/> 
   <Bitmask/>
</Excludes>
```

```xml
<Excludes>
   <IndexedFieldURI/> 
   <Bitmask/>
</Excludes>
```

<span data-ttu-id="7dd44-105">**ExcludesType**</span><span class="sxs-lookup"><span data-stu-id="7dd44-105">**ExcludesType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="7dd44-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="7dd44-106">Attributes and elements</span></span>

<span data-ttu-id="7dd44-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="7dd44-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7dd44-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="7dd44-108">Attributes</span></span>

<span data-ttu-id="7dd44-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="7dd44-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7dd44-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="7dd44-110">Child elements</span></span>

|<span data-ttu-id="7dd44-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="7dd44-111">**Element**</span></span>|<span data-ttu-id="7dd44-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7dd44-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7dd44-113">FieldURI</span><span class="sxs-lookup"><span data-stu-id="7dd44-113">FieldURI</span></span>](fielduri.md) <br/> |<span data-ttu-id="7dd44-114">Identifica las propiedades a las que se hace referencia con frecuencia mediante el URI.</span><span class="sxs-lookup"><span data-stu-id="7dd44-114">Identifies frequently referenced properties by URI.</span></span>  <br/> |
|[<span data-ttu-id="7dd44-115">IndexedFieldURI</span><span class="sxs-lookup"><span data-stu-id="7dd44-115">IndexedFieldURI</span></span>](indexedfielduri.md) <br/> |<span data-ttu-id="7dd44-116">Identifica a los miembros individuales de un diccionario.</span><span class="sxs-lookup"><span data-stu-id="7dd44-116">Identifies individual members of a dictionary.</span></span>  <br/> |
|[<span data-ttu-id="7dd44-117">ExtendedFieldURI</span><span class="sxs-lookup"><span data-stu-id="7dd44-117">ExtendedFieldURI</span></span>](extendedfielduri.md) <br/> |<span data-ttu-id="7dd44-118">Identifica las propiedades MAPI.</span><span class="sxs-lookup"><span data-stu-id="7dd44-118">Identifies MAPI properties.</span></span>  <br/> |
|[<span data-ttu-id="7dd44-119">Máscara</span><span class="sxs-lookup"><span data-stu-id="7dd44-119">Bitmask</span></span>](bitmask.md) <br/> |<span data-ttu-id="7dd44-120">Representa una máscara hexadecimal o decimal que se utilizará durante una operación de restricción de [exclusión](excludes.md) .</span><span class="sxs-lookup"><span data-stu-id="7dd44-120">Represents a hexadecimal or decimal mask to be used during an [Excludes](excludes.md) restriction operation.</span></span> <span data-ttu-id="7dd44-121">Si la máscara de la máscara representa un número hexadecimal, debe ir precedida de 0x o 0X.</span><span class="sxs-lookup"><span data-stu-id="7dd44-121">If the bitmask represents a hexadecimal number, it must be prefixed by 0x or 0X.</span></span> <span data-ttu-id="7dd44-122">De lo contrario, se considerará un número decimal.</span><span class="sxs-lookup"><span data-stu-id="7dd44-122">Otherwise, it will be considered a decimal number.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="7dd44-123">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="7dd44-123">Parent elements</span></span>

|<span data-ttu-id="7dd44-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="7dd44-124">**Element**</span></span>|<span data-ttu-id="7dd44-125">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7dd44-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7dd44-126">Restriction</span><span class="sxs-lookup"><span data-stu-id="7dd44-126">Restriction</span></span>](restriction.md) <br/> |<span data-ttu-id="7dd44-127">Representa la restricción o consulta que se usa para filtrar elementos o carpetas en las operaciones de carpeta de búsqueda FindItem/FindFolder.</span><span class="sxs-lookup"><span data-stu-id="7dd44-127">Represents the restriction or query that is used to filter items or folders in FindItem/FindFolder and search folder operations.</span></span>  <br/> |
|[<span data-ttu-id="7dd44-128">Not</span><span class="sxs-lookup"><span data-stu-id="7dd44-128">Not</span></span>](not.md) <br/> |<span data-ttu-id="7dd44-129">Representa una expresión de búsqueda que niega el valor booleano de la expresión de búsqueda que contiene.</span><span class="sxs-lookup"><span data-stu-id="7dd44-129">Represents a search expression that negates the Boolean value of the search expression that it contains.</span></span>  <br/> |
|[<span data-ttu-id="7dd44-130">And</span><span class="sxs-lookup"><span data-stu-id="7dd44-130">And</span></span>](and.md) <br/> |<span data-ttu-id="7dd44-131">Representa una expresión de búsqueda que permite realizar una operación and booleana entre dos o más expresiones de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="7dd44-131">Represents a search expression that allows you to perform a Boolean And operation between two or more search expressions.</span></span> <span data-ttu-id="7dd44-132">El resultado de la operación and es **true** si todas las expresiones de búsqueda incluidas en el y son **true**.</span><span class="sxs-lookup"><span data-stu-id="7dd44-132">The result of the And operation is **true** if all of the search expressions contained within the And are **true**.</span></span>  <br/> |
|[<span data-ttu-id="7dd44-133">Or</span><span class="sxs-lookup"><span data-stu-id="7dd44-133">Or</span></span>](or.md) <br/> |<span data-ttu-id="7dd44-134">Representa una expresión de búsqueda que realiza una operación lógica OR en la expresión de búsqueda que contiene.</span><span class="sxs-lookup"><span data-stu-id="7dd44-134">Represents a search expression that performs a logical OR on the search expression it contains.</span></span> <span data-ttu-id="7dd44-135">El elemento [o](or.md) devolverá **true** si cualquiera de sus secundarios devuelve **true**.</span><span class="sxs-lookup"><span data-stu-id="7dd44-135">The [Or](or.md) element will return **true** if any of its children return **true**.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7dd44-136">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7dd44-136">Remarks</span></span>

<span data-ttu-id="7dd44-137">**Exclude** se resolverá en **true** si una operación and realizada en el siguiente se resuelve en 0:</span><span class="sxs-lookup"><span data-stu-id="7dd44-137">**Excludes** will resolve to **true** if an AND operation performed on the following resolves to 0:</span></span> 
  
1. <span data-ttu-id="7dd44-138">El valor de bit a bit de la propiedad</span><span class="sxs-lookup"><span data-stu-id="7dd44-138">The bitwise value for the property</span></span>
    
2. <span data-ttu-id="7dd44-139">El valor de máscara de la propiedad</span><span class="sxs-lookup"><span data-stu-id="7dd44-139">The bitmask value for the property</span></span>
    
<span data-ttu-id="7dd44-140">**Exclude** solo se puede aplicar a una propiedad que tiene un valor entero.</span><span class="sxs-lookup"><span data-stu-id="7dd44-140">**Excludes** can only be applied to a property that has an integer value.</span></span> <span data-ttu-id="7dd44-141">Si el tipo de propiedad es distinto de un entero, se devuelve un código de error de **ErrorUnsupportedPathForQuery** en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7dd44-141">If the property type is anything other than an integer, an error code of **ErrorUnsupportedPathForQuery** is returned in the response.</span></span> 
  
<span data-ttu-id="7dd44-142">Puede realizar la operación inversa llamando a no (excluye).</span><span class="sxs-lookup"><span data-stu-id="7dd44-142">You can perform the reverse operation by calling Not(Excludes).</span></span>
  
<span data-ttu-id="7dd44-143">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="7dd44-143">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7dd44-144">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="7dd44-144">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7dd44-145">Namespace</span><span class="sxs-lookup"><span data-stu-id="7dd44-145">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="7dd44-146">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="7dd44-146">Schema Name</span></span>  <br/> |<span data-ttu-id="7dd44-147">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="7dd44-147">Types schema</span></span>  <br/> |
|<span data-ttu-id="7dd44-148">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="7dd44-148">Validation File</span></span>  <br/> |<span data-ttu-id="7dd44-149">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="7dd44-149">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="7dd44-150">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="7dd44-150">Can be Empty</span></span>  <br/> |<span data-ttu-id="7dd44-151">Falso</span><span class="sxs-lookup"><span data-stu-id="7dd44-151">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7dd44-152">Vea también</span><span class="sxs-lookup"><span data-stu-id="7dd44-152">See also</span></span>

- [<span data-ttu-id="7dd44-153">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="7dd44-153">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

