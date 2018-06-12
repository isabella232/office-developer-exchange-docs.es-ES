---
title: CalendarEvent
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CalendarEvent
api_type:
- schema
ms.assetid: 91958c01-1fcb-4ac0-8601-5e5b434c988a
description: El elemento CalendarEvent representa una repetición del elemento de calendario único.
ms.openlocfilehash: f7fff7ba511ca12813dd4c2d694e89c97589ba31
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763695"
---
# <a name="calendarevent"></a><span data-ttu-id="3c8c4-103">CalendarEvent</span><span class="sxs-lookup"><span data-stu-id="3c8c4-103">CalendarEvent</span></span>

<span data-ttu-id="3c8c4-104">El elemento **CalendarEvent** representa una repetición del elemento de calendario único.</span><span class="sxs-lookup"><span data-stu-id="3c8c4-104">The **CalendarEvent** element represents a unique calendar item occurrence.</span></span> 
  
[<span data-ttu-id="3c8c4-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="3c8c4-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="3c8c4-106">FreeBusyResponseArray</span><span class="sxs-lookup"><span data-stu-id="3c8c4-106">FreeBusyResponseArray</span></span>](freebusyresponsearray.md)
  
[<span data-ttu-id="3c8c4-107">FreeBusyResponse</span><span class="sxs-lookup"><span data-stu-id="3c8c4-107">FreeBusyResponse</span></span>](freebusyresponse.md)
  
[<span data-ttu-id="3c8c4-108">FreeBusyView</span><span class="sxs-lookup"><span data-stu-id="3c8c4-108">FreeBusyView</span></span>](freebusyview.md)
  
[<span data-ttu-id="3c8c4-109">CalendarEventArray</span><span class="sxs-lookup"><span data-stu-id="3c8c4-109">CalendarEventArray</span></span>](calendareventarray.md)
  
[<span data-ttu-id="3c8c4-110">CalendarEvent</span><span class="sxs-lookup"><span data-stu-id="3c8c4-110">CalendarEvent</span></span>](calendarevent.md)
  
```xml
<CalendarEvent>
   <StartTime>...</StartTime>
   <EndTime>...</EndTime>
   <BusyType>...</BusyType>
   <CalendarEventDetails>...</CalendarEventDetails>
</CalendarEvent>
```

 <span data-ttu-id="3c8c4-111">**CalendarEvent**</span><span class="sxs-lookup"><span data-stu-id="3c8c4-111">**CalendarEvent**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3c8c4-112">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="3c8c4-112">Attributes and elements</span></span>

<span data-ttu-id="3c8c4-113">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="3c8c4-113">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3c8c4-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="3c8c4-114">Attributes</span></span>

<span data-ttu-id="3c8c4-115">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="3c8c4-115">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3c8c4-116">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="3c8c4-116">Child elements</span></span>

|<span data-ttu-id="3c8c4-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="3c8c4-117">**Element**</span></span>|<span data-ttu-id="3c8c4-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3c8c4-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3c8c4-119">StartTime</span><span class="sxs-lookup"><span data-stu-id="3c8c4-119">StartTime</span></span>](starttime.md) <br/> |<span data-ttu-id="3c8c4-120">Representa el inicio de un evento de calendario.</span><span class="sxs-lookup"><span data-stu-id="3c8c4-120">Represents the start of a calendar event.</span></span> <span data-ttu-id="3c8c4-121">Esto es un elemento secundario necesario.</span><span class="sxs-lookup"><span data-stu-id="3c8c4-121">This is a required child element.</span></span>  <br/> |
|[<span data-ttu-id="3c8c4-122">Hora de finalización</span><span class="sxs-lookup"><span data-stu-id="3c8c4-122">EndTime</span></span>](endtime.md) <br/> |<span data-ttu-id="3c8c4-123">Representa el final de un evento de calendario.</span><span class="sxs-lookup"><span data-stu-id="3c8c4-123">Represents the end of a calendar event.</span></span> <span data-ttu-id="3c8c4-124">Esto es un elemento secundario necesario.</span><span class="sxs-lookup"><span data-stu-id="3c8c4-124">This is a required child element.</span></span>  <br/> |
|[<span data-ttu-id="3c8c4-125">BusyType</span><span class="sxs-lookup"><span data-stu-id="3c8c4-125">BusyType</span></span>](busytype.md) <br/> |<span data-ttu-id="3c8c4-126">Representa el estado de libre/ocupado establecido para un evento del calendario.</span><span class="sxs-lookup"><span data-stu-id="3c8c4-126">Represents the free/busy status set for a calendar event.</span></span> <span data-ttu-id="3c8c4-127">Esto es un elemento secundario necesario.</span><span class="sxs-lookup"><span data-stu-id="3c8c4-127">This is a required child element.</span></span>  <br/> |
|[<span data-ttu-id="3c8c4-128">CalendarEventDetails</span><span class="sxs-lookup"><span data-stu-id="3c8c4-128">CalendarEventDetails</span></span>](calendareventdetails.md) <br/> |<span data-ttu-id="3c8c4-129">Proporciona información adicional para un evento del calendario.</span><span class="sxs-lookup"><span data-stu-id="3c8c4-129">Provides additional information for a calendar event.</span></span> <span data-ttu-id="3c8c4-130">Esto es un elemento secundario opcional.</span><span class="sxs-lookup"><span data-stu-id="3c8c4-130">This is an optional child element.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="3c8c4-131">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="3c8c4-131">Parent elements</span></span>

