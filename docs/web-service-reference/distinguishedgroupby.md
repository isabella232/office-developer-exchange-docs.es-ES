---
title: DistinguishedGroupBy
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DistinguishedGroupBy
api_type:
- schema
ms.assetid: 6ff3ac48-02ba-40ec-a71b-c401bb2b127c
description: El elemento DistinguishedGroupBy proporciona agrupaciones estándar para las consultas FindItem.
ms.openlocfilehash: 004613d55419a19f69e960203ae13d8d906b74c8
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463142"
---
# <a name="distinguishedgroupby"></a><span data-ttu-id="18b9b-103">DistinguishedGroupBy</span><span class="sxs-lookup"><span data-stu-id="18b9b-103">DistinguishedGroupBy</span></span>

<span data-ttu-id="18b9b-104">El elemento **DistinguishedGroupBy** proporciona agrupaciones estándar para las consultas FindItem.</span><span class="sxs-lookup"><span data-stu-id="18b9b-104">The **DistinguishedGroupBy** element provides standard groupings for FindItem queries.</span></span> 
  
- [<span data-ttu-id="18b9b-105">FindItem</span><span class="sxs-lookup"><span data-stu-id="18b9b-105">FindItem</span></span>](finditem.md) 
- [<span data-ttu-id="18b9b-106">DistinguishedGroupBy</span><span class="sxs-lookup"><span data-stu-id="18b9b-106">DistinguishedGroupBy</span></span>](distinguishedgroupby.md)
  
```xml
<DistinguishedGroupBy>
   <StandardGroupBy/>
</DistinguishedGroupBy>
```

 <span data-ttu-id="18b9b-107">**DistinguishedGroupByType**</span><span class="sxs-lookup"><span data-stu-id="18b9b-107">**DistinguishedGroupByType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="18b9b-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="18b9b-108">Attributes and elements</span></span>

<span data-ttu-id="18b9b-109">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="18b9b-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="18b9b-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="18b9b-110">Attributes</span></span>

<span data-ttu-id="18b9b-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="18b9b-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="18b9b-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="18b9b-112">Child elements</span></span>

|<span data-ttu-id="18b9b-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="18b9b-113">**Element**</span></span>|<span data-ttu-id="18b9b-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="18b9b-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="18b9b-115">StandardGroupBy</span><span class="sxs-lookup"><span data-stu-id="18b9b-115">StandardGroupBy</span></span>](standardgroupby.md) <br/> |<span data-ttu-id="18b9b-116">Representa los mecanismos estándar de agrupación y agregación para una operación FindItem agrupada.</span><span class="sxs-lookup"><span data-stu-id="18b9b-116">Represents the standard grouping and aggregating mechanisms for a grouped FindItem operation.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="18b9b-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="18b9b-117">Parent elements</span></span>

|<span data-ttu-id="18b9b-118">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="18b9b-118">**Element**</span></span>|<span data-ttu-id="18b9b-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="18b9b-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="18b9b-120">FindItem</span><span class="sxs-lookup"><span data-stu-id="18b9b-120">FindItem</span></span>](finditem.md) <br/> |<span data-ttu-id="18b9b-121">Define una solicitud para buscar elementos en un buzón.</span><span class="sxs-lookup"><span data-stu-id="18b9b-121">Defines a request to find items in a mailbox.</span></span><br/><br/><span data-ttu-id="18b9b-122">La siguiente es la expresión XPath a este elemento:`/FindItem`</span><span class="sxs-lookup"><span data-stu-id="18b9b-122">The following is the XPath expression to this element:  `/FindItem`</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="18b9b-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="18b9b-123">Remarks</span></span>

<span data-ttu-id="18b9b-124">El elemento **DistinguishedGroupBy** se puede Agregar a una operación FindItem cuando los resultados deben ir agrupados y cuando uno de los grupos estándar cumple los requisitos de agrupación.</span><span class="sxs-lookup"><span data-stu-id="18b9b-124">The **DistinguishedGroupBy** element can be added to a FindItem operation when the results must come backed grouped and when one of the standard groups meets the grouping requirements.</span></span> <span data-ttu-id="18b9b-125">Si no se especifica el elemento **DistinguishedGroupBy** ni el elemento [GroupBy](groupby.md) , los resultados de FindItem se desagruparán de nuevo.</span><span class="sxs-lookup"><span data-stu-id="18b9b-125">If neither the **DistinguishedGroupBy** element nor the [GroupBy](groupby.md) element is specified, FindItem results will come back ungrouped.</span></span> 
  
<span data-ttu-id="18b9b-126">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="18b9b-126">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="18b9b-127">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="18b9b-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="18b9b-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="18b9b-128">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="18b9b-129">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="18b9b-129">Schema Name</span></span>  <br/> |<span data-ttu-id="18b9b-130">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="18b9b-130">Messages schema</span></span>  <br/> |
|<span data-ttu-id="18b9b-131">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="18b9b-131">Validation File</span></span>  <br/> |<span data-ttu-id="18b9b-132">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="18b9b-132">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="18b9b-133">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="18b9b-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="18b9b-134">Falso</span><span class="sxs-lookup"><span data-stu-id="18b9b-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="18b9b-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="18b9b-135">See also</span></span>

- [<span data-ttu-id="18b9b-136">Operación FindItem</span><span class="sxs-lookup"><span data-stu-id="18b9b-136">FindItem operation</span></span>](finditem-operation.md)
- [<span data-ttu-id="18b9b-137">Buscar elementos</span><span class="sxs-lookup"><span data-stu-id="18b9b-137">Finding Items</span></span>](https://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

