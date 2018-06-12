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
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764718"
---
# <a name="freebusyview"></a><span data-ttu-id="ce191-103">FreeBusyView</span><span class="sxs-lookup"><span data-stu-id="ce191-103">FreeBusyView</span></span>

<span data-ttu-id="ce191-104">El elemento **FreeBusyView** contiene la información de disponibilidad para un usuario específico.</span><span class="sxs-lookup"><span data-stu-id="ce191-104">The **FreeBusyView** element contains availability information for a specific user.</span></span> 
  
[<span data-ttu-id="ce191-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="ce191-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="ce191-106">FreeBusyResponseArray</span><span class="sxs-lookup"><span data-stu-id="ce191-106">FreeBusyResponseArray</span></span>](freebusyresponsearray.md)
  
[<span data-ttu-id="ce191-107">FreeBusyResponse</span><span class="sxs-lookup"><span data-stu-id="ce191-107">FreeBusyResponse</span></span>](freebusyresponse.md)
  
[<span data-ttu-id="ce191-108">FreeBusyView</span><span class="sxs-lookup"><span data-stu-id="ce191-108">FreeBusyView</span></span>](freebusyview.md)
  
```xml
<FreeBusyView>
   <FreeBusyViewType>...</FreeBusyViewType>
   <MergedFreeBusy>...</MergedFreeBusy>
   <CalendarEventArray>...</CalendarEventArray>
   <WorkingHours>...</WorkingHours>
</FreeBusyView>
```

 <span data-ttu-id="ce191-109">**FreeBusyView**</span><span class="sxs-lookup"><span data-stu-id="ce191-109">**FreeBusyView**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ce191-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="ce191-110">Attributes and elements</span></span>

<span data-ttu-id="ce191-111">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="ce191-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ce191-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="ce191-112">Attributes</span></span>

<span data-ttu-id="ce191-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="ce191-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ce191-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ce191-114">Child elements</span></span>

|<span data-ttu-id="ce191-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="ce191-115">**Element**</span></span>|<span data-ttu-id="ce191-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ce191-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ce191-117">FreeBusyViewType</span><span class="sxs-lookup"><span data-stu-id="ce191-117">FreeBusyViewType</span></span>](freebusyviewtype.md) <br/> |<span data-ttu-id="ce191-118">Representa el tipo de información de disponibilidad solicitada devuelto en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ce191-118">Represents the type of requested free/busy information returned in the response.</span></span>  <br/> |
|[<span data-ttu-id="ce191-119">MergedFreeBusy</span><span class="sxs-lookup"><span data-stu-id="ce191-119">MergedFreeBusy</span></span>](mergedfreebusy.md) <br/> |<span data-ttu-id="ce191-120">Contiene la secuencia de libre/ocupado combinada de datos.</span><span class="sxs-lookup"><span data-stu-id="ce191-120">Contains the merged free/busy stream of data.</span></span>  <br/> |
|[<span data-ttu-id="ce191-121">CalendarEventArray</span><span class="sxs-lookup"><span data-stu-id="ce191-121">CalendarEventArray</span></span>](calendareventarray.md) <br/> |<span data-ttu-id="ce191-122">Contiene un conjunto de repeticiones de elemento de calendario únicos que representan la disponibilidad del usuario solicitado.</span><span class="sxs-lookup"><span data-stu-id="ce191-122">Contains a set of unique calendar item occurrences that represent the requested user's availability.</span></span>  <br/> |
|[<span data-ttu-id="ce191-123">WorkingHours</span><span class="sxs-lookup"><span data-stu-id="ce191-123">WorkingHours</span></span>](workinghours-ex15websvcsotherref.md) <br/> |<span data-ttu-id="ce191-124">Representa la configuración de zona horaria y horario laboral para el usuario del buzón solicitado.</span><span class="sxs-lookup"><span data-stu-id="ce191-124">Represents the time zone settings and working hours for the requested mailbox user.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ce191-125">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="ce191-125">Parent elements</span></span>

|<span data-ttu-id="ce191-126">**Element**</span><span class="sxs-lookup"><span data-stu-id="ce191-126">**Element**</span></span>|<span data-ttu-id="ce191-127">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ce191-127">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ce191-128">FreeBusyResponse</span><span class="sxs-lookup"><span data-stu-id="ce191-128">FreeBusyResponse</span></span>](freebusyresponse.md) <br/> |<span data-ttu-id="ce191-129">Contiene la información de disponibilidad para un usuario de buzón único.</span><span class="sxs-lookup"><span data-stu-id="ce191-129">Contains the free/busy information for a single mailbox user.</span></span>  <br/> <span data-ttu-id="ce191-130">La siguiente es la expresión de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="ce191-130">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ce191-131">Notas</span><span class="sxs-lookup"><span data-stu-id="ce191-131">Remarks</span></span>

<span data-ttu-id="ce191-132">Todos los elementos secundarios se enumeran en la secuencia en la que se producen.</span><span class="sxs-lookup"><span data-stu-id="ce191-132">All the child elements are listed in the sequence in which they occur.</span></span> <span data-ttu-id="ce191-133">El nivel de detalle proporcionado por este elemento depende de los permisos concedidos para el solicitante.</span><span class="sxs-lookup"><span data-stu-id="ce191-133">The level of detail provided by this element depends on the permissions granted to the requestor.</span></span>
  
<span data-ttu-id="ce191-134">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="ce191-134">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ce191-135">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="ce191-135">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ce191-136">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="ce191-136">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ce191-137">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="ce191-137">Schema Name</span></span>  <br/> |<span data-ttu-id="ce191-138">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="ce191-138">Types schema</span></span>  <br/> |
|<span data-ttu-id="ce191-139">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="ce191-139">Validation File</span></span>  <br/> |<span data-ttu-id="ce191-140">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="ce191-140">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="ce191-141">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="ce191-141">Can be Empty</span></span>  <br/> |<span data-ttu-id="ce191-142">False</span><span class="sxs-lookup"><span data-stu-id="ce191-142">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ce191-143">Ver también</span><span class="sxs-lookup"><span data-stu-id="ce191-143">See also</span></span>



[<span data-ttu-id="ce191-144">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="ce191-144">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="ce191-145">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="ce191-145">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="ce191-146">Obtención de disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="ce191-146">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

