---
title: RootFolder (FindItemResponseMessage)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RootFolder
api_type:
- schema
ms.assetid: 187e009f-efaa-42a8-8962-329a645213ab
description: El elemento RootFolder contiene los resultados de una búsqueda de una sola carpeta raíz durante una operación de FindItem.
ms.openlocfilehash: ea17369ef4efc4112a738b430c8f0dbab3886341
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19837254"
---
# <a name="rootfolder-finditemresponsemessage"></a><span data-ttu-id="28388-103">RootFolder (FindItemResponseMessage)</span><span class="sxs-lookup"><span data-stu-id="28388-103">RootFolder (FindItemResponseMessage)</span></span>

<span data-ttu-id="28388-104">El elemento **RootFolder** contiene los resultados de una búsqueda de una sola carpeta raíz durante una [operación de FindItem](finditem-operation.md).</span><span class="sxs-lookup"><span data-stu-id="28388-104">The **RootFolder** element contains the results of a search of a single root folder during a [FindItem operation](finditem-operation.md).</span></span>
  
```xml
<RootFolder IndexedPagingOffset="" NumeratorOffset="" AbsoluteDenominator="" IncludesLastItemInRange="" TotalItemsInView="">
   <Items/>
   <Groups/>
</RootFolder>
```

 <span data-ttu-id="28388-105">**FindItemParentType**</span><span class="sxs-lookup"><span data-stu-id="28388-105">**FindItemParentType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="28388-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="28388-106">Attributes and elements</span></span>

<span data-ttu-id="28388-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="28388-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="28388-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="28388-108">Attributes</span></span>

|<span data-ttu-id="28388-109">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="28388-109">**Attribute**</span></span>|<span data-ttu-id="28388-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="28388-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="28388-111">**IndexedPagingOffset**</span><span class="sxs-lookup"><span data-stu-id="28388-111">**IndexedPagingOffset**</span></span> <br/> |<span data-ttu-id="28388-112">Representa el siguiente índice que se debe usar para la solicitud siguiente cuando se usa una vista indizada de paginación.</span><span class="sxs-lookup"><span data-stu-id="28388-112">Represents the next index that should be used for the next request when using an indexed paging view.</span></span>  <br/> |
|<span data-ttu-id="28388-113">**NumeratorOffset**</span><span class="sxs-lookup"><span data-stu-id="28388-113">**NumeratorOffset**</span></span> <br/> |<span data-ttu-id="28388-114">Representa el nuevo valor numerador debe usar para la solicitud siguiente con vistas de página de fracción.</span><span class="sxs-lookup"><span data-stu-id="28388-114">Represents the new numerator value to use for the next request when using fraction page views.</span></span>  <br/> |
|<span data-ttu-id="28388-115">**AbsoluteDenominator**</span><span class="sxs-lookup"><span data-stu-id="28388-115">**AbsoluteDenominator**</span></span> <br/> |<span data-ttu-id="28388-116">Representa el denominador siguiente para usar para la solicitud siguiente al realizar la paginación fraccionaria.</span><span class="sxs-lookup"><span data-stu-id="28388-116">Represents the next denominator to use for the next request when doing fractional paging.</span></span>  <br/> |
|<span data-ttu-id="28388-117">**IncludesLastItemInRange**</span><span class="sxs-lookup"><span data-stu-id="28388-117">**IncludesLastItemInRange**</span></span> <br/> |<span data-ttu-id="28388-118">Indica si los resultados actuales contienen el último elemento de la consulta, por ejemplo, que no es necesaria la paginación aún más.</span><span class="sxs-lookup"><span data-stu-id="28388-118">Indicates whether the current results contain the last item in the query, such that further paging is not needed.</span></span>  <br/> |
|<span data-ttu-id="28388-119">**TotalItemsInView**</span><span class="sxs-lookup"><span data-stu-id="28388-119">**TotalItemsInView**</span></span> <br/> |<span data-ttu-id="28388-120">Representa el número total de elementos que pase la restricción.</span><span class="sxs-lookup"><span data-stu-id="28388-120">Represents the total number of items that pass the restriction.</span></span> <span data-ttu-id="28388-121">En una [operación FindItem](finditem-operation.md)agrupada, el atributo **TotalItemsInView** devuelve el número total de elementos en la vista más el número total de grupos.</span><span class="sxs-lookup"><span data-stu-id="28388-121">In a grouped [FindItem operation](finditem-operation.md), the **TotalItemsInView** attribute returns the total number of items in the view plus the total number of groups.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="28388-122">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="28388-122">Child elements</span></span>

