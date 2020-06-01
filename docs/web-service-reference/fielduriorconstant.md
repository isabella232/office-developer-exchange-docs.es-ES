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
description: El elemento FieldURIOrConstant representa una propiedad o un valor constante que se utilizará al comparar con otra propiedad.
ms.openlocfilehash: 8b5cb888a3bd2026b15e38fc8c005ab5ef5a2b11
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461229"
---
# <a name="fielduriorconstant"></a><span data-ttu-id="e5053-103">FieldURIOrConstant</span><span class="sxs-lookup"><span data-stu-id="e5053-103">FieldURIOrConstant</span></span>

<span data-ttu-id="e5053-104">El elemento **FieldURIOrConstant** representa una propiedad o un valor constante que se utilizará al comparar con otra propiedad.</span><span class="sxs-lookup"><span data-stu-id="e5053-104">The **FieldURIOrConstant** element represents either a property or a constant value to be used when comparing with another property.</span></span> 
  
```xml
<FieldURIOrConstant>
   <Constant/>
</FieldURIOrConstant>
```

```xml
<FieldURIOrConstant>
    <IndexedFieldURI/> 
</FieldURIOrConstant>
```

```xml
<FieldURIOrConstant>
   <FieldURI/>
</FieldURIOrConstant>
```

```xml
<FieldURIOrConstant>
   <ExtendedFieldURI/> 
</FieldURIOrConstant>
```

<span data-ttu-id="e5053-105">**FieldURIOrConstantType**</span><span class="sxs-lookup"><span data-stu-id="e5053-105">**FieldURIOrConstantType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="e5053-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="e5053-106">Attributes and elements</span></span>

<span data-ttu-id="e5053-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="e5053-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e5053-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="e5053-108">Attributes</span></span>

<span data-ttu-id="e5053-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="e5053-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e5053-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="e5053-110">Child elements</span></span>

|<span data-ttu-id="e5053-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="e5053-111">**Element**</span></span>|<span data-ttu-id="e5053-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e5053-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e5053-113">Constante</span><span class="sxs-lookup"><span data-stu-id="e5053-113">Constant</span></span>](constant.md) <br/> |<span data-ttu-id="e5053-114">Identifica un valor constante en una restricción.</span><span class="sxs-lookup"><span data-stu-id="e5053-114">Identifies a constant value in a restriction.</span></span>  <br/> |
|[<span data-ttu-id="e5053-115">FieldURI</span><span class="sxs-lookup"><span data-stu-id="e5053-115">FieldURI</span></span>](fielduri.md) <br/> |<span data-ttu-id="e5053-116">Identifica las propiedades a las que se hace referencia con frecuencia mediante el URI.</span><span class="sxs-lookup"><span data-stu-id="e5053-116">Identifies frequently referenced properties by URI.</span></span>  <br/> |
|[<span data-ttu-id="e5053-117">IndexedFieldURI</span><span class="sxs-lookup"><span data-stu-id="e5053-117">IndexedFieldURI</span></span>](indexedfielduri.md) <br/> |<span data-ttu-id="e5053-118">Identifica a los miembros individuales de un diccionario.</span><span class="sxs-lookup"><span data-stu-id="e5053-118">Identifies individual members of a dictionary.</span></span>  <br/> |
|[<span data-ttu-id="e5053-119">ExtendedFieldURI</span><span class="sxs-lookup"><span data-stu-id="e5053-119">ExtendedFieldURI</span></span>](extendedfielduri.md) <br/> |<span data-ttu-id="e5053-120">Identifica las propiedades MAPI.</span><span class="sxs-lookup"><span data-stu-id="e5053-120">Identifies MAPI properties.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="e5053-121">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="e5053-121">Parent elements</span></span>

