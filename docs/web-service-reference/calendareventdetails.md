---
title: CalendarEventDetails
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CalendarEventDetails
api_type:
- schema
ms.assetid: 2dca0192-b91b-4154-aa09-84da74e875e9
description: El elemento CalendarEventDetails proporciona información adicional acerca de un evento de calendario.
ms.openlocfilehash: 8df4f3ed4f66c7dcba00e1f0c5b0c383075da0a0
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763697"
---
# <a name="calendareventdetails"></a><span data-ttu-id="1050e-103">CalendarEventDetails</span><span class="sxs-lookup"><span data-stu-id="1050e-103">CalendarEventDetails</span></span>

<span data-ttu-id="1050e-104">El elemento **CalendarEventDetails** proporciona información adicional acerca de un evento de calendario.</span><span class="sxs-lookup"><span data-stu-id="1050e-104">The **CalendarEventDetails** element provides additional information about a calendar event.</span></span> 
  
[<span data-ttu-id="1050e-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="1050e-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="1050e-106">FreeBusyResponseArray</span><span class="sxs-lookup"><span data-stu-id="1050e-106">FreeBusyResponseArray</span></span>](freebusyresponsearray.md)
  
[<span data-ttu-id="1050e-107">FreeBusyResponse</span><span class="sxs-lookup"><span data-stu-id="1050e-107">FreeBusyResponse</span></span>](freebusyresponse.md)
  
[<span data-ttu-id="1050e-108">FreeBusyView</span><span class="sxs-lookup"><span data-stu-id="1050e-108">FreeBusyView</span></span>](freebusyview.md)
  
[<span data-ttu-id="1050e-109">CalendarEventArray</span><span class="sxs-lookup"><span data-stu-id="1050e-109">CalendarEventArray</span></span>](calendareventarray.md)
  
[<span data-ttu-id="1050e-110">CalendarEvent</span><span class="sxs-lookup"><span data-stu-id="1050e-110">CalendarEvent</span></span>](calendarevent.md)
  
[<span data-ttu-id="1050e-111">CalendarEventDetails</span><span class="sxs-lookup"><span data-stu-id="1050e-111">CalendarEventDetails</span></span>](calendareventdetails.md)
  
```xml
<CalendarEventDetails>
   <ID/>
   <Subject/>
   <Location/>
   <IsMeeting/>
   <IsRecurring/>
   <IsException/>
   <IsReminderSet/>
   <IsPrivate/>
</CalendarEventDetails>
```

 <span data-ttu-id="1050e-112">**CalendarEventDetails**</span><span class="sxs-lookup"><span data-stu-id="1050e-112">**CalendarEventDetails**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1050e-113">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="1050e-113">Attributes and elements</span></span>

<span data-ttu-id="1050e-114">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="1050e-114">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1050e-115">Atributos</span><span class="sxs-lookup"><span data-stu-id="1050e-115">Attributes</span></span>

<span data-ttu-id="1050e-116">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="1050e-116">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1050e-117">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="1050e-117">Child elements</span></span>

|<span data-ttu-id="1050e-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="1050e-118">**Element**</span></span>|<span data-ttu-id="1050e-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1050e-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1050e-120">ID</span><span class="sxs-lookup"><span data-stu-id="1050e-120">ID</span></span>](id.md) <br/> |<span data-ttu-id="1050e-121">Representa el identificador de entrada del elemento de calendario.</span><span class="sxs-lookup"><span data-stu-id="1050e-121">Represents the entry ID of the calendar item.</span></span>  <br/> |
|[<span data-ttu-id="1050e-122">Asunto (CalendarEventDetails)</span><span class="sxs-lookup"><span data-stu-id="1050e-122">Subject (CalendarEventDetails)</span></span>](subject-calendareventdetails.md) <br/> |<span data-ttu-id="1050e-123">Representa al asunto del elemento de calendario.</span><span class="sxs-lookup"><span data-stu-id="1050e-123">Represents the subject of the calendar item.</span></span>  <br/> |
|[<span data-ttu-id="1050e-124">Ubicación (CalendarEventDetails)</span><span class="sxs-lookup"><span data-stu-id="1050e-124">Location (CalendarEventDetails)</span></span>](location-calendareventdetails.md) <br/> |<span data-ttu-id="1050e-125">Representa el campo de ubicación del elemento de calendario.</span><span class="sxs-lookup"><span data-stu-id="1050e-125">Represents the location field of the calendar item.</span></span>  <br/> |
|[<span data-ttu-id="1050e-126">IsMeeting (CalendarEventDetails)</span><span class="sxs-lookup"><span data-stu-id="1050e-126">IsMeeting (CalendarEventDetails)</span></span>](ismeeting-calendareventdetails.md) <br/> |<span data-ttu-id="1050e-127">Indica si el evento de calendario es una reunión o una cita.</span><span class="sxs-lookup"><span data-stu-id="1050e-127">Indicates whether the calendar event is a meeting or an appointment.</span></span>  <br/> |
|[<span data-ttu-id="1050e-128">IsRecurring (CalendarEventDetails)</span><span class="sxs-lookup"><span data-stu-id="1050e-128">IsRecurring (CalendarEventDetails)</span></span>](isrecurring-calendareventdetails.md) <br/> |<span data-ttu-id="1050e-129">Indica si el evento de calendario es una instancia de un elemento periódico del calendario o un elemento de calendario único.</span><span class="sxs-lookup"><span data-stu-id="1050e-129">Indicates whether the calendar event is an instance of a recurring calendar item or a single calendar item.</span></span>  <br/> |
|[<span data-ttu-id="1050e-130">IsException</span><span class="sxs-lookup"><span data-stu-id="1050e-130">IsException</span></span>](isexception.md) <br/> |<span data-ttu-id="1050e-131">Indica si se cambia una instancia de un elemento periódico del calendario desde el maestro.</span><span class="sxs-lookup"><span data-stu-id="1050e-131">Indicates whether an instance of a recurring calendar item is changed from the master.</span></span>  <br/> |
|[<span data-ttu-id="1050e-132">IsReminderSet</span><span class="sxs-lookup"><span data-stu-id="1050e-132">IsReminderSet</span></span>](isreminderset.md) <br/> |<span data-ttu-id="1050e-133">Indica si se ha establecido un aviso para el evento de calendario.</span><span class="sxs-lookup"><span data-stu-id="1050e-133">Indicates whether a reminder has been set for the calendar event.</span></span>  <br/> |
|[<span data-ttu-id="1050e-134">IsPrivate</span><span class="sxs-lookup"><span data-stu-id="1050e-134">IsPrivate</span></span>](isprivate.md) <br/> |<span data-ttu-id="1050e-135">Indica si el elemento de calendario es privado.</span><span class="sxs-lookup"><span data-stu-id="1050e-135">Indicates whether the calendar item is private.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="1050e-136">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="1050e-136">Parent elements</span></span>

