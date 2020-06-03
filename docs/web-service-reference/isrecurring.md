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
description: El elemento IsRecurring indica si un elemento de calendario, una convocatoria de reunión o una tarea forman parte de un elemento periódico. Este elemento es de sólo lectura.
ms.openlocfilehash: 72c71c1955b69f1c0df855ce4bd0ed02d4c89122
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526490"
---
# <a name="isrecurring"></a><span data-ttu-id="5c068-104">IsRecurring</span><span class="sxs-lookup"><span data-stu-id="5c068-104">IsRecurring</span></span>

<span data-ttu-id="5c068-105">El elemento **IsRecurring** indica si un elemento de calendario, una convocatoria de reunión o una tarea forman parte de un elemento periódico.</span><span class="sxs-lookup"><span data-stu-id="5c068-105">The **IsRecurring** element indicates whether a calendar item, meeting request, or task is part of a recurring item.</span></span> <span data-ttu-id="5c068-106">Este elemento es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="5c068-106">This element is read-only.</span></span> 
  
```xml
<IsRecurring/>
```

 <span data-ttu-id="5c068-107">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="5c068-107">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="5c068-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="5c068-108">Attributes and elements</span></span>

<span data-ttu-id="5c068-109">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="5c068-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5c068-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="5c068-110">Attributes</span></span>

<span data-ttu-id="5c068-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="5c068-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5c068-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="5c068-112">Child elements</span></span>

<span data-ttu-id="5c068-113">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="5c068-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="5c068-114">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="5c068-114">Parent elements</span></span>

|<span data-ttu-id="5c068-115">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="5c068-115">**Element**</span></span>|<span data-ttu-id="5c068-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5c068-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5c068-117">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="5c068-117">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="5c068-118">Representa un elemento de calendario de Exchange.</span><span class="sxs-lookup"><span data-stu-id="5c068-118">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="5c068-119">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="5c068-119">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="5c068-120">Representa una convocatoria de reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="5c068-120">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="5c068-121">Tarea</span><span class="sxs-lookup"><span data-stu-id="5c068-121">Task</span></span>](task.md) <br/> |<span data-ttu-id="5c068-122">Representa una tarea del almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="5c068-122">Represents a task in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="5c068-123">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="5c068-123">Text value</span></span>

<span data-ttu-id="5c068-124">Se requiere un valor de texto que representa un valor booleano.</span><span class="sxs-lookup"><span data-stu-id="5c068-124">A text value that represents a Boolean value is required.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5c068-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5c068-125">Remarks</span></span>

<span data-ttu-id="5c068-126">La siguiente tabla muestra cómo se establece la propiedad **IsRecurring** para distintos tipos de elemento de calendario para organizadores y asistentes, y para las convocatorias de reunión y las actualizaciones.</span><span class="sxs-lookup"><span data-stu-id="5c068-126">The following table shows how the **IsRecurring** property is set for different calendar item types for organizers and attendees and for meeting requests and updates.</span></span> 
  
|<span data-ttu-id="5c068-127">**Tipo CalendarItem**</span><span class="sxs-lookup"><span data-stu-id="5c068-127">**CalendarItem Type**</span></span>|<span data-ttu-id="5c068-128">**Organizador <br/> (IsRecurring)**</span><span class="sxs-lookup"><span data-stu-id="5c068-128">**Organizer  <br/> (IsRecurring)**</span></span>|<span data-ttu-id="5c068-129">**Asistente <br/> (IsRecurring)**</span><span class="sxs-lookup"><span data-stu-id="5c068-129">**Attendee  <br/> (IsRecurring)**</span></span>|<span data-ttu-id="5c068-130">**Convocatoria de reunión/actualización <br/> (IsRecurring)**</span><span class="sxs-lookup"><span data-stu-id="5c068-130">**Meeting request/update  <br/> (IsRecurring)**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="5c068-131">Ocurrencia única</span><span class="sxs-lookup"><span data-stu-id="5c068-131">Single Occurrence</span></span>  <br/> |<span data-ttu-id="5c068-132">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="5c068-132">**FALSE**</span></span> <br/> |<span data-ttu-id="5c068-133">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="5c068-133">**FALSE**</span></span> <br/> |<span data-ttu-id="5c068-134">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="5c068-134">**FALSE**</span></span> <br/> |
|<span data-ttu-id="5c068-135">Maestro recurrente</span><span class="sxs-lookup"><span data-stu-id="5c068-135">Recurring Master</span></span>  <br/> |<span data-ttu-id="5c068-136">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="5c068-136">**FALSE**</span></span> <br/> |<span data-ttu-id="5c068-137">**CASO**</span><span class="sxs-lookup"><span data-stu-id="5c068-137">**TRUE**</span></span> <br/> |<span data-ttu-id="5c068-138">**CASO**</span><span class="sxs-lookup"><span data-stu-id="5c068-138">**TRUE**</span></span> <br/> |
|<span data-ttu-id="5c068-139">Excepción periódica</span><span class="sxs-lookup"><span data-stu-id="5c068-139">Recurring Exception</span></span>  <br/> |<span data-ttu-id="5c068-140">**CASO**</span><span class="sxs-lookup"><span data-stu-id="5c068-140">**TRUE**</span></span> <br/> |<span data-ttu-id="5c068-141">**CASO**</span><span class="sxs-lookup"><span data-stu-id="5c068-141">**TRUE**</span></span> <br/> |<span data-ttu-id="5c068-142">**CASO**</span><span class="sxs-lookup"><span data-stu-id="5c068-142">**TRUE**</span></span> <br/> |
   
