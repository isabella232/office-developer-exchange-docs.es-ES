---
title: GroupedItems
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GroupedItems
api_type:
- schema
ms.assetid: 53170df4-4272-4b37-b23f-cd8e2d4a7396
description: El elemento GroupedItems representa una colección de elementos que son el resultado de una llamada a una operación FindItem agrupada.
ms.openlocfilehash: f8aed9b78fc54307f44b96a45e5c31a4cc76ab50
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19835756"
---
# <a name="groupeditems"></a><span data-ttu-id="d10c1-103">GroupedItems</span><span class="sxs-lookup"><span data-stu-id="d10c1-103">GroupedItems</span></span>

<span data-ttu-id="d10c1-104">El elemento **GroupedItems** representa una colección de elementos que son el resultado de una [operación FindItem](finditem-operation.md) de agrupada de llamadas.</span><span class="sxs-lookup"><span data-stu-id="d10c1-104">The **GroupedItems** element represents a collection of items that are the result of a grouped [FindItem operation](finditem-operation.md) call.</span></span> 
  
[<span data-ttu-id="d10c1-105">FindItemResponse</span><span class="sxs-lookup"><span data-stu-id="d10c1-105">FindItemResponse</span></span>](finditemresponse.md)
  
[<span data-ttu-id="d10c1-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="d10c1-106">ResponseMessages</span></span>](responsemessages.md)
  
[<span data-ttu-id="d10c1-107">FindItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="d10c1-107">FindItemResponseMessage</span></span>](finditemresponsemessage.md)
  
[<span data-ttu-id="d10c1-108">RootFolder (FindItemResponseMessage)</span><span class="sxs-lookup"><span data-stu-id="d10c1-108">RootFolder (FindItemResponseMessage)</span></span>](rootfolder-finditemresponsemessage.md)
  
[<span data-ttu-id="d10c1-109">Grupos</span><span class="sxs-lookup"><span data-stu-id="d10c1-109">Groups</span></span>](groups.md)
  
[<span data-ttu-id="d10c1-110">GroupedItems</span><span class="sxs-lookup"><span data-stu-id="d10c1-110">GroupedItems</span></span>](groupeditems.md)
  
```xml
<GroupedItems>
   <GroupIndex/>
   <Items/>
</GroupedItems>
```

 <span data-ttu-id="d10c1-111">**GroupedItemsType**</span><span class="sxs-lookup"><span data-stu-id="d10c1-111">**GroupedItemsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d10c1-112">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="d10c1-112">Attributes and elements</span></span>

<span data-ttu-id="d10c1-113">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="d10c1-113">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d10c1-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="d10c1-114">Attributes</span></span>

<span data-ttu-id="d10c1-115">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="d10c1-115">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d10c1-116">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="d10c1-116">Child elements</span></span>

|<span data-ttu-id="d10c1-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="d10c1-117">**Element**</span></span>|<span data-ttu-id="d10c1-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d10c1-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d10c1-119">GroupIndex</span><span class="sxs-lookup"><span data-stu-id="d10c1-119">GroupIndex</span></span>](groupindex.md) <br/> |<span data-ttu-id="d10c1-120">Representa el valor de la propiedad que se usa para agrupar los elementos en una [operación FindItem](finditem-operation.md) de agrupada de llamadas.</span><span class="sxs-lookup"><span data-stu-id="d10c1-120">Represents the property value that is used to group items in a grouped [FindItem operation](finditem-operation.md) call.</span></span>  <br/> |
|[<span data-ttu-id="d10c1-121">Items</span><span class="sxs-lookup"><span data-stu-id="d10c1-121">Items</span></span>](items.md) <br/> |<span data-ttu-id="d10c1-122">Contiene una matriz de elementos agrupados.</span><span class="sxs-lookup"><span data-stu-id="d10c1-122">Contains an array of grouped items.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d10c1-123">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="d10c1-123">Parent elements</span></span>

|<span data-ttu-id="d10c1-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="d10c1-124">**Element**</span></span>|<span data-ttu-id="d10c1-125">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d10c1-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d10c1-126">Grupos</span><span class="sxs-lookup"><span data-stu-id="d10c1-126">Groups</span></span>](groups.md) <br/> |<span data-ttu-id="d10c1-127">Contiene una colección de grupos que se encuentran con los criterios de búsqueda y de agregación que se identifica en la solicitud de [operación FindItem](finditem-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="d10c1-127">Contains a collection of groups that are found with the search and aggregation criteria that is identified in the [FindItem operation](finditem-operation.md) request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d10c1-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d10c1-128">Remarks</span></span>

<span data-ttu-id="d10c1-129">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2010 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="d10c1-129">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d10c1-130">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="d10c1-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d10c1-131">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d10c1-131">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d10c1-132">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="d10c1-132">Schema name</span></span>  <br/> |<span data-ttu-id="d10c1-133">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="d10c1-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="d10c1-134">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="d10c1-134">Validation file</span></span>  <br/> |<span data-ttu-id="d10c1-135">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="d10c1-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d10c1-136">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="d10c1-136">Can be empty</span></span>  <br/> |<span data-ttu-id="d10c1-137">False</span><span class="sxs-lookup"><span data-stu-id="d10c1-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d10c1-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="d10c1-138">See also</span></span>



[<span data-ttu-id="d10c1-139">Operación FindItem</span><span class="sxs-lookup"><span data-stu-id="d10c1-139">FindItem operation</span></span>](finditem-operation.md)


[<span data-ttu-id="d10c1-140">Buscar elementos</span><span class="sxs-lookup"><span data-stu-id="d10c1-140">Finding Items</span></span>](http://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

