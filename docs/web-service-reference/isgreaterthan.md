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
ms.openlocfilehash: 52f2c1b84e4072649092637de091c0dbd8187032
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530046"
---
# <a name="isgreaterthan"></a><span data-ttu-id="59387-103">IsGreaterThan</span><span class="sxs-lookup"><span data-stu-id="59387-103">IsGreaterThan</span></span>

<span data-ttu-id="59387-104">El elemento **IsGreaterThan** representa una expresión de búsqueda que compara una propiedad con un valor constante u otra propiedad y devuelve **true** si la primera propiedad es mayor.</span><span class="sxs-lookup"><span data-stu-id="59387-104">The **IsGreaterThan** element represents a search expression that compares a property with either a constant value or another property and returns **true** if the first property is greater.</span></span> 
  
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

<span data-ttu-id="59387-105">**IsGreaterThanType**</span><span class="sxs-lookup"><span data-stu-id="59387-105">**IsGreaterThanType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="59387-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="59387-106">Attributes and elements</span></span>

<span data-ttu-id="59387-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="59387-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="59387-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="59387-108">Attributes</span></span>

<span data-ttu-id="59387-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="59387-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="59387-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="59387-110">Child elements</span></span>

|<span data-ttu-id="59387-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="59387-111">**Element**</span></span>|<span data-ttu-id="59387-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="59387-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="59387-113">FieldURI</span><span class="sxs-lookup"><span data-stu-id="59387-113">FieldURI</span></span>](fielduri.md) <br/> |<span data-ttu-id="59387-114">Identifica las propiedades a las que se hace referencia con frecuencia mediante el URI.</span><span class="sxs-lookup"><span data-stu-id="59387-114">Identifies frequently referenced properties by URI.</span></span>  <br/> |
|[<span data-ttu-id="59387-115">IndexedFieldURI</span><span class="sxs-lookup"><span data-stu-id="59387-115">IndexedFieldURI</span></span>](indexedfielduri.md) <br/> |<span data-ttu-id="59387-116">Identifica a los miembros individuales de un diccionario.</span><span class="sxs-lookup"><span data-stu-id="59387-116">Identifies individual members of a dictionary.</span></span>  <br/> |
|[<span data-ttu-id="59387-117">ExtendedFieldURI</span><span class="sxs-lookup"><span data-stu-id="59387-117">ExtendedFieldURI</span></span>](extendedfielduri.md) <br/> |<span data-ttu-id="59387-118">Identifica las propiedades MAPI.</span><span class="sxs-lookup"><span data-stu-id="59387-118">Identifies MAPI properties.</span></span>  <br/> |
|[<span data-ttu-id="59387-119">FieldURIOrConstant</span><span class="sxs-lookup"><span data-stu-id="59387-119">FieldURIOrConstant</span></span>](fielduriorconstant.md) <br/> |<span data-ttu-id="59387-120">Representa una propiedad o un valor constante que se utilizará al comparar con otra propiedad.</span><span class="sxs-lookup"><span data-stu-id="59387-120">Represents either a property or a constant value to be used when comparing with another property.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="59387-121">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="59387-121">Parent elements</span></span>

|<span data-ttu-id="59387-122">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="59387-122">**Element**</span></span>|<span data-ttu-id="59387-123">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="59387-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="59387-124">Restriction</span><span class="sxs-lookup"><span data-stu-id="59387-124">Restriction</span></span>](restriction.md) <br/> |<span data-ttu-id="59387-125">Representa la restricción o consulta que se usa para filtrar elementos o carpetas en las operaciones de carpeta de búsqueda FindItem/FindFolder.</span><span class="sxs-lookup"><span data-stu-id="59387-125">Represents the restriction or query that is used to filter items or folders in FindItem/FindFolder and search folder operations.</span></span>  <br/> |
|[<span data-ttu-id="59387-126">Not</span><span class="sxs-lookup"><span data-stu-id="59387-126">Not</span></span>](not.md) <br/> |<span data-ttu-id="59387-127">Representa una expresión de búsqueda que niega el valor booleano de la expresión de búsqueda que contiene.</span><span class="sxs-lookup"><span data-stu-id="59387-127">Represents a search expression that negates the Boolean value of the search expression that it contains.</span></span>  <br/> |
|[<span data-ttu-id="59387-128">And</span><span class="sxs-lookup"><span data-stu-id="59387-128">And</span></span>](and.md) <br/> |<span data-ttu-id="59387-129">Representa una expresión de búsqueda que permite realizar una operación and booleana entre dos o más expresiones de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="59387-129">Represents a search expression that enables you to perform a Boolean And operation between two or more search expressions.</span></span> <span data-ttu-id="59387-130">El resultado de la operación and es **true** si todas las expresiones de búsqueda incluidas en el y son **true**.</span><span class="sxs-lookup"><span data-stu-id="59387-130">The result of the And operation is **true** if all the search expressions contained within the And are **true**.</span></span>  <br/> |
|[<span data-ttu-id="59387-131">Or</span><span class="sxs-lookup"><span data-stu-id="59387-131">Or</span></span>](or.md) <br/> |<span data-ttu-id="59387-132">Representa una expresión de búsqueda que realiza una operación lógica OR en la expresión de búsqueda que contiene.</span><span class="sxs-lookup"><span data-stu-id="59387-132">Represents a search expression that performs a logical OR on the search expression it contains.</span></span> <span data-ttu-id="59387-133">[O](or.md) devuelve **true** si cualquiera de sus elementos secundarios devuelve **true**.</span><span class="sxs-lookup"><span data-stu-id="59387-133">[Or](or.md) will return **true** if any of its children return **true**.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="59387-134">Comentarios</span><span class="sxs-lookup"><span data-stu-id="59387-134">Remarks</span></span>

<span data-ttu-id="59387-135">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="59387-135">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="59387-136">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="59387-136">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="59387-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="59387-137">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="59387-138">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="59387-138">Schema Name</span></span>  <br/> |<span data-ttu-id="59387-139">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="59387-139">Types schema</span></span>  <br/> |
|<span data-ttu-id="59387-140">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="59387-140">Validation File</span></span>  <br/> |<span data-ttu-id="59387-141">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="59387-141">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="59387-142">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="59387-142">Can be Empty</span></span>  <br/> |<span data-ttu-id="59387-143">Falso</span><span class="sxs-lookup"><span data-stu-id="59387-143">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="59387-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="59387-144">See also</span></span>

- [<span data-ttu-id="59387-145">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="59387-145">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

