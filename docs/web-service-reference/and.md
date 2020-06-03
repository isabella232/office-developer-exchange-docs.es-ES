---
title: And
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- And
api_type:
- schema
ms.assetid: 790246c2-37ad-49a8-91b9-6186d743b011
description: El elemento and representa una expresión de búsqueda que permite realizar una operación AND booleana entre dos o más expresiones de búsqueda. El resultado de la operación AND es true si todas las expresiones de búsqueda contenidas en el elemento and son true.
ms.openlocfilehash: f5239f19c2b5a931eefa9ff4a9dd8ed9d775bae2
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44464724"
---
# <a name="and"></a><span data-ttu-id="f4399-104">And</span><span class="sxs-lookup"><span data-stu-id="f4399-104">And</span></span>

<span data-ttu-id="f4399-105">El elemento **and** representa una expresión de búsqueda que permite realizar una operación **and** booleana entre dos o más expresiones de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="f4399-105">The **And** element represents a search expression that allows you to perform a Boolean **AND** operation between two or more search expressions.</span></span> <span data-ttu-id="f4399-106">El resultado de la operación **and** es **true** si todas las expresiones de búsqueda contenidas en el elemento **and** son **true**.</span><span class="sxs-lookup"><span data-stu-id="f4399-106">The result of the **AND** operation is **true** if all the search expressions contained within the **And** element are **true**.</span></span>
  
```xml
<And>
   <SearchExpression/>
   <SearchExpression/>
</And>
```

 <span data-ttu-id="f4399-107">**AndType**</span><span class="sxs-lookup"><span data-stu-id="f4399-107">**AndType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f4399-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="f4399-108">Attributes and elements</span></span>

<span data-ttu-id="f4399-109">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="f4399-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f4399-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="f4399-110">Attributes</span></span>

<span data-ttu-id="f4399-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="f4399-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f4399-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="f4399-112">Child elements</span></span>

|<span data-ttu-id="f4399-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="f4399-113">**Element**</span></span>|<span data-ttu-id="f4399-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f4399-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f4399-115">SearchExpression</span><span class="sxs-lookup"><span data-stu-id="f4399-115">SearchExpression</span></span>](searchexpression.md) <br/> | <span data-ttu-id="f4399-116">Representa la clase base para las expresiones dentro de una restricción.</span><span class="sxs-lookup"><span data-stu-id="f4399-116">Represents the base class for expressions within a restriction.</span></span> <span data-ttu-id="f4399-117">Debe haber dos o más expresiones de búsqueda en una operación and.</span><span class="sxs-lookup"><span data-stu-id="f4399-117">There must be two or more search expressions in an And operation.</span></span><br/><br/>  <span data-ttu-id="f4399-118">Se debe sustituir uno de los siguientes elementos por el elemento **SearchExpression** :</span><span class="sxs-lookup"><span data-stu-id="f4399-118">One of the following elements must be substituted for the **SearchExpression** element:</span></span><ul><li> [<span data-ttu-id="f4399-119">Exists</span><span class="sxs-lookup"><span data-stu-id="f4399-119">Exists</span></span>](exists.md)</li><li>[<span data-ttu-id="f4399-120">Excluye</span><span class="sxs-lookup"><span data-stu-id="f4399-120">Excludes</span></span>](excludes.md)</li><li>[<span data-ttu-id="f4399-121">IsEqualTo</span><span class="sxs-lookup"><span data-stu-id="f4399-121">IsEqualTo</span></span>](isequalto.md)</li><li>[<span data-ttu-id="f4399-122">IsNotEqualTo</span><span class="sxs-lookup"><span data-stu-id="f4399-122">IsNotEqualTo</span></span>](isnotequalto.md)</li><li>[<span data-ttu-id="f4399-123">IsGreaterThan</span><span class="sxs-lookup"><span data-stu-id="f4399-123">IsGreaterThan</span></span>](isgreaterthan.md)</li><li>[<span data-ttu-id="f4399-124">IsGreaterThanOrEqualTo</span><span class="sxs-lookup"><span data-stu-id="f4399-124">IsGreaterThanOrEqualTo</span></span>](isgreaterthanorequalto.md)</li><li>[<span data-ttu-id="f4399-125">IsLessThan</span><span class="sxs-lookup"><span data-stu-id="f4399-125">IsLessThan</span></span>](islessthan.md)</li><li>[<span data-ttu-id="f4399-126">IsLessThanOrEqualTo</span><span class="sxs-lookup"><span data-stu-id="f4399-126">IsLessThanOrEqualTo</span></span>](islessthanorequalto.md)</li><li>[<span data-ttu-id="f4399-127">Contains</span><span class="sxs-lookup"><span data-stu-id="f4399-127">Contains</span></span>](contains.md)</li><li>[<span data-ttu-id="f4399-128">Not</span><span class="sxs-lookup"><span data-stu-id="f4399-128">Not</span></span>](not.md)</li><li><span data-ttu-id="f4399-129">**And**</span><span class="sxs-lookup"><span data-stu-id="f4399-129">**And**</span></span></li><li>[<span data-ttu-id="f4399-130">Or</span><span class="sxs-lookup"><span data-stu-id="f4399-130">Or</span></span>](or.md) </li></ul> |
   
