---
title: 'O bien:'
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Or
api_type:
- schema
ms.assetid: 4876d83a-73a3-4953-9d95-3048e6b76ccb
description: El elemento or representa una expresión de búsqueda que realiza una operación lógica OR en la expresión de búsqueda que contiene. O devuelve true si cualquiera de sus elementos secundarios devuelve true. O debe tener dos o más elementos secundarios.
ms.openlocfilehash: 9bc676da5bbaad64f11f6717fb487c2e9bcf2d89
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462482"
---
# <a name="or"></a><span data-ttu-id="a4070-105">O bien:</span><span class="sxs-lookup"><span data-stu-id="a4070-105">Or</span></span>

<span data-ttu-id="a4070-106">El elemento **or** representa una expresión de búsqueda que realiza una operación lógica **or** en la expresión de búsqueda que contiene.</span><span class="sxs-lookup"><span data-stu-id="a4070-106">The **Or** element represents a search expression that performs a logical **OR** on the search expression that it contains.</span></span> <span data-ttu-id="a4070-107">**O** devuelve **true** si cualquiera de sus elementos secundarios devuelve **true**.</span><span class="sxs-lookup"><span data-stu-id="a4070-107">**Or** will return **true** if any of its children return **true**.</span></span> <span data-ttu-id="a4070-108">**O** debe tener dos o más elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="a4070-108">**Or** must have two or more children.</span></span> 
  
```xml
<Or>
   <SearchExpression/>
   <SearchExpression/>
</Or>
```

 <span data-ttu-id="a4070-109">**Obiblioteca**</span><span class="sxs-lookup"><span data-stu-id="a4070-109">**OrType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a4070-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="a4070-110">Attributes and elements</span></span>

<span data-ttu-id="a4070-111">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="a4070-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a4070-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="a4070-112">Attributes</span></span>

<span data-ttu-id="a4070-113">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="a4070-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a4070-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="a4070-114">Child elements</span></span>

|<span data-ttu-id="a4070-115">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="a4070-115">**Element**</span></span>|<span data-ttu-id="a4070-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a4070-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a4070-117">SearchExpression</span><span class="sxs-lookup"><span data-stu-id="a4070-117">SearchExpression</span></span>](searchexpression.md) <br/> | <span data-ttu-id="a4070-118">Representa la clase base para las expresiones dentro de una restricción.</span><span class="sxs-lookup"><span data-stu-id="a4070-118">Represents the base class for expressions within a restriction.</span></span> <br/><br/><span data-ttu-id="a4070-119">Se debe sustituir uno de los siguientes elementos por el elemento **SearchExpression** :</span><span class="sxs-lookup"><span data-stu-id="a4070-119">One of the following elements must be substituted for the **SearchExpression** element:</span></span> <br/> <br/><span data-ttu-id="a4070-120">- [Existente](exists.md)</span><span class="sxs-lookup"><span data-stu-id="a4070-120">- [Exists](exists.md)</span></span> <br/><span data-ttu-id="a4070-121">- [Excluye](excludes.md)</span><span class="sxs-lookup"><span data-stu-id="a4070-121">- [Excludes](excludes.md)</span></span> <br/><span data-ttu-id="a4070-122">- [IsEqualTo](isequalto.md)</span><span class="sxs-lookup"><span data-stu-id="a4070-122">- [IsEqualTo](isequalto.md)</span></span> <br/><span data-ttu-id="a4070-123">- [IsNotEqualTo](isnotequalto.md)</span><span class="sxs-lookup"><span data-stu-id="a4070-123">- [IsNotEqualTo](isnotequalto.md)</span></span> <br/><span data-ttu-id="a4070-124">- [IsGreaterThan](isgreaterthan.md)</span><span class="sxs-lookup"><span data-stu-id="a4070-124">- [IsGreaterThan](isgreaterthan.md)</span></span> <br/><span data-ttu-id="a4070-125">- [IsGreaterThanOrEqualTo](isgreaterthanorequalto.md)</span><span class="sxs-lookup"><span data-stu-id="a4070-125">- [IsGreaterThanOrEqualTo](isgreaterthanorequalto.md)</span></span> <br/><span data-ttu-id="a4070-126">- [IsLessThan](islessthan.md)</span><span class="sxs-lookup"><span data-stu-id="a4070-126">- [IsLessThan](islessthan.md)</span></span> <br/><span data-ttu-id="a4070-127">- [IsLessThanOrEqualTo](islessthanorequalto.md)</span><span class="sxs-lookup"><span data-stu-id="a4070-127">- [IsLessThanOrEqualTo](islessthanorequalto.md)</span></span> <br/><span data-ttu-id="a4070-128">- [Contener](contains.md)</span><span class="sxs-lookup"><span data-stu-id="a4070-128">- [Contains](contains.md)</span></span> <br/><span data-ttu-id="a4070-129">- [No](not.md)</span><span class="sxs-lookup"><span data-stu-id="a4070-129">- [Not](not.md)</span></span> <br/><span data-ttu-id="a4070-130">- [Y](and.md)</span><span class="sxs-lookup"><span data-stu-id="a4070-130">- [And](and.md)</span></span> <br/><span data-ttu-id="a4070-131">- **O**</span><span class="sxs-lookup"><span data-stu-id="a4070-131">- **Or**</span></span> <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="a4070-132">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="a4070-132">Parent elements</span></span>