|<span data-ttu-id="28388-123">**Element**</span><span class="sxs-lookup"><span data-stu-id="28388-123">**Element**</span></span>|<span data-ttu-id="28388-124">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="28388-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="28388-125">Items</span><span class="sxs-lookup"><span data-stu-id="28388-125">Items</span></span>](items.md) <br/> |<span data-ttu-id="28388-126">Contiene una matriz de elementos que tienen los criterios de búsqueda identificados en la solicitud de [operación FindItem](finditem-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="28388-126">Contains an array of items found that have the search criteria identified in the [FindItem operation](finditem-operation.md) request.</span></span>  <br/> |
|[<span data-ttu-id="28388-127">Grupos</span><span class="sxs-lookup"><span data-stu-id="28388-127">Groups</span></span>](groups.md) <br/> |<span data-ttu-id="28388-128">Contiene una colección de grupos encontrados que cumplen los criterios de búsqueda y agregación identificados en la solicitud de [operación FindItem](finditem-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="28388-128">Contains a collection of groups found that have the search and aggregation criteria identified in the [FindItem operation](finditem-operation.md) request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="28388-129">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="28388-129">Parent elements</span></span>

|<span data-ttu-id="28388-130">**Element**</span><span class="sxs-lookup"><span data-stu-id="28388-130">**Element**</span></span>|<span data-ttu-id="28388-131">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="28388-131">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="28388-132">FindItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="28388-132">FindItemResponseMessage</span></span>](finditemresponsemessage.md) <br/> |<span data-ttu-id="28388-133">Contiene el estado y el resultado de una solicitud de [operación FindItem](finditem-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="28388-133">Contains the status and result of a [FindItem operation](finditem-operation.md) request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="28388-134">Notas</span><span class="sxs-lookup"><span data-stu-id="28388-134">Remarks</span></span>

<span data-ttu-id="28388-135">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Exchange Server con la función de servidor de acceso de cliente instalada.</span><span class="sxs-lookup"><span data-stu-id="28388-135">The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange Server with the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="28388-136">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="28388-136">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="28388-137">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="28388-137">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="28388-138">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="28388-138">Schema name</span></span>  <br/> |<span data-ttu-id="28388-139">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="28388-139">Messages schema</span></span>  <br/> |
|<span data-ttu-id="28388-140">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="28388-140">Validation file</span></span>  <br/> |<span data-ttu-id="28388-141">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="28388-141">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="28388-142">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="28388-142">Can be empty</span></span>  <br/> |<span data-ttu-id="28388-143">False</span><span class="sxs-lookup"><span data-stu-id="28388-143">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="28388-144">Ver también</span><span class="sxs-lookup"><span data-stu-id="28388-144">See also</span></span>



[<span data-ttu-id="28388-145">Operación FindItem</span><span class="sxs-lookup"><span data-stu-id="28388-145">FindItem operation</span></span>](finditem-operation.md)
  
[<span data-ttu-id="28388-146">IndexedPagingOffset</span><span class="sxs-lookup"><span data-stu-id="28388-146">IndexedPagingOffset</span></span>](https://msdn.microsoft.com/library/ExchangeWebServices.FindItemParentType.IndexedPagingOffset.aspx)
  
[<span data-ttu-id="28388-147">NumeratorOffset</span><span class="sxs-lookup"><span data-stu-id="28388-147">NumeratorOffset</span></span>](https://msdn.microsoft.com/library/ExchangeWebServices.FindItemParentType.NumeratorOffset.aspx)
  
[<span data-ttu-id="28388-148">AbsoluteDenominator</span><span class="sxs-lookup"><span data-stu-id="28388-148">AbsoluteDenominator</span></span>](https://msdn.microsoft.com/library/ExchangeWebServices.FindItemParentType.AbsoluteDenominator.aspx)
  
[<span data-ttu-id="28388-149">IncludesLastItemInRange</span><span class="sxs-lookup"><span data-stu-id="28388-149">IncludesLastItemInRange</span></span>](https://msdn.microsoft.com/library/ExchangeWebServices.FindItemParentType.IncludesLastItemInRange.aspx)
  
[<span data-ttu-id="28388-150">TotalItemsInView</span><span class="sxs-lookup"><span data-stu-id="28388-150">TotalItemsInView</span></span>](https://msdn.microsoft.com/library/ExchangeWebServices.FindItemParentType.TotalItemsInView.aspx)


[<span data-ttu-id="28388-151">Buscar elementos</span><span class="sxs-lookup"><span data-stu-id="28388-151">Finding Items</span></span>](http://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

