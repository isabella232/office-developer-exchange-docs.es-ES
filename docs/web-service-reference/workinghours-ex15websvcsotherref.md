---
title: WorkingHours
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- WorkingHours
api_type:
- schema
ms.assetid: bbe97777-f728-46c5-b2aa-565112c24f3a
description: El elemento WorkingHours representa la configuración de la zona horaria y el horario laboral del usuario del buzón solicitado.
ms.openlocfilehash: 9cb21e72f7024b96b4b5f252a8a3b85bb704e67c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44468344"
---
# <a name="workinghours"></a><span data-ttu-id="d0add-103">WorkingHours</span><span class="sxs-lookup"><span data-stu-id="d0add-103">WorkingHours</span></span>

<span data-ttu-id="d0add-104">El elemento **WorkingHours** representa la configuración de la zona horaria y el horario laboral del usuario del buzón solicitado.</span><span class="sxs-lookup"><span data-stu-id="d0add-104">The **WorkingHours** element represents the time zone settings and working hours for the requested mailbox user.</span></span> 
  
[<span data-ttu-id="d0add-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="d0add-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="d0add-106">FreeBusyResponseArray</span><span class="sxs-lookup"><span data-stu-id="d0add-106">FreeBusyResponseArray</span></span>](freebusyresponsearray.md)
  
[<span data-ttu-id="d0add-107">FreeBusyResponse</span><span class="sxs-lookup"><span data-stu-id="d0add-107">FreeBusyResponse</span></span>](freebusyresponse.md)
  
[<span data-ttu-id="d0add-108">FreeBusyView</span><span class="sxs-lookup"><span data-stu-id="d0add-108">FreeBusyView</span></span>](freebusyview.md)
  
[<span data-ttu-id="d0add-109">WorkingHours</span><span class="sxs-lookup"><span data-stu-id="d0add-109">WorkingHours</span></span>](workinghours-ex15websvcsotherref.md)
  
```xml
<WorkingHours>
   <TimeZone>...</TimeZone>
   <WorkingPeriodArray>...</WorkingPeriodArray>
</WorkingHours>
```

 <span data-ttu-id="d0add-110">**WorkingHours**</span><span class="sxs-lookup"><span data-stu-id="d0add-110">**WorkingHours**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d0add-111">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="d0add-111">Attributes and elements</span></span>

<span data-ttu-id="d0add-112">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="d0add-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d0add-113">Atributos</span><span class="sxs-lookup"><span data-stu-id="d0add-113">Attributes</span></span>

<span data-ttu-id="d0add-114">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="d0add-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d0add-115">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="d0add-115">Child elements</span></span>

|<span data-ttu-id="d0add-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="d0add-116">**Element**</span></span>|<span data-ttu-id="d0add-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d0add-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d0add-118">Zona horaria (disponibilidad)</span><span class="sxs-lookup"><span data-stu-id="d0add-118">TimeZone (Availability)</span></span>](timezone-availability.md) <br/> |<span data-ttu-id="d0add-119">Contiene los elementos que identifican la información de la zona horaria.</span><span class="sxs-lookup"><span data-stu-id="d0add-119">Contains elements that identify time zone information.</span></span> <span data-ttu-id="d0add-120">Este elemento también contiene información sobre la transición entre el horario estándar y el horario de verano.</span><span class="sxs-lookup"><span data-stu-id="d0add-120">This element also contains information about the transition between standard time and daylight saving time.</span></span> <span data-ttu-id="d0add-121">Este elemento es obligatorio si se usa el elemento **WorkingHours** .</span><span class="sxs-lookup"><span data-stu-id="d0add-121">This element is required if the **WorkingHours** element is used.</span></span>  <br/> |
|[<span data-ttu-id="d0add-122">WorkingPeriodArray</span><span class="sxs-lookup"><span data-stu-id="d0add-122">WorkingPeriodArray</span></span>](workingperiodarray.md) <br/> |<span data-ttu-id="d0add-123">Contiene la información del período de trabajo del usuario del buzón.</span><span class="sxs-lookup"><span data-stu-id="d0add-123">Contains working period information for the mailbox user.</span></span> <span data-ttu-id="d0add-124">Este elemento es obligatorio si se usa el elemento **WorkingHours** .</span><span class="sxs-lookup"><span data-stu-id="d0add-124">This element is required if the **WorkingHours** element is used.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d0add-125">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="d0add-125">Parent elements</span></span>

|<span data-ttu-id="d0add-126">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="d0add-126">**Element**</span></span>|<span data-ttu-id="d0add-127">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d0add-127">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d0add-128">FreeBusyView</span><span class="sxs-lookup"><span data-stu-id="d0add-128">FreeBusyView</span></span>](freebusyview.md) <br/> |<span data-ttu-id="d0add-129">Contiene la información de disponibilidad de un usuario específico.</span><span class="sxs-lookup"><span data-stu-id="d0add-129">Contains availability information for a specific user.</span></span>  <br/> <span data-ttu-id="d0add-130">La siguiente es la expresión XPath a este elemento:</span><span class="sxs-lookup"><span data-stu-id="d0add-130">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d0add-131">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d0add-131">Remarks</span></span>

<span data-ttu-id="d0add-132">Todos los elementos secundarios se enumeran en la secuencia en que se producen.</span><span class="sxs-lookup"><span data-stu-id="d0add-132">All the child elements are listed in the sequence in which they occur.</span></span> <span data-ttu-id="d0add-133">El nivel de detalle proporcionado por este elemento depende de los permisos concedidos al solicitante.</span><span class="sxs-lookup"><span data-stu-id="d0add-133">The level of detail provided by this element depends on the permissions granted to the requestor.</span></span>
  
<span data-ttu-id="d0add-134">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="d0add-134">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d0add-135">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="d0add-135">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d0add-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="d0add-136">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d0add-137">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="d0add-137">Schema Name</span></span>  <br/> |<span data-ttu-id="d0add-138">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="d0add-138">Types schema</span></span>  <br/> |
|<span data-ttu-id="d0add-139">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="d0add-139">Validation File</span></span>  <br/> |<span data-ttu-id="d0add-140">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="d0add-140">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d0add-141">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="d0add-141">Can be Empty</span></span>  <br/> |<span data-ttu-id="d0add-142">Falso</span><span class="sxs-lookup"><span data-stu-id="d0add-142">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d0add-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="d0add-143">See also</span></span>



[<span data-ttu-id="d0add-144">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="d0add-144">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="d0add-145">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="d0add-145">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="d0add-146">Obtener disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="d0add-146">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

