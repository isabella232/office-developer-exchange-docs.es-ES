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
description: El elemento CalendarEvent representa una ocurrencia única del elemento de calendario.
ms.openlocfilehash: 8bf37c907ed726e33dd2b1eff9add5d6235704da
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459079"
---
# <a name="calendarevent"></a><span data-ttu-id="73ed9-103">CalendarEvent</span><span class="sxs-lookup"><span data-stu-id="73ed9-103">CalendarEvent</span></span>

<span data-ttu-id="73ed9-104">El elemento **CalendarEvent** representa una ocurrencia única del elemento de calendario.</span><span class="sxs-lookup"><span data-stu-id="73ed9-104">The **CalendarEvent** element represents a unique calendar item occurrence.</span></span> 
  
[<span data-ttu-id="73ed9-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="73ed9-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="73ed9-106">FreeBusyResponseArray</span><span class="sxs-lookup"><span data-stu-id="73ed9-106">FreeBusyResponseArray</span></span>](freebusyresponsearray.md)
  
[<span data-ttu-id="73ed9-107">FreeBusyResponse</span><span class="sxs-lookup"><span data-stu-id="73ed9-107">FreeBusyResponse</span></span>](freebusyresponse.md)
  
[<span data-ttu-id="73ed9-108">FreeBusyView</span><span class="sxs-lookup"><span data-stu-id="73ed9-108">FreeBusyView</span></span>](freebusyview.md)
  
[<span data-ttu-id="73ed9-109">CalendarEventArray</span><span class="sxs-lookup"><span data-stu-id="73ed9-109">CalendarEventArray</span></span>](calendareventarray.md)
  
[<span data-ttu-id="73ed9-110">CalendarEvent</span><span class="sxs-lookup"><span data-stu-id="73ed9-110">CalendarEvent</span></span>](calendarevent.md)
  
```xml
<CalendarEvent>
   <StartTime>...</StartTime>
   <EndTime>...</EndTime>
   <BusyType>...</BusyType>
   <CalendarEventDetails>...</CalendarEventDetails>
</CalendarEvent>
```

 <span data-ttu-id="73ed9-111">**CalendarEvent**</span><span class="sxs-lookup"><span data-stu-id="73ed9-111">**CalendarEvent**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="73ed9-112">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="73ed9-112">Attributes and elements</span></span>

<span data-ttu-id="73ed9-113">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="73ed9-113">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="73ed9-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="73ed9-114">Attributes</span></span>

<span data-ttu-id="73ed9-115">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="73ed9-115">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="73ed9-116">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="73ed9-116">Child elements</span></span>

|<span data-ttu-id="73ed9-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="73ed9-117">**Element**</span></span>|<span data-ttu-id="73ed9-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="73ed9-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="73ed9-119">StartTime</span><span class="sxs-lookup"><span data-stu-id="73ed9-119">StartTime</span></span>](starttime.md) <br/> |<span data-ttu-id="73ed9-120">Representa el inicio de un evento de calendario.</span><span class="sxs-lookup"><span data-stu-id="73ed9-120">Represents the start of a calendar event.</span></span> <span data-ttu-id="73ed9-121">Se trata de un elemento secundario obligatorio.</span><span class="sxs-lookup"><span data-stu-id="73ed9-121">This is a required child element.</span></span>  <br/> |
|[<span data-ttu-id="73ed9-122">EndTime</span><span class="sxs-lookup"><span data-stu-id="73ed9-122">EndTime</span></span>](endtime.md) <br/> |<span data-ttu-id="73ed9-123">Representa el final de un evento de calendario.</span><span class="sxs-lookup"><span data-stu-id="73ed9-123">Represents the end of a calendar event.</span></span> <span data-ttu-id="73ed9-124">Se trata de un elemento secundario obligatorio.</span><span class="sxs-lookup"><span data-stu-id="73ed9-124">This is a required child element.</span></span>  <br/> |
|[<span data-ttu-id="73ed9-125">BusyType</span><span class="sxs-lookup"><span data-stu-id="73ed9-125">BusyType</span></span>](busytype.md) <br/> |<span data-ttu-id="73ed9-126">Representa el conjunto de estado de disponibilidad para un evento de calendario.</span><span class="sxs-lookup"><span data-stu-id="73ed9-126">Represents the free/busy status set for a calendar event.</span></span> <span data-ttu-id="73ed9-127">Se trata de un elemento secundario obligatorio.</span><span class="sxs-lookup"><span data-stu-id="73ed9-127">This is a required child element.</span></span>  <br/> |
|[<span data-ttu-id="73ed9-128">CalendarEventDetails</span><span class="sxs-lookup"><span data-stu-id="73ed9-128">CalendarEventDetails</span></span>](calendareventdetails.md) <br/> |<span data-ttu-id="73ed9-129">Proporciona información adicional para un evento de calendario.</span><span class="sxs-lookup"><span data-stu-id="73ed9-129">Provides additional information for a calendar event.</span></span> <span data-ttu-id="73ed9-130">Se trata de un elemento secundario opcional.</span><span class="sxs-lookup"><span data-stu-id="73ed9-130">This is an optional child element.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="73ed9-131">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="73ed9-131">Parent elements</span></span>

