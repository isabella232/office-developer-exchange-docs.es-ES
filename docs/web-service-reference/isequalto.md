---
title: IsEqualTo
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsEqualTo
api_type:
- schema
ms.assetid: 48e7e067-049c-4184-8026-071e6f558e8a
description: El elemento IsEqualTo representa una expresión de búsqueda que compara una propiedad con un valor constante u otra propiedad, y evalúa en true si son iguales.
ms.openlocfilehash: 857192443ab0520bb26ead399bc5364cc862a4fb
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44455299"
---
# <a name="isequalto"></a><span data-ttu-id="fa099-103">IsEqualTo</span><span class="sxs-lookup"><span data-stu-id="fa099-103">IsEqualTo</span></span>

<span data-ttu-id="fa099-104">El elemento **IsEqualTo** representa una expresión de búsqueda que compara una propiedad con un valor constante u otra propiedad, y evalúa en true si son iguales.</span><span class="sxs-lookup"><span data-stu-id="fa099-104">The **IsEqualTo** element represents a search expression that compares a property with either a constant value or another property and evaluates to true if they are equal.</span></span> 
  
```xml
<IsEqualTo>
   <FieldURI/>
   <FieldURIOrConstant/>
</IsEqualTo>
```

```xml
<IsEqualTo>
   <ExtendedFieldURI/>
   <FieldURIOrConstant/>
</IsEqualTo>
```

```xml
<IsEqualTo>
   <IndexedFieldURI/> 
   <FieldURIOrConstant/>
</IsEqualTo>
```

<span data-ttu-id="fa099-105">**IsEqualToType**</span><span class="sxs-lookup"><span data-stu-id="fa099-105">**IsEqualToType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="fa099-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="fa099-106">Attributes and elements</span></span>

<span data-ttu-id="fa099-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="fa099-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fa099-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="fa099-108">Attributes</span></span>

<span data-ttu-id="fa099-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="fa099-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="fa099-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="fa099-110">Child elements</span></span>

|<span data-ttu-id="fa099-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="fa099-111">**Element**</span></span>|<span data-ttu-id="fa099-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="fa099-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fa099-113">FieldURI</span><span class="sxs-lookup"><span data-stu-id="fa099-113">FieldURI</span></span>](fielduri.md) <br/> |<span data-ttu-id="fa099-114">Identifica las propiedades a las que se hace referencia con frecuencia mediante el URI.</span><span class="sxs-lookup"><span data-stu-id="fa099-114">Identifies frequently referenced properties by URI.</span></span>  <br/> |
|[<span data-ttu-id="fa099-115">IndexedFieldURI</span><span class="sxs-lookup"><span data-stu-id="fa099-115">IndexedFieldURI</span></span>](indexedfielduri.md) <br/> |<span data-ttu-id="fa099-116">Identifica a los miembros individuales de un diccionario.</span><span class="sxs-lookup"><span data-stu-id="fa099-116">Identifies individual members of a dictionary.</span></span>  <br/> |
|[<span data-ttu-id="fa099-117">ExtendedFieldURI</span><span class="sxs-lookup"><span data-stu-id="fa099-117">ExtendedFieldURI</span></span>](extendedfielduri.md) <br/> |<span data-ttu-id="fa099-118">Identifica las propiedades MAPI.</span><span class="sxs-lookup"><span data-stu-id="fa099-118">Identifies MAPI properties.</span></span>  <br/> |
|[<span data-ttu-id="fa099-119">FieldURIOrConstant</span><span class="sxs-lookup"><span data-stu-id="fa099-119">FieldURIOrConstant</span></span>](fielduriorconstant.md) <br/> |<span data-ttu-id="fa099-120">Representa una propiedad o un valor constante que se utilizará al comparar con otra propiedad.</span><span class="sxs-lookup"><span data-stu-id="fa099-120">Represents either a property or a constant value to be used when comparing with another property.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="fa099-121">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="fa099-121">Parent elements</span></span>

