---
title: Grupos
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Groups
api_type:
- schema
ms.assetid: 6b6b2d67-219d-4dfb-a4ed-d627b1cfb33f
description: El elemento grupos contiene una colección de grupos que se encuentran con los criterios de búsqueda y de agregación que se identifica en la solicitud de operación FindItem.
ms.openlocfilehash: 406a1974899e89243f52ba7a56afcc172c4f3df6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19835786"
---
# <a name="groups"></a><span data-ttu-id="96af2-103">Grupos</span><span class="sxs-lookup"><span data-stu-id="96af2-103">Groups</span></span>

<span data-ttu-id="96af2-104">El elemento **grupos** contiene una colección de grupos que se encuentran con los criterios de búsqueda y de agregación que se identifica en la solicitud de [operación FindItem](finditem-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="96af2-104">The **Groups** element contains a collection of groups that are found with the search and aggregation criteria that is identified in the [FindItem operation](finditem-operation.md) request.</span></span> 
  
```xml
<Groups>
   <GroupedItems/>
</Groups>
```

 <span data-ttu-id="96af2-105">**ArrayOfGroupedItemsType**</span><span class="sxs-lookup"><span data-stu-id="96af2-105">**ArrayOfGroupedItemsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="96af2-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="96af2-106">Attributes and elements</span></span>

<span data-ttu-id="96af2-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="96af2-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="96af2-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="96af2-108">Attributes</span></span>

<span data-ttu-id="96af2-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="96af2-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="96af2-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="96af2-110">Child elements</span></span>

|<span data-ttu-id="96af2-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="96af2-111">**Element**</span></span>|<span data-ttu-id="96af2-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="96af2-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="96af2-113">GroupedItems</span><span class="sxs-lookup"><span data-stu-id="96af2-113">GroupedItems</span></span>](groupeditems.md) <br/> |<span data-ttu-id="96af2-114">Representa una colección de elementos que son el resultado de una [operación FindItem](finditem-operation.md) de agrupada de llamadas.</span><span class="sxs-lookup"><span data-stu-id="96af2-114">Represents a collection of items that are the result of a grouped [FindItem operation](finditem-operation.md) call.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="96af2-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="96af2-115">Parent elements</span></span>

|<span data-ttu-id="96af2-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="96af2-116">**Element**</span></span>|<span data-ttu-id="96af2-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="96af2-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="96af2-118">RootFolder (FindItemResponseMessage)</span><span class="sxs-lookup"><span data-stu-id="96af2-118">RootFolder (FindItemResponseMessage)</span></span>](rootfolder-finditemresponsemessage.md) <br/> |<span data-ttu-id="96af2-119">Contiene los resultados de una búsqueda de una sola carpeta raíz durante una operación de [operación FindItem](finditem-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="96af2-119">Contains the results from a search of a single root folder during a [FindItem operation](finditem-operation.md) operation.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="96af2-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="96af2-120">Remarks</span></span>

<span data-ttu-id="96af2-121">Se producirá una instancia de [GroupedItems](groupeditems.md) para cada grupo de distinto en el resultado.</span><span class="sxs-lookup"><span data-stu-id="96af2-121">One [GroupedItems](groupeditems.md) instance will occur for each distinct group within the result.</span></span> 
  
<span data-ttu-id="96af2-122">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2010 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="96af2-122">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="96af2-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="96af2-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="96af2-124">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="96af2-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="96af2-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="96af2-125">Schema name</span></span>  <br/> |<span data-ttu-id="96af2-126">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="96af2-126">Types schema</span></span>  <br/> |
|<span data-ttu-id="96af2-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="96af2-127">Validation file</span></span>  <br/> |<span data-ttu-id="96af2-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="96af2-128">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="96af2-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="96af2-129">Can be empty</span></span>  <br/> |<span data-ttu-id="96af2-130">False</span><span class="sxs-lookup"><span data-stu-id="96af2-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="96af2-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="96af2-131">See also</span></span>



[<span data-ttu-id="96af2-132">Operación FindItem</span><span class="sxs-lookup"><span data-stu-id="96af2-132">FindItem operation</span></span>](finditem-operation.md)


[<span data-ttu-id="96af2-133">Buscar elementos</span><span class="sxs-lookup"><span data-stu-id="96af2-133">Finding Items</span></span>](http://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

