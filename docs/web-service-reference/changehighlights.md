---
title: ChangeHighlights
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f9bd7323-44db-4d2f-aaaa-94c2dfdeead6
description: El elemento ChangeHighlights especifica lo que ha cambiado entre dos versiones de un mensaje de convocatoria de reunión.
ms.openlocfilehash: 6c78d2c96449ee41032859f90bf51d6e0faa92ae
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463282"
---
# <a name="changehighlights"></a><span data-ttu-id="3153c-103">ChangeHighlights</span><span class="sxs-lookup"><span data-stu-id="3153c-103">ChangeHighlights</span></span>

<span data-ttu-id="3153c-104">El elemento **ChangeHighlights** especifica lo que ha cambiado entre dos versiones de un mensaje de convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="3153c-104">The **ChangeHighlights** element specifies what has changed between two versions of a meeting request message.</span></span> 
  
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

 <span data-ttu-id="3153c-105">**ChangeHighlightsType**</span><span class="sxs-lookup"><span data-stu-id="3153c-105">**ChangeHighlightsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3153c-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="3153c-106">Attributes and elements</span></span>

<span data-ttu-id="3153c-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="3153c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3153c-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="3153c-108">Attributes</span></span>

<span data-ttu-id="3153c-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="3153c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3153c-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="3153c-110">Child elements</span></span>

|<span data-ttu-id="3153c-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="3153c-111">**Element**</span></span>|<span data-ttu-id="3153c-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3153c-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3153c-113">HasLocationChanged</span><span class="sxs-lookup"><span data-stu-id="3153c-113">HasLocationChanged</span></span>](haslocationchanged.md) <br/> |<span data-ttu-id="3153c-114">Especifica si la propiedad Location de una reunión ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="3153c-114">Specifies whether the location property of a meeting has changed.</span></span>  <br/> |
|[<span data-ttu-id="3153c-115">Ubicación</span><span class="sxs-lookup"><span data-stu-id="3153c-115">Location</span></span>](location.md) <br/> |<span data-ttu-id="3153c-116">Representa la ubicación de una reunión o cita.</span><span class="sxs-lookup"><span data-stu-id="3153c-116">Represents the location of a meeting or appointment.</span></span>  <br/> |
|[<span data-ttu-id="3153c-117">HasStartTimeChanged</span><span class="sxs-lookup"><span data-stu-id="3153c-117">HasStartTimeChanged</span></span>](hasstarttimechanged.md) <br/> |<span data-ttu-id="3153c-118">Especifica si la hora de inicio de una reunión ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="3153c-118">Specifies whether the start time for a meeting has changed.</span></span>  <br/> |
|[<span data-ttu-id="3153c-119">Start</span><span class="sxs-lookup"><span data-stu-id="3153c-119">Start</span></span>](start.md) <br/> |<span data-ttu-id="3153c-120">Representa el inicio de una duración.</span><span class="sxs-lookup"><span data-stu-id="3153c-120">Represents the start of a duration.</span></span>  <br/> |
|[<span data-ttu-id="3153c-121">HasEndTimeChanged</span><span class="sxs-lookup"><span data-stu-id="3153c-121">HasEndTimeChanged</span></span>](hasendtimechanged.md) <br/> |<span data-ttu-id="3153c-122">Especifica si ha cambiado la hora de finalización de una reunión.</span><span class="sxs-lookup"><span data-stu-id="3153c-122">Specifies whether the end time for a meeting has changed.</span></span>  <br/> |
|[<span data-ttu-id="3153c-123">Centraliza</span><span class="sxs-lookup"><span data-stu-id="3153c-123">End </span></span>](end-ex15websvcsotherref.md) <br/> |<span data-ttu-id="3153c-124">Representa el final de una duración.</span><span class="sxs-lookup"><span data-stu-id="3153c-124">Represents the end of a duration.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="3153c-125">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="3153c-125">Parent elements</span></span>

|<span data-ttu-id="3153c-126">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="3153c-126">**Element**</span></span>|<span data-ttu-id="3153c-127">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3153c-127">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3153c-128">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="3153c-128">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="3153c-129">Representa una convocatoria de reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="3153c-129">Represents a meeting request in the Exchange store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3153c-130">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3153c-130">Remarks</span></span>

<span data-ttu-id="3153c-131">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="3153c-131">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="3153c-132">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="3153c-132">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3153c-133">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="3153c-133">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3153c-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="3153c-134">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="3153c-135">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="3153c-135">Schema Name</span></span>  <br/> |<span data-ttu-id="3153c-136">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="3153c-136">Type schema</span></span>  <br/> |
|<span data-ttu-id="3153c-137">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="3153c-137">Validation File</span></span>  <br/> |<span data-ttu-id="3153c-138">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="3153c-138">types.xsd</span></span>  <br/> |
|<span data-ttu-id="3153c-139">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="3153c-139">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="3153c-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="3153c-140">See also</span></span>



- [<span data-ttu-id="3153c-141">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="3153c-141">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

