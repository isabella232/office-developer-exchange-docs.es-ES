---
title: FieldURIOrConstant
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FieldURIOrConstant
api_type:
- schema
ms.assetid: 89d7a87e-7c93-49b8-83ec-8798e08c1052
description: El elemento FieldURIOrConstant representa una propiedad o un valor constante que se usará cuando se comparan con otra propiedad.
ms.openlocfilehash: 5195feec2a314d9ec15dc4a25a7a014aded1696a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764593"
---
# <a name="fielduriorconstant"></a><span data-ttu-id="ae822-103">FieldURIOrConstant</span><span class="sxs-lookup"><span data-stu-id="ae822-103">FieldURIOrConstant</span></span>

<span data-ttu-id="ae822-104">El elemento **FieldURIOrConstant** representa una propiedad o un valor constante que se usará cuando se comparan con otra propiedad.</span><span class="sxs-lookup"><span data-stu-id="ae822-104">The **FieldURIOrConstant** element represents either a property or a constant value to be used when comparing with another property.</span></span> 
  
```xml
<FieldURIOrConstant>
   <Constant/>
</FieldURIOrConstant>
```

 <span data-ttu-id="ae822-105">**FieldURIOrConstantType**</span><span class="sxs-lookup"><span data-stu-id="ae822-105">**FieldURIOrConstantType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ae822-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="ae822-106">Attributes and elements</span></span>

<span data-ttu-id="ae822-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="ae822-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ae822-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="ae822-108">Attributes</span></span>

<span data-ttu-id="ae822-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="ae822-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ae822-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ae822-110">Child elements</span></span>

|<span data-ttu-id="ae822-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="ae822-111">**Element**</span></span>|<span data-ttu-id="ae822-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ae822-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ae822-113">Constante</span><span class="sxs-lookup"><span data-stu-id="ae822-113">Constant</span></span>](constant.md) <br/> |<span data-ttu-id="ae822-114">Identifica un valor constante en una restricción.</span><span class="sxs-lookup"><span data-stu-id="ae822-114">Identifies a constant value in a restriction.</span></span>  <br/> |
|[<span data-ttu-id="ae822-115">FieldURI</span><span class="sxs-lookup"><span data-stu-id="ae822-115">FieldURI</span></span>](fielduri.md) <br/> |<span data-ttu-id="ae822-116">Identifica las propiedades con frecuencia que se hace referencia mediante un identificador URI.</span><span class="sxs-lookup"><span data-stu-id="ae822-116">Identifies frequently referenced properties by URI.</span></span>  <br/> |
|[<span data-ttu-id="ae822-117">IndexedFieldURI</span><span class="sxs-lookup"><span data-stu-id="ae822-117">IndexedFieldURI</span></span>](indexedfielduri.md) <br/> |<span data-ttu-id="ae822-118">Identifica a los miembros individuales de un diccionario.</span><span class="sxs-lookup"><span data-stu-id="ae822-118">Identifies individual members of a dictionary.</span></span>  <br/> |
|[<span data-ttu-id="ae822-119">ExtendedFieldURI</span><span class="sxs-lookup"><span data-stu-id="ae822-119">ExtendedFieldURI</span></span>](extendedfielduri.md) <br/> |<span data-ttu-id="ae822-120">Identifica las propiedades MAPI.</span><span class="sxs-lookup"><span data-stu-id="ae822-120">Identifies MAPI properties.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ae822-121">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="ae822-121">Parent elements</span></span>

