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
description: El elemento WorkingPeriod contiene los días y las horas de la semana de trabajo del usuario del buzón.
ms.openlocfilehash: 5c217169fb193d4bb6dae4e18570873d55de6127
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459682"
---
# <a name="workingperiod"></a><span data-ttu-id="9584f-103">WorkingPeriod</span><span class="sxs-lookup"><span data-stu-id="9584f-103">WorkingPeriod</span></span>

<span data-ttu-id="9584f-104">El elemento **WorkingPeriod** contiene los días y las horas de la semana de trabajo del usuario del buzón.</span><span class="sxs-lookup"><span data-stu-id="9584f-104">The **WorkingPeriod** element contains the work week days and hours of the mailbox user.</span></span> 
  
[<span data-ttu-id="9584f-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="9584f-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="9584f-106">FreeBusyResponseArray</span><span class="sxs-lookup"><span data-stu-id="9584f-106">FreeBusyResponseArray</span></span>](freebusyresponsearray.md)
  
[<span data-ttu-id="9584f-107">FreeBusyResponse</span><span class="sxs-lookup"><span data-stu-id="9584f-107">FreeBusyResponse</span></span>](freebusyresponse.md)
  
[<span data-ttu-id="9584f-108">FreeBusyView</span><span class="sxs-lookup"><span data-stu-id="9584f-108">FreeBusyView</span></span>](freebusyview.md)
  
[<span data-ttu-id="9584f-109">WorkingHours</span><span class="sxs-lookup"><span data-stu-id="9584f-109">WorkingHours</span></span>](workinghours-ex15websvcsotherref.md)
  
[<span data-ttu-id="9584f-110">WorkingPeriodArray</span><span class="sxs-lookup"><span data-stu-id="9584f-110">WorkingPeriodArray</span></span>](workingperiodarray.md)
  
[<span data-ttu-id="9584f-111">WorkingPeriod</span><span class="sxs-lookup"><span data-stu-id="9584f-111">WorkingPeriod</span></span>](workingperiod.md)
  
```xml
<WorkingPeriod>
   <DayOfWeek>...</DayOfWeek>
   <StartTimeInMinutes>...</StartTimeInMinutes>
   <EndTimeInMinutes>...</EndTimeInMinutes>
</WorkingPeriod>
```

 <span data-ttu-id="9584f-112">**WorkingPeriod**</span><span class="sxs-lookup"><span data-stu-id="9584f-112">**WorkingPeriod**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9584f-113">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="9584f-113">Attributes and elements</span></span>

<span data-ttu-id="9584f-114">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="9584f-114">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9584f-115">Atributos</span><span class="sxs-lookup"><span data-stu-id="9584f-115">Attributes</span></span>

<span data-ttu-id="9584f-116">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="9584f-116">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="9584f-117">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="9584f-117">Child elements</span></span>

|<span data-ttu-id="9584f-118">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="9584f-118">**Element**</span></span>|<span data-ttu-id="9584f-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9584f-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9584f-120">DayOfWeek (WorkingPeriod)</span><span class="sxs-lookup"><span data-stu-id="9584f-120">DayOfWeek (WorkingPeriod)</span></span>](dayofweek-workingperiod.md) <br/> |<span data-ttu-id="9584f-121">Contiene la lista de días laborables programados para el usuario del buzón.</span><span class="sxs-lookup"><span data-stu-id="9584f-121">Contains the list of working days scheduled for the mailbox user.</span></span>  <br/> |
|[<span data-ttu-id="9584f-122">StartTimeInMinutes</span><span class="sxs-lookup"><span data-stu-id="9584f-122">StartTimeInMinutes</span></span>](starttimeinminutes.md) <br/> |<span data-ttu-id="9584f-123">Representa el comienzo del día laborable de un usuario de buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="9584f-123">Represents the start of the working day for a mailbox user.</span></span>  <br/> |
|[<span data-ttu-id="9584f-124">EndTimeInMinutes</span><span class="sxs-lookup"><span data-stu-id="9584f-124">EndTimeInMinutes</span></span>](endtimeinminutes.md) <br/> |<span data-ttu-id="9584f-125">Representa el final del día laborable de un usuario de buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="9584f-125">Represents the end of the working day for a mailbox user.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="9584f-126">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="9584f-126">Parent elements</span></span>

|<span data-ttu-id="9584f-127">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="9584f-127">**Element**</span></span>|<span data-ttu-id="9584f-128">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9584f-128">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9584f-129">WorkingPeriodArray</span><span class="sxs-lookup"><span data-stu-id="9584f-129">WorkingPeriodArray</span></span>](workingperiodarray.md) <br/> |<span data-ttu-id="9584f-130">Contiene la información del período de trabajo del usuario del buzón.</span><span class="sxs-lookup"><span data-stu-id="9584f-130">Contains working period information for the mailbox user.</span></span>  <br/> <span data-ttu-id="9584f-131">La siguiente es la expresión XPath a este elemento:</span><span class="sxs-lookup"><span data-stu-id="9584f-131">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/WorkingPeriodArray` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9584f-132">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9584f-132">Remarks</span></span>

<span data-ttu-id="9584f-133">Todos los elementos secundarios se enumeran en la secuencia en que se producen.</span><span class="sxs-lookup"><span data-stu-id="9584f-133">All the child elements are listed in the sequence in which they occur.</span></span> <span data-ttu-id="9584f-134">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="9584f-134">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9584f-135">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="9584f-135">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9584f-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="9584f-136">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="9584f-137">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="9584f-137">Schema Name</span></span>  <br/> |<span data-ttu-id="9584f-138">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="9584f-138">Types schema</span></span>  <br/> |
|<span data-ttu-id="9584f-139">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="9584f-139">Validation File</span></span>  <br/> |<span data-ttu-id="9584f-140">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="9584f-140">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="9584f-141">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="9584f-141">Can be Empty</span></span>  <br/> |<span data-ttu-id="9584f-142">Falso</span><span class="sxs-lookup"><span data-stu-id="9584f-142">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9584f-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="9584f-143">See also</span></span>



[<span data-ttu-id="9584f-144">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="9584f-144">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="9584f-145">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="9584f-145">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="9584f-146">Obtener disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="9584f-146">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

