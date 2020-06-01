---
title: CalendarEventArray
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CalendarEventArray
api_type:
- schema
ms.assetid: a00f7f56-d7f1-429d-ae02-97043718c864
description: El elemento CalendarEventArray contiene un conjunto de ocurrencias de elemento de calendario únicas que representan la disponibilidad del usuario solicitado.
ms.openlocfilehash: 6badba2477a9d48c6d109740de454e2815d3c211
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463373"
---
# <a name="calendareventarray"></a><span data-ttu-id="d4ee5-103">CalendarEventArray</span><span class="sxs-lookup"><span data-stu-id="d4ee5-103">CalendarEventArray</span></span>

<span data-ttu-id="d4ee5-104">El elemento **CalendarEventArray** contiene un conjunto de ocurrencias de elemento de calendario únicas que representan la disponibilidad del usuario solicitado.</span><span class="sxs-lookup"><span data-stu-id="d4ee5-104">The **CalendarEventArray** element contains a set of unique calendar item occurrences that represent the requested user's availability.</span></span> 
  
[<span data-ttu-id="d4ee5-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="d4ee5-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="d4ee5-106">FreeBusyResponseArray</span><span class="sxs-lookup"><span data-stu-id="d4ee5-106">FreeBusyResponseArray</span></span>](freebusyresponsearray.md)
  
[<span data-ttu-id="d4ee5-107">FreeBusyResponse</span><span class="sxs-lookup"><span data-stu-id="d4ee5-107">FreeBusyResponse</span></span>](freebusyresponse.md)
  
[<span data-ttu-id="d4ee5-108">FreeBusyView</span><span class="sxs-lookup"><span data-stu-id="d4ee5-108">FreeBusyView</span></span>](freebusyview.md)
  
[<span data-ttu-id="d4ee5-109">CalendarEventArray</span><span class="sxs-lookup"><span data-stu-id="d4ee5-109">CalendarEventArray</span></span>](calendareventarray.md)
  
```xml
<CalendarEventArray>
   <CalendarEvent>...</CalendarEvent>
</CalendarEventArray>
```

 <span data-ttu-id="d4ee5-110">**ArrayOfCalendarEvent**</span><span class="sxs-lookup"><span data-stu-id="d4ee5-110">**ArrayOfCalendarEvent**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d4ee5-111">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="d4ee5-111">Attributes and elements</span></span>

<span data-ttu-id="d4ee5-112">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="d4ee5-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d4ee5-113">Atributos</span><span class="sxs-lookup"><span data-stu-id="d4ee5-113">Attributes</span></span>

<span data-ttu-id="d4ee5-114">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="d4ee5-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d4ee5-115">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="d4ee5-115">Child elements</span></span>

|<span data-ttu-id="d4ee5-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="d4ee5-116">**Element**</span></span>|<span data-ttu-id="d4ee5-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d4ee5-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d4ee5-118">CalendarEvent</span><span class="sxs-lookup"><span data-stu-id="d4ee5-118">CalendarEvent</span></span>](calendarevent.md) <br/> |<span data-ttu-id="d4ee5-119">Representa una ocurrencia única del elemento de calendario.</span><span class="sxs-lookup"><span data-stu-id="d4ee5-119">Represents a unique calendar item occurrence.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d4ee5-120">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="d4ee5-120">Parent elements</span></span>

|<span data-ttu-id="d4ee5-121">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="d4ee5-121">**Element**</span></span>|<span data-ttu-id="d4ee5-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d4ee5-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d4ee5-123">FreeBusyView</span><span class="sxs-lookup"><span data-stu-id="d4ee5-123">FreeBusyView</span></span>](freebusyview.md) <br/> |<span data-ttu-id="d4ee5-124">Contiene la información de disponibilidad de un usuario específico.</span><span class="sxs-lookup"><span data-stu-id="d4ee5-124">Contains availability information for a specific user.</span></span>  <br/> <span data-ttu-id="d4ee5-125">La siguiente es la expresión XPath 2,0 a este elemento:</span><span class="sxs-lookup"><span data-stu-id="d4ee5-125">The following is the XPath 2.0 expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d4ee5-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d4ee5-126">Remarks</span></span>

<span data-ttu-id="d4ee5-127">El nivel de detalle proporcionado por este elemento depende de los permisos concedidos al solicitante.</span><span class="sxs-lookup"><span data-stu-id="d4ee5-127">The level of detail provided by this element depends on the permissions granted to the requestor.</span></span> <span data-ttu-id="d4ee5-128">Este elemento se incluye cuando el elemento [FreeBusyViewType](freebusyviewtype.md) se establece en **FreeBusy**, **FreeBusyMerged**, **Detailed**o **DetailedMerged**.</span><span class="sxs-lookup"><span data-stu-id="d4ee5-128">This element is included when the [FreeBusyViewType](freebusyviewtype.md) element is set to **FreeBusy**, **FreeBusyMerged**, **Detailed**, or **DetailedMerged**.</span></span> <span data-ttu-id="d4ee5-129">Este elemento no incluye ningún elemento secundario si no hay ningún elemento de calendario presente en la ventana de tiempo solicitada.</span><span class="sxs-lookup"><span data-stu-id="d4ee5-129">This element does not include any child elements if no calendar items are present in the requested time window.</span></span> 
  
<span data-ttu-id="d4ee5-130">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="d4ee5-130">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d4ee5-131">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="d4ee5-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d4ee5-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="d4ee5-132">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d4ee5-133">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="d4ee5-133">Schema Name</span></span>  <br/> |<span data-ttu-id="d4ee5-134">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="d4ee5-134">Types schema</span></span>  <br/> |
|<span data-ttu-id="d4ee5-135">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="d4ee5-135">Validation File</span></span>  <br/> |<span data-ttu-id="d4ee5-136">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="d4ee5-136">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d4ee5-137">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="d4ee5-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="d4ee5-138">Falso</span><span class="sxs-lookup"><span data-stu-id="d4ee5-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d4ee5-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="d4ee5-139">See also</span></span>



[<span data-ttu-id="d4ee5-140">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="d4ee5-140">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="d4ee5-141">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="d4ee5-141">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="d4ee5-142">Obtener disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="d4ee5-142">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

