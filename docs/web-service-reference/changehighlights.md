---
title: ChangeHighlights
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f9bd7323-44db-4d2f-aaaa-94c2dfdeead6
description: Mensaje de solicitud de la ChangeHighlights elemento especifica qué ha cambiado entre dos versiones de una reunión.
ms.openlocfilehash: 5fe7aa95f60ae95f1af24e8f7a0463ad49716f65
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763733"
---
# <a name="changehighlights"></a><span data-ttu-id="d8897-103">ChangeHighlights</span><span class="sxs-lookup"><span data-stu-id="d8897-103">ChangeHighlights</span></span>

<span data-ttu-id="d8897-104">El elemento **ChangeHighlights** especifica qué ha cambiado entre dos versiones de una reunión de mensaje de solicitud.</span><span class="sxs-lookup"><span data-stu-id="d8897-104">The **ChangeHighlights** element specifies what has changed between two versions of a meeting request message.</span></span> 
  
```XML
<ChangeHighlights>
    <HasLocationChanged></HasLocationChanged>
    <Location></Location>
    <HasStartTimeChanged></HasStartTimeChanged>
    <Start></Start>
    <HasEndTimeChanged></HasEndTimeChanged>
    <End></End>
</ChangeHighlights>
```

 <span data-ttu-id="d8897-105">**ChangeHighlightsType**</span><span class="sxs-lookup"><span data-stu-id="d8897-105">**ChangeHighlightsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d8897-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="d8897-106">Attributes and elements</span></span>

<span data-ttu-id="d8897-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="d8897-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d8897-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="d8897-108">Attributes</span></span>

<span data-ttu-id="d8897-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="d8897-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d8897-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="d8897-110">Child elements</span></span>

|<span data-ttu-id="d8897-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="d8897-111">**Element**</span></span>|<span data-ttu-id="d8897-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d8897-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d8897-113">HasLocationChanged</span><span class="sxs-lookup"><span data-stu-id="d8897-113">HasLocationChanged</span></span>](haslocationchanged.md) <br/> |<span data-ttu-id="d8897-114">Especifica si se ha cambiado la propiedad de ubicación de una reunión.</span><span class="sxs-lookup"><span data-stu-id="d8897-114">Specifies whether the location property of a meeting has changed.</span></span>  <br/> |
|[<span data-ttu-id="d8897-115">Location</span><span class="sxs-lookup"><span data-stu-id="d8897-115">Location</span></span>](location.md) <br/> |<span data-ttu-id="d8897-116">Representa la ubicación de una reunión o una cita.</span><span class="sxs-lookup"><span data-stu-id="d8897-116">Represents the location of a meeting or appointment.</span></span>  <br/> |
|[<span data-ttu-id="d8897-117">HasStartTimeChanged</span><span class="sxs-lookup"><span data-stu-id="d8897-117">HasStartTimeChanged</span></span>](hasstarttimechanged.md) <br/> |<span data-ttu-id="d8897-118">Especifica si se ha cambiado la hora de inicio para una reunión.</span><span class="sxs-lookup"><span data-stu-id="d8897-118">Specifies whether the start time for a meeting has changed.</span></span>  <br/> |
|[<span data-ttu-id="d8897-119">Start</span><span class="sxs-lookup"><span data-stu-id="d8897-119">Start</span></span>](start.md) <br/> |<span data-ttu-id="d8897-120">Representa el inicio de la duración.</span><span class="sxs-lookup"><span data-stu-id="d8897-120">Represents the start of a duration.</span></span>  <br/> |
|[<span data-ttu-id="d8897-121">HasEndTimeChanged</span><span class="sxs-lookup"><span data-stu-id="d8897-121">HasEndTimeChanged</span></span>](hasendtimechanged.md) <br/> |<span data-ttu-id="d8897-122">Especifica si se ha cambiado la hora de finalización de una reunión.</span><span class="sxs-lookup"><span data-stu-id="d8897-122">Specifies whether the end time for a meeting has changed.</span></span>  <br/> |
|[<span data-ttu-id="d8897-123">End</span><span class="sxs-lookup"><span data-stu-id="d8897-123">End </span></span>](end-ex15websvcsotherref.md) <br/> |<span data-ttu-id="d8897-124">Representa el final de una duración.</span><span class="sxs-lookup"><span data-stu-id="d8897-124">Represents the end of a duration.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d8897-125">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="d8897-125">Parent elements</span></span>

|<span data-ttu-id="d8897-126">**Element**</span><span class="sxs-lookup"><span data-stu-id="d8897-126">**Element**</span></span>|<span data-ttu-id="d8897-127">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d8897-127">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d8897-128">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="d8897-128">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="d8897-129">Representa una convocatoria de reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="d8897-129">Represents a meeting request in the Exchange store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d8897-130">Notas</span><span class="sxs-lookup"><span data-stu-id="d8897-130">Remarks</span></span>

<span data-ttu-id="d8897-131">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="d8897-131">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="d8897-132">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="d8897-132">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d8897-133">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="d8897-133">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d8897-134">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d8897-134">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d8897-135">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="d8897-135">Schema Name</span></span>  <br/> |<span data-ttu-id="d8897-136">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="d8897-136">Type schema</span></span>  <br/> |
|<span data-ttu-id="d8897-137">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="d8897-137">Validation File</span></span>  <br/> |<span data-ttu-id="d8897-138">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="d8897-138">types.xsd</span></span>  <br/> |
|<span data-ttu-id="d8897-139">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="d8897-139">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="d8897-140">Ver también</span><span class="sxs-lookup"><span data-stu-id="d8897-140">See also</span></span>



- [<span data-ttu-id="d8897-141">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="d8897-141">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