|<span data-ttu-id="e5053-122">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="e5053-122">**Element**</span></span>|<span data-ttu-id="e5053-123">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e5053-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e5053-124">IsEqualTo</span><span class="sxs-lookup"><span data-stu-id="e5053-124">IsEqualTo</span></span>](isequalto.md) <br/> |<span data-ttu-id="e5053-125">Representa una expresión de búsqueda que compara una propiedad con un valor constante u otra propiedad y evalúa en true si son iguales.</span><span class="sxs-lookup"><span data-stu-id="e5053-125">Represents a search expression that compares a property with either a constant value or another property and evaluates to true if they are equal.</span></span>  <br/> |
|[<span data-ttu-id="e5053-126">IsGreaterThan</span><span class="sxs-lookup"><span data-stu-id="e5053-126">IsGreaterThan</span></span>](isgreaterthan.md) <br/> |<span data-ttu-id="e5053-127">Representa una expresión de búsqueda que compara una propiedad con un valor constante u otra propiedad y devuelve true si la primera propiedad es mayor.</span><span class="sxs-lookup"><span data-stu-id="e5053-127">Represents a search expression that compares a property with either a constant value or another property and returns true if the first property is greater.</span></span>  <br/> |
|[<span data-ttu-id="e5053-128">IsGreaterThanOrEqualTo</span><span class="sxs-lookup"><span data-stu-id="e5053-128">IsGreaterThanOrEqualTo</span></span>](isgreaterthanorequalto.md) <br/> |<span data-ttu-id="e5053-129">Representa una expresión de búsqueda que compara una propiedad con un valor constante u otra propiedad y devuelve true si la primera propiedad es mayor o igual que el segundo valor o propiedad.</span><span class="sxs-lookup"><span data-stu-id="e5053-129">Represents a search expression that compares a property with either a constant value or another property and returns true if the first property is greater than or equal to the second value or property.</span></span>  <br/> |
|[<span data-ttu-id="e5053-130">IsLessThan</span><span class="sxs-lookup"><span data-stu-id="e5053-130">IsLessThan</span></span>](islessthan.md) <br/> |<span data-ttu-id="e5053-131">Representa una expresión de búsqueda que compara una propiedad con un valor constante u otra propiedad y devuelve true si la primera propiedad es menor que el segundo valor o propiedad.</span><span class="sxs-lookup"><span data-stu-id="e5053-131">Represents a search expression that compares a property with either a constant value or another property and returns true if the first property is less than the second value or property.</span></span>  <br/> |
|[<span data-ttu-id="e5053-132">IsLessThanOrEqualTo</span><span class="sxs-lookup"><span data-stu-id="e5053-132">IsLessThanOrEqualTo</span></span>](islessthanorequalto.md) <br/> |<span data-ttu-id="e5053-133">Representa una expresión de búsqueda que compara una propiedad con un valor constante u otra propiedad y devuelve true si la primera propiedad es menor o igual que el segundo valor o propiedad.</span><span class="sxs-lookup"><span data-stu-id="e5053-133">Represents a search expression that compares a property with either a constant value or another property and returns true if the first property is less than or equal to the second value or property.</span></span>  <br/> |
|[<span data-ttu-id="e5053-134">IsNotEqualTo</span><span class="sxs-lookup"><span data-stu-id="e5053-134">IsNotEqualTo</span></span>](isnotequalto.md) <br/> |<span data-ttu-id="e5053-135">Representa una expresión de búsqueda que compara una propiedad con un valor constante u otra propiedad y devuelve true si los valores no son los mismos.</span><span class="sxs-lookup"><span data-stu-id="e5053-135">Represents a search expression that compares a property with either a constant value or another property and returns true if the values are not the same.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e5053-136">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e5053-136">Remarks</span></span>

<span data-ttu-id="e5053-137">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="e5053-137">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="example"></a><span data-ttu-id="e5053-138">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e5053-138">Example</span></span>

<span data-ttu-id="e5053-139">El siguiente ejemplo de XML muestra el elemento FieldURIOrConstant usado con una constante y un URI de campo.</span><span class="sxs-lookup"><span data-stu-id="e5053-139">The following XML example shows the FieldURIOrConstant element used with both a constant and field URI.</span></span>
  
```xml
<Restriction>
  <Or xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
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

## <a name="element-information"></a><span data-ttu-id="e5053-140">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="e5053-140">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e5053-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="e5053-141">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="e5053-142">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="e5053-142">Schema Name</span></span>  <br/> |<span data-ttu-id="e5053-143">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="e5053-143">Types schema</span></span>  <br/> |
|<span data-ttu-id="e5053-144">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="e5053-144">Validation File</span></span>  <br/> |<span data-ttu-id="e5053-145">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="e5053-145">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="e5053-146">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="e5053-146">Can be Empty</span></span>  <br/> |<span data-ttu-id="e5053-147">Falso</span><span class="sxs-lookup"><span data-stu-id="e5053-147">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e5053-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="e5053-148">See also</span></span>

- [<span data-ttu-id="e5053-149">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="e5053-149">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

