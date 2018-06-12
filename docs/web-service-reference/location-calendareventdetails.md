---
title: Ubicación (CalendarEventDetails)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Location
api_type:
- schema
ms.assetid: 883cce6e-66b8-4dbc-935c-83ef5100a953
description: El elemento Location representa el campo de ubicación del elemento de calendario.
ms.openlocfilehash: 3678bd94851633fcca9817c020106670b57d110c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836245"
---
# <a name="location-calendareventdetails"></a><span data-ttu-id="4b6eb-103">Ubicación (CalendarEventDetails)</span><span class="sxs-lookup"><span data-stu-id="4b6eb-103">Location (CalendarEventDetails)</span></span>

<span data-ttu-id="4b6eb-104">El elemento **Location** representa el campo de ubicación del elemento de calendario.</span><span class="sxs-lookup"><span data-stu-id="4b6eb-104">The **Location** element represents the location field of the calendar item.</span></span> 
  
[<span data-ttu-id="4b6eb-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="4b6eb-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="4b6eb-106">FreeBusyResponseArray</span><span class="sxs-lookup"><span data-stu-id="4b6eb-106">FreeBusyResponseArray</span></span>](freebusyresponsearray.md)
  
[<span data-ttu-id="4b6eb-107">FreeBusyResponse</span><span class="sxs-lookup"><span data-stu-id="4b6eb-107">FreeBusyResponse</span></span>](freebusyresponse.md)
  
[<span data-ttu-id="4b6eb-108">FreeBusyView</span><span class="sxs-lookup"><span data-stu-id="4b6eb-108">FreeBusyView</span></span>](freebusyview.md)
  
[<span data-ttu-id="4b6eb-109">CalendarEventArray</span><span class="sxs-lookup"><span data-stu-id="4b6eb-109">CalendarEventArray</span></span>](calendareventarray.md)
  
[<span data-ttu-id="4b6eb-110">CalendarEvent</span><span class="sxs-lookup"><span data-stu-id="4b6eb-110">CalendarEvent</span></span>](calendarevent.md)
  
[<span data-ttu-id="4b6eb-111">CalendarEventDetails</span><span class="sxs-lookup"><span data-stu-id="4b6eb-111">CalendarEventDetails</span></span>](calendareventdetails.md)
  
[<span data-ttu-id="4b6eb-112">Ubicación (CalendarEventDetails)</span><span class="sxs-lookup"><span data-stu-id="4b6eb-112">Location (CalendarEventDetails)</span></span>](location-calendareventdetails.md)
  
```xml
<Location/>
```

 <span data-ttu-id="4b6eb-113">**string**</span><span class="sxs-lookup"><span data-stu-id="4b6eb-113">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4b6eb-114">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="4b6eb-114">Attributes and elements</span></span>

<span data-ttu-id="4b6eb-115">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="4b6eb-115">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4b6eb-116">Atributos</span><span class="sxs-lookup"><span data-stu-id="4b6eb-116">Attributes</span></span>

<span data-ttu-id="4b6eb-117">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="4b6eb-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4b6eb-118">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="4b6eb-118">Child elements</span></span>

<span data-ttu-id="4b6eb-119">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="4b6eb-119">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="4b6eb-120">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="4b6eb-120">Parent elements</span></span>

|<span data-ttu-id="4b6eb-121">**Element**</span><span class="sxs-lookup"><span data-stu-id="4b6eb-121">**Element**</span></span>|<span data-ttu-id="4b6eb-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4b6eb-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4b6eb-123">CalendarEventDetails</span><span class="sxs-lookup"><span data-stu-id="4b6eb-123">CalendarEventDetails</span></span>](calendareventdetails.md) <br/> |<span data-ttu-id="4b6eb-124">Proporciona información adicional para un evento del calendario.</span><span class="sxs-lookup"><span data-stu-id="4b6eb-124">Provides additional information for a calendar event.</span></span>  <br/> <span data-ttu-id="4b6eb-125">La siguiente es la expresión de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="4b6eb-125">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/CalendarEventArray/CalendarEvent[i]/CalendarEventDetails` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="4b6eb-126">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="4b6eb-126">Text value</span></span>

<span data-ttu-id="4b6eb-127">Si este elemento se devuelve en la respuesta, es necesario un valor de texto.</span><span class="sxs-lookup"><span data-stu-id="4b6eb-127">A text value is required if this element is returned in the response.</span></span> <span data-ttu-id="4b6eb-128">Este elemento puede contener una cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="4b6eb-128">This element can contain an empty string.</span></span> <span data-ttu-id="4b6eb-129">Este elemento es opcional si se utiliza el elemento [CalendarEventDetails](calendareventdetails.md) .</span><span class="sxs-lookup"><span data-stu-id="4b6eb-129">This element is optional if the [CalendarEventDetails](calendareventdetails.md) element is used.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="4b6eb-130">Notas</span><span class="sxs-lookup"><span data-stu-id="4b6eb-130">Remarks</span></span>

<span data-ttu-id="4b6eb-131">Este elemento se asigna a una propiedad con nombre de MAPI PR_Location.</span><span class="sxs-lookup"><span data-stu-id="4b6eb-131">This element maps to a PR_Location MAPI named property.</span></span>
  
<span data-ttu-id="4b6eb-132">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="4b6eb-132">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4b6eb-133">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="4b6eb-133">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4b6eb-134">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="4b6eb-134">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="4b6eb-135">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="4b6eb-135">Schema Name</span></span>  <br/> |<span data-ttu-id="4b6eb-136">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="4b6eb-136">Types schema</span></span>  <br/> |
|<span data-ttu-id="4b6eb-137">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="4b6eb-137">Validation File</span></span>  <br/> |<span data-ttu-id="4b6eb-138">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="4b6eb-138">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="4b6eb-139">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="4b6eb-139">Can be Empty</span></span>  <br/> |<span data-ttu-id="4b6eb-140">False</span><span class="sxs-lookup"><span data-stu-id="4b6eb-140">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4b6eb-141">Ver también</span><span class="sxs-lookup"><span data-stu-id="4b6eb-141">See also</span></span>



[<span data-ttu-id="4b6eb-142">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="4b6eb-142">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="4b6eb-143">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="4b6eb-143">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="4b6eb-144">Obtención de disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="4b6eb-144">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

