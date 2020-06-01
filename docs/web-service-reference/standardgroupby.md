---
title: StandardGroupBy
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- StandardGroupBy
api_type:
- schema
ms.assetid: 04a84f71-b7eb-44dc-ac2c-ed504b52c463
description: El elemento StandardGroupBy representa los mecanismos estándar de agrupación y agregación para una operación FindItem agrupada.
ms.openlocfilehash: 3e135feba322979de3d66d5a45d423654ccc9100
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467560"
---
# <a name="standardgroupby"></a><span data-ttu-id="64d58-103">StandardGroupBy</span><span class="sxs-lookup"><span data-stu-id="64d58-103">StandardGroupBy</span></span>

<span data-ttu-id="64d58-104">El elemento **StandardGroupBy** representa los mecanismos estándar de agrupación y agregación para una operación FindItem agrupada.</span><span class="sxs-lookup"><span data-stu-id="64d58-104">The **StandardGroupBy** element represents the standard grouping and aggregating mechanisms for a grouped FindItem operation.</span></span> 
  
[<span data-ttu-id="64d58-105">FindItem</span><span class="sxs-lookup"><span data-stu-id="64d58-105">FindItem</span></span>](finditem.md)
  
[<span data-ttu-id="64d58-106">DistinguishedGroupBy</span><span class="sxs-lookup"><span data-stu-id="64d58-106">DistinguishedGroupBy</span></span>](distinguishedgroupby.md)
  
[<span data-ttu-id="64d58-107">StandardGroupBy</span><span class="sxs-lookup"><span data-stu-id="64d58-107">StandardGroupBy</span></span>](standardgroupby.md)
  
```xml
<StandardGroupBy/>
```

 <span data-ttu-id="64d58-108">**StandardGroupByType**</span><span class="sxs-lookup"><span data-stu-id="64d58-108">**StandardGroupByType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="64d58-109">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="64d58-109">Attributes and elements</span></span>

<span data-ttu-id="64d58-110">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="64d58-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="64d58-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="64d58-111">Attributes</span></span>

<span data-ttu-id="64d58-112">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="64d58-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="64d58-113">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="64d58-113">Child elements</span></span>

<span data-ttu-id="64d58-114">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="64d58-114">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="64d58-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="64d58-115">Parent elements</span></span>

|<span data-ttu-id="64d58-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="64d58-116">**Element**</span></span>|<span data-ttu-id="64d58-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="64d58-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="64d58-118">DistinguishedGroupBy</span><span class="sxs-lookup"><span data-stu-id="64d58-118">DistinguishedGroupBy</span></span>](distinguishedgroupby.md) <br/> |<span data-ttu-id="64d58-119">Proporciona agrupaciones estándar para las consultas FindItem.</span><span class="sxs-lookup"><span data-stu-id="64d58-119">Provides standard groupings for FindItem queries.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="64d58-120">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="64d58-120">Text value</span></span>

<span data-ttu-id="64d58-121">Se requiere un valor de texto.</span><span class="sxs-lookup"><span data-stu-id="64d58-121">A text value is required.</span></span> <span data-ttu-id="64d58-122">El único valor que se puede usar para este elemento es **ConversationTopic**.</span><span class="sxs-lookup"><span data-stu-id="64d58-122">The only value that can be used for this element is **ConversationTopic**.</span></span> <span data-ttu-id="64d58-123">**ConversationTopic** grupos por mensaje: ConversationTopic y agregados en el elemento: DateTimeReceived (máximo).</span><span class="sxs-lookup"><span data-stu-id="64d58-123">**ConversationTopic** groups by message:ConversationTopic and aggregates on item:DateTimeReceived (maximum).</span></span> <span data-ttu-id="64d58-124">Para obtener más información acerca de la agregación, vea [AggregateOn](aggregateon.md).</span><span class="sxs-lookup"><span data-stu-id="64d58-124">For more information about aggregation, see [AggregateOn](aggregateon.md).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="64d58-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="64d58-125">Remarks</span></span>

<span data-ttu-id="64d58-126">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="64d58-126">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="64d58-127">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="64d58-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="64d58-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="64d58-128">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="64d58-129">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="64d58-129">Schema Name</span></span>  <br/> |<span data-ttu-id="64d58-130">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="64d58-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="64d58-131">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="64d58-131">Validation File</span></span>  <br/> |<span data-ttu-id="64d58-132">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="64d58-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="64d58-133">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="64d58-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="64d58-134">Falso</span><span class="sxs-lookup"><span data-stu-id="64d58-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="64d58-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="64d58-135">See also</span></span>



[<span data-ttu-id="64d58-136">Operación FindItem</span><span class="sxs-lookup"><span data-stu-id="64d58-136">FindItem operation</span></span>](finditem-operation.md)
  
[<span data-ttu-id="64d58-137">FindItem</span><span class="sxs-lookup"><span data-stu-id="64d58-137">FindItem</span></span>](finditem.md)


[<span data-ttu-id="64d58-138">Buscar elementos</span><span class="sxs-lookup"><span data-stu-id="64d58-138">Finding Items</span></span>](https://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

