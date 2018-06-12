---
title: IsRecurring
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsRecurring
api_type:
- schema
ms.assetid: f4df6997-8d5b-4893-a4a5-fc7047e0a9c3
description: El elemento IsRecurring indica si un elemento de calendario, una convocatoria de reunión o una tarea forma parte de un elemento periódico. Este elemento es de sólo lectura.
ms.openlocfilehash: dfb0c28fe225792c7128409a8cf010627c624fe0
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836104"
---
# <a name="isrecurring"></a><span data-ttu-id="4d6e7-104">IsRecurring</span><span class="sxs-lookup"><span data-stu-id="4d6e7-104">IsRecurring</span></span>

<span data-ttu-id="4d6e7-105">El elemento **IsRecurring** indica si un elemento de calendario, una convocatoria de reunión o una tarea forma parte de un elemento periódico.</span><span class="sxs-lookup"><span data-stu-id="4d6e7-105">The **IsRecurring** element indicates whether a calendar item, meeting request, or task is part of a recurring item.</span></span> <span data-ttu-id="4d6e7-106">Este elemento es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="4d6e7-106">This element is read-only.</span></span> 
  
```xml
<IsRecurring/>
```

 <span data-ttu-id="4d6e7-107">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="4d6e7-107">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4d6e7-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="4d6e7-108">Attributes and elements</span></span>

<span data-ttu-id="4d6e7-109">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="4d6e7-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4d6e7-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="4d6e7-110">Attributes</span></span>

<span data-ttu-id="4d6e7-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="4d6e7-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4d6e7-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="4d6e7-112">Child elements</span></span>

<span data-ttu-id="4d6e7-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="4d6e7-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="4d6e7-114">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="4d6e7-114">Parent elements</span></span>

|<span data-ttu-id="4d6e7-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="4d6e7-115">**Element**</span></span>|<span data-ttu-id="4d6e7-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4d6e7-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4d6e7-117">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="4d6e7-117">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="4d6e7-118">Representa un elemento de calendario de Exchange.</span><span class="sxs-lookup"><span data-stu-id="4d6e7-118">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="4d6e7-119">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="4d6e7-119">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="4d6e7-120">Representa una convocatoria de reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="4d6e7-120">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="4d6e7-121">Tarea</span><span class="sxs-lookup"><span data-stu-id="4d6e7-121">Task</span></span>](task.md) <br/> |<span data-ttu-id="4d6e7-122">Representa una tarea en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="4d6e7-122">Represents a task in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="4d6e7-123">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="4d6e7-123">Text value</span></span>

<span data-ttu-id="4d6e7-124">Se requiere un valor de texto que representa un valor de tipo Boolean.</span><span class="sxs-lookup"><span data-stu-id="4d6e7-124">A text value that represents a Boolean value is required.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4d6e7-125">Notas</span><span class="sxs-lookup"><span data-stu-id="4d6e7-125">Remarks</span></span>

<span data-ttu-id="4d6e7-126">En la tabla siguiente se muestra cómo se establece la propiedad **IsRecurring** para tipos de elemento de calendario diferente para los organizadores y los asistentes y para las convocatorias de reunión y actualizaciones.</span><span class="sxs-lookup"><span data-stu-id="4d6e7-126">The following table shows how the **IsRecurring** property is set for different calendar item types for organizers and attendees and for meeting requests and updates.</span></span> 
  
|<span data-ttu-id="4d6e7-127">**Tipo de CalendarItem**</span><span class="sxs-lookup"><span data-stu-id="4d6e7-127">**CalendarItem Type**</span></span>|<span data-ttu-id="4d6e7-128">**Organizador de <br/> (IsRecurring)**</span><span class="sxs-lookup"><span data-stu-id="4d6e7-128">**Organizer  <br/> (IsRecurring)**</span></span>|<span data-ttu-id="4d6e7-129">**ATTENDEE <br/> (IsRecurring)**</span><span class="sxs-lookup"><span data-stu-id="4d6e7-129">**Attendee  <br/> (IsRecurring)**</span></span>|<span data-ttu-id="4d6e7-130">**Solicitud y actualización de la reunión <br/> (IsRecurring)**</span><span class="sxs-lookup"><span data-stu-id="4d6e7-130">**Meeting request/update  <br/> (IsRecurring)**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="4d6e7-131">Ocurrencia</span><span class="sxs-lookup"><span data-stu-id="4d6e7-131">Single Occurrence</span></span>  <br/> |<span data-ttu-id="4d6e7-132">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="4d6e7-132">**FALSE**</span></span> <br/> |<span data-ttu-id="4d6e7-133">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="4d6e7-133">**FALSE**</span></span> <br/> |<span data-ttu-id="4d6e7-134">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="4d6e7-134">**FALSE**</span></span> <br/> |
|<span data-ttu-id="4d6e7-135">Maestro periódico</span><span class="sxs-lookup"><span data-stu-id="4d6e7-135">Recurring Master</span></span>  <br/> |<span data-ttu-id="4d6e7-136">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="4d6e7-136">**FALSE**</span></span> <br/> |<span data-ttu-id="4d6e7-137">**ES TRUE**</span><span class="sxs-lookup"><span data-stu-id="4d6e7-137">**TRUE**</span></span> <br/> |<span data-ttu-id="4d6e7-138">**ES TRUE**</span><span class="sxs-lookup"><span data-stu-id="4d6e7-138">**TRUE**</span></span> <br/> |
|<span data-ttu-id="4d6e7-139">Excepción periódica</span><span class="sxs-lookup"><span data-stu-id="4d6e7-139">Recurring Exception</span></span>  <br/> |<span data-ttu-id="4d6e7-140">**ES TRUE**</span><span class="sxs-lookup"><span data-stu-id="4d6e7-140">**TRUE**</span></span> <br/> |<span data-ttu-id="4d6e7-141">**ES TRUE**</span><span class="sxs-lookup"><span data-stu-id="4d6e7-141">**TRUE**</span></span> <br/> |<span data-ttu-id="4d6e7-142">**ES TRUE**</span><span class="sxs-lookup"><span data-stu-id="4d6e7-142">**TRUE**</span></span> <br/> |
   
