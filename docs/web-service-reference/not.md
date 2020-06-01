---
title: No
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Not
api_type:
- schema
ms.assetid: 1aa16318-7e90-4b19-bce8-dd1a20a66223
description: El elemento not representa una expresión de búsqueda que niega el valor booleano de la expresión de búsqueda que contiene.
ms.openlocfilehash: 84c64a6d9d39f260d416fc32e4e5f5fcdef027e5
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466720"
---
# <a name="not"></a><span data-ttu-id="0d3f2-103">No</span><span class="sxs-lookup"><span data-stu-id="0d3f2-103">Not</span></span>

<span data-ttu-id="0d3f2-104">El elemento **Not** representa una expresión de búsqueda que niega el valor booleano de la expresión de búsqueda que contiene.</span><span class="sxs-lookup"><span data-stu-id="0d3f2-104">The **Not** element represents a search expression that negates the Boolean value of the search expression that it contains.</span></span> 
  
```xml
<Not>
   <SearchExpression/>
</Not>
```

 <span data-ttu-id="0d3f2-105">**NotType**</span><span class="sxs-lookup"><span data-stu-id="0d3f2-105">**NotType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0d3f2-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="0d3f2-106">Attributes and elements</span></span>

<span data-ttu-id="0d3f2-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="0d3f2-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0d3f2-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="0d3f2-108">Attributes</span></span>

<span data-ttu-id="0d3f2-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="0d3f2-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0d3f2-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="0d3f2-110">Child elements</span></span>

|<span data-ttu-id="0d3f2-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="0d3f2-111">**Element**</span></span>|<span data-ttu-id="0d3f2-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0d3f2-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0d3f2-113">SearchExpression</span><span class="sxs-lookup"><span data-stu-id="0d3f2-113">SearchExpression</span></span>](searchexpression.md) <br/> | <span data-ttu-id="0d3f2-114">Representa la clase base para las expresiones dentro de una restricción.</span><span class="sxs-lookup"><span data-stu-id="0d3f2-114">Represents the base class for expressions within a restriction.</span></span> <br/><br/><span data-ttu-id="0d3f2-115">Se debe sustituir uno de los siguientes elementos por el elemento **SearchExpression** :</span><span class="sxs-lookup"><span data-stu-id="0d3f2-115">One of the following elements must be substituted for the **SearchExpression** element:</span></span> <br/> <br/><span data-ttu-id="0d3f2-116">- [Existente](exists.md)</span><span class="sxs-lookup"><span data-stu-id="0d3f2-116">- [Exists](exists.md)</span></span> <br/><span data-ttu-id="0d3f2-117">- [Excluye](excludes.md)</span><span class="sxs-lookup"><span data-stu-id="0d3f2-117">- [Excludes](excludes.md)</span></span> <br/><span data-ttu-id="0d3f2-118">- [IsEqualTo](isequalto.md)</span><span class="sxs-lookup"><span data-stu-id="0d3f2-118">- [IsEqualTo](isequalto.md)</span></span> <br/><span data-ttu-id="0d3f2-119">- [IsNotEqualTo](isnotequalto.md)</span><span class="sxs-lookup"><span data-stu-id="0d3f2-119">- [IsNotEqualTo](isnotequalto.md)</span></span> <br/><span data-ttu-id="0d3f2-120">- [IsGreaterThan](isgreaterthan.md)</span><span class="sxs-lookup"><span data-stu-id="0d3f2-120">- [IsGreaterThan](isgreaterthan.md)</span></span> <br/><span data-ttu-id="0d3f2-121">- [IsGreaterThanOrEqualTo](isgreaterthanorequalto.md)</span><span class="sxs-lookup"><span data-stu-id="0d3f2-121">- [IsGreaterThanOrEqualTo](isgreaterthanorequalto.md)</span></span> <br/><span data-ttu-id="0d3f2-122">- [IsLessThan](islessthan.md)</span><span class="sxs-lookup"><span data-stu-id="0d3f2-122">- [IsLessThan](islessthan.md)</span></span> <br/><span data-ttu-id="0d3f2-123">- [IsLessThanOrEqualTo](islessthanorequalto.md)</span><span class="sxs-lookup"><span data-stu-id="0d3f2-123">- [IsLessThanOrEqualTo](islessthanorequalto.md)</span></span> <br/><span data-ttu-id="0d3f2-124">- [Contener](contains.md)</span><span class="sxs-lookup"><span data-stu-id="0d3f2-124">- [Contains](contains.md)</span></span> <br/><span data-ttu-id="0d3f2-125">- **No**</span><span class="sxs-lookup"><span data-stu-id="0d3f2-125">- **Not**</span></span> <br/><span data-ttu-id="0d3f2-126">- [Y](and.md)</span><span class="sxs-lookup"><span data-stu-id="0d3f2-126">- [And](and.md)</span></span> <br/><span data-ttu-id="0d3f2-127">- [O](or.md)</span><span class="sxs-lookup"><span data-stu-id="0d3f2-127">- [Or](or.md)</span></span> <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="0d3f2-128">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="0d3f2-128">Parent elements</span></span>

