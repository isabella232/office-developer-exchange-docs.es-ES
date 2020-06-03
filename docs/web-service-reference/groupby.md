---
title: GroupBy
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GroupBy
api_type:
- schema
ms.assetid: 9728619b-4674-4b9d-9f6c-e75c6165966c
description: El elemento GroupBy especifica una agrupación arbitraria para consultas FindItem.
ms.openlocfilehash: 0d681e5376e4dd71921cc97f270211e49179db85
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530102"
---
# <a name="groupby"></a><span data-ttu-id="2765e-103">GroupBy</span><span class="sxs-lookup"><span data-stu-id="2765e-103">GroupBy</span></span>

<span data-ttu-id="2765e-104">El elemento **GroupBy** especifica una agrupación arbitraria para consultas FindItem.</span><span class="sxs-lookup"><span data-stu-id="2765e-104">The **GroupBy** element specifies an arbitrary grouping for FindItem queries.</span></span> 
  
- [<span data-ttu-id="2765e-105">FindItem</span><span class="sxs-lookup"><span data-stu-id="2765e-105">FindItem</span></span>](finditem.md)
- [<span data-ttu-id="2765e-106">GroupBy</span><span class="sxs-lookup"><span data-stu-id="2765e-106">GroupBy</span></span>](groupby.md)
  
```xml
<GroupBy Order="">
   <FieldURI/>
   <AggregateOn/>
</GroupBy>
```

```xml
<GroupBy Order="">
   <ExtendededFieldURI/>
   <AggregateOn/>
</GroupBy>
```

```xml
<GroupBy Order="">
   <IndexedFieldURI/>
   <AggregateOn/>
</GroupBy>
```

<span data-ttu-id="2765e-107">**GroupByType**</span><span class="sxs-lookup"><span data-stu-id="2765e-107">**GroupByType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="2765e-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="2765e-108">Attributes and elements</span></span>

<span data-ttu-id="2765e-109">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="2765e-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2765e-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="2765e-110">Attributes</span></span>

|<span data-ttu-id="2765e-111">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="2765e-111">**Attribute**</span></span>|<span data-ttu-id="2765e-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2765e-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2765e-113">**Order**</span><span class="sxs-lookup"><span data-stu-id="2765e-113">**Order**</span></span> <br/> | <span data-ttu-id="2765e-114">Determina el orden de los grupos en la matriz de elementos agrupados que se devuelve en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2765e-114">Determines the order of the groups in the grouped item array that is returned in the response.</span></span> <span data-ttu-id="2765e-115">Este atributo es del tipo SortDirectionType.</span><span class="sxs-lookup"><span data-stu-id="2765e-115">This attribute is of type SortDirectionType.</span></span>  <br/> |
   
#### <a name="order-attribute-values"></a><span data-ttu-id="2765e-116">Ordenar valores de atributos</span><span class="sxs-lookup"><span data-stu-id="2765e-116">Order attribute values</span></span>

|<span data-ttu-id="2765e-117">**Valor**</span><span class="sxs-lookup"><span data-stu-id="2765e-117">**Value**</span></span>|<span data-ttu-id="2765e-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2765e-118">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2765e-119">Ascendente</span><span class="sxs-lookup"><span data-stu-id="2765e-119">Ascending</span></span>  <br/> |<span data-ttu-id="2765e-120">Los grupos se ordenan en orden ascendente.</span><span class="sxs-lookup"><span data-stu-id="2765e-120">The groups are ordered in ascending order.</span></span>  <br/> |
|<span data-ttu-id="2765e-121">Descendente</span><span class="sxs-lookup"><span data-stu-id="2765e-121">Descending</span></span>  <br/> |<span data-ttu-id="2765e-122">Los grupos se ordenan en orden descendente.</span><span class="sxs-lookup"><span data-stu-id="2765e-122">The groups are ordered in descending order.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="2765e-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="2765e-123">Child elements</span></span>

