---
title: CalendarEventArray
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CalendarEventArray
api_type:
- schema
ms.assetid: a00f7f56-d7f1-429d-ae02-97043718c864
description: El elemento CalendarEventArray contiene un conjunto de repeticiones de elemento de calendario únicos que representan la disponibilidad del usuario solicitado.
ms.openlocfilehash: 2e56b7b2b94e12401ba708dfca94101064d625e1
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763696"
---
# <a name="calendareventarray"></a><span data-ttu-id="53d03-103">CalendarEventArray</span><span class="sxs-lookup"><span data-stu-id="53d03-103">CalendarEventArray</span></span>

<span data-ttu-id="53d03-104">El elemento **CalendarEventArray** contiene un conjunto de repeticiones de elemento de calendario únicos que representan la disponibilidad del usuario solicitado.</span><span class="sxs-lookup"><span data-stu-id="53d03-104">The **CalendarEventArray** element contains a set of unique calendar item occurrences that represent the requested user's availability.</span></span> 
  
[<span data-ttu-id="53d03-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="53d03-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="53d03-106">FreeBusyResponseArray</span><span class="sxs-lookup"><span data-stu-id="53d03-106">FreeBusyResponseArray</span></span>](freebusyresponsearray.md)
  
[<span data-ttu-id="53d03-107">FreeBusyResponse</span><span class="sxs-lookup"><span data-stu-id="53d03-107">FreeBusyResponse</span></span>](freebusyresponse.md)
  
[<span data-ttu-id="53d03-108">FreeBusyView</span><span class="sxs-lookup"><span data-stu-id="53d03-108">FreeBusyView</span></span>](freebusyview.md)
  
[<span data-ttu-id="53d03-109">CalendarEventArray</span><span class="sxs-lookup"><span data-stu-id="53d03-109">CalendarEventArray</span></span>](calendareventarray.md)
  
```xml
<CalendarEventArray>
   <CalendarEvent>...</CalendarEvent>
</CalendarEventArray>
```

 <span data-ttu-id="53d03-110">**ArrayOfCalendarEvent**</span><span class="sxs-lookup"><span data-stu-id="53d03-110">**ArrayOfCalendarEvent**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="53d03-111">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="53d03-111">Attributes and elements</span></span>

<span data-ttu-id="53d03-112">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="53d03-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="53d03-113">Atributos</span><span class="sxs-lookup"><span data-stu-id="53d03-113">Attributes</span></span>

<span data-ttu-id="53d03-114">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="53d03-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="53d03-115">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="53d03-115">Child elements</span></span>

|<span data-ttu-id="53d03-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="53d03-116">**Element**</span></span>|<span data-ttu-id="53d03-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="53d03-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="53d03-118">CalendarEvent</span><span class="sxs-lookup"><span data-stu-id="53d03-118">CalendarEvent</span></span>](calendarevent.md) <br/> |<span data-ttu-id="53d03-119">Representa una repetición del elemento de calendario único.</span><span class="sxs-lookup"><span data-stu-id="53d03-119">Represents a unique calendar item occurrence.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="53d03-120">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="53d03-120">Parent elements</span></span>

|<span data-ttu-id="53d03-121">**Element**</span><span class="sxs-lookup"><span data-stu-id="53d03-121">**Element**</span></span>|<span data-ttu-id="53d03-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="53d03-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="53d03-123">FreeBusyView</span><span class="sxs-lookup"><span data-stu-id="53d03-123">FreeBusyView</span></span>](freebusyview.md) <br/> |<span data-ttu-id="53d03-124">Contiene la información de disponibilidad para un usuario específico.</span><span class="sxs-lookup"><span data-stu-id="53d03-124">Contains availability information for a specific user.</span></span>  <br/> <span data-ttu-id="53d03-125">La siguiente es la expresión de XPath 2.0 para este elemento:</span><span class="sxs-lookup"><span data-stu-id="53d03-125">The following is the XPath 2.0 expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="53d03-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="53d03-126">Remarks</span></span>

<span data-ttu-id="53d03-127">El nivel de detalle proporcionado por este elemento depende de los permisos concedidos para el solicitante.</span><span class="sxs-lookup"><span data-stu-id="53d03-127">The level of detail provided by this element depends on the permissions granted to the requestor.</span></span> <span data-ttu-id="53d03-128">Este elemento se incluye cuando el elemento [FreeBusyViewType](freebusyviewtype.md) está establecido en **FreeBusy**, **FreeBusyMerged**, **Detailed**o **DetailedMerged**.</span><span class="sxs-lookup"><span data-stu-id="53d03-128">This element is included when the [FreeBusyViewType](freebusyviewtype.md) element is set to **FreeBusy**, **FreeBusyMerged**, **Detailed**, or **DetailedMerged**.</span></span> <span data-ttu-id="53d03-129">Este elemento no incluye los elementos secundarios si no hay elementos de calendario están presentes en la ventana de tiempo solicitado.</span><span class="sxs-lookup"><span data-stu-id="53d03-129">This element does not include any child elements if no calendar items are present in the requested time window.</span></span> 
  
<span data-ttu-id="53d03-130">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="53d03-130">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="53d03-131">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="53d03-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="53d03-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="53d03-132">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="53d03-133">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="53d03-133">Schema Name</span></span>  <br/> |<span data-ttu-id="53d03-134">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="53d03-134">Types schema</span></span>  <br/> |
|<span data-ttu-id="53d03-135">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="53d03-135">Validation File</span></span>  <br/> |<span data-ttu-id="53d03-136">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="53d03-136">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="53d03-137">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="53d03-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="53d03-138">False</span><span class="sxs-lookup"><span data-stu-id="53d03-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="53d03-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="53d03-139">See also</span></span>



[<span data-ttu-id="53d03-140">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="53d03-140">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="53d03-141">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="53d03-141">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="53d03-142">Obtención de disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="53d03-142">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

