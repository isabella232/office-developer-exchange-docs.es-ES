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
description: El elemento GroupedItems representa una colección de elementos que son el resultado de una llamada de operación FindItem agrupada.
ms.openlocfilehash: 0ee1ca3c6d0cf98e2daefa60a1cb1fd096cda478
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530814"
---
# <a name="groupeditems"></a><span data-ttu-id="f869a-103">GroupedItems</span><span class="sxs-lookup"><span data-stu-id="f869a-103">GroupedItems</span></span>

<span data-ttu-id="f869a-104">El elemento **GroupedItems** representa una colección de elementos que son el resultado de una llamada de [operación FindItem](finditem-operation.md) agrupada.</span><span class="sxs-lookup"><span data-stu-id="f869a-104">The **GroupedItems** element represents a collection of items that are the result of a grouped [FindItem operation](finditem-operation.md) call.</span></span> 
  
[<span data-ttu-id="f869a-105">FindItemResponse</span><span class="sxs-lookup"><span data-stu-id="f869a-105">FindItemResponse</span></span>](finditemresponse.md)
  
[<span data-ttu-id="f869a-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="f869a-106">ResponseMessages</span></span>](responsemessages.md)
  
[<span data-ttu-id="f869a-107">FindItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="f869a-107">FindItemResponseMessage</span></span>](finditemresponsemessage.md)
  
[<span data-ttu-id="f869a-108">RootFolder (FindItemResponseMessage)</span><span class="sxs-lookup"><span data-stu-id="f869a-108">RootFolder (FindItemResponseMessage)</span></span>](rootfolder-finditemresponsemessage.md)
  
[<span data-ttu-id="f869a-109">Grupos</span><span class="sxs-lookup"><span data-stu-id="f869a-109">Groups</span></span>](groups.md)
  
[<span data-ttu-id="f869a-110">GroupedItems</span><span class="sxs-lookup"><span data-stu-id="f869a-110">GroupedItems</span></span>](groupeditems.md)
  
```xml
<GroupedItems>
   <GroupIndex/>
   <Items/>
</GroupedItems>
```

 <span data-ttu-id="f869a-111">**GroupedItemsType**</span><span class="sxs-lookup"><span data-stu-id="f869a-111">**GroupedItemsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f869a-112">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="f869a-112">Attributes and elements</span></span>

<span data-ttu-id="f869a-113">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="f869a-113">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f869a-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="f869a-114">Attributes</span></span>

<span data-ttu-id="f869a-115">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="f869a-115">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f869a-116">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="f869a-116">Child elements</span></span>

|<span data-ttu-id="f869a-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="f869a-117">**Element**</span></span>|<span data-ttu-id="f869a-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f869a-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f869a-119">GroupIndex</span><span class="sxs-lookup"><span data-stu-id="f869a-119">GroupIndex</span></span>](groupindex.md) <br/> |<span data-ttu-id="f869a-120">Representa el valor de propiedad que se usa para agrupar elementos en una llamada de [operación FindItem](finditem-operation.md) agrupada.</span><span class="sxs-lookup"><span data-stu-id="f869a-120">Represents the property value that is used to group items in a grouped [FindItem operation](finditem-operation.md) call.</span></span>  <br/> |
|[<span data-ttu-id="f869a-121">Items</span><span class="sxs-lookup"><span data-stu-id="f869a-121">Items</span></span>](items.md) <br/> |<span data-ttu-id="f869a-122">Contiene una matriz de elementos agrupados.</span><span class="sxs-lookup"><span data-stu-id="f869a-122">Contains an array of grouped items.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="f869a-123">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="f869a-123">Parent elements</span></span>

|<span data-ttu-id="f869a-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="f869a-124">**Element**</span></span>|<span data-ttu-id="f869a-125">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f869a-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f869a-126">Grupos</span><span class="sxs-lookup"><span data-stu-id="f869a-126">Groups</span></span>](groups.md) <br/> |<span data-ttu-id="f869a-127">Contiene una colección de grupos que se encuentran con los criterios de búsqueda y agregación que se identifican en la solicitud de [operación FindItem](finditem-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="f869a-127">Contains a collection of groups that are found with the search and aggregation criteria that is identified in the [FindItem operation](finditem-operation.md) request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f869a-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f869a-128">Remarks</span></span>

<span data-ttu-id="f869a-129">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2010 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="f869a-129">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f869a-130">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="f869a-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f869a-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="f869a-131">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f869a-132">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="f869a-132">Schema name</span></span>  <br/> |<span data-ttu-id="f869a-133">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="f869a-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="f869a-134">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="f869a-134">Validation file</span></span>  <br/> |<span data-ttu-id="f869a-135">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="f869a-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="f869a-136">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="f869a-136">Can be empty</span></span>  <br/> |<span data-ttu-id="f869a-137">Falso</span><span class="sxs-lookup"><span data-stu-id="f869a-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f869a-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="f869a-138">See also</span></span>



[<span data-ttu-id="f869a-139">Operación FindItem</span><span class="sxs-lookup"><span data-stu-id="f869a-139">FindItem operation</span></span>](finditem-operation.md)


[<span data-ttu-id="f869a-140">Buscar elementos</span><span class="sxs-lookup"><span data-stu-id="f869a-140">Finding Items</span></span>](https://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

