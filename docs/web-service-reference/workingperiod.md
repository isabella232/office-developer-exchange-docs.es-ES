---
title: WorkingPeriod
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- WorkingPeriod
api_type:
- schema
ms.assetid: 3b4e48af-9880-42b9-a0dc-dae7ac43c264
description: El elemento WorkingPeriod contiene la semana laboral días y las horas del usuario de buzón de correo.
ms.openlocfilehash: 0f2707bede5e49174ed62a35ba704e39c0c48e9f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19841020"
---
# <a name="workingperiod"></a><span data-ttu-id="27612-103">WorkingPeriod</span><span class="sxs-lookup"><span data-stu-id="27612-103">WorkingPeriod</span></span>

<span data-ttu-id="27612-104">El elemento **WorkingPeriod** contiene la semana laboral días y las horas del usuario de buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="27612-104">The **WorkingPeriod** element contains the work week days and hours of the mailbox user.</span></span> 
  
[<span data-ttu-id="27612-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="27612-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="27612-106">FreeBusyResponseArray</span><span class="sxs-lookup"><span data-stu-id="27612-106">FreeBusyResponseArray</span></span>](freebusyresponsearray.md)
  
[<span data-ttu-id="27612-107">FreeBusyResponse</span><span class="sxs-lookup"><span data-stu-id="27612-107">FreeBusyResponse</span></span>](freebusyresponse.md)
  
[<span data-ttu-id="27612-108">FreeBusyView</span><span class="sxs-lookup"><span data-stu-id="27612-108">FreeBusyView</span></span>](freebusyview.md)
  
[<span data-ttu-id="27612-109">WorkingHours</span><span class="sxs-lookup"><span data-stu-id="27612-109">WorkingHours</span></span>](workinghours-ex15websvcsotherref.md)
  
[<span data-ttu-id="27612-110">WorkingPeriodArray</span><span class="sxs-lookup"><span data-stu-id="27612-110">WorkingPeriodArray</span></span>](workingperiodarray.md)
  
[<span data-ttu-id="27612-111">WorkingPeriod</span><span class="sxs-lookup"><span data-stu-id="27612-111">WorkingPeriod</span></span>](workingperiod.md)
  
```xml
<WorkingPeriod>
   <DayOfWeek>...</DayOfWeek>
   <StartTimeInMinutes>...</StartTimeInMinutes>
   <EndTimeInMinutes>...</EndTimeInMinutes>
</WorkingPeriod>
```

 <span data-ttu-id="27612-112">**WorkingPeriod**</span><span class="sxs-lookup"><span data-stu-id="27612-112">**WorkingPeriod**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="27612-113">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="27612-113">Attributes and elements</span></span>

<span data-ttu-id="27612-114">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="27612-114">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="27612-115">Atributos</span><span class="sxs-lookup"><span data-stu-id="27612-115">Attributes</span></span>

<span data-ttu-id="27612-116">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="27612-116">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="27612-117">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="27612-117">Child elements</span></span>

|<span data-ttu-id="27612-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="27612-118">**Element**</span></span>|<span data-ttu-id="27612-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="27612-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="27612-120">DayOfWeek (WorkingPeriod)</span><span class="sxs-lookup"><span data-stu-id="27612-120">DayOfWeek (WorkingPeriod)</span></span>](dayofweek-workingperiod.md) <br/> |<span data-ttu-id="27612-121">Contiene la lista de días de trabajo programado para el usuario del buzón.</span><span class="sxs-lookup"><span data-stu-id="27612-121">Contains the list of working days scheduled for the mailbox user.</span></span>  <br/> |
|[<span data-ttu-id="27612-122">StartTimeInMinutes</span><span class="sxs-lookup"><span data-stu-id="27612-122">StartTimeInMinutes</span></span>](starttimeinminutes.md) <br/> |<span data-ttu-id="27612-123">Representa el inicio del día laborable para un usuario de buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="27612-123">Represents the start of the working day for a mailbox user.</span></span>  <br/> |
|[<span data-ttu-id="27612-124">EndTimeInMinutes</span><span class="sxs-lookup"><span data-stu-id="27612-124">EndTimeInMinutes</span></span>](endtimeinminutes.md) <br/> |<span data-ttu-id="27612-125">Representa el final del día laborable para un usuario de buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="27612-125">Represents the end of the working day for a mailbox user.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="27612-126">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="27612-126">Parent elements</span></span>

|<span data-ttu-id="27612-127">**Element**</span><span class="sxs-lookup"><span data-stu-id="27612-127">**Element**</span></span>|<span data-ttu-id="27612-128">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="27612-128">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="27612-129">WorkingPeriodArray</span><span class="sxs-lookup"><span data-stu-id="27612-129">WorkingPeriodArray</span></span>](workingperiodarray.md) <br/> |<span data-ttu-id="27612-130">Contiene información del período para el usuario del buzón de trabajar.</span><span class="sxs-lookup"><span data-stu-id="27612-130">Contains working period information for the mailbox user.</span></span>  <br/> <span data-ttu-id="27612-131">La siguiente es la expresión de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="27612-131">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/WorkingPeriodArray` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="27612-132">Comentarios</span><span class="sxs-lookup"><span data-stu-id="27612-132">Remarks</span></span>

<span data-ttu-id="27612-133">Todos los elementos secundarios se enumeran en la secuencia en la que se producen.</span><span class="sxs-lookup"><span data-stu-id="27612-133">All the child elements are listed in the sequence in which they occur.</span></span> <span data-ttu-id="27612-134">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="27612-134">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="27612-135">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="27612-135">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="27612-136">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="27612-136">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="27612-137">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="27612-137">Schema Name</span></span>  <br/> |<span data-ttu-id="27612-138">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="27612-138">Types schema</span></span>  <br/> |
|<span data-ttu-id="27612-139">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="27612-139">Validation File</span></span>  <br/> |<span data-ttu-id="27612-140">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="27612-140">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="27612-141">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="27612-141">Can be Empty</span></span>  <br/> |<span data-ttu-id="27612-142">False</span><span class="sxs-lookup"><span data-stu-id="27612-142">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="27612-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="27612-143">See also</span></span>



[<span data-ttu-id="27612-144">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="27612-144">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="27612-145">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="27612-145">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="27612-146">Obtención de disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="27612-146">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