|<span data-ttu-id="1050e-137">**Element**</span><span class="sxs-lookup"><span data-stu-id="1050e-137">**Element**</span></span>|<span data-ttu-id="1050e-138">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1050e-138">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1050e-139">CalendarEvent</span><span class="sxs-lookup"><span data-stu-id="1050e-139">CalendarEvent</span></span>](calendarevent.md) <br/> |<span data-ttu-id="1050e-140">Representa una repetición del elemento de calendario único.</span><span class="sxs-lookup"><span data-stu-id="1050e-140">Represents a unique calendar item occurrence.</span></span>  <br/> <span data-ttu-id="1050e-141">La siguiente es la expresión de XPath 2.0 para este elemento:</span><span class="sxs-lookup"><span data-stu-id="1050e-141">The following is the XPath 2.0 expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/CalendarEventArray/CalendarEvent[i]` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1050e-142">Notas</span><span class="sxs-lookup"><span data-stu-id="1050e-142">Remarks</span></span>

<span data-ttu-id="1050e-143">Todos los elementos secundarios se enumeran en la secuencia en la que se producen.</span><span class="sxs-lookup"><span data-stu-id="1050e-143">All the child elements are listed in the sequence in which they occur.</span></span> 
  
<span data-ttu-id="1050e-144">Si el elemento [IsPrivate](isprivate.md) es **true**, todos los demás elementos en el elemento [CalendarEventDetails](calendareventdetails.md) no se devuelven en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1050e-144">If the [IsPrivate](isprivate.md) element is **true**, all the other elements in the [CalendarEventDetails](calendareventdetails.md) element are not returned in the response.</span></span> 
  
<span data-ttu-id="1050e-145">La operación GetUserAvailability no devuelve información detallada autor de la llamada a menos que el autor de la llamada tiene acceso de lectura en el calendario del usuario de destino.</span><span class="sxs-lookup"><span data-stu-id="1050e-145">The GetUserAvailability operation does not return detailed caller information unless the caller has read access on the target user's calendar.</span></span> <span data-ttu-id="1050e-146">Puede establecer permisos de acceso mediante el Shell de administración de Exchange.</span><span class="sxs-lookup"><span data-stu-id="1050e-146">You can set access permissions by using the Exchange Management Shell.</span></span>
  
<span data-ttu-id="1050e-147">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="1050e-147">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1050e-148">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="1050e-148">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1050e-149">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="1050e-149">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="1050e-150">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="1050e-150">Schema Name</span></span>  <br/> |<span data-ttu-id="1050e-151">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="1050e-151">Types schema</span></span>  <br/> |
|<span data-ttu-id="1050e-152">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="1050e-152">Validation File</span></span>  <br/> |<span data-ttu-id="1050e-153">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="1050e-153">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="1050e-154">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="1050e-154">Can be Empty</span></span>  <br/> |<span data-ttu-id="1050e-155">False</span><span class="sxs-lookup"><span data-stu-id="1050e-155">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1050e-156">Ver también</span><span class="sxs-lookup"><span data-stu-id="1050e-156">See also</span></span>



[<span data-ttu-id="1050e-157">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="1050e-157">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="1050e-158">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="1050e-158">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="1050e-159">Obtención de disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="1050e-159">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