|<span data-ttu-id="fa099-122">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="fa099-122">**Element**</span></span>|<span data-ttu-id="fa099-123">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="fa099-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fa099-124">Restriction</span><span class="sxs-lookup"><span data-stu-id="fa099-124">Restriction</span></span>](restriction.md) <br/> |<span data-ttu-id="fa099-125">Representa la restricción o consulta que se usa para filtrar elementos o carpetas en las operaciones de carpeta de búsqueda FindItem/FindFolder.</span><span class="sxs-lookup"><span data-stu-id="fa099-125">Represents the restriction or query that is used to filter items or folders in FindItem/FindFolder and search folder operations.</span></span>  <br/> |
|[<span data-ttu-id="fa099-126">Not</span><span class="sxs-lookup"><span data-stu-id="fa099-126">Not</span></span>](not.md) <br/> |<span data-ttu-id="fa099-127">Representa una expresión de búsqueda que niega el valor booleano de la expresión de búsqueda que contiene.</span><span class="sxs-lookup"><span data-stu-id="fa099-127">Represents a search expression that negates the Boolean value of the search expression that it contains.</span></span>  <br/> |
|[<span data-ttu-id="fa099-128">And</span><span class="sxs-lookup"><span data-stu-id="fa099-128">And</span></span>](and.md) <br/> |<span data-ttu-id="fa099-129">Representa una expresión de búsqueda que permite realizar una operación and booleana entre dos o más expresiones de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="fa099-129">Represents a search expression that allows you to perform a Boolean And operation between two or more search expressions.</span></span> <span data-ttu-id="fa099-130">El resultado de la operación and es **true** si todas las expresiones de búsqueda incluidas en el y son **true**.</span><span class="sxs-lookup"><span data-stu-id="fa099-130">The result of the And operation is **true** if all of the search expressions contained within the And are **true**.</span></span>  <br/> |
|[<span data-ttu-id="fa099-131">Or</span><span class="sxs-lookup"><span data-stu-id="fa099-131">Or</span></span>](or.md) <br/> |<span data-ttu-id="fa099-132">Representa una expresión de búsqueda que realiza una operación lógica OR en la expresión de búsqueda que contiene.</span><span class="sxs-lookup"><span data-stu-id="fa099-132">Represents a search expression that performs a logical OR on the search expression that it contains.</span></span> <span data-ttu-id="fa099-133">[O](or.md) devuelve true si cualquiera de sus elementos secundarios devuelve true.</span><span class="sxs-lookup"><span data-stu-id="fa099-133">[Or](or.md) will return true if any of its children return true.</span></span> <span data-ttu-id="fa099-134">**O** debe tener dos o más elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="fa099-134">**Or** must have two or more children.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fa099-135">Comentarios</span><span class="sxs-lookup"><span data-stu-id="fa099-135">Remarks</span></span>

<span data-ttu-id="fa099-136">Para realizar comparaciones de cadenas, considere la posibilidad de usar el elemento [Contains](contains.md) , ya que proporciona opciones para los parámetros coincidentes, como los espacios en blanco y los mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="fa099-136">To perform string comparisons, consider using the [Contains](contains.md) element, as it provides options for matching parameters, such as case and white space.</span></span> <span data-ttu-id="fa099-137">Use el elemento [Not](not.md) en combinación con el elemento [Contains](contains.md) para negar el resultado.</span><span class="sxs-lookup"><span data-stu-id="fa099-137">Use the [Not](not.md) element in conjunction with the [Contains](contains.md) element to negate the result.</span></span> 
  
<span data-ttu-id="fa099-138">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="fa099-138">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fa099-139">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="fa099-139">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fa099-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="fa099-140">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="fa099-141">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="fa099-141">Schema Name</span></span>  <br/> |<span data-ttu-id="fa099-142">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="fa099-142">Types schema</span></span>  <br/> |
|<span data-ttu-id="fa099-143">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="fa099-143">Validation File</span></span>  <br/> |<span data-ttu-id="fa099-144">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="fa099-144">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="fa099-145">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="fa099-145">Can be Empty</span></span>  <br/> |<span data-ttu-id="fa099-146">Falso</span><span class="sxs-lookup"><span data-stu-id="fa099-146">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fa099-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="fa099-147">See also</span></span>

- [<span data-ttu-id="fa099-148">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="fa099-148">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

