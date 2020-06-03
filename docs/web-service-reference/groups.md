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
description: El elemento Groups contiene una colección de grupos que se encuentran con los criterios de búsqueda y agregación que se identifican en la solicitud de operación FindItem.
ms.openlocfilehash: 915d9dffd6d8cec1def6634e6b70642d563b5242
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530792"
---
# <a name="groups"></a><span data-ttu-id="65bab-103">Grupos</span><span class="sxs-lookup"><span data-stu-id="65bab-103">Groups</span></span>

<span data-ttu-id="65bab-104">El elemento **Groups** contiene una colección de grupos que se encuentran con los criterios de búsqueda y agregación que se identifican en la solicitud de [operación FindItem](finditem-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="65bab-104">The **Groups** element contains a collection of groups that are found with the search and aggregation criteria that is identified in the [FindItem operation](finditem-operation.md) request.</span></span> 
  
```xml
<Groups>
   <GroupedItems/>
</Groups>
```

 <span data-ttu-id="65bab-105">**ArrayOfGroupedItemsType**</span><span class="sxs-lookup"><span data-stu-id="65bab-105">**ArrayOfGroupedItemsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="65bab-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="65bab-106">Attributes and elements</span></span>

<span data-ttu-id="65bab-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="65bab-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="65bab-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="65bab-108">Attributes</span></span>

<span data-ttu-id="65bab-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="65bab-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="65bab-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="65bab-110">Child elements</span></span>

|<span data-ttu-id="65bab-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="65bab-111">**Element**</span></span>|<span data-ttu-id="65bab-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="65bab-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="65bab-113">GroupedItems</span><span class="sxs-lookup"><span data-stu-id="65bab-113">GroupedItems</span></span>](groupeditems.md) <br/> |<span data-ttu-id="65bab-114">Representa una colección de elementos que son el resultado de una llamada de [operación FindItem](finditem-operation.md) agrupada.</span><span class="sxs-lookup"><span data-stu-id="65bab-114">Represents a collection of items that are the result of a grouped [FindItem operation](finditem-operation.md) call.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="65bab-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="65bab-115">Parent elements</span></span>

|<span data-ttu-id="65bab-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="65bab-116">**Element**</span></span>|<span data-ttu-id="65bab-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="65bab-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="65bab-118">RootFolder (FindItemResponseMessage)</span><span class="sxs-lookup"><span data-stu-id="65bab-118">RootFolder (FindItemResponseMessage)</span></span>](rootfolder-finditemresponsemessage.md) <br/> |<span data-ttu-id="65bab-119">Contiene los resultados de una búsqueda de una carpeta raíz única durante una operación de [operación FindItem](finditem-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="65bab-119">Contains the results from a search of a single root folder during a [FindItem operation](finditem-operation.md) operation.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="65bab-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="65bab-120">Remarks</span></span>

<span data-ttu-id="65bab-121">Se producirá una instancia de [GroupedItems](groupeditems.md) para cada grupo definido dentro del resultado.</span><span class="sxs-lookup"><span data-stu-id="65bab-121">One [GroupedItems](groupeditems.md) instance will occur for each distinct group within the result.</span></span> 
  
<span data-ttu-id="65bab-122">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2010 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="65bab-122">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="65bab-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="65bab-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="65bab-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="65bab-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="65bab-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="65bab-125">Schema name</span></span>  <br/> |<span data-ttu-id="65bab-126">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="65bab-126">Types schema</span></span>  <br/> |
|<span data-ttu-id="65bab-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="65bab-127">Validation file</span></span>  <br/> |<span data-ttu-id="65bab-128">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="65bab-128">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="65bab-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="65bab-129">Can be empty</span></span>  <br/> |<span data-ttu-id="65bab-130">Falso</span><span class="sxs-lookup"><span data-stu-id="65bab-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="65bab-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="65bab-131">See also</span></span>



[<span data-ttu-id="65bab-132">Operación FindItem</span><span class="sxs-lookup"><span data-stu-id="65bab-132">FindItem operation</span></span>](finditem-operation.md)


[<span data-ttu-id="65bab-133">Buscar elementos</span><span class="sxs-lookup"><span data-stu-id="65bab-133">Finding Items</span></span>](https://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