|<span data-ttu-id="2765e-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="2765e-124">**Element**</span></span>|<span data-ttu-id="2765e-125">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2765e-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2765e-126">FieldURI</span><span class="sxs-lookup"><span data-stu-id="2765e-126">FieldURI</span></span>](fielduri.md) <br/> |<span data-ttu-id="2765e-127">Identifica las propiedades a las que se hace referencia con frecuencia mediante el URI.</span><span class="sxs-lookup"><span data-stu-id="2765e-127">Identifies frequently referenced properties by URI.</span></span>  <br/> |
|[<span data-ttu-id="2765e-128">IndexedFieldURI</span><span class="sxs-lookup"><span data-stu-id="2765e-128">IndexedFieldURI</span></span>](indexedfielduri.md) <br/> |<span data-ttu-id="2765e-129">Identifica a los miembros individuales de un diccionario.</span><span class="sxs-lookup"><span data-stu-id="2765e-129">Identifies individual members of a dictionary.</span></span>  <br/> |
|[<span data-ttu-id="2765e-130">ExtendedFieldURI</span><span class="sxs-lookup"><span data-stu-id="2765e-130">ExtendedFieldURI</span></span>](extendedfielduri.md) <br/> |<span data-ttu-id="2765e-131">Identifica las propiedades MAPI extendidas para obtener, establecer o crear.</span><span class="sxs-lookup"><span data-stu-id="2765e-131">Identifies extended MAPI properties to get, set, or create.</span></span>  <br/> |
|[<span data-ttu-id="2765e-132">AggregateOn</span><span class="sxs-lookup"><span data-stu-id="2765e-132">AggregateOn</span></span>](aggregateon.md) <br/> |<span data-ttu-id="2765e-133">Representa el campo que se usa para determinar el orden de los grupos en una respuesta.</span><span class="sxs-lookup"><span data-stu-id="2765e-133">Represents the field that is used to determine the order of groups in a response.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="2765e-134">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="2765e-134">Parent elements</span></span>

|<span data-ttu-id="2765e-135">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="2765e-135">**Element**</span></span>|<span data-ttu-id="2765e-136">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2765e-136">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2765e-137">FindItem</span><span class="sxs-lookup"><span data-stu-id="2765e-137">FindItem</span></span>](finditem.md) <br/> |<span data-ttu-id="2765e-138">Define una solicitud para buscar elementos en un buzón.</span><span class="sxs-lookup"><span data-stu-id="2765e-138">Defines a request to find items in a mailbox.</span></span>  <br/><br/> <span data-ttu-id="2765e-139">La siguiente es la expresión XPath a este elemento:`/FindItem`</span><span class="sxs-lookup"><span data-stu-id="2765e-139">The following is the XPath expression to this element:  `/FindItem`</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2765e-140">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2765e-140">Remarks</span></span>

<span data-ttu-id="2765e-141">La respuesta FindItem contendrá una colección de grupos.</span><span class="sxs-lookup"><span data-stu-id="2765e-141">The FindItem response will contain a collection of groups.</span></span> <span data-ttu-id="2765e-142">Cada grupo contendrá todos los elementos que coinciden con los valores de la propiedad **GroupBy** .</span><span class="sxs-lookup"><span data-stu-id="2765e-142">Each group will contain all items that had matching values for the **GroupBy** property.</span></span> <span data-ttu-id="2765e-143">La propiedad que determina la agrupación se identifica en el elemento [FieldURI](fielduri.md), [IndexedFieldURI](indexedfielduri.md)o [ExtendedFieldURI](extendedfielduri.md) .</span><span class="sxs-lookup"><span data-stu-id="2765e-143">The property that determines the grouping is identified in the [FieldURI](fielduri.md), [IndexedFieldURI](indexedfielduri.md), or [ExtendedFieldURI](extendedfielduri.md) element.</span></span> 
  
<span data-ttu-id="2765e-144">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="2765e-144">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2765e-145">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="2765e-145">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2765e-146">Namespace</span><span class="sxs-lookup"><span data-stu-id="2765e-146">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="2765e-147">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="2765e-147">Schema Name</span></span>  <br/> |<span data-ttu-id="2765e-148">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="2765e-148">Messages schema</span></span>  <br/> |
|<span data-ttu-id="2765e-149">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="2765e-149">Validation File</span></span>  <br/> |<span data-ttu-id="2765e-150">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="2765e-150">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="2765e-151">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="2765e-151">Can be Empty</span></span>  <br/> |<span data-ttu-id="2765e-152">Falso</span><span class="sxs-lookup"><span data-stu-id="2765e-152">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2765e-153">Vea también</span><span class="sxs-lookup"><span data-stu-id="2765e-153">See also</span></span>

- [<span data-ttu-id="2765e-154">Operación FindItem</span><span class="sxs-lookup"><span data-stu-id="2765e-154">FindItem operation</span></span>](finditem-operation.md)
- [<span data-ttu-id="2765e-155">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="2765e-155">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="2765e-156">Buscar elementos</span><span class="sxs-lookup"><span data-stu-id="2765e-156">Finding Items</span></span>](https://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

