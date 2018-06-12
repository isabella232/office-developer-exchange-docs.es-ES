---
title: IsMeeting (CalendarEventDetails)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsMeeting
api_type:
- schema
ms.assetid: dd6900e4-e4a3-471a-909d-7240ebec501b
description: El elemento IsMeeting indica si el evento de calendario es una reunión o una cita.
ms.openlocfilehash: f3f6e0cc5fbfe29e5a818d69794cbaf5b6855962
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836046"
---
# <a name="ismeeting-calendareventdetails"></a><span data-ttu-id="4eb8f-103">IsMeeting (CalendarEventDetails)</span><span class="sxs-lookup"><span data-stu-id="4eb8f-103">IsMeeting (CalendarEventDetails)</span></span>

<span data-ttu-id="4eb8f-104">El elemento **IsMeeting** indica si el evento de calendario es una reunión o una cita.</span><span class="sxs-lookup"><span data-stu-id="4eb8f-104">The **IsMeeting** element indicates whether the calendar event is a meeting or an appointment.</span></span> 
  
[<span data-ttu-id="4eb8f-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="4eb8f-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="4eb8f-106">FreeBusyResponseArray</span><span class="sxs-lookup"><span data-stu-id="4eb8f-106">FreeBusyResponseArray</span></span>](freebusyresponsearray.md)
  
[<span data-ttu-id="4eb8f-107">FreeBusyResponse</span><span class="sxs-lookup"><span data-stu-id="4eb8f-107">FreeBusyResponse</span></span>](freebusyresponse.md)
  
[<span data-ttu-id="4eb8f-108">FreeBusyView</span><span class="sxs-lookup"><span data-stu-id="4eb8f-108">FreeBusyView</span></span>](freebusyview.md)
  
[<span data-ttu-id="4eb8f-109">CalendarEventArray</span><span class="sxs-lookup"><span data-stu-id="4eb8f-109">CalendarEventArray</span></span>](calendareventarray.md)
  
[<span data-ttu-id="4eb8f-110">CalendarEvent</span><span class="sxs-lookup"><span data-stu-id="4eb8f-110">CalendarEvent</span></span>](calendarevent.md)
  
[<span data-ttu-id="4eb8f-111">CalendarEventDetails</span><span class="sxs-lookup"><span data-stu-id="4eb8f-111">CalendarEventDetails</span></span>](calendareventdetails.md)
  
[<span data-ttu-id="4eb8f-112">IsMeeting (CalendarEventDetails)</span><span class="sxs-lookup"><span data-stu-id="4eb8f-112">IsMeeting (CalendarEventDetails)</span></span>](ismeeting-calendareventdetails.md)
  
```xml
<IsMeeting>true or false</IsMeeting>
```

 <span data-ttu-id="4eb8f-113">**boolean**</span><span class="sxs-lookup"><span data-stu-id="4eb8f-113">**boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4eb8f-114">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="4eb8f-114">Attributes and elements</span></span>

<span data-ttu-id="4eb8f-115">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="4eb8f-115">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4eb8f-116">Atributos</span><span class="sxs-lookup"><span data-stu-id="4eb8f-116">Attributes</span></span>

<span data-ttu-id="4eb8f-117">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="4eb8f-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4eb8f-118">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="4eb8f-118">Child elements</span></span>

<span data-ttu-id="4eb8f-119">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="4eb8f-119">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="4eb8f-120">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="4eb8f-120">Parent elements</span></span>

|<span data-ttu-id="4eb8f-121">**Element**</span><span class="sxs-lookup"><span data-stu-id="4eb8f-121">**Element**</span></span>|<span data-ttu-id="4eb8f-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4eb8f-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4eb8f-123">CalendarEventDetails</span><span class="sxs-lookup"><span data-stu-id="4eb8f-123">CalendarEventDetails</span></span>](calendareventdetails.md) <br/> |<span data-ttu-id="4eb8f-124">Proporciona información adicional para un evento del calendario.</span><span class="sxs-lookup"><span data-stu-id="4eb8f-124">Provides additional information for a calendar event.</span></span>  <br/> <span data-ttu-id="4eb8f-125">La siguiente es la expresión de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="4eb8f-125">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/CalendarEventArray/CalendarEvent[i]/CalendarEventDetails` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="4eb8f-126">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="4eb8f-126">Text value</span></span>

<span data-ttu-id="4eb8f-127">Si este elemento se devuelve en la respuesta, es necesario un valor de texto.</span><span class="sxs-lookup"><span data-stu-id="4eb8f-127">A text value is required if this element is returned in the response.</span></span> <span data-ttu-id="4eb8f-128">Este elemento es necesario si se usa el elemento [CalendarEventDetails](calendareventdetails.md) .</span><span class="sxs-lookup"><span data-stu-id="4eb8f-128">This element is required if the [CalendarEventDetails](calendareventdetails.md) element is used.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="4eb8f-129">Notas</span><span class="sxs-lookup"><span data-stu-id="4eb8f-129">Remarks</span></span>

<span data-ttu-id="4eb8f-130">La diferencia entre una reunión y una cita es que una reunión es un elemento de calendario que incluye a los asistentes; una cita es un elemento de calendario que no incluye a los asistentes.</span><span class="sxs-lookup"><span data-stu-id="4eb8f-130">The difference between a meeting and an appointment is that a meeting is a calendar item that includes attendees; an appointment is a calendar item that does not include attendees.</span></span>
  
<span data-ttu-id="4eb8f-131">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="4eb8f-131">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4eb8f-132">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="4eb8f-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4eb8f-133">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="4eb8f-133">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="4eb8f-134">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="4eb8f-134">Schema Name</span></span>  <br/> |<span data-ttu-id="4eb8f-135">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="4eb8f-135">Types schema</span></span>  <br/> |
|<span data-ttu-id="4eb8f-136">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="4eb8f-136">Validation File</span></span>  <br/> |<span data-ttu-id="4eb8f-137">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="4eb8f-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="4eb8f-138">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="4eb8f-138">Can be Empty</span></span>  <br/> |<span data-ttu-id="4eb8f-139">False</span><span class="sxs-lookup"><span data-stu-id="4eb8f-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4eb8f-140">Ver también</span><span class="sxs-lookup"><span data-stu-id="4eb8f-140">See also</span></span>



[<span data-ttu-id="4eb8f-141">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="4eb8f-141">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="4eb8f-142">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="4eb8f-142">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="4eb8f-143">Obtención de disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="4eb8f-143">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

