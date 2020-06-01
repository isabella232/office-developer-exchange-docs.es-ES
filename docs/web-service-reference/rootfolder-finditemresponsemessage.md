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
description: El elemento RootFolder contiene los resultados de una búsqueda de una sola carpeta raíz durante una operación FindItem.
ms.openlocfilehash: 3bbab325dff26139739c50ef519b215aea620a0b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457133"
---
# <a name="rootfolder-finditemresponsemessage"></a><span data-ttu-id="71e20-103">RootFolder (FindItemResponseMessage)</span><span class="sxs-lookup"><span data-stu-id="71e20-103">RootFolder (FindItemResponseMessage)</span></span>

<span data-ttu-id="71e20-104">El elemento **RootFolder** contiene los resultados de una búsqueda de una sola carpeta raíz durante una [operación FindItem](finditem-operation.md).</span><span class="sxs-lookup"><span data-stu-id="71e20-104">The **RootFolder** element contains the results of a search of a single root folder during a [FindItem operation](finditem-operation.md).</span></span>
  
```xml
<RootFolder IndexedPagingOffset="" NumeratorOffset="" AbsoluteDenominator="" IncludesLastItemInRange="" TotalItemsInView="">
   <Items/>
   <Groups/>
</RootFolder>
```

 <span data-ttu-id="71e20-105">**FindItemParentType**</span><span class="sxs-lookup"><span data-stu-id="71e20-105">**FindItemParentType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="71e20-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="71e20-106">Attributes and elements</span></span>

<span data-ttu-id="71e20-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="71e20-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="71e20-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="71e20-108">Attributes</span></span>

|<span data-ttu-id="71e20-109">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="71e20-109">**Attribute**</span></span>|<span data-ttu-id="71e20-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="71e20-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="71e20-111">**IndexedPagingOffset**</span><span class="sxs-lookup"><span data-stu-id="71e20-111">**IndexedPagingOffset**</span></span> <br/> |<span data-ttu-id="71e20-112">Representa el siguiente índice que se debe usar para la siguiente solicitud al usar una vista de paginación indizada.</span><span class="sxs-lookup"><span data-stu-id="71e20-112">Represents the next index that should be used for the next request when using an indexed paging view.</span></span>  <br/> |
|<span data-ttu-id="71e20-113">**NumeratorOffset**</span><span class="sxs-lookup"><span data-stu-id="71e20-113">**NumeratorOffset**</span></span> <br/> |<span data-ttu-id="71e20-114">Representa el nuevo valor del numerador que se va a usar para la siguiente solicitud al usar las vistas de página de fracción.</span><span class="sxs-lookup"><span data-stu-id="71e20-114">Represents the new numerator value to use for the next request when using fraction page views.</span></span>  <br/> |
|<span data-ttu-id="71e20-115">**AbsoluteDenominator**</span><span class="sxs-lookup"><span data-stu-id="71e20-115">**AbsoluteDenominator**</span></span> <br/> |<span data-ttu-id="71e20-116">Representa el siguiente denominador que se va a usar para la siguiente solicitud cuando se realiza una paginación fraccionada.</span><span class="sxs-lookup"><span data-stu-id="71e20-116">Represents the next denominator to use for the next request when doing fractional paging.</span></span>  <br/> |
|<span data-ttu-id="71e20-117">**IncludesLastItemInRange**</span><span class="sxs-lookup"><span data-stu-id="71e20-117">**IncludesLastItemInRange**</span></span> <br/> |<span data-ttu-id="71e20-118">Indica si los resultados actuales contienen el último elemento de la consulta, de modo que no es necesario realizar más paginación.</span><span class="sxs-lookup"><span data-stu-id="71e20-118">Indicates whether the current results contain the last item in the query, such that further paging is not needed.</span></span>  <br/> |
|<span data-ttu-id="71e20-119">**TotalItemsInView**</span><span class="sxs-lookup"><span data-stu-id="71e20-119">**TotalItemsInView**</span></span> <br/> |<span data-ttu-id="71e20-120">Representa el número total de elementos que supera la restricción.</span><span class="sxs-lookup"><span data-stu-id="71e20-120">Represents the total number of items that pass the restriction.</span></span> <span data-ttu-id="71e20-121">En una [operación FindItem](finditem-operation.md)agrupada, el atributo **TotalItemsInView** devuelve el número total de elementos en la vista más el número total de grupos.</span><span class="sxs-lookup"><span data-stu-id="71e20-121">In a grouped [FindItem operation](finditem-operation.md), the **TotalItemsInView** attribute returns the total number of items in the view plus the total number of groups.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="71e20-122">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="71e20-122">Child elements</span></span>