|<span data-ttu-id="73ed9-132">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="73ed9-132">**Element**</span></span>|<span data-ttu-id="73ed9-133">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="73ed9-133">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="73ed9-134">CalendarEventArray</span><span class="sxs-lookup"><span data-stu-id="73ed9-134">CalendarEventArray</span></span>](calendareventarray.md) <br/> |<span data-ttu-id="73ed9-135">Contiene un conjunto de ocurrencias de elemento de calendario únicas que representan la disponibilidad del usuario solicitado.</span><span class="sxs-lookup"><span data-stu-id="73ed9-135">Contains a set of unique calendar item occurrences that represent the requested user's availability.</span></span>  <br/> <span data-ttu-id="73ed9-136">La siguiente es la expresión XPath 2,0 a este elemento:</span><span class="sxs-lookup"><span data-stu-id="73ed9-136">The following is the XPath 2.0 expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/CalendarEventArray` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="73ed9-137">Comentarios</span><span class="sxs-lookup"><span data-stu-id="73ed9-137">Remarks</span></span>

<span data-ttu-id="73ed9-138">Las horas de la cita y la reunión se devuelven en la zona horaria del cliente.</span><span class="sxs-lookup"><span data-stu-id="73ed9-138">The appointment and meeting times are returned in the time zone of the client.</span></span> <span data-ttu-id="73ed9-139">Todos los elementos secundarios se enumeran en la secuencia en que se producen.</span><span class="sxs-lookup"><span data-stu-id="73ed9-139">All the child elements are listed in the sequence in which they occur.</span></span> <span data-ttu-id="73ed9-140">El nivel de detalle proporcionado por este elemento depende de los permisos concedidos al solicitante.</span><span class="sxs-lookup"><span data-stu-id="73ed9-140">The level of detail provided by this element depends on the permissions granted to the requestor.</span></span>
  
<span data-ttu-id="73ed9-141">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="73ed9-141">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="73ed9-142">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="73ed9-142">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="73ed9-143">Namespace</span><span class="sxs-lookup"><span data-stu-id="73ed9-143">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="73ed9-144">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="73ed9-144">Schema Name</span></span>  <br/> |<span data-ttu-id="73ed9-145">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="73ed9-145">Types schema</span></span>  <br/> |
|<span data-ttu-id="73ed9-146">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="73ed9-146">Validation File</span></span>  <br/> |<span data-ttu-id="73ed9-147">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="73ed9-147">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="73ed9-148">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="73ed9-148">Can be Empty</span></span>  <br/> |<span data-ttu-id="73ed9-149">Falso</span><span class="sxs-lookup"><span data-stu-id="73ed9-149">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="73ed9-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="73ed9-150">See also</span></span>



[<span data-ttu-id="73ed9-151">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="73ed9-151">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="73ed9-152">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="73ed9-152">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="73ed9-153">Obtener disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="73ed9-153">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