|<span data-ttu-id="ae822-122">**Element**</span><span class="sxs-lookup"><span data-stu-id="ae822-122">**Element**</span></span>|<span data-ttu-id="ae822-123">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ae822-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ae822-124">IsEqualTo</span><span class="sxs-lookup"><span data-stu-id="ae822-124">IsEqualTo</span></span>](isequalto.md) <br/> |<span data-ttu-id="ae822-125">Representa una expresión de búsqueda que compara una propiedad con un valor constante u otra propiedad y se evalúa como true si son iguales.</span><span class="sxs-lookup"><span data-stu-id="ae822-125">Represents a search expression that compares a property with either a constant value or another property and evaluates to true if they are equal.</span></span>  <br/> |
|[<span data-ttu-id="ae822-126">IsGreaterThan</span><span class="sxs-lookup"><span data-stu-id="ae822-126">IsGreaterThan</span></span>](isgreaterthan.md) <br/> |<span data-ttu-id="ae822-127">Representa una expresión de búsqueda que compara una propiedad con un valor constante u otra propiedad y devuelve true si la primera propiedad es mayor.</span><span class="sxs-lookup"><span data-stu-id="ae822-127">Represents a search expression that compares a property with either a constant value or another property and returns true if the first property is greater.</span></span>  <br/> |
|[<span data-ttu-id="ae822-128">IsGreaterThanOrEqualTo</span><span class="sxs-lookup"><span data-stu-id="ae822-128">IsGreaterThanOrEqualTo</span></span>](isgreaterthanorequalto.md) <br/> |<span data-ttu-id="ae822-129">Representa una expresión de búsqueda que compara una propiedad con un valor constante u otra propiedad y devuelve true si la primera propiedad es mayor o igual que el segundo valor o propiedad.</span><span class="sxs-lookup"><span data-stu-id="ae822-129">Represents a search expression that compares a property with either a constant value or another property and returns true if the first property is greater than or equal to the second value or property.</span></span>  <br/> |
|[<span data-ttu-id="ae822-130">IsLessThan</span><span class="sxs-lookup"><span data-stu-id="ae822-130">IsLessThan</span></span>](islessthan.md) <br/> |<span data-ttu-id="ae822-131">Representa una expresión de búsqueda que compara una propiedad con un valor constante u otra propiedad y devuelve true si la primera propiedad es menor que el segundo valor o propiedad.</span><span class="sxs-lookup"><span data-stu-id="ae822-131">Represents a search expression that compares a property with either a constant value or another property and returns true if the first property is less than the second value or property.</span></span>  <br/> |
|[<span data-ttu-id="ae822-132">IsLessThanOrEqualTo</span><span class="sxs-lookup"><span data-stu-id="ae822-132">IsLessThanOrEqualTo</span></span>](islessthanorequalto.md) <br/> |<span data-ttu-id="ae822-133">Representa una expresión de búsqueda que compara una propiedad con un valor constante u otra propiedad y devuelve true si la primera propiedad es menor o igual que el segundo valor o propiedad.</span><span class="sxs-lookup"><span data-stu-id="ae822-133">Represents a search expression that compares a property with either a constant value or another property and returns true if the first property is less than or equal to the second value or property.</span></span>  <br/> |
|[<span data-ttu-id="ae822-134">IsNotEqualTo</span><span class="sxs-lookup"><span data-stu-id="ae822-134">IsNotEqualTo</span></span>](isnotequalto.md) <br/> |<span data-ttu-id="ae822-135">Representa una expresión de búsqueda que compara una propiedad con un valor constante u otra propiedad y devuelve true si los valores no son los mismos.</span><span class="sxs-lookup"><span data-stu-id="ae822-135">Represents a search expression that compares a property with either a constant value or another property and returns true if the values are not the same.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ae822-136">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ae822-136">Remarks</span></span>

<span data-ttu-id="ae822-137">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="ae822-137">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="example"></a><span data-ttu-id="ae822-138">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ae822-138">Example</span></span>

<span data-ttu-id="ae822-139">En el ejemplo de XML siguiente se muestra el elemento de FieldURIOrConstant que se utiliza con una constante y el campo URI.</span><span class="sxs-lookup"><span data-stu-id="ae822-139">The following XML example shows the FieldURIOrConstant element used with both a constant and field URI.</span></span>
  
```
[xml]
<Restriction>
  <Or xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
    <IsEqualTo>
      <FieldURI FieldURI="item:DateTimeCreated"/>
      <FieldURIOrConstant>
        <FieldURI FieldURI="item:DateTimeReceived"/>
      </FieldURIOrConstant>
    </IsEqualTo>
    <IsEqualTo>
      <FieldURI FieldURI="item:Subject"/>
      <FieldURIOrConstant>
        <Constant Value="Here is a test message"/>
      </FieldURIOrConstant>
    </IsEqualTo>
  </Or>
</Restriction>
```

## <a name="element-information"></a><span data-ttu-id="ae822-140">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="ae822-140">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ae822-141">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="ae822-141">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ae822-142">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="ae822-142">Schema Name</span></span>  <br/> |<span data-ttu-id="ae822-143">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="ae822-143">Types schema</span></span>  <br/> |
|<span data-ttu-id="ae822-144">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="ae822-144">Validation File</span></span>  <br/> |<span data-ttu-id="ae822-145">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="ae822-145">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="ae822-146">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="ae822-146">Can be Empty</span></span>  <br/> |<span data-ttu-id="ae822-147">False</span><span class="sxs-lookup"><span data-stu-id="ae822-147">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ae822-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="ae822-148">See also</span></span>



- [<span data-ttu-id="ae822-149">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="ae822-149">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