<span data-ttu-id="5c068-143">El valor de la propiedad **IsRecurring** que se establece para los elementos de calendario maestro periódicos para el organizador es incorrecto; Este valor debe establecerse en **true**.</span><span class="sxs-lookup"><span data-stu-id="5c068-143">The **IsRecurring** property value that is set for recurring master calendar items for the organizer is incorrect; this value should be set to **TRUE**.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="5c068-144">La operación GetUserAvailability también tiene un elemento [IsRecurring (CalendarEventDetails)](isrecurring-calendareventdetails.md) .</span><span class="sxs-lookup"><span data-stu-id="5c068-144">The GetUserAvailability operation also has an [IsRecurring (CalendarEventDetails)](isrecurring-calendareventdetails.md) element.</span></span> 
  
<span data-ttu-id="5c068-145">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="5c068-145">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5c068-146">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="5c068-146">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5c068-147">Namespace</span><span class="sxs-lookup"><span data-stu-id="5c068-147">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="5c068-148">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="5c068-148">Schema name</span></span>  <br/> |<span data-ttu-id="5c068-149">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="5c068-149">Types schema</span></span>  <br/> |
|<span data-ttu-id="5c068-150">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="5c068-150">Validation file</span></span>  <br/> |<span data-ttu-id="5c068-151">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="5c068-151">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="5c068-152">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="5c068-152">Can be empty</span></span>  <br/> |<span data-ttu-id="5c068-153">Falso</span><span class="sxs-lookup"><span data-stu-id="5c068-153">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5c068-154">Vea también</span><span class="sxs-lookup"><span data-stu-id="5c068-154">See also</span></span>



[<span data-ttu-id="5c068-155">TaskType. IsRecurring</span><span class="sxs-lookup"><span data-stu-id="5c068-155">TaskType.IsRecurring</span></span>](https://msdn.microsoft.com/library/ExchangeWebServices.TaskType.IsRecurring.aspx)
  
[<span data-ttu-id="5c068-156">CalendarEventDetails. IsRecurring</span><span class="sxs-lookup"><span data-stu-id="5c068-156">CalendarEventDetails.IsRecurring</span></span>](https://msdn.microsoft.com/library/ExchangeWebServices.CalendarEventDetails.IsRecurring.aspx)
  
[<span data-ttu-id="5c068-157">CalendarItemType. IsRecurring</span><span class="sxs-lookup"><span data-stu-id="5c068-157">CalendarItemType.IsRecurring</span></span>](https://msdn.microsoft.com/library/ExchangeWebServices.CalendarItemType.IsRecurring.aspx)
  
[<span data-ttu-id="5c068-158">MeetingRequestMessageType. IsRecurring</span><span class="sxs-lookup"><span data-stu-id="5c068-158">MeetingRequestMessageType.IsRecurring</span></span>](https://msdn.microsoft.com/library/ExchangeWebServices.MeetingRequestMessageType.IsRecurring.aspx)
  
[<span data-ttu-id="5c068-159">CalendarItemType.IsRecurringSpecified</span><span class="sxs-lookup"><span data-stu-id="5c068-159">CalendarItemType.IsRecurringSpecified</span></span>](https://msdn.microsoft.com/library/ExchangeWebServices.CalendarItemType.IsRecurringSpecified.aspx)
  
[<span data-ttu-id="5c068-160">MeetingRequestMessageType.IsRecurringSpecified</span><span class="sxs-lookup"><span data-stu-id="5c068-160">MeetingRequestMessageType.IsRecurringSpecified</span></span>](https://msdn.microsoft.com/library/ExchangeWebServices.MeetingRequestMessageType.IsRecurringSpecified.aspx)
  
[<span data-ttu-id="5c068-161">TaskType. IsRecurringSpecified</span><span class="sxs-lookup"><span data-stu-id="5c068-161">TaskType.IsRecurringSpecified</span></span>](https://msdn.microsoft.com/library/ExchangeWebServices.TaskType.IsRecurringSpecified.aspx)


- [<span data-ttu-id="5c068-162">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="5c068-162">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