|<span data-ttu-id="3c8c4-132">**Element**</span><span class="sxs-lookup"><span data-stu-id="3c8c4-132">**Element**</span></span>|<span data-ttu-id="3c8c4-133">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3c8c4-133">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3c8c4-134">CalendarEventArray</span><span class="sxs-lookup"><span data-stu-id="3c8c4-134">CalendarEventArray</span></span>](calendareventarray.md) <br/> |<span data-ttu-id="3c8c4-135">Contiene un conjunto de repeticiones de elemento de calendario únicos que representan la disponibilidad del usuario solicitado.</span><span class="sxs-lookup"><span data-stu-id="3c8c4-135">Contains a set of unique calendar item occurrences that represent the requested user's availability.</span></span>  <br/> <span data-ttu-id="3c8c4-136">La siguiente es la expresión de XPath 2.0 para este elemento:</span><span class="sxs-lookup"><span data-stu-id="3c8c4-136">The following is the XPath 2.0 expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/CalendarEventArray` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3c8c4-137">Notas</span><span class="sxs-lookup"><span data-stu-id="3c8c4-137">Remarks</span></span>

<span data-ttu-id="3c8c4-138">Las horas de reunión y de cita se devuelven en la zona horaria del cliente.</span><span class="sxs-lookup"><span data-stu-id="3c8c4-138">The appointment and meeting times are returned in the time zone of the client.</span></span> <span data-ttu-id="3c8c4-139">Todos los elementos secundarios se enumeran en la secuencia en la que se producen.</span><span class="sxs-lookup"><span data-stu-id="3c8c4-139">All the child elements are listed in the sequence in which they occur.</span></span> <span data-ttu-id="3c8c4-140">El nivel de detalle proporcionado por este elemento depende de los permisos concedidos para el solicitante.</span><span class="sxs-lookup"><span data-stu-id="3c8c4-140">The level of detail provided by this element depends on the permissions granted to the requestor.</span></span>
  
<span data-ttu-id="3c8c4-141">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="3c8c4-141">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3c8c4-142">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="3c8c4-142">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3c8c4-143">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3c8c4-143">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="3c8c4-144">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="3c8c4-144">Schema Name</span></span>  <br/> |<span data-ttu-id="3c8c4-145">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="3c8c4-145">Types schema</span></span>  <br/> |
|<span data-ttu-id="3c8c4-146">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="3c8c4-146">Validation File</span></span>  <br/> |<span data-ttu-id="3c8c4-147">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="3c8c4-147">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="3c8c4-148">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="3c8c4-148">Can be Empty</span></span>  <br/> |<span data-ttu-id="3c8c4-149">False</span><span class="sxs-lookup"><span data-stu-id="3c8c4-149">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3c8c4-150">Ver también</span><span class="sxs-lookup"><span data-stu-id="3c8c4-150">See also</span></span>



[<span data-ttu-id="3c8c4-151">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="3c8c4-151">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="3c8c4-152">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="3c8c4-152">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="3c8c4-153">Obtención de disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="3c8c4-153">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