### <a name="parent-elements"></a><span data-ttu-id="f4399-131">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="f4399-131">Parent elements</span></span>

|<span data-ttu-id="f4399-132">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="f4399-132">**Element**</span></span>|<span data-ttu-id="f4399-133">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f4399-133">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f4399-134">Restriction</span><span class="sxs-lookup"><span data-stu-id="f4399-134">Restriction</span></span>](restriction.md) <br/> |<span data-ttu-id="f4399-135">Representa la restricción o consulta que se usa para filtrar elementos o carpetas en las operaciones de carpeta de búsqueda FindItem/FindFolder.</span><span class="sxs-lookup"><span data-stu-id="f4399-135">Represents the restriction or query that is used to filter items or folders in FindItem/FindFolder and search folder operations.</span></span>  <br/> |
|[<span data-ttu-id="f4399-136">Not</span><span class="sxs-lookup"><span data-stu-id="f4399-136">Not</span></span>](not.md) <br/> |<span data-ttu-id="f4399-137">Representa una expresión de búsqueda que niega el valor booleano de la expresión de búsqueda que contiene.</span><span class="sxs-lookup"><span data-stu-id="f4399-137">Represents a search expression that negates the Boolean value of the search expression that it contains.</span></span>  <br/> |
|<span data-ttu-id="f4399-138">**And**</span><span class="sxs-lookup"><span data-stu-id="f4399-138">**And**</span></span> <br/> |<span data-ttu-id="f4399-139">Representa una expresión de búsqueda que permite realizar una operación **and** booleana entre dos o más expresiones de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="f4399-139">Represents a search expression that allows you to perform a Boolean **AND** operation between two or more search expressions.</span></span> <span data-ttu-id="f4399-140">El resultado de la operación **and** es **true** si todas las expresiones de búsqueda contenidas en el elemento **and** son **true**.</span><span class="sxs-lookup"><span data-stu-id="f4399-140">The result of the **AND** operation is **true** if all of the search expressions contained within the **And** element are **true**.</span></span>  <br/> |
|[<span data-ttu-id="f4399-141">Or</span><span class="sxs-lookup"><span data-stu-id="f4399-141">Or</span></span>](or.md) <br/> |<span data-ttu-id="f4399-142">Representa una expresión de búsqueda que realiza una operación **or** lógica en la expresión de búsqueda que contiene.</span><span class="sxs-lookup"><span data-stu-id="f4399-142">Represents a search expression that performs a logical **OR** operation on the search expression that it contains.</span></span> <span data-ttu-id="f4399-143">**O** devuelve **true** si cualquiera de sus elementos secundarios devuelve **true**.</span><span class="sxs-lookup"><span data-stu-id="f4399-143">**Or** will return **true** if any of its children return **true**.</span></span> <span data-ttu-id="f4399-144">**O** debe tener dos o más elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="f4399-144">**Or** must have two or more children.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f4399-145">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f4399-145">Remarks</span></span>

<span data-ttu-id="f4399-146">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="f4399-146">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f4399-147">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="f4399-147">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f4399-148">Namespace</span><span class="sxs-lookup"><span data-stu-id="f4399-148">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f4399-149">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="f4399-149">Schema Name</span></span>  <br/> |<span data-ttu-id="f4399-150">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="f4399-150">Types schema</span></span>  <br/> |
|<span data-ttu-id="f4399-151">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="f4399-151">Validation File</span></span>  <br/> |<span data-ttu-id="f4399-152">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="f4399-152">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="f4399-153">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="f4399-153">Can be Empty</span></span>  <br/> |<span data-ttu-id="f4399-154">Falso</span><span class="sxs-lookup"><span data-stu-id="f4399-154">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f4399-155">Vea también</span><span class="sxs-lookup"><span data-stu-id="f4399-155">See also</span></span>

- [<span data-ttu-id="f4399-156">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="f4399-156">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