|<span data-ttu-id="0d3f2-129">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="0d3f2-129">**Element**</span></span>|<span data-ttu-id="0d3f2-130">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0d3f2-130">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0d3f2-131">Restriction</span><span class="sxs-lookup"><span data-stu-id="0d3f2-131">Restriction</span></span>](restriction.md) <br/> |<span data-ttu-id="0d3f2-132">Representa la restricción o consulta que se usa para filtrar elementos o carpetas en las operaciones de carpeta de búsqueda FindItem/FindFolder.</span><span class="sxs-lookup"><span data-stu-id="0d3f2-132">Represents the restriction or query that is used to filter items or folders in FindItem/FindFolder and search folder operations.</span></span>  <br/> |
|<span data-ttu-id="0d3f2-133">**Not**</span><span class="sxs-lookup"><span data-stu-id="0d3f2-133">**Not**</span></span> <br/> |<span data-ttu-id="0d3f2-134">Representa una expresión de búsqueda que niega el valor booleano de la expresión de búsqueda que contiene.</span><span class="sxs-lookup"><span data-stu-id="0d3f2-134">Represents a search expression that negates the Boolean value of the search expression that it contains.</span></span>  <br/> |
|[<span data-ttu-id="0d3f2-135">And</span><span class="sxs-lookup"><span data-stu-id="0d3f2-135">And</span></span>](and.md) <br/> |<span data-ttu-id="0d3f2-136">Representa una expresión de búsqueda que permite realizar una operación **and** booleana entre dos o más expresiones de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="0d3f2-136">Represents a search expression that allows you to perform a Boolean **AND** operation between two or more search expressions.</span></span> <span data-ttu-id="0d3f2-137">El resultado de la operación **and** es **true** si todas las expresiones de búsqueda contenidas en el elemento **and** son **true**.</span><span class="sxs-lookup"><span data-stu-id="0d3f2-137">The result of the **AND** operation is **true** if all the search expressions contained within the **And** element are **true**.</span></span>  <br/> |
|[<span data-ttu-id="0d3f2-138">Or</span><span class="sxs-lookup"><span data-stu-id="0d3f2-138">Or</span></span>](or.md) <br/> |<span data-ttu-id="0d3f2-139">Representa una expresión de búsqueda que realiza una operación **or** lógica en la expresión de búsqueda que contiene.</span><span class="sxs-lookup"><span data-stu-id="0d3f2-139">Represents a search expression that performs a logical **OR** operation on the search expression that it contains.</span></span> <span data-ttu-id="0d3f2-140">**O** devuelve **true** si cualquiera de sus elementos secundarios devuelve **true**.</span><span class="sxs-lookup"><span data-stu-id="0d3f2-140">**Or** will return **true** if any of its children return **true**.</span></span> <span data-ttu-id="0d3f2-141">**O** debe tener dos o más elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="0d3f2-141">**Or** must have two or more children.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0d3f2-142">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0d3f2-142">Remarks</span></span>

<span data-ttu-id="0d3f2-143">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="0d3f2-143">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0d3f2-144">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="0d3f2-144">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0d3f2-145">Namespace</span><span class="sxs-lookup"><span data-stu-id="0d3f2-145">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="0d3f2-146">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="0d3f2-146">Schema Name</span></span>  <br/> |<span data-ttu-id="0d3f2-147">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="0d3f2-147">Types schema</span></span>  <br/> |
|<span data-ttu-id="0d3f2-148">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="0d3f2-148">Validation File</span></span>  <br/> |<span data-ttu-id="0d3f2-149">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="0d3f2-149">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="0d3f2-150">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="0d3f2-150">Can be Empty</span></span>  <br/> |<span data-ttu-id="0d3f2-151">Falso</span><span class="sxs-lookup"><span data-stu-id="0d3f2-151">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0d3f2-152">Vea también</span><span class="sxs-lookup"><span data-stu-id="0d3f2-152">See also</span></span>

- [<span data-ttu-id="0d3f2-153">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="0d3f2-153">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

