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
description: El elemento WorkingHours representa la configuración de zona horaria y horario laboral para el usuario del buzón solicitado.
ms.openlocfilehash: c53779422b87adebed370a1ed88e4e91c7a2dcaf
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19841008"
---
# <a name="workinghours"></a><span data-ttu-id="8398c-103">WorkingHours</span><span class="sxs-lookup"><span data-stu-id="8398c-103">WorkingHours</span></span>

<span data-ttu-id="8398c-104">El elemento **WorkingHours** representa la configuración de zona horaria y horario laboral para el usuario del buzón solicitado.</span><span class="sxs-lookup"><span data-stu-id="8398c-104">The **WorkingHours** element represents the time zone settings and working hours for the requested mailbox user.</span></span> 
  
[<span data-ttu-id="8398c-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="8398c-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="8398c-106">FreeBusyResponseArray</span><span class="sxs-lookup"><span data-stu-id="8398c-106">FreeBusyResponseArray</span></span>](freebusyresponsearray.md)
  
[<span data-ttu-id="8398c-107">FreeBusyResponse</span><span class="sxs-lookup"><span data-stu-id="8398c-107">FreeBusyResponse</span></span>](freebusyresponse.md)
  
[<span data-ttu-id="8398c-108">FreeBusyView</span><span class="sxs-lookup"><span data-stu-id="8398c-108">FreeBusyView</span></span>](freebusyview.md)
  
[<span data-ttu-id="8398c-109">WorkingHours</span><span class="sxs-lookup"><span data-stu-id="8398c-109">WorkingHours</span></span>](workinghours-ex15websvcsotherref.md)
  
```xml
<WorkingHours>
   <TimeZone>...</TimeZone>
   <WorkingPeriodArray>...</WorkingPeriodArray>
</WorkingHours>
```

 <span data-ttu-id="8398c-110">**WorkingHours**</span><span class="sxs-lookup"><span data-stu-id="8398c-110">**WorkingHours**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="8398c-111">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="8398c-111">Attributes and elements</span></span>

<span data-ttu-id="8398c-112">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="8398c-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8398c-113">Atributos</span><span class="sxs-lookup"><span data-stu-id="8398c-113">Attributes</span></span>

<span data-ttu-id="8398c-114">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="8398c-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="8398c-115">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="8398c-115">Child elements</span></span>

|<span data-ttu-id="8398c-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="8398c-116">**Element**</span></span>|<span data-ttu-id="8398c-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8398c-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8398c-118">TimeZone (disponibilidad)</span><span class="sxs-lookup"><span data-stu-id="8398c-118">TimeZone (Availability)</span></span>](timezone-availability.md) <br/> |<span data-ttu-id="8398c-119">Contiene elementos que identifican la información de zona horaria.</span><span class="sxs-lookup"><span data-stu-id="8398c-119">Contains elements that identify time zone information.</span></span> <span data-ttu-id="8398c-120">Este elemento también contiene información sobre la transición entre la hora estándar y el horario de verano.</span><span class="sxs-lookup"><span data-stu-id="8398c-120">This element also contains information about the transition between standard time and daylight saving time.</span></span> <span data-ttu-id="8398c-121">Este elemento es necesario si se usa el elemento **WorkingHours** .</span><span class="sxs-lookup"><span data-stu-id="8398c-121">This element is required if the **WorkingHours** element is used.</span></span>  <br/> |
|[<span data-ttu-id="8398c-122">WorkingPeriodArray</span><span class="sxs-lookup"><span data-stu-id="8398c-122">WorkingPeriodArray</span></span>](workingperiodarray.md) <br/> |<span data-ttu-id="8398c-123">Contiene información del período para el usuario del buzón de trabajar.</span><span class="sxs-lookup"><span data-stu-id="8398c-123">Contains working period information for the mailbox user.</span></span> <span data-ttu-id="8398c-124">Este elemento es necesario si se usa el elemento **WorkingHours** .</span><span class="sxs-lookup"><span data-stu-id="8398c-124">This element is required if the **WorkingHours** element is used.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="8398c-125">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="8398c-125">Parent elements</span></span>

|<span data-ttu-id="8398c-126">**Element**</span><span class="sxs-lookup"><span data-stu-id="8398c-126">**Element**</span></span>|<span data-ttu-id="8398c-127">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8398c-127">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8398c-128">FreeBusyView</span><span class="sxs-lookup"><span data-stu-id="8398c-128">FreeBusyView</span></span>](freebusyview.md) <br/> |<span data-ttu-id="8398c-129">Contiene la información de disponibilidad para un usuario específico.</span><span class="sxs-lookup"><span data-stu-id="8398c-129">Contains availability information for a specific user.</span></span>  <br/> <span data-ttu-id="8398c-130">La siguiente es la expresión de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="8398c-130">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8398c-131">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8398c-131">Remarks</span></span>

<span data-ttu-id="8398c-132">Todos los elementos secundarios se enumeran en la secuencia en la que se producen.</span><span class="sxs-lookup"><span data-stu-id="8398c-132">All the child elements are listed in the sequence in which they occur.</span></span> <span data-ttu-id="8398c-133">El nivel de detalle proporcionado por este elemento depende de los permisos concedidos para el solicitante.</span><span class="sxs-lookup"><span data-stu-id="8398c-133">The level of detail provided by this element depends on the permissions granted to the requestor.</span></span>
  
<span data-ttu-id="8398c-134">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="8398c-134">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8398c-135">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="8398c-135">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8398c-136">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="8398c-136">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="8398c-137">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="8398c-137">Schema Name</span></span>  <br/> |<span data-ttu-id="8398c-138">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="8398c-138">Types schema</span></span>  <br/> |
|<span data-ttu-id="8398c-139">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="8398c-139">Validation File</span></span>  <br/> |<span data-ttu-id="8398c-140">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="8398c-140">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="8398c-141">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="8398c-141">Can be Empty</span></span>  <br/> |<span data-ttu-id="8398c-142">False</span><span class="sxs-lookup"><span data-stu-id="8398c-142">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8398c-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="8398c-143">See also</span></span>



[<span data-ttu-id="8398c-144">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="8398c-144">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="8398c-145">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="8398c-145">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="8398c-146">Obtención de disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="8398c-146">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

