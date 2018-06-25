---
title: FreeBusyView
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FreeBusyView
api_type:
- schema
ms.assetid: cb18434f-5f41-4e05-a5ce-d921b2721a8c
description: El elemento FreeBusyView contiene la información de disponibilidad para un usuario específico.
ms.openlocfilehash: d0d603f18642a94e841a1a6bb8e8849aa6b5b273
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764718"
---
# <a name="freebusyview"></a><span data-ttu-id="8cd28-103">FreeBusyView</span><span class="sxs-lookup"><span data-stu-id="8cd28-103">FreeBusyView</span></span>

<span data-ttu-id="8cd28-104">El elemento **FreeBusyView** contiene la información de disponibilidad para un usuario específico.</span><span class="sxs-lookup"><span data-stu-id="8cd28-104">The **FreeBusyView** element contains availability information for a specific user.</span></span> 
  
[<span data-ttu-id="8cd28-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="8cd28-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="8cd28-106">FreeBusyResponseArray</span><span class="sxs-lookup"><span data-stu-id="8cd28-106">FreeBusyResponseArray</span></span>](freebusyresponsearray.md)
  
[<span data-ttu-id="8cd28-107">FreeBusyResponse</span><span class="sxs-lookup"><span data-stu-id="8cd28-107">FreeBusyResponse</span></span>](freebusyresponse.md)
  
[<span data-ttu-id="8cd28-108">FreeBusyView</span><span class="sxs-lookup"><span data-stu-id="8cd28-108">FreeBusyView</span></span>](freebusyview.md)
  
```xml
<FreeBusyView>
   <FreeBusyViewType>...</FreeBusyViewType>
   <MergedFreeBusy>...</MergedFreeBusy>
   <CalendarEventArray>...</CalendarEventArray>
   <WorkingHours>...</WorkingHours>
</FreeBusyView>
```

 <span data-ttu-id="8cd28-109">**FreeBusyView**</span><span class="sxs-lookup"><span data-stu-id="8cd28-109">**FreeBusyView**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="8cd28-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="8cd28-110">Attributes and elements</span></span>

<span data-ttu-id="8cd28-111">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="8cd28-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8cd28-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="8cd28-112">Attributes</span></span>

<span data-ttu-id="8cd28-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="8cd28-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="8cd28-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="8cd28-114">Child elements</span></span>

|<span data-ttu-id="8cd28-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="8cd28-115">**Element**</span></span>|<span data-ttu-id="8cd28-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8cd28-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8cd28-117">FreeBusyViewType</span><span class="sxs-lookup"><span data-stu-id="8cd28-117">FreeBusyViewType</span></span>](freebusyviewtype.md) <br/> |<span data-ttu-id="8cd28-118">Representa el tipo de información de disponibilidad solicitada devuelto en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8cd28-118">Represents the type of requested free/busy information returned in the response.</span></span>  <br/> |
|[<span data-ttu-id="8cd28-119">MergedFreeBusy</span><span class="sxs-lookup"><span data-stu-id="8cd28-119">MergedFreeBusy</span></span>](mergedfreebusy.md) <br/> |<span data-ttu-id="8cd28-120">Contiene la secuencia de libre/ocupado combinada de datos.</span><span class="sxs-lookup"><span data-stu-id="8cd28-120">Contains the merged free/busy stream of data.</span></span>  <br/> |
|[<span data-ttu-id="8cd28-121">CalendarEventArray</span><span class="sxs-lookup"><span data-stu-id="8cd28-121">CalendarEventArray</span></span>](calendareventarray.md) <br/> |<span data-ttu-id="8cd28-122">Contiene un conjunto de repeticiones de elemento de calendario únicos que representan la disponibilidad del usuario solicitado.</span><span class="sxs-lookup"><span data-stu-id="8cd28-122">Contains a set of unique calendar item occurrences that represent the requested user's availability.</span></span>  <br/> |
|[<span data-ttu-id="8cd28-123">WorkingHours</span><span class="sxs-lookup"><span data-stu-id="8cd28-123">WorkingHours</span></span>](workinghours-ex15websvcsotherref.md) <br/> |<span data-ttu-id="8cd28-124">Representa la configuración de zona horaria y horario laboral para el usuario del buzón solicitado.</span><span class="sxs-lookup"><span data-stu-id="8cd28-124">Represents the time zone settings and working hours for the requested mailbox user.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="8cd28-125">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="8cd28-125">Parent elements</span></span>

|<span data-ttu-id="8cd28-126">**Element**</span><span class="sxs-lookup"><span data-stu-id="8cd28-126">**Element**</span></span>|<span data-ttu-id="8cd28-127">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8cd28-127">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8cd28-128">FreeBusyResponse</span><span class="sxs-lookup"><span data-stu-id="8cd28-128">FreeBusyResponse</span></span>](freebusyresponse.md) <br/> |<span data-ttu-id="8cd28-129">Contiene la información de disponibilidad para un usuario de buzón único.</span><span class="sxs-lookup"><span data-stu-id="8cd28-129">Contains the free/busy information for a single mailbox user.</span></span>  <br/> <span data-ttu-id="8cd28-130">La siguiente es la expresión de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="8cd28-130">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8cd28-131">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8cd28-131">Remarks</span></span>

<span data-ttu-id="8cd28-132">Todos los elementos secundarios se enumeran en la secuencia en la que se producen.</span><span class="sxs-lookup"><span data-stu-id="8cd28-132">All the child elements are listed in the sequence in which they occur.</span></span> <span data-ttu-id="8cd28-133">El nivel de detalle proporcionado por este elemento depende de los permisos concedidos para el solicitante.</span><span class="sxs-lookup"><span data-stu-id="8cd28-133">The level of detail provided by this element depends on the permissions granted to the requestor.</span></span>
  
<span data-ttu-id="8cd28-134">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="8cd28-134">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8cd28-135">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="8cd28-135">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8cd28-136">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="8cd28-136">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="8cd28-137">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="8cd28-137">Schema Name</span></span>  <br/> |<span data-ttu-id="8cd28-138">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="8cd28-138">Types schema</span></span>  <br/> |
|<span data-ttu-id="8cd28-139">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="8cd28-139">Validation File</span></span>  <br/> |<span data-ttu-id="8cd28-140">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="8cd28-140">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="8cd28-141">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="8cd28-141">Can be Empty</span></span>  <br/> |<span data-ttu-id="8cd28-142">False</span><span class="sxs-lookup"><span data-stu-id="8cd28-142">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8cd28-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="8cd28-143">See also</span></span>



[<span data-ttu-id="8cd28-144">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="8cd28-144">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="8cd28-145">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="8cd28-145">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="8cd28-146">Obtención de disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="8cd28-146">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

