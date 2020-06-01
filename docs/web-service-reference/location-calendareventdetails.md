---
title: Ubicación (CalendarEventDetails)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Location
api_type:
- schema
ms.assetid: 883cce6e-66b8-4dbc-935c-83ef5100a953
description: El elemento Location representa el campo de ubicación del elemento de calendario.
ms.openlocfilehash: 4a590c315d2211ce9128305a514e68f1c785596c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44468001"
---
# <a name="location-calendareventdetails"></a><span data-ttu-id="e187a-103">Ubicación (CalendarEventDetails)</span><span class="sxs-lookup"><span data-stu-id="e187a-103">Location (CalendarEventDetails)</span></span>

<span data-ttu-id="e187a-104">El elemento **Location** representa el campo de ubicación del elemento de calendario.</span><span class="sxs-lookup"><span data-stu-id="e187a-104">The **Location** element represents the location field of the calendar item.</span></span> 
  
[<span data-ttu-id="e187a-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="e187a-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="e187a-106">FreeBusyResponseArray</span><span class="sxs-lookup"><span data-stu-id="e187a-106">FreeBusyResponseArray</span></span>](freebusyresponsearray.md)
  
[<span data-ttu-id="e187a-107">FreeBusyResponse</span><span class="sxs-lookup"><span data-stu-id="e187a-107">FreeBusyResponse</span></span>](freebusyresponse.md)
  
[<span data-ttu-id="e187a-108">FreeBusyView</span><span class="sxs-lookup"><span data-stu-id="e187a-108">FreeBusyView</span></span>](freebusyview.md)
  
[<span data-ttu-id="e187a-109">CalendarEventArray</span><span class="sxs-lookup"><span data-stu-id="e187a-109">CalendarEventArray</span></span>](calendareventarray.md)
  
[<span data-ttu-id="e187a-110">CalendarEvent</span><span class="sxs-lookup"><span data-stu-id="e187a-110">CalendarEvent</span></span>](calendarevent.md)
  
[<span data-ttu-id="e187a-111">CalendarEventDetails</span><span class="sxs-lookup"><span data-stu-id="e187a-111">CalendarEventDetails</span></span>](calendareventdetails.md)
  
[<span data-ttu-id="e187a-112">Ubicación (CalendarEventDetails)</span><span class="sxs-lookup"><span data-stu-id="e187a-112">Location (CalendarEventDetails)</span></span>](location-calendareventdetails.md)
  
```xml
<Location/>
```

 <span data-ttu-id="e187a-113">**string**</span><span class="sxs-lookup"><span data-stu-id="e187a-113">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e187a-114">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="e187a-114">Attributes and elements</span></span>

<span data-ttu-id="e187a-115">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="e187a-115">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e187a-116">Atributos</span><span class="sxs-lookup"><span data-stu-id="e187a-116">Attributes</span></span>

<span data-ttu-id="e187a-117">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="e187a-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e187a-118">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="e187a-118">Child elements</span></span>

<span data-ttu-id="e187a-119">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="e187a-119">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="e187a-120">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="e187a-120">Parent elements</span></span>

|<span data-ttu-id="e187a-121">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="e187a-121">**Element**</span></span>|<span data-ttu-id="e187a-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e187a-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e187a-123">CalendarEventDetails</span><span class="sxs-lookup"><span data-stu-id="e187a-123">CalendarEventDetails</span></span>](calendareventdetails.md) <br/> |<span data-ttu-id="e187a-124">Proporciona información adicional para un evento de calendario.</span><span class="sxs-lookup"><span data-stu-id="e187a-124">Provides additional information for a calendar event.</span></span>  <br/> <span data-ttu-id="e187a-125">La siguiente es la expresión XPath a este elemento:</span><span class="sxs-lookup"><span data-stu-id="e187a-125">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/CalendarEventArray/CalendarEvent[i]/CalendarEventDetails` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="e187a-126">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="e187a-126">Text value</span></span>

<span data-ttu-id="e187a-127">Es necesario un valor de texto si este elemento se devuelve en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e187a-127">A text value is required if this element is returned in the response.</span></span> <span data-ttu-id="e187a-128">Este elemento puede contener una cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="e187a-128">This element can contain an empty string.</span></span> <span data-ttu-id="e187a-129">Este elemento es opcional si se usa el elemento [CalendarEventDetails](calendareventdetails.md) .</span><span class="sxs-lookup"><span data-stu-id="e187a-129">This element is optional if the [CalendarEventDetails](calendareventdetails.md) element is used.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="e187a-130">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e187a-130">Remarks</span></span>

<span data-ttu-id="e187a-131">Este elemento se asigna a un PR_Location propiedad con nombre de MAPI.</span><span class="sxs-lookup"><span data-stu-id="e187a-131">This element maps to a PR_Location MAPI named property.</span></span>
  
<span data-ttu-id="e187a-132">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="e187a-132">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e187a-133">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="e187a-133">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e187a-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="e187a-134">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="e187a-135">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="e187a-135">Schema Name</span></span>  <br/> |<span data-ttu-id="e187a-136">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="e187a-136">Types schema</span></span>  <br/> |
|<span data-ttu-id="e187a-137">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="e187a-137">Validation File</span></span>  <br/> |<span data-ttu-id="e187a-138">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="e187a-138">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="e187a-139">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="e187a-139">Can be Empty</span></span>  <br/> |<span data-ttu-id="e187a-140">Falso</span><span class="sxs-lookup"><span data-stu-id="e187a-140">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e187a-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="e187a-141">See also</span></span>



[<span data-ttu-id="e187a-142">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="e187a-142">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="e187a-143">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="e187a-143">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="e187a-144">Obtener disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="e187a-144">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

