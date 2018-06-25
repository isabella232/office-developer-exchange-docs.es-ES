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
description: El elemento DistinguishedGroupBy proporciona agrupaciones estándares para las consultas de FindItem.
ms.openlocfilehash: 0635366447675bf28dedf3af4f7d76094ee5e0a4
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764245"
---
# <a name="distinguishedgroupby"></a><span data-ttu-id="e6780-103">DistinguishedGroupBy</span><span class="sxs-lookup"><span data-stu-id="e6780-103">DistinguishedGroupBy</span></span>

<span data-ttu-id="e6780-104">El elemento **DistinguishedGroupBy** proporciona agrupaciones estándares para las consultas de FindItem.</span><span class="sxs-lookup"><span data-stu-id="e6780-104">The **DistinguishedGroupBy** element provides standard groupings for FindItem queries.</span></span> 
  
- [<span data-ttu-id="e6780-105">FindItem</span><span class="sxs-lookup"><span data-stu-id="e6780-105">FindItem</span></span>](finditem.md) 
- [<span data-ttu-id="e6780-106">DistinguishedGroupBy</span><span class="sxs-lookup"><span data-stu-id="e6780-106">DistinguishedGroupBy</span></span>](distinguishedgroupby.md)
  
```xml
<DistinguishedGroupBy>
   <StandardGroupBy/>
</DistinguishedGroupBy>
```

 <span data-ttu-id="e6780-107">**DistinguishedGroupByType**</span><span class="sxs-lookup"><span data-stu-id="e6780-107">**DistinguishedGroupByType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e6780-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="e6780-108">Attributes and elements</span></span>

<span data-ttu-id="e6780-109">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="e6780-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e6780-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="e6780-110">Attributes</span></span>

<span data-ttu-id="e6780-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="e6780-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e6780-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="e6780-112">Child elements</span></span>

|<span data-ttu-id="e6780-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="e6780-113">**Element**</span></span>|<span data-ttu-id="e6780-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e6780-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e6780-115">StandardGroupBy</span><span class="sxs-lookup"><span data-stu-id="e6780-115">StandardGroupBy</span></span>](standardgroupby.md) <br/> |<span data-ttu-id="e6780-116">Representa el estándar agrupar y agregar mecanismos para una operación FindItem agrupada.</span><span class="sxs-lookup"><span data-stu-id="e6780-116">Represents the standard grouping and aggregating mechanisms for a grouped FindItem operation.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="e6780-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="e6780-117">Parent elements</span></span>

|<span data-ttu-id="e6780-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="e6780-118">**Element**</span></span>|<span data-ttu-id="e6780-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e6780-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e6780-120">FindItem</span><span class="sxs-lookup"><span data-stu-id="e6780-120">FindItem</span></span>](finditem.md) <br/> |<span data-ttu-id="e6780-121">Define una solicitud para buscar elementos en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="e6780-121">Defines a request to find items in a mailbox.</span></span><br/><br/><span data-ttu-id="e6780-122">La siguiente es la expresión de XPath para este elemento:`/FindItem`</span><span class="sxs-lookup"><span data-stu-id="e6780-122">The following is the XPath expression to this element:  `/FindItem`</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e6780-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e6780-123">Remarks</span></span>

<span data-ttu-id="e6780-124">El elemento **DistinguishedGroupBy** puede agregarse a una operación FindItem cuando los resultados deben están respaldados agrupan y cuando uno de los grupos estándares cumple los requisitos de agrupación.</span><span class="sxs-lookup"><span data-stu-id="e6780-124">The **DistinguishedGroupBy** element can be added to a FindItem operation when the results must come backed grouped and when one of the standard groups meets the grouping requirements.</span></span> <span data-ttu-id="e6780-125">Si se especifica el elemento **DistinguishedGroupBy** ni el elemento [GroupBy](groupby.md) , desagrupado FindItem resultados se activará nuevamente.</span><span class="sxs-lookup"><span data-stu-id="e6780-125">If neither the **DistinguishedGroupBy** element nor the [GroupBy](groupby.md) element is specified, FindItem results will come back ungrouped.</span></span> 
  
<span data-ttu-id="e6780-126">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="e6780-126">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e6780-127">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="e6780-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e6780-128">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e6780-128">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="e6780-129">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="e6780-129">Schema Name</span></span>  <br/> |<span data-ttu-id="e6780-130">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="e6780-130">Messages schema</span></span>  <br/> |
|<span data-ttu-id="e6780-131">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="e6780-131">Validation File</span></span>  <br/> |<span data-ttu-id="e6780-132">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="e6780-132">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="e6780-133">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="e6780-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="e6780-134">False</span><span class="sxs-lookup"><span data-stu-id="e6780-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e6780-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="e6780-135">See also</span></span>

- [<span data-ttu-id="e6780-136">Operación FindItem</span><span class="sxs-lookup"><span data-stu-id="e6780-136">FindItem operation</span></span>](finditem-operation.md)
- [<span data-ttu-id="e6780-137">Buscar elementos</span><span class="sxs-lookup"><span data-stu-id="e6780-137">Finding Items</span></span>](http://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)