|<span data-ttu-id="a4070-133">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="a4070-133">**Element**</span></span>|<span data-ttu-id="a4070-134">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a4070-134">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a4070-135">Restriction</span><span class="sxs-lookup"><span data-stu-id="a4070-135">Restriction</span></span>](restriction.md) <br/> |<span data-ttu-id="a4070-136">Representa la restricción o consulta que se usa para filtrar elementos o carpetas en las operaciones de carpeta de búsqueda FindItem/FindFolder.</span><span class="sxs-lookup"><span data-stu-id="a4070-136">Represents the restriction or query that is used to filter items or folders in FindItem/FindFolder and search folder operations.</span></span>  <br/> |
|[<span data-ttu-id="a4070-137">Not</span><span class="sxs-lookup"><span data-stu-id="a4070-137">Not</span></span>](not.md) <br/> |<span data-ttu-id="a4070-138">Representa una expresión de búsqueda que niega el valor booleano de la expresión de búsqueda que contiene.</span><span class="sxs-lookup"><span data-stu-id="a4070-138">Represents a search expression that negates the Boolean value of the search expression that it contains.</span></span>  <br/> |
|[<span data-ttu-id="a4070-139">And</span><span class="sxs-lookup"><span data-stu-id="a4070-139">And</span></span>](and.md) <br/> |<span data-ttu-id="a4070-140">Representa una expresión de búsqueda que permite realizar una operación **and** booleana entre dos o más expresiones de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="a4070-140">Represents a search expression that allows you to perform a Boolean **AND** operation between two or more search expressions.</span></span> <span data-ttu-id="a4070-141">El resultado de la operación **and** es **true** si todas las expresiones de búsqueda contenidas en el elemento **and** son **true**.</span><span class="sxs-lookup"><span data-stu-id="a4070-141">The result of the **AND** operation is **true** if all the search expressions contained within the **And** element are **true**.</span></span>  <br/> |
|<span data-ttu-id="a4070-142">**Or**</span><span class="sxs-lookup"><span data-stu-id="a4070-142">**Or**</span></span> <br/> |<span data-ttu-id="a4070-143">Representa una expresión de búsqueda que realiza una operación **or** lógica en la expresión de búsqueda que contiene.</span><span class="sxs-lookup"><span data-stu-id="a4070-143">Represents a search expression that performs a logical **OR** operation on the search expression that it contains.</span></span> <span data-ttu-id="a4070-144">**O** devuelve **true** si cualquiera de sus elementos secundarios devuelve **true**.</span><span class="sxs-lookup"><span data-stu-id="a4070-144">**Or** will return **true** if any of its children return **true**.</span></span> <span data-ttu-id="a4070-145">**O** debe tener dos o más elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="a4070-145">**Or** must have two or more children.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a4070-146">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a4070-146">Remarks</span></span>

<span data-ttu-id="a4070-147">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="a4070-147">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a4070-148">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="a4070-148">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a4070-149">Namespace</span><span class="sxs-lookup"><span data-stu-id="a4070-149">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a4070-150">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="a4070-150">Schema Name</span></span>  <br/> |<span data-ttu-id="a4070-151">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="a4070-151">Types schema</span></span>  <br/> |
|<span data-ttu-id="a4070-152">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="a4070-152">Validation File</span></span>  <br/> |<span data-ttu-id="a4070-153">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="a4070-153">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="a4070-154">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="a4070-154">Can be Empty</span></span>  <br/> |<span data-ttu-id="a4070-155">Falso</span><span class="sxs-lookup"><span data-stu-id="a4070-155">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a4070-156">Vea también</span><span class="sxs-lookup"><span data-stu-id="a4070-156">See also</span></span>

- [<span data-ttu-id="a4070-157">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="a4070-157">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