<span data-ttu-id="4d6e7-143">El valor de propiedad **IsRecurring** que se establece para los elementos periódicos de calendario principal para el organizador no es correcto; Este valor debe establecerse en **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="4d6e7-143">The **IsRecurring** property value that is set for recurring master calendar items for the organizer is incorrect; this value should be set to **TRUE**.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="4d6e7-144">La operación GetUserAvailability también tiene un elemento [IsRecurring (CalendarEventDetails)](isrecurring-calendareventdetails.md) .</span><span class="sxs-lookup"><span data-stu-id="4d6e7-144">The GetUserAvailability operation also has an [IsRecurring (CalendarEventDetails)](isrecurring-calendareventdetails.md) element.</span></span> 
  
<span data-ttu-id="4d6e7-145">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="4d6e7-145">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4d6e7-146">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="4d6e7-146">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4d6e7-147">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="4d6e7-147">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="4d6e7-148">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="4d6e7-148">Schema name</span></span>  <br/> |<span data-ttu-id="4d6e7-149">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="4d6e7-149">Types schema</span></span>  <br/> |
|<span data-ttu-id="4d6e7-150">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="4d6e7-150">Validation file</span></span>  <br/> |<span data-ttu-id="4d6e7-151">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="4d6e7-151">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="4d6e7-152">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="4d6e7-152">Can be empty</span></span>  <br/> |<span data-ttu-id="4d6e7-153">False</span><span class="sxs-lookup"><span data-stu-id="4d6e7-153">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4d6e7-154">Ver también</span><span class="sxs-lookup"><span data-stu-id="4d6e7-154">See also</span></span>



[<span data-ttu-id="4d6e7-155">TaskType.IsRecurring</span><span class="sxs-lookup"><span data-stu-id="4d6e7-155">TaskType.IsRecurring</span></span>](https://msdn.microsoft.com/library/ExchangeWebServices.TaskType.IsRecurring.aspx)
  
[<span data-ttu-id="4d6e7-156">CalendarEventDetails.IsRecurring</span><span class="sxs-lookup"><span data-stu-id="4d6e7-156">CalendarEventDetails.IsRecurring</span></span>](https://msdn.microsoft.com/library/ExchangeWebServices.CalendarEventDetails.IsRecurring.aspx)
  
[<span data-ttu-id="4d6e7-157">CalendarItemType.IsRecurring</span><span class="sxs-lookup"><span data-stu-id="4d6e7-157">CalendarItemType.IsRecurring</span></span>](https://msdn.microsoft.com/library/ExchangeWebServices.CalendarItemType.IsRecurring.aspx)
  
[<span data-ttu-id="4d6e7-158">MeetingRequestMessageType.IsRecurring</span><span class="sxs-lookup"><span data-stu-id="4d6e7-158">MeetingRequestMessageType.IsRecurring</span></span>](https://msdn.microsoft.com/library/ExchangeWebServices.MeetingRequestMessageType.IsRecurring.aspx)
  
[<span data-ttu-id="4d6e7-159">CalendarItemType.IsRecurringSpecified</span><span class="sxs-lookup"><span data-stu-id="4d6e7-159">CalendarItemType.IsRecurringSpecified</span></span>](https://msdn.microsoft.com/library/ExchangeWebServices.CalendarItemType.IsRecurringSpecified.aspx)
  
[<span data-ttu-id="4d6e7-160">MeetingRequestMessageType.IsRecurringSpecified</span><span class="sxs-lookup"><span data-stu-id="4d6e7-160">MeetingRequestMessageType.IsRecurringSpecified</span></span>](https://msdn.microsoft.com/library/ExchangeWebServices.MeetingRequestMessageType.IsRecurringSpecified.aspx)
  
[<span data-ttu-id="4d6e7-161">TaskType.IsRecurringSpecified</span><span class="sxs-lookup"><span data-stu-id="4d6e7-161">TaskType.IsRecurringSpecified</span></span>](https://msdn.microsoft.com/library/ExchangeWebServices.TaskType.IsRecurringSpecified.aspx)


- [<span data-ttu-id="4d6e7-162">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="4d6e7-162">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