|<span data-ttu-id="71e20-123">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="71e20-123">**Element**</span></span>|<span data-ttu-id="71e20-124">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="71e20-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="71e20-125">Items</span><span class="sxs-lookup"><span data-stu-id="71e20-125">Items</span></span>](items.md) <br/> |<span data-ttu-id="71e20-126">Contiene una matriz de elementos encontrados que tienen los criterios de búsqueda identificados en la solicitud de [operación FindItem](finditem-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="71e20-126">Contains an array of items found that have the search criteria identified in the [FindItem operation](finditem-operation.md) request.</span></span>  <br/> |
|[<span data-ttu-id="71e20-127">Grupos</span><span class="sxs-lookup"><span data-stu-id="71e20-127">Groups</span></span>](groups.md) <br/> |<span data-ttu-id="71e20-128">Contiene una colección de grupos encontrados que tienen los criterios de búsqueda y agregación identificados en la solicitud de [operación FindItem](finditem-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="71e20-128">Contains a collection of groups found that have the search and aggregation criteria identified in the [FindItem operation](finditem-operation.md) request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="71e20-129">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="71e20-129">Parent elements</span></span>

|<span data-ttu-id="71e20-130">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="71e20-130">**Element**</span></span>|<span data-ttu-id="71e20-131">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="71e20-131">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="71e20-132">FindItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="71e20-132">FindItemResponseMessage</span></span>](finditemresponsemessage.md) <br/> |<span data-ttu-id="71e20-133">Contiene el estado y el resultado de una solicitud de [operación de FindItem](finditem-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="71e20-133">Contains the status and result of a [FindItem operation](finditem-operation.md) request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="71e20-134">Comentarios</span><span class="sxs-lookup"><span data-stu-id="71e20-134">Remarks</span></span>

<span data-ttu-id="71e20-135">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Exchange Server con el rol de servidor acceso de clientes instalado.</span><span class="sxs-lookup"><span data-stu-id="71e20-135">The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange Server with the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="71e20-136">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="71e20-136">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="71e20-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="71e20-137">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="71e20-138">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="71e20-138">Schema name</span></span>  <br/> |<span data-ttu-id="71e20-139">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="71e20-139">Messages schema</span></span>  <br/> |
|<span data-ttu-id="71e20-140">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="71e20-140">Validation file</span></span>  <br/> |<span data-ttu-id="71e20-141">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="71e20-141">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="71e20-142">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="71e20-142">Can be empty</span></span>  <br/> |<span data-ttu-id="71e20-143">Falso</span><span class="sxs-lookup"><span data-stu-id="71e20-143">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="71e20-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="71e20-144">See also</span></span>



[<span data-ttu-id="71e20-145">Operación FindItem</span><span class="sxs-lookup"><span data-stu-id="71e20-145">FindItem operation</span></span>](finditem-operation.md)
  
[<span data-ttu-id="71e20-146">IndexedPagingOffset</span><span class="sxs-lookup"><span data-stu-id="71e20-146">IndexedPagingOffset</span></span>](https://msdn.microsoft.com/library/ExchangeWebServices.FindItemParentType.IndexedPagingOffset.aspx)
  
[<span data-ttu-id="71e20-147">NumeratorOffset</span><span class="sxs-lookup"><span data-stu-id="71e20-147">NumeratorOffset</span></span>](https://msdn.microsoft.com/library/ExchangeWebServices.FindItemParentType.NumeratorOffset.aspx)
  
[<span data-ttu-id="71e20-148">AbsoluteDenominator</span><span class="sxs-lookup"><span data-stu-id="71e20-148">AbsoluteDenominator</span></span>](https://msdn.microsoft.com/library/ExchangeWebServices.FindItemParentType.AbsoluteDenominator.aspx)
  
[<span data-ttu-id="71e20-149">IncludesLastItemInRange</span><span class="sxs-lookup"><span data-stu-id="71e20-149">IncludesLastItemInRange</span></span>](https://msdn.microsoft.com/library/ExchangeWebServices.FindItemParentType.IncludesLastItemInRange.aspx)
  
[<span data-ttu-id="71e20-150">TotalItemsInView</span><span class="sxs-lookup"><span data-stu-id="71e20-150">TotalItemsInView</span></span>](https://msdn.microsoft.com/library/ExchangeWebServices.FindItemParentType.TotalItemsInView.aspx)


[<span data-ttu-id="71e20-151">Buscar elementos</span><span class="sxs-lookup"><span data-stu-id="71e20-151">Finding Items</span></span>](https://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

